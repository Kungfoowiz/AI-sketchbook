---  
name: engine  
description: Ask the user for a question file and target folder. Answer all questions from file against the target folder. Combine and review the answers into one output file.  
disable-model-invocation: true  
---  

# Task  
1. ALWAYS confirm with the user:
  1.1. Target name. Show user example: `Name`
  1.2. Input questions. Show user exmaple: `C:\questions.md`
  1.3. Target folder. Show user example: `C:\target`  
  1.3. Combined answers file. Show user example: `C:\combined-answers.md`

3. Create combined answers file and set: target name, and question, target, and output locations.

4. Answer all questions in the questions file, by running subagents, with prompts from `agents/` subfolder: 3 process, 1 combine, 3 review, in order.

5. After all subagents, ask the user to paste in the output of /cost, and then add the following to the combined answers file:
  4.1. Total time.
  4.2. Cost.
  4.3. Tokens used.

# Guardrails  
1. Run each process subagent on Sonnet model, in order, using files as promots: `process-1.md`, then `process-2.md`, then `process-3.md`.
  1.1. Give each process subagent the questions and target folder only.

2. After all process subagents finish, then run combine subagent on Haiku model, using file 

3. After all 


4. After `combine.md` finishes, run `review-1.md`, then `review-2.md`, and then `review-3.md`.  
5. Each review flags problems and does not block.  
6. No review retries a failed check.  
7. Rules are in `reference/rules.md`.  

# Exit criteria  
1. All 3 process agents have finished answering the questions.  
2. All 3 review agents have finished reviewing the combined answers.  
3. All information added to the section `# Status, cost, time, and tokens used` in `combined-answers.md` file.  

