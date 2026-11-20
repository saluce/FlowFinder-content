# FlowFinder GitHub experiments

Public files used by the app's optional GitHub features. Checked 20 November 2026.

| Feature | File to view/edit | What the app can use |
| --- | --- | --- |
| Online information | [content.json](content.json) | Help, known issues, release notes and supplementary river notes in `entries`. |
| Widget short names | [content.json](content.json) → `sectionShortNames` | Section-name overrides. Other sections use the app's abbreviation rules. |
| Online prediction updates | [predictions/shortlist.json](predictions/shortlist.json) | 78 compatible Prediction B candidate selections, with model fingerprints and evidence dates. |
| Fitted model files | [predictions/bundled/index.json](predictions/bundled/index.json) | Public inspection snapshot, including 11 early Welsh fits, Leven and fitted runout curves. |
| Feature inventory | [experiments/README.md](experiments/README.md) | Which experiments use GitHub and which are implemented in the app. Documentation only. |

App download addresses:

- Notes and names: https://raw.githubusercontent.com/saluce/FlowFinder-content/main/content.json
- Prediction choices: https://raw.githubusercontent.com/saluce/FlowFinder-content/main/predictions/shortlist.json

Enable Experimental and the relevant online option in FlowFinder, then explicitly refresh/check GitHub. Prediction downloads require review and Use update. The prediction address is derived from the notes address. No background polling or GitHub login is required.

These files do not install app code, new model coefficients, gauge mappings or remote settings. Incompatible prediction updates are rejected. Updating this repository does not silently enable experimental options on anyone's phone.

No private records, reports, screenshots, research databases, credentials or unpublished privacy-policy drafts belong in this repository.

## Content format and editing
# FlowFinder online information trial

The widget can read a `sectionShortNames` object from the same JSON file. Add it alongside `entries`, using section IDs as keys, for example `"sectionShortNames": {"leven": "Newby → Wood", "lune-beck": "Beck → Rawt"}`. Labels can contain up to 20 characters. Publish changes to the same notes repository and refresh Online information in Experimental to download them.

Upload `content.json` to a public GitHub repository with Pages enabled. Paste its full HTTPS file address into Settings → Experimental → Online information. A raw.githubusercontent.com file address also works. No login/token is needed or stored. Never upload personal logs, reports, passwords or keys.

Enable both the experimental master switch and Online information. Press Save address & refresh to download; there is no background polling. Old built-in content remains. Turning the experiment off hides downloaded content. Clear downloaded information removes the local copy.

This is a display-only trial: river notes supplement the Guide tab. It does not alter names, grades, gauge assignments, thresholds, access coordinates, routes or personal data. Those catalogue updates need a separately validated workflow.

The file has `format: "flowfinder-content"`, `schema: 1`, and an `entries` array. Each entry requires a unique `id`, a `kind` (`patch`, `help`, `issue` or `river`), `title`, and plain `text`. River entries also require an existing catalogue `section` ID. Optional `minVersionCode` and `maxVersionCode` restrict visibility to compatible installed builds. Use exact version-code bounds for release-specific patch notes. Plain text and bullet characters work; HTML and executable content are not interpreted.

Example entry (place inside entries):

```json
{
  "id": "leven-gate-context",
  "kind": "river",
  "section": "leven",
  "title": "Sluice gates",
  "text": "Gate operations may influence readings. No live gate-status feed is available."
}
```

Limits: 500 KB download, 500 entries, 160-character titles, 12,000-character text per entry. Invalid files are rejected in full. Redirects are rejected; use the final public file URL. Updating the same address keeps the last good copy on failure. Changing addresses clears the previous source's copy. Download timestamps are shown; publication does not confirm current river conditions. GitHub receives ordinary network connection information such as the requesting IP address.
