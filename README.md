# Wanderseason

Find the best places to visit by month across anywhere in the world. Every place has a 3-day itinerary, photo spots, where to eat (including gelato and sweet stops), a budget calculator, visa rules by passport, what to book, ways to save on lodging, and a packing list that follows the season.

It is a single static page with no build step and no dependencies. Open `index.html` in a browser, or host the folder anywhere.

## Run it

    python3 -m http.server 8000

Then open http://localhost:8000.

## Put it online

Turn on GitHub Pages for this repository (Settings, Pages, deploy from the `main` branch). GitHub Pages on a free account needs a public repository.

## Put it on a phone

- **Quickest:** open the hosted link on a phone and choose "Add to Home Screen". The included manifest and service worker make it behave like an app and open offline after the first visit.
- **App Store and Google Play:** wrap the same page with [Capacitor](https://capacitorjs.com/). You need an Apple Developer account and a Google Play developer account.

      npm init -y && npm i @capacitor/core @capacitor/cli @capacitor/ios @capacitor/android
      npx cap init Wanderseason com.example.wanderseason --web-dir .
      npx cap add ios && npx cap add android
      npx cap open ios      # or: npx cap open android

## Data

Places, budgets, food and booking notes live in `index.html` (search for `const D=[` and `const X={`). Visa rules are in the `entry()` function. Budgets are rough estimates in US dollars per person per day, without flights.

Visa rules were last checked on Oct 3, 2026 from government pages and travel sites. They change often, so confirm on the official site before booking. Festival dates, closures and reservation rules change every year too.

## Copyright

© 2026 Lalitha Priya Gorre. All rights reserved. See `LICENSE`. This repository being visible does not grant permission to copy or reuse it.
