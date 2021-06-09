### Copying, moving and deleting

Now we are going to bring some files into our folder `intro_to_cli` to play around with. Let's download the files, firstly with your GUI, then with the CLI. Download the course file by [clicking this link](https://github.com/altanner/intro_to_CLI/raw/main/text_files.zip). That file will then be in your default downloads folder. Open up a file explorer (Finder on Mac, Explorer on Windows. Click and drag, or copy and paste, the download `text_files.zip` to your folder `intro_to_CLI`. Then double click it to unzip it. Go to your terminal to see what has changed, with `ls` (make sure you are in the right folder). You should see the new file and a new folder. But, we want to do the same with the command line, so let's delete those with the command `rm`:

```
rm text_files.zip
"Remove (delete) the file called text_files.zip"
rm -r text_files
"Remove the folder called text_files, and everything inside it, recursively (-r)"
```

Here we have used our first **flag**, `-r`. This modifies the command `rm`; if you asked `rm` to delete a folder which has files in, it will let you know it cannot do that.

**The command line does not have an undo button or a recycle bin. Deleted files are gone forever!**

Your folder `intro_to_cli` should be empty again, so let's get that download using the command line. Here we are using `wget` to do the download:

```
wget https://github.com/altanner/intro_to_CLI/raw/main/text_files.zip
"Download from the internet the file at this URL location"
```

Now let's unzip the file do we can look at the folder and files inside:

```
unzip command_line_files.zip
"Unzip and decompress the zip file called command_line_files.zip
```

The terminal will tell you what it has just done, and if you `ls` you will be able to see the new files. Have a look around the new files with `cd`. Notice how these commands relate to your GUI - we can do all the same things (and more!) as you are used to in your graphical interface. Let's copy a file. In the folder called `example_files`, copy the file called `cat.txt`:

```
cp cat.txt dog.txt
"Copy the file called cat.txt to a new file called dog.txt"
```

**The command line will overwrite files with no warning! If, for example, dog.txt already existed, the above command would overwrite it with cat.txt**

We have already used `rm` above, so try to remove your new file called `dog.txt`. Copying a folder is very similar - copy the folder called `folder_of_files`:

```
cp -r folder_of_files a_copied_folder
"Copy, recursively, this folder to that folder"
```

Can you `cp` a file to the folder above the one you are in? Finally, let's look at moving files. 

```
mv data1 data2
"Move the file called to data1 to a file called data2"
```

**I've said it before and will say it again: The command line will overwrite files with no warning! If `data2` already existed, it would be DELETED by moving `data1` onto it!**

Next page: [Navigation]({{ site.baseurl }}{% link 01_navigation.md %}) • [Copying, moving and deleting]({{ site.baseurl }}{% link 02_manipulation.md %}) • [Viewing file contents]({{ site.baseurl }}{% link 03_viewing_files.md %}) • [Editing files]({{ site.baseurl }}{% link 04_editing_files.md %}) • [Searching]({{ site.baseurl }}{% link 05_searching.md %}) • [Further skills]({{ site.baseurl }}{% link 06_further.md %})
