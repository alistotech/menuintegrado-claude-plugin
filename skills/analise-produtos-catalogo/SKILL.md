---
name: analise-produtos-catalogo
description: Analise produtos e catálogo do Menu Integrado: cadastro, variações, fichas técnicas, métricas e histórico de vendas.
---

# Análise de produtos e catálogo

Use as tools MCP para consultar o catálogo e o desempenho dos produtos da unidade escolhida. Separe informações cadastrais, ficha técnica e histórico de vendas.

## Escopo e identificação

1. Identifique a unidade antes de consultar o catálogo.
2. Se a unidade não estiver clara, use `list_restaurants` e peça que o usuário escolha uma unidade antes de consultar o catálogo.
3. Use `list_menu_products` uma vez para localizar produtos e filtre o resultado em memória.
4. Se houver mais de um produto compatível, peça confirmação. Não escolha pelo primeiro resultado.
5. Depois de identificar o produto, use o `product_slug` retornado pelo catálogo.

## Escolha das tools

- Use `list_menu_products` para listar ou pesquisar produtos do catálogo.
- Use `get_product_details` para informações cadastrais do produto.
- Use `get_product_variations` quando o usuário perguntar por variações e seus itens.
- Use `get_product_recipe` quando o usuário pedir a ficha técnica, insumos ou composição.
- Use `get_products_metrics` para desempenho agregado de vários produtos em um período.
- Use `get_product_sales_history` para o histórico de um produto específico, agrupado por dia, semana, mês, trimestre ou ano.

Não chame detalhes, variações ou ficha técnica para todos os produtos quando o usuário pediu apenas uma listagem ou uma busca. Não faça uma chamada de histórico para cada produto quando uma métrica agregada resolver a pergunta.

## Atualização da imagem do produto

- Atualize a imagem somente quando o usuário pedir explicitamente para gerar ou substituir a imagem do produto.
- Identifique a unidade e o produto com `list_menu_products`; se houver mais de uma correspondência, peça ao usuário para escolher antes de alterar o cadastro.
- Gere a imagem com uma ferramenta de geração disponível no cliente. Se não houver uma ferramenta disponível, peça ao usuário que forneça a imagem; não diga que gerou uma imagem.
- Envie a imagem como data URL Base64 PNG, JPEG ou WebP, com menos de 5 MB, para `update_product_image`.
- A tool só aparece quando a conexão tem o escopo `mcp:write`. Se não estiver disponível, explique que é preciso autorizar novamente a conexão com permissão para alterar imagens.
- Confirme a atualização somente depois de receber sucesso da tool.

## Análise e limites

- Para saber quanto um produto vendeu, quando vendeu ou como evoluiu, use `get_product_sales_history` com uma unidade, um produto e um período.
- Para comparar produtos, use `get_products_metrics` uma vez e compare os resultados retornados.
- Para comparar períodos de um produto, repita `get_product_sales_history` para cada período quando necessário.
- Combine detalhes, variações e ficha técnica somente quando a pergunta exigir uma análise do cadastro.
- Não afirme que códigos fiscais, descrições, macros ou custos estão corretos sem dados suficientes.
- Não invente ingredientes, valores nutricionais, margens ou informações que não estejam no retorno das tools.
- Diferencie quantidade de itens vendidos, quantidade de pedidos e faturamento.
- Informe a unidade, o produto e o período usados na resposta.
