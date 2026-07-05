---
title: "GitHub 템플릿으로 실제 사이트 통째로 클론하기"
weight: 2
---

[사이트 디자인 한 번에 클론 코딩](../clone-site-in-one-line/)이 매번 처음부터 DOM·스타일을 분석하는 방식이라면, 이 사례는 클로닝 전용으로 미리 만들어둔 **GitHub 템플릿 저장소**를 뼈대로 삼아 훨씬 빠르고 완성도 높게 결과물을 뽑아내는 실제 사용 경험입니다.

## 한 줄 명령

오른쪽 위 복사 아이콘을 눌러 그대로 붙여넣으세요. `{특정사이트: stripe.com}`의 `stripe.com` 부분만 원하는 대상 사이트로 바꾸면 됩니다. 별도의 스킬이 설치되어 있지 않아도 이 문장 그대로 동작합니다.

```text
깃헙의 ai-website-cloner-template 을 활용해서 {특정사이트: stripe.com} 사이트를 clone 해줘
```

## 결과 예시

실제로 이 한 줄 명령으로 받은 결과입니다 (Stripe.com 클론, 소요 시간 약 17분 38초).

> stripe.com 클론이 완성됐습니다. http://localhost:3000 에서 확인할 수 있습니다.

구현된 내용 요약:

| 섹션 | 특징 |
|---|---|
| Navigation | sticky + scroll 시 blur/shadow 효과, 모바일 메뉴 |
| Hero | Canvas 애니메이션 그래디언트(orange/purple/pink), GDP 실시간 카운터 |
| LogoBar | OpenAI·Amazon·NVIDIA 등 무한 마퀴 스크롤 |
| Flexible Solutions | 6개 탭 전환(Payments/Billing/Issuing/Connect/Crypto/Treasury), UI 미리보기 카드 |
| Stats | 450+/1%/>195+/100+ 뷰포트 진입 시 count-up 애니메이션 |
| Business Sections | Startup 프로그램, Enterprise, SaaS 플랫폼 |
| Developer | 다크 테마 + 실제 curl/JSON 코드 블록 |
| CTA + Footer | 국가 선택 버튼, 전체 링크 트리 |

기술 스택: Next.js 16 · React 19 · TypeScript strict · Tailwind CSS v4 · Inter 폰트(sohne-var 대체) · Stripe 색상 토큰(`#533afd`, `#061b31`)

## 무엇이 일어나는가

1. 클로닝 전용 템플릿 저장소를 받아 프로젝트 뼈대(Next.js + Tailwind 등 표준 스택)를 그대로 활용
2. 대상 URL의 실제 섹션 구조와 인터랙션(스크롤 애니메이션, 탭 전환, count-up 등)을 분석
3. 템플릿이 이미 제공하는 컴포넌트 패턴에 맞춰 섹션(Navigation/Hero/LogoBar/…)을 채워 넣기
4. 브랜드 색상 토큰·폰트를 대상 사이트에 맞게 교체
5. 로컬 개발 서버로 즉시 확인 (`localhost:3000`)

{{< callout type="info" >}}
매번 DOM을 처음부터 분석하는 [사이트 디자인 한 번에 클론 코딩](../clone-site-in-one-line/)과 달리, 이 방식은 이미 검증된 애니메이션·레이아웃 패턴(마퀴 스크롤, count-up, sticky nav 등)을 템플릿에서 그대로 재사용하기 때문에 완성도와 속도 모두 크게 올라갑니다. 클로닝을 자주 한다면 이런 템플릿 저장소를 직접 만들어 축적해두는 것 자체가 [보일러플레이트/스캐폴딩 자동 생성](../../docs/clone-and-scaffold/scaffold-boilerplate/) 패턴입니다.
{{< /callout >}}

## 사전 조건

- Node.js/Next.js 로컬 개발 환경
- 클론 대상이 본인 소유이거나 학습·데모 목적임이 명확할 것 — 브랜드 색상 토큰·폰트·로고 등 상표 자산을 상업적으로 재배포하지 않을 것
- 템플릿 저장소에 대한 접근 권한 (공개 저장소라면 별도 설정 불필요)

{{< callout type="warning" >}}
결과가 빠르고 완성도 있게 나올수록, "원본과 얼마나 똑같은가"보다 "저작권·상표를 침해하지 않는 선"을 지켰는지 검토하는 것을 잊기 쉽습니다. 실제 배포 전에는 항상 사람이 직접 확인하세요.
{{< /callout >}}

## 더 깊이 알아보기

- 원리: [클론·생성 스킬](../../docs/clone-and-scaffold/clone-site-design/)
- 함께 보기: [사이트 디자인 한 번에 클론 코딩](../clone-site-in-one-line/) — 템플릿 없이 처음부터 분석하는 방식
- 직접 따라 하기: [Lab 1: 사이트 클론 코딩 스킬 만들기](../../labs/lab1-clone-skill/)
