# Vim shortcuts

## MASSIVE help document
* open vim and type `:help | only`
* will open help.txt in whole window

## Navigation through tags
* `CTRL-]` to into a tag
* `CTRL-O` to go back
* `CTRL-I` to go through

## Compatible option
* `nocompatible` : Vi-compatibility switched off

------------------------------------------------------------

## Chapter 2
* `x`	: to delete a char on cursor
* `dd`	: to delete a line
* `J`	: to delete a line break
* `U`	: undo things in line(if two times, Undo Undo)

## `:wq` family
* `:ZZ`	: Save and exit. Same with `:wq`
* `:x`	: Save when it has been modified and exit

> **Difference between `:wq` and `:x`**  

`:wq` always saves file whereas `:x` saves file only when it has been modified
Huge difference when you use *make* command (based on modification times)

* `e!`	: Reload original version of this file

------------------------------------------------------------

## Chapter 3
* `{number} $`	: move to the end of below lines (1$ same, 2$ next line ...)
* `;`	: Repeat search
* `,`	: Repeat search in opposite direction
* `%`	: Finds first parenthesis and go to it's pair

## Moving in file
* `gg`	: to the begining of a file
* `G`	: to the end of a file
* `{number} G`	: move to number line
* `{number} %`	: move to number% of file
* `H`	: to the begining of window (Home)
* `M`	: to the middle of window (Middle)
* `L`	: to the last of window (Last)

## Scrolling file
* `CTRL-F`	: scroll Forward
* `CTRL-U`	: scroll halfway Up
* `CTRL-E`	: scroll up(Extra line)
* `CTRL-Y`	: scorll down
* `CTRL-D`	: scroll halfway Down
* `CTRL-B`	: scroll Below
* `zt`	: put cursor top
* `zz`	: put cursor middle
* `zb`	: put cursor bottom
* set scrolloff={Number}	: option to always put some lines below cursor


## Search texts
* `/string`	: search string
* `?string` : search string opposite way
* `n`	: goto next match
* `N`	: goto next match opposite way
* set ignorecase	: option to ignore case
* **Every boolean options has option or nooption**
* ``*``	: search for the word in cursor
* `#`	: search for the word in cursor opposite way

> **Match start and end of word**

 Use `\>` for word ends and `\<` for the begining. By default, ``*``and `#` will use these to search. If you want to allow part of words to match use ``g*`` instead

> **Highlight option**

`:set hlsearch` to set general configuration. use `:nohlsearch` to erase highlight for only this time.

## Search patterns
* `/word$`	: end of the sentence
* `/^word`	: beginning of the sentence
* `.`	: any single character

## Marks
* Unnamed mark
	* `''`	: move to previous jump position
	
	> **Jump command** 
	  Includes search(`/` or `n`) and line jumps(`G`) but not `j`, `k`

	* `CTRL-O`	: jump to Older position
	* `CTRL-I`	: jump to Newer position (I is next to O)
	* `Tab`	: same with `CTRL-I`
	* `:jumps`	: list of jump positions

* Named mark
	* `m{alpha}`	: set mark alphabet
	* `'{alpha}`	: go to mark
	* `:marks`	:list of marks

	> **Special marks**
	> * `'`	: last jump position
	* `"`	: last editiong file
	* `[`	: start of the last change
	* `]`	: end of the last change
	


