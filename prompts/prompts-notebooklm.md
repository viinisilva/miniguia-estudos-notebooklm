# 🤖 Banco de Prompts — NotebookLM

Documentação dos prompts testados, respostas reais obtidas e lições aprendidas.

---

## 🔹 Prompt 1 — Vantagens do Python para Ciência de Dados

**Pergunta enviada:**
> "Com base nas fontes carregadas, quais são as 3 principais vantagens de Python para Ciência de Dados? Cite exemplos práticos e referencie as fontes."

**Resposta obtida (síntese):**
O NotebookLM identificou três vantagens principais:

1. **Amplo ecossistema de bibliotecas** — bibliotecas como Scikit-learn permitem implementar algoritmos complexos de Machine Learning (como k-NN e Random Forest) com apenas dois comandos: `fit()` para treinar e `predict()` para prever.

2. **Eficiência no Data Wrangling** — através do Pandas, tarefas que consumiriam horas são resolvidas em uma linha. Exemplo: `fillna()` para tratar valores nulos e `drop_duplicates()` para remover registros repetidos.

3. **Facilidade de uso e legibilidade** — Python exige menos linhas de código que outras linguagens. O `read_csv()` do Pandas carrega arquivos pesados em segundos, algo que travaria o Excel com milhões de linhas.

**✅ Resultado:** Ótimo — respostas objetivas, com exemplos de código reais e referências às fontes.

**💡 Sugestões geradas pelo NotebookLM para explorar mais:**
- Como utilizar o Pandas para limpar dados de forma eficiente?
- Quais bibliotecas Python são usadas para criar modelos de Machine Learning?
- Qual é a diferença prática entre usar Python ou Excel?

---

## 🔹 Prompt 2 — O que é um DataFrame?

**Pergunta enviada:**
> "Explique o conceito de DataFrame no Pandas como se eu fosse um iniciante absoluto. Use uma analogia com planilhas do Excel e mostre exemplos simples de código."

**Resposta obtida (síntese):**
O NotebookLM usou a analogia do Excel com muita clareza:

- **Colunas** = categorias/variáveis ("Nome", "Preço", "Data")
- **Linhas** = cada registro individual (um cliente, um dia de vendas)
- **Índice** = a coluna lateral numerada que identifica cada linha

A diferença destacada em relação ao Excel: o DataFrame foi projetado para lidar com milhões de linhas sem travar, e toda a lógica fica registrada em código reprodutível.

**Exemplo de código gerado:**
```python
import pandas as pd

dados = {
    'Produto': ['Maçã', 'Banana', 'Laranja'],
    'Preço': [5.50, 3.20, 4.80],
    'Estoque': [10, 25, 12]
}

df = pd.DataFrame(dados)
print(df.head())

# Carregando de um arquivo
df_vendas = pd.read_csv("vendas.csv")
print(df_vendas.shape)
df_vendas.info()
```

**✅ Resultado:** Excelente — a analogia com Excel foi perfeita para iniciantes, e os exemplos de código são práticos e reais.

**💡 Sugestões geradas pelo NotebookLM para explorar mais:**
- Quais são as melhores bibliotecas para visualização de dados?
- Como o Pandas lida com milhões de linhas de dados?
- Qual a diferença entre uma Series e um DataFrame?

---

## 🔹 Prompt 3 — Glossário de Termos

**Pergunta enviada:**
> "Com base em todas as fontes, gere um glossário com os 15 termos mais importantes de Ciência de Dados para iniciantes, com definição curta e exemplo de uso."

**Resposta obtida:**
O NotebookLM gerou um glossário completo cruzando todas as fontes. Os 15 termos cobertos foram:

| # | Termo | Destaque da definição |
|---|-------|----------------------|
| 1 | Ciência de Dados | Área multidisciplinar para extrair insights de grandes bases de dados |
| 2 | Data Wrangling | Coletar, limpar e transformar dados brutos para análise |
| 3 | DataFrame | Tabela bidimensional do Pandas, similar a planilha Excel |
| 4 | Series | Array unidimensional do Pandas — equivale a uma coluna |
| 5 | Machine Learning | Algoritmos que aprendem padrões para fazer previsões |
| 6 | Limpeza de Dados | Remover erros, duplicatas e tratar valores ausentes |
| 7 | Outliers | Valores que fogem drasticamente do padrão do dataset |
| 8 | Acurácia | Proporção de acertos de um modelo em relação ao total |
| 9 | Classificação | Tarefa de ML para atribuir categorias a novos dados |
| 10 | Clustering | Agrupar dados por similaridade sem rótulos prévios |
| 11 | Big Data | Volumes enormes de dados que exigem tecnologias especiais |
| 12 | Mediana | Valor central de um conjunto — mais resistente a outliers que a média |
| 13 | Média | Soma dos valores dividida pelo total de observações |
| 14 | Histograma | Gráfico de distribuição de frequências de um atributo numérico |
| 15 | Atributo (Feature) | Cada coluna do dataset que descreve uma característica do objeto |

**✅ Resultado:** Muito bom — definições consistentes com exemplos do mundo real (streaming, filtro de spam, imóveis).

---

## 📊 Tabela de Aprendizados (Troubleshooting)

| O que funcionou bem | Por quê |
|---------------------|---------|
| Pedir para "citar as fontes" | Aumentou a confiabilidade e rastreabilidade das respostas |
| Usar "com base nas fontes carregadas" | Focou o NotebookLM no material estudado, sem inventar |
| Pedir analogias ("como se fosse iniciante") | Gerou explicações muito mais didáticas e acessíveis |
| Especificar número de itens ("15 termos") | Controlou o tamanho da resposta e evitou listas gigantes |
| Pedir exemplos de código junto com a teoria | Tornou o aprendizado muito mais prático e aplicável |

---

## 📌 Prompts Reutilizáveis para Revisões Futuras

```
# REVISÃO GERAL
Com base nas fontes carregadas, resuma os principais conceitos de [TEMA],
estruturando em: definição, por que é importante e exemplo prático.

# EXPLICAÇÃO PARA INICIANTE
Explique [CONCEITO] como se eu tivesse 0 experiência na área.
Use uma analogia do dia a dia e um exemplo com código Python simples.

# COMPARAÇÃO DE CONCEITOS
Qual a diferença entre [CONCEITO A] e [CONCEITO B]?
Crie uma tabela comparativa com: definição, quando usar e exemplo.

# GERAÇÃO DE QUIZ
Crie 5 perguntas de múltipla escolha sobre [TEMA] que testem aplicação
prática, não memorização. Inclua gabarito com explicação. Nível iniciante.

# MAPA DE ESTUDO
Liste as 10 coisas mais importantes que um iniciante deve saber sobre [TEMA],
em ordem de prioridade de aprendizado.

# TROUBLESHOOTING
Quais são os erros mais comuns que iniciantes cometem ao [TAREFA]?
Como evitá-los? Cite exemplos das fontes carregadas.
```
