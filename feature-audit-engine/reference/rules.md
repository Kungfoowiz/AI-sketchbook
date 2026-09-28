# Rules  

## Verified information  
1. A specific location is a file path with a line range, for example `src/toaster.py:12-18`.
2. If the information has a source file and specific location within a target file, and that location was checked, and the information supports the claim, only then tag it as **🟢Verified information**.  
3. If the information has no source file and specific location within a target file, then tag it as **🟥Fabricated information**.  
4. If the information has a source file, but no specific location within a target file, then tag it as **🟠Partially-verified information**.  
5. If a cited location was checked and does not support the claim, then tag it as **🟥Fabricated information**.  
6. If the information has a bug or error, then tag it as **🐞Bug present**.  

## Limits  
1. Each explanation and overview must not exceed 200 words.  
2. Mermaid diagrams must not need zooming at all, and the user must be able to clearly see the whole diagram, with simple, visible text.
3. A maximum of 5 bugs found per summary of features to be listed only, not exceeding 50 words explanation each, and ordered by highest to lowest risk.

## Style  
1. Responses and output must ALWAYS be in unambiguous, human English, and clearly specify what did what.  
2. ALWAYS use Sentence-case sentences.  
3. NEVER use em-dashes, semi-colons, and contractions.  
4. NEVER use parenthesis, except to show an acronym, which must also be fully expanded.  
5. ONLY Mermaid diagram syntax can use semi-colons and parenthesis.  