---
title: "VibeSec-Skill로 OWASP 취약점 해소"
weight: 2
---

## 한 줄 명령

오른쪽 위 복사 아이콘을 눌러 그대로 붙여넣으세요.

```text
VibeSec-Skill로 이 PR의 OWASP 관점 취약점 점검하고 고쳐줘
```

## 무엇이 일어나는가

1. Semgrep/CodeQL 등으로 정적 분석(SAST) 실행
2. 발견된 이슈를 OWASP Top 10 카테고리로 분류
3. 심각도와 실제 도달 가능성 기준으로 우선순위화
4. 파라미터 바인딩, 이스케이프 등 안전한 패턴으로 자동 수정 제안
5. 수정 후 기존 테스트가 여전히 통과하는지 회귀 확인

## 사전 조건

- 정적 분석 도구(Semgrep 등) 설치
- 자동 수정 결과를 반드시 사람이 diff로 검토할 것 — 특히 인증·권한·암호화 영역

## 더 깊이 알아보기

- 원리: [VibeSec-Skill로 OWASP 취약점 해소](../../docs/security-and-quality/vibesec-owasp/)
- 직접 따라 하기: [Lab 2: VibeSec 스타일 OWASP 점검 스킬 만들기](../../labs/lab2-vibesec-skill/)
- 도구: [정적분석·보안 스캐너](../../tools/security-scanners/)
