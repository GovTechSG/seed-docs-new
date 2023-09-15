# General FAQ

<details><summary>What data can I store on a GMD?</summary>

GMDs are to facilitate development work for developers to access GCC 2.0 and SGTS securely. Production and live data should **not be stored on GMDs**.

</details>

<details><summary>I have lost my GMD. What should I do?</summary>

1. Inform the manager-in-charge and operations manager and get an approval to delete the data from the lost device.
2. Raise a [service request][service-request] to notify the SEED team about the lost device.
3. In this service request, indicate if the device had any sensitive data to prioritise the remote wipe.

> **Note**: To wipe the device, the device needs to be powered on and be connected to the internet so it can receive the communication for it to be wiped.

4. Attach the approvals from your managers so that the SEED Administrator can take the required actions accordingly to prevent any data breach.

</details>
<details><summary>What happens when the security of a GMD is compromised?</summary>

Once the SEED team detects that a security of the device is compromised, it will contact the device owner to disconnect the affected device from the network. SEED proceeds to do a remote wipe, after getting the required consent and approval from the device owner and the manager-in-charge, respectively.

> **Note**: To wipe the device, the device needs to be powered on and be connected to the internet so it can receive the communication for it to be wiped.

</details>
<details><summary>What happens when a remote wipe is performed on a GMD?</summary>

Remote wipe in SEED is the feature where SEED administrator can remotely delete and destroy data on a device or system. Remote wipe is performed only if the device is stolen, lost or its security is compromised.

When remote wipe is performed on a device, all the data on it will be erased. For more information, refer to the [Terms and Policies][terms-and-policies].

> **Note**: To wipe the device, the device needs to be powered on and be connected to the internet so it can receive the communication for it to be wiped.

</details>
<details><summary>Is remote wipe done only on devices that belong to public sector agencies?</summary>

No, remote wipe will be done on any GMD which is lost or whose security is compromised to prevent data breach. However, remote wipe is performed only if the device is stolen, lost or its security is compromised. For more information, refer to the [Terms and Policies][terms-and-policies].

> **Note**: To wipe the device, the device needs to be powered on and be connected to the internet so it can receive the communication for it to be wiped.

</details>

<details><summary>Why am I prompted to turn on my system integrity protection on my macOS device?</summary>

  This is a policy requirement of the SEED team. System Integrity Protection is a security technology in OS X El Capitan and later that's designed to help prevent potentially malicious software from modifying protected files and folders on your macOS. System Integrity Protection restricts the root user account and limits the actions that the root user can perform on protected parts of the macOS.

 </details>


 <details>
   <summary>Why do I need to turn on File Vault encryption?</summary>

 File Vault encryption is needed to ensure device security and compliance.

 </details>

 <details><summary>Why does my device slowdown after onboarding to Microsoft Intune?</summary>

 SEED is designed to use **Microsoft Defender for Endpoint** to ensure device is free from malware, prevent and respond to advanced threats. If there is any other antivirus or anti-malware running simultaneously, it could compromise the performance of the operating system. To resolve this, disable or uninstall antivirus other than **Microsoft Defender for Endpoint**.

 </details>


<details><summary>Previously I had successfully onboarded my Internet Device to SEED, but now I received an email stating that I may not be able to access SEED-protected resources such as GCC 2.0 and SGTS products. What’s the reason, and what should I do?</summary>

Most likely, this indicates that we detected some issues with your device configuration for SEED. For example, your Microsoft Defender could be unhealthy. As it could pose a security risk, we revoked your access to SEED-protected resources.

If the issue could be resolved automatically, your access to SEED-protected resources will be restored and you will be notified via an email.

If this issue can't be automatically resolved, you will receive an email stating that you can't access SEED-protected resources. This email allows you to do one of the following based on your needs:

- [Offboard your device](https://docs.developer.tech.gov.sg/docs/security-suite-for-engineering-endpoint-devices/offboard-device/offboard-device-from-seed) if you no longer need to access SEED-protected resources.

- Submit an [incident request][service-request] to restore access to SEED-protected resources. Specify that your SEED access has been revoked due to device misconfiguration. This would allow us to process the ticket accordingly.


</details>

<details><summary>Why did I receive the successfully onboarded email again?</summary>

If you've received this email again, some or all the services that make your device SEED-compliant may have had configuration issues, causing you to temporarily lose access to SEED-protected resources .

When the configurations of the impacted services return to a healthy state, you will receive the successfully onboarded email indicating that you can access the SEED-protected resources again.

</details>


[techpass-documentation]: https://docs.developer.tech.gov.sg/docs/techpass-user-guide/#/
[terms-and-policies]: https://docs.developer.tech.gov.sg/docs/security-suite-for-engineering-endpoint-devices/#/additional-resources/terms-and-policies
[service-request]: https://go.gov.sg/seed-techpass-support
