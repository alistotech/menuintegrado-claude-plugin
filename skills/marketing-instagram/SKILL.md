---
name: marketing-instagram
description: Crie e publique posts no Instagram de uma unidade pelo MCP do Menu Integrado. Use quando o usuário pedir explicitamente para criar ou publicar um post.
---

# Posts no Instagram

A tool `create_instagram_post` cria o post e coloca sua publicação na fila no Instagram conectado à unidade. Ela não cria um rascunho.

1. Identifique a unidade. Se ela não estiver clara, use `list_restaurants` e peça que o usuário escolha.
2. Use uma capacidade de geração de imagem disponível para criar de uma a dez imagens JPEG. Se não houver geração disponível, peça que o usuário forneça as imagens.
3. Envie para a tool o `restaurant_slug`, um `subject`, a legenda opcional e as imagens como data URLs JPEG Base64 (`data:image/jpeg;base64,...`).
4. A tool requer `mcp:write` e um plano com acesso a marketing. Se não estiver disponível, explique o que falta.
5. Confirme que o post foi criado e que a publicação foi colocada na fila apenas após sucesso da tool. Não diga que já foi publicado: a publicação é processada em segundo plano.

Chame a tool somente quando o usuário pedir para criar/publicar o post. Um pedido para escrever uma legenda ou preparar uma ideia não autoriza a publicação.
