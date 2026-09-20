# ✨ Claude AI knowledge and reusability  


Claude AI's knowledge is stored in CLAUDE.md Markdown file in the main project folder.  

It stores learning without you reasking Claude AI.  

More learning can be added and you can also have reusable flows called skills.  

  
### 🧠 Claude.md example
``` 
# Test project.

## My learning.
@focus.md  
@report-format.md  
@data.md  

## How I work?
1. Answers must follow instructions from my learning.
2. Run only what's asked.
3. Use /run-all-tests to do all testing.
```

### focus.md example
```
# Focus

1. Analysis accuracy is actual analysis checked against evidence.
2. Test coverage is calculated in percentages of all types of testing from a test strategy.
3. Known past issues were incorrect evidence and scenario counts from actual analysis.
```

### data.md example
```
# Data

1. Always ask the user to confirm all actual input to reusable flows.
2. Always ask the user to confirm all expected output to reusable flows.
3. Test coverage comes from checking the code.
4. Missing or bad data is flagged as a bug.
```

### report-format.md example
```
# Report format

Reports should:
1. State what was measured.
2. Show numbers plainly, examples: found vs. expected, coverage %.
3. Flag bugs clearly, do not hide anything.
4. Suggest next steps only when we need to do something.
```

### .claude/skills/get-analysis-accuracy/SKILL.md reusable flow
```
---
name: get-analysis-accuracy
description: Use when the user asks to check, verify, or get the accuracy of the analysis output against actual evidence.
---

# Get analysis accuracy.

1. Use the rules in data.md.
1. Load the actual inputted analysis.
2. Count the number of actual evidences.
3. Compare it to the number of evidences the user found in expected output.
4. Show the analysis evidence count, the expected evidence count and bugs.
```

### .claude/skills/get-test-coverage/SKILL.md reusable flow
```
---
name: get-test-coverage
description: The user asks for test coverage of code or how well something is tested.
---

# Get test coverage

1. Use the rules in focus.md and data.md.
2. Find information about the test coverage.
3. Summarise test coverage by scenarios and then test types based on the test strategy.
4. Flag bugs for less than full coverage.
```

### .claude/skills/report-test-plan-suggestions/SKILL.md reusable flow
```
---
name: report-test-plan-suggestions
description: Creates test plan suggestions from analysis, accuracy, test coverage and bugs.
---

# Report test plan suggestions.

1. Use the rules in focus.md, data.md, and report-format.md.
2. Use the inputted actual analysis.
3. Use the inputted test strategy.
3. Use outputs of get-analysis-accuracy and get-test-coverage skills.
4. Identify all quality escapes, including risks and endurance testing gaps.
5. Suggest one important next step only.
6. Show an estimated test plan, based on quality escape, risks, testing gaps and for each scenario and the percentage for each testing type.
```

### .claude/skills/run-all-tests/SKILL.md reusable flow
```
---
name: run-all-tests
description: Run all tests in order.
---
# Run all tests.
1. Run get-analysis-accuracy skill.
2. Run get-test-coverage skill.
3. Run report-test-plan-suggestions skill using outputs from 1 and 2.
4. Create a combined report using report-format.md.
```
