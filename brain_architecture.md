# 🧠 Application Brain & Architecture

This document outlines the internal logic, state management, and algorithmic processing that makes RIZEN DAYS "smart".

## State Management
The application relies on a centralized `state` object to maintain truth across the UI:
```javascript
let state = {
    lat: 25.4358, 
    lon: 81.8463,
    city: 'Prayagraj', // Default fallback
    isMetric: true,
    weatherData: null,
    aqiData: null,
    theme: 'dark', // Dark mode by default
    favorites: [...],
    recent: [...],
    currentChartView: 'trend' 
};
```
Whenever an API call resolves, or a user changes a setting (like metric to imperial), the `state` is mutated and the `updateUI()` render cycle is triggered.

## Caching Strategy
To ensure speed and respect API rate limits, RIZEN DAYS uses an aggressive local caching strategy.
1. On data fetch, `state` is serialized and saved to `localStorage` with a timestamp.
2. On initial load, `loadFromCache()` checks the timestamp.
3. If data is less than **2 hours old**, the app instantly renders from the cache, preventing an immediate network request. A background fetch can be optionally triggered to keep data fresh.

## Weather Intelligence Algorithms
The app generates human-readable text and UI components dynamically by parsing the raw API numbers.

### Smart Recommendations Logic
The `generateSmartRecommendations` function acts as a rules engine:
*   **Clothing:** Evaluates `current.temperature_2m`. `<10°C` suggests a Heavy Coat; `<20°C` suggests a Light Jacket; otherwise, Light Clothing.
*   **Gear:** Checks `daily.precipitation_probability_max`. `>40%` triggers an Umbrella recommendation. Checks `daily.uv_index_max` for Sunscreen recommendations.
*   **Health:** Evaluates `current.european_aqi`. `>100` triggers a "Wear Mask" alert, overriding normal conditions.
*   **Activity:** Looks at `current.wind_speed_10m` and precipitation probability to suggest whether it's a good day for a walk or better to stay indoors.

### Custom Chart Engine Physics
The custom Meteogram isn't just a static chart. An animation loop (`requestAnimationFrame`) uses the Chart.js dataset metadata to calculate exact X/Y coordinates on the temperature curve. 
If the underlying data index shows a high precipitation probability, the loop spawns rain particles that fall and trigger a "splash" rendering routine exactly where the particle's Y coordinate intersects the chart's curve.