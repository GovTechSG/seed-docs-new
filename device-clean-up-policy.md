# Device clean-up policy

The device clean-up policy applies exclusively to SEED users with TechPass IDs belonging to the TechPass AAD. You can identify a TechPass AAD account if your TechPass ID's domain is *techpass.gov.sg*. For example, *james_lee@techpass.gov.sg* is associated with the TechPass AAD.

> **Note**:
> 
> - The device clean-up policy does **not apply** if your TechPass ID belongs to the **WOG AAD**.
> - A TechPass ID in the WOG AAD typically aligns with your organizational email address, which is in the format *\<your_name\>@\<acronym for your agency\>.gov.sg*. For example, *peter_wilson@tech.gov.sg*.


### Purpose of the policy

The primary objective of this policy is to remove inactive device records from the Intune portal.

### What happens if my GMD is inactive?


If your TechPass ID belongs to the TechPass AAD and you have not logged into your GMD (the Internet Device onboarded to SEED) for 90 consecutive days, the GMD becomes inactive, and its records are soft deleted from the Intune portal.

It is essential to note that when your device records are soft deleted, it does not wipe or retire the device. Instead, the device record is temporarily removed from Intune.

As a result, SEED administrators will not be able to access details such as the device's health status, and they can no longer manage it from the SEED Dashboard.


### Restore my device records on Intune

You can restore your device records on Intune by simply logging in to your GMD device the next time, provided that:

- Your TechPass account is still active.
- Your MDM certificate is still valid or within 180 days after its expiry.

## MDM certificate

When you onboard your Internet Device to SEED, you receive an MDM certificate that is valid for one year from the date of onboarding. The certificate is automatically renewed if you are logged in to your GMD when it expires.

> **Note**:
> 
> - Ensure that your TechPass account remains active.

If the MDM certificate expires, it can be automatically renewed by logging in to your device within 180 days from the expiration date. In such cases, re-onboarding your device to SEED is not required.

However, if more than 180 days have passed since the certificate expired, your device record is hard deleted, and access to SGTS products using that device is no longer possible.



