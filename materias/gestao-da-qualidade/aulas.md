> Material derivado das aulas da Profa. Cibele Russo (ICMC/USP), organizado com auxílio do NotebookLM. [↩ Voltar à trilha](README.md)

# Guia de Estudo: Gestão da Qualidade e Controle Estatístico de Processos

Este guia de estudo foi estruturado para consolidar os conhecimentos teóricos, operacionais e estatísticos sobre a Gestão da Qualidade e o Controle Estatístico de Processos (CEP), combinando definições conceituais, formulações matemáticas, aplicações computacionais (em R e Python) e o contexto histórico das metodologias da qualidade.

## 1. Síntese Teórica do Conteúdo

#### Conceitos Fundamentais e Dimensões da Qualidade

#### A qualidade pode ser definida sob três perspectivas principais:

1. Adequação ao uso: Captação das necessidades do cliente e conformidade do produto/serviço ao fim a que se destina.
2. Relação inversa com a variabilidade: A qualidade é inversamente proporcional à variabilidade. Quanto menor a variação nas características de um produto, maior a sua qualidade.
3. Redução do desperdício: A melhoria da qualidade consiste na redução contínua da variabilidade nos processos, minimizando perdas de tempo, custos, matéria-prima e esforço humano.

As dimensões da qualidade englobam: desempenho, confiabilidade, durabilidade, assistência técnica, estética, características secundárias, qualidade percebida e conformidade com as especificações.

#### Existem diferenças cruciais entre os limites do processo e do projeto:

* Limites de Especificação (LIE e LSE): Definidos externamente pelo cliente, projeto engenheirado ou funcionalidade do produto. Não são calculados probabilisticamente.
* Limites de Controle (LIC e LSC): Calculados estatisticamente a partir do comportamento natural e da variabilidade inerente ao processo.

#### Evolução Histórica e Filosofias da Qualidade

* W. Edwards Deming: Teve papel fundamental na reconstrução do parque industrial japonês pós-Segunda Guerra Mundial. Enfatizou que a melhoria da qualidade exige o gerenciamento de todo o processo e o engajamento da alta gerência, em vez da simples inspeção final.
* Joseph M. Juran: Um dos criadores do Controle Estatístico do Processo (CEP) e coautor do Quality Control Handbook. Enfatizou a gestão do processo e a trípode do planejamento, controle e melhoria.
* Armand Feigenbaum: Introduziu o Controle da Qualidade Total (Total Quality Management - TQM), argumentando que a qualidade deve envolver toda a estrutura organizacional em 19 passos, dos quais os métodos estatísticos constituem apenas uma das etapas.
* Histórico de Ferramentas: Desde a divisão do trabalho de Frederick Taylor e os padrões de tempo de Frank Gilbreth, passando pelas cartas de controle de Walter Shewhart (década de 1920) e amostragem de aceitação de Dodge e Romig, até a consolidação das normas ISO 9000/9001 e o surgimento do programa Seis Sigma na Motorola (década de 1980).

#### Filosofia Seis Sigma e Estrutura DMAIC

O programa Seis Sigma visa reduzir a variação de forma que os limites de especificação estejam localizados a seis desvios-padrão $`(\pm 6\sigma)`$ de distância da média do processo.

* Desempenho Probabilístico (Distribuição Normal):
  * $`\pm 1\sigma: 68,27\%`$ de conformidade; 317.300 partes por milhão (PPM) defeituosas.
  * $`\pm 2\sigma: 95,45\%`$ de conformidade; 45.500 PPM defeituosas.
  * $`\pm 3\sigma: 99,73\%`$ de conformidade; 2.700 PPM defeituosas $`(0,27\%)`$.
  * $`\pm 6\sigma: 99,9999998\%`$ de conformidade; 0,002 PPM defeituosas (ou 3,4 PPM considerando o deslocamento típico da média).
* Estrutura DMAIC:
  * Define (Definir): Identificar o cliente, suas necessidades/expectativas (CTQ - Critical to Quality), escopo do projeto e fluxo do processo.
  * Measure (Medir): Desenvolver plano de coleta de dados, validar o sistema de medição e mapear o desempenho atual em nível Sigma.
  * Analyze (Analisar): Analisar dados para identificar causas-raiz de variações, lacunas de desempenho e capacidade do processo.
  * Improve (Melhorar): Desenvolver, testar e implementar soluções para eliminar as causas-raiz de falhas.
  * Control (Controlar): Estabelecer padrões de monitoramento contínuo (cartas de controle, procedimentos à prova de erro) para manter os ganhos.

