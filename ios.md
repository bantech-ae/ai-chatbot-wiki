# ChatBantechSDK

**ChatBantechSDK** is a Swift-based modular SDK designed to integrate a customizable chatbot interface into iOS applications. It provides a modern SwiftUI-based chat experience with web integration, background views, and clean configuration options.

## 🧩 Features

- SwiftUI-based modular components  
- Interactive chat interface with AI-style flow  
- WebView integration for backend connectivity  
- Fully customizable backgrounds and themes  
- Simple SDK configuration and initialization  

## 🛠 Installation

### 1. Swift Package Manager (SPM)

You can integrate **ChatBantechSDK** using Swift Package Manager:

1. In Xcode, open your project.
2. Go to **File → Add Packages...**
3. Enter the repository URL of your SDK (for example):
   ```
   https://github.com/bantech-ae/ai-chatbot-mobile-sdk-ios.git
   ```
4. Choose **Add Package** and select your app target.

Once added, import the SDK:

```swift
import ChatBantechSDK
```

## ⚙️ Configuration

Before using any view, initialize the SDK with your backend base URL.  
This must be done early in your app’s lifecycle, ideally in `AppDelegate` or `@main` App struct.

```swift
import ChatBantechSDK

@main
struct MyApp: App {
    init() {
        setupChatSDK()
    }
    
    func setupChatSDK() {
        Task {
            let config = ChatBantechConfgration(
                apiBaseUrl: "https://chat.emyaa.com",
                cid: "YOUR_CLIENT_ID",
                token: "YOUR_AUTH_TOKEN"
            )
            await ChatBantechSDK.shared.config(config)
        }
    }

    var body: some Scene {
        WindowGroup {
            ChatbotWelcomeView()
        }
    }
}
```

## 💬 Usage

You can start the chatbot interface by presenting the **ChatbotWelcomeView**:

```swift
import SwiftUI
import ChatBantechSDK

struct ContentView: View {
    @State private var isLoading = false

    var body: some View {
        BDIWebView(isLoading: $isLoading, error: .constant(nil))
    }
}
```

## 📦 Requirements

- iOS 16.0+  
- Swift 5.9+  
- Xcode 15+  

---

## 📬 Support
For technical support, contact **support@bantech.ae** or open an issue on the [GitHub repository](https://github.com/bantech-ae/ai-chatbot-mobile-sdk-ios).
