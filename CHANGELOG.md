# Changelog

All notable changes to **ReVa** will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

---

## [5.0.0.0] - 2026-11-07

### 🚀 Major Highlights
- **Full ReVa App-Level Rebranding**: Unified design language, brand identities, and theme across web and native Android platforms.
- **Native Android v5.0.0.0 Package**: Compiled for Android 15 (Target SDK 35) with custom multi-density launcher icons, adaptive icons, and official Google Services Firebase integration (`com.reva.app`).
- **In-App GitHub Release Update Engine**: Built-in universal update checker fetching from GitHub Releases, CDN mirrors, and repository manifests with an interactive download and installation modal.
- **Material Design 3 Android UI/UX Philosophy**: 5-tab bottom navigation with active pills, native hardware back button handling with double-tap exit, offline network status banner, edge-to-edge safe area insets, and tactile haptic touch feedback.
- **Inter-Location Fund Transfers**: Transfer money between wallets, banks, and mobile banking services with full BDT cash note denomination tracking.

### Added
- **In-App Updates & Releases Screen (`/dashboard/account`)**:
  - Live version check against GitHub Releases and CDN mirrors.
  - Interactive Material 3 update dialog displaying version badges, release dates, and formatted changelogs.
  - One-click APK download and installation trigger via `@capacitor/browser`.
  - Rate-limited background checking (every 4 hours) with optional "Remind Me Later" and version skip persistence.
  - Support for mandatory updates with dismissal lock for critical patches.
- **Account & Preferences Management**:
  - Profile avatar upload with local persistent storage (`@capacitor/preferences`).
  - Inline display name editor and verified user badge.
  - Instant Dark Mode / Light Mode toggle with system preference auto-detection.
  - Haptic feedback toggle.
  - Force Cloud Sync button to refresh Firestore transactions on demand.
  - Local cache and session storage clearing tool with confirmation modal.
  - Direct links to GitHub repository, Issue tracker, and Privacy Policy.
- **Android Material 3 Navigation & Gestures**:
  - 5-tab Bottom Navigation Bar: **Home**, **Money**, **Snacks**, **Loans**, and **Account**.
  - Modern pill active indicators and animated touch scaling.
  - Haptic feedback on tab selection via `@capacitor/haptics`.
  - Hardware back button listener via `@capacitor/app`: double-tap back within 2 seconds to safely exit on the dashboard; smooth back navigation on sub-screens.
  - Top offline network banner notifying users when operating offline via `@capacitor/network`.
  - Edge-to-edge safe area insets (`viewport-fit=cover`, `env(safe-area-inset-top)`, `env(safe-area-inset-bottom)`).
  - Disabled 300ms tap delays and tap highlight overlays for a fluid native feel.
- **Money & Transfers**:
  - Fund Transfer dialog in Money Dashboard (`/dashboard/money`).
  - Cash-to-cash, cash-to-digital, and digital-to-digital transfers.
  - Denomination breakdown for notes transferred and received.
  - Transfer transaction history with distinct blue indicator icons (`ArrowRightLeft`).
  - Multi-location deletion and balance recount safeguards.
- **Snacks & Inventory**:
  - Individual snack deletion with real-time recalculation of remaining inventory value.
  - Form validation preventing negative counts or zero quantities.
  - Protection against `NaN` divide-by-zero errors when calculating remaining unit values.
- **Loans Management**:
  - Individual loan deletion with confirmation.
  - Real-time loan repayment progress bar and remaining balance calculations.
  - Financial insights recalculations updated dynamically on loan status changes.

### Changed
- Upgraded runtime to **Capacitor 8** (`@capacitor/core`, `@capacitor/android`, `@capacitor/app`, `@capacitor/haptics`, `@capacitor/keyboard`, `@capacitor/status-bar`, `@capacitor/splash-screen`, `@capacitor/preferences`, `@capacitor/browser`, `@capacitor/network`).
- Upgraded web framework to **Next.js 16** with Turbopack and React 19.
- Updated Android build configuration: `compileSdkVersion 35`, `targetSdkVersion 35`, `minSdkVersion 22`, `versionCode 50000`, `versionName "5.0.0.0"`.
- Migrated ESLint configuration to native flat config format (`eslint.config.mjs`) compatible with ESLint 9.
- Dashboard header now features user profile avatar linking directly to `/dashboard/account`.

