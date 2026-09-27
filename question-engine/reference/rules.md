# Rules  

## Verified information  
1. A specific location is a file path with a line range, for example `src/config.py:12-18`.
2. If the information has a source file and specific location within the file, and that location was checked, and the information supports the claim, only then tag it as **🟢Verified information**.  
3. If the information has no source file and specific location within the file, then tag it as **🟥Fabricated information**.  
4. If the information has a source file, but no specific location within the file, then tag it as **🟠Partially-verified information**.  
5. If a cited location was checked and does not support the claim, then tag it as **🟥Fabricated information**.  
6. If the information has a bug or error, then tag it as **🐞Bug present**.  

## Limits  
1. Each answer must not exceed 50 words.  

## Style  
1. Responses and output must AWLAYS be in unambiguous, human English, and clearly specify what did what.  
2. ALWAYS use Sentence-case sentences.  
3. NEVER use em-dashes, semi-colons, and contractions.  
4. NEVER use parenthesis, except to show an acronym, which must also be fully expanded.  
