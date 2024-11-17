# MAT-320-Notes

\documentclass{article}
\usepackage{amsmath,amssymb,amsthm}

% Theorem Styles
\newtheorem{definition}{Definition}
\newtheorem{lemma}{Lemma}
\newtheorem{proposition}{Proposition}
\newtheorem{theorem}{Theorem}
\newtheorem{corollary}{Corollary}

\begin{document}

\section*{Cheat Sheet}

\section*{The Mean Value Theorem}
\textbf{Theorem:} Let $f: [a, b] \to \mathbb{R}$ be a continuous function on the closed interval $[a, b]$ and differentiable on the open interval $(a, b)$. Then there exists a point $c \in (a, b)$ such that
\[
f'(c) = \frac{f(b) - f(a)}{b - a}.
\]

\section*{Rolle's Theorem}
\textbf{Theorem:} Let $f: [a, b] \to \mathbb{R}$ be a continuous function on the closed interval $[a, b]$, differentiable on the open interval $(a, b)$, and suppose $f(a) = f(b)$. Then there exists a point $c \in (a, b)$ such that
\[
f'(c) = 0.

\begin{theorem}[Intermediate Value Theorem (IVT)]
Let $f : [a, b] \to \mathbb{R}$ be a continuous function. If $f(a) \neq f(b)$ and $k$ is any value between $f(a)$ and $f(b)$, then there exists some $c \in (a, b)$ such that $f(c) = k$.
\end{theorem}

\begin{theorem}[Extreme Value Theorem (Weierstrass)]
Let $f : [a, b] \to \mathbb{R}$ be a continuous function. Then $f$ attains both a maximum and a minimum value on $[a, b]$. That is, there exist $x_m, x_M \in [a, b]$ such that
\[
    f(x_m) \leq f(x) \leq f(x_M) \quad \text{for all } x \in [a, b].
\]
\end{theorem}

\section*{Metric Spaces}

\begin{definition}[Metric Space]
A metric space is a set $X$ equipped with a function $d$ such that:
\begin{enumerate}
    \item $d(x, y) = 0 \iff x = y$ (identity of indiscernibles),
    \item $d(x, y) = d(y, x)$ (symmetry),
    \item $d(x, z) \leq d(x, y) + d(y, z)$ (triangle inequality).
\end{enumerate}
\end{definition}

\subsection*{Topology}

\begin{definition}
A subset $U \subseteq X$ of a metric space $(X, d)$ is \textbf{open} if for every $x \in U$, there exists $\varepsilon > 0$ such that $B(x, \varepsilon) \subseteq U$, where $B(x, \varepsilon)$ denotes the open ball centered at $x$ with radius $\varepsilon$.
\end{definition}

\begin{definition}
A subset $F \subseteq X$ of a metric space $(X, d)$ is \textbf{closed} if its complement $X \setminus F$ is open.
\end{definition}

\begin{proposition}
The intersection of any collection of closed sets is closed. The union of any collection of open sets is open.
\end{proposition}

\begin{proposition}
A subset $F \subseteq X$ of a metric space $(X, d)$ is closed if and only if it contains all its limit points.
\end{proposition}

\begin{definition}[Limit Point]
A point $x \in X$ is a \textbf{limit point} of a subset $A \subseteq X$ if every open ball $B(x, \varepsilon)$ centered at $x$ with radius $\varepsilon > 0$ intersects $A$ in some point other than $x$ itself.
\end{definition}

\section*{Connectedness}

\begin{definition}[Connected/Disconnected Metric Space]
We say that a metric space $(X, d)$ is connected if the only subsets $E \subseteq X$ that are simultaneously open and closed are $E = X$ and $E = \emptyset$. A metric space that is not connected is called disconnected.
\end{definition}

\begin{lemma}
A metric space $(X, d)$ is disconnected if and only if there are two non-empty, disjoint, open subsets $A, B \subseteq X$ such that $X = A \cup B$.
\end{lemma}

\begin{definition}[Connected Subset]
A subset $E \subseteq X$ of a metric space $(X, d)$ is connected if $(E, d_E)$ is a connected metric space, where $d_E$ is the restriction of $d$ to $E \times E$.
\end{definition}

\begin{proposition}
A subset $E \subseteq X$ of a metric space $(X, d)$ is disconnected if and only if $E \subseteq U \cup V$ for two open subsets $U, V \subseteq X$ such that $U \cap E \neq \emptyset$, $V \cap E \neq \emptyset$, and $(U \cap V) \cap E = \emptyset$.
\end{proposition}

\begin{proposition}
An open subset $E \subseteq X$ of a metric space $(X, d)$ is disconnected if and only if there are two non-empty, disjoint, open subsets $A, B \subseteq X$ such that $E = A \cup B$.
\end{proposition}

\begin{theorem}
The interval $(0, 1) \subseteq \mathbb{R}$ is connected.
\end{theorem}

\begin{theorem}
Suppose that $f : X \to Y$ is a continuous map between metric spaces. If $E \subseteq X$ is connected, then $f(E) \subseteq Y$ is connected.
\end{theorem}

\begin{definition}[Property P]
We say that a set $I \subseteq \mathbb{R}$ has property $P$ if whenever $a \leq z \leq b$ with $a, b \in I$, then $z \in I$.
\end{definition}

\begin{theorem}
A non-empty subset $I \subseteq \mathbb{R}$ is connected if and only if it is an interval.
\end{theorem}

\begin{corollary}
Let $(X, d)$ be a connected metric space and $f : X \to \mathbb{R}$ be a continuous function. Then the image of $f$ is an interval $I \subseteq \mathbb{R}$.
\end{corollary}

\begin{theorem}[Bolzano's Theorem]
Suppose that $f : [a, b] \to \mathbb{R}$ is a continuous function. If $f(a) < c$ and $f(b) > c$, then there is some $x \in (a, b)$ such that $f(x) = c$.
\end{theorem}

\begin{definition}[Path Connectedness]
Let $(X, d)$ be a metric space. A path connecting two points $x$ and $y \in X$ is a continuous function $\gamma : [0, 1] \to X$ such that $\gamma(0) = x$ and $\gamma(1) = y$. We say that $(X, d)$ is path connected if every pair of points of $X$ is connected by a path.
\end{definition}

\begin{theorem}
A path connected metric space is connected.
\end{theorem}

\section*{Compactness}

\begin{definition}[Compact Metric Space]
A metric space $(X, d)$ is called compact if given any collection of open sets $\{U_\alpha \subseteq X : \alpha \in I\}$ such that:
\[
X = \bigcup_{\alpha \in I} U_\alpha,
\]
one can find finitely many indices $\alpha_1, \ldots, \alpha_n \in I$ such that:
\[
X = U_{\alpha_1} \cup \cdots \cup U_{\alpha_n}.
\]
\end{definition}

\begin{example}
The metric space $X = \mathbb{R}$ is not compact. To see this, consider the open cover $\{U_\alpha : \alpha \in [1, \infty)\}$ where $U_\alpha = (-\alpha, \alpha)$. For any finite subcollection $\{U_{\alpha_1}, \ldots, U_{\alpha_n}\}$, the union is $(-M, M)$ with $M = \max\{\alpha_1, \ldots, \alpha_n\}$, which does not cover $\mathbb{R}$ entirely.
\end{example}

\begin{definition}[Compact Subset]
A subset $E \subseteq X$ of a metric space $(X, d)$ is compact if for every open cover $\{U_\alpha \subseteq X : \alpha \in I\}$ such that:
\[
E \subseteq \bigcup_{\alpha \in I} U_\alpha,
\]
there exists a finite subcover $\{U_{\alpha_1}, \ldots, U_{\alpha_n}\}$ such that:
\[
E \subseteq U_{\alpha_1} \cup \cdots \cup U_{\alpha_n}.
\]
\end{definition}

\begin{lemma}
A subset $E \subseteq X$ of a metric space $(X, d)$ is compact if and only if the metric space $(E, d_E)$ is compact, where $d_E$ is the restriction of $d$ to $E \times E$.
\end{lemma}

\begin{theorem}
The closed interval $[0, 1] \subseteq \mathbb{R}$ is compact.
\end{theorem}

\begin{proof}
Let $\{U_\alpha \subseteq \mathbb{R} : \alpha \in I\}$ be an open cover of $[0, 1]$. Assume, by contradiction, that no finite subcover exists. Construct a nested sequence of intervals $[0, 1] = I_0 \supseteq I_1 \supseteq I_2 \supseteq \cdots$, where each $I_n = [a_n, b_n]$ cannot be covered by finitely many sets in the open cover. The length of $I_n$ decreases geometrically, and the intersection of all $I_n$ contains exactly one point $x$. This $x$ must belong to some $U_\alpha$, contradicting the assumption that no finite subcover exists.
\end{proof}

\begin{theorem}[Compactness and Continuity]
If $f : X \to Y$ is a continuous function and $K \subseteq X$ is compact, then $f(K) \subseteq Y$ is compact.
\end{theorem}

\begin{corollary}
Any finite, closed interval $[a, b] \subseteq \mathbb{R}$ is compact.
\end{corollary}

\begin{lemma}
A compact subset $K$ of a metric space $X$ is closed.
\end{lemma}

\begin{theorem}[Weierstrass Theorem]
A continuous function $f : [a, b] \to \mathbb{R}$ attains its maximum and minimum values. That is, there exist $x_m, x_M \in [a, b]$ such that:
\[
f(x_m) = \min_{x \in [a, b]} f(x), \quad f(x_M) = \max_{x \in [a, b]} f(x).
\]
\end{theorem}

\begin{theorem}[Heine-Borel Theorem]
A subset of $\mathbb{R}^n$ is compact if and only if it is closed and bounded.
\end{theorem}

\begin{definition} [Sequential Compactness]
A metric space (X, d) is sequentially compact if every sequence of points in X has a convergent subsequence converging to a point in X.
\end{definition}

\begin{corollary} [Sequential Compactness]
A metric space (X, d) is compact if and only if it is sequentially compact.
\end{corollary}

\section*{Completeness}

\begin{definition}[Cauchy Sequence]
A sequence $\{x_n\}$ in a metric space $(X, d)$ is a \textbf{Cauchy sequence} if for every $\varepsilon > 0$ there exists an $N \in \mathbb{N}$ such that:
\[
d(x_n, x_m) < \varepsilon \quad \text{for all } n, m \geq N.
\]
\end{definition}

\begin{definition}[Complete Metric Space]
A metric space $(X, d)$ is called \textbf{complete} if every Cauchy sequence in $X$ converges to a point in $X$.
\end{definition}

\begin{lemma}
Any converging sequence in a metric space is a Cauchy sequence.
\end{lemma}

\begin{lemma}
A Cauchy sequence $\{x_n\}$ in a metric space has bounded diameter. Specifically, there exists a constant $C$ such that:
\[
\sup_{n,m} d(x_n, x_m) \leq C.
\]
\end{lemma}

\begin{lemma}
If a Cauchy sequence $\{x_n\}$ in a metric space has a converging subsequence $\{x_{n_k}\}$, then $\{x_n\}$ converges to the same limit.
\end{lemma}

\begin{theorem}
A compact metric space is complete.
\end{theorem}

\begin{theorem}
The space $\mathbb{R}^n$ with the standard Euclidean metric is a complete metric space.
\end{theorem}

\begin{theorem}
The space $\ell^2$ (the space of square-summable sequences) is a complete metric space.
\end{theorem}

\subsection*{Sequences of Functions}

\begin{definition}[Pointwise Convergence]
A sequence of functions $\{f_n : I \to \mathbb{R}\}$ is said to converge \textbf{pointwise} to a function $f : I \to \mathbb{R}$ on a set $E \subseteq I$ if for every $x \in E$:
\[
\lim_{n \to \infty} f_n(x) = f(x).
\]
\end{definition}

\begin{definition}[Uniform Convergence]
A sequence of functions $\{f_n : I \to \mathbb{R}\}$ is said to converge \textbf{uniformly} to a function $f : I \to \mathbb{R}$ on a set $E \subseteq I$ if for every $\varepsilon > 0$, there exists an $N \in \mathbb{N}$ such that:
\[
|f_n(x) - f(x)| < \varepsilon \quad \text{for all } n \geq N \text{ and } x \in E.
\]
\end{definition}

\begin{proposition}
A sequence $\{f_n\}$ of functions in $B(E, \mathbb{R})$ converges in the metric:
\[
d(f, g) = \sup_{x \in E} |f(x) - g(x)|
\]
if and only if it converges uniformly on $E$.
\end{proposition}

\begin{theorem}
The metric space $B(E, \mathbb{R})$ (the space of bounded functions on $E$) is complete under the uniform metric.
\end{theorem}


\end{document}
