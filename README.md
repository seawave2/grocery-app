# 🛒 GroceryFlow (v1.7)

A modern, fast, lightweight, and fully customizable **Progressive Web App (PWA)** designed to make grocery shopping and list management effortless. Built with vanilla JavaScript, Tailwind CSS, FontAwesome icons, and complete offline capability.

---

## 🌟 Overview & Key Architecture

The application is structured around a fast, intuitive **Two-List Architecture** designed for real-world supermarket shopping:

1. **Active Shopping List**: Displays items you currently plan to buy.
   - **Full Mode**: Checking off an item marks it with a strike-through animation and smoothly transfers it into a collapsible "Checked-off Items" basket.
   - **Simple Mode**: Checking off an item immediately removes it from the list and returns it directly to the available catalog below without accumulating a checked-off list.
2. **Available Catalog**: A comprehensive database of 525+ popular grocery items.
   - Filterable by department / aisle, searchable with real-time multilingual autocomplete, and sortable by frequency of use, alphabetical order, or category.
   - Selecting any catalog item instantly adds it to your active shopping list.

---

## ✨ Features

### 🏪 Supermarket Focus Mode
- **One-Tap In-Store Focus**: Dedicated storefront button (`🏪`) in the top navigation bar instantly hides the entire 525-product catalog, categories, search, and sort controls.
- **Enlarged Touch Targets**: Shopping list cards expand to a spacious layout with generous padding, making them effortless to tap with one thumb while walking through supermarket aisles.
- **High-Visibility Typography**: Item names scale up to a bold, prominent size (`1.25rem / 20px Bold`) with enlarged checkmark circles (`1.55rem / 25px`) for instant reading from shopping cart phone mounts or arm's length.
- **Quick Exit Banner**: A slim indicator at the bottom of the list confirms Supermarket Mode is active and provides a single-tap "Show Catalog" button to return to catalog browsing anytime.
- **Persistent State**: Preserved automatically in local storage across browser reloads.

### 🍞 Dedicated Product Emojis
- **Item-Specific Visual Icons**: Over 85% of catalog products feature tailored, specific emojis (e.g., 🍞 bread, 🥖 baguette, 🫓 pita, 🥛 milk, 🥚 eggs, 🧈 butter, 🧀 cheese, 🍅 tomatoes, 🥒 cucumbers, 🥕 carrots, 🧅 onions, 🥔 potatoes, 🍎 apples, 🍌 bananas, 🍗 chicken, 🥩 beef, 🐟 fish, ☕ coffee, 🍵 tea, 🍫 chocolate, 🍿 snacks, 🧼 soap, 🧻 paper towels, 🍼 baby supplies, 🐶 dog food, 🐱 cat food) rather than only generic department icons.
- **Omnipresent Integration**: Product emojis appear seamlessly across active list cards, purchased items, the master catalog, autocomplete search suggestions, list import previews, price editing modals, and native WhatsApp sharing.

### 💾 Data Backup & Restore
- **Built-in Local Backup**: Located under Settings > Advanced (directly above Interface Language).
- **One-Click Export**: Generates and downloads a lightweight JSON backup file containing all active cart items, purchased history, item notes, custom quantities, user-defined prices, custom products, saved templates, and design preferences.
- **Safe Import & Restore**: Validate and load any backup file on a new device or browser, with confirmation protection before overwriting and seamless automatic refresh.
- **Zero Cloud Required**: All data operations remain strictly local to your device for total privacy.

### 🎛️ Balanced Header & Mode Switcher
- **Ergonomic Top Navigation Bar**: Features a balanced layout with Help (`?`) and the Mode Switcher grouped on the right (in RTL), the custom **GroceryFlow** logo centered, and Supermarket Mode (`🏪`), Settings (`⚙️`), and Undo (`↩️`) grouped on the left.
- **Header Mode Switcher**: Compact segmented toggle allows instant switching between **Full Mode** (all feature badges and modules active) and **Simple Mode** (clean, minimalist interface).
- **Default on First Install**: The application launches in **Simple Mode** by default on fresh installations, providing a clean, frictionless start.

