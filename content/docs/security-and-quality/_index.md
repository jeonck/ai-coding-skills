---
title: "③ 보안·품질 스킬"
weight: 3
---

빠르게 생성한 코드는 빠르게 취약점도 함께 생성합니다. 이 섹션은 "VibeSec-Skill로 OWASP 관점 보안 취약점 해소"처럼, 코드가 만들어진 직후 한 줄 명령으로 보안·품질을 점검하고 고치는 스킬을 다룹니다.

{{< callout type="warning" >}}
자동 수정 스킬은 편리하지만 맹신하면 안 됩니다. 자동으로 고친 취약점이라도 반드시 사람이 diff를 확인하고, 특히 인증·권한·암호화처럼 되돌리기 어려운 영역은 별도로 검토해야 합니다.
{{< /callout >}}

## 이 섹션에서 다루는 내용

1. **VibeSec-Skill로 OWASP 취약점 해소** — OWASP Top 10 관점의 자동 점검·수정 스킬
2. **자동 코드 리뷰 스킬 설계** — PR 단위로 반복되는 리뷰 관점을 스킬로 고정하기
3. **테스트 자동 생성** — 변경분에 대한 테스트 케이스를 스킬로 생성하기

{{< cards >}}
  {{< card link="vibesec-owasp" title="VibeSec-Skill로 OWASP 취약점 해소" subtitle="OWASP Top 10 관점의 자동 점검·수정 스킬" >}}
  {{< card link="auto-code-review" title="자동 코드 리뷰 스킬 설계" subtitle="PR 단위로 반복되는 리뷰 관점을 스킬로 고정하기" >}}
  {{< card link="test-generation" title="테스트 자동 생성" subtitle="변경분에 대한 테스트 케이스를 스킬로 생성하기" >}}
{{< /cards >}}

{{< callout type="info" >}}
개별 스킬을 익혔다면, 이 스킬들을 커밋·PR 이벤트에 자동으로 연결하는 방법을 [오케스트레이션·자동화](../orchestration/)에서 다룹니다.
{{< /callout >}}
