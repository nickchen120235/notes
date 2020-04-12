# LaTeX Notes
## Table of Contents
- <a href=https://github.com/nickchen120235/notes/blob/master/miscellaneous/LaTeX.md#set-paper-margin>Set Paper Margin</a>
- <a href=https://github.com/nickchen120235/notes/blob/master/miscellaneous/LaTeX.md#integral-subtraction>Integral Subtraction</a>
- <a href=https://github.com/nickchen120235/notes/blob/master/miscellaneous/LaTeX.md#bigger-fraction>Bigger fraction</a>
- <a href=https://github.com/nickchen120235/notes/blob/master/miscellaneous/LaTeX.md#bigger-cases>Bigger cases</a>
- <a href=https://github.com/nickchen120235/notes/blob/master/miscellaneous/LaTeX.md#fourier-transform-symbols>Fourier Transform Symbols</a>
- <a href=https://github.com/nickchen120235/notes/blob/master/miscellaneous/LaTeX.md#words-abovebelow-arrow>Words above/below Arrow</a>
- <a href=https://github.com/nickchen120235/notes/blob/master/miscellaneous/LaTeX.md#limit>Limit</a>
- <a href=https://github.com/nickchen120235/notes/blob/master/miscellaneous/LaTeX.md#modulo-with->modulo with ()</a>
- <a href=https://github.com/nickchen120235/notes/blob/master/miscellaneous/LaTeX.md#bolditatic>**bold**/*itatic*</a>
- <a href=https://github.com/nickchen120235/notes/blob/master/miscellaneous/LaTeX.md#number-sets>Number Sets</a>
- <a href=https://github.com/nickchen120235/notes/blob/master/miscellaneous/LaTeX.md#multiline-math-environment>Multiline Math Environment</a>
-<a href=https://github.com/nickchen120235/notes/blob/master/miscellaneous/LaTeX.md#macro>Macro</a>
---

#### Set Paper Margin
```latex
\usepackage[a4paper, margin=.5in]{geometry}
```
#### Integral Subtraction
```latex
\def\at{
    \left.
    \vphantom{\int}
    \right|
}
```
#### Bigger fraction
```latex
\dfrac
```
#### Bigger cases
```latex
\usepackage{mathtools}
\begin{dcases}
    ...
\end{dcases}
```
#### Fourier Transform Symbols
```latex
\usepackage{mathrsfs}
\mathscr{F} %Fourier Transform
\mathfrak{Im} %Imaginary Part (also works for "Re")
```
#### Words above/below Arrow
```latex
\usepackage{mathtools}
\xrightarrow[below]{above}
\xRightarrow[below]{above}
```
#### Limit
```latex
\lim_{A\to B}
```
#### modulo with ()
```latex
\pmod{}
```
#### **bold**/*itatic*
bold
```latex
\textbf{}
```
italic
```latex
\textit{}
```
#### Number Sets
```latex
\usepackage{amssymb}
\mathbb{P} % prime numbers
\mathbb{W} % whole numbers
\mathbb{N} % natural numbers
\mathbb{Z} % integers
\mathbb{I} % irrational numbers
\mathbb{Q} % rational numbers
\mathbb{R} % real numbers
\mathbb{C} % complex numbers
```
#### Multiline Math Environment
```latex
\usepackage{mathtools} %amsmath
\begin{align*}
    ...
\end{align*}
```
#### Macro
```latex
\def\commandname[#1]{Print``#1''} %\def <command> <parameter-text>{<replacement-text>}
```