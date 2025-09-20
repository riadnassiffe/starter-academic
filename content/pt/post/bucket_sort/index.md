---
title: "Bucksort"
date: 2025-09-18T14:33:15-03:00
draft: false
---
# Aula sobre Bucket Sort

## 1. Introdução ao Bucket Sort

O Bucket Sort, também conhecido como Bin Sort, é um algoritmo de ordenação não comparativo que funciona distribuindo os elementos de um array em um número finito de 'baldes' (buckets). Cada balde é então ordenado individualmente, e os elementos são concatenados para formar o array ordenado.

É mais eficiente quando os dados de entrada são uniformemente distribuídos em um determinado intervalo.

## 2. Como Funciona o Bucket Sort

O processo do Bucket Sort geralmente segue os seguintes passos:

1. **Criação dos Baldes:** Inicialmente, um conjunto de baldes vazios é criado. O número de baldes pode variar dependendo da distribuição dos dados e do tamanho do array de entrada.
2. **Distribuição:** Cada elemento do array de entrada é colocado em seu respectivo balde. A escolha do balde para cada elemento é baseada em uma função de mapeamento que distribui os elementos de forma uniforme.
3. **Ordenação Individual:** Cada balde é então ordenado individualmente. Para isso, pode-se usar outro algoritmo de ordenação (como Insertion Sort, que é eficiente para pequenos conjuntos de dados) ou até mesmo o próprio Bucket Sort recursivamente, dependendo da complexidade dos dados dentro do balde.
4. **Concatenação:** Finalmente, os elementos dos baldes são concatenados na ordem dos baldes para formar o array final ordenado.

## 3. Complexidade do Bucket Sort

A complexidade do Bucket Sort depende de alguns fatores:

*   **Algoritmo de ordenação usado dentro dos baldes:** Se um algoritmo eficiente como o Insertion Sort for usado para pequenos baldes, a complexidade pode ser otimizada.
*   **Número de baldes:** Um número adequado de baldes é crucial para a performance.
*   **Distribuição dos dados de entrada:** O Bucket Sort tem seu melhor desempenho quando os dados são uniformemente distribuídos.

### Complexidade de Tempo:

*   **Melhor Caso:** O(n + k), onde 'n' é o número de elementos e 'k' é o número de baldes. Isso ocorre quando os elementos são distribuídos uniformemente e a ordenação dentro dos baldes é rápida.
*   **Caso Médio:** O(n + k).
*   **Pior Caso:** O(n^2). Isso pode acontecer se todos os elementos caírem no mesmo balde, transformando o problema em uma ordenação de um único balde grande, onde a complexidade do algoritmo de ordenação interno domina.

### Complexidade de Espaço:

*   **O(n + k):** Requer espaço adicional para armazenar os baldes e os elementos dentro deles.

## 4. Casos de Uso do Bucket Sort

O Bucket Sort é particularmente útil em cenários onde:

*   Os dados de entrada são uniformemente distribuídos em um determinado intervalo.
*   A faixa de valores dos elementos é conhecida ou pode ser facilmente determinada.
*   A eficiência é crítica e a distribuição dos dados permite um bom desempenho.

Exemplos de aplicações:

*   Ordenação de números de ponto flutuante.
*   Ordenação de dados com uma distribuição conhecida, como notas de alunos (0-100).
*   Processamento de grandes volumes de dados onde a distribuição uniforme pode ser explorada para paralelização.



## 5. Implementação em Python

A seguir, um exemplo de implementação do algoritmo Bucket Sort em Python:

```python
def bucket_sort(arr):
    # Encontra o valor máximo no array para determinar o número de baldes
    max_val = max(arr)
    size = max_val / len(arr)

    buckets = [[] for _ in range(len(arr))]

    # Distribui os elementos nos baldes
    for i in range(len(arr)):
        j = int(arr[i] / size)
        if j != len(arr):
            buckets[j].append(arr[i])
        else:
            buckets[len(arr) - 1].append(arr[i])

    # Ordena os elementos dentro de cada balde e concatena
    sorted_arr = []
    for i in range(len(arr)):
        # Usando Insertion Sort para ordenar os baldes
        buckets[i].sort()  # Python's sort é Timsort, eficiente para pequenos arrays
        sorted_arr.extend(buckets[i])

    return sorted_arr

# Exemplo de uso:
if __name__ == "__main__":
    data = [0.42, 0.32, 0.33, 0.52, 0.37, 0.47, 0.51]
    print(f"Array original: {data}")
    sorted_data = bucket_sort(data)
    print(f"Array ordenado: {sorted_data}")

    data2 = [29, 13, 22, 37, 52, 49, 46, 71, 56]
    print(f"\nArray original: {data2}")
    sorted_data2 = bucket_sort(data2)
    print(f"Array ordenado: {sorted_data2}")
```

