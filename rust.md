# Rust tools how-to in MacOS

### Installing

[Original installation instructions](https://www.rust-lang.org/tools/install)

#### MacOS Homebrew
```shell
brew install rustup-init

# It will install rustc and cargo
```

### Rust documentation
```shell
rustup doc
```

### To update
```shell
rustup update
```

### To create a new project
```shell
# For binary project
cargo new --bin <project_name>

# For library project
cargo new --lib <library_name>
```

### To compile
```shell
# To compile and run at the same time
cargo run

# For devlopment/debug build
cargo build

# For release build
cargo build --release
```

### Idiomatic rust check
```shell
cargo clippy
```
