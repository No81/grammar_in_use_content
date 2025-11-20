# Unit Format Conversion Task

## 문제 상황
Unit 7-15의 YAML 파일이 잘못된 형식(`content` 마크다운)으로 작성되어 viewer.html에서 오류 발생:
```
undefined is not an object (evaluating 'section.items.forEach')
```

## 완료된 작업

### 1. viewer.html 수정 (임시 해결책)
- marked.js 라이브러리 추가
- 마크다운 콘텐츠 렌더링 지원
- **주의**: 이 방식은 정답 숨기기 기능이 없어 학습 효과 감소

### 2. 에이전트 업데이트
- `content-creator.md`: CRITICAL FORMAT WARNING 추가
- `content-reviewer.md`: 형식 검사 항목 추가

### 3. Unit 7 변환 완료
- `units/unit7-simple-present-questions.yaml`
- `content` 마크다운 → `items` 배열 형식으로 변환
- 컨텐츠 내용은 100% 보존

## 남은 작업 (8개 유닛)

다음 유닛들을 `items` 배열 형식으로 변환 필요:

- [ ] `unit8-present-continuous-vs-simple-present.yaml`
- [ ] `unit9-have-and-have-got.yaml`
- [ ] `unit10-was-were.yaml`
- [ ] `unit11-worked-got-went-simple-past.yaml`
- [ ] `unit12-simple-past-negative-and-questions.yaml`
- [ ] `unit13-i-was-doing-past-continuous.yaml`
- [ ] `unit14-past-continuous-and-simple-past.yaml`
- [ ] `unit15-i-used-to.yaml`

## 변환 규칙

### 잘못된 형식 (현재 Unit 8-15)
```yaml
sections:
  - id: 1
    title: "섹션 제목"
    content: |
      # 마크다운 콘텐츠
      - 리스트 항목
      ## 정답:
      1. 답1
```

### 올바른 형식 (변환 목표)
```yaml
sections:
  - title: "1. 섹션 제목"
    items:
      - type: text
        content: "설명 텍스트"
      - type: list
        heading: "리스트 제목"
        list:
          - "항목 1"
          - "항목 2"
      - type: qna
        question: "질문?"
        answer: "정답과 설명"
      - type: note
        content: "노트 내용"
```

## 변환 시 주의사항

1. **컨텐츠 100% 보존** - 내용 수정 금지, 구조만 변환
2. **정답 분리** - 마크다운의 "정답:" 섹션을 각 qna의 answer로 분리
3. **섹션 제목 형식** - "1. 핵심 개념 정리" 형태로 번호 포함
4. **10개 섹션 구조** 유지:
   - 1. 핵심 개념 정리
   - 2. Noticing 활동
   - 3. 회상 연습 (Retrieval Practice)
   - 4. 기초 연습 - 빈칸 채우기
   - 5. 문장 만들기 - 번역
   - 6. 변형 연습
   - 7. 실생활 적용
   - 8. 종합 문제
   - 9. 내일 복습용 문제 (Spaced Repetition Review)
   - 10. 자기 점검 & 격려

## 참고 파일

- 변환 완료 예시: `units/unit7-simple-present-questions.yaml`
- 기존 올바른 형식: `units/unit6-simple-present-negative.yaml`

## 테스트 방법

```bash
npx http-server -p 8080
```
http://127.0.0.1:8080 에서 각 유닛 클릭하여 정상 표시 확인
