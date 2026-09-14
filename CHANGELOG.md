# Changelog

All notable changes to this project will be documented in this file.

The project follows Semantic Versioning: `MAJOR.MINOR.PATCH`.

## [Unreleased]

### Added
- Show the names of AppX applications whose removal failed or whose package was not installed.

### Fixed
- Prevent repeated AppX removal submissions while a removal operation is in progress.

## [0.1.2] - 2026-08-24

### Security
- Remove the unnecessary `-ExecutionPolicy Bypass` flag from the PowerShell process used for AppX removal. The tool executes an inline command and does not need to weaken the host execution-policy setting.

## [0.1.1] - 2026-08-20

### Fixed
- Wait for each PowerShell removal command before reporting completion.
- Report successful and failed removal operations instead of always showing success.
- Avoid opening a visible PowerShell window for every selected application.

## [0.1.0] - 2023-03-15

### Added
- Initial Windows Forms prototype for selecting and removing selected AppX applications.
