# Maps

> Geocode, find nearby POIs, calculate routes and distances using OpenStreetMap/Nominatim/OSRM — 44 categories, no API key required.

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://github.com/Marrowleaf/hermes-maps)

## Features

- 8 commands: search, reverse, nearby, distance, directions, timezone, area, bbox
- 44 POI categories (restaurants, hospitals, pharmacies, hotels, etc.)
- Auto-geocode addresses with `--near` flag for nearby searches
- Driving, walking, and cycling routes via OSRM
- Timezone lookups for any coordinates
- Bounding box area calculations
- Clickable Google Maps URLs in results
- Zero dependencies (Python stdlib only) — no API key required
- Telegram location pin support

## Installation

```bash
hermes skills install productivity/maps
```

Or manually clone into `~/.hermes/skills/productivity/maps/`.

## Usage

```bash
# Search for a place
python3 ~/.hermes/skills/maps/scripts/maps_client.py search "Eiffel Tower"

# Find nearby restaurants
python3 ~/.hermes/skills/maps/scripts/maps_client.py nearby --near "Times Square" --category restaurant --limit 10

# Calculate driving distance
python3 ~/.hermes/skills/maps/scripts/maps_client.py distance "Paris" --to "Lyon" --mode driving

# Get walking directions
python3 ~/.hermes/skills/maps/scripts/maps_client.py directions "Big Ben" --to "Tower Bridge" --mode walking

# Timezone lookup
python3 ~/.hermes/skills/maps/scripts/maps_client.py timezone 48.8584 2.2945
```

## Configuration

No additional configuration required. No API key needed — uses free OpenStreetMap, Nominatim, Overpass, and OSRM APIs.

## Requirements

- Python 3.8+ (stdlib only — no pip installs)
- Internet access for API calls
- Note: Nominatim ToS limits to 1 request/second (handled automatically)

## License

MIT