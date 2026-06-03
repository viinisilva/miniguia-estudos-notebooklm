# 📝 Resumos Estruturados — Ciência de Dados com Python

---

## Módulo 1: O que é Ciência de Dados?

Ciência de Dados é uma área interdisciplinar que combina **estatística**, **programação** e **conhecimento de domínio** para extrair insights e valor a partir de dados. O objetivo central é transformar dados brutos em informações que apoiem decisões.

### O Cientista de Dados faz:
- Coleta e organiza grandes volumes de dados
- Limpa e prepara dados para análise
- Explora padrões e tendências (EDA)
- Cria visualizações para comunicar resultados
- Constrói modelos preditivos com Machine Learning

### Por que Python?
- Sintaxe simples e legível — ideal para iniciantes
- Ecossistema robusto de bibliotecas de dados
- Comunidade gigante e muito material de aprendizado
- Usado tanto em pesquisa quanto na indústria

---

## Módulo 2: O Pipeline de Ciência de Dados

```
1. DEFINIÇÃO DO PROBLEMA
   → O que queremos descobrir? Qual pergunta estamos respondendo?

2. COLETA DE DADOS
   → Fontes: CSV, APIs, bancos de dados, web scraping
   → Ferramentas: Pandas (read_csv), requests, SQLAlchemy

3. LIMPEZA E PREPARAÇÃO (Data Wrangling)
   → Tratar valores nulos, duplicatas, tipos incorretos
   → Ferramentas: Pandas (dropna, fillna, astype)

4. ANÁLISE EXPLORATÓRIA (EDA)
   → Entender distribuições, correlações, outliers
   → Ferramentas: Pandas (describe, value_counts), Seaborn, Matplotlib

5. MODELAGEM
   → Construir e treinar modelos preditivos
   → Ferramentas: Scikit-learn

6. AVALIAÇÃO
   → Medir a qualidade do modelo
   → Métricas: acurácia, precisão, recall, RMSE

7. COMUNICAÇÃO
   → Apresentar resultados em gráficos e relatórios
   → Ferramentas: Matplotlib, Seaborn, Jupyter Notebooks
```

---

## Módulo 3: Bibliotecas Essenciais

### NumPy
- **O que faz:** Computação numérica de alta performance com arrays multidimensionais
- **Quando usar:** Operações matemáticas, álgebra linear, geração de números aleatórios
- **Exemplo:**
```python
import numpy as np

arr = np.array([1, 2, 3, 4, 5])
print(arr.mean())    # 3.0
print(arr * 2)       # [2, 4, 6, 8, 10]
```

### Pandas
- **O que faz:** Manipulação e análise de dados tabulares
- **Quando usar:** Ler arquivos CSV/Excel, filtrar dados, agrupar, calcular estatísticas
- **Exemplo:**
```python
import pandas as pd

df = pd.read_csv('dados.csv')
print(df.shape)             # linhas e colunas
print(df.describe())        # estatísticas básicas
print(df['coluna'].mean())  # média de uma coluna
```

### Matplotlib
- **O que faz:** Criação de gráficos estáticos
- **Quando usar:** Gráficos de linha, barra, dispersão, histogramas
- **Exemplo:**
```python
import matplotlib.pyplot as plt

plt.plot([1, 2, 3], [10, 20, 15])
plt.title('Meu Gráfico')
plt.show()
```

### Seaborn
- **O que faz:** Visualizações estatísticas mais elegantes (construído sobre Matplotlib)
- **Quando usar:** Heatmaps de correlação, boxplots, distribuições, gráficos de regressão
- **Exemplo:**
```python
import seaborn as sns

sns.heatmap(df.corr(), annot=True)
plt.show()
```

### Scikit-learn
- **O que faz:** Machine Learning — treinar e avaliar modelos
- **Quando usar:** Classificação, regressão, clustering, pré-processamento
- **Exemplo:**
```python
from sklearn.linear_model import LinearRegression

modelo = LinearRegression()
modelo.fit(X_train, y_train)
previsoes = modelo.predict(X_test)
```

---

## Módulo 4: Análise Exploratória de Dados (EDA)

EDA é o processo de "conhecer" seus dados antes de qualquer análise aprofundada. É uma das etapas mais importantes e negligenciadas por iniciantes.

### Checklist de EDA para iniciantes:

```python
# 1. Tamanho do dataset
print(df.shape)

# 2. Tipos de dados
print(df.dtypes)

# 3. Primeiras linhas
print(df.head())

# 4. Valores nulos
print(df.isnull().sum())

# 5. Estatísticas descritivas
print(df.describe())

# 6. Valores únicos por coluna categórica
print(df['categoria'].value_counts())

# 7. Correlação entre variáveis numéricas
print(df.corr())
```

---

## Módulo 5: Limpeza de Dados

Os dados do mundo real são bagunçados. Saber limpar dados é uma das habilidades mais valorizadas em Ciência de Dados.

### Problemas comuns e soluções:

| Problema | Como identificar | Como resolver |
|----------|-----------------|---------------|
| Valores nulos | `df.isnull().sum()` | `df.dropna()` ou `df.fillna(valor)` |
| Duplicatas | `df.duplicated().sum()` | `df.drop_duplicates()` |
| Tipo errado | `df.dtypes` | `df['col'].astype('int')` |
| Espaços extras | `df['col'].str.strip()` | `df['col'].str.strip()` |
| Inconsistência de texto | `df['col'].unique()` | `df['col'].str.lower()` |
