# Installation Guide

This guide will help you set up the Personal Profile Card project on your local machine.

## 📋 Prerequisites

- Modern web browser (Chrome, Firefox, Safari, Edge)
- Text editor (VS Code, Sublime Text, etc.)
- Git (for cloning the repository)

## 🚀 Quick Installation

### Method 1: Direct Download
1. Go to [GitHub Repository](https://github.com/harshityadav-7/personal-card)
2. Click **Code** → **Download ZIP**
3. Extract the ZIP file to your desired location
4. Open `index.html` in your web browser

### Method 2: Git Clone
```bash
git clone https://github.com/harshityadav-7/personal-card.git
cd personal-card
```

### Method 3: Fork and Clone
1. Fork the repository on GitHub
2. Clone your fork:
```bash
git clone https://github.com/YOUR_USERNAME/personal-card.git
cd personal-card
```

## 📁 Project Structure After Installation

```
personal-card/
├── index.html              # Main HTML file
├── styles.css              # Styling and animations
├── Pictures/               # Image assets
│   ├── iron man.jpg        # Profile avatar
│   ├── CololioLogoImage.png # Profile badge
│   ├── LinkedInImage.png   # LinkedIn icon
│   └── platform icons/     # Coding platform icons
├── README.md               # Project documentation
└── wiki/                   # This wiki documentation
```

## 🔧 Development Setup

### For Development:
1. Install a local development server (optional but recommended)
2. Popular options:
   - **VS Code**: Install "Live Server" extension
   - **Python**: `python -m http.server 8000`
   - **Node.js**: `npx http-server`
   - **PHP**: `php -S localhost:8000`

### Using VS Code Live Server:
1. Install the "Live Server" extension
2. Right-click on `index.html`
3. Select "Open with Live Server"
4. Your browser will open with live reload functionality

## 🌍 Browser Testing

Test your installation in multiple browsers:
- ✅ Chrome (Recommended)
- ✅ Firefox
- ✅ Safari
- ✅ Edge
- ⚠️ Internet Explorer (Limited support)

## ✅ Verification Steps

1. **HTML loads correctly**: Page displays without errors
2. **CSS applies properly**: Dark theme and styling visible
3. **Images load**: Avatar and platform icons appear
4. **Animation works**: Background SVG rotates smoothly
5. **Links function**: Social platform links open correctly
6. **Responsive design**: Card adapts to different screen sizes

## 🐛 Common Installation Issues

### Images not loading:
- Verify the `Pictures/` folder exists
- Check file names match exactly (case-sensitive)
- Ensure all image files are present

### CSS not applying:
- Confirm `styles.css` is in the same directory as `index.html`
- Check for any console errors in browser developer tools

### Animation not working:
- Update to a modern browser version
- Enable hardware acceleration in browser settings

## 🔄 Updating

To update to the latest version:
```bash
git pull origin main
```

Or download the latest version and replace your files.

---

**Next Steps**: Check out the [Quick Start Guide](Quick-Start.md) to begin customizing your profile card!
