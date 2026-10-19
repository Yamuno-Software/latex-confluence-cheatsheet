# LaTeX cheat sheet for Confluence

The LaTeX commands people actually use when writing math in Confluence, with the source next to the rendered result.

It targets [KaTeX](https://katex.org/docs/supported.html), which is what [LaTeX Math for Confluence](https://yamuno.com/products/latex-math-for-confluence) uses to render equations. GitHub renders the examples below with its own math engine, so a few look slightly different here than on a Confluence page. For a step-by-step guide to adding equations to a page, see [How to add math equations to Confluence](https://yamuno.com/blogs/how-to-add-math-equations-to-confluence).

## Contents

- [Before you start](#before-you-start)
- [Fractions and roots](#fractions-and-roots)
- [Subscripts and superscripts](#subscripts-and-superscripts)
- [Operators](#operators)
- [Sums, integrals and limits](#sums-integrals-and-limits)
- [Greek letters](#greek-letters)
- [Relations](#relations)
- [Arrows and logic](#arrows-and-logic)
- [Sets](#sets)
- [Brackets that grow](#brackets-that-grow)
- [Accents](#accents)
- [Text inside math](#text-inside-math)
- [Matrices](#matrices)
- [Aligned equations](#aligned-equations)
- [Cases](#cases)
- [Degrees, percent and other escapes](#degrees-percent-and-other-escapes)
- [Chemistry](#chemistry)
- [Colour](#colour)
- [What KaTeX does not do](#what-katex-does-not-do)

## Before you start

In Confluence, type `/latex` and pick the inline or block macro.

- **Inline** sits inside a sentence. Keep it to one line: no matrices, `aligned` or `cases`.
- **Block** gets its own line and handles everything on this page.

You type the LaTeX without `$` signs. The `$...$` you see in this README is only there so GitHub renders the examples.

## Fractions and roots

| Source | Result |
| --- | --- |
| `\frac{a}{b}` | $\frac{a}{b}$ |
| `\dfrac{a}{b}` | $\dfrac{a}{b}$ |
| `\tfrac{1}{2}` | $\tfrac{1}{2}$ |
| `a/b` | $a/b$ |
| `\sqrt{x}` | $\sqrt{x}$ |
| `\sqrt[3]{x}` | $\sqrt[3]{x}$ |
| `\binom{n}{k}` | $\binom{n}{k}$ |

`\dfrac` keeps a fraction full size inside a line of text. `\tfrac` makes it small.

More: [fractions](https://yamuno.com/latex/symbols/fraction-slash), [binomial coefficient](https://yamuno.com/latex/symbols/choose)

## Subscripts and superscripts

| Source | Result |
| --- | --- |
| `x^2` | $x^2$ |
| `x^{10}` | $x^{10}$ |
| `x_i` | $x_i$ |
| `x_{i,j}` | $x_{i,j}$ |
| `x_i^2` | $x_i^2$ |
| `e^{-x^2}` | $e^{-x^2}$ |
| `f'(x)` | $f'(x)$ |

Use braces when the sub or superscript is more than one character: `x^10` gives $x^10$, not $x^{10}$.

More: [prime](https://yamuno.com/latex/symbols/prime)

## Operators

| Source | Result |
| --- | --- |
| `\pm` | $\pm$ |
| `\mp` | $\mp$ |
| `\times` | $\times$ |
| `\cdot` | $\cdot$ |
| `\div` | $\div$ |
| `\nabla` | $\nabla$ |
| `\partial` | $\partial$ |
| `\infty` | $\infty$ |
| `\sin x`, `\cos x`, `\log x`, `\ln x` | $\sin x, \cos x, \log x, \ln x$ |
| `\operatorname{argmax}_x` | $\operatorname{argmax}_x$ |

Write `\sin x`, not `sin x`. Without the backslash, KaTeX sets the letters in italics as if they were variables.

More: [plus-minus](https://yamuno.com/latex/symbols/plus-minus), [times](https://yamuno.com/latex/symbols/times), [dot](https://yamuno.com/latex/symbols/multiplication-dot), [division](https://yamuno.com/latex/symbols/division), [nabla](https://yamuno.com/latex/symbols/nabla), [partial derivative](https://yamuno.com/latex/symbols/partial-derivative), [infinity](https://yamuno.com/latex/symbols/infinity)

## Sums, integrals and limits

| Source | Result |
| --- | --- |
| `\sum_{i=1}^{n} i` | $\sum_{i=1}^{n} i$ |
| `\prod_{i=1}^{n} x_i` | $\prod_{i=1}^{n} x_i$ |
| `\int_0^1 x\,dx` | $\int_0^1 x\\,dx$ |
| `\iint_D f\,dA` | $\iint_D f\\,dA$ |
| `\oint_C F \cdot dr` | $\oint_C F \cdot dr$ |
| `\lim_{x \to 0} \frac{\sin x}{x}` | $\lim_{x \to 0} \frac{\sin x}{x}$ |
| `\frac{d}{dx} f(x)` | $\frac{d}{dx} f(x)$ |
| `\frac{\partial f}{\partial x}` | $\frac{\partial f}{\partial x}$ |

In a block macro the limits sit above and below the symbol. Inline, they move to the side. `\,` adds a thin space before `dx`.

```math
\int_{-\infty}^{\infty} e^{-x^2}\,dx = \sqrt{\pi}
```

More: [sum](https://yamuno.com/latex/symbols/sum), [product](https://yamuno.com/latex/symbols/product), [integral](https://yamuno.com/latex/symbols/integral), [limit](https://yamuno.com/latex/symbols/limit), [differentiation](https://yamuno.com/latex/symbols/differentiation)

## Greek letters

| Source | Result | Source | Result |
| --- | --- | --- | --- |
| `\alpha` | $\alpha$ | `\Gamma` | $\Gamma$ |
| `\beta` | $\beta$ | `\Delta` | $\Delta$ |
| `\gamma` | $\gamma$ | `\Theta` | $\Theta$ |
| `\delta` | $\delta$ | `\Lambda` | $\Lambda$ |
| `\epsilon`, `\varepsilon` | $\epsilon, \varepsilon$ | `\Pi` | $\Pi$ |
| `\theta` | $\theta$ | `\Sigma` | $\Sigma$ |
| `\lambda` | $\lambda$ | `\Phi` | $\Phi$ |
| `\mu` | $\mu$ | `\Psi` | $\Psi$ |
| `\pi` | $\pi$ | `\Omega` | $\Omega$ |
| `\sigma` | $\sigma$ | | |
| `\phi`, `\varphi` | $\phi, \varphi$ | | |
| `\omega` | $\omega$ | | |

Capital letters that look like Latin ones (A, B, E, ...) have no command. Just type the Latin letter.

More: [Greek letters](https://yamuno.com/latex/symbols/greek-letters), [delta](https://yamuno.com/latex/symbols/delta)

## Relations

| Source | Result |
| --- | --- |
| `\leq`, `\geq` | $\leq, \geq$ |
| `\neq` | $\neq$ |
| `\approx` | $\approx$ |
| `\equiv` | $\equiv$ |
| `\sim` | $\sim$ |
| `\propto` | $\propto$ |
| `\ll`, `\gg` | $\ll, \gg$ |
| `a \mid b` | $a \mid b$ |

More: [greater than](https://yamuno.com/latex/symbols/greater-than), [not equal](https://yamuno.com/latex/symbols/not-equal), [approximately equal](https://yamuno.com/latex/symbols/approximately-equal), [equivalent](https://yamuno.com/latex/symbols/equivalent), [proportional](https://yamuno.com/latex/symbols/proportional), [divides](https://yamuno.com/latex/symbols/divides)

## Arrows and logic

| Source | Result |
| --- | --- |
| `\to`, `\rightarrow` | $\to$ |
| `\leftarrow` | $\leftarrow$ |
| `\leftrightarrow` | $\leftrightarrow$ |
| `\Rightarrow`, `\implies` | $\Rightarrow$ |
| `\Leftrightarrow`, `\iff` | $\Leftrightarrow$ |
| `\mapsto` | $\mapsto$ |
| `\forall` | $\forall$ |
| `\exists` | $\exists$ |
| `\neg` | $\neg$ |
| `\land`, `\lor` | $\land, \lor$ |
| `\therefore` | $\therefore$ |

More: [arrows](https://yamuno.com/latex/symbols/arrows), [implies](https://yamuno.com/latex/symbols/implies), [for all](https://yamuno.com/latex/symbols/for-all), [there exists](https://yamuno.com/latex/symbols/there-exists), [therefore](https://yamuno.com/latex/symbols/therefore)

## Sets

| Source | Result |
| --- | --- |
| `\in`, `\notin` | $\in, \notin$ |
| `\subset`, `\subseteq` | $\subset, \subseteq$ |
| `\cup`, `\cap` | $\cup, \cap$ |
| `\setminus` | $\setminus$ |
| `\emptyset`, `\varnothing` | $\emptyset, \varnothing$ |
| `\mathbb{R}`, `\mathbb{N}`, `\mathbb{Z}` | $\mathbb{R}, \mathbb{N}, \mathbb{Z}$ |
| `\{1, 2, 3\}` | $\\{1, 2, 3\\}$ |
| `\{x \in \mathbb{R} : x > 0\}` | $\\{x \in \mathbb{R} : x > 0\\}$ |

Curly braces are LaTeX syntax, so write `\{` and `\}` to show them.

More: [element of](https://yamuno.com/latex/symbols/element-of), [subset](https://yamuno.com/latex/symbols/subset), [union](https://yamuno.com/latex/symbols/union), [intersection](https://yamuno.com/latex/symbols/intersection), [empty set](https://yamuno.com/latex/symbols/empty-set), [real numbers](https://yamuno.com/latex/symbols/real-numbers)

## Brackets that grow

Plain brackets stay the same height. `\left` and `\right` make them fit what is inside.

| Source | Result |
| --- | --- |
| `(\frac{a}{b})` | $(\frac{a}{b})$ |
| `\left(\frac{a}{b}\right)` | $\left(\frac{a}{b}\right)$ |
| `\left[\frac{a}{b}\right]` | $\left[\frac{a}{b}\right]$ |
| `\left\lvert x \right\rvert` | $\left\lvert x \right\rvert$ |
| `\lVert v \rVert` | $\lVert v \rVert$ |
| `\langle u, v \rangle` | $\langle u, v \rangle$ |
| `\lfloor x \rfloor`, `\lceil x \rceil` | $\lfloor x \rfloor, \lceil x \rceil$ |

Every `\left` needs a matching `\right`. Use `\right.` for an invisible one.

More: [absolute value](https://yamuno.com/latex/symbols/absolute-value), [vertical bar](https://yamuno.com/latex/symbols/vertical-bar)

## Accents

| Source | Result |
| --- | --- |
| `\hat{x}` | $\hat{x}$ |
| `\bar{x}` | $\bar{x}$ |
| `\overline{AB}` | $\overline{AB}$ |
| `\vec{v}` | $\vec{v}$ |
| `\tilde{x}` | $\tilde{x}$ |
| `\dot{x}`, `\ddot{x}` | $\dot{x}, \ddot{x}$ |

More: [hat](https://yamuno.com/latex/symbols/hat), [bar](https://yamuno.com/latex/symbols/bar), [vector arrow](https://yamuno.com/latex/symbols/vector-arrow), [tilde](https://yamuno.com/latex/symbols/tilde)

## Text inside math

Spaces are ignored in math mode and letters are set as italic variables. Use `\text{}` for words.

| Source | Result |
| --- | --- |
| `v = d / t \text{ in m/s}` | $v = d / t \text{ in m/s}$ |
| `x = 1 \text{ if } y > 0` | $x = 1 \text{ if } y > 0$ |
| `\mathrm{kg}` | $\mathrm{kg}$ |
| `\mathbf{F} = m\mathbf{a}` | $\mathbf{F} = m\mathbf{a}$ |
| `a \quad b \qquad c` | $a \quad b \qquad c$ |

## Matrices

Use a block macro. `&` separates columns and `\\` ends a row.

```latex
\begin{pmatrix} a & b \\ c & d \end{pmatrix}
\begin{bmatrix} 1 & 0 \\ 0 & 1 \end{bmatrix}
\begin{vmatrix} a & b \\ c & d \end{vmatrix}
```

```math
\begin{pmatrix} a & b \\ c & d \end{pmatrix}
\quad
\begin{bmatrix} 1 & 0 \\ 0 & 1 \end{bmatrix}
\quad
\begin{vmatrix} a & b \\ c & d \end{vmatrix}
```

`pmatrix` uses round brackets, `bmatrix` square ones, `vmatrix` vertical bars for a determinant, and `matrix` has none. For a large matrix use `\cdots`, `\vdots` and `\ddots`:

```latex
\begin{bmatrix}
a_{11} & \cdots & a_{1n} \\
\vdots & \ddots & \vdots \\
a_{m1} & \cdots & a_{mn}
\end{bmatrix}
```

```math
\begin{bmatrix}
a_{11} & \cdots & a_{1n} \\
\vdots & \ddots & \vdots \\
a_{m1} & \cdots & a_{mn}
\end{bmatrix}
```

## Aligned equations

Put `&` before the sign you want to line up.

```latex
\begin{aligned}
(a + b)^2 &= (a + b)(a + b) \\
          &= a^2 + 2ab + b^2
\end{aligned}
```

```math
\begin{aligned}
(a + b)^2 &= (a + b)(a + b) \\
          &= a^2 + 2ab + b^2
\end{aligned}
```

## Cases

```latex
f(x) = \begin{cases}
  x^2 & \text{if } x \geq 0 \\
  -x  & \text{otherwise}
\end{cases}
```

```math
f(x) = \begin{cases}
  x^2 & \text{if } x \geq 0 \\
  -x  & \text{otherwise}
\end{cases}
```

## Degrees, percent and other escapes

Some characters mean something in LaTeX, so they need a backslash to show up.

| You want | Source |
| --- | --- |
| % | `\%` |
| & | `\&` |
| $ | `\$` |
| # | `\#` |
| _ | `\_` |
| { } | `\{ \}` |
| \ | `\backslash` |

```math
50\% \quad \text{R\&D} \quad \$10 \quad \#1 \quad \text{file\_name}
```

Degrees:

| Source | Result |
| --- | --- |
| `90^\circ` | $90^\circ$ |
| `25^\circ\text{C}` | $25^\circ\text{C}$ |
| `\angle ABC = 45^\circ` | $\angle ABC = 45^\circ$ |

A bare `%` starts a comment in LaTeX, so everything after it on that line disappears. This is the most common reason an equation looks cut off.

More: [percent](https://yamuno.com/latex/symbols/percent), [degree](https://yamuno.com/latex/symbols/degree)

## Chemistry

LaTeX Math for Confluence supports `\ce{}` for chemical formulas and reactions. GitHub does not render `\ce`, so these are source only.

```latex
\ce{H2O}
\ce{CO2 + H2O -> H2CO3}
\ce{2H2 + O2 -> 2H2O}
\ce{SO4^2-}
\ce{N2 + 3H2 <=> 2NH3}
```

Inside `\ce{}`, numbers after an element become subscripts and `->` or `<=>` become reaction arrows.

## Colour

| Source | Result |
| --- | --- |
| `\textcolor{red}{x} + \textcolor{blue}{y}` | $\textcolor{red}{x} + \textcolor{blue}{y}$ |
| `\color{teal} a^2 + b^2` | $\color{teal} a^2 + b^2$ |

Use colour sparingly. Pages are also read in dark mode.

## What KaTeX does not do

KaTeX renders math only. These do not work in Confluence:

- `\usepackage{...}`. Packages are not loaded, and the commonly used math is already built in.
- TikZ and PGF drawings. Use a diagram app or an image for those.
- Document commands such as `\section`, `\begin{document}` or `\cite`.
- A `\newcommand` in one macro is not available in the next. Define it again in each macro that uses it, or write the command out.

The full list of supported commands is in the [KaTeX documentation](https://katex.org/docs/supported.html).

## More

- [LaTeX symbols reference](https://yamuno.com/latex/symbols), with a page per symbol
- [Common math symbols cheat sheet](https://yamuno.com/latex/symbols/math-symbols)
- [How to add math equations to Confluence](https://yamuno.com/blogs/how-to-add-math-equations-to-confluence)
- [LaTeX Math for Confluence](https://yamuno.com/products/latex-math-for-confluence)

Spotted a mistake or a command people need that is missing? Open an issue or a pull request.

## License

[CC BY 4.0](LICENSE). Made by the Yamuno team.
