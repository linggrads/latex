# LaTeX for Linguists

This is a repository for linguistics-related LaTeX resources.

[Examples of essential functions](/ExampleFiles/exampleFiles.md)

# Learning LaTeX

* [Wikibook for latex for linguists](https://en.wikibooks.org/wiki/LaTeX/Linguistics)

# Very useful tools

* [Table generator](https://www.tablesgenerator.com/) - Generates latex code for excel-style tables.
* [comphrehensive latex symbols list](http://tug.ctan.org/info/symbols/comprehensive/symbols-a4.pdf)
* [detexify](https://detexify.kirelabs.org/classify.html) - You draw the symbol and it tells you which package you can get it in, and its command.
* [Kevin's OT table generator](https://meluhha.com/tabular/)


# Packages


## Glossing packages

There are three main glossing packages.  In order of difficulty, they are: ```gb4e``` ([documentation](https://ctan.math.illinois.edu/macros/latex/contrib/gb4e/gb4e-doc.pdf)), ```linguex``` ([documentation](https://texdoc.org/serve/linguex-doc.pdf/0)), and ```expex``` ([documentation](https://ctan.mirrors.hoobly.com/macros/generic/expex/expex-doc.pdf)).  **NOTE:** Do not declare more than one glossing packages in your preamble!


Let's examine how to write the following simple examples:

![](/ExampleFiles/Images/glosses.png)




### gb4e

[PDF](/ExampleFiles/SinglePackageExamples/gb4e.pdf), [TeX](/ExampleFiles/SinglePackageExamples/gb4e.tex)

<details>
<summary>
Code
</summary>

```

\documentclass{article}

\usepackage{gb4e}

\begin{document}


Consider the following sentence

\begin{exe}
\ex\label{ex:first} This is a sentence
\ex
    \begin{xlist}
    \ex[*]{Sentence a}
    \ex[\#]{Sentence b}
    \ex[]{Sentence c}
    \end{xlist}

\end{exe}

Shiny glosses!  I can refer to example (\ref{ex:first}) like this. %Have to put \ref{} in parentheses

Example (\ref{ex:Turkish}) is a nice sentence in Turkish.


\begin{exe}
    \ex\label{ex:Turkish}
        \gll 
       Öğretmen-ler öğrenci-ler-e iki kitap ok-ut-tu.\\
       teacher-{\sc pl.nom} student-{\sc pl-acc} two book read-{\sc caus-pst}\\ %Do not forget line breaks!
        `The teacher made the students read two books..'
\end{exe}

\end{document}

```
</details>
<br>

Other examples
* []


### linguex

[PDF](/ExampleFiles/SinglePackageExamples/linguex.pdf), [TeX](/ExampleFiles/SinglePackageExamples/linguex.tex)

<details>
<summary> 
Code
</summary>

```
\documentclass{article}
\usepackage[utf8]{inputenc}

\usepackage{linguex}

\begin{document}

Consider the following sentence:

\ex.This is a sentence \label{ex:first}\\

\ex.\a.*Sentence a %Do not put space b/w judgment symobl and the first word! 
    \b.\#Sentence b
    \b. Sentence c
    
Shiny glosses!  I can refer to example \ref{ex:first} like this. %Do not put parentheses around \ref{}

Example \ref{ex:Turkish} is a nice sentence in Turkish.

\exg.Öğretmen-ler öğrenci-ler-e iki kitap ok-ut-tu. \label{ex:Turkish}\\
       teacher-{\sc pl.nom} student-{\sc pl-acc} two book read-{\sc caus-pst}\\ %Do not forget line breaks!
        `The teacher made the students read two books..'



\end{document}

```

</details>
<br>

Other examples:
* []

### expex

[PDF](/ExampleFiles/SinglePackageExamples/expexExamples.pdf), [TeX](/ExampleFiles/SinglePackageExamples/expexExamples.tex)
<details><summary> 
Code
</summary>

```
\documentclass{article}

\usepackage{parskip} %For paragraph formatting
\usepackage{expex} % Linguistic examples & glosses

\lingset{everygla={},aboveglftskip=-0.5ex,aboveexskip=1ex,belowexskip=-1ex,Everyex={\parskip=0pt}} % Expex gloss configuration to work with parskip (removes unnecessary whitespace).  Also unitalicizes top line of gloss


\begin{document}


Consider the following sentence:

% This uses expex formatting - see http://mirrors.ibiblio.org/CTAN/macros/generic/expex/expex-doc.pdf
\ex This is a sentence \label{ex:first}
\xe
\pex~ % Use the tilde for consecutive examples to get better spacing
\a \ljudge{*} Sentence a
\a \ljudge{\#} Sentence b
\a Sentence c
\xe

Shiny glosses! I can refer to example (\ref{ex:first}) like this. %Requires you to have put a \label there.


Example (\ref{ex:Turkish}) is a nice sentence in Turkish.

\ex \label{ex:Turkish}
\begingl
\gla Öğretmen-ler öğrenci-ler-e iki kitap ok-ut-tu. //
\glb teacher-{\sc pl.nom} student-{\sc pl-acc} two book read-{\sc caus-pst}//
\glft `The teacher made the students read two books.'//
\endgl
\xe

\end{document}
```

</details>

Other examples:
* Handout 10 function application [PDF](/ExampleFiles/Handout%2010-Function%20Application-FilledOut.tex), [TeX](/ExampleFiles/Handout%2010-Function%20Application-FilledOut.tex)






# Sample Files

## Sample abstracts

* Kirby, Ian. 2022. Pre-exhaustification Creates Multifunctionality: Evidence from Tuvan *-daa*. (WCCFL). [[PDF](/ExampleFiles/Kirby%20WCCFL%202022%20Abstract.pdf),  [TeX](/ExampleFiles/Kirby%20WCCFL%202022%20Abstract.tex)]
* Ross, Hayley. 2022. Quantifiying weak and strong crossover for *wh*-crossover and proper names. (SuB). [[PDF](/ExampleFiles/SuB_Abstract_Crossover.pdf), [TeX](/ExampleFiles/SuB_Abstract_Crossover.tex)]

## Sample handouts

## Sample posters

* Ross, Hayley. 2022. Impliciations of the Danish definiteness alternation for concord in Nanosyntax. (SinFonIJA). [[PDF](/ExampleFiles/SinFonIJAPosterNanosyntax.pdf)], [TeX](/ExampleFiles/SinfonIJAPosterNanosyntax.tex)]

## Sample slides

* Ross, Hayley. 2021. Implications of the Danish definiteness alternation for concord in Nanosyntax. (SinFonIJA) [[PDF](/ExampleFiles/SinFonIJALightningTalkImplicationsDanishNanosyntax.pdf), [TeX](/ExampleFiles/SinFonIJALightningTalkImplicationsDanishNanosyntax.tex)]