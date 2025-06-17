### Basic Terminal Commands
- `pwd` - _print working directory_, this shows you the full path of the directory you are currently in.
- `ls` - _list_ all contents of the directory
- `cd` - navigate to a directory
- `tab` - autocomplete the file or directory you are beginning to type
- `.` - the current directory you are in
- `..` - the directory above the one you're in
- `code` - command to open up a directory in vscode
- `~` - home or root
- `mkdir` - _make directory_
- `touch` - create a file
- `mv` - move a file or directory
- `rm` - _remove_ a file (this is permanent deletion)
- `rm -rf` - _remove_ a directory (this is permanent deletion)

_add this function to your .zshrc file for a safer way to delete a directory_
1. run the command `code ~./zshrc` in your terminal to open your zsh configuration file in vscode
2. Add the following to the bottom of the file
3. Reload your shell instance (your terminal) with the command `source ~/.zshrc`
```bash
function nuke {
	echo -n "Are you sure you want to PERMANENTLY delete $1 [y/n] "
	read yn
	case $yn in
		[Yy]*) rm -rf "$1"; return 0 ;;
		[Nn]*) echo "That was a close one. Exiting."; return 1 ;;
		*) echo "Invalid response. Exiting."; return 1 ;;
	esac
}
```
### VS Code Commands
- Selecting Code: `shift + click`, `double click`, `triple click`
- Coping and Pasting Code: `cmd + c / cmd + v` | `ctr + c / ctrl + v`
- Undoing: `cmd + z` | `ctrl + z`
- Redoing: `cmd + shift + z` | `ctrl + shift + z` | `ctrl + y`
- Moving a line of code: `opt + arrow` | `alt + arrow`
- Copying a line (or selection) of code up or down: `opt + shift + arrow` | `alt + shift + arrow`
- Saving a file: `cmd + s` | `ctrl + s`
- Saving all files: `cmd + opt + s` | `ctrl+k s`
- Selecting multiple instances of the same word: `cmd + d` | `ctrl + d`
- Select *every* instance of the same word: `cmd + shift + l` | `ctrl + shift + l`
- Place your cursor in multiple places: `opt + click` | `alt + click`
- Select all: `cmd + a` | `ctrl + a`
- Formatting: `opt + shift + f` | `alt + shift + f`

### Other Commands
- Switching Windows `cmd + tab` | `alt + tab`
- `cmd + ~`
- Splitting screens `ctrl + opt + arrow` | `windows + arrow`