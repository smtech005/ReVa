<div align="center">

# 💰 ReVa

**Personal Finance Manager for Bangladesh**

[![Version](https://img.shields.io/badge/version-3.1.1-green.svg)](https://github.com/smtech005/ReVa/releases)
[![Platform](https://img.shields.io/badge/platform-Android-brightgreen.svg)](https://github.com/smtech005/ReVa/releases)
[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
[![Firebase](https://img.shields.io/badge/Firebase-Enabled-orange.svg)](https://firebase.google.com/)

<img src="public/icon-512.png" alt="ReVa Logo" width="120" height="120">

**Track your money, snacks, and loans with precision**

[Download APK](https://github.com/smtech005/ReVa/releases/latest) · [Report Bug](https://github.com/smtech005/ReVa/issues) · [Request Feature](https://github.com/smtech005/ReVa/issues)

</div>

---

## ✨ Features

### 💵 Money Management
- **Multiple Locations**: Track cash, mobile banking (bKash, Nagad, Rocket, Upay), bank accounts, and international accounts (PayPal, Payoneer, Wise)
- **BDT Denominations**: Count your cash by notes (৳5, ৳10, ৳20, ৳50, ৳100, ৳200, ৳500, ৳1000)
- **Transaction History**: Full date/time stamps in Bangladesh timezone
- **Income & Expense**: Track where your money goes

### 🍿 Snack Inventory
- **Add & Track Snacks**: Name, quantity, unit cost, image
- **Consumption Tracking**: Record when you eat snacks with notes
- **Low Stock Alerts**: Get notified when snacks are running low
- **History Tab**: View all consumption with precise timestamps
- **Edit & Delete**: Full control over your inventory

### 💳 Loan Tracking
- **Lent & Borrowed**: Track money you've lent or borrowed
- **Payment History**: Record partial payments
- **Status Tracking**: Pending, partial, or settled
- **Due Date Reminders**: Never forget to collect or pay

### 📊 Financial Insights
- **Charts & Analytics**: Visualize your spending patterns
- **Category Breakdown**: See where your money goes
- **Monthly Trends**: Track your financial health over time

### 👤 Profile & Settings
- **Editable Profile**: Change your display name
- **Profile Photo**: Set a photo (saved locally)
- **Theme Toggle**: Light/Dark mode
- **Push Notifications**: Get updates and reminders
- **Manual Sync**: Force sync your data
- **Cache Management**: Clear local storage

---

## 📱 Screenshots

| Home | Money | Snacks | Insights |
|------|-------|--------|----------|
| Dashboard overview | Track locations | Inventory management | Analytics |

---

## 🚀 Installation

### Download APK (Recommended)

1. Go to [Releases](https://github.com/smtech005/ReVa/releases/latest)
2. Download `ReVa-v3.1.1.apk`
3. Install on your Android device
4. Allow installation from unknown sources if prompted

### Build from Source

#### Prerequisites

- Node.js 18+
- pnpm (recommended) or npm
- Android Studio
- Java JDK 17+ (tested with JDK 25)

#### Steps

```bash
# Clone the repository
git clone https://github.com/smtech005/ReVa.git
cd ReVa

# Install dependencies
pnpm install

# Build the Next.js app
pnpm run build

# Sync with Android
npx cap sync android

# Build APK
cd android
./gradlew assembleRelease
```

APK will be at: `android/app/build/outputs/apk/release/app-release-unsigned.apk`

---

## 🔧 Tech Stack

| Technology | Purpose |
|------------|---------|
| **Next.js 15** | React framework with App Router |
| **Capacitor 6** | Native mobile functionality |
| **Firebase** | Authentication, Firestore, FCM |
| **Tailwind CSS** | Styling |
| **TypeScript** | Type safety |
| **Recharts** | Charts and analytics |
| **Radix UI** | Accessible components |

### Capacitor Plugins

| Plugin | Purpose |
|--------|---------|
| `@capacitor/app` | App lifecycle, back button |
| `@capacitor/browser` | Open external links |
| `@capacitor/haptics` | Vibration feedback |
| `@capacitor/keyboard` | Keyboard management |
| `@capacitor/network` | Network status |
| `@capacitor/preferences` | Local storage (profile photo) |
| `@capacitor/push-notifications` | FCM notifications |
| `@capacitor/splash-screen` | Splash screen |
| `@capacitor/status-bar` | Status bar styling |

---

## 📁 Project Structure

```
ReVa/
├── app/                      # Next.js app routes
│   ├── dashboard/            # Main dashboard pages
│   │   ├── account/          # Account settings & profile
│   │   ├── insights/         # Financial analytics
│   │   ├── loans/            # Loan management
│   │   ├── money/            # Money tracking
│   │   └── snacks/           # Snack inventory
│   ├── globals.css           # Global styles
│   ├── layout.tsx            # Root layout
│   └── page.tsx              # Login page
├── components/               # React components
│   ├── skeletons/            # Loading skeletons
│   ├── ui/                   # UI components (shadcn)
│   ├── auth-provider.tsx     # Firebase auth context
│   ├── mobile-initializer.tsx # Capacitor init
│   ├── mobile-nav.tsx        # Bottom navigation
│   └── update-dialog.tsx     # Update notifications
├── lib/                      # Utilities
│   ├── hooks/                # Custom React hooks
│   ├── fcm.ts                # Firebase Cloud Messaging
│   ├── firebase.ts           # Firebase client
│   ├── types.ts              # TypeScript types
│   ├── utils.ts              # Utility functions (dates, formatting)
│   └── version-check.ts      # Update checking
├── android/                  # Android native code
├── public/                   # Static assets & icons
├── capacitor.config.json     # Capacitor config
├── CHANGELOG.md              # Version history
├── LICENSE                   # MIT License
└── package.json
```

---

## 🔐 Environment Variables

Create a `.env.local` file:

```env
# Firebase Configuration
NEXT_PUBLIC_FIREBASE_API_KEY=your-api-key
NEXT_PUBLIC_FIREBASE_AUTH_DOMAIN=your-project.firebaseapp.com
NEXT_PUBLIC_FIREBASE_PROJECT_ID=your-project-id
NEXT_PUBLIC_FIREBASE_STORAGE_BUCKET=your-project.appspot.com
NEXT_PUBLIC_FIREBASE_MESSAGING_SENDER_ID=your-sender-id
NEXT_PUBLIC_FIREBASE_APP_ID=your-app-id
```

---

## 📝 Changelog

See [CHANGELOG.md](CHANGELOG.md) for a detailed history of changes.

### Latest: v3.1.1 (2025-12-24)

- 🔧 **Bug Fixes**: Fixed account page linting issues, improved error handling
- 📊 **Performance**: Resolved Firestore index issues for better data fetching
- 👤 **Account Page**: Enhanced settings page with better error messages
- 🛠️ **Stability**: General improvements and bug fixes

---

## 🐛 Troubleshooting

### Build Issues

```bash
# Clear caches
rm -rf .next out node_modules
pnpm install
pnpm run build
npx cap sync
```

### Android Issues

- Ensure Android Studio is updated
- Install Android SDK 34+
- If using Java 25, lint may fail - already disabled in build.gradle

### Common Errors

| Error | Solution |
|-------|----------|
| `Cannot find module` | Run `pnpm install` |
| `Capacitor sync failed` | Delete `android` folder and re-add |
| `Lint failed` | Already handled in build.gradle |
| `Firebase not initialized` | Check `.env.local` values |

---

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## 👨‍💻 Author

**SM Tech** ([@smtech005](https://github.com/smtech005))

---

## 🙏 Acknowledgments

- [Next.js](https://nextjs.org/) - The React Framework
- [Capacitor](https://capacitorjs.com/) - Cross-platform native runtime
- [Firebase](https://firebase.google.com/) - Backend as a Service
- [shadcn/ui](https://ui.shadcn.com/) - Beautiful UI components
- [Tailwind CSS](https://tailwindcss.com/) - Utility-first CSS

---

<div align="center">

Made with ❤️ in Bangladesh 🇧🇩

**[⬆ Back to Top](#-reva)**

</div>
