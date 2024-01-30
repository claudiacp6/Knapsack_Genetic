# Knapsack_Genetic
Resolução do 'Knapsack Problem' com algoritmo genético

**Algoritmo Genético**:
1. Codifica um algoritmo capaz de fazer uma procura pelo ótimo global.

   1.1 Função ´create_ksp´
   1.2 Função initialize_population
   1.3 Função evaluate_population
   1.4 Função select_parents
   1.5 Função crossover
   1.6 Função mutate
   1.7 Função genetic_algorithm
   
2. Explica a escolha de representação do cromossoma, e a maneira como as duas operações de reprodução foram codificadas:
    * mutação
    * cross-over
      
A representação do cromossomo em algoritmos genéticos é uma escolha crucial, pois afeta diretamente como a informação genética é manipulada durante as operações genéticas, como crossover (cruzamento) e mutação. No contexto do Problema da Mochila (Knapsack Problem), em que você está tentando encontrar uma combinação de itens que maximize o valor total sem exceder a capacidade da mochila, a representação do cromossomo pode ser binária.

Escolha da Representação do Cromossomo:
Para o Problema da Mochila, uma representação comum é usar um vetor binário, onde cada posição no vetor representa a presença (1) ou ausência (0) de um determinado item na mochila. Cada posição no vetor corresponde a um item específico.

Por exemplo, suponha que você tenha 5 itens e seu cromossomo seja representado como [1, 0, 1, 0, 1]. Isso significa que o primeiro, terceiro e quinto itens estão incluídos na mochila, enquanto o segundo e quarto itens não estão incluídos.

Operações de Reprodução Codificadas:

Mutação:

A mutação é a operação que introduz pequenas alterações aleatórias em um cromossomo. No contexto do Problema da Mochila, uma mutação pode envolver a troca do estado (presença ou ausência) de um item aleatório. Por exemplo, se o cromossomo original é [1, 0, 1, 0, 1], a mutação poderia gerar algo como [0, 0, 1, 0, 1].

Crossover (Cruzamento):

O crossover é a operação que combina informações genéticas de dois pais para gerar descendentes. No contexto binário, o ponto de crossover é geralmente escolhido aleatoriamente. Um exemplo de crossover poderia ser:
Pai 1: [1, 0, 1, 0, 1]
Pai 2: [0, 1, 0, 1, 0]
Ponto de Crossover: 2 (por exemplo)
Descendente: [1, 1, 0, 1, 0]

Essas operações visam explorar diferentes combinações de itens para encontrar soluções melhores. A escolha da representação binária permite uma manipulação direta e intuitiva dos cromossomos em operações como crossover e mutação, facilitando a busca por soluções ótimas para o Problema da Mochila.

4. O que acontece se o item adicionado for aquele que tiver um rácio de utilidade e peso maior em todas as iterações? A solução final com este método é melhor que a solução original?

   Se, em todas as iterações do algoritmo genético, o item adicionado for aquele que tem o maior rácio de utilidade para peso, é provável que a solução final seja melhor que a solução original em termos de valor total.

   O motivo é que o rácio de utilidade para peso representa efetivamente o "retorno do investimento" de cada item em termos de valor obtido por unidade de peso. Selecionar itens com maiores rácios significa escolher itens que proporcionam mais valor relativo ao seu peso.

  Ao longo das iterações, se o algoritmo genético está favorecendo consistentemente a inclusão de itens com maiores rácios de utilidade para peso, a mochila estará sendo preenchida com itens que oferecem um equilíbrio mais favorável entre valor e peso. Isso geralmente resultará em uma solução que tem um valor total maior em comparação com a solução original.

  Entretanto, é importante notar que a eficácia do algoritmo depende de vários fatores, como a representação do cromossomo, as operações genéticas específicas e os parâmetros do algoritmo. Além disso, o Problema da Mochila é NP-difícil, o que significa que encontrar a solução ótima em tempo polinomial para todos os casos não é garantido. O algoritmo genético pode encontrar boas soluções aproximadas, mas pode não garantir a solução ótima em todos os cenários.
   