#### Níveis de Capacitação (Belts):

* White Belt: Principiante na filosofia Seis Sigma.
* Yellow Belt: Conhecimento básico das ferramentas e suporte aos projetos.
* Green Belt: Domínio intermediário, executa projetos de melhoria locais.
* Black Belt: Especialista faixa-preta, lidera projetos complexos de alta relevância.
* Master Black Belt: Nível estratégico, treina e orienta os Black Belts e gerencia o programa na organização.

#### Análise de Custos da Qualidade e Princípio de Pareto

#### Os custos da qualidade dividem-se em quatro categorias centrais:

1. Custos de Prevenção: Investimentos para evitar defeitos e peças não conformes (ex.: treinamento, projeto do processo).
2. Custos de Avaliação: Gastos com inspeção, medição, auditoria e testes de produtos/materiais.
3. Custos de Falha Interna: Prejuízos identificados antes da entrega do produto ao cliente (ex.: refugo/sucata, retrabalho).
4. Custos de Falha Externa: Prejuízos decorrentes de falhas identificadas após a entrega ao cliente (ex.: garantias, recalls, perda de reputação).

O Princípio de Pareto (Regra 80/20) estabelece que a maior parte dos custos e perdas decorre de um número reduzido de causas essenciais. O Diagrama de Pareto ordena os defeitos da maior para a menor frequência/custo, direcionando prioridade às falhas mais impactantes.

## 2. Cartas de Controle Estatístico de Processo

```text
+-------------------------------------------------------------------------+
|                  Classificação das Cartas de Controle                   |
+------------------------------------+------------------------------------+
|            Variáveis               |             Atributos              |
|  (Medidas Contínuas)               |  (Contagens / Discretos)           |
+------------------------------------+------------------------------------+
| • X-barra e R (Amostras pequenas)  | • Carta p (Fração não conforme)    |
| • X-barra e S (Amostras grandes/var)| • Carta np (Número de não conf.)   |
| • CUSUM (Pequenos deslocamentos)   | • Carta c (Número de defeitos)     |
| • EWMA (Deslocamentos suaves)      | • Carta u (Defeitos por unidade)   |
| • T² de Hotelling (Multivariado)   |                                    |
+------------------------------------+------------------------------------+
```

#### Cartas por Variáveis

* Gráfico $`\bar{X}`$ e R: Utilizado quando o tamanho da amostra n é pequeno ($`n \le 10`$ ou 12). A média das amostras $`\bar{X}`$ monitora a tendência central, e a amplitude R monitora a variabilidade do processo. $`\text{Linha Central (LC)} = \bar{\bar{X}}, \quad \text{LSC} = \bar{\bar{X}} + A_2 \bar{R}, \quad \text{LIC} = \bar{\bar{X}} - A_2 \bar{R}`$
* Gráfico $`\bar{X}`$ e S: Preferível quando o tamanho da amostra n é moderado ou grande (n > 10 ou 12) ou quando n é variável. O desvio-padrão amostral S é estatisticamente mais eficiente que a amplitude R. Como S é um estimador viesado para o desvio-padrão populacional $`\sigma`$, utiliza-se a constante $`c_4 (E(S) = c_4 \sigma). \text{Para o gráfico }`$ $`S: \quad \text{LC} = \bar{S}, \quad \text{LSC} = B_4 \bar{S}, \quad \text{LIC} = B_3 \bar{S} \text{Para o gráfico } \bar{X}: \quad \text{LC} = \bar{\bar{X}}, \quad \text{LSC} = \bar{\bar{X}} + A_3 \bar{S}, \quad \text{LIC} = \bar{\bar{X}} - A_3 \bar{S}`$

#### Cartas por Atributos

* Gráfico de Fração Não Conforme (Gráfico p): Utilizado para dados do tipo Bernoulli ($`1 = \text{não conforme}`$, $`0 = \text{conforme}`$). Seja p a proporção de itens defeituosos e $`\hat{p} = \bar{p}`$ a estimativa obtida das amostras piloto de tamanho $`n: \text{LC} = \bar{p}, \quad \text{LSC} = \bar{p} + 3 \sqrt{\frac{\bar{p}(1-\bar{p})}{n}}, \quad \text{LIC} = \max\left(0, \bar{p} - 3 \sqrt{\frac{\bar{p}(1-\bar{p})}{n}}\right)`$

