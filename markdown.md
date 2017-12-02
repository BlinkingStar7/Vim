# [Markdown] (https://github.github.com/gfm/)

## Paragraphs
* Every consecutive tabs and spaces are treated only once
* Spaces in front of a sentence means nothing unless...
	* You put 4 spaces or a tab in the start of line,
	it will make codeblock
		[EX] like this
* If you want to move to next line, end sentence with two spaces  
[EX] This sentence will go to next line
	

* Should start with characters (not spaces or tabs)
* Sepearted by blank lines
* __When you want to put `<br />`__
	* You should end your sentence with _two or more spaces_. Or,
	* You need to seperate paragraphs with _one or more blank lines_.


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

