# Biofeedback Engine — Tester Install Guide

Thanks for testing! This turns your **heart rate into live control** of a toy
and/or an OBS overlay. Everything runs locally on your machine — nothing is
uploaded anywhere.

Grab the installer for your OS from the
[latest release](https://github.com/SparkleDammit/biofeedback-engine-releases/releases/latest).

## Install

**Windows**
1. Download `Biofeedback Engine Setup 0.1.0.exe`.
2. Run it. Windows SmartScreen will warn (the app isn't signed yet) → click
   **More info** → **Run anyway**.
3. Follow the installer.

**macOS**
1. Download the `.dmg` — `-arm64` for Apple Silicon / M-chips, `-x64` for Intel
   Macs (if unsure, pick arm64).
2. Open it, drag the app to **Applications**.
3. First launch: **right-click the app → Open → Open**. (A normal double-click
   gets blocked because it's unsigned — the right-click bypass is a one-time
   thing.)

## Connect your heart rate

Any of these works — pick one:
- **Chest strap / armband** (Polar H10, COOSPO, Wahoo, etc.) — pairs directly
  over Bluetooth from inside the app.
- **Watch** (Apple Watch, Galaxy Watch) — via a free relay: **Pulsoid** or
  **HypeRate**. Paste your token in the app's **Sources** tab.
- **No hardware?** Use the built-in **simulator** to try the whole thing dry.

## Quick start

1. Open the app → **Sources** tab → connect your strap/watch (or pick simulator).
2. Watch the heart-rate and intensity gauges move.
3. **Tune** tab — adjust the intensity cap and pattern to taste. The big **STOP**
   button halts output instantly.
4. **OBS** tab — copy the overlay URL into an OBS **Browser Source** to show HR /
   intensity on stream.

## Safety

- Start the **intensity cap low** and raise it gradually.
- **STOP** cuts output immediately, any time.

## Reporting back

Please tell me: your OS, what HR device you used, and anything that felt off —
jumpy readings, connection drops, values that need better defaults. Screenshots
welcome.
