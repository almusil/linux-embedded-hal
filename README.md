# `linux-embedded-hal`

> Implementation of the [`embedded-hal`] traits for Linux devices

This project is developed and maintained by the [Embedded Linux team][team].

[`embedded-hal`]: https://crates.io/crates/embedded-hal

## [Documentation](https://docs.rs/linux-embedded-hal)

## GPIO character device

Since Linux kernel v4.4 the use of sysfs GPIO was deprecated and replaced by the character device GPIO.
See [gpio-cdev documentation](https://github.com/rust-embedded/gpio-cdev#sysfs-gpio-vs-gpio-character-device) for details.

This crate includes feature flag `gpio_cdev` that replaces [sysfs_gpio](https://crates.io/crates/sysfs_gpio) by [gpio-cdev](https://crates.io/crates/gpio-cdev).
To enable it update your Cargo.toml. 
```
linux-embedded-hal = { version = "0.3", features = ["gpio_cdev"] }
``` 

## License

Licensed under either of

- Apache License, Version 2.0 ([LICENSE-APACHE](LICENSE-APACHE) or
  http://www.apache.org/licenses/LICENSE-2.0)
- MIT license ([LICENSE-MIT](LICENSE-MIT) or http://opensource.org/licenses/MIT)

at your option.

### Contribution

Unless you explicitly state otherwise, any contribution intentionally submitted
for inclusion in the work by you, as defined in the Apache-2.0 license, shall be
dual licensed as above, without any additional terms or conditions.

## Code of Conduct

Contribution to this crate is organized under the terms of the [Rust Code of
Conduct][CoC], the maintainer of this crate, the [HAL team][team], promises
to intervene to uphold that code of conduct.

[CoC]: CODE_OF_CONDUCT.md
[team]: https://github.com/rust-embedded/wg/#the-embedded-linux-team
