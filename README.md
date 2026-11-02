# FlowFinder online information trial

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
