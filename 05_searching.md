### Searching

#### Searching _for_ files

We usually use `find` as our search command, but it has some strange syntax, so if you are a little confused, you are not alone! The syntax is `find [where to start looking] [a flag for the type or naming of the file] ["the match you are looking for, in quotes"]`. Let's go back to your folder `command_line_files`, and run each of these commands.

```
find . -iname "data1"
find . -iname "data*"
find . -iname "*txt"
find . -iname "*a*"
find . -iname "dugong"
```

Here we are using `.` (the current location) as the starting point, and `find` will look in all the containing folders below that location. To search a whole file system, we could go `find / -iname "my_file"`, but just like doing this in a GUI, it is very slow. `find` will also, unhelpfully, tell you all the folders you do not have access to.

The flag `-iname` is saying "the file or folder is has this name, case insensitive" (you can do `-name` too, if you are sure of the case). In the name, we can have wildcards to say "anything", and 💙 it is common to put `*` at both ends of your query, just in case you are forgetting part of the name. (More on wildcards later.) Notice the last query, for `"dugong"`, does not find anything, but the command line doesn't tell you that. It just finishes and gives you your prompt back. ❗ This is standard for the command line - unless you get an error, your command did run correctly - sometime with no output at all!

💙 If you are on MacOS or Linux, you may have a command installed called `fzf` - "fuzzy find". This is a much more modern search command than `find`, which will find matches and similiar matches (without having to use wildcards), and give you a list of the closest matches. Give it a try with just `fzf` (and `enter` without a search query), then start typing your query and it will search as you type, a little like a browser can. You can scroll the results with your arrow keys, and press `enter` to print results to the terminal.

#### Searching _in_ files

A strength of the command line is being able to search through files. Here we will use a command called `grep`. Strange name I agree, but apparenly back in the depths of time it stood for "global search using regular expressions and print". Don't worry about what that means! Although, in programming "global" means "everywhere" - nothing to do with the world!

💙 Think of `grep` as `ctrl-f` ("find"), that you might use in a document or a browser, to find particular words. Change folder into `some_plays` and try this command: 

```
grep fish king-lear.txt
```

Here we are saying "Use grep to seach for the word fish in the file king-lear.txt". `grep` will show you the lines with exact matches. ❗ Be careful that grep is both case sensitive, and it will do exactly what you asked - fish will also be in parts of words other than "fish" itself. `grep` can take many useful flags. Try each of these commands, and work out what they do:

```
grep faith king-lear.txt
grep Faith king-lear.txt
grep -i faith king-lear.txt
grep -n faith king-lear.txt
grep -c faith king-lear.txt
grep -c Faith king-lear.txt
grep -ci faith king-lear.txt
grep faith king-lear.txt julius-caesar.txt
```

Note that we can 💙 combine multiple flags, as in that `-ci` command above. Also, that final command doesn't have flags, but is asking to search two files for the same match. Note that if you want to search for something with a space in it, you will need quotes around your query, for example

```
grep "this scattered kingdom" king-lear.txt
```

If the quotes were absent, `grep this scattered kingdom king-lear.txt`, the command line would think you want to find the word "this", in the files called "scattered", "kingdom", and "king-lear.txt".

Now let's search multiple files. We can do this in a couple of way. First, let's move out of the folder `some_plays`, back one level with `cd ..`. From here, let's recursively search for something inside `some_plays` with a couple of commands

```
grep -r sparrow some_plays
grep -rc sparrow some_plays
```

Often, when referring to the file we want to search (or apply any command to), we can use 💙 **wildcards** to specify files with similarities in name. Move back into the folder called `some_plays`, and use this command

```
grep sparrow *
```

Here, `*` means "every file and folder in this location". We could also specify just part of the filename - try these commands:

```
grep sparrow t*
grep sparrow the*
grep dog *night*
```

We won't go into it here, but `grep` can search in very sophisticated ways not possible with `ctrl-f`, for example finding ambiguous spellings, returning matches a certain distance from the actual match, or being able to look ahead or behind to conditionally match the true match. Don't worry if that doesn't make sense! 💙 If you are wondering what the command line version of "find and replace" is, look up a command called `sed` ("string editor") - this command is beyond the scope of this course, but is a commonly-used command for automating modification to files.

To use wildcards in the search query itself, we have to use regular expressions ("regex"). For example searching for variations of spelling, or when a word is near another match, or not showing the match but the word after the match, or the line after the match. ❗ **One more note on `grep`: when counting, it only counts the number of __lines__ that the match appears on. If the same match occurs twice on the same line, it will only count as 1 match. `grep` can count all matches, rather than lines, but you can look that up for yourself**

Have a more bit of practice with wildcards, by going back a folder (you should be in `command_line_files`) - what do you get if you run these commands?

```
ls *
tail -3 some_plays/*
head -10 some_plays/king*
```

With those `tail` and `head` examples, note that we are using the **relative path** to the folder `some_plays`. 💙 Remember that anything ending with a `/` character is a folder, not a file. We could also use the **absolute path**, ie the path that will work from any location in the filesystem. For me, that would be `/Users/at9362/Code/intro_to_CLI/command_line_files`, but for you it will be something different.

## Next page: [Further skills]({{ site.baseurl }}{% link 06_further.md %})

All pages: [Introduction](https://altanner.github.io/intro_to_CLI) • [Navigation]({{ site.baseurl }}{% link 01_navigation.md %}) • [Copying, moving and deleting]({{ site.baseurl }}{% link 02_manipulation.md %}) • [Viewing file contents]({{ site.baseurl }}{% link 03_viewing_files.md %}) • [Editing files]({{ site.baseurl }}{% link 04_editing_files.md %}) • [Searching]({{ site.baseurl }}{% link 05_searching.md %}) • [Further skills]({{ site.baseurl }}{% link 06_further.md %})
