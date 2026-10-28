# Client updater: release and file policy

**Status: locked / planning stage. No real client downloads authorized.**

## Default-deny policy

The [machine-readable policy](../updates/release-policy.json) has `approved_install_paths: []`. Until the project reviews the exact client build, upstream license obligations and which files may legally be redistributed, **no file may be installed**.

To approve a future file, document its *exact relative destination path* (never a wildcard), its ownership/license, why it is required, and whether it can be updated without affecting user progress. Add that path to the allowlist only after review. Neither `.exe` nor `.dll` is automatically allowed.

## Mandatory checks for each real Release

1. Review contents and licensing before uploading source or binaries. Never upload game dumps or extracted proprietary audio, textures, videos, models or archives.
2. Release artifact must be assembled from a curated list; **never zip the game folder or build directory**.
3. Never package `.bak`, `.backup`, `.old`, temporary files, diagnostics, crash reports, configuration, credentials or per-seed Archipelago state.
4. Use a versioned GitHub Release, not a mutable branch URL, for client payloads. Require explicit version, asset URL, expected byte size and SHA-256 hash. Limit URL origin and redirect destinations.
5. An updater must **fail closed** for missing or invalid metadata, path traversal, absolute paths, symlinks, disallowed extensions, duplicate or ambiguous paths, unexpected files, hash mismatches, missing signatures and stale or downgraded releases.
6. An authenticated GitHub HTTPS download plus a SHA-256 string fetched from the same modifiable manifest does **not** alone protect against a compromised publisher account. Plan for a trusted signing key and signed release manifests before unattended installation.
7. Stage and verify *everything* before modifying files; wait for the game process to exit; preserve user data; use a journal and recover after interruption or power loss. Test on clean installations.
8. APWorld is versioned independently and downloaded manually. Advise players that some changes require regenerating a multiworld.

## Sample future manifest (documentation only; not active)

```json
{
  "schema_version": 2,
  "client": {
    "version": "1.0.0",
    "release_url": "https://github.com/OWNER/UPDATES/releases/tag/v1.0.0",
    "files": [
      {
        "install_path": "EXACT_APPROVED_CLIENT_FILE.dll",
        "download_url": "https://github.com/OWNER/UPDATES/releases/download/v1.0.0/EXACT_APPROVED_CLIENT_FILE.dll",
        "size": 12345,
        "sha256": "64 lowercase hex characters"
      }
    ]
  },
  "apworld": {
    "version": "1.0.0",
    "download_page": "https://github.com/OWNER/UPDATES/releases/tag/apworld-v1.0.0"
  }
}
```

This sample is **not** a valid downloadable manifest until real reviewed values replace every placeholder. The live `updates/manifest.json` stays at `0.0.0` to preserve the current working F8 checker.

## How to validate future files

A release validator must compare all payload paths against the exact allowlist and verify size and SHA-256 after download. The allowlist in this repository is **documentation for future implementation**; it currently does not change or govern the executable updater.
