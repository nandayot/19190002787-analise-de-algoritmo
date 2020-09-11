---
description: >-
  Visão geral da estrutura usada para projeto e análise dos algoritmos,
  divisão-e-conquista e ordenação por intercalação
---

# Introdução à Análise de Algoritmos

## Problema da Ordenação

Voltamos novamente para falar sobre o problema da ordenação. E nessa aula vamos analisar realmente o algoritmo de ordenação por inserção \(Insertion Sort\).

**Entrada**: uma sequência de $$n$$ números \( $$a_1, a_2, . . . , a_n$$ \)

**Saída**: uma permutação \( $$a'_1, a'_2, . . . , a'_n$$ \) da sequência de entrada de tal forma que a $$a'_1 \leq a'_2 \leq . . . \leq a'_n$$

## Algoritmo

{% tabs %}
{% tab title="Pseudocódigo" %}
```c
InsertionSort(A)
    para j ← 2 até A.length
        chave ← A[j]
        //insere A[j] na sequência ordenada A[1..j−1]
        i ← j−1
        enquanto i > 0 E A[i] > chave
            A[i+1] ← A[i]
            i ← i−1
        A[i+1] ← chave
```
{% endtab %}
{% endtabs %}

Veja o gif sobre o funcionamento [aqui](https://upload.wikimedia.org/wikipedia/commons/thumb/0/0f/Insertion-sort-example-300px.gif/220px-Insertion-sort-example-300px.gif).

## Correção do Algoritmo

### Invariantes e a correção do _Insertion Sort_

O índice j indica a posição atual para qual você está olhando. No início de cada iteração da estrutura de repetição para, o vetor consistindo dos elementos **A\[1..j−1\]** é o atual vetor ordenado até o momento da leitura do j. O restante do vetor **A\[j+1..n\]** são os elemento que ainda não foram analisados. Os elementos em **A\[1..j−1\]** são aqueles que originalmente estavam armazenados neste intervalo do vetor, mas agora estão ordenados.

Para algoritmos iterativos, aqueles que não possuem recursão e tem estruturas de repetição, conseguimos extrair propriedades para explicar que o algoritmo está correto por meio da indução.

A  propriedade do vetor **A\[1..j−1\]** pode ser descrita como um **invariante**: 

No começo de cada iteração da estrutura de repetição **para** das linhas 2–9, o vetor **A\[1..j−1\]** consiste dos elementos originalmente em **A\[1..j−1\]**, mas em ordem crescente.

### Propriedades do invariante

Para provar a correção de um algoritmo por meio do invariante precisamos mostrar 3 coisas.

#### Inicialização

Antes da estrutura de repetição do algoritmo começar, precisamos mostrar que o invariante associado a ela está correto. Seria a base da indução.

#### Manutenção

Depois temos que elaborar a Hipótese de Indução \(H.I\). Se o invariante é válido antes da inicialização, ele permanece verdadeiro antes da próxima iteração.

#### Término

Depois que a estrutura de repetição termina o invariante fornece uma informação importante que determina se está correto.

Agora vamos provar que o algoritmo está correto por meio do invariante utilizando estas propriedades.

1. **Inicialização**: Antes da primeira iteração temos que j=2, sendo assim, o vetor A\[1..j-1\] possui somente um elemento. Logo, o vetor já está ordenado. Isso conclui que o invariante está correto antes da primeira iteração.
2. **Manutenção**: Durante a execução da estrutura de repetição o algoritmo vai movimentar os elemento A\[j-1\], A\[j-2\] ... uma posição para direita até achar a posição correta para o A\[j\]. Quando este é inserido percebemos que o vetor A\[1..j\] foi rearranjado de tal forma que o elementos estejam ordenados. Assim, quando incrementamos o invariante, ele ainda permanece correto.
3. **Término**: A condição de parada da estrutura de repetição é $$ j > A.length = n$$ . Então na próxima iteração o j é j = n+1. Substituindo no invariante A\[1..j-1\] temos que A\[1..n\]. Ou seja, como mostrado na manutenção, esse vetor A\[1..n\] está rearranjado de maneira ordenada e ele é o vetor original completo que antes foi recebido como entrada desordenado mas agora foi rearranjado em ordem crescente. Logo, o algoritmo está correto.
4. Provamos que o algoritmo funciona para **qualquer** entrada n. 

## Continua...



> Conteúdo tirado dos slides do professor da disciplina **Fábio Henrique Viduani Martinez** - FACOM/UFMS; Todos os créditos reservados a ele.



