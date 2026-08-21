# Windows Debloater GUI

A small Windows Forms prototype for selecting installed AppX applications and removing the selected items.

## Current status

This is an early prototype. The repository currently contains the main form logic only; project/solution files and a packaged installer are not included.

Versioning follows Semantic Versioning. The current maintenance baseline is `0.1.1`.

## Safety

Removing AppX applications changes the current Windows user profile. Review the selection carefully and create a restore point or other backup before making system changes. The tool uses explicit AppX package identifiers rather than display-name wildcard matching and reports packages that fail or are not installed.

## Updating

### Automatic update

An unattended self-updater is intentionally not enabled in this prototype because the project is not yet packaged or signed. If an automatic update check is added later, it must use builds from the repository's `main` branch only, reject feature/development branches, validate the replacement before activation, and keep a known-good copy for rollback. Updates must never silently replace the application immediately before a destructive operation.

### Manual update

For a source checkout:

```powershell
git fetch origin main --prune
git pull --ff-only origin main
```

To reproduce a known version or roll back, check out a known-good commit and rebuild. Release tags, once introduced for packaged builds, should be used for manual distribution and rollback rather than as an alternate automatic-update source.

## Dependencies

The current prototype uses the Windows Forms and PowerShell/AppX capabilities supplied by supported Windows installations and has no third-party package dependency manifest. Future dependencies should use supported, actively maintained packages; deprecated or unmaintained packages should not be introduced.

## Next steps

- Add a Visual Studio solution/project and reproducible build instructions.
- Add preflight checks and per-package result details in the UI.
- Package signed builds and add an opt-in `main`-only update check.
