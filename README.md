# 📊 Miniguia de Estudos: Ciência de Dados com Python

> Projeto desenvolvido como parte do Bootcamp da DIO, utilizando o **NotebookLM** como ferramenta de curadoria e síntese de conhecimento.

---

## 📌 Contexto e Objetivos

### Sobre o tema escolhido

**Ciência de Dados com Python** é uma das áreas mais requisitadas do mercado de tecnologia atualmente. Python se tornou a linguagem padrão do ecossistema de dados por sua simplicidade, comunidade ativa e ecossistema rico de bibliotecas como Pandas, NumPy, Matplotlib e Scikit-learn.

### Objetivos de estudo

- ✅ Compreender o que é Ciência de Dados e seu fluxo de trabalho (pipeline)
- ✅ Aprender os fundamentos de Python aplicados à análise de dados
- ✅ Conhecer as principais bibliotecas do ecossistema de dados em Python
- ✅ Entender os conceitos de manipulação, limpeza e visualização de dados
- ✅ Criar uma base sólida para evoluir para Machine Learning

---

## 📚 Curadoria de Fontes

As fontes abaixo foram selecionadas e carregadas no **NotebookLM** para criação do caderno temático:

| # | Fonte | Tipo | Link |
|---|-------|------|------|
| 1 | Python Data Science Handbook – Jake VanderPlas | Livro (PDF/HTML) | [acesso gratuito](https://jakevdp.github.io/PythonDataScienceHandbook/) |
| 2 | Documentação oficial do Pandas | Docs | [pandas.pydata.org](https://pandas.pydata.org/docs/getting_started/intro_tutorials/) |
| 3 | Kaggle Learn – Intro to Data Science | Curso gratuito | [kaggle.com/learn](https://www.kaggle.com/learn/intro-to-programming) |
| 4 | Real Python – Data Science Tutorials | Artigos | [realpython.com](https://realpython.com/tutorials/data-science/) |
| 5 | IBM Skills Network – Data Science Fundamentals | PDF/Artigo | [skills.network](https://skills.network) |

> 💡 **Como usar:** Acesse cada link, baixe o PDF ou copie o conteúdo da página e faça o upload direto no seu notebook no NotebookLM.

---

## 🧪 Engenharia de Prompts e "Cicatrizes"

### Prompts testados no NotebookLM

Esta seção documenta as perguntas estratégicas elaboradas, as variações testadas e as lições aprendidas.

---

#### 🔹 Prompt 1 — Visão Geral

**Pergunta inicial:**
> "O que é Ciência de Dados e por que Python é a linguagem mais usada nessa área?"

**Resposta obtida (síntese):**
O NotebookLM cruzou informações do Python Data Science Handbook com os tutoriais do Kaggle e gerou uma explicação clara, citando as fontes diretamente. A resposta destacou a simplicidade de Python, a rica coleção de bibliotecas e a comunidade ativa como os principais fatores.

**📌 Dificuldade encontrada:**
A resposta foi muito genérica na primeira tentativa. Precisei refinar o prompt.

**Prompt refinado:**
> "Com base nas fontes carregadas, quais são as 3 principais vantagens de Python para Ciência de Dados em comparação com R ou Julia? Cite exemplos práticos de uso das bibliotecas."

**Resultado:** Muito melhor — a IA passou a citar casos de uso concretos e a referenciar trechos específicos das fontes.

---

#### 🔹 Prompt 2 — Conceitos Técnicos

**Pergunta inicial:**
> "O que é um DataFrame?"

**Resposta obtida:**
Definição básica de DataFrame como estrutura tabular bidimensional do Pandas.

**📌 Dificuldade encontrada:**
Resposta superficial, sem exemplos de código ou casos de uso.

**Prompt refinado:**
> "Explique o conceito de DataFrame no Pandas como se eu fosse um iniciante absoluto. Use uma analogia com planilhas do Excel e mostre como criar, acessar e filtrar dados em um DataFrame com exemplos simples de código Python."

**Resultado:** A IA gerou uma explicação com analogia, exemplos de código e até mencionou os métodos `.head()`, `.describe()` e `.loc[]`.

---

#### 🔹 Prompt 3 — Conexão entre conceitos

**Pergunta:**
> "Crie um mapa mental dos principais conceitos de Ciência de Dados que aparecem nas fontes carregadas, conectando as etapas do pipeline de dados."

**Resultado:** Excelente! O NotebookLM gerou uma estrutura hierárquica conectando: Coleta → Limpeza → Exploração (EDA) → Modelagem → Comunicação.

---

#### 🔹 Prompt 4 — Glossário

**Pergunta:**
> "Com base em todas as fontes, gere um glossário com os 15 termos técnicos mais importantes de Ciência de Dados para iniciantes, com definição curta e exemplo de uso."

**Resultado:** Funcionou muito bem. O NotebookLM cruzou as fontes e gerou definições consistentes, sempre indicando de onde veio cada conceito.

---

#### 🔹 Prompt 5 — Geração de Quiz

**Pergunta:**
> "Crie 5 perguntas de múltipla escolha para testar meu conhecimento sobre Pandas e NumPy, com nível iniciante. Inclua a resposta correta e uma explicação."

**📌 Dificuldade encontrada:**
O NotebookLM às vezes gerava perguntas muito simples. Ajustei pedindo que as questões testassem "aplicação prática", não apenas memorização.

---

### 💡 Lições aprendidas (Troubleshooting)

| Problema | Causa | Solução |
|----------|-------|---------|
| Respostas genéricas | Prompt muito aberto | Adicionar contexto, exemplos esperados e nível de detalhe |
| Sem citação de fontes | Não solicitei explicitamente | Adicionar "cite as fontes" ou "com base nas fontes carregadas" |
| Resposta longa demais | Sem limite definido | Especificar: "em até 300 palavras" ou "em tópicos" |
| Conceitos misturados | Muitos tópicos na mesma pergunta | Dividir em perguntas menores e específicas |

---

## 📖 Miniguia de Estudo (Entrega Final)

### 1. Resumos Estruturados

#### 🔷 O que é Ciência de Dados?

Ciência de Dados é uma área interdisciplinar que combina **estatística**, **programação** e **conhecimento de domínio** para extrair insights e conhecimento a partir de dados. O objetivo é transformar dados brutos em informações que apoiem decisões.

**O pipeline de Ciência de Dados:**

```
📥 Coleta de Dados
      ↓
🔧 Limpeza e Preparação (Data Wrangling)
      ↓
🔍 Análise Exploratória (EDA)
      ↓
📊 Visualização
      ↓
🤖 Modelagem (Machine Learning)
      ↓
📣 Comunicação dos Resultados
```

---

#### 🔷 Python para Ciência de Dados — Bibliotecas Essenciais

| Biblioteca | Para que serve | Exemplo de uso |
|------------|---------------|----------------|
| **NumPy** | Operações matemáticas e arrays | Calcular médias, matrizes |
| **Pandas** | Manipulação de dados tabulares | Ler CSV, filtrar, agrupar |
| **Matplotlib** | Gráficos básicos | Gráficos de linha, barra |
| **Seaborn** | Visualizações estatísticas | Heatmaps, boxplots |
| **Scikit-learn** | Machine Learning | Classificação, regressão |

---

#### 🔷 Pandas: Conceitos Fundamentais

**Series:** Estrutura unidimensional (como uma coluna de tabela)

```python
import pandas as pd

notas = pd.Series([8.5, 7.0, 9.2, 6.8], index=['Ana', 'Bruno', 'Carla', 'Diego'])
print(notas['Ana'])  # 8.5
```

**DataFrame:** Estrutura bidimensional (como uma planilha)

```python
dados = {
    'Nome': ['Ana', 'Bruno', 'Carla'],
    'Idade': [25, 30, 22],
    'Nota': [8.5, 7.0, 9.2]
}

df = pd.DataFrame(dados)
print(df.head())       # primeiras linhas
print(df.describe())   # estatísticas básicas
print(df[df['Nota'] > 8])  # filtrar por condição
```

---

#### 🔷 Análise Exploratória de Dados (EDA)

EDA é a etapa de "conhecer" seus dados antes de qualquer análise mais profunda. Perguntas típicas de EDA:

- Quantas linhas e colunas tem o dataset? → `df.shape`
- Existem valores nulos? → `df.isnull().sum()`
- Qual a distribuição das variáveis? → `df.describe()`
- Existem outliers? → boxplot com Seaborn

---

### 2. Glossário de Conceitos

| Termo | Definição |
|-------|-----------|
| **Dataset** | Conjunto de dados organizado em linhas e colunas, base de qualquer análise |
| **DataFrame** | Estrutura de dados tabular bidimensional da biblioteca Pandas |
| **Series** | Estrutura de dados unidimensional do Pandas, equivalente a uma coluna |
| **EDA** | Análise Exploratória de Dados — processo de investigar e resumir as características de um dataset |
| **Feature** | Variável de entrada usada em modelos de Machine Learning (cada coluna do dataset) |
| **Target** | Variável que se deseja prever em um modelo preditivo |
| **Outlier** | Valor discrepante que se afasta significativamente dos demais no dataset |
| **Data Wrangling** | Processo de limpeza, transformação e preparação dos dados para análise |
| **Correlação** | Medida estatística que indica a relação entre duas variáveis (-1 a +1) |
| **Overfitting** | Quando um modelo "decora" os dados de treino e performa mal em dados novos |
| **Pipeline** | Sequência de etapas encadeadas no processo de Ciência de Dados |
| **Numpy Array** | Estrutura de dados do NumPy para operações matemáticas de alta performance |
| **Visualização de Dados** | Representação gráfica de dados para facilitar a interpretação de padrões |
| **Machine Learning** | Subárea da IA onde algoritmos aprendem padrões a partir de dados |
| **Jupyter Notebook** | Ambiente interativo para escrever e executar código Python com texto e gráficos |

---

### 3. Prompts Reutilizáveis para Revisões Futuras

Salve esses prompts no seu NotebookLM ou num arquivo de notas para usar em futuras sessões de estudo:

```
📌 REVISÃO GERAL
"Resuma os principais conceitos de [TEMA] abordados nas fontes, 
estruturando em: definição, por que é importante e exemplo prático."

📌 EXPLICAÇÃO PARA INICIANTE
"Explique [CONCEITO] como se eu tivesse 0 experiência na área. 
Use uma analogia do dia a dia e um exemplo com código Python simples."

📌 COMPARAÇÃO DE CONCEITOS
"Qual a diferença entre [CONCEITO A] e [CONCEITO B]? 
Crie uma tabela comparativa com: definição, quando usar e exemplo."

📌 GERAÇÃO DE QUIZ
"Crie 5 perguntas de múltipla escolha sobre [TEMA] com nível iniciante/intermediário.
Teste aplicação prática, não apenas memorização. Inclua gabarito comentado."

📌 MAPA DE ESTUDO
"Liste as 10 coisas mais importantes que um iniciante deve saber sobre [TEMA], 
em ordem de prioridade de aprendizado."

📌 TROUBLESHOOTING
"Quais são os erros mais comuns que iniciantes cometem ao [TAREFA]? 
Como evitá-los? Cite exemplos das fontes carregadas."

📌 APLICAÇÃO PRÁTICA
"Sugira 3 projetos práticos para iniciantes que queiram praticar [TEMA].
Para cada projeto: objetivo, dados sugeridos, bibliotecas e dificuldade estimada."
```

---

## 🗂️ Estrutura do Repositório

```
miniguia-estudos-notebooklm/
│
├── README.md                    # Este arquivo — guia principal
├── fontes/
│   └── links-e-referencias.md  # Links detalhados das fontes usadas
├── prompts/
│   └── prompts-notebooklm.md   # Banco de prompts testados e reutilizáveis
└── miniguia/
    ├── resumos.md               # Resumos estruturados por tema
    └── glossario.md             # Glossário completo de termos
```

---

## 🛠️ Ferramentas Utilizadas

- [NotebookLM](https://notebooklm.google.com/) — Curadoria e síntese das fontes
- [GitHub](https://github.com) — Versionamento e entrega do projeto
- [Python 3.x](https://python.org) — Linguagem base dos estudos

---

## 👩‍💻 Como Reproduzir Este Projeto

1. Acesse o [NotebookLM](https://notebooklm.google.com/)
2. Crie um novo notebook e dê um nome descritivo
3. Faça upload das fontes listadas na seção **Curadoria de Fontes**
4. Use os **prompts reutilizáveis** desta seção para conduzir seus estudos
5. Documente suas descobertas e dificuldades (as "cicatrizes" valem muito!)

---

## 📝 Licença

Este projeto foi desenvolvido para fins educacionais no contexto do Bootcamp DIO.

---

*Feito com 💙 e muito café durante o Bootcamp DIO*
