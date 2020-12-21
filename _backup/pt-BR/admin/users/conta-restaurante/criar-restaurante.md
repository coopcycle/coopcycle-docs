---
title: Criar Restaurante
lang: pt-BR
ref: creating-restaurant
parent: Conta Restaurante
grand_parent: Usuários
nav_order: 1
custom_scripts:
  - "https://cdnjs.cloudflare.com/ajax/libs/jquery-zoom/1.7.21/jquery.zoom.min.js"
  - "/assets/scripts/zoom.js"
---

# Criando restaurantes

Esta página descreve o processo de criação de um restaurante na plataforma CoopCycle. Não hesite em pedir ajuda [contact@coopcycle.org] (mailto: contact@coopcycle.org) para configurar os primeiros restaurantes.

Isso ocorre em duas etapas:
- Crie o restaurante na plataforma CoopCycle
- Crie uma conta [Stripe] (https://dashboard.stripe.com/register)

Depois de executar estas duas etapas:

- Crie uma conta para o gerente do restaurante na seção "Usuários"
- Atribua o restaurante a esse gerente para que ele possa acessar o back office


Pré-requisito:

- Tendo configurado corretamente a conta da Stripe vinculada à plataforma (link para a página correspondente)


Informações mínimas necessárias previamente:

- Nome, primeiro nome do gerente
- Nome legal do restaurante
- Número de telefone do restaurante
- Endereço do restaurante
- IBAN do restaurante
- **Digitalização frente/verso colorida da carteira de identidade do proprietário do restaurante em formato JPEG ou PNG (solicitação de distribuição após os primeiros pedidos de verificação de identidade)**
- Informações contratuais (que taxa de entrega para o dono do restaurante? Para o cliente? Quem paga as taxas?)


Informação opcional:

- Horário de funcionamento (horário em que a entrega está ativada)
- Número CNPJ

## 1 - Criando um restaurante

- Na guia "Restaurantes", clique em "Adicionar restaurante"
- Insira informações nos campos correspondentes

! [Criação de um restaurante] (/assets/images/creation_resto_fr.png)

- Clique em "Salvar"

## 2 - Criando uma conta do restaurante Stripe

- **No painel do Stripe**, [https://dashboard.stripe.com/account}(https://dashboard.stripe.com/account), crie uma nova conta clicando no canto superior esquerdo em "Novo Conta". Indique o nome do restaurante.

<span class = "zoomable">! [Stripe] (/assets/images/stripe_resto_account_fr.png) </span>
![Stripe] (/assets/images/stripe_resto_account_fr_2.png)

- **Na página do restaurante na plataforma**, na seção "Conta da Stripe", clique no botão "Conectar com a Stripe". O processo deve ser repetido para operação dev e operação em produção.

! [Stripe] (/assets/images/stripe_resto_account_fr_3.png)

- Uma página de distribuição é aberta. No menu suspenso "Alternar conta", selecione o restaurante correspondente.

! [Stripe] (/assets/images/stripe_resto_account_fr_4.png)

- Insira as informações do restaurante correspondente. <span style = "color: red"> **Atenção: no campo “Número de telefone do cliente” indica seu número de telefone no telefone para restaurante.** </span>


- Verifique seu número de telefone no seguinte endereço: [https://dashboard.stripe.com/phone-verification?source=email{(https://dashboard.stripe.com/phone-verification?source=email): digite seu número de telefone e copie o código recebido por SMS (você deveria ter recebido uma notificação por email)

- E aí vai! Para verificar se tudo está em ordem com o Stripe:
  - No painel do Stripe, selecione sua conta principal (a conta da cooperativa) no menu suspenso no canto superior esquerdo
  - Clique em "Conectar" e "Contas" na coluna da esquerda
  - Na lista "Contas conectadas recentemente" que aparece, clique no primeiro (a última conta vinculada)
  - Verifique se "Pagamentos" e "Pagamentos" estão verdes - em caso de problemas, entre em contato com [dev@coopcycle.org] (mailto: dev@coopcycle.org)
  
  ![Stripe] (/assets/images/stripe_resto_account_fr_5.png)

  
     
