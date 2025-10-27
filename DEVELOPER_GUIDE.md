# 🦀 Rust-LTSS Developer Guide

This document provides practical guidance for developers and contributors of the **Rust-LTSS** project — a Long-Term Sustain Support initiative for industrial Rust ecosystems.

---

## 🧭 Overview

Rust-LTSS focuses on creating a **stable, LLVM-independent** Rust ecosystem suitable for industrial and embedded environments.  
The development philosophy emphasizes **consistency, maintainability, and long-term reliability**.

---

## 🧱 Repository Structure




rust-ltss/
├── src/                  # Core sources
├── docs/                 # Documentation
├── examples/             # Example implementations
├── tests/                # Unit & integration tests
├── .github/workflows/    # CI/CD pipelines
└── Cargo.toml            # Rust manifest



---

## 🧰 Build & Test

### Prerequisites
- Rust ≥ 1.78 (or MRustC compatible toolchain)
- Git, Cargo, and Make (for Unix-based systems)
- Optional: NASM, GCC, or Clang for low-level builds

### Build
```bash
cargo build --release



Test


cargo test



For continuous testing on multiple OSes, check .github/workflows/ci.yml.



⚙️ Git & Branching Rules




Branch
Purpose
Auto Release




main
Stable and verified builds
✅ Auto-tagged as *-stable


dev
Development and staging area
❌ Manual


docs
Documentation-only updates
✅ Triggered via workflow dispatch




All commits to main must pass CI checks.

No direct pushes — use pull requests (PRs) with descriptive titles.



🔄 CI/CD Overview


Rust-LTSS uses GitHub Actions to automate:




Build & test on Ubuntu, macOS, and Windows


Automatic tagging and releasing (vYY.MM.DD-stable)


SHA256 checksum verification


Documentation auto-publishing




To trigger a manual release:


gh workflow run release.yml




🧩 Contribution Workflow




Fork the repository.


Create a new branch for your feature or fix:

git checkout -b feature/new-mechanism





Commit clearly with a message format:

[Module] Short change summary





Submit a Pull Request with a concise explanation and test evidence.





🪶 Coding Style




Follow Rust 2021 Edition conventions.


Use Clippy and rustfmt before pushing:

cargo fmt
cargo clippy --all-targets --all-features -- -D warnings





Avoid unsafe code unless necessary for performance or embedded access.





🔐 Security & LTSS Policy


All changes affecting long-term stability must align with the LTSS_POLICY.md.

Critical patches require dual approval (maintainer + reviewer).

Security reports should be submitted via private email (see SECURITY.md).



📦 Release Checklist


Before tagging a stable release:




[ ] All workflows passed ✅


[ ] README and docs updated


[ ] SHA256 verified


[ ] Version tag consistent with date pattern


[ ] Release assets tested across OSes





💬 Contact & Community




Discussions: GitHub Discussions


Issues: GitHub Issues


Maintainer: r3c-foundation core team






“Stability first, speed later — Rust-LTSS exists to make Rust last.”





Last updated: {{current_date}}



---

