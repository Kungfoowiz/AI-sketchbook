---  
name: engine  
description: Multi-agent AI that asks the user for a numbered list of questions in a file and a target folder of information. The AI will then answer all the questions from file, with 3 subagents, process-1 for first third of questions, process-2 for middle third of questions, process-3 for last third of questions. The 3 process subagents will answer questions on the information in the target folder. The AI will then combine all answers into a single output file, with 1 subagent, combine. Then the AI will review all the answers in the single output file, with 3 subagents, review-1 for coherency, review-2 for sourcing, and review-3 for missed information.   
disable-model-invocation: true  
---  

# Task  
1. ALWAYS ask the user for the:
  1.1. Target name. Show user example: `Name`
  1.2. Input questions. Show user exmaple: `C:\questions.md`
  1.3. Target folder. Show user example: `C:\target`  
  1.4. Combined answers file. Show user example: `C:\combined-answers.md`

3. Create the combined answers file and set: target name, and question, target, and output locations.

4. Answer all questions in the questions file, by running subagents, with prompts from `agents/` subfolder: 3 process, 1 combine, 3 review, in order.

5. After all subagents, ask the user to paste in the output of /cost, and then add the following to the combined answers file:
  5.1. Total time.
  5.2. Cost.
  5.3. Tokens used.

# Guardrails  
1. Run 3 **process** subagents on Sonnet model, in order, using files as prompts: `process-1.md`, then `process-2.md`, then `process-3.md`.
  1.1. Give each process subagent the questions, target folder, and rules only.  

2. After all process subagents finish, then run the **combine** subagent on Haiku model, using file prompt `combine.md`. 
  2.1. Give the combine subagent all process output files and rules only.  

3. After the combine subagent finishes, run 3 **review** subagents on Opus model, in order, using files as prompts: `review-1.md`, then `review-2.md`, then `review-3.md`.
  3.1. Give each review subagent the questions, target folder, the combined answers file, and rules only.  

4. All review subagents can flag problems, edit answers in the combined answers file, but do not block finishing all reviews.  

5. No review subagent can retry a failed review.  

6. Rules must ALWAYS be followed in `reference/rules.md`.  

# Exit criteria  
1. All 7 subagents are finished.  
2. Target name, and question, target, and combined answers locations are added to the combined answers file.  
3. Subagent statuses, total time, cost, and tokens used information are added to the combined answers file.  
