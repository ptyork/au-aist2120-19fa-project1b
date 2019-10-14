# Project 1b: Word Mirror 

This is a simple little utility with a twist. I can't really think of a useful purpose for this particular script in real life, but the general concept of parsing and modifying a file word-by-word is VERY useful. Regardless, the goal is to reverse the letters of each individual word in a given input file. 

The script, wmirror.py, should: 

1. Ask the user for a file name 
2. Open the requested file 
3. Split the contents of the file into words 
4. Iterate over each word 
5. Reverse the letters of the word 
6. Output the mirrored word to the screen 

__THE HARD'ISH PART__: When splitting out the words, be careful to check the LAST character of the word. If it's punctuation, be sure to deal with that correctly. In other words, "well, let's go." should be "llew, s'tel og." NOT ",llew s'tel .og" 

## REQUIRED IMPLEMENTATION NOTES 

1. You MUST abstract your most useful logic by creating a function named mirror that takes a word and returns the reversed version (properly handling the punctuation issue outlined above). This function should be "called" as your step 5 above, which will make the main script much cleaner. So to reiterate, the following function MUST be in your code: 

``` 
        def mirror(word): 
            ....
``` 

2. You MUST modify getty.txt, replacing Abraham Lincoln's name with your own. 

3. You MUST then mirror getty.txt and redirect the output to mirror-getty.txt. In other words, you should run `python wmirror.py > mirror-getty.txt` and select getty.txt when prompted. Include this file in your final submission. 

## LOGISTICS 

Same basic deal as with the homeworks. 

1. From your AIST2120 folder, run `git clone [URL]` to make a local copy of this assignment. 
2. DO THE WORK 
3. TEST YOUR WORK A WHOLE LOT 
4. TEST IT SOME MORE LIKE YOU MEAN IT THIS TIME 
5. When done, run `git add .` 
6. Then run `git commit –m "type a clever message here"` 
7. Finally run `git push` to push your changes back up to GitHub 
8. Breathe a sigh of relief 

## OPTIONAL CHALLENGES 

1. Create a second version of the script, wmirror2.py. This version should import the mirror function from wmirror (`from wmirror import mirror`). Instead of asking for a file name and reading the text from the file, instead read in the text line-by-line from sys.stdin. This should allow you to run it interactively AND to pipe in text from another command (e.g., `type getty.txt | python wmirror.py`). 

2. Instead of mirroring the words, scramble them. In other words, use every letter, but randomly. This is challenging, but doable. You will need to use the randint() function from the random module. Hint: consider converting each word to a list of characters and then "pop()" a letter from a random location in the word until all characters are used. Assuming your list of characters in called word, something like `ch = word.pop(randint(0,len(word)))` might be useful code here.
