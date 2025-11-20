# 다음 세션 컨텍스트 (Session Context)

이 파일을 다음 세션 시작 시 Claude Code에게 보여주세요.

## 📋 프로젝트 개요

**목적**: Grammar in Use 교재 기반 영어 문법 학습 자료를 AI 에이전트로 자동 생성

**학습자**: 초등 6학년, 한국어 모국어, 기본 읽기 가능하지만 문법 지식 부족

---

## ✅ 완료된 작업

### 1. AI 에이전트 생성 (2개)

**Content Creator Agent** (`.claude/agents/content-creator.md`)
- YAML 형식으로 문법 학습 자료 생성
- **10개 섹션 표준 구조** 필수:
  1. 핵심 개념 정리 (8-10개 이상 예문 필수)
  2. Noticing 활동
  3. 회상 연습
  4. 기초 연습 - 빈칸 채우기
  5. 문장 만들기 - 번역
  6. 변형 연습
  7. 실생활 적용
  8. 종합 문제
  9. 내일 복습용 문제
  10. 자기 점검 & 격려

**Content Reviewer Agent** (`.claude/agents/content-reviewer.md`)
- 6가지 차원으로 품질 검수
- Critical Error 식별
- 개선 제안 제공

### 2. 워크플로우 시스템 구축

**슬래시 커맨드**: `/generate-units`
- 자동으로 생성 → 검수 → 수정 워크플로우 실행
- `present_units.txt`에서 유닛 목록 읽기

**파일들**:
- `.claude/commands/generate-units.md` - 워크플로우 슬래시 커맨드
- `workflow.py` - Python 스크립트 (사용자 Python 미설치)
- `WORKFLOW.md` - 워크플로우 문서
- `present_units.txt` - Present 파트 9개 유닛 목록

### 3. Present 파트 완료 (Unit 1-9)

**생성 완료된 유닛**:
- `units/unit1-am-is-are.yaml`
- `units/unit2-am-is-are-questions.yaml`
- `units/unit3-i-am-doing-present-continuous.yaml`
- `units/unit4-are-you-doing-present-continuous-questions.yaml`
- `units/unit5-i-do-work-like-simple-present.yaml`
- `units/unit6-simple-present-negative.yaml`
- `units/unit7-simple-present-questions.yaml`
- `units/unit8-present-continuous-vs-simple-present.yaml`
- `units/unit9-have-and-have-got.yaml`
- `units/review-units-1-9.yaml` (Present 파트 복습)

### 4. Past 파트 완료 (Unit 10-15)

**생성 완료된 유닛**:
- `units/unit10-was-were.yaml` (Good)
- `units/unit11-simple-past.yaml` (Good)
- `units/unit12-simple-past-negative-questions.yaml` (Good)
- `units/unit13-past-continuous.yaml` (Good)
- `units/unit14-past-continuous-vs-simple-past.yaml` (Good)
- `units/unit15-used-to.yaml` (Excellent)
- `units/review-units-10-15.yaml` (Past 파트 복습)

### 5. 뷰어 생성

**HTML 뷰어**: `viewer.html`
- YAML 파일을 브라우저에서 보기 좋게 표시
- 로컬 서버 실행 중: `http://127.0.0.1:8000/viewer.html`

---

## 🎯 다음에 할 일

### 즉시 시작 가능한 작업

#### Option 1: Present Perfect 파트 생성 (Unit 16-19)

아직 생성 안 된 유닛:
- Unit 16: I've just... I've already... I haven't...yet
- Unit 17: Have you ever...?
- Unit 18: How long have you...?
- Unit 19: for, since, ago

#### Option 2: Future 파트 생성 (Unit 20-25)

- Unit 20: I'm going to...
- Unit 21: will
- Unit 22: will vs I'm going to...
- Unit 23: Shall I...? Will you...?
- Unit 24: might
- Unit 25: can and could

#### Option 3: 자동 워크플로우 실행

```
/generate-units
```

그러면:
1. 생성할 유닛 선택 (전체/특정/범위)
2. 자동으로 각 유닛 생성 → 검수 → 수정
3. `units/` 폴더에 저장
4. `reviews/` 폴더에 검수 리포트 저장

---

## 📂 프로젝트 구조

