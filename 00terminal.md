# Basic Terminal Commands

## Navigating

To change directories use the `cd` command. Each sub-directory is seperated by a forward slash so for example we could have a file structure like so:

```
 cd Pictures/holidays/2014
```
Continuing with the example above, if we are in the *holidays* directory and want to move up a level simply type: 

```
 cd ..
```

This can also be used with `/` to create a path to a specific directory. Let's assume we're viewing the 2014 holiday photos and want to navigate to 2013 instead. We have to move up a directory to *holidays* and then into the *2013* directory. This can be achieved with the following:

```
 cd ../2013
```

To view the contents of the directory you are in simply type `ls` to list all the files and directories.  

## Working with files and folders

### Create a New File:
An easy way to create a new file is with the `touch` command. Lets create a new text file called _myFile_ :

```
 touch myFile.txt
```

You can also create new files using the `cat` command. See <a href="#Outputting_information_to_the_terminal">the section below </a>for more.

If you now run `ls` you should see that *myFile.txt* is now in your current directory.

Raspbian contains a few good text editors straight out of the box. Although Vim is probably more powerful, nano is a bit more user friendly. 

### Editing Text Files:
Let's edit *myFile.txt* using nano:

```
 nano myFile.txt
```

If you're not the super user on your machine you'll have to preface most command with `sudo` or "super user do" like so:

```
sudo nano myFile.txt
```

Once you're happy with your changes, save and exit nano. The keyboard shortcuts are displayed along the bottom of the screen so just hit __CTRL__ + __O__ to write out (i.e. save) the contents of your file to disk and then __CRTL__ + __X__ to exit nano. 

### Creating New Directories

To create a new directory use the make directory, `mkdir` command, followed by the name you want to give your directory.

```
 mkdir newFolder
```

### Moving Files 
Moving files is accomplished with the move command, `mv`. The move command needs two pieces of information. First you have to specify which file you wish to move, and secondly you need to tell it where you want to move the file to. Lets move *myFile.txt* into *newFolder*. 

```
 mv myFile.txt newFolder

```

If you now `cd` into *newFolder* and `ls` the contents you will see that your text file has been moved.

### Copying Files
The copying command, `cp`, is used in much the same way as the `mv` command in that you have to specify first the file you want to copy and then tell it the file you want to copy it to. Lets create a copy of *myFile.txt* and call it *myFile2.txt* instead.

```
 cp myFile.txt myFile2.txt
```

Again, you can specify full paths, so the files don't have to be in the same directory and your new file can have what ever name you want it to have. 

### Deleting Files
You can delete a file by using the remove command `rm`. If we want to remove our new *myFile2.txt* file we simple type: 

```
 rm myFile2.txt
```

A quick `ls` will reveal that the file is now gone!

### Deleting Folders

To delete a folder, the computer essentailly has to go into the folder, delete it's entire contents and then delete the folder itself. This is acheived by passing the following arguments (or flags) to the remove command:

```
rm -r -f myFolder
```

the `-r` flag means that the command should be called recursively (similar to repeatedly) and the `-f` flag means force, in other words, you're telling the computer "I know what I want to do here, go ahead and do what I've told you to do."

### Outputting information to the terminal  

This can be done using the `cat` command which is short for concatenate. For example, the code:

```
cat myFile.txt
```

will print the contents of `myFile.txt` to the terminal.

### Sorting the Contents of a File
Let's create a text file, called _computers.txt_ that contains some computer manufacturers. 

```
touch computers.txt
```

We'll then edit it to add some data:

```
sudo nano computers.txt
```


Add in some different manufacturers, for example: HP, Lenovo, Raspberry Pi, Asus, Acer, Apple, Dell, Compaq etc.

To sort the contents of this file alphabetically simply type:

```
sort computers.txt
```

and the entries will be listed from A to Z.

To sort in reverse alphabetical order:

```
sort -r computers.txt
```

To sort numerical data:

```
sort -n myNumbers.txt
```

It is also possible to sort months in their correct chronological order:

```
sort -M someMonths.txt
```
## Summary

To go back to the chapter overview click [here](mdwiki.html#!00overview.md)

To return to the Raspberry Pi Recipes page click [here](http://domhnallohanlon.github.io/rpi)

Note: You can find more termial commands (and plenty more besides) over on <a href="http://ss64.com" target="_blank">SS64.com</a>. There are lots of references to get help you find your way around the command line.

## What's Next?

Great stuff - why not try set up your own [web server?](mdwiki.html#!01overview.md)