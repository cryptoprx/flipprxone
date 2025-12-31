# FLIPPRX ONE Wiki Files

This folder contains the wiki documentation for FLIPPRX ONE.

## 📚 Wiki Pages Created

1. **Home.md** - Main wiki landing page with navigation
2. **Getting-Started.md** - Complete setup and first-time user guide
3. **Security.md** - Comprehensive security documentation
4. **FAQ.md** - Frequently asked questions

## 🚀 How to Upload to GitHub Wiki

### Method 1: Via GitHub Web Interface (Easiest)

1. Go to your repository: https://github.com/cryptoprx/flipprxone
2. Click the **"Wiki"** tab at the top
3. Click **"Create the first page"**
4. For each wiki page:
   - Click **"New Page"**
   - Copy content from the corresponding .md file
   - Paste into the editor
   - Set the page title (e.g., "Home", "Getting Started", etc.)
   - Click **"Save Page"**

### Method 2: Clone Wiki Repository (Advanced)

```bash
# Clone the wiki repository
git clone https://github.com/cryptoprx/flipprxone.wiki.git

# Copy wiki files
cd flipprxone.wiki
cp ../wiki/*.md .

# Commit and push
git add .
git commit -m "Add initial wiki documentation"
git push origin master
```

## 📖 Wiki Structure

```
Home (Home.md)
├── Getting Started (Getting-Started.md)
├── Security (Security.md)
├── FAQ (FAQ.md)
└── More pages coming soon...
```

## 🔗 Internal Links

Wiki pages use internal links like:
- `[Getting Started](Getting-Started)`
- `[Security Guide](Security)`
- `[FAQ](FAQ)`

These will automatically work once uploaded to GitHub Wiki.

## ✨ Features Covered

### Home Page
- Overview and quick links
- Key features summary
- Navigation to all sections

### Getting Started
- Creating new wallets
- Importing existing wallets
- First transactions
- Security setup
- Troubleshooting

### Security Guide
- SnapTap WebAuth explanation
- Encryption standards
- Best practices
- Security checklist
- Threat protection

### FAQ
- General questions
- Security questions
- Transaction questions
- Troubleshooting
- Quick reference

## 📝 Future Wiki Pages

Consider adding:
- Features.md - Detailed feature documentation
- LP-Trading.md - Liquidity pool trading guide
- Multi-Chain.md - Supra and Coreum setup
- MIMO.md - Messenger guide
- Exchange.md - Changelly integration guide
- Transactions.md - Transaction management
- NFT-Gallery.md - NFT management guide
- Domains.md - Domain Depot guide
- Architecture.md - Technical architecture
- API.md - API integration guide

---

**Ready to upload to GitHub Wiki!** 🚀
