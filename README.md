# 🌟 Cyberpunk Invoice Generator

A futuristic, cyberpunk-themed invoice generator with TikTok optimization mode. Perfect for digital resellers, gaming services, and content creators.

![Cyberpunk Invoice](https://img.shields.io/badge/Style-Cyberpunk-00E5FF?style=for-the-badge)
![TikTok Ready](https://img.shields.io/badge/TikTok-9:16%20Ready-FF0050?style=for-the-badge)
![License](https://img.shields.io/badge/License-MIT-FFE600?style=for-the-badge)

## ✨ Features

### 🎨 Cyberpunk Design
- Neon yellow/gold color scheme with dark backgrounds
- Glass morphism effects and glowing elements
- FUI (Fictional User Interface) corner markers
- Animated stats dashboard
- Professional typography with Orbitron and Rajdhani fonts

### 📱 TikTok Mode (9:16 Aspect Ratio)
- One-click toggle for TikTok-optimized layout
- Visual safe zone indicators (hidden in downloads)
- Perfect vertical format for social media
- Optimized font sizes for mobile viewing

### 💰 Smart Features
- Auto-calculating discount system (amount → percentage)
- Real-time price preview
- Payment status tracking (Paid/Pending/Failed)
- Customer review section with star ratings
- Payment proof upload support
- Invoice history with localStorage

### 📊 Dashboard Stats
- Total Value (10x multiplier)
- Revenue Estimate (5x multiplier)
- Balance (2x multiplier)
- Service Price (actual amount)
- Animated progress bars

### 🎯 Service Providers
Pre-configured for popular gaming services:
- DRIP CLINT
- HG CHEATS
- IOS FLUORITE
- PRIME HOOK
- PATO TEAM
- Custom/Special Services

## 🚀 Live Demo

**[Launch Invoice Generator](https://susantedit.github.io/invoicegenerator/invoice.html)**

## 📦 Installation

### Option 1: Direct Use
1. Clone the repository:
```bash
git clone https://github.com/susantedit/invoicegenerator.git
cd invoicegenerator
```

2. Open `invoice.html` in your browser

### Option 2: GitHub Pages
The project is automatically deployed via GitHub Pages. Just visit the live demo link above.

## 🎮 Usage

### Basic Invoice Generation
1. Fill in customer details (Name, Phone, TikTok ID)
2. Select service provider
3. Enter order description
4. Set price and discount amount
5. Choose payment status
6. Click "GENERATE INVOICE"

### TikTok Mode
1. Check the "📱 TikTok Mode (9:16 Ratio)" box
2. Red safe zones appear showing TikTok UI areas
3. Generate your invoice
4. Download PNG (safe zones automatically removed)
5. Upload to TikTok - perfect fit!

### Customer Reviews
1. Select star rating (1-5 stars)
2. Write custom review message (optional)
3. Auto-generates professional usernames
4. Appears at bottom of invoice with verified badge

### Download Options
- **Download PNG**: High-quality 2K resolution image
- **Copy Invoice ID**: Quick copy for reference
- **View History**: Access previously generated invoices

## 🛠️ Technical Details

### Technologies
- Pure HTML5, CSS3, JavaScript (no frameworks)
- html2canvas for PNG export
- localStorage for invoice history
- Google Fonts (Rajdhani, Orbitron, Share Tech Mono)

### Browser Support
- Chrome/Edge (recommended)
- Firefox
- Safari
- Mobile browsers

### File Structure
```
invoicegenerator/
├── invoice.html          # Main application (all-in-one)
├── logo.png             # Brand logo
├── README.md            # Documentation
└── [image assets]       # Service provider images
```

## 🎨 Customization

### Change Colors
Edit CSS variables in `invoice.html`:
```css
:root{
  --y:#FFE600;        /* Primary yellow */
  --bg:#0A0A0A;       /* Background */
  --text:#E8E8E8;     /* Text color */
  --green:#00FF88;    /* Success color */
}
```

### Add Service Providers
Update the `GAMES` object in JavaScript:
```javascript
const GAMES = {
  NEWSERVICE: { 
    name:"SERVICE NAME", 
    img:"image-url.jpg" 
  }
};
```

## 📱 TikTok Safe Zones

When TikTok mode is enabled:
- **Right side (70px)**: Reserved for Like/Comment/Share buttons
- **Bottom (80px)**: Reserved for video description
- Content automatically adjusts to avoid these areas
- Safe zone indicators are visual guides only (not in downloads)

## 🔒 Privacy

- All data stored locally in browser (localStorage)
- No server-side processing
- No data collection or tracking
- Images converted to base64 for secure downloads

## 📄 License

MIT License - feel free to use for personal or commercial projects.

## 👨‍💻 Author

**SUSANTEDIT**
- Trusted Reseller · Nepal · Est. 2024
- GitHub: [@susantedit](https://github.com/susantedit)

## 🤝 Contributing

Contributions welcome! Feel free to:
- Report bugs
- Suggest features
- Submit pull requests

## 📞 Support

For issues or questions, please open an issue on GitHub.

---

Made with 💛 in Nepal 🇳🇵
