# SkillsQuark Task 3 – Validation Test Cases

## Test Case 1 – Direct document question

Document:
`data/sample_knowledge.txt`

Question:
"What is the purpose of the project?"

Expected:
The chatbot should explain that the project is designed to demonstrate a custom document-question-answering chatbot using uploaded files and retrieval.

Result:
Record the actual output and mark PASS/FAIL.

## Test Case 2 – Multi-part question

Question:
"What are the main features and who are the target users?"

Expected:
The answer should contain information about both the features and target users, based only on the document.

Result:
Record the actual output and mark PASS/FAIL.

## Test Case 3 – Unknown information

Question:
"What is the company's annual revenue?"

Expected:
The sample document does not contain revenue information. The chatbot should say it cannot find that information rather than inventing a number.

Result:
Record the actual output and mark PASS/FAIL.

## Test Case 4 – PDF test

Upload any text-based PDF related to a college/project topic.

Question:
Ask a factual question whose answer is clearly present in the PDF.

Expected:
The chatbot should answer using the PDF and show retrieved passages/source information.

Result:
Record the actual output and mark PASS/FAIL.

## Validation table

| Test | Input | Expected behaviour | Actual result | Status |
|---|---|---|---|---|
| 1 | Project-purpose question | Relevant answer | Fill after running | PASS/FAIL |
| 2 | Multi-part question | Complete contextual answer | Fill after running | PASS/FAIL |
| 3 | Unknown question | No fabricated answer | Fill after running | PASS/FAIL |
| 4 | PDF question | Answer grounded in PDF | Fill after running | PASS/FAIL |
