### Editing files

We can create and modify files on the command line using text editors. These are like very stripped-back word-processors, with no formatting options, but with many powerful ways of editing that are not available in word-processors. There are lots of different command line editors, which range from user-friendly (but less powerful), to more difficult (but powerful, once the shortcuts and other tricks are learned). Some examples are `nano`, `micro`, `emacs`, and `vim`, with `vim` being the slowest to learn. `nano` is the easiest for beginners, and is available on most systems, so we will use that. Run this command:

```
nano animals.txt
"Use nano to edit a file called animals.txt"
```

The screen will look a little different: just like with `less`, *you are now not on the command line*, but running the program called `nano`. Try making some changes to the file. There are many shortcuts that `nano` can do, but for now I will just tell you that to save you press `ctrl-o` ("output a file"), `ctrl-w` is search ("where?"), and `ctrl-x` is used to leave `nano`. Note that there is a basic cheatsheet along the bottom of the screen for some common commands inside `nano`. Also, you can create a new file using the command

```
nano my_new_file
"Use nano to create a new file (unless it already exists, in which case open it)"
```

If you try to leave `nano` (`ctrl-x`) when there are unsaved changes, it will ask to `save modified buffer?`. "Buffer", in CLI speak, is information that exists in a file, or your RAM, but does not exist in memory storage. So, save or not with `y` or `n`, and let's look at examining files back on the command line.

Next page: [Searching]({{ site.baseurl }}{% link 05_searching.md %})

All pages: [Introduction](https://altanner.github.io/intro_to_CLI) • [Navigation]({{ site.baseurl }}{% link 01_navigation.md %}) • [Copying, moving and deleting]({{ site.baseurl }}{% link 02_manipulation.md %}) • [Viewing file contents]({{ site.baseurl }}{% link 03_viewing_files.md %}) • [Editing files]({{ site.baseurl }}{% link 04_editing_files.md %}) • [Searching]({{ site.baseurl }}{% link 05_searching.md %}) • [Further skills]({{ site.baseurl }}{% link 06_further.md %})
