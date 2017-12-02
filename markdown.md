# [Markdown] (https://github.github.com/gfm/)

## Paragraphs
* Spaces in front of a sentence means nothing unless...
	* You put 4 spaces or a tab in the start of line, it will make codeblock
		(EX) like this
* Tabs in front of a sentence are treated as 4 spaces 
* If you want to move to next line, end sentence with two spaces  
(EX) This sentence will go to next line

* Blank lines are used to differentiate paragrahs
	

* Should start with characters (not spaces or tabs)
* Sepearted by blank lines
* __When you want to put `<br />`__
	* You should end your sentence with _two or more spaces_. Or,
	* You need to seperate paragraphs with _one or more blank lines_.


## Blocks and inlines
* Documents are a sequence of Blocks
	* paragraph, block quotation, list, heading ...
	* Blocks often contain other blocks
	* Some block(like headings and paragraphs) contain inline context
		* text, links, code spans ...
* Block indicator takes precedence over inline structure
* Continaer blocks(who can possess other blocks) and leaf blocks

### Leaf blocks
* Thematic breaks
	* line consisting of 0-3 spaces of indentation and three or more `-`, `_`, `*`
	* Can put spaces between them `(EX) - - - - - `
	* But no other characters in the line
	* Do not need blank lines before or after
	* Can interrupt paragraphs

* ATX headings
	* Series of # plus at least one space and contents for heading
	* This is not a heading `#5 bolt` or `#hashtag`
	* Do not need blank lines before or after
	* Can interrupt paragraphs
	* There is a setext headings which put an underline as a heading indicator

* Indented code blocks
	* Start with 4 or more spaces
	* Can contain several blank lines inside
	* And end with another block(which doesn't meet indentation rule)
	* Contents are not interpreted as markdown
	* __Can't interrupt a paragraph(need a preceding blank line)__
	* But no need to put blank line after indented code blocks

* Fenced code blocks
	* Start with three \` or ~ characters followed by info string
	* Can interrupt a paragraph

* Paragraphs
	* A Sequence of __non-balnk lines that cannot be interpreted as other blocks__
	* Contents are striped 
	* Every consecutive tabs and spaces are treated only once (HTML thing)

* Blank lines
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

