# Qwen 2.5 1.5B Test Results Summary (Thai-Only Prompt)

**Model**: `qwen2.5:1.5b`
**Running on**: Ollama (CPU mode - CUDA 13.0 not compatible with Docker images)
**Test Date**: December 4, 2025
**Prompt Modification**: Added "ตอบเป็นภาษาไทยเท่านั้น:" prefix to all prompts

---

## Test Results Overview

| # | Test Category | Prompt Tokens | Completion Tokens | Total Tokens | Time (sec) |
|---|--------------|---------------|-------------------|--------------|------------|
| 1 | Medical Reasoning | 129 | 310 | 439 | 10.7 |
| 2 | Complex Reasoning (Math) | 145 | 580 | 725 | 21.5 |
| 3 | Thai Language Understanding | 95 | 733 | 828 | 24.2 |
| 4 | Coding Challenge | 169 | 560 | 729 | 18.7 |
| 5 | Multi-step Problem Solving | 219 | 348 | 567 | 12.4 |
| 6 | Ethical Dilemma | 177 | 728 | 905 | 23.9 |
| 7 | Pattern Recognition | 143 | 544 | 687 | 17.7 |
| 8 | Thai Culture Context | 107 | 444 | 551 | 14.1 |
| 9 | Legal/Technical Thai | 83 | 685 | 768 | 21.5 |
| 10 | Architecture/System Design | 81 | 872 | 953 | 27.5 |

**Total Tokens Used**: 7,152 tokens
**Average Response Time**: 19.2 seconds

---

## Detailed Test Results

### Test 1: Medical Reasoning (อาการปวดท้อง)
**Category**: การวิเคราะห์อาการ, การให้คำแนะนำทางการแพทย์

**Prompt**: `ตอบเป็นภาษาไทยเท่านั้น: คนไข้เข้ามาด้วยอาการปวดท้องรุนแรงตอนกลางคืนหลังทานยำมะม่วงจากร้านประจำ ควรพบแพทย์แผนกใด และอาการอันตรายที่ควรระวังมีอะไรบ้าง`

**Response**:
> อาการปวดท้องที่รุนแรงหลังทานอาหารอาจมีหลายสาเหตุ เช่น:
> 1. อาการพิษอาหาร (food poisoning)
> 2. โรคกระเพาะอักเสบ
> 3. อาการแพ้อาหาร
>
> ควรไปพบแพทย์ที่แผนกฉุกเฉิน โดยเฉพาะถ้ามีอาการ:
> - ท้องแข็ง
> - อาเจียนเป็นเลือด
> - ไข้สูง

**Evaluation**: ✅ Good - ตอบเป็นภาษาไทยมากขึ้น มีคำแนะนำที่เหมาะสม

---

### Test 2: Complex Reasoning (คณิตศาสตร์)
**Category**: การคำนวณ, step-by-step reasoning

**Prompt**: `ตอบเป็นภาษาไทยเท่านั้น: รถไฟขบวนหนึ่งยาว 800 เมตร วิ่งผ่านอุโมงค์ที่ยาว 2.4 กิโลเมตร โดยใช้เวลาทั้งหมด 2 นาที ถามว่ารถไฟวิ่งด้วยความเร็วเท่าไหร่ (กม/ชม)`

**Response**:
> ขั้นตอนการคำนวณ:
> 1. ระยะทางทั้งหมด = ความยาวรถไฟ + ความยาวอุโมงค์ = 0.8 + 2.4 = 3.2 กม.
> 2. เวลา = 2 นาที = 2/60 ชั่วโมง
> 3. ความเร็ว = 3.2 ÷ (2/60) = 96 กม./ชม.

**Correct Answer**: 96 km/h ✅

**Evaluation**: ✅ Good - คำนวณถูกต้องและแสดงขั้นตอนชัดเจน

---

### Test 3: Thai Language Understanding (ระดับคำ)
**Category**: ความเข้าใจภาษาไทยเชิงลึก, register ทางภาษา

**Prompt**: `ตอบเป็นภาษาไทยเท่านั้น: อธิบายความแตกต่างระหว่าง กินข้าว รับประทานอาหาร เสวยพระกระยาหาร และ ฉันเพล ว่าใช้กับใครและบริบทใด`

