---
title: Pagamento Stripe
lang: pt-BR
ref: admin-stripe
parent: Guia do Administrador
nav_order: 4
---


#Gerenciando pagamentos via Stripe

## O que é o Stripe?

Stripe é um provedor de serviços de pagamento, que nos permite gerenciar pagamentos com cartão de crédito de maneira segura. Além disso, a funcionalidade "Stripe Connect" permite gerenciar o aspecto "plataforma" do pagamento, ou seja, a distribuição de pagamentos entre a plataforma (dinheiro que vai para a cooperativa de entrega) e o restaurante.

Devido ao fato de a cooperativa européia ser financiada por contribuições, nós (CoopCycle) não cobramos uma comissão por pagamentos. O Stripe cobra uma taxa por cada transação ([verifique os preços do seu país aqui] (https://stripe.com/pricing) {: target = "_blank"}).


Por que o Stripe?

O Stripe se estabeleceu como o "rols-Royce" dos serviços de pagamento. O serviço tem a reputação de ser de excelente qualidade. É possível encontrar serviços mais baratos, mas acreditamos que o preço vale a pena. Um ponto negativo conhecido sobre o Stripe é que a (boa) interface de administração do Stripe nem sempre está disponível no idioma do usuário.

## O que é o "modo ao vivo" e o "modo de teste" do Stripe?

A plataforma CoopCycle pode ser configurada para usar o modo "ao vivo" ou "teste" na aba "configurações". No modo de teste, os clientes não serão debitados. Você precisa usar cartões de teste (normalmente 4242 4242 4242 4242 4242). **Não se esqueça de mudar para o modo "ao vivo" antes de entrar em produção!**

## Como configurar o Stripe/Stripe Connect na sua plataforma?

1. Crie uma conta do Stripe <a target="_blank" href="https://dashboard.stripe.com/register"> aqui </a> e, em seguida:
    * Obtenha as quatro chaves de distribuição da API (teste Privado/Público ao vivo, Privado/Público) aqui: <a target="_blank" href="https://dashboard.stripe.com/apikeys"> https://dashboard.stripe.com/apikeys </a> (<a target="_blank" href="https://www.youtube.com/watch?v=XLzg_K_0C5k"> em vídeo </a>)
    * Obtenha os dois identificadores do Stripe Connect (ao vivo/teste) aqui: <a target="_blank" href="https://dashboard.stripe.com/account/applications/settings"> https://dashboard.stripe.com/account/applications/settings </a>
    * Cole-os nos campos correspondentes na guia "parâmetros" do administrador.

Nota: As chaves e IDs ativos e de teste não são exibidos na tela ao mesmo tempo. Há uma opção na página para exibir dados de teste ou ao vivo.

2. Configure o URL de redirecionamento para o Stripe Connect
   * Vá para <a target="_blank" href="https://dashboard.stripe.com/account/applications/settings"> https://dashboard.stripe.com/account/applications/settings </a>
   * Clique em "Adicionar URI de redirecionamento" (**Isso deve ser feito nos modos ao vivo e teste**). Em seguida, insira este valor "https://<nome_do_domínio>/stripe/connect/standard" (por exemplo, `https://demo.coopcycle.org/stripe/connect/standard`)

## Como ativar sua conta do Stripe para usar a plataforma?

Você precisa ativar sua conta do Stripe para começar a usar a plataforma "ao vivo". Clique em "Ativar sua conta" à esquerda e insira as informações necessárias. (vídeo: <a target="_blank" href="https://www.youtube.com/watch?v=XLzg_K_0C5k"> https://www.youtube.com/watch?v=XLzg_K_0C5k </a>)

## Como ver o dinheiro ganho através da plataforma?

Os ganhos que vieram através da plataforma (a cooperativa de entrega) são calculados como uma comissão sobre o pagamento do comerciante. Vá para este URL <a target="_blank" href="https://dashboard.stripe.com/test/applications/fees"> https://dashboard.stripe.com/test/applications/fees </a> .

## Como receber esse dinheiro em sua conta?

Os pagamentos da sua conta do Stripe para a sua conta bancária serão feitos regularmente ("pagamentos"). Você pode acessar a lista de pagamentos aqui: <a target="_blank" href="https://dashboard.stripe.com/test/balance/overview"> https://dashboard.stripe.com/test/balance/overview </a>. Você também pode solicitar nesta página uma transferência imediata para sua conta.