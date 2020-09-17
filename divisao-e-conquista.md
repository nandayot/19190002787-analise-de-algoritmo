---
description: >-
  Aprederemos sobre segmento de soma máxima, método da substituição, método da
  árvore de recursão, método mestre
---

# Divisão e conquista

## Merge Sort

Anteriormente vimos que o algoritmo Merge Sort é um exemplo que utiliza a técnica de divisão-e-conquista. Onde ele **divide** o problema em subproblemas, **conquista** \(soluciona\) cada subproblmea e depois **combina** as soluções em um só.

## Recorrências

Recorrências estão intrinsicamente ligadas ao método de divisão-e-conquista pois elas são uma forma de caracterizar o tempo de execução de algoritmos recursivos. 

**Recorrências** são inequações que descrevem funções sobre os seus termos menores. Como é o caso da demonstração da função da quantidade de movimentos que você realiza para completar a Torre de Hanói.

## Motivação

Imagina por exemplo uma grandeza que varia de acordo com o tempo. Ora cresce, ora descresce. Tomamos como exemplo, ações na bolsa de valores. Dependendo do dia a ação pode valorizar ou desvalorizar. Temos que encontrar um determinando intervalor em que essa grandeza acumulada seja máxima. Esse é um problema bastante conhecido chamado _**problema da soma-máxima**_. E para resolvermos precisamos saber alguns **conceitos**.

* um **segmento** de um vetor A\[p..r\] é qualquer subvetor da forma A\[i..k\], com $$p \leq i \leq k \leq r$$ 
* a **soma** de um segmento A\[i..k\] é o valor $$A[i]+A[i+1]+···A[k]$$ 
* a **solidez** de um vetor A\[p..r\] é a soma de um segmento de soma máxima

## Problema computacional

### Problema do segmento de soma máxima

Dado um vetor $$A[p..r]$$ de números inteiros, com $$r−p+1 > 1$$ , calcular a solidez de $$A[p..r]$$ .

## Continua...

> Conteúdo tirado dos slides do professor da disciplina **Fábio Henrique Viduani Martinez** - FACOM/UFMS; Todos os créditos reservados a ele.

