# 🐻 Bearing Compass 🧭

Calculate true and magnetic bearings between waypoints on a map.

**Usage**: Open in your browser. Click to add waypoints, double-click to zoom.

## Features

- Calculate true bearing, magnetic bearing, declination, and distance for route legs
- WMM2025 magnetic model (valid 2025-2030) embedded, no API calls
- Mobile-optimized with swipeable result cards
- Shareable URLs with encoded waypoints
- Color-coded routes

## Tech Stack

- **[Leaflet.js](https://leafletjs.com/)** - Map rendering
- **[OpenTopoMap](https://opentopomap.org/)** - Topographic tiles
- **[geomagJS](https://github.com/cmweiss/geomagJS)** - WMM2025 implementation
- Single self-contained HTML file

## Methodology

**True Bearing**: Forward azimuth formula on WGS84 ellipsoid
**Distance**: Haversine formula (great circle)
**Magnetic Bearing**: True bearing adjusted by WMM2025 declination

```
Magnetic Bearing = True Bearing - Declination
```

Declination accuracy: ±1°, sufficient for navigation.

## Data Sources

- **WMM2025**: [NOAA NCEI](https://www.ncei.noaa.gov/products/world-magnetic-model) (public domain)
- **Map tiles**: [OpenTopoMap](https://opentopomap.org/) / [OpenStreetMap](https://www.openstreetmap.org/) (CC-BY-SA 3.0)

## Credits

- Christopher Weiss ([@cmweiss](https://github.com/cmweiss)) - geomagJS
- Vladimir Agafonkin - Leaflet.js
- NOAA NCEI - World Magnetic Model