# Biofeedback Engine — Tester Install Guide

Thanks for testing! This turns your **heart rate into live control** of a toy
and/or an OBS overlay. Everything runs locally on your machine — nothing is
uploaded anywhere.

Grab the installer for your OS from the
[latest release](https://github.com/SparkleDammit/biofeedback-engine-releases/releases/latest).

## Install

**Windows**
1. Download `Biofeedback.Engine.Setup.0.1.1.exe`.
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
  over Bluetooth from inside the app. **No subscription, best signal** (and the
  only option that gives HRV). This is the recommended path — *if the computer
  running the app has Bluetooth.* Many streaming desktops don't; if you see
  "no Bluetooth", pair the strap to the free **HypeRate** phone app and use the
  relay below instead (no local Bluetooth needed).
- **Apple Watch** — the free **HeartCast** app (App Store) rebroadcasts your Watch
  over Bluetooth, so it connects like a strap (needs Bluetooth on the PC). Or use a
  relay below.
- **Watch, via a relay** (Apple Watch, Galaxy Watch, etc.) — in **Setup → Sources**,
  paste a token:
  - **HypeRate** — **free**; request an API key at [hyperate.io](https://www.hyperate.io/).
  - **Pulsoid** — works, but its API token requires a **paid Pulsoid plan**. Only
    use it if you already subscribe; otherwise use HypeRate or a strap.
- **No hardware?** Use the built-in **simulator** to try the whole thing dry.

## Quick start

The app opens on a calm live view. Everything you set up lives behind the
**⚙ Setup** button (top-right).

1. Click **⚙ Setup → Sources** → connect your strap or watch (or click **Simulate**
   to try it dry). Your heart rate appears in the big heart.
2. Rest a moment and watch the intensity react to your heart rate.
3. **Setup → Tune** — set the max intensity cap (it always shows in the header) and
   pick a pattern. The big **STOP** button halts output instantly.
4. **Setup → OBS** — copy an overlay URL into an OBS **Browser Source** to show HR /
   intensity on stream.

If you step away and the connection drops, the heart-rate relay reconnects on its
own; if the toy drops, just click **Connect toy** again — no need to restart.

## Safety

- Start the **intensity cap low** and raise it gradually.
- **STOP** cuts output immediately, any time.

## Reporting back

Please tell me: your OS, what HR device you used, and anything that felt off —
jumpy readings, connection drops, values that need better defaults. Screenshots
welcome.
