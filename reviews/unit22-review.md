# Unit 22 Review: be/have/do in present and past tenses

**Reviewer**: AI Content Reviewer
**Date**: 2025-12-06
**Unit File**: `units/unit22-be-have-do-in-present-and-past-tenses.yaml`

---

## Overall Assessment

**Quality Rating**: 8.5/10
**Recommendation**: APPROVE with minor revisions

---

## 1. Pedagogical Quality (9/10)

### Strengths
- **Excellent scaffolding**: The unit progressively builds from core concepts through noticing activities to retrieval practice, which aligns with cognitive load theory
- **Strong retrieval practice**: Section 3 effectively implements spaced retrieval without allowing students to peek at answers first
- **Differentiated exercises**: Wide variety of exercise types (fill-in-the-blank, translation, transformation, real-life application) caters to different learning styles
- **Metacognitive support**: Self-checking section (10) encourages learners to reflect on their understanding
- **Authentic context**: Examples are highly relevant to 6th graders (school, family, hobbies)

### Areas for Improvement
- **Noticing activity depth**: Q3 in Section 2 could guide students more explicitly to discover patterns (e.g., "Look at sentences 7-9. What do these three verbs have in common?")
- **Cognitive load in Section 1**: Introducing all three verbs simultaneously with both present AND past forms (12 forms total) may overwhelm learners. Consider splitting into two lessons or adding a comparison table

---

## 2. Content Accuracy (9.5/10)

### Strengths
- **Grammatically correct**: All example sentences are accurate
- **Comprehensive form coverage**: Correctly presents all forms (am/is/are, was/were, have/has, had, do/does, did)
- **Accurate explanations**: The distinction between auxiliary and main verb uses is clearly explained
- **Proper Korean translations**: Korean explanations are accurate and age-appropriate

### Issues Found

#### Minor Issue 1: Incomplete explanation
**Location**: Lines 18-20 (Section 1, meanings)
**Issue**: While the unit explains that these verbs can be used as both main verbs and auxiliaries, it doesn't clarify that auxiliary usage is more advanced and will be covered in detail later.
**Recommendation**: Add a note: "조동사 용법은 나중에 더 자세히 배울 거예요. 지금은 일반동사 용법에 집중하세요!"

#### Minor Issue 2: Example sequence
**Location**: Lines 24-36 (more examples)
**Issue**: Mixing auxiliary and main verb examples without clear grouping may confuse learners at this level.
**Recommendation**: Group examples - first show all main verb uses (lines 24-29, 31, 34), then clearly separate auxiliary uses (lines 30, 31, 32, 35) with a subheading.

---

## 3. Completeness (9/10)

### Strengths
- **All required sections present**: 10 sections as per standard format
- **Sufficient exercise quantity**:
  - Section 4: 8 exercises
  - Section 5: 8 exercises
  - Section 6: 8 exercises
  - Section 7: 4 exercises
  - Section 8: 4 exercises
  - Section 9: 10 exercises
- **Comprehensive coverage**: Covers forms, meanings, usage contexts, common errors, and contrasts

### Missing Elements

#### Missing: Visual organization aid
**Location**: Section 1 (lines 10-16)
**Issue**: The three verbs are presented in text format but a comparison table would enhance understanding
**Recommendation**: Add after line 9:
```yaml
- type: text
  content: "<table class='grammar-table'><thead><tr><th>동사</th><th>현재형</th><th>과거형</th></tr></thead><tbody><tr><td>be</td><td>am/is/are</td><td>was/were</td></tr><tr><td>have</td><td>have/has</td><td>had</td></tr><tr><td>do</td><td>do/does</td><td>did</td></tr></tbody></table>"
```

#### Missing: Practice with negatives and questions
**Location**: Throughout exercises
**Issue**: Most exercises focus on affirmative forms. Only Section 6 (TF8) and Section 8 (C2) practice interrogatives. No dedicated negative form practice for have/do.
**Recommendation**: Add 2-3 exercises in Section 4 or 6 specifically for negative/interrogative forms of have and do.

---

## 4. Format & Structure (9/10)

### Strengths
- **Consistent YAML structure**: Properly formatted with correct indentation
- **Proper use of HTML tags**: Consistent use of `<span class='highlight'>`, `<strong>`, `<br />` tags
- **Clear section organization**: Follows the established 10-section framework
- **Appropriate metadata**: Title and meta information are correctly formatted

