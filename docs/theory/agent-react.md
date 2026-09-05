# Agent와 ReAct

## ReAct

**Reasoning + Acting**

Agent가 단순히 한 번에 답하지 않고 다음 루프를 반복한다.

```text
생각 → Tool 실행 → 결과 관찰 → 다시 생각 → Tool 실행 → ... → 답변
```

예: 장애 분석

```text
장애 발생
→ 로그 확인 필요
→ 로그 Tool 호출
→ DB timeout 발견
→ DB metric 확인
→ 최근 배포 확인
→ 원인 가설 생성
```

## Context Engineering과의 관계

ReAct 루프가 반복될수록 Tool 결과와 상태가 계속 쌓이므로, 어떤 정보를 유지·압축·삭제할지 관리하는 Context Engineering이 중요하다.
