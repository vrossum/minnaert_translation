This is an unauthorized English translation of the book 
'Marcel Minnaert, astrofysicus 1893-1970. De rok van het universum' written by 
Leo Molenaar. The original book can be found here: 
https://www.dbnl.org/tekst/mole016marc01_01/
For figures and full bibliography, see that original file.

The translation was main done via the Ollama version of Deepseek,  deepseek-r1:70b.

## A note on the translation script

In order to translate a large text, I used the following steps
1. Extract txt from pdf with pdftotext
2. Split with into 100 line blocks 
> cat file.txt | sed 's/[.!?]  */&\n/g'  |split --lines=100
3. translate each block
I used the prompt:
> pr="From now on, do a translation of the Dutch text in square brackets into English. Do not show your thinking, notes, or interpretation. Put the full translation in quotation marks. Don't summarize."
>  pr="${pr}  [$(cat $file)]"
> ollama run deepseek-r1:70b $pr > tr_$file
4. concat translation

Manual corrections were necessary. 
Sometimes Deepseek did summarize instead of translate; note numbers in the text could trigger halucination; it did not distinguish section headers from sentences.

A better pdftotext would solve some of these problems.
