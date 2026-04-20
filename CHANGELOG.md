# Changelog

All notable changes to FLIPPRX ONE will be documented in this file.

## [2.0.0] - 2026-04-20

### 🔥 Major - The Architecture Ecosystem Update
- **Unified SPA Hub** - Completely migrated the wallet into a seamless Single Page Application. No more hard page reloads.
- **The fApp Ecosystem** - Introduced native Mini-dApps integrated purely into the wallet dashboard avoiding third-party routing.
- **FLIPPRX Marketplace SPA Integration** - Marketplace now runs entirely inside the wallet as an fApp, providing ultra-smooth bid/ask execution.
- **Glassmorphic Redesign** - Purged all legacy brutalist CSS in favor of a sleek translucent `glass-card` design pattern affecting everything from NFT Cards to the central Dashboard.
- **Zero Backend Required** - Successfully removed all legacy PostgreSQL and Prisma architecture (specifically offboarding legacy minting) to embrace 100% XRPL on-chain dependency.
- **Domain Depot Viewer** - Upgraded the domain system to scan and route strictly via the native `Domain` field in the user's `AccountRoot` on the ledger.
- **Full SnapTap Prioritization** - Shifted documentation and user onboarding to exclusively emphasize WebAuthn KMS (FaceID/TouchID) creation over legacy 12-word seeds.

---

## [1.4.0] - 2026-02-27

### 🎯 Added - UX Improvements
- **Recent Recipients** - Last 3 addresses shown as quick-tap chips on Send (XRP + Solana)
- **One-Tap QR Receive** - Dashboard button opens compact QR modal for current network address
- **MAX Send Button** - Auto-fills maximum sendable balance (reserves 10 XRP for account reserve)
- **Live USD Equivalent** - Real-time dollar value shown while typing send amounts
- **Transaction Receipts** - Copy formatted receipt (amount, destination, tx hash) after sending
- **Network Indicator Badge** - Persistent pill with pulse dot showing active blockchain
- **Swipe Tab Navigation** - Swipe left/right on mobile to navigate between tabs
- **Smart Notifications** - Success auto-dismisses in 3s, errors stay for 8s

### 🎨 Enhanced - Styling & Polish
- **Active Tab Glow** - Pulsing green shadow on selected tab
- **Balance Shimmer Loading** - Skeleton placeholders while balances load
- **Animated Numbers** - Smooth counting animation on total USD value changes
- **Balance Flash** - Green flash on successful balance refresh
- **Button Tap Feedback** - `active:scale-95` on all buttons for mobile feel
- **Input Focus Glow** - Green halo on focused input fields
- **Glass Card Dark Mode** - Backdrop-blur and subtle glow in dark mode
- **Modal Backdrop Blur** - Upgraded overlay with blur effect
- **Update Toast** - Compact bottom notification replaces aggressive modal

---

## [1.3.0] - 2026-02-27

### 🔒 Added - Security Hardening
- **Server-Side Input Validation** - All 14 API routes hardened with strict input validation
- **DApp Transaction Approval** - Transactions from connected dApps require explicit user approval
- **Clipboard Hijack Protection** - Visual confirmation toast on all address paste events
- **Auto-Lock / Session Timeout** - Wallet locks after inactivity period for safety
- **Address Book Sanitization** - Contact names stripped of HTML tags and length-limited
- **Wallet Version System** - Centralized `WALLET_VERSION` constant with changelog notifications

### 🚀 Added - Multi-Chain Expansion
- **Solana Mainnet** - Full send, receive, and SPL token support
- **Bitcoin Support** - Bitcoin wallet activation and transactions (preview)
- **Network Switcher** - Seamless switching between XRPL, Solana, Supra, and Bitcoin

---

## [1.2.0] - 2024-12-31

### 🌍 Added - Bilingual Support
- **Complete Spanish Language Support** - 350+ translation keys covering entire UI
- **Real-time Language Switching** - Toggle between English and Spanish in Settings
- **Persistent Language Preference** - User choice saved in localStorage
- **Event-Driven Updates** - All components update instantly on language change
- **Comprehensive Coverage** - All features translated:
  - Main navigation and settings
  - Balance display and transaction forms
  - NFT gallery and search (including incoming transfers)
  - Exchange forms (Buy/Sell and Swap)
  - Transaction history and status tracking
  - Domains manager and MIMO messenger
  - LP trading and swap modules
  - Trustline management
  - DApp connections

### 🔧 Fixed - Security & UX Improvements
- **Import Errors** - Fixed duplicate icon imports across multiple components
- **Component Structure** - Resolved JSX syntax errors in NFTSearch and ExchangeForm
- **Missing Imports** - Added missing useLanguage hooks to all components
- **Code Quality** - Cleaned up duplicate code and improved maintainability

### 🎨 Enhanced
- **NFT Search** - Added "Check NFT for Incoming Transfer" feature
- **Exchange Forms** - Improved form labels and validation messages
- **Transaction Status** - Enhanced empty state messages
- **Address Validation** - Real-time crypto address format verification

---

## [1.1.0] - 2024-12

### 🚀 Added
- **Changelly Exchange Integration** - Buy and sell crypto with fiat
- **NFT Pack System** - Purchase and reveal collectible NFT packs
- **Domain Manager** - 2MCLUB domain claiming for 2M+ FLIPPRX holders
- **Transaction Status Tracking** - Monitor exchange and swap transactions
- **Address Validation** - Real-time validation for multiple blockchain addresses

### 🔧 Improved
- **LP Trading** - Enhanced NFT authorization checks
- **Trustline Manager** - Added support for LP tokens (ECP, JNT, MFLIP)
- **NFT Gallery** - Improved metadata display and image loading
- **MIMO Messenger** - Enhanced notification system

---

## [1.0.0] - 2024-11

### 🎉 Initial Release
- **SnapTap WebAuth** - Revolutionary dual-key NFC/biometric security
- **Multi-Chain Support** - XRPL, Supra, and Coreum integration
- **Tiered Transaction Fees** - Reduced fees for NFT holders
- **LP Trading** - NFT-authorized liquidity pools
- **NFT Gallery** - Complete collection management
- **MIMO Messenger** - Encrypted on-chain messaging
- **DApp Connector** - Connect to XRPL dApps
- **Transaction History** - Complete audit trail
- **Trustline Manager** - Easy token management
- **Sound Effects** - Enhanced user experience

---

## Upcoming Features

### 🔄 In Development
- Mobile app (PWA) optimization
- Additional Solana DeFi integrations
- Enhanced NFT marketplace features
- Advanced trading tools and charting
- Portfolio analytics dashboard
- Multi-language expansion beyond English/Spanish

---

**For detailed technical changes, see the [commit history](https://github.com/cryptoprx/flipprxwallet/commits/main)**
