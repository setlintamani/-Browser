
# Automation FAQ: Comprehensive Guide to Multilogin API and Features

## What Tasks Can Be Done Through Multilogin API Endpoints?

The **Multilogin API** provides extensive functionality to automate and manage your browser profiles and team operations effectively. Below are the key tasks you can perform:

### Key Features of Multilogin API

1. **User Management**:
   - Sign in, generate new tokens, and manage folder permissions.

2. **Browser Profile Management**:
   - Create, update, move, remove, restore, and clone profiles.

3. **Folder Management**:
   - Create, update, remove, and list folders for better organization.

4. **Profile Operations**:
   - Start and stop regular or quick browser profiles seamlessly.

5. **Proxy Information Management**:
   - Generate proxies, retrieve proxy details, and monitor current traffic balance.

6. **Cookie Management**:
   - Import, update, or create lists of cookies for advanced profile customization.

For a detailed list of API endpoints, visit the [Multilogin X API Documenter](https://documenter.getpostman.com/view/28533318/2s946h9Cv9). It includes script examples and detailed parameter explanations.

---

## Can Team Members Use API Endpoints?

Yes, team members in a workspace can utilize API endpoints. However, note that **subscription rate limits** are shared among all team members.

---

## Sample Automation Scripts for Puppeteer, Selenium, and Playwright

Multilogin provides sample automation scripts for popular frameworks:

- [Puppeteer Automation Example](https://multilogin.com/help/api/puppeteer-automation-example)
- [Selenium Automation Example](https://multilogin.com/help/api/selenium-automation-example)
- [Playwright Automation Example](https://multilogin.com/help/api/playwright-automation-example)

These examples streamline automation setups, saving you time and effort.

---

## How to Create Profiles in Bulk?

To create multiple profiles simultaneously, use the `times` parameter and specify the desired number of profiles (maximum 10 profiles at a time).

---

## Start URL: Setting Custom Launch Pages

You can set custom start URLs and additional links to open when launching a profile. Options include:

1. **In the User Interface (UI)**:
   - Go to profile settings under the "Essentials" tab to configure start URLs.
   
2. **In the API**:
   - Use the `custom_start_urls` parameter for both [regular](https://documenter.getpostman.com/view/28533318/2s946h9Cv9#f28d0fc7-9eb0-4e7e-84fe-1fb7a1ea1f9a) and [quick](https://documenter.getpostman.com/view/28533318/2s946h9Cv9#551806ee-4b2a-413f-bd07-44c2dfe31602) profiles.

> Websites cannot detect visits to [Multilogin's IP Checker Page](https://app.multiloginapp.com/WhatIsMyIP) due to the **same-origin policy**, which restricts access to cookies from other domains.

---

## How to Minimize Proxy Traffic Usage?

Excessive proxy data can impact performance. To optimize usage:
- Define a list of URLs where proxy traffic should not be routed.
- Use custom arguments to exclude these URLs from proxy usage, saving bandwidth and improving speed.

---

## Using Multilogin Proxies Outside Multilogin

Multilogin proxies can also be utilized outside the platform. Use the [Generate Proxy](https://documenter.getpostman.com/view/28533318/2s946h9Cv9#bef6f3b7-e77d-4129-9310-38af156cdc82) endpoint to:
- Select proxy type, location, and IP rotation duration.
- Generate credentials formatted as `host:port:username:password`.

Note: Proxy type (HTTP, HTTPS, SOCKS5) must be specified separately when necessary.

---

## Enhancing API Rate Limits

Higher rate limits can be achieved by generating an [Automation Token](https://documenter.getpostman.com/view/28533318/2s946h9Cv9#918a9c42-cb0f-497f-9bdd-a44d9d760be5) instead of using the regular token. This feature is available for **Solo, Team, and Custom Plan users**.

---

## Updating Fingerprints in Existing Profiles

Updating fingerprints is possible but not recommended, as it may lead to account bans. Use the [Profile Partial Update](https://documenter.getpostman.com/view/28533318/2s946h9Cv9#8b21ce69-3e09-4346-bf8c-61037df47e86) endpoint for Mimic profiles.

```json
"fingerprint": {
  "cmd_params": {
    "params": [
      {
        "flag": "disable-popup-blocking",
        "value": "True"
      }
    ]
  }
}
```

---

## Using Headless Browsers with Multilogin

Headless browser functionality is available for **Solo, Team, and Custom Plan users**. Starter Plan users do not have access to this feature.

---

## Local WebDriver Support

Multilogin browser profiles can only be controlled via a **remote WebDriver** when using Selenium, Puppeteer, or Playwright. Attempting to use a local WebDriver will result in automation failure.

---

## Multilogin: The Industry Leader in Antidetect Browsers

Break free from website restrictions with Multilogin—the pioneer in antidetect browsers with 9 years of industry experience. Manage multiple accounts seamlessly, automate actions effortlessly, and enjoy premium residential proxies covering 150+ countries. Avoid bans with unique browser profiles and advanced fingerprint customization. Whether you're into affiliate marketing, web scraping, or social media management, Multilogin gives you a competitive edge.

Ready to unlock the internet? Get started ☞ [1-st antidetect browser on the market](https://bit.ly/multIlogin)
