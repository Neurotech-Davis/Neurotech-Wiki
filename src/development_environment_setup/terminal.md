By Priyal Patel for _Neurotech@Davis_

# What is the Terminal?

<img width="225" alt="terminal" src="https://github.com/user-attachments/assets/c6b8b932-01b7-4194-ae33-b34f29b7bb38" />

The Terminal is an application primarily used to easily access and edit your files using special commands. It is referred to as the Command Prompt on Windows. The commands used will differ based on the type of computer you have such as a MAC or Windows laptop. Developers also use the terminal to install packages and run their code. The code's output or errors with how the code was written will be printed in the terminal.

**Commands**

<img width="350" alt="Screenshot 2025-01-21 at 6 06 26 PM" src="https://github.com/user-attachments/assets/c249d6fe-1b61-4599-a913-bc874ab6af8c" />

Commands are what you type after the cursor mark. Commands are structured as "[abbreviated action] [inputs]". When reading an instruction set, you can recognize terminal commands by '$', '>', or '%' appearing before the command. To run the command, you will need to copy everything that appears right after one of these symbols into the terminal and then hit enter. Commands are space and spelling sensitive, so you need to make sure you write each command exactly as it appears.

**Path**

A path is a way to represent where a folder or file is located. Each folder or file is separated by a '/'. Your desired folder or file will be the rightmost item and the folder(s) that contains this item will be located to the left; for example, "/folder/folder/file".

**Absolute Path**

This path starts with the root directory usually the 'Users' folder. The root directory is the folder that holds all of your folders and files; for example, "/Users/priyal/Desktop/Neurotech".

**Relative Path**

This is the shorthand version of the absolute path. To represent the previous folder, you can use '.'; for example, if you are currently in 'priyal' folder, then your shorthand path is "./Desktop/Neurotech".

# Common Linux Commands

If you have a Windows laptop, then you will need to either install WSL before being able to run these commands or use the equivalent Windows commands. See 'Additional Resources' for more information.

Manual Page: man

See what a command does and how to use it.

```
$ man pwd
```

Present Working Directory: pwd

See what folder you are currently in (absolute path).

```
$ pwd
```

List: ls

See the contents of the folder you are currently in.

```
$ ls
```

Concatenate: cat

See the contents of one or more files in the order specified.

```
$ cat <file1 name> <file2 name>
```

Move: mv

Move a file to a new location or rename file/keep file in same location.

```
$ mv <file-you-want-to-move> <new-path or name>
```

Change Directory: cd

Go from your current folder to another folder.

```
$ cd <absolute or relative path>
```

The shorthand to go back to the parent folder is:
'''
$ cd ..
'''
Make Directory: mkdir

Create a folder with the specified name.

```
$ mkdir <folder name>
```

Remove Directory: rm -d

```
$ rm -d <folder name>
```

Remove File: rm

```
$ rm <file name>
```

Clear: clear

Remove all commands from terminal display. If you use the ^ arrow, then you can still see some of the past commands used.

```
$ clear
```

Stop Execution: ^c (ctrl+c)

After running a command, you can use this shortcut to prevent the command from finishing executing the command.

```
$ <command>
^c
```

For a full list of commands, see the 'Unix Tutorial' in Additional Resources.

# Additional Resources

- [WSL Installation Guide](https://learn.microsoft.com/en-us/windows/wsl/install)
- [Windows Commands](https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/windows-commands)
- [Unix Tutorial](https://info-ee.surrey.ac.uk/Teaching/Unix/index.html)
