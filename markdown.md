# [Markdown] (https://github.github.com/gfm/)

## Blocks and inlines
* Documents are a sequence of Blocks
	* paragraph, block quotation, list, heading ...
	* Blocks often contain other blocks
	* Some block(like headings and paragraphs) contain inline context
		* text, links, code spans ...
* Block indicator takes precedence over inline structure(Block structure parsed first)
* There are continaer blocks(who can possess other blocks) and leaf blocks

### Leaf blocks
#### Thematic breaks
* Line consisting of 0-3 spaces of indentation and three or more `-`, `_`, `*`
* Can put spaces between them `(EX) - - - - - `
* But no other characters in the line
* Do not need blank lines before or after
* Can interrupt paragraphs

#### ATX headings
* Series of # plus at __least one space__ and contents for heading
* This is not a heading `#5 bolt` or `#hashtag`
* Do not need blank lines before or after
* Can interrupt paragraphs

#### Indented code blocks
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

#### Fenced code blocks
* Start with three \` or ~ characters followed by info string
* Can interrupt a paragraph & Don't need blank lines

#### Paragraphs
* A Sequence of __non-balnk lines that cannot be interpreted as other blocks__
* Lines are concatenated and then striped 
* Every consecutive tabs and spaces are treated only once (HTML thing)
* To put `</br>` end sentence with two spaces or \\

#### Blank lines
* Blank lines between blocks are ignored, except for determining whether a list is tight or loose

### Continaer blocks
* Block quotes
	* Start with 0-3 spaces of indentation and > charater 
	* Can omit > charater (if the content is continuous paragraph)
	* If you want to put indendted code block inside, start with 5 spaces











## Block quotes
* Use > to initiate block quotes
* Best to start every line with > but can be lazy : only put > at the start of paragraphs
* Can be nested (use >>)


## Lists
* Unordered list : Can use any of *, -, +
* Ordere list : Can use any nubmer, but should start with 1.
* Shoulde be followed by one or more spaces(tabs)
* If you seperates lists with blank lines, mark down will put their item into `<p>` tags
	If you want to put multiple paragraphs within the same item, you should start first line of the
	paragraph with 4 spaces or a tab.
* To put block quote in list, you should indent >
	> like this


## Code block
* To put code blocks, you should start with indent of 4 spaces or a tab
* And within a list, you should double your indent (8 spaces or two tabs)  


## Code 
* You can put `code` with \` backtick quotes.
* If you have \` bakctick in your code you have to put double backtick to start code
* all the speacial characters in code area will be encoded as HTML entitiy automatically


## Links
* `[Tag](URL)` : inline links
* `[Tag][ID]` : reference-style links
 need to put `[ID]: URL` somewhere in the document

