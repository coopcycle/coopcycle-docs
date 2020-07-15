---
lang: pt-BR
title: WooCommerce
ref: plugins-woocommerce
parent: Plugins
---

O CoopCycle é enviado com um [plugin WordPress para WooCommerce](https://wordpress.org/plugins/coopcycle/).

Visão geral
--------

O plug-in CoopCycle para WordPress permite adicionar um [método de envio](https://docs.woocommerce.com/document/setting-up-shipping-zones/) ao WooCommerce, e transmitir os dados de entrega para a CoopCycle diretamente, usando a API.

Se um de seus parceiros já tiver um site de comércio eletrônico baseado no WooCommerce, é a melhor maneira de ter uma integração perfeita.

No CoopCycle, os dados de entrega enviados serão anexados a uma [loja](pt-BR/admin/lojas), portanto, você precisará criar uma loja se ainda não a tiver.
As configurações da loja modificam o comportamento do plug-in, em particular a configuração do intervalo de tempo usado.

Obtendo um token de API
----------------------

A primeira coisa a fazer é obter um token da API, para que o site que executa o WooCommerce possa interagir com a API CoopCycle.

Vá para Configuração ›API e clique em «Adicionar». Digite o nome do aplicativo (por exemplo, o nome do site executando o WooCommerce), selecione a loja para a qual você deseja gerar um token de API e pressione «Salvar».

Você deve obter duas credenciais, uma "API Key" e "API Secret", necessárias para configurar o plug-in.

Instalando e configurando o plug-in
-------------------------------------

O plug-in CoopCycle para WooCommerce pode ser instalado em [wordpress.org] (https://wordpress.org/plugins/coopcycle/).

Na área de administração do WordPress, vá para a página Plugins e procure por "coopcycle".

Na página de configurações do plug-in, insira o URL base da instância CoopCycle, a «API Key» e a «API Secret» e salve as alterações.

Configurando o WooCommerce
-----------------------

Depois que o plug-in CoopCycle estiver configurado, você precisará adicionar a um [método de envio para uma zona](https://docs.woocommerce.com/document/setting-up-shipping-zones/#section-6).

Vá para WooCommerce › Configurações › entrega. Se ainda não o fez, clique em «Adicionar zona de expedição» ou edite uma das suas zonas de expedição existentes.

Clique em «Adicionar método de envio» e selecione «CoopCycle».

Após a adição do método de envio, você pode configurá-lo. As configurações são as mesmas do método padrão [Envio de taxa fixa](https://docs.woocommerce.com/document/flat-rate-shipping/) do WooCommerce.

A coisa mais importante que você precisa configurar é o **custo de envio**.

Parabéns! 🎉

Agora, ao inserir um endereço que corresponda à zona de entrega, os clientes poderão escolher o método de entrega CoopCycle.