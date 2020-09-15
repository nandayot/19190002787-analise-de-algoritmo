# Crescimento de funções

## Ordem de Crescimento

Retomando a aula passada, estudamos a taxa de crescimento de funções do tempo de execução de algoritmos, ou ordem de crescimento para avaliar a sua eficiência. Essa ordem também permite realizar a comparação com outros algoritmos relativos.

Geralmente estudamos algoritmos levando em conta o crescimento ao infinito do número de entrada. Assim, os coeficientes e termos de menor ordem da função não causam grande impacto no tempo de execução e para isso eles são descartados para fins de simplificação. Desse modo, estudamos a eficiência assintótica dos algoritmos.

## Notação $$\Theta$$ 

Essa é uma das informações mais essenciais do curso de Análise de Algoritmos. E entendo-a é possível entender outras notações.

Com base na definição do livro do Cormen:

Dada uma função $$g(n)$$ , denotamos $$\Theta (g(n))$$ o conjunto de funções:

$$\Theta (g(n))$$ = {$$f(n)$$: existem constantes positivas $$c_1$$ , $$c_2$$e $$n_0$$tais que $$0 \leq c_1g(n) \leq f(n) \leq c_2g(n)$$ para todo $$n > n_0$$ }.

$$g(n)$$é assintoticamente justo para $$f(n)$$ se $$f(n) \in g(n)$$e toda $$f(n) \in g(n)$$é assintoticamente não negativa por definição, sendo assim, $$g(n)$$também é.

## O que fazemos agora?

Vemos o que é a definição dessa notação mas e agora? Podemos provar, por meio dessa definição que algumas funções pertences a outras. Como o exemplo abaixo:

### Como mostrar que $$\frac{1}{2}n^2 −3n = \Theta(n^2)$$ ?

Basta mostrarmos que existem constantes positivias c1 e c2 que satisfazem a inequação:

$$
0 \leq c_1n^2 \leq \frac{1}{2}n^2 −3n \leq c_2n^2
$$

para todo $$n \geq n_0$$ 

### Prova

![](.gitbook/assets/primeiroex.jpg)

Para substituir a expressão $$f(n) \in g(n)$$, usualmente escrevemos que $$f(n) \in g(n)$$.

Em geral podemos utilizar essa lógica para qualquer polinômio $$ p(n) = \sum_{i=0}^{d} a_in^i$$ . Ou seja, para constantes $$a_i$$ constantes e $$a_d > 0$$ , temos que $$p(n) = \Theta(n^d)$$ .

Consequentemente é verdade que $$\Theta(n^0) = \Theta(1)$$ para funções constantes.

## Notação $$O$$ 

## Continua...

> Conteúdo tirado dos slides do professor da disciplina **Fábio Henrique Viduani Martinez** - FACOM/UFMS; Todos os créditos reservados a ele.

