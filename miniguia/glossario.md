# 📖 Glossário — Ciência de Dados com Python

Termos organizados por ordem de importância para iniciantes.

---

| # | Termo | Definição | Exemplo de uso |
|---|-------|-----------|----------------|
| 1 | **Dataset** | Conjunto de dados organizado em linhas (observações) e colunas (variáveis). É a matéria-prima de toda análise. | Um CSV com vendas mensais de uma loja |
| 2 | **DataFrame** | Estrutura de dados tabular bidimensional da biblioteca Pandas. Pense numa planilha Excel dentro do Python. | `df = pd.read_csv('vendas.csv')` |
| 3 | **Series** | Estrutura unidimensional do Pandas. Equivale a uma única coluna de um DataFrame. | `df['preço']` retorna uma Series |
| 4 | **EDA** | Análise Exploratória de Dados. Processo de investigar, resumir e visualizar as características principais de um dataset antes de qualquer modelagem. | Verificar nulos, distribuições e outliers |
| 5 | **Variável / Feature** | Cada coluna de um dataset representa uma variável ou característica. Em ML, features são as entradas do modelo. | Idade, salário e cidade num dataset de clientes |
| 6 | **Target / Label** | A variável que queremos prever ou classificar num modelo de Machine Learning. | Prever se um cliente vai cancelar o serviço (churn) |
| 7 | **Outlier** | Valor que se distancia significativamente dos demais numa distribuição. Pode ser erro de medição ou dado legítimo incomum. | Uma venda de R$100.000 num dataset de vendas medianas de R$500 |
| 8 | **Data Wrangling** | Processo de limpeza, transformação e preparação dos dados brutos para análise. É onde a maior parte do tempo de um cientista de dados é gasto. | Tratar nulos, corrigir tipos, padronizar textos |
| 9 | **Valor Nulo / NaN** | Ausência de valor em uma célula do dataset. Precisa ser tratado antes da análise. NaN = "Not a Number". | `df.fillna(0)` substitui nulos por zero |
| 10 | **Correlação** | Medida estatística (-1 a +1) que indica o grau de relação linear entre duas variáveis. +1 = correlação positiva perfeita, -1 = negativa, 0 = sem correlação. | Altura e peso tendem a ter correlação positiva |
| 11 | **Distribuição** | Como os valores de uma variável se espalham. Pode ser normal (bell curve), uniforme, assimétrica etc. | `df['idade'].hist()` mostra a distribuição de idades |
| 12 | **Pipeline** | Sequência encadeada de etapas de processamento de dados. Em ML, automatiza pré-processamento + modelo. | Coleta → Limpeza → EDA → Modelagem → Deploy |
| 13 | **Overfitting** | Quando um modelo aprende os dados de treino tão bem que perde capacidade de generalizar para dados novos. É como decorar as respostas sem entender o conteúdo. | Modelo com 99% de acurácia no treino e 60% no teste |
| 14 | **Underfitting** | Quando um modelo é simples demais para capturar os padrões dos dados. Performa mal tanto no treino quanto no teste. | Usar regressão linear para prever algo não-linear |
| 15 | **Train/Test Split** | Divisão do dataset em conjunto de treino (para aprender) e teste (para avaliar). Evita que o modelo seja avaliado nos mesmos dados que aprendeu. | `train_test_split(X, y, test_size=0.2)` |
| 16 | **Acurácia** | Proporção de previsões corretas em relação ao total. Métrica básica para classificação. Atenção: pode enganar em datasets desbalanceados. | 90% de acurácia = 9 em 10 previsões corretas |
| 17 | **Matriz de Confusão** | Tabela que mostra verdadeiros positivos, falsos positivos, verdadeiros negativos e falsos negativos de um classificador. | Avaliar quantos spams foram detectados corretamente |
| 18 | **Hiperparâmetro** | Configuração do modelo definida antes do treino (não aprendida pelos dados). Ajustá-los é chamado de "tuning". | Número de árvores num Random Forest |
| 19 | **Jupyter Notebook** | Ambiente interativo que combina código Python, texto e visualizações em células executáveis. Padrão na exploração de dados. | Executar análises passo a passo com comentários |
| 20 | **Array** | Estrutura de dados do NumPy para armazenar elementos do mesmo tipo, otimizada para operações matemáticas. | `np.array([1.5, 2.3, 4.1])` |
| 21 | **Normalização** | Redimensionar valores de uma variável para um intervalo padrão (geralmente 0-1 ou média 0 com desvio 1). Importante antes de ML. | `(x - x.min()) / (x.max() - x.min())` |
| 22 | **Agrupamento (groupby)** | Operação que divide o dataset em grupos baseados em uma ou mais colunas, aplica uma função e combina os resultados. | `df.groupby('cidade')['vendas'].sum()` |
| 23 | **Merge / Join** | Combinação de dois DataFrames com base em uma coluna em comum, similar ao JOIN do SQL. | Unir tabela de clientes com tabela de pedidos pelo ID do cliente |
| 24 | **Pivot Table** | Tabela dinâmica que reorganiza e resume dados. Similar à Tabela Dinâmica do Excel. | `df.pivot_table(values='vendas', index='mês', columns='produto')` |
| 25 | **Modelo Preditivo** | Algoritmo treinado com dados históricos para fazer previsões sobre novos dados. | Prever o preço de um imóvel com base em suas características |
