# LaTeX Notes

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