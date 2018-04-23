Open the sudoers file: sudo visudo will open the /etc/sudoers file in the editor defined in $EDITOR (probably GNU nano - set the variable if it's not what you want, eg export EDITOR="nano" and try sudo visudo again).

Add the below line to the end of the file.

username ALL=(ALL) ALL   # Change the user name before you issue the commands
Then perform WriteOut with Ctrl + O. The editor will ask you for the file name to write into. The default will be a temporary file that's used by visudo to check for syntax errors before saving to the actual sudoers file. Press Enter to accept it. Quit the nano editor with Ctrl + X.

Done!

**get from: **https://askubuntu.com/questions/7477/how-can-i-add-a-new-user-as-sudoer-using-the-command-line
