# Premium Calculator

A modern **calculator** built with **HTML, CSS, and vanilla JavaScript**. The app features smooth button animations, a glassmorphism UI, real-time display updates, and full keyboard support.

---

## Overview

This is a **single-page frontend calculator** designed with a premium look and feel. Users can perform all standard arithmetic operations, delete individual digits, clear the display, and interact entirely via keyboard — all without any frameworks, build tools, or backend.

---

## Features

### Arithmetic Operations
- Supports Addition, Subtraction, Multiplication, and Division
- Chained operations — automatically computes the previous result before applying a new operator
- Division-by-zero protection built into the `compute()` method

---

### Smart Display
- Two-line display: previous operand with operator on top, current operand below
- Numbers formatted with `toLocaleString` for comma-separated readability
- Decimal support with duplicate-dot prevention
- Flash animation on every calculation result

---

### Keyboard Support
- Number keys `0–9` and `.` for digit input
- `+`, `-`, `*`, `/` for arithmetic operations
- `Enter` or `=` to evaluate
- `Backspace` to delete the last digit
- `Escape` to clear all

---

### UI & Animations
- Glassmorphism card with `backdrop-filter` blur and layered box shadows
- Subtle floating animation on the calculator body using `@keyframes float`
- Button hover lift effect and press feedback via CSS transitions
- Radial gradient background for visual depth
- Google Fonts (`Outfit`) for modern, clean typography

---

### Responsive Design
- Full-screen layout on small screens (`max-width: 400px`)
- Touch-optimized buttons with `-webkit-tap-highlight-color` disabled
- Safe area bottom padding on mobile

---

## Technologies Used

- HTML5
- CSS3 (Custom Properties, CSS Grid, Keyframe Animations, Glassmorphism)
- JavaScript (ES6+ Class syntax)
- Google Fonts (Outfit)

---

## Project Structure

```text
├── index.html    # Calculator markup, button grid, and data attributes
├── style.css     # Styling, glassmorphism, animations, and responsive layout
├── script.js     # Calculator class, keyboard support, and display logic
```

---

## Setup & Usage

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/premium-calculator.git
   ```
   **OR** download the project as a `.zip` file and extract it.

2. Open `index.html` in any modern web browser.

No build tools, package managers, or server setup required.

---

## Implementation Details

- All calculator logic is encapsulated in a `Calculator` ES6 class with clearly separated methods: `clear()`, `delete()`, `appendNumber()`, `chooseOperation()`, `compute()`, and `updateDisplay()`
- `getDisplayNumber()` handles integer formatting via `toLocaleString` while preserving decimal digits exactly as typed
- The display flash animation is triggered by removing and immediately re-adding the `.animate` class — a forced reflow via `offsetWidth` ensures the keyframe restarts on every calculation
- Keyboard input is mapped to calculator methods via a `keydown` listener on `document`, covering all standard number, operator, and control keys
- Buttons use `data-*` attributes (`data-number`, `data-operation`, `data-action`) for clean DOM querying and event binding

---

## Limitations

- No percentage `%` or sign-toggle `±` function
- No calculation history or memory storage
- Long numbers may overflow the display on very small screens
- No support for scientific or advanced functions

---

## License

This project is **open-source** and intended for educational and portfolio use.

---

## Author

Designed and developed by **Zaman Siraj**