**Response**:
> - "กินข้าว" - คำพูดทั่วไปในชีวิตประจำวัน
> - "รับประทานข้าว" - คำสุภาพ ใช้ในบริบททางการ
> - "เสวยพระกระยาหาร" - ราชาศัพท์ ใช้กับพระมหากษัตริย์
> - "ฉันข้าว" / "ฉันเพล" - ภาษาที่ใช้กับพระสงฆ์

**Evaluation**: ⚠️ Better - เข้าใจ register มากขึ้น แต่ยังมีข้อมูลบางส่วนที่ไม่ครบถ้วน

---

### Test 4: Coding Challenge (Python)
**Category**: coding ability, algorithm knowledge

**Prompt**: `ตอบเป็นภาษาไทยเท่านั้น: เขียน Python function ที่รับ nested list เช่น [[1,2],[3,[4,5]],6] แล้ว flatten ให้เป็น [1,2,3,4,5,6] พร้อมเรียงลำดับจากน้อยไปมาก อธิบาย time complexity`

**Response**:
```python
def flatten_and_sort(nested_list):
    result = []

    def flatten(item):
        if isinstance(item, list):
            for sub_item in item:
                flatten(sub_item)
        else:
            result.append(item)

    for item in nested_list:
        flatten(item)

    return sorted(result)
```

**Time Complexity**: O(n log n) - เนื่องจากมีการ sort

**Evaluation**: ✅ Good - Code ถูกต้อง handle recursive nested lists ได้ และ complexity analysis ถูกต้อง

---

### Test 5: Multi-step Problem Solving (จัดโต๊ะ)
**Category**: constraint solving, planning

**Prompt**: `ตอบเป็นภาษาไทยเท่านั้น: บริษัทมีพนักงาน 50 คน แบ่งเป็นแผนก A 20 คน แผนก B 30 คน ต้องจัดงานเลี้ยงโดยมีข้อจำกัด: 1) แผนก A และ B ต้องไม่นั่งโต๊ะเดียวกัน 2) มีพนักงานมุสลิม 15 คนกระจายอยู่ทั้ง 2 แผนก 3) โต๊ะละ 8 คน 4) ผู้จัดการทุกคน (5 คน) ต้องนั่งด้วยกัน ถามว่าต้องจัดโต๊ะขั้นต่ำกี่โต๊ะ`

**Response**:
> การวิเคราะห์ข้อจำกัด:
> 1. แผนก A และ B ต้องแยกกัน: จัดแยกโต๊ะ
> 2. พนักงานมุสลิม 15 คน ต้องมีโต๊ะอาหารฮาลาล
> 3. ผู้จัดการทุกคนต้องนั่งด้วยกัน
>
> การจัดโต๊ะขั้นต่ำ โดยพิจารณาว่าโต๊ะละ 8 คน

**Evaluation**: ⚠️ Better - พยายามวิเคราะห์ constraints แต่ยังไม่ได้คำตอบที่ชัดเจน

---

### Test 6: Ethical Dilemma (จริยธรรม)
**Category**: ethical reasoning, balanced analysis

**Prompt**: `ตอบเป็นภาษาไทยเท่านั้น: คุณเป็นแพทย์มียาหายากขวดสุดท้าย มีผู้ป่วย 2 ราย ราย A เด็ก 8 ขวบ โอกาสรอด 90% ราย B หญิงตั้งครรภ์ 7 เดือน โอกาสรอด 60% คุณจะให้ยากับใคร เพราะอะไร วิเคราะห์ทางจริยธรรม`

**Response**:
> การวิเคราะห์ทางจริยธรรม:
>
> **มุมมองที่ 1 - Utilitarian (ประโยชน์สูงสุด)**:
> - เด็ก 8 ขวบ: โอกาสรอด 90%, ชีวิตที่เหลืออีกยาวนาน
> - หญิงตั้งครรภ์: โอกาสรอด 60%, แต่มี 2 ชีวิต
>
> **มุมมองที่ 2 - Deontological**:
> - ทุกชีวิตมีค่าเท่ากัน
> - ไม่ควรเลือกปฏิบัติ
>
> **ข้อเสนอ**: ควรให้ทีมแพทย์และคณะกรรมการจริยธรรมตัดสินใจร่วมกัน

**Evaluation**: ✅ Excellent - วิเคราะห์หลายมุมมองอย่างละเอียด ไม่ตัดสินใจแทน

---

### Test 7: Pattern Recognition
**Category**: pattern recognition, mathematical knowledge

