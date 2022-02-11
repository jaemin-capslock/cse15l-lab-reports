# Week 6 Report

## Copying the entire folder

To do this, we will obviously use the `scp` command, but now with some modifiers. To copy the entire directory, we must add `-r` with the command to tell the terminal that this is a recursive operation; i.e., all the files inside the folder will also be copied.

![Image][1]

[1]:recursivescp.png

As you can see, the entire folder (which is `cse15-week5-test`) and its files are copied to our ieng6 server. Great!

## Running the test

Let's `ssh` inside, compile the test and run:

![Image][2]

[2]:multitest.png

Test runs fine! Like before, I am using `javac` and `java` to run the test. 

## Running this all in one step.

Recall that by using semicolons and quotation marks, we can run multiple commands in sequence at once. To do this, we should combine the recursive `scp` command, `ssh` inside the server, and then use `javac`, `java` to run the tester file. Long line!

```
scp -r . cs15lwi22amd@ieng6.ucsd.edu:~/; ssh cs15lwi22amd@ieng6.ucsd.edu "javac -cp lib/junit-4.13.2.jar:lib/hamcrest-core-1.3.jar:. MultiTest.java; java -cp .:lib/junit-4.13.2.jar:lib/hamcrest-core-1.3.jar org.junit.runner.JUnitCore MultiTest"
```
Thick line, but it's really just copy-pasting what we've done so far. Let us see the result:

![Image][3]

[3]:chaintest.png

You can see that we have first copied the file, sshed inside, and then we can observe that the test files have run successfully - good!

