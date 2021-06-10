### Copying, moving and deleting

Now we are going to bring some files into our folder `intro_to_cli` to play around with. Let's download the course files, using the CLI. Firstly, make sure you are in the the folder you made, `intro_to_cli`, and enter (copy and paste) this command

```
curl -O https://github.com/altanner/intro_to_CLI/raw/main/command_line_files.zip
```

This means "go to this internet address and download the file there into a file here. Don't worry about `curl` right now - it is a more advanced command and isn't used again in the course. But it is a command for getting information from the internet, just like in your browser. Now let's unzip the file do we can look at the folder and files inside:

```
unzip command_line_files.zip
```

Here we are expanding the zip file, like double-clicking an archive or compressed item in your GUI. The terminal will tell you what it has just done, and if you `ls` you will be able to see the new files. Move into the new folder with `cd`. Notice how these commands relate to your GUI - we can do all the same things (and more!) as you are used to in your graphical interface. 

Let's move into the folder called `sandbox` and play with some files. Firstly, let's copy a file: 

```
cp data1 data3
```

Here we are saying "copy the file called data1 to a new file called data3". We now have two identical copies of the same file, only different by name. ❗ **The command line will overwrite files with no warning! If, for example, `data3` already existed, the above command would overwrite it with `data1`!!!** Now let's try to delete, or remove, the file we just made by copying.

```
rm data3
```

Here we said "remove the file called data3". 💙 Remember, "remove" is the same as delete. ❗ **The command line has no recyle bin, undo, or back button! Be very careful when you are doing `rm`, `cp` and `mv` commands: all of them have the potential to cause permanent data loss!**

Now let's try copying, moving and removing folders. There are some folders in the sandbox to play with. Have a go at using `cp` and `rm` on there, and notice what it will and will not let you do. For folders that are not empty, we will need to use our first **flag**:

```
cp -r folder_with_files_inside folder_copy
```

"Copy, recursively, this folder to that folder". Empty folders can be copied, moved and removed, but you will need to use `-r` if there are items insides. `-r` is a common flag which we will use again later however 💙 not all flags mean the same, when applied to other commands! `-r` does the same thing for `cp` and `mv` and `rm`, but don't assume it does the same thing for all commands!

Try moving into the folder with files inside. Can you `cp` a file to the folder *above* the one you are in? Finally, let's look at moving files. 

```
mv data1 data4
```

Which means, "Move the file called to data1 to a file called data4". Move is essentially "rename" (although it is doing exactly the same as moving items in your graphical interface). As such: ❗ **I've said it before and will say it again: The command line will overwrite files with no warning! If `data4` already existed, it would be DELETED by moving `data1` onto it! Be very careful with `mv`!**

## Next page: [Viewing file contents]({{ site.baseurl }}{% link 03_viewing_files.md %})

All pages: [Introduction](https://altanner.github.io/intro_to_CLI) • [Navigation]({{ site.baseurl }}{% link 01_navigation.md %}) • [Copying, moving and deleting]({{ site.baseurl }}{% link 02_manipulation.md %}) • [Viewing file contents]({{ site.baseurl }}{% link 03_viewing_files.md %}) • [Editing files]({{ site.baseurl }}{% link 04_editing_files.md %}) • [Searching]({{ site.baseurl }}{% link 05_searching.md %}) • [Further skills]({{ site.baseurl }}{% link 06_further.md %})
