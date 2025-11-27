# Big-O, Estruturas de Dados e Algoritmos

Repositório dedicado ao estudo de Big-O, algoritmos e estruturas de dados, com exemplos práticos e análises de complexidade.

---

## Big-O

![Big-O Graph](img/big-o_graph.jpg)

A Notação Big-O (O) é a principal métrica para descrever a complexidade (desempenho) de um algoritmo em função do tamanho da entrada (n). Ela mede como o tempo de execução ou o espaço de memória requerido pelo algoritmo cresce à medida que o tamanho da entrada aumenta, focando no pior caso.

---

| Notação Big-O | Nome               | Descrição                                                                                   | Exemplo Comum                                                |
|---------------|--------------------|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| O(1)          | Tempo Constante    | O tempo de execução não muda com o tamanho da entrada.                                        | Acessar um elemento por índice em um array.                  |
| O(log n)      | Tempo Logarítmico  | O tempo de execução se reduz pela metade a cada passo. Muito rápido.                          | Busca Binária (Binary Search).                               |
| O(n)          | Tempo Linear       | O tempo de execução cresce proporcionalmente ao tamanho da entrada.                           | Iterar uma lista/array uma vez.                              |
| O(n log n)    | Tempo Linearítmico | Comum em algoritmos de ordenação eficientes.                                                   | Merge Sort, Heap Sort.                                       |
| O(n²)         | Tempo Quadrático   | O tempo cresce com o quadrado do tamanho da entrada. Normalmente loops aninhados.             | Bubble Sort, comparar pares em um array.                     |
| O(2ⁿ)         | Tempo Exponencial  | O tempo dobra a cada nova unidade da entrada. Muito lento.                                     | Fibonacci com recursão ingênua.                              |
| O(n!)         | Tempo Fatorial     | Crescimento absurdo (permutações). Inviável para entradas maiores que 10–20.                  | Traveling Salesman por força bruta.                          |

---

### Complexidade - O(1) Tempo Constante

A complexidade de tempo O(1) (Tempo Constante) é a mais eficiente em termos de Big-O. Ela significa que o tempo de execução de um algoritmo ou de uma operação não muda em relação ao tamanho da entrada (n).Independentemente se você está trabalhando com 1 item, 1.000 itens ou 1 bilhão de itens, a operação levará essencialmente o mesmo tempo.

#### Exemplos de Uso:

> [Ruby O(1)](ruby/exe_o(1).rb)

> [Javascript O(1)](javascript/exe_o(1).js)

---

### Complexidade - O(log n) Tempo Logarítmico

O Tempo Logarítmico, representado como O(log n), descreve um algoritmo cuja eficiência de execução (o tempo que ele leva) cresce de forma muito lenta conforme o tamanho da entrada (n) aumenta. É muito mais rápido do que o tempo linear O(n).

A chave do tempo logarítmico é o conceito de dividir para conquistar. Em cada passo ou iteração, o algoritmo consegue descartar uma grande porção dos dados de entrada, geralmente metade deles. Isso significa que, para dobrar o tamanho da entrada, você só precisa de uma operação extra para processar os dados.

#### Exemplo Clássico:

O exemplo mais comum de um algoritmo com complexidade O(log n) é a **Busca Binária** (Binary Search).

1. **Pré-requisito:**  A Busca Binária só funciona em listas ou arrays que já estão ordenados.

2. **Mecanismo:**  Para encontrar um item em uma lista ordenada, o algoritmo não verifica elemento por elemento (isso seria O(n)). Em vez disso, ele:

- **Verifica o elemento do meio** da lista.
  
- Compara o valor do meio com o valor que está procurando.
  
- Se o valor do meio for menor, ele sabe que o item desejado deve estar na **metade superior** da lista e **descarta toda a metade inferior.**

3. **Resultado:**  Em cada passo, o espaço de busca é **reduzido pela metade.** É por isso que a eficiência é logarítmica (na base 2, log_2 n).

#### Exemplos de Uso:

> [Ruby O(log n)](ruby/tempo_logaritmico.rb)

> [Javascript O(log n)](javascript/tempo_logaritmico.js)