#### Cartas para Pequenos Deslocamentos e Avançadas

* CUSUM (Somas Cumulativas): Acumula desvios da média em relação ao valor-alvo $`\mu_0`$, sendo altamente eficaz na detecção rápida de pequenas mudanças (entre $`0,5\sigma`$ e $`1,5\sigma`$).
  * CUSUM Tabular: Monitora $`C_i^+`$ (desvios positivos) e $`C_i^-`$ (desvios negativos) com parâmetro de referência K e limite de decisão H.
  * Máscara V: Procedimento gráfico ajustado sobre os pontos acumulados para identificar pontos fora do controle quando ultrapassam os braços da máscara.
* EWMA (Média Móvel Exponencialmente Ponderada): Aplica pesos decrescentes geometricamente às observações passadas, priorizando as observações mais recentes: $`Z_i = \lambda X_i + (1-\lambda) Z_{i-1}, \quad \lambda \in (0`$, 1] Possui limites de controle variáveis que convergem para um estado estacionário à medida que o índice i cresce.
* Gráfico Multivariado ($`T^2`$ de Hotelling): Utilizado quando p características da qualidade correlacionadas são monitoradas simultaneamente. $`\text{Estatística: } T^2 = n (\bar{\mathbf{X}} - \boldsymbol{\mu}_0)^T \boldsymbol{\Sigma}^{-1} (\bar{\mathbf{X}} - \boldsymbol{\mu}_0)`$ Nas Fases 1 e 2 de monitoramento, utiliza-se o vetor de médias amostrais $`\bar{\bar{\mathbf{X}}}`$ e a matriz de variâncias e covariâncias combinada $`\mathbf{S}`$, ajustando os limites de controle pela distribuição F de Snedecor.

## 3. Análise do Sistema de Medição (MSA) via ANOVA

Para garantir que a variação observada nos dados venha do processo e não do instrumento de medição, realiza-se o estudo de R&R (Repetitividade e Reprodutibilidade).

* Modelo com Dois Fatores Aleatórios e Interação: $`y_{ijk} = \mu + P_i + O_j + (PO)_{ij} + \epsilon_{ijk}`$ Em que $`P_i \sim N(0, \sigma^2_P)`$ representa a peça, $`O_j \sim N(0, \sigma^2_O)`$ o operador, $`(PO)_{ij} \sim N(0, \sigma^2_{PO})`$ a interação peça-operador e $`\epsilon_{ijk} \sim N(0, \sigma^2_e)`$ o erro experimental.
* Decomposição da Variância Total: $`\sigma^2_{\text{total}} = \sigma^2_{\text{peça}} + \sigma^2_{\text{medidor}} \sigma^2_{\text{medidor}} = \sigma^2_{\text{repetitividade}} + \sigma^2_{\text{reprodutibilidade}} = \sigma^2_e + \left(\sigma^2_O + \sigma^2_{PO}\right)`$
* Razão de Precisão sobre Tolerância (P/T Ratio): $`P/T = \frac{6 \hat{\sigma}_{\text{medidor}}}{\text{LSE} - \text{LIE}}`$ Critério de Aceitação: Valores de $`P/T \le 0,10 (10\%)`$ indicam um sistema de medição excelente e adequado. Valores acima de $`0,30 (30\%)`$ são considerados inaceitáveis.

## 4. Questionário de Avaliação (10 Perguntas Curtas)

#### Pergunta 1

Como a qualidade é definida sob a perspectiva estatística e qual a sua relação com a variabilidade dos processos?

#### Pergunta 2

Quais são as diferenças de aplicação entre as cartas de controle de $`\bar{X}-R`$ e $`\bar{X}-S?`$

#### Pergunta 3

O que caracteriza um processo operando no nível Seis Sigma em termos de percentual de conformidade e partes por milhão (PPM) defeituosas?

#### Pergunta 4

Qual é o procedimento adotado ao identificar causas atribuíveis em pontos fora dos limites de controle na Fase 1 da construção de uma carta de controle?

#### Pergunta 5

Como diferem as abordagens e contribuições centrais de W. Edwards Deming, Joseph Juran e Armand Feigenbaum para a gestão da qualidade?

#### Pergunta 6

Quais são as quatro categorias centrais dos custos da qualidade e como o Princípio de Pareto auxilia em sua gestão?

#### Pergunta 7

Por que os gráficos de controle CUSUM e EWMA são superiores às cartas tradicionais de Shewhart para a detecção de pequenos deslocamentos na média?

