# *nix Scavenger Hunt

Complete the following challenges using the command-line interface on your favorite
Unix or Linux operating system. You are welcome and encouraged to consult any
additional documentation online or in books.

Please add your answers/responses/text pastes to the document after each prompt.

Note: For some of the challenges you will need to reference files included with
this repository, so you will need to fork the repo into your own Github account
and then clone it to your development environment.

## The Challenges

### Navigating the Filesystem

* Get an idea of where you are in the operating system. Use the `pwd` command to find your "path to working directory"--your current location in the filesystem of your devbox. *Paste the output of the `pwd` command here:*

```
==============================================================================
/home/kelly/SUWebDev/github/wats3030-intro-to-unix
==============================================================================
```


* Discover more about this filesystem. Use `ls` (the "list" command)to see what is in this directory. *What directories and files do you see when you run `ls`?*

```
==============================================================================
challenge_files  nix_scavenger_hunt.md          README.md
LICENSE          nix_scavenger_hunt_stretch.md  super_scavengers.md
==============================================================================
```

* You can use *options* to modify how a command runs. Try using `ls -alh` to see the contents of your current directory. *How are the results different when you use the `-alh` options?*

```
==============================================================================
total 40K
drwxr-xr-x  4 kelly kelly 4.0K Jan 15 13:43 .
drwxr-xr-x 13 kelly kelly 4.0K Jan 15 13:43 ..
drwxr-xr-x  7 kelly kelly 4.0K Jan 15 13:43 challenge_files
drwxr-xr-x  8 kelly kelly 4.0K Jan 15 13:43 .git
-rw-r--r--  1 kelly kelly 1.1K Jan 15 13:43 LICENSE
-rw-r--r--  1 kelly kelly 6.0K Jan 16 20:32 nix_scavenger_hunt.md
-rw-r--r--  1 kelly kelly  317 Jan 15 13:43 nix_scavenger_hunt_stretch.md
-rw-r--r--  1 kelly kelly 2.7K Jan 15 13:43 README.md
-rw-r--r--  1 kelly kelly  191 Jan 15 13:43 super_scavengers.md
==============================================================================
```

