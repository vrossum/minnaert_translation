This is an unauthorized English translation of the book 
'Marcel Minnaert, astrofysicus 1893-1970. De rok van het universum' written by 
Leo Molenaar. The original book can be found here: 
https://www.dbnl.org/tekst/mole016marc01_01/
For figures and full bibliography, see there.

The translation was main done via the Ollama version of Deepseek,  deepseek-r1:70b.

## A note on the translation script

In order to translate a large text, I used the following steps
1. Extract txt from pdf with pdf2text
2. Split with into 100 line blocks 
> cat file.txt | sed 's/[.!?]  */&\n/g'  |split --lines=100
3. translate each block
4. put concat translation
