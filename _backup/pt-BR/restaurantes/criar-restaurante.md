---
title: Criar um restaurante
lang: pt-BR
ref: creation-restaurant
parent: Guida do Restaurante
nav_order: 5
---

# Criar um restaurante

Entre em contato com uma cooperativa da CoopCycle. Somente um administrador pode criar um novo restaurante.

## Etapa 1: adicionar informações gerais

Agora você deve adicionar informações gerais sobre o seu restaurante. Algumas dessas informações podem ser editadas posteriormente com a conta do restaurante, mas outras, como os termos do contrato ou as opções, só podem ser acessadas com a conta do administrador. 4 guias devem estar completas:

- [Geral] (#Geral)
- [Opções] (#Opções)
- [Planejamento] (#Planejamento)
- [Contrato] (#Contrato)

### Geral

Nesta guia 'Geral', você pode modificar as informações gerais sobre o seu restaurante:

- Exibido aos clientes:
  - Nome do restaurante no CoopCycle
  - Tipo de negócios
  - Endereço
  - Descrição do seu restaurante
  - Redes Sociais
  
- Não exibido para clientes:
  - Site
  - Número de telefone
  - Informação de negócios
  
### Opções

4 opções devem ser decididas nesta guia:

- O restaurante é exclusivo, o que significa que ele só está disponível no CoopCycle.
- Restaurante é destaque na página inicial
- O restaurante também aceita preços fixoa (por exemplo: refeições)
- Ativar sistema de pagamento e reembolso

### Planejamento

#### Horários
Nesta página, você pode escolher entre dois tipos de atividades ou escolher os dois:
- Retirada, o que significa que o cliente vem ao restaurante para retirar seu pedido
- Entrega, o que significa que a cooperativa entrega o pedido ao cliente

Para cada atividade, você pode editar uma programação que determina quando os clientes podem receber seus pedidos ou comparecer ao restaurante.

Para cada programação, você deve escolher entre *O mais rápido possível* e *Horário marcado*:
- *Assim que possível*: o cliente recebe seu pedido o mais rápido possível. Em seu pedido, o cliente durante o pedido vê: "em XX minutos"
- *Horário marcado*: o cliente escolhe quando recebe o pedido. Em sua inscrição, o cliente durante o pedido vê: "Entre XX PM/AM e XX PM/AM"

Para cada agendamento, você deve escolher com o administrador se o proprietário do restaurante tem o direito de alterar esses agendamentos. Clique em "permitir edição", se for o caso.

#### Opções globais

- Definir um perímetro de entrega
- Defina, se necessário, uma antecedência ao fazer o pedido. Por exemplo, se você colocar 1 no campo 'dia', os clientes terão que pedir no dia anterior.
- Defina, se necessário, várias opções de remessa

### Contrato

Você encontrará nesta página **os termos do contrato** entre o coletivo de entrega local e o restaurante. Eles abrangem os seguintes aspectos:
- Preço de entrega :
    - Parte a ser paga pelo restaurante ("Valor cobrado pela plataforma" por um custo fixo e "Taxa da plataforma por entregas" por uma taxa proporcional). Também é possível criar sua própria regra de preço e aplicá-la nesta página. Consulte a documentação sobre preços no guia logística do administrador.
    - Parte a ser paga pelo cliente final ("Valor pago pelo cliente" por um custo fixo e "Taxas pagas pelo cliente" por uma taxa proporcional). Também é possível criar sua própria regra de preço e aplicá-la nesta página.
- Valor mínimo da cesta
- Taxas de plataforma para retirada no local.

## Etapa 2: vincular uma conta a um restaurante

### Crie uma conta ou convite

#### Método 1: crie sua conta
O proprietário do restaurante precisa criar uma conta no CoopCycle. Ele deve preencher as seguintes informações:

- O email
- Nome do usuário
- Senha
- Nome e sobrenome
- Número de telefone

Mantenha segredo seu nome de usuário e senha, você terá que usá-lo quando estiver usando o CoopCycle para gerenciar seu restaurante.

#### Método 2: convite

Neste segundo método, são os administradores que convidam você no CoopCycle.

Para fazer isso, os Administradores precisam clicar na guia 'usuários' na parte superior do painel do administrador. Nesta nova página, um botão azul "Convidar um usuário" permite que os administradores criem uma conta em nome de um usuário. Ele deve preencher os seguintes campos:
- Nome do usuário
- Email (da pessoa convidada)
- Nome e sobrenome
- O status da conta - Nesse caso, escolha *Restaurante* se você convidar o proprietário de um restaurante

No final, é o usuário quem escolherá sua senha, que é secreta.

### Adicionar uma função: dono de restaurante

Somente os administradores podem adicionar uma função na sua conta de *Restaurante*. Se você usou o *Método 2*, não precisa alterar o status da conta, porque sua conta já foi criada como *Restaurante*.

Se você usou o *Método 1*, deve seguir estas etapas:
- Os administradores clicam na guia 'usuários' na parte superior do painel do administrador.
- Os administradores pesquisam seu nome de usuário no campo 'busca' ou encontram na lista e clicam no botão verde 'editar'.
- Os administradores adicionam a você uma função *Restaurante* e clicam em 'salvar'

### Vincule uma conta a um ou mais restaurantes.

Somente administradores podem vincular uma conta a um restaurante. Na mesma página 'editar' de antes, preencha o campo 'adicionar um restaurante' com o nome do restaurante.

Após essa etapa, quando o proprietário do restaurante estiver se conectando ao CoopCycle com seu nome de usuário e senha, ele só terá acesso ao seu restaurante.

## Etapa 3: crie uma conta do Stripe e vincule-a ao seu restaurante

Sobre a criação da sua conta do Stripe, consulte [Guia do administrador/Stripe]{https://docs.coopcycle.org/pt-BR/admin/pagamentos-stripe.html}. As instruções são as mesmas para cooperativas e restaurantes. A única diferença é o que você faz a seguir com sua conta do Stripe.

Quando um restaurante cria sua conta do Stripe, esta pode ser conectada à plataforma CoopCycle e ao restaurante:
- Se os administradores ativaram o restaurante para gerenciar sua própria conta do Stripe, o proprietário do restaurante com sua própria conta pode conectar a conta do Stripe acessando *Informações gerais* clicando no nome do restaurante ou no botão 'editar'. Em seguida, clique na guia 'Pagamento' e conecte-se ao Stripe.
- Se os administradores desativaram o restaurante para gerenciar sua própria conta do Stripe, você deve seguir as mesmas etapas, mas com uma conta de administrador para conectar a conta do restaurante.