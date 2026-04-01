# Phase 3 — 디자인 가이드

> 작성일: 2026-04-01
> 확정 방향: 라이트 베이스 + Warm Amber + Instrument Serif × Pretendard

---

## 1. 컬러 시스템

### 1-1. 팔레트 전체

```
/* ── Background ── */
--color-bg:          #F7F5F0   /* 따뜻한 오프화이트, 전체 페이지 배경 */
--color-surface:     #FFFFFF   /* 카드, 모달, 입력 필드 배경 */
--color-surface-2:   #F0EDE6   /* 섹션 구분용 약간 더 어두운 배경 */

/* ── Brand Accent (Warm Amber) ── */
--color-amber-50:    #FEF3E2
--color-amber-100:   #FDDDA6
--color-amber-200:   #FBC96A
--color-amber-300:   #F5A623
--color-amber-400:   #E8941A   /* 주 사용 Accent */
--color-amber-500:   #C8781A   /* Primary Accent — 버튼, 링크, 강조 */
--color-amber-600:   #A85E0F
--color-amber-700:   #7A4209

/* ── Text ── */
--color-text-primary:    #111111   /* 헤딩, 주요 본문 */
--color-text-secondary:  #555555   /* 보조 텍스트, 캡션 */
--color-text-tertiary:   #999999   /* 플레이스홀더, 비활성 */
--color-text-inverse:    #FFFFFF   /* 다크 배경 위 텍스트 */

/* ── Neutral Gray ── */
--color-gray-50:     #FAFAF8
--color-gray-100:    #F0EDE6
--color-gray-200:    #E2DDD4
--color-gray-300:    #C8C2B8
--color-gray-400:    #A8A098
--color-gray-500:    #7A7268
--color-gray-600:    #555048
--color-gray-700:    #3A3530
--color-gray-800:    #222018
--color-gray-900:    #111111

/* ── Semantic ── */
--color-success:     #2D7A4F
--color-warning:     #C8781A   /* Amber 500 재활용 */
--color-error:       #C0392B

/* ── Dark Section (Inverted) ── */
--color-dark-bg:     #111111
--color-dark-surface:#1C1C1A
```

---

### 1-2. 사용 원칙

