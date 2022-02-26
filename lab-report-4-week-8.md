# Lab report

## File 1

![Image][1]

[1]:file1expected.png

This is the expected output of this markdown file, and thus we have four links

Running on my testfile,

![Image][2]

[2]:mytestfile1.png

![Image][3]

[3]:myresult1.png

The test fails.

Running on the other's implementation,

![Image][4]

[4]:theirtestfile1.png

![Image][5]

[5]:theirresult1.png

The test also fails. But notice that the produced output is different.

## Fixable?

Both my implementation and their implementaion currently lacks the ability to check for backticks (`). Frankly speaking, I am not sure how I can handle this issue; our code checks for brackets, whitespaces and exclamation marks, but backticks were not in the consideration. We would probably have to edit quite a few if statements (and add more logic), create new variables, and so on. It will be more than 10 lines.

On their file, on the other hand, the acutal output only varies by one backtick. I tried to create a new variable and added a logic, and it didn't work, but I do believe that it can be fixed if I examine the if statements more carefully.

## File 2

![Image][6]

[6]:file2expected.png

Running on my test file,

![Image][7]

[7]:mytestfile2.png

![Image][8]

[8]:myresult2.png


Running on their test file,

![Image][9]

[9]:theirtestfile2.png

![Image][10]

[10]:theirresult2.png


## Fixable?

Both tests failed, but we can also observed that they produced different output. We can thus infer that we have different logic on handling nested parentheses.

The main issue that it does not work in our group's file, as well as theirs, is because we currently have only one variable that looks for an open parenthese character, which then looks for a closing parenthese character. Fixing this would mean that we would have to either create a list/hashmap/stack that tracks the amount of open parentheses, or to create more variables. This fix would require more logic and more variables, which would be fairly complex.

## File 3

![Image][11]

[11]:file3expected.png

Running on my test file,

![Image][12]

[12]:mytestfile3.png

![Image][13]

[13]:myresult3.png

Running on their test file,

![Image][14]

[14]:theirtestfile3.png

![Image][15]

[15]:theirresult3.png


## Fixable?

Again, both tests fail, but our group's file and their file produces different results. It can be observed that our group's file fail to detect any links inside of the provided file, whereas their groups file get (some of) links as well as non-link tests.

To fix this, we would have to handle files that contain "\n" symbols and such. This would add more variables and logic, which I doubt to be fixed in few lines.
