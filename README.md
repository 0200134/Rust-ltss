
**🦀 R3C Rust-LTSS — Long-Term Sustain Support**

Freeze once. Sustain forever.

Deterministic Rust toolchain for compiler research, embedded systems, and long-term infrastructure.
Part of the R3C-Foundation ecosystem.


---

🧭 Vision & Core Mission

> “Independent Rust that never breaks.”



R3C Rust-LTSS provides a frozen, reproducible Rust 1.70.0 toolchain,
ensuring stable compiler research and embedded builds for decades.

Goal	Description

🧱 Determinism	Identical builds across all OSes
🌍 Cross-Platform	Linux / macOS / Windows parity
🦀 Rust Independence	Works without LLVM or rustup updates
🧩 Integration	Core layer for R3C / cpppm / Beyond-LLVM
🔒 Sustainability	10-year guaranteed reproducibility



---

⚙️ Toolchain Overview

Component	Version	Purpose

Rust Compiler	1.70.0	Frozen baseline
Cargo	1.70	Deterministic build manager
LLVM	Optional / Frozen	Avoids automatic updates
Supported OS	Linux · macOS · Windows	Verified parity builds



---

📦 Installation

git clone https://github.com/r3c-foundation/rust-ltss.git
cd rust-ltss
cargo build --release

Rust toolchain is auto-locked via rust-toolchain.toml.
All artifacts appear in target/ltss/.


---

🔧 Fork & Experiment

> Want to test your own LTSS build, patch CI, or run cross-platform verification?



👉 Fork this repository
and start from the fork-lab branch.





🔁 fork-lab resets weekly — always clean for experiments

🧩 Contribute via CONTRIBUTING.md

💬 Submit a “💡 Fork Task” issue to document your experiment



---

🧱 Ecosystem Integration

Layer	Repository	Role

🧠 Core Compiler	r3c	C++ → Rust → ASM pipeline
📦 Package Manager	cpppm	Zero-dependency C++ package layer
🦀 Rust-LTSS	(this repo)	Long-term Rust base
⚙️ Nightly LTSS	r3c-nightly-ltss	Experimental ASM builds
🔬 Beyond-LLVM	beyond-llvm	Research & post-LLVM extensions



---

🧩 Lifecycle Policy

Support Level	Period	Description

Full	2025–2030	Security + compatibility updates
Extended	2030–2035	Critical rebuilds only
Archive	2035 +	Frozen reference image



---





---

📜 License

MIT License © R3C-Foundation
“Freeze once. Sustain forever.”


---
