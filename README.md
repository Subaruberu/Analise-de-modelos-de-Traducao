# Tradução Automática Neural e Aperfeiçoamento Linguístico: Um Estudo Comparativo de Modelos Open-Source no Par Italiano-Português

**Trabalho de Conclusão de Curso — Ciência de Dados e Inteligência Artificial, PUC-SP**
Orientação: Eric Bacconi Gonçalves e Rooney Ribeiro Albuquerque Coelho

## Contexto e problema

A avaliação de qualidade em tradução automática costuma depender de métricas automáticas (BLEU, RTT) que nem sempre capturam nuances culturais e semânticas — especialmente em pares linguísticos como italiano-português, onde proximidade lexical pode mascarar erros de tradução. Este trabalho comparou quatro modelos open-source de tradução neural em quatro tipos de texto com características linguísticas distintas.

## Modelos avaliados

- **M2M100**
- **T5 / Flan-T5**
- **NLLB-200**
- **mBART**

## Corpus de teste

Quatro gêneros textuais deliberadamente heterogêneos, escolhidos para estressar diferentes capacidades dos modelos:

| Tipo de texto | Exemplo | Desafio principal |
|---|---|---|
| Religioso/formal | Dei Verbum (documento papal) | Registro formal, terminologia teológica |
| Poético | L'Infinito (Leopardi) | Ambiguidade, métrica, licença poética |
| Musical | Bella Ciao | Coloquialismo, repetição, ritmo |
| Jornalístico | Notícia contemporânea | Terminologia técnica/atual, objetividade |

## Instrumentos desenvolvidos

Além das métricas padrão de mercado, o trabalho propôs instrumentos próprios de avaliação:

- **IFC (Índice de Fidelidade Cultural)** — mede o quanto a tradução preserva referências e conotações culturais do texto-fonte, não capturadas por métricas puramente lexicais.
- **RTT (Round-Trip Translation)** — tradução de ida e volta como proxy de fidelidade semântica.
- **Heatmap de erros** — visualização comparativa dos padrões de erro por modelo e por tipo de texto, permitindo identificar onde cada arquitetura falha sistematicamente.

## Achado central: falsa positividade métrica

Um dos resultados mais relevantes do trabalho foi identificar um caso de **RTT = 100 no texto poético traduzido pelo T5**, aparentemente um resultado perfeito. A análise qualitativa revelou que o modelo havia produzido uma tradução *off-target* (fora do par linguístico esperado), e o ciclo de ida-e-volta "corrigia" artificialmente o erro, mascarando uma falha real do modelo por trás de uma métrica aparentemente ótima.

Esse achado ilustra um risco metodológico importante: **métricas de tradução automática podem ser enganosas quando usadas isoladamente**, reforçando a necessidade de avaliação qualitativa complementar — motivação direta por trás do IFC e do heatmap de erros propostos neste trabalho.

## Stack técnica

Python · Hugging Face Transformers · Jupyter Notebooks · modelos M2M100/T5/NLLB-200/mBART · visualização de dados para o heatmap de erros

## Principais competências demonstradas

- Design experimental controlado (mesmo corpus, múltiplos modelos, múltiplas dimensões de avaliação)
- Criação de métricas customizadas quando as métricas de mercado se mostraram insuficientes
- Análise crítica de resultados quantitativos (identificação de falsos positivos metodológicos)
- Comunicação técnica de achados complexos para banca examinadora
