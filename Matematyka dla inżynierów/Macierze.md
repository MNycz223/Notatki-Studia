# Macierze

Macierz tworzą liczby wpisane do prostokątnej tabelki

$$
    A_{m,n} = 
    \begin{bmatrix}
        a_{1,1} & a_{1,2} & \cdots & a_{1,n} \\
        a_{2,1} & a_{2,2} & \cdots & a_{2,n} \\
        \vdots & \vdots & \ddots & \vdots \\
        a_{m,1} & a_{m,2} & \cdots & a_{m,n} \\
    \end{bmatrix}
$$

$$a_{ij}$$
$`i`$ - numer wiersza;
$`j`$ - numer kolumny;

$$
    M^{m \;\times\; n} \quad \text{- Zbiór wszystklich macierzy wymiaru m}  \times \text{n}
$$

## Szczególne typy macierzy

### Macierz zerowa
Maicerz złożona z samych zer

$$
    \theta _{3 \times 2} = 
    \begin{bmatrix}
        0 & 0 \\
        0 & 0 \\
        0 & 0 \\
    \end{bmatrix}
$$

### Macierz kwadratowa
Macierz w której liczba wierwszy równa się liczbie kolumn ($`m=n`$)

Wyróżniamy główną przekątną
```math
\begin{bmatrix}
    \ddots & \\
    & \ddots
\end{bmatrix}
```
$$
(a_{1,1}, \; a_{2,2}, \;\dots\; a_{n,n})
$$

### Macierz trójkątna
To macierz kwadratowa w której wszystkie elementy nad (dolna) lub pod (górna) główną przekątną wynoszą zero

```math
    \begin{bmatrix}
    \ddots &  0 \\
    \cdots & \ddots
    \end{bmatrix}
    \\
    \text{Dolna}
```

```math
    \begin{bmatrix}
    \ddots & \cdots \\
    0 & \ddots
    \end{bmatrix}
    \\
    \text{Górna}
```

### Macierz diagonalna
To macierz która jest trójkątna górna i dolna.
Inaczej mówiąc jest to macierz kwadratowa w której poza główną przekątną występują same zera

$$
    \begin{bmatrix}
    \ddots & 0 \\
    0 & \ddots
    \end{bmatrix}
$$

Każda macierz kwadratowa wymiaru **jeden** jest diagonalna

### Macierz jednostkowa
To macierz diagonalna w której na głównej przekątnej występują same `1`

$$
    I =
    \begin{bmatrix}
    1 &   &         & 0 \\
    & 1 &         &   \\
    &   & \ddots  &   \\
    0 &   &         & 1 \\
    \end{bmatrix}
$$

$$
    I_1 =
    \begin{bmatrix}
    1
    \end{bmatrix}
$$
$$
    I_2 =
    \begin{bmatrix}
    1 & 0 & 0 \\
    0 & 1 & 0 \\
    0 & 0 & 1 \\
    \end{bmatrix}
$$

## Działania na macierzach

### Transponowanie (Transpozycja)

$$
    A \in M^{m\;\times\;n},\quad
    B \in M^{n\;\times\;m} \qquad
    \substack
    {
        i \in \{1,2, \cdots,m\}\\
        j \in \{1,2, \cdots,n\}
    }
    \\
    B = A^T \iff b_{ji} = a_{ij}
$$

Aby transponować macierz $`A`$ należy zamienić wiersze macierzy $`A`$ na kolumny (albo kolumny na wiersze)

$$
    A = 
    \begin{bmatrix}
    3 & 0 & 5 \\
    4 & 7 & 1
    \end{bmatrix}
    \qquad
    A^T =
    \begin{bmatrix}
    3 & 4 \\
    0 & 7 \\
    5 & 1
    \end{bmatrix}
$$

### Mnożenie macierzy przez liczbę

