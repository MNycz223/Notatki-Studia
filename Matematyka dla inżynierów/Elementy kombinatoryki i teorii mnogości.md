# Elementy kombinatoryki i teorii mnogości

## Działania na zbiorach

```math
C = A \cup B \qquad\text{Suma}
```
```math
D = A \cap B \qquad\text{Iloczyn}
```
```math
E = A \setminus B \qquad\text{Różnica}
```
```math
A` = X \setminus A \qquad\text{Dopełnienie zbioru A}
```

## Iloczyn kartezjański

```math
A \times B = \{(a, b) : a \in A \; \text{i} \; b \in B\}
```

```math
\substack{
    A = \{a, b, c\} \qquad B = \{1, 2\} \\
    A \times B = \{(a,1)(a,2)(b,1)(b,2)(c,1)(c,2)\}
}
```

Oznaczenie: $`|X| \text{ - ilość elementów}`$

Tw. $`|A \times B| = |A| \cdot |B|`$

$`\mathbb{R}`$ - zbiór liczb rzeczywistych (prosta liczbowa)

$`\mathbb{R}^2 = \mathbb{R} \times \mathbb{R} = \{(x,y) : x \in \mathbb{R} \; \text{i} \; y \in \mathbb{R}\}`$ - płaszczyzna

$`\mathbb{R}^n`$ - przestrzeń $`n`$ - wymiarowa

## Kombinatoryka

### Silnia

$`n!` - $`n`$ silnia $`n \in \mathbb{N}_0`$

```math
n! = 
\begin{cases}
    1, & \quad n = 0 \lor n = 1 \\
    1 \cdot 2 \cdot \ldots \cdot n, & \quad n > 1
\end{cases}
```

```math
n! = (n - 1)! \cdot n, \quad n \in \mathbb{N}
```

Def. Permutacja skończonego zbioru A to ciąg wszystkich elementów zbioru A.

Tw. Ilość wszystkich permutacji zbioru $`n`$-elementowego wynosi $`n!`$

### Symbol Newtona

```math
\binom{n}{k} = 
\frac{n!}{k!(n-k)!} \qquad
\substack{
    k,\;n\;\in\;\mathbb{N}_0 \\
    k\;\leqslant\;n
}
```

```math
\binom{n}{n-k} = 
\binom{n}{k} \quad dla
\substack{
    k,\;n\;\in\;\mathbb{N}_0 \\
    k\;\leqslant\;n
}
```

```math
\binom{n}{0} = 1 \quad
\binom{n}{1} = n \quad
\binom{n}{n - 1} = n \quad
\binom{n}{n} = 1 \quad
```

Tw. Ilość wszystkich $`k`$-elementowych podzbiorów zbioru $`n`$-elementowego wynosi $`\binom{n}{k}`$

Tw. Ilość wszystkich podzbiorów zbioru $`n`$-elementowego $`2^n`$

Tw. Dla $`k,n \in \mathbb{N}, k \leqslant n`$
```math
\binom{n}{k-1}+
\binom{n}{k} = 
\binom{n+1}{k}
```

## Symbol sumy

$`\sum`$ - sigma, symbol sumy

```math
\sum^{5}_{i=2} i^2 = 2^2 + 3^2 + 4^2 + 5^2 = 4 + 9 + 16 + 25 = 54
```

## Symbol iloczynu

$`\prod`$ - pi, symbol iloczynu

```math
\prod^{n}_{i=1} i = 1 \cdot 2 \cdot 3 \cdot \ldots \cdot n = n!
```

## Trójkąt Pascala

```math
\binom{0}{0} \\
\binom{1}{0}\quad\binom{1}{1} \\
\binom{2}{0}\quad\binom{2}{1}\quad\binom{2}{2} \\
\binom{3}{0}\quad\binom{3}{1}\quad\binom{3}{2}\quad\binom{3}{3} \\
\binom{4}{0}\quad\binom{4}{1}\quad\binom{4}{2}\quad\binom{4}{3}\quad\binom{4}{4} \\
\binom{5}{0}\quad\binom{5}{1}\quad\binom{5}{2}\quad\binom{5}{3}\quad\binom{5}{4}\quad\binom{5}{5} \\
\binom{6}{0}\quad\binom{6}{1}\quad\binom{6}{2}\quad\binom{6}{3}\quad\binom{6}{4}\quad\binom{6}{5}\quad\binom{6}{6}
```

```math
1 \\
1\quad1 \\
1\quad2\quad1 \\
1\quad3\quad3\quad1 \\
1\quad4\quad6\quad4\quad1 \\
1\quad5\quad10\quad10\quad5\quad1 \\
1\quad6\quad15\quad20\quad15\quad6\quad1
```

### Dwumian Newtona

Tw. Dwumian Newtona, Dla  $`a, b \in \mathbb{R} \;\text{i}\; n \in \mathbb{N}`$

```math
(a+b)^n = \sum^{n}_{k=0} \binom{n}{k}a^{n-k}b^k
```