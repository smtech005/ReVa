<div align="center">

# 💰 ReVa

**Personal Finance & Inventory Manager for Bangladesh**

[![Version](https://img.shields.io/badge/version-5.0.0.0-emerald.svg)](https://github.com/smtech005/ReVa/releases)
[![Platform](https://img.shields.io/badge/platform-Android%20%7C%20Web-brightgreen.svg)](https://github.com/smtech005/ReVa/releases)
[![Target SDK](https://img.shields.io/badge/Target%20SDK-35%20(Android%2015)-blue.svg)](https://developer.android.com/about/versions/15)
[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
[![Firebase](https://img.shields.io/badge/Firebase-Firestore%20%7C%20Auth-orange.svg)](https://firebase.google.com/)

<img src="public/icon-512.png" alt="ReVa Logo" width="120" height="120">

### Track your money, snacks, and loans with precision

[Download APK v5.0.0.0](https://github.com/smtech005/ReVa/releases/download/v5.0.0.0/ReVa-v5.0.0.0.apk) · [Latest Release Notes](https://github.com/smtech005/ReVa/releases/tag/v5.0.0.0) · [Report Bug](https://github.com/smtech005/ReVa/issues) · [Request Feature](https://github.com/smtech005/ReVa/issues)

</div>

---

## 🚀 What's New in v5.0.0.0

ReVa **v5.0.0.0** is a major release featuring a full application-level rebranding, a native Android build with custom launcher icons, and a complete implementation of modern Android Material Design 3 UI/UX principles.

- **Native Android APK v5.0.0.0**: Compiled for Android 15 (Target SDK 35) with native Google Services Firebase configuration (`com.reva.app`).
- **In-App GitHub Release Update Engine**: Check for updates directly inside the app with interactive modal prompts and one-click APK installation.
- **Material Design 3 Bottom Navigation**: 5 distinct navigation tabs with smooth active pills and tactile haptic touch feedback.
- **Hardware Back Button Navigation**: Double-tap back within 2 seconds to safely exit on the dashboard; seamless stack navigation on sub-screens.
- **Inter-Location Fund Transfers**: Transfer balances between cash, bank, and mobile wallets with full cash note denomination tracking.
- **Account & Preferences Screen**: Complete profile customizer (avatar photo upload, display name editing), dark/light mode toggle, cloud sync, and cache management.
- **Offline Network Indicator**: Real-time status banner indicating offline mode with automated local cache synchronization upon reconnection.

---

## ✨ Features

### 💵 Money Management
- **Multiple Locations**: Track physical cash, mobile banking (**bKash**, **Nagad**, **Rocket**, **Upay**), bank accounts, and international accounts (**PayPal**, **Payoneer**, **Wise** in USD).
- **BDT Denominations**: Track physical cash note counts by denomination (৳5, ৳10, ৳20, ৳50, ৳100, ৳200, ৳500, ৳1000) with automatic total valuation.
- **Fund Transfers**: Transfer money between any two locations with full cash note breakdown for physical cash transfers.
- **Cash Expense with Change Tracking**: Pay with larger notes, record change received, and track net expense automatically.
- **Transaction History**: Real-time chronological logging with transaction type badges (Income, Expense, Transfer) and Bangladesh timezone (Asia/Dhaka) formatting.

### 🍿 Snack Inventory
- **Inventory Tracking**: Name, quantity, unit cost, and remaining quantity calculation.
- **Consumption Logging**: Record when snacks are consumed with custom notes and precise timestamps.
- **Low Stock Badges**: Visual alerts when inventory falls below minimum thresholds.
- **Safe Operations**: Validation preventing negative entries and protection against divide-by-zero errors.

### 💳 Loan Tracking
- **Lent & Borrowed**: Monitor funds you've lent out or borrowed from others.
- **Payment Installments**: Record partial repayments and track remaining balances in real time.
- **Status Indicators**: Dynamic status badges (Pending, Partial, Settled).
- **Due Date Reminders**: Keep track of repayment schedules with due dates.

### 📊 Financial Insights
- **Net Worth Overview**: Consolidated balance calculation across all accounts and physical cash.
- **Spending Visualizations**: Interactive category distribution charts powered by Recharts.
- **Asset Breakdown**: Real-time analysis of liquid cash, bank deposits, and snack inventory value.

### 👤 Account, Settings & In-App Updates
- **Profile Customization**: Upload and change your profile photo (persisted in offline storage) and edit your display name.
- **In-App Updates**: Built-in GitHub Releases updater that automatically checks for newer APK versions and guides installation.
- **Appearance**: One-tap toggle between Light Mode and Dark Mode.
- **Haptic Touch Engine**: Vibration feedback on navigation tabs, button presses, and confirmations.
- **Data & Sync Tools**: Force cloud sync with Firestore and clear local cache safely.

---

## 📱 Screenshots

| Home Dashboard | Money & Transfers | Snack Inventory | Account & Settings |
|:---:|:---:|:---:|:---:|
| Overview & Balances | Denominations & Transfer | Stock & Consumption | Profile & Updates |

---

## 📲 Installation

### Direct APK Download (Recommended)

1. Navigate to [ReVa v5.0.0.0 Release](https://github.com/smtech005/ReVa/releases/tag/v5.0.0.0).
2. Download **[`ReVa-v5.0.0.0.apk`](https://github.com/smtech005/ReVa/releases/download/v5.0.0.0/ReVa-v5.0.0.0.apk)**.
3. Open the downloaded file on your Android device and tap **Install** (allow *Install from Unknown Sources* if prompted).
4. Launch ReVa and enjoy!

---

## 🛠️ Build from Source

### Prerequisites

- **Node.js**: v18.0+ or v20.0+
- **Package Manager**: `pnpm` (recommended)
- **Java Development Kit**: OpenJDK 17 LTS
- **Android SDK**: Android SDK Platforms 34 / 35 with Build Tools 35.0.0
- **Gradle**: 8.13+ (or included Gradle wrapper)

### Step-by-Step Instructions

```bash
# 1. Clone the repository
git clone https://github.com/smtech005/ReVa.git
cd ReVa

# 2. Install dependencies
pnpm install

# 3. Build the static Next.js export for Capacitor
pnpm build:mobile

# 4. Sync web assets with the Android native project
npx cap sync android

# 5. Build the Android APK
cd android
./gradlew assembleDebug
```

The generated APK will be located at:
```text
android/app/build/outputs/apk/debug/app-debug.apk
```

---

## 🔧 Architecture & Tech Stack

| Component | Technology | Version | Purpose |
|:---|:---|:---:|:---|
| **Web Framework** | Next.js (App Router) | `16.0.10` | High-performance React application core |
| **Mobile Runtime** | Capacitor Android | `8.6.0` | Native Android bridge and platform APIs |
| **Language** | TypeScript / Java | `5.0` / `17` | End-to-end type safety and Android compilation |
| **Database** | Firebase Firestore | `v10+` | Real-time multi-device cloud database with local cache |
| **Authentication** | Firebase Auth | `v10+` | Secure email/password and OAuth authentication |
| **Styling** | Tailwind CSS / shadcn/ui | `v4` | Material Design 3 inspired responsive UI components |
| **Charts** | Recharts | `v2` | Financial data visualizations and spending trends |

### Capacitor Plugins

- `@capacitor/core`: Native runtime bridge.
- `@capacitor/app`: Native lifecycle events & hardware back button listener.
- `@capacitor/browser`: In-app browser for external links and APK downloads.
- `@capacitor/haptics`: Tactile vibration feedback.
- `@capacitor/network`: Real-time network connectivity monitoring.
- `@capacitor/preferences`: Encrypted offline preferences and profile storage.
- `@capacitor/status-bar`: Dynamic status bar color & overlay control.
- `@capacitor/splash-screen`: Native launch screen management.
- `@capacitor/keyboard`: Viewport resize management for on-screen keyboards.

---

## 📁 Repository Structure

```text
ReVa/
├── android/                          # Native Android Studio project
│   ├── app/
│   │   ├── google-services.json      # Firebase Android configuration
│   │   ├── src/main/AndroidManifest.xml
│   │   ├── src/main/java/com/reva/app/MainActivity.java
│   │   └── src/main/res/             # Launcher icons & drawables
│   └── build.gradle
├── app/                              # Next.js App Router
│   ├── dashboard/
│   │   ├── account/                  # Account, Settings & In-App Updates
│   │   ├── insights/                 # Financial analytics
│   │   ├── loans/                    # Loan tracking & payments
│   │   ├── money/                    # Balances, Denominations & Transfers
│   │   ├── snacks/                   # Snack inventory management
│   │   └── page.tsx                  # Home overview dashboard
│   ├── globals.css                   # Tailwind styles & safe-area insets
│   └── layout.tsx                    # Root layout with MobileInitializer
├── components/                       # UI components
│   ├── ui/                           # Radix / shadcn/ui primitives
│   ├── mobile-nav.tsx                # Material 3 Bottom Navigation
│   ├── mobile-initializer.tsx        # Native initialization & update check
│   ├── network-status-bar.tsx        # Offline connection banner
│   └── update-dialog.tsx             # Interactive release update dialog
├── lib/                              # Core logic & utilities
│   ├── firebase.ts                   # Firebase initialization with fallbacks
│   ├── native.ts                     # Native hardware & haptics bridge
│   ├── types.ts                      # TypeScript interfaces & types
│   └── version-checker.ts            # GitHub Release update engine
├── version.json                      # Version manifest for in-app updates
├── CHANGELOG.md                      # Release version history
└── README.md                         # Project documentation
```

---

## 🔐 Environment Variables

For web hosting or custom Firebase deployments, configure `.env.local`:

```env
NEXT_PUBLIC_FIREBASE_API_KEY=your-api-key
NEXT_PUBLIC_FIREBASE_AUTH_DOMAIN=your-project.firebaseapp.com
NEXT_PUBLIC_FIREBASE_PROJECT_ID=your-project-id
NEXT_PUBLIC_FIREBASE_STORAGE_BUCKET=your-project.firebasestorage.app
NEXT_PUBLIC_FIREBASE_MESSAGING_SENDER_ID=your-sender-id
NEXT_PUBLIC_FIREBASE_APP_ID=your-app-id
```

---

## 🤝 Contributing

Contributions are always welcome:

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

---

## 📄 License

Distributed under the **MIT License**. See [`LICENSE`](LICENSE) for more information.

---

## 👨‍💻 Maintainer

**SM Tech** ([@smtech005](https://github.com/smtech005))

<div align="center">

Made with ❤️ in Bangladesh 🇧🇩

**[⬆ Back to Top](#-reva)**

</div>
