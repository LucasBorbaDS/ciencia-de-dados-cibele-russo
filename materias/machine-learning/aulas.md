> Material derivado das aulas da Profa. Cibele Russo (ICMC/USP), organizado com auxílio do NotebookLM. [↩ Voltar à trilha](README.md)

# Trilha de Aprendizagem e Guia de Estudos: Aprendizado de Máquina Estatístico

Bem-vindo à Trilha de Aprendizagem e Guia de Estudos em Aprendizado de Máquina Estatístico! Este material foi minuciosamente elaborado com base nas aulas e na concepção pedagógica da Professora Dra. Cibele Russo (Instituto de Ciências Matemáticas e de Computação - ICMC/USP São Carlos).

O propósito central desta trilha é desmistificar os fundamentos teóricos, estatísticos e computacionais que estruturam a inteligência artificial moderna e a modelagem preditiva. Ao longo de 11 módulos integrados, você evoluirá de forma consistente: desde os conceitos históricos da inteligência artificial e pré-processamento rigoroso de dados até algoritmos clássicos baseados em distância (KNN), modelos paramétricos (Regressão Logística), probabilísticos (Naive Bayes) e arquiteturas de Redes Neurais Artificiais (Perceptron e Multilayer Perceptron).

#### Sumário Geral e Visão Geral da Trilha

A tabela a seguir apresenta o roadmap completo da nossa jornada de aprendizado, detalhando o número da aula, o título do tópico, os conceitos-chave abordados e a videoaula correspondente ministrada pela Professora Cibele Russo.

| Aula | Título da Aula | Tópicos Chave | Vídeo Original (Profa. Cibele Russo) |
|---|---|---|---|
| 1 | Introdução ao Aprendizado de Máquina, Teste de Turing e Tipos de Aprendizado | Definição formal de Tom Mitchell (P, T, E), Jogo da Imitação (1950), IA Generativa, Aprendizado Supervisionado vs. Não Supervisionado. | Aprendizado de máquina estatístico - Introdução ao aprendizado de máquina |
| 2 | Pré-Processamento de Dados, Imputação e Escalonamento em Python | Limpeza de dados, remoção de colunas irrelevantes, imputação condicional por grupos, StandardScaler, detecção crítica de outliers via Boxplot. | Aprendizado de máquina estatístico - Pré Processamento de dados em Python |
| 3 | Fundamentos da Classificação Supervisionada e Classificador de Bayes | Rótulos categóricos, falha da perda quadrática, erro empírico via função indicadora, otimalidade do Classificador Teórico de Bayes. | Aprendizado de máquina estatístico - Aprendizado para classificação parte1 |
| 4 | Matriz de Confusão e Métricas de Desempenho | Matriz $`2 \times 2`$ (VP, VN, FP, FN), Acurácia, Taxa de Erro, Precisão, Sensibilidade (Recall), Especificidade, F1-Score em dados reais. | Aprendizado de Máquina Estatístico: Classificação parte2 Critérios de desempenho, matriz de confusão |
| 5 | Curva ROC e Área Sob a Curva (AUC) | Trade-off entre Sensibilidade e $`(1 - \text{Especificidade})`$, construção da Curva ROC, ponto ideal (0,1), interpretação probabilística da AUC. | Aprendizado de máquina estatístico - Classificação parte 3 - Curva ROC |
| 6 | Métodos Baseados em Distância - Algoritmo KNN | Algoritmo não paramétrico K-Vizinhos Mais Próximos, Distância Euclidiana, Votação por Moda, Regressão por Média, Escolha do K e Overfitting. | Aprendizado de máquina estatístico - Métodos baseados em distâncias - KNN |
| 7 | Regressão Logística, Razão de Chances (Odds Ratio) e Fronteira de Decisão | Função Sigmoide/Logística, transformação Logit, Chances (Odds), Razão de Chances $`(e^\beta)`$, ajuste via statsmodels (GLM) e scikit-learn. | Aprendizado de máquina estatístico - Aplicação em Python de Regressão logística e KNN |
| 8 | Probabilidade Condicional, Teorema de Bayes e Classificador Naive Bayes | Probabilidade Total, Inversão de Condicionamento, Suposição de Independência Condicional, Critério MAP, GaussianNB vs. Multinomial/Bernoulli. | Aprendizado de máquina estatístico - Revisão de Probabilidades e Naive Bayes com aplicação em Python |
| 9 | Introdução às Redes Neurais Artificiais e Arquitetura do Neurônio Simples | Mapeamento Biológico vs. Artificial, combinação linear $`\text{net}`$, papel geométrico do Viés (Bias), Função de Ativação Degrau Bipolar. | Aprendizado de máquina estatístico - Uma introdução às redes neurais artificiais - parte 1 |
| 10 | O Algoritmo Perceptron e Treinamento com a Porta Lógica AND | Algoritmo de aprendizado do Perceptron, Regra de Atualização com taxa $`\eta`$, Ativação Binária, Convergência Linear e Tabela Verdade do AND. | Aprendizado de máquina estatístico - Redes neurais artificiais 2 - Algoritmo perceptron - AND lógico |
| 11 | Redes Neurais Multicamadas (MLP), Funções Não Lineares e Backpropagation | Problema do XOR, Arquitetura Multicamadas, Funções Sigmoide/Tanh/ReLU, Prova da Falha de Ativações Lineares, Algoritmo Backpropagation. | Aprendizado de máquina estatístico - Introdução a Redes neurais multicamadas - Multilayer perceptron |

#### Como Navegar pelo Guia de Estudos

Para garantir uma assimilação profunda e duradoura do conteúdo, recomendasse o estudo rigoroso e sequencial de cada módulo:

1. Leitura Teórica e Didática: Compreenda as motivações e o contexto histórico por trás de cada modelo estatístico.
2. Desenvolvimento Matemático: Acompanhe as equações em LaTeX, prestando atenção à transição entre fórmulas genéricas e deduções numéricas.
3. Exemplos em Python: Analise criticamente os blocos de código fornecidos. Execute-os em seu ambiente de desenvolvimento e observe o comportamento das funções do pandas, statsmodels e scikit-learn.
4. Análise de Erros Comuns: Atente-se à seção "Erros Comuns de Alunos" para evitar armadilhas conceituais frequentes no mercado e na academia.
5. Exercícios de Fixação: Resolva as 3 questões ao final de cada aula antes de consultar o gabarito comentado. O gabarito traz a resolução passo a passo de cada cálculo e raciocínio lógico.

Com essa visão estruturada do nosso itinerário acadêmico, iniciamos a nossa jornada investigando a natureza teórica do aprendizado e os critérios históricos de inteligência computacional.

### Aula 1: Introdução ao Aprendizado de Máquina, Teste de Turing e Tipos de Aprendizado

#### Fonte

Baseado no vídeo: "Aprendizado de máquina estatístico - Introdução ao aprendizado de máquina" (Profa. Cibele Russo).

#### Objetivo de Aprendizagem

Definir formalmente o conceito de Aprendizado de Máquina segundo a formulação de Tom Mitchell, analisar o contexto histórico e contemporâneo do Teste de Turing e estabelecer a distinção entre os paradigmas de Aprendizado Supervisionado (Classificação e Regressão) e Não Supervisionado (Agrupamento e Redução de Dimensionalidade).

#### Explicação Simples & Analogias

## 1. A Definição Formal de Tom Mitchell

De acordo com a definição clássica formulada por Tom Mitchell (1997), diz-se que um programa de computador aprende com a experiência E, com relação a uma classe de tarefas T e medida de desempenho P, se o seu desempenho em tarefas em T, medido por P, melhora com a experiência E.

#### Para evitar abstrações genéricas, vamos quantificar esses três pilares:

* Tarefa (T): A ação que o algoritmo deve executar. Exemplo: Classificar se uma mensagem de e-mail recebida é "Spam" ou "Não Spam" (Classificação Binária).
* Experiência (E): O histórico de dados fornecido ao algoritmo. Exemplo: Uma base de dados com N = 10.000 e-mails previamente rotulados por usuários humanos.
* Medida de Desempenho (P): A métrica quantitativa estatística que avalia o sucesso da tarefa. Exemplo: A Acurácia do sistema ou a Taxa de Erro Empírico dada por 1 - R(g), onde R(g) é a proporção de mensagens incorretamente classificadas na base de teste.

## 2. O Teste de Turing e o Jogo da Imitação

Em seu histórico artigo de 1950, "Computing Machinery and Intelligence", Alan Turing propôs o "Jogo da Imitação" para substituir a pergunta filosófica "Máquinas podem pensar?".

#### O teste envolve três participantes isolados em salas cegas:

* Um entrevistador humano (C).
* Um participante humano (B).
* Um computador (A).

O entrevistador C faz perguntas via terminais de texto (sem contato visual ou auditivo) aos participantes A e B. Se C não conseguir determinar de maneira estatisticamente confiável qual dos interlocutores é o ser humano e qual é a máquina, o computador passou no teste de inteligência operacional.

Na atualidade, o debate reemerge com o advento das ferramentas de Inteligência Artificial Generativa baseadas em Large Language Models (LLMs, como o ChatGPT). Tais modelos aprendem padrões sintáticos e semânticos em volumes massivos de texto (E) para produzir respostas escritas e códigos que emulam perfeitamente a linguagem humana, reacendendo os desafios do Teste de Turing sob a ótica dos riscos de alucinação e veracidade.

## 3. Paradigmas: Aprendizado Supervisionado vs. Não Supervisionado

* Aprendizado Supervisionado: Há a presença explícita de uma variável de resposta (chamada de target, rótulo ou Y) associada às variáveis preditoras (X). Diz-se que se "aprende com um professor", pois o modelo recebe o gabarito durante o treinamento para ajustar sua função de mapeamento $`X \rightarrow Y`$.
* Aprendizado Não Supervisionado: Não há variável de resposta Y nem rótulos prévios. O algoritmo busca encontrar estruturas ocultas, distribuições de probabilidade conjuntas, agrupamentos (clusters) ou relações de associação entre as variáveis X de forma autônoma.

```text
                         PARADIGMAS DE APRENDIZADO
                                     |
           +-------------------------+-------------------------+
           |                                                   |
    SUPERVISIONADO                                     NÃO SUPERVISIONADO
    (Existe Target Y)                                  (Sem Target Y)
           |                                                   |
     +-----+-----+                                       +-----+-----+
     |           |                                       |           |
```

CLASSIFICAÇÃO  REGRESSÃO                            AGRUPAMENTO   REDUÇÃO DE
(Y discreto) (Y contínuo)                          (Clustering) DIMENSIONALIDADE

#### Exemplo Passo a Passo: Os Três Principais Problemas

1. Classificação Binária (Supervisionado): Prever se um cliente bancário se tornará "Adimplente" (Y=0) ou "Inadimplente" (Y=1), com base em suas preditoras socioeconômicas $`X = [\text{Salário}, \text{Saldo Devedor}]`$.
2. Regressão (Supervisionado): Prever o valor quantitativo contínuo do preço de um imóvel em Reais $`(Y \in \mathbb{R}^+)`$ a partir do vetor $`X = [\text{Área em m}^2, \text{Número de Quartos}, \text{Idade do Imóvel}]`$.
3. Agrupamento / Clustering (Não Supervisionado): Segmentar uma base de 50.000 clientes em K grupos distintos de comportamento de compras sem utilizar qualquer rótulo pré-existente, apenas calculando distâncias entre os perfis observados.

