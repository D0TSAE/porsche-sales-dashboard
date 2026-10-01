# Porsche Sales Dashboard

Dashboard interativa desenvolvida em HTML para análise de uma base sanitizada com 100 registros de vendas da Porsche.

## Objetivo

O objetivo do projeto foi transformar uma planilha de vendas em uma dashboard simples, interativa e publicada na web, usando filtros, indicadores e perguntas de negócio.

## Perguntas de negócio

### 1. Quais modelos concentram maior valor de vendas?

Foi utilizado um gráfico de barras horizontais com o valor total registrado por modelo.  
A escolha ajuda a identificar rapidamente quais modelos representam maior volume financeiro dentro da base.

### 2. Quais estados concentram maior valor de vendas?

Foi utilizado um gráfico de barras com o valor total registrado por estado.  
Foi escolhido estado em vez de cidade porque a base possui muitas cidades diferentes em relação ao total de registros, o que deixaria a visualização mais poluída.

### 3. Quais métodos de pagamento são mais utilizados?

Foi utilizado um gráfico de rosca com a quantidade de registros por método de pagamento.  
Essa análise permite entender como os clientes estão distribuídos entre financiamento, transferência, cartão, dinheiro e outros meios de pagamento.

## Indicadores

A dashboard apresenta quatro indicadores principais:

- Quantidade de registros;
- Valor total registrado;
- Ticket médio;
- Quantidade de veículos entregues.

O termo **valor total registrado** foi usado no lugar de receita porque a base também contém registros com status como `Pending`, `In Transit` e `Cancelled`.

## Filtros

A dashboard permite filtrar os dados por:

- Modelo;
- Ano do modelo;
- Estado;
- Método de pagamento;
- Status de entrega.

Todos os filtros atualizam automaticamente os indicadores e os gráficos.

## Tratamento da base

A planilha original possuía dados brutos e versões sanitizadas dos mesmos campos.

Para a dashboard foram mantidos apenas os campos necessários para análise:

- ID da venda;
- Data sanitizada;
- Modelo;
- Ano do modelo;
- Preço;
- Quilometragem;
- Método de pagamento;
- Cidade;
- Estado;
- Status de entrega.

Também foram realizados os seguintes ajustes:

- Conversão de preço para valor numérico;
- Conversão do ano do modelo para número;
- Conversão da quilometragem para número;
- Remoção de colunas brutas que não eram necessárias;
- Remoção de informações pessoais desnecessárias para a análise.

A coluna de data sanitizada possui alguns registros `INVALID`, por isso ela não foi usada como uma das perguntas principais da dashboard.

## Processo de criação com IA

A dashboard foi construída com auxílio do ChatGPT.

O primeiro prompt definiu:

- Criação de uma dashboard em HTML;
- Uso da base sanitizada;
- Filtros por modelo, ano, estado, método de pagamento e status;
- Indicadores de topo;
- Três perguntas de negócio;
- Visual escuro inspirado na identidade da Porsche.

Depois da primeira versão funcional, foram feitos refinamentos:

- Melhoria dos textos das perguntas de negócio;
- Troca do gráfico de método de pagamento para gráfico de rosca;
- Inclusão de uma observação sobre o uso do termo “valor total registrado”;
- Pequenos ajustes visuais e de responsividade;
- Manutenção de todos os dados diretamente no HTML para facilitar a publicação.

Não foi utilizado um agente com skill própria nesta versão.

## Tecnologias

- HTML
- CSS
- JavaScript
- Chart.js
- GitHub Pages

## Estrutura do projeto

```text
porsche-sales-dashboard/
├── index.html
├── README.md
├── porsche_sales_base_preparada.xlsx
└── assets/
    └── dashboard-preview.png
```

## Preview

![Preview da dashboard](assets/dashboard-preview.png)

## Dashboard publicada

Após ativar o GitHub Pages, adicione aqui o link da dashboard:

`https://SEU-USUARIO.github.io/porsche-sales-dashboard/`

## Como executar localmente

1. Baixe ou clone o repositório.
2. Abra o arquivo `index.html` em um navegador.
3. Mantenha conexão com a internet para carregar a biblioteca Chart.js.

## Observação

A base utilizada no projeto é uma versão sanitizada disponibilizada para fins educacionais.
