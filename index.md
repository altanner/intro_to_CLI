## Introduction to the Command Line Interface

Welcome!

Here you will find materials to accompany our course **Introduction to the Command Line Interface**, delivered by the University of Bristol Research Software Engineering team. This document provides a reference for commands used in the session, as well as some materials beyond the scope of the course for those wishing to go further. We also provide some text files for learning to view, search and edit on the command line. 

There are six main sections here

##### 1 [Navigation]({{ site.baseurl }}{% link 01_navigation.md %}) 
##### 2 [Copying, moving and deleting]({{ site.baseurl }}{% link 02_manipulation.md %})
##### 3 [Viewing file contents]({{ site.baseurl }}{% link 03_viewing_files.md %})
##### 4 [Editing files]({{ site.baseurl }}{% link 04_editing_files.md %})
##### 5 [Searching]({{ site.baseurl }}{% link 05_searching.md %})
##### 6 [Further skills]({{ site.baseurl }}{% link 06_further.md %})

### Important things to remember, plus some tips

⚠️ The command line is case-sensitive. The letter `H` is entirely different from `h`, for example! So if you are having issues, always check your capitalisation is correct.
⚠️ You *can* select, cut etc with the mouse cursor, **but you cannot move the position of your typing cursor with the mouse**! You can only do that with the arrow keys. A couple of useful shortcuts are `ctrl-a` is "move my cursor to the start of the line", `ctrl-e` is "move cursor to end of line", and `option-arrowkey` will move your typing cursor word by word, rather than character by character.
✨ If it looks like the terminal is stuck, or you want to cancel a command, it is `ctrl-c`.
✨ To exit a terminal session, type `exit`.

### Opening a command line session

All operating systems offer a terminal: 
- on MacOS you can use *Terminal* or *iTerm* (find them in Launchpad or Spotlight)
- on Windows *PowerShell*, *GitBash*, or a terminal under *Windows Subsystems for Linux* 
- Linux provides *Konsole*, *Terminal* or *xterm* as default.

Terminal windows are often white or black by default, but don't worry if yours is a different colour. When you open a terminal, you will be provided with a **prompt**. This tells you where you are, and provides a line where you will type your commands. Here is what a typical prompt looks like:

```
[at9362@dc2-d0:~] $
```

Your prompt will look different, but here is what it means

```
[ your_name @ computer_name : the_current_folder ] $
```

Here, the computer name (also known as the "hostname") is `dc2-d0`, but yours might be more friendly, like `Megans_iMac` or `ubuntu`, for example. 
The `$` sign means the terminal is waiting for a command. **Sometimes you will see commands on the internet which include the `$` symbol at the start of the command! You don't need to include this as part of the command, say if you cut and paste!** The name of the folder you are working in is after the `:` symbol. Here it says `~` - find out what that means in the next section. 

## Next page: [Navigation]({{ site.baseurl }}{% link 01_navigation.md %})

All pages: [Introduction](https://altanner.github.io/intro_to_CLI) • [Navigation]({{ site.baseurl }}{% link 01_navigation.md %}) • [Copying, moving and deleting]({{ site.baseurl }}{% link 02_manipulation.md %}) • [Viewing file contents]({{ site.baseurl }}{% link 03_viewing_files.md %}) • [Editing files]({{ site.baseurl }}{% link 04_editing_files.md %}) • [Searching]({{ site.baseurl }}{% link 05_searching.md %}) • [Further skills]({{ site.baseurl }}{% link 06_further.md %})
