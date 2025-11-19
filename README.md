# 📚 Grammar in Use - 영문법 학습 자료

초등학교 6학년을 위한 연구 기반 영문법 학습 자료입니다.

## 🌐 온라인 뷰어

**👉 [https://no81.github.io/grammar_in_use_content/](https://no81.github.io/grammar_in_use_content/)**

위 링크에서 모든 유닛과 복습 자료를 바로 확인할 수 있습니다.

## 📖 학습 자료 구성

### Present Tense Units (1-9)

| Unit | 주제 | 설명 |
|------|------|------|
| **Unit 1** | am/is/are | be동사의 기본 형태와 사용법 |
| **Unit 2** | am/is/are (questions) | be동사를 사용한 의문문 |
| **Unit 3** | I am doing (present continuous) | 현재진행형 - 지금 하고 있는 일 |
| **Unit 4** | Are you doing? (present continuous questions) | 현재진행형 의문문 |
| **Unit 5** | I do/work/like (simple present) | 단순 현재 - 습관과 일반적 사실 |
| **Unit 6** | I don't... (simple present negative) | 단순 현재 부정문 |
| **Unit 7** | Do you...? (simple present questions) | 단순 현재 의문문 |
| **Unit 8** | I am doing and I do (comparison) | 현재진행형 vs 단순 현재 비교 |
| **Unit 9** | I have... and I've got... | 소유 표현 두 가지 방법 |

### 📝 Reviews

- **Units 1-9 종합 복습**: 모든 유닛을 통합적으로 복습하는 35-50분 분량의 종합 리뷰 자료

## 🎯 학습 특징

### 연구 기반 학습 원리 적용

이 학습 자료는 인지과학 연구 결과를 기반으로 제작되었습니다:

- **📅 Spaced Repetition (간격 반복)**: 최적의 시간 간격으로 복습하도록 설계
- **🧠 Retrieval Practice (인출 연습)**: 능동적으로 기억을 떠올리는 연습 포함
- **🔀 Interleaving (교차 학습)**: 여러 개념을 섞어서 연습하여 변별력 향상
- **🎨 Dual Coding (이중 부호화)**: 시각적 자료와 언어적 설명을 결합
- **🔍 Metacognition (메타인지)**: 자기 점검과 학습 성찰 활동 포함
- **📊 Progressive Difficulty (점진적 난이도)**: 기초부터 응용까지 체계적 구성

### 각 유닛 구성 (약 30분)

모든 유닛은 동일한 10단계 구조로 구성되어 있습니다:

1. **핵심 개념 정리** - 문법 규칙과 예시 학습
2. **Noticing 활동** - 패턴을 스스로 발견
3. **회상 연습** - 힌트 없이 기억 떠올리기
4. **기초 연습** - 빈칸 채우기
5. **문장 만들기** - 한영 번역 연습
6. **변형 연습** - 문장 형태 바꾸기
7. **실생활 적용** - 실제 상황에서 사용하기
8. **종합 문제** - 통합 평가
9. **내일 복습용 문제** - 간격 반복을 위한 복습
10. **자기 점검 & 격려** - 학습 성찰 및 동기 부여

## 💻 로컬에서 보기

### 방법 1: 온라인 뷰어 사용 (추천)
위의 GitHub Pages 링크를 사용하세요.

### 방법 2: 로컬 서버 실행

```bash
# Python이 설치되어 있는 경우
python -m http.server 8000

# 브라우저에서 접속
http://localhost:8000
```

### 방법 3: viewer.html로 파일 직접 로드

1. `viewer.html` 파일을 브라우저로 열기
2. 파일 선택 버튼으로 원하는 YAML 파일 선택

## 📂 프로젝트 구조

```
grammar_in_use_content/
├── index.html              # 메인 랜딩 페이지 (유닛 목록)
├── viewer.html             # YAML 뷰어
├── units/                  # 유닛 및 복습 자료
│   ├── unit1-am-is-are.yaml
│   ├── unit2-am-is-are-questions.yaml
│   ├── unit3-i-am-doing-present-continuous.yaml
│   ├── unit4-are-you-doing-present-continuous-questions.yaml
│   ├── unit5-i-do-work-like-simple-present.yaml
│   ├── unit6-simple-present-negative.yaml
│   ├── unit7-simple-present-questions.yaml
│   ├── unit8-present-continuous-vs-simple-present.yaml
│   ├── unit9-have-and-have-got.yaml
│   └── review-units-1-9.yaml
├── reviews/                # 에이전트 리뷰 결과 저장
└── README.md              # 이 파일
```

## 🎓 대상 학습자

- **학년**: 초등학교 6학년
- **모국어**: 한국어
- **영어 수준**: 문장은 읽을 수 있으나 정확한 문법 지식이 부족한 학습자
- **세션 시간**: 각 유닛 약 30분

## 🛠️ 기술 스택

- **콘텐츠 형식**: YAML
- **뷰어**: HTML + JavaScript (Vanilla)
- **YAML 파싱**: js-yaml 라이브러리
- **배포**: GitHub Pages

## 📝 콘텐츠 제작 원칙

### 한국 학습자를 위한 맞춤 설계

- 모든 문법 설명은 **한국어**로 제공
- 한국 초등학생의 실생활과 관련된 예시 사용
  - 학교 생활 (급식, 숙제, 체육 시간)
  - 가족과 친구
  - K-pop, 게임, 유튜브 등 관심사
  - 떡볶이, 김치 등 한국 음식

### 오류 예방 중심

- 한국 학습자가 자주 하는 실수를 집중적으로 다룸
- 예: 3인칭 단수 -s, be동사 vs 일반동사 혼동 등

## 📊 평가와 피드백

각 유닛과 복습 자료는 다음을 포함합니다:

- ✅ 자기 진단 체크리스트
- 📈 진행도 추적
- 🎯 즉각적인 피드백 (정답/해설)
- 💪 격려 메시지

## 🔄 업데이트 계획

- [ ] Units 10-20 추가 (과거 시제, 미래 시제 등)
- [ ] 오디오 발음 가이드 추가
- [ ] 인터랙티브 퀴즈 기능 강화
- [ ] 학습 진행도 저장 기능

## 👥 기여하기

이 프로젝트는 오픈 소스입니다. 개선 사항이나 제안이 있으시면:

1. Issue를 열어 문제나 제안 사항을 공유해주세요
2. Pull Request를 통해 직접 기여해주세요

## 📜 라이선스

이 프로젝트는 교육 목적으로 자유롭게 사용할 수 있습니다.

## 📧 문의

프로젝트 관련 문의는 GitHub Issues를 통해 남겨주세요.

---

**🌟 즐겁게 학습하세요! Happy Learning!**
