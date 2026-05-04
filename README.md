# IT3040 - ITPM Assignment 1: Transliteration Accuracy Testing

**Course:** BSc (Hons) in Information Technology, Year 3
**Module:** IT3040 – ITPM
**Semester:** Semester 1
**Assignment:** Assignment 1 - Option 1

---

## Objective

Test the Chat Sinhala transliteration function at:
https://www.pixelssuite.com/chat-translator

Identify **50 test cases** where the system fails to convert chat-style **Singlish into Sinhala correctly**.

---

**Registration Number:** IT23206946
**Submission Date:** 5th May 2026
**GitHub Repository:** https://github.com/chathumi-dot/IT3040-chat-singlish-transliteration-testing

---

## Prerequisites

* Python 3.11 or 3.12
* Google Chrome (recommended)

---

## Installation

1. Clone the repository:

```bash
git clone https://github.com/chathumi-dot/IT3040-chat-singlish-transliteration-testing.git
cd IT3040-chat-singlish-transliteration-testing
```

2. Install dependencies:

```bash
pip install -U pip
pip install playwright openpyxl
playwright install
```

---

## Run Tests

Execute the following command from the project directory:

```bash
python test_automation.py --excel "Assignment 1 - Test cases.xlsx" --url "https://www.pixelssuite.com/chat-translator" --wait-ms 5000 --type-delay-ms 80 --slow-mo-ms 200 --save-every 1 --keep-open
```

---

## Test Cases

* **Total:** 50 test cases
* **Distribution:**

  * 2 test cases per each of 24 Singlish input types (48)
  * * 2 additional test cases

### Input Types Covered

* Question forms
* Command forms
* Greetings
* Requests
* Responses
* Repeated Words
* Inputs with Punctuation Marks
* Romanization/Spelling Variants
* Isolated English Word Insertions
* Multi-Word English Phrases
* English Digital Terms
* Platform/App Names
* English Abbreviations/Acronyms
* English Clipped Forms
* Place Names Embedded in Singlish
* Person Names Embedded in Singlish
* Inputs with Numbers and Numeric Suffixes
* Inputs with Currency
* Inputs with Time Formats
* Inputs with Dates
* Inputs with Unit of Measurements
* Inputs with Slang and Casual Phrasing
* Online Identifiers in Singlish
* Inputs Containing Emojis

---

## Output

The script updates **Assignment 1 - Test cases.xlsx** with:

* Actual output from the application
* Pass/Fail status for each test case

### Manual Additions (after automation)

Add two columns to the Excel file:

* Singlish input types covered
* Evidence or rationale for the input type covered

---

## Repository Structure

```
IT3040-chat-singlish-transliteration-testing/
├── test_automation.py              # Main Playwright automation script
├── Assignment 1 - Test cases.xlsx  # Test cases Excel file
├── README.md                       # This file
├── requirements.txt                # Python dependencies (if any)
└── .gitignore                      # Git ignore file
```

---

## Command Parameters

| Parameter       | Description                           | Value                                       |
| --------------- | ------------------------------------- | ------------------------------------------- |
| --excel         | Path to Excel test cases file         | Assignment 1 - Test cases.xlsx              |
| --url           | Target application URL                | https://www.pixelssuite.com/chat-translator |
| --wait-ms       | Wait time after page load             | 5000 ms                                     |
| --type-delay-ms | Delay between keystrokes              | 80 ms                                       |
| --slow-mo-ms    | Slow motion execution speed           | 200 ms                                      |
| --save-every    | Save results after every N test cases | 1                                           |
| --keep-open     | Keep browser open after execution     | Flag                                        |

---
