
# Multi-Account Management with SessionBox and MultiLogin

Effortlessly manage multiple accounts and sessions on the same website with advanced cookie isolation techniques and tools like SessionBox and MultiLogin. These solutions are tailored for anyone seeking seamless multi-login functionality.

## The Basics of Multi-Account Management

Modern websites use cookies to record unique user identifiers, enabling login-free browsing within a single session. However, in standard browsers (without private mode activated), you cannot log into multiple accounts on the same site simultaneously. This limitation arises because cookies belong to a specific domain name, and they are shared across all tabs within the same browser session.

To overcome this, you can isolate cookies per browser tab, creating independent user sessions.

### How Cookie Isolation Works

The core idea is to save cookies in `sessionStorage` and restore them automatically when the tab is displayed or before navigating to a new page. This approach ensures smooth transitions between multiple accounts without logging out.

Key considerations for implementation:
- Ensure a new user ID is created during login, even if a cookie already exists.
- Use the `SessionBox.close()` function to log out and delete session cookies securely.

#### Example (in PHP):
```php
session_name('COOKIE1');
$newid = session_create_id();
session_id($newid);
session_start();
```

## Client-Side Implementation

For managing cookies, this setup depends on the `js-cookie` library. Include the following scripts in your project:

```html
<script src="js.cookie.min.js"></script>
<script src="sessionbox.js"></script>
```

Declare all cookies used in the user session. Pre-existing cookies from the first connection should be indicated with the value `true`.

### Updating Cookies and iFrame Support

A cookie can be saved later (e.g., during a subsequent connection via iFrame) but must be declared beforehand:

```javascript
sessionbox.save('COOKIE2');
```

### Logging Out

To log out and delete cookies, use:

```javascript
sessionbox.close();
```

## Demo and Setup

Launch the demo using the following command:

```bash
./start.sh
```

Access the demo locally via:
[http://localhost:8000](http://localhost:8000)

---

## Why Choose Multilogin?

Break free from website restrictions with Multilogin—the pioneer in antidetect browsers with 9 years of industry experience. Manage multiple accounts seamlessly, automate actions effortlessly, and enjoy premium residential proxies covering 150+ countries. Avoid bans with unique browser profiles and advanced fingerprint customization. Whether you're into affiliate marketing, web scraping, or social media management, Multilogin gives you a competitive edge.

Ready to unlock the internet? Get started ☞ [1-st antidetect browser on the market](https://bit.ly/multIlogin)

---

### About the Author

For more technical insights, visit [Emmanuel ROECKER](https://www.rymetemmanuel.fr/emmanuel-roecker.html).
