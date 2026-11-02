# 🛒 GroceryFlow (v2.4)

A modern, lightning-fast, and fully customizable **Progressive Web App (PWA)** designed to make supermarket grocery shopping and list management effortless, intuitive, and fun. Built with vanilla JavaScript, Tailwind CSS, FontAwesome icons, and complete offline capability.

---

## 🌟 Architecture & Core Workflow

GroceryFlow is built around a practical, real-world **Two-List Architecture** tailored for fast in-store navigation:

1. **Active Shopping List**: Items currently in your cart or on your shopping list.
   - **Full Mode**: Checking off an item marks it with a smooth animation and moves it to a collapsible "Checked-off Items" basket.
   - **Simple Mode**: Checking off an item immediately removes it from the list and returns it directly to the available catalog without accumulating past items.
   - **Aisle Grouping**: Items can be grouped automatically by supermarket department for linear, organized in-store walking routes.
   - **Inline Quantity Controls**: Quick `+` / `-` steppers for effortless quantity adjustments.

2. **Master Product Catalog**: A comprehensive database of 550+ popular grocery items across all supermarket aisles, including specialized sections for **Pet Supplies** (חיות מחמד 🐾) and authentic **Russian Delicatessen** (מעדניה רוסית 🪆).
   - **Quick Add**: Single tap on any catalog card adds it to the active shopping list instantly.
   - **Custom Creation**: Type any unlisted item name to automatically create and save it in the catalog.
   - **Card Long-Press Menu**: Long-press any product card to edit its name, department, custom notes, custom price, or remove it.
   - **Elevated Title Balloon**: Long-pressing a truncated product title in compact grid mode pops an elevated preview balloon floating comfortably above the finger for effortless reading.

---

## ✨ Features & Capabilities

### 🔍 Smart Catalog Search & Category Carousel
- **Department Carousel**: Horizontally scrollable category chips with custom aisle emojis for rapid visual browsing.
- **Smart Department Recognition**: Typing any department/category name in the search bar (e.g., *"ירקות"*, *"בשר ועוף"*, *"מוצרי חלב"*, *"Dairy"*, *"Vegetables"*, *"Овощи"*) automatically shifts the carousel, centers the active chip, and reveals the entire department's products without filtering down to an individual product title.
- **Dedicated Product Search**: Specific product queries (e.g., *"חלב"*, *"לחם"*, *"קפה"*) continue to filter directly for matching items with highlighted matching characters.
- **Multiple Sorting Modes**: Sort catalog items by frequency of use (*"תדירות"*), alphabetical order (*"א'-ב'"*), department (*"מחלקה"*), or price (*"מחיר"*). When dietary filters hide items from the catalog, an unobtrusive indicator is displayed alongside the sorting options.

### 📱 Mobile-First UX & Keyboard Management
- **Dismiss on Scroll / Drag**: Touching or scrolling the catalog product cards automatically dismisses the mobile virtual keyboard (`blur()`), instantly reclaiming 50% of screen space.
- **Native Search/Enter Action**: Equipped with `enterkeyhint="search"`, pressing Enter or Search on mobile keyboards immediately commits the search and closes the keyboard.
- **Quick Keyboard Toggle**: Dedicated keyboard icon button (<i class="fa-solid fa-keyboard"></i>) alongside the search bar for one-tap dismissal.
- **Auto-Dismiss on Department Selection**: The keyboard collapses automatically when a full department name is matched or when tapping any category chip.
- **Extended Bottom Clearance**: Generous `pb-44` bottom spacing ensures all product cards can be scrolled comfortably above sticky bars and virtual keyboards.
- **No-Zoom Policy**: Viewport settings (`maximum-scale=1.0, user-scalable=no, viewport-fit=cover`), touch action manipulation, and gesture event guards prevent accidental pinch-to-zoom or double-tap magnification for an authentic native app touch feel.

### 🌍 Regional Product Catalogs & Dynamic Markets
- **5 Regional Catalogs**: Dynamically switch between **Israel (ישראל)**, **United States (ארצות הברית)**, **Europe (אירופה)**, **Asia (אסיה)**, and **Middle East (המזרח התיכון)**.
- **Authentic Local Assortments**: Dedicated product databases loaded seamlessly from `regional_catalogs.js` and synced with regional Excel catalogs (`catalog_il_market.xlsx`, `catalog_us_market.xlsx`, `catalog_eu_market.xlsx`, `catalog_asia_market.xlsx`, `catalog_arab_market.xlsx`).
- **Intelligent Currency & Language Pairing**: Switching catalog region automatically configures the matching default currency (USD `$`, EUR `€`, ILS `₪`) and switches the interface language to English for international markets (and back to Hebrew when returning to Israel).
- **Metric Standardization**: Cleaned and standardized units across Hebrew catalogs (grams/kg).

