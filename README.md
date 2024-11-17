# Cheat Sheet

## The Mean Value Theorem
**Theorem**:  
Let \( f : [a, b] \to \mathbb{R} \) be a continuous function on the closed interval \([a, b]\), and differentiable on the open interval \((a, b)\). Then, there exists a point \( c \in (a, b) \) such that:
\[
f'(c) = \frac{f(b) - f(a)}{b - a}.
\]

---

## Rolle's Theorem
**Theorem**:  
Let \( f : [a, b] \to \mathbb{R} \) be a continuous function on the closed interval \([a, b]\), differentiable on the open interval \((a, b)\), and suppose \( f(a) = f(b) \). Then, there exists a point \( c \in (a, b) \) such that:
\[
f'(c) = 0.
\]

---

## Intermediate Value Theorem (IVT)
**Theorem**:  
Let \( f : [a, b] \to \mathbb{R} \) be a continuous function. If \( f(a) \neq f(b) \) and \( k \) is any value between \( f(a) \) and \( f(b) \), then there exists some \( c \in (a, b) \) such that:
\[
f(c) = k.
\]

---

## Extreme Value Theorem (Weierstrass)
**Theorem**:  
Let \( f : [a, b] \to \mathbb{R} \) be a continuous function. Then \( f \) attains both a maximum and a minimum value on \([a, b]\). That is, there exist \( x_m, x_M \in [a, b] \) such that:
\[
f(x_m) \leq f(x) \leq f(x_M), \quad \text{for all } x \in [a, b].
\]

---

## Metric Spaces

### Metric Space
A **metric space** is a set \( X \) equipped with a distance function \( d \) such that for all \( x, y, z \in X \):
1. \( d(x, y) = 0 \iff x = y \) (identity of indiscernibles),
2. \( d(x, y) = d(y, x) \) (symmetry),
3. \( d(x, z) \leq d(x, y) + d(y, z) \) (triangle inequality).

---

### Open and Closed Sets
- A subset \( U \subseteq X \) is **open** if for every \( x \in U \), there exists \( \varepsilon > 0 \) such that the open ball \( B(x, \varepsilon) \subseteq U \).  
- A subset \( F \subseteq X \) is **closed** if its complement \( X \setminus F \) is open.

**Propositions**:
1. The intersection of any collection of closed sets is closed.
2. The union of any collection of open sets is open.
3. A subset \( F \subseteq X \) is closed if and only if it contains all its limit points.

### Limit Point
A point \( x \in X \) is a **limit point** of a subset \( A \subseteq X \) if every open ball \( B(x, \varepsilon) \) intersects \( A \) in some point other than \( x \) itself.

---

## Connectedness

### Definition
A metric space \( (X, d) \) is **connected** if the only subsets \( E \subseteq X \) that are simultaneously open and closed are \( E = X \) and \( E = \emptyset \). A metric space that is not connected is called **disconnected**.

### Lemma
A metric space \( (X, d) \) is disconnected if and only if there exist two non-empty, disjoint, open subsets \( A, B \subseteq X \) such that \( X = A \cup B \).

---

## Compactness

### Definition
A metric space \( (X, d) \) is **compact** if every open cover of \( X \) has a finite subcover.

### Examples
- The metric space \( \mathbb{R} \) is **not compact**.
- The closed interval \([0, 1] \subseteq \mathbb{R}\) is **compact**.

### Theorems
1. A subset \( E \subseteq X \) is compact if and only if \( (E, d_E) \) is compact.
2. A compact metric space is closed and bounded.

**Heine-Borel Theorem**:  
A subset of \( \mathbb{R}^n \) is compact if and only if it is closed and bounded.

---

## Completeness

### Definitions
- A **Cauchy sequence** is a sequence \( (x_n) \) in \( (X, d) \) such that for every \( \varepsilon > 0 \), there exists \( N \in \mathbb{N} \) such that \( d(x_n, x_m) < \varepsilon \) for all \( n, m \geq N \).
- A metric space \( (X, d) \) is **complete** if every Cauchy sequence in \( X \) converges to a point in \( X \).

### Theorems
1. A compact metric space is complete.
2. \( \mathbb{R}^n \) with the standard Euclidean metric is complete.

---

## Path Connectedness

### Definition
A metric space \( (X, d) \) is **path connected** if any two points \( x, y \in X \) can be joined by a continuous path \( \gamma : [0, 1] \to X \) such that \( \gamma(0) = x \) and \( \gamma(1) = y \).

### Theorem
Every path connected metric space is connected.
