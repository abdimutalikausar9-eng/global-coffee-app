# GLOBAL COFFEE — COMMERCIAL WEB APPLICATION & AI VOICE ORDERING SYSTEM

[![GitHub Pages Deployment](https://img.shields.io/badge/Deployment-GitHub%20Pages-success)](https://abdimutalikausar9-eng.github.io/global-coffee-app/)
[![UI Style](https://img.shields.io/badge/Design-Commercial%20Coyote%20App-1F140E)](https://github.com/abdimutalikausar9-eng/global-coffee-app)
[![Localization](https://img.shields.io/badge/Languages-KZ%20%7C%20RU%20%7C%20EN-D97706)](https://github.com/abdimutalikausar9-eng/global-coffee-app)
[![Voice Ordering](https://img.shields.io/badge/AI-Voice%20Ordering%20%26%20Speech-EF4444)](https://github.com/abdimutalikausar9-eng/global-coffee-app)

A customer-facing web application and AI Delivery & Voice Ordering System for **Global Coffee**, engineered with the visual design language, restrained aesthetic, and layout hierarchy of the official Global Coffee (Coyote) mobile app.

---

## 🔗 Live Application Links

- **Live GitHub Pages URL:** [https://abdimutalikausar9-eng.github.io/global-coffee-app/](https://abdimutalikausar9-eng.github.io/global-coffee-app/)
- **GitHub Repository:** [https://github.com/abdimutalikausar9-eng/global-coffee-app](https://github.com/abdimutalikausar9-eng/global-coffee-app)

---

## 🌟 Implemented Features & UI Improvements

### 1. Introductory Welcome Screen
- **First Screen on Open:** Displays the authentic Global Coffee promotional artwork (`image(4).png`), brand mark, and typography.
- **Brand Identity:** Header tag *"SPECIALTY COFFEE & DELIVERY"*, bold heading **GLOBAL COFFEE APP**, and description.
- **Clean "Enter" Action:** An elegant gold-terracotta pill button (*"Войти в приложение"* / *"Enter Application"*) with smooth fade-out transition into the storefront.

### 2. Simplified, Intuitive Customer Interface
- **Pure Customer Experience:** All employee/employer pages, staff hub dashboards, and role switchers have been completely removed.
- **5 Focused Navigation Tabs:** Home, Menu, Orders, Bonuses, and Profile.

### 3. Preparation Timer Bug Fix & Real Order Sequence
- **Strict Payment Dependency:** Before an order is paid and confirmed, **no preparation timer runs**.
- **Correct Flow:**
  1. Customer selects coffee & bakery items from menu.
  2. Proceeds to checkout and selects Delivery or Pickup.
  3. Completes payment method simulation.
  4. Payment is successfully confirmed.
  5. The order is created (`#GC-XXXXX`) and **ONLY NOW does the preparation countdown timer start**.
- **Dynamic Estimated Time Notification:** Immediately after payment confirmation, displays:
  *"Ваш заказ принят! Ваш заказ будет готов примерно через [X] минут"* (where `[X]` is computed dynamically based on the number of drinks in the cart).
- **Persistent State:** Timer is bound to the order's timestamp (`startTime` + `totalSeconds`) and saved in `localStorage`, so page reloads or tab navigation will never reset or restart the countdown.
- **Never Fake Advancement:** When countdown reaches zero, the order does not arbitrarily jump to ready; instead, a clear delay notice appears explaining that the barista is taking extra care during peak rush.

### 4. Sequential Main-Screen Stages (No Numbered Steps)
- **Elimination of Numbered Labels:** Numbered steps (e.g. *Step 1, Step 2, Step 3, Этап 1 из 6*) have been completely removed.
- **Hero Stage Focus:** Stages appear one after another as the primary hero content of the screen with smooth transitions:
  - **Delivery Flow:**
    1. *Ваш заказ принят / Готовим ваш кофе* (Large countdown timer)
    2. *Проверка качества и упаковка* (Packaging timer)
    3. *Курьер назначен* (Courier card, rating, call & message actions)
    4. *Курьер в пути* (Interactive 2GIS live route map)
    5. *Заказ доставлен* (Confirmation checkmark & bonus claim)
  - **Pickup Flow:**
    1. *Ваш заказ принят / Готовим ваш кофе* (Large countdown timer)
    2. *Проверка качества и упаковка* (Packaging timer)
    3. *Заказ готов к выдаче* (Large pickup code `#GC-XXXXX` for the barista counter)
    4. *Заказ получен* (Confirmation checkmark & bonus claim)

### 5. Pitch Demo Mode with "Skip to next stage" Button
- **Presentation Journey:** Allows pitch presenters to step through the entire order lifecycle seamlessly without waiting for real timers.
- **Discreet Presentation Bar:** Appears only when an active paid order exists.
- **One-Click Progression:** Clicking *"Skip to next stage"* smoothly advances the order to the next stage in the exact delivery or pickup sequence and awards bonuses upon delivery.
- **Security Guardrail:** Does not bypass payment verification—the button is only active after checkout.

### 6. AI Chat & Voice Ordering (Kazakh, Russian, English)
- **Natural Voice Recognition:** Speech-to-text via Web Speech API (`webkitSpeechRecognition` / `SpeechRecognition`) with pulsing recording indicator.
- **Drink & Customization Parser:** Recognizes drink names (latte, cappuccino, flat white, cold brew, raf, matcha, croissant, cheesecake), cup sizes (small, medium, large), milk varieties (oat, almond, lactose-free, regular), and quantities.
- **Voice Confirmation Workflow:**
  - *Customer:* «Хочу большой латте на овсяном молоке и один карамельный раф»
  - *AI:* «Вы выбрали: Большой Caramel Velvet Latte на Oat milk (1 шт.) и Карамельный раф (1 шт.). Всё верно?»
  - *Customer:* Confirms with voice («Да», «Верно») or clicks the interactive button.
  - *AI:* Adds products to the existing cart and prompts to open checkout.
- **Voice Readback:** AI speaks answers aloud using Web Speech Synthesis (`speechSynthesis.speak()`) with an audio toggle.
- **Cart Voice Controls:** Voice commands to remove drinks or clear the cart («Очисти корзину»).
- **Never Auto-Charges:** Voice commands never complete payment automatically; orders must be reviewed in checkout.

---

## 🎨 Design System & Commercial Coyote Aesthetic

- **Typography:** `Inter` sans-serif system (`400`, `500`, `600`, and `700` weights).
- **Numerals:** `font-variant-numeric: tabular-nums` for prices, timers, and bonus balances.
- **Currency:** Standardized to **₸ (Kazakhstani Tenge)** throughout.
- **Zero Unicode Emojis:** Replaced with clean, Lucide-style outline inline SVG icons with unified stroke weight (`1.8px` / `2px`).
- **Loyalty Program:** Points balance, tier badge, expiration date, and confetti celebration chime.

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
3. A pre-packaged archive containing all assets, images, and translations is available at:
   ```text
   C:\Users\Admin\.gemini\antigravity\scratch\global-coffee-app\global-coffee-app.zip
   ```
