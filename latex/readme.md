## Document Processing with LaTeX
### An Introduction

**Lallu Anthoor**

_Assistant Professor, CSE, MIT Kannur_

_`lallu[at]mitkannur[dot]ac[dot]in`_

<br>

`https://bit.ly/latexvjec`

<br>
October 2015

---

### Agenda

- Introduction
- Installation and Configuration
- Syntax
- Organizing Content
- Lists
- Adding Figures and Tables
- Bibliography and Citations
- Formulae and Equations
- Preparing Presentations

---

### Introduction

------

#### What is LaTeX
- pronounced "La Tech"
- markup language
- high typeset quality
- scientific publishing
- easy to include mathematical formulae
- platform independent
- free and open sourced

------

#### History

<div>
<img src="knuth.jpg" height="350px">
<img src="lamport.jpg" height="350px">
</div>
<div>

- TeX developed by Donald E Knuth
- Leslie B Lamport extended TeX to LaTeX
- LaTeX is a collection of macros

</div>
<div>

_Images from Wikipedia_

<div>

Note:
- Knuth: Turing prize (1974), von Neuman prize (1995), KMP algorithm
- Lamport: Turing prize (2013), Dijkstra prize (2000, 2005, 2014)

---

### Installation and Configuration

------

#### On Debian and derivatives
- includes Debian, ubuntu, kubuntu, Linux Mint, etc.
- install from PPA

```bash
# for basic installation
sudo apt-get update && sudo apt-get install -y texlive

# for full installation
sudo apt-get update && sudo apt-get install -y texlive-full
```

------

#### LaTeX editors
```bash
# on GNOME/Unity use texmaker or texstudio
sudo apt-get install -y texmaker
# or
sudo apt-get install -y texstudio

# on KDE based systems use kile
sudo apt-get install -y kile
```

Alternatively, use Visual Studio Code along with the LaTeX Workshop plugin

Get VS Code from https://code.visualstudio.com

Get the LaTeX Workshop plugin from https://marketplace.visualstudio.com/items?itemName=James-Yu.latex-workshop

------