#### Pergunta 8

No contexto do estudo do Sistema de Medição (MSA) via ANOVA, como são conceituadas e decompostas a repetitividade e a reprodutibilidade?

#### Pergunta 9

Por que o monitoramento isolado por cartas univariadas pode falhar ao avaliar múltiplas características de qualidade correlacionadas, e como a estatística $`T^2`$ de Hotelling resolve essa limitação?

#### Pergunta 10

Como a independência probabilística das componentes afeta a taxa de conformidade do produto final em sistemas compostos por múltiplos elementos?

## 5. Gabarito das Perguntas Curtas

#### Resposta 1

Sob a perspectiva estatística, a qualidade é inversamente proporcional à variabilidade. Isso significa que quanto menor a variação observada nas características de um produto ou serviço, maior será a sua qualidade. A melhoria contínua consiste em aplicar ferramentas estatísticas para identificar, gerenciar e reduzir progressivamente a variação dos processos.

#### Resposta 2

As cartas de $`\bar{X}-R`$ utilizam a amplitude para estimar a variabilidade, sendo recomendadas para amostras pequenas $`(n \le 10)`$. Já as cartas de $`\bar{X}-S`$ utilizam o desvio-padrão amostral, sendo preferíveis para amostras moderadas ou grandes (n > 10) ou quando o tamanho amostral é variável. O desvio-padrão amostral preserva a eficiência estatística e reduz a sensibilidade a valores extremos em amostras maiores.

#### Resposta 3

Um processo no nível Seis Sigma preconiza que os limites de especificação estejam posicionados a seis desvios-padrão $`(\pm 6\sigma)`$ da média. Considerando uma distribuição normal bilateral ideal, isso equivale a $`99,9999998\%`$ de produtos dentro das especificações e uma taxa de falhas de apenas 0,002 partes por milhão (PPM). Em cenários práticos com deslocamento da média de $`1,5\sigma`$, a taxa de falhas resultante é de 3,4 PPM.

#### Resposta 4

Na Fase 1, quando um ponto ultrapassa os limites de controle e uma causa atribuível é identificada (como falha mecânica, lote de matéria-prima alterado ou operador inexperiente), essa amostra deve ser excluída do cálculo dos limites de controle. Em seguida, os limites de controle são recalculados para as amostras remanescentes. No entanto, o ponto removido deve permanecer registrado visualmente no gráfico para fins de histórico e documentação do processo.

#### Resposta 5

Deming focou na gestão do processo como um todo e no papel decisivo da liderança gerencial para a transformação cultural, destacando-se na indústria japonesa pós-guerra. Juran sistematizou o Controle Estatístico de Processo (CEP) focado no planejamento, controle e melhoria contínua da qualidade. Feigenbaum desenvolveu o Controle da Qualidade Total (TQM), defendendo que a qualidade deve abranger todas as áreas organizacionais em 19 passos, dos quais os métodos estatísticos são apenas uma parte.

#### Resposta 6

As quatro categorias são custos de prevenção, custos de avaliação, custos de falha interna e custos de falha externa. O Princípio de Pareto (regra 80/20) auxilia na identificação de que a maior fração dos custos de não conformidade advém de um número reduzido de falhas graves. Ao ordenar os custos do mais representativo para o menos representativo, a organização pode focar seus recursos na eliminação das causas de maior impacto financeiro.

#### Resposta 7

As cartas de Shewhart avaliam apenas a última amostra coletada e desconsideram o histórico do processo, tornando-as pouco sensíveis a pequenos deslocamentos na média (entre $`0,5\sigma`$ e $`1,5\sigma`$). O CUSUM supera essa limitação ao acumular sequencialmente os desvios em relação ao valor-alvo, enquanto o EWMA aplica uma média ponderada exponencial aos dados passados. Ambas as técnicas incorporam a memória do processo, permitindo uma sinalização consideravelmente mais rápida de pequenas desviações.

#### Resposta 8

A repetitividade é a variação inerente ao instrumento de medição quando utilizado pelo mesmo operador, na mesma peça e sob as mesmas condições, sendo estimada pela variância dos erros residuais $`(\sigma^2_e)`$. A reprodutibilidade reflete a variação decorrente de diferentes operadores medindo a mesma peça, sendo decomposta pela variância dos operadores $`(\sigma^2_O)`$ e pela interação peça-operador $`(\sigma^2_{PO})`$. A variação total do medidor é dada pela soma dessas componentes.

#### Resposta 9

