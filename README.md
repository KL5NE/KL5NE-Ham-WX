# KL5NE Ham WX

A CORSAIR XENEON EDGE dashboard for ham-radio operating conditions and local Palmer, Alaska weather.

## What it shows

- NOAA SWPC space weather: Solar Flux Index, planetary Kp, running A, IMF Bz, and solar-wind speed
- Alaska-oriented HF condition summary and simple 10/15/20/40/80 m indicators
- Polar-path caution
- National Weather Service current conditions and short hourly forecast for Palmer, Alaska
- Local time and UTC
- Cached last-good readings when a service is temporarily unavailable

## Requirements

- CORSAIR iCUE 5.47+
- XENEON EDGE
- iCUE Widget CLI for local validation/packaging if desired

Install the CLI locally with:

```bash
npm install -g icuewidget-cli
```

Validate and package:

```bash
icuewidget validate .
icuewidget package . -o KL5NE-Ham-WX.icuewidget
```

## GitHub Actions build

The included workflow automatically validates and packages the widget on each push to `main` and on manual runs.

To download a build:

**Actions → Build iCUE Widget → latest successful run → Artifacts → KL5NE-Ham-WX**

## Data sources

- NOAA Space Weather Prediction Center
- National Weather Service API

No API keys are required.

## Default location

Palmer, Alaska city-center coordinates: 61.5997, -149.1128.

The location label, latitude, and longitude are exposed as widget settings.

## Note about HF indicators

The Alaska HF impact, polar caution, and band badges are deliberately simple operator heuristics derived from Kp, Bz, solar-wind speed, and solar flux. They are not a substitute for a full propagation model.

## Version

0.1.0
