# California South Delta Water Ski Conditions

A live telemetry dashboard for evaluating real-time and 7-day forecasted water-skiing conditions across the **California South Delta** sloughs.

**Live Site:** https://gomce62.github.io/california-delta-water-ski-conditions/

---

## What This Site Does

This dashboard helps water skiers find the calmest, smoothest water ("butter") in the California South Delta by combining slough geometry with live weather, wind, tide, and water-temperature telemetry:

- **Best Water Right Now:** Automatically ranks Delta sloughs by estimated lee wind speed and surface chop to highlight the best current skiing spot.
- **Conditions Now · Delta Telemetry:** Displays live air temperature, wind speed/direction, tide height and trend, and water temperature.
- **Detailed Conditions per Slough:** Breaks down wind angle relative to each slough's orientation, effective lee wind, and water-surface rating.
- **7-Day Water-Skiing Forecast:** Multi-day outlook of wind, temperature, and precipitation for planning ski sessions ahead.
- **Interactive Dual-Pin Map:** Uses Leaflet to visualize the selected slough alongside the active Weather Underground Personal Weather Station (PWS).
- **Built-In User Guide & Key Concepts:** Includes hover pop-ups and an overview section explaining leeward shelter, tide currents, and telemetry sources.

### Data Sources

The app runs entirely in the browser and fetches live public telemetry from:
- **Open-Meteo** & **National Weather Service (`api.weather.gov`)** — current weather, wind, and 7-day forecasts
- **NOAA Tides & Currents** — tide predictions, observed water levels, and water temperature
- **USGS NWIS** & **California CDEC** — Delta water temperature sensors
- **Weather Underground PWS API** *(optional)* — hyper-local personal weather station observations if a station ID and API key are provided in the UI

---

## How to Install & Run Locally

This project is a **zero-build, static HTML application** (`index.html`). All UI libraries (Tailwind CSS, Lucide Icons, Leaflet, and Google Fonts) are loaded via CDN, so no `npm install` or backend server is required.

### 1. Clone the repository

```bash
git clone https://github.com/gomce62/california-delta-water-ski-conditions.git
cd california-delta-water-ski-conditions
```

### 2. Run the site

**Option A — Local HTTP server (recommended):**

Using Python:
```bash
python3 -m http.server 8000
```
Then open [http://localhost:8000](http://localhost:8000) in your browser.

Or using Node.js:
```bash
npx serve .
```

**Option B — Open directly:**
Double-click `index.html` (or `california_delta_water_ski_slough_telemetry_dashboard.html`) to open it directly in your browser.

---

## Deploying & Updating Google Sites (`sites.google.com`)

This repository is configured for **GitHub Pages** (serving `index.html` from the `main` branch):

- **Hosted URL:** `https://gomce62.github.io/california-delta-water-ski-conditions/`

To embed or update this dashboard in **Google Sites**:
1. Open your site in [sites.google.com](https://sites.google.com).
2. Go to **Insert → Embed → By URL**.
3. Paste `https://gomce62.github.io/california-delta-water-ski-conditions/` and choose **Whole page** (or resize the embed frame as desired).
4. Click **Publish** in Google Sites to make the update live.
