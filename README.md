# Nearby Essentials

A web app that finds the nearest pharmacies, ATMs, clinics, cafes, restaurants and bus stops around you, ranked by distance, with car, bike and walking times.

**Live site:** PASTE_YOUR_GITHUB_PAGES_LINK
**Course:** MAI412-2 Full Stack Development, CIA-I, Christ (Deemed to be University)

## Problem
On OpenStreetMap, search is not tied to the user's location. After pressing "locate me" and searching "pharmacy", results appeared outside India; the user had to type an area name such as "pharmacy near Hosur Road". Results also show no distance, and travel time needs a separate directions tool.

## Solution
One flow: locate or type an address, pick a category, read a distance-ranked list, and tap Directions for car, bike and walk times.

## Features
- Use my location or search by address, with live form validation
- Six categories and a radius from 500 m to 25 km
- Results sorted by distance, shown on a Leaflet map
- Directions with car, bike and walking time and distance
- Saved places stored in the browser (localStorage)
- Loading, empty and error states; responsive layout; hover effects

## Tech stack
HTML5 (semantic tags), Tailwind CSS (CDN), JavaScript (Fetch API, JSON, DOM events), Leaflet.

## APIs used
- Nominatim (address search and reverse geocoding)
- Photon (backup address search)
- Overpass API (places around a point, 4 servers raced)
- Nominatim bounded search (backup for places)
- routing.openstreetmap.de (car, bike, foot routes)
- Browser Geolocation API and localStorage

## Run locally
    git clone YOUR_REPO_URL
    cd nearby-essentials
    python -m http.server 8000
Open http://localhost:8000 (location only works on https or localhost).

## Limitations
Public OSM servers can be slow or rate-limited; OSM data is volunteer-edited so some places are missing; saved places are per browser; only the 15 nearest results are shown.

## Data and credits
Map data (c) OpenStreetMap contributors. 

## AI usage declaration
AI assistance (Claude) was used to help interpret the case study, suggest usability problems, generate and debug the initial code, and draft documentation. The team tested OpenStreetMap, verified every observation, ran and tested the application, added media, set up GitHub, deployed the site, and can explain the full implementation.