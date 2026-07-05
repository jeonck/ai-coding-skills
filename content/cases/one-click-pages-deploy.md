---
title: "저장소 생성부터 배포까지 한 번에"
weight: 5
---

## 한 줄 명령

오른쪽 위 복사 아이콘을 눌러 그대로 붙여넣으세요.

```text
이 프로젝트로 GitHub 저장소 만들고 GitHub Pages까지 배포해줘
```

## 무엇이 일어나는가

1. 원격 저장소 생성 (이름·공개 범위는 실행 전 확인)
2. 초기 커밋·푸시
3. Pages 소스를 GitHub Actions로 설정
4. CI 워크플로우가 빌드·배포를 자동 수행
5. 배포된 URL에 실제로 접속해 정상 렌더링 확인

## 사전 조건

- `gh auth status`로 GitHub CLI 인증 확인
- 빌드 도구(Hugo 등) 버전이 워크플로우 파일에 고정되어 있을 것
- 워크플로우 `permissions`가 필요한 범위로 최소화되어 있을 것

## 더 깊이 알아보기

- 원리: [한 줄 명령으로 GitHub Pages/Vercel 배포](../../docs/deploy-and-ops/one-click-deploy/)
- 직접 따라 하기: [Lab 3: 훅으로 배포 파이프라인 자동화하기](../../labs/lab3-deploy-hook/)
- 배포 후 확인: [배포 후 모니터링·알림 자동화](../../docs/deploy-and-ops/monitoring-hook/)
