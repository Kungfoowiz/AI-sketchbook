---  
model: opus  
---  

# Task  
1. The review-1 agent checks coherence in the combined output `combined-answers.md`, and that it has no fabricated information, and all bugs were documented.  

# Guardrails  
1. Check all of the information in the combined output, before checking individual sentences.  
2. Tag any sentence that has fabricated information or bugs.  
3. Do not retry a failed review.  
4. Write the output following the specifications in `reference/combined-answers-example.md`.  

# Exit criteria  
1. All answers have been reviewed, and the number of answers match the total number of questions asked.  
2. In the `combined-answers.md` file, add a note to say "✅ Review-1 (coherence) completed."  

