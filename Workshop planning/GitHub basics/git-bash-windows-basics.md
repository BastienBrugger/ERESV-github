
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
- `rmdir` will fail if the folder is not empty; solution is to force it to work with `rm -r -f`, where `-r` stands for recursive and `-f` stands for force. 





