# 🛒 GroceryFlow (v2.0)

A modern, lightning-fast, and fully customizable **Progressive Web App (PWA)** designed to make supermarket grocery shopping and list management effortless, intuitive, and fun. Built with vanilla JavaScript, Tailwind CSS, FontAwesome icons, and complete offline capability.

---

## 🌟 Key Architecture & Workflow

GroceryFlow is built around a practical, real-world **Two-List Architecture** tailored for fast in-store navigation:

1. **Active Shopping List**: Items currently in your cart or on your shopping list.
   - **Full Mode**: Checking off an item marks it with a smooth animation and moves it to a collapsible "Checked-off Items" basket.
   - **Simple Mode**: Checking off an item immediately removes it from the list and returns it directly to the available catalog without accumulating past items.
2. **Master Product Catalog**: A comprehensive database of 550+ popular grocery items across all supermarket aisles, including specialized sections for **Pet Supplies** (חיות מחמד 🐾) and authentic **Russian Delicatessen** (מעדניה רוסית 🪆).
   - Filter by department, search in real-time with multilingual autocomplete, or sort by frequency of use, alphabetical order, or aisle.
   - Tap any catalog card to add it to your shopping cart instantly.

---

## ✨ Features

### 🏪 Supermarket Focus Mode
- **One-Tap Storefront Mode**: A dedicated button (`🏪` / `מצב`) in the header instantly hides the entire product catalog, search bars, and filters, leaving only your active shopping list on the screen.
- **Enlarged Touch Targets**: Shopping cards expand with generous padding and large checkmarks (`25px`) for effortless one-thumb tapping while walking down supermarket aisles or viewing from shopping cart phone mounts.
- **High-Visibility Typography**: Item names scale up to bold, prominent typography for quick, arm's-length readability.
- **Quick Exit Banner**: A slim bottom indicator confirms Supermarket Mode is active and allows instant return to the catalog anytime.

### 🍎 Comprehensive Catalog with Tailored Emojis
- **Item-Specific Visual Icons**: Over 85% of catalog products feature tailored, specific emojis (e.g., 🍞 bread, 🥖 baguette, 🫓 pita, 🥛 milk, 🥚 eggs, 🧈 butter, 🧀 cheese, 🍅 tomatoes, 🥒 cucumbers, 🥕 carrots, 🧅 onions, 🥔 potatoes, 🍎 apples, 🍌 bananas, 🍗 chicken, 🥩 beef, 🐟 fish, ☕ coffee, 🍵 tea, 🍫 chocolate, 🍿 snacks, 🧼 soap, 🧻 paper towels, 🍼 baby supplies, 🐶 dog food, 🐱 cat food, 🥟 pelmeni, 🥫 canned goods) rather than generic aisle icons.
- **Visual Consistency**: Emojis appear throughout active lists, catalog cards, search suggestions, import previews, and WhatsApp sharing.

### 🔥 Nutritional Information (Calories per 100g)
- **Estimated Nutritional Values**: Integrated nutritional database covering 500+ food items with estimated calories per 100g.
- **Independent Setting**: Toggle nutritional calories on or off anytime under General Settings without affecting price displays.
- **Subtle Visual Presentation**: Displayed as a delicate badge (`🔥 52 ק` / `kcal` / `ккал`) across list items, catalog cards, search results, and product details.

### 🏷️ Estimated Pricing & Basket Totals
- **Realistic Supermarket Prices**: Built-in price estimates based on average retail shelf prices, with official government-regulated pricing for staple products.
- **Live Basket Sum**: Displays estimated cart totals and updates in real time as items are checked off or quantities are adjusted.
- **Custom Price Editing**: Long-press any product card to override the default price with your own store price or reset back to default.

### ✏️ Item Notes & Catalog Customization
- **Shopping Notes**: Add custom remarks to any product (e.g., *"Thinly sliced"*, *"Extra firm"*, *"On sale only"*), displayed as an italic subtitle and included when sharing.
- **Full Catalog Control**: Long-press any catalog card to edit its name, reassign its department, update notes, or remove it from the catalog.
- **Custom Product Creation**: Type any unlisted product name in search to automatically create it, assign an aisle, and save it for future trips.

### 🔖 Templates & Saved Lists
- **One-Click Routine Lists**: Save your current shopping basket under custom names (e.g., *"Weekly Essentials"*, *"Shabbat Dinner"*, *"Barbecue"*) for repeated use.
- **Flexible Loading**: Merge saved templates into your existing cart or load them as a fresh list.

### 📋 Smart List Import (Paste from Text)
- **Automatic Recognition**: Paste a WhatsApp message or raw text list into the Import tool; GroceryFlow automatically identifies items, extracts quantities, matches catalog entries, and adds them to your cart with one tap.

### 📤 Instant Sharing
- **Formatted Share Output**: Export your shopping list directly to WhatsApp, SMS, or the clipboard, complete with quantities, custom notes, and aisle groupings.

### 🧩 Modular Interface Customizer
- **Tailor Every Module**: Turn individual interface components on or off according to personal preference:
  - Checked-off items basket
  - Shopping progress bar
  - Inline quantity controls (+/-)
  - Aisle grouping and section dividers
  - Catalog category carousel
  - Category tags and emojis
- **Header View Switcher**: Switch on the fly between **Full Mode** and clean **Simple Mode**.

### 🎨 Themes, Accessibility & Design
- **Theme Color Accents**: Choose from modern color palettes (Emerald, Blue, Purple, Amber, Rose, Slate).
- **Dark Mode**: Fully styled dark theme with high-contrast borders and smooth transitions.
- **Typography Sizing**: Select between Normal, Medium, Large, and Extra Large font sizes, plus an optional Bold Text mode for maximum legibility.

### 💾 Local Backup & Zero-Cloud Privacy
- **100% Private**: All lists, custom items, notes, prices, and preferences are stored strictly on your local device (`localStorage`). No tracking, accounts, or cloud dependencies.
- **One-Click Backup & Restore**: Export all your data to a lightweight JSON file and restore it effortlessly across devices or browsers.

### 🌐 Comprehensive Multilingual Localization (8 Languages)
- Full, native support for 8 languages across all 550+ products, categories, buttons, settings, and help guides:
  - 🇮🇱 **Hebrew (עברית)** - Native RTL layout
  - 🇸🇦 **Arabic (العربية)** - Native RTL layout
  - 🇺🇸 **English** - LTR
  - 🇷🇺 **Russian (Русский)** - LTR
  - 🇪🇸 **Spanish (Español)** - LTR
  - 🇫🇷 **French (Français)** - LTR
  - 🇧🇷 **Portuguese (Português)** - LTR
  - 🇩🇪 **German (Deutsch)** - LTR

### 📱 Installable PWA with Full Offline Capability
- Installable on **Android, iOS, Windows, macOS, and Linux**.
- **100% Offline Capable**: Powered by a Service Worker that caches all core application assets, ensuring reliable operation deep inside supermarkets with no mobile signal.

---

## 🛠️ Technologies Used

- **HTML5 & Vanilla JavaScript (ES6+)**
- **Tailwind CSS** (Utility-first styling with dynamic CSS variables and dark mode support)
- **FontAwesome 6** (Vector iconography)
- **Web Share API & Clipboard API** (Native sharing integrations)
- **Service Worker & Cache API** (Reliable offline PWA functionality)

---

## 📄 License & Credits

Created with ❤️ by **seawave**.  
Feedback & Suggestions: [seawave2@gmail.com](mailto:seawave2@gmail.com?subject=Grocery%20List%20Feedback)  
Licensed under the [MIT License](LICENSE).
