# LWPredictOps

Projeto desenvolvido para o Enterprise Challenge da FIAP em parceria com a Locaweb.

## Objetivo

O LWPredictOps é uma solução preditiva para análise de incidentes P2 e P3.

A proposta é utilizar séries temporais para gerar previsões D+1 e D+7 e apoiar o planejamento operacional e a tomada de decisão.

## Tecnologias

- Python
- Pandas
- NumPy
- Statsmodels
- Scikit-learn
- Google Colab
- Azure SQL
- Power BI

## Fluxo da solução

Dataset → Python/Colab → ARIMA → Azure SQL → Power BI

## Metodologia

1. Leitura e tratamento dos dados
2. Seleção dos incidentes P2 e P3 de 2025
3. Criação da série temporal diária
4. Teste de estacionariedade ADF
5. Primeira diferenciação da série
6. Comparação de diferentes modelos ARIMA
7. Seleção do modelo pelo menor MAE
8. Previsão para os sete primeiros dias de 2026
9. Visualização dos resultados no Power BI

## Resultados

- Incidentes P2/P3 analisados: **56.905**
- Modelo selecionado: **ARIMA(1,1,0)**
- MAE: **123,23**
- Previsão D+1: **429 incidentes**
- Previsão D+7: **417 incidentes**
- Acumulado previsto em 7 dias: **2.930 incidentes**

## Dashboard

Acesse o dashboard interativo no Power BI:

[Dashboard LWPredictOps](https://app.powerbi.com/view?r=eyJrIjoiYTA2ODA4ZTEtNjUwZC00YjQ4LTk3MmItZDkyYjU1Njk2MzdkIiwidCI6IjExZGJiZmUyLTg5YjgtNDU0OS1iZTEwLWNlYzM2NGU1OTU1MSIsImMiOjR9)

## Arquivos do repositório

- `LWPredictOps.ipynb` — tratamento, análise e modelagem
- `serie_diaria_2025.csv` — série temporal diária
- `previsoes_2026.csv` — previsões geradas pelo ARIMA
- `lwpredict.pbix` — dashboard do Power BI

