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
An easy way to create a new file is with the `touch` command. Lets create a new text file:

```
 touch myFile.txt
```
 If you now run `ls` you should see that *myFile.txt* is now in your current directory.

Raspbian contains a few good text editors straight out of the box. Although Vim is probably more powerful, nano is a bit more user friendly. 

### Editing Text Files:
Let's edit *myFile.txt* using nano:

```
 nano myFile.txt
```

Once you're happy with your changes, save and exit nano.

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

## Summary

To go back to the chapter overview click [here](mdwiki.html#!00overview.md)

To return to the Raspberry Pi Recipes page click [here](http://domhnallohanlon.github.io/rpi)

## What's Next?

Great stuff - why not try set up your own [web server?](mdwiki.html#!01overview.md)