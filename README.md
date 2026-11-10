# GLOBAL COFFEE — COMMERCIAL WEB APPLICATION & AI DELIVERY SYSTEM

[![GitHub Pages Deployment](https://img.shields.io/badge/Deployment-GitHub%20Pages-success)](https://abdimutalikausar9-eng.github.io/global-coffee-app/)
[![UI Style](https://img.shields.io/badge/Design-Commercial%20Coyote%20App-1F140E)](https://github.com/abdimutalikausar9-eng/global-coffee-app)
[![Localization](https://img.shields.io/badge/Languages-KZ%20%7C%20RU%20%7C%20EN-D97706)](https://github.com/abdimutalikausar9-eng/global-coffee-app)

A customer-facing web application and AI Delivery Intelligence System for **Global Coffee**, engineered with the visual design language, restrained aesthetic, and layout hierarchy of the official Global Coffee (Coyote) mobile app.

---

## 🔗 Live Application Links

- **Live GitHub Pages URL:** [https://abdimutalikausar9-eng.github.io/global-coffee-app/](https://abdimutalikausar9-eng.github.io/global-coffee-app/)
- **GitHub Repository:** [https://github.com/abdimutalikausar9-eng/global-coffee-app](https://github.com/abdimutalikausar9-eng/global-coffee-app)

---

## 🌟 Key Architecture & Implemented Modules

### 1. Dynamic Sequential Order Progress & Preparation Countdown Timer
Replaces static list-style trackers with a dynamic, sequential order experience:
- **Adaptive Fulfillment Flows:**
  - **Delivery Flow (6 stages):**
    1. Order Confirmed
    2. Preparing Your Coffee
    3. Quality Check & Packing
    4. Courier Assigned (with courier card & direct contact triggers)
    5. On the Way (with live 2GIS route map & simulated GPS tracking)
    6. Delivered (with bonus claim trigger)
  - **Pickup Flow (5 stages):**
    1. Order Confirmed
    2. Preparing Your Coffee
    3. Quality Check & Packing
    4. Ready for Pickup (prominent `#GC-89421` pickup verification code for barista counter; no courier or delivery map)
    5. Order Collected
- **Intelligent Countdown Timers:**
  - Dedicated contextual timer labels: *"Preparation time remaining"*, *"Packaging time"*, *"Estimated courier arrival"*, *"Ready at counter"*.
  - Tabular numerals with zero-jitter monospace layout (`font-variant-numeric: tabular-nums`).
  - **Graceful Delay Handling:** Never advances the order simply because a timer reaches zero. If preparation exceeds standard SLA or staff flags a rush, a delay alert banner appears: *"Preparation is taking longer than expected — our barista is taking extra care during peak rush to ensure barista-grade quality."*

### 2. Smart Map & Live Delivery Tracking
- **2GIS Map Integration:** Interactive map with branch markers (Dostyk Plaza, Mega Alma-Ata, Downtown Flagship, Esentai Mall, Dostyk Medeu).
- **Interactive Map Address Picker:** In checkout, users can click *"Select on 2GIS map"* to drop a pin and set their delivery coordinates directly from the map.
- **Provider Abstraction:** Built on a modular `MapProvider` abstraction capable of swapping between 2GIS Tiles, Leaflet/OSM, or custom vector SDKs without changing application logic.
- **Live Courier Tracking:** Displays delivery route polylines and real-time courier positioning.

### 3. Grounded AI Customer Assistant (AI Concierge)
- **Floating Trigger & Slide-Up Drawer:** Fast access to the AI Concierge via a minimalist sparkles bot icon.
- **Context-Aware Knowledge Engine:**
  - Directly connected to real order state (`State.activeOrder.stage`, `isDelayed`, `fulfillment`, `total`, `bonusBalance`).
  - Strictly truthful: Never hallucinates delivery coordinates, fake confirmation codes, or invented statuses.
  - Quick action prompt pills: *"Where is my coffee?"*, *"Recommend a drink"*, *"What plant milk options exist?"*, *"How do bonuses work?"*, *"Why is there a delay?"*.
  - Answers coffee questions: Specialty bean origin, oat/almond milk options, syrups, and 10% loyalty cashback rules.

### 4. AI Delivery Monitoring & Incident Alert Center (Staff Dashboard)
- Accessible via the top navigation bar toggle (`Role: Customer ⇄ Staff Hub`) or `#view-staff`:
  - **Live SLA Metrics:** Average Preparation SLA (8.2m), Courier Pickup SLA (6.4m), SLA Breach Rate (1.2%), Critical Incidents count.
  - **Incident Resolution Center:** Real-time alert cards for preparation delays, unassigned couriers, and delivery stalls with status workflow (`New` ➔ `In Progress` ➔ `Resolved`).
  - **Live Barista & Courier Operations:** Barista stage progression controls and delay simulator.
  - **SLA Threshold Tuning:** Interactive sliders for maximum preparation time, courier dispatch limits, and courier inactivity timeouts.

### 5. Three-Language System (Қазақша / Русский / English)
- Multi-language switcher available in the top bar (`RU | KZ | EN`) and profile preferences.
- Dynamic key interpolation via `[data-i18n]` and dynamic rendering.
- Complete localized dictionaries in:
  - `translations/kk.json` (Қазақша)
  - `translations/ru.json` (Русский)
  - `translations/en.json` (English)
- **Zero-CORS Embedded Fallback:** Includes `window.TRANSLATIONS` directly inside `index.html` to allow seamless local testing via `file:///` without browser cross-origin policy restrictions.

---

## 🎨 Design System & Commercial Coyote Aesthetic

- **Typography:** `Inter` sans-serif system (`400`, `500`, `600`, and `700` weights).
- **Numerals:** `font-variant-numeric: tabular-nums` for banking/retail-grade price alignment, timers, and bonus balances.
- **Currency System:** Standardized to **₸ (Kazakhstani Tenge)** across the store catalog, order calculation, delivery fee, bonuses, and payment summary (e.g. `1 850 ₸`, `2 100 ₸`, `850 ₸`).
- **Zero Unicode Emojis:** Replaced with clean, Lucide-style outline inline SVG icons with unified stroke weight (`1.8px` / `2px`) and consistent bounding boxes.
- **Storefront & Menu Layout:** Warm espresso brand palette (`#1F140E`, `#D97706`, `#F8F5F1`), horizontal category filter pills, drink customization sheet with cup size, milk options, syrups, and live price recalculation.
- **Loyalty & Rewards Dashboard:** Based on the official Global Coffee points screen: tabular points balance, expiration reminder, coupon tiers, and interactive celebratory confetti animation with Web Audio harmonic chime.

---

## 💻 How to Run Locally on Windows in Google Chrome

1. Navigate to:
   ```text
   C:\Users\Admin\.gemini\antigravity\scratch\global-coffee-app
   ```
2. Double-click [index.html](file:///C:/Users/Admin/.gemini/antigravity/scratch/global-coffee-app/index.html) or open it with Google Chrome:
   ```text
   file:///C:/Users/Admin/.gemini/antigravity/scratch/global-coffee-app/index.html
   ```
3. A pre-packaged archive containing all assets and translations is available at:
   ```text
   C:\Users\Admin\.gemini\antigravity\scratch\global-coffee-app\global-coffee-app.zip
   ```
