# Previsão Ibovespa

## 🎯 Objetivo:
desenvolver um modelo preditivo capaz de prever se o índice IBOVESPA vai fechar em 
alta ou baixa no dia seguinte, com base em dados históricos do próprio índice. Esse
modelo será usado como insumo para alimentar dashboards internos de tomada de 
decisão dos analistas quantitativos da empresa.

## 📦 Bibliotecas Utilizadas no Modelo


| Biblioteca | Descrição |
|------------|-----------|
| **[yfinance](https://github.com/ranaroussi/yfinance)** | Biblioteca para baixar dados históricos do mercado financeiro diretamente do Yahoo Finance. Usada para obter os dados diários do IBOVESPA (`^BVSP`). |
| **[pandas](https://pandas.pydata.org/)** | Manipulação de dados em formato de tabelas (DataFrame). Usada para tratar os dados, calcular indicadores técnicos e preparar o conjunto de dados. |
| **[numpy](https://numpy.org/)** | Suporte a operações numéricas e vetoriais, utilizada para cálculos matemáticos e criação de colunas como variações percentuais. |
| **[xgboost](https://xgboost.readthedocs.io/)** | Framework de Gradient Boosting de alto desempenho, utilizado para treinar o modelo preditivo (`XGBClassifier`). |
| **[scikit-learn](https://scikit-learn.org/)** | Utilizada para pré-processamento (escalonamento com `StandardScaler`), avaliação do modelo (`accuracy_score`, `confusion_matrix`, `classification_report`) e divisão dos dados (`TimeSeriesSplit`). |
| **[matplotlib](https://matplotlib.org/)** | Biblioteca de visualização para criar gráficos e comparar previsões com os dados reais. |
| **[seaborn](https://seaborn.pydata.org/)** | Extensão do matplotlib que facilita visualizações estatísticas, como mapas de calor para matrizes de confusão. |


## ⚙️ Funcionalidades do código

- Download automático de dados do IBOVESPA com `yfinance`
- Criação de features com indicadores técnicos (RSI, MACD, Bandas de Bollinger, OBV, etc.)
- Modelagem com `XGBoost` para classificação binária (Alta ou Baixa)
- Avaliação da acurácia e relatório de desempenho
- Visualização gráfica dos resultados
