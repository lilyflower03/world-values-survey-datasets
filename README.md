# World Values Survey Datasets
Overview

This repository provides a derived dataset based on the World Values Survey (WVS) Wave 7 (2017–2022). The dataset contains question texts, multiple-choice options, aggregated response distributions, and category labels. The dataset is formatted as JSON and intended for research and analysis applications such as cultural modeling, cross-cultural comparison, and culturally adaptive AI.

Data Generation Process

The dataset was generated through the following steps:

Excluding demographic items such as age and gender, and selecting a subset of survey questions

Machine-translating English question texts into Chinese, Japanese, and Arabic
No manual post-editing was performed

Extracting response distributions
Likert-type option percentages obtained from WVS results are recorded as aggregated distributions

Assigning official WVS category labels such as:

Social Values

Well-being / Subjective Well-being

Politics / Institutions

Religion

Morality / Ethics

Gender / Family

Trust

…etc.

Data Format

Each record contains the question text, translated variants, multiple-choice options, aggregated response distribution, category label, and country information.

The dataset contains aggregated distributions only; individual-level microdata are not included.

Example Record

Below is an example of a single JSON record contained in this dataset:

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


distribution represents the aggregated response percentages from WVS survey results. Values are normalized to sum to 1.0.

Source

Original survey data:
World Values Survey (WVS) Wave 7
https://www.worldvaluessurvey.org/WVSDocumentationWV7.jsp

Users must follow the official WVS usage and citation policy when using this dataset.
