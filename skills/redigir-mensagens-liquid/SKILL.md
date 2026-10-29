---
name: redigir-mensagens-liquid
description: Ajude a criar ou revisar mensagens Liquid e templates personalizados de impressão usados no Menu Integrado, consultando as variáveis disponíveis para o contexto correto. Use para mensagens a clientes, pedidos, conversas, promoções ou impressões HTML, ESC/POS e ZPL.
---

# Redigir mensagens com Liquid

Use `get_liquid_variables` antes de escrever ou revisar uma mensagem ou template Liquid do Menu Integrado. A ferramenta é a fonte das variáveis, filtros, exemplos e limitações disponíveis em cada contexto.

1. Se o contexto estiver claro, consulte a ferramenta com o contexto correspondente: `customer_message` para mensagens a clientes e ativações; `order_notification` para notificações de pedido; `conversation_message` para respostas e mensagens de conversa do chatbot; `promotion_message` para mensagens de promoções por meta de pedidos; `print_order_html` para impressões personalizadas HTML; `print_order_native` para impressões nativas ESC/POS ou ZPL; `print_voucher` para vouchers de produto; `print_variation_item` para o subtemplate de variações e opcionais.
2. Se o contexto ou formato de impressão não estiver claro, chame a ferramenta sem contexto, apresente as opções retornadas e pergunte onde o template será usado antes de redigir.
3. Use somente nomes de variáveis e filtros retornados para aquele contexto. Preserve a grafia exata. Não presuma que uma variável de outro contexto esteja disponível.
4. Entregue um template pronto para copiar e explique brevemente as variáveis ou condições usadas quando isso ajudar. Respeite as notas e os exemplos retornados, inclusive condições de disponibilidade.
5. Para impressão, respeite as diferenças entre HTML/Markdown, ESC/POS e ZPL e as limitações descritas pelo contexto. Não inclua `totals_table` em HTML; use apenas se o contexto nativo a disponibilizar.
6. Informe que o resultado é um rascunho para copiar: essa ferramenta não salva nem altera as configurações de mensagens ou impressão.

Não chame ferramentas de escrita para um pedido de redação ou revisão de mensagem. Só faça alterações no sistema se o usuário pedir explicitamente uma ação de escrita suportada por outra ferramenta.
