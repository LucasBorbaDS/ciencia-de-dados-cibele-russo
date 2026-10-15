> Material derivado das aulas da Profa. Cibele Russo (ICMC/USP), organizado com auxílio do NotebookLM. [↩ Voltar à trilha](README.md)

# Guia de Estudos: Estatística e Otimização para Ciência de Dados e Pesquisa Operacional

Este guia de estudos foi elaborado a partir das diretrizes teóricas, metodológicas e práticas do curso de atualização Estatística e Otimização para Ciência de Dados e Pesquisa Operacional (CDPO), oferecido pelo Instituto de Ciências Matemáticas e de Computação da Universidade de São Paulo (ICMC-USP, São Carlos) sob a regência dos professores Dra. Cibele Russo e Dr. Elias Helou.

## 1. Visão Geral e Síntese dos Módulos

O programa do curso integra duas grandes pilares do conhecimento voltados ao suporte à tomada de decisão e à inteligência artificial: a Estatística (para análise, caracterização e construção de modelos preditivos a partir dos dados) e a Otimização / Pesquisa Operacional (para a seleção e prescrição da decisão ótima e treinamento de algoritmos).

```text
                      ┌─────────────────────────────────────────┐
                      │              CURSO CDPO                 │
                      └────────────────────┬────────────────────┘
                                           │
             ┌─────────────────────────────┴─────────────────────────────┐
             ▼                                                           ▼
┌───────────────────────────┐                               ┌───────────────────────────┐
│        ESTATÍSTICA        │                               │        OTIMIZAÇÃO         │
├───────────────────────────┤                               ├───────────────────────────┤
│ • Estatística para        │                               │ • Otimização Contínua     │
│   Ciência de Dados        │                               │   (Linear e Não Linear;   │
│   (Análise Exploratória,  │                               │   Aprendizado Profundo,   │
│   Probabilidades,         │                               │   Fluxo Máximo, Mistura)  │
│   Inferência Clássica)    │                               │                           │
│ • Métodos Estatísticos    │                               │ • Otimização Discreta     │
│   Aplicados               │                               │   (Inteira, Caixeiro      │
│   (Não-paramétricos,      │                               │   Viajante - TSP,         │
│   Regressão Linear/       │                               │   Timetabling, Mochila,   │
│   Logística, Bayesiana)   │                               │   Multiobjetivo)          │
└───────────────────────────┘                               └───────────────────────────┘
```

## 2. Questionário de Fixação (10 Questões de Resposta Curta)

#### Questões

1. Testes de Hipóteses e Decisão Estatística: O que significa a decisão formal de "não rejeitar a hipótese nula $`(H_0)"`$ e por que a estatística rigorosa evita o uso do termo "aceitar $`H_0"?`$
2. **Modelagem de Otimização Numérica:**quais são os três componentes fundamentais que constituem um modelo de otimização matemática formal, conforme demonstrado no exemplo clássico da otimização da lata cilíndrica?
3. Processamento de Linguagem Natural (PLN): Qual é a diferença teórica e prática entre a abordagem de vetorização por Bag of Words e o uso de Word Embeddings pré-treinados (como o Glove)?
4. Testes Paramétricos versus Não Paramétricos: Em quais circunstâncias metodológicas o pesquisador deve optar por um teste não paramétrico, como o Teste de Mann-Whitney ou o Teste de Wilcoxon, em detrimento do Teste t de Student?
5. Otimização no Treinamento de Redes Neurais: De que maneira a otimização matemática contínua atua durante o processo de treinamento (fit) de uma rede neural profunda para classificação binária?
6. Análise Exploratória e Visualização de Dados: Por que o boxplot é considerado uma das representações gráficas mais completas e informativas na Análise Exploratória de Dados quantitativos?
7. Erros de Decisão Estatística ($`\alpha`$ e $`\beta`$): Como são definidos os erros do Tipo I e do Tipo II em um teste de hipóteses e qual é a dinâmica existente entre as probabilidades de ocorrência de ambos?
8. Manipulação de Dados Espaciais no Pandas/GeoPandas: Qual é a função metodológica da operação de fusão de dados (merge) na construção de mapas coropléticos para análise geográfica?
9. Modelagem Estatística de Classificação: Por que o Modelo de Regressão Logística é preferível à regressão linear simples quando a variável resposta é dicotômica (binária)?
10. Escopo da Otimização Discreta: O que caracteriza um problema no âmbito da Otimização Discreta dentro da Pesquisa Operacional e quais são alguns dos seus problemas clássicos?

