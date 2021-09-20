# Rust HowTo

### Installing

[Original installation instructions](https://www.rust-lang.org/tools/install)

#### MacOS Homebrew
```sh
brew install rustup-init

# It will install rustc and cargo
```

### Rust documentation
```sh
rustup doc
```

### To update
```sh
rustup update
```

### To create a new project
```
# For binary project
cargo new --bin <project_name>

# For library project
cargo new --lib <library_name>
```

### To compile
```sh
# To compile and run at the same time
cargo run

# For devlopment/debug build
cargo build

# For release build
cargo build --release
```

### Idiomatic rust check
```sh
cargo clippy
```
