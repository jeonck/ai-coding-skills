---
title: "정적분석·보안 스캐너"
weight: 2
---

## Semgrep

- **링크**: https://semgrep.dev/
- **설명**: 패턴 기반 정적 분석(SAST) 도구. OWASP Top 10 규칙셋을 기본 제공해 [VibeSec-Skill로 OWASP 취약점 해소](../../docs/security-and-quality/vibesec-owasp/)류의 스킬 내부 엔진으로 자주 쓰입니다.
- **설치**: `pip install semgrep`

## CodeQL

- **링크**: https://codeql.github.com/
- **설명**: GitHub이 제공하는 시맨틱 코드 분석 엔진. 데이터 흐름을 추적해 더 깊은 인젝션·권한 관련 취약점을 탐지합니다.
- **설치**: `gh extension install github/gh-codeql`

## Trivy

- **링크**: https://trivy.dev/
- **설명**: 컨테이너 이미지·의존성·IaC 설정의 취약점을 스캔하는 도구. 공급망(SCA) 관점 점검에 사용됩니다.
- **설치**: `brew install trivy`
