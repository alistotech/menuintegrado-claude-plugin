---
name: marketing-anuncios
description: Crie anúncios no Menu Integrado para ativação posterior. Use quando o usuário pedir explicitamente para criar um anúncio.
---

# Criar anúncios

A tool `create_ad` salva o anúncio e o orçamento no Menu Integrado e enfileira `Ads::AfterCreateJob`. O MI replica o anúncio e ativa a campanha no Meta Ads quando processa o job; isso poderá gerar gastos conforme o orçamento diário.

1. Identifique a unidade. Se não estiver clara, use `list_restaurants` e peça que o usuário escolha.
2. Peça as informações que faltarem: nome interno, texto, título, link de destino e orçamento diário na moeda da conta Meta.
3. Não estime nem invente o orçamento diário. O usuário precisa informar o valor.
4. Gere uma imagem PNG ou JPEG com a ferramenta de imagem disponível, ou peça ao usuário que forneça a imagem. Envie como data URL Base64, com menos de 30 MB.
5. A tool exige o escopo `mcp:write` e um plano com acesso a marketing.
6. Após sucesso, confirme que o anúncio foi salvo e que a ativação foi enfileirada. Explique que o MI ativará a campanha ao processar o job e que isso poderá gerar gastos conforme o orçamento diário. Não diga que a campanha já está ativa.
