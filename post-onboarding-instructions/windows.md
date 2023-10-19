# Post onboarding instructions for Windows

After onboarding your Windows Internet Device to SEED, you need to enable Cloudflare WARP.

## Turn on Cloudflare WARP for Windows

!> Ensure that your device is not connected to any other VPN, as it might conflict with Cloudflare WARP.

**Activation steps**:

1. Open the Cloudflare WARP client from the Windows Taskbar. You will see the information page, followed by the privacy policy.

2. Click **Next**,then, **Accept** to agree to the Cloudflare’s privacy policy.

  ![cloudflare-for-teams](../images/cloudflare-warp-windows/cloudflare-for-teams.png ':size=50%')

3. When prompted to sign in, choose **Azure AD – TechPass Prod**.

  ![azure-ad-techpass-prod](../images/cloudflare-warp-windows/azure-ad-techpass-prod.png ':size=50%')

If you encounter an error stating that your user account is not found in the respective tenant, follow these instructions:

- Open a new browser tab
- Visit https://myaccount.microsoft.com
- Sign out of your current account
- Retry the action

4. Sign in using your TechPass login details.

  ![techpass-sign-in](../images/cloudflare-warp-macos/techpass-sign-in.png ':size=50%')

5. After successfully signing in, click **Open Cloudflare WARP app** to establish your WARP connection.

  When the device is connected to WARP, you should see the WARP Zero Trust in the connected state.
  
  ![after-signed-in](../images/cloudflare-warp-windows/after-signed-in.png ':size=50%')

6. Open Cloudflare WARP **Settings**, and ensure **Gateway with WARP** is selected.

WARP is now active, safeguarding your Internet connection.







