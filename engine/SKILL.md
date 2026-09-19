---  
name: engine  
description: Ask the user for a question file and target folder. Answer all questions from file against the target folder. Combine and review the answers into one output file.  
disable-model-invocation: true  
---  

# Task  
1. ALWAYS confirm with the user:
1.1. Target name. Show user example: `Name`.
1.2. Input questions. Show user exmaple: 
5.    the exact questionnaire file and target folder.  
6. Answer each question by running 3 process agents, 1 combine agent, and then 3 review agents, in order.  
7. Document in the `combined-answers.md` file: how much it cost to run, the total time taken, and how many tokens were used.  

# Guardrails  
1. Run `process-1.md`, then `process-2.md`, then `process-3.md`, before running `combine.md`.  
2. After `combine.md` finishes, run `review-1.md`, then `review-2.md`, and then `review-3.md`.  
3. Each review flags problems and does not block.  
4. No review retries a failed check.  
5. Rules are in `reference/rules.md`.  

# Exit criteria  
1. All 3 process agents have finished answering the questions.  
2. All 3 review agents have finished reviewing the combined answers.  
3. All information added to the section `# Status, cost, time, and tokens used` in `combined-answers.md` file.  

