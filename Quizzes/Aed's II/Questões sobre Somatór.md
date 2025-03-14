# Questões sobre Somatório e Complexidade de Algoritmos

## 1. Somatório de uma Progressão Aritmética
**Questão:**
Calcule o valor do seguinte somatório e encontre sua fórmula fechada:

$$
S = \sum_{i=1}^{n} (2i + 3)
$$

a) 
𝑂
(
𝑛
)


b) 
𝑂
(
𝑛
²
)


c) 
𝑂
(
log
⁡
𝑛
)


d) 
𝑂
(
𝑛
log
⁡
𝑛
)


e) 
𝑂
(
2^n
)


**Resolução:**  
Esse somatório pode ser dividido em duas partes:

$$
S = \sum_{i=1}^{n} 2i + \sum_{i=1}^{n} 3
$$

A primeira parte é uma progressão aritmética:

$$
\sum_{i=1}^{n} i = \frac{n(n+1)}{2}
$$

Multiplicando por 2:

$$
\sum_{i=1}^{n} 2i = n(n+1)
$$

A segunda parte é:

$$
\sum_{i=1}^{n} 3 = 3n
$$

Portanto:

$$
S = n(n+1) + 3n = n^2 + 4n
$$

**Complexidade:** \( O(𝑛²) \)

**Resposta:** \( O(𝑛²) \)

---

## 2. Somatório de uma Progressão Geométrica
**Questão:**
Considere o seguinte somatório:

$$
S = \sum_{i=0}^{n} 2^i
$$

a) 
𝑂
(
𝑛
)


b) 
𝑂
(
𝑛
²
)


c) 
𝑂
(
log
⁡
𝑛
)


d) 
𝑂
(
𝑛
log
⁡
𝑛
)


e) 
𝑂
(
2^n
)

**Resolução:**  
Esse é um somatório de uma **progressão geométrica** de razão \( r = 2 \). A soma de uma progressão geométrica é dada por:

$$
S = \frac{2^{n+1} - 1}{2 - 1} = 2^{n+1} - 1
$$

**Complexidade:** \( O(2^n) \) (cresce exponencialmente)

**Resposta:** \( O(2^n) \)

---

## 3. Somatório de Comparações no Insertion Sort
**Questão:**
No pior caso, o Insertion Sort realiza o seguinte número de comparações:

$$
S = \sum_{i=1}^{n-1} i
$$

a) 
𝑂
(
𝑛
)


b) 
𝑂
(
𝑛
²
)


c) 
𝑂
(
log
⁡
𝑛
)


d) 
𝑂
(
𝑛
log
⁡
𝑛
)


e) 
𝑂
(
2^n
)

**Resolução:**  
Esse somatório é uma **progressão aritmética**:

$$
S = \frac{(n-1)n}{2}
$$

**Resposta:** A complexidade é **O(n²)**.


---

## 4. Somatório de Operações em um Loop Duplo
**Questão:**
Considere o seguinte código:

```c
for (i = 1; i <= n; i++) {
    for (j = 1; j <= i; j++) {
        // Operação constante
    }
}
```

a) 
𝑂
(
𝑛
)


b) 
𝑂
(
𝑛
²
)


c) 
𝑂
(
log
⁡
𝑛
)


d) 
𝑂
(
𝑛
log
⁡
𝑛
)


e) 
𝑂
(
2^n
)

**Resolução:**  
O número total de operações é:

$$
S = \sum_{i=1}^{n} i = \frac{n(n+1)}{2}
$$

**Resposta:** A complexidade é **O(n²)**.


---

## 5. Somatório e Complexidade do MergeSort
**Questão:**
O algoritmo MergeSort divide um array de tamanho **n** em duas partes, realiza a ordenação recursivamente e, ao final, faz a fusão dos elementos. Sua recorrência é dada por:

$$
T(n) = 2T(n/2) + O(n)
$$

a) 
𝑂
(
𝑛
)


b) 
𝑂
(
𝑛
²
)


c) 
𝑂
(
log
⁡
𝑛
)


d) 
𝑂
(
𝑛
log
⁡
𝑛
)


e) 
𝑂
(
2^n
)

**Resolução:**  
Expandindo a recorrência:

$$
T(n) = 2T(n/2) + n
$$

$$
= 4T(n/4) + 2n
$$

$$
= 8T(n/8) + 3n
$$

Após \( \log n \) divisões, temos:

$$
T(n) = O(n \log n)
$$

**Resposta:** \( O(n \log n) \)

---

## 6. Somatório no Bubble Sort
**Questão:**
O algoritmo Bubble Sort, no pior caso, realiza as seguintes comparações:

$$
S = \sum_{i=1}^{n-1} (n-i)
$$

**Resolução:**  
Esse somatório é equivalente a:

$$
S = \frac{n(n-1)}{2}
$$

a) 
𝑂
(
𝑛
)


b) 
𝑂
(
𝑛
²
)


c) 
𝑂
(
log
⁡
𝑛
)


d) 
𝑂
(
𝑛
log
⁡
𝑛
)


e) 
𝑂
(
2^n
)

**Resposta:** A complexidade é **O(n²)**.


---

## 7. Complexidade de um Algoritmo com Loop Aninhado
**Questão:**
Considere o seguinte código:

```c
for (i = 1; i <= n; i *= 2) {
    for (j = 1; j <= n; j++) {
        // Operação constante
    }
}
```
Expresse o número total de operações como um somatório e determine sua complexidade.

a) 
𝑂
(
𝑛
)



b) 
𝑂
(
𝑛
log
⁡
𝑛
)


c) 
𝑂
(
𝑛
2
)


d) 
𝑂
(
log
⁡
𝑛
)


e) 
𝑂
(
1
)


**Resolução:**  
O loop externo executa enquanto \( i \) cresce como uma progressão geométrica \( i = 1, 2, 4, 8, \dots \), então ele roda **log(n) vezes**. O loop interno executa **n vezes**.  

Total de operações:

$$
S = \sum_{k=1}^{\log n} n = n \log n
$$

**Resposta:** A complexidade é **O(n log n)**.


---

## 8. Somatório e Complexidade do QuickSort
**Questão:**
O algoritmo QuickSort, no pior caso, faz a seguinte quantidade de comparações:

$$
S = \sum_{i=1}^{n} i
$$

Qual a complexidade desse somatório?

a) 
𝑂
(
𝑛
)



b) 
𝑂
(
𝑛
log
⁡
𝑛
)


c) 
𝑂
(
𝑛
²
)


d) 
𝑂
(
log
⁡
𝑛
)


e) 
𝑂
(
𝑛
log
⁡
𝑛²
)



**Resolução:**  
Esse somatório é uma progressão aritmética:

$$
S = \frac{n(n+1)}{2}
$$

**Resposta:** A complexidade é **O(n²)**.