O monitoramento univariado isolado ignora a estrutura de covariância entre variáveis correlacionadas, o que pode levar a alarmes falsos ou a falhas na detecção de peças fora do padrão conjunto. A estatística $`T^2`$ de Hotelling resolve essa deficiência ao sintetizar todas as p variáveis em um único indicador quadrático estroncado. Esse indicador pondera a distância do vetor de médias amostrais até o vetor-alvo por meio da inversa da matriz de covariâncias.

#### Resposta 10

Quando um produto é composto por múltiplos componentes interdependentes, a probabilidade final de o produto ser conforme é o produto das probabilidades de conformidade de cada componente individual. Dessa forma, mesmo que cada componente tenha uma alta taxa de qualidade isolada (por exemplo, $`99\%`$), a probabilidade acumulada cai exponencialmente à medida que o número de componentes aumenta. Essa redução na qualidade final evidencia a necessidade do padrão Seis Sigma em sistemas de alta complexidade.

## 6. Questões Dissertativas (Sem Gabarito)

#### Questão 1

Analise detalhadamente o impacto do efeito cumulativo da não conformidade em produtos complexos constituídos por múltiplos componentes independentes. Em sua resposta, utilize a formulação probabilística para comparar o desempenho de um sistema de 100 componentes sob o nível de qualidade 3-Sigma ($`99,73\%`$ por item) em relação ao nível 6-Sigma ($`99,9999998\%`$ por item), e discuta as implicações econômicas decorrentes da taxa de refugo resultante em cada cenário.

#### Questão 2

Discuta o ciclo DMAIC no contexto da filosofia Seis Sigma, detalhando os objetivos primários, as ferramentas estatísticas e operacionais empregadas e as entregas requeridas em cada uma das suas cinco etapas (Definir, Medir, Analisar, Melhorar e Controlar). Explique de que maneira a fase de Controle assegura que os ganhos obtidos na fase de Melhoria não se deteriorem ao longo do tempo.

#### Questão 3

Compare e contraste a modelagem e a aplicação das cartas de controle por variáveis ($`\bar{X}-R`$ e $`\bar{X}-S`$) e por atributos (carta p). Aborde em sua resposta:

1. As suposições distributivas de cada tipo de carta.
2. A sensibilidade estatística e os custos de inspeção associados.
3. As condições metodológicas sob as quais o gráfico S deve substituir o gráfico R.

#### Questão 4

Avalie o método da Análise de Variância (ANOVA) aplicado aos estudos de Repetitividade e Reprodutibilidade (R&R) de Sistemas de Medição com dois fatores aleatórios e interação. Explique como a decomposição das somas de quadrados e a estimativa das componentes de variância auxiliam na identificação do componente dominante do erro de medição, e discuta a interpretação prática da Razão de Precisão sobre Tolerância (P/T).

#### Questão 5

Considere o problema de monitorar processos industriais modernos com múltiplas características de qualidade correlacionadas. Explique por que a construção de regiões de controle retangulares univariadas baseadas em limites de Shewhart independentes pode induzir a erros de Decisão do Tipo I e Tipo II. Desenvolva os fundamentos matemáticos e geométricos da estatística $`T^2`$ de Hotelling e mostre como a matriz de covariâncias afeta o formato e a orientação da elipse de controle conjunta.

## 7. Glossário Exaustivo de Termos-Chave

