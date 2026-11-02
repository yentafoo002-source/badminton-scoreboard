# 🏸 Badminton Live Scoreboard (Web App)

A modern, responsive, and serverless **Badminton Scoreboard Web Application** designed for seamless real-time score synchronization between a **Mobile Phone (Controller)** and an **iPad/Tablet (Courtside Display)** using WebRTC (PeerJS).

---

## 🌟 Key Features

### 1. Dual Device Setup (Phone + iPad)
- **Controller Mode (Phone):** Held by the umpire or scorer outside the court.
  - **Tap anywhere on a side:** Adds +1 point for that team.
  - **Swipe Down on a side:** Subtracts -1 point from that side.
  - **Haptic Vibration:** Haptic feedback on score changes so you never need to take your eyes off the match.
  - **Accidental Touch Lock:** One-tap lock screen mode when holding the phone in hand or pocket.
  - **Quick Action Bar:** `Undo`, `Swap Ends` (สลับฝั่ง), `Toggle Serve`, `Break Timer`, and `Reset Match`.
  
- **Display Mode (iPad / TV / Monitor):** Placed courtside for players and spectators.
  - **100% Read-Only & Touch-Immune:** All touch and click events are shielded to prevent accidental tampering when balls or players hit the screen.
  - **Screen Wake Lock API:** Prevents the iPad screen from sleeping or dimming during the entire match.
  - **Ultra-Large Score Digits:** High contrast, legible from 15+ meters across the sports hall.
  - **One-Click Fullscreen:** Maximizes the screen and hides browser address bars.

---

### 2. Zero-Friction Pairing
1. **Instant QR Code:** On your phone, tap **Options -> Controller Mode**. A dynamic QR Code and a 6-digit PIN are displayed.
2. **Instant Scan:** Point your iPad's camera at the QR code. It opens the web app with `?mode=display&room=XXXXXX` and connects **instantly without typing anything**!
3. **Manual 6-Digit PIN:** Or select **Options -> Display Score** on the iPad and enter the 6-digit PIN code.

---

### 3. Official BWF Rules & Smart Umpire
- **21 Points per Game (Best of 3 Sets)** (Customizable to 15 or 11 points).
- **Deuce Logic:** At 20–20, a team must lead by 2 points. Hard-cap at 30 points (sudden death at 29–29).
- **Game Point & Match Point Indicators:** Visual badges (`🔥 GAME POINT` / `🏆 MATCH POINT`) highlight critical moments.
- **Interactive Break Countdown Timer:** 60-second Interval at 11 points and 120-second Game Break with circular countdown and audio buzzer!
- **Voice Umpire (Speech Synthesis):** Automatic score announcements in Thai (🇹🇭) or English (🇬🇧) following BWF serving order.
- **Past Sets Tracker:** Displays summary of previous set scores (e.g. `G1: 21-18 | G2: 19-21`).
- **Server & Court Indicator:** Shuttlecock icon (🏸) indicates the serving side, along with **Right Court (Even Score)** or **Left Court (Odd Score)**.
- **Match Winner Celebration:** Confetti celebration when a team wins 2 sets.

---

## 🚀 How to Run Locally

You can test this right now on your computer!

### Option 1: Open Directly in Browser
Double-click `index.html` in Finder or run in terminal:
```bash
open index.html
```

### Option 2: Run a Local Web Server (Recommended for testing on Phone + iPad on the same Wi-Fi)
From this project directory:
```bash
# Using Python 3 built-in server:
python3 -m http.server 8080

# Or using Node.js npx:
npx serve .
```
Then find your computer's local IP (e.g. `192.168.1.XX:8080`) to open it on both your phone and iPad!

---

## 🌐 Free 1-Click Deployment (Public URL)

To make it accessible to everyone anywhere in the world on cellular 4G/5G or gym Wi-Fi:

### Option A: GitHub Pages (Free forever)
1. Push this folder to your GitHub repository.
2. Go to **Settings -> Pages**.
3. Under **Branch**, select `main` and root `/`, then click **Save**.
4. Your scoreboard will be live at `https://<username>.github.io/<repo-name>/`.

### Option B: Vercel (https://badminton-live-score.vercel.app)
1. Import this repository in [Vercel](https://vercel.com/new).
2. Set Project Name to `badminton-live-score` (or any custom domain).
3. Click **Deploy**. Vercel will automatically read `vercel.json` and deploy in 5 seconds with an HTTPS URL.
