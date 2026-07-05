---
title: "Lab 3: 훅으로 배포 파이프라인 자동화하기"
weight: 3
---

## 목표

커밋 전 검증(pre-commit)과 GitHub Actions 배포 워크플로우를 연결해, "커밋 → 자동 검증 → main 푸시 → 자동 배포"가 사람의 추가 개입 없이 이어지는 구조를 만듭니다.

## 사전 준비

- Hugo(Extended) 또는 임의의 정적 사이트 생성기 프로젝트
- GitHub 저장소 (본인 소유)

```bash
gh auth status
```

## 단계별 실행

### 1. pre-commit 훅 작성

```bash
mkdir -p .git/hooks
```

```bash
# .git/hooks/pre-commit
#!/bin/sh
hugo --minify -d /tmp/build-check || {
  echo "빌드 실패 — 커밋을 중단합니다"
  exit 1
}
```

```bash
chmod +x .git/hooks/pre-commit
```

### 2. GitHub Actions 배포 워크플로우 작성

```python
# .github/workflows/deploy.yml 핵심 구조 (의사 코드)
on: push to main
permissions: contents: read, pages: write, id-token: write
jobs:
  build: hugo --minify --baseURL "<pages-url>"
  deploy: actions/deploy-pages
```

## 결과 확인

1. 의도적으로 빌드가 깨지는 변경을 만들어 커밋을 시도 — pre-commit 훅이 커밋을 막는지 확인
2. 정상 변경을 `main`에 푸시 — Actions 탭에서 build → deploy 작업이 순서대로 성공하는지 확인
3. 배포된 URL에 실제로 접속해 변경사항이 반영됐는지 확인

## 체크리스트

- [ ] 빌드가 깨지는 커밋이 pre-commit 훅에서 차단된다
- [ ] `main` 푸시 시 GitHub Actions가 자동으로 빌드·배포를 수행한다
- [ ] 워크플로우 파일의 `permissions`이 필요한 범위로 최소화되어 있다