```math
    A,B \in M^{m\;\times\;n},\quad
    \alpha \in R \qquad
    \substack
    {
        i \in \{1,2, \cdots,m\}\\
        j \in \{1,2, \cdots,n\}
    }
    \\
    B = \alpha \cdot A \iff b_{ij} = \alpha \cdot a_{ij}
```

Aby pomnożyć Macierz $`A`$ przez liczbę $`\alpha`$ każdy element macierzy A mnożymy przez liczbę $`\alpha`$

$$
    A = 
    \begin{bmatrix}
    3 & 5 \\
    0 & -1 \\
    -4 & 8
    \end{bmatrix}\qquad
    3A = 
    \begin{bmatrix}
    9 & 15 \\
    0 & -3 \\
    -12 & 24
    \end{bmatrix}
$$

### Dodawanie i odejmowanie macierzy

$$
    A,B,C,D \in M^{m\;\times\;n}\qquad
    \substack
    {
        i \in \{1,2, \cdots,m\}\\
        j \in \{1,2, \cdots,n\}
    }
    \\
    C = A + B \iff c_{ij} = a_{ij} + b_{ij}\\
    D = A - B \iff c_{ij} = a_{ij} - b_{ij}\\
$$

Dodawanie i odejmowanie można wykonać tylko na macierzach tego samego wymiaru.

Działania te wykonujemy na współrzędnych to znaczy dodajemy/odejmujemy liczby na tych samych pozycjach.

```math
A =
\begin{bmatrix}
4 & 0 & -3 \\
-2 & 5 & 1 \\
\end{bmatrix}\quad
B =
\begin{bmatrix}
-7 & 6 & 4 \\
-9 & 8 & 0 \\
\end{bmatrix}
```

```math
A + B =
\begin{bmatrix}
4 & 0 & -3 \\
-2 & 5 & 1 \\
\end{bmatrix}
+
\begin{bmatrix}
-7 & 6 & 4 \\
-9 & 8 & 0 \\
\end{bmatrix}
=
\begin{bmatrix}
-3 & 6 & 1 \\
-11 & 13 & 1 \\
\end{bmatrix}
```

```math
A - B =
\begin{bmatrix}
4 & 0 & -3 \\
-2 & 5 & 1 \\
\end{bmatrix}
-
\begin{bmatrix}
-7 & 6 & 4 \\
-9 & 8 & 0 \\
\end{bmatrix}
=
\begin{bmatrix}
11 & -6 & -7 \\
7 & -3 & 1 \\
\end{bmatrix}
```
```math
B - A =
\begin{bmatrix}
-11 & 6 & 7 \\
-7 & 3 & -1 \\
\end{bmatrix}
```

### Mnożenie macierzy

$$
    A \in M^{m \times p},\quad
    B \in M^{p \times n},\quad
    C \in M^{m \times n}
    \qquad
    \substack
    {
        i \in \{1,2, \cdots,m\}\\
        j \in \{1,2, \cdots,n\}
    }
    \\
    C = A \cdot B \iff c_{ij} = \sum_{k=1}^p a_{ik} \cdot b_{kj}
$$

Aby wykonać mnożenie $`A`$ razy $`B`$ liczba kolumn macierzy $`A`$ musi być równa liczbie wierszy macierzy $`B`$

$$
    \begin{bmatrix}
    a_1, a_2, \cdots\!, a_n 
    \end{bmatrix}
    \cdot
    \begin{bmatrix}
    b_1\\ 
    b_2\\
    \vdots\\
     b_n 
    \end{bmatrix} =
    a_1b_1 + a_2b_2+\dots a_nb_n
$$

Aby wykonać mnożenie $`A \cdot B`$ pierwszy wiersz $`A`$ mnożymy przez wszystkie kolumny $`B`$, następnie drugi wiersz $`A`$ przez wszystkie kolumny $`B`$ i tak dalej.

$$
    A =
    \begin{bmatrix}
    4 & 0 & -2 \\
    1 & 5 & -1
    \end{bmatrix}\quad
    B =
    \begin{bmatrix}
    3 & 1 \\
    0 & 2 \\
    4 & 0
    \end{bmatrix}
