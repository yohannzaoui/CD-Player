

---

# Technics SL-PS740A Digital Audio Player - Documentation

## ⚙️ Core Specifications

* "Brand: Technics"
* "Model: SL-PS740A"
* "Technology: MASH 1-BIT DAC Simulation"
* "Visual Style: Vintage VFD (Vacuum Fluorescent Display)"
* "Language: English Only"
* "Theme: Dark Mode Only"

---

## 🚀 Key Features

### 1. Advanced Time Display

* **Anti-Jumping Logic**: Implementation of a "Slot-Based" grid where each digit is contained in a fixed-width `<span>`. This prevents the UI from shifting when the digit "1" appears.
* **Dual Mode**: Toggle between "Elapsed Time" and "Remaining Time".
* **Visual Polish**: High-glow green text with a 15px radial blur for a realistic phosphor effect.

### 2. Brand Identity

* **Logo**: High-definition `Technics_logo.png` set to exactly **70px** height.
* **Relief Effect**: Custom CSS filters applied to the logo for a 3D metallic look.

### 3. Integrated Audio Tools

* **VU Meter**: Dual-channel (L/R) canvas-based visualizer with peak-hold simulation.
* **Jog Shuttle**: A functional range slider for manual track scrubbing with dynamic status feedback.
* **Indicators**:
* "SHUFFLE: Displays only the word 'SHUFFLE' when active."
* "REPEAT: Cycles through 'Repeat 1' and 'Repeat All'."
* "A-B: Visual indicator for loop points."



---

## 📂 Project Structure

> /Project-Root
> ├── index.html (Core application & logic)
> ├── manifest.json (PWA configuration)
> └── img/
> ├── Technics_logo.png (70px height)
> └── favicon_512.png (App icon & Media Artwork)

---

## 🛠 Recent Fixes (2026-01-12)

| Feature | Update Description |
| --- | --- |
| **Logo** | Resized to **70px** for better visual balance. |
| **Navigation** | Removed vertical bars from `<<` and `>>` buttons. |
| **Stability** | Separated timer digits into individual containers to stop text movement. |
| **Shuffle** | Changed indicator label from "SHUFFLE ON" to just "SHUFFLE". |

---

## 📱 Mobile & PWA Optimization

* **Meta Tags**: Full support for `apple-mobile-web-app-capable` to hide the Safari URL bar.
* **Media Session API**: Allows track control and metadata display on the phone's lock screen and Bluetooth devices.
---

## 📖 User Guide

### 1. Track Navigation & Playback

* **Play/Pause**: Starts or pauses the current track. The status line will toggle between `PLAY` and `PAUSE`.
* **Next/Previous (`>>` / `<<`)**: Skips to the next or previous track in the playlist. The active track number will glow red in the track grid.
* **Stop**: Stops playback and resets the timer to `00:00`. It also clears any active **A-B Repeat** points.

### 2. Jog Shuttle (Search Mode)

The **Jog Shuttle** at the bottom allows for precision scrubbing within a track:

* **Forward Search**: Move the slider to the right to fast-forward. The status will display `SEARCH >>`.
* **Backward Search**: Move the slider to the left to rewind. The status will display `<< SEARCH`.
* **Variable Speed**: The further you move the slider, the faster the search becomes. Releasing the slider (or letting it snap back to center) resumes normal playback.

### 3. A-B Repeat Function

This allows you to loop a specific section of a song:

1. While a track is playing, press **A-B** once to set the start point (**Point A**). The `A-B Repeat` indicator will light up.
2. Press **A-B** a second time to set the end point (**Point B**). The player will now loop continuously between these two points.
3. Press **A-B** a third time to clear the loop and return to normal playback.

### 4. Advanced Display Features

* **Time Toggle**: Press the **Time** button to switch between:
* `Elapsed Time`: Time passed since the start of the track.
* `Remaining Time`: Countdown until the end of the track.


* **VU Mode**: Press **VU** to toggle the visibility of the fluorescent level meters if you prefer a minimal interface.
* **Peak Search**: Simulates the hardware's ability to find the loudest part of a disc (useful for setting recording levels).

### 5. Playback Modes

* **Shuffle**: Randomizes the play order. The indicator will show **SHUFFLE**.
* **Repeat**:
* `Repeat 1`: Loops the current track indefinitely.
* `Repeat All`: Loops the entire playlist.



---

## 💾 Saving Preferences

The application is designed to remember your settings. Your **Language** (English) and **Theme** (Dark Mode) are automatically saved in your browser's local storage so that the player is ready the moment you reopen it.

---

