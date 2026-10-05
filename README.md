# Diani Beach → Tsavo West: 3-Day Safari Route Map

An interactive 3D map of a 3-day road safari from **Diani Beach** on Kenya's south coast to **Tsavo West National Park**, with an overnight stay at **Voyager Ziwani Tented Camp**, and back again.

🗺️ **See the full itinerary and the live map:**
[3-dniowe safari do Parku Narodowego Tsavo Zachodniego z plaży Diani](https://safarikenia.com.pl/3-dniowe-safari-do-parku-narodowego-tsavo-zachodniego-z-plazy-diani/) on **Safari Kenia**

---

## The route

The map traces the real driving route between the coast and the park:

| Stop | Location | Accommodation |
|------|----------|---------------|
| Start | Diani Beach | — |
| Day 1 & 2 | Ziwani area, Tsavo West | Voyager Ziwani Tented Camp |
| Day 3 | Return to Diani Beach | — |

**Outbound:** Diani Beach → Likoni Ferry → Mariakani junction → Mackinnon Road → Voi → Mwatate → Taveta road → Ziwani
**Return:** Ziwani → Mariakani → Likoni Ferry → Diani Beach

The interface labels are in Polish, matching the tour page it's embedded on.

## Features

- **Satellite basemap with 3D terrain** — Mapbox Standard Satellite style with DEM terrain (1.5× exaggeration) and a tilted camera, so the Taita Hills and the Tsavo landscape stand out.
- **Road-accurate route** — each leg is fetched from the Mapbox Directions API (driving profile) and stitched into one line. If a request fails, it falls back to a straight segment, so the route always renders.
- **Animated route line** — a golden "marching ants" dashed line over a soft glow layer.
- **Interactive itinerary panel** — a glassmorphism sidebar lists each day. Clicking a card flies the camera to that stop and opens its popup with the lodge name.
- **Custom markers** — gold SVG pins for the main stops. Waypoints shape the route without cluttering the map.
- **Mobile-friendly** — on small screens the sidebar becomes a bottom sheet, and cooperative gestures prevent the map from hijacking page scroll.
- **WordPress-ready** — all styles are scoped to a single container, so it can be pasted into a Custom HTML block without clashing with the theme.

## Tech stack

- [Mapbox GL JS](https://docs.mapbox.com/mapbox-gl-js/) v3.9.0
- [Mapbox Directions API](https://docs.mapbox.com/api/navigation/directions/)
- Vanilla JavaScript, with no build step
- Plus Jakarta Sans (Google Fonts)

## Usage

1. Copy the contents of the HTML file into a WordPress **Custom HTML** block, or into any web page.
2. Replace the Mapbox access token with your own. Restrict it to your domain in your [Mapbox account](https://account.mapbox.com/access-tokens/).
3. Adjust the container height in `.wp-safari-itinerary-container` to fit your layout.

To change the route, edit the `itineraryData` array. Entries with `isWaypoint: true` shape the route only. All other entries get a marker and a sidebar card.

## About

Built for [Safari Kenia](https://safarikenia.com.pl/), Polish-language safari tours and travel guides for Kenya.

➡️ [View this safari itinerary](https://safarikenia.com.pl/3-dniowe-safari-do-parku-narodowego-tsavo-zachodniego-z-plazy-diani/)
