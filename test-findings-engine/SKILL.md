---
name: test-findings-engine
description: Analyses a code project, using optional documentation and a current test strategy, and identifies the highest-risk issues across correctness, architecture, maintainability, testability, security, and operational resilience.
disable-model-invocation: true
---

# Task  
1. Ask the user for a target project folder (required), a target documentation folder (optional), and a current test strategy document (optional).  
2. Read the target project folder, and the documentation folder and test strategy document if given.  
3. Analyse the codebase for correctness, architecture, maintainability, testability, testing strategy, security, operational resilience, and performance.  
4. Identify the 5 highest-risk findings, ranked by impact on system health, reliability, security, and future development velocity.  
5. Write the findings to `test-strategy-findings.md`, as a Markdown table with columns `Title | Description | Risk`, ordered highest risk first.  

# Guardrails  
1. Base findings only on the target project folder and, if given, the documentation folder and test strategy document.  
2. Cite exact source files and line ranges within each `Description`.  
3. Grade `Risk` as Critical, High, Medium, or Low, and order findings highest risk first.  
4. Keep each `Description` to a maximum of 200 words.  
5. Cover correctness, architecture, maintainability, testability, testing strategy, security, operational resilience, and performance, at least once each.  
6. Prefer objective engineering concerns over stylistic preferences, avoiding formatting or linting issues unless they create material risk, and avoiding duplicate findings for the same underlying issue.  

# Exit criteria  
1. `test-strategy-findings.md` exists, with exactly 5 findings, ordered highest-risk first, each citing exact file paths and line ranges within a `Description` under 200 words.  

