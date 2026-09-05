# Context

## Context Window

LLM이 한 번의 요청에서 참고할 수 있는 정보량의 한계다.

`1M context window`는 약 100만 토큰까지 넣을 수 있다는 뜻이지, **100만 토큰 전체를 동일한 품질로 기억하고 활용한다는 뜻은 아니다.**

## Lost in the Middle

긴 컨텍스트에서 **중간에 위치한 정보를 상대적으로 놓치기 쉬운 현상**이다.

따라서 컨텍스트가 크다고 모든 자료를 무조건 넣는 것이 좋은 전략은 아니다.

## Context Engineering

LLM/Agent가 현재 작업을 잘 수행하도록 컨텍스트 윈도우 안에 **어떤 정보를 넣고, 유지하고, 요약하고, 검색해 추가하고, 버릴지 설계하는 것**이다.

대상 예:
- System Prompt
- 이전 대화
- RAG 검색 결과
- Tool 실행 결과
- Memory
- 작업 상태
- 이전 작업 요약

> **Context Window = 책상 크기**  
> **Context Engineering = 그 책상 위에 필요한 자료를 잘 배치하는 기술**

넓게 보면 Harness Engineering의 핵심 하위 영역으로 볼 수 있다.
