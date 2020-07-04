---
title: Administrando um Restaurante
lang: pt-BR
ref: admin-restaurant
parent: Guia do Restaurante
nav_order: 2
---

# Administrando um Restaurante

As páginas de administração de restaurante são apresentadas em abas no canto superior direito da página do restaurante.

![Restaurante]({{ "/assets/images/restaurant_detail_fr.png" | absolute_url }})

- [Produtos](#Produtos)
- [Opções](#Opções-e-extras--Colocando-extras)
- [Menus](#Menus)
- [Pedidos](#Pedidos)
- [Agenda](#Agenda)


### Produtos

A lista de produtos permite que você registre diferentes produtos que o restaurante entrega. O restaurante deve criar os pratos que produz e deixá-los disponíveis na plataforma:
- nome do produto
- descrição
- se o produto está ativo ou indisponível
- o preço e os impostos incidentes
- os alergenos (Atenção: o restaurante é responsável pela informação dada ao consumidor)
- as dietas em que o produto se enquadra (por exemplo: vegetariana, vegana, sem lactose etc.)

### Opções e extras / Colocando extras

Um produto pode ter várias opções associadas (veja abaixo), que precisam ser criadas com antecedência. Por exemplo a opção de ketchup, maionese, ou molhos para uma porção de fritas.

As opções permitem deixar os produtos configuráveis. Eles permitem por exemplo inserir adicionais, ou escolher outros itens do menu (acompanhamentos, bebidas). Um adicional é uma lista de produtos associados ao produto no menu.

![Opção]({{ "/assets/images/option_fr.png" | absolute_url }})

Essa lista tem as seguintes características:
- Nome
- Método de cálculo do preço
  - Grátis, sem custo no adicional
  - Preço fixo pra qualquer escolha, o preço é o mesmo independente do adicional escolhido
  - Preço dependendo da escolha, o preço varia de acordo com o adicional escolhido
- Checkbox: o adicional é obrigatório?
  - Se for, o ciente é obrigado a escolher uma opção
  - Se não for, significa que você pode:
    - Deixar o valor mínimo 0, que significa que o ciente não tem que escolher uma opção.
    - Deixar o valor máximo em X, deixando a possibilidade do cliente escolher várias opções. (ex: escolher ketchup E maionese como opção de molho, ex2: escolher batata frita (+R$10,00), onion rings (+R$15,00) e queijo extra (+R$3,00) com um hamburguer)

Você deve primeiro criar os adicionais necessários na aba específica usando o botão "adicionar" antes de associar eles a algum produto.
Para associar um adicional a um produto, é só ativar ele num produto do seu restaurante. Vá para a aba "produto" do seu restaurante, e clique no botão "modificar" do produto escolhido.
No fim das opções de cada produto você encontra os adicionais que você tinha criado. É só selecionar o ou os que você escolher.

### Menus

Cada restaurante pode administrar independentemente seu menu. Restaurantes têm a possibilidade de criar vários menus e ativar o que corresponde ao que vai ser usado naquele momento.

![Menu]({{ "/assets/images/menus_fr.png" | absolute_url }})

#### Criando um menu

Na aba "Menus" você pode criar quantos menus quiser e forem necessários. Isso permite que os menus sejam configurados previamente e facilmente serem ativados na hora certa.

Menus se referem aos produtos que o restaurante trabalha em cada momento. Por exemplo: Almoço, jantar, dias de semana, finais de semana, verão, inverno, dia dos namorados, semanas intercaladas...

Para criar um menu, aperte o botão de "Adicionar". Aí simplesmente indique o nome do menu e aperte "salvar". Seu menu está pronto para ser configurado! Você pode ativar o menu clicando no botão "Ativar". O menu é sinalizado como ativado por um sinal de "check" a lado do seu nome.

#### Adicionando uma seção ao menu

Para configurar seu menu, você deve primeiro adicionar uma ou mais seções de menu. Por exemplo: entrada, prato principal, sobremesa. As seções também podem ser coisas como "especiais da casa" e "Pratos Feitos"... Para fazer isso, digite o nome da seção que você deseja criar e clique em "Adicionar uma seção".

É mais fácil criar todos os produtos de uma seção e associá-los diretamente na seção correta. (especialmente se você tiver uma grande lista de produtos), em vez de criar todos eles e arrastá-los para as seções corretas.

#### Configurando um menu

Use o editor de menus para compor adicionar ou remover produtos do menu, arrastando-os - veja abaixo como criar um produto. Para disponibilizá-los para venda, basta arrastar e soltar os produtos nas seções à esquerda. Se você deseja retirar um produto da venda, solte-o na seção "Produtos", à direita.

Não se esqueça de clicar no botão "Salvar alterações" na parte inferior da página.


### Pedidos

Todos os pedidos de um restaurante estão disponíveis na guia "pedido" do restaurante. Eles estão listados no painel do lado esquerdo por data de realização. Um pedido tem um identificador exclusivo, um status (novo, validado, pronto, cancelado), uma data de preparação com uma programação, um resumo e um preço incluindo impostos. Clique em um pedido presente na lista para exibir suas informações.

No painel do lado direito, são exibidas as informações do comando selecionado. Os pratos estão listados lá, bem como o cálculo dos impostos. Por fim, os botões permitem que o restaurante/administrador aceite ou recuse o pedido. Depois de indicar "aceito", o restaurante deve indicar que o pedido está pronto. Ele ainda pode, nesta fase, cancelar o pedido. Depois que o pedido for notificado como pronto, não será mais possível cancelar um pedido.

Você também pode ativar o 'modo lotado' nesta página. O modo lotado multiplica por 2 o tempo de preparação que você configurou no "modo normal"

### Agenda
### Programando horários de funcionamento / fechando um restaurante

Esse recurso permite fechar temporariamente um restaurante. Os fechamentos programados são visíveis no calendário.

### Comportamento do horário de funcionamento

Esse recurso permite determinar como o cliente pode escolher o horário da entrega. "O mais rápido possível" só permitirá que ela faça o pedido no primeiro horário disponível. "Programado" permitirá que ela determine um horário com antecedência para a entrega.

### Antecedência adicional antes de fazer o pedido

Esse recurso permite forçar os clientes a fazerem pedidos com antecedência mínimo. Por exemplo, se você deseja que os clientes façam pedidos pelo menos um dia antes da abertura do restaurante, você pode escolher 1 dia e 0 horas.

### Número de opções de envio (em dias)

Este parâmetro determina os dias máximos de antecedência para solicitar uma entrega.