### Fixed
- Fixed SSR `auth/invalid-api-key` crash during Next.js static prerendering by providing safe build-time fallbacks in Firebase initialization.
- Fixed dual `request.json()` consumption bug in `/api/v1/auth/route.ts` API route handler.
- Fixed composite Firestore query failures by creating proper compound indexes for `{ userId, type, date }` and `{ userId, createdAt }`.
- Fixed Kotlin stdlib duplicate class collisions (`kotlin-stdlib-jdk7` / `kotlin-stdlib-jdk8`) in Gradle build via BOM alignment and resolution strategy.
- Fixed AndroidX compileSdk 36 dependency requirement by pinning compatible Android 15 libraries (`androidx.activity:1.9.3`, `androidx.core:1.15.0`, `androidx.browser:1.8.0`).

---

## [3.1.1] - 2025-12-24

### Fixed
- Account page: Removed unused error variables causing linting warnings.
- Data fetching: Improved error handling and Firestore query optimization.
- Performance: Resolved index issues for `moneyLocations` queries.

### Changed
- Version check: Updated to fetch from ReVa repository instead of legacy fork.
- Account page: Enhanced error messages and stability.

---

## [3.1.0] - 2025-12-24

### Fixed
- Android: Ensured Firebase initializes reliably on all devices with verified Google Services plugin.
- Improved build reliability for Android 13/14.

### Changed
- Bumped version for Android and web to 3.1.0.

---

## [3.0.0] - 2025-12-24

### Added
- **Universal Update System**:
  - Persistent, platform-aware update modal.
  - Mandatory and optional update support.
  - In-app release notes display.
  - Safeguard preventing APK download in unsupported browser environments.
  - Background polling mechanism.

### Changed
- Modernized update instruction prompts.
- Improved native platform detection and reliability.

---

## [2.3.0] - 2024-12-24

### Added
- **Cash Expense with Change Tracking**:
  - Pay with larger notes and record change received.
  - Automatic net expense calculation and note tracking.
- **Fund Transfer Between Locations**:
  - Transfer money between locations (cash, bank, mobile banking).
  - Full denomination tracking for physical cash transfers.
- **Profile on Home Dashboard**:
  - Profile photo displayed on home page with welcome greeting.
- **Transaction History Sorting**:
  - Ordered by date (newest first) with color-coded badges.

---

## [2.2.0] - 2024-12-24

### Added
- Snacks inventory editing, consumption history tab, and low stock badges.
- Profile display name and local photo selection.
- Bangladesh timezone (Asia/Dhaka) formatting on timestamps.

---

## [2.0.0] - 2024-12-23

### Added
- Rebranding to ReVa.
- FCM push notifications support.
- In-app update notifications and GitHub Releases integration.
- Light/Dark mode toggle.

---

## [1.0.0] - 2024-12-22

### Added
- Initial release of ReVa personal finance manager.
- Multi-location money tracking (Cash with BDT denominations, bKash, Nagad, Rocket, Bank accounts).
- Snack inventory management and consumption tracking.
- Loan tracking (lent/borrowed) with due dates.
- Financial insights charts with Recharts.
- Firebase Auth & Firestore with offline cache.

---

## Version History Summary

| Version | Build Number | Release Date | Platform | Status |
|:-------:|:------------:|:------------:|:--------:|:------:|
| **5.0.0.0** | **50000** | **2026-11-07** | **Android / Web** | **Current (Latest)** |
| 3.1.1 | 5 | 2025-12-24 | Android / Web | Superseded |
| 3.1.0 | 4 | 2025-12-24 | Android / Web | Superseded |
| 3.0.0 | 3 | 2025-12-24 | Android / Web | Superseded |
| 2.3.0 | 5 | 2024-12-24 | Android | Superseded |
| 2.2.0 | 4 | 2024-12-24 | Android | Superseded |
| 2.1.0 | 3 | 2024-12-23 | Android | Superseded |
| 2.0.0 | 2 | 2024-12-23 | Android | Superseded |
| 1.0.0 | 1 | 2024-12-22 | Android | Initial Release |
