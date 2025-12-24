# [3.1.1] - 2025-12-24

### Fixed
- Account page: Removed unused error variables causing linting warnings
- Data fetching: Improved error handling and Firestore query optimization
- Performance: Resolved index issues for moneyLocations queries

### Changed
- Version check: Updated to fetch from ReVa repository instead of v0-money-inventory-app
- Account page: Enhanced error messages and stability

# [3.1.0] - 2025-12-24

### Fixed
- Android: Ensure Firebase initializes correctly on all devices (Google Services plugin and config verified)
- Improved build reliability for Android 13/14

### Changed
- Version bump for Android and web to 3.1.0

# [3.0.0] - 2025-12-24

### Added
- **Universal Update System**
  - Persistent, platform-aware update modal
  - Mandatory and optional update support
  - Release notes always shown
  - Prevents APK download in unsupported browsers
  - FCM push and background polling

### Changed
- Modern, clear update instructions
- Improved platform detection and reliability

---
# Changelog

All notable changes to ReVa will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [2.3.0] - 2024-12-24

### Added
- **Cash Expense with Change Tracking**
  - Pay with larger notes and record change received
  - Automatic net expense calculation
  - Track exactly which notes you gave and received back
  - Summary showing: Notes Given, Change Back, Net Expense

- **Fund Transfer Between Locations**
  - Transfer money from one location to another
  - Move cash from wallet to bank account
  - Withdraw from mobile banking to physical cash
  - Full denomination tracking for cash-to-cash transfers
  - Digital transfer for bank/mobile banking locations

- **Profile on Home Dashboard**
  - Your profile photo displayed on home page
  - Display name shown in welcome section
  - Quick identity access

- **Transaction History Improvements**
  - Properly sorted by date (newest first)
  - Transfer transactions shown in blue
  - Clear visual indicators for transaction types
  - Fixed ordering with Firestore orderBy

### Changed
- Transaction type now includes "transfer" alongside income/expense
- Money page action buttons changed to 3-column grid
- Enhanced Transaction type with transfer-related fields

### Technical
- Added orderBy("createdAt", "desc") to all transaction queries
- Updated Transaction interface with fromLocationId, toLocationId
- Added changeReceived and notesReceived to Transaction type

## [2.2.0] - 2024-12-24

### Added
- **Snacks Management Improvements**
  - Edit snacks (name, image, quantity, cost)
  - Delete snacks with confirmation
  - Consumption history tab with timestamps
  - Low stock alerts (yellow/red badges)
  - Notes field for consumption entries
  - Better UI with Inventory/History tabs
  
- **Profile Editing**
  - Editable display name
  - Profile photo selection (saved locally)
  - Quick edit buttons on profile card
  
- **Precise Timestamps**
  - Full date/time on transaction history
  - Full date/time on consumption history
  - Bangladesh timezone (Asia/Dhaka) support

### Changed
- Snacks sorted by low stock first
- Improved dark mode colors for transaction cards
- Better accessibility with aria-labels

### Fixed
- TypeScript errors with Firestore timestamps
- Lint warnings for accessibility

## [2.1.0] - 2024-12-23

### Added
- jsDelivr CDN for faster version checks
- Update check on every app open

### Changed
- Version check interval reduced to 0 (instant)

## [2.0.0] - 2024-12-23

### Added
- Complete app rebranding to "ReVa"
- Firebase Cloud Messaging (FCM) for push notifications
- In-app update notifications
- Version checking system
- GitHub Releases integration
- Mobile-specific optimizations

### Changed
- New gradient header design on homepage
- Enhanced navbar with active state indicator
- Improved account page with functional settings
  - Theme toggle (light/dark)
  - Push notifications toggle
  - Manual sync button
  - Cache clear option
  - Update checker

### Fixed
- Java 25 compatibility with Gradle 9.2.1 + AGP 8.7.3

## [1.0.0] - 2024-12-22

### Added
- Initial release of ReVa mobile app
- Money tracking across multiple locations
  - Cash with BDT denominations (৳5 to ৳1000)
  - Mobile banking (bKash, Nagad, Rocket, Upay)
  - Bank accounts
  - International accounts (PayPal, Payoneer, Wise)
- Snack inventory management
- Loan tracking (lent/borrowed)
- Financial insights with charts
- Offline support with local caching
- Firebase Authentication
- Real-time Firestore sync
- Dark mode support
- Haptic feedback
- Status bar customization

---

## Version History

| Version | Build | Date | Status |
|---------|-------|------|--------|
| 2.3.0 | 5 | 2024-12-24 | Current |
| 2.2.0 | 4 | 2024-12-24 | - |
| 2.1.0 | 3 | 2024-12-23 | - |
| 2.0.0 | 2 | 2024-12-23 | - |
| 1.0.0 | 1 | 2024-12-22 | Initial |