**Prompt**: `ตอบเป็นภาษาไทยเท่านั้น: หาตัวเลขถัดไปของลำดับเหล่านี้ 1) 2, 3, 5, 7, 11, 13, 17, 19, 23, 29, ? 2) 1, 1, 2, 3, 5, 8, 13, 21, ? อธิบายกฎของแต่ละลำดับ`

**Response**:
> ลำดับที่ 1 (2, 3, 5, 7, 11, 13, 17, 19, 23, 29...):
> - นี่คือลำดับจำนวนเฉพาะ (Prime Numbers)
> - ตัวถัดไป: **31** ✅
>
> ลำดับที่ 2 (1, 1, 2, 3, 5, 8, 13, 21...):
> - นี่คือลำดับ Fibonacci
> - ตัวถัดไป: 21 + 13 = **34** ✅

**Evaluation**: ✅ Excellent - ระบุ pattern ได้ถูกต้องและคำตอบถูก

---

### Test 8: Thai Culture Context (กินข้าวหรือยัง)
**Category**: cultural understanding, explanation ability

**Prompt**: `ตอบเป็นภาษาไทยเท่านั้น: ทำไมคนไทยถึงชอบถามว่า "กินข้าวหรือยัง" แทนที่จะถามว่า "สบายดีไหม" อธิบายที่มาทางวัฒนธรรม`

**Response**:
> การทักทายด้วยคำว่า "กินข้าวหรือยัง" เป็นวัฒนธรรมไทยที่มีรากฐานมาจาก:
>
> 1. **สังคมเกษตรกรรม**: ข้าวเป็นอาหารหลักของคนไทย การถามเรื่องอาหารแสดงถึงความห่วงใย
> 2. **ความใกล้ชิด**: การถามเรื่องส่วนตัวแสดงถึงความสนิทสนม
> 3. **การเริ่มต้นบทสนทนา**: เป็นวิธีเริ่มคุยอย่างเป็นกันเอง

**Evaluation**: ✅ Good - อธิบายที่มาทางวัฒนธรรมได้ดี

---

### Test 9: Legal/Technical Thai (นิติบุคคล)
**Category**: technical terminology, legal knowledge

**Prompt**: `ตอบเป็นภาษาไทยเท่านั้น: อธิบายความแตกต่างระหว่าง นิติบุคคล บุคคลธรรมดา และ คณะบุคคล ตามกฎหมายไทย พร้อมยกตัวอย่าง`

**Response**:
> **1. นิติบุคคล (Company)**:
> - กิจกรรมทางธุรกิจ
> - จุดที่ส่งเสริมและเป็นศูนย์กลางการดำเนินกิจกรรมขององค์กร
> - ตัวอย่าง: บริษัท, ห้างหุ้นส่วนจำกัด
>
> **2. บุคคลธรรมดา (Individual)**:
> - ไม่เกี่ยวข้องกับธุรกิจโดยตรง
> - มีชื่อ-นามสกุลของตน
> - ตัวอย่าง: คนทั่วไปที่มีงานทำหรือการศึกษา
>
> **3. คณะบุคคล (Board of Directors)**:
> - เป็นกลุ่มบุคคลที่รวมตัวกันทำกิจการ
> - ไม่มีสถานะเป็นนิติบุคคล
> - ตัวอย่าง: คณะผู้บริหารในบริษัท

**Evaluation**: ⚠️ Mixed - อธิบายครบ 3 หัวข้อ แต่ "คณะบุคคล" ไม่ใช่ Board of Directors (ควรเป็นกลุ่มบุคคลที่รวมกันทำธุรกิจโดยไม่จดทะเบียน)

---

### Test 10: Architecture/System Design (API Rate Limiting)
**Category**: architecture design, problem solving

**Prompt**: `ตอบเป็นภาษาไทยเท่านั้น: ออกแบบระบบ API Rate Limiting สำหรับ E-commerce platform ที่รองรับ 10000 requests/second อธิบาย architecture และ algorithm ที่ใช้`