### 💎 Modern Frosted Gradient Header & Segmented Screen Switcher
- **Dynamic Gradient Header**: Rich vertical gradient (`linear-gradient(180deg, var(--theme-primary-dark) 0%, var(--theme-primary) 100%)`) with an elegant curved bottom contour (`rounded-b-2xl sm:rounded-b-3xl`), border glow, and depth shadow.
- **Symmetrical Glassmorphic Controls**: Frosted-glass circular squircle buttons for **Help** (עזרה), **Settings** (הגדרות), and **Undo** (בטל), featuring tactile micro-press animations and subtle borders.
- **Symmetrical Segmented Pill Switcher**: Centralized iOS/Material 3 style pill capsule for toggling between **Cart** (סל) and **Catalog** (קטלוג), with a crisp white active indicator and high-contrast theme typography.
- **Directional Symmetrical Alignment**: The "More" / "עוד" action button aligns directly above "View" / "תצוגה" on mobile screens in both RTL and LTR modes, with viewport-safe dropdown positioning that prevents off-screen clipping.

### 🍎 Item-Specific Visual Emojis
- **Tailored Product Icons**: Over 85% of catalog products feature tailored, specific emojis (e.g., 🍞 bread, 🥖 baguette, 🫓 pita, 🥛 milk, 🥚 eggs, 🧈 butter, 🧀 cheese, 🍅 tomatoes, 🥒 cucumbers, 🥕 carrots, 🧅 onions, 🥔 potatoes, 🍎 apples, 🍌 bananas, 🍗 chicken, 🥩 beef, 🐟 fish, ☕ coffee, 🍵 tea, 🍫 chocolate, 🍿 snacks, 🧼 soap, 🧻 paper towels, 🍼 baby supplies, 🐶 dog food, 🐱 cat food, 🥟 pelmeni, 🥫 canned goods) rather than generic aisle icons.
- **Visual Consistency**: Emojis appear throughout active lists, catalog cards, search suggestions, import previews, and WhatsApp sharing.

### 🔥 Nutritional Information (Calories per 100g)
- **Estimated Nutritional Values**: Integrated nutritional database covering 500+ food items with estimated calories per 100g.
- **Independent Setting**: Toggle nutritional calories on or off anytime under General Settings (disabled by default) without affecting price displays.
- **Subtle Visual Presentation**: Displayed as a delicate badge (`🔥 52 ק` / `kcal` / `ккал`) across list items, catalog cards, search results, and product details.

### 🏷️ Estimated Pricing & Basket Totals
- **Realistic Supermarket Prices**: Built-in price estimates based on average retail shelf prices, with official government-regulated pricing for staple products (disabled by default for clean initial setup).
- **Live Basket Sum**: Displays estimated cart totals and updates in real time as items are checked off or quantities are adjusted.
- **Custom Price Editing**: Long-press any product card to override the default price with your own store price or reset back to default.
- **Live Daily Exchange Rates**: Automatic daily updates for USD, EUR, and ILS currency conversions.

### ✏️ Item Notes
- **Shopping Notes**: Add custom remarks to any product (e.g., *"Thinly sliced"*, *"Extra firm"*, *"On sale only"*), displayed as an italic subtitle and included when sharing.

### 🔖 Templates & Saved Lists
- **One-Click Routine Lists**: Save your current shopping basket under custom names (e.g., *"Weekly Essentials"*, *"Shabbat Dinner"*, *"Barbecue"*) for repeated use.
- **Flexible Loading**: Merge saved templates into your existing cart or load them as a fresh list.

### 📋 Smart List Import (Paste from Text)
- **Automatic Recognition**: Paste a WhatsApp message or raw text list into the Import tool; GroceryFlow automatically identifies items, extracts quantities, matches catalog entries, and adds them to your cart with one tap.

### 📤 Instant Sharing
- **Formatted Share Output**: Export your shopping list directly to WhatsApp, SMS, or the clipboard, complete with quantities, custom notes, and aisle groupings.