#### Erros Comuns de Alunos

* Confundir codificação numérica de variáveis categóricas com variáveis quantitativas operáveis: Achar que ao registrar a variável categórica Y como 0 e 1 (ou de 0 a 9 em reconhecimento de dígitos), pode-se efetuar operações aritméticas triviais como soma ou diferença quadrática. Os valores 0 e 1 são meros códigos/rótulos qualitativos.
* Procurar "resposta certa" ou gabarito no Aprendizado Não Supervisionado: Tentar avaliar modelos de agrupamento (K-Means) comparando as saídas com um Y de teste, esquecendo que dados não supervisionados não possuem variável de resposta.

#### Resumo em 3 Pontos

1. O Aprendizado de Máquina otimiza iterativamente o desempenho P em uma tarefa T através da experiência E obtida dos dados.
2. O Aprendizado Supervisionado depende de uma variável de resposta (Y), dividindo-se em Classificação (resposta categórica) e Regressão (resposta contínua).
3. O Aprendizado Não Supervisionado busca extrair padrões, perfis e agrupamentos implícitos na estrutura dos dados sem auxílio de rótulos prévios.

#### 3 Exercícios de Fixação com Gabarito Comentado

#### Questões

1. (Teórica - Teste de Turing) Qual é a mecânica do "Jogo da Imitação" descrito por Alan Turing em seu artigo histórico de 1950, "Computing Machinery and Intelligence", e qual é o critério decisório para que uma máquina seja considerada bem-sucedida?
2. (Classificação de Paradigma) Determine o paradigma de aprendizado (Supervisionado ou Não Supervisionado) e a categoria específica para as tarefas:
  * Task A: Reduzir a dimensão de uma base de dados de 100 variáveis fisiológicas para 3 componentes principais mantendo a máxima variância.
  * Task B: Prever o tempo de permanência (em dias) de um paciente internado em um hospital com base em exames admissionais.
3. (Classificação de Variáveis Y) Em um estudo médico epidemiológico, ajustam-se dois modelos: (I) Prever a probabilidade/status se o paciente possui diabetes ("Sim" / "Não") e (II) Prever a taxa de glicose no sangue em mg/dL. Classifique o problema preditivo envolvido em cada modelo.

#### Gabarito Comentado

1. Resposta: No artigo de 1950, Turing propôs um jogo com um interrogador humano (C) e dois interlocutores ocultos: um humano (B) e um computador (A). O interrogador faz perguntas via texto e tenta identificar qual participante é a máquina. Se o interrogador C não conseguir realizar essa distinção de forma estatisticamente significante (ou seja, se o computador simular as respostas humanas a ponto de induzir o juiz ao erro), a máquina é considerada bem-sucedida.
2. Resposta:
  * Task A: Aprendizado Não Supervisionado (Redução de Dimensionalidade / Análise de Componentes Principais), pois não há variável de resposta Y.
  * Task B: Aprendizado Supervisionado - Regressão, pois busca-se prever uma variável de resposta Y contínua (tempo em dias) a partir de atributos X.
3. Resposta: O Modelo (I) é um problema de Classificação Supervisionada (variável de resposta categórica binária: "Sim" ou "Não"). O Modelo (II) é um problema de Regressão Supervisionada (variável de resposta quantitativa contínua: taxa de glicose em mg/dL).

Com a estrutura conceitual estabelecida, a próxima etapa imperativa em qualquer fluxo de trabalho estatístico é a limpeza, a imputação e o escalonamento dos dados brutos.

### Aula 2: Pré-Processamento de Dados, Imputação e Escalonamento em Python

#### Fonte

Baseado no vídeo: "Aprendizado de máquina estatístico - Pré Processamento de dados em Python" (Profa. Cibele Russo).

#### Objetivo de Aprendizagem

Capacitar o aluno a executar o pipeline de preparação, limpeza e transformação de dados em Python utilizando a base Iris, abordando a remoção de colunas irrelevantes, a imputação de dados faltantes condicional por grupos, o escalonamento via StandardScaler e a avaliação crítica rigorosa de outliers via regra do Boxplot.

#### Explicação Simples & Analogias

* O Mise en Place do Cientista de Dados: O pré-processamento equivale à preparação dos ingredientes na culinária profissional. Inserir dados brutos com ruídos, escalas discrepantes ou valores faltantes em um algoritmo avançado produzirá resultados degradados ("Garbage In, Garbage Out").
* Por que Imputar por Grupo e Não Pela Média Geral?: Apagar linhas que contêm valores ausentes reduz drasticamente o tamanho da amostra e destrói informações valiosas contidas nas outras variáveis. Contudo, substituir um dado ausente de largura da sépala pela média geral da base Iris mistura espécies com anatomias completamente distintas (por exemplo, a espécie setosa possui sépalas significativamente mais largas e curtas do que a virginica). O procedimento correto é imputar o valor médio calculado condicionalmente dentro do grupo/espécie correspondente.

#### Exemplo Numérico & Código Passo a Passo

## 1. Remoção de Coluna Irrelevante

Atributos identificadores como ID ou número de registro de chave primária não possuem relação estocástica com o fenômeno biológico e devem ser descartados via .drop().

## 2. Imputação Condicional Por Grupo (Espécie)

Imagine que a 4ª observação do conjunto Iris pertence à espécie setosa e apresenta um dado faltante (NaN) na variável largura_sepala.

* Se calculássemos a média global de todas as 150 flores, obteríamos um valor impróprio.
* Calculando a média condicional apenas para as flores da espécie setosa, encontramos o valor $`3,418750 \approx 3,4187`$. Substitui-se o NaN por este valor específico do grupo.

## 3. Escalonamento via StandardScaler

Algoritmos baseados em distância ou otimização por gradiente exigem que os atributos estejam na mesma escala. O StandardScaler transforma a variável X em um valor padronizado Z com média $`\mu = 0`$ e desvio padrão $`\sigma = 1`$: $`Z = \frac{X - \mu}{\sigma}`$

## 4. Código Python Ilustrativo e Limpo

```python
import pandas as pd
import numpy as np
from sklearn.preprocessing import StandardScaler

# Simulando o carregamento da base Iris tratada nas aulas da Profa. Cibele Russo
# 1. Remoção da coluna de identificação irrelevante
df = df.drop(columns=['ID'], errors='ignore')

# 2. Imputação de dados faltantes utilizando a média condicional por espécie (grupo)
df['largura_sepala'] = df['largura_sepala'].fillna(
    df.groupby('species')['largura_sepala'].transform('mean')
)

# 3. Escalonamento das variáveis quantitativas contínuas
features = ['comprimento_sepala', 'largura_sepala', 'comprimento_petala', 'largura_petala']
scaler = StandardScaler()

# Ajuste do escalonador e transformação dos dados
X_scaled = scaler.fit_transform(df[features])

# Criando um DataFrame com os dados padronizados
df_scaled = pd.DataFrame(X_scaled, columns=features)
print(df_scaled.describe().round(4))
```

## 5. Avaliação Crítica de Outliers via Regra do Boxplot

A regra estatística clássica baseada no intervalo interquartil $`(IQR = Q_3 - Q_1)`$ define os limites de detecção: $`\text{Limite Inferior} = Q_1 - 1,5 \times IQR \text{Limite Superior} = Q_3 + 1,5 \times IQR`$

Análise Crítica da Observação 98: No conjunto de dados Iris trazido pela professora, a observação 98 pertence à espécie versicolor e possui uma largura de sépala de 3,0 cm.

* Ao analisar a espécie versicolor isoladamente, o primeiro quartil é $`Q_1 = 2,525`$ e o terceiro quartil é $`Q_3 = 3,000`$.
* O intervalo interquartil é IQR = 3,000 - 2,525 = 0,475.
* O limite superior calculado é $`\text{LS} = 3,000 + 1,5 \times (0,475) = 3,7125`$.
* Embora o ponto 3,0 cm esteja próximo da borda da distribuição da versicolor, ele é um dado biológico perfeitamente válido e não deve ser excluído de forma automatizada por scripts de limpeza cega! Excluem-se apenas erros grotescos de digitação ou falhas de medição comprovadas.

#### Erros Comuns de Alunos

* Imputar dados faltantes usando a média global: Preencher lacunas de uma subpopulação com a média de toda a base de dados, distorcendo as propriedades condicionais do atributo.
* Deletar outliers de forma automatizada sem inspeção: Executar exclusões cegas em qualquer ponto que ultrapasse os limites do Boxplot, eliminando a variabilidade real do fenômeno sob estudo.

#### Resumo em 3 Pontos

1. Atributos sem poder discriminativo (como ID) devem ser removidos no início do pipeline.
2. A imputação de dados ausentes por média/mediana condicional do grupo/classe preserva as distribuições internas das subpopulações.
3. O StandardScaler transforma as variáveis para média 0 e desvio padrão 1, garantindo que variáveis de maior magnitude não dominem os algoritmos.

#### 3 Exercícios de Fixação com Gabarito Comentado

#### Questões

1. (Cálculo do Z-score) Uma observação do comprimento da pétala possui valor original X = 5,8 cm. Sabendo que a média da variável na base é $`\mu = 3,8`$ cm e o desvio padrão é $`\sigma = 1,0`$ cm, calcule o valor padronizado Z.
2. (Cálculo de Limites do Boxplot) Para a largura da sépala de uma determinada espécie, foram calculados $`Q_1 = 2,8`$ cm e $`Q_3 = 3,4`$ cm. Determine o intervalo interquartil (IQR) e os limites inferior e superior para a detecção de potenciais outliers.
3. (Decisão de Imputação) Por que a substituição de um dado ausente de largura de sépala na espécie setosa pela média global de todas as flores pode enviesar o treinamento de um classificador?

#### Gabarito Comentado

1. Resposta: Aplicando a fórmula de padronização: $`Z = \frac{X - \mu}{\sigma} = \frac{5,8 - 3,8}{1,0} = \frac{2,0}{1,0} = 2,0`$ O valor padronizado é Z = 2,0 (exatamente 2 desvios padrões acima da média).
2. Resposta:
  * $`IQR = Q_3 - Q_1 = 3,4 - 2,8 = 0,6`$ cm.
  * $`\text{Limite Inferior} = Q_1 - 1,5 \times IQR = 2,8 - 1,5(0,6) = 2,8 - 0,9 = 1,9`$ cm.
  * $`\text{Limite Superior} = Q_3 + 1,5 \times IQR = 3,4 + 1,5(0,6) = 3,4 + 0,9 = 4,3`$ cm.
3. Resposta: Porque a espécie setosa possui em média sépalas significativamente mais largas do que as espécies versicolor e virginica. Ao utilizar a média global (que é puxada para baixo pelas outras espécies), o valor imputado para a setosa ficaria artificialmente menor do que o perfil real da espécie, introduzindo um viés sistemático na base de treino.

Com os dados devidamente tratados, limpos e padronizados, podemos avançar para a formalização matemática da classificação supervisionada.

### Aula 3: Fundamentos da Classificação Supervisionada e Classificador de Bayes

#### Fonte

Baseado no vídeo: "Aprendizado de máquina estatístico - Aprendizado para classificação parte1" (Profa. Cibele Russo).

#### Objetivo de Aprendizagem

Compreender a formulação matemática da classificação supervisionada, demonstrar a inadequação do risco quadrático para variáveis de resposta categóricas, definir o risco empírico via função indicadora e deduzir a otimalidade teórica do Classificador de Bayes.

#### Explicação Simples & Analogias

