### Editing files

We can create and modify files on the command line using text editors. These are like very stripped-back word-processors, with no formatting options, but with many powerful ways of editing that are not available in word-processors. There are lots of different command line editors, which range from user-friendly (but less powerful), to more difficult (but powerful, once the shortcuts and other tricks are learned). Some examples are `nano`, `micro`, `emacs`, and `vim`, with `vim` being the slowest to learn. So, we will start with `nano`. Run this command:

```
nano animals.txt
"Use nano to edit a file called animals.txt"
```

The screen will look a little different: just like with `less`, *you are now not on the command line*, but running the program called `nano`. Try making some changes to the file. There are many shortcuts that `nano` can do, but for now I will just tell you that to save you press `ctrl-o` ("output a file"), and `ctrl-x` is used to leave `nano`. Also, you can create a new file using the command

```
nano my_new_file
"Use nano to create a new file (unless it already exists, in which case open it)"
```



Next page: [Navigation]({{ site.baseurl }}{% link 01_navigation.md %}) • [Copying, moving and deleting]({{ site.baseurl }}{% link 02_manipulation.md %}) • [Viewing file contents]({{ site.baseurl }}{% link 03_viewing_files.md %}) • [Editing files]({{ site.baseurl }}{% link 04_editing_files.md %}) • [Searching]({{ site.baseurl }}{% link 05_searching.md %}) • [Further skills]({{ site.baseurl }}{% link 06_further.md %})
