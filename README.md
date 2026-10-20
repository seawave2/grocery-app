# 🛒 Smart Grocery List App (רשימת קניות חכמה)

A modern, fast, lightweight, and customizable **Progressive Web App (PWA)** for managing your shopping and grocery lists effortlessly. Built with clean vanilla JavaScript, Tailwind CSS, FontAwesome icons, and complete offline capability.

---

## ✨ Key Features

- **⚡ Two-List Smart Architecture**:
  - **1. Active Shopping List**: Items currently needed. Click anywhere on an item card to check it off with a strike-through and smooth removal.
  - **2. Available Catalog**: Fast selection from a rich database of 460+ items sorted by frequency of use, alphabetical order, or aisle / family. Clean catalog header without unnecessary counters.

- **🔖 Saved Lists & Pre-made Templates (רשימות שמורות ותבניות)**:
  - Save your active shopping cart under a custom name (or auto-generated date) for recurring use.
  - Quick access from the active list header with two loading modes:
    - **➕ Add to Cart (הוסף לסל)**: Merges template items and quantities into the current cart.
    - **🔄 Load as New (טען כחדשה)**: Replaces the current cart with the template list.
  - Delete saved lists with a single tap (🗑️).
  - Includes **6 built-in, curated templates**:
    - *סל בסיסי שבועי* (Weekly Essentials)
    - *שבת ואירוח* (Shabbat & Hosting)
    - *מנגל ועל האש* (BBQ & Picnic)
    - *ניקיון ותחזוקת הבית* (Cleaning & Home Supplies)
    - *בוקר בריא ומוזלי* (Healthy Breakfast & Muesli)
    - *ערב איטלקי - פסטה ופיצה* (Italian Pasta & Pizza Night)
  - Full Undo (`Ctrl+Z`) support for all template actions.

- **💰 Estimated Prices & Live Basket Calculator (מחירים משוערים וסיכום סל)**:
  - Realistic Israeli supermarket price database for 460+ products (updated in NIS ₪).
  - Accurate pricing per 1 kg for fruits, vegetables, and weighted goods.
  - Toggle on/off in Settings: "הצג מחירים משוערים" with dynamic last-updated date indicator.
  - Real-time basket summary bar calculating the estimated total cost of active items and already purchased items.
  - Clean, unbolded micro-price badges placed thoughtfully to ensure product names always remain clearly visible.

- **💡 Keep Screen Awake (מסך דולק תמיד)**:
  - Convenient toggle in Settings to prevent your phone screen from dimming or locking while navigating supermarket aisles.
  - Powered by the native **Screen Wake Lock API** (requires HTTPS like Netlify or GitHub Pages).

- **✅ Collapsible Purchased Items (פריטים שנקנו)**:
  - Checked-off items smoothly move into a collapsible accordion section.
  - Dedicated button to clear all purchased items with full multi-level Undo support.

- **📤 Export & Share Shopping List**:
  - Export and share your active shopping list with a single click via the **"שתף" (Share)** button in the list header.
  - Opens the native **mobile share sheet** (WhatsApp, Telegram, SMS, Email, Notes, etc.) on supported devices (HTTPS / Web Share API).
  - Automatically falls back to one-click **clipboard copy** on unsupported platforms.
  - Smart contextual formatting:
    - **Grouped mode**: Organized by supermarket aisle/category with family headers and emoji icons.
    - **Flat mode**: Each product listed with its dedicated colorful family emoji and item quantities.

- **🎨 Color Themes (Palette Customizer)**:
  - Personalize the app's look and feel with a palette of vibrant themes: **Emerald Green (Default), Classic Blue, Purple, Amber, Rose, and Teal**.
  - Selectable in Settings via clean, icon-based color swatches.
  - Dynamically updates header navigation, action buttons, active item tints, category chips, and floating buttons.

- **🔤 Font Size & Typography Options**:
  - Three distinct text sizes: **Medium (בינוני)**, **Large (גדול)** (Default), and **Extra Large (גדול מאוד)**.
  - **Bold Text (הדגשת טקסט)**: Optional high-contrast toggle for thicker, highly legible typography across the app (enabled by default for maximum readability).
  - Responsive layout designed to scale without overflowing settings or modals.

- **🧼 Simple Mode (Classic Clean UI)**:
  - Optional one-click toggle in Settings for users who prefer the original ultra-clean, minimalist interface.
  - Disables advanced UI badges, quantity controls, and floating action buttons, presenting a streamlined, distraction-free list.

- **🔢 Item Quantities & Aisle Grouping**:
  - Increment / decrement quantity counters ($+$ / $-$) directly on active shopping list items.
  - Quick toggle button in the list header to show or hide quantity counters.
  - Option to group active items by supermarket aisle/category.

- **🔍 Flexible Search & Add**:
  - Choose between a classic **Top Search Bar** or a mobile-friendly **Floating Action Button (+)** in Settings.
  - Live trilingual autocomplete search matching names across all supported languages.
  - Automatically prompts for category/family assignment when typing a new custom item.

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

- **📬 Direct Feedback**:
  - Clickable "Made by Seawave" footer in Settings to send instant feedback or suggestions directly via email.

- **📱 Installable Progressive Web App (PWA)**:
  - Works on **Android, iPhone, and Desktop**.
  - Install directly from browser ("Install App" / "Add to Home Screen") as a native-feeling standalone app.
  - **100% Offline Capable**: Powered by a Service Worker and local storage cache; requires no active internet or Wi-Fi while shopping in the supermarket.

- **💾 Zero-Cloud Privacy**:
  - All lists, custom products, and usage statistics are stored strictly on your local device (`localStorage`).
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
├── index.html            # Main application layout, styles, and core logic
├── translations.js       # Comprehensive trilingual dictionary (Hebrew, English, Russian) & categories
├── list_categorized.xlsx # Categorized product catalog with estimated Israeli market prices
├── manifest.json         # PWA Web App Manifest (app name, icons, display mode)
├── sw.js                 # Service Worker for offline caching and standalone execution
├── icon-192.png          # 192x192 app launcher icon
├── icon-512.png          # 512x512 splash screen / store icon
├── netlify.toml          # Optional Netlify configuration header rules
└── README.md             # Project documentation
```

---

## 🛠️ Technologies Used

- **HTML5 & Vanilla JavaScript (ES6+)**
- **Tailwind CSS** (via CDN with dynamic theme variables and dark mode support)
- **FontAwesome 6** (Icons)
- **SheetJS (xlsx)** (Client-side spreadsheet engine)
- **Web Share API & Clipboard API**
- **Service Worker & Cache API** (Offline PWA)

---

## 📄 License & Credits

© Made with ❤️ by **seawave**.  
Feedback & Suggestions: [seawave2@gmail.com](mailto:seawave2@gmail.com?subject=Grocery%20List%20Feedback)  
Licensed under the [MIT License](LICENSE).
