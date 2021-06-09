### Viewing files

There are two main ways of viewing the contents of files on the command line: printing the output to the terminal window, and viewing with a pager. Let's look at outputting first. Move into the folder called `example_files`, and run this command

```
cat meaning_of_life.txt
"Display the contents of of the file "meaning_of_life.txt"
```

`cat` is short for "conCATenate", which means "join files end to end", but it can also output a single file too, so is useful for seeing what is in short files. Long files, it is less useful. Try this and see for yourself:

```
cat the-tempest.txt
```

The entire contents of the file have filled the terminal, which might be what you want, but it isn't. Instead, we can just see a part of a file, so experiment with these commands:

```
head -35 the-tempest.txt
tail -5 the-tempest.txt
```

We have another flag here, the number. I am sure you can work out what it does! Here are some more commands for outputting file contents in a variety of ways. Try them on the example files and work out what they do. You might wand to run these commands on shorter files to make it easier to understand the output, `animals.txt` might be useful here.

```
tac
rev
uniq
sort
shuf
```

These might seem trivial (maybe even useless!) but these are powerful building blocks for arranging data. You will also see these terms using in programming languages, in particular `head` and `tail` are common especially in Python.

Finally let's look at using a pager. A pager does not put the file contents to the terminal output, but instead shows it to you in a piece of dedicated software. It might not look like it, since it is still just plain text in your terminal window! But when using a pager, you are no longer on the command line. We will use the command `less`, which will open a pager to view a file.

```
less the-temptest.txt
```

The file will be shown, and you can scroll down and up with `space` and `b`. `Page up` and `page down` keys will also work. This is useful for large files, since it does not need to load the whole file into memory to show it to you. To leave the pager, press `q`. There are many things that `less` can do, but for now I will mention that you can search by pressing `/` and typing what you are looking for, and you can start `less` at the bottom of the file with `less +G filename`.

## Next page: [Editing files]({{ site.baseurl }}{% link 04_editing_files.md %})

All pages: [Introduction](https://altanner.github.io/intro_to_CLI) • [Navigation]({{ site.baseurl }}{% link 01_navigation.md %}) • [Copying, moving and deleting]({{ site.baseurl }}{% link 02_manipulation.md %}) • [Viewing file contents]({{ site.baseurl }}{% link 03_viewing_files.md %}) • [Editing files]({{ site.baseurl }}{% link 04_editing_files.md %}) • [Searching]({{ site.baseurl }}{% link 05_searching.md %}) • [Further skills]({{ site.baseurl }}{% link 06_further.md %})
