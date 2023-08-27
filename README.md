## Reference

- [A guide to cross-compilation in Rust](https://blog.logrocket.com/guide-cross-compilation-rust/)

## RUST platform specific

`<arch><sub>-<vendor>-<sys>-<env>`

```
> cargo build
> Hello, world from x86_64-unknown-linux-gnu! I was compiled on x86_64-unknown-linux-gnu.
```

## クロスコンパイルの手順

```shell
$ cargo install cross

$ CROSS_CONTAINER_ENGINE=podman cross run --target x86_64-pc-windows-gnu
   Compiling rust-win-compile v0.1.0 (/project)
    Finished dev [unoptimized + debuginfo] target(s) in 0.14s
     Running `wine /target/x86_64-pc-windows-gnu/debug/rust-win-compile.exe`
Hello, world from x86_64-pc-windows-gnu! I was compiled on x86_64-unknown-linux-gnu.
This will only get printed on Windows.
```
