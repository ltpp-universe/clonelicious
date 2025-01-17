# clonelicious

[![](https://img.shields.io/crates/v/clonelicious.svg)](https://crates.io/crates/clonelicious)
[![](https://docs.rs/clonelicious/badge.svg)](https://docs.rs/clonelicious)
[![](https://img.shields.io/crates/l/clonelicious.svg)](./LICENSE)
[![](https://github.com/ltpp-universe/clonelicious/workflows/Rust/badge.svg)](https://github.com/ltpp-universe/clonelicious/actions?query=workflow:Rust)

[Official Documentation](https://docs.ltpp.vip/clonelicious/)

A Rust macro library that simplifies cloning and closure execution. The `clone!` macro automatically clones variables and immediately executes the closure with the cloned values, streamlining common patterns in Rust programming.

## Installation

To install `clonelicious` run cmd:

```sh
cargo add clonelicious
```

## Usage

```rust
use clonelicious::*;
let s1: String = String::from("Hello");
let s2: String = String::from("World");
clone!(s1, s2; move |x: String, y: String| {
    assert_eq!(x, String::from("Hello"));
    assert_eq!(y, String::from("World"));
});
```

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Contributing

Contributions are welcome! Please open an issue or submit a pull request.

## Contact

For any inquiries, please reach out to the author at [ltpp-universe <root@ltpp.vip>](mailto:root@ltpp.vip).
