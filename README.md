# Bantech AI Chatbot Integration Guides

Welcome to the official integration wiki for **Bantech AI Chatbot Platform**, including SDK setup, API usage, and embedding guides for web and desktop applications.

---

## ✨ Features

- **Multi-Platform Support** — Seamless integration across  
  [🌐 Web](./wiki/web.md), [📱 iOS](./wiki/ios.md), [🤖 Android](./wiki/android.md), and [💻 Desktop (Win & Mac)](./wiki/desktop.md).  
- **AI-Powered Conversations** — Smart, context-aware responses using the Bantech AI engine.  
- **Customizable Chat Interface** — Easily theme and style the chatbot to match your brand.  
- **Secure Authentication** — Supports both **guest sessions** and **authenticated users** via `cid` and `token`.  
- **Real-Time Messaging** — Built-in **WebSocket** and **Pusher** integration for instant communication.  
- **Conversation Memory** — Persistent user context across sessions and devices.  
- **Dashboard Integration** — Manage users, view analytics, and configure behavior from the [📊 Bantech Dashboard](https://ai-chatbot.bantech.ae).  
- **Widget & SDK Packages** — Ready-to-use [JS Widget](./wiki/web.md), [Swift SDK](./wiki/ios.md), and [Android Library](./wiki/android.md).  
- **Scalable Architecture** — API-first design with CORS-enabled chat endpoints like `chat.bantech.ae`.  
- **Enterprise-Ready** — Compliant with modern security and privacy standards.  


---

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
[Read the Web guide →](./wiki/web.md)

### 🍎 iOS Integration
[Read the iOS guide →](./wiki/ios.md)

### 📱 Android Integration
[Read the Android guide →](./wiki/android.md)

---

## 📬 Support
For technical support, contact **support@bantech.ae** or open an issue on the [GitHub repositories](https://github.com/orgs/bantech-ae/repositories).
