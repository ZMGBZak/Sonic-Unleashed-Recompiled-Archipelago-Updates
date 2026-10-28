# Sonic Unleashed Recompiled × Archipelago — Updates

Public, **metadata-only** repository for the Archipelago connector update checker.

**No game content, backups, private saves, or client binaries are distributed here.**

## How it works

The game checks [`updates/manifest.json`](updates/manifest.json) for the current client and APWorld versions. These are deliberately set to `0.0.0` until an actual, legally reviewed release is ready.

The private development repository is separate. Never copy the development/build/game directory here.

## Publication rules

- Publish only release metadata and separately reviewed distributable files.
- Never include game dumps, proprietary game assets, extracted textures/models/music/video, local backups or patch scripts with private data.
- Review source licenses and redistribution conditions before offering compiled binaries.
- For releases, use an allowlist of approved files and verify each artifact before upload.
- Keep checksums and download links explicit. Do not claim an update is available before publishing an actual release.
- Do not store GitHub tokens in the client.

## Planned updates

- **Client:** notify about a newer version, then a separate updater will install approved client files after the game exits.
- **APWorld:** notify users and point them to an approved GitHub download page. It is not automatically installed.
