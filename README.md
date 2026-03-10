# 🛰 Kepler73

**A real-time satellite tracking application for amateur radio operators.**

Built by SA1CKW with help of AI — designed for practical use at the radio shack.

---

## Overview

Kepler73 is a web-based satellite tracker that runs locally on your machine. It uses SGP4 orbital mechanics to compute real-time satellite positions, predict upcoming passes, and assist with amateur radio satellite operations — including Doppler correction and pass alarms.

The interface runs in your browser, but everything is computed locally. No cloud, no account, no ads.

---

## Features

### 🗺 Live Map
- Real-time satellite positions on an interactive world map (OpenStreetMap / Esri Satellite)
- Ground tracks shown for all active satellites
- Extended 3-orbit track for the selected satellite
- Footprint circle showing coverage area
- Observer marker at your configured location

### 📡 Satellite Modules
- Organize satellites into named modules (e.g. LEO, Weather, AMSAT)
- Each module holds a custom list of satellites by NORAD ID
- TLE data fetched automatically from Celestrak
- Manual TLE refresh available from the menu

### 🧭 Polar View
- Real-time azimuth/elevation strobe pointing toward the selected satellite
- Yellow dot appears when the satellite rises above the horizon
- AZ and EL readout updated live
- Compass rose with N/E/S/W orientation

### 🔔 Pass Alarm
- Configurable audio alarm before AOS (default: 3 minutes)
- Multiple alarm sounds: CW beep, three beeps, rising tone, long beep
- Per-satellite alarm toggle — only alarms for satellites you care about
- Alarm resets automatically for each new pass

### 📻 Transponder & Doppler
- Transponder data fetched from SatNOGS database
- Shows uplink/downlink frequencies, mode, and status
- Real-time Doppler shift calculated and displayed (Hz and kHz Δ)
- Before a pass: shows maximum expected Doppler shift
- During a pass: live Doppler correction updated every second

### ⚙️ Settings
- Observer location (latitude, longitude, altitude)
- Minimum elevation for pass prediction
- Alarm timing and sound selection
- Offline mode — works without internet using cached TLE data (Not tested yet!)

---

## Installation (Windows)

A pre-built Windows executable is available under [Releases](../../releases).

1. Download and unzip `Kepler73-Win.zip`
2. Browse to \Kepler73-Win\dist\Kepler73
3. Double-click `Kepler73.exe`
4. Your browser opens automatically at `http://127.0.0.1:5000`

No Python or any other software required.

---

## Roadmap

- [x] Live satellite tracking
- [x] Pass prediction
- [x] Pass alarms
- [x] Polar view with real-time strobe
- [x] SatNOGS transponder data
- [x] Real-time Doppler correction
- [ ] CAT radio control (Hamlib)
- [ ] Rotor control (Hamlib)
- [ ] macOS and Linux builds

---

## License

Personal/amateur use. TLE data courtesy of [Celestrak](https://celestrak.org). Transponder data courtesy of [SatNOGS](https://db.satnogs.org).

---

*73 de SA1CKW*
