# Catalog-crypto-api

README.md:
markdown
Copy
Edit
# Catalog Crypto API

The **Catalog Crypto API** is a comprehensive RESTful API designed for managing and querying cryptocurrency-related historical data. This API provides endpoints for various cryptocurrency histories such as depth, earnings, swap, and runepool units. It is built with Rust and provides efficient access to the required data through various routes and migration scripts.

---

## Project Overview

This API allows users to interact with cryptocurrency-related data, such as:
- Depth history
- Earnings history
- Swap history
- Runepool units history

The project includes models, migrations, routes, and cron jobs that automate fetching and storing the data at regular intervals.

---

## Repository Contents

- **`Cargo.toml`** - The project's dependencies and configuration file for the Rust build system.
- **`Cargo.lock`** - Contains a snapshot of the exact versions of dependencies.
- **`migrations/`** - Contains SQL migration files for creating and modifying database schemas.
- **`src/api/`** - Contains the main logic for handling API requests and defining routes (depth, earnings, swap, etc.).
- **`src/config/`** - Configuration files, including the database connection logic.
- **`src/core/`** - Core models and logic for the application.
- **`src/services/`** - Service layer that interacts with the database, cron jobs for scheduling tasks, and repositories for data fetching and storing.
- **`src/main.rs`** - The entry point of the application that starts the server.

---

## Installation

To run the Catalog Crypto API locally, follow these steps:

1. **Clone the repository:**
   ```bash
   git clone https://github.com/yourusername/Catalog-crypto-api.git
   cd Catalog-crypto-api
Install Rust:

If you haven’t already installed Rust, you can do so by following the installation instructions on the Rust official website.

bash
Copy
Edit
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
Build and run the project:

After ensuring all dependencies are in place, build the project:

bash
Copy
Edit
cargo build
Then run the server:

bash
Copy
Edit
cargo run
The API will be available at http://localhost:8000.

Running Migrations:

Run the database migrations to set up the schema:

bash
Copy
Edit
cargo run --release
This will apply any new database changes and create the necessary tables.

API Endpoints
The following endpoints are available:

Depth History: /api/depth

Earnings History: /api/earnings

Swap History: /api/swap

Runepool Units History: /api/runepool

These routes are handled in the src/api/routes folder, and each corresponds to a specific database model for handling the respective data.

Cron Jobs
This project includes cron jobs that periodically fetch and update cryptocurrency data. The jobs are located in the src/services/jobs/cron/ directory. You can run the cron jobs by executing the cargo run command.

Contributing
Contributions are welcome! Feel free to open an issue or submit a pull request for bug fixes, enhancements, or ideas.

License
Specify your license here (e.g., MIT License).

Contact
For any questions or feedback, please contact:
Tiru Ram Narla
Email: tiruramchowdary@gmail.com
