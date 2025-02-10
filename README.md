# RRWA - Rust Real World Application

## Prerequisites

- Docker
- Rust / Cargo
- sqlx CLI: `cargo install sqlx-cli --no-default-features --features rustls,postgres`

## Getting Started

For the very first run you need to initialize your dev environment:

```bash
# Copy the env file and set your information
cp .env.example .env

# Init the database
sqlx database create

# Run the migrations
sqlx migrate run
```

