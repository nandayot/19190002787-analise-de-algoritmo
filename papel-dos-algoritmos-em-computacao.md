---
description: >-
  Nesta seção vamos entender como os algoritmos funcionam no meio da computação,
  alguns exemplos e problemas.
---

# Papel dos algoritmos em Computação

## Definição Inicial

O que é um Algoritmo? Um algoritmo é um processo computacionalmente bem definido que recebe um conjunto de valores como entrada e produz um conjunto de valores como saída.

Um algoritmo é uma ferramenta para solucionar um problema computacional bem definido

## Ordenação

### Problema da Ordenação

**Entrada**: uma sequência de $$n$$ números \( $$a_1, a_2, . . . , a_n$$ \)

**Saída**: uma permutação \( $$a'_1, a'_2, . . . , a'_n$$ \) da sequência de entrada de tal forma que a $$a'_1 \leq a'_2 \leq . . . \leq a'_n$$ 

Os problemas descritos na disciplina seguem essa característica de entrada e saída de um algoritmo qualquer.

A sequencia de entrada também pode ser chamada de **instância** e uma instância de um problema consiste da entrada necessária para computar a solução do problema.

### Qual o melhor?

Ao nos depararmos com um problema de ordenação, temos diversos algoritmos conhecidos que resolvem o problema. Algoritmos iterativos e recursivos em que cada um possui sua técnica associada. Diante disto, como podemos classificar o qual é o melhor?

Isto depende muito da aplicação e do usuário do algoritmo. Podemos escolher com base no processador/memória do computador do usuário ou também com base nos elementos de entrada que serão apresentados.

## Correção

Como podemos classificar um algoritmo como **correto**? Dizemos que ele está correto se ele para, para toda entrada, e devolve a resposta correta para esta entrada. Analogamente, um algoritmo está **incorreto** se ele não para e não devolve a resposta correta \(fica em estado de _loop infinito_\). Ele também pode continuar sendo incorreto caso pare com uma resposta errada.

## Exemplos de problemas computacionais

### Tipos de problemas que podem ser resolvidos com algoritmos

* **Projeto Genoma Humano**: sequenciamento do genoma humano, determinação dos genes do DNA, etc;
* Internet: acesso rápido e recuperação, gerenciamento e manipulação de grandes quantidades de informação, etc;
* Comércio eletrônico: manutenção de informações sigilosas, etc;
* Empresas e indústrias: otimização de recursos e lucros, etc;
* entre outros...

##  Organização da Informação

### Estruturas de Dados

Nesta disciplina vamos trabalhar com diversas estruturas de dados que já estudados na disciplina de Estruturas de Dados. Não é possível utilizar somente uma estrutura então utilizaremos diversas que já sabemos suas características, limitações e complexidade.

## Algoritmos eficientes vs Problemas Intratáveis

Algoritmos estudados dentro do curso são na maioria das vezes resolvíveis. Pode ser complexo ou não mas conseguimos resolver eficientemente. Porém existem problemas que até hoje não somos capazes de resolver de maneira eficiente, e esses problema são conhecidos como **NP-completos** que vai ser melhor abordado no final da disciplina.

## Computadores atuais e futuros

As vezes temos problemas de memória e processamento de alguns algoritmos complexos que muitas vezes achamos que o problema está no computador que não possui um hardware capacitado. Isso é verdade num certo parâmetro mas não podemos ficar restritos somente a isto.

Temos de pensar no aumento da complexidade de um algoritmo. E se o numero de entradas for enormemente grande? E se for infinitamente maior?

Nesse caso teríamos um computador infinitamente rápido e uma memória infinitamente grande? Não, isso é impossível. Computadores futuro podem ser sim muito rápidos mas o custo existe.

Ou seja, tempo e espaço computacional são recursos limitados. Não tem jeito.

## Eficiência de Algoritmos

Para um problema, como o de Ordenação, existem diversos algoritmos que o resolvem e cada um tem uma eficiência diferente que não é somente por questões de hardware/software.

Peguemos de exemplo a **ordenação por inserção** \(Insertion Sort\) e a **ordenação por intercalação** \(Merge Sort\).

O Insertion Sort é resolvido sem recursão e o tempo de execução é $$c_1 n^2$$ onde $$n$$ é o número de entrada e $$c_1$$ uma constante que não depende de $$n$$. Essa função depende do número de entrada e é uma função quadrática que aumenta quadraticamente conforme o número de entrada.

Já o Merge Sort o tempo de execução  é $$c_2 nlg_2n$$ que por ser uma algoritmo recursivo a função sofre uma redução no tempo se comparado ao Insertion Sort pois o algoritmo não percorre toda a entrada.

## Comparação de algoritmos

Vamos supor um exemplo em que beneficiamos o Insertion Sort. Ou seja, imagine que um computador **A** muito rápido esteja o executando e o computador **B** muito lento esteja executando o Merge Sort. E suponha que tenhamos um milhão de números. \(1.000.000\).

Suponha que o computador A seja 100 vezes mais rápido. Onde ele executa 1 bilhão de instruções por segundo e o computador B execute 10 milhões.

Agora imaginemos que um dos melhores programadores do mundo desenvolveu um programa para a ordenação por inserção, em que o tempo foi $$ 2 n^ 2 $$. A ordenação por intercalação, no entanto, foi implementada por um programador mediano em uma linguagem de programação que possui um compilador ineficiente, e o tempo foi $$50 n lg_2 n$$ .

Agora vamos avaliar o tempo de execução com a entrada mencionada em cada algoritmo.

#### Computador A

### $$\frac{2 · (10^6)^2 \text{ instruções}}{109 \text{ instruções por segundo}} = 2000 \text{ segundos}$$ 

#### Computador B

### $$\frac{50 · 10^6 lg 10^6 \text{ instruções}}{10^7 \text{ instruções por segundo}} \thickapprox  100 \text{ segundos}$$

Mesmo com um compilador ruim o computador B consegue ser 20 vezes mais rápido que o computador A.

![Gr&#xE1;fico retirado dos slides do professor. Cr&#xE9;ditos a ele.](.gitbook/assets/comparacao%20%281%29.png)

Matematicamente falando, a função do Merge Sort, ao longo que o número de elementos cresce, o crescimento de uma logarítmica é bem menor que o crescimento de funções quadráticas.

## Pesquisa em algoritmos

Estudar estruturas de dados e entender como algoritmos funcionam é fundamental para se destacar no meio da computação. Entender a complexidade, eficiência e limitações de algoritmos é um diferencial para conseguir trazer soluções mais robustas para algum problema de mercado.

> Conteúdo tirado dos slides do professor da disciplina **Fábio Henrique Viduani Martinez** - FACOM/UFMS; Todos os créditos reservados a ele.

