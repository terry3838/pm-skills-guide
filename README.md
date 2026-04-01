# PM Skills 마스터 가이드

**비개발자를 위한 체계적 제품 관리 스킬 학습서**

---

## 이 가이드는 무엇인가?

이 가이드는 [PM Skills Marketplace](https://github.com/phuryn/pm-skills)에 수록된 **65개 PM 스킬**을 체계적으로 학습하기 위한 교육 문서입니다. 각 스킬이 무엇을 하는지, 언제 사용하는지, 어떤 순서로 실행해야 최대 효과를 얻는지를 설명합니다.

PM 스킬은 독립적으로도 사용할 수 있지만, 올바른 순서로 연결하면 산출물이 다음 스킬의 입력이 되어 전략 수립의 품질이 크게 높아집니다. 이 가이드는 그 연결 고리를 명확하게 보여줍니다.

---

## 대상 독자

이 가이드는 다음과 같은 분을 위해 작성되었습니다.

- **PM 경험이 없는 Product Owner (PO)**: 체계적인 제품 관리 교육을 받지 않았지만, 제품의 방향을 결정해야 하는 역할을 맡고 있는 분
- **AI 코딩 에이전트 사용 경험이 있는 분**: Claude Code, Cursor, Copilot 등 AI 도구를 활용해 개발을 진행해본 경험이 있는 분
- **"무엇을 만들지"보다 "왜 만드는지"를 고민하기 시작한 분**: 기능 구현은 할 수 있지만, 전략적 우선순위 결정에 어려움을 느끼는 분

코딩 지식은 필요하지 않습니다. 모든 PM 스킬은 질문에 답하는 방식으로 작동합니다.

---

## PM Skills이란?

PM Skills은 **Claude Code에서 `/pm-...` 슬래시 명령어로 실행하는 AI 보조 도구**입니다.

작동 방식은 간단합니다:

1. Claude Code에서 `/pm-카테고리:스킬명` 형식으로 명령어를 입력합니다
2. AI가 해당 스킬에 맞는 질문들을 순서대로 던집니다
3. 질문에 답변하면, AI가 답변을 바탕으로 **전략 문서를 자동 생성**합니다

예를 들어 `/pm-product-strategy:product-strategy`를 실행하면, 비전, 타겟 고객, 핵심 문제, 차별화 요소 등 9개 섹션에 대한 질문을 받고, 답변을 종합한 "제품 전략 캔버스" 문서가 만들어집니다.

코딩과 무관하며, **제품 전략에 대한 구조화된 사고**를 돕는 도구입니다.

---

## PM Skills 생태계 전체 구조

![Diagram 1](assets/diagrams/README__diagram_1.svg)

---

## 8개 카테고리 개요

PM Skills은 8개 카테고리, 총 65개 스킬로 구성됩니다. 각 카테고리의 역할과 포함된 스킬을 소개합니다.

### 1. pm-product-strategy (제품 전략) -- 12 스킬

| 항목 | 내용 |
|------|------|
| **핵심 설명** | 제품의 방향성을 잡는 전략 도구 모음. 비전 수립부터 비즈니스 모델, 가격 책정, 경쟁 분석까지 제품 전략의 전 영역을 다룹니다. |
| **주요 스킬** | 제품 전략 캔버스, 비전 선언문, 비즈니스 모델 캔버스, 가격 전략, 경쟁 분석, 가치 제안, SWOT 분석, Ansoff 매트릭스, Lean Canvas, Startup Canvas |
| **난이도 범위** | 초급 ~ 중급 |
| **언제 사용하나** | 제품을 처음 기획할 때, 방향 전환을 고려할 때, 투자자/이해관계자에게 전략을 설명해야 할 때 |
| **상세 문서** | [categories/pm-product-strategy.md](categories/pm-product-strategy.md) |

### 2. pm-product-discovery (제품 발견) -- 13 스킬

| 항목 | 내용 |
|------|------|
| **핵심 설명** | 아이디어를 검증하고 실험을 설계하는 도구 모음. "이것을 만들어야 하는가?"라는 질문에 데이터로 답하게 해줍니다. |
| **주요 스킬** | 아이디어 브레인스토밍, 실험 설계(신규/기존 제품), 가정 검증, OST(기회 해결 트리), 사용자 인터뷰 가이드, Pretotype, Kano 모델, JTBD 분석, 스테이크홀더 맵 |
| **난이도 범위** | 초급 ~ 고급 |
| **언제 사용하나** | 새 기능을 만들기 전에 수요를 확인할 때, 어떤 문제가 진짜 문제인지 판별할 때, 실험을 설계할 때 |
| **상세 문서** | [categories/pm-product-discovery.md](categories/pm-product-discovery.md) |

### 3. pm-market-research (시장 조사) -- 7 스킬

| 항목 | 내용 |
|------|------|
| **핵심 설명** | 시장과 고객을 이해하는 리서치 도구 모음. 누가 고객인지, 시장이 얼마나 큰지, 고객의 여정이 어떤지를 파악합니다. |
| **주요 스킬** | 사용자 페르소나, 시장 세그먼트, 고객 여정 맵, 시장 규모(TAM/SAM/SOM), 경쟁 분석, 감성 분석, PESTLE 분석 |
| **난이도 범위** | 초급 ~ 중급 |
| **언제 사용하나** | 타겟 고객을 정의할 때, 시장 진입 전략을 세울 때, 경쟁 환경을 파악할 때 |
| **상세 문서** | [categories/pm-market-research.md](categories/pm-market-research.md) |

### 4. pm-execution (실행) -- 15 스킬

| 항목 | 내용 |
|------|------|
| **핵심 설명** | 전략을 실행으로 옮기는 도구 모음. PRD 작성, OKR 설정, 로드맵, 스프린트 관리, 회고까지 실행의 전 과정을 지원합니다. |
| **주요 스킬** | PRD 작성, OKR 브레인스토밍, 우선순위 프레임워크(RICE/ICE/MoSCoW), 결과 로드맵, 스프린트 계획, 회고, 릴리스 노트, Pre-mortem, 의존성 관리, 리스크 분석 |
| **난이도 범위** | 초급 ~ 고급 |
| **언제 사용하나** | 전략을 구체적 계획으로 전환할 때, 개발팀(또는 AI 에이전트)에 작업을 전달할 때, 실행 결과를 복기할 때 |
| **상세 문서** | [categories/pm-execution.md](categories/pm-execution.md) |

### 5. pm-go-to-market (시장 진입) -- 6 스킬

| 항목 | 내용 |
|------|------|
| **핵심 설명** | 제품을 시장에 내놓는 전략 도구 모음. 첫 번째 고객을 어떻게 확보하고, 어떤 시장에서 시작할지를 결정합니다. |
| **주요 스킬** | GTM 전략, Beachhead 세그먼트, ICP(이상적 고객 프로필), 성장 루프, Porter's Five Forces, 채널 전략 |
| **난이도 범위** | 중급 ~ 고급 |
| **언제 사용하나** | 첫 고객을 확보하려 할 때, 어떤 시장부터 공략할지 결정할 때, 성장 전략을 수립할 때 |
| **상세 문서** | [categories/pm-go-to-market.md](categories/pm-go-to-market.md) |

### 6. pm-marketing-growth (마케팅/성장) -- 5 스킬

| 항목 | 내용 |
|------|------|
| **핵심 설명** | 제품 성장을 이끄는 마케팅 전략 도구 모음. 포지셔닝, 핵심 지표, 마케팅 아이디어를 체계적으로 만듭니다. |
| **주요 스킬** | 마케팅 아이디어 생성, 포지셔닝 전략, North Star Metric, 성장 실험, 콘텐츠 전략 |
| **난이도 범위** | 중급 ~ 고급 |
| **언제 사용하나** | 제품을 어떻게 알릴지 고민할 때, 핵심 성과 지표를 정의할 때, 성장 전략을 실험할 때 |
| **상세 문서** | [categories/pm-marketing-growth.md](categories/pm-marketing-growth.md) |

### 7. pm-data-analytics (데이터 분석) -- 3 스킬

| 항목 | 내용 |
|------|------|
| **핵심 설명** | 데이터로 의사결정을 지원하는 분석 도구 모음. SQL 쿼리 생성, 코호트 분석, A/B 테스트 분석을 AI 도움으로 수행합니다. |
| **주요 스킬** | SQL 쿼리 생성, 코호트 분석, A/B 테스트 분석 |
| **난이도 범위** | 중급 ~ 고급 |
| **언제 사용하나** | 사용자 행동 데이터를 분석할 때, 실험 결과를 통계적으로 검증할 때, 특정 사용자 그룹의 패턴을 파악할 때 |
| **상세 문서** | [categories/pm-data-analytics.md](categories/pm-data-analytics.md) |

### 8. pm-toolkit (도구함) -- 4 스킬

| 항목 | 내용 |
|------|------|
| **핵심 설명** | PM 업무에 필요한 실용적 보조 도구 모음. 문서 교정, 법률 문서 초안, 이력서 검토 등 일상 업무를 지원합니다. |
| **주요 스킬** | 문법/스타일 체크, NDA 초안 작성, 개인정보 처리 방침, 이력서 리뷰 |
| **난이도 범위** | 초급 |
| **언제 사용하나** | 중요 문서의 문법을 점검할 때, 파트너십/계약 관련 문서가 필요할 때, 채용 시 이력서를 검토할 때 |
| **상세 문서** | [categories/pm-toolkit.md](categories/pm-toolkit.md) |

---

## 추천 학습 경로 요약

PM 스킬은 특정 순서로 실행할 때 가장 효과적입니다. 이전 스킬의 산출물이 다음 스킬의 입력이 되기 때문입니다.

![Diagram 2](assets/diagrams/README__diagram_2.svg)

자세한 학습 경로, 각 스킬 간의 연결 관계, SprintX 맞춤 실행 순서는 [01-learning-paths.md](01-learning-paths.md)를 참조하세요.

---

## 문서 구조

이 가이드는 다음과 같이 구성되어 있습니다.

```
pm-skills-guide/
├── README.md                              # 이 문서 (전체 개요)
├── 01-learning-paths.md                   # 학습 경로 상세 가이드
├── 02-glossary.md                         # PM 용어 사전 (50+ 용어)
└── categories/                            # 카테고리별 상세 문서
    ├── pm-product-strategy.md             # 제품 전략 (12 스킬)
    ├── pm-product-discovery.md            # 제품 발견 (13 스킬)
    ├── pm-market-research.md              # 시장 조사 (7 스킬)
    ├── pm-execution.md                    # 실행 (15 스킬)
    ├── pm-go-to-market.md                 # 시장 진입 (6 스킬)
    ├── pm-marketing-growth.md             # 마케팅/성장 (5 스킬)
    ├── pm-data-analytics.md               # 데이터 분석 (3 스킬)
    └── pm-toolkit.md                      # 도구함 (4 스킬)
```

---

## 참고 자료

### PM Skills 원본

- **PM Skills GitHub**: [https://github.com/phuryn/pm-skills](https://github.com/phuryn/pm-skills) -- 65개 스킬의 원본 코드와 프롬프트

### 뉴스레터

- **Product Compass Newsletter**: [https://www.productcompass.pm](https://www.productcompass.pm) -- PM Skills의 기반이 된 제품 관리 뉴스레터. 실무 PM 프레임워크와 사례를 주간으로 제공합니다.

### 영감을 준 저자들

이 가이드와 PM Skills에 영향을 준 주요 저자와 그들의 핵심 기여:

| 저자 | 핵심 기여 | 대표 저서/개념 |
|------|----------|---------------|
| **Teresa Torres** | Continuous Discovery Habits | OST(Opportunity Solution Tree), 주간 사용자 접점 습관화 |
| **Marty Cagan** | Product Management 원칙 | Empowered Product Teams, Product Discovery vs Delivery |
| **Alberto Savoia** | Pretotyping | "Build the right it before you build it right", Fake Door Test |
| **Dan Olsen** | Lean Product Playbook | PMF 피라미드, 체계적 제품-시장 적합성 달성 방법론 |
| **Eric Ries** | Lean Startup | MVP, Build-Measure-Learn, 검증된 학습 |
| **Alexander Osterwalder** | Business Model Canvas | 비즈니스 모델 시각화, Value Proposition Canvas |
| **Geoffrey Moore** | Crossing the Chasm | Beachhead 전략, 기술 채택 생명주기 |
| **Sean Ellis** | Growth Hacking | North Star Metric, PMF 설문 ("매우 실망할 것" 40% 기준) |

---

> 이 가이드에 대한 질문이나 개선 제안은 GitHub Issues로 남겨주세요.

<!-- GUIDE_SYNC:START -->
## 자동 동기화 상태

- origin repo: `pm-skills`
- latest source commit: `36ccefdc6c2e`
- sync mode: `no-change`
- 영향 분류: 일반 변경

### 이번 반영 포인트

이번 싸이클에서는 origin 변경이 없어 guide 본문은 유지했고, 동기화 기준점만 재확인했습니다.

### 변경 파일 샘플

- 이번 싸이클에서는 신규 변경 파일이 없습니다.

> 이 블록은 guide sync가 자동 갱신합니다.
<!-- GUIDE_SYNC:END -->
