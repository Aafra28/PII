# PII- Parliamentary Inquiry Insights(Lok Sabha Edition)
## Overview
This project aims to analyze questions asked in the Lok Sabha (House of the People - lower house of the Indian Parliament) during its Seventeenth (17th) Session. The dataset includes 4750 questions from November 29, 2021, to December 23, 2021, sourced from PDFs available on the Official Lok Sabha Website.

## Dataset Information
The dataset provides detailed information for each question, including:
- **Question ID:** The official question number.
- **Question Type:** Type of question (starred/unstarred).
- **Question Date:** Session Date in which the question was presented.
- **Question From:** Asking Member(s) of Parliament.
- **Question To:** Ministry/Department sought in the question.
- **Question Topic:** Topic of the question.
- **Question Contents:** Question body.
- **Member Party:** Political affiliation of the Asking Member.
- **Member State:** Asking Member's state.
- **Member Constituency:** Asking Member's constituency.
- **Member Constituency Type:** Asking Member's constituency type.

## Challenges and Data Processing
Parsing PDFs of session questions presented significant challenges due to a large volume of data and typing inconsistencies. Mapping MPs' names was particularly difficult, given variations like "Shri Sunil Kumar Singh," "Shri S.K. Singh," etc. Fuzzy matching of Indian names, facilitated by thefuzz, was employed to address this issue.

## Dataset Files
The project includes two CSV files:
1. **questions.csv:** Contains 4250 entries representing individual questions.
2. **questions_flattened.csv:** An augmented version addressing the many-to-many relationship, with 7050 entries, where multiple MPs may ask a single question, and a single MP may ask multiple questions.

## Key Questions for Analysis
The project aims to answer several questions, including but not limited to:
- What questions were asked by a specific MP?
- What questions were asked from a particular state?
- How many questions were asked on a specific topic?
- Are there trends in questions asked by MPs, and is there any correlation with their political affiliations?

## Note
- The data is publicly available at http://loksabhaph.nic.in/Questions/questionlist.aspx as of December 15, 2021.
- The project involves text analytics, natural language processing, and semantic parsing of complex and messy data, making it prone to errors.

**Disclaimer:** Any information presented here is an interpretation and should not be used as a substitute for real data.
