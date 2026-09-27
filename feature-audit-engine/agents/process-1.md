---
name: process-1
description: Retell a feature in a chosen theme with a diagram, list existing bugs, then give an overview of unit, integration, and end-to-end testing gaps, and estimate the effort to automate them, in working days, for Devin AI and one automation tester.
---

# Task  
1. Analyse each feature in the answers file.  

2. One feature at a time, write the following information into the specified output file:  
    2.1. Step-by-step explain how the feature works, and pair it with a retelling in the specified theme.  
    2.2. Create a Mermaid diagram, picturing how the steps work.  
    
3. Summarising all features, write the following information into the specified output file:
    3.1. Known bugs.
    3.2. Give a general overview of the gaps in unit, integration, and end-to-end (E2E) testing.  
    3.3. Estimate how long, in working days, the testing gaps will take for Devin AI and 1 automation tester to do.  

# Guardrails  
1. Analyse only target features, specified in the answers file.  
2. Always cite exact source files and locations.  
3. Write changes to the output file, following the output specification.  
4. Each feature step-by-step explanation must not exceed 150 words.  
5. Mermaid diagrams must not need zooming at all, to see the whole picture clearly, with simple, visible text.  
6. A maximum of 5 known bugs to be listed only, not exceeding 50 words each, and ordered by highest to lowest risk.
7. General overview of gaps in testing must not exceed 200 words.  


# Exit criteria  
1. All features from the answers file, explained in detailed steps, paired with retellings and Mermaid diagrams.  
2. Summarised for all the features: 
    2.1. A numbered, detailed list of bugs, referencing features. 
    2.2. An estimate for the testing gaps.
3. Cited source files, which are tagged verified, fabricated, or partially-verified.  
4. In the output file, add a note to say "✅ Process-1 audit completed."