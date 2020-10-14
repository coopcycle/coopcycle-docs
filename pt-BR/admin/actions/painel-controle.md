---
title: Painel de Controle
lang: pt-BR
ref: dispatch
parent: Logística
grand_parent: Guia do Administrador
nav_order: 1
custom_scripts:
  - "https://cdnjs.cloudflare.com/ajax/libs/jquery-zoom/1.7.21/jquery.zoom.min.js"
  - "/assets/scripts/zoom.js"
---

# Painel de Controle

O painel de controle (chamado painel neste documento) permite controlar todas as funções para criar e gerenciar tarefas, bem como gerenciar o envio de encomendas manualmente. É possível exibi-lo em tela cheia clicando no botão

<span class = "zoomable">! [Painel] (/assets/images/dashboard_fr.png) </span>

## Criar, atribuir e editar uma tarefa

Uma tarefa é criada clicando no botão <i class = "fa fa-plus fa-lg" aria-hidden = "true"> </i> na seção 'Não atribuído' do painel. Um pop-up é aberto e permite que você configure a tarefa. Três ações são possíveis para uma tarefa:
- Adicionar, que permite criar uma tarefa
- Editar, que permite alterar ou verificar o status e o histórico de uma tarefa
- Concluir a tarefa, que permite a alteração do status da tarefa:
- A Realizar
- Sucesso
- Falha

Enquanto uma tarefa não for atribuída a um mensageiro, esta permanecerá na seção "Não atribuído".

## Adicionar/criar uma tarefa

As seguintes informações estão disponíveis para criar uma tarefa:

* Caixa de seleção: tipo de tarefa
  - Pegar
  - Recusar

* Campo: endereço do ponto de entrega ou retirada

* '+': mais opções
  - Campo: código postal (preenchimento automático)
  - Campo: Cidade (preenchimento automático)
  - Campo: Piso
  - Campo: instruções

Dropdown: Conquistas
  - Data de início
  - Data final
* Dropdown: escolha uma tag

## Editar uma tarefa

As mesmas informações que "adicionar" estão disponíveis para edição. Além disso, é possível:
* Dropdown: Atribuir um mensageiro
* Dropdown: Veja o histórico

## Concluir uma tarefa

Para concluir uma tarefa, basta clicar no botão "Concluir tarefa" no canto superior direito da janela pop-up. Os recursos disponíveis são:
* Menu suspenso: "pendente", "falhou", "sucesso"
* Campo: comentário sobre a conclusão da tarefa

## Veja o mensageiro conectado no painel

Quando um mensageiro se conecta ao aplicativo e sua localização é ativada, um marcador indicando sua posição é exibido no painel.

## Adicione um mensageiro à seção Designado.

Adicionar um mensageiro à agenda significa que ele está disponível para ser designado para tarefas e, portanto, para entregar pedidos. Para adicionar um mensageiro à agenda, clique no botão '+' na seção 'Designado'.

Atribuir uma tarefa a um mensageiro.

Se for possível atribuir um mensageiro a uma tarefa no pop-up para criar ou editar uma tarefa, é muito mais conveniente usar a função arrastar e soltar do painel: solte a tarefa diretamente na área de atribuição de mensageiros.

## Criar tarefa

A tarefa aparece na seção 'Não atribuído'.
O expeditor move a tarefa para um mensageiro adicionado anteriormente à programação.

## Obter informações de um pedido

Assim que duas tarefas são atribuídas a um mensageiro, uma entrega é criada. Várias informações estão disponíveis:
* Duração estimada de entrega;
* A distância a ser percorrida (em relação à rota) (botão "Mapa": mostra/oculta a rota de entrega, que é a rota proposta ao mensageiro para entrega)

## Atribuir tarefas a um mensageiro considerando a otimização

O expedidor pode otimizar a rota de entrega do mensageiro movendo as corridas na pilha de tarefas atribuídas a este último. Em ordem, o primeiro da pilha será o primeiro ponto de rota levado em consideração e assim por diante até o final da pilha.
O expedidor pode mover as tarefas na pilha para reorganizá-las.

## Crie uma etiqueta e uma tarefa

Etiquetas são valores que podem ser atribuídos a uma tarefa para classificá-los no painel. Uma etiqueta é composta por um título e uma cor. Para atribuir uma marca a uma tarefa, você deve primeiro criar as marcas necessárias ao expedidor.
* Vá para o painel de configuração, seção "Etiqueta";
* Crie uma etiqueta clicando no botão "Criar uma nova etiqueta";
* Dê um nome e uma cor à etiqueta;
* Valide.

No painel, o expedidor encontrará as etiquetas criando uma tarefa ou editando-a.
* Clique no botão "Adicionar uma etiqueta" (roda dentada);
* Adicione a etiqueta;
É possível atribuir várias etiquetas a uma tarefa.

## Manipular os diferentes filtros

Filtros diferentes são aplicáveis ​​para exibir apenas determinadas tarefas. É possível filtrar por:
* Status da tarefa:
* Tarefas concluídas
* Tarefas sem marcação
* Por etiqueta

É possível combinar os filtros.

## Calendário suspenso: altere a data

Para alterar o dia, basta usar o calendário suspenso à esquerda da barra superior do painel.

## Importar tarefas de um arquivo CSV

Para evitar a criação manual de um grande número de tarefas, é possível importá-las em massa por meio de um arquivo CSV. No painel, clique no botão 'Importar': uma janela é aberta para permitir o upload de um arquivo. Você deve pelo menos especificar um endereço para cada tarefa, as outras colunas são opcionais. Para importar um arquivo, clique no botão 'Importar' localizado na barra superior do painel.

As colunas antes e depois para especificar o intervalo de tempo aceitam valores em diferentes formatos. Aqui estão os valores das colunas acompanhados de um exemplo:
- tipo
- endereço.nome
- endereço.telefone
- endereço
- adress.floor
- descrição de endereço
- depois de
- antes
- comentários
- etiqueta

Você pode baixar um [arquivo de amostra] (https://demo.coopcycle.org/help/tasks_import.example.en.csv).

## Exportar tarefas em um arquivo CSV

A exportação é mais eficiente .csv mostra os comandos do seu dia a partir do link 'Exportar' situado na barra superior do painel.