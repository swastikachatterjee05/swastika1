<div align="center">

  <h1>✨ ApexCalc — Professional React Web Calculator</h1>
  
  <p>
    <b>A modern, feature-rich, and production-grade Calculator & Unit Converter Web Application built with React 19, Vite, and Vanilla CSS3.</b>
  </p>

  <p>
    <a href="https://react.dev"><img src="https://img.shields.io/badge/React-19.0-61DAFB?style=for-the-badge&logo=react&logoColor=black" alt="React 19" /></a>
    <a href="https://vitejs.dev"><img src="https://img.shields.io/badge/Vite-8.0-646CFF?style=for-the-badge&logo=vite&logoColor=white" alt="Vite 8" /></a>
    <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript"><img src="https://img.shields.io/badge/JavaScript-ES6+-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black" alt="ES6+" /></a>
    <a href="https://lucide.dev"><img src="https://img.shields.io/badge/Icons-Lucide--React-F43F5E?style=for-the-badge" alt="Lucide Icons" /></a>
    <a href="https://opensource.org/licenses/MIT"><img src="https://img.shields.io/badge/License-MIT-green.svg?style=for-the-badge" alt="License MIT" /></a>
  </p>

  <p>
    <a href="#-features">Features</a> •
    <a href="#-live-demo">Live Demo</a> •
    <a href="#-tech-stack">Tech Stack</a> •
    <a href="#-getting-started">Getting Started</a> •
    <a href="#-keyboard-shortcuts">Shortcuts</a> •
    <a href="#-architecture">Architecture</a>
  </p>

  <br/>
</div>

---

## 🌟 Features

- 🧮 **Standard Arithmetic Mode**: Addition, Subtraction, Multiplication, Division, Decimal validation, Percentages (`%`), and Toggle Sign (`±`).
- 🔬 **Scientific Calculator Mode**: Advanced mathematical functions including Trigonometry (`sin`, `cos`, `tan`), Logarithms (`log`, `ln`), Exponents (`x²`, `1/x`), Constants (`π`, `e`), and Square Root (`√`).
- 🔄 **Real-Time Unit Converter**: Multi-category converter supporting:
  - **Length**: Meters, Kilometers, Feet, Inches, Miles, etc.
  - **Weight**: Kilograms, Grams, Pounds, Ounces.
  - **Temperature**: Celsius, Fahrenheit, Kelvin.
  - **Data Storage**: Bytes, KB, MB, GB, TB.
  - **Currency**: USD, EUR, GBP, INR, JPY, CAD, AUD.
- 📜 **Persistent Calculation History**: Automatically stores recent calculation history using `localStorage` with entry recall capabilities.
- 🎨 **Dual Glassmorphism Theme System**: High-contrast Dark and Light modes with automatic system preference detection (`prefers-color-scheme`).
- ⌨️ **Full Keyboard Support**: Seamlessly interact using physical keys with visual button press animations (`.btn-pressed`).
- 📋 **One-Click Clipboard Copy**: Instantly copy results to clipboard with feedback tooltip notifications.
- ♿ **Accessible & Responsive**: Accessible screen-reader live alerts (`aria-live`), fluid `clamp()` typography, and 320px to 4K viewport support.

---

## 📸 Interface Preview

```text
┌─────────────────────────────────────────────────────────────┐
│  ApexCalc                                [Std] [Sci] [⇄] 🌙 │
├─────────────────────────────────────────────────────────────┤
│                                                125 × 24 =   │
│                                                     3,000   │
├─────────────────────────────────────────────────────────────┤
│   [ AC ]   [ ⌫ ]   [ % ]   [ ÷ ]                            │
│   [  7 ]   [ 8 ]   [ 9 ]   [ × ]                            │
│   [  4 ]   [ 5 ]   [ 6 ]   [ − ]                            │
│   [  1 ]   [ 2 ]   [ 3 ]   [ + ]                            │
│   [  ± ]   [ 0 ]   [ . ]   [ = ]                            │
└─────────────────────────────────────────────────────────────┘
```

---

## 🛠️ Tech Stack

| Component | Technology Used |
| :--- | :--- |
| **Framework** | [React 19](https://react.dev/) |
| **Build Tool** | [Vite 8](https://vitejs.dev/) |
| **Styling** | Vanilla CSS3 (CSS Variables, Flexbox, CSS Grid, Glassmorphism) |
| **Icons** | [Lucide React](https://lucide.dev/) |
| **Typography** | Google Fonts (`Outfit` & `JetBrains Mono`) |
| **Parsing Engine** | Custom Shunting-Yard & RPN Evaluator (eval-free) |

---

## 🚀 Getting Started

### Prerequisites

Ensure you have [Node.js](https://nodejs.org/) (v18 or higher) installed.

### Installation

1. **Clone the repository**:
   ```bash
   git clone https://github.com/your-username/apexcalc-web-app.git
   cd apexcalc-web-app
   ```

2. **Install dependencies**:
   ```bash
   npm install
   ```

3. **Start local development server**:
   ```bash
   npm run dev
   ```
   Open `http://localhost:5173` in your browser.

4. **Build for production**:
   ```bash
   npm run build
   ```

---

## ⌨️ Keyboard Shortcuts

| Shortcut | Description |
| :--- | :--- |
| `0` – `9` | Input Number |
| `.` | Input Decimal Point |
| `+` | Addition (`+`) |
| `-` | Subtraction (`−`) |
| `*` | Multiplication (`×`) |
| `/` | Division (`÷`) |
| `%` | Percentage (`%`) |
| `Enter` or `=` | Evaluate Result |
| `Backspace` | Delete last digit |
| `Escape` | Clear All (`AC`) |
| `H` | Toggle History Drawer |
| `T` | Toggle Dark/Light Theme |

---

## 📐 Math Engine Architecture

ApexCalc processes expressions through a safe, custom evaluation pipeline without using unsafe dynamic execution functions (`eval()` or `Function()`):

```text
User Formula (e.g. "125 × 24 + 5")
       │
       ▼
1. Lexical Tokenizer ──► ["125", "*", "24", "+", "5"]
       │
       ▼
2. Shunting-Yard Parser ──► RPN Stack: [125, 24, *, 5, +]
       │
       ▼
3. RPN Stack Evaluator ──► Result: 3005
       │
       ▼
4. Epsilon Precision Corrector ──► 3005
```

---

## 📄 License

This project is licensed under the [MIT License](LICENSE).
