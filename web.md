
# 🌐 Web Widget Integration

This guide explains how to embed and configure **Bantech AI Chatbot Widget** on your website.  
With just a few lines of code, you can add an interactive AI assistant to your pages.

> ⚙️ **Before You Start:** Make sure your environment meets all [prerequisites](./README.md#-prerequisites).

---

## 🧩 Features

- 🧩 Plug-and-Play Widget – Add a chatbot to your website with a single script tag.
- 💬 AI-Powered Conversations – Engage users with natural, human-like chat experiences.
- ⚙️ Backend Integration Ready – Supports guest sessions and authenticated customers via secure API tokens.
- 🎨 Customizable Appearance – Match your brand colors, positions, and welcome messages.
- 🔄 Persistent Sessions – Automatically remembers users and previous chat history.
- 🌐 Lightweight & Fast – Built with modern JavaScript and ES Modules for instant load time.
- 🔒 Secure by Design – Uses HTTPS, token authentication, and CORS-safe communication.
- 📱 Responsive Layout – Optimized for all devices: desktop, tablet, and mobile.

---

## 🚀 Integration Guide

Follow these steps to add the AI Chatbot widget to your website:

### Step 1: Embed the Widget

Add the following snippet **just before the closing `</body>` tag** of your HTML file to display the AI Chatbot widget:

```html
<script type="module" src="https://cdn.widget.bantech.ae/v1.0.8/ai-chatbot-widget.js" async></script>
<div class="bantech-ai-chatbot-widget"></div>
```

> ✅ Once added, the chatbot will automatically appear on your website.

---

### Step 2: Set User Information

You can initialize the widget in two ways — depending on whether the user is a **guest** or a **registered customer**.

#### 🧑‍💻 Option 1: Guest Users
For guest visitors, you can provide basic user information using `data` attributes:

```html
<script type="module" src="https://cdn.widget.bantech.ae/v1.0.8/ai-chatbot-widget.js" async></script>
<div 
  class="bantech-ai-chatbot-widget"
  data-client-email="guest@bantech.ae"
  data-client-name="Guest User">
</div>
```

| Attribute | Description | Example |
|------------|-------------|----------|
| `data-client-email` | Guest’s email address | `data-client-email="guest@bantech.ae"` |
| `data-client-name` | Guest’s name or nickname | `data-client-name="Guest User"` |

---

#### 🔐 Option 2: Registered Customers
For authenticated users, use **unique identifiers** and **access tokens** generated via your backend integration.

```html
<script type="module" src="https://cdn.widget.bantech.ae/v1.0.8/ai-chatbot-widget.js" async></script>
<div 
  class="bantech-ai-chatbot-widget"
  data-client-uid="USER_ID"
  data-client-token="USER_ACCESS_TOKEN">
</div>
```

| Attribute | Description | Example |
|------------|-------------|----------|
| `data-client-uid` | Unique user ID returned by the `/api/customers` endpoint | `data-client-uid="a018cb2144094105a16b4992916b1a4a"` |
| `data-client-token` | Secure token associated with the user | `data-client-token="73886139\|wjhbxgcHdUXx0UFO22jMF..."` |

---

### Step 3: Backend Integration (Registered Customers)

To create and manage customer records, integrate with the following API endpoint from your backend:

**Endpoint:**  
```
POST /api/customers
```

**Example Request:**
```bash
curl -X POST https://ai-chatbot.bantech.ae/api/customers \
  -H "Content-Type: application/json" \
  -d '{
    "name": "John Doe",
    "email": "john@bantech.ae"
  }'
```

**Example Response:**
```json
{
  "id": "a018cb2144094105a16b4992916b1a4a",
  "token": "22886819|wjhbxgcHdUXx0UFO22jMF..."
}
```

Use these returned values (`id` and `token`) in your chatbot widget as shown in **Option 2**:

```html
<script type="module" src="https://cdn.widget.bantech.ae/v1.0.8/ai-chatbot-widget.js" async></script>
<div 
  class="bantech-ai-chatbot-widget"
  data-client-uid="USER_ID"
  data-client-token="USER_ACCESS_TOKEN">
</div>
```

---

### Step 4: You’re Done 🎉
Once integrated, the chatbot will automatically identify users, remember conversations, and personalize responses.  

---

## 📬 Support
For technical support, contact **support@bantech.ae** or open an issue on the [GitHub repository](https://github.com/bantech-ae/ai-chatbot-widget).
