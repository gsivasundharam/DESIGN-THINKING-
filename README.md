# 🌾⚡ LoRa Solar Mesh Node — Interactive 3D Prototype

> A fully interactive, in-browser 3D simulation of a solar-powered, LoRa-connected smart irrigation retrofit device — built entirely in a single self-contained HTML file. No installs, no build step, no dependencies to manage. Just open it and start exploring. 🚰📡☀️

<p align="left">
  <img alt="Three.js" src="https://img.shields.io/badge/Three.js-r128-black?logo=three.js&logoColor=white&style=for-the-badge">
  <img alt="No Build Step" src="https://img.shields.io/badge/Build%20Step-None%20needed-brightgreen?style=for-the-badge">
  <img alt="Single File" src="https://img.shields.io/badge/Dependencies-Single%20HTML%20File-blue?style=for-the-badge">
  <img alt="Mobile Friendly" src="https://img.shields.io/badge/Mobile-Friendly-ff69b4?style=for-the-badge">
  <img alt="License" src="https://img.shields.io/badge/License-MIT-yellow?style=for-the-badge">
</p>

---

## ✨ What is this?

This is a **virtual prototype** of a retrofit irrigation automation device — the kind that clamps onto an existing field valve without replacing any plumbing. Instead of a static render, this prototype is a **living, breathing 3D simulation** you can orbit, explode, X-ray, and poke at in real time, right in your browser.

It was built to make an engineering concept *tangible* before a single physical part gets ordered — showing exactly how the hardware works, how the day/night solar cycle affects it, and how the valve logic responds to soil moisture, all without needing a CAD license or a 3D printer. 🧪

---

## 🚀 Try it

1. Download `LoRa_Solar_Mesh_Node___Interactive_3D.html`
2. Double-click it — it opens straight in your browser. That's it. 🎉
3. Or host it on **GitHub Pages** for a shareable live demo link (see [Deploying](#-deploying-to-github-pages) below).

No `npm install`. No bundler. No server. Just HTML, CSS, and [Three.js](https://threejs.org/) loaded from a CDN.

---

## 🕹️ Features

| | |
|---|---|
| 🔄 **Orbit camera** | Drag to rotate, scroll or pinch to zoom, auto-spin toggle |
| 💥 **Explode view** | Slide to pull every component apart and see how it all fits together |
| 🩻 **X-ray mode** | See through the enclosure without opening it |
| 🔓 **Open lid** | Pop the IP67 enclosure open to reveal the electronics inside |
| 👆 **Tap-to-inspect** | Click/tap any part — PCB, battery, solar panel, valve, probe — for a plain-English description |
| ☀️ **Time-of-day simulation** | Drag the sun across a full day cycle, or hit "Run day" to animate it automatically |
| 💧 **Live soil moisture control** | Manually set moisture, or let the system respond automatically |
| ⚙️ **Autonomous valve logic** | Watch the valve open below 30% moisture and close above 65% — fully automatic, battery-aware |
| 📶 **LoRa mesh visualization** | Animated signal rings and a dashed packet path show live communication with a remote gateway |
| 📊 **Live HUD** | Soil moisture, battery %, solar input (W), valve state, time, and LoRa signal (dBm) update in real time |

---

## 🔧 What's actually being simulated

Every labeled part corresponds to a real component in the underlying concept:

- 🧰 **IP67 weatherproof enclosure** — sealed housing for all electronics
- 🧠 **ESP32 + LoRa module** — runs deep-sleep firmware and talks to the mesh network (865–867 MHz band)
- 🔋 **LiFePO4 battery** — stores solar energy for night-time and cloudy-day operation
- ☀️ **Solar panel + MPPT charge controller** — off-grid power, protected against over/deep-discharge
- ⚙️ **Gear motor + universal clamp** — retrofits directly onto an existing gate valve, no plumbing replacement needed
- 🌱 **Capacitive soil probe** — corrosion-free, contact-free moisture sensing
- 📡 **Remote LoRa gateway** — receives node data from kilometers away and forwards it to the cloud/app
- 🛡️ **TVS diode surge protection** — guards the electronics against voltage spikes

---

## 🎛️ Controls reference

| Control | What it does |
|---|---|
| **Explode** | Pulls all components apart radially |
| **Time of day** | Manually scrub through a full day/night cycle |
| **Soil moisture** | Manually set the moisture reading |
| **X-ray** | Makes the enclosure semi-transparent |
| **Open lid** | Animates the enclosure lid open |
| **Auto** | Lets the valve logic run autonomously based on moisture + battery |
| **Valve open** | Manual override (disabled while Auto is on) |
| **Run day** | Auto-advances the time-of-day slider |
| **Spin** | Toggles automatic camera rotation |
| **Reset view** | Returns the camera and all toggles to their default state |

---

## 🌐 Deploying to GitHub Pages

Want a shareable link instead of a local file?

1. Push this repo to GitHub.
2. Go to **Settings → Pages**.
3. Under **Source**, select your default branch and `/ (root)`.
4. Save — your live demo will be published at:
   `https://<your-username>.github.io/<repo-name>/LoRa_Solar_Mesh_Node___Interactive_3D.html`

---

## 🛠️ Tech stack

- **[Three.js r128](https://threejs.org/)** (loaded via CDN, WebGL rendering)
- Vanilla **HTML / CSS / JavaScript** — no framework, no build tooling
- Procedurally generated geometry — every part is built in code, no external 3D model files

---

## 📁 Project structure

```
.
└── LoRa_Solar_Mesh_Node___Interactive_3D.html   ← everything lives in this one file
```

Yes, really — scene setup, lighting, geometry, materials, physics-ish simulation logic, and UI are all in a single ~180-line file. 🙌

---

## 🙏 Acknowledgments

Built with [Three.js](https://threejs.org/), the open-source 3D library that made a no-build-tool interactive prototype like this possible in pure vanilla JS.

---

## 📜 License

Released under the [MIT License](LICENSE) — feel free to fork, remix, and reuse for your own prototypes.

---

<p align="center">Made with 💧 + ☀️ + 📡 for smarter, more affordable irrigation.</p>