* A Triagem Médica e as Classes: Na classificação, o objetivo é mapear o vetor de preditoras X para um rótulo discreto pertencente a um conjunto finito de classes $`C = \{C_1, C_2, \dots, C_K\}`$.
* Por que o Erro Quadrático Não Funciona em Classificação?: Suponha que estamos classificando dígitos manuscritos de 0 a 9. Se a imagem real for o dígito 2 e o modelo prever 3, o erro quadrático é $`(2 - 3)^2 = 1`$. Se o modelo prever 9, o erro quadrático é $`(2 - 9)^2 = 49`$. Estatisticamente, a métrica quadrática diria que prever 9 é 49 vezes "pior" do que prever 3. No entanto, qualitativamente ambas as previsões são diagnósticos totalmente incorretos! Os códigos categóricos não possuem relação de distância métrica no espaço contínuo.

#### Exemplo Numérico/Matemático Passo a Passo

## 1. Risco Empírico via Função Indicadora $`I(\cdot)`$

Para mensurar a taxa de erro de um classificador g(X) em uma amostra de tamanho N, utiliza-se a função indicadora $`I(\cdot)`$, que retorna 1 se a condição for verdadeira (erro) e 0 se for falsa (acerto): $`R(g) = \frac{1}{N} \sum_{i=1}^N I(y_i \neq g(x_i))`$ onde: $`I(y_i \neq g(x_i)) = \begin{cases} 1, & \text{se } y_i \neq g(x_i) \text{ (classificação incorreta)} \\ 0, & \text{se } y_i = g(x_i) \text{ (classificação correta)} \end{cases}`$

## 2. Minimização da Perda Esperada e o Classificador de Bayes

Queremos encontrar a regra de decisão $`g^*(X)`$ que minimiza o Risco Teórico $`R(g) = E_{X,Y}[I(Y \neq`$ g(X))].

Pela Lei da Expectativa Total, podemos reescrever o risco condicionado ao vetor de preditoras $`X: E_{X,Y}[I(Y \neq`$ g(X))] = $`E_X \left[ \sum_{k=1}^K P(Y \neq C_k \mid X) \cdot I(g(X) = C_k) \right]`$ Como $`P(Y \neq C_k \mid X) = 1 - P(Y = C_k \mid X)`$, minimizar a probabilidade de erro equivale a maximizar a probabilidade a posteriori $`P(Y = C_k \mid X)`$.

Assim, deduz-se a Regra de Decisão do Classificador de Bayes: $`g^*(X) = \arg\max_{C_k \in C}`$ $`P(Y = C_k \mid X)`$

Para uma resposta binária onde $`Y \in \{0, 1\}`$, a regra se simplifica para: $`g^*(X) = 1 \iff P(Y = 1 \mid X) \ge 0,5`$

## 3. Exemplo Numérico de Tomada de Decisão

Imagine que um modelo de risco de crédito estimou as probabilidades a posteriori para dois clientes:

