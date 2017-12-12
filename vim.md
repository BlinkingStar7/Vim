# Vim shortcuts

### MASSIVE help document
* open vim and type `:help | only`
* will open help.txt in whole window

### Navigation through tags
* `CTRL-]` to into a tag
* `CTRL-O` to go back
* `CTRL-I` to go through

### Compatible option
* `nocompatible` : Vi-compatibility switched off

------------------------------------------------------------

## Chapter 2
* `x`	: to delete a char on cursor
* `dd`	: to delete a line
* `J`	: to delete a line break
* `U`	: undo things in line(if two times, Undo Undo)

### `:wq` family
* `:ZZ`	: Save and exit. Same with `:wq`
* `:x`	: Save when it has been modified and exit

> **Difference between `:wq` and `:x`**  
>
> `:wq` always saves file whereas `:x` saves file only when it has been modified
Huge difference when you use *make* command (based on modification times)

* `e!`	: Reload original version of this file

------------------------------------------------------------

## Chapter 3
* `{number} $`	: move to the end of below lines (1$ same, 2$ next line ...)
* `;`	: Repeat search
* `,`	: Repeat search in opposite direction
* `%`	: Finds first parenthesis and go to it's pair

### Moving in file
* `gg`	: to the begining of a file
* `G`	: to the end of a file
* `{number} G`	: move to number line
* `{number} %`	: move to number% of file
* `H`	: to the begining of window (Home)
* `M`	: to the middle of window (Middle)
* `L`	: to the last of window (Last)

### Scrolling file
* `CTRL-B`	: scroll Below
* `CTRL-U`	: scroll halfway Up
* `CTRL-Y`	: scorll up
* `CTRL-E`	: scroll down(Extra line)
* `CTRL-D`	: scroll halfway Down
* `CTRL-F`	: scroll Forward
* `zt`	: put cursor top
* `zz`	: put cursor middle
* `zb`	: put cursor bottom
* set scrolloff={Number}	: option to always put some lines below cursor


### Search texts
* `/string`	: search string
* `?string` : search string opposite way
* `n`	: goto next match
* `N`	: goto next match opposite way
* set ignorecase	: option to ignore case
* **Every boolean options has option or nooption**
* `*`	: search for the word in cursor
* `#`	: search for the word in cursor opposite way

> **Match start and end of word**
>
> Use `\>` for word ends and `\<` for the begining. By default, ``*``and `#` will use these to search. If you want to allow part of words to match use ``g*`` instead
> * `g*`	: search for the word in cursor(partial word allowed)

> **Highlight option**
>
> `:set hlsearch` to set general configuration. use `:nohlsearch` to erase highlight for only this time.

### Search patterns
* `/word$`	: end of the sentence
* `/^word`	: beginning of the sentence
* `.`	: any single character

### Marks
* Unnamed mark
	> **Jump command** 
	>
	> Includes search(`/` or `n`) and line jumps(`G`) but not `j`, `k`

	* `''`	: move to previous jump position
	* `CTRL-O`	: jump to Older position
	* `CTRL-I`	: jump to Newer position (I is next to O)
	* `Tab`	: same with `CTRL-I`
	* `:jumps`	: list of jump positions

* Named mark
	* `m{alpha}`	: set mark alphabet
	* `'{alpha}`	: go to mark
	* `` `{alpha} ``	: go to mark (line and col)
	* `:marks`	: list of marks
	* `:delmarks {alpha}`	: delete marks


	> **Special marks**
	>
	> * `'`	: last jump position
	> * `"`	: last editing file
	> * `[`	: start of the last change
	> * `]`	: end of the last change
	
------------------------------------------------------------

## Chapter 4

### Changing small texts
* `x`	: `dl`
* `X`	: `dh`
* `s`	: `cl`
* `S`	: `cc`
* `r`	: `cl`, `s`
  * Can do things `5rx` which will change next 5 chars to x
* `.`	: Repeat last change (except `u` and `CTRL-R`)
* `R`	: replce mode
* `BS`	: backspace (undo changes in insert mode)
* `I`	: start insert after moving the cursor to the first non-blank in line

### Visual mode
* `v`	: visual mode
* `V`	: line visual mode
* `CTRL-V`	: block visual mode
> Going to the other side
> - `o`	: move to the other side
> - `O`	: move to the other diagonal (in block visual mode)

### Moving text
* `p`	: put below the cursor(more than a line) or after the cursor (a word)
* `y`	: `yl` or `yw` are also possible (`Y` == `yy`, `D` == `d$`)

> __Text objects__

> Instead of operator - motion, operator - text object is also possible
> - `daw`	: delete a word(where cursor is)
> - `cis`	: change inner sentenece(excluding white spaces)
> - `cas`	: change inner sentenece(excluding white spaces)

------------------------------------------------------------

## Chapter 5

### Example options
* `set nocompatible`	: Use vim only (not vi)
* `set autoindent`	: Newly created line has same indent of the previous line
* `set hlsearch`	: highlight matches
* `set showcmd`	: Show incomplete command in the lower right corner
* restore cursor
      autocmd BufReadPost *
	    \ if line("'\"") > 1 && line("'\"") <= line("$") |
	    \   exe "normal! g`\"" |
	    \ endif
* `set ruler`	: show cursor position and %
* `set optionname&`	: set option to default value

### Simple mapping
* `:map <F5> i{<Esc>ea}<Esc>`	: make "word" into "{word}", should literally type 4 characters for `<F5>`
* map to `\op` can avoid mapping to exist command 


------------------------------------------------------------

## Chapter 7

### List of files
* `vim one.c two.c three.c`	: open several vim files
* `next`	: move to next file(quit current file)
* `wnext`	: save and move next
* `2next`	: move tot 2 next file
* `previous`	: move to previous file
* `last`, `first`	: move to a last/first files
* `args`	: see current location
* `args *.txt`	: edit another list of files
* `CTRL-^`	: move to alternate file

### MARKS
* `'"`	: last cursor position (where exited)
* `'.`	: last change position
* lower case marks are local to file
* upper case marks are global (can be used from any file)
	> __Tip__
	>
	> H for header file, M in makefile, C in code file
* `marks {mark}`	: show marked position
* `CTRL-O`, `CTRL-I`	: older and nwer positions

### Registers
* `"{a-z}yw`	: yank to register
* `wdaw`	: delete to register
* `:write >> logfile`	: append current file to logfile

### Viewing a file
* `vim -R file`	: readonly mode
* `view file`	: readonly mode
* `vim -M file`	: unmodifiable mode

### Opening a file
* `w newfile`	: write current file to newfile
* `sav(eas) newfile`	: write current file to newfile and open

------------------------------------------------------------

## Chapter 8

### Spliting new windows
* `split`	: make a horizontal new window of current buffer above
* `only`	: closes all windows, except for the current one
* `CTRL-W CTRL-W`	: move cursor from one window to the other
* `split {file}`	: open file above
* `{num}split {file}`	: split window with num line size`
* `vsplit`	: make a vertical new window
* Putting `vertical` command will create everyting vertical

### Window manipulation
* `CTRL-W +`	: increase one line
* `CTRL-W -`	: decrease one line
* `CTRL-W =`	: set same height
* `CTRL-W t`	: goto top window
* `CTRL-W b`	: goto bottom window
* `{height}CTRL-W _ `	: set height
* `CTRL-W {HJKL}`	: move window that direction


### Vertical new windows


