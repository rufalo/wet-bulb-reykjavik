<img src="assets/icon.svg" width="64" height="64" alt="">

# Wet Bulb Reykjavík

A one-screen web app that shows the current **wet bulb temperature** in Reykjavík, Iceland. Add it to your phone's home screen and it opens like an app.

- **Data:** latest hourly observation from the Icelandic Met Office (Veðurstofa Íslands) Reykjavík station via `xmlweather.vedur.is`. If that fails, it falls back to Open-Meteo model data. Neither needs an API key.
- **Calculation:** wet bulb is solved from temperature, relative humidity and station pressure using the psychrometric equation (bisection), not the Stull approximation, which is about 0.5–0.7 °C too cold near freezing.
- Refreshes when opened, every 10 minutes, and on the Refresh button. The last reading is cached so it shows instantly.

It's plain static files (`index.html`, `manifest.webmanifest`, `sw.js`, `assets/`), so you can host it anywhere: GitHub Pages, Netlify, etc.

## Add to home screen

- **iPhone (Safari):** Share → *Add to Home Screen*
- **Android (Chrome):** ⋮ menu → *Add to Home screen* / *Install app*
