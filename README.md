# Yaris Cross Hybrid — Fuel Ledger (2023–2025)

A single-page presentation of three years of fuel records for a Toyota Yaris Cross
Icon HEV, reconciled against till receipts. Every implausible economy figure was
traced back to a real transaction rather than smoothed away.

**Headline:** 23,161 miles · 1,816.53 L · £2,560.98 · **58.8 MPG lifetime** (UK, brim-to-brim).

## View it

- **Live page:** <https://mveplus.github.io/Fuel-ledger-Toyota-Yaris-Cross-Hybrid/>
- **Offline:** open `index.html` directly in a browser. All assets are local — no internet needed.
- **GitHub Pages setup:** `index.html` is at the repo root; Settings → Pages → deploy from `main`.

## What's inside

```
index.html                     the page (data embedded inline)
assets/
  chart.umd.min.js             Chart.js 4.4.3 (vendored)
  chartjs-adapter-date-fns…js  time-axis adapter + date-fns (vendored)
  fonts.css + fonts/           Space Grotesk, IBM Plex Sans, IBM Plex Mono (latin)
  img/                         vehicle photos (see note below)
```

The companion spreadsheet (`Yaris_Cross_fuel_log.xlsx`) holds the full formula-driven
model: per-fill log, brim-to-brim MPG, courtesy-car sheet, and a summary with chart.

## Method

MPG is calculated **brim-to-brim**: miles between two full tanks ÷ (litres refilled ÷ 4.54609),
with partial fills rolled into the following full tank. This is robust to missing logs —
the lifetime figure divides total distance by total fuel between the first and last full tank.

Five corrections were applied from receipts and the odometer:

| Date | Change | Effect |
|------|--------|--------|
| 22/12/2023 | date typo (was 22/12/2024) | chronology only |
| 24/04/2024 | date typo (was 24/02/2024) | chronology only |
| 31/05/2024 | 6.95 L/£10 → 30.42 L/£43.77 | removed false 97 MPG |
| 21/10/2024 | date corrected (was 28/10/2024) | same fill, 16,624 mi |
| 11/10/2024 | added missing 31.48 L/£41.52 fill | removed false 82 MPG |

Dates are DD/MM/YYYY. Prices in GBP. Imperial gallon = 4.54609 L.

## Vehicle (anonymised V5C)

Identifying fields (registration, VIN, engine number, document reference, dealer) are
deliberately omitted. Technical details only:

| Field | Value |
|-------|-------|
| Model | Toyota Yaris Cross Icon HEV (auto) |
| First registered | April 2023 |
| Body / category | 5-door SUV / M1 |
| Powertrain | 1.5 L petrol-electric hybrid, 1490 cc |
| Max net power | 68 kW |
| Fuel / tax class | Hybrid electric / Alternative fuel car |
| CO₂ | 100 g/km |
| Emissions standard | Euro 6 AP, RDE2 |
| CO / THC / NOₓ | 0.157 / 0.016 / 0.007 g/km |
| Kerb weight (mass in service) | 1254 kg |
| Max permissible mass | 1690 kg |
| Towing — braked / unbraked | 750 / 550 kg |
| Noise — stationary / drive-by | 71 dB(A) @ 2500 min⁻¹ / 68 dB(A) |
| Seats | 5 |
| Colour | Grey |
| Type approval | e6\*2018/858\*00013\*03 |

## Privacy / image handling

All photos in `assets/img/` have been processed before publication:

- **EXIF metadata stripped**, including GPS — the source photos carried location
  coordinates; the published copies carry none.
- **Number plates redacted** (front, rear, and front three-quarter views).
- Three views (`front-quarter`, `rear-quarter`, `rear`) are background-removed cutouts,
  so they reveal no surroundings. `front.jpg` and `side.jpg` retain a generic driveway
  background and are not used on the page.

## Licence

Fonts are Fontsource builds (SIL OFL 1.1 / Apache-2.0), redistributable.
Chart.js is MIT. Vehicle data and photos © the owner.
