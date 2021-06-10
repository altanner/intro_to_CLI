### Looking around and moving around

Let's run our first command:

```
pwd
```

With `pwd` we are asking "print my current working directory / where am I?" You will then get some **output** to the terminal window, something like

```
/home/at9362
```

This is your current location, here shown as an **absolute path** - the full description for what folder you are in. 💙 The sign `~` is an abbreviation for "your home folder". There are five abbreviations for locations that you might come across

```markdown
~    "Tilde"    Your home folder
.    "Dot"      Your current working folder.
..   "Dot dot"  One folder "up" or "back" from here.
-    "Dash"     The folder you were *most* *recently* in.
/    "Root"     The root folder, containing the whole folder system.    
```

`.`, `..`, and `-` are **relative paths** - they only relate to where your working folder is. Now let's see what is here

```
ls
```

Now that we know where we are, let's see what is here. This is much like looking at the file manager window in a GUI, Finder in MacOS or Explorer on Windows: run a command called `ls`

```
ls
```

For me, I get this output, a list of what is here.

```
1jun_logfile  6jan  credentials.txt  creds  data_depot  git
```

Yours will be different. Each of these things are the items (files and folders, usually) in your current working directory. For most terminals, items in white are files, and items in blue are folders. The first thing we are going to do is make a new folder, where we will be doing our work. We will use the command `mkdir`:

```
mkdir intro_to_cli
```

This command is asking "make a new folder (directory) here, called intro_to_cli". You'll be getting used to the names of commands being abbreviations! Run `ls` again, and see what has changed. Hopefully you will see a new folder, appropriately named. We can then move into the folder we have made with

```
cd intro_to_cli
```

Here we are asking to "change my working folder (directory) to intro_to_cli". This is the same as double-clicking a folder in your GUI, to move into that folder. Try doing `ls` and `pwd` here, to see how the output changes. We can go back to your home folder by going

```
cd ..
```

This means "change folder to the one above this one". Going `cd ..` will always move you "backwards" in your folders, unless you are in the root folder `/`

**There are actually three ways we could move back to our home folder from here. `cd ..` as above, `cd -`, and just `cd`. `cd` alone will always take you back to your home folder.** Try repeating `cd ..`, and do `ls` each time. Where do you end up if you do this several times? What is here? Can you return to the folder you named `intro_to_cli`, in your home folder *using its absolute path*?

## Next page: [Copying, moving and deleting]({{ site.baseurl }}{% link 02_manipulation.md %})

All pages: [Introduction](https://altanner.github.io/intro_to_CLI) • [Navigation]({{ site.baseurl }}{% link 01_navigation.md %}) • [Copying, moving and deleting]({{ site.baseurl }}{% link 02_manipulation.md %}) • [Viewing file contents]({{ site.baseurl }}{% link 03_viewing_files.md %}) • [Editing files]({{ site.baseurl }}{% link 04_editing_files.md %}) • [Searching]({{ site.baseurl }}{% link 05_searching.md %}) • [Further skills]({{ site.baseurl }}{% link 06_further.md %})