### 🧩 Modular Interface & Dietary Customizer
- **Dedicated Dual-Tab Customizer Modal**: Accessible directly from Settings via **"התאמת רכיבי ממשק והגבלות תזונה"** (Interface & Dietary Customizer), featuring two tabs:
  - **Interface Tab (ממשק)**: Toggle modular layout components on or off (all enabled by default):
    - Checked-off items basket (`purchasedList`)
    - Shopping progress bar (`progressBar`)
    - List action buttons toolbar (`listActions`)
    - Catalog department carousel (`categoryCarousel`)
    - Category tags and emojis (`categoryTags`)
  - **Dietary & Religious Filters Tab (תזונתי)**: Real-time visibility controls across all regional catalogs based on religious and dietary requirements (all categories checked/visible by default; unchecking hides that category from the catalog and search):
    - 🥩 **Meat, Poultry & Fish (בשר, עוף ודגים)**: Show/hide meat, poultry, and fish (uncheck for vegetarian diets).
    - 🧀 **Dairy & Eggs (מוצרי חלב וביצים)**: Show/hide dairy, cheese, and eggs (uncheck for vegan diets).
    - ✡️ **Non-Kosher (מוצרים שאינם כשרים)**: Show/hide non-kosher products (pork, shellfish, and meat-dairy combinations).
    - ☪️ **Non-Halal (מוצרים שאינם חלאל)**: Show/hide non-halal products (pork and alcohol).
    - 🥓 **Pork (מוצרי חזיר)**: Show/hide pork products (bacon, prosciutto, sausages, lard).
    - 🦐 **Shellfish (פירות ים)**: Show/hide shrimp, calamari, mussels, oysters, and oyster sauce.
    - 🥩 **Beef (בשר בקר ועגל)**: Show/hide beef and veal items (for Hindu or beef-free diets).
    - 🍷 **Alcohol (אלכוהול)**: Show/hide beer, wine, and spirits.
- **Active Dietary Filters Banner & Quick Edit**: When items are hidden from the catalog, an unobtrusive banner displays the active exclusions with a one-tap "שינוי" (Change) button.
- **Elevated Long-Press Tooltip Balloon**: Pressing and holding the active filter notice displays a floating preview balloon showing the full list of excluded items, which dismisses immediately upon release.
- **Discreet Catalog Icon Mode ("הסתר התראה בקטלוג")**: Users can hide the text banner in favor of a sleek, compact slashed-catalog icon button (`fa-boxes-stacked` with a diagonal line) positioned in the header row between "Available Products" and the sort selector.
- **Clean Multilingual Labels**: Native Hebrew labels are refined and free of redundant English culinary annotations, while full English and Russian translations remain accurately synchronized across all tabs and guides.

### 🎨 Themes, Accessibility & Design
- **Theme Color Accents**: Choose from modern color palettes (Emerald, Blue, Purple, Amber, Rose, Teal).
- **Dark Mode**: Fully styled dark theme with high-contrast borders and smooth transitions.
- **Typography Sizing**: Select between Normal, Medium, Large, and Extra Large font sizes, plus an optional Bold Text mode for maximum legibility.
- **Keep Screen Awake (Wake Lock)**: Screen lock prevention while navigating store aisles.

### 🔊 Tactile & Audio Feedback (Haptic Vibration & Scanner Beep)
- **Mobile Haptic Feedback**: Gentle vibration response across interactions, buttons, and list operations (enabled by default for tactile, silent operation).
- **Authentic POS Scanner Beep**: Synthesized in real time using the browser's Web Audio API (`2093 Hz`), producing a crisp, zero-latency cash-register barcode scanner sound when checking off items in the cart (disabled by default, can be toggled on anytime in General Settings).
- **Independent Controls in General Settings**: Sound feedback and vibration feedback can be toggled individually under General Settings.

### 💾 Local Backup & Zero-Cloud Privacy
- **100% Private**: All lists, custom items, notes, prices, and preferences are stored strictly on your local device (`localStorage`). No tracking, accounts, or cloud dependencies.
- **One-Click Backup & Restore**: Export all your data to a lightweight JSON file and restore it effortlessly across devices or browsers.

### 🌐 Comprehensive Multilingual Localization (8 Languages)
- Full, native support for 8 languages across all products, categories, buttons, settings, and help guides:
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
- **100% Offline Capable**: Powered by Service Worker v24 (`grocery-list-v24`) that caches all core application assets, ensuring reliable operation deep inside supermarkets with no mobile signal.

---

## 🛠️ Technologies Used

- **HTML5 & Vanilla JavaScript (ES6+)**
- **Web Audio API** (Real-time synthesizer for checkout scanner audio feedback)
- **Tailwind CSS** (Utility-first styling with dynamic CSS variables and dark mode support)
- **FontAwesome 6** (Vector iconography)
- **Web Share API & Clipboard API** (Native sharing integrations)
- **Service Worker & Cache API** (Reliable offline PWA functionality)

---

## 📄 License & Credits

Created with ❤️ by **seawave**.  
Feedback & Suggestions: [seawave2@gmail.com](mailto:seawave2@gmail.com?subject=Grocery%20List%20Feedback)  
Licensed under the [MIT License](LICENSE).
