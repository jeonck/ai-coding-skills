---
title: "Hugo+Hextra 지식베이스 한 번에 스캐폴딩"
weight: 4
---

## 한 줄 명령

오른쪽 위 복사 아이콘을 눌러 그대로 붙여넣으세요. `(새 주제)` 부분만 원하는 주제로 바꾸면, 별도 스킬 없이도 바로 동작합니다.

```text
Hugo와 Hextra 테마로 '(새 주제)' 지식베이스 사이트를 만들어줘. 홈/로드맵/실습/도구/용어집 구조로 구성하고, GitHub 저장소를 새로 만들어서 GitHub Pages로 배포까지 해줘
```

## 무엇이 일어나는가

1. Hugo 프로젝트 초기화 + Hextra 테마 submodule 추가
2. 홈/로드맵/실습/도구/블로그/용어집 템플릿을 새 주제에 맞게 채워 넣기
3. 좌측 사이드바 토글, 검색(flexsearch), 용어집 숏코드 등 표준 기능 적용
4. GitHub 저장소 생성 → 초기 커밋/푸시 → Pages를 GitHub Actions 소스로 설정
5. 로컬 빌드로 깨진 링크·렌더링 문제를 먼저 확인한 뒤 배포

{{< callout type="warning" >}}
이 사이트 자체가 바로 위 문장을 반복 실행해 다듬은 뒤 `hextra-roadmap-kb`라는 스킬로 저장한 결과물입니다 — 한 번 스킬로 저장해두면, 완전히 다른 주제의 지식베이스도 이름만 불러 몇 시간 안에 배포까지 끝낼 수 있습니다.
{{< /callout >}}

## 사전 조건

- Hugo Extended, git, GitHub CLI(`gh`) 설치 및 인증
- 저장소 이름·공개 범위는 실행 전 반드시 사람이 확인

## 더 깊이 알아보기

- 원리: [보일러플레이트/스캐폴딩 자동 생성](../../docs/clone-and-scaffold/scaffold-boilerplate/)
- 배포 절차: [한 줄 명령으로 GitHub Pages/Vercel 배포](../../docs/deploy-and-ops/one-click-deploy/)
