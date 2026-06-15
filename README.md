# Simulado de Exploração e Análise de Vendas
 
## Sobre o projeto
O **RetailView** é um simulado de análise exploratória de dados (EDA) de vendas, baseado na base de dados **Online Retail II** — transações de um varejo online do Reino Unido entre 2009 e 2011.

## O que o projeto analisa
- Receita total e volume de vendas por mês e trimestre
- Top produtos e categorias por receita
- Desempenho por país (região)
- Segmentação de clientes por nível de gasto (Bronze, Prata, Ouro)
- Comparação entre os dados com e sem tratamento de outliers (v1 e v2)
- Exportação de relatórios 

## Estrutura do projeto
```
Simulado_RetailView/
|-- data/
|   |-- raw/                       # online_retail_II.csv
|   |-- processed/
|   |   |-- v1_com_outliers/       # limpeza, outliers mantidos 
|   |   |-- v2_outliers_tratado/   # limpeza + outliers tratados
|   |-- final/                     # versao escolhida (v2) 
|-- notebooks/
|   |-- retailview.ipynb           # notebook principal de EDA
|-- outputs/
|   |-- metricas_por_mes.csv
|   |-- segmentacao_clientes.csv
|   |-- estatisticas_gerais.json
|   |-- graficos/                  # Gráficos exportados
|-- README.md
```

## Decisão de versão (dados)
A análise final usa a versão **v2** (outliers tratados). A v1 (com outliers) fica preservada em `data/processed/` para consulta futura.

## Observação sobre a coluna `categoria`
A base Online Retail II não traz uma categoria pronta. Neste simulado, a coluna `categoria` é **derivada por palavras-chave** da descrição do produto (ex.: "CHRISTMAS" é Natal, "BAG" é Bolsas), com o rótulo `Outros` como padrão.

## Ferramentas utilizadas
- Python 3.10+
- Bibliotecas: pandas, numpy, matplotlib, seaborn

## Vídeo de demonstração
[Inserir link do Google Drive ou YouTube aqui]