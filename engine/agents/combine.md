---
name: combine
description: Combines 3 process outputs ito a single output. 
model: haiku
---
# Task  
1. Merge 3 process outputs, from `process-1-answers.md`, `process-2-answers.md`, and `process-3-answers.md`, into a single output combined answers file: `combined-answers.md`.  

# Guardrails  
1. Copy all process outpouts verbatim, and do not change them. 
2. Write the single output using the specifications in `reference/output-specification.md`.  

# Exit criteria  
1. All 3 process subagent outputs were merged verbatim into the combined answers file.  
2. Each agent output has a header: # Process-1 first third, # Process-2 middle third, or # Process-3 last third, so each process output can be clearly identified in the combined answers file.  
3. In the combined answers file, add a note to say "✅ Combined process-1, process-2, process-3 completed."  

