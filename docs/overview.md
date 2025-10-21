
# 📁 Rust-LTSS 폴더 구조 로드맵

> ⚙️ 이 문서는 향후 Rust-LTSS 프로젝트에 생성될 주요 폴더 구조를 정의합니다.  
> 코드가 아닌 구조 설계만 포함되어 있습니다.

---

## 🧩 전체 구조 (계획)




Rust-LTSS/
├── src/                  # LTSS 핵심 코드
│   ├── abi/              # ABI 고정 및 호환성 계층
│   ├── system/           # OS별 구현 (linux / windows / macos)
│   └── build/            # R3C 통합 빌드 로직
│
├── ltss/                 # LTS 버전별 스냅샷
│   ├── 2025-LTS/         # 첫 장기 안정 버전
│   └── 2027-LTS/         # 차기 Rust-LTSS 주기 버전
│
├── tools/                # LTSS 전용 CLI / 관리 도구
│   ├── ltsctl/           # LTS 버전 제어, freeze, diff 등
│   ├── checker/          # ABI 안정성 검사기
│   └── reporter/         # LTS 상태 리포트 생성기
│
├── scripts/              # 빌드 및 릴리즈 자동화 스크립트
│   ├── build.sh
│   ├── release.sh
│   └── ci-check.sh
│
├── docs/                 # 공식 문서 및 철학 자료
│   ├── overview.md
│   ├── ltss_spec.md
│   ├── roadmap.md
│   └── philosophy.md
│
└── .github/
└── workflows/        # CI/CD 자동화
├── build.yml
├── ltss-freeze.yml
└── release.yml



---

## 🧠 요약

- `src/` → Rust-LTSS 핵심 엔진  
- `ltss/` → 버전별 LTS 스냅샷 (2025-LTS, 2027-LTS 등)  
- `tools/` → CLI, 분석기, 리포트 도구  
- `scripts/` → 자동화 빌드 및 릴리즈  
- `docs/` → 설계/철학/표준 문서  
- `.github/` → 워크플로우 및 CI 관리

---

> 🪶 *“Rust-LTSS는 Rust의 장기 수명(LTS)과 C 독립 생태계를 위한 실험 플랫폼이다.”*




