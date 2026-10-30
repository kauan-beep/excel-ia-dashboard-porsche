# Excel com IA: dashboard de vendas Porsche

Dashboard interativa criada a partir de uma planilha de 100 vendas da Porsche, com a liberdade visual que os gráficos do Excel não dão. Projeto do desafio "Criando uma Dashboard da Porsche com Agentes de IA" (DIO).

**Dashboard publicada:** https://kauan-beep.github.io/excel-ia-dashboard-porsche/



![Print da dashboard](prints/dashboard.png)




![Filtro aplicado: modelo Macan](prints/filtro-aplicado.png)



## Perguntas de negócio

1. **Quais modelos geram mais receita?** Mostra onde está o dinheiro. Um modelo pode vender muito e render pouco, ou o contrário.
2. **Como a receita evoluiu por ano?** Mostra se o negócio cresce e qual ano foi o melhor.
3. **Como os clientes pagam?** Mostra o peso de cada forma de pagamento, útil para decidir onde oferecer condições.

Cada gráfico tem uma frase de leitura que se atualiza com os filtros.

## Indicadores e filtros

- Indicadores de topo: total de vendas, receita total e ticket médio.
- Filtros: modelo, estado, cidade, ano e método de pagamento.
- Botão para limpar filtros e opção de carregar outra base em CSV.

## Tratamento da base antes da IA

- Mantive só as colunas sanitizadas: modelo, cidade, estado, ano, preço e método de pagamento.
- Converti preço e ano para número.
- Colei tudo como valores, sem fórmulas, para não sobrar referência quebrada.
- Embuti os dados no HTML.
- Conferi que não há dado sensível na base, porque ela fica pública.

## Prompt

```
Tenho uma planilha com 100 vendas da Porsche (modelo, cidade, estado, ano, preço, método de pagamento).
Crie uma dashboard em HTML de arquivo único que responda 3 perguntas:
1) quais modelos geram mais receita, 2) como a receita evolui por ano, 3) como os clientes pagam.
Inclua filtros por modelo, estado, cidade, ano e pagamento, e indicadores de topo
com total de vendas, receita e ticket médio. Dados embutidos no HTML, sem bibliotecas externas.
```

O que mudou até a versão final:

- Troquei os gráficos por barras feitas em HTML/CSS, para funcionar sem internet e sem biblioteca.
- Adicionei a frase de leitura abaixo de cada pergunta.
- Adicionei o botão de carregar CSV e o modo escuro automático.
- Defini a paleta: cinza-grafite, branco gelo e vermelho Porsche como destaque.

## Ferramentas usadas

- Excel para preparar a base.
- IA (Claude) para gerar e refinar o HTML.

## Arquivos

- `index.html`: a dashboard completa (HTML, CSS e JavaScript).
- `prints/`: capturas de tela da dashboard.

## Como publicar

1. Crie o repositório público `excel-ia-dashboard-porsche`.
2. Envie `index.html`, `README.md` e a pasta `prints`.
3. Em Settings, Pages, escolha a branch `main` e a pasta `/ (root)`.
