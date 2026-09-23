# Fogline Stays: San Francisco Airbnb Listings

A web page that loads and displays the first 50 Airbnb listings in San Francisco, built with vanilla HTML, CSS and JavaScript for the CS5610 JavaScript and DOM self-assessment.

## Live demo

https://hard3007.github.io/webdev_fall-2026-self-ass-2/

## What it does

The page loads `airbnb_sf_listings_500.json` with `fetch` and `await`, keeps the first 50 listings, and renders each one with its name, description, amenities, host name and photo, nightly price and thumbnail.

You can search by listing name or neighborhood, filter by room type, set a maximum nightly price with a slider, sort by price, rating or name, and switch between a list layout and a grid layout.

## Creative additions

**Trip cost calculator.** Opening a listing shows a nights stepper that calculates the total cost of the stay.

**Saved stays.** The heart button on any listing adds it to a saved panel, where every saved stay shows its total for the same number of nights so they can be compared side by side. Saved stays are kept in `localStorage`, so they survive a page reload.

**Neighborhood chips built from the data.** Instead of a hardcoded list, the neighborhood filters are generated from the listings themselves, with a count for each area.

**Golden Gate hero.** The header illustration is an inline SVG of the bridge that draws itself on page load (and stays static if the visitor prefers reduced motion).

## How it's built

All listing text is escaped before it is inserted into the page, and listing descriptions are converted from HTML to plain text with `DOMParser`. The detail view uses the native `<dialog>` element, so it closes with the Escape key and keeps keyboard focus inside while open. Listing cards can be opened with the keyboard as well as the mouse.

## Run it locally

Browsers block `fetch` on files opened directly from disk, so serve the folder instead:

```bash
python -m http.server 8000
```

Then open http://localhost:8000. VS Code Live Server works too.

## Tech stack

HTML, CSS, JavaScript, JSON, GitHub Pages

## Course

CS5610 Web Development, Northeastern University, Fall 2026
Hard Gondaliya
