# Configuration of common Developer CLI tools with Cloudflare WARP

This guide provides instructions on how to configure the following commonly used applications by software developers in Singapore Government agencies.

> **Note**:
>- The tools listed here are commonly used by software developers in Singapore Government agencies.
>- For configuring other applications or tools, refer to the [Cloudflare documentation](https://developers.cloudflare.com/cloudflare-one/connections/connect-devices/warp/install-cloudflare-cert).

- [Node.js and NPM](#nodejs-and-npm)
- [Docker](#docker)
- [AWS CLI](#aws-cli)
- [Golang](#golang)

> **Note**:
>- If you encounter any issues while using CLI tools and applications to access SGTS services, please raise a [support request](https://go.gov.sg/seed-techpass-support).
>- For all other issues unrelated to SGTS products, contact [Cloudflare Community Support Forums](https://support.cloudflare.com/hc/en-us)

## Node.js and NPM

Node.js and NPM use a hardcoded certificate store and require additional configuration to trust the Cloudflare Certificate.

**macOS users**

If you are using macOS and Zsh is your default terminal, execute the following commands:

```bash
mkdir -p "${HOME}/.config/.cloudflare"
curl -sSLj -o "${HOME}/.config/.cloudflare/Cloudflare_CA.pem" "https://developers.cloudflare.com/cloudflare-one/static/documentation/connections/Cloudflare_CA.pem"
echo 'export NODE_EXTRA_CA_CERTS="${HOME}/.config/.cloudflare/Cloudflare_CA.pem"' | tee -a "${HOME}/.zshrc"
source "${HOME}/.zshrc"
```

**Linux users**

If you are using Linux, Bash is your default terminal. Execute the following commands:

```bash
mkdir -p "${HOME}/.config/.cloudflare"
curl -sSLj -o "${HOME}/.config/.cloudflare/Cloudflare_CA.pem" "https://developers.cloudflare.com/cloudflare-one/static/documentation/connections/Cloudflare_CA.pem"
echo 'export NODE_EXTRA_CA_CERTS="${HOME}/.config/.cloudflare/Cloudflare_CA.pem"' | tee -a "${HOME}/.bashrc"
source "${HOME}/.bashrc"
```


## Docker

Docker for Desktop on macOS and Windows relies on virtual machines to host the Docker engine. To ensure compatibility with the Cloudflare Certificate, it's necessary to configure the Docker engine accordingly.

These instructions are provided to ensure the Docker engine functions seamlessly alongside Cloudflare WARP. However, it's important to note that this approach is not the recommended method for building production-ready Docker images.

For a more suitable solution, explore [SHIP-HATS CI/CD](https://www.ship.gov.sg/) for Docker image creation

- [Pull Docker images from a Docker image repository with Cloudflare Warp](#pull-docker-images-from-a-docker-image-repository-with-cloudflare-warp)
- [Connect operating system in your Docker container to Internet with Cloudflare Warp](#connect-operating-system-in-your-docker-container-to-internet-with-cloudflare-warp)

### Pull Docker images from a Docker image repository with Cloudflare Warp

To pull Docker images from a Docker image repository with Cloudflare Warp turned on, you need to configure the Docker engine on your host machine to trust the Cloudflare Certificate Authority (CA) certificate.

**To configure Docker engine on your host machine to trust Cloudflare Certificate Authority (CA) certificate**


1.	Locate the Docker engine configuration directory on your host machine. This directory is commonly named `.docker` and is typically located in your user home directory. Create the `.docker` directory if it does not exist.
2.	Locate the certificate directory for your Docker image repository. This is located in the `certs.d` directory in the `.docker` directory. Create the directory for your Docker Image repository if it does not exist in the `certs.d` directory.

For example, `mkdir -p ~/.docker/certs.d/registry-in.ship.gov.sg`.

3. Copy the Cloudflare CA certificate from https://developers.cloudflare.com/cloudflare-one/static/documentation/connections/Cloudflare_CA.pem and save it in the Docker Image repository certificate directory as ca-certificates.crt.
For example:

```
curl -sSLj -o ~/.docker/certs.d/registry-in.ship.gov.sg/ca-certificates.crt https://developers.cloudflare.com/cloudflare-one/static/documentation/connections/Cloudflare_CA.pem
```

### Connect operating system in your Docker container to Internet with Cloudflare Warp

To establish a connection between the operating system in your Docker container and the Internet with Cloudflare Warp enabled, you need to configure the operating system on the Docker container to trust the Cloudflare CA certificate.

**To configure operating system to trust Cloudflare certificate**

The Dockerfile snippet below demonstrates how to configure the operating system to trust the Cloudflare Certificate.

- Disable Cloudflare WARP and execute the `apt-get commands`. This step is required to correctly run the Dockerfile provided below.

> **Note**:
> The source of the following snippet is Ubuntu.

```
RUN \
    apt-get update && \
    apt-get install -y ca-certificates && \
    curl -sSLj -o "/etc/ssl/certs/Cloudflare_CA.pem" "https://developers.cloudflare.com/cloudflare-one/static/documentation/connections/Cloudflare_CA.pem" && \
    update-ca-certificates
```

## AWS CLI

AWS CLI utilises its own certificate store. It must be configured to trust the Cloudflare Certificate.

For Linux & macOS users:

1. Open your terminal.

2. Run the following command to navigate to the directory containing AWS CLI certificates:

```bash
mkdir -p "${HOME}/.config/.cloudflare"
curl -sSLj -o "${HOME}/.config/.cloudflare/Cloudflare_CA.pem" "https://developers.cloudflare.com/cloudflare-one/static/documentation/connections/Cloudflare_CA.pem"

# If you are using macOS, Zsh is likely to be your default terminal. If you are using Zsh, please run the following commands:
echo 'export AWS_CA_BUNDLE="${HOME}/.config/.cloudflare/Cloudflare_CA.pem"' | "tee -a ${HOME}/.zshrc"
source "${HOME}/.zshrc"

# If you are using Linux, Bash is likely to be your default terminal. If you are using Bash, please run the following commands:
echo 'export AWS_CA_BUNDLE="${HOME}/.config/.cloudflare/Cloudflare_CA.pem"' | "tee -a ${HOME}/.bashrc"
source "${HOME}/.bashrc"
```



## AWS SDK


### Javascript
```js
import { readFileSync } from “fs”;
import { Agent } from “https”;
import { config } from “aws-sdk”:

const certs = [ readFileSync(“path-to-cert”) ];

config.update({
        httpOptions: {
            agent: new Agent({
                ca: certs,
            }),
        },
    });
```


## Golang
Golang on macOS does not use the Big Sur DNS resolver by default, resulting in DNS resolution by golang binaries not being able to work with VPN clients such as OpenVPN or Cloudflare WARP. Please ensure that you build your golang binaries with cgo enabled.