## 3. Chave de Respostas do Questionário

1. Resposta: A decisão de "não rejeitar $`H_0"`$ indica que a amostra analisada não forneceu evidências estatísticas suficientes para descartar a hipótese nula sob o nível de significância $`(\alpha)`$ adotado. Evita-se o termo "aceitar $`H_0"`$ porque existem múltiplos valores populacionais plausíveis dentro da variabilidade amostral que não seriam rejeitados, tornando impossível provar que a hipótese nula é rigorosamente verdadeira a partir de uma amostra.
2. Resposta: Os três componentes fundamentais são as variáveis de decisão (como a altura a e o raio r), a função objetivo a ser minimizada ou maximizada (como a área de metal gasto) e as restrições de igualdade ou desigualdade que os parâmetros devem satisfazer (como a exigência de um volume fixo V). O modelo busca encontrar o ponto ótimo que minimiza a função objetivo sem violar nenhuma restrição.
3. Resposta: A vetorização por Bag of Words apenas contabiliza a frequência das palavras no texto de forma isolada, ignorando a ordem sintática e o contexto semântico dos termos. Já os Word Embeddings (como o Glove) mapeiam cada palavra para um vetor denso em um espaço multidimensional contínuo, preservando relações de contexto, similaridade e significado complexo entre os termos.
4. Resposta: Deve-se optar por testes não paramétricos quando a suposição de normalidade da variável contínua é violada (conforme verificado por testes como o de Shapiro-Wilk) ou quando os dados possuem natureza qualitativa ordinal. O Teste de Mann-Whitney (para amostras independentes) e o Teste de Wilcoxon (para amostras pareadas) realizam comparações populacionais baseadas em postos (ordenamento), dispensando a premissa de distribuição paramétrica.
5. Resposta: O treinamento da rede neural consiste na resolução de um problema de minimização da função de perda (como a entropia cruzada binária), que mede a discrepância entre os valores reais da base de treino e as predições do modelo. Algoritmos de otimização matemática iterativa (como Adam ou Nadam) calculam os gradientes para atualizar progressivamente os vetores de parâmetros (pesos e viéses) da rede até alcançar o ponto de perda mínima.
6. Resposta: O boxplot sintetiza em uma única figura as cinco estatísticas de ordem fundamentais (mínimo, primeiro quartil, mediana, terceiro quartil e máximo não discrepante), permitindo avaliar simultaneamente a posição central, a dispersão, a assimetria da distribuição e a presença explícita de valores discrepantes (outliers).
7. Resposta: O erro do Tipo $`I (\alpha)`$ ocorre ao rejeitar uma hipótese nula $`(H_0)`$ que é verdadeira na realidade, enquanto o erro do Tipo $`II (\beta)`$ ocorre ao não rejeitar uma $`H_0`$ que é falsa. Há um compromisso de compensação (trade-off) entre eles; por isso, na prática, fixa-se a probabilidade do erro do Tipo I (nível de significância, em geral a $`5\%`$) e busca-se maximizar o poder do teste $`(1 - \beta)`$.
8. Resposta: A função merge une dois data frames relacionando linhas com base em colunas de correspondência compartilhadas (chaves). No contexto do GeoPandas, ela associa uma base com indicadores numéricos agregados (como taxas médias de inadimplência por distrito) a uma base geográfica com as geometrias dos multipolígonos para viabilizar a renderização espacial dos dados.
9. Resposta: A regressão linear simples pode prever valores fora do intervalo [0,1], o que é inadequado para representar probabilidades. A regressão logística soluciona esse limitação ao aplicar a transformação logito sobre a probabilidade do evento de interesse, garantindo respostas limitadas entre 0 e 1 e permitindo a interpretação do efeito das variáveis por meio da razão de chances (odds ratio).
10. Resposta: A Otimização Discreta é definida por problemas cujas variáveis de decisão só podem assumir valores inteiros, combinatórios ou binários (0 ou 1). Seus problemas clássicos de Pesquisa Operacional incluem o Problema do Caixeiro Viajante (TSP), o Problema da Mochila (Knapsack Problem), o Timetabling (agendamento) e o Roteamento de Veículos.

