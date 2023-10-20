# Podstawy logiki matematycznej

- [Podstawy logiki matematycznej](#podstawy-logiki-matematycznej)
  - [Elementy logiki matematycznej](#elementy-logiki-matematycznej)
    - [Negatyw $\sim$](#negatyw-sim)
    - [Alternatywa $\lor$](#alternatywa-lor)
    - [Koniunkcja $\wedge$](#koniunkcja-wedge)
    - [Implikacja $\implies$](#implikacja-implies)
    - [Równoważność $\iff$](#równoważność-iff)
  - [Prawa Logiczne](#prawa-logiczne)
    - [Prawa de Morgana](#prawa-de-morgana)
    - [Prawo kontrapozycji](#prawo-kontrapozycji)


## Elementy logiki matematycznej

### Negatyw $\sim$

| $p$ | $\sim\!p$ |
| :-: |  :---: |
| 1 | 0 |
| 0 | 1 |

### Alternatywa $\lor$

| $p$ | $q$ | $p \lor q$ |
| :-: | :-: | :---: |
| 1 | 1 | 1 |
| 1 | 0 | 1 |
| 0 | 1 | 1 |
| 0 | 0 | 0 |

### Koniunkcja $\wedge$

| $p$ | $q$ | $p \wedge q$ |
| :-: | :-: | :---: |
| 1 | 1 | 1 |
| 1 | 0 | 0 |
| 0 | 1 | 0 |
| 0 | 0 | 0 |

### Implikacja $\implies$

| $p$ | $q$ | $p \implies q$ |
| :-: | :-: | :---: |
| 0 | 0 | 1 |
| 0 | 1 | 1 |
| 1 | 0 | 0 |
| 1 | 1 | 1 |

### Równoważność $\iff$

| $p$ | $q$ | $p \iff q$ |
| :-: | :-: | :---: |
| 1 | 1 | 1 |
| 0 | 0 | 1 |
| 1 | 0 | 0 |
| 0 | 1 | 0 |

## Prawa Logiczne

**Tautologia** - Zdanie zawsze prawdziwe.

### Prawa de Morgana

$[\sim\!(p \wedge q)] \iff (\sim\!p \; \lor \sim\!q)$

| $p$ | $q$ | $p \wedge q$ | $\sim\!(p \wedge q)$ | $\sim\!p$ | $\sim\!q$ | $\sim\!p\;\lor \sim\!q$ | $... \iff ...$ |
| :-: | :-: | :---: | :---: | :---: | :---: | :---: | :---: |
| 0 | 0 | 0 | 1 | 1 | 1 | 1 | 1 |
| 0 | 1 | 0 | 1 | 1 | 0 | 1 | 1 |
| 1 | 0 | 0 | 1 | 0 | 1 | 1 | 1 |
| 1 | 1 | 1 | 0 | 0 | 0 | 0 | 1 |

$[\sim\!(p \lor q)] \iff (\sim\!p \; \wedge \sim\!q)$

| $p$ | $q$ | $p \lor q$ | $\sim\!(p \lor q)$ | $\sim\!p$ | $\sim\!q$ | $\sim\!p\;\wedge \sim\!q$ | $... \iff ...$ |
| :-: | :-: | :---: | :---: | :---: | :---: | :---: | :---: |
| 0 | 0 | 0 | 1 | 1 | 1 | 1 | 1 |
| 0 | 1 | 1 | 0 | 1 | 0 | 0 | 1 |
| 1 | 0 | 1 | 0 | 0 | 1 | 0 | 1 |
| 1 | 1 | 1 | 0 | 0 | 0 | 0 | 1 |

### Prawo kontrapozycji

$(p \implies q) \iff (\sim\!p \implies \sim\!q)$

| $p$ | $q$ | $p \implies q$ | $\sim\!q$ | $\sim\!p$ | $\sim\!q\implies \sim\!p$ | $... \iff ...$ |
| :-: | :-: | :---: | :---: | :---: | :---: | :---: |
| 0 | 0 | 1 | 1 | 1 | 1 | 1 |
| 0 | 1 | 1 | 0 | 1 | 1 | 1 |
| 1 | 0 | 0 | 1 | 0 | 0 | 1 |
| 1 | 1 | 1 | 0 | 0 | 1 | 1 |