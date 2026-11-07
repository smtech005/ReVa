<div align="center">

# 💰 ReVa

**Intelligent Personal Finance, Cash Denominations & Inventory Manager with Google Gemini AI**

[![Version](https://img.shields.io/badge/version-6.0.0.1-emerald.svg)](https://github.com/smtech005/ReVa/releases)
[![Platform](https://img.shields.io/badge/platform-Android%20%7C%20Web-brightgreen.svg)](https://github.com/smtech005/ReVa/releases)
[![Target SDK](https://img.shields.io/badge/Target%20SDK-35%20(Android%2015)-blue.svg)](https://developer.android.com/about/versions/15)
[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
[![Firebase](https://img.shields.io/badge/Firebase-Firestore%20%7C%20Auth-orange.svg)](https://firebase.google.com/)
[![Gemini AI](https://img.shields.io/badge/Google%20Gemini-2.5%20Flash%20%7C%202.0%20Flash-8E24AA.svg)](https://aistudio.google.com/)

<img src="https://raw.githubusercontent.com/smtech005/v0-money-inventory-app/main/public/icon-512.png" alt="ReVa Logo" width="120" height="120">

### Track your money, physical cash changes, loans, and snacks with intelligent AI guidance

[Download Signed APK v6.0.0.1](https://github.com/smtech005/ReVa/releases/download/v6.0.0.1/ReVa-v6.0.0.1.apk) · [Release Notes](CHANGELOG.md) · [Report Bug](https://github.com/smtech005/ReVa/issues) · [Request Feature](https://github.com/smtech005/ReVa/issues)

</div>

---

## 🚀 What's New in v6.0.0.1

ReVa **v6.0.0.1** is a landmark release introducing end-to-end **Physical Cash Change Register**, deep on-device **Google Gemini AI** integration, **Standardized Financial Categories**, and a complete **Emerald Fintech UI/UX** overhaul.

- **💵 Physical Cash Change Register**: Track exact physical BDT notes handed to merchants (tendered) and automatically calculate or customize change notes returned into your wallet.
- **🤖 Next-Gen Google Gemini AI**:
  - Full support for **Free Tier** (`gemini-2.5-flash`, `gemini-2.0-flash`, `gemini-2.0-flash-lite`, `gemini-1.5-flash`) and **Pro Tier** (`gemini-2.5-pro`, `gemini-1.5-pro`).
  - Resilient automatic multi-model fallback engine (`callGeminiApiWithFallback`) ensuring 100% availability.
  - Interactive **ReVa AI Financial Advisor** chat with real-time awareness of cash balances, loans, and transaction history.
  - Natural Language **Quick Log** (*"Paid 500 for lunch, got 380 back"*).
  - AI **"Can I Afford This?"** purchase simulator.
  - Deep **Expense Leak Analyzer** and **Financial Health Scorecards** (0–100).
- **🏷️ Standardized Categories**: Clean, unified expense and income categories with icons and color coding across the entire app.
- **🎨 Modern Emerald Fintech UI/UX**: Sticky edge-to-edge header with instant AI trigger, glassmorphic cards, floating mobile navigation, and accessible Radix confirmation dialogs.
- **📱 Signed Android Release Package**: Standalone signed APK (`ReVa-v6.0.0.1.apk`, 4.24 MB) verified with APK Signature Schemes v1 & v2 for instant installation on any Android device.

---

## ✨ Features

### 💵 Money Management & Cash Change Register
- **Multiple Locations**: Track physical cash, mobile banking (**bKash**, **Nagad**, **Rocket**, **Upay**), bank accounts, and international accounts (**PayPal**, **Payoneer**, **Wise** in USD).
- **BDT Denominations**: Track physical cash note counts by denomination (৳5, ৳10, ৳20, ৳50, ৳100, ৳200, ৳500, ৳1000) with automatic total valuation.
- **Cash Tendered & Change Tracking**: When paying cash, specify the exact notes handed over. ReVa calculates the expected change and lets you log received change notes with one-tap greedy denomination auto-fill.
- **Fund Transfers**: Transfer money between any two locations with full cash note breakdown for physical cash transfers.
- **Transaction History**: Real-time chronological logging with transaction type badges (Income, Expense, Transfer) and Bangladesh timezone (Asia/Dhaka) formatting.

### 🤖 Google Gemini AI Core
- **Interactive Advisor**: Floating AI trigger on desktop and mobile bottom navigation providing instant personal finance advice tailored to your actual wallet and loan balances.
- **Natural Language Quick Log**: Type naturally to record expenses without filling out long forms.
- **"Can I Afford This?" Simulator**: Instant AI feasibility verdict based on emergency buffers, recurring burn rate, and liquid cash.
- **Financial Health Audit & Leak Analysis**: Objective 0–100 score with identified leakage categories and monthly savings targets.
- **Secure On-Device Storage**: Encrypted API key storage via `@capacitor/preferences`. No intermediate proxy servers.

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
- **AI Health Audit**: Deep algorithmic and generative audit of financial stability.

### 👤 Account, Settings & In-App Updates
- **Gemini AI Settings**: Direct key input, show/hide toggle, model selector with Free and Pro badges, and one-click connection testing.
- **Profile Customization**: Upload and change your profile photo (persisted in offline storage) and edit your display name.
- **In-App Updates**: Built-in GitHub Releases updater that automatically checks for newer APK versions and guides installation.
- **Appearance**: One-tap toggle between Light Mode and Dark Mode.
- **Haptic Touch Engine**: Vibration feedback on navigation tabs, button presses, and confirmations.
- **Data & Sync Tools**: Force cloud sync with Firestore and clear local cache safely.

---

## 📱 Screenshots

| Home Dashboard | Money & Cash Change | AI Financial Advisor | Insights & AI Audit |
|:---:|:---:|:---:|:---:|
| Overview & Quick Log | Notes & Change Breakdown | Live Contextual Advice | Health Score & Leak Analysis |

---

## 📲 Installation

### Direct APK Download (Recommended)

1. Navigate to [ReVa v6.0.0.1 Release](https://github.com/smtech005/ReVa/releases/tag/v6.0.0.1).
2. Download **[`ReVa-v6.0.0.1.apk`](https://github.com/smtech005/ReVa/releases/download/v6.0.0.1/ReVa-v6.0.0.1.apk)**.
3. Open the downloaded file on your Android device and tap **Install** (allow *Install from Unknown Sources* if prompted).
4. Launch ReVa and enjoy!

---

## 🛠️ Build from Source

### Prerequisites

- **Node.js**: v18.0+ or v20.0+
- **Package Manager**: `pnpm` (recommended)
- **Java Development Kit**: OpenJDK 17 LTS
- **Android SDK**: Android SDK Platforms 34 / 35 with Build Tools 35.0.0
- **Gradle**: 8.11+ (or included Gradle wrapper)

### Step-by-Step Instructions

```bash
# 1. Clone the repository
git clone https://github.com/smtech005/v0-money-inventory-app.git
cd v0-money-inventory-app

# 2. Install dependencies
pnpm install

# 3. Build the static Next.js export for Capacitor
pnpm build:mobile

# 4. Sync web assets with the Android native project
npx cap sync android

# 5. Build the signed Release APK
cd android
./gradlew assembleRelease
```

The generated signed release APK will be located at:
```text
android/app/build/outputs/apk/release/app-release.apk
```
Or in the pre-packaged release directory:
```text
release/ReVa-v6.0.0.1.apk
```

---

## 🔧 Architecture & Tech Stack

| Component | Technology | Version | Purpose |
|:---|:---|:---:|:---|
| **Web Framework** | Next.js (App Router) | `16.0.10` | High-performance React application core |
| **AI Engine** | Google Gemini API | `v1beta` | 2.5 Flash / 2.0 Flash / 2.5 Pro financial intelligence |
| **Mobile Runtime** | Capacitor Android | `8.6.0` | Native Android bridge and platform APIs |
| **Language** | TypeScript / Java | `5.0` / `17` | End-to-end type safety and Android compilation |
| **Database** | Firebase Firestore | `v12+` | Real-time multi-device cloud database with local cache |
| **Authentication** | Firebase Auth | `v12+` | Secure email/password and OAuth authentication |
| **Styling** | Tailwind CSS / Radix UI | `v4` | Modern emerald fintech UI components |
| **Charts** | Recharts | `v2` | Financial data visualizations and spending trends |
