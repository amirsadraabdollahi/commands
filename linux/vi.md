# Vi

### modes
- insert
- command

1. move in file
- h: left
- j: down
- k: up
- l: right
- w: next word in the current line
- e: next end of word in the current line
- b: previous begining of the word in the current line
- Ctrl+f: scroll forward one page
- Ctrl+b: scroll backward one page
- G(capital): with no number, will jump to then end. but 10G will jump to line 10
- H(capital): with no number, will jump to first line in the current screen. 5H will jump to the 5th line from the top of the screen (the current screen not all the file).
- H(capital): with no number, will jump to last line in the current screen. 5L will jump to the 5th line from the bottom of the screen (the current screen not all the file).

2. some useful keys
- r: replace only one character
- o: open new line below the curser and go to the insert mode
- O: open new line above the curser and go to the insert mode
- x: delete only current character
- X: delete only previous character.
- d: delete. mix this with other char such as w. dw delete a word.
- dd: delete the current line
- p: paste the last deleted text after the cursor
- P: paste the last deleted text before the cursor
- u: undo
- 
3. search
- /word: search for word
- n: next founded word
- N: previous founded word
- ?: search backward (n and N's function will be changed)
