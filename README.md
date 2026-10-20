# 🛒 Smart Grocery List App

A modern, fast, lightweight, and fully customizable **Progressive Web App (PWA)** designed to make grocery shopping and list management effortless. Built with vanilla JavaScript, Tailwind CSS, FontAwesome icons, and complete offline capability.

---

## 🌟 Overview & Key Architecture

The application is structured around a fast, intuitive **Two-List Architecture** designed for real-world supermarket shopping:

1. **Active Shopping List**: Displays items you currently plan to buy.
   - **Full Mode**: Checking off an item marks it with a strike-through animation and smoothly transfers it into a collapsible "Checked-off Items" basket.
   - **Simple Mode**: Checking off an item immediately removes it from the list and returns it directly to the available catalog below without accumulating a checked-off list.
2. **Available Catalog**: A comprehensive database of 460+ popular grocery items.
   - Filterable by department / aisle, searchable with real-time multilingual autocomplete, and sortable by frequency of use, alphabetical order, or category.
   - Selecting any catalog item instantly adds it to your active shopping list.

---

## ✨ Features

### 🎛️ Header Mode Switcher
- **Segmented Control in Top Bar**: Easily accessible directly next to the Help icon in the sticky top navigation bar.
- **Instant One-Tap Toggle**: Quickly switch between **Full Mode** (all features and badges enabled) and **Simple Mode** (clean, minimalist interface).
- **Silent & Responsive**: Visually highlights the selected mode directly on the button with zero disruptive popup alerts.

### 🧩 Modular UI Components Customizer
- **Granular Feature Checkboxes**: Tailor the user interface to your exact workflow via Settings > General > "UI Components Customizer". You can independently enable or disable:
  - **Purchased Items List**: Separate collapsible container for completed items (when disabled, checking off items removes them directly back to the available catalog).
  - **Shopping Progress Bar**: Progress meter and percentage indicator at the top of the shopping list.
  - **Quantity Controls**: Plus and minus buttons on list items to adjust quantities.
  - **Aisle Grouping**: Automatic sorting and section dividers by supermarket aisles.
  - **Catalog Category Carousel**: Horizontal scrollable category filter chips above the catalog.
  - **Category Tags & Emojis**: Department labels and emojis displayed beneath item names.
- **One-Click Presets**:
  - **Reset to Simple Mode (Default)**: Unchecks all 6 modules for an ultra-clean, distraction-free interface.
  - **Full Mode (All Features)**: Enables all 6 modules simultaneously.
- **Dynamic Status Indicator**: Displays your active configuration badge (`Simple`, `Full`, or `Custom (X/6)`) in Settings.

### 📊 Ultra-Compact Shopping Progress Bar
- Slim, single-row progress tracker displaying completed items and percentage (e.g., `🛒 3 of 8 (38%)` with a sleek 6px rounded bar).
- Automatically hidden when the shopping list is empty or when the progress bar module is turned off.
- Celebratory completion indicator when all items on your list are purchased.

### 🔖 Saved Lists & Pre-made Templates
- Save any current shopping basket under a custom name (or auto-generated timestamp) for recurring weekly or monthly routines.
- Two loading options:
  - **Add to Cart**: Merges saved template items and their quantities into the current cart.
  - **Load as New**: Replaces the active shopping list with the saved template.
- Includes **6 curated default templates**:
  - *Weekly Essentials* (produce, dairy, bakery, and staples)
  - *Shabbat & Hosting*
  - *BBQ & Grilling*
  - *Cleaning & Home Maintenance*
  - *Healthy Breakfast & Muesli*
  - *Italian Night (Pasta & Pizza)*
- Quick template deletion with a single tap, plus full Undo support.

### 💰 Estimated Prices & Live Basket Summary
- Integrated price database for 460+ items in Israeli Shekels (NIS ₪).
- Accurate pricing per kilogram for fruits, vegetables, and weighted goods.
- Optional toggle in Settings with a dynamic last-updated date indicator.
- Real-time basket summary bar calculating the estimated total cost of both active items and purchased items.
- Non-intrusive micro-price badges placed to keep product titles readable and clear.

### 💡 Keep Screen Awake
- Prevents your mobile display from dimming or locking while navigating supermarket aisles.
- Powered by the native **Screen Wake Lock API** (active when served over HTTPS).