* The `man` ("manual") command tells you more about how any given command works. (*WARNING:* CodeAnywhere does not support the man command. You can click the following link to complete this task: http://linux.die.net/man/). Run `man` to see instructions about how to use `man`. Then use `man` to learn what the `a`, `l`, and `h` options mean when used with the `ls` command. *Write down what those options do?*

```
==============================================================================
-a, --all
              do not ignore entries starting with .
==============================================================================
-l     use a long listing format
==============================================================================
-h, --human-readable
	          with -l and/or -s, print human readable sizes (e.g., 1K 234M 2G)
==============================================================================
```

* Commands can also take *arguments*, which are usually the names of files or locations that you want the command to work with. Try running `ls /` to see what files are in the *root* directory of the filesystem. *What files and directories do you see listed?*
```
==============================================================================
I'd rather not share that here
==============================================================================
```

* A Unix filesystem has a few special shortcuts to refer to specific locations. `/` indicates the *root* of the filesystem, meaning the top-most directory in the filesystem hierarchy. Use the `cd` ("change directory") command to move to the root directory. (Hint: Use `man` to look up the `cd` command if you have any issues) *Then run `pwd` and paste the output here:*
```
==============================================================================
/
==============================================================================
```
* Another special shortcut in Unix is the `~` location. This indicates the *user root* directory, meaning the top-most directory in the hierarchy that comes below your user account. Use `cd` to move to `~`. *Run `pwd` and paste the response here:*
```
==============================================================================
/home/kelly
==============================================================================
```
* Change directory into the `challenge_files` directory. Use `ls` to find only the files with a `.demo` pattern. *How many files do you find?*
```
==============================================================================
3
==============================================================================
```
* Use the `cd` command to move "up" one directory. *Where are you in the filesystem now?*
```
==============================================================================
/home/kelly/SUWebDev/github/wats3030-intro-to-unix
==============================================================================
```
* Press the up arrow on your keyboard. *What just happened?*
```
==============================================================================
Previous command is loaded into prompt
==============================================================================
```
* Press the up arrow a few more times. *What do you see?*
```
==============================================================================
More previous commands are loaded into prompt
==============================================================================
```
* Run the `history` command. *What do you see?*
```
==============================================================================
Outputs previous commands run sequentially numbered
==============================================================================
```

### Observing the System

* Discover what account you are logged into using the `whoami` command. *What username are you currently using?*
```
==============================================================================
kelly
==============================================================================
```
* Discover who else is on your system with the `who` command. *Are any other users using your system? If so, list them here:*
```
==============================================================================
I'd rather not share that here
==============================================================================
```
* How long has your system been running? Use `uptime` to see, and *paste the result here:*
```
==============================================================================
I'd rather not share that here
==============================================================================
```
* Run `ps aux` and review the results. (Hint: Use `man` to learn more about the `ps` command and options.) *How do you interpret what you see here?*
```
==============================================================================
ps outputs a report of currently running processes in columnar format; the -a
flag displays processes for all users, -u specifies to print associated user
with process, and -x specifies to show processes regardless of if they are
attached to the terminal or not (interpretation: lots going on!)
==============================================================================
```
* Run `top` and review the results. (Hint: You may need to use `ctrl-c` to get out of this app.) *How do you interpret what you see here?*
```
==============================================================================
top and ps are both process viewers but ps provides a static snapshot of
active processes while top gives you a dynamic real-time view of all running
processes
==============================================================================
```

### Finding and Viewing Files

* Make sure you are in the `challenge_files` directory. Use the `*` wildcard to find all the files that have the word "credit" in the filename. *How many files did you find?*
```
==============================================================================
2
==============================================================================
```

* Use the `more` command to view one of the `credit_cards` files you just discovered. (Hint: Type `q` to quit viewing the file. Press the `spacebar` to page down. Use your keyboard arrows to move up/down.) *What is the date in the file you have viewed?*
```
==============================================================================
01-15-2015
==============================================================================
```
* Use the `find` command to search for files more effectively. Search the sub-directories under `challenge_files` to find the location of the file named `modi_laboriosam.txt`. *Where is that file located?*
```
==============================================================================
/home/kelly/SUWebDev/github/wats3030-intro-to-unix/challenge_files/tmp/modi_laboriosam.txt
==============================================================================
```
* Use the `grep` command to search for text within a file. Use `grep` on all the `.user` files in `challenge_files` to find which files contain "WA" (the abbreviation for Washington state). *How many files did you find?*
```
==============================================================================
2
==============================================================================
```
* Use the `-r` option of `grep` to *recursively* find the text "Waldo" hidden in a file somewhere under the `challenge_files` directory. *Paste the result showing the file and line where the word "Waldo" shows up.*
```
==============================================================================
./serial-numbers/eaque_molestiae.txt:4:Ut est maiores quia autem. Nisi modi Waldo sed corporis sit explicabo ut est. Et est placeat ea sunt sunt consectetur sunt incidunt. Explicabo vel esse blanditiis dolorem culpa non quia.
==============================================================================
```

### Pipes and Connecting Commands

* Sometimes it's useful to output the results of a command to a text file for further analysis, reference, or processing. Try running `ls > files.txt`. Notice that the file `files.txt` was created. View that file using `more`. *What do you see in the `files.txt` file?*
```
==============================================================================
list of files in working directory
==============================================================================
```
* Notice that if you run `ls -alh` in the `challenge_files` directory, the files scroll by very quickly. Sometimes it would be better to get the results in a paginated format. Try running `ls -alh | more`. *Describe what you see when you run `ls -alh | more`.*
```
==============================================================================
Output is paginated and you can spacebar through at your leisure
==============================================================================
```
* Earlier, when you viewed the list of active processes on your devbox using `ps aux`, the list was probably really long. You can make this list more manageable by using the pipe (`|`) to filter the results of `ps` using `grep`. Run `ps aux | grep <your_username>` to see what processes are running for your specific user. *Paste the list of processes that reference your username here:*
```
==============================================================================
I'd rather not share that here
==============================================================================
```
