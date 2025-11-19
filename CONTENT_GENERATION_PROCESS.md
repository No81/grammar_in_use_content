# 📚 Grammar in Use 컨텐츠 생성 프로세스

이 문서는 curriculum 폴더의 유닛 그룹 파일을 기반으로 학습 컨텐츠를 생성하는 전체 프로세스를 설명합니다.

---

## 🎯 프로세스 개요

```
1. 커리큘럼 파일 선택
2. 컨텐츠 생성 (병렬 실행)
3. 검수 실행
4. 이슈 반영 및 수정
5. 최종 커밋
```

---

## 📁 커리큘럼 파일 구조

### 위치
```
E:\code\grammar_in_use_content\curriculum\
```

### 파일 목록 (21개 그룹)
```
01-present_units.txt                (Units 1-9)     ✅ 완료
02-past_units.txt                   (Units 10-15)
03-present-perfect_units.txt        (Units 16-19)
04-passive_units.txt                (Units 20-21)
05-verb-forms_units.txt             (Units 22-23)
06-future_units.txt                 (Units 24-26)
07-modals_units.txt                 (Units 27-34)
08-there-and-it_units.txt           (Units 35-37)
09-auxiliary-verbs_units.txt        (Units 38-41)
10-questions_units.txt              (Units 42-47)
11-reported-speech_units.txt        (Unit 48)
12-ing-and-to_units.txt             (Units 49-52)
13-go-get-do-make-have_units.txt    (Units 53-56)
14-pronouns-and-possessives_units.txt (Units 57-62)
15-a-and-the_units.txt              (Units 63-71)
16-determiners-and-pronouns_units.txt (Units 72-82)
17-adjectives-and-adverbs_units.txt (Units 83-90)
18-word-order_units.txt             (Units 91-94)
19-conjunctions-and-clauses_units.txt (Units 95-100)
20-prepositions_units.txt           (Units 101-111)
21-phrasal-verbs_units.txt          (Units 112-113)
```

---

## 📋 Step 1: 커리큘럼 파일 확인

### 명령어
```bash
# 커리큘럼 폴더 내용 확인
ls -lh E:\code\grammar_in_use_content\curriculum\

# 특정 파일 내용 읽기 (예: Past 유닛)
cat E:\code\grammar_in_use_content\curriculum\02-past_units.txt
```

### 예상 출력 예시
```
Past: Unit10 - was/were
Past: Unit11 - worked/got/went, etc. (simple past)
Past: Unit12 - I didn't . . . Did you . . . ? (simple past negative and questions)
Past: Unit13 - I was doing (past continuous)
Past: Unit14 - I was doing (past continuous) and I did (simple past)
Past: Unit15 - I used to . . .
```

---

## 📋 Step 2: 컨텐츠 생성 (병렬 실행)

### 2.1 단일 에이전트 사용 (권장)

**사용 에이전트:** `general-purpose`

```markdown
Task 프롬프트 예시:

You are the content-creator agent. Generate learning materials for all units in curriculum/02-past_units.txt

Requirements:
1. Read curriculum/02-past_units.txt to get the list of units
2. Generate YAML files for ALL units in PARALLEL (매우 중요!)
3. Save each unit as: units/unit{번호}-{slug}.yaml
   - Example: units/unit10-was-were.yaml
4. Follow the same structure as existing units (unit1-unit9)
5. Apply research-based learning principles (spaced repetition, retrieval practice, etc.)

Target learner:
- Grade: 6th grade elementary
- Native language: Korean
- English level: Can read sentences but lacks precise grammatical knowledge
- Session duration: 30 minutes per unit

Return a summary of:
- How many units were generated
- File paths for each unit
- Any issues encountered
```

### 2.2 병렬 실행 확인 사항

**중요:** 에이전트에게 명시적으로 병렬 실행을 요청해야 합니다.

✅ **올바른 방법:**
```
"Generate YAML files for ALL units IN PARALLEL"
"Use parallel execution to create all 6 unit files simultaneously"
```

❌ **잘못된 방법:**
```
"Generate unit files one by one" (순차 실행 - 느림)
```

### 2.3 생성될 파일 예시 (Past units)

```
units/unit10-was-were.yaml
units/unit11-worked-got-went-simple-past.yaml
units/unit12-simple-past-negative-and-questions.yaml
units/unit13-i-was-doing-past-continuous.yaml
units/unit14-past-continuous-and-simple-past.yaml
units/unit15-i-used-to.yaml
```

---

## 📋 Step 3: 검수 실행

### 3.1 검수 에이전트 실행

**사용 에이전트:** `general-purpose`

