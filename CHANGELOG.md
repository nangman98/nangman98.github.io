# nangman98.github.io — 수정 이력 및 향후 계획

## 수정 이력 (Changelog)

### v1.0 — Initial Commit (`03347ea`)
- Hugo 기반 개인 학술 홈페이지 생성
- 커스텀 테마 `nangman` (Bootstrap 5 + Inter 폰트)
- 6개 페이지 구조: Home, About, Research, Publications, Talks, Photos
- GitHub Actions 자동 배포 워크플로우 설정

### v1.1 — 프로필 및 다크모드 (`5f4fd5d`)
- 홈 페이지에 프로필 사진 + Recent News 타임라인 추가
- About 페이지: 이메일, 학력, GitHub 링크
- Talks: ICAMD 2025 포스터 발표 항목 추가
- Photos: UC Berkeley 방문 연구 사진
- **다크모드 토글** (localStorage 기반 상태 유지)
- SVG 파비콘 (SP)

### v1.2 — 학회 사진 및 발표 (`59c6cd0`)
- BESC2025 단체 사진 추가 (Berkeley 방문 사진 교체)
- Talks: 1st BerkeleyGW Tutorial Workshop & BESC2025 참가 기록

### v1.3 — ICAMD 포스터 사진 (`58f5650`)
- ICAMD 2025 포스터 발표 현장 사진 추가

### v1.4 — 취미 섹션 (`43bb6ff`)
- About 페이지에 Hobbies 추가: 서핑, 패들보드, 주짓수, 사진

### v1.5 — 대외활동 (`86c5d7d`)
- Extracurricular Activities 섹션 추가
  - 주짓수 대회, 가우디움 여행 동아리, SK커뮤니케이션즈, 피플카, 학생회 등
- 전체 영문 통일

### v1.6 — About & Research 리디자인 (`fd8737b`)
- Research Experience: 접이식 detail memo 카드
- Activities: collapsible details → HTML 코멘트 처리
- Research 페이지: 1D 나노구조, 저차원 물질 주제 추가
- Tools: VASP, Python, pymatgen, Phonopy (홈페이지 링크 포함)
- Hobbies: 여행, 캠핑, 별 관측 추가 / BJJ Blue Belt 2-Stripe 뱃지
- Photography 카드에 Instagram 링크
- M.S. 시작일 2025.02로 수정
- many-body perturbation theory 용어 통일

### v1.7 — 이중언어 타이틀 & 레이아웃 정리 (`5ea2bbb`)
- 섹션 타이틀 한/영 병기: 연구 경험/Research Experience, 대외활동/Extracurricular, 취미/Hobbies
- 취미 카드에 서프보드, 패들보드, 배낭 일러스트 SVG 추가
- 카드 사이즈 `aspect-ratio`로 통일
- B.S. 학력에 (Graduated) 표기

---

## 현재 구현된 기능

| 기능 | 상태 | 설명 |
|------|------|------|
| 반응형 레이아웃 | ✅ | Bootstrap 5, 모바일 햄버거 메뉴 |
| 다크모드 | ✅ | 토글 버튼, localStorage 저장, CSS 변수 기반 |
| 사진 갤러리 | ✅ | Lightbox 모달, 키보드 내비게이션, 지연 로딩, 페이지네이션 |
| 프로필/약력 | ✅ | 사진, 학력, 연구 분야, 이메일 |
| 연구 소개 | ✅ | 현재 연구, 관심 분야, 사용 도구 |
| 발표/학회 | ✅ | 발표 이력, 워크숍 참가 기록 |
| 자동 배포 | ✅ | GitHub Actions → GitHub Pages |
| 취미/대외활동 | ✅ | 카드 UI, SVG 일러스트, 뱃지 |

---

## 향후 추가 사항 (TODO)

### 🔴 우선순위 높음
- [ ] **Publications 페이지 채우기** — 논문 발표 시 DOI 링크와 함께 역순 정리
- [ ] **Google Scholar 프로필 링크** — About 페이지에 연결 (현재 TODO 주석 상태)
- [ ] **CV/Resume PDF 업로드** — About 페이지에서 다운로드 가능하도록

### 🟡 중간 우선순위
- [ ] **SEO 메타 태그** — Open Graph, Twitter Card, description 태그 추가
- [ ] **사이트맵 생성** — Hugo 내장 sitemap 템플릿 활성화
- [ ] **Google Analytics 연결** — `hugo.toml`에 GA ID 설정 (코드는 이미 준비됨)
- [ ] **사진 갤러리 확장** — 연구실 생활, 학회, 일상 사진 카테고리화
- [ ] **ORCID 링크 추가** — About 페이지 소셜 링크에 포함

### 🟢 추가 가능한 기능
- [ ] **블로그/포스트 섹션** — 연구 노트, TIL, 계산 팁 등 기록용
- [ ] **프로젝트 쇼케이스** — GitHub 레포를 카드 형태로 소개 (API 연동 가능)
- [ ] **검색 기능** — Fuse.js 기반 클라이언트 사이드 전문 검색
- [ ] **댓글 시스템** — giscus (GitHub Discussions 기반) 또는 utterances
- [ ] **방문자 카운터** — GoatCounter 등 프라이버시 친화적 분석 도구
- [ ] **애니메이션** — 스크롤 시 fade-in, intersection observer 활용
- [ ] **i18n 다국어 지원** — Hugo 내장 기능으로 한/영 페이지 분리
- [ ] **RSS 피드** — Hugo 기본 RSS 템플릿 활성화 (블로그 섹션과 연계)
- [ ] **타임라인 페이지** — 학부 입학부터 현재까지 연구 여정 시각화
- [ ] **연구 도구 인터랙티브 소개** — 사용하는 DFT 코드/워크플로우를 다이어그램으로

---

## 기술 스택

- **Static Site Generator**: Hugo v0.128.0 (extended)
- **Theme**: nangman (커스텀)
- **CSS Framework**: Bootstrap 5.3.3 + Bootstrap Icons
- **Font**: Inter (Google Fonts)
- **Deploy**: GitHub Actions → GitHub Pages
- **Domain**: nangman98.github.io