### ✏️ Item Notes & Catalog Product Editing
- **Dedicated Pencil Action Button**: Each item card in the catalog includes an edit button (`✏️`) next to the delete trash can.
- **Long-Press Protection**: Requires a 500ms press-and-hold (with visual scale animation and haptic feedback) to open the editor, preventing accidental clicks. A short tap provides a helpful guidance toast.
- **Comprehensive Product Editor**:
  - **Product Name**: Rename items or fix typos.
  - **Category / Aisle**: Reassign items to any store aisle via a clean dropdown.
  - **Item Notes**: Add custom shopping remarks (e.g., *"Thinly sliced"*, *"Firm only"*, *"On sale only"*).
- **Subtle Visual Feedback**: Products with active custom notes highlight their pencil icon in emerald green and display the note as an elegant italic subtitle with a `💬` icon under the product name in both the active shopping list and catalog.
- **Native Sharing Integration**: Custom notes are automatically included when sharing lists to WhatsApp or copying to the clipboard (e.g., `• 🧀 Yellow Cheese (1 pcs) — Thinly sliced`).
- **Complete Undo Integration**: Any product edit or rename can be reverted immediately via Undo (`Ctrl+Z`).

### 🔍 Quick-Clear Search & Filter Fields
- **One-Tap 'X' Clearing**: Both the main product search bar and the catalog filter field feature a discrete gray clear button (`fa-xmark`) that appears when typing to instantly clear input in a single tap.
- **Keyboard Shortcuts**: Pressing the `Escape` key inside search inputs clears the text and closes autocomplete suggestions.

### 🧩 Modular UI Components Customizer
- **Granular Feature Checkboxes**: Tailor the user interface to your exact workflow via Settings > General > "UI Components Customizer". You can independently enable or disable:
  - **Purchased Items List**: Separate collapsible container for completed items.
  - **Shopping Progress Bar**: Progress meter and percentage indicator at the top of the shopping list.
  - **Quantity Controls**: Plus and minus buttons on list items to adjust quantities.
  - **Aisle Grouping**: Automatic sorting and section dividers by supermarket aisles.
  - **Catalog Category Carousel**: Horizontal scrollable category filter chips above the catalog.
  - **Category Tags & Emojis**: Department labels and emojis displayed beneath item names.
- **One-Click Presets**:
  - **Reset to Simple Mode (Default)**: Unchecks all modules for an ultra-clean, distraction-free interface.
  - **Full Mode (All Features)**: Enables all modules simultaneously.
- **Dynamic Status Indicator**: Displays your active configuration badge (`Simple`, `Full`, or `Custom (X/6)`) in Settings.

### 📊 Ultra-Compact Shopping Progress Bar
- Slim, single-row progress tracker displaying completed items and percentage (e.g., `🛒 3 of 8 (38%)` with a sleek 6px rounded bar).
- Automatically hidden when the shopping list is empty or when the progress bar module is turned off.
- Celebratory completion indicator when all items on your list are purchased.

### 🔖 Saved Lists & Pre-made Templates
- Save any current shopping basket under a custom name for recurring weekly or monthly routines.
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

### 📋 Smart Text & Message Import (Paste)
- **Instant Shopping List Parsing**: Paste any freeform text or WhatsApp message directly via the "Paste" (`הדבק`) button on the active shopping list bar.
- **Intelligent Recognition**: Automatically identifies items from the 525+ product database, extracts quantities (e.g., `3 חלב`, `2 bread`, `1 kg tomatoes`), resolves plural and singular forms, and filters out conversational filler.
- **Interactive Review Modal**: Preview recognized products, toggle individual items with checkboxes, adjust quantities with stepper buttons (`-` / `+`), and optionally add unrecognized items as custom products before adding them all to your active shopping list in a single click.
- **Full Undo Support**: Easily reverse any batch import operation with a single tap of the Undo (`בטל`) button or `Ctrl+Z`.

### 💰 Estimated Prices & Live Basket Summary
- Integrated price database for 525+ items in Israeli Shekels (NIS ₪) with accurate pricing per kilogram for fruits, vegetables, and weighted goods.
- Default database prices are benchmarked to average retail shelf prices in leading supermarket chains, with basic staples reflecting officially regulated consumer prices.
- Optional toggle in Settings with a dynamic last-updated date indicator and BETA badge.
- Real-time basket summary bar calculating the estimated total cost of both active items and purchased items.
- Dedicated `🏷️` price tag icon on items with long-press support to set or edit custom item prices independently.