### Issues Found

#### Minor Issue: HTML consistency
**Location**: Line 18
**Current**: `<span class='highlight'>의미/뉘앙스:</span><br />• <strong>be:</strong>`
**Issue**: Mixing `<span class='highlight'>` for headings with `<strong>` for emphasis within the same visual hierarchy level
**Recommendation**: Use consistent heading markup. Consider: `<strong class='highlight'>` for both, or stick to one style.

---

## 5. Alignment with Existing Units (8.5/10)

### Comparison with Unit 1 (am/is/are) and Unit 10 (was/were)

#### Strengths
- **Consistent structure**: Maintains the 10-section framework established in earlier units
- **Similar exercise types**: Fill-in-blank, translation, transformation exercises match Unit 1 and Unit 10 patterns
- **Consistent tone**: Encouraging, student-friendly language matches previous units
- **Korean support**: Maintains the same level of L1 support as earlier units

#### Inconsistencies

##### Issue 1: Complexity mismatch
**Observation**: Units 1 and 10 focus on ONE verb form each (be present, be past). Unit 22 covers THREE verbs across TWO tenses = 6 verb patterns in one unit.
**Impact**: This is significantly more complex than the precedent set by earlier units
**Recommendation**: Consider whether this should be split into Unit 22 (be/have/do present) and Unit 23 (be/have/do past), especially since Unit 23 exists and covers regular/irregular verbs. This would better align with the pacing of Units 1-10.

##### Issue 2: Example quantity
**Observation**: Unit 1 has 12 examples (lines 21-34), Unit 10 has 10 examples (lines 21-31), but Unit 22 has 12 examples (lines 24-36)
**Assessment**: Quantity is appropriate, but mixing auxiliary and main verb uses without clear separation adds complexity not present in earlier units
**Recommendation**: Maintain 12 examples but reorganize into two clear groups (main verb: 8 examples, auxiliary: 4 examples with note that these will be studied in detail later)

##### Issue 3: Common errors section
**Observation**: Unit 22's error section (line 37) is more detailed than Unit 1 (line 36) or Unit 10 (line 33)
**Assessment**: This is actually a strength - shows progression in complexity
**Recommendation**: Keep as is; this demonstrates appropriate scaffolding

---

## 6. Target Audience Fit (9/10)

### Age Appropriateness (6th Grade Korean Learners)

#### Strengths
- **Relevant contexts**: Examples mention student life, family, homework, sports, pets - all familiar to 6th graders
- **Appropriate vocabulary**: Uses high-frequency words that 6th graders would know (student, bike, happy, homework, etc.)
- **Cognitive level**: The distinction between main verb and auxiliary use is challenging but appropriate for 6th grade
- **Cultural sensitivity**: Examples are culturally neutral and relatable to Korean students

#### Areas for Improvement

##### Issue 1: Sentence length
**Location**: Lines 29-32 (examples with auxiliary verbs)
**Observation**: "I have finished." and "She has eaten." use present perfect, which may not have been taught yet
**Concern**: If present perfect hasn't been introduced, these examples may confuse rather than clarify
**Recommendation**: Check curriculum sequence. If present perfect comes later, replace with simpler auxiliary examples:
- "I am eating lunch." (present continuous)
- "She was studying English." (past continuous)
- "Do you like pizza?" (present simple question)

##### Issue 2: Metalinguistic terminology
**Location**: Lines 18-20
**Term**: "조동사" (auxiliary verb) and "일반동사" (main verb)
**Assessment**: This terminology is appropriate for 6th grade Korean students, as Korean grammar education uses similar metalinguistic terms
**Recommendation**: Keep as is, but ensure these terms were introduced in earlier units (check Units 1-10)

---

## Specific Corrections Needed

### Critical Corrections: NONE

### Minor Corrections:

#### Correction 1: Add progressive note about auxiliary verbs
**Location**: After line 20
**Add**:
```yaml
- type: note
  content: "💡 참고: 조동사 용법은 앞으로 진행형(Unit 3), 완료형(Unit 16-19) 등에서 더 자세히 배웁니다. 지금은 일반동사로 쓰이는 경우를 중심으로 익히세요!"
```

