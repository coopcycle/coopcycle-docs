---
title: Pacotes
lang: pt-BR
ref: packages-set
parent: Logística
grand_parent: Guia do Administrador
nav_order: 4
---

**Conjuntos de pacotes** permitem configurar diferentes unidades de volume quando as lojas criam pedidos.

É útil diferenciar o preço, dependendo do tipo de pacote.

No final, um **pacote** será traduzido na criação de pedidos pelas lojas, como na imagem abaixo
![Conjuntos de pacotes] (/assets/images/package_order.png)

---

## Configurando o conjunto de pacotes

Dependendo das necessidades de seus clientes, você pode criar um conjunto de pacotes comuns (definindo que pequeno = um volume definido) ou criar conjuntos de pacotes diferentes (para uma loja de flores, isso pode depender do tamanho dos buquês).
Para criar um conjunto de pacotes, você precisa ir na seção Pacotes do menu suspenso Configuração.

Ao criar um conjunto de pacotes, você deve criar diferentes pacotes associados a unidades de volume, como na imagem abaixo:
![Conjuntos de pacotes] (/assets/images/package_config.png)

### Criando uma regra de preço

A incorporação de pacotes à regra de preços não é difícil, você precisa determinar o preço quando os pedidos contêm pelo menos um tipo de pacote.
Você pode combinar diferentes tipos de pacotes para criar a regra mais adequada.
Lembre-se de que as regras mais específicas precisam estar no topo da hierarquia de regras.
![Conjuntos de pacotes] (/assets/images/package_pricing.png)

### Vinculando uma loja a um conjunto de pacotes
Depois de definir seus conjuntos e preços, é necessário adicionar as opções de pacote à loja.
Basta ir nas configurações da loja desejada, vinculá-la ao preço correto e alterar a opção **Requer especificação de pacotes**.
