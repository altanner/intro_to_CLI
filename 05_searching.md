### Searching through files

A strength of the command line is being able to search through files. Here we will use a command called `grep`. Strange name I agree, but apparenly back in the depths of time it stood for "global search using regular expressions and print". Don't worry about what that means! Although, in programming "global" means "everywhere" - nothing to do with the world!

Think of `grep` as `ctrl-f` ("find"), that you might use in a document or a browser, to find particular words. Change folder into `some_plays` and try this command: 

```
grep fish king-lear.txt
"Use grep to seach for the word fish in the file king-lear.txt"
```

`grep` will show you the lines with exact matches. Be careful that it will do exactly what you asked - fish will also be in parts of words other than "fish" itself. `grep` can take many useful flags. Try each of these commands, and work out what they do:

```
grep "faith" king-lear.txt
grep "Faith" king-lear.txt
grep -i "faith" king-lear.txt
grep -n "faith" king-lear.txt
grep -c "faith" king-lear.txt
grep -c "Faith" king-lear.txt
grep -ci "faith" king-lear.txt
```

Note that we can combine flags, as in that `-ci` command above. Now let's search multiple files. We can do this in a couple of way. First, let's move out of the folder `some_plays`, back one level with `cd ..`. From here, let's recursively search for something inside `some_plays` with a couple of commands

```
grep -r sparrow some_plays
grep -rc sparrow some_plays
```

Often, we will search with **wildcards**. Move back into the folder called `some_plays`, and use this command

```
grep sparrow *
```

Here, `*` means "every file and folder in this location". We could also specify just part of the filename - try these commands:

```
grep sparrow t*
grep sparrow the*
grep dog *night*
```

We won't go into it here, but `grep` can search in very sophisticated ways. To use wildcards in the search query itself, we have to use regular expressions ("regex"). For example searching for variations of spelling, or when a word is near another match, or not showing the match but the word after the match, or the line after the match. 

Have one more bit of practice with wildcards, by going back a folder (you should be in `command_line_files`), and try

```
ls *
```


Next page: [Further skills]({{ site.baseurl }}{% link 06_further.md %})

All pages: [Navigation]({{ site.baseurl }}{% link 01_navigation.md %}) • [Copying, moving and deleting]({{ site.baseurl }}{% link 02_manipulation.md %}) • [Viewing file contents]({{ site.baseurl }}{% link 03_viewing_files.md %}) • [Editing files]({{ site.baseurl }}{% link 04_editing_files.md %}) • [Searching]({{ site.baseurl }}{% link 05_searching.md %}) • [Further skills]({{ site.baseurl }}{% link 06_further.md %})
