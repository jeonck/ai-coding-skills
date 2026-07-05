---
title: "실전 사례"
cascade:
  type: docs
sidebar:
  open: true
---

## 이 섹션은 무엇이 다른가

[생산성 로드맵](../docs/)이 "왜, 무엇을"을 설명하고 [실습(Labs)](../labs/)이 "따라 하며 배우는" 과정이라면, 이 **실전 사례** 섹션은 그 둘을 건너뛰고 **지금 바로 복사해서 써먹을 수 있는 한 줄 명령**만 모아둔 치트시트입니다.

{{< callout type="warning" >}}
**전제: 어떤 스킬도 미리 설치되어 있지 않은 상태**를 기준으로 작성되어 있습니다. 그래서 명령문 안에 특정 스킬 이름을 부르는 표현("~스킬로 해줘")은 쓰지 않습니다 — 대신 에이전트가 그 자리에서 바로 이해하고 수행할 수 있도록, 하고 싶은 작업을 그대로 자연어로 풀어씁니다. 같은 작업을 반복해서 쓴다면, 이 문장 자체를 [스킬로 저장](../docs/foundations/what-is-skill/)해두고 다음부터는 이름만 불러도 됩니다.
{{< /callout >}}

각 사례는 다음 형식으로 고정되어 있습니다.

1. **한 줄 명령** — 코드 블록으로 제공되어, 오른쪽 위 복사 아이콘 클릭 한 번으로 바로 붙여넣을 수 있는 자연어 지시문 (스킬 미설치 상태에서도 그대로 동작)
2. **무엇이 일어나는가** — 이 한 줄 뒤에서 에이전트가 실제로 수행하는 작업
3. **사전 조건** — 이 명령이 안전하게 동작하기 위해 미리 갖춰야 할 것
4. **더 깊이 알아보기** — 원리를 자세히 알고 싶을 때 이어질 로드맵/실습 링크

{{< callout type="info" >}}
새로운 실전 사례를 발견할 때마다 이 섹션에 계속 추가합니다. 특정 사례가 왜 동작하는지 원리부터 이해하고 싶다면 [생산성 로드맵](../docs/)을 먼저 참고하세요.
{{< /callout >}}

## 사례 목록

{{< cards >}}
  {{< card link="clone-site-in-one-line" title="사이트 디자인 한 번에 클론 코딩" subtitle="URL 하나로 구조·스타일을 분석해 코드로 재현" icon="template" >}}
  {{< card link="clone-with-website-cloner-template" title="GitHub 템플릿으로 실제 사이트 통째로 클론하기" subtitle="실제 경험담 — Stripe.com 클론, 17분 38초" icon="duplicate" >}}
  {{< card link="vibesec-owasp-fix" title="VibeSec-Skill로 OWASP 취약점 해소" subtitle="정적 분석 → 분류 → 자동 수정을 한 번에" icon="shield-check" >}}
  {{< card link="scaffold-new-kb-site" title="Hugo+Hextra 지식베이스 한 번에 스캐폴딩" subtitle="이 사이트 자체가 이 스킬로 만들어졌습니다" icon="collection" >}}
  {{< card link="auto-pr-review-hook" title="PR 생성 시 자동 코드 리뷰" subtitle="사람이 열기도 전에 1차 리뷰가 끝나있게" icon="clipboard-check" >}}
  {{< card link="one-click-pages-deploy" title="저장소 생성부터 배포까지 한 번에" subtitle="Pages 소스 설정, 워크플로우 확인까지 포함" icon="lightning-bolt" >}}
  {{< card link="test-gen-on-diff" title="변경분 테스트 자동 생성" subtitle="수정 전 코드로 돌리면 실패하는 테스트부터" icon="beaker" >}}
{{< /cards >}}
