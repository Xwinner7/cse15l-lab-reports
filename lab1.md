Lab Report 1:
---
**examples of using the command `cd` `ls` `pwd` with no arguments**
1. `cd`
   * ![Image](cd.png)
   * The working directory when the command was run is `/home`.
   * Using the command with no argument in this case with `cd` means there's no directory it can be changed into. Hence in the filesystem it would only be `/home` as the given path does not have any files to print out. Futher explains why the output is empty with nothing being printed out.
   * The output is not an error.
2. `ls`
   * ![Image](ls.png)
   * The working directory when the command was run is `/home`.
   * Using the `ls` command with no argument means it would list the the files and folders of the given path, in this case with no given path would list the single folder within the filesystem `/home`, makes the output `lecture1`in blue and bolded font.
   * This output is not an error.
3. `cat`
   * ![Image](cat.png)
   * The working directory when the command was run is `/home`.
   * Using the `cat` command with no argument would not print out any contents as there isn't any contents of any files that are given by the path, path are the argument, hence there's nothing for `cat` to read and print out as output.
   * This output is an error, because it would keep on repeating to print out the blank output with the blank argument non stopping.

**examples of using the command `cd` `ls` `cat` with a path to a directory as an argument**
1. `cd` with path to a directory
   * ![Image](cdWithDirectory.png)
   * The working directory when the command was run is `/home`.
   * Using the `cd` command with a path `/home/lecture1` as an argument permits the swiitch from the current working directory `/home` to the given path `/home/lecture1`, the directory have been successfully changed with the terminal display in green with `~/lecture1`.
   * This output is not an error.
2. `ls` with path to a directory
   * ![Image](lsWithDirectory.png)
   * The working directory when the command was run is `/home/lecture1`.
   * Using the `ls` command with a path `/home/lecture1` as an argument would list out all the name of the file and folder within the filesystem, and in this case from `/home/lecture1`, `Hello.class`, `Hello.java`, `messages` and `README` are the four file and folder within the `lecture1` folder that are being listed out.
   * This output is not an error.
3. `cat` with path to a directory
   * ![Image](catWithDirectory.png)
   * The working directory when the command was run is `/home/lecture1`.
   * Using the `cat` command with a path `/home/lecture1` 
  





For each of the commands cd, ls, and cat, and using the workspace you created in this lab:

Share an example of using the command with no arguments.
Share an example of using the command with a path to a directory as an argument.
Share an example of using the command with a path to a file as an argument.

So that's 9 total examples (3 for each command). For each, include:

A screenshot or Markdown code block showing the command and its output
What the working directory was when the command was run
A sentence or two explaining why you got that output (e.g. what was in the filesystem, what it meant to have no arguments).
Indicate whether the output is an error or not, and if it's an error, explain why it's an error.
