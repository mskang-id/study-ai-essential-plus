# AI Essential Plus 교육 노트

AI/LLM 학습 과정에서 질문하고 정리한 내용을 Markdown으로 관리하고, MkDocs Material로 GitHub Pages에 배포하기 위한 공개 학습 노트입니다.

## 노트 구성

- 키워드 모음
- 이론
- 실습
- 노트
- 응용
- 시험

## 공개 원칙

이 저장소는 공개 자료이므로 다음 기준으로 정리합니다.

- 개인 식별 정보는 기록하지 않습니다.
- 회사명, 사내 시스템명, 내부 URL, 실제 운영 데이터 등 비공개 정보는 기록하지 않습니다.
- 특정 조직의 실제 장애나 업무 사례는 일반적인 예제로 추상화합니다.
- 교육 자료나 시험 문제 원문을 그대로 복제하지 않고, 개념과 개인적인 이해를 중심으로 재정리합니다.
- 코드 예시는 공개 가능한 일반 예제만 사용합니다.

## 로컬 실행

```bash
python -m pip install -r requirements.txt
mkdocs serve
```

## GitHub Pages

`main` 브랜치에 push하면 GitHub Actions가 MkDocs 사이트를 빌드하고 Pages에 배포하도록 구성되어 있습니다.
