# 시험

> 시험 문제는 강의 노트 본문과 분리해 관리한다.

## Q1 — LangGraph 실행 흐름 연결
**정답: ③ `add_edge()`**

## Q2 — `create_agent` 동작에 가장 영향이 적은 인자
**정답: ④ `debug`**

## Q3 — `@tool` 함수의 docstring 역할
**정답: ②**  
LLM이 Tool의 용도와 적용 범위를 판단하는 핵심 설명으로 사용된다.

## Q4 — Embedding Model 변경
**정답: ②**  
임베딩 모델을 변경하면 전체 문서를 새 모델로 재임베딩한다.

## Q5 — PRD 분석 Sub-Agent
**정답: ② `ask_planner`**

## Q6 — 상태 변경 + 다음 노드 이동
**정답: ③ `Command`**

```python
Command(update={"status": "done"}, goto="next_node")
```

## Q7 — Retriever 결과를 문서 1개로 제한
**정답: ③**

```python
vector_store.as_retriever(search_kwargs={"k": 1})
```

## Q8 — Sub-Agent 최종 응답 추출
**정답: ②**

```python
result["messages"][-1].content
```

Python에서 `[-1]`은 마지막 요소다.

## Q9 — `ToolStrategy(ProductReviewList)`
**정답: ②**  
LLM 응답을 지정한 스키마에 맞는 구조화된 데이터로 생성한다.

```python
rating: int | None = Field(ge=1, le=5)
```

정수라면 1 이상 5 이하이며 `None`도 허용한다.

## Q10 — LlamaCpp GPU Offloading
**정답: ④ `n_gpu_layers=-1`**
