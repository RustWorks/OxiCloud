# 🚀 OxiCloud [![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

<p align="center">
  <img src="static/oxicloud-logo.svg" alt="OxiCloud" width="300" />
</p>

## A lightweight, Rust-powered alternative to NextCloud

I built OxiCloud because I wanted a simpler, faster file storage solution than existing options. After struggling with NextCloud's performance on my home server, I decided to create something that prioritizes speed and simplicity while still being robust enough for daily use.

![OxiCloud Dashboard](doc/images/Captura%20de%20pantalla%202025-03-23%20230739.png)

*OxiCloud's straightforward interface for file and folder management*

## ✨ What makes OxiCloud different?

- **Lightweight**: Minimal resource requirements compared to PHP-based alternatives
- **Responsive UI**: Clean, fast interface that works well on both desktop and mobile
- **Rust Performance**: Built with Rust for memory safety and speed
- **Simple Setup**: Get running with minimal configuration
- **Multilingual**: Full support for English and Spanish interfaces

## 🛠️ Getting Started

### Prerequisites
- Rust 1.70+ and Cargo
- PostgreSQL 13+ database
- 512MB RAM minimum (1GB+ recommended)

### Installation

```bash
# Clone the repository
git clone https://github.com/DioCrafts/oxicloud.git
cd oxicloud

# Configure your database (create .env file with your PostgreSQL connection)
echo "DATABASE_URL=postgres://username:password@localhost/oxicloud" > .env

# Build the project
cargo build --release

# Run database migrations
cargo run --bin migrate

# Run the server
cargo run --release
```

The server will be available at `http://localhost:8085`

## 🧩 Technical Implementation

OxiCloud follows Clean Architecture principles with clear separation of concerns:

- **Domain Layer**: Core business logic and entities
- **Application Layer**: Use cases and application services
- **Infrastructure Layer**: External systems and implementations
- **Interfaces Layer**: API and web controllers

The architecture makes it easy to extend functionality or swap components without affecting the core system.

## 🚧 Development

```bash
# Core development workflow
cargo build                 # Build the project
cargo run                   # Run the project locally
cargo check                 # Quick check for compilation errors

# Testing
cargo test                  # Run all tests
cargo test <test_name>      # Run a specific test

# Code quality
cargo clippy                # Run linter
cargo fmt                   # Format code

# Debugging
RUST_LOG=debug cargo run    # Run with detailed logging
```

## 🗺️ Roadmap

I'm actively working on improving OxiCloud with features that I need personally:

- User authentication and multi-user support (in progress)
- File sharing with simple links
- WebDAV support for desktop integration
- Basic file versioning
- Simple mobile-friendly web interface enhancements
- Trash bin functionality (in progress)

See [TODO-LIST.md](TODO-LIST.md) for my current development priorities.

## 🤝 Contributing

Contributions are welcome! The project is still in early stages, so there's lots of room for improvement.

Please see [CONTRIBUTING.md](CONTRIBUTING.md) for detailed information on how to contribute to OxiCloud. All contributors are expected to follow our [Code of Conduct](CODE_OF_CONDUCT.md).

## 📜 License

OxiCloud is available under the [MIT License](LICENSE). See the [LICENSE](LICENSE) file for more information.

---

Built by a developer who just wanted better file storage. Feedback and contributions welcome!
