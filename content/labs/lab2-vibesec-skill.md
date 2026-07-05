---
title: "Lab 2: VibeSec 스타일 OWASP 점검 스킬 만들기"
weight: 2
---

## 목표

작은 샘플 웹 애플리케이션에 의도적으로 삽입된 취약점을, 정적 분석 → OWASP 카테고리 분류 → 자동 수정 절차를 담은 스킬로 탐지하고 고칩니다.

## 사전 준비

- Semgrep (오픈소스 정적 분석 도구)
- 취약점이 포함된 샘플 코드 (직접 작성하거나 OWASP 공식 취약 웹앱 예제 사용)

```bash
pip install semgrep
```

## 단계별 실행

### 1. 의도적으로 취약한 샘플 작성

```python
# vulnerable.py
import sqlite3

def get_user(username):
    conn = sqlite3.connect("app.db")
    query = "SELECT * FROM users WHERE username = '" + username + "'"
    return conn.execute(query).fetchall()
```

### 2. 정적 분석 실행 및 OWASP 매핑

```bash
semgrep --config p/owasp-top-ten vulnerable.py
```

출력된 각 결과를 A03(Injection) 같은 OWASP 카테고리로 분류하고, 심각도 순으로 정렬합니다.

## 결과 확인

Semgrep이 문자열 결합 SQL 쿼리를 injection 위험으로 표시하는지 확인합니다. 이후 파라미터 바인딩으로 교체한 뒤 다시 스캔해 해당 경고가 사라지는지 확인합니다.

```python
def get_user(username):
    conn = sqlite3.connect("app.db")
    return conn.execute(
        "SELECT * FROM users WHERE username = ?", (username,)
    ).fetchall()
```

## 체크리스트

- [ ] 최소 1개의 OWASP Top 10 카테고리 취약점을 의도적으로 삽입하고 탐지했다
- [ ] 자동 수정 전/후로 스캔을 다시 돌려 경고가 해소됐음을 확인했다
- [ ] 수정된 코드에 대한 회귀 테스트를 작성했다
