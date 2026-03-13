---
name: metrics-dashboard
description: "핵심 지표, 데이터 소스, 시각화 유형, 알림 임계값을 포함한 제품 지표 대시보드를 정의하고 설계합니다. 지표 대시보드 구축, KPI 정의, 제품 분석 설정, 데이터 모니터링 계획 수립 시 활용하세요."
---

## 제품 지표 대시보드

올바른 지표, 시각화, 알림 임계값을 갖춘 종합적인 제품 지표 대시보드를 설계합니다.

### 컨텍스트

**$ARGUMENTS**를 위한 지표 대시보드를 설계합니다.

사용자가 파일(기존 대시보드, 분석 데이터, OKR, 전략 문서 등)을 제공하면 먼저 읽으세요.

### 도메인 컨텍스트

**Metrics vs KPIs vs NSM**: Metrics = 측정 가능한 모든 것. KPIs = 장기간 추적하는 핵심 정량 지표 몇 가지. North Star Metric = 비즈니스 성공의 선행 지표이자 고객 중심의 단일 KPI.

**좋은 지표의 4가지 기준** (Ben Yoskovitz, *Lean Analytics*): (1) 이해 가능 — 공통 언어 형성. (2) 비교 가능 — 스냅샷이 아닌 시간에 따른 변화. (3) 비율 또는 비 — 절대값보다 더 많은 인사이트 제공. (4) 행동 변화 유발 — 황금 원칙: "지표가 당신의 행동을 바꾸지 않는다면, 그것은 나쁜 지표다."

**8가지 지표 유형**: Vanity vs Actionable (행동을 바꾸는 것은 실행 가능한 지표뿐), Qualitative vs Quantitative (WHAT vs WHY — 둘 다 필요; 고객과의 대화를 멈추지 마세요), Exploratory vs Reporting (데이터를 탐색해 예상치 못한 인사이트 발굴), Lagging vs Leading (선행 지표는 더 빠른 학습 사이클을 가능하게 함, 예: 고객 불만은 이탈을 예측).

**5가지 실행 단계**: (1) 좋은 지표의 4가지 기준으로 지표 감사. (2) 대시보드 업데이트 — 모든 핵심 지표가 좋은 지표인지 확인. (3) Vanity 지표 파악 — 사용 방식에 주의. (4) 선행 vs 후행 지표 분류. (5) 문제 하나를 선택하고 데이터를 심층 분석.

자세한 사례 연구: Ben Yoskovitz의 [Are You Tracking the Right Metrics?](https://www.productcompass.pm/p/are-you-tracking-the-right-metrics)

### 지시문

1. **지표 프레임워크 정의** — 지표를 다음 레이어로 구성:

   **North Star Metric**: 핵심 가치 전달을 가장 잘 나타내는 단일 지표

   **Input Metrics** (3–5개): North Star를 움직이는 레버

   **Health Metrics**: 전반적인 제품 건강성을 보장하는 가드레일

   **Business Metrics**: 매출, 비용, 유닛 이코노믹스

2. **각 지표에 대해 정의**:

   | Metric | 정의 | 데이터 소스 | 시각화 | 목표값 | 알림 임계값 |
   |---|---|---|---|---|---|
   | [이름] | [정확한 계산식: 분자/분모, 시간 범위] | [데이터 출처] | [Line chart / Bar / Number / Funnel] | [목표값] | [알림 발생 조건] |

3. **대시보드 레이아웃 설계**:

   ```
   ┌─────────────────────────────────────────────┐
   │  NORTH STAR: [Metric] — [Current Value]     │
   │  Trend: [↑/↓ X% vs last period]             │
   ├──────────────────┬──────────────────────────┤
   │  Input Metric 1  │  Input Metric 2          │
   │  [Sparkline]     │  [Sparkline]             │
   ├──────────────────┼──────────────────────────┤
   │  Input Metric 3  │  Input Metric 4          │
   │  [Sparkline]     │  [Sparkline]             │
   ├──────────────────┴──────────────────────────┤
   │  HEALTH: [Latency] [Error Rate] [NPS]       │
   ├─────────────────────────────────────────────┤
   │  BUSINESS: [MRR] [CAC] [LTV] [Churn]        │
   └─────────────────────────────────────────────┘
   ```

4. **검토 주기 설정**:
   - **매일**: 운영 건강성 (오류, 지연, 핵심 플로우)
   - **매주**: Input 지표 및 참여 트렌드
   - **매월**: North Star, 비즈니스 지표, OKR 진행 상황
   - **분기별**: 전략적 검토 및 지표 재조정

5. **알림 정의**:
   - 어떤 임계값에서 조사를 시작할 것인가?
   - 누가, 어떤 채널을 통해 알림을 받는가?
   - 예상 대응 시간은 얼마인가?

6. **사용자 컨텍스트에 맞는 도구 추천**:
   - Amplitude, Mixpanel, PostHog — 제품 분석
   - Looker, Metabase, Mode — SQL 기반 대시보드
   - Datadog, Grafana — 운영 건강성 모니터링

단계적으로 생각하세요. 대시보드 명세서를 마크다운 문서로 저장하세요.

---

### 추가 자료

- [The Ultimate List of Product Metrics](https://www.productcompass.pm/p/the-ultimate-list-of-product-metrics)
- [The North Star Framework 101](https://www.productcompass.pm/p/the-north-star-framework-101)
- [The Product Analytics Playbook: AARRR, HEART, Cohorts & Funnels for PMs](https://www.productcompass.pm/p/the-product-analytics-playbook-aarrr)
- [AARRR (Pirate) Metrics: The 5-Stage Framework for Growth](https://www.productcompass.pm/p/aarrr-pirate-metrics)
- [The Google HEART Framework: Your Guide to Measuring User-Centric Success](https://www.productcompass.pm/p/the-google-heart-framework)
- [Funnel Analysis 101: How to Track and Optimize Your User Journey](https://www.productcompass.pm/p/funnel-analysis)
- [Are You Tracking the Right Metrics?](https://www.productcompass.pm/p/are-you-tracking-the-right-metrics)
- [Continuous Product Discovery Masterclass (CPDM)](https://www.productcompass.pm/p/cpdm) (video course)
