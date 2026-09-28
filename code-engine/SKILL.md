---
name: test-strategy-engine
description: Creates 2 independent test strategies in Markdown for a fully automated Claude Code AI testing lifecycle, using fully synthetic test data end-to-end and prioritising highest risks first.
disable-model-invocation: true
---

# Task  
1. Read the current test strategy file, the Question Engine answers file, and the Feature Audit Engine output file.  
2. Analyse the 3 files and write a new test strategy in Markdown to `test-strategy-1.md`, for a fully automated Claude Code AI testing lifecycle, using fully synthetic test data end-to-end, prioritising the highest risks first.  
3. Repeat step 2 once more, ignoring the previous test strategy, and save to `test-strategy-2.md`.  

# Guardrails  
1. Never copy text from a previous test strategy.  
2. Keep each test strategy under 500 words.  

# Exit criteria  
1. `test-strategy-1.md` and `test-strategy-2.md` both exist.  
2. Each file was created from an independent analysis of the same 3 source files.  
