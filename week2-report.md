# Jaemin Ko

## Installing VSCode

To install VSCode, go to the official website in the link below:

[Link](https://code.visualstudio.com)

Click the Download button to get the version that fits your operating system. The website (in my Mac environment) looks like:

![Image][1]

[1]:VSCodescreen.png

After installing, now we can proceed on remotely connecting to the school server! Let's (finally) make our tuitions a bit more worth.

First, open the terminal attached to your VSCode. You should see it at the menu bar on the top of your screen, and it should look like this:

![Image][2]

[2]:terminalscreen.png

Now, you should have your `ieng6` id issued by UCSD. With that, type at terminal:

```
ssh cs15lwi22zz@ieng6.ucsd.edu
```
Replace the `zz` with your issued ID. Enter your UCSD password when it prompts to do so. You should see the result like:


![Image][3]

[3]:terminalscreen2.png

Alright, now let's try out some commands that we've covered in the class! Let's see what files are here in this server with `ls`.

![Image][4]

[4]:lsscreen.png
We see a java file, class file, and a file called perl5... Hmm. Not a lot going on. *That's it?*

Well, try out the command `ls -lat`:

![Image][5]

[5]:lslatscreen.png

Woah, now we are seeing a lot of files here! Impressive. Now, let's try making a directory inside of the server using `mkdir`:

![Image][6]

[6]:mkdirscreen.png

Now we can see a folder that we've created named `bobcat`. (It's still a cat!)

Awesome. Now let's try copying a file to our server. This can be done by the `scp` command. Create any file, and enter this command:

![Image][7]

[7]:scpscreen.png

The format is `scp filename cse15lwi22zz@ieng6.ucsd.edu:~/`. After copying the file, I ssh'ed to the server and used ls command. Notice that now the server has my `hi.txt`file. 
