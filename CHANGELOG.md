# Changelog

## [1.0.1] - 2026-06-26

### Changed
- Increased default `connect_timeout` from 10s to 30s for better support of slow Oracle connections
- Added `db_mcp_server.exe` to `.gitignore` to prevent tracking Windows binary

### Fixed
- Oracle database connections timing out with default 10s timeout
- Removed accidentally tracked Windows binary from repository

## [1.0.0] - 2026-06-25

### Added
- Initial public release of DB MCP Server
- Multi-database connection support (MySQL, PostgreSQL, Oracle, SQLite, MSSQL)
- Dynamic MCP tool generation per database connection
- PostgreSQL TimescaleDB extension detection and tools
- Oracle Cloud Wallet and TNS connection support
- SQLite with SQLCipher encryption support
- Connection pooling with configurable pool settings
- Lazy loading mode for 10+ database connections
- Transport modes: SSE (HTTP) and STDIO (JSON-RPC)
- GitHub Actions CI/CD with multi-platform builds
- Docker image publishing to GitHub Container Registry
- NPM package for easy MCP client integration
- `--version` CLI flag
- Unified tools mode with database parameter

### Changed
- Fully detached from upstream FreePeak/cortex — own module path, Docker images, npm package
- Renamed binary to `db_mcp_server`