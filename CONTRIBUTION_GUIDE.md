# Contribution Guide

For internal & external contributors to the book. Please add anything to this document you find helpful.

See [template chapter](https://github.com/afrimapr/afrimapr-book/blob/main/16-template.Rmd) which sets out standard format for chapters

Internal contributors are encouraged to push text changes directly (you don't need to submit pull requests). To minimise potential for conflicts remember to pull before making changes and communicate with others about what you are working on. 

## to build the book & debug locally

`bookdown::serve_book()`  
This updates local copy of the book every time you make a change (turn off by restarting R or with `servr::daemon_stop(1)`).
It creates a temporary file `bookdown-demo.Rmd` which collates all the code from the chapters into a single file. Error messages may refer to line numbers in this file, e.g. `Quitting from lines 901-906 (bookdown-demo.Rmd)`. To debug look up the lines in `bookdown-demo.Rmd` and then find where they are in a chapter source file and attempt to fix the problem there. You may be prompted to delete the temporary file before building the book locally again, it is fine to do that.  

## temporary comments

To make temporary comments for yourself and others enclose them in square brackets []. You can include your name or a collaborators immediately after the bracket so that you or others can search for things you still need to look at. So Andy might include :
[andy: I haven't finished this] or [martyna: can you have a look at this?]. If it is a bigger thing we recommend submitting a Github issue. Markdown comments that will be visible in the source file but not in the created book can be enclosed with <!--- commented text --->.


## markdown tips

* Blank lines before section headers (# ## ##) to get them to work
* For R to consider a chunk of text a section heading there needs to be a space between the hashtag # and the title
* I sometimes run a section of code or text in a simple markdown file to check it. Great way to quickly check the formatting. 
* The numbering of the section can be removed by using {-} after the section title
* Sub-sections (level 2 headings) cannot be referred to (links cannot be created)
* To control how table of contents (TOC) behaves when clicking on it we need to set 'collapse:' in output.yml file to: section, subsection or null, depending on the level we want our TOC to expand and collapse. So if you want only the top-level headings to be displayed initially (like in our book) use 'section'.
* It is worth naming code chunks so that it is easier to identify failing code in case it happens. The name can be added to the code chunk in the following way: {r code-name-without-spaces, ...}
* You can collapse (unfold) parts of the Rmd file with the downward (upward) pointed arrow next to the line number, where this function is possible. The collapsible parts are at the section/subsection level or r code chunks. It makes it easier to navigate through the long chapter files, where finalised parts can be "hidden".
* A keyboard shortcut Ctrl + Shift + F allows for searching of a phrase inside the all files in the project.
* To quickly rename a .Rmd file use file.rename("old-name.Rmd", "new-name.Rmd") in the Console. The files with new names have to be added to Github before the changes are pushed. This can be done by typing "git add new-file.Rmd" in the Terminal. After that commit and push changes as usual.
* To hide a chapter (and stop it from rendering altogether) add an underscore _ before file name. All the files that start with an underscore are passed during rendering but they still appear in the repo.

## Netlify deploy

We have stopped auto-publishing, so contact Andy to update manually from the draft after you've made a commit.

## required packages

It's best not to include evaluated code to install packages in the Rmd files. If you want to add a new package, add it to Imports in the Description file. If you want to demonstrate install you can set eval=FALSE for that chunk. You will need to have packages installed locally to build the book. 