#### Correction 2: Reorganize examples for clarity
**Location**: Lines 22-36
**Current**: Mixed main verb and auxiliary examples
**Recommended**: Reorganize with subheadings:
```yaml
- type: list
  heading: "일반동사로 쓰일 때 (Main Verb Usage)"
  list:
    - "<strong>be 현재:</strong> I <span class='highlight'>am</span> a student..."
    - ... (lines 24-29, 31, 34)

- type: list
  heading: "조동사로 쓰일 때 (Auxiliary Verb - 참고용)"
  list:
    - "<strong>be + -ing:</strong> I <span class='highlight'>am</span> reading..."
    - ... (lines 30, 32, 35)
```

#### Correction 3: Add table for visual learners
**Location**: After line 9, before line 10
**Add**:
```yaml
- type: text
  content: "<div class='info-box'><strong>한눈에 보기:</strong><br />• be동사: am/is/are (현재) → was/were (과거)<br />• have: have/has (현재) → had (과거)<br />• do: do/does (현재) → did (과거)</div>"
```

#### Correction 4: Add negative/question practice
**Location**: Section 6, after TF8
**Add**:
```yaml
- type: qna
  question: "TF9. I have a dog. → 부정문으로"
  answer: "I don't have a dog. / I do not have a dog.<br />설명: have의 부정문은 don't have를 씁니다."
- type: qna
  question: "TF10. She does homework. → 의문문으로"
  answer: "Does she do homework?<br />설명: do의 의문문은 Does를 앞에 씁니다."
```

#### Correction 5: Simplify auxiliary examples if Present Perfect not yet taught
**Location**: Lines 31-32
**Current**: Uses present perfect ("have finished", "has eaten")
**Check**: If Present Perfect (Units 16-19) comes after Unit 22 in the curriculum
**If yes, replace with**:
```yaml
- "<strong>be 조동사:</strong> I <span class='highlight'>am</span> reading. (나는 읽고 있다) - 진행형"
- "<strong>be 조동사:</strong> She <span class='highlight'>was</span> sleeping. (그녀는 자고 있었다) - 과거진행형"
- "<strong>do 조동사:</strong> <span class='highlight'>Do</span> you like pizza? (너 피자 좋아하니?) - 의문문"
```

---

## Detailed Section-by-Section Analysis

### Section 1: 핵심 개념 정리 (8.5/10)
- **Strengths**: Comprehensive coverage, clear Korean explanations, good examples
- **Weaknesses**: Could be overwhelming with 3 verbs × 2 tenses; needs better visual organization
- **Recommendation**: Add summary table and reorganize examples

### Section 2: Noticing 활동 (9/10)
- **Strengths**: Good variety of example sentences, clear patterns
- **Weaknesses**: Q3 could scaffold discovery more explicitly
- **Recommendation**: Rephrase Q3 to guide students to notice the auxiliary+verb pattern

### Section 3: 회상 연습 (9.5/10)
- **Strengths**: Excellent retrieval practice design, appropriate difficulty gradation
- **Weaknesses**: None significant
- **Recommendation**: Keep as is

### Section 4: 기초 연습 (9/10)
- **Strengths**: Good variety, clear explanations, appropriate difficulty
- **Weaknesses**: Focuses only on affirmative forms; lacks negative/interrogative practice
- **Recommendation**: Add 2 questions for negative and interrogative forms

### Section 5: 문장 만들기 (9/10)
- **Strengths**: Relevant translations, flexible evaluation criteria
- **Weaknesses**: T8 uses present perfect structure that may not have been taught
- **Recommendation**: Check if "Did she have breakfast?" would be more appropriate than "Did she have breakfast?" depending on curriculum sequence

### Section 6: 변형 연습 (9/10)
- **Strengths**: Good variety of transformations (tense, subject, form)
- **Weaknesses**: Only 8 exercises; could add 2 more for have/do negative forms
- **Recommendation**: Add TF9-10 as suggested in Correction 4

### Section 7: 실생활 적용 (10/10)
- **Strengths**: Excellent personalization, clear evaluation criteria, age-appropriate
- **Weaknesses**: None
- **Recommendation**: Keep as is - this section is exemplary

### Section 8: 종합 문제 (9/10)
- **Strengths**: Integrative tasks, dialogue completion, error correction
- **Weaknesses**: C4 may be too challenging for some students as it requires understanding auxiliary vs. main verb distinction
- **Recommendation**: Consider adding a hint for C4

