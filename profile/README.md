<p align="center">
  <img src="https://raw.githubusercontent.com/Loment-Lang/loment/main/editors/loment-banner.png" width="720" alt="Loment — Programming Language">
</p>

### A systems programming language

A program becomes a native x86-64 executable — Linux ELF, Windows PE, or a bare object for metal —
with **no runtime and no libc**. The toolchain is itself written in Loment, and running it needs no
Python, no clang and no WSL.

```rust
module hello

fn _start() {
    let s: str = "hello from Loment\n";
    syscall4(1, 1, str_ptr(s) as u64, str_len(s) as u64);
    syscall4(60, 0, 0, 0);
}
```

```console
$ loment run hello.lomt
hello from Loment
```

- **Small.** No runtime, no libc, no interpreter.
- **Accountable.** A capability domain says how far a unit may reach, and a form object records what
  it holds and reaches — so what a program can touch is answerable without reading all of it.
- **Familiar.** Rust-flavored syntax, and the same program can be written in six more: C, C++, Java,
  C#, Go or Python.

### What lives here

| Repository | What it is |
|---|---|
| **[loment](https://github.com/Loment-Lang/loment)** | The compiler, the standard library and the toolchain. **Start here.** |
| **[lompi](https://github.com/Loment-Lang/lompi)** | The package manager. A library is a directory, and its identity is a content hash. |
| **[loment-site](https://github.com/Loment-Lang/loment-site)** | The website: front page, install instructions, short runnable examples. |

<p>
  <a href="https://loment-lang.github.io/loment-site/"><b>Website</b></a> ·
  <a href="https://github.com/Loment-Lang/loment/releases/latest"><b>Download</b></a> ·
  <a href="https://github.com/Loment-Lang/loment/blob/main/QUICKSTART.md"><b>Quick start</b></a> ·
  <a href="https://github.com/Loment-Lang/loment/blob/main/standard/LLS.md"><b>Standard (LLS)</b></a> ·
  <a href="https://loment.fandom.com/"><b>Wiki</b></a>
</p>

Ask in an [issue](https://github.com/Loment-Lang/loment/issues), on
[Discord](https://discord.gg/rGw7NRNU) or on [Mastodon](https://mastodon.social/@Loment).
Questions are as welcome as bug reports.
