<div align="center">

![DureClaw](https://raw.githubusercontent.com/DureClaw/.github/main/profile/assets/hero.png)

# DureClaw

**분산 디바이스를 하나의 협력 AI 크루로 — 두뇌는 분산, 결정은 사람**
_Turn scattered devices into one collaborating AI crew — distributed brains, human decisions_

</div>

---

DureClaw는 **이미 잘 돌아가는 다플랫폼 인프라 위에** 얹혀, **에이전트(Claw)가 스스로 네트워크와 동작을 정의**하도록 돕습니다.
새 시스템으로 갈아엎지 않고, **현 인프라에서 데이터 수집·분석을 시작**해 **자동화와 AX(AI Transformation)로 가는 첫 걸음**이 됩니다.

> DureClaw sits **on top of infrastructure that already works**, letting the **agent (Claw) define its own network and behavior**.
> Without replacing anything, it's the **starting point** to begin **data collection & analysis on your existing infrastructure** — and the on-ramp to **automation and AX**.

여러 머신(엣지 Pi · GPU · Windows · Mac)을 **하나의 실시간 채널로 묶고**, LLM 호출은 마스터가 흡수해 엣지는 **키·비용 0**,
승인된 판단은 **결정론적 룰로 컴파일**해 재사용합니다. _Many machines on one channel · keyless edges · approved decisions compiled into rules._

### 시작점 → AX 여정 / From here to AX

```
[기존 인프라]  ──▶  ① 데이터 수집  ──▶  ② 분석(LLM)  ──▶  ③ 자동화(룰 컴파일)  ──▶  ④ AX
 갈아엎지 않음        collect            analyze           automate                AI transformation
   (Claw 가 네트워크·동작을 스스로 정의 — self-defining network & behavior)
```

---

## 프로젝트 / Projects

**Core — the bus**

| Repo | 무엇 / What | |
|------|------------|---|
| **[dureclaw](https://github.com/DureClaw/dureclaw)** | 분산 에이전트 협력 버스 (Phoenix Channel) — 멀티머신 에이전트 팀을 WebSocket 한 채널로 오케스트레이션. Claude Code 플러그인. | `multi-agent` `orchestration` |

**Native nodes — built bus-first (한 줄로 fleet 합류, keyless)**

| Repo | 무엇 / What | |
|------|------------|---|
| **[edgeclaw](https://github.com/DureClaw/edgeclaw)** | **OS 노드** — 단일 정적 Go 바이너리. Win·Mac·Linux·**Pi Zero(armv6)**·riscv64… 어디서나. 로컬 핸드(shell/sensor) + LLM은 마스터에 keyless 위임. **사전빌드 릴리즈 + 설치 원라이너.** | `go` `cross-platform` |
| **[webclaw](https://github.com/DureClaw/webclaw)** | **브라우저 노드** — Chrome MV3 확장. 브라우저를 fleet에 빌려준다(fetch·DOM, CORS-free, 상시). 순수 JS, 빌드 0. *assistant 아니라 node.* | `chrome-extension` `browser` |

**Adapters — 기존 도구를 fleet에 붙이는 브리지 (`dureclaw/` 동봉)**

| Repo | 원본 / Upstream | |
|------|------------|---|
| **[picoclaw](https://github.com/DureClaw/picoclaw)** · **[nanobot](https://github.com/DureClaw/nanobot)** · **[zeroclaw](https://github.com/DureClaw/zeroclaw)** · **[nullclaw](https://github.com/DureClaw/nullclaw)** | sipeed/picoclaw(Go) · HKUDS/nanobot(Py) · zeroclaw-labs(Rust) · nullclaw(Zig) — 각 repo에 `dureclaw/` 브리지를 더해 fleet에 합류 | `adapter` `bridge` |

**Demo**

| Repo | 무엇 / What | |
|------|------------|---|
| **[dure-factory-public](https://github.com/DureClaw/dure-factory-public)** | 분산 엣지 × 제조 MES 데모 — 흩어진 공장 장비를 한 버스로 묶어 *센싱 → 종합 → 승인 → 결정 동결*. DureClaw + [Open MES Korea](https://github.com/baryonlabs/open-mes-korea). | `edge` `manufacturing` |

> **edge**claw(OS) · **web**claw(브라우저) = *네이티브 노드* | pico·nano·zero·null = *기존 도구 어댑터*. 둘 다 같은 버스, 같은 keyless 위임.

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
