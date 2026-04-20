# Frequently Asked Questions (FAQ)

Common questions about the FLIPPRX Wallet ecosystem answered.

---

## 🌐 General Questions

### What is FLIPPRX Wallet?

FLIPPRX is an advanced, non-custodial wallet ecosystem running entirely in your browser. It features multi-chain support (XRPL, Solana, Bitcoin), a unified UI of built-in Mini-dApps, and utilizes revolutionary SnapTap WebAuth security. 

### Do I need to download an extension?

**No.** FLIPPRX runs directly in your secure browser context. There is no chrome extension to install, nor an app store application to download. Simply navigate to [one.flipprx.xyz](https://one.flipprx.xyz) on Desktop or Mobile, and the wallet mounts securely.

### Is it free to use?

Yes! The wallet and the internal fApps are entirely free. You are only responsible for the native blockchain network fees (e.g., standard minuscule XRP transaction drops or SOL gas fees).

### Can FLIPPRX ONE access my funds?

**No.** FLIPPRX is 100% self-custodial. We have zero backend tracking or centralized key storage. Your private keys are derived and encrypted locally on your device hardware. We cannot access your funds under any circumstances.

---

## 🔐 Security Questions

### What is SnapTap KMS?

Traditional wallets rely on you physically writing down 12-to-24 random words perfectly (Seed Phrases). If you lose the paper, or a hacker finds it, your funds are gone.

**SnapTap** is our Key Management System that uses the WebAuthn standard to seal your encryption keys inside your device's Secure Enclave (like Apple's FaceID or Windows Hello). To authorize a transaction or mount the wallet, you simply scan your face or fingerprint.

### What if my device breaks or is stolen?

Because SnapTap seals keys to the device hardware, if your device is permanently destroyed, the keys are lost. **However**, FLIPPRX includes an advanced **Account Recovery (Guardian)** fApp. You can designate trusted friends or secondary ledgers as "Guardians" (Multi-Sig). If you lose your phone, your Guardians can collectively authorize a transaction to move your funds safely to a new wallet.

[Learn more about Security →](Security)

---

## 📱 The fApp Ecosystem

### What is a fApp?

A **fApp** (FLIPPRX Mini-dApp) is an application built natively into the wallet's dashboard. Instead of connecting your wallet to hundreds of external, potentially malicious websites, we build the most useful DeFi tools directly into our interface.

### How do I use the FLIPPRX Marketplace?

Simply load the wallet, click the "Apps" tab, and open the "FLIPPRX Marketplace". Because it is a native fApp, you don't need to sign external permissions. You can instantly browse the NFT gallery, check live filtering and rarity statistics, and submit zero-fee bid/ask transactions safely. 

### What are Encrypted Notes?

Inside the Apps tab, you can access **Encrypted Notes**. Because we built military-grade cryptographic key generation for your money, we realized we could use the same keys to encrypt text. Write down passwords, contacts, or secrets, and your wallet will encrypt them. Only your biometric scan can decrypt and read them.

### What are Payment Checks?

Exclusive to the XRPL, the **Checks** fApp allows you to write a digital check to an address. Instead of sending funds directly (which forces them into the recipient's wallet), a Check sits on the ledger waiting for the recipient to "Cash" it. If they don't cash it, you can "Cancel" the check and take your funds back. 

---

## 🌐 Multi-Chain Questions

### I want to use Solana. Do I need a new seed?

**No.** Your primary wallet mathematically derives your Solana (SOL) and Bitcoin (BTC) keypairs seamlessly. From the dashboard header, simply toggle the Network menu from XRPL to Solana. The dashboard will instantly restructure itself to show your SPL tokens and SOL balances, and the send/receive modal will adapt accordingly.

### Which chains are currently supported?

1. **XRP Ledger (XRPL):** Full native support, trustlines, Escrows, Checks.
2. **Solana (SOL):** Full native support, high-speed transfers, SPL tracking.
3. **Bitcoin (BTC):** Native Segwit high-security store-of-value.

---

## 🔧 Troubleshooting

### My balance isn't updating

1. Ensure your internet connection is active.
2. We connect directly to public RPC nodes. If a node is heavily congested globally, balances might lag by a few seconds.
3. Confirm you are toggled to the correct Network in the top-right corner.

### Transaction Failed

Common reasons:
- **Insufficient Base Reserve (XRPL):** XRPL requires 1 XRP permanently locked to activate an account.
- **Insufficient Trustline Reserve:** Adding a custom token or NFT requires locking an additional 0.2 XRP per item.
- **Invalid Address:** Ensure the destination exists on the correct chain (You cannot send SOL to an XRPL address).

### I forgot my WebAuth PIN / Biometrics failed

If your device biometric module fails permanently (e.g., hardware damage), you must rely on your previously established Guardian system, or standard Seed Recovery if you manually exported your seed. 

## 🆘 Support Questions

If you didn't find your answer here:

1. Join our [Telegram community](https://t.me/flipprx)
2. Contact support@flipprx.one
