---  
name: feature-audit-engine  
description: Retell features in a chosen theme with diagrams, identifying how they are currently tested, and list existing bugs. Then estimate required unit, integration, and end‑to‑end (E2E) testing, and estimate the effort for automating the tests, by Devin AI or 1 tester.
disable-model-invocation: true  
---  

# Task  
1. ALWAYS ask the user for the:
  1.1. Target name. Show user example: `Name`
  1.2. Theme. Show user example: `Pirates`
  1.3. Target folder. Show user example: `C:\target`  
  1.4. Answers file. Show user exmaple: `C:\answers.md`
  1.5. Output file. Show user example: `C:\target.md`

2. Create the output file and set: target name and theme, and target, answers, and output locations.

3. Run subagents, with prompts from `agents/` subfolder: 1 process, then 3 reviews, in order.

4. After all subagents are finished, then ask the user to paste in the output of /cost, and add the following to the output file:
  4.1. Total time.
  4.2. Cost.
  4.3. Tokens used.

# Guardrails  
1. Run **process** subagent on Sonnet model, using this file as a prompt: `process-1.md`.
  1.1. Give the process subagent the theme, target folder, answers file, output file, and rules only.  

2. After the process subagent finishes, run 3 **review** subagents on Opus model, in order, using files as prompts: `review-1.md`, then `review-2.md`, then `review-3.md`.
  2.1. Give each review subagent the theme, target folder, answers file, output file, and rules only.  

3. All review subagents can flag problems, edit answers in the output file, but do not block finishing all reviews.  
  3.1. No review subagent can retry a failed review.  

4. Rules must ALWAYS be followed in `reference/rules.md`.  

# Exit criteria  
1. All 4 subagents are finished.  
2. Target name and theme, and target folder, answers, and output locations are added to the output file.  
3. Subagent statuses, total time, cost, and tokens used information are added to the combined answers file.  
