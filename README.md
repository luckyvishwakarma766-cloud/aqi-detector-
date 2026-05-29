# 🌫️ AQI Detector

> Real-time Air Quality Index tracker with live alerts & health insights

![Python](https://img.shields.io/badge/Python-3.10+-3776AB?style=flat-square&logo=python&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-22c55e?style=flat-square)
![Status](https://img.shields.io/badge/Status-Active-22c55e?style=flat-square)
![API](https://img.shields.io/badge/API-OpenWeather-orange?style=flat-square)
![PRs Welcome](https://img.shields.io/badge/PRs-Welcome-7C3AED?style=flat-square)

---

## 📖 Overview

**AQI Detector** ek real-time air quality monitoring tool hai jo kisi bhi city ka AQI fetch karke health-based alerts deta hai. Yeh **OpenWeatherMap API** use karta hai aur CLI + Web dono interfaces support karta hai.

---

## ✨ Features

- 🌐 **City-wise AQI fetching** — OpenWeatherMap API se live data
- 🚨 **Health Alerts** — Good / Moderate / Unhealthy / Hazardous levels
- 📊 **Pollutant Breakdown** — PM2.5, PM10, NO₂, CO, O₃ alag-alag dikhata hai
- 🗺️ **Multi-city Support** — Ek saath kai cities monitor karo
- 📁 **Export Option** — Results ko JSON / CSV me save karo
- ⚡ **Fast & Lightweight** — Minimal dependencies

---

## 🏗️ Project Structure

```
aqi-detector/
├── 📁 src/
│   ├── aqi_fetcher.py     # API calls & data parsing
│   ├── alerts.py          # Health level logic
│   └── exporter.py        # JSON / CSV export
├── 📁 tests/              # Unit tests
├── .env.example           # API key template
├── requirements.txt
└── README.md
```

---

## ⚙️ Installation

```bash
# 1. Clone karo
git clone https://github.com/your-username/aqi-detector.git
cd aqi-detector

# 2. Virtual environment banao
python -m venv venv
source venv/bin/activate   # Windows: venv\Scripts\activate

# 3. Dependencies install karo
pip install -r requirements.txt

# 4. API key set karo
cp .env.example .env       # .env me apni OpenWeatherMap API key dalo
```

---

## 🚀 Usage

```bash
# Single city check
python main.py --city "Delhi"

# Multiple cities ek saath
python main.py --city "Delhi" "Mumbai" "Chennai"

# CSV export ke saath
python main.py --city "Kolkata" --export csv

# JSON export
python main.py --city "Bangalore" --export json
```

**Sample Output:**
```
City: Delhi
AQI: 187 🔴 Unhealthy
PM2.5: 98.4 µg/m³
PM10: 142.1 µg/m³
NO₂: 45.2 µg/m³
⚠️  Alert: Outdoor activities avoid karein. Sensitive groups ghar pe rahein.
```

---

## 📊 AQI Scale Reference

| AQI Range | Category | Health Impact |
|-----------|----------|---------------|
| 0 – 50 | 🟢 Good | Koi risk nahi |
| 51 – 100 | 🟡 Moderate | Sensitive logon ko savdhani |
| 101 – 150 | 🟠 Unhealthy for Sensitive | Outdoor activity kam karo |
| 151 – 200 | 🔴 Unhealthy | Sabko health effects |
| 201 – 300 | 🟣 Very Unhealthy | Serious risk, ghar pe raho |
| 301+ | ⚫ Hazardous | Emergency conditions |

---

## 🔑 API Setup

1. [OpenWeatherMap](https://openweathermap.org/api) pe free account banao
2. **Air Pollution API** enable karo
3. `.env` file me key paste karo:

```env
OPENWEATHER_API_KEY=your_api_key_here
```

---

## 🧪 Tests Run Karna

```bash
pytest tests/ -v
```

---

## 🤝 Contributing

Contributions welcome hain! 🙌

1. Fork karo (`git fork`)
2. Branch banao (`git checkout -b feature/naya-feature`)
3. Changes commit karo (`git commit -m 'Add naya feature'`)
4. Push karo (`git push origin feature/naya-feature`)
5. Pull Request submit karo

Bugs ya suggestions ke liye [Issues](https://github.com/your-username/aqi-detector/issues) open karo.

---

## 📄 License

[MIT License](LICENSE) — Freely use, modify, aur distribute karo.

---

<p align="center">Made with ❤️ for cleaner air awareness 🌿</p>
<p align="center">
  <a href="https://github.com/your-username/aqi-detector/issues">Report Bug</a> ·
  <a href="https://github.com/your-username/aqi-detector/issues">Request Feature</a>
</p>
