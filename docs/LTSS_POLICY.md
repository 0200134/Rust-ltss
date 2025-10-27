# 🦀 R3C Rust-LTSS — Policy

> **Freeze once. Sustain forever.**  
> This document defines the long-term sustain support (LTSS) policy for the Rust layer used across the R3C ecosystem.

- **Policy ID:** R3C-LTSS-2025.01
- **Scope:** `r3c`, `rust-ltss`, `cpppm`, and dependent repos in the R3C Foundation org
- **Baseline Toolchain:** **Rust 1.70.0** (rustc/cargo/std/rust-src)

---

## 1) Version Freeze

- **Frozen channel:** `1.70.0` — no upgrades, no rustup auto-updates.
- **Mandatory file:** `rust-toolchain.toml`
  ```toml
  [toolchain]
  channel = "1.70.0"
  components = ["rust-src","rustfmt","clippy"]
  profile = "minimal"





Any PR that changes the toolchain version is rejected unless the TSC (Technical Steering Committee) approves a new LTSS line (rare).





2) Release Cadence & Tags




Annual stable (once per year, January target).


Optional Quarterly validation (build/verify only, no feature).


Tag format:



Stable: r3c-rust1.70-ltss-vYYYY.MM (e.g., r3c-rust1.70-ltss-v2025.01)


Nightly/Test: r3c-rust1.70-nightly-YYYYMMDD






Each release must include:



Prebuilt artifacts per OS


SHA256SUMS.txt


LTSS-MANIFEST.toml (see §3)









3) Manifest & Reproducibility




LTSS-MANIFEST.toml (top-level in each release):

[ltss]
rust = "1.70.0"
r3c_version = "<git-tag-or-commit>"
date = "YYYY-MM-DD"
platforms = ["linux-x64","macos-x64","windows-x64"]

[hashes]
linux = "sha256:<...>"
macos = "sha256:<...>"
windows = "sha256:<...>"
manifest = "sha256:<self>"





Builds must be deterministic: same inputs → same outputs across Linux/macOS/Windows.


CI MUST generate and publish SHA256SUMS.txt. Local verification:

sha256sum -c SHA256SUMS.txt








4) Support Tiers




Tier
Window
What we do
Notes




Full
2025–2030
Build validation, critical bug fixes, doc updates
Default for main


Extended
2030–2035
Security backports, rebuilds for toolchain drift
No new features


Archive
2035+
Frozen artifacts, read-only references
No fixes unless legal/security critical





5) Change Control (What’s allowed)




✅ Build scripts, CI, docs, examples


✅ Backports that do not require Rust > 1.70


✅ Security patches compatible with 1.70 std/crates


❌ Toolchain upgrades, language features post-1.70


❌ Breaking public APIs without deprecation (see §8)




All changes require:




Green CI on all OS targets


Updated LTSS-MANIFEST.toml when artifacts change





6) Security & Supply Chain




Integrity: SHA256 for all artifacts; optional .asc signatures


Third-party crates:



Pin exact versions in Cargo.lock


Prefer audited crates; avoid recent unstable features


No build.rs network access






Report vulnerabilities via private security issue (Security tab).

Disclosure target: 90 days after fix availability.





7) CI Requirements (Hard Rules)




Matrix: ubuntu-latest, macos-latest, windows-latest


Steps: checkout → toolchain 1.70 → build → tests → hashes → release


CI must fail if:



toolchain ≠ 1.70.0


missing SHA256SUMS.txt


tests not executed on any OS






Artifacts stored under dist/ and attached to the release.





8) Deprecation & Backport Policy




Deprecate features with two stable LTSS cycles notice (≈2 years).


Backports only if:



Security impact is high, or


Breakage prevents deterministic builds






Backport PR must include:



Rationale


Risk assessment


Repro steps before/after









9) Governance & Roles




TSC (Technical Steering Committee): approves new LTSS lines, deprecations, security embargo decisions.


Maintainers: enforce tooling freeze and CI policy.


Contributors: must sign DCO/CLA (if enabled) and follow this policy.




Decision rule: simple majority of TSC; tie → freeze (no change).



10) Issue / PR Checklist




[ ] Uses Rust 1.70.0 (verified by CI)


[ ] No new language features beyond 1.70


[ ] Cross-OS tests added or not applicable


[ ] Repro instructions included


[ ] Docs updated (docs/, README, manifests)


[ ] SHA256SUMS.txt regenerated (for releases)





11) Compatibility Contract




Targeted CPU/OS: x86_64 Linux/macOS/Windows

(ARM builds are best-effort; not covered by LTSS guarantees yet.)


C ABI boundaries and generated ASM are stable per release; changes require deprecation window (§8).





12) Data Retention




Keep last 5 stable LTSS releases online.


Nightly artifacts may be pruned automatically after 90 days.





13) Opening a New LTSS Line (Rare)


A brand-new LTSS baseline (e.g., Rust 1.74) requires:




Written proposal (motivation, risks, migration cost)


2-OS reproducibility demo + hash verification


TSC approval (≥⅔)


Parallel support plan; no forced migration





14) Contacts




Security: use GitHub Security tab (private report)


General: open an Issue with [LTSS] prefix


Governance: OWNERS.md / TSC contact list





Status: Active

Next review: 2026-01

MIT © R3C Foundation — Open, Stable, Deterministic.






