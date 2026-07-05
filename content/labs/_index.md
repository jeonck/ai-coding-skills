---
title: "실습 (Hands-on Labs)"
cascade:
  type: docs
sidebar:
  open: true
---

## 이 섹션은 무엇이 다른가

[생산성 로드맵](../docs/)은 AI 코딩 생산성 스킬의 개념과 원리를 체계적으로 설명합니다. 반면 이 **실습(Labs)** 섹션은 **그대로 따라 하면 재현되는, 단계별로 실행 가능한 실습 가이드**만 담습니다. 각 실습은 다음과 같은 동일한 구조를 따릅니다.

1. **목표** — 이 실습을 통해 무엇을 만들고 확인하는가
2. **사전 준비** — 필요한 도구, 환경, 저장소
3. **단계별 실행** — 복사해서 실행할 수 있는 명령어와 스킬 정의 예시
4. **결과 확인** — 출력을 어떻게 해석하고 무엇을 기록해야 하는가
5. **체크리스트** — 실습을 완료했는지 자가 점검

{{< callout type="info" >}}
아래 실습은 Claude Code, Hugo(Extended), git, GitHub CLI(`gh`)가 설치된 환경을 기준으로 작성되었습니다.

```bash
brew install hugo gh
gh auth login
```
{{< /callout >}}

## 실습 목록

{{< cards >}}
  {{< card link="lab1-clone-skill" title="Lab 1: 사이트 클론 코딩 스킬 만들기" subtitle="대상 사이트를 분석해 코드로 재현하는 스킬 정의 작성" >}}
  {{< card link="lab2-vibesec-skill" title="Lab 2: VibeSec 스타일 OWASP 점검 스킬 만들기" subtitle="정적 분석 → 분류 → 자동 수정까지 이어지는 스킬 정의 작성" >}}
  {{< card link="lab3-deploy-hook" title="Lab 3: 훅으로 배포 파이프라인 자동화하기" subtitle="커밋 전 훅 + GitHub Actions 배포 워크플로우 연결" >}}
{{< /cards >}}

{{< callout type="warning" >}}
이 섹션의 모든 실습은 **본인이 소유하거나 명시적으로 권한을 부여받은 저장소/시스템**에서만 수행하세요. 타인의 서비스, 프로덕션 시스템에 대한 무단 클론·스캔·배포 자동화는 서비스 약관 위반 및 법적 책임을 수반할 수 있습니다.
{{< /callout >}}
