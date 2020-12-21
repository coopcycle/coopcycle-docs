---
lang: pt-BR
title: Administração de Entregas
ref: app-order-management
parent: App
nav_order: 3
---

# Gerenciamento de pedidos

## Encomendas

A tela principal está organizada da seguinte forma:

![interface do restaurante para pedidos] (/assets/images/resto_order_list_fr.png)

- **Por data (a data atual padrão):**
<br>
Também permite que você tenha um histórico de pedidos anteriores e futuros, selecionando a data através do calendário, clicando no botão a seguir
![botão de data] (/assets/images/resto_date_fr.png).

- **Por seção:**
- **Novos pedidos:**
<br>
Aqui você verá todos os novos pedidos de clientes aguardando validação.
<br>
Você também pode recusar, então você tem três opções:

- Estou fora de estoque
<br>
Este pedido será cancelado e você continuará recebendo novos pedidos.

- Estou no meio de uma corrida.
<br>
Este pedido será cancelado e você continuará recebendo novos pedidos.

- Eu vou fechar.
<br>
Este pedido será cancelado e você não receberá mais novos pedidos.

- **Pedidos aceitos:**
<br>
Aqui você pode ver todos os pedidos aceitos.
<br>
A partir desta etapa, se tudo correr bem, você só precisa preparar o pedido, aguardar o entregador e automaticamente o pedido será feito na seção abaixo [pedido entregue] (#entrega do pedido).
<br>
Caso contrário, você pode:

- Atraso no pedido:
- Em 10 minutos.
- 20 minutos.
- Em 30 minutos.
- Cancelar o pedido
- Cancelado pelo cliente
<br>
Este pedido será cancelado e você continuará recebendo novos pedidos.

- Estou fora de estoque
<br>
Este pedido será cancelado e você continuará recebendo novos pedidos.

- Estou no meio de uma corrida.
<br>
Este pedido será cancelado e você continuará recebendo novos pedidos.

- **Pedidos cancelados:**
<br>
Aqui está uma lista de todos os pedidos que foram cancelados.
- ** <span id = "order-delivery"> Pedidos entregues: </span> **
<br>
Aqui está uma lista de todos os pedidos que foram entregues.

Em cada uma das seções, os pedidos são representados por seu ID, o total do pedido e o tempo para começar a prepará-lo. Para acessar os detalhes do pedido e interagir com ele, basta clicar nele.

**Observe que você pode, a qualquer momento, pressionar o botão![Resfresh] (/assets/images/resto_refresh_btn_fr.png) atualizar a página para a data atual.**

<br>
<br>
<br>

---
<br>

## Configurações

### As configurações são acessadas através do ícone![Settings] (/assets/images/resto_param_icon.png) no canto superior direito da página. Eles são divididos em duas partes:

- **Mudar para o modo rápido:**
<br>
Quando o modo urgente é ativado, você não recebe mais pedidos; para continuar recebendo pedidos novamente, desative-o.

- **Gerenciar produtos:**
<br>
Nesta seção, você pode ver uma lista de todos os produtos que compõem seu catálogo e a capacidade de desativar cada um deles.
Os produtos desativados não são visíveis pelo cliente; isso pode ser útil se, por exemplo, você estiver sem estoque de um ingrediente essencial para preparar um prato.
Por padrão, todos os produtos estão habilitados.

<br>
<br>

---
<br>

## Restaurante de fechamento/reabertura on-line

Este botão![Ícone do botão liga/desliga] (/assets/images/resto_power_icon.png) permite que você exiba seu restaurante como fechado na interface do cliente, para que ele não possa mais fazer pedidos.
<br>
Para redefinir o restaurante para o status "aberto", basta clicar no botão Fechar![Ícone do botão Fechar] (/assets/images/resto_close_banner_icon.png) do banner abaixo que aparece após o fechamento do restaurante.
<br>
<br>
![restaurante está fechado] (/assets/images/resto_closed_banner_fr.png)