* Cliente A: P(Y=1 $`\mid X_A) = 0,68`$ (onde Y=1 significa "Inadimplente").
* Cliente B: P(Y=1 $`\mid X_B) = 0,32`$.

#### Aplicando a regra de Bayes com limiar 0,5:

* Para o Cliente A: Como $`0,68 \ge 0,5`$, atribui-se $`\hat{Y}_A = 1`$ (Inadimplente).
* Para o Cliente B: Como 0,32 < 0,5, atribui-se $`\hat{Y}_B = 0`$ (Adimplente).

#### Erros Comuns de Alunos

* Calcular erro quadrático em códigos categóricos: Tentar aplicar a fórmula do erro quadrático médio (EQM) em problemas de classificação binária ou multiclasse.
* Avaliar o modelo na mesma base utilizada para o treinamento: Avaliar a taxa de erro empírica R(g) no próprio conjunto de treino, omitindo a avaliação de generalização em dados não vistos (amostra de teste).

#### Resumo em 3 Pontos

1. A classificação trata de variáveis de resposta qualitativas/discretas, tornando a perda quadrática conceitualmente inadequada.
2. A avaliação de um classificador é mensurada pela probabilidade de erro computada pela função indicadora $`I(y \neq \hat{y})`$.
3. O Classificador de Bayes é o modelo teórico ótimo que minimiza o risco ao atribuir a observação à classe que maximiza a probabilidade a posteriori $`P(Y = C_k \mid X)`$.

#### 3 Exercícios de Fixação com Gabarito Comentado

#### Questões

1. (Cálculo do Risco Empírico) Um modelo preditivo de diagnósticos médicos avaliou 6 pacientes na base de teste. Os rótulos reais eram y = [1, 0, 1, 1, 0, 0] e as previsões fornecidas foram $`\hat{y} = [1`$, 0, 0, 1, 1, 0]. Calcule o risco empírico R(g).
2. (Aplicação da Regra de Bayes) Um modelo probabilístico retornou as seguintes probabilidades P(Y=1 $`\mid X`$) para três pacientes: $`P_1 = 0,48, P_2 = 0,51`$ e $`P_3 = 0,89`$. Adotando o ponto de corte estatístico de 0,50, quais serão as classes preditas $`\hat{Y}_1, \hat{Y}_2`$ e $`\hat{Y}_3?`$
3. (Dedução da Regra Ótima) Mostre matematicamente por que maximizar $`P(Y = C_k \mid X)`$ é equivalente a minimizar a probabilidade de erro $`1 - P(Y = C_k \mid X)`$.

#### Gabarito Comentado

1. Resposta: Avaliando elemento por elemento com a função indicadora $`I(y_i \neq \hat{y}_i)`$:
  * i=1: $`y_1=1, \hat{y}_1=1 \Rightarrow I(1 \neq 1) = 0`$
  * i=2: $`y_2=0, \hat{y}_2=0 \Rightarrow I(0 \neq 0) = 0`$
  * i=3: $`y_3=1, \hat{y}_3=0 \Rightarrow I(1 \neq 0) = 1`$ (Erro)
  * i=4: $`y_4=1, \hat{y}_4=1 \Rightarrow I(1 \neq 1) = 0`$
  * i=5: $`y_5=0, \hat{y}_5=1 \Rightarrow I(0 \neq 1) = 1`$ (Erro)
  * i=6: $`y_6=0, \hat{y}_6=0 \Rightarrow I(0 \neq 0) = 0`$

Total de erros = 2. Risco Empírico $`R(g) = \frac{2}{6} = \frac{1}{3} \approx 0,3333`$ (33,33% de erro).

1. Resposta:
  * Paciente $`1: P_1 = 0,48 < 0,50 \Rightarrow \hat{Y}_1 = 0`$.
  * Paciente $`2: P_2 = 0,51 \ge 0,50 \Rightarrow \hat{Y}_2 = 1`$.
  * Paciente $`3: P_3 = 0,89 \ge 0,50 \Rightarrow \hat{Y}_3 = 1`$.
2. Resposta: A probabilidade de cometer um erro ao atribuir a observação à classe $`C_k`$ dado o vetor X é $`P(\text{Erro} \mid X) = P(Y \neq C_k \mid X) = 1 - P(Y = C_k \mid X)`$. Como o valor 1 é uma constante fixa, minimizar $`(1 - P(Y = C_k \mid X))`$ exige diretamente a escolha da classe $`C_k`$ que maximiza $`P(Y = C_k \mid X)`$.

Uma vez compreendida a tomada de decisão Bayesiana, a próxima etapa é decompor os tipos de erros e acertos do modelo utilizando a Matriz de Confusão.

### Aula 4: Matriz de Confusão e Métricas de Desempenho

#### Fonte

Baseado no vídeo: "Aprendizado de Máquina Estatístico: Classificação parte2 Critérios de desempenho, matriz de confusão" (Profa. Cibele Russo).

#### Objetivo de Aprendizagem

Construir, preencher e interpretar a Matriz de Confusão $`2 \times 2`$ e calcular com precisão estrita as métricas operacionais: Acurácia Total, Taxa de Erro, Precisão, Sensibilidade (Recall), Especificidade e F1-Score em dados de crédito bancário.

#### Explicação Simples & Analogias

* A Analogia do Exame Médico:
  * Verdadeiro Positivo (VP): O paciente está doente e o exame deu positivo (Acerto na classe de interesse).
  * Verdadeiro Negativo (VN): O paciente está saudável e o exame deu negativo (Acerto na classe de controle).
  * Falso Positivo (FP): Alarme falso. O paciente é saudável, mas o teste aponta doença.
  * Falso Negativo (FN): Perigo silencioso. O paciente está doente, mas o teste diz que ele é saudável.

#### Exemplo Numérico Resolvido Passo a Passo

Utilizaremos os dados reais apresentados pela Profa. Cibele Russo para validação de um modelo preditivo de inadimplência bancária com um tamanho amostral total de N = 1.665 clientes no conjunto de teste.

## 1. A Matriz de Confusão $`2 \times 2`$

|   | Classe Predita: Inadimplente $`(\hat{Y}=1)`$ | Classe Predita: Adimplente $`(\hat{Y}=0)`$ | Total Real |
|---|---|---|---|
| Classe Real: Inadimplente (Y=1) | VP = 163 | FN = 359 | 522 |
| Classe Real: Adimplente (Y=0) | FP = 50 | VN = 1093 | 1143 |
| Total Predito | 213 | 1452 | N = 1665 |

## 2. Cálculo Detalhado das Métricas Estatísticas

Para manter o rigor formal, mantermos 5 casas decimais nos passos intermediários antes da conversão percentual:

* Acurácia Total: Proporção global de acertos do modelo. $`\text{Acurácia} = \frac{VP + VN}{N} = \frac{163 + 1093}{1665} = \frac{1256}{1665} \approx 0,75435 \quad (75,44\%)`$
* Taxa de Erro Total: Proporção global de falhas do modelo. $`\text{Taxa de Erro} = \frac{FP + FN}{N} = \frac{50 + 359}{1665} = \frac{409}{1665} \approx 0,24565 \quad (24,56\%)`$
* Precisão: Proporção de acertos entre todas as observações que o modelo rotulou como positivas $`(\hat{Y}=1). \text{Precisão} = \frac{VP}{VP + FP} = \frac{163}{163 + 50} = \frac{163}{213} \approx 0,76526 \quad (76,53\%)`$
* Sensibilidade (Recall / Taxa de Verdadeiros Positivos): Proporção de acertos entre todos os clientes que eram de fato inadimplentes (Y=1). $`\text{Sensibilidade} = \frac{VP}{VP + FN} = \frac{163}{163 + 359} = \frac{163}{522} \approx 0,31226 \quad (31,23\%)`$
* Especificidade (Taxa de Verdadeiros Negativos): Proporção de acertos entre todos os clientes que eram de fato adimplentes (Y=0). $`\text{Especificidade} = \frac{VN}{VN + FP} = \frac{1093}{1093 + 50} = \frac{1093}{1143} \approx 0,95625 \quad (95,63\%)`$
* F1-Score: Média harmônica entre Precisão e Sensibilidade, fornecendo um balanço único para bases desbalanceadas. $`\text{F1-Score} = 2 \times \frac{\text{Precisão} \times \text{Sensibilidade}}{\text{Precisão} + \text{Sensibilidade}} = 2 \times \frac{0,76526 \times 0,31226}{0,76526 + 0,31226} = 2 \times \frac{0,23896}{1,07752} \approx 0,44354 \quad (44,35\%)`$

Análise da Profa. Cibele Russo: Note que embora a Acurácia pareça aceitável $`(75,44\%)`$, o modelo possui uma Sensibilidade muito baixa $`(31,23\%)`$, detectando menos de um terço dos maus pagadores reais. Ele compensa isso com uma Especificidade alta $`(95,63\%)`$.

#### Erros Comuns de Alunos

* Inverter Sensibilidade e Precisão: A Sensibilidade responde "De todos os doentes/inadimplentes reais, quantos eu capturei?". A Precisão responde "De todos que o modelo apontou como doentes/inadimplentes, quantos realmente eram?".
* Confiar unicamente na Acurácia em cenários desbalanceados: Em detecção de fraudes (onde $`99\%`$ das transações são legítimas), um modelo trivial que classifica 100% dos dados como "Legítima" obterá $`99\%`$ de acurácia, mas possuirá Sensibilidade $`0\%`$, falhando completamente em detectar fraudes.

#### Resumo em 3 Pontos

1. A Matriz de Confusão detalha os quatro cenários de previsão: VP, VN, FP e FN.
2. Sensibilidade mede a taxa de captura da classe de interesse (Y=1), enquanto a Especificidade mede a taxa de acerto da classe de controle (Y=0).
3. O F1-Score é a média harmônica entre Precisão e Sensibilidade, sendo a métrica ideal para comparar modelos em conjuntos de dados desbalanceados.

#### 3 Exercícios de Fixação com Gabarito Comentado

#### Questões

1. (Construção de Matriz de Confusão) Um sistema de detecção de invasão cibernética avaliou N = 2.000 conexões. A base continha 200 ataques reais (Y=1) e 1.800 acessos legítimos (Y=0). O sistema identificou corretamente 150 ataques e gerou 90 alarmes falsos (acessos legítimos classificados como ataque). Monte a Matriz de Confusão preenchendo os valores de VP, FN, FP e VN.
2. (Cálculo de Sensibilidade e Especificidade) Com base na matriz obtida no exercício 1, calcule a Sensibilidade e a Especificidade do sistema de detecção.
3. (Cálculo de Precisão e F1-Score) Utilizando os dados dos exercícios anteriores, calcule a Precisão do sistema e o seu F1-Score.

#### Gabarito Comentado

1. Resposta:
  * Ataques Reais (Y=1): Total = 200. Acertos $`VP = 150 \Rightarrow FN = 200 - 150 = 50`$.
  * Legítimos Reais (Y=0): Total = 1.800. Erros $`FP = 90 \Rightarrow VN = 1.800 - 90 = 1.710`$.

Matriz: VP = 150, FN = 50, FP = 90, VN = 1.710. Total N = 2.000.

1. Resposta:
  * $`\text{Sensibilidade} = \frac{VP}{VP + FN} = \frac{150}{200} = 0,7500 \quad (75,00\%)`$.
  * $`\text{Especificidade} = \frac{VN}{VN + FP} = \frac{1710}{1800} = 0,9500 \quad (95,00\%)`$.
2. Resposta:
  * $`\text{Precisão} = \frac{VP}{VP + FP} = \frac{150}{150 + 90} = \frac{150}{240} = 0,6250 \quad (62,50\%)`$.
  * $`\text{F1-Score} = 2 \times \frac{\text{Precisão} \times \text{Sensibilidade}}{\text{Precisão} + \text{Sensibilidade}} = 2 \times \frac{0,6250 \times 0,7500}{0,6250 + 0,7500} = 2 \times \frac{0,46875}{1,3750} \approx 0,6818 \quad (68,18\%)`$.

Para avaliar o desempenho do classificador em todos os limiares de probabilidade possíveis (e não apenas no ponto fixo 0.5), recorre-se à Curva ROC.

### Aula 5: Curva ROC e Área Sob a Curva (AUC)

#### Fonte

Baseado no vídeo: "Aprendizado de máquina estatístico - Classificação parte 3 - Curva ROC" (Profa. Cibele Russo).

#### Objetivo de Aprendizagem

Compreender a construção gráfica da Curva ROC (Receiver Operating Characteristic), analisar a relação de compensação (trade-off) entre Sensibilidade e a Taxa de Falsos Positivos $`(1 - \text{Especificidade})`$ e interpretar o significado estocástico da Área Sob a Curva (AUC).

#### Explicação Simples & Analogias

* Ajustando a Sensibilidade de um Alarme de Incêndio:
  * Se definirmos um limiar de probabilidade p de disparo do alarme extremamente baixo (p = 0,05), qualquer fumaça de cozinha disparará a sirene. O sistema detectará todos os incêndios reais $`(\text{Sensibilidade} \approx 100\%)`$, porém gerará um volume absurdo de alarmes falsos ($`\text{Especificidade}`$ baixíssima, logo $`1 - \text{Especificidade}`$ muito alto).
  * Se aumentarmos o limiar para p = 0,95, o alarme só tocará quando a casa estiver em chamas generalizadas. Não haverá alarmes falsos $`(1 - \text{Especificidade} \approx 0)`$, porém muitos incêndios iniciais não serão detectados ($`\text{Sensibilidade}`$ perigosamente baixa).
  * A Curva ROC traça essa troca (trade-off) para todos os pontos de corte possíveis entre 0 e 1.

#### Exemplo Numérico e Gráfico Passo a Passo

#### A Curva ROC é um gráfico cartesiano onde:

* Eixo Y: Sensibilidade (Taxa de Verdadeiros Positivos).
* Eixo X: $`1 - \text{Especificidade}`$ (Taxa de Falsos Positivos).

## 1. Demonstração Numérica da Variação do Limiar p

Imagine que alteramos o ponto de corte p para classificar um cliente como inadimplente em um banco. Observe a dinâmica na tabela abaixo:

| Limiar p | Sensibilidade (Eixo Y) | Especificidade | $`1 - \text{Especificidade}`$ (Eixo X) | Impacto Prático na Decisão |
|---|---|---|---|---|
| 0,90 | 0,10 | 0,99 | 0,01 | Regra conservadora. Quase não aponta risco, perde maus pagadores. |
| 0,80 | 0,25 | 0,97 | 0,03 | Sensibilidade ainda insuficiente. |
| 0,50 | 0,65 | 0,85 | 0,15 | Ponto de corte padrão equilibrado. |
| 0,20 | 0,92 | 0,55 | 0,45 | Captura 92% dos inadimplentes, mas aumenta os alarmes falsos. |
| 0,05 | 0,99 | 0,10 | 0,90 | Regra agressiva. Captura todos os riscos, recusa bons clientes. |

Efeito de Deslocamento: Note que ao reduzir o limiar p de 0,80 para 0,20, a Sensibilidade aumenta expressivamente de 0,25 para 0,92 (mais Verdadeiros Positivos são capturados), mas o custo cobrado é o aumento na Taxa de Falsos Positivos de 0,03 para 0,45.

## 2. O Ponto Ideal e a Área Sob a Curva (AUC)

* Ponto Perfeito Ideal: Canto superior esquerdo (0, 1), onde $`1 - \text{Especificidade} = 0`$ e $`\text{Sensibilidade} = 1,0`$.
* Área Sob a Curva (AUC - Area Under the Curve): É a área integrada sob a curva ROC.
  * $`\text{AUC} = 0,5`$: O modelo é equivalente a uma linha diagonal aleatória (chute sem poder discriminativo).
  * $`\text{AUC} = 1,0`$: Classificador perfeito. Separação absoluta das distribuições das classes.

Sensibilidade (Eixo Y)
```text
  1.0 |        * PONTO IDEAL PERFECTO (0,1)
      |       /|
      |      / |  <-- Curva ROC do Modelo A (AUC = 0.88)
      |     /  |
  0.5 |    /   |  <-- Linha de Chute Aleatório (AUC = 0.50)
      |   /    |
  0.0 +--+-----+-------------------
     0.0      0.5                 1.0
             1 - Especificidade (Eixo X)
```

#### Erros Comuns de Alunos

* Plotar a Especificidade diretamente no Eixo X: O correto é plotar a Taxa de Falsos Positivos dada pelo complemento $`(1 - \text{Especificidade})`$.
* Acreditar que o ponto de corte deve ser obrigatoriamente 0,5: Em negócios reais com custos assimétricos (ex: perda por fraude de R\$ 10.000 vs. incômodo de checagem de R\$ 5), deve-se alterar o ponto de corte para priorizar a Sensibilidade.

#### Resumo em 3 Pontos

1. A Curva ROC mapeia a Sensibilidade vs. $`(1 - \text{Especificidade})`$ para todos os limiares de decisão possíveis.
2. O ponto (0, 1) no canto superior esquerdo representa a perfeição estatística ($`100\%`$ Sensibilidade e $`0\%`$ Falsos Positivos).
3. A AUC mensura a capacidade global de discriminação da modelo: valores próximos de 1,0 indicam um modelo excelente; 0,5 indica chute aleatório.

#### 3 Exercícios de Fixação com Gabarito Comentado

#### Questões

1. (Cálculo de Coordenada no Eixo X) Um modelo operando em um determinado ponto de corte obteve uma Especificidade de 0,92. Qual é a coordenada X correspondente que deve ser plotada no gráfico da Curva ROC?
2. (Interpretação Probabilística de AUC) Um cientista de dados comparou dois modelos de detecção de fraudes: o Modelo Alpha obteve $`\text{AUC} = 0,91`$ e o Modelo Beta obteve $`\text{AUC} = 0,53`$. Interprete a capacidade de discriminação de ambos os modelos.
3. (Escolha do Limiar de Decisão) Se uma instituição hospitalar prioriza evitar a qualquer custo que um paciente doente receba alta sem tratamento (evitar Falsos Negativos), ela deve aumentar ou diminuir o limiar de probabilidade p para diagnosticar a doença?

#### Gabarito Comentado

1. Resposta: O Eixo X da Curva ROC representa $`1 - \text{Especificidade}`$. Portanto: $`\text{Eixo X} = 1 - 0,92 = 0,08`$ A coordenada plotada no Eixo X será 0,08 (8% de Falsos Positivos).
2. Resposta: O Modelo Alpha possui excelente capacidade discriminativa $`(\text{AUC} = 0,91)`$, significando que há 91% de probabilidade de ele atribuir um score mais alto a uma transação fraudulenta real do que a uma transação legítima. O Modelo Beta $`(\text{AUC} = 0,53)`$ é inútil na prática, pois possui desempenho próximo ao de um lançamento de moeda aleatório $`(\text{AUC} = 0,50)`$.
3. Resposta: A instituição deve diminuir o limiar de probabilidade p (por exemplo, reduzindo de 0,50 para 0,15). Isso tornará o teste médico mais permissivo para diagnosticar a doença, aumentando drasticamente a Sensibilidade e capturando praticamente todos os pacientes doentes.

Encerrada a fase de métricas de avaliação, iniciamos a exploração dos algoritmos preditivos na prática, a começar pelo método não paramétrico baseado em distância KNN.

### Aula 6: Métodos Baseados em Distância - Algoritmo KNN

#### Fonte

Baseado no vídeo: "Aprendizado de máquina estatístico - Métodos baseados em distâncias - KNN" (Profa. Cibele Russo).

#### Objetivo de Aprendizagem

Compreender o algoritmo não paramétrico K-Vizinhos Mais Próximos (K-Nearest Neighbors - KNN) para classificação e regressão, calcular a distância Euclidiana passo a passo, analisar a influência do hiperparâmetro K no balanço entre viés e variância e reconhecer o impacto do escalonamento de variáveis.

#### Explicação Simples & Analogias

* "Diga-me com quem andas e te direi quem és": O KNN é um algoritmo lazy (preguiçoso) e não paramétrico. Ele não aprende coeficientes ou equações durante o treinamento. Para classificar um novo ponto de teste, ele encontra no espaço os K pontos da base de treino mais próximos e atribui a classe mais frequente entre esses vizinhos (votação por moda).
* KNN para Regressão: Se o objetivo for prever um valor contínuo $`Y \in \mathbb{R}`$, o KNN localiza os K vizinhos mais próximos no espaço e calcula a média aritmética simples dos seus valores $`Y: \hat{Y}(P) = \frac{1}{K} \sum_{i \in N_K(P)} Y_i`$

#### Exemplo Numérico Resolvido Passo a Passo

Considere uma base de treinamento bidimensional $`(X_1, X_2)`$ com 4 observações conhecidas descritas na tabela abaixo, e um novo ponto de teste P = (2, 3) a ser classificado.

## 1. Coordenadas dos Pontos de Treino

| Ponto | Coordenada $`X_1`$ | Coordenada $`X_2`$ | Classe Real (Y) |
|---|---|---|---|
| A | 1 | 2 | Azul |
| B | 2 | 1 | Azul |
| C | 4 | 5 | Vermelho |
| D | 5 | 4 | Vermelho |

## 2. Cálculo da Distância Euclidiana de P = (2, 3) aos Pontos de Treino

#### Fórmula: d(P, $`Q) = \sqrt{(x_{1P} - x_{1Q})^2 + (x_{2P} - x_{2Q})^2}`$

* Distância a A (1, 2): d(P, A) = $`\sqrt{(2 - 1)^2 + (3 - 2)^2} = \sqrt{1^2 + 1^2} = \sqrt{2} \approx 1,414`$
* Distância a B (2, 1): d(P, $`B) = \sqrt{(2 - 2)^2 + (3 - 1)^2} = \sqrt{0^2 + 2^2} = \sqrt{4} = 2,000`$
* Distância a C (4, 5): d(P, $`C) = \sqrt{(2 - 4)^2 + (3 - 5)^2} = \sqrt{(-2)^2 + (-2)^2} = \sqrt{8} \approx 2,828`$
* Distância a D (5, 4): d(P, $`D) = \sqrt{(2 - 5)^2 + (3 - 4)^2} = \sqrt{(-3)^2 + (-1)^2} = \sqrt{10} \approx 3,162`$

## 3. Classificação por Votação

* Para K = 1: O vizinho mais próximo de P é o Ponto A $`(d \approx 1,414)`$. Previsão: Azul.
* Para K = 3: Os 3 vizinhos mais próximos são A ($`d \approx 1,414`$, Azul), B (d = 2,000, Azul) e C ($`d \approx 2,828`$, Vermelho). Votação por Moda: 2 votos para Azul e 1 voto para Vermelho. Previsão: Azul.

## 4. O Balanço entre Viés e Variância (Bias-Variance Trade-off)

* K = 1: Baixo viés, mas alta variância. A fronteira de decisão é extremamente complexa, recortada e ajustada ao ruído da base de treino (risco severo de overfitting / interpolação).
* K = N (total de observações): Alto viés e variância nula. O modelo prevê sempre a classe majoritária da base inteira, independente das características do ponto de teste.
* Escolha Prática: O valor ideal de K deve ser determinado via validação cruzada (cross-validation).

#### Erros Comuns de Alunos

* Não padronizar as variáveis antes do KNN: Se $`X_1`$ for o Salário em Reais (de R\$ 1.000 a R\$ 50.000) e $`X_2`$ for a Idade em Anos (18 a 80), a variação numérica do Salário dominará a soma dos quadrados da distância Euclidiana, tornando a Idade irrelevante. É obrigatório aplicar o StandardScaler.
* Subestimar o custo computacional de teste: O KNN exige armazenar toda a base em memória e calcular a distância do ponto de teste contra todos os N pontos de treino, o que se torna muito lento para grandes bases de dados.

#### Resumo em 3 Pontos

1. O KNN é um método geométrico não paramétrico: classifica por maioria simples de votos (moda) e realiza regressão por média aritmética dos K vizinhos.
2. A padronização das variáveis é indispensável para evitar que atributos com maior escala numérica dominem o cálculo de distância.
3. O hiperparâmetro K controla a complexidade do modelo: K pequeno induz alta variância (overfitting); K grande gera alto viés (underfitting).

#### 3 Exercícios de Fixação com Gabarito Comentado

#### Questões

1. (Cálculo de Distância Euclidiana) Dado o ponto de teste P = (3, 3) e duas amostras de treino $`M_1 = (0`$, 0) com rótulo Y = 1 e $`M_2 = (4`$, 3) com rótulo Y = 0, determine qual das duas amostras é a mais próxima de P.
2. (Regressão KNN) Em um problema de regressão preditiva, os 3 vizinhos mais próximos de uma observação de teste possuem os seguintes valores da variável contínua Y: 12,0, 15,0 e 18,0. Qual é o valor predito $`\hat{Y}(P)`$ pelo KNN com K = 3?
3. (Efeito do Escalonamento) O que ocorre com a fronteira de decisão do KNN se uma variável tiver intervalo de 0 a 1.000.000 e outra tiver intervalo de 0 a 1, caso a padronização não seja executada?

#### Gabarito Comentado

1. Resposta:
  * $`d(P, M_1) = \sqrt{(3 - 0)^2 + (3 - 0)^2} = \sqrt{9 + 9} = \sqrt{18} \approx 4,2426`$.
  * $`d(P, M_2) = \sqrt{(3 - 4)^2 + (3 - 3)^2} = \sqrt{(-1)^2 + 0^2} = \sqrt{1} = 1,0000`$.

A amostra $`M_2`$ é o vizinho mais próximo (d = 1,0000).

1. Resposta: Para regressão, calcula-se a média aritmética simples dos K vizinhos: $`\hat{Y}(P) = \frac{12,0 + 15,0 + 18,0}{3} = \frac{45,0}{3} = 15,0`$
2. Resposta: A variável de grande escala (0 a 1.000.000) dominará completamente a soma dos quadrados das diferenças na fórmula da distância Euclidiana. As diferenças na variável menor (0 a 1) se tornarão matematicamente insignificantes, fazendo com que o algoritmo decida a vizinhança ignorando a segunda variável.

Migrando das abordagens geométricas não paramétricas para a modelagem estatística paramétrica, exploramos a Regressão Logística.

### Aula 7: Regressão Logística, Razão de Chances (Odds Ratio) e Fronteira de Decisão

#### Fonte

Baseado no vídeo: "Aprendizado de máquina estatístico - Aplicação em Python de Regressão logística e KNN" (Profa. Cibele Russo).

#### Objetivo de Aprendizagem

Formular o modelo de Regressão Logística, compreender a transformação Logit, diferenciar com precisão os domínios do Logit, das Chances (Odds) e da Probabilidade (p), calcular a Razão de Chances (Odds Ratio - OR) e comparar a implementação prática em Python via statsmodels (GLM) e scikit-learn com as fronteiras de decisão do KNN.

#### Explicação Simples & Analogias

* A Escala Sigmoide de Risco: Uma regressão linear ordinária tenta ajustar uma reta $`Y = \beta_0 + \beta_1 X`$, o que pode produzir "probabilidades" absurdas como -0,3 ou 1,4. A Regressão Logística resolve isso utilizando a Função Sigmoide/Logística, que achata qualquer combinação linear que vá de $`-\infty`$ a $`+\infty`$ e a comprime suavemente entre 0 e 1.

#### Exemplo Numérico e Código Passo a Passo

## 1. Formulação Matemática do Modelo Logit

Para uma variável de resposta binária $`Y \in \{0, 1\}`$, seja p = P(Y=1 $`\mid X`$) a probabilidade de sucesso.

* Combinação Linear (Logit / Log-Odds): $`\text{Logit}(p) = \ln\left(\frac{p}{1-p}\right) = \alpha + \beta_1 X_1 + \beta_2 X_2`$
* Probabilidade Isolada (p): $`p = \frac{e^{\alpha + \beta_1 X_1 + \beta_2 X_2}}{1 + e^{\alpha + \beta_1 X_1 + \beta_2 X_2}}`$
* Chance (Odds): Razão entre a probabilidade de ocorrência e não ocorrência do evento: $`\text{Odds} = \frac{p}{1-p} = e^{\alpha + \beta_1 X_1 + \beta_2 X_2}`$
* Razão de Chances (Odds Ratio - OR): O impacto de aumentar 1 unidade na variável $`X_k`$ multiplica a chance original por $`e^{\beta_k}`$.

## 2. Tabela de Conversão entre Domínios

| Domínio | Expressão Matemática | Intervalo de Valores | Exemplo Notável |
|---|---|---|---|
| Logit (Log-Odds) | $`\ln\left(\frac{p}{1-p}\right)`$ | $`(-\infty, +\infty)`$ | $`\text{Logit} = 0`$ |
| Chance (Odds) | $`\frac{p}{1-p}`$ | [$`0, +\infty`$) | $`\text{Odds} = 1,0`$ (1 para 1) |
| Probabilidade (p) | p | [0, 1] | $`p = 0,50 (50\%)`$ |

## 3. Ajuste em Python via statsmodels e Avaliação de Previsões

Código completo para ajuste do Modelo Linear Generalizado (GLM) da família Binomial aplicado à base bancária com as variáveis salario e devedor_cartao:

```python
import numpy as np
import pandas as pd
import statsmodels.api as sm
from sklearn.model_selection import train_test_split

# Dividindo os dados (80% treino, 20% teste)
X_train, X_test, y_train, y_test = train_test_split(
    df[['salario', 'devedor_cartao']], df['inadimplente'], test_size=0.2, random_state=42
)

# Adicionando a constante obrigatoria para estimar o intercepto (alpha)
X_train_const = sm.add_constant(X_train)

# Ajustando o modelo GLM Binomial com funcao de ligacao Logit
glm_model = sm.GLM(
    y_train,
    X_train_const,
    family=sm.families.Binomial(link=sm.families.links.Logit())
)
results = glm_model.fit()

# Exibindo o resumo com coeficientes e p-valores
print(results.summary())

# Calculando a Razao de Chances (Odds Ratio) para os coeficientes
odds_ratios = np.exp(results.params)
print("\nRazao de Chances (Odds Ratio):\n", odds_ratios)

# Previsao no conjunto de teste
X_test_const = sm.add_constant(X_test)
y_prob = results.predict(X_test_const)

# Convertendo probabilidades em classificacoes binarias no limiar 0.5
y_pred = (y_prob >= 0.5).astype(int)
```

## 4. Fronteira de Decisão: Regressão Logística vs. KNN

* Regressão Logística: Produz uma fronteira de decisão estritamente linear no espaço dos atributos (uma reta em 2D, um plano em 3D). Altamente interpretável via coeficientes estatísticos e Razão de Chances.
* KNN: Produz uma fronteira não linear, recortada e flexível, adaptando-se a padrões locais complexos, porém sem fornecer coeficientes estatísticos explicativos.

Regressão Logística (Fronteira Linear)     KNN (Fronteira Não Linear)
```text
    X2 |         /                    X2 |      .--.
       |        /                        |     /    \  /--\
       |       /                         |    |      \/    |
       |      /                          |     \          /
       +------------ X1                  +------------------ X1
```

#### Erros Comuns de Alunos

* Interpretar o coeficiente $`\beta`$ como alteração direta na probabilidade p: O coeficiente $`\beta`$ representa a alteração aditiva no logaritmo da chance $`(\ln(\text{Odds}))`$, enquanto $`e^\beta`$ é o fator multiplicativo na chance (Odds). O impacto final na probabilidade p não é constante, variando ao longo da curva sigmoide.
* Não adicionar a constante (sm.add_constant) no statsmodels: Esquecer a constante força o intercepto $`\alpha`$ a ser zero, exigindo erroneamente que p = 0,5 quando todas as variáveis preditoras forem zero.

#### Resumo em 3 Pontos

1. A Regressão Logística modela o logaritmo da chance via transformação Logit, garantindo probabilidades no intervalo [0, 1].
2. Exponenciar os coeficientes $`(e^\beta)`$ fornece a Razão de Chances (Odds Ratio), que mede a variação multiplicativa na chance de sucesso para cada unidade incrementada na preditora.
3. A Regressão Logística gera fronteiras de decisão lineares e parametricamente interpretáveis, enquanto o KNN gera fronteiras flexíveis e não paramétricas.

#### 3 Exercícios de Fixação com Gabarito Comentado

#### Questões

1. (Cálculo de Chance/Odds) Se a probabilidade estimada de um cliente atrasar uma fatura é p = 0,25, qual é a sua Chance (Odds) de atraso?
2. (Interpretação de Razão de Chances) Um modelo logístico para concessão de crédito obteve um coeficiente $`\beta_1 = 0,6931`$ para a variável indicadora de histórico de restrição no nome. Calcule $`e^{\beta_1}`$ e interprete a Razão de Chances.
3. (Obtenção da Probabilidade p) Dado o modelo logístico estimado $`\text{Logit}(p) = -2,0 + 0,50 X_1`$, calcule a probabilidade estimada p para um indivíduo com $`X_1 = 4`$.

#### Gabarito Comentado

1. Resposta: Aplicando a fórmula da chance: $`\text{Odds} = \frac{p}{1-p} = \frac{0,25}{1 - 0,25} = \frac{0,25}{0,75} = \frac{1}{3} \approx 0,3333`$ A chance é de 0,3333 (ou 1 para 3).
2. Resposta: Exponenciando o coeficiente: $`\text{OR} = e^{0,6931} \approx 2,0000`$ A presença de histórico de restrição no nome dobra (aumenta em $`100\%`$) a chance (Odds) de inadimplência do cliente em relação a um cliente sem restrição.
3. Resposta: Primeiro, calcula-se o valor da combinação linear do Logit: $`\text{Logit} = -2,0 + 0,50(4) = -2,0 + 2,0 = 0,0`$ Em seguida, aplica-se a transformação Sigmoide para obter p: $`p = \frac{e^0}{1 + e^0} = \frac{1}{1 + 1} = \frac{1}{2} = 0,50 \quad (50\%)`$

Aprofundando a abordagem probabilística, exploramos o Teorema de Bayes e o algoritmo de classificação Naive Bayes.

### Aula 8: Probabilidade Condicional, Teorema de Bayes e Classificador Naive Bayes

#### Fonte

Baseado no vídeo: "Aprendizado de máquina estatístico - Revisão de Probabilidades e Naive Bayes com aplicação em Python" (Profa. Cibele Russo).

#### Objetivo de Aprendizagem

Revisar a Lei da Probabilidade Total, aplicar a inversão do condicionamento via Teorema de Bayes, compreender a suposição de independência condicional do algoritmo Naive Bayes e diferenciar suas variantes (GaussianNB, MultinomialNB e BernoulliNB).

#### Explicação Simples & Analogias

* Filtro de Spam por Palavras-Chave: Para determinar se um e-mail é "Spam" com base na presença de palavras isoladas ("desconto", "promoção", "grátis"), o Naive Bayes inverte o problema: ele utiliza o histórico para avaliar a frequência dessas palavras em e-mails que sabidamente eram Spam vs. e-mails legítimos.
* Por que é chamado de "Ingênuo" (Naive)?: Porque o algoritmo assume que, dada a classe da flor, a largura e o comprimento da pétala são variáveis totalmente independentes entre si. Na natureza, flores maiores tendem a ter tanto o comprimento quanto a largura aumentados simultaneamente. Apesar de essa premissa ser biologicamente falsa ("ingênua"), ela simplifica os cálculos matemáticos e funciona muito bem na prática.

#### Exemplo Numérico e Matemático Passo a Passo

## 1. Inversão pelo Teorema de Bayes

O Teorema de Bayes realiza a inversão da probabilidade condicional: $`P(Y = C_j \mid X) = \frac{P(Y = C_j) \cdot P(X \mid Y = C_j)}{P(X)}`$

#### onde:

* $`P(Y = C_j)`$ é a probabilidade a priori da classe $`C_j`$.
* $`P(X \mid Y = C_j)`$ é a verossimilhança conjunta do vetor de preditoras $`X = [X_1, X_2, \dots, X_p]`$.
* P(X) é a probabilidade marginal (constante de normalização).

## 2. A Premissa de Independência Condicional do Naive Bayes

Dada a classe $`C_j`$, assume-se que os atributos $`X_1, X_2, \dots, X_p`$ são condicionalmente independentes: $`P(X_1, X_2, \dots, X_p \mid Y = C_j) = \prod_{k=1}^p P(X_k \mid Y = C_j)`$

## 3. Decisão pelo Critério MAP (Maximum A Posteriori)

Como o denominador P(X) é idêntico para todas as classes, a regra de classificação seleciona a classe $`C_j`$ que maximiza o produto: $`\hat{Y} = \arg\max_{C_j} \left[ P(Y = C_j) \prod_{k=1}^p P(X_k \mid Y = C_j) \right]`$

## 4. Variantes do Naive Bayes no scikit-learn

* GaussianNB: Indicado para preditoras numéricas quantitativas contínuas, assumindo que $`P(X_k \mid Y = C_j)`$ segue uma distribuição Normal/Gaussiana.
* MultinomialNB: Indicado para dados discretos de contagem (ex: frequência de palavras em e-mails).
* BernoulliNB: Indicado para variáveis binárias de presença/ausência (0 ou 1).

## 5. Código Python Standalone com GaussianNB no Iris

```python
import pandas as pd
from sklearn.datasets import load_iris
from sklearn.model_selection import train_test_split
from sklearn.naive_bayes import GaussianNB
from sklearn.metrics import accuracy_score, confusion_matrix

# Carregando a base Iris
iris = load_iris()
X = iris.data
y = iris.target

# Divisao em treino (80%) e teste (20%)
X_train, X_test, y_train, y_test = train_test_split(
    X, y, test_size=0.2, random_state=42, stratify=y
)

# Instanciando e ajustando o Naive Bayes Gaussiano
gnb = GaussianNB()
gnb.fit(X_train, y_train)

# Previsoes na base de teste
y_pred = gnb.predict(X_test)

# Avaliacao de desempenho
acc = accuracy_score(y_test, y_pred)
print(f"Acuracia do Naive Bayes Gaussiano: {acc:.4f}")
print("Matriz de Confusao:\n", confusion_matrix(y_test, y_pred))

Erros Comuns de Alunos

* Acreditar que a violação da independência inutiliza o algoritmo: O Naive Bayes costuma ser rápido, estável e altamente competitivo em problemas de alta dimensionalidade (como filtragem de texto), mesmo quando os atributos possuem correlação parcial.
* Utilizar a variante errada para o tipo de dado: Aplicar MultinomialNB em variáveis numéricas contínuas padronizadas com valores negativos.

Resumo em 3 Pontos
```

1. O Teorema de Bayes permite calcular a probabilidade a posteriori $`P(Y \mid X)`$ invertendo o condicionamento da verossimilhança.
2. O Naive Bayes assume independência condicional entre as preditoras dada a classe, transformando probabilidades conjuntas em um produto de probabilidades unidimensionais.
3. Escolhe-se a variante do modelo segundo a natureza dos dados: GaussianNB (contínuos), MultinomialNB (contagens) ou BernoulliNB (binários).

#### 3 Exercícios de Fixação com Gabarito Comentado

#### Questões

1. (Aplicação do Teorema de Bayes) Em uma base de transações bancárias, a probabilidade a priori de fraude é $`P(\text{Fraude}) = 0,04`$. A probabilidade de uma transação vir de um IP estrangeiro dado que é fraude é $`P(\text{IP Estrangeiro} \mid \text{Fraude}) = 0,75`$. Sabendo que a probabilidade marginal global de uma transação vir de um IP estrangeiro é $`P(\text{IP Estrangeiro}) = 0,10`$, calcule a probabilidade a posteriori $`P(\text{Fraude} \mid \text{IP Estrangeiro})`$.
2. (Cálculo pelo Critério MAP) Considere um problema binário com classes $`C_1`$ e $`C_2`$, onde as probabilidades a priori são P(C_1) = 0,60 e P(C_2) = 0,40. Para duas variáveis observadas $`X_1`$ e $`X_2`$, as verossimilhanças são:
  * Para $`C_1: P(X_1 \mid C_1) = 0,50`$ e $`P(X_2 \mid C_1) = 0,20`$.
  * Para $`C_2: P(X_1 \mid C_2) = 0,10`$ e $`P(X_2 \mid C_2) = 0,80`$.

Utilizando o critério MAP do Naive Bayes, determine qual classe será atribuída ao ponto.

1. (Conceitual - Tipos de Naive Bayes) Qual classe do scikit-learn deve ser selecionada para classificar textos representados por vetores de contagem de palavras (Bag-of-Words)?

#### Gabarito Comentado

1. Resposta: Aplicando o Teorema de Bayes: $`P(\text{Fraude} \mid \text{IP Estrangeiro}) = \frac{P(\text{Fraude}) \cdot P(\text{IP Estrangeiro} \mid \text{Fraude})}{P(\text{IP Estrangeiro})} P(\text{Fraude} \mid \text{IP Estrangeiro}) = \frac{0,04 \times 0,75}{0,10} = \frac{0,03}{0,10} = 0,3000 \quad (30,00\%)`$
2. Resposta: Calcula-se o produto sem normalizador para cada classe:
  * Pontuação de $`C_1: P(C_1) \cdot P(X_1 \mid C_1) \cdot P(X_2 \mid C_1) = 0,60 \times 0,50 \times 0,20 = 0,0600`$.
  * Pontuação de $`C_2: P(C_2) \cdot P(X_1 \mid C_2) \cdot P(X_2 \mid C_2) = 0,40 \times 0,10 \times 0,80 = 0,0320`$.

Como 0,0600 > 0,0320, a classe atribuída pelo critério MAP é $`C_1`$.

1. Resposta: Deve-se utilizar a variante MultinomialNB, pois ela é desenhada especificamente para lidar com dados de frequência e contagem de ocorrências de termos em documentos.

Saindo dos métodos estatísticos e probabilísticos clássicos, entramos no estudo dos modelos inspirados na estrutura biológica: as Redes Neurais Artificiais.

### Aula 9: Introdução às Redes Neurais Artificiais e Arquitetura do Neurônio Simples

#### Fonte

Baseado no vídeo: "Aprendizado de máquina estatístico - Uma introdução às redes neurais artificiais - parte 1" (Profa. Cibele Russo).

#### Objetivo de Aprendizagem

Mapear a correspondência entre a estrutura do neurônio biológico e a unidade artificial de processamento, calcular a combinação linear $`\text{net}`$, compreender o papel geométrico do Viés (Bias) e aplicar a Função de Ativação Degrau Bipolar.

#### Explicação Simples & Analogias

* A Analogia Biológica detalhada:

| Componente Biológico | Equivalente Artificial | Função Matemática no Modelo |
|---|---|---|
| Dendritos | Entradas $`(X_1, X_2, \dots, X_p)`$ | VETOR DE PREDITORAS: Recebe os atributos de entrada. |
| Sinapses | Pesos $`(w_{11}, w_{12}, \dots, w_{1p})`$ | PARÂMETROS AJUSTÁVEIS: Ponderam a relevância de cada entrada. |
| Corpo Celular (Soma) | Combinador Linear $`(\text{net})`$ | INTEGRAÇÃO: Soma ponderada dos impulsos acrescida do Viés. |
| Axônio / Estímulo | Função de Ativação e Saída (Y) | TRANSFORMAÇÃO: Gera o sinal de saída (+1 ou -1). |

#### Exemplo Numérico e Matemático Passo a Passo

## 1. A Combinação Linear $`\text{net}`$

A unidade básica integra as p entradas $`X_j`$ multiplicadas pelos seus respectivos pesos $`w_{1j}`$, somada ao termo de viés ($`\theta`$ ou $`b): \text{net} = \sum_{j=1}^p w_{1j} X_j + \theta = w_{11} X_1 + w_{12} X_2 + \dots + w_{1p} X_p + \theta`$

## 2. O Papel Geométrico do Viés $`(\theta)`$

O termo de viés $`\theta`$ é fundamental porque permite que o hiperplano de decisão seja transladado para longe da origem (0,0). Sem o viés $`(\theta = 0)`$, qualquer hiperplano de separação seria forçado a passar pelo ponto central do espaço, reduzindo drasticamente a capacidade do modelo.

## 3. Função de Ativação Degrau Bipolar

Nesta aula teórica introdutória, apresenta-se a Função Degrau Bipolar com limiar $`\Delta`$, cujo domínio de saída é $`\{-1, +1\}: f(\text{net}) = \begin{cases} +1, & \text{se } \text{net} \ge \Delta \\ -1, & \text{se } \text{net} < \Delta \end{cases}`$

(Nota Didática Importante): Fique atento ao domínio de saída da função de ativação! Nesta Aula 9, utilizamos o formato Bipolar $`(\{-1, +1\})`$ para ilustrar a teoria clássica de McCulloch-Pitts. Na Aula 10, ao resolver a porta lógica AND, adotaremos o formato Binário $`(\{0, 1\})`$.

## 4. Exemplo Numérico Manual Completo

#### Considere um neurônio com os seguintes parâmetros:

* Entradas: $`X_1 = 0,5, X_2 = 1,0`$
* Pesos: $`w_{11} = 0,8, w_{12} = -0,4`$
* Viés: $`\theta = 0,2`$
* Limiar da Ativação Bipolar: $`\Delta = 0,5`$

Cálculo da combinação linear $`\text{net}: \text{net} = (0,8 \times 0,5) + (-0,4 \times 1,0) + 0,2 = 0,4 - 0,4 + 0,2 = 0,2`$

Aplicação da Função Degrau Bipolar $`f(\text{net})`$: Como $`\text{net} = 0,2 < \Delta = 0,5`$, a saída ativada é $`f(\text{net}) = -1`$.

#### Erros Comuns de Alunos

* Confundir Pesos (W) com Entradas (X): As entradas X são os dados fixos observados das amostras; os pesos W são os parâmetros dinâmicos que o algoritmo ajusta durante o treinamento.
* Omitir o Viés $`(\theta)`$: Forçar a reta ou hiperplano a passar obrigatoriamente pela origem (0,0), impedindo a classificação de conjuntos de dados transladados.

#### Resumo em 3 Pontos

1. O neurônio artificial integra estímulos externos multiplicando entradas X por pesos W e somando o termo de viés $`\theta`$.
2. O viés $`\theta`$ translada o hiperplano no espaço, permitindo separar classes fora da origem.
3. A função de ativação mapeia a soma linear contínua $`\text{net}`$ em um sinal de saída discreto ou limitado.

#### 3 Exercícios de Fixação com Gabarito Comentado

#### Questões

1. (Cálculo do Valor $`\text{net}`$) Um neurônio simples recebe as entradas $`X_1 = 2,0`$ e $`X_2 = 3,0`$, com os pesos $`w_{11} = 1,5`$ e $`w_{12} = -0,5`$, e viés $`\theta = 1,0`$. Calcule o valor da combinação linear $`\text{net}`$.
2. (Aplicação da Ativação Bipolar) Utilizando o valor de $`\text{net}`$ obtido no exercício 1 e uma função de ativação degrau bipolar com limiar $`\Delta = 2,0`$ (retorna +1 se $`\text{net} \ge 2,0`$ e -1 caso contrário), qual será a saída emitida pelo neurônio?
3. (Equação da Fronteira) Dados os pesos $`w_{11} = 2,0, w_{12} = 4,0`$ e viés $`\theta = -8,0`$, encontre a equação da reta de decisão no plano $`(X_1, X_2)`$ definida por $`\text{net} = 0`$.

#### Gabarito Comentado

1. Resposta: $`\text{net} = (1,5 \times 2,0) + (-0,5 \times 3,0) + 1,0 = 3,0 - 1,5 + 1,0 = 2,5`$
2. Resposta: Como $`\text{net} = 2,5 \ge 2,0`$ (limiar $`\Delta`$), a saída da função degrau bipolar é +1.
3. Resposta: A fronteira de decisão ocorre quando $`\text{net} = 0`$: $`2,0 X_1 + 4,0 X_2 - 8,0 = 0 \Rightarrow 4,0 X_2 = -2,0 X_1 + 8,0 \Rightarrow X_2 = -0,50 X_1 + 2,0`$ Trata-se de uma reta com inclinação -0,50 e intercepto no eixo $`X_2`$ igual a 2,0.

Apresentada a arquitetura estática do neurônio simples, avançamos para o algoritmo dinâmico de aprendizado supervisionado Perceptron.

### Aula 10: O Algoritmo Perceptron e Treinamento com a Porta Lógica AND

#### Fonte

Baseado no vídeo: "Aprendizado de máquina estatístico - Redes neurais artificiais 2 - Algoritmo perceptron - AND lógico" (Profa. Cibele Russo).

#### Objetivo de Aprendizagem

Executar o algoritmo de aprendizado supervisionado do Perceptron de camada única, aplicar a regra de atualização de pesos com taxa de aprendizado $`\eta`$, utilizar a função de ativação degrau binária e demonstrar a convergência para o operador lógico AND.

#### Explicação Simples & Analogias

* Ajuste de Alvo por Correção Proporcional ao Erro: O Perceptron analisa uma amostra e realiza uma previsão $`\hat{Y}`$. Se acertar, nenhum parâmetro é alterado $`(\text{Erro} = 0)`$. Se errar, o algoritmo ajusta os pesos dando um passo proporcional ao erro $`(Y_i - \hat{Y}_i)`$ na direção da entrada $`X_{ji}`$.

#### Exemplo Numérico Resolvido Passo a Passo (Rastreamento Rígido da Fonte)

Resolveremos a porta lógica AND com saídas binárias $`Y \in \{0, 1\}`$.

## 1. Tabela Verdade da Porta Lógica AND

| Observação (i) | Entrada $`X_1`$ | Entrada $`X_2`$ | Saída Alvo Real $`(Y_i)`$ |
|---|---|---|---|
| 1 | 0 | 0 | 0 |
| 2 | 1 | 0 | 0 |
| 3 | 0 | 1 | 0 |
| 4 | 1 | 1 | 1 |

## 2. Parâmetros e Regras Fixadas na Aula da Profa. Cibele Russo

* Pesos Iniciais: $`w_{11} = 1,2, w_{12} = 0,6`$.
* Viés Fixo: b = 1,0 (mantido constante neste exercício didático).
* Taxa de Aprendizado: $`\eta = 0,5`$.
* Limiar de Ativação Binária: $`\Delta = 2,0`$.
* Regra de Decisão Binária: $`\text{net}_i = w_{11} X_{1i} + w_{12} X_{2i} + b \hat{Y}_i = \begin{cases} 1, & \text{se } \text{net}_i \ge 2,0 \\ 0, & \text{se } \text{net}_i < 2,0 \end{cases}`$
* Regra de Atualização de Pesos em Erro: $`\Delta w_{1j} = \eta \cdot (Y_i - \hat{Y}_i) \cdot X_{ji} w_{1j}^{(\text{novo})} = w_{1j}^{(\text{atual})} + \Delta w_{1j}`$

## 3. Tabela de Rastreamento Passo a Passo do Algoritmo Perceptron

| Época / Iteração | Obs (i) | $`(X_1, X_2)`$ | Cálculo do $`\text{net}`$ | Predição $`\hat{Y}`$ | Alvo Y | Erro $`(Y - \hat{Y})`$ | Ação / Atualização de Pesos |
|---|---|---|---|---|---|---|---|
| Época 1 | 1 | (0, 0) | 1,2(0) + 0,6(0) + 1 = 1,0 | 0 | 0 | 0 | Acerto! Pesos mantidos: W = [1,2; 0,6]. |
| Época 1 | 2 | (1, 0) | 1,2(1) + 0,6(0) + 1 = 2,2 | 1 | 0 | -1 | Erro! $`\Delta w_1`$ = 0,5(-1)(1) = -0,5.<br>W_1 $`\leftarrow 1,2 - 0,5 = 0,7; W_2 \leftarrow 0,6`$. |
| Época 2 | 1 | (0, 0) | 0,7(0) + 0,6(0) + 1 = 1,0 | 0 | 0 | 0 | Acerto! Pesos mantidos: W = [0,7; 0,6]. |
| Época 2 | 2 | (1, 0) | 0,7(1) + 0,6(0) + 1 = 1,7 | 0 | 0 | 0 | Acerto! Pesos mantidos: W = [0,7; 0,6]. |
| Época 2 | 3 | (0, 1) | 0,7(0) + 0,6(1) + 1 = 1,6 | 0 | 0 | 0 | Acerto! Pesos mantidos: W = [0,7; 0,6]. |
| Época 2 | 4 | (1, 1) | 0,7(1) + 0,6(1) + 1 = 2,3 | 1 | 1 | 0 | Acerto! Pesos mantidos: W = [0,7; 0,6]. |

Conclusão da Convergência: Na Época 2, todas as 4 observações foram reavaliadas com os novos pesos $`W_1 = 0,7`$ e $`W_2 = 0,6`$ e obtiveram $`100\%`$ de acerto. O algoritmo convergiu com sucesso.

#### Erros Comuns de Alunos

* Atualizar pesos quando a previsão do modelo está correta: Aplicar modificações nos pesos quando o erro $`(Y_i - \hat{Y}_i)`$ é zero.
* Tentar resolver problemas não linearmente separáveis (como o XOR) com o Perceptron de camada única: O Perceptron de camada única só converge se as classes puderem ser separadas por um único hiperplano. Aplicá-lo ao problema do XOR fará o algoritmo entrar em um loop infinito.

#### Resumo em 3 Pontos

1. O algoritmo Perceptron ajusta seus pesos na direção proporcional ao erro $`(Y_i - \hat{Y}_i)`$ multiplicado pela taxa de aprendizado $`\eta`$ e a entrada $`X_{ji}`$.
2. A convergência perfeita do Perceptron para erro zero é matematicamente garantida para dados linearmente separáveis (Teorema da Convergência do Perceptron).
3. Para problemas não linearmente separáveis, deve-se limitar o número máximo de épocas para interromper o treinamento.

#### 3 Exercícios de Fixação com Gabarito Comentado

#### Questões

1. (Treinamento da Porta Lógica OR) Considere a porta lógica OR com saídas $`Y \in \{0, 1\}`$ (onde Y=0 apenas se $`X_1=0`$ e $`X_2=0`$, e Y=1 caso contrário). Suponha os pesos iniciais $`w_1 = 0,5, w_2 = 0,5`$, viés b = 0, taxa de aprendizado $`\eta = 0,5`$ e limiar $`\Delta = 0,5`$. Teste a amostra $`X_1 = 0, X_2 = 1`$ (Alvo Y = 1). O Perceptron acertará a previsão? Haverá atualização de pesos?
2. (Cálculo de Atualização de Pesos) No mesmo contexto da questão 1, avalie a amostra $`X_1 = 1, X_2 = 0`$ (Alvo Y = 1). Se os pesos estivessem em $`w_1 = 0,1`$ e $`w_2 = 0,1`$, resultando em $`\text{net} = 0,1 < 0,5 (\hat{Y} = 0)`$, calcule os novos valores atualizados dos pesos $`w_1`$ e $`w_2`$.
3. (Conceitual - Limitação da Camada Única) Por que o Perceptron de camada única não consegue resolver a porta lógica XOR (Ou Exclusivo)?

#### Gabarito Comentado

1. Resposta:
  * Cálculo do $`\text{net}: \text{net} = 0,5(0) + 0,5(1) + 0 = 0,5`$.
  * Como $`\text{net} = 0,5 \ge 0,5`$, a previsão é $`\hat{Y} = 1`$.
  * Como o Alvo é Y = 1, o modelo acertou! Erro = 1 - 1 = 0. Os pesos não sofrem alteração $`(\Delta w = 0)`$.
2. Resposta:
  * Erro: $`Y - \hat{Y} = 1 - 0 = +1`$.
  * Atualização do peso $`w_1: \Delta w_1 = \eta \cdot (Y - \hat{Y}) \cdot X_1 = 0,5 \times (+1) \times 1 = +0,5`$.
  * Novo $`w_1 = 0,1 + 0,5 = 0,6`$.
  * Atualização do peso $`w_2: \Delta w_2 = \eta \cdot (Y - \hat{Y}) \cdot X_2 = 0,5 \times (+1) \times 0 = 0`$.
  * Novo $`w_2 = 0,1 + 0 = 0,1`$.
3. Resposta: Porque o operador lógico XOR não é linearmente separável no plano $`2\text{D}`$. Não existe nenhuma reta capaz de separar os pontos de classe 0 nas posições (0,0) e (1,1) dos pontos de classe 1 nas posições (1,0) e (0,1).

Para superar a limitação da separabilidade linear e resolver problemas complexos como o XOR, avançamos para as Redes Neurais Multicamadas.

### Aula 11: Redes Neurais Multicamadas (MLP), Funções Não Lineares e Backpropagation

#### Fonte

Baseado no vídeo: "Aprendizado de máquina estatístico - Introdução a Redes neurais multicamadas - Multilayer perceptron" (Profa. Cibele Russo).

#### Objetivo de Aprendizagem

Compreender a arquitetura da Multilayer Perceptron (MLP), demonstrar matematicamente por que funções de ativação não lineares são indispensáveis para evitar o colapso do modelo em uma camada única, e dominar a derivação do algoritmo Backpropagation via regra da cadeia do cálculo.

#### Explicação Simples & Analogias

* A Geometria do XOR: Para separar as classes da porta lógica XOR, é impossível utilizar uma única reta. São necessárias pelo menos duas retas combinadas operadas por neurônios em uma camada escondida/oculta para isolar as regiões do espaço.
* A Linha de Montagem de Veículos:
  * Passo para Frente (Forward Pass): As variáveis de entrada atravessam as camadas ocultas até a saída, onde a previsão $`\hat{Y}`$ é gerada e o erro global E é medido.
  * Passo para Trás (Backward Pass): O erro E é propagado de trás para frente, avaliando a "responsabilidade" de cada peso no resultado final e ajustando suas conexões.

#### Exemplo Numérico, Matemático e Arquitetural Passo a Passo

## 1. Principais Funções de Ativação Não Lineares

| Função de Ativação | Fórmula em LaTeX | Intervalo de Saída | Propriedade & Aplicação |
|---|---|---|---|
| Linear | f(x) = x | $`(-\infty, +\infty)`$ | Não insere não linearidade. Usada em regressão na camada de saída. |
| Sigmoide (Logística) | $`f(x) = \frac{1}{1 + e^{-x}}`$ | (0, 1) | Suave e contínua. Utilizada para probabilidade na saída de classificadores. |
| Tangente Hiperbólica (Tanh) | $`f(x) = \frac{e^x - e^{-x}}{e^x + e^{-x}}`$ | (-1, +1) | Centrada no zero. Facilita a convergência nas camadas ocultas. |
| ReLU (Rectified Linear Unit) | $`f(x) = \max(0, x)`$ | [$`0, +\infty`$) | Eficiente computacionalmente; combate o esvanecimento do gradiente. |

```text
    Função Sigmoide               Função ReLU
      1 |      /--             |       /
        |     /                |      /
    0.5 |    /                 |     /
        | --/                  |    /
      0 +----------           -+---/-------
       -3  0  3                   0
```

2. Prova Matemática: Por que Ativações Lineares Colapsam a Rede?

Considere uma rede MLP com vetor de entrada X, uma camada oculta Y = A $`\cdot X`$ e uma camada de saída $`Z = B \cdot Y`$, onde A e B são matrizes de pesos lineares.

Substituindo Y na equação de Z: $`Z = B \cdot`$ (A $`\cdot X) = (B \cdot`$ A) $`\cdot X = W_{\text{equivalente}} \cdot X`$ Como o produto de duas matrizes constantes $`B \cdot`$ A resulta em uma única matriz $`W_{\text{equivalente}}`$, uma rede de 100 camadas ocultas que utilize apenas ativações lineares é matematicamente equivalente a uma rede simples de camada única sem camadas ocultas!

## 3. O Algoritmo Backpropagation e a Regra da Cadeia

O objetivo é minimizar a função de perda quadrática global dos pesos: E = $`\frac{1}{2} \sum_{i=1}^N (Y_i - \hat{Y}_i)^2`$

Para atualizar um peso $`w_{jl}`$ localizado em uma camada oculta intermediária, aplica-se a Regra da Cadeia do Cálculo diferencial para decompor a derivada parcial do erro: $`\frac{\partial E}{\partial w_{jl}} = \frac{\partial E}{\partial \hat{Y}_l} \cdot \frac{\partial \hat{Y}_l}{\partial \text{net}_l} \cdot \frac{\partial \text{net}_l}{\partial w_{jl}}`$

#### Onde:

* $`\frac{\partial \text{net}_l}{\partial w_{jl}} = X_j`$ (o sinal de entrada recebido do neurônio anterior).
* Definindo o termo de erro retropropagado como $`\delta_l = -\frac{\partial E}{\partial \text{net}_l}`$, a regra de atualização do Gradiente Descendente se reduz a: $`w_{jl}^{(t+1)} = w_{jl}^{(t)} + \eta \cdot X_j \cdot \delta_l`$

#### Erros Comuns de Alunos

* Utilizar funções de ativação lineares nas camadas ocultas: Acreditar que adicionar mais camadas ocultas resolverá problemas complexos como o XOR mantendo ativações lineares.
* Utilizar funções não diferenciáveis: Escolher funções de ativação descontinuas que impedem o cálculo de derivadas parciais durante a etapa Backward Pass.

#### Resumo em 3 Pontos

1. A arquitetura MLP resolve problemas complexos e não linearmente separáveis (como o XOR) utilizando camadas ocultas e funções não lineares.
2. Sem ativações não lineares, a composição de transformações lineares colapsa matematicamente em um modelo simples de camada única.
3. O algoritmo Backpropagation treina a rede alternando passos Forward (geração de previsões) e Backward (ajuste de pesos via Regra da Cadeia e Gradiente Descendente).

#### 3 Exercícios de Fixação com Gabarito Comentado

#### Questões

1. (Ativação ReLU) Calcule a saída da função de ativação ReLU $`f(x) = \max(0, x)`$ para os valores de entrada $`x_1 = -4,2, x_2 = 0,0`$ e $`x_3 = 3,7`$.
2. (Derivada da Sigmoide) A derivada da função Sigmoide S(x) possui a propriedade S'(x) = $`S(x) \cdot (1 - S(x))`$. Se em um neurônio a saída ativada foi S(x) = 0,70, calcule o valor exato da derivada a ser multiplicada na etapa do Backpropagation.
3. (Conceitual - Passos Forward e Backward) Diferencie resumidamente as atribuições da etapa Forward Pass e da etapa Backward Pass no treinamento de uma rede MLP.

#### Gabarito Comentado

1. Resposta: Aplicando $`f(x) = \max(0, x)`$:
  * Para $`x_1 = -4,2`$: $`f(-4,2) = \max(0, -4,2) = 0,0`$.
  * Para $`x_2 = 0,0`$: $`f(0,0) = \max(0, 0,0) = 0,0`$.
  * Para $`x_3 = 3,7`$: $`f(3,7) = \max(0, 3,7) = 3,7`$.
2. Resposta: Aplicando a fórmula da derivada: S'(x) = $`0,70 \times (1 - 0,70) = 0,70 \times 0,30 = 0,2100`$ O valor do gradiente local retornado para a regra da cadeia é 0,2100.
3. Resposta:
  * Forward Pass: Transporta os dados de entrada através das camadas ocultas até a camada de saída para gerar a previsão $`\hat{Y}`$ e calcular o erro global E.
  * Backward Pass: Propaga o erro E de trás para frente na rede, aplicando a Regra da Cadeia e o Gradiente Descendente para atualizar iterativamente todos os pesos e vieses.

#### Conclusão da Jornada de Aprendizado

Parabéns! Você concluiu com êxito a Trilha de Aprendizagem e Guia de Estudos em Aprendizado de Máquina Estatístico, baseada no curso da Professora Dra. Cibele Russo (USP São Carlos).

#### Ao longo desta jornada de 11 módulos, você construiu uma sólida base acadêmica e prática:

* Compreendeu a fundamentação teórica da IA e o rigor do pré-processamento de dados.
* Formalizou o problema estatístico de classificação e dominou o Classificador Teórico de Bayes.
* Diagnosticou modelos via Matriz de Confusão, métricas completas e análise de Curvas ROC/AUC.
* Dominou modelos baseados em distância (KNN), modelos paramétricos (Regressão Logística) e probabilísticos (Naive Bayes).
* Compreendeu a arquitetura de Redes Neurais Artificiais, dominando o treinamento do Perceptron e a matemática do algoritmo Backpropagation em Redes Multicamadas (MLP).

Estes fundamentos estatísticos e computacionais constituem o alicerce indispensável para o domínio de técnicas avançadas de Ciência de Dados, Deep Learning e Inteligência Artificial. Continue praticando, ajustando modelos e explorando novas bases de dados reais!
