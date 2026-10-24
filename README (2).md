# RIZEN DAYS | Modern Weather Intelligence 🌤️

<div align="center">
  <p><strong>A premium, lightning-fast, single-page weather web application built for speed, accuracy, and visual elegance.</strong></p>
</div>

---

## 📖 Overview

**RIZEN DAYS** goes beyond raw numbers to provide actionable weather intelligence. Designed with a clean, distraction-free "Glassmorphism" aesthetic, it delivers real-time weather forecasting, interactive meteograms, air quality indexing, and smart outdoor recommendations. 

The best part? **No user logins, no subscriptions, no build steps, and no API keys are required.**

## ✨ Core Features

*   **🔍 Smart Search & Geolocation:** Search for any city worldwide or use precise browser geolocation to get instant weather data.
*   **📊 Interactive Meteogram:** A custom-built, animated Chart.js area chart showing the temperature trend over the next 24 hours, complete with day/night background shading and dynamic raindrop canvas animations.
*   **🧠 Weather Intelligence:** Actionable "Smart Recommendations" (Clothing, Gear, Health, Activity) and auto-generated text summaries based on current conditions, UV, and AQI.
*   **🌍 Comprehensive Metrics:** 
    *   Current Temperature & "Feels Like"
    *   Hourly Forecast (24h) & 7-Day Daily Forecast
    *   Air Quality Index (AQI EU), PM2.5, and PM10
    *   Humidity, Wind Speed, UV Index, Pressure, and Visibility
*   **🌓 Adaptive UI:** The interface defaults to a premium night theme but fully supports light mode. Particle background effects dynamically adapt to weather conditions (e.g., falling rain/snow).
*   **⚡ Local Caching:** Weather data and favorite locations are cached in the browser's `localStorage` for instant loads and offline fallback.

## 🚀 Quick Start

Since RIZEN DAYS is built as a zero-build Single Page Application (SPA), getting started takes less than 10 seconds:

1. **Clone the repository:**
   ```bash
   git clone https://github.com/yourusername/rizen-days.git
   ```
2. **Open the app:**
   Simply double-click `index.html` to open it in any modern web browser.
3. *That's it!* No `npm install`, no build steps, and no environment variables required.

## 🛠️ Technology Stack

RIZEN DAYS is lightweight and fast, avoiding heavy JavaScript frameworks in favor of native browser capabilities and optimized CDNs.

*   **HTML5 & CSS3:** Semantic structure with custom CSS for glassmorphism filters, scrollbars, and keyframe animations.
*   **JavaScript (Vanilla ES6+):** Manages state, asynchronous API fetching, DOM manipulation, and HTML5 Canvas particle physics.
*   **[Tailwind CSS (CDN)](https://tailwindcss.com/):** Utility-first styling for rapid, responsive design without a build step.
*   **[Chart.js](https://www.chartjs.org/):** Powers the Interactive Meteogram and historical trends.
*   **[Phosphor Icons](https://phosphoricons.com/):** Consistent, clean SVG icon set.

## 🌐 API Services Used

This project relies entirely on robust, free-to-use APIs that do not require authentication for non-commercial use:

*   **[Open-Meteo](https://open-meteo.com/):** Provides the core Weather Forecast, Air Quality, and Geocoding APIs.
*   **[OpenStreetMap Nominatim](https://nominatim.openstreetmap.org/):** Handles highly accurate reverse geocoding when using the "Locate Me" feature.

## 🤝 Contributing

Contributions, issues, and feature requests are always welcome! 
If you have ideas to improve the UI or add new weather metrics, feel free to check the [issues page](../../issues) or submit a Pull Request.

## 📄 License

This project is open-source and available under the [MIT License](LICENSE).