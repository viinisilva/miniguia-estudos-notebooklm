# 🤖 Banco de Prompts — NotebookLM

Documentação completa dos prompts testados, suas variações e resultados obtidos.

---

## Como usar este arquivo

Cada prompt está organizado com:
- **Objetivo:** o que queremos extrair
- **Prompt original:** primeira tentativa
- **Resultado:** o que aconteceu
- **Problema encontrado:** dificuldade (quando houver)
- **Prompt refinado:** versão melhorada
- **Resultado final:** avaliação do que funcionou

---

## 🔹 Categoria 1: Visão Geral e Contexto

### Prompt 1.1
**Objetivo:** Entender o que é Ciência de Dados

```
O que é Ciência de Dados e por que Python é a linguagem mais usada nessa área?
```
**Resultado:** Genérico, sem citar as fontes.

**Problema:** Pergunta aberta demais.

**Refinado:**
```
Com base nas fontes carregadas, quais são as 3 principais vantagens de Python 
para Ciência de Dados em comparação com R ou Julia? Cite exemplos práticos 
de uso das bibliotecas e referencie as fontes.
```
**Resultado final:** ⭐⭐⭐⭐⭐ Excelente — citações específicas, exemplos concretos.

---

### Prompt 1.2
**Objetivo:** Entender o pipeline de Ciência de Dados

```
Quais são as etapas do pipeline de Ciência de Dados? Descreva cada uma brevemente.
```
**Resultado:** Boa resposta, mas muito teórica.

**Refinado:**
```
Descreva as etapas do pipeline de Ciência de Dados de forma sequencial, 
como se fosse um guia passo a passo para iniciantes. 
Para cada etapa, mencione: o que é feito, quais ferramentas Python são usadas 
e um exemplo simples de código ou tarefa típica.
```
**Resultado final:** ⭐⭐⭐⭐⭐ Perfeito — estruturado, prático e com exemplos.

---

## 🔹 Categoria 2: Conceitos Técnicos

### Prompt 2.1
**Objetivo:** Entender DataFrames no Pandas

```
O que é um DataFrame?
```
**Resultado:** Definição básica e curta.

**Problema:** Muito superficial para aprendizado real.

**Refinado:**
```
Explique o conceito de DataFrame no Pandas como se eu fosse um iniciante absoluto. 
Use uma analogia com planilhas do Excel, mostre como criar um DataFrame simples, 
e demonstre como: acessar colunas, filtrar linhas e calcular estatísticas básicas.
```
**Resultado final:** ⭐⭐⭐⭐⭐ Transformou um conceito abstrato em algo muito concreto.

---

### Prompt 2.2
**Objetivo:** Aprender sobre limpeza de dados

```
Como limpar dados com Pandas?
```
**Resultado:** Lista de métodos sem contexto.

**Refinado:**
```
Quais são os 5 problemas mais comuns em datasets sujos e como resolvê-los 
com Pandas? Para cada problema, mostre: como identificar, qual método usar 
e um exemplo de código. Foque no nível iniciante.
```
**Resultado final:** ⭐⭐⭐⭐ Muito bom — problemas reais com soluções práticas.

---

## 🔹 Categoria 3: Síntese e Conexão de Conceitos

### Prompt 3.1
**Objetivo:** Criar mapa conceitual

```
Crie um mapa mental dos principais conceitos de Ciência de Dados que aparecem 
nas fontes carregadas, conectando as etapas do pipeline de dados.
```
**Resultado:** ⭐⭐⭐⭐⭐ Excelente — gerou estrutura hierárquica clara e bem conectada.

---

### Prompt 3.2
**Objetivo:** Conectar NumPy e Pandas

```
Qual a relação entre NumPy e Pandas? Quando devo usar cada um?
Explique com exemplos simples e mostre como eles se complementam na prática.
```
**Resultado:** ⭐⭐⭐⭐⭐ Muito claro — analogia ótima e exemplos de código úteis.

---

## 🔹 Categoria 4: Revisão e Memorização

### Prompt 4.1 — Glossário

```
Com base em todas as fontes, gere um glossário com os 15 termos técnicos mais 
importantes de Ciência de Dados para iniciantes, em ordem de importância. 
Para cada termo: definição em 2 linhas e um exemplo de uso no contexto de Python.
```
**Resultado:** ⭐⭐⭐⭐⭐ Perfeito — cruzou as fontes e gerou definições consistentes.

---

### Prompt 4.2 — Quiz de revisão

```
Crie 5 perguntas de múltipla escolha para testar meu conhecimento sobre 
Pandas e NumPy com nível iniciante. Inclua a resposta correta e uma explicação 
de por que as outras alternativas estão erradas.
```
**Resultado inicial:** Perguntas muito simples (decoreba).

**Refinado:**
```
Crie 5 perguntas de múltipla escolha sobre Pandas e NumPy que testem 
aplicação prática, não memorização. Cada questão deve apresentar um 
cenário real (ex: "Dado esse dataset, o que acontece se você executar..."). 
Inclua gabarito com explicação detalhada. Nível: iniciante/intermediário.
```
**Resultado final:** ⭐⭐⭐⭐⭐ Muito melhor — questões situacionais e úteis.

---

## 🔹 Prompts Reutilizáveis (Templates)

```
# REVISÃO GERAL
Resuma os principais conceitos de [TEMA] abordados nas fontes, 
estruturando em: definição, por que é importante e exemplo prático.

# EXPLICAÇÃO PARA INICIANTE  
Explique [CONCEITO] como se eu tivesse 0 experiência na área.
Use uma analogia do dia a dia e um exemplo com código Python simples.

# COMPARAÇÃO DE CONCEITOS
Qual a diferença entre [CONCEITO A] e [CONCEITO B]?
Crie uma tabela comparativa com: definição, quando usar e exemplo.

# GERAÇÃO DE QUIZ
Crie 5 perguntas de múltipla escolha sobre [TEMA] com nível iniciante/intermediário.
Teste aplicação prática, não apenas memorização. Inclua gabarito comentado.

# MAPA DE ESTUDO
Liste as 10 coisas mais importantes que um iniciante deve saber sobre [TEMA],
em ordem de prioridade de aprendizado.

# TROUBLESHOOTING
Quais são os erros mais comuns que iniciantes cometem ao [TAREFA]?
Como evitá-los? Cite exemplos das fontes carregadas.

# PROJETO PRÁTICO
Sugira 3 projetos práticos para iniciantes que queiram praticar [TEMA].
Para cada projeto: objetivo, dados sugeridos, bibliotecas e dificuldade estimada.
```

---

## 📊 Tabela de Aprendizados

| Técnica | Resultado |
|---------|-----------|
| Adicionar "como se eu fosse iniciante" | ✅ Simplifica explicações complexas |
| Pedir analogias com o dia a dia | ✅ Facilita muito a compreensão |
| Especificar número de itens ("5 exemplos") | ✅ Evita respostas muito longas ou curtas |
| Pedir para "citar as fontes" | ✅ Aumenta confiabilidade da resposta |
| Usar "com base nas fontes carregadas" | ✅ Foca no material estudado |
| Perguntas muito genéricas ("O que é X?") | ❌ Gera respostas superficiais |
| Múltiplos tópicos na mesma pergunta | ❌ Confunde e dilui as respostas |
