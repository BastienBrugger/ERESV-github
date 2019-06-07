
Content borrowed from : **Command Line Essentials: Git Bash on Windows (Udemy)**

Why command line?
- Lots of command line centric tools (git, etc.). More powerful control than their GUI versions
- Standard syntax across platforms
- Online help; extensive documentations
- Excellent opportunity to learn what's really going on at low level

What is Shell?
- User interface that allows interacting with the computer's resources like files and folders. 
- Text-only shells (as compared to graphical shells like Windows) are commonly referred to as *command line* interpreters.  
- Bash is the default command line interpreter on MacOS and most Linux distributions. 
- Bash is also a rudimentary programming/scripting language
- More expressive than Windows command shell
- Git Bash is a nice Bash shell environment in Windows; free and open source; comes installed with git

Basic commands:
- `pwd`: present working directory
- `ls`: list files and folders
- `ls -l`: list of files and folders with more details like read/write persmissions, etc.
- `cd`: change directory (press Tab for auto-completion)
- `cd ..`: backup one directory level
- `cd My\ Documents/`: backslash `\` used to denote the `space` character in file or folder names
- `cd ~`: return to user's home directory; also typing just `cd` works 

Locating commands: `which ls` allows to figure out the location of a command, if its installed. 

Echo:
- prints on the screen
- `echo "Hello World"` will print `Helo world`
- `echo $PATH` will print the value of the system variable `PATH`; $ indicated variable

Reviewing file content:
- `cat <file-name>` directly outputs the content of the file on to the terminal
- `less <file-name>` avoids the file content filling up the entire display; scroll up and down; exit with `q`

File Handling:
- `touch <file-name>` to create a file
- `mv <old-file-name> <new-file-name>` to rename a file; technically moving the old file's content to a new file
- `rm <file-name>` to remove the file

Create and delete folders:
- `mkdir <folder-name>` to make a new folder
- `mkdir -p <level-1-folder>/<level-2-folder>/<level-3-folder>`: use `-p` to create multi-level folders at once
- `rmdir <folder-name>` to remove a folder
- `rmdir` will fail if the folder is not empty; solution is to force it to work with `rm -r -f`, where `-r` stands for recursive and `-f` stands for force. *Use with caution!!!*

Clear the output on the screen: `clear`

Exit the terminal: `exit`

Output to a file:
- `echo "some text" >> demo.txt`: creates demo.txt and adds the text or appends the text if demo.txt already exists.
- `echo "some text" > demo.ext`: will overwrite the content of demo.txt
- Output of commands can also be written to files. For example, `ls -l > demo.txt` writes the output of `ls -l` to demo.txt

Create a simple shell script:
- Shell scripts are basically shell commands (in this case Bash) placed into a file for later execution. 
- Open a new shell script file using the text editor you have linked to Git Bash. A popular choice is notepad++. 
  - `notepad++ example.sh`
- *Note*: Make sure that notepad++ is set up to use Unix line endings (Edit > EOL Conversion > Unix)
- In example.sh, type this script:
  - `#!<path to bash>`
   - This is called a shebang or a "bang" line.
    - It is nothing but the absolute path to the Bash interpreter.
    - It consists of a number sign and an exclamation point character (#!), followed by the full path to the interpreter such as /bin/bash.
    - All scripts under Linux execute using the interpreter specified on a first line.
    - Almost all bash scripts often begin with #!/bin/bash (assuming that Bash has been installed in /bin)
    - This ensures that Bash will be used to interpret the script, even if it is executed under another shell.
    - `echo "Hi, everyone"`: simple command that will be executed when we run this script
- Save and exit the file.
- `ls -al` to see the permissions of `example.sh`. If execute permission flag `x` is absent, we can add that using `chmond +x example.sh`
- `./example.sh` to execute the example.sh file which is in the current directory. For executing a file in a different directory, just type `<path to file>`. The dot at the start is not needed.

Customizing the Bash environment using the .bashrc file:
- `cd ~`: Make sure you are in the root directory
- `notepad++ .bashrc` create/open the .bashrc file
- *Note*: Make sure that notepad++ is set up to use Unix line endings (Edit > EOL Conversion > Unix)
- A simple example is establishing an alias for an existing commands. This is usually used to shorten the length of long commands. 
  - `alias npp='notepad++'`: this means that `npp` is now equivalent to the command `notepad++`
- Before using the alias we need to reload the .bashrc file using `source .bashrc`
- Now `npp` should open notepad++


   





