# World Values Survey Datasets

## **Overview**
This repository provides a derived dataset based on the **World Values Survey (WVS) Wave 7 (2017–2022)**.  
The dataset contains:

- Question texts
- Multiple-choice response options
- Aggregated response distributions
- WVS category labels

---

## **Data Generation Process**
The dataset was generated through the following steps:

1. **Excluding demographic items** (e.g., age, gender) and selecting a subset of survey questions
2. **Machine-translating English questions** into **Chinese**, **Japanese**, and **Arabic**  
   _No manual post-editing was performed_
3. **Extracting aggregated response distributions**  
   Likert-type option percentages obtained from WVS results
4. **Assigning official WVS category labels**, such as:
   - Social Values
   - Well-being / Subjective Well-being
   - Politics / Institutions
   - Religion
   - Morality / Ethics
   - Gender / Family
   - Trust  
   - …etc.

---

## **Data Format**
Each record contains:

- Question text (EN + translated variants)
- Options
- Aggregated distribution
- Category label
- Country information


---

## **Example Record**
Below is an example of a JSON record contained in this dataset:

```json
{
  "id": "Q1",
  "question_id": "1",
  "topic": "SOCIAL VALUES",
  "question_text": "How important is family in your life?",
  "options": [
    "1. Very important",
    "2. Rather important",
    "3. Not very important",
    "4. Not at all important"
  ],
  "most_common_response": "1",
  "distribution": {
    "1": 0.91,
    "2": 0.07,
    "3": 0.01,
    "4": 0.0
  }
}

## **Source**
Original survey data:  
**World Values Survey (WVS) Wave 7 (2017–2022)**  
<https://www.worldvaluessurvey.org/WVSDocumentationWV7.jsp>

Users must follow the official WVS usage and citation policy when using this dataset.

