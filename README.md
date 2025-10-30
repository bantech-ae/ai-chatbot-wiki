# Bantech AI Chatbot Integration Guides

Welcome to the official integration wiki for **Bantech AI Chatbot Platform**, including SDK setup, API usage, and embedding guides for web and desktop applications.

------------------------------------------------------------------------

## 📌 Prerequisites

Before integrating or consuming the SDK/API, ensure you have the following:

- 🔑 **Valid API key** — Obtain from your Bantech AI Chatbot **Dashboard**.  
- 🪪 **Customer ID (`cid`) and Auth Token (`token`)** — Generated via your backend integration.  
- 🌐 **API Base URL** — Must point to a backend domain authorized with CORS and in partnership with **Bantech** (e.g., `https://ai-chatbot.bantech.ae/api/`).  
- 🌐 **Chat Interface Base URL** — Must point to a CORS-authorized domain partnered with Bantech, such as: `https://chat.bantech.ae`
- ⚙️ **Socket App Key** — Required for real-time events (e.g., Pusher or Socket.IO).  
- 💻 **Platform Access** —  
  - iOS developers: GitHub access for the mobile SDK repo.  
  - Android developers: Access to the `chatlib` dependency (see Android docs).  
  - Staff members: Access to the dashboard or desktop (Win/Mac) app.  

> Ensure that your API and socket configurations are correctly linked to your Bantech project before deployment.

---

## 🧩 Integration Guides

Choose your platform below to get started:

### 🌐 Web Integration
[Read the Web guide →](./web.md)

### 🍎 iOS Integration
[Read the iOS guide →](./ios.md)

### 📱 Android Integration
[Read the Android guide →](./android.md)

---

## 📬 Support
For technical support, contact **support@bantech.ae** or open an issue on the [GitHub repositories](https://github.com/orgs/bantech-ae/repositories).
