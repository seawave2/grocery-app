# 🛒 Smart Grocery List App (רשימת קניות חכמה) `v1.5`

A modern, fast, lightweight, and highly customizable **Progressive Web App (PWA)** for managing your shopping and grocery lists effortlessly. Built with clean vanilla JavaScript, Tailwind CSS, FontAwesome icons, and complete offline capability.

---

## ✨ Key Features & What's New in v1.5

### 🎛️ Header Mode Switcher (כפתור מצב מלא / פשוט בכותרת)
- **Top Navigation Segmented Switcher**: Conveniently located in the sticky top header right next to the Help button (`?`).
- **Instant 1-Tap Switching**: Seamlessly toggle between **Full Mode (מלא)** and **Simple Mode (פשוט)** at any time while shopping.
- **Silent & Unobtrusive**: Highlights the active mode directly on the pill button without annoying popup banners.

### 🧩 Modular UI Components Customizer (התאמת רכיבי ממשק עם תיבות סימון ✓)
- **Granular Feature Checkboxes (V)**: Tailor the interface to your exact personal preferences via Settings > General > "התאמת רכיבי ממשק":
  1. **רשימת פריטים שנקנו (Purchased Items List)**: Dedicated collapsible basket for checked-off items. When unchecked, checking off an item directly removes it back to the available catalog without storing it in a purchased list.
  2. **מד התקדמות קנייה (Shopping Progress Bar)**: Sleek completion progress tracker at the top of the shopping list.
  3. **כפתורי שינוי כמויות +/- (Quantity Controls)**: Intuitive plus and minus buttons to control amounts directly on item cards.
  4. **סידור לפי מחלקות סופרמרקט (Supermarket Aisle Grouping)**: Automatic grouping and sorting by store aisles and categories.
  5. **קרוסלת מחלקות בקטלוג (Catalog Category Carousel)**: Horizontal scrolling chips bar to filter available items by category.
  6. **תגיות מחלקה ואימוג'י במוצרים (Category Tags & Emojis)**: Category indicators and icons under product titles.
- **1-Click Presets**:
  - **שחזר למצב פשוט (ברירת מחדל)**: Sets all 6 features to unchecked for the cleanest, fastest minimalist experience.
  - **מצב מלא (כל הרכיבים)**: Turns on all 6 features with a single tap.
- **Live Status Badge**: Displays dynamic status in Settings: `פשוט`, `מלא`, or `מותאם (X/6)`.

### ⚡ Two-List Smart Architecture & Direct Removal
- **1. Active Shopping List**: Items currently needed.
  - In **Simple Mode Default**: Clicking an item checks it off and immediately returns it to the available products catalog below **without passing through "פריטים שנקנו"**.
  - In **Full Mode**: Checked-off items move gracefully into a collapsible "פריטים שנקנו" basket.
- **2. Available Catalog**: Fast selection from a rich database of 460+ items sorted by frequency of use, alphabetical order, or aisle / family. Clean catalog header without unnecessary counters.

### 📊 Ultra-Compact Shopping Progress Bar (מד התקדמות קנייה קומפקטי)
- Ultra-slim single-row progress bar (`🛒 3 מתוך 8 (38%)` with a smooth 6px rounded bar).
- Automatically hidden when the shopping list is empty or when the progress bar feature is turned off.
- Celebratory completion animation (`🎉 כל המוצרים נקנו!`) when all items are checked off.

### 🔖 Saved Lists & Pre-made Templates (רשימות שמורות ותבניות)
- Save your active shopping cart under a custom name (or auto-generated date) for recurring use.
- Quick access from the active list header with two loading modes:
  - **➕ Add to Cart (הוסף לסל)**: Merges template items and quantities into the current cart.
  - **🔄 Load as New (טען כחדשה)**: Replaces the current cart with the template list.
- Delete saved lists with a single tap (🗑️).
- Includes **6 built-in, curated templates**:
  - *סל בסיסי שבועי* (Weekly Essentials - updated with fresh produce, cheese, pitas, and balanced quantities)
  - *שבת ואירוח* (Shabbat & Hosting)
  - *מנגל ועל האש* (BBQ & Picnic)
  - *ניקיון ותחזוקת הבית* (Cleaning & Home Supplies)
  - *בוקר בריא ומוזלי* (Healthy Breakfast & Muesli)
  - *ערב איטלקי - פסטה ופיצה* (Italian Pasta & Pizza Night)
- Full Undo (`Ctrl+Z`) support for all template actions.

### 💰 Estimated Prices & Live Basket Calculator (מחירים משוערים וסיכום סל)
- Realistic Israeli supermarket price database for 460+ products (updated in NIS ₪).
- Accurate pricing per 1 kg for fruits, vegetables, and weighted goods.
- Toggle on/off in Settings: "הצג מחירים משוערים" with dynamic date indicator (`10/2026`).
- Real-time basket summary bar calculating the estimated total cost of active items and already purchased items.
- Clean, unbolded micro-price badges placed thoughtfully to ensure product names always remain clearly visible.

