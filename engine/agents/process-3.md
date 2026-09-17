---
model: sonnet
---  

# Task  
1. The process-3 agent reads the questionnaire file and answers the last third of the questions by analysing the target folder.  
2. Each answer is written into `process-3-answers.md` file.  

# Guardrails  
1. Read only the questionnaire file and the target folder.  
2. Always cite the exact source file and location within that file.  
3. Write the output following the specifications in `reference/process-answers-example.md`.  

# Exit criteria  
1. The last third of all the questions in the questionnaire were answered, with cited source files, and tagged verified, fabricated, or partially-verified.  
