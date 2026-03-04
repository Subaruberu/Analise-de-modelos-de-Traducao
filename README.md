Estudo Comparativo de Modelos de Tradução Automática Neural
Italiano → Português em Textos Formais

Autor: Willian Fernandes Dias
Orientador: Prof. Rooney Ribeiro Albuquerque Coelho
Curso: Ciência de Dados e Inteligência Artificial – MA-7 – PUC-SP

1. Resumo e Motivação

Este Trabalho de Conclusão de Curso tem como objetivo a avaliação comparativa de modelos de Tradução Automática Neural (NMT) no par linguístico Italiano → Português, com foco específico em textos formais de alta complexidade linguística.

A pesquisa foi motivada pela necessidade de precisão terminológica e estabilidade estrutural na tradução de documentos técnicos e institucionais, além da observação de inconsistências em modelos generalistas ao lidar com o italiano formal.

Durante o estudo da língua italiana, foi identificada a ausência de um modelo amplamente validado para garantir consistência técnica, fidelidade semântica e uniformidade estilística nesse domínio específico.

2. Objetivos da Pesquisa

Construção de Corpus Paralelo:
Definir e preparar um corpus robusto Italiano-Português para avaliação sistemática.

Aplicação de Métricas Automatizadas:
Implementar métricas quantitativas como:

BLEU Score

Jaccard Index

Análise Estatística e Interpretativa:
Identificar padrões de desempenho, estabilidade e volatilidade entre os modelos avaliados.

3. Metodologia
3.1 Corpus de Referência (Ground Truth)

O corpus utilizado foi composto por documentos oficiais da Igreja Católica, especificamente a Exortação Apostólica Dilexi te, publicada pelo Vaticano.

Justificativa da Escolha:

Alta complexidade sintática

Linguagem formal e teológica

Existência de versão oficial em português

Estrutura organizada por capítulos e parágrafos

Os textos foram segmentados em parágrafos para permitir análise comparativa detalhada por unidade textual.

3.2 Modelos Avaliados

Foram analisados quatro modelos baseados na arquitetura Transformer:

Modelo	Categoria	Característica Principal
NLLB-200-distilled-600M	Multilíngue Especializado	Alta uniformidade entre 200 idiomas
Facebook M2M100-418M	Multilíngue Especializado	Tradução direta entre múltiplos pares linguísticos
FLAN-T5	Generalista (Instruction-based)	Versátil, porém menos consistente em textos formais
MBART	Multilíngue Especializado	Desempenho intermediário e estável
4. Análise Quantitativa dos Resultados
4.1 BLEU Score

A análise por parágrafo evidenciou:

Superioridade consistente:
NLLB-200 e M2M100 apresentaram os maiores valores de BLEU na maioria dos segmentos analisados.

Volatilidade do FLAN-T5:
O modelo generalista demonstrou maior instabilidade, especialmente em parágrafos extensos ou sintaticamente complexos.

4.2 Jaccard Index (Média por Modelo)
Modelo	Média Jaccard
NLLB-200	≈ 0.16
MBART	≈ 0.14
M2M100-418M	≈ 0.10
FLAN-T5	≈ 0.09

Interpretação:
O NLLB-200 apresentou maior similaridade lexical média e melhor uniformidade de desempenho.

5. Conclusão

Os resultados demonstram que:

Modelos multilíngues especializados superam modelos generalistas em textos formais.

O NLLB-200 apresentou maior estabilidade, melhor desempenho médio e maior fidelidade estrutural.

A escolha do modelo é determinante para garantir qualidade em domínios técnicos e religiosos.

Assim, conclui-se que o NLLB-200-distilled-600M é a opção mais adequada para o par Italiano → Português em textos formais.

6. Trabalhos Futuros

Para continuidade da pesquisa, propõe-se:

Treinamento com corpora específicos de domínio (religioso, jurídico, acadêmico)

Inclusão de métricas modernas como:

COMET

BLEURT

Análise de custo computacional versus desempenho

Construção de pipeline automatizado de tradução e avaliação

© 2024 – Willian Fernandes Dias