| 역할 | 사용 컬러 | 비고 |
|------|-----------|------|
| 페이지 배경 | `--color-bg` (#F7F5F0) | 차가운 흰색 X, 따뜻한 오프화이트 |
| 카드/컴포넌트 배경 | `--color-surface` (#FFFFFF) | bg와 대비 |
| 주요 강조 (CTA, 링크) | `--color-amber-500` (#C8781A) | 절제해서 사용 |
| Hover Accent | `--color-amber-400` (#E8941A) | 밝아지는 방향 |
| 주 본문 | `--color-text-primary` (#111111) | 순수 블랙 X |
| 보조 텍스트 | `--color-text-secondary` (#555555) | |
| 다크 섹션 (Footer 등) | `--color-dark-bg` (#111111) | 전체의 20% 이내 |
| 태그 / 배지 | `--color-amber-50` 배경 + `--color-amber-600` 텍스트 | |

**Amber 사용 빈도 원칙:**
- 많이 쓸수록 희석됨 → 한 페이지에 5군데 이내
- 주로: CTA 버튼, 링크 언더라인, 섹션 악센트 라인, 태그

---

### 1-3. 다크 섹션 (Footer / 히어로 변형)

```
배경: #111111
텍스트: #F7F5F0
Accent: #E8941A (Amber 400 — 다크 위에서 더 밝게)
보조: #7A7268 (Gray 500)
```

---

### 1-4. 접근성

- 본문 (#111111 on #F7F5F0): 명암비 **15.3:1** ✅ AAA
- Amber CTA (#C8781A on #FFFFFF): 명암비 **4.6:1** ✅ AA
- 다크 섹션 텍스트 (#F7F5F0 on #111111): 명암비 **15.3:1** ✅ AAA

---

## 2. 타이포그래피 시스템

### 2-1. 폰트 스택

```css
/* Display & Hero — 영문 */
font-family: 'Instrument Serif', Georgia, serif;

/* Body & UI — 영문 */
font-family: 'Plus Jakarta Sans', -apple-system, sans-serif;

/* 전체 — 한글 */
font-family: 'Pretendard', 'Apple SD Gothic Neo', sans-serif;

/* 레이블/코드 (선택적) */
font-family: 'JetBrains Mono', monospace;
```

**로딩 전략:**
- Pretendard: 자체 호스팅 (CDN 의존 X)
- Instrument Serif: Google Fonts (display swap)
- Plus Jakarta Sans: Google Fonts (display swap)

---

### 2-2. 타입 스케일

| 토큰 | 크기 | Line-height | Letter-spacing | 폰트 | 용도 |
|------|------|-------------|----------------|------|------|
| `display-2xl` | 80px | 1.05 | -0.03em | Instrument Serif | 최대 히어로 |
| `display-xl` | 64px | 1.1 | -0.025em | Instrument Serif | 히어로 주 헤딩 |
| `display-lg` | 52px | 1.1 | -0.02em | Instrument Serif | 섹션 주 헤딩 |
| `heading-xl` | 40px | 1.2 | -0.015em | Plus Jakarta Sans 700 | 서브 헤딩 |
| `heading-lg` | 32px | 1.25 | -0.01em | Plus Jakarta Sans 600 | 카드 타이틀 |
| `heading-md` | 24px | 1.3 | 0 | Plus Jakarta Sans 600 | 소섹션 타이틀 |
| `heading-sm` | 20px | 1.35 | 0 | Plus Jakarta Sans 600 | 컴포넌트 타이틀 |
| `body-xl` | 20px | 1.7 | 0 | Plus Jakarta Sans 400 | 리드 카피, 서브헤드 |
| `body-lg` | 18px | 1.7 | 0 | Plus Jakarta Sans 400 | 주요 본문 |
| `body-md` | 16px | 1.65 | 0 | Plus Jakarta Sans 400 | 기본 본문 |
| `body-sm` | 14px | 1.6 | 0 | Plus Jakarta Sans 400 | 보조 본문 |
| `label-lg` | 13px | 1.4 | 0.06em | Plus Jakarta Sans 500 | 태그, 버튼 |
| `label-md` | 11px | 1.4 | 0.1em | Plus Jakarta Sans 600 | 섹션 레이블, 배지 |
| `mono` | 13px | 1.5 | 0.02em | JetBrains Mono | 코드 레이블, 날짜 |

**한글은 동일 스케일 적용, Pretendard 사용**
- 한글 Line-height: 영문보다 0.1 증가 (예: body-lg → 1.8)
- 한글 Letter-spacing: 기본값 유지 (조정 불필요)

---

### 2-3. 타이포그래피 사용 패턴

**히어로 섹션 (전형적 구조):**
```
[label-md / Mono / Amber]   MASHUP VENTURES  ·  SINCE 2013
[display-xl / Instrument Serif]  가장 이른 순간,
                                 가장 깊이 함께합니다.
[body-xl / Plus Jakarta Sans]   매쉬업벤처스는 창업자 출신 파트너와...
[label-lg / Plus Jakarta Sans]  → 투자검토 신청
```

**섹션 헤딩 패턴:**
```
[label-md / Mono / Amber / uppercase]  // PORTFOLIO
[display-lg / Instrument Serif]  206개사와 함께한
                                 성장의 기록
```

---

## 3. 간격 & 레이아웃 시스템

### 3-1. 스페이싱 토큰 (8px 기반)

```
--space-1:    4px
--space-2:    8px
--space-3:    12px
--space-4:    16px
--space-5:    20px
--space-6:    24px
--space-8:    32px
--space-10:   40px
--space-12:   48px
--space-16:   64px
--space-20:   80px
--space-24:   96px
--space-32:   128px
--space-40:   160px
```

---

### 3-2. 레이아웃 & 그리드

```
최대 너비:         1280px
페이지 마진:       120px (데스크탑) / 48px (태블릿) / 24px (모바일)
컨텐츠 너비:       1040px (글 읽기용 최대)
좁은 컨텐츠:       720px (단일 컬럼 텍스트)

그리드:            12컬럼 / 28px 거터 (데스크탑)
                   8컬럼 / 24px 거터 (태블릿)
                   4컬럼 / 16px 거터 (모바일)
```

---

### 3-3. 섹션 패딩

```
Hero:              160px top / 120px bottom (데스크탑)
                   100px top / 80px bottom (모바일)

일반 섹션:         120px top/bottom (데스크탑)
                   80px top/bottom (모바일)

타이트 섹션:       80px top/bottom (데스크탑)
                   56px top/bottom (모바일)
```

**원칙: 여백을 아끼지 않는다.** 빽빽한 레이아웃은 권위를 낮춤.

---

### 3-4. Breakpoints

```
mobile:    < 768px
tablet:    768px – 1023px
desktop:   1024px – 1279px
wide:      ≥ 1280px
```

---

## 4. 컴포넌트 가이드라인

### 4-1. 버튼

```
Primary (Amber Fill)
  배경: --color-amber-500
  텍스트: #FFFFFF
  Hover: --color-amber-400
  Padding: 14px 28px
  Border-radius: 4px
  Font: label-lg / Plus Jakarta Sans 500

Secondary (Outline)
  배경: transparent
  보더: 1.5px solid --color-text-primary
  텍스트: --color-text-primary
  Hover: 배경 --color-gray-100

Ghost (Text Link)
  텍스트: --color-amber-500
  밑줄: 얇은 언더라인 (1px)
  Hover: --color-amber-400
```

---

### 4-2. 카드

```
배경: --color-surface (#FFFFFF)
보더: 1px solid --color-gray-200
Border-radius: 8px
Shadow: 없음 (flat) — hover 시만 subtle shadow
Padding: 32px (기본) / 24px (컴팩트)
Hover: translateY(-2px) + box-shadow 0 8px 24px rgba(0,0,0,0.06)
Transition: 0.2s ease
```

---

### 4-3. 태그 / 배지

```
IPO / M&A 배지:
  배경: --color-amber-50
  텍스트: --color-amber-600
  Font: label-md / uppercase / letter-spacing 0.1em
  Padding: 4px 10px
  Border-radius: 2px

카테고리 태그:
  배경: --color-gray-100
  텍스트: --color-gray-600
  동일 구조
```

---

### 4-4. 내비게이션

```
높이: 64px (데스크탑) / 56px (모바일)
배경: --color-bg / backdrop-filter: blur(12px) + 80% 불투명도 (스크롤 시)
로고: 좌측 고정
메뉴: 우측 정렬 / Plus Jakarta Sans 400 / 15px
CTA 버튼: Primary (Amber) — "투자검토 신청"
언어 토글: EN | KO — 우측 상단, label-md 스타일
Mobile: 풀스크린 오버레이 메뉴 (Pretendard, 큰 사이즈)
```

---

### 4-5. 섹션 레이블 패턴 (BlueBrown식 코드 레이블)

히어로나 섹션 시작부에 소문자 + 모노스페이스로 컨텍스트 제공:
```
// portfolio          // team           // growth-network
```
색상: `--color-amber-500` or `--color-text-tertiary`
Font: JetBrains Mono 13px

---

## 5. 이미지 & 비주얼 가이드라인

### 5-1. 이미지 스타일
- **인물 사진**: 자연스럽고 따뜻한 톤 — 지나친 보정 X
- **포트폴리오사 로고**: SVG 우선, 다크/라이트 버전 모두 확보
- **배경 이미지**: 사용 최소화 — 배경은 컬러로 해결
- **OG 이미지**: Amber 베이스 + Instrument Serif 로고 텍스트

### 5-2. 이미지 처리
- 포맷: WebP (fallback: JPEG/PNG)
- 모든 이미지: `loading="lazy"` + `srcset`
- 비율: 팀 프로필 1:1, 포트폴리오 카드 4:3, 히어로 16:9

### 5-3. 아이콘
- **라이브러리**: Lucide Icons (Material Icons 교체)
- 스타일: stroke 기반, 1.5px stroke-width
- 크기: 16px / 20px / 24px 3단계
- 컬러: 텍스트 컬러 상속 or Amber Accent

---

## 6. 인터랙션 & 애니메이션 원칙

### 6-1. 기본 트랜지션

```css
/* 기본 */
transition: all 0.2s ease;

/* 카드 hover */
transition: transform 0.25s ease, box-shadow 0.25s ease;

/* 페이지 진입 fade */
transition: opacity 0.4s ease, transform 0.4s ease;

/* 내비 배경 blur */
transition: background 0.3s ease, backdrop-filter 0.3s ease;
```

---

### 6-2. 스크롤 진입 애니메이션

```
패턴: opacity 0 → 1 + translateY(24px → 0)
Duration: 0.5s
Easing: cubic-bezier(0.16, 1, 0.3, 1)   /* ease-out-expo */
Delay: 섹션 내 요소 순서에 따라 0.05s 스태거

적용 대상: 섹션 헤딩, 카드, 통계 숫자
비적용: 네비게이션, 버튼, 인라인 텍스트
```

---

### 6-3. 숫자 카운터 애니메이션

투자 성과 수치 (206개사, 11.3조원 등) — 뷰포트 진입 시 카운트업
```
Duration: 1.2s
Easing: ease-out
Start: 뷰포트 50% 진입 시
```

---

### 6-4. 절제 원칙
- **모션은 의미 있을 때만** — 장식용 애니메이션 X
- **Reduced Motion 대응 필수** (`prefers-reduced-motion: reduce`)
- **parallax 지양** — 권위 있는 브랜드는 조용한 자신감

---

## 7. 다크 섹션 사용 가이드

전체의 **20% 이내**로 절제. 사용 권장 위치:
- Footer
- 투자 성과 강조 섹션 (숫자가 드라마틱하게 보임)
- CTA 마지막 섹션 ("지금 신청하세요")

다크 섹션 내부 규칙:
```
배경: #111111
텍스트: #F7F5F0
Accent: --color-amber-400 (#E8941A)
보더/구분선: rgba(255,255,255,0.1)
```

---

## 8. 한/영 전환 원칙

```
토글 위치: 내비게이션 우측 상단
형태: KO | EN  (현재 언어 Amber 강조, 비활성 Gray)
전환 방식: URL 기반 (/en/) or lang attr 기반
영문 카피: 번역 X, 독립 재작성
폰트: 한/영 동일 스케일, 폰트만 전환
  KO: Pretendard
  EN: Instrument Serif (display) + Plus Jakarta Sans (body)
```

---

## 9. 금지 사항 (Don'ts)

| ❌ 하지 말 것 | ✅ 대신 |
|-------------|---------|
| 순수 흰색 (#FFFFFF) 배경 전체 사용 | #F7F5F0 오프화이트 |
| 파란 계열 컬러 사용 | Amber 단일 포인트 |
| 그라디언트 | flat color |
| 드롭쉐도우 과다 사용 | 미니멀 shadow (hover 시만) |
| 폰트 3가지 이상 혼재 | 지정된 3종만 |
| 자간 좁히기 (음수 자간 과다) | 스케일 내 값만 |
| 버튼 border-radius 크게 (pill 형태) | max 8px |
| 과도한 스크롤 애니메이션 | 진입 fade만 |
| 포트폴리오 로고만 나열 | 스토리/컨텍스트 함께 |

---

## 10. 요약 — 한눈에 보기

```
베이스 컬러:   #F7F5F0 (따뜻한 오프화이트)
포인트 컬러:   #C8781A (Warm Amber)
다크 컬러:     #111111
주요 텍스트:   #111111

디스플레이:    Instrument Serif (EN 헤딩)
바디:          Plus Jakarta Sans (EN 본문) + Pretendard (KO)
레이블:        JetBrains Mono (코드 스타일 레이블)

히어로 카피:   "가장 이른 순간, 가장 깊이 함께합니다."
               "We back founders before the world does."

핵심 원칙:     여백을 아끼지 않는다 / Amber는 절제해서 쓴다 / 모션은 조용하게
```
