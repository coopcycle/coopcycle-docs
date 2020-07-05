---
title: Preços
lang: pt-BR
ref: pricings
parent: Logística
grand_parent: Guia do Administrador
nav_order: 2
---

# Precificação

Como parte da criação de uma conta da loja, é possível criar preços (por exemplo, preços expressos, preços normais) a partir da seção de administração, clicando no ícone e na seção Preços.

[screenshot]

O preço é configurado no painel de administração por meio de um conjunto de regras com base nas seguintes variáveis:
A distância que é medida em metros. Essa distância pode ser definida com os operadores de:
- &gt; maior que *variável em metros*
- &lt; menor que *variável em metros*
entre duas variáveis

O peso que é avaliado em gramas. Esse peso pode ser definido com os mesmos operadores que a distância. 
A zona definida ao carregar um arquivo GeoJSON na configuração da instância;
O tipo de bicicleta que é definido selecionando-o em uma lista na qual estão disponíveis:
A bicicleta simples
A bicicleta cargueira

[screenshot]

Essas regras são organizadas como uma pilha em ordem de processamento; o preço no topo da lista será o primeiro a ser processado pelo software, que verificará se ele corresponde às características da entrega; não é o caso do software ir para o segundo preço na lista e assim por diante. Com cada entrega criada, essa pilha será usada para criar o preço. A escolha é feita automaticamente de acordo com os critérios especificados para cada entrega.

Por exemplo, eu crio uma regra que especifica um preço:
- no departamento 93 com bicicleta cargueira colocada no topo da pilha;
- em Paris intramural com bicicleta cargueira colocada no meio da pilha;
- na Paris intramural colocada no fundo da pilha.

Se uma entrega for criada envolvendo uma série de tarefas em Paris intramurais com uma única bicicleta, a primeira regra será ignorada e a segunda será usada como base de entrega. As regras precisas (ou seja, com a maioria das variáveis) devem estar no topo da pilha e as mais gerais na parte inferior da pilha, para que casos especiais sejam selecionados pelo software como base de preço. . Se, por exemplo, elevar minha lista de preços da seguinte forma:
em Paris intramural;
em Paris intramural com bicicleta cargueira;
no departamento de 93 com bicicleta cargueira.

Se uma entrega for criada para Paris intramural com uma bicicleta cargueira, a primeira regra será ignorada. O segundo corresponde à entrega, portanto seu preço será aplicado. A segunda regra sendo cumprida, a terceira é ignorada.

As regras mais precisas (ou seja, com o maior número de parâmetros) devem estar no topo da pilha e as regras mais gerais na parte inferior da pilha, para que os casos específicos sejam selecionados pelo software como base para o preço. Se, por exemplo, eu modificar os preços acima da seguinte maneira:

na Paris intramural;
na Paris intramural com bicicleta cargueira;
no departamento 93 com bicicleta cargueira.
Se uma entrega em Paris intramural for criada com a necessidade de entrega por bicicleta cargueira, o preço especificado para a primeira regra será aplicado, porque nenhum tipo de bicicleta é especificado para ela e a segunda será ignorada.
