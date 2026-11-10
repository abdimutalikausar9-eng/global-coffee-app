# GLOBAL COFFEE — COMMERCIAL MOBILE APPLICATION (COYOTE REDESIGN)

This repository contains the visual interface redesign of the **Global Coffee** customer web app, engineered to reflect the design language, layout hierarchy, and visual restraint of the official Global Coffee (Coyote) mobile application.

---

## 🎨 Design System & Visual Redesign Highlights

### 1. Typography & Numerals
- **Typeface:** `Inter` sans-serif system (`400`, `500`, `600`, and `700` weights).
- **Tabular Numerals:** Configured with `font-variant-numeric: tabular-nums` and tighter letter-spacing (`-0.011em` to `-0.03em`) for banking/retail-grade price alignment, timer displays, and bonus balances.
- **Currency System:** Standardized to **₸ (Kazakhstani Tenge)** across the entire store catalog, order calculation, delivery fee, bonuses, and payment summary (e.g. `1 850 ₸`, `2 100 ₸`, `850 ₸`).

### 2. Complete Removal of Unicode Emojis
- **Zero Decorative Emojis:** All decorative emojis have been eliminated from every screen, modal, and button.
- **Consistent Minimalist SVG Icons:** Replaced with clean, Lucide-style outline inline SVG icons with unified stroke weight (`1.8px` / `2px`), consistent bounding boxes, and alignment:
  - Navigation: Home, Compass/Menu, Bag/Orders, Gift/Bonuses, User/Profile.
  - Action elements: Chevron chevrons, Cart, Clock, Pin, Heart favorites, Sliders filter, Steppers, Call & Message actions.

### 3. Storefront & Menu Layout (Screenshot 2 Reference)
- **Top Header:** Clean brand identity with Global Coffee mark, real-time branch status with "Change" action, notification trigger, and cart pill with live count and subtotal.
- **Promotional Hero Banner:** Warm bronze gradient card ("Your Daily Coffee, Ready In One Tap / 60% Off") paired with clean coffee imagery and pill button.
- **Category Filter Pills:** Horizontal pill navigation ("All", "Hot Coffee", "Cold Coffee", "Matcha & Tea", "Lemonades", "Bakery & Sweets", "Snacks") featuring solid dark espresso active state (`#1F140E`).
- **Product Cards:** Clean cards with subtle border `#E8E2DB`, rating, calories/volume, price in `₸`, and minimalist add trigger.

### 4. Drink Customization Sheet (Screenshot 2 Reference)
- Centered product photography with back navigation button and favorite toggle.
- Product title with inline `[-] 1 [+]` quantity stepper.
- Rating & preparation time: `4.8 (600) • 20-30 min`.
- **Cup Size Pills:** Small (+0 ₸), Medium (+300 ₸), Large (+550 ₸).
- **Sugar Level Pills:** Normal, Less, No sugar, Extra sugar.
- **Milk Options & Syrups:** Regular milk, Lactose-free milk, Oat milk, Almond milk, Vanilla, Caramel, Hazelnut.
- **Extra Ingredients:** Extra espresso shot, Extra milk, Extra syrup, Whipped cream.
- **Sticky CTA Bar:** Dark espresso pill button with dynamic price updates.

### 5. Loyalty & Bonus Dashboard (Screenshot 1 Reference)
- Directly modeled after the official Global Coffee points screen:
  - Header: "Your points" with large tabular numeral (`1 500 ₸`).
  - Card: "Expires on December 31, 2026" with clock icon.
  - Reward rows: "Your rewards >", "1 000 ₸ off coupon", "Ways to earn >", "Ways to redeem >".
  - Tier Progress Card: "Gold Barista > Earn 500 Points by Dec 31, 2026 to reach Platinum" with terracotta progress bar.

### 6. Order Tracking & 2GIS Map
- 5-stage timeline stepper with clean vector badges.
- Courier card (Daniyar K., 4.95 Rating, E-scooter) with call/message actions.
- Interactive 2GIS map integration with live route line and simulated GPS courier marker.
- Stage testing toolbar with quick stage buttons and auto-play simulation.

### 7. Bottom Navigation Bar (Screenshot 2 Reference)
- Fixed dark espresso bar (`#1F140E`) with outline SVG icons for **Home**, **Menu**, **Orders**, **Bonuses**, and **Profile**.

---

## 🚀 How to Run on Windows in Google Chrome

1. Navigate to:
   ```text
   C:\Users\Admin\.gemini\antigravity\scratch\global-coffee-app
   ```
2. Double-click [index.html](file:///C:/Users/Admin/.gemini/antigravity/scratch/global-coffee-app/index.html) or right-click and select **Open with → Google Chrome**.
3. Direct Chrome address:
   ```text
   file:///C:/Users/Admin/.gemini/antigravity/scratch/global-coffee-app/index.html
   ```
