# 🇧🇷 🇮🇹 Estudo Comparativo de Modelos de Tradução Automática (TA)

**[Estudo Focado no Par Italiano $\rightarrow$ Português (It. $\rightarrow$ Pt.) para Textos Formais]**

[cite_start]**Autor:** Willian Fernandes Dias [cite: 4]
[cite_start]**Orientador:** Prof. Rooney Ribeiro Albuquerque Coelho [cite: 6]
[cite_start]**Curso:** Ciência de Dados e Inteligência Artificial MA-7 (PUC-SP) [cite: 4, 7]

---

## 💡 1. Resumo e Motivação

[cite_start]Este projeto de TCC tem como foco a **avaliação rigorosa de modelos de Tradução Automática Neural (NMT)**, motivado pela necessidade de **precisão formal** em textos técnicos e a **qualidade variável** entre as arquiteturas de IA[cite: 12, 14].

[cite_start]A motivação pessoal surgiu durante o estudo da língua italiana, onde foi identificada a inexistência de um modelo de tradução tecnicamente consistente para as particularidades do italiano formal[cite: 22].

### 🎯 Objetivos da Pesquisa

1.  [cite_start]**Corpus Paralelo:** Definir e preparar um *corpus* robusto de avaliação com textos Italiano-Português[cite: 39, 40].
2.  [cite_start]**Aplicação de Métricas:** Implementar métricas automatizadas (BLEU Score, Jaccard Index) para análise quantitativa[cite: 42, 158].
3.  [cite_start]**Análise de Resultados:** Interpretar dados e identificar padrões de desempenho e instabilidade entre os modelos[cite: 44].

---

## 🔬 2. Metodologia e Modelos Avaliados

### 2.1. Corpus de Referência (Ground Truth)

[cite_start]O *corpus* selecionado para os experimentos foram **Documentos Papais** (Esortazione Apostolica *Dilexi te*)[cite: 152].
* [cite_start]**Escolha Estratégica:** A seleção se deu pela **complexidade linguística**, o **caráter formal** e a existência de **versões oficiais em Português**, servindo como *ground truth* de alta fidelidade para a comparação[cite: 152, 153].
* [cite_start]**Preparação:** Os textos foram segmentados em capítulos e parágrafos para permitir uma comparação sistemática[cite: 154].

### 2.2. Arquiteturas NMT Avaliadas

[cite_start]Os segmentos textuais foram processados por três modelos amplamente utilizados em PLN, todos baseados na arquitetura Transformer[cite: 31, 156]:

| Modelo | Categoria | Descrição e Desempenho (Prévio) |
| :--- | :--- | :--- |
| **NLLB-200-distilled-600M** | Especializado (Multilíngue) | [cite_start]Modelo mais recente da Meta, projetado para alta uniformidade e estabilidade entre 200 idiomas[cite: 146]. |
| **Facebook M2M100-418M** | Especializado (Multilíngue) | [cite_start]Versão ampliada do M2M100, com suporte direto a vários pares linguísticos[cite: 146]. |
| **FLAN-T5** | Generalista (Instruction-based) | Trata tarefas de linguagem como conversão de texto. [cite_start]Apresenta **Baixa consistência** em textos formais[cite: 146]. |
| **MBART** | Especializado (Multilíngue) | [cite_start]Modelo pré-treinado em 50 idiomas com **Desempenho intermediário e estável**[cite: 146]. |

---

## 📈 3. Análise Quantitativa dos Resultados

O desempenho dos modelos foi medido através do **BLEU Score** (para acurácia de *n-gramas*) e do **Jaccard Index** (para similaridade de conjuntos de palavras).

### 3.1. Grau Comparativo de BLEU Score

A análise comparativa por parágrafo (Slides 16 e 17) demonstra um padrão claro:
* [cite_start]**Superioridade Consistente:** O **NLLB** e o **M2M100** consistentemente alcançaram as pontuações BLEU mais altas na maioria dos parágrafos, evidenciando maior fidelidade na tradução[cite: 565, 566, 617].
* [cite_start]**Volatilidade do T5:** O **FLAN-T5** (T5) apresentou o desempenho mais baixo e inconsistente, com maior perda de qualidade em parágrafos mais longos ou de maior complexidade estrutural[cite: 565, 617].

### 3.2. Média de Jaccard por Modelo

A média do Jaccard Index confirmou a ordenação de desempenho e a eficácia dos modelos especializados:

| Modelo | Média Jaccard |
| :--- | :--- |
| **NLLB** | [cite_start]Aproximadamente 0.16 [cite: 634] |
| **MBART** | [cite_start]Aproximadamente 0.14 [cite: 633] |
| **M2M100-418M** | [cite_start]Aproximadamente 0.10 [cite: 631] |
| **FLAN-T5** | [cite_start]Aproximadamente 0.09 [cite: 630] |

[cite_start]**Conclusão da Métrica:** O **NLLB-200** destacou-se em todas as métricas, atingindo o maior grau de similaridade (Jaccard: $\approx 0.16$) e alta uniformidade na tradução, validando a premissa de que a qualidade da TA é diretamente proporcional à adequação do modelo ao seu propósito[cite: 644, 646].

---

## 🚀 4. Conclusão e Próximos Passos

### Conclusão Final

[cite_start]A comparação demonstrou que, ao contrário dos modelos generalistas (FLAN-T5), os **modelos multilingues especializados (NLLB e M2M100) são indispensáveis** para garantir a fidelidade da mensagem original[cite: 643]. [cite_start]O NLLB-200 é o modelo mais adequado para o tratamento de textos formais (It. $\rightarrow$ Pt.) devido à sua comprovada estabilidade e superioridade nas métricas automáticas[cite: 646].

### Trabalhos Futuros

[cite_start]As seguintes etapas são sugeridas para dar continuidade a esta pesquisa: [cite: 647]
* [cite_start]**Treinar modelos com dados específicos do domínio:** Incluir *corpora* religiosos, jurídicos ou formais para melhorar a fidelidade terminológica[cite: 650, 651].
* [cite_start]**Avaliar novas métricas além do BLEU:** Utilizar métricas modernas, como **COMET** e **BLEURT**, que capturam melhor nuances semânticas[cite: 654].
* [cite_start]**Comparar custo vs. desempenho:** Analisar o custo computacional de cada modelo para escolher a solução mais eficiente para uso real[cite: 652, 653].
* [cite_start]**Construir um pipeline automatizado de tradução:** Criar um sistema completo, do pré-processamento à avaliação automática[cite: 649].

---

**© 2024 - Willian Fernandes Dias**# Analise-de-modelos-de-Traducao