### 💡 Keep Screen Awake
- Prevents your mobile display from dimming or locking while navigating supermarket aisles.
- Powered by the native **Screen Wake Lock API** (active when served over HTTPS).

### 📤 Export & Multi-Platform Sharing
- Share your active shopping list with a single click via the "Share" button in the list header.
- Opens the native **mobile share sheet** (WhatsApp, Telegram, Messages, Email, Notes, etc.) on supported devices via the Web Share API.
- Automatically falls back to one-click **clipboard copy** on unsupported browsers.
- Automatically formats items neatly:
  - *Grouped view*: Organized by store aisle with department titles, emojis, and item notes.
  - *Flat view*: Clean list with item emojis, quantities, and item notes.

### 🎨 Theme Color Palette
- Choose from 6 interface accent themes: **Emerald Green (Default), Classic Blue, Purple, Amber, Rose, and Teal**.
- Seamlessly updates top navigation, active buttons, category chips, and floating elements.

### 🔤 Typography & Contrast Controls
- Three selectable font sizes: **Medium**, **Large (Default)**, and **Extra Large**.
- **Responsive Mobile Safeguards**: Fluid responsive layout and modal constraints ensuring seamless display with zero screen overflow, even on compact mobile screens with Extra Large font enabled.
- **Bold Text Mode**: High-contrast, bolder typography across the application for enhanced readability under bright supermarket lights.

### 🔍 Flexible Search & Input Layout
- Choose between a classic **Top Search Bar** or a mobile-friendly **Floating Action Button (+)** in Settings.
- Real-time trilingual autocomplete search matching names across all supported languages.
- Prompts for department / category assignment when adding a custom, unlisted product.

### ↩️ Multi-Level Undo
- Header Undo button reverses accidental deletions, additions, checking off items, product editing, list clearing, or template loading.
- Full keyboard shortcut support: `Ctrl + Z` / `Cmd + Z`.

### 🌐 Trilingual Localization & RTL/LTR
- Instant language switching across the entire app: **Hebrew (עברית)**, **English**, and **Russian (Русский)** with 100% feature and tooltip parity.
- Full layout mirroring supporting Right-to-Left (RTL) for Hebrew and Left-to-Right (LTR) for English and Russian.
- Complete localization for all 525+ items, categories, buttons, tooltips, and modal guides.

### 🌙 Dark Mode
- Built-in Dark Theme with persistent preferences, styled contrast borders, and smooth transition animations.

### 📱 Installable Progressive Web App (PWA)
- Fully installable on **Android, iOS, macOS, Windows, and Linux** ("Install App" / "Add to Home Screen").
- Operates standalone without browser address bar clutter.
- **100% Offline Capable**: Cached by a dedicated Service Worker; requires no active mobile data or Wi-Fi inside supermarkets.

### 🔒 Zero-Cloud Privacy
- All lists, templates, custom products, item notes, custom prices, and usage counters are stored strictly on your local device (`localStorage`).
- No user accounts, logins, telemetry, or remote tracking.

---

## 🚀 Deployment & Installation

Because the application is built entirely with standard web technologies, it requires **no build step, compilers, or server-side runtimes**. It can be deployed in seconds to any static hosting provider:

- **Netlify**: Drag and drop the release `.zip` directly into the Netlify dashboard.
- **GitHub Pages**: Push the repository to GitHub and enable Pages in repository settings under the `main` branch.
- **Vercel / Cloudflare Pages**: Connect the repository for instant static deployment.
- **Local Network (Wi-Fi)**: Run the included `server.ps1` script to access the app across any device connected to your local Wi-Fi.

---

## 📁 Project Directory Structure

```text
├── index.html            # Main application layout, styles, and logic
├── translations.js       # Trilingual dictionary (Hebrew, English, Russian), categories & pricing
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
- **Web Share API & Clipboard API** (Native sharing)
- **Screen Wake Lock API** (Screen management)
- **Service Worker & Cache API** (Offline PWA)

---

## 📄 License & Credits

Created by **seawave**.  
Feedback & Suggestions: [seawave2@gmail.com](mailto:seawave2@gmail.com?subject=Grocery%20List%20Feedback)  
Licensed under the [MIT License](LICENSE).
