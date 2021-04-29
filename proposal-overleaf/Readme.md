This directory contains a minimal version of the proposal template that can be used on Overleaf instead of the command line.

Compiling "main.tex" will generate the entire proposal document.
Compiling any one of the files in the "sections" directory will compile just that section and generate the references.
New sections should copy the format of "01_introduction.tex":
```tex
\documentclass[../main.tex]{subfiles}
\begin{document}

% Section text goes here

\dobib
\end{document}
```

I also changed the bibliography format to use the ACL style.
