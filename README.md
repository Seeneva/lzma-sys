# lzma-sys

Rust sys crate which build [liblzma](https://tukaani.org/xz/) library and provide it to requested crate.

This crate is primiarly for inner usage by Seeneva app. For full raw binding please use [xz2](https://github.com/alexcrichton/xz2-rs) crate.

## Requirements

Your system should be able to run '[autotools](https://www.gnu.org/software/automake/faq/autotools-faq.html)' commands to build this crate.

## Paths

Requested crate should call `env::var("DEP_LZMA_ROOT")` to get root path to build result.

- **${DEP_LZMA_ROOT}/lib/liblzma.a** - path to the lzma library.
- **${DEP_LZMA_ROOT}/include** - path to lzma headers.

## License

The `lzma-sys` Rust crate is licensed under either of

- Apache License, Version 2.0, ([LICENSE-APACHE](LICENSE-APACHE) or http://www.apache.org/licenses/LICENSE-2.0)
- MIT license ([LICENSE-MIT](LICENSE-MIT) or http://opensource.org/licenses/MIT)

at your option.

Please read [XZ Utils](https://tukaani.org/xz/) documentation or [3RD-PARTY-LICENSES](docs/3RD-PARTY-LICENSES.md) to know more about `liblzma` license.
