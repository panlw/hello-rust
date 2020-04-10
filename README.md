# Hello Rust

## Install

Profile rustup mirror server of China:

```sh
export RUSTUP_DIST_SERVER=https://mirrors.tuna.tsinghua.edu.cn/rustup
source "${HOME}/.cargo/env"
```

Install rustup and toolchain:

```sh
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh

rustup component add rust-analysis --toolchain stable-x86_64-unknown-linux-gnu
rustup component add rust-src --toolchain stable-x86_64-unknown-linux-gnu 
rustup component add rls --toolchain stable-x86_64-unknown-linux-gnu
```

Install VSCode plugin:

```sh
ext install rust-lang.rust
```

## Build

Press `ctrl+shift+b`, and select `Rust: cargo build`

The following error will be thrown if C build environment not ready:

```log
error: linker `cc` not found
```

Then you should install package `build-essential`

```sh
sudo apt install build-essential
```

And then build again.

## Run

Press ``ctrl+``` to open terminal, execute the following command:

```
cargo run
```
