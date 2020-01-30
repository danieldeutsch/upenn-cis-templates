This project has the Thesis template for UPenn CIS students, that I got by modifying the template [here](https://guides.library.upenn.edu/dissertation_manual/formatting).
As far as I can tell by inspecting earlier theses before me, this template is correct. 

I have organized chapters into folders so that all `.tex` files relevant to a certain chapter remain in one place. 

I also have a makefile that compiles chapters separately (with bibliography), so that you can quickly compile the chapter you are working on, without compiling the entire thesis. 


### Compile Entire Thesis

Ensure that the correct biblio setting is active, 

```latex
%% TO TURN ON BIB FOR CHAPTER (when compiling chapters separately)
% \def\biblio{\bibliographystyle{abbrvnat}\bibliography{thesis}}
%% TO TURN OFF BIB FOR EACH CHAPTER, (for compiling the whole thesis)
\def\biblio{}
```

And then run 

```
make clean; make
```

### Compile Chapter Separately
To compile a single chapter for proofreading. 

Ensure that the correct biblio setting is active, 

```latex
%% TO TURN ON BIB FOR CHAPTER (when compiling chapters separately)
\def\biblio{\bibliographystyle{abbrvnat}\bibliography{thesis}}
%% TO TURN OFF BIB FOR EACH CHAPTER, (for compiling the whole thesis)
% \def\biblio{}
```

And then run 

```
make clean; make chapter1.pdf
```

### Remove Line Numbering

Line numbers are useful for getting comments from people. Remove them for the final version by commenting out the following

```
% FOR ADDING LINE NO. I have checked, this does not mess with margins (i.e. the # appears outside the margins, so no new orphans/widows are introduced)
\usepackage{lineno}
\linenumbers

```
