> Material derivado das aulas da Profa. Cibele Russo (ICMC/USP), organizado com auxílio do NotebookLM. [↩ Voltar à trilha](README.md)

# Guia de Estudo: Visualização e Exploração de Dados em R e Python

Este guia de estudo oferece uma síntese abrangente e estruturada do conteúdo sobre representação, visualização e exploração de dados quantitativos e qualitativos, utilizando as linguagens de programação R e Python. O material abrange desde o cálculo manual de estatísticas descritivas até técnicas avançadas de representação multidimensional, medidas de desigualdade e testes de associação.

#### Questionário de Revisão (Quiz)

#### Questões de Resposta Curta

1. Qual é a diferença conceitual e estrutural entre o gráfico de barras e o histograma na representação de dados?
2. Como transformações afins nas variáveis (do tipo $`u = \frac{x-a}{b}`$ e $`v = \frac{y-c}{d}`$) afetam o Coeficiente de Correlação Linear de Pearson?
3. O que é a Curva de Lorenz e como ela é utilizada para interpretar a distribuição de uma variável como a renda?
4. No software R, qual é a finalidade do comando par(mfrow = c(2, 2)) na fase de construção visual?
5. O que representa a métrica de Discrepância Máxima $`(L_{max})`$ no contexto da Curva de Lorenz e como ela se relaciona com a média dos dados?
6. Ao analisar um histograma ou gráfico de densidade de salários de uma empresa, o que a presença de múltiplos picos (multimodalidade) costuma indicar?
7. Qual a estratégia de estruturação de dados exigida pelo pacote ggplot2 em R para gerar visualmente uma Pirâmide Etária?
8. O que caracteriza um gráfico de mapa de árvore (Treemap) e para qual estrutura de dados ele é indicado?
9. No contexto dos momentos amostrais centrais, qual é a definição do primeiro e do segundo momento central em relação à média?
10. Quais são os pacotes em Python mencionados para a geração automatizada de relatórios visuais e estatísticos de Análise Exploratória de Dados (EDA)?

#### Gabarito do Questionário

1. O gráfico de barras é utilizado para variáveis qualitativas ou quantitativas discretas, apresentando barras separadas entre si. O histograma é indicado para variáveis quantitativas contínuas organizadas em intervalos de classe (faixas), apresentando retângulos adjacentes (unidos) onde a área corresponde à frequência ou densidade.
2. A magnitude absoluta do coeficiente de correlação de Pearson não se altera sob transformações afins. O sinal da correlação permanece o mesmo se o produto dos fatores de escala $`(b \cdot d)`$ for positivo, e inverte o sinal (torna-se o oposto) se o produto dos fatores for negativo.
3. A Curva de Lorenz é uma representação gráfica da proporção acumulada de posições $`(p_i)`$ versus a proporção acumulada de valores $`(q_i)`$ de um conjunto de dados ordenados. Quanto mais próxima a curva estiver da reta de identidade (diagonal de 0 a 1), mais igualitária é a distribuição da variável.
4. O comando par(mfrow = c(2, 2)) configura a janela gráfica do R para dispor quatro gráficos simultâneos em um único painel, organizado em uma matriz de duas linhas e duas colunas.
5. A Discrepância Máxima $`(L_{max})`$ mede a maior distância vertical entre a reta de igualdade perfeita e a Curva de Lorenz. O ponto de maior discrepância ocorre no último valor ordenado do conjunto de dados que é menor ou igual à média aritmética da amostra.
6. A presença de múltiplos picos em distribuições contínuas sugere fortemente a existência de subgrupos heterogêneos não identificados na análise univariada (por exemplo, salários diferenciados por tipo de empresa ou gênero).
7. A pirâmide etária exige a composição de dois gráficos de barras adjacentes ou espelhados por sexo, nos quais os valores de frequência de um dos gêneros (frequentemente o masculino) são transformados em números negativos, permitindo a inversão do eixo via coord_flip().
8. O Treemap exibe dados organizados de forma hierárquica por meio de retângulos aninhados. O tamanho de cada retângulo representa uma variável quantitativa de volume (como a população), enquanto a intensidade da cor representa uma segunda métrica (como a renda per capita).
9. O primeiro momento amostral central é sempre igual a zero $`(m_1 = 0)`$, pois representa a soma dos desvios em relação à média dividida por n. O segundo momento amostral central $`(m_2)`$ corresponde à variância da amostra (dividida por n).
10. Os pacotes mencionados são o pandas-profiling (chamado via método .profile_report()) e o sweetviz (executado via sv.analyze()), ambos gerando relatórios completos em formato HTML.

#### Questões para Dissertação (Sem Gabarito)