### 📤 Export & Multi-Platform Sharing
- Share your active shopping list with a single click via the "Share" button in the list header.
- Opens the native **mobile share sheet** (WhatsApp, Telegram, Messages, Email, Notes, etc.) on supported devices via the Web Share API.
- Automatically falls back to one-click **clipboard copy** on unsupported browsers.
- Automatically formats items neatly:
  - *Grouped view*: Organized by store aisle with department titles and emojis.
  - *Flat view*: Clean list with item emojis and quantities.

### 🎨 Theme Color Palette
- Choose from 6 interface accent themes: **Emerald Green (Default), Classic Blue, Purple, Amber, Rose, and Teal**.
- Seamlessly updates top navigation, active buttons, category chips, and floating elements.

### 🔤 Typography & Contrast Controls
- Three selectable font sizes: **Medium**, **Large (Default)**, and **Extra Large**.
- **Bold Text Mode**: High-contrast, bolder typography across the application for enhanced readability under bright supermarket lights.

### 🔍 Flexible Search & Input Layout
- Choose between a classic **Top Search Bar** or a mobile-friendly **Floating Action Button (+)** in Settings.
- Real-time trilingual autocomplete search matching names across all supported languages.
- Prompts for department / category assignment when adding a custom, unlisted product.

### ↩️ Multi-Level Undo
- Header Undo button reverses accidental deletions, additions, checking off items, list clearing, or template loading.
- Full keyboard shortcut support: `Ctrl + Z` / `Cmd + Z`.

### 🌐 Trilingual Localization & RTL/LTR
- Instant language switching across the entire app: **Hebrew (עברית)**, **English**, and **Russian (Русский)**.
- Full layout mirroring supporting Right-to-Left (RTL) for Hebrew and Left-to-Right (LTR) for English and Russian.
- Complete localization for all 460+ items, categories, buttons, tooltips, and modal guides.

### 🌙 Dark Mode
- Built-in Dark Theme with persistent preferences, styled contrast borders, and smooth transition animations.

### 📱 Installable Progressive Web App (PWA)
- Fully installable on **Android, iOS, macOS, Windows, and Linux** ("Install App" / "Add to Home Screen").
- Operates standalone without browser address bar clutter.
- **100% Offline Capable**: Cached by a dedicated Service Worker; requires no active mobile data or Wi-Fi inside supermarkets.

### 🔒 Zero-Cloud Privacy
- All lists, templates, custom products, and usage counters are stored strictly on your local device (`localStorage`).
- No user accounts, logins, telemetry, or remote tracking.

---

## 🚀 Deployment & Installation

Because the application is built entirely with standard web technologies, it requires **no build step, compilers, or server-side runtimes**. It can be deployed in seconds to any static hosting provider:

- **Netlify**: Drag and drop the release `.zip` directly into the Netlify dashboard.
- **GitHub Pages**: Push the repository to GitHub and enable Pages in repository settings under the `main` branch.
- **Vercel / Cloudflare Pages**: Connect the repository for instant static deployment.
- **Local Network (Wi-Fi)**: Run the included `server.ps1` script (or Python `python -m http.server 8080`) to access the app across any device connected to your local Wi-Fi.

---

## 📁 Project Directory Structure

```text
├── index.html            # Main application layout, styles, and logic
├── translations.js       # Trilingual dictionary (Hebrew, English, Russian) & product mappings
├── list_categorized.xlsx # Product catalog spreadsheet with estimated market pricing
├── manifest.json         # PWA Web App Manifest (display mode, name, theme colors)
├── sw.js                 # Service Worker for offline execution and asset caching
├── icon-192.png          # 192x192 app launcher icon
├── icon-512.png          # 512x512 splash screen / store icon
├── netlify.toml          # Netlify configuration and HTTP caching headers
├── server.ps1            # High-performance local HTTP server script for development & Wi-Fi testing
└── README.md             # Project documentation
```

---

## 🛠️ Technologies Used

- **HTML5 & Vanilla JavaScript (ES6+)**
- **Tailwind CSS** (via CDN with dynamic theme color variables and dark mode classes)
- **FontAwesome 6** (Vector icons)
- **SheetJS (xlsx)** (Client-side spreadsheet parsing)
- **Web Share API & Clipboard API** (Native sharing)
- **Screen Wake Lock API** (Screen management)
- **Service Worker & Cache API** (Offline PWA)

---

## 📄 License & Credits

Created by **seawave**.  
Feedback & Suggestions: [seawave2@gmail.com](mailto:seawave2@gmail.com?subject=Grocery%20List%20Feedback)  
Licensed under the [MIT License](LICENSE).
