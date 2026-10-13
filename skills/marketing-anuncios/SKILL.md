---
name: marketing-anuncios
description: Crie campanhas de anúncios no Menu Integrado com um ou mais anúncios. Use quando o usuário pedir explicitamente para criar uma campanha de anúncios.
---

# Criar campanhas de anúncios

A tool `create_ad` cria uma campanha no Menu Integrado com orçamento diário compartilhado. Cada anúncio da campanha tem seu próprio texto, título, link de destino e imagem. O MI envia a campanha e os anúncios para o Meta Ads após processar o job; isso poderá gerar gastos conforme o orçamento diário.

1. Identifique a unidade. Se não estiver clara, use `list_restaurants` e peça que o usuário escolha.
2. Peça as informações que faltarem: nome da campanha, orçamento diário na moeda da conta Meta e, para cada anúncio, nome interno, texto, título, link de destino e imagem. Passe os anúncios no campo ads, com name, message, headline, link_url e image_data em cada item. Se o usuário quiser apenas um anúncio, envie uma lista com um item.
3. Não estime nem invente o orçamento diário. O usuário precisa informar o valor.
4. Gere ou obtenha uma imagem PNG ou JPEG própria para cada anúncio. Envie cada imagem como data URL Base64, com menos de 30 MB.
5. A tool exige o escopo `mcp:write` e um plano com acesso a marketing.
6. Após sucesso, confirme que a campanha foi salva e sua ativação foi enfileirada. Informe que a campanha poderá gerar gastos conforme o orçamento diário. Não diga que já está ativa.
