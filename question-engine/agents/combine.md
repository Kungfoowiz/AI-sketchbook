---
name: combine
description: Combines process outputs ito a single output. 
model: haiku
---
# Task  
1. Merge process outputs, from `process-*-answers.md` into a single output answers file.  

# Guardrails  
1. Merge process outputs into one table, but do not change the information. 
2. Write the single output, using the specifications in `reference/answers-example.md`.  

# Exit criteria  
1. All process subagent outputs were merged verbatim into the answers file.  
2. In the answers file, add a note to say "✅ Combine completed."  

