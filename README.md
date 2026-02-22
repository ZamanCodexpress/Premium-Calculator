# Premium Calculator

A sleek, **client-side Calculator** built using **HTML, CSS, and vanilla JavaScript**. Designed with a premium aesthetic, smooth animations, and full keyboard support — all without any backend or frameworks.

---

## Overview

This is a **single-page frontend application** that provides a clean and intuitive calculation experience. Users can perform arithmetic operations through both mouse clicks and keyboard input, with real-time display updates and subtle visual feedback on every interaction.

All logic runs entirely in the browser with **no external dependencies** beyond a Google Font.

---

## Features

###  Core Arithmetic
* Addition, subtraction, multiplication, and division
* Chained operations (compute mid-sequence without pressing equals)
* Division-by-zero protection
* Decimal point support with duplicate-entry prevention

###  Keyboard Support
* Number keys `0–9` and `.` for input
* `+`, `-`, `*`, `/` for operations
* `Enter` or `=` to compute
* `Backspace` to delete the last digit
* `Escape` to clear all

###  Display
* Two-line display showing the current operand and the previous expression
* Locale-formatted number output (comma separators)
* Flash animation on result calculation

###  Design & Animations
* Glassmorphism UI with `backdrop-filter` blur
* Floating idle animation on the calculator body
* Hover lift effect and active press feedback on all buttons
* Radial gradient background with a dark color palette
* Color-coded button groups: numbers, operators, controls, and equals

###  Responsive Design
* Adapts to mobile screens (full-screen layout on small viewports)
* Touch-friendly button sizing and tap highlight removal

---

## Technologies Used

* HTML5
* CSS3 (Glassmorphism, Custom Properties, Keyframe Animations, Grid Layout)
* JavaScript (ES6+ Classes)
* Google Fonts (Outfit)

---

## Project Structure

```text
├── index.html    # Calculator layout and button structure
├── style.css     # Styling, animations, and responsive design
├── script.js     # Calculator class, event listeners, keyboard support
```

---

## Setup & Usage

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/premium-calculator.git
   ```
   **OR** download the project as a `.zip` file and extract it.

2. Open `index.html` in any modern web browser.

No build tools, dependencies, or server setup required.

---

## Implementation Details

* Calculator state is encapsulated in a `Calculator` ES6 class
* Display updates are handled through direct DOM manipulation
* Button events are delegated using `querySelectorAll` with `forEach`
* Keyboard events are captured globally via `document.addEventListener('keydown')`
* The display flash animation is triggered by toggling a CSS class and forcing a reflow

---

## Limitations

* No history or memory functions (M+, M-, MR)
* No percentage or square root operations
* No persistent state — clears on page refresh

---

## License

This project is **open-source** and intended for **educational and portfolio use**.

---

## Author

Built as a frontend practice project to demonstrate:

* Premium UI design with CSS animations
* Object-oriented JavaScript
* Keyboard accessibility
* Responsive and mobile-first layout
