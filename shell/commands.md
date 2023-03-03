# Shell Commands
Following are the commands that will make you familiar with Shell.

## `echo`

'echo' is a command to print out messages on your console, like the print() function in any programming language 

```sh
echo 'Hello shello!!'
```
> output: `Hello shello!!`

```sh
echo $COLUMNS X $LINES
```
> output: `80 X 24`

*Note* that it is case sensitive, the variables needs to be called uppercased

## `ls` and `cd`

ls means list, it lists all the files and folders in a particular folder.

cd means change directory, the last will change the directory/folder/file you are accessing.
```sh
ls
ls -l  // it will list the working directory/files and shows more information on each of the folder/files like name, date, size etc
ls -l *.txt    // it will list all the files with txt extension
cd /path/to/desired/folder   // will change the working directory to provided path
cd .. // will change the working directory to its immediate parent directory
cd frontend // will change the working directory to frontend directory
```

## `pwd` (Printing working Directory)

Sometimes the terminal you are using will not show you the directory you are at the moment, that is when you use pwd command.

```sh
pwd
```

## `mkdir`, `mv` (Organising Files)

mkdir: stands for make directory
mv: stands for move

```sh
mkdir Desktop/folder_name       // it would create a new directory
mv file.txt new_folder          // it would move file.txt to the provided folder ie: new_folder
mv Desktop/new_folder/*.pdf Desktop     // it would move all the pdfs to Desktop directory
```

## `curl` (Download)

This is the way to download files inside shell env, 


```sh
curl -L -o dictionary.txt 'https://tinyurl.com/zeyq9vc'
```

It would hit the tinyurl and saves its response inside dictionary.txt after following redirects.
-L: specifies follow redirects as well


## `cat`, `less` (File View)

cat: is short for catenate or concatenate.It reads the file and output its content
less: shows you piece by piece of a file, you can scroll down page to see line by line

```sh
cat dictionary.txt
less dictionary.txt
```

## `rm`, `rmdir` (Removing files)

rm: is short for removing files
rmdir: is short for remove directory

```sh
rm dictionary.txt
rmdir curldata/dictionary.txt
```

## `grep`, `wc` (Search and Pipes)

grep: global regular expression print, which means it can be used to see the received input matches a specified pattern.
wc: word count
```sh
grep shell dictionary.txt
bombshell
bombshells
bushelled
cockleshell
eggshell
```
Above we searched for all lines inside the dictionary.txt file that contains the shell word

```
grep shell dictionary.txt | less
```
When the output of lines of lines searched is too big, we can use the vertical bar | (pipe) to send the output to less command, as the example below:

```sh
curl -L 'https://tinyurl.com/zeyq9vc' | grep fish | wc -l
```
grep found the 'fish' word on the URL and fed it to word count to list the number of lines it was found on, in this case 105 lines.

```sh
curl -L 'https://tinyurl.com/zeyq9vc' | grep -c fish
```

Another way of doing that is giving the grep a '-c' to count the number of 'fish' words found.
```sh
grep -c ibo dictionary.txt
```

grep will look for the word ibo inside dictonary.txt file and output its count

## Environment variables and shell

As other programming languages, shell has its own syntax to give variables values (=) and to call ($) these variables
```sh
numbers='one two three'
echo $numbers
echo $PWD
```

## Controlling the shell prompt

There are many different types of shells which can be used by Linux terminals.By default, The Bourn Again SHell, or bash for short is used. Upon logging in, several login scripts are run which loads a users personal preference. One of these scripts is `.bashrc`
To edit your .bashrc file use a command line editor like vim or nano:

```sh
vim ~/.bashrc
nano ~/.bashrc
```
To modify an environment variable, like PATH, add the line:
```sh
export PATH=$PATH:<path/to/dir>
```
Activating a Python environment is as simple as adding the line:
```sh
source <path/to/env>/bin/activate
```
You can create aliases as well
```sh
alias ll="ls -l"
```
Press escape then :wq in case of vi
Press CTRL-Z follwed by Y in case of nano