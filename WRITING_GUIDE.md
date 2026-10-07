# Writing Cheat Sheet for this Thesis Project

The most important commands for writing in the files under `chapters/`, `pages/` and `appendix/`.

## 1. Chapters and sections

```tex
\chapter{Introduction}
\section{Motivation}
\subsection{Research question}
```

- `\chapter{...}` creates a chapter.
- `\section{...}` creates a section.
- `\subsection{...}` creates a subsection.

Special pages without a chapter number usually use:

```tex
\chapter*{Abstract}
\phantomsection\addcontentsline{toc}{chapter}{\protect Abstract}
```

## 2. Placeholder text

```tex
\bt
```

- `\bt` is defined in the preamble as a shortcut for filler text.
- Use it only as a placeholder and delete it later.

## 3. Math shortcuts

```tex
$\N, \Z, \Q, \R, \C$
```

- `\N` natural numbers
- `\Z` integers
- `\Q` rational numbers
- `\R` real numbers
- `\C` complex numbers

More shortcuts:

```tex
$\D x, \E^{x}, \I, \1$
```

- `\D` upright differential `d`
- `\E` Euler's number `e`
- `\I` imaginary unit `i`
- `\1` one / indicator symbol

## 4. Vectors and operators

```tex
$\bs{x}$
$\diag(-,+,+,+)$
$\arsinh(x)$
```

- `\bs{...}` makes math symbols bold, e.g. for vectors.
- `\diag(...)` typesets the `diag` operator.
- `\arsinh(...)` typesets the `arsinh` operator.

## 5. Units and numbers with `siunitx`

```tex
\SI{1.23}{\meter}
\SI{299792458}{\meter\per\second}
```

- `\SI{number}{unit}` is the standard form for physical quantities.
- Units such as `\meter`, `\second`, `\kilogram`, `\kelvin` can be used directly.

Additional units defined in this project:

```tex
\SI{1}{\au}
\SI{4.2}{\ly}
\SI{3}{\parsec}
\SI{10}{\yr}
```

- `\au` astronomical unit
- `\ly` light year
- `\parsec` parsec
- `\yr` year

## 6. Equations

Inline:

```tex
The energy is given by $E = mc^2$.
```

Displayed:

```tex
\begin{align*}
    E &= mc^2 \\
    p &= mv
\end{align*}
```

- `align*` is handy for several aligned equations.
- The `*` suppresses equation numbers.

## 7. Figures

```tex
\begin{figure}[!h]
    \centering
    \includegraphics[width=0.7\linewidth]{figures/example.png}
    \caption{Example figure.}
    \label{fig:example}
\end{figure}
```

- Images go into the `figures/` folder.
- `\label{...}` lets you reference the figure later.

## 8. Cross-references

```tex
As shown in Figure~\ref{fig:example}, ...
```

- `\label{...}` sets a marker.
- `\ref{...}` refers to it.

Useful naming patterns:

- `fig:...` for figures
- `sec:...` for sections
- `eq:...` for equations
- `tab:...` for tables

## 9. Citations and bibliography

The bibliography is handled by `biblatex`. Typical command:

```tex
\cite{key}
```

To cite a source you need:

- an entry in `sources/bachelorarbeit.bib`
- the matching key in `\cite{...}`

## 10. Project macros

These are mainly used on the title pages:

```tex
\getAuthor
\getTitleEN
\getTitleDE
\getSupervisorOne
\getSupervisorTwo
```

- The values are set in `preamble_thesis.tex`.
- Normal chapter writing rarely needs them.

## 11. Minimal chapter example

```tex
\chapter{An Example Chapter}

\section{Introduction}
Your text goes here. Number sets can be written as $\R$ or $\C$.

\section{Model}
Consider the vector $\bs{x}$ and the metric $\diag(-,+,+,+)$.

\begin{align*}
    E &= mc^2
\end{align*}

A measured value is \SI{2.5}{\meter}.
```

## 12. Everyday writing tips

- Use `\section` and `\subsection` for structure.
- Use `\bt` only as a temporary placeholder.
- Use `\SI{...}{...}` consistently for units.
- Add `\label` and `\ref` while writing so references stay stable.
- Use the shortcuts `\R`, `\C`, `\bs`, `\diag` for consistent notation.
