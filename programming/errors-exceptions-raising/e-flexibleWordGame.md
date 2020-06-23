#### Exercise : Flexible Word Game

Implement a word game similar to the one you implement in the <trigger trigger="click" for="modal:flexibleWordGame-wordGame">previous Word Game Exercise</trigger>, but with the following difference:
* The player is asked to choose the word size. The word size can only be 4 to 8 (both inclusive). If the user entry is not an integer or not in the range 4..8, the program keeps asking for the word size.
 
<modal large header="%%Programming Basics → Lists → List Methods%%" id="modal:flexibleWordGame-wordGame">
  <include src="../lists-methods/e-wordGame.md"/>
</modal>
 
Given below is a sample session. Try to follow the exact output format in your implementation:
```
========================================================
Welcome to the FLEXIBLE WORD GAME
Enter the word size (4 to 8): xyz
That is not a number. Try again
Enter the word size (4 to 8): 3
Number not in correct range. Try again
Enter the word size (4 to 8): 5
Give all 5-letter words you know, one word at a time
Enter the word 'end' to exit
========================================================
What's the next word?  frame
What's the next word?  great
What's the next word?  treat
What's the next word?  fat
Not a 5-letter word
What's the next word?  creamy
Not a 5-letter word
What's the next word?  treat
Repeated word! treat is number 3 in the accepted words list.
treat is no longer an accepted word and is banned
What's the next word?  crime
What's the next word?  treat
treat is banned!
What's the next word?  end
========================================================
Your score: 3
Accepted words (in order of entry): frame great crime
Accepted words (in sorted order): crime frame great
Banned words (in sorted order): treat
Thank you for playing the FLEXIBLE WORD GAME
========================================================
``` 
