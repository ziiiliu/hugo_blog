---
title: "Markdown basics"
date: 2019-09-17T14:50:36+08:00
draft: false
tags: [md]
---
* ### Headers 
     First level header: ====== beneath  
Second lever header: ------- beneath

* ### Size
    No.s of # you put in front of a paragraph determines the size of 
the font of this paragraph.

* ### Blockquote 
  >So this is a blockquote. 

    A blockquote is done with a '>' at the very front of the line for every line that you want to quote.

    >This is one line  
    >This is another  
    >Easy Peasy
 
* For a nested blockquote, we simply use multiple > to make this happen.

        >Hi
        >
        >>Hello
    
  > Hi
  >
  >> Hello

  _NB: The blank quote in-between the Hi and Hello is necessary._



* ### Emphasis
   Use \* or \_ on both sides to make *italics*, like this:
 \*italics\* ; And __bold__ with double \* or \_, like  this: 
 \__bold\__
 
* ### Code Blocks
  For code blocks, we simply indent them with 4 spaces or 1 tab  

        This is a code block.
    If the code block is inside a list (like this one), then use two tabs or 8 spaces to deliever the effect.
  <br/><br/>
  For an in-line code, we can simply use \`blah blah\` to make `blah blah` happen.
    
* ### Others 
  Use \<br/\> to create as many blank lines as you want.

* &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;To do an indentation manually, we have to use
the inline html code (just like the creating blank line feature) `&nbsp;`. One such code 
represents one space.

* To have a horizontal line, use --- or ***.

* Links such as this, [Google.com](https://google.com), is made by enclosing the
link text in the [] square brackets and putting the URL in parantheses directly
afterwards.

  Foe example, we can have [Github](https://www.github.com "The only and real hub you need")
  using the code`[Github](www.github.com "The only and real hub you need")`.
  
  To quickly turn a URL into a link, simply put angle brackets around it.
  <www.cam.ac.uk>
  
* Don't forget many html features and codes are not supported here in markdown,
since md is essentially a converting-to-html tool. Use HTML codes here instead
if some particular syntaxes are not supported by md.

* For images, it's basically the same as adding links. Just add a ! in front of the square brackets. That's it!

* If you want the link to open a new tab, use html codes instead here.

        <a href = "https://apple.com" target = "_blank"> Apple </a> 
       

