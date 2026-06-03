# Claude Property Hunt

Italy Property Hunt Planner — an interactive single-page application for planning a 63-night Italian property scouting trip.

Built by Claude from configuration data in [italy_property_hunt_planner](https://github.com/dankraut/italy_property_hunt_planner) (read-only source).

## Features

- **Property Browser** — searchable/filterable table of 627 Italian properties, filter by region, province, realtor, sort by price or size
- **Itinerary Planner** — four suggested itineraries (A–D), each showing base towns with nights, radius, and live property-count within range
- **Constraint Panel** — trip parameters, car swap dates, and hard date commitments in the sidebar
- **Interactive Map** — Leaflet map with base location markers, radius circles, and car swap points

## Data

All data is sourced read-only from [`italy_property_hunt_planner/client/src/config`](https://github.com/dankraut/italy_property_hunt_planner/tree/main/client/src/config):

| File | Contents |
|------|----------|
| `data/properties.json` | 627 Italian properties (town, province, region, price, rooms, size, realtor) |
| `data/locations.json` | 26 base locations with long-stay/short-stay classification |
| `data/itineraries.json` | 4 suggested itineraries (A, B, C, D) |
| `data/constraints.json` | Trip parameters, car swap dates, hard date commitments |
| `data/coordinates.json` | Lat/lng for 245 towns used in radius calculations |

## Running Locally

Because the app loads data files via `fetch()`, you need an HTTP server:

```bash
git clone https://github.com/dankraut/Claude-property-hunt.git
cd Claude-property-hunt
python3 -m http.server 8080
# Open http://localhost:8080
```

## Trip Overview

- **Departs:** June 9, 2026 · **Duration:** 63 nights
- **Car swaps:** Florence Airport (day 26) · Turin Airport (day 56)
- **Hard commitments:** Children's visit Aug 6–11 · Asti/Bra Jul 22–25