```markdown
Task 프롬프트 예시:

You are the content-reviewer agent. Review all Past tense units (Unit 10-15) that were just generated.

Files to review:
- units/unit10-was-were.yaml
- units/unit11-worked-got-went-simple-past.yaml
- units/unit12-simple-past-negative-and-questions.yaml
- units/unit13-i-was-doing-past-continuous.yaml
- units/unit14-past-continuous-and-simple-past.yaml
- units/unit15-i-used-to.yaml

Evaluation criteria:
1. Pedagogical Quality (research-based principles applied?)
2. Content Accuracy (grammar explanations correct?)
3. Completeness (all required sections present?)
4. Format & Structure (consistent YAML structure?)
5. Alignment (consistent with Units 1-9 style?)

For EACH unit, provide:
- Strengths
- Issues found (critical/minor)
- Specific corrections needed
- Quality rating (out of 10)
- Recommendation (approve/revise)

Save review results to:
reviews/unit10-review.md
reviews/unit11-review.md
...
reviews/unit15-review.md

Return a summary table of all reviews.
```

### 3.2 검수 결과 확인

```bash
# 검수 결과 파일 확인
ls -lh E:\code\grammar_in_use_content\reviews/unit*.md

# 특정 리뷰 읽기
cat E:\code\grammar_in_use_content\reviews/unit10-review.md
```

---

## 📋 Step 4: 이슈 반영 및 수정

### 4.1 검수 결과 요약 요청

```markdown
User 프롬프트:

검수 결과를 요약해주세요. 수정이 필요한 이슈들을 우선순위별로 정리해주세요.
```

### 4.2 이슈 수정

**방법 1: 자동 수정 (권장)**
```markdown
User 프롬프트:

검수에서 발견된 모든 이슈를 반영해서 컨텐츠를 업데이트해주세요.
```

**방법 2: 수동 확인 후 수정**
```markdown
User 프롬프트:

다음 이슈들을 수정해주세요:
1. Unit 10: 시간 표기 불일치 (meta field)
2. Unit 12: 예시 문장 오타
3. Unit 14: 정답 키 누락
```

### 4.3 수정 확인

```bash
# 수정된 파일 확인
git status

# 변경 내용 확인
git diff units/unit10-was-were.yaml
```

---

## 📋 Step 5: 복습 자료 생성 (선택사항)

### 5.1 그룹 복습 자료 생성

```markdown
Task 프롬프트 예시:

Generate a comprehensive review file for Past tense units (Units 10-15).

Requirements:
1. Read all units: unit10-unit15
2. Create integrated review covering all 6 units
3. Include:
   - Self-diagnosis checklist
   - Mixed retrieval practice
   - Diagnostic test (identify weak units)
   - Interleaving exercises
   - Final comprehensive assessment
   - Spaced repetition schedule
4. Save as: units/review-units-10-15.yaml
5. Follow the same structure as units/review-units-1-9.yaml

Return summary of review content created.
```

---

## 📋 Step 6: 최종 커밋

### 6.1 변경사항 확인

```bash
git status
```

### 6.2 커밋 메시지 작성

```bash
git add units/unit10-*.yaml units/unit11-*.yaml ... units/unit15-*.yaml
git add reviews/unit10-review.md ... reviews/unit15-review.md

git commit -m "Add Past tense units (10-15) with reviews

- Add unit10-was-were.yaml
- Add unit11-worked-got-went-simple-past.yaml
- Add unit12-simple-past-negative-and-questions.yaml
- Add unit13-i-was-doing-past-continuous.yaml
- Add unit14-past-continuous-and-simple-past.yaml
- Add unit15-i-used-to.yaml
- Add review files for all units
- All units reviewed and issues resolved

🎓 Generated with Claude Code"

git push origin main
```

---

## 🔄 세션 간 작업 재개 가이드

### 다음 세션에서 이어하기

1. **진행 상황 파악**
```bash
# 어떤 유닛들이 이미 생성되었는지 확인
ls -1 units/unit*.yaml | wc -l

# 마지막으로 생성된 유닛 확인
ls -lt units/unit*.yaml | head -5
```

2. **다음 그룹 선택**
```bash
# 커리큘럼 파일 목록 확인
ls -1 curriculum/*.txt

# 예: Past 완료 → Present Perfect 시작
cat curriculum/03-present-perfect_units.txt
```

3. **프로세스 반복**
- Step 2부터 다시 시작
- 새로운 커리큘럼 파일(예: 03-present-perfect_units.txt) 사용

---

## 📊 진행 상황 추적

### 체크리스트

