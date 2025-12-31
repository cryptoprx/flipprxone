# Security Guide

FLIPPRX ONE is built with security as the top priority. This guide explains our security architecture and best practices.

---

## 🔐 SnapTap WebAuth Security

### What is SnapTap?

**SnapTap** is a revolutionary dual-key authentication system that combines:

1. **Device Key** - Generated and stored on your device
2. **Authentication Key** - Created via NFC tap or biometric scan

**Both keys are required** to decrypt your wallet, providing unparalleled security.

### How It Works

```
Your Wallet = Device Key + Authentication Key
```

**Device Key:**
- Generated using Web Crypto API
- Stored in encrypted browser storage
- Never transmitted
- Unique per device

**Authentication Key:**
- Created via WebAuth API
- Requires NFC tap or biometric scan
- Ephemeral (temporary)
- Cannot be stolen remotely

### Security Benefits

| Attack Type | Traditional Password | SnapTap |
|-------------|---------------------|---------|
| Phishing | ❌ Vulnerable | ✅ Protected |
| Keylogging | ❌ Vulnerable | ✅ Protected |
| Device Theft | ❌ Vulnerable | ✅ Protected |
| Remote Attack | ❌ Vulnerable | ✅ Protected |
| Brute Force | ⚠️ Possible | ✅ Impossible |

---

## 🛡️ Encryption Standards

### AES-256-GCM

**Military-Grade Encryption**

- **Algorithm**: AES-256-GCM (Galois/Counter Mode)
- **Key Length**: 256 bits
- **Authentication**: Built-in authenticated encryption
- **Standard**: NIST approved, industry standard

**Features:**
- Prevents tampering
- Detects unauthorized modifications
- Constant-time operations
- Hardware-accelerated

### HKDF Key Derivation

**Secure Key Generation**

- **Algorithm**: HKDF (HMAC-based Key Derivation Function)
- **Iterations**: 100,000
- **Salt**: Random 16-byte salt per wallet
- **Output**: Cryptographically secure keys

**Benefits:**
- Prevents rainbow table attacks
- Unique keys per wallet
- Forward secrecy
- Resistant to brute force

### Web Crypto API

**Browser-Native Security**

All cryptographic operations use the Web Crypto API:
- Hardware-accelerated
- Secure random number generation
- Constant-time operations
- No external dependencies

---

## 🔑 Key Management

### Private Key Storage

**Your private keys are:**
- ✅ Encrypted with AES-256-GCM
- ✅ Stored only in browser storage
- ✅ Never transmitted to any server
- ✅ Protected by dual-key system

**We cannot:**
- ❌ Access your private keys
- ❌ Decrypt your wallet
- ❌ Recover your funds
- ❌ See your seed phrase

### Seed Phrase Security

**Your seed phrase is the master key:**

**Critical Rules:**
1. ✅ Write it down on paper
2. ✅ Store in multiple secure locations
3. ✅ Keep it offline
4. ❌ Never share with anyone
5. ❌ Never store digitally
6. ❌ Never take photos

**Recovery:**
- Your seed phrase can restore your entire wallet
- Without it, funds cannot be recovered
- Even we cannot help without your seed phrase

---

## 🔒 Self-Custodial Architecture

### Zero Backend

**100% Client-Side**

```
Your Device → XRPL Network
     ↓
  No Server
  No Database
  No Intermediary
```

**Benefits:**
- No server to hack
- No data to leak
- No third-party risk
- Complete privacy

### Direct XRPL Connection

**Peer-to-Peer**

- Direct WebSocket to XRPL nodes
- No intermediary servers
- Transactions signed locally
- Immediate blockchain submission

---

## 🌐 Network Security

### HTTPS Only

**Encrypted Connections**

- TLS 1.3 protocol
- Certificate pinning
- No mixed content
- Secure by default

### Content Security Policy (CSP)

**XSS Protection**

Strict CSP headers prevent:
- Cross-site scripting (XSS)
- Code injection
- Unauthorized connections
- Data exfiltration

**Allowed Connections:**
- XRPL mainnet nodes
- XRPL testnet nodes
- Official XRPL explorers
- Verified API endpoints

### Rate Limiting

**DDoS Protection**

- API routes: 30-60 requests/minute
- Prevents abuse
- Fair usage enforcement
- Automatic throttling

---

## 🎯 Best Practices

### For Maximum Security

#### 1. Use SnapTap WebAuth

**Enable dual-key authentication:**
- Setup biometric authentication
- Or use NFC tag
- Provides maximum protection
- Phishing resistant

#### 2. Secure Your Seed Phrase

**Backup properly:**
- Write on paper (not digital)
- Store in safe/vault
- Keep multiple copies
- Test recovery process

#### 3. Verify Addresses

**Before sending:**
- Double-check recipient address
- Verify amount
- Confirm transaction details
- Transactions are irreversible

