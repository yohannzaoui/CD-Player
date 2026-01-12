---

# Technics SL-PS740A Digital Audio Player - Documentation

## ⚙️ Core Specifications

* **Brand:** Technics
* **Model:** SL-PS740A
* **Technology:** MASH 1-BIT DAC Simulation
* **Visual Style:** Vintage VFD (Vacuum Fluorescent Display)
* **Language:** English Only
* **Theme:** Dark Mode Only

---

## 🚀 Key Features

### 1. Advanced Time Display

* **Anti-Jumping Logic:** Implementation of a "Slot-Based" grid where each digit is contained in a fixed-width `<span>`. This prevents the UI from shifting when the digit "1" appears.
* **Dual Mode:** Toggle between "Elapsed Time" and "Remaining Time".
* **Visual Polish:** High-glow green text with a 15px radial blur for a realistic phosphor effect.

### 2. Brand Identity

* **Logo:** High-definition `Technics_logo.png` set to exactly **70px** height.
* **Relief Effect:** Custom CSS filters applied to the logo for a 3D metallic look:
```css
filter: drop-shadow(0px 2px 2px rgba(0,0,0,0.8)) drop-shadow(0px 1px 0px rgba(255,255,255,0.1));

```



### 3. Integrated Audio Tools

* **VU Meter:** Dual-channel (L/R) canvas-based visualizer with peak-hold simulation (Red/Orange/Green segments).
* **Jog Shuttle:** A functional range slider for manual track scrubbing with dynamic status feedback (`SEARCH >>`).
* **Indicators:** * `SHUFFLE`: Displays only the word "SHUFFLE" when active.
* `REPEAT`: Cycles through "Repeat 1" and "Repeat All".
* `A-B`: Visual indicator for loop points.



---

## 📂 Project Structure

```text
/Project-Root
│
├── index.html           # Core application & logic
├── manifest.json        # PWA configuration
└── img/
    ├── Technics_logo.png # Logo (70px height)
    └── favicon_512.png   # App icon & Media Artwork

```

---

## 🛠 Recent Fixes (2026-01-12)

| Feature | Update Description |
| --- | --- |
| **Logo** | Resized to **70px** for better visual balance. |
| **Navigation** | Removed vertical bars from `<<` and `>>` buttons. |
| **Stability** | Separated timer digits into individual containers to stop text movement. |
| **Shuffle** | Changed indicator label from "SHUFFLE ON" to just "**SHUFFLE**". |
| **YAML Fix** | Applied proper block quoting in documentation to prevent parsing errors. |

---

## 📱 Mobile & PWA Optimization

* **Meta Tags:** Full support for `apple-mobile-web-app-capable` to hide the Safari URL bar.
* **Media Session API:** Allows track control and metadata display on the phone's lock screen and Bluetooth devices.

---