### Section 9: 내일 복습용 문제 (9.5/10)
- **Strengths**: Excellent spaced repetition design, good variety
- **Weaknesses**: None significant
- **Recommendation**: Keep as is

### Section 10: 자기 점검 & 격려 (10/10)
- **Strengths**: Excellent metacognitive support, encouraging tone, actionable advice
- **Weaknesses**: None
- **Recommendation**: Keep as is - this section is exemplary

---

## Research-Based Principles Applied

### ✅ Successfully Applied

1. **Spaced Repetition**: Section 9 explicitly implements next-day review
2. **Retrieval Practice**: Section 3 requires recall without looking back
3. **Interleaving**: Mixes all three verbs throughout exercises rather than blocking by verb
4. **Elaborative Interrogation**: "Why?" questions in Noticing section
5. **Metacognition**: Self-checking in Section 10
6. **Scaffolding**: Progressive difficulty from fill-in to translation to transformation
7. **Authentic Context**: Real-life application in Section 7
8. **Error Anticipation**: Common learner errors explicitly addressed

### ⚠️ Could Be Enhanced

1. **Dual Coding**: Add visual comparison table for three verbs
2. **Desirable Difficulties**: Current difficulty level is high due to covering 3 verbs × 2 tenses; consider splitting
3. **Generative Learning**: Could add more opportunities for students to create their own examples

---

## Comparison with Similar Units

| Aspect | Unit 1 (am/is/are) | Unit 10 (was/were) | Unit 22 (be/have/do) | Assessment |
|--------|-------------------|-------------------|---------------------|------------|
| Scope | 1 verb, 1 tense | 1 verb, 1 tense | 3 verbs, 2 tenses | Too broad? |
| Examples | 12 | 10 | 12 | Appropriate |
| Exercises (Sec 4) | 8 | 8 | 8 | Consistent |
| Complexity | Basic | Basic | Intermediate | Appropriate for Unit 22 |
| Auxiliary usage | No | No | Yes | Adds complexity |

**Finding**: Unit 22 is notably more complex than Units 1 and 10. This is appropriate for a later unit (Unit 22) but may challenge some learners. Consider adding extra support or splitting content.

---

## Summary of Key Issues

### Critical Issues: 0

### Minor Issues: 5

1. **Cognitive Load**: Covering 3 verbs × 2 tenses in one unit may overwhelm some learners
2. **Example Organization**: Mixing auxiliary and main verb uses without clear separation
3. **Missing Visual Aid**: Would benefit from a comparison table
4. **Limited Negative/Question Practice**: Mostly focuses on affirmative statements
5. **Curriculum Dependency**: Uses present perfect examples that may not have been taught yet

---

## Recommendations

### Priority 1 (High - Implement before publication)
1. Add subheadings to separate main verb and auxiliary verb examples (Correction 2)
2. Verify that present perfect has been taught before Unit 22; if not, replace examples (Correction 5)
3. Add visual summary table or info box (Correction 3)

### Priority 2 (Medium - Implement if time allows)
1. Add 2 exercises for negative and interrogative forms (Correction 4)
2. Add note about auxiliary verbs being covered in detail later (Correction 1)
3. Consider whether content should be split across two units

### Priority 3 (Low - Nice to have)
1. Add visual comparison table in HTML format
2. Add hints to more challenging questions (Section 8, C4)
3. Add more explicit pattern discovery scaffolding in Noticing section

---

## Overall Evaluation

**Strengths**:
- Pedagogically sound with excellent use of retrieval practice and spaced repetition
- Comprehensive coverage of three essential verbs
- Engaging, age-appropriate examples and contexts
- Strong metacognitive support through self-checking
- Consistent with established unit format

**Weaknesses**:
- Broader scope than earlier units may challenge some learners
- Needs better organization to distinguish main verb vs. auxiliary usage
- Could benefit from visual comparison aids
- Limited practice with negative and interrogative forms

**Final Recommendation**: **APPROVE** with minor revisions listed in Priority 1. This is a high-quality unit that effectively teaches important foundational verbs. With the suggested improvements to organization and clarity, it will serve students very well.

---

**Next Steps**:
1. Implement Priority 1 corrections
2. Review curriculum sequence to verify present perfect timing
3. Consider learner feedback after implementation to assess whether cognitive load is appropriate
4. If students struggle, consider splitting into two units in future revision
