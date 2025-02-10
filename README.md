# RRWA - Rust Real World Application

This repository demonstrates how to develop a real world application in Rust. Here's the stack:

- CSR / SSR: [Leptos](https://leptos.dev/)
- Relational + non-relational: [PostgreSQL](https://www.postgresql.org/)
- Database library and migration system: [SQLx](https://github.com/launchbadge/sqlx)
- Server: [Axum](https://github.com/tokio-rs/axum)
- Functional / E2E tests: [cucumber-rs](https://github.com/cucumber-rs/cucumber) and [thirtyfour](https://github.com/Vrtgs/thirtyfour)
- API tests: [Grillon](https://github.com/theredfish/grillon)
- Payment system: [Stripe](https://stripe.com/en-fr)
- Desktop app: [Tauri](https://v2.tauri.app/)
- Online host: TBD...

I'm building this real-world application to showcase the capabilities of Rust in a practical setting. The project will evolve to the point of selling real products, allowing you to support my work and [Indiedevcasts](https://indiedevcasts.com).

This application will also serve as a core asset in my courses on testing in Rust: because what’s better than a real-world project to learn from?

I've open-sourced the project to make distribution easier and to give others the opportunity to learn from the codebase.

**Note:** The project is still in its early stages. I’ll provide concrete links once key parts of the website are developed.

## Prerequisites

- Docker
- Rust / Cargo

```bash
# Sqlx CLI for postgres
cargo install sqlx-cli --no-default-features --features rustls,postgres

# Trunk for Leptos
cargo install trunk

# Leptos formatter used with
cargo install leptosfmt

# Add WASM target for CSR
rustup target add wasm32-unknown-unknown
```

## Getting Started

For the very first run you need to initialize your dev environment:

```bash
# Copy the env file and set your information
cp .env.example .env

# Run postgres container
docker-compose up -d

# Init the database
sqlx database create

# Run the migrations
sqlx migrate run

# Run (you can skip --open if you run into issues)
trunk serve --port 3000 --open
```

