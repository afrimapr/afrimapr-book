# Contribution Guide

For internal & external contributors to the book. Please add anything to this document you find helpful.

See [template chapter](https://github.com/afrimapr/afrimapr-book/blob/main/16-template.Rmd) which sets out standard format for chapters

Internal contributors are encouraged to push text changes directly (you don't need to submit pull requests). To minimise potential for conflicts remember to pull before making changes and communicate with others about what you are working on. 

## to build the book locally

`bookdown::serve_book()`  
This updates local copy of the book every time you make a change (turn off by restarting R).


## markdown tips

* Blank lines before section headers (# ## ##) to get them to work
* For R to consider a chunk of text a section heading there needs to be a space between the hashtag # and the title
* I sometimes run a section of code or text in a simple markdown file to check it. Great way to quickly check the formatting. 
* The numbering of the section can be removed by using {-} after the section title
* Sub-sections (level 2 headings) cannot be referred to (links cannot be created)
* To control how table of contents (TOC) behaves when clicking on it we need to set 'collapse:' in output.yml file to: section, subsection or null, depending on the level we want our TOC to expand and collapse. So if you want only the top-level headings to be displayed initially (like in our book) use 'section'.
* It is worth naming code chunks so that it is easier to identify failing code in case it happens. The name can be added to the code chunk in the following way: {r code-name-without-spaces, ...}