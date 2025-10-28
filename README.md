
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





🌿 Fork & Experiment


Interested in exploring deterministic Rust builds or testing LTSS behavior on your own platform?

You’re welcome to fork this repository and start experimenting freely.


👉 Fork on GitHub




The fork-lab branch is refreshed weekly to provide a clean sandbox for experiments.

You can submit your improvements through Pull Requests or share results in a “💡 Fork Task” issue.




Why fork?




🔬 Test deterministic builds across OSes


🧩 Contribute to CI or checksum verification scripts


📘 Add documentation or reproducibility studies


🧠 Experiment with R3C compiler integration




Start here:




Check CONTRIBUTING.md for simple fork instructions


Open an issue with the “💡 Fork Task” template to document your experiment

## 💰 Sponsor the R3C Foundation

The **R3C Foundation** is an open research and development collective dedicated to sustaining long-term compiler ecosystems — independent, transparent, and LLVM-free.

Your support directly funds:
- 🧩 Development of R3C, cpppm, and LTSS toolchains  
- ⚙️ Continuous Integration and testing infrastructure  
- 📚 Documentation, education, and community initiatives  
- 🌍 Research toward a sustainable, compiler-sovereign ecosystem  

Every contribution is **publicly visible and transparently managed** via [OpenCollective](https://opencollective.com/r3c-foundation).  
You can view all donations and expenses in real-time.

👉 **Sponsor now:**  
🔗 [https://opencollective.com/r3c-foundation](https://opencollective.com/r3c-foundation)

---

> 💡 *R3C Foundation operates as an open and auditable collective — ensuring that every contribution fuels the next generation of compiler innovation.*