1. Assimetria e Medidas de Tendência Central: Discuta o comportamento relativo da média, mediana e moda em distribuições simétricas, assimétricas à direita e assimétricas à esquerda. Explique como a presença de outliers afeta essas estatísticas e demonstre o cálculo da assimetria com base nos momentos centrais amostrais.
2. Transformação de Variáveis e Propriedade de Invariância da Correlação: Apresente matematicamente a demonstração de que o Coeficiente de Correlação Linear de Pearson entre duas variáveis transformadas $`u_i`$ = a $`\cdot x_i + b`$ e $`v_i = c \cdot y_i + d`$ mantém-se equivalente à correlação original $`r_{xy}`$, destacando o papel dos sinais de a e c e as propriedades da covariância e variância amostrais.
3. Análise de Dados Multidimensionais e Condicionamento Visual: Compare o uso de gráficos de dispersão condicionados (como as funções coplot e xyplot do pacote lattice em R) com representações tridimensionais (como 3D Scatterplot e 3D Bubble Plot). Quais são as vantagens e limitações de condicionar variáveis quantitativas por fatores qualitativos ou por faixas (shingles)?
4. Mensuração Teórica e Prática da Desigualdade: Detalhe a formalização matemática do Índice de Gini a partir da área entre a linha de igualdade perfeita e a Curva de Lorenz. Explique a fórmula computacional baseada nos valores acumulados $`q_i`$ e discuta por que dois conjuntos de dados com distribuições visuais distintas podem resultar no mesmo valor do Índice de Gini.
5. Estrutura de Análise Exploratória Bivariada em Python: Descreva o fluxo de trabalho para investigar a associação entre variáveis para os três cenários possíveis: (a) Qualitativa vs. Qualitativa, (b) Qualitativa vs. Quantitativa, e (c) Quantitativa vs. Quantitativa. Detalhe os gráficos (mosaico, barras empilhadas, boxplots, violinos, dispersão) e os testes ou estatísticas associadas a cada cenário no ecossistema Pandas/Seaborn/SciPy.

#### Glossário de Termos Técnicos

| Termo | Definição Baseada nas Fontes |
|---|---|
| Amplitude Interquartil (IQR) | Medida de dispersão dada pela diferença entre o terceiro e o primeiro quartil $`(Q_3 - Q_1)`$. Representa o intervalo ocupado pelos 50% centrais dos dados organizados. |
| Assimetria (Skewness) | Parâmetro que indica o grau de desvio de uma distribuição em relação à simetria. É positiva quando a cauda direita é mais longa (média > mediana > moda) e negativa quando a cauda esquerda é mais longa. |
| Barreira Interna (Fence) | Limites calculados no boxplot ($`Q_1 - 1,5 \times IQR`$ e $`Q_3 + 1,5 \times IQR`$) para identificar potenciais outliers (pontos atípicos). |
| Boxplot (Gráfico de Caixa) | Representação visual baseada no resumo de cinco números (mínimo, $`Q_1`$, mediana, $`Q_3`$, máximo não atípico) que evidencia posição, dispersão, assimetria e pontos atípicos. |
| Coplot (Gráfico Condicionado) | Matriz de gráficos de dispersão onde a relação entre duas variáveis quantitativas é exibida em painéis condicionados às faixas ou categorias de uma terceira variável. |
| Covariância Amostral | Medida da dependência linear entre duas variáveis quantitativas. Indica se desvios positivos em relação à média de uma variável estão associados a desvios positivos ou negativos na outra. |
| Curva de Lorenz | Gráfico que relaciona a proporção acumulada da população $`(p_i)`$ com a proporção acumulada de uma variável acumulável ($`q_i`$, como renda ou patrimônio). |
| Curtose (Kurtosis) | Métrica que descreve o grau de achatamento da distribuição de dados em comparação com a distribuição normal. Distribuições podem ser leptocúrticas (mais afuniladas), mesocúrticas (normal) ou platicúrticas (mais achatadas). |
| Densidade Alisada (KDE) | Estimativa não paramétrica da função densidade de probabilidade de uma variável contínua, gerando uma curva suave sobre o histograma. |
| Discrepância Máxima $`(L_{max})`$ | Maior distância vertical observada entre a reta de igualdade perfeita e a Curva de Lorenz. Ocorre exatamente no valor ordenado correspondente à média dos dados. |
| Gráfico de Mosaico | Técnica gráfica para variáveis qualitativas onde a área de cada retângulo é proporcional à frequência conjunta de duas ou mais variáveis categóricas. |
| Gráfico de Ramos e Folhas | Representação semigráfica para dados quantitativos pequenos que preserva os valores numéricos originais, dividindo cada dado em um "ramo" (dígito inicial) e uma "folha" (dígito final). |
| Gráfico de Violino | Combinação de um boxplot com a estimativa de densidade alisada espelhada em ambos os lados, permitindo visualizar a multimodalidade e a densidade dos dados. |
| Heatmap (Mapa de Calor) | Matriz bidimensional que utiliza uma escala de cores graduais para representar magnitudes numéricas, frequentemente combinada com dendrogramas para agrupamento (clustering). |
| Índice de Gini | Métrica de desigualdade calculada como o dobro da área entre a reta de igualdade perfeita e a Curva de Lorenz. Varia de 0 (igualdade absoluta) até 1 - 1/n (desigualdade máxima). |
| Média Aparada (Trimmed Mean) | Média aritmética calculada após a remoção de uma porcentagem fixa das menores e maiores observações ordenadas, reduzindo a sensibilidade a outliers. |
| Média Harmônica | Inverso da média aritmética dos inversos dos valores de um conjunto de dados. É indicada para calcular taxas e velocidades médias. |
| Momento Amostral Central | Média dos desvios elevados à potência k em relação à média aritmética amostral $`(m_k = \frac{1}{n}\sum (x_i - \bar{x})^k)`$. |
| Ogiva | Polígono de frequências acumuladas de uma variável quantitativa contínua. |
| Pareto Chart | Gráfico de barras ordenado de forma decrescente por frequências, acompanhado por uma linha indicando a porcentagem acumulada do total. |
| Teste Qui-Quadrado de Independência | Teste estatístico não paramétrico aplicado a tabelas de dupla entrada para verificar se existe associação significativa entre duas variáveis qualitativas. |
| Treemap | Gráfico hierárquico que utiliza retângulos subdivididos para representar variáveis de volume e intensidade por meio de tamanho e cor. |
