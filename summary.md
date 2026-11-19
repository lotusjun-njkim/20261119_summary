## 실무 예시로 전체 흐름 파악
**사용자** : 한 직원이 업무의 요청을 묻는 경우<br>
**FastAPI** : 인증과 입력을 받고 기록한다.<br>
**Context** : 최근 대화와 기존 통과했던 문구를 고른다.<br>
**Prompt** : 시스템 규칙, 조문 질문을 템플릿에 채운다.<br>
**PostgreSQL** : 요청한 내용을 DB 적재를 한다<br>
**Embedding**: parsing-cleaning-chunking-validate-retriever 한다.<br>
**LLM client**: 에 호출하여 출력과 재시도를 한다.<br> 
**출력검사**: 근거검토를 하여 답변과 실제 chunk에서 나왔는 지 대조하여 사유를 기록한다.<br>
**응답** : 답변과 출처 근거 사유를 기록한다.<br>