### 💡 Keep Screen Awake (מסך דולק תמיד)
- Convenient toggle in Settings to prevent your phone screen from dimming or locking while navigating supermarket aisles.
- Powered by the native **Screen Wake Lock API** (requires HTTPS like Netlify or GitHub Pages).

### 📤 Export & Share Shopping List (שיתוף מהיר)
- Export and share your active shopping list with a single click via the **"שתף" (Share)** button in the list header.
- Opens the native **mobile share sheet** (WhatsApp, Telegram, SMS, Email, Notes, etc.) on supported devices (HTTPS / Web Share API).
- Automatically falls back to one-click **clipboard copy** on unsupported platforms.
- Smart contextual formatting:
  - **Grouped mode**: Organized by supermarket aisle/category with family headers and emoji icons.
  - **Flat mode**: Each product listed with its dedicated colorful family emoji and item quantities.

### 🎨 Color Themes (Palette Customizer)
- Personalize the app's look and feel with a palette of vibrant themes: **Emerald Green (Default), Classic Blue, Purple, Amber, Rose, and Teal**.
- Selectable in Settings via clean, icon-based color swatches.
- Dynamically updates header navigation, action buttons, active item tints, category chips, and floating buttons.

### 🔤 Font Size & Typography Options
- Three distinct text sizes: **Medium (בינוני)**, **Large (גדול)** (Default), and **Extra Large (גדול מאוד)**.
- **Bold Text (הדגשת טקסט)**: Optional high-contrast toggle for thicker, highly legible typography across the app (enabled by default for maximum readability).
- Responsive layout designed to scale without overflowing settings or modals.

### 🔍 Flexible Search & Add
- Choose between a classic **Top Search Bar** or a mobile-friendly **Floating Action Button (+)** in Settings.
- Live trilingual autocomplete search matching names across all supported languages.
- Automatically prompts for category/family assignment when typing a new custom item.

### ↩️ Full Multi-Level UNDO
- Dedicated **Undo button** in the header.
- Reverses accidental deletions, list clearing, additions, checking off items, or catalog changes.
- Supports keyboard shortcut: `Ctrl + Z` / `Cmd + Z`.

### 🌐 Trilingual Support (עברית | English | Русский)
- Instant one-click language toggle across the entire application.
- Full RTL (Right-to-Left) and LTR layout switching.
- Seamless localization for all UI texts, categories, and 460+ products.

### 🌙 Dark Mode
- Smooth light/dark theme transition with persistent user preference and RTL-aware toggle animation.

### 📬 Direct Feedback
- Clickable "Made by Seawave" footer in Settings to send instant feedback or suggestions directly via email.

### 📱 Installable Progressive Web App (PWA)
- Works on **Android, iPhone, and Desktop**.
- Install directly from browser ("Install App" / "Add to Home Screen") as a native-feeling standalone app.
- **100% Offline Capable**: Powered by a Service Worker and local storage cache; requires no active internet or Wi-Fi while shopping in the supermarket.

### 💾 Zero-Cloud Privacy
- All lists, custom products, and usage statistics are stored strictly on your local device (`localStorage`).
- No account registration, tracking, or external database required.

---

## 🚀 Live Demo & Deployment

This project is fully static and requires **no build step or backend**. It can be deployed in seconds to:
- **GitHub Pages**
- **Netlify**
- **Vercel**
- Or served locally with any HTTP server (e.g. PowerShell `server.ps1`, Python `http.server`, Live Server, etc.)

### Deploying to GitHub Pages:
1. Fork or clone this repository.
2. In your GitHub repository, go to **Settings** > **Pages**.
3. Under **Branch**, select `main` (root) and click **Save**.
4. Your grocery app will be live at `https://<your-username>.github.io/<repository-name>/`.

---

## 📁 Project Structure

```text
├── index.html            # Main application layout, styles, and core logic (v1.5)
├── translations.js       # Comprehensive trilingual dictionary (Hebrew, English, Russian) & categories
├── list_categorized.xlsx # Categorized product catalog with estimated Israeli market prices
├── manifest.json         # PWA Web App Manifest (app name, icons, display mode)
├── sw.js                 # Service Worker for offline caching and standalone execution (v1.5)
├── icon-192.png          # 192x192 app launcher icon
├── icon-512.png          # 512x512 splash screen / store icon
├── netlify.toml          # Optional Netlify configuration header rules
├── server.ps1            # Lightweight high-performance local WiFi development server
└── README.md             # Project documentation
```

---

## 🛠️ Technologies Used

- **HTML5 & Vanilla JavaScript (ES6+)**
- **Tailwind CSS** (via CDN with dynamic theme variables and dark mode support)
- **FontAwesome 6** (Icons)
- **SheetJS (xlsx)** (Client-side spreadsheet engine)
- **Web Share API & Clipboard API**
- **Screen Wake Lock API**
- **Service Worker & Cache API** (Offline PWA)

---

## 📄 License & Credits

© Made with ❤️ by **seawave**.  
Feedback & Suggestions: [seawave2@gmail.com](mailto:seawave2@gmail.com?subject=Grocery%20List%20Feedback)  
Licensed under the [MIT License](LICENSE).
