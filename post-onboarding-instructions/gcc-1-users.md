# Post onboarding instructions for GCC 1.0 users

This guide is for GCC 1.0 users who have successfully onboarded their Internet Devices to SEED. Once your device is onboarded to SEED, it becomes a Government Managed Device (GMD).

**Verification steps**:

1.	As only one VPN connection can be active at a time, go to the Cloudflare WARP icon on your GMD and toggle the **Connected** switch to **Paused**.

<kbd>![cloudflare-switch](../images/gcc-1-users/pause-connection.png ':size=75%')</kbd>

?> Cloudflare will automatically reconnect after three hours.

2. Launch and connect the GlobalProtect VPN client using your VPN ID and password.

<kbd>![globalprotect-vpn-client](../images/gcc-1-users/connect-to-globalprotect-vpn.png ':size=50%')</kbd>

3. Go to [myapplications.microsoft.com](https://myapplications.microsoft.com/) and log in with your Cloud ID and password.

4. Verify if you are able to access GCC 1.0 resources successfully.
![verify-gcc-resources](../images/gcc-1-users/gcc-1-resources.png)

?> **Note**: The above image is an example, and your actual GCC 1.0 resources may vary based on your account.

5. To verify if you are able to access the DEEP dashboard, click **Disconnect** in the GlobalProtect VPN client.

![disconnect](../images/gcc-1-users/disconnect.png ':size=75%')

6. Click the Cloudflare WARP icon and toggle the switch from **Paused** to **Connected**. If the Cloudflare WARP for Teams appears as shown below, it indicates that you are connected to Cloudflare WARP, allowing access the SEED dashboard.

![connected](../images/gcc-1-users/connected.png ':size=75%')

7. Go to [SEED dashboard](https://dashboard.seed.tech.gov.sg).

<kbd>![](../images/gcc-1-users/cloudflare-azure.png)</kbd>

8. Select **Azure AD TechPass Prod**.
9. When prompted, log in with your TechPass account.

<kbd>![](../images/gcc-1-users/techpass-login.png ':size=75%')</kbd>

?> If you are public officer, you may need to authenticate your WOG account first by using the one-time password code displayed under your SG Govt M365 profile in the Authenticator app.

10. On the **SEED** login page, click **Sign in with TechPass**.

<kbd>![](../images/gcc-1-users/deep-login-with-techpass.png)</kbd>

You will be directed to your SEED dashboard.

![](../images/gcc-1-users/seed-dashboard.png)
