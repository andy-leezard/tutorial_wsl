# Rust project for a webserver

This process is tested on Debian Linux

# Requirements

- Docker

# Dependencies

- Surreal DB
- Websocket (tungstenite)
- jsonwebtoken (Auth)

# STEPS

1. Install Rust via RustUp.

```
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
```

2. Install Cargo Watch

```
cargo install cargo-watch
```

- Cargo Watch watches over your project's source for changes, and runs Cargo commands when they occur.

3. Create a new project

```
cargo new your_project_name
```

4. Install Dependencies

Add the necessary dependencies for SurrealDB, WebSockets and authentication to your ```Cargo.toml``` file.

- will be installed in a folder named "target"

```
cargo check
```

This command will perform a quick check of the project's dependencies to see if there are any updates available.
If any updates are found, you will receive a message indicating the name and version of the outdated dependency.

If you want to update all of the outdated dependencies in your project, you can run the following command:

```
cargo update
```

This command will update all of the dependencies to the latest available version.
Be aware that updating dependencies can sometimes result in breaking changes,
so it's important to thoroughly test your project after updating dependencies.
