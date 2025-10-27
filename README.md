# 🦀 R3C Rust-LTSS — Long-Term Sustain Support

> **Freeze once. Sustain forever.**  
> Deterministic Rust toolchain for compiler research, embedded systems, and long-term infrastructure.


[![Release](https://img.shields.io/github/v/release/r3c-foundation/rust-ltss?label=release)](https://github.com/r3c-foundation/rust-ltss/releases)
[![Rust](https://img.shields.io/badge/Rust-1.70.0-orange)](#)
[![License](https://img.shields.io/github/license/r3c-foundation/rust-ltss)](./LICENSE)
[![OS](https://img.shields.io/badge/OS-Linux%20%7C%20macOS%20%7C%20Windows-blue)](#)
[![Downloads](https://img.shields.io/github/downloads/r3c-foundation/rust-ltss/total?color=brightgreen)](https://github.com/r3c-foundation/rust-ltss/releases)

---

## 📖 Overview

**R3C Rust-LTSS** is a **frozen Rust 1.70.0 environment** maintained for long-term stability,  
LLVM-free compatibility, and reproducible builds across all major platforms.  

This project ensures that the R3C compiler ecosystem remains **independent of upstream Rust and LLVM volatility**,  
serving as the base layer for sustainable compiler research and embedded deployment.

---

## ⚙️ Toolchain Specification

| Component | Version | Purpose |
|------------|----------|----------|
| Rust Compiler | **1.70.0** | Long-term stable baseline |
| Cargo | 1.70 toolchain default | Deterministic build manager |
| LLVM | Frozen / optional | Avoids automatic updates |
| Supported OS | Linux / macOS / Windows | Verified parity builds |

---

## 🧩 Installation

**1. Clone Repository**
```bash
git clone https://github.com/r3c-foundation/rust-ltss.git
cd rust-ltss

2. Auto-select Rust 1.70 Rust version is locked via rust-toolchain.toml:

[toolchain]
channel = "1.70.0"
components = ["rust-src", "rustfmt", "clippy"]
profile = "minimal"

3. Verify

rustc --version
# rustc 1.70.0 (90c541806 2023-05-31)

4. Build

cargo build --release

All artifacts will be in target/ltss/.


---

🧠 Philosophy

> R3C LTSS = Rust Independence + Deterministic Sustainability



R3C Rust-LTSS exists to guarantee that compiler research and embedded workflows
can operate without breaking changes, LLVM regressions, or toolchain drift.

🔒 No forced Rustup updates

🧾 Verified SHA256 checksums

⚙️ Identical results across OSes

🧩 Integrated with R3C and cpppm



---

🧭 Design Goals

Goal	Description

🧱 Determinism	Reproduce identical builds across years
🌍 Cross-Platform	Unified Linux/macOS/Windows parity
🦀 Rust Independence	Function without LLVM dependency
🧩 Integration	Used by R3C Core / cpppm / LTSS ecosystem
🧭 Long-Term	10-year sustainable compiler environment



---

🗓️ Lifecycle Policy

Support Level	Period	Description

Full Support	2025–2030	Security + compatibility updates
Extended Support	2030–2035	Critical patch rebuilds
Archive	2035+	Frozen reference image



---

🧾 Release Convention

Type	Tag Example	Description

Stable LTSS	r3c-rust1.70-ltss-v2025.01	Verified multi-OS release
Nightly	r3c-rust1.70-nightly	Experimental



---

🧭 Ecosystem Integration

Rust-LTSS powers the R3C LLVM-Zero Ecosystem:

🧱 R3C — C++ → Rust → ASM compiler core

📦 cpppm — Zero-dependency C++ package manager

🦀 Rust-LTSS — Stable long-term Rust layer

⚙️ Beyond-LLVM / Post-R3C — Research extensions



---



👤 User Guide — Rust-LTSS Usage and Policy


R3C Rust-LTSS provides a frozen, long-term Rust toolchain for developers and researchers who require deterministic, stable, and reproducible environments.

This guide explains how to install, verify, and operate within the LTSS framework.



🧩 1. Setup






Clone the repository


git clone https://github.com/r3c-foundation/rust-ltss.git
cd rust-ltss







Automatic toolchain selection

The Rust toolchain is locked via rust-toolchain.toml.

No manual rustup setup is required.


[toolchain]
channel = "1.70.0"
components = ["rust-src", "rustfmt", "clippy"]
profile = "minimal"







Verify the environment


rustc --version
# rustc 1.70.0 (90c541806 2023-05-31)







Build


cargo build --release



Build results will be stored in target/ltss/.







🧠 2. Guidelines for Users




Guideline
Description




🔒 Immutable Toolchain
Never upgrade Rust beyond 1.70.0 within this repository.


🧾 Integrity First
Always verify builds using the provided SHA256SUMS.txt file.


⚙️ Cross-Platform Consistency
Builds must behave identically on Linux, macOS, and Windows.


🧱 No External Dependencies
Avoid crates or toolchains that force new Rust versions.


🧩 Ecosystem Alignment
Use Rust-LTSS only within R3C, cpppm, and Beyond-LLVM layers.





🧾 3. Release Workflow


Rust-LTSS uses automated CI releases through GitHub Actions.




Type
Tag Example
Description




Stable
r3c-rust1.70-ltss-v2025.01
Annual verified release


Nightly
r3c-rust1.70-nightly
Experimental branch for testing




Each release includes:




Precompiled binaries for Linux/macOS/Windows


SHA256 integrity file


Generated tag + timestamp





🧭 4. Long-Term Policy




Support Level
Duration
Scope




Full Support
2025–2030
Regular rebuilds, minor fixes


Extended Support
2030–2035
Security updates, re-validation


Archive
2035+
Frozen, read-only reference





⚖️ 5. License and Contribution




Licensed under MIT.


Contributions are allowed only if they do not alter the Rust toolchain version.


Pull requests must include updated checksum verification (SHA256SUMS.txt).





🧭 Summary




R3C Rust-LTSS is a long-term, reproducible Rust base that enables stable compiler research and sustainable embedded builds.


“Freeze once. Sustain forever.”


---

## 📚 Developer Resources

- [Developer Guide](./DEVELOPER_GUIDE.md)
- [User Guide](./USER_GUIDE.md)
- [LTSS Policy](./LTSS_POLICY.md)

> For long-term contributors and maintainers:  
> Follow the LTSS principles before merging or releasing stable versions.

## 🧭 Extended Documentation

- [Vision](./VISION.md)
- [Roadmap](./ROADMAP.md)
- [Ecosystem Valuation Report](./ECOSYSTEM_VALUE.md)
