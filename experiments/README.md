# Experimental feature inventory

Checked against the current FlowFinder implementation on 17 November 2026.

## GitHub-backed files

- **Online information:** [`../content.json`](../content.json). Its `entries` array is available for public help, issues, patch notes and supplementary river notes. An empty array is valid; built-in notes remain available.
- **Widget names:** the same file's `sectionShortNames` object. Currently contains the Leven and Lune overrides. All other section labels are generated locally, so an override is only needed when a generated name should change. Section IDs must already be known to the installed app; labels are at most 20 characters.
- **Online Prediction B selections:** [`../predictions/shortlist.json`](../predictions/shortlist.json), with [format and compatibility notes](../predictions/README.md). Contains 78 gauge selections from the 17 November 2026 frozen matched ranking export. Each selection names an installed candidate, its evidence and the exact coefficient-file fingerprint.

Use the app's own validation and preview before applying changes. A published selection is research evidence, not proof of future accuracy. Wrong-gauge levels and paddling thresholds cannot be interchanged.

## Public inspection snapshots

[predictions/bundled/index.json](../predictions/bundled/index.json) lists the release coefficient files and fitted runout curves, including Welsh and Leven experimental models. These are files to inspect; the app does not download/install these coefficients. The optional Highlight GitHub text setting marks downloaded notes/names/selections. Source/version labels distinguish git selections from loc models.

## Experiments currently implemented in the app

These run locally and are not remotely installed. Fitted-data inspection snapshots are linked above:

- Basic/Research prediction engines, coefficient files and shaded model-spread areas.
- Leven drainage/gate scenarios and retrospective suspected gate-change markers. No confirmed live gate feed.
- 48-hour prediction opt-in and its supported horizon.
- Runout curves and their bundled fitted data.
- Cumulative rainfall map totals.
- Recent modelled rain icons.
- Private river reports and manual sharing.
- Experimental enable/disable choices, which stay on the device.

Changing these algorithms or adding new coefficient files, gauges, gauge assignments or remote configuration support currently requires an app update. The online shortlist only selects among compatible candidates already installed. This repository does not contain the full app source code or a remote feature-switch system.

## Privacy

The existing online features make explicit public GitHub downloads. No personal logs, reports, API keys, device location or profile data are uploaded by these features. GitHub receives normal connection information, including the requesting IP address. This index adds documentation, not a new network service or new data collection.
