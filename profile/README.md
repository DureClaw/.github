<div align="center">

![DureClaw](https://raw.githubusercontent.com/DureClaw/.github/main/profile/assets/hero.png)

# DureClaw

**분산 디바이스를 하나의 협력 AI 크루로 — 두뇌는 분산, 결정은 사람**
_Turn scattered devices into one collaborating AI crew — distributed brains, human decisions_

</div>

---

여러 머신(엣지 Pi · GPU · Windows · Mac)을 **하나의 실시간 채널로 묶어** 협동하는 AI 에이전트 인프라를 만듭니다.
LLM 호출은 마스터가 흡수해 엣지는 **키·비용 0**, 승인된 판단은 **결정론적 룰로 컴파일**해 재사용합니다.

> We build infrastructure that joins many machines (edge Pi · GPU · Windows · Mac) on **one real-time channel** to collaborate as an AI crew.
> The master absorbs LLM calls (so edges stay **keyless, zero-cost**), and approved judgments are **compiled into deterministic rules** for reuse.

---

## 프로젝트 / Projects

| Repo | 무엇 / What | |
|------|------------|---|
| **[dureclaw](https://github.com/DureClaw/dureclaw)** | 분산 에이전트 협력 버스 (Phoenix Channel) — 멀티머신 에이전트 팀을 WebSocket 한 채널로 오케스트레이션. Claude Code 플러그인. | `multi-agent` `orchestration` |
| **[dure-factory-public](https://github.com/DureClaw/dure-factory-public)** | 분산 엣지 × 제조 MES 데모 — 흩어진 공장 장비를 한 버스로 묶어 *센싱 → 종합 → 승인 → 결정 동결*. DureClaw + [Open MES Korea](https://github.com/baryonlabs/open-mes-korea). | `edge` `manufacturing` |

---

## 어떻게 동작하나 / How it works

```
[흩어진 디바이스]            [협력 버스]              [마스터 브레인]         [사람]
 센서·GPU·PC ──── one line ──▶ DureClaw ──fan-out──▶ Claude (종합·제안) ──▶ 승인 · 결정 동결
   (keyless)                  presence·task                                      ↓
        └────────── 닫힌 학습 루프: 승인된 결정을 룰로 컴파일 → µs 재사용 (LLM 0회) ──────────┘
```

1. **센싱** — 흩어진 노드가 키 없이 한 줄로 버스에 합류, 자기 역할을 관측
2. **종합** — 마스터(Claude)가 fan-in 수집해 추론·**제안** (직접 실행 0)
3. **승인** — 사람이 검토·사인
4. **결정 동결 (LLM as compiler)** — 승인된 판단을 결정론적 룰로 → 같은 문제는 **LLM 0회**로 µs 재사용

---

## 원칙 / Principles

**데이터는 엣지 · 두뇌는 분산 · 학습은 닫힌 루프 · 결정은 사람**
_Data at the edge · brains distributed · learning in a closed loop · humans decide_

<div align="center">
<sub>DureClaw · distributed AI agent crew orchestration</sub>
</div>
