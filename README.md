# 🧮 Calculator — HTML, CSS & JavaScript

A modern, responsive glassmorphism calculator built with pure HTML, CSS, and JavaScript. No frameworks, no dependencies.

---
<img width="1906" height="845" alt="image" src="https://github.com/user-attachments/assets/aab0172e-b30f-422e-9faa-fadd918cb7f8" />

## 🚀 How to Run

### Option 1 — Open directly in browser (simplest)
Double-click `HH.html` — it opens in your default browser instantly.

### Option 2 — Open via terminal
```powershell
start "C:\Users\ankit\OneDrive\Desktop\unified-mentor\task1\HH.html"
```

### Option 3 — Use a local server (recommended for development)
```powershell
cd "C:\Users\ankit\OneDrive\Desktop\unified-mentor\task1"
python -m http.server 8000
```
Then visit: **http://localhost:8000/HH.html**

---

## 📁 Project Structure

```
task1/
├── HH.html      ← Single file: HTML + CSS + JavaScript
└── README.md    ← This file
```

---

## ✨ Features

| Feature | Description |
|---|---|
| 🎨 Glassmorphism UI | Frosted glass card with gradient purple/blue background |
| 🌙☀️ Dark / Light Mode | Toggle button in the top-right corner |
| ➕➖✖️➗ Basic Arithmetic | Addition, subtraction, multiplication, division |
| ⛓️ Chained Operations | Calculates progressively (e.g., `3 + 4 × 2`) |
| +/− Toggle | Flip the sign of the current number |
| % Percent | Converts input to percentage (e.g., `50%` → `0.5`) |
| ⌨️ Keyboard Support | Full keyboard input (see table below) |
| 💧 Ripple Animation | Click ripple effect on every button |
| 📱 Responsive | Works on mobile and desktop screens |
| ♿ Accessible | `aria-label` on all buttons, `aria-live` on display |

---

## ⌨️ Keyboard Shortcuts

| Key | Action |
|---|---|
| `0` – `9` | Enter digits |
| `+`, `-`, `*`, `/` | Operators |
| `Enter` or `=` | Calculate result |
| `Backspace` | Delete last character |
| `Escape` | Clear all |
| `.` or `,` | Decimal point |
| `%` | Percent |

---

## 🏗️ How It Works

### HTML
- Semantic structure using `<div>`, `<button>`, and `aria-*` attributes.
- Each button has a `data-value` (digit or operator) or `data-action` (clear, calculate, etc.) attribute.

### CSS
- CSS custom properties (`--var`) for easy dark/light theming.
- `backdrop-filter: blur()` for the glassmorphism effect.
- Grid layout for the button pad.
- Smooth transitions and ripple animation via `@keyframes`.

### JavaScript
- **No `eval()`** — uses a custom `safeCalculate(a, op, b)` function.
- Maintains a simple state object `{ current, previous, operator, justCalculated }`.
- Single event listener on the button grid (event delegation).
- Keyboard events mapped to the same action functions.
- Theme toggle switches `data-theme` attribute on `<html>`.

---

## 🔒 Safety

- Division by zero returns `"Error"` instead of crashing.
- Invalid input is caught and displays `"Error"`.
- Input length is capped at 15 characters to prevent overflow.

---

## 🛠️ Tech Stack

- **HTML5** — Semantic markup
- **CSS3** — Custom properties, Grid, Flexbox, Animations
- **Vanilla JavaScript (ES6+)** — No libraries or frameworks

---

## 📸 Preview

Open `HH.html` in your browser to see the live calculator with:
- Purple/blue gradient background
- Frosted glass calculator card
- Smooth button animations
- Dark/Light mode toggle
