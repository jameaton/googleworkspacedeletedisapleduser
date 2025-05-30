# 🧹 Google Workspace Suspended User Auto-Cleanup Script

This Google Apps Script automatically:

- Identifies **suspended but non-archived** users in your Google Workspace domain  
- Removes them from **all Google Groups**
- **Deletes** their user account
- Sends a **summary report** to a designated **Slack channel** every night at midnight

---

## 📦 Features

- 🧑‍💻 Written in Google Apps Script — no server hosting needed  
- 🔒 Skips archived users to preserve data for legal/compliance retention  
- 🔁 Runs automatically via a daily midnight trigger  
- 📣 Posts results to Slack via Incoming Webhook  
- 💬 Configurable domain and Slack channel  
- ✅ Super admin permissions required

---

## ⚙️ Setup Instructions

### 1. **Copy the Script**

Open [Google Apps Script](https://script.google.com/) and create a new project. Paste in the contents of `Code.gs`.

### 2. **Enable Admin SDK**

Go to **Extensions → Services** and add:

- `Admin SDK` (listed as `AdminDirectory`)

### 3. **Configure Your Domain and Webhook**

In the script, replace:

```javascript
const DOMAIN = 'airfinity.com';
const SLACK_WEBHOOK_URL = 'https://hooks.slack.com/services/XXXXXXXXX/XXXXXXXXX/XXXXXXXXXX';
