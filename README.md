# vtt2txt
Script to convert vtt files to plain text files

The script is pretty easy and can be opened with any text editor.
It's a bash script, don't run it with sudo privileges if not necessary.

### 1. Make the Script Executable
Ensure that the script is executable. If you haven't done so already, use the command:

```chmod +x vtt2text```

### 2. Move the Script to a Directory Included in the PATH
To make the script usable as a system command, you need to place it in a directory that is included in the PATH environment variable. Some common directories that are part of the PATH are:

  */usr/local/bin/
  */usr/bin/
  */home/your_user/.local/bin/ (on some distributions)
  */home/your_user/bin/ (you can create this directory if it doesn't exist)
  
To move the script, use the mv command. For example, to move it to /usr/local/bin/, run:

```sudo mv vtt2text /usr/local/bin/```

If you prefer not to use sudo, you can create a bin directory in your home directory (if it doesn't already exist) and move the script there:

```mkdir -p ~/bin```

```mv vtt2text ~/bin/```

### 3. Update the PATH (if necessary)
If you have moved the script to a directory that is not already included in the PATH, you need to add that directory to the PATH. For example, if you placed the script in ~/bin/, add the following line to your .bashrc (or .zshrc, depending on the shell you use):

```export PATH="$HOME/bin:$PATH"```

After updating .bashrc or .zshrc, run

```source ~/.bashrc```

Or if you use zsh:

```source ~/.zshrc```

### 4. Run the Command
You should now be able to run your script as a regular command from any directory by simply typing the command name (in this case, vtt2text), followed by the required argument:

```vtt2text file.vtt```

This command will convert the subtitles in the .vtt file to a .txt file in the same way it would if executed locally in the script's directory.
