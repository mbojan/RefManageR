biblatex
========

R package biblatex

To Do:
==================================================================================================================
Important
-------------------
1. get DOIs from crossref
2. new open function; convert all other RefManager.R functions to work with bibentry class
3. read pdf's using pdftotext.exe; use list.files to add folder to database
* read bibliographies from pdftotext
4. "+.BibEntry" function for merging two bibentry classes: [S/O thread for overloading `+`](http://stackoverflow.com/questions/8022979/operator-overloading-and-class-definition-in-r-use-a-different-base-field-corpu). Also see ?Ops
  * handling duplicate entries
5. write to zotero: http://www.zotero.org/support/dev/server_api/v2/write_requests
6. boolean for how invalid entries are handled: either change to misc or drop (see what force=TRUE does in bibentry fnctn)
7. new `[` function e.g. db['author', 'mclean', 1:3] = first three entries in bib with mclean as author $\neq$ db[1:3, 'author', 'mclean']
8. add option for sorting results of subsetting based on diff fields and printing. See: utils:::sort.bibentry
9. plot function. sig.: plot(db, field, plottype, ...)  both 'author' and 'author-full' possible          
  * See igraph pkg or perhaps adapt http://bl.ocks.org/mbostock/3037015 (add counts on edges)
  * See the [wordcloud package](http://blog.fellstat.com/?cat=11)
10. make table function.  table(db, field)  both 'author' and 'author-full'    
11. change the print.bibentry function for when style='bibtex' and add style='biblatex'  
  * (i.e. convert biblatex to bibtex for submitting to journal.  
  * i.e. change toBibtex function and add toBibLaTeX function)
[S/O thread explaining how to do this](http://tex.stackexchange.com/questions/114787/converting-from-biblatex-to-bibtex-format-using-biber)  
have check=FALSE argument in print.BibEntry if user does not want to check proper format when printing biblatex or bibtex  
have printonly=FALSE argument in toBibtex.BibEntry and toBibLatex.BibEntry if user does not want converted BibEntry object returned
12. how to change entry type?
* fix print to handle date field and 
* implement a useful summary function
* let users set "[.BibEntry" and "+.BibEntry" defaults using getOptions() or BibEntryOptions() accessors and mutators

### Less Important/Smaller
* Make sure unicode handled properly? Unicode_alphabetic_tokenizer function in Unicode pkg  
Also see ?Encoding and ?iconv.  biblatex to bibtex function should use `iconv`
* where do 
* http://opencitations.net/
* handle crossrefs for new BibLaTeX "in" fields
* write "-.BibEntry" function
* see the `scholar` R package.  Imports bibtex data using scholar id's
* see R package CITAN for "scientometrics"
* see knitcitations: install_github("knitcitations", "cboettig")
* handle Zotero using techreport for arXiv files
* add merge function as wrapper for "+.BibEntry"
* add search function as wrapper for "[.BibEntry"
* is [`stringi`](http://docs.rexamine.com/R-man/stringi/stringi-encoding.html) worth using over `Unicode` package?
* Distinguish what can be imported and needs to be re-implemented from `bibtex` and `utils`

DONE     
==================================================================================================================

* read from Zotero: http://www.zotero.org/support/dev/server_api/v2/read_requests
* open browser to Google Scholar for bibtex entry
* Biblatex entry types and fields supported
* Unicode can be supported with little effort. encoding option in WriteBib; Unicode pkg; Encoding function

==================================================================================================================