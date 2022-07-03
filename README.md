## Install Rust
Here is the link: https://www.rust-lang.org/learn/get-started
## Set up on my local: 

- Depedency on Cargo.toml looks like this:
```bash
cat Cargo.toml

[package]
name = "hello-rust"
version = "0.1.0"
edition = "2021"

# See more keys and their definitions at https://doc.rust-lang.org/cargo/reference/manifest.html

[dependencies]
ferris-says = "0.2"
```

- Main rust is fairly simple. Trying it out.
```bash
cat hello-rust/src/main.rs
use ferris_says::say; // Added as part of the cargo.toml as dependency
use std::io::{stdout, BufWriter};

fn main() {
    let stdout = stdout();
    let message = String::from("Hello fellow Rustaceans! I am a Madhu :)");
    let width = message.chars().count();

    let mut writer = BufWriter::new(stdout.lock());
    say(message.as_bytes(), width, &mut writer).unwrap();
}
```

```bash
.
└── hello-rust
    ├── Cargo.lock
    ├── Cargo.toml
    ├── src
    │   └── main.rs
    └── target
        ├── CACHEDIR.TAG
        └── debug
            ├── build
            ├── deps
```