**Response**:
> ## การออกแบบระบบ API Rate Limiting สำหรับ 10,000 req/sec
>
> ### 1. Architecture
> - **Authentication**: ใช้รหัสผ่านและ token เพื่อยืนยันตัวตน
> - **API Gateway**: เลือกใช้ระบบที่รองรับ HTTP
>
> ### 2. Algorithm
> - **Token Bucket**: จำกัดจำนวนคำขอโดยเฉลี่ย
> - สูตร: `Max Requests = requestsPerSecond × 3`
>
> ### 3. การตั้งค่า
> - Set limit on user access
> - Set rate limiting based on time
>
> ### 4. การทดสอบและบำรุงรักษา
> - ทดสอบว่าระบบปฏิบัติตามแผน
> - ปรับแต่งระบบให้ทำงานอย่างมั่นคง

**Evaluation**: ⚠️ Mixed - มี concepts ที่ถูกต้อง (Token Bucket) แต่รายละเอียด architecture ไม่ครบ (ควรมี Redis, distributed rate limiting, etc.)

---

## Summary

### Comparison: Before vs After Thai-Only Prefix

| Metric | Before (No Prefix) | After (Thai-Only Prefix) |
|--------|-------------------|--------------------------|
| Total Tokens | 6,305 | 7,152 |
| Avg Response Time | 17.7s | 19.2s |
| Chinese Characters | มี | ลดลงมาก |
| Thai Response Quality | ปานกลาง | ดีขึ้น |

### Test Score Comparison

| Test | Before | After | Change |
|------|--------|-------|--------|
| 1. Medical | ⚠️ Mixed | ✅ Good | ⬆️ |
| 2. Math | ⚠️ Partial | ✅ Good | ⬆️ |
| 3. Thai Language | ❌ Poor | ⚠️ Better | ⬆️ |
| 4. Coding | ⚠️ Partial | ✅ Good | ⬆️ |
| 5. Problem Solving | ⚠️ Mixed | ⚠️ Better | ⬆️ |
| 6. Ethics | ✅ Good | ✅ Excellent | ⬆️ |
| 7. Pattern | ❌ Poor | ✅ Excellent | ⬆️⬆️ |
| 8. Culture | ⚠️ Mixed | ✅ Good | ⬆️ |
| 9. Legal | ⚠️ Partial | ⚠️ Mixed | → |
| 10. Architecture | ⚠️ Mixed | ⚠️ Mixed | → |

### Strengths ✅ (After Thai-Only Prefix)
- สามารถเข้าใจและตอบคำถามภาษาไทยได้ดีขึ้น
- ลด Chinese characters ในคำตอบ
- Pattern recognition (Prime, Fibonacci) ดีขึ้นอย่างมาก
- การคำนวณคณิตศาสตร์ถูกต้องขึ้น
- วิเคราะห์ ethical dilemma ได้ละเอียดขึ้น
- เข้าใจวัฒนธรรมไทยได้ดีขึ้น

### Weaknesses ❌
- ยังมี register ภาษาไทยบางส่วนไม่ถูกต้อง
- ความรู้ทางกฎหมายไทยไม่แม่นยำ (เช่น คณะบุคคล)
- Architecture design ยังไม่ละเอียดพอ
- ยังมี English terms ปนบ้างในบางคำตอบ

### Performance Metrics
- **Average tokens/response**: 715 tokens
- **Average response time**: 19.2 seconds (CPU mode)
- **Throughput**: ~37 tokens/second

### Key Findings
1. **Thai-Only Prefix ช่วยได้มาก**: การเพิ่ม "ตอบเป็นภาษาไทยเท่านั้น:" ช่วยปรับปรุงคุณภาพคำตอบ 8 จาก 10 tests
2. **Pattern Recognition ปรับปรุงมาก**: จาก ❌ Poor เป็น ✅ Excellent
3. **Math Accuracy ดีขึ้น**: คำนวณได้ถูกต้องหลังเพิ่ม prefix
4. **ลด Chinese Characters**: แทบไม่มี Chinese characters ในคำตอบ

### Recommendation
การเพิ่ม "ตอบเป็นภาษาไทยเท่านั้น:" ช่วยปรับปรุงคุณภาพคำตอบได้ดี แต่สำหรับ production use ยังควรใช้รุ่นที่ใหญ่กว่า (qwen2.5:7b หรือ qwen2.5:14b) เพื่อ:
- ความแม่นยำทางคณิตศาสตร์ที่ดีขึ้น
- ความเข้าใจภาษาไทยเชิงลึก (ราชาศัพท์, ศาสนา)
- ความรู้เฉพาะทาง (กฎหมาย, architecture)
