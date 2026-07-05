---
title: 생산성 로드맵
linkTitle: 생산성 로드맵
cascade:
  type: docs
sidebar:
  open: true
---

## AI 코딩 생산성 스킬, 어떻게 쌓아가야 할까

"사이트 디자인 한 번에 클론 코딩", "VibeSec-Skill로 OWASP 취약점 해소"처럼 **한 줄 명령으로 품질과 안정성을 함께 끌어올리는 AI 코딩 기법**이 매주 새로 등장하고 있습니다. 문제는 각자 흩어진 채로 한 번 쓰고 잊혀진다는 것 — 이 로드맵은 이런 기법을 **5개의 스킬 축**과 **하나의 거버넌스 축**으로 나눠 쌓고, 검색해서 재사용할 수 있게 합니다.

1. **[기반 개념](foundations)** — 스킬·서브에이전트·훅·MCP 개념과 한 줄 명령이 동작하는 원리
2. **[클론·생성 스킬](clone-and-scaffold)** — 사이트/디자인 클론 코딩, 스캐폴딩, 디자인→코드 자동화
3. **[보안·품질 스킬](security-and-quality)** — OWASP 취약점 자동 해소, 코드 리뷰, 테스트 생성 자동화
4. **[오케스트레이션·자동화](orchestration)** — 멀티에이전트 병렬화, 훅, MCP 연동
5. **[배포·운영 스킬](deploy-and-ops)** — 한 줄 배포, CI/CD, 모니터링 자동화
6. **[실전 사례·거버넌스](practice-and-governance)** — 스킬 축적 전략, 팀 도입, 안전장치

{{< callout type="info" >}}
**추천 학습 순서: 1 → 2 → 3 → 4 → 5 → 6**

먼저 "스킬이 왜 프롬프트보다 강력한가"라는 원리(①)를 이해해야, 클론 코딩(②)이나 보안 자동화(③) 같은 개별 스킬을 볼 때 "이게 왜 한 줄로 되는지"가 보입니다. ④에서 여러 스킬을 조합·병렬화하는 법을 배운 뒤, ⑤에서 결과물을 실제로 내보내고, 마지막 ⑥에서 이 모든 걸 팀 단위로 안전하게 축적하는 법을 다룹니다.
{{< /callout >}}

## 배경별 추천 진입점

{{< cards >}}
  {{< card link="foundations/what-is-skill" title="스킬을 처음 써보는 개발자" subtitle="① 기반 개념부터 순서대로" icon="academic-cap" >}}
  {{< card link="clone-and-scaffold/clone-site-design" title="프런트엔드·풀스택 개발자" subtitle="② 클론·생성 스킬로 바로 진입" icon="template" >}}
  {{< card link="security-and-quality/vibesec-owasp" title="시큐리티/AppSec 엔지니어" subtitle="③ 보안·품질 스킬부터" icon="shield-check" >}}
  {{< card link="orchestration/multi-agent-parallel" title="AI 에이전트 플랫폼 팀" subtitle="④ 오케스트레이션·자동화부터" icon="cog" >}}
{{< /cards >}}

## 4주 학습 플랜

| 주차 | 내용 |
|---|---|
| 1주차 | 기반 개념 — 스킬/서브에이전트/훅/MCP 용어와 원리 정리 |
| 2주차 | 클론·생성 스킬 + 보안·품질 스킬 3~4개를 직접 만들어보기 |
| 3주차 | 오케스트레이션·자동화 — 여러 스킬을 훅/멀티에이전트로 연결 |
| 4주차 | 배포·운영 스킬 적용 + 팀 거버넌스 규칙 수립 |

자세한 실습 가이드는 [실습 (Labs)](../labs/) 섹션을 참고하세요.

## 전체 섹션

{{< cards >}}
  {{< card link="foundations" title="① 기반 개념" subtitle="스킬·서브에이전트·훅·MCP — 한 줄 명령이 실제로 동작하는 원리" icon="light-bulb" >}}
  {{< card link="clone-and-scaffold" title="② 클론·생성 스킬" subtitle="사이트 디자인 클론 코딩, 스캐폴딩, 디자인→코드 자동화 스킬" icon="template" >}}
  {{< card link="security-and-quality" title="③ 보안·품질 스킬" subtitle="VibeSec-Skill류의 OWASP 취약점 해소, 자동 코드 리뷰, 테스트 생성" icon="shield-check" >}}
  {{< card link="orchestration" title="④ 오케스트레이션·자동화" subtitle="멀티에이전트 병렬화, 훅 자동화, MCP 연동" icon="cog" >}}
  {{< card link="deploy-and-ops" title="⑤ 배포·운영 스킬" subtitle="한 줄 배포, CI/CD 자동 구성, 배포 후 모니터링" icon="rocket-launch" >}}
  {{< card link="practice-and-governance" title="⑥ 실전 사례·거버넌스" subtitle="스킬 축적·버전관리, 팀 도입 전략, 안전장치와 리스크 관리" icon="academic-cap" >}}
{{< /cards >}}