```
E:\code\grammar_in_use_content/
├── .claude/
│   ├── agents/
│   │   ├── content-creator.md      ⭐ 컨텐츠 생성 AI
│   │   └── content-reviewer.md     ⭐ 검수 AI
│   ├── commands/
│   │   └── generate-units.md       ⭐ 워크플로우 커맨드
│   └── config.json                 (autoCompact: false)
│
├── units/
│   ├── unit1-am-is-are.yaml                ✅ Present
│   ├── unit2-am-is-are-questions.yaml      ✅ Present
│   ├── unit3-i-am-doing-present-continuous.yaml  ✅ Present
│   ├── unit4-are-you-doing-present-continuous-questions.yaml  ✅ Present
│   ├── unit5-i-do-work-like-simple-present.yaml  ✅ Present
│   ├── unit6-simple-present-negative.yaml  ✅ Present
│   ├── unit7-simple-present-questions.yaml ✅ Present
│   ├── unit8-present-continuous-vs-simple-present.yaml  ✅ Present
│   ├── unit9-have-and-have-got.yaml        ✅ Present
│   ├── unit10-was-were.yaml                ✅ Past
│   ├── unit11-simple-past.yaml             ✅ Past
│   ├── unit12-simple-past-negative-questions.yaml  ✅ Past
│   ├── unit13-past-continuous.yaml         ✅ Past
│   ├── unit14-past-continuous-vs-simple-past.yaml  ✅ Past
│   ├── unit15-used-to.yaml                 ✅ Past
│   ├── review-units-1-9.yaml               ✅ Review
│   └── review-units-10-15.yaml             ✅ Review
│
├── reviews/
│   └── (검수 리포트)
│
├── viewer.html                     ⭐ YAML 뷰어
├── present_units.txt               ⭐ 유닛 목록
├── WORKFLOW.md                     ⭐ 워크플로우 가이드
├── workflow.py                     (Python 미설치로 미사용)
└── SESSION_CONTEXT.md              ⭐ 이 파일!
```

---

## 🚀 다음 세션 시작 방법

### 방법 1: 이 파일 보여주기

다음 세션에서 Claude Code에게:

```
@SESSION_CONTEXT.md 파일을 읽고 작업을 이어서 진행해줘.
Present 파트 나머지 유닛들을 생성하자.
```

### 방법 2: 슬래시 커맨드 바로 실행

```
/generate-units
```

### 방법 3: 구체적 지시

```
Unit 1부터 5까지 순서대로 생성해줘.
각 유닛마다 생성 → 검수 → 수정 워크플로우를 실행해.
```

---

## 🔧 중요한 설정

### 에이전트 호출 방법

**Content Creator 호출 예시**:
```
Task tool 사용, subagent_type='general-purpose'
프롬프트: .claude/agents/content-creator.md 읽고 따르기
입력: "Present: Unit1 - am/is/are"
출력: YAML 코드블록만
```

**Content Reviewer 호출 예시**:
```
Task tool 사용, subagent_type='general-purpose'
프롬프트: .claude/agents/content-reviewer.md 읽고 따르기
입력: units/unit1-am-is-are.yaml 파일 경로
출력: 검수 리포트
```

### 파일명 규칙

```
Present: Unit{N} - {제목}
→ units/unit{N}-{slug}.yaml

예시:
"Present: Unit1 - am/is/are"
→ units/unit1-am-is-are.yaml

"Present: Unit3 - I am doing (present continuous)"
→ units/unit3-i-am-doing-present-continuous.yaml
```

---

## ⚠️ 주의사항

1. **구조 일관성**: 모든 유닛은 정확히 10개 섹션, 정해진 순서
2. **Section 1**: 반드시 8-10개 이상의 다양한 예문 포함
3. **검수 필수**: 모든 유닛은 생성 후 반드시 검수
4. **Critical Error 발견 시**: 자동으로 수정 워크플로우 실행
5. **저작권**: Grammar in Use 원본 내용 절대 복사 금지

---

## 📊 진행 상황

- [x] 에이전트 2개 생성
- [x] 워크플로우 시스템 구축
- [x] Present 파트 완료 (Unit 1-9)
- [x] Past 파트 완료 (Unit 10-15)
- [x] 복습 유닛 완료 (Units 1-9, 10-15)
- [ ] Present Perfect 파트 생성 (16-19)
- [ ] Future 파트 생성 (20-25)

**현재**: 15개 유닛 + 2개 복습 유닛 완료

---

## 💡 팁

- 한 번에 2-3개 유닛씩 생성 권장 (품질 관리)
- 각 유닛마다 검수 리포트 확인
- Critical Error가 반복되면 에이전트 프롬프트 개선 필요
- 로컬 서버로 뷰어에서 실시간 확인 가능

---

**마지막 업데이트**: 2025-11-21
**다음 작업**: Present Perfect 파트 생성 (Unit 16-19)
