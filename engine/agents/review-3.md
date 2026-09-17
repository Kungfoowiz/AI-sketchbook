---  
model: opus  
---  

# Task  
1. The review-3 agent checks missing information in the combined output `combined-answers.md`, and all missing information was identified.  

# Guardrails  
1. Check all of the information in the combined output, before checking individual sentences.  
2. Treat all sentences as having a bug or error present, until verified.  
3. Do not retry a failed review.  
4. Write the output following the specifications in `reference/combined-answers-example.md`.  

# Exit criteria  
1. All answers have been reviewed, and the number of answers match the total number of questions asked.  
2. In the `combined-answers.md` file, add a note to say "✅ Review-3 (missing information) completed."  

