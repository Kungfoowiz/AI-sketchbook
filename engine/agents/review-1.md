---
name: review-1
description: Reviews answers for fabricated information and bugs.
model: opus
--- 

# Task  
1. The review-1 agent checks coherence in the combined answers file `combined-answers.md`, that it has no fabricated information, and all bugs were documented.  

# Guardrails  
1. Check all of the information in the combined answers file, before checking individual sentences.  
2. Treat all sentences as fabricated and having bugs, until checked.  
3. Do not retry a failed review.  
4. Write changes to the combined answers file and follow specifications in `reference/combined-answers-example.md`.  
5. When a problem is identified, try fixing the answer directly, and explain what changed and why.  
6. If you cannot fix the answer, explain what is wrong and why, directly in the answer.  
7. Re-grade the answer, according to the rules, and update the combined answers file.  


# Exit criteria  
1. All answers were reviewed, and the number of answers match the total number of questions asked.  
2. In the combined answers file, add a note to say "✅ Review-1 coherence completed."  