#### 4. Keep Software Updated

**Stay current:**
- Update your browser
- Keep OS updated
- Enable automatic updates
- Use latest wallet version

#### 5. Use Strong Device Security

**Protect your device:**
- Enable device encryption
- Use strong device password
- Enable biometric lock
- Keep device secure

### What to Avoid

#### ❌ Never Share Your Seed

- No one legitimate will ask for it
- Not support staff
- Not developers
- Not anyone

#### ❌ Don't Use Public Computers

- Avoid public WiFi for transactions
- Don't use shared computers
- Use your personal device
- Use trusted networks

#### ❌ Beware of Phishing

**Red flags:**
- Emails asking for seed phrase
- Fake wallet websites
- Suspicious links
- Too-good-to-be-true offers

**Always verify:**
- URL is correct: one.flipprx.xyz
- HTTPS connection
- Official social media links

#### ❌ Don't Install Unknown Extensions

- Browser extensions can access data
- Only install from official sources
- Review permissions carefully
- Keep extensions minimal

---

## 🚨 Security Checklist

### Initial Setup

- [ ] Created wallet with SnapTap
- [ ] Wrote down seed phrase on paper
- [ ] Stored backup in secure location
- [ ] Verified backup by restoration test
- [ ] Enabled device security

### Regular Maintenance

- [ ] Browser is up to date
- [ ] Device OS is updated
- [ ] Reviewed transaction history
- [ ] No suspicious activity detected
- [ ] Seed phrase still secure

### Before Each Transaction

- [ ] Verified recipient address
- [ ] Double-checked amount
- [ ] Confirmed network fees
- [ ] Reviewed transaction details
- [ ] Authenticated with SnapTap

---

## 🔍 Security Audits

### Current Status

- ✅ Internal security review completed
- ✅ Peer code review
- ✅ Penetration testing
- 🔄 Third-party audit (planned)

### Continuous Monitoring

- Automated security scanning
- Dependency vulnerability checks
- Code quality analysis
- Regular security updates

---

## 🐛 Reporting Security Issues

### Responsible Disclosure

Found a security vulnerability? We appreciate responsible disclosure.

**Contact:** security@flipprx.one

**Please Include:**
- Detailed description
- Steps to reproduce
- Potential impact
- Suggested fix (if any)

**We Promise:**
- Acknowledgment within 24 hours
- Regular updates on progress
- Credit for responsible disclosure
- No legal action for good-faith research

---

## 📊 Security Comparison

### FLIPPRX ONE vs Traditional Wallets

| Feature | Traditional | FLIPPRX ONE |
|---------|------------|-------------|
| Authentication | Password only | Dual-key + Biometric |
| Encryption | Varies | AES-256-GCM |
| Key Storage | Server/Device | Device only |
| Phishing Protection | ❌ | ✅ |
| Self-Custodial | Sometimes | Always |
| Open Source | Varies | ✅ |
| No Data Collection | Varies | ✅ |

---

## 🎓 Security Education

### Understanding Threats

**Common Attack Vectors:**

1. **Phishing**
   - Fake websites
   - Malicious emails
   - Social engineering
   - **Protection:** SnapTap WebAuth

2. **Malware**
   - Keyloggers
   - Screen capture
   - Clipboard hijacking
   - **Protection:** Device security + SnapTap

3. **Social Engineering**
   - Impersonation
   - Fake support
   - Urgency tactics
   - **Protection:** Never share seed phrase

4. **Physical Theft**
   - Device stolen
   - Shoulder surfing
   - Lost hardware
   - **Protection:** Device encryption + SnapTap

### Staying Safe

**General Tips:**
- Trust but verify
- If it seems too good to be true, it is
- Take your time with transactions
- When in doubt, ask the community
- Keep learning about security

---

## 📚 Additional Resources

### Learn More

- [XRPL Security Best Practices](https://xrpl.org/security)
- [Web Crypto API Documentation](https://developer.mozilla.org/en-US/docs/Web/API/Web_Crypto_API)
- [WebAuthn Guide](https://webauthn.guide/)

### Community Resources

- [FLIPPRX Telegram](https://t.me/flipprx)
- [Security Discussions](https://github.com/cryptoprx/flipprxone/discussions)

---

## ⚠️ Disclaimer

**Your Responsibility:**

You are responsible for:
- Keeping your seed phrase secure
- Protecting your device
- Verifying transaction details
- Maintaining backups
- Following security best practices

**We Cannot:**
- Recover lost seed phrases
- Reverse transactions
- Access your wallet
- Restore lost funds
- Override blockchain rules

**Use FLIPPRX ONE at your own risk.**

---

**Security is a shared responsibility. We provide the tools, you protect your assets.** 🔐

**Questions? Contact security@flipprx.one**
