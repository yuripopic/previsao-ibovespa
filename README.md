# Previsão Ibovespa

## 🎯 Objetivo:
desenvolver um modelo preditivo capaz de prever se o índice IBOVESPA vai fechar em 
alta ou baixa no dia seguinte, com base em dados históricos do próprio índice. Esse
modelo será usado como insumo para alimentar dashboards internos de tomada de 
decisão dos analistas quantitativos da empresa.

## 📦 Bibliotecas Utilizadas no Modelo

Este projeto utiliza as seguintes bibliotecas Python:

- **`numpy`**  
  Utilizada para manipulação eficiente de arrays e operações matemáticas vetorizadas.

- **`pandas`**  
  Usada para carregar, tratar e organizar os dados históricos do Ibovespa em estruturas tabulares (DataFrames).

- **`sklearn.preprocessing.MinMaxScaler`**  
  Responsável por normalizar os dados numéricos para a faixa de 0 a 1, facilitando o treinamento do modelo LSTM.

- **`sklearn.metrics`**  
  Conjunto de métricas usadas para avaliar a performance do modelo, como:
  - MAE (Erro Absoluto Médio)
  - MAPE (Erro Percentual Absoluto Médio)
  - RMSE (Raiz do Erro Quadrático Médio)

- **`keras.models.Sequential` & `keras.layers` (LSTM, Dense)**  
  Utilizadas para construir e treinar a rede neural LSTM.

- **`plotly.graph_objects`**  
  Usado para visualização interativa de gráficos.

- **`pathlib.Path`**  
  Permite manipular caminhos de arquivos de forma mais segura e multiplataforma.

- **`datetime.timedelta`**  
  Usado para trabalhar com operações de datas, como calcular o próximo dia após o valor mais recente da base.

- **`os`**  
  Auxilia na obtenção e manipulação de caminhos de diretórios locais.


