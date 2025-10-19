# Changelog

All notable changes to **inlayr** will be documented in this file.

## [Unreleased]

### Added
- Initial docs polishing and packaging improvements.
- Extras for chain families (`evm`, `solana`) in `pyproject.toml`.
- Packaged `py.typed`.

### Changed
- Cleaned up project classifiers and metadata.

### Fixed
- Valid TOML in `pyproject.toml` (no duplicate tables or placeholders).
- Long description will render on PyPI via non-empty `README.md`.

## [0.1.0] - 2025-10-08

### Added
- First public release of **inlayr**.
- Minimal, typed core with optional extras for heavy chain SDKs.
- Basic test scaffolding.
