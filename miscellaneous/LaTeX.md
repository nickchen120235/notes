# LaTeX Notes

- Set paper margin
```latex
\usepackage[a4paper, margin=.5in]{geometry}
```
- Integral Subtraction
```latex
\def\at{
    \left.
    \vphantom{\int}
    \right|
}
```
- Bigger fraction
```latex
\dfrac
```
- Bigger cases
```latex
\usepackage{mathtools}
\begin{dcases}
    ...
\end{dcases}
```