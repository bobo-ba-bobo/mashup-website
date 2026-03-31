# 매쉬업벤처스 웹사이트 리뉴얼 프로세스

> 목표: 현재 mashupventures.co를 더 세련되고, 힙하고, 직관적인 웹사이트로 전면 리뉴얼

---

## PHASE 1. 리서치 & 방향 정의

### Step 1-1. 현황 분석
- [ ] 현재 사이트 감사 (디자인, UX, 콘텐츠, 기술 스택)
- [ ] 페이지별 사용자 흐름 정리 (홈 → 팀 → 포트폴리오 → 어플라이 등)
- [ ] 현재 사이트의 문제점 / 개선 포인트 목록화
- [ ] 모바일 대응 현황 확인

### Step 1-2. 레퍼런스 수집
- [ ] 국내외 VC/PE 웹사이트 레퍼런스 20개 이상 수집
- [ ] 스타트업/테크 회사 중 힙한 디자인 사례 수집
- [ ] 디자인 무드보드 작성 (Figma / Notion)
- [ ] 벤치마킹 포인트 정리 (레이아웃, 인터랙션, 타이포, 색상)

### Step 1-3. 목표 정의
- [ ] 리뉴얼 목적 명확화 (브랜드 인지도 / 투자 유치 / 인재 채용 / 포트폴리오 쇼케이스 등)
- [ ] 주요 타겟 유저 정의 (창업자, 투자자, 취준생, 일반 대중)
- [ ] 성공 지표(KPI) 설정
- [ ] 리뉴얼 범위 확정 (전체 리뉴얼 vs 부분 개선)

---

## PHASE 2. BI / CI 정의

### Step 2-1. 브랜드 아이덴티티(BI) 재정의
- [ ] 매쉬업벤처스의 브랜드 포지셔닝 재정립
  - 어떤 VC인가? (초기/초격차/커뮤니티 기반 등)
  - 어떤 감성을 줄 것인가? (Professional / Friendly / Bold / Minimal 등)
- [ ] 브랜드 키워드 도출 (3~5개)
- [ ] 브랜드 보이스 & 톤 정의 (영어/한국어 카피 원칙)

### Step 2-2. 로고 검토
- [ ] 현재 로고 유지 여부 결정
- [ ] 필요 시 로고 리터칭 또는 리디자인
- [ ] 로고 사용 규정 정의 (최소 크기, 여백, 컬러 버전)
- [ ] 파비콘, OG 이미지 업데이트

---

## PHASE 3. 디자인 가이드 수립

### Step 3-1. 컬러 시스템
- [ ] Primary Color 선정 (브랜드 메인 컬러)
- [ ] Secondary / Accent Color 선정
- [ ] Neutral Palette 정의 (배경, 텍스트, 보더용 회색 계열)
- [ ] Semantic Color 정의 (성공/경고/오류 등)
- [ ] 다크모드 대응 여부 결정
- [ ] 컬러 접근성 검토 (WCAG AA 기준 명암비)

```
예시 컬러 구조:
--color-primary: #000000
--color-primary-light: #1a1a1a
--color-accent: #XX (브랜드 포인트 컬러)
--color-gray-100 ~ gray-900
--color-background: #FAFAFA
--color-surface: #FFFFFF
```

### Step 3-2. 타이포그래피 시스템
- [ ] 영문 폰트 선정 (현재: Noto Sans KR → 교체 검토)
- [ ] 한글 폰트 선정 (Pretendard / SUIT / Noto Sans KR 등)
- [ ] 타입 스케일 정의 (Display / H1~H4 / Body / Caption / Label)
- [ ] Line-height, Letter-spacing 규칙 정의
- [ ] 반응형 타입 스케일 정의 (데스크탑 / 태블릿 / 모바일)

```
예시 타입 스케일:
Display: 64px / 700weight
H1: 48px / 700weight
H2: 36px / 600weight
H3: 28px / 600weight
Body L: 18px / 400weight
Body M: 16px / 400weight
Caption: 13px / 400weight
```

### Step 3-3. 간격 & 레이아웃 시스템
- [ ] 8px 기반 스페이싱 시스템 정의
- [ ] 페이지 최대 너비 설정 (1280px / 1440px)
- [ ] 컨텐츠 영역 마진 설정 (데스크탑: 120px / 태블릿: 48px / 모바일: 24px)
- [ ] Grid 시스템 정의 (12컬럼 등)
- [ ] Section padding 규칙 정의

### Step 3-4. 이미지 & 아이콘
- [ ] 이미지 스타일 가이드 (흑백 / 컬러 / 모노톤 필터 등)
- [ ] 아이콘 라이브러리 선택 (Lucide / Phosphor / Heroicons 등)
- [ ] 일러스트레이션 사용 여부 결정

---

## PHASE 4. 디자인 시스템 구축

### Step 4-1. 컴포넌트 목록 정의
- [ ] 원자(Atom): Button, Input, Tag, Badge, Icon, Avatar, Divider
- [ ] 분자(Molecule): Card, NavItem, FormField, Tooltip, Modal
- [ ] 유기체(Organism): Header, Footer, Hero, PortfolioGrid, TeamCard, ContentCard
- [ ] 템플릿: Page layouts per page type

