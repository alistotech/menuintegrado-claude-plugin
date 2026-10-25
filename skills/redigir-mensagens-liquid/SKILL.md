---
name: redigir-mensagens-liquid
description: Ajude a criar ou revisar mensagens e templates Liquid usados no Menu Integrado, consultando as variáveis disponíveis para o contexto correto. Use quando o usuário pedir uma mensagem com personalização Liquid para clientes, pedidos, conversas do chatbot ou promoções.
---

# Redigir mensagens com Liquid

Use `get_liquid_variables` antes de escrever ou revisar um template Liquid do Menu Integrado. A ferramenta é a fonte das variáveis, filtros, exemplos e observações disponíveis em cada contexto.

1. Se o contexto estiver claro, consulte a ferramenta com o contexto correspondente: `customer_message` para mensagens a clientes e ativações; `order_notification` para notificações de pedido; `conversation_message` para respostas e mensagens de conversa do chatbot; `promotion_message` para mensagens de promoções por meta de pedidos.
2. Se o contexto não estiver claro, chame a ferramenta sem contexto, apresente as opções retornadas e pergunte onde a mensagem será usada antes de redigir.
3. Use somente nomes de variáveis e filtros retornados para aquele contexto. Preserve a grafia exata. Não presuma que uma variável de outro contexto esteja disponível.
4. Entregue um template pronto para copiar e explique brevemente as variáveis ou condições usadas quando isso ajudar. Respeite as notas e os exemplos retornados, inclusive condições de disponibilidade.
5. Informe que o resultado é um rascunho para copiar: essa ferramenta não salva nem altera as configurações do chatbot.

Não chame ferramentas de escrita para um pedido de redação ou revisão de mensagem. Só faça alterações no sistema se o usuário pedir explicitamente uma ação de escrita suportada por outra ferramenta.
