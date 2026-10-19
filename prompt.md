# Prompt usado para gerar a dashboard

## Versão final

```
Você é um analista de dados e designer front-end. Crie uma dashboard em HTML,
em um único arquivo (HTML + CSS + JavaScript juntos), a partir da base em anexo
(base_tratada.csv), com 100 vendas da Porsche.

A dashboard precisa responder três perguntas de negócio:
1. Qual família de modelo mais vende? (agrupar pelo início do nome: 911, 718,
   Cayenne, Macan, Taycan, Panamera) -> gráfico de barras com a quantidade.
2. Qual estado vende mais? -> gráfico de barras horizontais por estado.
3. Qual o preço médio de cada família? -> gráfico de barras com o ticket médio,
   ordenado do mais caro para o mais barato.

Indicadores no topo: total de vendas, receita total, ticket médio e
% de vendas entregues (status "Delivered").

Filtros (todos atualizando indicadores e gráficos ao mesmo tempo):
família, estado, ano do modelo e método de pagamento, com um botão para limpar.
Não use a data da venda como filtro, porque 24 registros têm data INVALID.

Visual: estilo vintage, inspirado em pôsteres antigos de corrida da Porsche.
Fundo creme envelhecido, textos em preto, destaques em vermelho Porsche e
dourado do brasão. Tipografia serifada clássica nos títulos e uma fonte
monoespaçada para os números. Abaixo de cada gráfico, uma frase curta
explicando o que ele responde.

Use Chart.js via CDN. Os dados devem ficar embutidos no próprio HTML.
Valores em dólar (US$). Textos da interface em português.
```

## O que mudou até a versão final

- **Pergunta 1:** a ideia inicial era "qual o modelo mais vendido". Olhando a base,
  existem 40 modelos diferentes e o primeiro lugar tem só 4 vendas, empatado com
  outros cinco. Troquei para agrupar por **família**, e aí a resposta ficou clara.
- **Pergunta 3:** era "média de valores dos mais vendidos". Virou "preço médio de
  cada família", para dar pra comparar todas lado a lado.
- **Filtro de data:** foi trocado por **ano do modelo**, por causa das datas INVALID.
