# HomeOS Prototype 0.3.0 — Home Dashboard

This release upgrades the Home dashboard while preserving the existing IPTV, entertainment, AI demo, smart-home demo, apps and settings modules from 0.2.5.

## New in 0.3.0
- Redesigned responsive home dashboard with welcome panel and quick launch
- Clock/date, TV, entertainment, assistant, devices and system widgets
- Customise dashboard: hide/show widgets, move up/down, compact spacing, reset
- Customisations saved in the existing browser localStorage key (`homeos01`)
- Unified version 0.3.0 across header, Settings and diagnostics

## Deploy to GitHub Pages
Upload **all five files** into the repository root, replacing older versions, and commit. Then visit https://kingandcastle.github.io/homeos-prototype/?v=030#dashboard

## Notes
The smart-home and AI modules are still demonstrations. Weather is intentionally not shown as live weather because no weather provider or location permission is configured. The IPTV module remains at its 0.2.5 functional baseline. No API keys are required.
