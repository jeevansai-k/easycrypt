# 🔐 Easy Crypt - Secure Password Manager

Easy Crypt is a sleek, modern, and highly secure Android application designed to help you generate, hash, and store your passwords with ease. Built with **Material 3 Design** and **Biometric Security**, it ensures your sensitive data stays private and accessible only to you.

---

## ✨ Features

*   **🎲 Password Generator:** Create strong, random passwords with customizable lengths and character sets (Numbers, Special Characters).
*   **🔗 Hashing Utility:** Securely hash any text using industry-standard algorithms (SHA-256, MD5, etc.).
*   **📂 Secure Storage:** Save your generated passwords or hashes locally using a high-performance **Room Database**.
*   **🛡️ Biometric Protection:** Accessing your saved passwords requires **Fingerprint, Face Unlock, or Device PIN** verification.
*   **🎨 Sleek UI:** Features a modern glassmorphism "Pill" tab layout, smooth transitions, and a dark-themed aesthetic.
*   **📋 One-Tap Copy:** Quickly copy your saved passwords to the clipboard from a beautiful, wide-format detail popup.

---

## 🛠️ How It Works

1.  **Generation:** The app uses `kotlin.random.Random` for non-deterministic password generation and `java.security.MessageDigest` for cryptographic hashing.
2.  **Authentication:** Leverages the `AndroidX Biometric` library to interface with the system's secure enclave for user identity verification.
3.  **Persistence:** Data is stored in an encrypted-at-rest-ready (optional extension) SQLite database via the **Room Persistence Library**.
4.  **UI/UX:** Uses **ViewBinding** for type-safe layout interactions and **Material Components** for a polished look.

---

## 📂 File Structure

```text
easycrypt/
├── app/
│   ├── src/
│   │   ├── main/
│   │   │   ├── java/com/example/easycrypt/
│   │   │   │   ├── MainActivity.kt        # Main Logic & Biometric Auth
│   │   │   │   ├── PasswordAdapter.kt     # RecyclerView Logic & Masking
│   │   │   │   ├── AppDatabase.kt         # Room Database Config
│   │   │   │   ├── PasswordEntry.kt       # Data Entity
│   │   │   │   └── PasswordDao.kt         # Database Operations
│   │   │   └── res/
│   │   │       ├── layout/                # UI XML Files
│   │   │       ├── values/                # Colors, Strings, Themes
│   │   │       └── mipmap/                # App Icons
│   └── build.gradle.kts                   # App-level dependencies
├── gradle/                                # Gradle Wrapper & Version Catalog
├── build.gradle.kts                       # Project-level build config
└── README.md                              # You are here!
```

---

## 🚀 GitHub Upload Guide

When sharing your project on GitHub, it is crucial to upload only the necessary source files and avoid build artifacts or sensitive keys.

### ✅ Files to UPLOAD (Include these):
*   `app/src/` (All your code and resources)
*   `app/build.gradle.kts`
*   `build.gradle.kts` (Root level)
*   `settings.gradle.kts`
*   `gradle/` folder (Includes `libs.versions.toml`)
*   `gradlew`, `gradlew.bat`
*   `.gitignore`
*   `README.md`

### ❌ Files to AVOID (Do NOT upload these):
*   `**/build/` folders (The compiled output)
*   `.gradle/` (Local gradle cache)
*   `local.properties` (Contains your local SDK path)
*   `*.jks` or `*.keystore` files ( **CRITICAL:** These are your private signing keys!)
*   `.idea/` (Android Studio specific user settings)
*   `*.apk` or `*.aab` (Binaries should be in "Releases", not the source tree)

---

## 📱 Screenshots

| Generate Tab | Saved Tab | Detail Popup |
| :---: | :---: | :---: |
| ![Generate](https://via.placeholder.com/200x400?text=Generate+UI) | ![Saved](https://via.placeholder.com/200x400?text=Saved+UI) | ![Detail](https://via.placeholder.com/200x400?text=Sleek+Popup) |

---

## 🛡️ License
This project is licensed under the MIT License - see the LICENSE file for details.
