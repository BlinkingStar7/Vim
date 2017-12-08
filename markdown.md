# [Markdown] (https://github.github.com/gfm/)

## Blocks and inlines
* Documents are a sequence of Blocks
	* paragraph, block quotation, list, heading ...
	* Blocks often contain other blocks
	* Some block(like headings and paragraphs) contain inline context
          * text, links, code spans ...
* Block indicator takes precedence over inline structure(Block structure parsed first)
* There are continaer blocks(who can possess other blocks) and leaf blocks

## Leaf blocks
### Thematic breaks
* Line consisting of 0-3 spaces of indentation and three or more `-`, `_`, `*`
* Can put spaces between them `(EX) - - - - - `
* But no other characters in the line
* Do not need blank lines before or after
* Can interrupt paragraphs

### ATX headings
* Series of # plus at __least one space__ and contents for heading
* This is not a heading `#5 bolt` or `#hashtag`
* Do not need blank lines before or after
* Can interrupt paragraphs

### Indented code blocks
* Start with 4 or more spaces
* And end when it met another block(which doesn't meet indentation rule)
* Contents are not interpreted as markdown
* __Can't interrupt a paragraph(need a preceding blank line)__
* But no need to put blank line after indented code blocks

      [EX]
	  Foo
	      bar
	  will be
	  <p> Foo bar </p>
* List item vs Indented code blocks : list takes precedene

### Fenced code blocks
* Start with three \` or ~ characters followed by info string
* Can interrupt a paragraph & Don't need blank lines

### Paragraphs
* A Sequence of __non-balnk lines that cannot be interpreted as other blocks__
* Lines are concatenated and then striped 
* Every consecutive tabs and spaces are treated only once (HTML thing)

### Blank lines
* Blank lines between blocks are ignored, except for determining whether a list is tight or loose


## Continaer blocks
### Block quotes
* Block quote marker : > + space or > itself
* Can be indented 0-3 spaces
* If a string of lines Ls constitute a sequence of blocks Bs,
	* Basic case : block quote marker + L (everyline) is block quote of B
	* Laziness : can ommit quote marker if next non-whitespace character can't initiate new paragraph(if A and B are in same paragraph, can ommit B's marker)
	* Consecutiveness : should put a blank line between two block quotes
* Can interrupt paragraphs and doesn't need blank lines
* But there can be a situation where laziness trigger ambiguity(put blank line)
* __Because block quote marker includes a one space, you should start with 5 spaces if you wnat to put indented code block__


### Lists items
* List marker
	* Bullet list marker : *, -, +
	* Ordered list marker : sequence of 1-9 digits followed by . or )
* Unordered list : Can use any of *, -, +
* Ordere list : Can use any nubmer, but should start with 1.
* If a string of lines Ls constitute a sequence of blocks Bs, __not separated from each other by more than one blank line__
	* _W includes initial indent too!_
	* Base case : which starts with __non-whitespace character__ 
				 list marker(W) + initial spaces(1-4, N) at the first line and indent W+N in the other line is a list item
	* Code block : If you want to start with a code block, you should put 5(W+1+4) spaces (1 for marker, 4 for code block)
	* Indentation : Indenting above cases 0-3 spaces is same
	* Laziness : You can omit indentation (and even part of it) when the next non-whitespace char is paragraph continuation
	* Sublists : You have to indent enough to make them included in a same paragraph	
	
### Lists
* Sequence of list items that may be __seperated by any number of blank lines__
* loose : any of list items are seperated by blank lines or there is a blank line within list items (\<p> tags are used)
* tight : otherwise (no \<p> tags are used)
* List can interrupt paragraph(terminate paragraph)
* To sepearte two lists, you should put empty HTML comment (\<!--.-->)


### Code spans
* You can put `code` with \` backtick quotes
* From same length of backtick to same length
* Striped and line endings are treated as spaces


### Links
* `[TEXT](URL)` : inline links
* `[TEXT][Tag]` : reference-style links

  need to put `[Tag]: URL "title"` somewhere in the document
* `[Tag]` : shortcut reference links

  need to put `[Tag]: URL "title"` somewhere in the document

* `<URL>` : auto link (Should put absolute URL)
* Tags are case-insensitive

### Images
* Simillar to Links
* `![TEXT](URL)` : inline links
* `![Tag]` : shortcut refence links

### Hard line breaks
* two or more spaces that does not occur at the end of a block
* \\ can be used too