$$

$$
    A \cdot B = 
    \begin{bmatrix}
    4 & 0 & -2 \\
    1 & 5 & -1
    \end{bmatrix}\cdot
    \begin{bmatrix}
    3 & 1 \\
    0 & 2 \\
    4 & 0
    \end{bmatrix} =
    \begin{bmatrix}
    4\cdot3+0\cdot0+4\cdot(-2) & 4\cdot1+0\cdot2+(-2)\cdot0 \\
    1\cdot3+5\cdot0+(-1)\cdot4 & 1\cdot1+5\cdot2+(-1)\cdot0 
    \end{bmatrix}\\ = 
    \begin{bmatrix}
    4 & 4 \\
    -1 & 11 
    \end{bmatrix} 
$$
$$
    B \cdot A = 
    \begin{bmatrix}
    3 & 1 \\
    0 & 2 \\
    4 & 0
    \end{bmatrix}\cdot
    \begin{bmatrix}
    4 & 0 & -2 \\
    1 & 5 & -1
    \end{bmatrix} =
    \begin{bmatrix}
    3\cdot4+1\cdot1 & 3\cdot0+1\cdot5 & 3\cdot(-2)+3\cdot(-1) \\
    0\cdot4+2\cdot1 & 0\cdot0+2\cdot5 & 0\cdot(-2)+2\cdot(-1) \\
    4\cdot4+0\cdot1 & 4\cdot0+0\cdot5 & 4\cdot(-2)+0\cdot(-1) 
    \end{bmatrix}\\ = 
    \begin{bmatrix}
    13 & 5 & -9 \\
    2 & 10 & -2 \\
    16 & 0 & -8 
    \end{bmatrix} 
$$

### Wyznacznik macierzy

Wyznacznik to liczba przyporządkowana macierzy kwadratowej
```math
detA \text{ - wyznacznik} 
```

```math
n=1
\quad
A =
\begin{bmatrix}
a
\end{bmatrix}
\quad
detA = a
```

```math
n=2
\quad
A =
\begin{bmatrix}
a & b \\
c & d
\end{bmatrix}
\quad
detA =ad - bc
```

#### Wzory Sarrusa 
```math
    n = 3
```

```math
det
\substack{
    \begin{bmatrix}
    1 & 0 & 3 \\
    0 & 2 & 5 \\
    4 & 1 & 6
    \end{bmatrix}
    \\
    \begin{matrix}
    1 & 0 & 3 \\
    0 & 2 & 5
    \end{matrix}
} =
(1 \cdot 2 \cdot 6 + 0 \cdot 1 \cdot 3 + 4 \cdot 0 \cdot 5) - (4 \cdot 2 \cdot 3 + 1 \cdot 1 \cdot 5 + 0 \cdot 0 \cdot 6) = 12 - 29 = -17
```

#### Tw. Laplace'a
Jeżeli $`A`$ jest macierzą kwadratową wymioaru $`n \geqslant 2`$, to 

```math
detA =
\sum^{n}_{j = 1}
a_{ij}D_{ij}
\qquad
\text{Rozwinięcie względem wiersza} \; i
```
```math
detA =
\sum^{n}_{i = 1}
a_{ij}D_{ij}
\qquad
\text{Rozwinięcie względem kolumny} \; j
```

Gdzie $`D_{ij}`$ to dopełnienie algebraiczne $`a_{ij}`$

```math
D_{ij} = (-1)^{i+j} \cdot detA_{ij}
```
gdzie $`A_{ij}`$ to macierz, która powstaje z $`A`$ przez skreślenie wiersza $`i`$ oraz kolumny $`j`$

Stosując wzór laplace'a szukamy wiersza lub kolumny z największą ilością zer.
Jeżeli w maceirzy występuje wiersz lub kolumna złożona z samych zer to $`detA = 0`$.
