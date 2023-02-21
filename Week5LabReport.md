# Week 5 Lab Report
Welcome to the week 5 lab report. Today we will be talking about grep and alternate uses with examples.

## Grep with exact wording.

`grep -w "word" filename.txt` 

This is `grep` but what's different about it is that it looks for the specific whole word in the line, then prints the whole line.
Below are two examples from the same text file.


`grep -w  "store" ch1.txt`


![image](https://i.imgur.com/HUzQlHF.png)


`grep -w "cut" ch1.txt`


![image](https://i.imgur.com/R49CGX6.png)

As seen in the examples below, the keywords that we used were `store` and `cut` and the grep function found the lines/pargraphs that contained those words.

## Grep finding through multiple files

Lets say that, we really don't want to search things one file at a time. Then we can use the following command. 

`grep "txt" *.txt`

This command searching through all the text files in the current directory and pastes what it finds of the text. 


`grep -w "places"  *.txt`


![image](https://i.imgur.com/F4CSoU3.png)


`grep -w "location" *.txt`


![image](https://i.imgur.com/hUgRJgP.png)

In the two examples shown above, we can see the lines where the grep texts are and which files it's in based on the output, such as whether it's in ch1-ch15, it would state it first then continue on.

## Grep with the line number

Lets say, you're still trying to find that magical place where you have your text specifically but want to save some time on finding out what line it's on. Well, have no fear for the `-n` prompt is here. This additional command prints out the line that the text is in and the text itself.


`grep -n -w "power" ch1.txt`


![image](https://i.imgur.com/6Uxfloy.png)


`grep -n -w "store" ch1.txt`


![image](https://i.imgur.com/8PiljpQ.png)

Above are the examples where you can see that they have the the line number displayed before the text.

## Grep but reversed kind of?

What if you have too much of one word that appears in your text, and you start wondering what lines don't have that word? Well there's also a solution for that with the `-v` extension.


`grep -v "a" *.txt`


![image](https://i.imgur.com/u6IByD3.png)


`grep -v "the" ch1.txt`


![image](https://i.imgur.com/ag4pKRq.png)

This searches for any lines that doees NOT have the word that the grep is "looking" for, and can be useful when trying to ignore a certain word.

## Conclude
This wraps it all up today you have learned how to search for whole words, search multiple files, have the line number be displayed and ignoring certain words while using the command grep. Come back next time and learn something new I guess.