### Step 4-2. Figma 디자인 시스템 구축
- [ ] Figma Variables 설정 (Color, Typography, Spacing)
- [ ] 컴포넌트별 모든 상태 디자인 (Default / Hover / Active / Disabled / Focus)
- [ ] Auto Layout 적용
- [ ] 반응형 breakpoint별 컴포넌트 변형 정의
- [ ] Design Token 명세서 작성

### Step 4-3. 인터랙션 & 애니메이션 원칙
- [ ] Transition 기본 설정 (duration, easing 함수)
- [ ] Hover 효과 원칙
- [ ] 스크롤 인터랙션 범위 정의 (parallax / fade-in 등)
- [ ] 페이지 전환 방식 결정
- [ ] 로딩 상태 처리 방식

---

## PHASE 5. 정보 구조(IA) & UX 설계

### Step 5-1. 사이트맵 재설계
- [ ] 현재 사이트맵 정리
- [ ] 신규 사이트맵 설계
  - 홈 / 팀 / 포트폴리오 / 그로스 네트워크 / 콘텐츠 / 커리어 / 어플라이
- [ ] URL 구조 정의
- [ ] 네비게이션 구조 결정 (GNB / 사이드바 / 풀스크린 등)

### Step 5-2. 와이어프레임
- [ ] 홈페이지 와이어프레임
- [ ] 팀 페이지 와이어프레임
- [ ] 포트폴리오 페이지 와이어프레임
- [ ] 그로스 네트워크 페이지 와이어프레임
- [ ] 콘텐츠(블로그) 페이지 와이어프레임
- [ ] 어플라이 페이지 와이어프레임
- [ ] 모바일 레이아웃 와이어프레임

### Step 5-3. 콘텐츠 전략
- [ ] 각 페이지 카피 재작성 계획
- [ ] 포트폴리오 데이터 구조 정의
- [ ] 팀 프로필 포맷 통일
- [ ] SEO 키워드 전략

---

## PHASE 6. 시각 디자인 (UI Design)

### Step 6-1. 페이지별 UI 디자인
- [ ] 홈페이지 디자인 (데스크탑 → 모바일)
- [ ] 팀 페이지
- [ ] 포트폴리오 페이지
- [ ] 그로스 네트워크 페이지
- [ ] 콘텐츠 페이지
- [ ] 어플라이 페이지
- [ ] 404 / 에러 페이지

### Step 6-2. 디자인 검토
- [ ] 내부 리뷰 (팀 피드백)
- [ ] 브랜드 일관성 체크
- [ ] 접근성 검토 (색상 대비, 폰트 크기, 탭 인덱스)
- [ ] 반응형 레이아웃 확인

---

## PHASE 7. 개발

### Step 7-1. 기술 스택 결정
- [ ] 프레임워크 선택 (Next.js / Astro / 순수 HTML 등)
- [ ] 스타일링 방식 (Tailwind CSS / CSS Modules / Styled Components 등)
- [ ] CMS 도입 여부 (콘텐츠, 포트폴리오 관리용)
- [ ] 호스팅 플랫폼 확정 (Vercel)
- [ ] 도메인 및 SSL 확인

### Step 7-2. 개발 환경 세팅
- [ ] GitHub 저장소 구성
- [ ] 브랜치 전략 정의 (main / dev / feature/*)
- [ ] 디자인 토큰 → CSS Variables / Tailwind config 연동
- [ ] 컴포넌트 개발 순서 계획

### Step 7-3. 개발 & QA
- [ ] 컴포넌트 개발
- [ ] 페이지 개발
- [ ] 크로스 브라우저 테스트 (Chrome / Safari / Firefox)
- [ ] 반응형 테스트 (Mobile / Tablet / Desktop)
- [ ] 퍼포먼스 최적화 (LCP, CLS, FID)
- [ ] SEO 메타태그, OG 태그 적용

---

## PHASE 8. 런칭 & 이후

### Step 8-1. 런칭 준비
- [ ] 스테이징 환경 최종 확인
- [ ] GA4 / 분석 툴 연동
- [ ] Sitemap.xml, robots.txt 설정
- [ ] 도메인 연결 및 DNS 설정

### Step 8-2. 런칭
- [ ] 기존 사이트 백업
- [ ] 신규 사이트 배포
- [ ] 런칭 후 모니터링 (에러, 속도, 사용자 반응)

### Step 8-3. 운영
- [ ] 콘텐츠 업데이트 프로세스 정의
- [ ] 포트폴리오 추가/수정 프로세스
- [ ] 팀 프로필 업데이트 프로세스
- [ ] 정기 성과 리뷰

---

## 현재 사이트 현황 메모

| 항목 | 현재 |
|------|------|
| 폰트 | Noto Sans KR |
| 주요 컬러 | White + Blue 계열 |
| 네비게이션 | Team / Portfolio / Growth Network / Contents / Career / Apply |
| 주요 섹션 | Hero / 포트폴리오 그리드 / 투자 성과 / 투자 전략 / TIPS / 멘토 / 창업자 후기 / 콘텐츠 |
| 기술 스택 | 미확인 (정적 사이트 추정) |

---

## 참고 레퍼런스 (수집 예정)

- [ ] a16z.com
- [ ] sequoiacap.com
- [ ] accel.com
- [ ] bonfire.vc
- [ ] lerer.vc
- [ ] 국내: sopoong.net, bluepoint.ac, primer.kr