| Termo / Conceito | Definição Baseada no Contexto |
|---|---|
| Adequação ao Uso | Conceito primário de qualidade que define se um produto ou serviço atende satisfatoriamente às necessidades e expectativas funcionais do cliente. |
| Amplitude (R) | Medida descritiva de variabilidade calculada pela diferença entre o maior e o menor valor observado em uma amostra $`(R = X_{\max} - X_{\min})`$. |
| Análise de Pareto | Ferramenta de ordenação de causas de defeitos ou custos da qualidade baseada no princípio de que a maioria das perdas decorre de poucas causas vitais (Regra 80/20). |
| Capacidade do Processo $`(C_p)`$ | Razão entre a largura da faixa de especificação emitida pelo cliente e a variação natural do processo $`(6\sigma)`$. Mede o potencial do processo em produzir itens conformes $`(C_p = \frac{\text{LSE} - \text{LIE}}{6\sigma})`$. |
| Causa Atribuível | Causa específica, identificável e não aleatória responsável por desviar o processo de seu estado de controle estatístico (ex.: desgaste de ferramenta, erro operacional). |
| Causa Comum (Aleatória) | Variação inerente e natural ao processo, presente mesmo quando este se encontra em estado estável sob controle estatístico. |
| Carta de Controle (p) | Gráfico de controle por atributos projetado para monitorar a proporção de itens não conformes em amostras derivadas de uma distribuição de Bernoulli. |
| CUSUM (Somas Cumulativas) | Gráfico de controle que monitora a soma acumulada dos desvios das médias amostrais em relação a um valor-alvo. Possui alta sensibilidade para pequenos deslocamentos da média. |
| Desvio-Padrão $`(S / \sigma)`$ | Medida estatística de dispersão em relação à média. Utilizada como indicador primário da variabilidade do processo. |
| DMAIC | Metodologia estruturada em cinco fases (Define, Measure, Analyze, Improve, Control) utilizada no Seis Sigma para a melhoria de processos existentes. |
| EWMA | Média Móvel Exponencialmente Ponderada. Gráfico de controle que atribui pesos decrescentes às observações passadas, útil para detectar pequenos deslocamentos na média. |
| Fator $`c_4`$ | Constante tabelada dependente do tamanho amostral n, utilizada para corrigir o viés da estimativa do desvio-padrão amostral S em relação ao desvio populacional $`\sigma (E(S) = c_4 \sigma)`$. |
| ISO 9000 / 9001 | Conjunto de normas técnicas internacionais que estabelecem requisitos e diretrizes para a estruturação e auditoria de Sistemas de Gestão da Qualidade. |
| Limite Inferior de Controle (LIC) | Limite estatístico inferior calculado para determinar a fronteira mínima esperada de variação natural de um processo sob controle. |
| Limite Superior de Controle (LSC) | Limite estatístico superior que estabelece a fronteira máxima esperada de variação natural do processo. Pontos além dessa linha sinalizam instabilidade. |
| Limites de Especificação (LIE / LSE) | Margens limites (Inferior e Superior) de variação aceitável para as dimensões de um produto, estipuladas pelo projeto, cliente ou funcionalidade. |
| Máscara V | Dispositivo geométrico em formato de V aplicado sobre os pontos acumulados de um gráfico CUSUM para determinar se um processo saiu do estado de controle. |
| Não Conformidade | Qualquer desvio específico de uma característica de qualidade em relação aos requisitos e especificações estabelecidos. |
| Partes por Milhão (PPM) | Métrica estandardizada que expressa a taxa de defeitos ou falhas ocorridas a cada um milhão de oportunidades de produção. |
| Princípio de Pareto | Princípio empírico apontando que aproximadamente $`80\%`$ dos problemas ou custos resultam de $`20\%`$ das causas raízes. |
| Razão P/T (Precisão/Tolerância) | Indicador da qualidade de um sistema de medição que relaciona a variação do medidor $`(6\sigma_{\text{medidor}})`$ com a faixa de tolerância de especificação $`(\text{LSE} - \text{LIE})`$. |
| Repetitividade | Variabilidade inerente ao equipamento ou instrumento de medição observada em testes repetidos sob condições idênticas de operador e peça. |
| Reprodutibilidade | Variabilidade no sistema de medição resultante da diferença nas médias das medições realizadas por diferentes operadores utilizando o mesmo instrumento. |
| Seis Sigma | Filosofia de gestão voltada à redução drástica da variabilidade, visando atingir um nível de qualidade com no máximo 3,4 defeitos por milhão de oportunidades. |
| SIPOC | Ferramenta de mapeamento de processos que identifica os Fornecedores (Suppliers), Entradas (Inputs), Processo (Process), Saídas (Outputs) e Clientes (Customers). |
| $`T^2`$ de Hotelling | Estatística quadrática multivariada utilizada para monitorar simultaneamente o vetor de médias de p características de qualidade correlacionadas. |
| TQM (Gestão da Qualidade Total) | Abordagem gerencial holística que busca a melhoria contínua da qualidade em todos os processos e níveis de uma organização, integrando liderança e colaboradores. |
| Valor Alvo $`(\mu_0)`$ | Valor ideal ou nominal projetado para uma característica de qualidade, em torno do qual o processo deve ser mantido centralizado. |
| Variabilidade | Grau de variação ou dispersão observado nas medidas de um produto ou processo. É a principal causa de degradação da qualidade. |
| Variável Latente | Variável não observável diretamente que precisa ser estimada a partir de indicadores secundários ou questionários (ex.: percepção de amizade ou satisfação). |
