Algorithm SentenceAnalysis
Variables:
    char c
    integer length ← 0
    integer words ← 1       // Start with 1 word unless sentence is empty
    integer vowels ← 0

Begin
    Read first character c
    
    While c ≠ '.'
        length ← length + 1
        
        // Count vowels (both uppercase and lowercase)
        If c in ['a','e','i','o','u','A','E','I','O','U'] then
            vowels ← vowels + 1
        EndIf
        
        // Count words when space is found
        If c = ' ' then
            words ← words + 1
        EndIf
        
        Read next character c
    EndWhile
    
    // Add the period to the sentence length
    length ← length + 1

    Write "Sentence length: ", length
    Write "Number of words: ", words
    Write "Number of vowels: ", vowels
End
