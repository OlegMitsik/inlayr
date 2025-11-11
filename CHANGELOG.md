# Changelog

All notable changes to **inlayr** will be documented in this file.

## [Unreleased]

### Added
- Comprehensive input validation utilities (`ValidationError`, `validate_token_address`, `validate_amount`, `validate_slippage`, `validate_chain_id`)
- HTTP utilities with automatic retry logic and configurable timeouts
- Request timeout support (30s default) for all aggregator and RPC HTTP calls
- Automatic retry logic with exponential backoff for transient failures (429, 5xx errors)
- HTTP error handling with `raise_for_status()` for better error reporting
- Extensive test coverage for validation, timeouts, and error handling (60+ new tests)
- Initial docs polishing and packaging improvements
- Extras for chain families (`evm`, `solana`) in `pyproject.toml`
- Packaged `py.typed`

### Changed
- RPC connectors (ankr, 1rpc) now validate `chain_id` on initialization with helpful error messages
- Raydium aggregator now handles missing `priority_fee` parameter with 'medium' default
- All aggregators now use session with retry logic instead of basic `requests.Session`
- Cleaned up project classifiers and metadata

### Fixed
- KeyError when using unsupported `chain_id` in onerpc RPC (now raises `ValidationError`)
- KeyError when using unsupported `chain_id` in ankr RPC (now raises `ValidationError`)
- KeyError when `priority_fee` not provided to Raydium aggregator
- Missing timeouts on HTTP requests (could hang indefinitely)
- Missing error handling for failed HTTP requests
- Valid TOML in `pyproject.toml` (no duplicate tables or placeholders)
- Long description will render on PyPI via non-empty `README.md`

## [0.1.0] - 2025-10-08
## [0.1.1] - 2025-10-19
## [0.1.2] - 2025-10-20
## [0.1.21] - 2025-10-21

### Added
- First public release of **inlayr**.
- Minimal, typed core with optional extras for heavy chain SDKs.
- Basic test scaffolding.
