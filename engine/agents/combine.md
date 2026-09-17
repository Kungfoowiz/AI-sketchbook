---  
model: sonnet  
---  
# Task  
1. Merge 3 process outputs, from `process-1`, `process-2`, and `process-3`, into a single output `combined-answers.md`.  

# Guardrails  
1. Copy all process outpouts verbatim, and do not change them. 
2. Write the single output using the specifications in `reference/output-specification.md`.  

# Exit criteria  
1. All 3 process agent outputs have been combined into `combined-answers.md` file.  
2. Each agent output has a header: # Process-1 (first third), # Process-2 (middle third), or # Process (last third), so each process output can be clearly identified in the `combined-answers.md` file.  
3. In the `combined-answers.md` file, add a note to say "✅ Combined (process-1, process-2, process-3) completed."  

