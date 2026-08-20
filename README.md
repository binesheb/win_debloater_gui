# Windows Debloater GUI

A small Windows Forms prototype for selecting installed AppX applications and removing the selected items.

## Current status

This is an early prototype. The repository currently contains the main form logic only; project/solution files and a packaged installer are not included.

Versioning follows Semantic Versioning. The current maintenance baseline is `0.1.1`.

## Safety

Removing AppX applications changes the current Windows user profile. Review the selection carefully and create a restore point or other backup before making system changes. The tool should not claim success until the PowerShell command has completed.

## Updating

### Automatic update

An unattended self-updater is intentionally not enabled in this prototype. Future packaged builds should check GitHub Releases for a newer version, show the release notes, and require explicit confirmation before downloading and replacing the application.

### Manual update

For a source checkout:

```powershell
git fetch --tags --prune
git pull --ff-only
```

To reproduce a known version, check out a release tag or exact commit. To roll back, check out the previous known-good tag or commit and rebuild.

## Next steps

- Add a Visual Studio solution/project and reproducible build instructions.
- Replace display-name wildcard matching with explicit package identifiers.
- Add preflight checks and per-package result details.
- Package signed builds and add an opt-in GitHub Release update check.
