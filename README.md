# Shopview Importer — Updates

This repository hosts the version manifest for the [Shopview Importer Chrome extension](https://github.com/YOUR-USERNAME/shopview-importer-updates).

The extension fetches `version.json` on startup to check if a newer version is available. If yes, it shows a banner to team members with a download link.

## How to publish a new version

1. Edit `version.json` and bump the `version` field (semver: e.g. `1.2.0` → `1.3.0`).
2. Update `releaseNotes` with a short description of what changed.
3. Update `downloadUrl` if the location of the new build has changed.
4. Commit the change.

That's it — all installed extensions will detect the update within a minute of opening.

## Version file format

```json
{
  "version": "1.3.0",
  "downloadUrl": "https://example.com/path-to-latest-build.zip",
  "releaseNotes": "Short summary of what's new in this release"
}
```

| Field | Description |
|---|---|
| `version` | Semver string. Must be higher than installed version to trigger banner. |
| `downloadUrl` | Where users go to download the new build (zip, Drive link, GitHub release, etc.) |
| `releaseNotes` | Short text shown in the update banner inside the extension. |
