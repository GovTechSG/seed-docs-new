# General FAQ

<details><summary>What data can I store on a GMD?</summary>

GMDs are intended to facilitate development work for accessing GCC 2.0 and SGTS securely. Do not store production or live data on GMDs.

</details>

<details><summary>I have lost my GMD. What should I do?</summary>

1. Notify your manager and operations manager to approve data deletion on the lost device.
2. Raise a [service request](https://go.gov.sg/seed-techpass-support) to notify the SEED team about the lost device.
3. Mention any sensitive data in the request to prioritise remote wiping.
4. Attach manager approvals for necessary actions to prevent data breaches.

</details>

<details><summary>What happens when the security of a GMD is compromised?</summary>

  When SEED detects a compromised device, it contacts the owner for disconnection. After obtaining owner and manager approvals, SEED performs a remote wipe.

> **Note**: 
> The device must be powered on and connected to the internet for remote wiping.

</details>
<details><summary>What happens when a remote wipe is performed on a GMD?</summary>

  Remote wipe erases all data on the device, performed only for theft, loss, or security compromise. For more information, refer to the [Terms and Policies](terms-and-policies).

</details>
<details><summary>Is remote wipe done only on devices that belong to public sector agencies?</summary>

  No, remote wipe applies to any lost or compromised GMD to prevent data breaches. For more information, refer to the [Terms and Policies](terms-and-policies).

</details>

<details><summary>Why am I prompted to turn on my system integrity protection on my macOS device?</summary>

  This is a SEED policy requirement. System Integrity Protection enhances macOS security and is designed to help prevent potentially malicious software from modifying protected files and folders on your macOS. System Integrity Protection restricts the root user account and limits the actions that the root user can perform on protected parts of the macOS.


 </details>


<details><summary>Why do I need to turn on File Vault encryption?</summary>

  FileVault encryption is essential to ensure device security and compliance.

 </details>

<details><summary>Why does my device slow down after onboarding to Microsoft Intune?</summary>

 SEED uses **Microsoft Defender for Endpoint** for security. Other antivirus software may impact performance. Disable or uninstall non-**Microsoft Defender for Endpoint** antivirus software.

 </details>

<details><summary>Previously, I successfully onboarded my Internet Device to SEED, but now I received an email indicating limited access to SEED-protected resources. Why, and what should I do? </summary>

This suggests SEED detected device configuration issues. For example, an unhealthy Microsoft Defender. For resolution:

- Offboard your device if access is no longer needed.

- Raise a [service request](https://go.gov.sg/seed-techpass-support) to restore access to SEED-protected resources. Specify that your SEED access was revoked due to device misconfiguration, allowing us to process the request accordingly.

</details>

<details><summary>Why did I receive the successfully onboarded email again?</summary>

Receiving this email again indicates that services ensuring SEED compliance may have had configuration issues, temporarily affecting SEED access.

</details>

<details><summary>Do I need to re-onboard my device to SEED after returning from a long leave?</summary>

If you belong to the TechPass AAD and your GMD (the Internet Device onboarded to SEED) has not been logged into for 90 consecutive days, the GMD becomes inactive, and its records are softly removed from the Intune portal.

It's important to understand that when your device records are softly removed, it does not perform a device wipe or retirement. Instead, the device record is temporarily taken out of Intune.

Consequently, SEED administrators will no longer have access to details such as the device's health status, and they won't be able to manage it from the SEED Dashboard.

For more information, refer to [device clean-up policy](device-clean-up-policy).

</details>
     


<details><summary>Will I receive any notification of MDM certificate expiration?</summary>


No, you will not receive any notification for this.

</details>

<details>
  <summary>Do I need to change my SEED onboarding password after a year, and what are the password requirements for it?</summary>
  
  Yes, you are required to change your SEED onboarding password after a year. The password requirements for SEED onboarding are as follows:

- It should contain at least 12 characters.
- It should not be the same as the previous three passwords.
- The same character cannot be used consecutively.
- It cannot have three sequential characters.
- It should contain at least one number and one alphabetic character.
</details>
