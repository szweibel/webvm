If you have finished both tasks in the bedroom, you are ready to keep going.
This part gets harder a bit fast, so make sure to read and do things calmly, only moving on when you feel comfortable.

First, make sure you are in the right place. Use `pwd` to check if you are in the bed.

Our goal is to find out the number of characters of all the markdown files in the bed directory combined. Even though the way to do it is only a one-line command, it takes a few more steps to understand what we are doing.

Markdown files have ".md" extensions in the end of the file name.

In Bash, you can use wild cards to find all files with names in a specific pattern. A very powerful wildcard is "*", which can be understood as "anything".
For instance, if you run `ls d*`, it will list all the files that start with "d". For bash, what you meant by `d*` was "All files that start with d and are followed by anything".

In the same way, `*.txt` will mean "All files whose names start with anything and end with '.txt' "

	Try running these just to see it at work (notice that these are case-sensitive):
		`ls d*`
		`ls *.txt`

Wild cards can be used with any command. We will use them with cat, so we can see how many characters the markdown files have COMBINED.

You could try `cat *.md` and manually count the characters. But that doesn't seem like a fun task.

	Run `cat *.md` just to see it at work, but don't waste your time counting characters.

Instead, let's use another command, wc (word count). Despite the name, it can be used to count words, lines, or characters.
Let's see how it works:

	Run `wc --help` and read the first few lines.

You will see something like this: "Print newline, word, and byte counts for each FILE, and a total line if                                                                                      more than one FILE is specified."

Let's try it with a file:

	run `wc PILLOW.txt`

You should see three numbers: the first one is the number of lines, the second is the number of words and the third is the number of bytes.
But we don't want any of those, we want the number of characters. (Sometimes the number of bytes is the same as the number of characters, but not always)

The help message above also said that "-m, --chars print the character counts"

	Try either `wc -m PILLOW.txt` or `wc --chars PILLOW.txt`
	(Both options should work the same)

See if you're getting the number 39 in the output.

If so, now it's time to add it all together:

	CHALLENGE: Run a command that will count the number of characters of all files that have the markdown extension.
	Write the total down and go read the next instructions in done2.md

