# 🌐 API Services

RIZEN DAYS relies entirely on robust, free-to-use APIs that do not require authentication or API keys for non-commercial use. 

### 1. Open-Meteo Forecast API
*   **Endpoint:** `https://api.open-meteo.com/v1/forecast`
*   **Usage:** Fetches current weather, hourly forecasts (temperature, precipitation, weather codes), and daily forecasts (min/max temps, sunrise/sunset, UV index).
*   **Features Used:** `past_days=7` for historical chart context, auto-timezone alignment.

### 2. Open-Meteo Air Quality API
*   **Endpoint:** `https://air-quality-api.open-meteo.com/v1/air-quality`
*   **Usage:** Retrieves European AQI and specific particulate matter (PM10, PM2.5) concentrations.

### 3. Open-Meteo Geocoding API
*   **Endpoint:** `https://geocoding-api.open-meteo.com/v1/search`
*   **Usage:** Powers the "Smart Search" bar, translating city text inputs into accurate latitude and longitude coordinates.

### 4. Nominatim (OpenStreetMap) API
*   **Endpoint:** `https://nominatim.openstreetmap.org/reverse`
*   **Usage:** Used specifically for *reverse* geocoding. When a user clicks "Use My Location", the browser provides coordinates. Nominatim translates these coordinates into a highly accurate, human-readable city or neighborhood name.