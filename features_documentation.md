# 🌟 Features

RIZEN DAYS is packed with modern weather features designed to provide actionable intelligence rather than just raw numbers.

### 🔍 Smart Search & Geolocation
*   **Global Search:** Search for any city or region worldwide.
*   **Reverse Geocoding:** Click the "target" icon to automatically detect your location using the browser's Geolocation API and translate coordinates into a readable city name.
*   **Favorites & Recents:** Save frequently visited cities. The app automatically tracks your recent searches for quick switching.

### 📊 Interactive Data Visualization
*   **Custom Meteogram:** A smooth, Chart.js-powered area chart showing the temperature trend over the next 24 hours.
*   **Dynamic Backgrounds:** The chart visually splits into day/night vertical bands.
*   **Canvas Animations:** Raindrop and splash animations physically interact with the chart curve based on precipitation probability.

### 🧠 Weather Intelligence
*   **Smart Recommendations:** Actionable tiles that advise on:
    *   **Clothing:** (e.g., Heavy Coat, Light Jacket) based on temperature.
    *   **Gear:** (e.g., Umbrella, Sunglasses) based on rain probability and UV index.
    *   **Health:** (e.g., Wear Mask, Sunscreen) based on AQI and UV levels.
    *   **Activity:** Advice on outdoor activities based on wind speed and storms.
*   **Quick Intel:** A dynamically generated text summary of the day's weather outlook.

### 🌍 Air Quality & Metrics
*   **AQI Tracker:** Real-time European AQI, PM2.5, and PM10 metrics.
*   **Deep Metrics:** Sunrise/Sunset times, UV Index, Pressure, Visibility, and Cloud Cover.

### ⚡ Offline & Caching
*   **Local Caching:** Weather data is cached in `localStorage` for 2 hours to prevent API spam and ensure instant loads on refresh.
*   **Offline Indicator:** If network connection drops, the app falls back to the last cached data and displays an offline badge.