```
✅ 01-present_units.txt          (Units 1-9)   - COMPLETED
⬜ 02-past_units.txt             (Units 10-15) - IN PROGRESS
⬜ 03-present-perfect_units.txt  (Units 16-19)
⬜ 04-passive_units.txt          (Units 20-21)
⬜ 05-verb-forms_units.txt       (Units 22-23)
⬜ 06-future_units.txt           (Units 24-26)
⬜ 07-modals_units.txt           (Units 27-34)
⬜ 08-there-and-it_units.txt     (Units 35-37)
⬜ 09-auxiliary-verbs_units.txt  (Units 38-41)
⬜ 10-questions_units.txt        (Units 42-47)
⬜ 11-reported-speech_units.txt  (Unit 48)
⬜ 12-ing-and-to_units.txt       (Units 49-52)
⬜ 13-go-get-do-make-have_units.txt (Units 53-56)
⬜ 14-pronouns-and-possessives_units.txt (Units 57-62)
⬜ 15-a-and-the_units.txt        (Units 63-71)
⬜ 16-determiners-and-pronouns_units.txt (Units 72-82)
⬜ 17-adjectives-and-adverbs_units.txt (Units 83-90)
⬜ 18-word-order_units.txt       (Units 91-94)
⬜ 19-conjunctions-and-clauses_units.txt (Units 95-100)
⬜ 20-prepositions_units.txt     (Units 101-111)
⬜ 21-phrasal-verbs_units.txt    (Units 112-113)
```

---

## 🚨 문제 해결 가이드

### Issue 1: 에이전트가 순차 실행함

**증상:** 유닛을 하나씩 생성함 (느림)

**해결:**
```markdown
프롬프트에 명시적으로 추가:
"IMPORTANT: Generate ALL unit files IN PARALLEL using multiple tool calls in a single message."
```

### Issue 2: YAML 파일 형식 오류

**증상:** 파일이 생성되었지만 viewer.html에서 로드 안 됨

**해결:**
```bash
# YAML 문법 검증
python -c "import yaml; yaml.safe_load(open('units/unit10-was-were.yaml'))"

# 에이전트에게 수정 요청
"unit10 파일에 YAML 문법 오류가 있습니다. 수정해주세요."
```

### Issue 3: 검수 결과 파일 누락

**증상:** 일부 유닛의 리뷰 파일이 없음

**해결:**
```markdown
"다음 유닛들의 검수 결과가 누락되었습니다. 검수를 다시 실행해주세요:
- unit12
- unit14"
```

### Issue 4: 파일명 불일치

**증상:** 파일명이 규칙을 따르지 않음

**해결:**
```bash
# 파일명 수정
mv units/unit10.yaml units/unit10-was-were.yaml

# 또는 에이전트에게 요청
"파일명이 일관성 없습니다. unit{번호}-{slug}.yaml 형식으로 변경해주세요."
```

---

## 💡 팁과 모범 사례

### 1. 병렬 실행 최대화
- 한 번에 한 그룹(5-10개 유닛)씩 생성
- 너무 많은 유닛(20개 이상)을 한 번에 요청하지 말 것

### 2. 검수는 필수
- 컨텐츠 생성 직후 바로 검수 실행
- 검수 결과를 반드시 반영한 후 커밋

### 3. 정기적 커밋
- 각 그룹 완료 시 커밋
- 커밋 메시지에 유닛 범위 명시

### 4. 백업
- 중요한 변경 전에 브랜치 생성
```bash
git checkout -b backup-before-past-units
git checkout main
```

### 5. 진행 상황 문서화
- 이 문서의 체크리스트 업데이트
- README.md에 진행 상황 반영

---

## 📚 참고 자료

- **기존 유닛 예시:** `units/unit1-am-is-are.yaml` ~ `units/unit9-have-and-have-got.yaml`
- **검수 예시:** `reviews/unit3-review.md` ~ `reviews/unit9-review.md`
- **복습 자료 예시:** `units/review-units-1-9.yaml`
- **뷰어 테스트:** `viewer.html?file=units/unit1-am-is-are.yaml`

---

## 🎯 빠른 시작 템플릿

### 새 그룹 시작 시 복사해서 사용:

```markdown
# Step 1: 커리큘럼 확인
@curriculum/02-past_units.txt 파일을 읽고 Past 그룹 유닛 목록을 확인해주세요.

# Step 2: 컨텐츠 생성
content-creator 에이전트에게 curriculum/02-past_units.txt에 있는 모든 유닛의 학습 자료를 병렬로 생성해달라고 요청해주세요.

# Step 3: 검수
생성이 완료되면 content-reviewer 에이전트에게 모든 Past 유닛(10-15)을 검수해달라고 요청해주세요.

# Step 4: 이슈 반영
검수에서 발견된 이슈들을 반영해서 컨텐츠를 업데이트해주세요.

# Step 5: 커밋
변경사항을 커밋하고 푸시해주세요.
```

---

**작성일:** 2025-11-19
**버전:** 1.0
**상태:** ✅ Present 완료, 🚧 Past 준비 중
