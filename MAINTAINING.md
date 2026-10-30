# Maintaining Liangtu

The canonical repository is https://github.com/shelter1995/liangtu, with Windows source at the root of `main`. Track issues and publish future Windows releases here. Keep the former fork available for existing users and historical links.

## Development

Use the .NET 8 SDK, PowerShell 7, Visual C++ Build Tools and Windows SDK on Windows x64. From the repository root:

```powershell
pwsh -NoProfile -File test-safe.ps1
pwsh -NoProfile -File build.ps1
```

Run additional checks for the area being changed. Off-screen/simulated checks and physical desktop validation have different scopes; describe the actual coverage in `docs/verification-v<version>.md`.

## Releases

1. Update the application version and installer defaults together. Build from the exact source commit that will be tagged.
2. Follow `docs/windows-release-checklist.md`. Keep the `windows-v<version>` tag and `Liangtu-<version>-...` asset names, since the updater checks these formats.
3. Verify portable manifests, package SHA-256, installer metadata and the matching source commit. Publish installer EXE, installer bundle, portable ZIP and their SHA-256 files as applicable.
4. Update both README languages and release notes with tested behavior and remaining limitations. Retain upstream attribution, license notices and third-party component notices.

Only source on `main` has the migrated update endpoint. Do not replace historical release assets under an existing tag to add this change. Publish a new version when ready, and tell users of the migrated releases to upgrade manually from this repository.

Automatic work or release scheduling is not configured. Future development and releases are performed in response to maintenance requests.
