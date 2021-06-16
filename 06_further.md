### Further topics

If you have got this far, then you have covered the most useful commands for the command line interface! Although there are many commands, the ones mentioned in this workshop make up 90% of what most people need to do on the command line. Congratulations!

This page will cover some more advanced ways of using the command line, particular **1** how to link different commands together, and **2** how to interact with remote computers. 

Firstly we will cover a concept called "redirecting". Move into the folder `example_files`. We can see, for example, the first three lines of `plants.txt` with the command

```
head -3 plants.txt
```

But what if, instead of printing the output to the terminal, we wanted to put it into a file? This is called "redirecting", and is done with the symbol `>`

```
head -3 plants.txt > first_three_plants.txt
```

The terminal will not give you any output, but what is inside the file `first_three_plants.txt`? Let's expand on this by using wildcards. Try this command, and examine the contents of the output file:

```
head -3 * > my_new_file
```

**Be careful! Redirects will overwrite the target file!! If `my_new_file` already existed, it would be permanently overwritten by the above command!** If we want to **append** to a file, we use a double arrow, for example we can go:

```
tail -10 romeo-and-juliet.txt >> another_file
tail -10 king-lear.txt >> another_file
```

Finally, we will look at how to make one command take the output from another command. This is called a "pipe", `|`. That is the "bar symbol", on Mac keyboards it is next to `enter`, on Windows it is usually by the left shift key, and on Linux it is usually to the left of the 1 key. Move to the folder `some_plays`, and let's use a new command, `wc`

```
wc -l macbeth.txt
```

`wc` is "word count", but here we are asking for the number of lines with the flag `-l`. We can use a wildcard to see how many lines are in all of the plays, with

```
wc -l *
```

But what if we wanted these in order? We can use the output of `wc` as the input for `sort`. Try these commands

```
wc -l * | sort
wc -l * | sort -r
```

Combining redirects and pipes can make powerful scripts, here is a simple example where we pipe one command to another, then send the output of the next command into a file:

```
wc -l * | sort -r > ordered_by_line
```

Understanding this kind of flow is essentially the first step towards programming. While the command line is a whole scripting language in itself, as things get more sophisticated we start to use proper programming languages. This aids in compatibility, portability, allows you to use purpose-built tools. 

Further useful commands to explore for yourself (there are thousands, so here are just a handful!). Some of these will run by themselves, some of them will need files to work on. (Some of these might not be available on your particular system.)

```
history
man
file
cut
sed
tr
du
df
who
w
whoami
tree
exit
```

### Secure shell

If you are working with computing clusters (for example with the University of Bristol we have BlueCrystal, BluePebble, Catalyst, Isambard, and other high-performance computers), to run things you will need to log in remotely to those machines. This is done with a command called `ssh` or "secure shell". As the name suggests, this opens a secure communications channel with another computer. Here is a typical `ssh` command (these identity credentials are not valid!):

```
ssh altanner@isambard.bris.ac.uk
```

or

```
ssh -p 22 user36256@364.287.3.1
```

Notice that the login is essentially the same as your local address, that we see in the prompt when on your own machine. You provide your username, the name of the machine (or its IP address), and in some cases you might tell the remote machine which port you want to connect to (as in the lower example above). Typically, you will then be asked for a password. For many machines, you will need to be on an authorised VPN before trying to connect - otherwise the remote machine will ignore your attempts to access it.

### Secure copy

To move information between different machines, we use a program called `scp` - "secure copy". This is the same as `cp`, except that the contents of your files are encrypted (you can `scp` locally, although there isn't a gerat deal of point - however, if you see a *local file* unexpectedly named a *remote machine*, and you are wondering why your `scp` didn't work, it may be because your syntax was not right, and the command line thought you wanted to copy a file locally - a common mistake!). Here is the syntax for copying locally to remotely:

```
scp my_file user003@isambard.bris.ac.uk:~/my_folder
```

which, while it looks more complex, is the same syntax as with `cp`. You specify what to copy, then where to copy it, using the address of the remote machine **then a colon** `:` then the folder of where it is to go. To send something to your home folder, you can just leave it blank (but include the colon):

```
scp file_i_am_sending user003@isambard.bris.ac.uk:
```

❗ **I've said it before but I will say it again!! if `file_i_am_sending` already exists in your home folder in the destination machine, it will be overwritten by this `scp` command!!!

To copy something remotely, back to your own computer, we just reverse the syntax, just like with `cp`:

```
scp user003@isambard.bris.ac.uk:~/my_folder/another_folder/the_file_i_want .
```

💙 Note the `.` at the end there, which is saying "the destination for the remote file is here". You could have a path instead, if you didn't want to bring the file to your current working directory. Also, if you need to bring a whole folder, you can use the flag `-r` , just like with `cp`, to copy recursively.

All pages: [Introduction](https://altanner.github.io/intro_to_CLI) • [Navigation]({{ site.baseurl }}{% link 01_navigation.md %}) • [Copying, moving and deleting]({{ site.baseurl }}{% link 02_manipulation.md %}) • [Viewing file contents]({{ site.baseurl }}{% link 03_viewing_files.md %}) • [Editing files]({{ site.baseurl }}{% link 04_editing_files.md %}) • [Searching]({{ site.baseurl }}{% link 05_searching.md %}) • [Further skills]({{ site.baseurl }}{% link 06_further.md %})
