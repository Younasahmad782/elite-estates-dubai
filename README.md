# ELITE ESTATES DUBAI — Luxury Real Estate Website

A complete, bilingual (English / العربية) luxury real estate agency website for the
fictional Dubai brand **ELITE ESTATES DUBAI** — "Discover Exceptional Living."

## How to open it

**Option 1 — open the file directly:** unzip and double-click `index.html`.
**Option 2 — serve it locally:** `python3 -m http.server 8000` inside the folder,
then open http://localhost:8000

Everything is self-contained: the page, 39 photographs and the fonts (Playfair Display,
Poppins, Amiri, Tajawal) all live in this folder. No build step, no backend, no CDN.

## What is inside

- **Hero** — cinematic Dubai skyline, animated headline, BUY / RENT / OFF-PLAN tabs,
  and a working search (location, type, min/max price, bedrooms) that filters the
  real listing data and jumps to the results.
- **Featured properties** — 7 handpicked listings with hover zoom, favourite hearts
  (saved in localStorage, survives reload) and demo-listing badges.
- **Property discovery** — all 12 listings with text search, status chips
  (All / Buy / Rent / Off-Plan / Favourites), type, area, price and bedroom filters,
  sorting (newest, price low→high, high→low), result counts and an empty state.
- **Property detail view** — full gallery (arrows, thumbnails, full-screen lightbox,
  keyboard navigation), specs, bilingual description, features, amenities, nearby
  attractions, demo location card and 3 similar properties.
- **Enquiry + booking** — tabbed panel: send an enquiry or book a viewing (date +
  time) with full validation and a demo confirmation screen. WhatsApp and Call
  buttons; the WhatsApp message is prefilled with the property name.
- **ROI calculator** — purchase price, annual rent, maintenance → net income,
  gross and net yield, with an "illustrative estimates, not financial advice" note.
- **Locations** — Downtown, Marina, Palm Jumeirah, Business Bay, Dubai Hills,
  JVC. Each card filters the listings by that area.
- **Off-plan projects** — 3 fictional developments with developer, starting price,
  completion date and payment plan, opening a detail modal.
- **About** — story, approach, animated demo statistics (labelled fictional).
- **Testimonials** — carousel with prev/next controls and dots (fictional samples).
- **Bilingual** — instant EN ↔ عربي toggle, full RTL layout, Arabic typography,
  every string translated (navigation, buttons, forms, validation, property data,
  footer). Language is remembered between visits.
- **List Your Property** — modal form with validation and a demo confirmation.
- **Footer** — quick links, locations, newsletter (validated, demo), privacy and
  terms modals.
- **Floating WhatsApp button** — bottom-right in English, mirrored bottom-left in
  Arabic, property-specific prefilled message.

## Demo notes (important)

- All 12 properties, 3 off-plan projects, testimonials and statistics are
  **fictional demonstration content**, labelled as such on the site.
- The WhatsApp number **+92 345 7305226** is the developer's real number —
  messages from the floating button, property enquiries and the call button all
  go to it. The email `hello@eliteestates-dubai.demo` is still a demo address.
- Forms (enquiry, booking, contact, newsletter, list-your-property) are
  **frontend-only demos** — nothing is sent anywhere; no backend is connected.

## Files

```
elite-estates/
  index.html          The whole website (HTML + CSS + JS, one file)
  photos/             39 photographs (hero, properties, interiors, locations, off-plan, office)
  photos/manifest-*.json   Photo sources
  fonts/              Playfair Display, Poppins, Amiri, Tajawal
  screenshots/        Desktop / mobile / Arabic screenshots
  README.md           This file
```

## Verification (2026-11-08)

65/65 Playwright checks green, both languages, at 360 / 390 / 430 / 768 / 1280 /
1440 / 1920 px: search and filters (incl. empty state and reset), sorting,
detail view and gallery, enquiry validation + booking success, favourites
persistence across reload, ROI math, testimonials, location filtering, off-plan
modal, list-your-property modal, contact + newsletter validation, RTL layout and
mirrored WhatsApp button, mobile drawer, zero horizontal overflow, zero console
errors.
