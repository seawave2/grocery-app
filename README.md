# 🛒 Smart Grocery List App (רשימת קניות חכמה)

A modern, fast, and lightweight **Progressive Web App (PWA)** for managing your shopping and grocery lists effortlessly. Built with clean vanilla JavaScript, Tailwind CSS, FontAwesome icons, and complete offline support.

---

## ✨ Key Features

- **⚡ Two-List Smart Interface**:
  - **1. Active Shopping List**: Items currently needed. Click anywhere on an item card to check it off and remove it.
  - **2. Available Catalog**: Fast selection from a rich database of 460+ items sorted by frequency of use, alphabetical order, or category/family.

- **↩️ Full Multi-Level UNDO**:
  - Dedicated **Undo button** in the header.
  - Reverses accidental deletions, list clearing, additions, or catalog changes.
  - Supports keyboard shortcut: `Ctrl + Z` / `Cmd + Z`.

- **🌐 Trilingual Support (עברית | English | Русский)**:
  - Instant one-click language toggle across the entire application.
  - Full RTL (Right-to-Left) and LTR layout switching.
  - Seamless localization for all UI texts, categories, and 460+ products.

- **🌙 Dark Mode**:
  - Smooth light/dark theme transition with persistent user preference and RTL-aware toggle animation.

- **🔍 Smart Search & Categorized Additions**:
  - Live autocomplete search matching names across all supported languages.
  - Automatically prompts for a product category/family when typing a new custom item.

- **📱 Installable Progressive Web App (PWA)**:
  - Works on **Android, iPhone, and Desktop**.
  - Install directly from browser ("Install App" / "Add to Home Screen") as a native-feeling standalone app.
  - **100% Offline Capable**: Powered by a Service Worker and local storage cache; requires no active internet or Wi-Fi while shopping in the supermarket.

- **💾 Zero-Cloud Privacy**:
  - All lists and catalog usage statistics are stored strictly on your local device (`localStorage`).
  - No account registration, tracking, or external database required.

---

## 🚀 Live Demo & Deployment

This project is fully static and requires **no build step or backend**. It can be deployed in seconds to:
- **GitHub Pages**
- **Netlify**
- **Vercel**
- Or served locally with any HTTP server (e.g. Python `http.server`, Live Server, etc.)

### Deploying to GitHub Pages:
1. Fork or clone this repository.
2. In your GitHub repository, go to **Settings** > **Pages**.
3. Under **Branch**, select `main` (root) and click **Save**.
4. Your grocery app will be live at `https://<your-username>.github.io/<repository-name>/`.

---

## 📁 Project Structure

```text
├── index.html         # Main application layout, styles, and core logic
├── translations.js    # Comprehensive trilingual dictionary (Hebrew, English, Russian) & categories
├── manifest.json      # PWA Web App Manifest (app name, icons, display mode)
├── sw.js              # Service Worker for offline caching and standalone execution
├── icon-192.png       # 192x192 app launcher icon
├── icon-512.png       # 512x512 splash screen / store icon
├── netlify.toml       # Optional Netlify configuration header rules
└── README.md          # Project documentation
```

---

## 🛠️ Technologies Used

- **HTML5 & Vanilla JavaScript (ES6+)**
- **Tailwind CSS** (via CDN with dark mode support)
- **FontAwesome 6** (Icons)
- **SheetJS (xlsx)** (Client-side spreadsheet engine)
- **Service Worker & Cache API** (Offline PWA)

---

## 📄 License & Credits

© Made with ❤️ by **seawave**.  
Licensed under the [MIT License](LICENSE).