## 4. Propostas de Questões Discursivas (Ensaios)

Instruções: Estas propostas de ensaios analíticos foram elaboradas para testar a capacidade de síntese e argumentação teórica. Não são fornecidas chaves de resposta para estas questões.

1. Complementaridade entre Análise Preditiva e Prescritiva: Disserte sobre a diferença fundamental entre "analisar/prever" (Análise Preditiva e Modelagem Estatística) e "decidir" (Pesquisa Operacional e Otimização). Utilize exemplos do texto fonte (como gestão de leitos/equipes de enfermagem, distribuição de EPIs na pandemia ou otimização de embalagens) para ilustrar como a otimização atua após a etapa estatística na tomada de decisão em cenários reais.
2. Fundamentação Epistemológica do p-valor e do Nível de Significância: Analise o papel do p-valor nos testes de hipóteses estatísticos. Aborde a sua definição probabilística rigorosa ("probabilidade de observar uma estatística tão ou mais extrema sob $`H_0"`$), a diferença metodológica entre o erro do Tipo $`I (\alpha)`$ e o erro do Tipo $`II (\beta)`$, e discuta por que limiares rígidos (como $`p = 0{,}05`$) devem ser interpretados com cautela técnica.
3. Modelagem de Linguagem para Classificação de Sentimentos: Compare criticamente duas estratégias apresentadas para a classificação binária de textos (reviews positivos/negativos): a abordagem por Bag of Words aliada à Regressão Logística Regularizada (Lasso) e o uso de Word Embeddings (Glove) integrados a Redes Neurais Profundas Recorrentes/LSTM. Considere aspectos como interpretabilidade, capacidade computacional e acurácia da predição.
4. Formulação e Simplificação de Problemas de Otimização: Com base na formulação matemática da lata cilíndrica de volume fixo V, explique como uma restrição de igualdade pode ser utilizada para eliminar variáveis e transformar um problema multivariado restrito em um problema univariado irrestrito. Discuta o papel das condições teóricas de otimalidade e as limitações de tentar resolver problemas industriais complexos por vias puramente algébricas frente aos métodos numéricos.
5. Avaliabilidade e Métricas de Desempenho em Modelos Preditivos: Explique o processo de validação de modelos de aprendizado de máquina supervisionados por meio do fracionamento de dados em conjuntos de Treinamento e Teste/Validação. Discuta a Matriz de Confusão e suas métricas derivadas (Acurácia, Sensibilidade, Especificidade, Curva ROC) e comente os riscos e distorções ao utilizar unicamente a Acurácia em conjuntos de dados altamente desbalanceados.

## 5. Glossário Completo de Termos Chave

* Acurácia (Accuracy): Métrica de avaliação de desempenho de um modelo de classificação calculada pela razão entre o número de predições corretas (soma de verdadeiros positivos e verdadeiros negativos) e o total geral de instâncias avaliadas.
* Análise Exploratória de Dados (AED): Conjunto de procedimentos estatísticos voltado a resumir, visualizar e compreender as propriedades fundamentais de uma base de dados (tendência central, variabilidade, distribuições e associações) antes de aplicar inferência ou modelagem avançada.
* Bag of Words: Método de representação simplificada de textos no qual uma frase ou documento é convertido em um vetor numérico correspondente à frequência das palavras constituintes, descartando a sintaxe e a ordem.
* Boxplot (Gráfico de Caixa): Gráfico não paramétrico estruturado sobre cinco estatísticas de ordem (mínimo, $`Q_1`$, mediana $`Q_2, Q_3`$ e máximo não discrepante). O corpo da caixa é delimitado pela amplitude interquartil $`(\text{IQR} = Q_3 - Q_1)`$, e os valores além de $`1{,}5 \times \text{IQR}`$ são denotados como outliers.
* Curso CDPO: Sigla do curso de atualização oferecido pela USP intitulado "Estatística e Otimização para Ciência de Dados e Pesquisa Operacional", focado na integração da modelagem matemática teórico-prática executada em linguagem Python.
* Entropia Cruzada Binária (Binary Cross-Entropy): Função de perda (loss function) utilizada na otimização de modelos de classificação binária. Mensura a disparidade entre a distribuição de probabilidades real e as probabilidades estimadas pelo algoritmo.
* Erro do Tipo $`I (\alpha)`$: Ocorrência estatística onde a regra de decisão leva à rejeição de uma hipótese nula $`(H_0)`$ que é verdadeira na população real. Sua probabilidade limite é definida pelo nível de significância do teste.
* Erro do Tipo $`II (\beta)`$: Ocorrência estatística na qual o teste falha em rejeitar uma hipótese nula $`(H_0)`$ que é falsa na população real.
* Função Objetivo: Expressão matemática formalizada dentro de um modelo de otimização que quantifica a meta a ser atingida — devendo ser minimizada (ex.: custo, erro de predição, área de material) ou maximizada (ex.: lucro, eficiência, taxa de recuperação).
* Glove (Global Vectors for Word Representation): Algoritmo e modelo de word embedding pré-treinado em grandes corpora de linguagem natural que transforma palavras individuais em vetores numéricos contínuos em um espaço denso, preservando semelhanças semânticas.
* Hipótese Nula $`(H_0)`$: Premissa estipulada em um teste estatístico que geralmente assume a condição de igualdade, ausência de efeito ou parâmetro populacional fixo a ser confrontado com as evidências da amostra.
* Inadimplência: Indicador categórico ou proporcional que denota o descumprimento de obrigações financeiras por parte de um devedor ou cliente dentro de um período ou carteira de crédito.
* Inferência Estatística: Ramo da estatística que fornece métodos (estimação pontual, intervalos de confiança e testes de hipóteses) para generalizar conclusões e tomar decisões sobre parâmetros de uma população inteira a partir de dados coletados em uma amostra.
* Merge (Pandas): Função da biblioteca Pandas que realiza a junção relacional (join) de dois data frames relacionando linhas com base em uma ou mais colunas que servem como chaves de ligação.
* Nadam / Adam: Algoritmos de otimização numérica baseados no cálculo do gradiente descendente stocástico. Utilizados no treinamento de redes neurais profundas para atualizar iterativamente os pesos dos neurônios e minimizar a função de perda.
* Otimização Contínua: Ramo da otimização matemática no qual as variáveis de decisão do modelo podem assumir qualquer valor real contínuo dentro de um intervalo de busca estabelecido.
* Otimização Discreta: Ramo da otimização no qual as variáveis de decisão são restritas a um conjunto discreto ou contável de valores (geralmente números inteiros ou decisões binárias 0/1).
* Outliers (Valores Discrepantes): Observações estatísticas extremamente distantes do padrão geral de concentração da amostra. Em regras de boxplot, são caracterizados por estarem posicionados a uma distância superior a $`1{,}5`$ vezes a amplitude interquartil a partir do primeiro ou terceiro quartil.
* P-valor (p-valor): Probabilidade de se obter uma estatística de teste amostral tão ou mais extrema quanto a observada, assumindo-se que a hipótese nula $`(H_0)`$ seja verdadeira. Utilizado como indicador contínuo de evidência contra $`H_0`$.
* Pesquisa Operacional (PO): Disciplina aplicada que emprega modelagem matemática, teoria dos grafos e métodos de otimização para estruturar, analisar e solucionar problemas complexos de tomada de decisão operacional e estratégica em organizações.
* Regressão Logística: Modelo estatístico supervisionado para dados em que a variável resposta é binária. Modela a probabilidade de ocorrência da classe 1 utilizando o preditor linear associado à função de ligação logito (logaritmo da razão de chances).
* Restrições (em Otimização): Conjunto de equações ou inequações matemáticas que delimitam o espaço de soluções viáveis, estabelecendo as condições físicas, econômicas ou técnicas que as variáveis de decisão devem obrigatoriamente satisfazer.
* Stopwords: Palavras gramaticais neutras de alta frequência em uma língua (como preposições, artigos e pronomes) que não agregam conteúdo semântico relevante a modelos de Processamento de Linguagem Natural e são filtradas durante o pré-processamento.
* Teste t Pareado: Teste paramétrico de hipóteses indicado para comparar as médias de duas populações ou condições quando os dados são amostrados em pares correlacionados (como medições tomadas do mesmo sujeito antes e depois de uma intervenção).
* Tokenização: Primeira fase do pré-processamento de dados textuais em Processamento de Linguagem Natural, constituída pelo fracionamento de uma cadeia contínua de texto em unidades menores (tokens), tais como palavras isoladas ou subpalavras.
