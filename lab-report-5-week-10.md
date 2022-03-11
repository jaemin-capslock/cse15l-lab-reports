# Week 10 Lab report


## How did I found the bugs?

I generated ```results.txt``` using bash, and then used ```diff``` command to compare the results of the two implementation to find the difference.

## Bug 1

Regarding ```14.md```, there was a difference:

![Image][1]

[1]: bug1.png

I chose the first file (which is the given implementation, wheras the second is our own implementation to fix)

Copying the ```14.md``` to the CommonMark Demo show the expected result.

![Image][2]

[2]: week10expected1.png

We can observe that there is no actual Markdown link in this file. Thus, both are errors as both have added "\foo" once or twice in the code.

The reason why this is not a valid markdown link is because of the backslash ```\``` included at the beginning of the each line of the file. Removing this makes the link legal:

![Image][3]

[3]: week10iffixed1.png

Observing the code immediately gives why this error occurs.

![Image][4]

[4]: week10code1actual.png

The code does not have a logic to check if it has a backslash or not. The bug could have been fixed if we added the logic to check for backslash (and perhaps other illegal characters).
## Bug 2

The next difference occured at ```22.md```.

The difference:
![Image][5]

[5]: bug2.png

The expected output, produced using commonmark is 

![Image][6]

[6]: week10expected2.png

Thus we can see that our implementation works correctly while the given file doesn't.

This bug likely occured due to this logic:

![Image][7]

[7]:week10bugcode2.png

Where if there is a whitespace " " found in the link, then it disregards and does not add as a potentialLink.

While it does make sense that an actual link would not have whitespace (least in a normal sense), this error could be avoided if we deleted the if statement and not check for white space in the link. 