# Experimental predictions

Updated for FlowFinder 2.1.19 (242), 17 November 2026.

- [shortlist.json](shortlist.json): 78 compatible English Prediction B selections refreshed from the latest frozen Lab rankings (source 0.10.8-web.1). Evidence dates remain per gauge; older evidence retains the previous compatible selection. Research rankings are not automatic model promotion or proof of future accuracy.
- [bundled/index.json](bundled/index.json): SHA-256 index of the fitted prediction assets packaged in this release.
- [bundled/prediction/welsh.json](bundled/prediction/welsh.json): 11 early experimental Welsh station/parameter models, stage-only A and own-rain B, 1–48 hourly leads. Source coefficient file hashes are included. No upstream-network challenger is enabled in the phone.
- [bundled/prediction/rivers.json](bundled/prediction/rivers.json): English model/gauge index; individual coefficient files are in the same folder.
- [bundled/prediction/leven-sluices.json](bundled/prediction/leven-sluices.json): Leven experimental latent drainage regimes. Estimated/scenario counts are unconfirmed, not live gate telemetry.
- [bundled/runout/models.json](bundled/runout/models.json): falling-water references, with fitted *-curves.csv files beside it. Raw training observations are excluded.

Only shortlist.json is installed by the existing online prediction trial. Open Settings → Experimental → Online prediction updates, Check GitHub, review, then Use update. Fingerprints and evidence requirements are checked. Use bundled predictions restores local choices.

The button shows git or loc beside the actual fitted model version. git means an applied compatible downloaded selection, not remotely installed model coefficients. Welsh and Leven gate coefficients remain loc in this build. Highlight GitHub text is a separate optional setting for downloaded notes, widget short-name overrides and online prediction selections.

The bundled folder is a public inspection snapshot. Editing it does not update coefficients, mappings, thresholds or app code on users' phones. These require a separately validated app/data-loader update. No release schedule or validated uncertainty band is claimed for the Welsh research fits. Missing inputs remain unavailable; they are never replaced with zero rain.

Source environmental observations: Environment Agency (OGL v3), NRW and the source notices in the models. Research rainfall: Open-Meteo / ERA5-Copernicus, CC BY 4.0. Fitted references are research material, not a guarantee of safety, access or paddling suitability. No private logs, screenshots, credentials, personal contact data or research databases are included.
