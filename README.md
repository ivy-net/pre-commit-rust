# Rust hooks for pre-commit

[Rust](https://www.rust-lang.org) tools package for [pre-commit](https://pre-commit.com).

This a fork of the [fork](https://github.com/tylerjw/pre-commit-rust) of the [original repo](https://github.com/doublify/pre-commit-rust/forks).

Additions are:
* Cargo Machete - https://github.com/lklimek/cargo-machete/blob/main/README.md
* Cargo LLVM Cov - https://github.com/taiki-e/cargo-llvm-cov
* Cargo Test - run tests

## Using rust tools with pre-commit

```yaml
-   repo: https://github.com/ivy-net/pre-commit-rust
    rev: master
    hooks:
    -   id: fmt
    -   id: cargo-check
```

## Passing arguments to rustfmt

```yaml
-   repo: https://github.com/ivy-net/pre-commit-rust
    rev: master
    hooks:
    -   id: fmt
        args: ['--verbose', '--edition', '2018', '--']
```
