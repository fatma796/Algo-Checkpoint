# Sentence Analyzer

##  Exercice Description
This project is a simple program that analyzes a sentence by counting the number of **characters**, **words**, and **vowels**. 
The algorithm uses a loop to read through the sentence and updates counters accordingly.

##  Algorithm Overview
The algorithm reads a sentence entered by the user, then counts:
1. **Characters**: Every character except the period at the end.
2. **Words**: Counted by detecting spaces.
3. **Vowels**: Identified by checking for the characters `a, e, i, o, u`.

##  Code
```
ALGORITHM Count_CountSentenceLength,Words,AndVowels
VAR
    str: STRING  // This VAR is used to store the sentence.
    i: INTEGER   // This VAR is used as an index for the loop.
    NB_C, NB_V: INTEGER := 0  // This VAR will count the number of characters and vowels.
    NB_W: INTEGER := 1    // This VAR will count the number of words.
BEGIN
    write("Enter a sentence")
    read(str)
    WHILE (str(i) <> ".") DO // Loop until the period is found.
        NB_C = NB_C + 1 // We add the Character counter by 1 for each character found.
        IF (str(i) = " ") THEN  
            NB_W = NB_W + 1   // We add the Words counter by 1 if we found a space.
        END_IF
        IF (str(i) = ("a", "e", "i", "u", "o")) THEN 
            NB_V = NB_V + 1   // We add the Vowels counter by 1 if we found a vowel.
        END_IF
        i++
    END_WHILE
    write(NB_C)
    write(NB_V)
    write(NB_W)
END