#### Online Editors
- if you do not have the bandwidth to download the whole `texlive` package or
- if you do not have enough space on device or
- if you are not allowed to install programs on the device
- use online LaTeX editors like [Overleaf](https://www.overleaf.com/)

---

### Syntax

------

#### General syntax of LaTeX

```latex
% anything after % is a comment

% general structure of a LaTeX markdown command is as follows
\command[options]{argument}


% block structures like document, image, table, etc. are enclosed within a begin
% and an end command tag
\begin{something}
% ...
\end{something}
```

------

#### Basic structure of a document

```latex
% there will be a document class declaration which will tell LaTeX what is the
% general template we want to follow, along with some additional properties of
% the document like paper size and font size
\documentclass[a4paper,12pt]{article}

% package imports; packages are add-on modules that provide extra functionality
% to our LaTeX document
\usepackage[utf8]{inputenc}

% additional metadata about the document like title, author, etc.
\title{Document Preparation with LaTeX: General Syntax Guide on How To Use LaTeX}
\author{Lallu Anthoor}

% the content of the document will be enclosed within a begin..end block
\begin{document}
% ...
\end{document}
```

------

#### File Formats
- LaTeX files are stored with an extension `.tex`
- the contents should be in plain text format
- cannot use word processing or rich text editors for working with LaTeX

------

#### Compiling a TeX Project

```bash
# if you want the output as a PDF document, use pdflatex to compile your project
pdflatex filename.tex  # it will produce filename.pdf

# if you want the output to be DVI, use latex to compile your project
latex filename.tex     # it will produce filename.dvi
```

---

### Organizing Content

------

#### Chapters and Sections - I

```latex
\documentclass{article}
\begin{document}

% top-most level of content hierarchy is called part. a part can have several 
% chapters. a chapter can have multiple sections, a section can have multiple
% sub-sections, and a sub-section can have multiple sub-sub-sections.
\part{Part Name}
\chapter{Chapter Title}
This is a paragraph in the chapter.
\section{Section Title}
This is a paragraph in the section.
\subsection{Sub-section Title}
This is a paragraph in the sub-section
\subsubsection{Sub-sub-section Title}
This is a paragraph in the sub-sub-section.

% a chapter continues till the beginning of the next chapter, a section continues
% till the beginning of the next section and so on. there is no explicit ending
% tags for content divisions
\subsubsection{Second Sub-sub-section Title}
This is a paragraph in the second sub-sub-section.

\end{document}
```

------

#### Chapters and Sections - II

```latex
% if the name of your chapter/section/etc. is too long, you can define a shorter
% version of it, which will be used in table of contents, footers, etc. like this
\chapter[Short Title]{A Extremely Long Title for a Chapter That Cannot Go in Table of Contents}

% by default, LaTeX numbers all content divisions. chapters are numbered 1, 2, 3, ...
% sections are numbered 1.1, 1.2, ..., 2.1, 2.2, ... and so on. you can turn off
% the numbering for any particular division using *
\chapter*{Chapter Name}
```

------

#### Table of Contents - I

```latex
% LaTeX will automatically generate a table of contents for you based on the
% chapters, sections, sub-sections, and sub-sub-sections.
\documentclass{article}
\begin{document}

% the magic line
\tableofcontents

\section{Section Name}
% ...

\subsection{Sub-section Name}
% ...

\end{document}
```

------

#### Table of Contents - II

```latex
% if you want to limit the depth of the table of contents, i.e. limit upto what
% level the table of contents should list, you can use the following command
\setcounter{tocdepth}{1}

% if -2 is used, nothing is added to ToC
% if -1 is used, only parts are added to ToC
% if 0 is used, parts and chapters are added to ToC
% if 1 is used, parts, chapters and sections are added to ToC
% 2 for upto sub-section
% 3 for upto sub-sub-section

% by default, the table of contents is added with title "Contents". you can
% change it using
\renewcommand{\contentsname}{New Name}
```

------

#### Organizing Large Projects - I

```latex
% when you have large projects like a thesis or a lab record, it is difficult
% to maintain everything in a single .tex file. you can divide the project into
% multiple .tex files based on chapters/experiments/etc. there will be one root
% file with the document definition and the preamble, and all other sub-files
% will have only chapter content. a sample directory structure is given below.
.
├── chapters
│   ├── ch1
│   │   ├── img
│   │   │   ├── img001.svg
│   │   │   └── img002.svg
│   │   └── chapter1.tex
│   └── ch2
│       ├── img
│       │   └── img001.svg
│       └── chapter2.tex
└── book.tex
```

------

#### Organizing Large Projects - II

```latex
% --- book.tex ---
\documentclass{book}

\uspackage[utf8]{inputenc}

\begin{document}

\input{chapters/ch1/chapter1.tex}
\input{chapters/ch2/chapter2.tex}

\end{document}


% --- chapter1.tex ---
\chapter{Chapter One Title}

% chapter one content
```

---

### Lists

------

#### Bulleted Lists

```latex
% use begin..end itemize to add a bulleted list
\begin{itemize}
  \item first bullet point
  \item second bullet point
  % ...
\end{itemize}

% you can nest the lists
\begin{itemize}
  \item item at level 1
  \begin{itemize}
    \item item at level 2
    % ...
  \end{itemize}
  % ...
\end{itemize}
```

------

#### Numbered Lists

```latex
% use begin..end enumerate for numbered lists
\begin{enumerate}
  \item first point
  \item second point
  % ...
\end{enumerate}

% you can nest the lists
\begin{enumerate}
  \item item at level 1
  \begin{enumerate}
    \item item at level 2
    % ...
  \end{enumerate}
  % ...
\end{enumerate}
```

------

#### Hybrid Lists

```latex
% you can nest numbered list inside bulleted list and vice-versa for any number
% of levels. the numbering and bulleting will be adjusted automatically.
\begin{itemize}
  \item bulleted item 1
  \begin{enumerate}
    \item numbered item 11
    % ...
  \end{enumerate}
  % ...
\end{itemize}

\begin{enumerate}
  \item numbered item 1
  \begin{itemize}
    \item bulleted item 11
    % ...
  \end{itemize}
  % ...
\end{enumerate}
```

---

### Adding Figures and Tables

------

#### Adding an Image - I

```latex
\documentclass{article}

% we use the package graphicx to include images into your document
% import it using
\usepackage{graphicx}

% tell graphics where your images are located (preferably, a sub-directory)
\graphicspath{ {./images/} }

\begin{document}

\section{Section Title}

% add the image
\includegraphics{imagefilename}

\end{document}
```

------

#### Adding an Image - II

```latex
% you can resize the image using the following constructs

% using relative scaling
\includegraphics[scale=0.6]{imagefilename}

% scale it to match the width of page
\includegraphics[width=\textwidth]{imagefilename}

% using exact values
\includegraphics[width=5cm]{imagefilename}

% if you want to add numbering/caption to the image, you can wrap it in figure tag
\begin{figure}
  \includegraphics{imagefilename}
  
  % this is added to the bottom of image with the image number
  \caption{This is a caption for image}

  % this is used to refer to this image later in the text
  \label{fig-001}
\end{figure}
```

------

#### Adding a Table - I

```latex
% tables are added using the tabular command
\documentclass{article}

\begin{document}

\section{Section Title}

% add the table, letters l, c, r are used to define alignment of text within
% the columns. l for left, r for right and c for center alignment. & is used
% to mark the columns and \\ is used to mark rows. | is added between columns
% to denote vertical borders and \hline is added to denote horizontal borders
\begin{tabular}{|c|c|c|}
\hline
cell-11 & cell-12 & cell-13 \\
\hline
cell-21 & cell-22 & cell-23
\hline
\end{tabular}

\end{document}
```

------

#### Adding a Table - II

```latex
% adjust column width using array package
\documentclass{article}

%include the array package
\usepackage{array}

\begin{document}

\section{Section Title}

% define the size of column within { }
\begin{tabular}{|l{5cm}|c{10cm}|r{3cm}|}
\hline
cell-11 & cell-12 & cell-13 \\
\hline
cell-21 & cell-22 & cell-23
\hline
\end{tabular}

\end{document}
```

------

#### Adding a Table - III

```latex
% if you want to add numbers, captions and references to table
% use the tabular command
\begin{tabular}
  \begin{table}{|l|c|r|}
  \end{table}

  % caption is added along with the table and the number
  \caption{Table Caption}

  % label is used to refer to the table later in text
  \label{table-001}
\end{tabular}
```

------

#### Referencing Tables and Figures

```latex
% you will have to refer to the image number multiple times in the text. if you
% hard code the number, you will have to edit it several times if there is a new
% image added in between or an image removed from between. LaTeX avoids this
% issue using the labels. the method is same for both figures and tables.
\begin{figure}
  \includegraphics{imagefilename}
  \caption{My image caption}
  
  % define a label using the label command
  \label{fig-important-image}
\end{figure}

% ...

\section{Another Section Elsewhere}

% later in text you can refer to the image using ref command
As shown in Fig. \ref{fig-important-image}, the fact is proved.

% LaTeX compiler will automatically update the figure numbers and references
% everywhere without any user intervention.
```

---

### Bibliography and Citations

------

#### Bibliography File
- LaTeX provides an easy to use and reusable mechanism of storing bibliography
- implemented using `bibtex` package
- bibliography is stored in a separate file with `.bib` extension
- we can refer to the articles/books/journals papers/etc. using `cite` command
- popular websites like Google Scholar, ResearchGate, etc. provides citations in `bibtex` compatible format

------

#### Bibliography File Format

- several types of bibliography entries are supported
- first item in the entry (`texbook`, `knuth:1984` in the example) is used as the label
- other information like author, title, publisher, volume, etc. can be maintained

```bibtex
@book{texbook,
  author = {Donald E. Knuth},
  year = {1986},
  title = {The \TeX{} Book},
  publisher = {Addison-Wesley Professional}
}

@article{knuth:1984,
  title={Literate Programming},
  author={Donald E. Knuth},
  journal={The Computer Journal},
  volume={27},
  number={2},
  pages={97--111},
  year={1984},
  publisher={Oxford University Press}
}
```

------

#### Including References

```latex
\documentclass{article}

\begin{document}

\section{Section Title}
This is a theory stated in another paper \cite{knuth:1984}.
It is also described in another book \cite{texbook}.

% define the styling for the references section. here a plain style is used.
\bibliographystyle{plain}

% define the source of the bibliography. here the bibliography will be picked
% from a file called refs.bib
\bibliography{refs}

\end{document}

% numbering of the references, updating the citation with the numbers, etc. are
% handled by bibtex. users don't have to bother with adding or updating numbers.
```

------

#### Compiling with BiBTeX

```bash
# once you add bibliography, it is not sufficient to run pdflatex or latex
# to compile. you need to run bibtex command to process the bib file and
# generate appropriate references. the whole compilation sequence would be

# this will generate an aux file with unprocessed reference entries
pdflatex filename.tex

# this will use the aux file and the bib file to compute the references
bibtex filename.aux

# pdflatex is ran twice afterwards to ensure all references are updated
# it is mandatory to run it twice
pdflatex filename.tex
pdflatex filename.tex
```

---

### Formulae and Equations

------

#### Mathematical Formulae - I

```latex
% inline mode using \(...\) or $...$ to add formulae in line with the text.
% alternatively, you can use begin..end with math
% it is recommended to use \(...\) for inline math
Pythagoras said that \(x^2 + y^2 = z^2\) in a right angled triangle where $x^2$
is the square of the base and \begin{math}y^2\end{math} is the square of the 
height and $z^2$ is the square of the hypoteneus.

% for super-script (exponent), LaTeX uses ^ as shown above. if there are more
% than one character in the exponent, use { } to group them
\( x^{a+b} = x^a \times x^b \)

% for sub-script, LaTeX uses _. if there are more than one character in the
% subscript, use { } to group them
\( 2 \times H_2 + O_2 = 2 \times H_2O \)

1- Pentanol is represented as \( C_5 H_{11} OH \).
```

------

#### Mathematical Formulae - II

```latex
% display mode for adding the formulae in a separate line
% use begin..end with equation or displaymath, or \[...\]
\begin{equation}
  x^2 + y^2 = z^2
\end{equation}

% for single line equations without numbering
\[E=m \times c^2\]

% by default begin..end with equation will add numbering for the equation. if
% you don't want numbering, you can use begin..end with align*
\begin{align*}
A & = B+C+D \\
  & = B+E \\
  & = F
\end{align*}
% this will align the equation lines w.r.t =
```

------

#### Referencing Equations

```latex
% LaTeX consistently uses label and ref for referencing
\begin{equation}
  \label{very-important-equation}
  % ...
\end{equation}

% ...
\section{A Later Section}
As shown in the very important equation (\ref{very-important-equation}), ...
```

---

### Preparing Presentations

------

#### Introduction to Beamer
- `beamer` is a `documentclass` provided by LaTeX to handle presentations
- slides are called `frame`s
- uses standard LaTeX commands like `title`, `author`, `institue`, etc. to create title slide
- it supports content division into sections, sub-sections, etc. and `\tableofcontents`
- standard LaTeX syntax apply for lists, images, tables, equations, etc.

------

#### Defining Slides

```latex
\documentclass{beamer}

\begin{document}

  % each slide is a frame in beamer
  \begin{frame}
    \frametitle{Title of Frame}
    % ...
  \end{frame}

  % or alternatively
  \begin{frame}{Title of Frame}
    % ...
  \end{frame}

\end{document}
```

------

#### Adding Effects
- a simple reveal effect is supported by the lists

```latex
\begin{frame}
  \begin{itemize}
    \item<1-> item visible from first slide onwards
    \item<-2> item visible till second slide
    \item<3> item visible only on third slide
    \item<4-> item visible from fourth slide onwards
    % ...
  \end{itemize}
\end{frame}

% each item in the above list will create a new page in the PDF output, giving
% an impression that there is animation in the presentation
```

---

### References

------

#### For this presentation
- Slides prepared using [reveal.js](https://github.com/hakimel/reveal.js)
- Edited in [Visual Studio Code](https://github.com/microsoft/vscode)
- Index page prepared using [Bootstrap](https://github.com/twbs/bootstrap)
- Slides are hosted using [GitHub Pages](https://docs.github.com/en/pages/getting-started-with-github-pages/about-github-pages)
- Source code for this slide available in [GitHub](https://github.com/anthoor/slides/tree/main/latex)

------

#### Further reading
- [Donald Knuth](https://en.wikipedia.org/wiki/Donald_Knuth)
- [Leslie Lamport](https://en.wikipedia.org/wiki/Leslie_Lamport)
- [Markup Language](https://en.wikipedia.org/wiki/Markup_language)
- [Free and Open Source Software](https://en.wikipedia.org/wiki/Free_and_open-source_software)
- [Overleaf Documentation](https://www.overleaf.com/learn)
- [StackExchange](https://tex.stackexchange.com/)
- [CTAN](https://www.ctan.org/)
