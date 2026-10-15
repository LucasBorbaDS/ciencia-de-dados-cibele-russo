> Material derivado das aulas da Profa. Cibele Russo (ICMC/USP), organizado com auxílio do NotebookLM. [↩ Voltar à trilha](README.md)

# Guia de Estudos: Trilha Didática de Análise Multivariada e Aprendizado Não-Supervisionado

## SUMÁRIO GERAL DA TRILHA

| Módulo | Aula | Título da Aula | Conceito-Chave | Tempo Estimado |
|---|---|---|---|---|
| Módulo 1 | Aula 1 | Análise Descritiva Multivariada: Matrizes, Médias e Matrizes de Variância-Covariância | Estruturação $`X_{n \times p}`$, Vetor de Médias e Matrizes S e R | 15 min |
|   | Aula 2 | Vetores Aleatórios, Matrizes e Propriedades das Transformações Lineares | Operações com E(AX+B) e Var(AX+B) | 15 min |
| Módulo 2 | Aula 3 | Distribuição Normal Multivariada: Densidade, Geometria e Distância de Mahalanobis | $`FDP N_p(\mu, \Sigma)`$, Contornos Elípticos e Distância Estatística | 20 min |
| Módulo 3 | Aula 4 | Teste $`T^2`$ de Hotelling para um Vetor de Médias e Elipsoides de Confiança | Testes de Hipóteses $`H_0: \mu = \mu_0`$ e Conversão para Distribuição F | 20 min |
|   | Aula 5 | Comparação de Vetores de Médias: Amostras Pareadas e Independentes | $`T^2`$ para Diferenças Pareadas, Matriz $`S_{pooled}`$ e Teste M de Box | 20 min |
|   | Aula 6 | MANOVA: Comparação de G Grupos Multivariados e Estatística Lambda de Wilks | Decomposição T = B + W e Teste Lambda de Wilks | 20 min |
| Módulo 4 | Aula 7 | Regressão Linear Multivariada: Múltiplas Respostas e Múltiplos Preditores | Modelo $`Y = Z\beta`$ + E, Mínimos Quadrados e Diagnóstico de Resíduos | 20 min |
|   | Aula 8 | Análise de Correlações Canônicas: Associando Blocos de Variáveis | Variáveis Canônicas $`(U_k, V_k)`$ e Otimização Restrita | 20 min |
| Módulo 5 | Aula 9 | Análise de Componentes Principais (PCA): Teoria e Decomposição Espectral | Transformação Ortogonal, Autovalores e Variância Explicada | 20 min |
|   | Aula 10 | Aplicação de PCA: Interpretação de Scores, Loadings e Scree Plot | Seleção de Componentes, Scree Plot, Loadings e Scores em Python | 20 min |
| Módulo 6 | Aula 11 | Clustering Hierárquico Aglomerativo: Distâncias, Métodos de Ligação e Dendrogramas | Matrizes de Dissimilaridade, Métodos de Ligação e Corte do Dendrograma | 25 min |
|   | Aula 12 | Clustering Não-Hierárquico: O Algoritmo k-Médias (k-means) e Mapeamento Geográfico | Algoritmo Iterativo, Método do Cotovelo e Inércia Intra-cluster | 20 min |
| Módulo 7 | Aula 13 | Análise Discriminante Linear (LDA) e Regressão Logística para Classificação | Classificação Supervisionada, Fronteiras Lineares e Validação Treino/Teste | 20 min |
|   | Aula 14 | Introdução à Análise de Correspondência (CA) e Síntese de Aprendizado Multivariado | Tabelas de Contingência, Decomposição em Valores Singulares e Mapa Global | 20 min |

## DESENVOLVIMENTO DAS AULAS DA TRILHA

## MÓDULO 1: FUNDAMENTOS DESCRITIVOS E NOTAÇÃO MATRICIAL

### Aula 1: Análise Descritiva Multivariada: Matrizes, Médias e Matrizes de Variância-Covariância

## 1. Título da Aula

Análise Descritiva Multivariada: Matrizes, Médias e Matrizes de Variância-Covariância.

## 2. Objetivo de Aprendizagem

Aprender a organizar conjuntos de dados multivariados em matrizes de dimensão $`n \times p`$ e calcular formalmente vetores de médias amostrais $`(\bar{X})`$, matrizes de variância-covariância (S) e matrizes de correlação (R).

## 3. Fonte Original

Vídeo "Análise Multivariada e Aprendizado Não-Supervisionado - Análise descritiva" (Profa. Cibele Russo).

## 4. Explicação Simples com Analogias

Analisar uma única variável é como olhar para a fotografia frontal de uma pessoa: temos apenas a informação da altura. A análise multivariada é equivalente a um modelo tridimensional completo, no qual observamos simultaneamente altura, peso e largura dos ombros, capturando como essas diferentes dimensões mudam e se relacionam juntas no mesmo indivíduo.

## 5. Diagrama Visual ASCII

```text
   Estrutura da Matriz de Dados Multivariados X (n x p)

            Variável 1   Variável 2   ...   Variável p
          +------------+------------+-----+------------+
  Obs 1   |   x_11     |   x_12     | ... |   x_1p     |
  Obs 2   |   x_21     |   x_22     | ... |   x_2p     |  ===> Vetor de Médias X_barra (p x 1)
   ...    |    ...     |    ...     | ... |    ...     |  ===> Matriz de Covariância S (p x p)
  Obs n   |   x_n1     |   x_n2     | ... |   x_np     |  ===> Matriz de Correlação R (p x p)
          +------------+------------+-----+------------+
```

## 6. Exemplo Numérico Resolvido Passo a Passo

Considere o registro de vendas de livros com n = 4 vendas (observações) e p = 2 variáveis: $`X_1`$ = valor da nota em R\$, e $`X_2`$ = número de livros vendidos.

Os dados observados são organizados na matriz de dados $`X_{4 \times 2}`$: $`X = \begin{bmatrix} 42 & 2 \\ 52 & 3 \\ 48 & 2 \\ 58 & 3 \end{bmatrix}`$

Passo 1: Vetor de Médias Amostrais $`(\bar{X}_{2 \times 1}) \bar{x}_1 = \frac{42 + 52 + 48 + 58}{4} = \frac{200}{4} = 50 \bar{x}_2 = \frac{2 + 3 + 2 + 3}{4} = \frac{10}{4} = 2,5 \bar{X} = \begin{bmatrix} \bar{x}_1 \\ \bar{x}_2 \end{bmatrix} = \begin{bmatrix} 50 \\ 2,5 \end{bmatrix}`$

Passo 2: Variâncias e Covariâncias Amostrais $`(S_{2 \times 2})`$ Utilizando a fórmula da covariância amostral com divisor $`n = 4: s_{ik} = \frac{1}{n}\sum_{j=1}^{n}(x_{ji} - \bar{x}_i)(x_{jk} - \bar{x}_k)`$

* Variância de $`X_1: s_{11} = \frac{(42-50)^2 + (52-50)^2 + (48-50)^2 + (58-50)^2}{4} = \frac{(-8)^2 + 2^2 + (-2)^2 + 8^2}{4} = \frac{64 + 4 + 4 + 64}{4} = \frac{136}{4} = 34`$
* Variância de $`X_2: s_{22} = \frac{(2-2,5)^2 + (3-2,5)^2 + (2-2,5)^2 + (3-2,5)^2}{4} = \frac{(-0,5)^2 + 0,5^2 + (-0,5)^2 + 0,5^2}{4} = \frac{0,25 + 0,25 + 0,25 + 0,25}{4} = \frac{1,0}{4} = 0,25`$
* Covariância entre $`X_1`$ e $`X_2: s_{12} = \frac{(-8)(-0,5) + (2)(0,5) + (-2)(-0,5) + (8)(0,5)}{4} = \frac{4 + 1 + 1 + 4}{4} = \frac{10}{4} = 2,5`$

Portanto, a matriz de covariância S é: $`S = \begin{bmatrix} 34 & 2,5 \\ 2,5 & 0,25 \end{bmatrix}`$

Passo 3: Matriz de Correlação Amostral $`(R_{2 \times 2}) r_{12} = \frac{s_{12}}{\sqrt{s_{11} s_{22}}} = \frac{2,5}{\sqrt{34 \times 0,25}} = \frac{2,5}{\sqrt{8,5}} \approx \frac{2,5}{2,915476} \approx 0,8575`$ $`R = \begin{bmatrix} 1 & 0,8575 \\ 0,8575 & 1 \end{bmatrix}`$

## 7. Implementação Computacional (Python)

```python
import numpy as np
import pandas as pd

# Matriz de dados X (4x2)
X = np.array([[42, 2],
              [52, 3],
              [48, 2],
              [58, 3]])

# Vetor de médias
x_bar = np.mean(X, axis=0)

# Matriz de covariância amostral (ddof=0 para divisor n)
S = np.cov(X, rowvar=False, ddof=0)

# Matriz de correlação
R = np.corrcoef(X, rowvar=False)

print("Vetor de Médias:\n", x_bar)
print("Matriz de Covariância S:\n", S)
print("Matriz de Correlação R:\n", R)
```

## 8. Erros Comuns e Como Evitá-los

* Erro: Confundir a média amostral ($`\bar{x}_k`$, uma estatística calculada a partir de dados amostrais) com o valor esperado populacional ($`\mu_k`$, um parâmetro obtido via integração ou probabilidade teórica).
* Como evitar: Utilize rigorosamente a barra sobre a variável $`(\bar{x})`$ para estatísticas amostrais (obtidas por divisões por n ou n-1) e a letra grega $`\mu`$ para valores esperados populacionais.

## 9. Resumo da Aula em 3 Pontos

1. A matriz de dados $`X_{n \times p}`$ armazena n observações nas linhas e p variáveis nas colunas.
2. O vetor de médias $`\bar{X}_{p \times 1}`$ condensa o centro de gravidade amostral de cada uma das p variáveis.
3. A covariância $`s_{ik}`$ varia na escala das variáveis, enquanto a correlação $`r_{ik}`$ é estritamente padronizada no intervalo [-1, 1].

Aplicações e Tomada de Decisão Executiva: Em relatórios executivos, apresentar apenas médias isoladas mascara riscos operacionais severos. A matriz de covariância revela a variabilidade conjunta dos ativos ou indicadores comerciais, permitindo que executivos identifiquem redundâncias operacionais e diversifiquem portfólios com base em variáveis fortemente correlacionadas (r > 0,70).

## 10. Exercícios Práticos com Gabarito Comentado Passo a Passo

Exercício 1: Dada a matriz de dados $`X = \begin{bmatrix} 10 & 20 \\ 20 & 40 \end{bmatrix}`$ com n=2 e p=2, calcule o vetor de médias amostrais $`\bar{X}`$. Gabarito Passo a Passo:

1. Média de $`X_1: \bar{x}_1 = \frac{10 + 20}{2} = \frac{30}{2} = 15`$.
2. Média de $`X_2: \bar{x}_2 = \frac{20 + 40}{2} = \frac{60}{2} = 30`$.
3. Vetor coluna de médias: $`\bar{X} = \begin{bmatrix} 15 \\ 30 \end{bmatrix}`$.

Exercício 2: Se a covariância entre duas variáveis é $`s_{12} = 6`$, e as variâncias são $`s_{11} = 16`$ e $`s_{22} = 9`$, calcule a correlação amostral $`r_{12}`$. Gabarito Passo a Passo:

1. Identifique o denominador: $`\sqrt{s_{11} \cdot s_{22}} = \sqrt{16 \cdot 9} = \sqrt{144} = 12`$.
2. Aplique a fórmula: $`r_{12} = \frac{s_{12}}{\sqrt{s_{11} s_{22}}} = \frac{6}{12} = 0,50`$.

Exercício 3: Demonstre por que a diagonal principal da matriz de correlação R é sempre composta por números iguais a 1. Gabarito Passo a Passo:

1. A correlação da variável $`X_k`$ com ela mesma é dada por $`r_{kk} = \frac{s_{kk}}{\sqrt{s_{kk} \cdot s_{kk}}}`$.
2. Simplificando o denominador: $`\sqrt{s_{kk}^2} = s_{kk}`$.
3. Logo, $`r_{kk} = \frac{s_{kk}}{s_{kk}} = 1`$ para todo $`k = 1, \dots, p`$.

A transição da descrição tabular de dados para a modelagem teórica exige a formalização algébrica do comportamento de vetores de variáveis aleatórias.

### Aula 2: Vetores Aleatórios, Matrizes e Propriedades das Transformações Lineares

## 1. Título da Aula

Vetores Aleatórios, Matrizes e Propriedades das Transformações Lineares.

## 2. Objetivo de Aprendizagem

Capacitar o estudante a manipular algebraicamente vetores aleatórios e aplicar as propriedades operacionais do valor esperado E(AX + B) e da matriz de variância-covariância Var(AX + B).

## 3. Fonte Original

Vídeo "Análise Multivariada e Aprendizado Não-Supervisionado - Aula 4a Distribuição Normal Multivariada" (Profa. Cibele Russo).

## 4. Explicação Simples com Analogias

Imagine alterar a escala e a orientação de um mapa geográfico: multiplicar um vetor aleatório por uma matriz A equivale a girar, esticar e comprimir os eixos de coordenadas, alterando a dispersão (variabilidade). Somar um vetor constante B equivale simplesmente a deslocar todo o mapa para uma nova posição na mesa, alterando a média sem modificar as distâncias internas (variâncias).

## 5. Diagrama Visual ASCII

```text
                     Transformação Linear: Y = A*X + B

  Espaço Original (X)           Operação Matricial A              Espaço Transformado (Y)
    [ E(X) = mu ]            +-----------------------+              [ E(Y) = A*mu + B ]
    [ Var(X) = Sigma ]  ===> | A: Rotação / Escala   |  ========>   [ Var(Y) = A*Sigma*A^T ]
                             | B: Traslação (Offset) |
                             +-----------------------+
```

## 6. Exemplo Numérico Resolvido Passo a Passo

Seja $`X = \begin{bmatrix} X_1 \\ X_2 \end{bmatrix}`$ um vetor aleatório bivariado com vetor de médias $`\mu = \begin{bmatrix} 1 \\ 2 \end{bmatrix}`$ e matriz de covariância $`\Sigma = \begin{bmatrix} 4 & 1 \\ 1 & 3 \end{bmatrix}`$.

Considere a transformação linear escalar Y = A X + B, em que A = $`a^T = \begin{bmatrix} 2 & -1 \end{bmatrix}`$ e B = 5. Ou seja, Y = 2X_1 - $`X_2 + 5`$.

Passo 1: Calcular o Valor Esperado E(Y) $`E(Y) = E(a^T X + B) = a^T E(X) + B = a^T \mu + B`$ $`E(Y) = \begin{bmatrix} 2 & -1 \end{bmatrix} \begin{bmatrix} 1 \\ 2 \end{bmatrix} + 5 = (2 \cdot 1 + (-1) \cdot 2) + 5 = (2 - 2) + 5 = 5`$

Passo 2: Calcular a Variância Var(Y) $`Var(Y) = Var(a^T X + B) = a^T Var(X)`$ a = $`a^T \Sigma`$ a Primeiro, calcule o produto $`a^T \Sigma: a^T \Sigma = \begin{bmatrix} 2 & -1 \end{bmatrix} \begin{bmatrix} 4 & 1 \\ 1 & 3 \end{bmatrix} = \begin{bmatrix} (2 \cdot 4 + (-1) \cdot 1) & (2 \cdot 1 + (-1) \cdot 3) \end{bmatrix} = \begin{bmatrix} 7 & -1 \end{bmatrix}`$ Agora, multiplique pelo vetor coluna a: $`Var(Y) = \begin{bmatrix} 7 & -1 \end{bmatrix} \begin{bmatrix} 2 \\ -1 \end{bmatrix} = 7 \cdot 2 + (-1)(-1) = 14 + 1 = 15`$

## 7. Implementação Computacional (Python)

```python
import numpy as np

# Definindo parâmetros
mu = np.array([1, 2])
Sigma = np.array([[4, 1],
                  [1, 3]])
A = np.array([2, -1])  # Matriz A (1x2)
B = 5

# Calculando E(Y) e Var(Y)
E_Y = np.dot(A, mu) + B
Var_Y = np.dot(A, np.dot(Sigma, A.T))

print("E(Y) transformado:", E_Y)
print("Var(Y) transformada:", Var_Y)
```

## 8. Erros Comuns e Como Evitá-los

* Erro: Escrever Var(AX) = A Var(X), esquecendo de transpor a matriz do lado direito (A $`\Sigma A^T`$).
* Como evitar: Verifique sempre a compatibilidade das dimensões matriciais: se A possui dimensão $`q \times p`$ e $`\Sigma`$ possui dimensão $`p \times p`$, a multiplicação A $`\Sigma`$ resulta em uma matriz $`q \times p`$. Para obter uma matriz quadrada $`q \times q`$ compatível com a covariância do vetor transformado, é estritamente necessário pós-multiplicar por $`A^T (p \times q)`$.

## 9. Resumo da Aula em 3 Pontos

1. O valor esperado de um vetor aleatório é um operador linear: E(AX + B) = A E(X) + B.
2. Constantes aditivas B alteram o centro da distribuição, mas não impactam a matriz de covariância: Var(AX + B) = Var(AX).
3. A matriz de covariância de uma combinação linear segue a propriedade quadrática matricial: Var(AX) = A $`\Sigma A^T`$.

Dica Pedagógica: Ao transformar eixos de dados (como em índices sintéticos financeiros ou padronizações), lembre-se de que matrizes operam rotações e expansões, mas a covariância absorve a transformação ao quadrado (A $`\Sigma A^T`$).

## 10. Exercícios Práticos com Gabarito Comentado Passo a Passo

Exercício 1: Seja X um vetor aleatório $`2 \times 1`$ com $`\mu = \begin{bmatrix} 3 \\ 4 \end{bmatrix}`$. Qual o valor esperado do vetor $`Y = \begin{bmatrix} 1 & 2 \\ 0 & 1 \end{bmatrix}`$ X? Gabarito Passo a Passo:

1. Aplique a propriedade da linearidade: E(Y) = A E(X) = A $`\mu`$.
2. Efetue a multiplicação matricial: $`E(Y) = \begin{bmatrix} 1 & 2 \\ 0 & 1 \end{bmatrix} \begin{bmatrix} 3 \\ 4 \end{bmatrix} = \begin{bmatrix} 1(3) + 2(4) \\ 0(3) + 1(4) \end{bmatrix} = \begin{bmatrix} 3 + 8 \\ 0 + 4 \end{bmatrix} = \begin{bmatrix} 11 \\ 4 \end{bmatrix}`$

Exercício 2: Seja $`Var(X) = \Sigma`$. Demonstre formalmente por que $`Var(cX) = c^2 \Sigma`$, sendo c um escalar constante. Gabarito Passo a Passo:

1. Escreva o escalar como uma matriz diagonal A = $`c I_p`$, em que $`I_p`$ é a matriz identidade $`p \times p`$.
2. Aplique a propriedade da variância matricial: Var(AX) = A $`\Sigma A^T = (c I_p) \Sigma (c I_p)^T`$.
3. Como c é um escalar e $`I_p^T = I_p`$, reorganize os termos: $`(c I_p) \Sigma (c I_p) = c^2 (I_p \Sigma I_p) = c^2 \Sigma`$.

Exercício 3: Se Var(X_1) = 4, Var(X_2) = 9 e $`Cov(X_1, X_2) = 1`$, determine a variância da combinação $`Y = X_1`$ - 2X_2. Gabarito Passo a Passo:

1. Escreva $`Y = a^T X`$ com a = $`\begin{bmatrix} 1 \\ -2 \end{bmatrix}`$ e $`\Sigma = \begin{bmatrix} 4 & 1 \\ 1 & 9 \end{bmatrix}`$.
2. Aplique $`Var(Y) = a^T \Sigma`$ a: $`a^T \Sigma = \begin{bmatrix} 1 & -2 \end{bmatrix} \begin{bmatrix} 4 & 1 \\ 1 & 9 \end{bmatrix} = \begin{bmatrix} 1(4) + (-2)(1) & 1(1) + (-2)(9) \end{bmatrix} = \begin{bmatrix} 2 & -17 \end{bmatrix}`$
3. Pós-multiplique por a: $`Var(Y) = \begin{bmatrix} 2 & -17 \end{bmatrix} \begin{bmatrix} 1 \\ -2 \end{bmatrix} = 2(1)`$ + (-17)(-2) = 2 + 34 = 36.

Com as propriedades de transformações lineares consolidadas, torna-se possível derivar a distribuição de probabilidade contínua central da análise multivariada.

## MÓDULO 2: MODELAGEM PROBABILÍSTICA MULTIVARIADA

### Aula 3: Distribuição Normal Multivariada: Densidade, Geometria e Distância de Mahalanobis

## 1. Título da Aula

Distribuição Normal Multivariada: Densidade, Geometria e Distância de Mahalanobis.

## 2. Objetivo de Aprendizagem

Compreender a Função Densidade de Probabilidade (FDP) da Normal Multivariada $`N_p(\mu, \Sigma)`$, a geometria dos contornos elípticos e a formulação da Distância de Mahalanobis.

## 3. Fonte Original

Vídeos "Aula 4a Distribuição Normal Multivariada" e "Aula 4b Visualização em R e Python" (Profa. Cibele Russo).

## 4. Explicação Simples com Analogias

Pense na distribuição Normal Bivariada como uma montanha ou vulcão em um espaço tridimensional. Se cortarmos essa montanha horizontalmente em diferentes altitudes, o contorno gerado no chão será uma elipse. Essas elipses representam curvas de nível onde todos os pontos possuem exatamente a mesma densidade de probabilidade.

## 5. Diagrama Visual ASCII

```text
       Densidade f(x)
           /\
          /  \         <- Superfície 3D da Normal Bivariada
         /    \
  ------/------\------ <- Corte em Altitude FDP Constante
       (  . .   )      <- Projeção 2D: Contorno Elíptico de Mahalanobis
      /          \
     +------------+    <- Eixos direcionados polos Autovetores de Sigma
```

## 6. Exemplo Numérico Resolvido Passo a Passo

A FDP do vetor aleatório $`X_{p \times 1} \sim N_p(\mu, \Sigma)`$ é dada por: $`f(x) = \frac{1}{(2\pi)^{p/2} \vert \Sigma\vert ^{1/2}} \exp\left( -\frac{1}{2} (x - \mu)^T \Sigma^{-1} (x - \mu) \right)`$

O termo no expoente define a Distância de Mahalanobis ao quadrado $`(d^2): d^2 = (x - \mu)^T \Sigma^{-1} (x - \mu)`$

Cálculo Prático em Caso Bivariado (p=2): Sejam $`x = \begin{bmatrix} 2 \\ 3 \end{bmatrix}, \mu = \begin{bmatrix} 0 \\ 0 \end{bmatrix}`$ e $`\Sigma = \begin{bmatrix} 2 & 0 \\ 0 & 1 \end{bmatrix}`$.

1. Calcule a matriz inversa $`\Sigma^{-1}`$: Como $`\Sigma`$ é diagonal, $`\Sigma^{-1} = \begin{bmatrix} 1/2 & 0 \\ 0 & 1/1 \end{bmatrix} = \begin{bmatrix} 0,5 & 0 \\ 0 & 1 \end{bmatrix}`$.
2. Subtraia o vetor de médias: $`x - \mu = \begin{bmatrix} 2 - 0 \\ 3 - 0 \end{bmatrix} = \begin{bmatrix} 2 \\ 3 \end{bmatrix}`$.
3. Calcule a forma quadrática $`d^2: d^2 = \begin{bmatrix} 2 & 3 \end{bmatrix} \begin{bmatrix} 0,5 & 0 \\ 0 & 1 \end{bmatrix} \begin{bmatrix} 2 \\ 3 \end{bmatrix} = \begin{bmatrix} 2 & 3 \end{bmatrix} \begin{bmatrix} 1 \\ 3 \end{bmatrix} = 2(1) + 3(3) = 2 + 9 = 11`$

Pela teoria probabilística, essa forma quadrática $`d^2`$ possui distribuição Qui-Quadrado com p graus de liberdade: $`d^2 \sim \chi^2_p`$.

## 7. Implementação Computacional (R & Python)

#### Código R:

```r
library(mvtnorm)

mu <- c(0, 0)
Sigma <- matrix(c(2, 0, 0, 1), nrow = 2)
x_ponto <- c(2, 3)

# Densidade da Normal Multivariada
densidade <- dmvnorm(x_ponto, mean = mu, sigma = Sigma)
print(paste("Densidade:", densidade))

# Distância de Mahalanobis
d2 <- mahalanobis(x_ponto, center = mu, cov = Sigma)
print(paste("Distância de Mahalanobis ao quadrado:", d2))
```

#### Código Python:

```python
import numpy as np
from scipy.stats import multivariate_normal

mu = np.array([0, 0])
Sigma = np.array([[2, 0], [0, 1]])
x_ponto = np.array([2, 3])

# Densidade
fdp = multivariate_normal.pdf(x_ponto, mean=mu, cov=Sigma)

# Distância de Mahalanobis ao quadrado
Sigma_inv = np.linalg.inv(Sigma)
diff = x_ponto - mu
d2 = np.dot(diff.T, np.dot(Sigma_inv, diff))

print(f"FDP: {fdp:.6f}")
print(f"Mahalanobis d^2: {d2:.2f}")
```

## 8. Erros Comuns e Como Evitá-los

* Erro: Utilizar a distância Euclidiana simples para avaliar a probabilidade de pontos em variáveis correlacionadas ou com variâncias distintas.
* Como evitar: Use sempre a Distância de Mahalanobis. Ela padroniza a distância dividindo os eixos pelas suas variâncias e rotaciona os eixos eliminando o efeito da covariância por meio do termo $`\Sigma^{-1}`$.

## 9. Resumo da Aula em 3 Pontos

1. A Normal Multivariada $`N_p(\mu, \Sigma)`$ é inteiramente caracterizada por seu vetor de médias $`\mu`$ e sua matriz de covariância $`\Sigma`$.
2. Os contornos de densidade constante formam elipsoides definidos polos autovalores e autovetores da matriz $`\Sigma`$.
3. A distância estatística de Mahalanobis $`(x-\mu)^T \Sigma^{-1} (x-\mu)`$ segue rigorosamente uma distribuição $`\chi^2_p`$.

Alerta Estatístico: Na detecção de outliers multivariados (como fraudes bancárias), pontos com valores euclidianos normais podem ter uma distância de Mahalanobis gigantesca se violarem a estrutura de covariância do sistema.

## 10. Exercícios Práticos com Gabarito Comentado Passo a Passo

Exercício 1: Se $`X \sim N_p(\mu, \Sigma)`$ e $`\Sigma`$ é uma matriz diagonal, qual é a relação entre as componentes do vetor X? Gabarito Passo a Passo:

1. Se $`\Sigma`$ é diagonal, as covariâncias $`s_{ik} = 0`$ para todo $`i \neq k`$.
2. Na distribuição Normal Multivariada, a covariância nula implica que a densidade conjunta f(x) pode ser fatorada exatamente no produto das densidades marginais $`f_1(x_1) \cdot f_2(x_2) \cdots f_p(x_p)`$.
3. Logo, as variáveis do vetor X são mutuamente independentes.

Exercício 2: Qual a distribuição exata da forma quadrática $`d^2 = (X - \mu)^T \Sigma^{-1} (X - \mu)`$ para um vetor $`X \sim N_3(\mu, \Sigma)?`$ Gabarito Passo a Passo:

1. Defina o vetor padronizado $`Z = \Sigma^{-1/2}(X - \mu) \sim N_3(0, I_3)`$.
2. Reescreva a forma quadrática: $`d^2 = Z^T Z = Z_1^2 + Z_2^2 + Z_3^2`$.
3. A soma dos quadrados de p=3 variáveis N(0,1) independentes segue por definição uma distribuição Qui-Quadrado com 3 graus de liberdade $`(\chi^2_3)`$.

Exercício 3: Se $`X_{5 \times 1} \sim N_5(\mu, \Sigma)`$, qual é a distribuição marginal do subvetor $`X^{(1)} = \begin{bmatrix} X_1 \\ X_2 \end{bmatrix}?`$ Gabarito Passo a Passo:

1. Particione o vetor de médias $`\mu = \begin{bmatrix} \mu^{(1)} \\ \mu^{(2)} \end{bmatrix}`$ e a matriz de covariância $`\Sigma = \begin{bmatrix} \Sigma_{11} & \Sigma_{12} \\ \Sigma_{21} & \Sigma_{22} \end{bmatrix}`$.
2. Pelas propriedades teóricas da Normal Multivariada, a integração do subvetor complementar $`X^{(2)}`$ resulta em uma densidade gaussiana marginal.
3. Assim, o subvetor $`X^{(1)}`$ segue uma distribuição Normal Bivariada $`N_2(\mu^{(1)}, \Sigma_{11})`$.

A sólida base teórica da Normal Multivariada e das formas quadráticas permite estruturar testes de hipóteses inferenciais para vetores de médias.

## MÓDULO 3: INFERÊNCIA ESTATÍSTICA PARA VETORES DE MÉDIAS

### Aula 4: Teste $`T^2`$ de Hotelling para um Vetor de Médias e Elipsoides de Confiança

## 1. Título da Aula

Teste $`T^2`$ de Hotelling para um Vetor de Médias e Elipsoides de Confiança.

## 2. Objetivo de Aprendizagem

Formular e aplicar o teste de hipóteses multivariado $`H_0: \mu = \mu_0`$ versus $`H_1: \mu \neq \mu_0`$ utilizando a estatística $`T^2`$ de Hotelling e construir regiões elipsoidais de confiança.

## 3. Fonte Original

Vídeos "Aula 5a Testes de Hipóteses..." e "Aula 5b Aplicações em Python..." (Profa. Cibele Russo).

## 4. Explicação Simples com Analogias

Imagine avaliar se a qualidade de um lote de carros atende simultaneamente aos padrões do fabricante em termos de velocidade máxima, consumo de combustível e emissão de poluentes. Fazer testes individuais para cada item ignora que carros mais potentes consomem mais combustível. O teste $`T^2`$ de Hotelling avalia todas as metas juntas em um único indicador global.

## 5. Diagrama Visual ASCII

```text
                 Região Elipsoidal de Confiança (95%)
                     . - - - - - - - - .
                   .     * mu_0          .
                  .    (Não Rejeitado)   .
                 .      Se T^2 <= F_crit  .
                  .          * X_barra    .
                   .                     .
                     . - - - - - - - - .
```

## 6. Exemplo Numérico Resolvido Passo a Passo

Dada uma amostra de tamanho n proveniente de $`N_p(\mu, \Sigma)`$, testamos $`H_0: \mu = \mu_0`$ contra $`H_1: \mu \neq \mu_0`$.

#### Estatística $`T^2`$ de Hotelling: $`T^2 = n (\bar{X} - \mu_0)^T S^{-1} (\bar{X} - \mu_0)`$

Para a tomada de decisão, converte-se a estatística $`T^2`$ em um valor F de Snedecor: $`\frac{n-p}{p(n-1)} T^2 \sim F_{p, n-p}`$

Rejeita-se $`H_0`$ ao nível de significância $`\alpha`$ se: $`T^2 > \frac{p(n-1)}{n-p} F_{p, n-p}(\alpha)`$

Estudo de Dados Bancários (n=100, p=9 variáveis): Considere p=9 variáveis financeiras (idade, limite do cartão, renda mensal, saldo devedor, etc.). Queremos testar se o vetor de médias populacional pode ser considerado igual a um vetor pré-especificado $`\mu_0`$.

* Dados do Teste: n = 100, $`p = 9, \alpha = 0,05`$.
* A estatística observada calculada via algoritmo resulta em $`T^2_{obs} = 14,0`$.
* Conversão para $`F_{obs}: F_{obs} = \frac{100 - 9}{9(100 - 1)} \times 14,0 = \frac{91}{891} \times 14,0 \approx 0,10213 \times 14,0 \approx 1,43`$
* O valor crítico da distribuição F com 9 e 91 graus de liberdade ao nível de 5% é $`F_{9, 91}(0,05) \approx 1,98`$.
* Cálculo do p-valor: P(F_{9, 91} > 1,43) = 0,176.

Conclusão: Como $`F_{obs} = 1,43 \le 1,98`$ (ou $`p\text{-valor} = 0,176 > 0,05`$), não rejeitamos $`H_0`$. O vetor $`\mu_0`$ testado está contido dentro do elipsoide de confiança de 95% centrado em $`\bar{X}`$.

## 7. Implementação Computacional (Python)

```python
import numpy as np
from scipy.stats import f

def teste_hotelling_uma_amostra(X, mu0, alpha=0.05):
    n, p = X.shape
    x_bar = np.mean(X, axis=0)
    S = np.cov(X, rowvar=False)
    S_inv = np.linalg.inv(S)

    diff = x_bar - mu0
    T2 = n * np.dot(diff.T, np.dot(S_inv, diff))

    # Conversão para F
    F_obs = ((n - p) / (p * (n - 1))) * T2
    df1 = p
    df2 = n - p
    p_value = 1.0 - f.cdf(F_obs, df1, df2)

    f_critico = f.ppf(1 - alpha, df1, df2)
    T2_critico = ((p * (n - 1)) / (n - p)) * f_critico

    rejeita = T2 > T2_critico
    return T2, F_obs, p_value, rejeita

# Teste com dados simulados
np.random.seed(42)
X_banco = np.random.multivariate_normal(mean=np.zeros(9), cov=np.eye(9), size=100)
mu0_teste = np.zeros(9)
T2, F_val, p_val, rej = teste_hotelling_uma_amostra(X_banco, mu0_teste)
print(f"T2: {T2:.2f}, F: {F_val:.2f}, p-valor: {p_val:.4f}, Rejeita H0? {rej}")
```

## 8. Erros Comuns e Como Evitá-los

* Erro: Executar p testes t de Student univariados separados em vez de um único teste $`T^2`$ multivariado.
* Como evitar: Testes univariados múltiplos inflam severamente a taxa de erro Tipo $`I (\alpha`$ global = $`1 - (1-\alpha)^p`$), pois ignoram as correlações entre as variáveis. Use sempre o teste $`T^2`$.

## 9. Resumo da Aula em 3 Pontos

1. O teste $`T^2`$ de Hotelling generaliza o teste t univariado para vetores de p dimensões.
2. A estatística $`T^2`$ é uma forma quadrática baseada na matriz de covariância amostral S.
3. Há equivalência matemática absoluta entre não rejeitar $`H_0: \mu = \mu_0`$ e verificar que $`\mu_0`$ pertence ao elipsoide de confiança de $`100(1-\alpha)\%`$.

Aplicações e Tomada de Decisão Executiva: Em auditorias de conformidade bancária ou metas de governança ESG, o teste $`T^2`$ permite a validação global e simultânea de múltiplos indicadores regulatórios, evitando a falsa impressão de inconformidade gerada por testes individuais acumulados.

## 10. Exercícios Práticos com Gabarito Comentado Passo a Passo

Exercício 1: Em um teste $`T^2`$ com n=21 observações e p=2 variáveis, calcule o fator de conversão multiplicativo que transforma $`T^2`$ em uma variável com distribuição $`F_{2, 19}`$. Gabarito Passo a Passo:

1. Identifique a fórmula da constante: $`\frac{n-p}{p(n-1)}`$.
2. Substitua n=21 e p=2: $`\text{Fator} = \frac{21 - 2}{2(21 - 1)} = \frac{19}{2(20)} = \frac{19}{40} = 0,475`$

Exercício 2: Se rejeitamos $`H_0: \mu = \mu_0`$ em um teste $`T^2`$ ao nível $`\alpha = 0,05`$, determine se o ponto $`\mu_0`$ está dentro ou fora do elipsoide de confiança de 95%. Gabarito Passo a Passo:

1. A região de confiança de $`95\%`$ é definida pelo conjunto de pontos $`\mu`$ que cumprem $`n(\bar{X}-\mu)^T S^{-1} (\bar{X}-\mu) \le T^2_{crítico}`$.
2. A rejeição de $`H_0`$ implica que $`T^2_{obs} > T^2_{crítico}`$.
3. Consequentemente, o ponto $`\mu_0`$ encontra-se estritamente fora do elipsoide de confiança.

Exercício 3: Qual a distribuição assintótica do teste $`T^2`$ quando o tamanho amostral n tende ao infinito $`(n \to \infty)?`$ Gabarito Passo a Passo:

1. Quando $`n \to \infty`$, a matriz S converge quase certamente para $`\Sigma (Lei`$ dos Grandes Números).
2. O fator $`\frac{n-p}{p(n-1)}`$ aproxima-se de $`\frac{1}{p}`$, e $`p \cdot F_{p, n-p} \to \chi^2_p`$.
3. Assim, $`T^2`$ aproxima-se assintoticamente de uma distribuição Qui-Quadrado com p graus de liberdade $`(\chi^2_p)`$.

Uma vez dominada a comparação de uma amostra contra um padrão fixo, o próximo passo é comparar duas populações distintas.

### Aula 5: Comparação de Vetores de Médias: Amostras Pareadas e Independentes

## 1. Título da Aula

Comparação de Vetores de Médias: Amostras Pareadas e Independentes.

## 2. Objetivo de Aprendizagem

Diferenciar e aplicar os testes estatísticos para comparação de vetores de médias em cenários de amostras pareadas (medidas repetidas) e de duas populações independentes, incluindo a verificação de homocedasticidade via Teste M de Box.

## 3. Fonte Original

Vídeos "Aula 5a Testes de Hipóteses..." e "Aula 5b Aplicações em Python..." (Profa. Cibele Russo).

## 4. Explicação Simples com Analogias

* Pareadas: Medir a pressão arterial e a taxa de glicose no mesmo paciente antes e depois da ministração de um medicamento.
* Independentes: Comparar o perfil financeiro (renda e limite de crédito) entre dois grupos completamente distintos: clientes masculinos vs. clientes femininos.

## 5. Diagrama Visual ASCII

```text
     Amostras Pareadas (Mesmo Indivíduo)       Amostras Independentes (Grupos Distintos)
     [ Antes: X_1j ]  ->  [ Depois: X_2j ]     [ Grupo 1: X_1j (n1) ]  vs  [ Grupo 2: X_2j (n2) ]
              \            /                              \                  /
            Diferença: D_j = X_1j - X_2j               Matriz Combinada: S_pooled (Box's M Test)
```

## 6. Exemplo Numérico Resolvido Passo a Passo

#### Caso 1: Amostras Pareadas

Para observações correlacionadas $`X_{1j}`$ e $`X_{2j}`$ (j=1, $`\dots, n`$), calcula-se o vetor de diferenças individuais: $`D_j = X_{1j} - X_{2j}`$ O teste de igualdade de médias $`H_0: \mu_1 = \mu_2`$ reduz-se exatamente ao teste $`T^2`$ de uma amostra para $`H_0: \mu_d = 0: T^2 = n \bar{D}^T S_d^{-1} \bar{D}`$

#### Caso 2: Duas Populações Independentes

Para amostras independentes de tamanhos $`n_1`$ e $`n_2`$, é necessário pregressamente testar a suposição de igualdade de matrizes de covariância $`(H_0: \Sigma_1 = \Sigma_2)`$ utilizando o Teste M de Box: $`M = (n_1 + n_2 - 2) \ln \vert S_{pooled}\vert  - (n_1 - 1) \ln`$ |S_1| - $`(n_2 - 1) \ln`$ |S_2|

Se o Teste M de Box não rejeitar a homocedasticidade multivariada, calcula-se a matriz de covariância combinada $`(S_{pooled}): S_{pooled} = \frac{(n_1 - 1)S_1 + (n_2 - 1)S_2}{n_1 + n_2 - 2}`$

A estatística de teste para $`H_0: \mu_1 - \mu_2 = \Delta_0`$ (frequentemente $`\Delta_0 = 0`$) é: $`T^2 = (\bar{X}_1 - \bar{X}_2 - \Delta_0)^T \left[ \left(\frac{1}{n_1} + \frac{1}{n_2}\right) S_{pooled} \right]^{-1} (\bar{X}_1 - \bar{X}_2 - \Delta_0)`$

A conversão para a distribuição F utiliza os graus de liberdade ajustados: $`\frac{n_1 + n_2 - p - 1}{p(n_1 + n_2 - 2)} T^2 \sim F_{p, n_1 + n_2 - p - 1}`$

## 7. Implementação Computacional (Python)

```python
import numpy as np
from scipy.stats import f

def hotelling_t2_duas_amostras(X1, X2):
    n1, p = X1.shape
    n2, _ = X2.shape

    x1_bar = np.mean(X1, axis=0)
    x2_bar = np.mean(X2, axis=0)

    S1 = np.cov(X1, rowvar=False)
    S2 = np.cov(X2, rowvar=False)

    S_pooled = ((n1 - 1) * S1 + (n2 - 1) * S2) / (n1 + n2 - 2)
    S_pooled_inv = np.linalg.inv(S_pooled)

    diff = x1_bar - x2_bar
    fator_escala = (1/n1) + (1/n2)

    T2 = (1 / fator_escala) * np.dot(diff.T, np.dot(S_pooled_inv, diff))

    # Conversão F
    df1 = p
    df2 = n1 + n2 - p - 1
    F_obs = ((n1 + n2 - p - 1) / (p * (n1 + n2 - 2))) * T2
    p_value = 1.0 - f.cdf(F_obs, df1, df2)

    return T2, F_obs, p_value

# Exemplo com 31 mulheres e 69 homens
np.random.seed(42)
X_mulheres = np.random.multivariate_normal(mean=np.zeros(4), cov=np.eye(4), size=31)
X_homens = np.random.multivariate_normal(mean=np.ones(4)*0.2, cov=np.eye(4), size=69)

T2, F_val, p_val = hotelling_t2_duas_amostras(X_mulheres, X_homens)
print(f"T2 Independente: {T2:.2f}, F: {F_val:.2f}, p-valor: {p_val:.4f}")
```

## 8. Erros Comuns e Como Evitá-los

* Erro: Aplicar a fórmula de amostras independentes $`(S_{pooled})`$ em dados pareados sem verificar a dependência, ou omitir a verificação de igualdade de matrizes de covariância.
* Como evitar: Aplique sempre o Teste M de Box antes de utilizar $`S_{pooled}`$. Se houver dependência entre pares (medidas no mesmo indivíduo), calcule $`D_j = X_{1j} - X_{2j}`$ e rode o teste $`T^2`$ pareado.

## 9. Resumo da Aula em 3 Pontos

1. Amostras pareadas são simplificadas reduzindo o problema a uma única amostra de diferenças $`D_j`$.
2. Para amostras independentes, exige-se a verificação de homocedasticidade $`(\Sigma_1 = \Sigma_2)`$ via Teste M de Box antes do cálculo da matriz $`S_{pooled}`$.
3. A estatística $`T^2`$ ajustada para duas amostras considera os tamanhos $`n_1`$ e $`n_2`$ através do fator $`\left(\frac{1}{n_1} + \frac{1}{n_2}\right)`$.

Aplicações e Tomada de Decisão Executiva: Ao comparar o efeito de duas campanhas de marketing em mercados distintos, utilizar o Teste M de Box garante que a variabilidade operacional dos públicos não distorça a avaliação da efetividade média das estratégias.

## 10. Exercícios Práticos com Gabarito Comentado Passo a Passo

Exercício 1: Em um estudo pareado antes/depois com n=50 pacientes e p=3 variáveis fisiológicas, qual a dimensão do vetor de diferenças médias $`\bar{D}`$ e quantos graus de liberdade possui a distribuição F associada? Gabarito Passo a Passo:

1. O vetor de diferenças $`D_j = X_{1j} - X_{2j}`$ é calculado para cada paciente, mantendo as p=3 variáveis. Logo, $`\bar{D}`$ possui dimensão $`3 \times 1`$.
2. A conversão de $`T^2`$ para F segue a fórmula de uma amostra com n=50 e p=3: $`F_{p, n-p} = F_{3, 50-3} = F_{3, 47}`$.

Exercício 2: Duas amostras independentes têm $`n_1 = 31`$ e $`n_2 = 69`$. Qual o denominador da fórmula de cálculo da matriz de covariância combinada $`S_{pooled}?`$ Gabarito Passo a Passo:

1. A fórmula de $`S_{pooled}`$ pondera as matrizes individuais pelos seus graus de liberdade: $`S_{pooled} = \frac{(n_1-1)S_1 + (n_2-1)S_2}{n_1 + n_2 - 2}`$.
2. O denominador é (31 - 1) + (69 - 1) = 30 + 68 = 98.

Exercício 3: Se o Teste M de Box rejeita a hipótese de igualdade de matrizes de covariância $`(\Sigma_1 \neq \Sigma_2)`$ para duas amostras independentes grandes, qual a alternativa para testar a diferença entre os vetores de médias? Gabarito Passo a Passo:

1. Na ausência de homocedasticidade multivariada, a matriz $`S_{pooled}`$ torna-se um estimador inválido.
2. Utiliza-se a aproximação de Welch-James para o problema de Behrens-Fisher multivariado, onde a matriz de covariância do contraste é estimada diretamente por $`S_{contraste} = \frac{1}{n_1} S_1 + \frac{1}{n_2} S_2`$.

A expansão natural da comparação de duas populações independentes para três ou mais populações é realizada via Análise de Variância Multivariada.

### Aula 6: MANOVA: Comparação de G Grupos Multivariados e Estatística Lambda de Wilks

## 1. Título da Aula

MANOVA: Comparação de G Grupos Multivariados e Estatística Lambda de Wilks.

## 2. Objetivo de Aprendizagem

Decompor a variabilidade multivariada total em matrizes de soma de quadrados e produtos cruzados "Entre Grupos" (B) e "Dentro dos Grupos" (W), e aplicar o teste Lambda de Wilks.

## 3. Fonte Original

Vídeos "Aula 6a MANOVA" e "Aula 6b Aplicação de MANOVA em R" (Profa. Cibele Russo).

## 4. Explicação Simples com Analogias

Comparar o desempenho acadêmico de alunos provenientes de 5 escolas diferentes analisando simultaneamente notas de Matemática, Português, História e Ciências. A MANOVA avalia se os centros de gravidade pedagógicos de cada escola são estatisticamente distintos em relação ao ruído interno de cada instituição.

## 5. Diagrama Visual ASCII

```text
              Decomposição da Variabilidade Total (MANOVA)

    Matriz Total T (n - 1 df)
         +-------------------------------------------------+
         | Variabilidade Total em relação à Média Geral    |
         +-------------------------------------------------+
                                  ||
                 +----------------+----------------+
                 ||                               ||
    Matriz Entre Grupos B (G - 1 df)     Matriz Dentro Grupos W (n - G df)
  +-----------------------------------+ +-----------------------------------+
  | Dife. entre Médias de Grupos e    | | Ruído / Resíduo Interno nos   |
  | a Média Geral                     | | Próprios Grupos                   |
  +-----------------------------------+ +-----------------------------------+
```

## 6. Exemplo Numérico Resolvido Passo a Passo

Na MANOVA com G grupos, a observação j do grupo k é modelada por: $`X_{kj} = \mu + \tau_k + \epsilon_{kj}`$

#### A variabilidade total é decomposta em matrizes $`p \times p`$: T = B + W

* T (Total): $`\sum_{k=1}^G \sum_{j=1}^{n_k} (X_{kj} - \bar{X})(X_{kj} - \bar{X})^T`$
* B (Entre / Between): $`\sum_{k=1}^G n_k (\bar{X}_k - \bar{X})(\bar{X}_k - \bar{X})^T`$
* W (Dentro / Within / Resíduo): $`\sum_{k=1}^G \sum_{j=1}^{n_k} (X_{kj} - \bar{X}_k)(X_{kj} - \bar{X}_k)^T`$

#### Tabela de MANOVA:

| Fonte de Variação | Matriz de Soma de Quadrados e Prod. Cruzados | Graus de Liberdade |
|---|---|---|
| Tratamentos (Entre) | B | G - 1 |
| Resíduos (Dentro) | W | $`\sum n_k - G = n - G`$ |
| Total | T = B + W | n - 1 |

Estatística Lambda de Wilks $`(\Lambda^*): \Lambda^* = \frac{\vert W\vert }{\vert B + W\vert } = \frac{\vert W\vert }{\vert T\vert }`$

Rejeita-se $`H_0: \tau_1 = \tau_2 = \dots = \tau_G = 0`$ quando $`\Lambda^*`$ é suficientemente pequeno (indicando que a variabilidade intra-grupo W é pequena frente à variabilidade total T).

Estudo Real dos Crânios Egípcios (G=5 épocas, p=4 medidas anatômicas, n=150 crânios): Ao ajustar a MANOVA para testar a igualdade das medidas anatômicas nas 5 épocas históricas (c4000BC, c3300BC, c1850BC, c200BC, cAD150):

* Valor de Lambda de Wilks observado: $`\Lambda^* \approx 0,664`$.
* Conversão para aproximação F de Rao: $`p\text{-valor} < 0,001`$.
* Decisão: Rejeita-se $`H_0`$. Há evidências altamente significativas de alterações nas dimensões anatômicas médias dos crânios ao longo das épocas históricas.

## 7. Implementação Computacional (R)

# Carregamento e ajuste da MANOVA para os dados de Crânios Egípcios
```r
library(HSAUR3)
data("skulls")

# Ajuste do modelo linear multivariado
modelo_skulls <- lm(cbind(mb, bh, bl, nh) ~ epoch, data = skulls)

# Teste MANOVA com estatística Lambda de Wilks
manova_resultado <- manova(modelo_skulls)
summary(manova_resultado, test = "Wilks")
```

## 8. Erros Comuns e Como Evitá-los

* Erro: Interpretar a rejeição de $`H_0`$ na MANOVA concluindo que todas as variáveis isoladas são diferentes entre todos os grupos.
* Como evitar: A MANOVA valida a rejeição de uma diferença global. Após rejeitar $`H_0`$, realize ANOVAs univariadas de acompanhamento para cada variável individual (com correção de Bonferroni) e testes de comparações múltiplas.

## 9. Resumo da Aula em 3 Pontos

1. A MANOVA decompõe a matriz de variabilidade total na soma T = B + W.
2. A estatística $`\Lambda^*`$ de Wilks utiliza a razão dos determinantes para comparar a variância generalizada residual com a total.
3. Exige suposições de normalidade multivariada nos resíduos e homocedasticidade das matrizes de covariância entre os G grupos.

Aplicações e Tomada de Decisão Executiva: Em testes A/B/C multinacionais para plataformas digitais, a MANOVA permite testar se novos layouts alteram simultaneamente o tempo de permanência, a taxa de cliques e o Ticket Médio sem inflar a probabilidade de falsos alarmes.

## 10. Exercícios Práticos com Gabarito Comentado Passo a Passo

Exercício 1: Em um estudo MANOVA com G=4 grupos, p=3 variáveis e n=100 observações totais, determine os graus de liberdade associados às matrizes B, W e T. Gabarito Passo a Passo:

1. Graus de liberdade Entre Grupos (B): G - 1 = 4 - 1 = 3.
2. Graus de liberdade Dentro dos Grupos (W): n - G = 100 - 4 = 96.
3. Graus de liberdade Total (T): n - 1 = 100 - 1 = 99.

Exercício 2: Se a matriz B = 0 (ou seja, todas as médias amostrais dos G grupos são perfeitamente idênticas à média geral), qual o valor do Lambda de Wilks $`(\Lambda^*)?`$ Gabarito Passo a Passo:

1. A estatística é dada por $`\Lambda^* = \frac{\vert W\vert }{\vert B + W\vert }`$.
2. Substituindo B = 0, temos B + W = 0 + W = W.
3. Logo, $`\Lambda^* = \frac{\vert W\vert }{\vert W\vert } = 1`$.

Exercício 3: Por que a razão de determinantes $`\frac{\vert W\vert }{\vert B + W\vert }`$ é utilizada como medida de dispersão generalizada na estatística $`\Lambda^*?`$ Gabarito Passo a Passo:

1. O determinante de uma matriz de covariância/soma de quadrados representa o volume geométrico do elipsoide de dispersão (conhecido como variância generalizada).
2. A razão $`\frac{\vert W\vert }{\vert T\vert }`$ compara o volume de variação não explicada (resíduo) com o volume de variação total. Se a variação entre grupos B for grande, |T| cresce muito frente a |W|, fazendo $`\Lambda^*`$ tender a 0.

Passando das comparações de vetores de médias entre grupos, explora-se a modelagem funcional entre conjuntos de variáveis preditoras e múltiplas respostas.

## MÓDULO 4: MODELOS DE REGRESSÃO E CORRELAÇÃO

### Aula 7: Regressão Multivariada Clássica

## 1. Título da Aula

Regressão Linear Multivariada: Múltiplas Respostas e Múltiplos Preditores.

## 2. Objetivo de Aprendizagem

Formular matricialmente o modelo de regressão multivariada $`Y_{n \times m} = Z_{n \times (r+1)} \beta_{(r+1) \times m} + E_{n \times m}`$, estimar a matriz de parâmetros $`\hat{\beta}`$ e conduzir diagnósticos de resíduos.

## 3. Fonte Original

Vídeo "Aula 6d Regressão Multivariada em R" (Profa. Cibele Russo).

## 4. Explicação Simples com Analogias

Imagine prever simultaneamente a potência do motor, o consumo de combustível e a emissão de carbono de um veículo utilizando como preditores o tamanho do motor, o peso do carro e o tipo de injeção, capturando a correlação natural que existe entre os resíduos dessas respostas.

## 5. Diagrama Visual ASCII

```text
                      Estrutura da Regressão Multivariada

    Y (n x m)       =      Z (n x [r+1])      *      beta ([r+1] x m)   +    E (n x m)
  [ Respostas ]          [ Preditores + 1s ]        [ Coeficientes ]       [ Erros Multiv. ]

  [Y1  Y2  ... Ym]       [1  Z11 ... Z1r]           [beta_01 ... beta_0m]    [e11 ... e1m]
  [ .   .   .   .]   =   [1  Z21 ... Z2r]     *     [ .       .     .   ]  + [ .   .   .  ]
  [Yn1 Yn2 ... Ynm]      [1  Zn1 ... Znr]           [beta_r1 ... beta_rm]    [en1 ... enm]
```

## 6. Exemplo Numérico Resolvido Passo a Passo

Estudo de resistência de fibras com m=4 variáveis resposta ($`Y_1`$: comprimento na quebra, $`Y_2`$: módulo de elasticidade, $`Y_3`$: estresse na falha, $`Y_4`$: resistência à quebra) e r=4 covariáveis preditoras $`Z_1, Z_2, Z_3, Z_4`$.

#### Estrutura Matricial do Modelo: $`Y = Z \beta`$ + E

* Y é a matriz $`n \times m`$ de variáveis resposta.
* Z é a matriz $`n \times (r+1)`$ de preditores (incluindo a coluna de 1s para o intercepto).
* $`\beta`$ é a matriz de coeficientes $`(r+1) \times m`$.
* E é a matriz de erros $`n \times m`$, em que cada linha tem covariância $`\Sigma_E`$.

#### Estimador de Mínimos Quadrados Ordinários Matricial: $`\hat{\beta} = (Z^T Z)^{-1} Z^T Y`$

A estimativa da matriz de parâmetros $`\hat{\beta}`$ para cada coluna j equivale numericamente ao ajuste da j-ésima regressão univariada individual. Contudo, a matriz de resíduos $`\hat{E} = Y - Z \hat{\beta}`$ permite estimar a matriz de covariância conjunta do erro: $`\hat{\Sigma}_E = \frac{1}{n - r - 1} \hat{E}^T \hat{E}`$

## 7. Implementação Computacional (R)

# Carregamento dos dados de resistência de fibras e ajuste multivariado
# y1..y4: respostas; z1..z4: preditores
modelo_fibras <- lm(cbind(Y1, Y2, Y3, Y4) ~ Z1 + Z2 + Z3 + Z4, data = dados_fibras)

# Resumo dos coeficientes ajustados
summary(modelo_fibras)

# Matriz de covariância dos resíduos multivariados
residuos <- residuals(modelo_fibras)
Sigma_E_hat <- cov(residuos)
print(Sigma_E_hat)

## 8. Erros Comuns e Como Evitá-los

* Erro: Ajustar m regressões univariadas isoladas ignorando a matriz de covariância dos resíduos e realizar testes de hipóteses individuais sobre os preditores.
* Como evitar: Se as variáveis resposta Y forem correlacionadas, o modelo multivariado integrado é estritamente necessário para testes de hipóteses globais (como testar se uma covariável afeta simultaneamente todas as respostas via teste de Wilks).

## 9. Resumo da Aula em 3 Pontos

1. O modelo $`Y_{n \times m} = Z_{n \times (r+1)} \beta`$ + E estende a regressão múltipla para m respostas simultâneas.
2. Os coeficientes são estimados matricialmente por $`\hat{\beta} = (Z^T Z)^{-1} Z^T Y`$.
3. A análise de diagnósticos deve inspecionar padrões heteroscedásticos e a matriz de covariância dos resíduos entre as respostas.

Aplicações e Tomada de Decisão Executiva: Em engenharia de processos ou modelos econométricos, prever respostas conjuntas permite otimizar covariáveis operacionais para maximizar a qualidade final e minimizar custos simultaneamente, capturando a compensação (trade-off) entre os produtos.

## 10. Exercícios Práticos com Gabarito Comentado Passo a Passo

Exercício 1: Em um modelo de regressão multivariada com m=3 variáveis resposta, r=5 preditores contínuos e n=50 observações, determine as dimensões das matrizes Y, $`Z, \beta`$ e $`\hat{\Sigma}_E`$. Gabarito Passo a Passo:

1. Matriz de respostas Y: $`n \times m = 50 \times 3`$.
2. Matriz de projeto Z (incluindo intercepto): $`n \times (r+1) = 50 \times (5+1) = 50 \times 6`$.
3. Matriz de parâmetros $`\beta: (r+1) \times m = 6 \times 3`$.
4. Matriz de covariância residual $`\hat{\Sigma}_E: m \times m = 3 \times 3`$.

Exercício 2: Mostre que a matriz de valores preditos $`\hat{Y}`$ pode ser escrita utilizando a matriz chapéu (Hat Matrix) H. Gabarito Passo a Passo:

1. A matriz de parâmetros estimada é $`\hat{\beta} = (Z^T Z)^{-1} Z^T Y`$.
2. Os valores preditos são dada por $`\hat{Y} = Z \hat{\beta} = Z \left[ (Z^T Z)^{-1} Z^T Y \right]`$.
3. Agrupando os termos: $`\hat{Y} = \left[ Z (Z^T Z)^{-1} Z^T \right] Y = H`$ Y, em que $`H = Z (Z^T Z)^{-1} Z^T`$ possui dimensão $`n \times n`$.

Exercício 3: Se os resíduos das m variáveis resposta forem inteiramente não correlacionados ($`\hat{\Sigma}_E`$ é diagonal), existe perda de precisão matemática ao usar Mínimos Quadrados Ordinários em relação a Mínimos Quadrados Generalizados? Gabarito Passo a Passo:

1. Na regressão multivariada clássica com os mesmos preditores Z para todas as respostas, os estimadores de MQO ponto a ponto são numericamente idênticos aos estimadores de Mínimos Quadrados Generalizados (SUR - Seemingly Unrelated Regressions).
2. Se $`\hat{\Sigma}_E`$ for diagonal, as respostas são independentes no resíduo e o modelo multivariado reduz-se exatamente a m regressões univariadas independentes sem nenhuma perda de precisão.

Além de prever respostas a partir de preditores, pode-se buscar a associação linear pura entre dois blocos inteiros de variáveis aleatórias.

### Aula 8: Análise de Correlações Canônicas (CCA)

## 1. Título da Aula

Análise de Correlações Canônicas: Associando Blocos de Variáveis.

## 2. Objetivo de Aprendizagem

Formular o método de Correlações Canônicas para maximizar a correlação linear entre combinações lineares de dois conjuntos de variáveis $`X_{p \times 1}`$ e $`Y_{q \times 1}`$, criando pares de variáveis canônicas $`(U_k, V_k)`$.

## 3. Fonte Original

Vídeos "Análise de Correlações Canônicas" e "Aula 9b Aplicação em Python" (Profa. Cibele Russo).

## 4. Explicação Simples com Analogias

Imagine avaliar a associação entre o "Desempenho Acadêmico" de um aluno (composto por notas de Matemática, Física e Química) e suas "Características Psicológicas" (motivação, autoconceito e controle). A CCA constrói dois índices sintéticos (um para o bloco acadêmico e outro para o psicológico) ajustados para obter a maior correlação possível entre si.

## 5. Diagrama Visual ASCII

```text
                    Estrutura da Correlação Canônica (CCA)

  Bloco X (p vars)                                            Bloco Y (q vars)
  [Psicológico]                                               [Acadêmico]
        |                                                          |
  Combinação Linear (a1)                                     Combinação Linear (b1)
        |                                                          |
        v                                                          v
  Var Canônica U1 = a1^T * X  <==== Max Corr(U1, V1) ====>  Var Canônica V1 = b1^T * Y
                                   rho_1 = sqrt(lambda_1)
```

## 6. Exemplo Numérico Resolvido Passo a Passo

Sejam dois blocos de variáveis $`X_{p \times 1}`$ e $`Y_{q \times 1}`$. Queremos definir o primeiro par canônico: $`U_1 = a_1^T X \quad \text{e} \quad V_1 = b_1^T Y`$

Problema de Otimização Restrita: $`\max_{a_1, b_1} \text{Corr}(U_1, V_1) = \frac{a_1^T \Sigma_{XY} b_1}{\sqrt{a_1^T \Sigma_{XX} a_1} \sqrt{b_1^T \Sigma_{YY} b_1}}`$ sujeito a $`Var(U_1) = a_1^T \Sigma_{XX} a_1 = 1`$ e $`Var(V_1) = b_1^T \Sigma_{YY} b_1 = 1`$.

A solução via multiplicadores de Lagrange reduz-se ao problema de autovalores das matrizes: $`\Sigma_{XX}^{-1} \Sigma_{XY} \Sigma_{YY}^{-1} \Sigma_{YX} a_1 = \lambda_1 a_1 \Sigma_{YY}^{-1} \Sigma_{YX} \Sigma_{XX}^{-1} \Sigma_{XY} b_1 = \lambda_1 b_1`$

A primeira correlação canônica é a raiz quadrada do maior autovalor: $`\rho_1 = \sqrt{\lambda_1}`$

#### Estudo Real com 600 Indivíduos (p=3 psicológicas, q=5 acadêmicas/gênero):

* Número máximo de pares canônicos: $`k = \min(p, q) = \min(3, 5) = 3`$.
* Primeiro par canônico obtido: $`\rho_1 = 0,464 (\lambda_1 \approx 0,215)`$.
* Segundo par canônico: $`\rho_2 = 0,167 (\lambda_2 \approx 0,028)`$.
* Terceiro par canônico: $`\rho_3 = 0,100 (\lambda_3 \approx 0,010)`$.

## 7. Implementação Computacional (Python)

```python
import pandas as pd
from sklearn.cross_decomposition import CCA

# Carregamento dos dados dos 600 estudantes
url = "https://stats.idre.ucla.edu/stat/data/mmreg.csv"
dados = pd.read_csv(url)

X = dados[['locus_of_control', 'self_concept', 'motivation']] # p = 3
Y = dados[['read', 'write', 'math', 'science', 'female']]      # q = 5

# Ajuste da CCA para 3 componentes
cca = CCA(n_components=3)
cca.fit(X, Y)

X_c, Y_c = cca.transform(X, Y)

# Calculando as correlações canônicas amostrais
correlacoes = [np.corrcoef(X_c[:, i], Y_c[:, i])[0, 1] for i in range(3)]
for idx, r in enumerate(correlacoes):
    print(f"Par Canônico {idx+1} - Correlação Canônica (rho): {r:.4f}")
```

## 8. Erros Comuns e Como Evitá-los

* Erro: Confundir a correlação canônica $`\rho_1`$ com a correlação linear de Pearson simples entre duas variáveis isoladas dos conjuntos.
* Como evitar: Lembre-se de que a CCA mede a correlação entre combinações lineares sintéticas de blocos ($`U_1`$ e $`V_1`$), e não entre variáveis originais individuais.

## 9. Resumo da Aula em 3 Pontos

1. A CCA resume a relação entre dois blocos de variáveis em $`k = \min(p, q)`$ pares de variáveis canônicas $`(U_k, V_k)`$.
2. As correlações canônicas correspondem às raízes quadradas dos autovalores $`\rho_k = \sqrt{\lambda_k}`$ das matrizes do sistema.
3. Pares canônicos de ordens distintas são ortogonais entre si (Cov(U_i, $`U_j) = 0`$ para $`i \neq j`$).

Aplicações e Tomada de Decisão Executiva: Em pesquisas de satisfação de clientes, a CCA permite conectar o bloco de "Percepções de Marca" ao bloco de "Engajamento e Comportamento de Compra", identificando os fatores sintéticos subjacentes que impulsionam a lealdade do cliente.

## 10. Exercícios Práticos com Gabarito Comentado Passo a Passo

Exercício 1: Se o Bloco X possui p=4 variáveis e o Bloco Y possui q=2 variáveis, quantos pares de variáveis canônicas podem ser construídos? Gabarito Passo a Passo:

1. O número máximo de pares canônicos k é limitado pela menor dimensão entre os dois blocos: $`k = \min(p, q)`$.
2. Substituindo os valores: $`k = \min(4, 2) = 2`$.

Exercício 2: Se o maior autovalor obtido no sistema matricial da CCA foi $`\lambda_1 = 0,64`$, qual a primeira correlação canônica $`\rho_1?`$ Gabarito Passo a Passo:

1. A relação entre o autovalor do sistema e a correlação canônica é $`\rho_k = \sqrt{\lambda_k}`$.
2. Calculando para o primeiro par: $`\rho_1 = \sqrt{0,64} = 0,80`$.

Exercício 3: Demonstre que a variância de uma variável canônica padronizada $`U_1 = a_1^T X`$ é igual a 1 quando $`a_1`$ é o autovetor do sistema. Gabarito Passo a Passo:

1. $`Var(U_1) = Var(a_1^T X) = a_1^T Var(X) a_1 = a_1^T \Sigma_{XX} a_1`$.
2. Na formulação do problema de otimização restrita via Lagrange, impõe-se explicitamente a restrição de normalização $`a_1^T \Sigma_{XX} a_1 = 1`$.
3. Logo, os autovetores calculados $`a_1`$ são escalados para garantir Var(U_1) = 1.

Ao buscar reduzir a dimensão de um único bloco de variáveis correlacionadas, entra-se no domínio da Análise de Componentes Principais.

## MÓDULO 5: REDUÇÃO DE DIMENSIONALIDADE

### Aula 9: Análise de Componentes Principais (PCA) – Teoria e Decomposição Espectral

## 1. Título da Aula

Análise de Componentes Principais (PCA): Teoria e Decomposição Espectral.

## 2. Objetivo de Aprendizagem

Derivar matematicamente as componentes principais como combinações lineares não-correlacionadas que maximizam a variância retida a partir da decomposição espectral de $`\Sigma`$ ou R.

## 3. Fonte Original

Vídeo "Aula 7a Análise de Componentes Principais" (Profa. Cibele Russo).

## 4. Explicação Simples com Analogias

Imagine fotografar uma escultura tridimensional do ângulo exato que captura a sua maior largura e variação de profundidade. A PCA projeta os dados de um espaço com p dimensões para poucas dimensões mantendo a máxima dispersão (informação) original sem distorcer as distâncias.

## 5. Diagrama Visual ASCII

```text
                   Projeção Geométrica da PCA

       Eixo X2 |       . * (Direção do Autovetor e1 -> Maior Variância PC1)
               |     . *
               |   . *
               | . *     (Direção Ortogonal e2 -> PC2)
               +------------ Eixo X1
```

## 6. Exemplo Numérico Resolvido Passo a Passo

Seja $`X_{p \times 1}`$ um vetor aleatório com matriz de covariância $`\Sigma_{p \times p}`$. Pelo Teorema da Decomposição Espectral: $`\Sigma = V \Lambda V^T = \sum_{j=1}^p \lambda_j e_j e_j^T`$ em que $`\lambda_1 \ge \lambda_2 \ge \dots \ge \lambda_p \ge 0`$ são os autovalores de $`\Sigma`$, e $`e_j`$ são os autovetores ortonormais correspondentes ($`e_i^T e_j = 0`$ para $`i \neq j`$, e $`e_j^T e_j = 1`$).

#### A j-ésima Componente Principal: $`Y_j = e_j^T X = e_{j1}X_1 + e_{j2}X_2 + \dots + e_{jp}X_p`$

#### Propriedades Fundamentais:

1. $`Var(Y_j) = e_j^T \Sigma e_j = \lambda_j`$ (a variância da componente é o autovalor).
2. $`Cov(Y_i, Y_j) = 0`$ para $`i \neq j`$ (as componentes são ortogonais/não-correlacionadas).
3. $`\sum_{j=1}^p Var(X_j) = \text{tr}(\Sigma) = \sum_{j=1}^p \lambda_j = \sum_{j=1}^p Var(Y_j)`$ (a variabilidade total é preservada).

Proporção de Variância Explicada pela j-ésima componente: $`\text{Proporção}_j = \frac{\lambda_j}{\sum_{k=1}^p \lambda_k}`$

## 7. Implementação Computacional (Python)

```python
import numpy as np

# Matriz de Covariância populacional ou amostral S (3x3)
Sigma = np.array([[6, 2, 0],
                  [2, 3, 0],
                  [0, 0, 1]])

# Decomposição espectral (Autovalores e Autovetores)
autovalores, autovetores = np.linalg.eigh(Sigma)

# Ordenação decrescente
idx = np.argsort(autovalores)[::-1]
autovalores = autovalores[idx]
autovetores = autovetores[:, idx]

variabilidade_total = np.sum(autovalores)
proporcao_explicada = autovalores / variabilidade_total

print("Autovalores (Variâncias das PCs):", autovalores)
print("Proporção Explicada:", proporcao_explicada)
```

## 8. Erros Comuns e Como Evitá-los

* Erro: Executar a PCA sobre a matriz de covariância S quando as variáveis possuem unidades de medida com ordens de grandeza distintas (ex: faturamento em R\$ versus idade em anos).
* Como evitar: Padronize as variáveis préviamente via StandardScaler ou execute a PCA diretamente através da matriz de correlação R.

## 9. Resumo da Aula em 3 Pontos

1. A PCA transforma p variáveis correlacionadas em p componentes ortogonais ordenadas por variância.
2. A variância da j-ésima componente é exatamente o j-ésimo autovalor $`\lambda_j`$ da matriz de covariância ou correlação.
3. A soma de todos os autovalores é igual à variância total preservada no sistema original.

Dica Pedagógica: Na matriz de correlação R, a variabilidade total é sempre igual ao número de variáveis p, facilitando a interpretação do impacto de cada autovalor $`(\lambda_j > 1)`$.

## 10. Exercícios Práticos com Gabarito Comentado Passo a Passo

Exercício 1: Os autovalores da matriz de covariância de um sistema com p=3 variáveis são $`\lambda_1 = 6, \lambda_2 = 3`$ e $`\lambda_3 = 1`$. Qual a variabilidade total dos dados e a proporção acumulada pelas duas primeiras componentes? Gabarito Passo a Passo:

1. Variabilidade Total = $`\sum_{k=1}^3 \lambda_k = 6 + 3 + 1 = 10`$.
2. Proporção de $`PC_1: \frac{6}{10} = 0,60 (60\%)`$.
3. Proporção de $`PC_2: \frac{3}{10} = 0,30 (30\%)`$.
4. Proporção Acumulada por $`(PC_1 + PC_2): 60\% + 30\% = 90\%`$.

Exercício 2: Se usarmos a matriz de correlação $`R_{4 \times 4}`$ para rodar uma PCA com p=4 variáveis, qual é a soma de todos os autovalores? Gabarito Passo a Passo:

1. Na matriz de correlação R, os elementos da diagonal principal são todos iguais a 1.
2. O traço da matriz é $`\text{tr}(R) = \sum_{i=1}^4 r_{ii} = 1 + 1 + 1 + 1 = 4`$.
3. Pela propriedade espectral, $`\sum_{j=1}^4 \lambda_j = \text{tr}(R) = 4`$.

Exercício 3: Demonstre que duas componentes principais $`Y_i = e_i^T X`$ e $`Y_j = e_j^T X`$ possuem covariância nula para $`i \neq j`$. Gabarito Passo a Passo:

1. $`Cov(Y_i, Y_j) = Cov(e_i^T X, e_j^T X) = e_i^T Var(X) e_j = e_i^T \Sigma e_j`$.
2. Como $`e_j`$ é autovetor de $`\Sigma`$, temos $`\Sigma e_j = \lambda_j e_j`$.
3. Substituindo: $`Cov(Y_i, Y_j) = e_i^T (\lambda_j e_j) = \lambda_j (e_i^T e_j)`$.
4. Como os autovetores são ortonormais, $`e_i^T e_j = 0`$ para $`i \neq j`$. Logo, $`Cov(Y_i, Y_j) = 0`$.

Com a álgebra da PCA estabelecida, estuda-se a sua aplicação prática na redução de dimensão, ranqueamento e análise visual.

### Aula 10: Aplicação Prática de PCA e Critérios de Seleção de Componentes

## 1. Título da Aula

Aplicação de PCA: Interpretação de Scores, Loadings e Scree Plot.

## 2. Objetivo de Aprendizagem

Executar a PCA utilizando a biblioteca scikit-learn em Python, selecionar o número ideal de componentes com auxílio do Scree Plot e interpretar loadings e scores.

## 3. Fonte Original

Vídeos "Aula 7b PCA em Python", "Aula aberta" e "Análise descritiva" (Profa. Cibele Russo).

## 4. Explicação Simples com Analogias

No Decatlo (competição esportiva com 10 provas diferentes), em vez de premiar atletas com 10 medalhas separadas, a PCA reduz os 10 resultados individuais a um "Índice de Desempenho Geral" único, atribuindo pesos otimizados a cada prova.

## 5. Diagrama Visual ASCII

```text
                  Scree Plot (Gráfico do Cotovelo)
     Variância Explicada
        1.0 |   * (PC1 ~80%)
        0.8 |    \
        0.6 |     \
        0.4 |      \
        0.2 |       * (PC2 ~14%)  <--- Ponto de Inflexão (Cotovelo em k=2)
        0.0 +--------*-----*-----*---
                    PC1   PC2   PC3
```

## 6. Exemplo Numérico Resolvido Passo a Passo

Estudo do Decatlo (n=41 atletas, p=10 provas esportivas: 100m rasos, salto em distância, arremesso de peso, salto em altura, 400m, 110m com barreiras, disco, salto com vara, dardo, 1500m).

#### Critério de Seleção via Scree Plot:

* Resultado da variância acumulada:
  * $`PC_1`$ explica $`80\%`$ da variabilidade.
  * $`PC_2`$ explica $`14\%`$ da variabilidade.
  * $`PC_1 + PC_2`$ acumulam $`94\%`$ da variância total.
* Decisão: Retemos k=2 componentes, reduzindo o problema de 10 variáveis para apenas 2 sem perda expressiva de informação.

#### Diferença entre Loadings e Scores:

* Loadings (Coeficientes): Os pesos de cada prova na combinação linear. Ex: $`PC_1 = -0,001 \cdot X_{\text{100m}} + 0,008 \cdot X_{\text{peso}} + \dots + 0,105 \cdot X_{\text{1500m}}`$.
* Scores (Novos Valores): Os novos valores transformados calculados para cada atleta individual, gerando as coordenadas no espaço reduzido usadas para o ranqueamento.

## 7. Implementação Computacional (Python)

```python
import pandas as pd
from sklearn.decomposition import PCA
from sklearn.preprocessing import StandardScaler

# Exemplo de pipeline em Python para o Decatlo
# X_decatlo: matriz 41x10 com os resultados das provas

scaler = StandardScaler()
X_scaled = scaler.fit_transform(X_decatlo)

# Instanciando PCA com 2 componentes
pca = PCA(n_components=2)
scores = pca.fit_transform(X_scaled)

# Matriz de Loadings (Componentes x Variáveis)
loadings = pd.DataFrame(pca.components_, columns=nome_provas, index=['PC1', 'PC2'])

print("Proporção de Variância Explicada:", pca.explained_variance_ratio_)
print("\nMatriz de Loadings:\n", loadings)
```

## 8. Erros Comuns e Como Evitá-los

* Erro: Confundir Loadings (pesos das variáveis originais na combinação linear) com Scores (as coordenadas transformadas dos indivíduos nas componentes).
* Como evitar: Mnemônico: Loadings pertencem às colunas (variáveis, dimensão p); Scores pertencem às linhas (observações/indivíduos, dimensão n).

## 9. Resumo da Aula em 3 Pontos

1. O Scree Plot identifica o ponto de inflexão ("cotovelo") para decidir o número k de componentes a reter.
2. Os loadings indicam o peso e o sentido da contribuição de cada variável original na componente.
3. Os scores são os novos valores transformados dos indivíduos, utilizados em rankings e modelos secundários.

Aplicações e Tomada de Decisão Executiva: Na criação de rankings operacionais de filiais, utilizar os scores da $`PC_1`$ elimina o arbítrio humano na escolha de pesos para KPIs, garantindo uma ordenação estatisticamente ideal que minimiza distorções comerciais.

## 10. Exercícios Práticos com Gabarito Comentado Passo a Passo

Exercício 1: Se as duas primeiras componentes principais explicam $`75\%`$ e $`18\%`$ da variância total, respectivamente, qual a variância acumulada por esse par? Gabarito Passo a Passo:

1. Some as proporções individuais: $`\text{Variância Acumulada} = \text{Prop}(PC_1) + \text{Prop}(PC_2)`$.
2. $`\text{Variância Acumulada} = 75\% + 18\% = 93\%`$.

Exercício 2: Em um estudo com n=50 indivíduos e p=8 variáveis, qual a dimensão da matriz de Scores obtida ao reter k=2 componentes? Gabarito Passo a Passo:

1. Cada indivíduo recebe um valor para cada componente mantida.
2. A matriz de Scores possui n linhas e k colunas.
3. Dimensão resultante: $`50 \times 2`$.

Exercício 3: Em uma prova de corrida (ex: 100m rasos), um tempo menor indica melhor desempenho. Já no salto em altura, uma marca maior indica vitória. Como a PCA harmoniza o sinal dos loadings para compor um índice de performance único? Gabarito Passo a Passo:

1. A PCA ajusta o sinal algébrico dos coeficientes dos autovetores para refletir a covariância conjunta.
2. Provas de tempo receberão loadings com sinal oposto aos de provas de marca (ex: negativo para 100m e positivo para salto).
3. Isso garante que a componente aumente na direção do desempenho esportivo superior global.

A partir deste ponto, encerra-se o bloco de redução de variáveis para iniciar o agrupamento de observações similares (Clustering).

## MÓDULO 6: APRENDIZADO NÃO-SUPERVISIONADO E AGRUPAMENTOS (CLUSTERING)

### Aula 11: Clustering Hierárquico Aglomerativo: Distâncias, Métodos de Ligação e Dendrogramas

## 1. Título da Aula

Clustering Hierárquico Aglomerativo: Distâncias, Métodos de Ligação e Dendrogramas.

## 2. Objetivo de Aprendizagem

Agrupar observações iterativamente por algoritmos hierárquicos aglomerativos, aplicando métricas de distância e métodos de ligação (Simples, Completa, Média e Ward) com suporte visual de Dendrogramas.

## 3. Fonte Original

Vídeos "Aula 10a Análise de Agrupamentos", "Aula 10b Aplicação em Python" e "Aula 10c Exemplo passo a passo" (Profa. Cibele Russo).

## 4. Explicação Simples com Analogias

Construir uma árvore genealógica de países baseando-se em seus indicadores econômicos: o algoritmo une primeiro os dois "países irmãos" mais parecidos em um pequeno grupo, e vai fundindo esses grupos progressivamente até formar blocos continentais inteiros.

## 5. Diagrama Visual ASCII

```text
                  Dendrograma de Fusão Hierárquica
   Altura
    12.7 |            +-------+
     6.4 |      +-----+       |
     4.1 |      |     |    +--+--+
     3.2 |   +--+--+  |    |     |
         +---+-----+--+----+-----+---
             A     B  E    C     F
```

## 6. Exemplo Numérico Resolvido Passo a Passo

#### Dada a matriz de distâncias $`6 \times 6`$ contendo os elementos $`\{A, B, C, D, E, F\}`$:

#### Matriz de Distâncias Inicial $`(D_0)`$:

|   | A | B | C | D | E | F |
|---|---|---|---|---|---|---|
| A | 0 | 3,23 | 15,74 | 13,19 | 6,44 | 13,39 |
| B | 3,23 | 0 | 12,73 | 12,04 | 6,44 | 10,19 |
| C | 15,74 | 12,73 | 0 | 16,29 | 17,06 | 4,12 |
| D | 13,19 | 12,04 | 16,29 | 0 | 19,33 | 16,19 |
| E | 6,44 | 6,44 | 17,06 | 19,33 | 0 | 18,00 |
| F | 13,39 | 10,19 | 4,12 | 16,19 | 18,00 | 0 |

Passo 1: Identificar a menor distância global A menor distância na matriz é d(A, B) = 3,23.

* Ação: Fundem-se as observações A e B formando o cluster (AB).

Passo 2: Recalcular a matriz de distâncias usando o Método da Ligação Simples (Mínimo das distâncias) d((AB), $`C) = \min(d(A,C), d(B,C)) = \min(15,74; 12,73) = 12,73`$ d((AB), $`D) = \min(d(A,D), d(B,D)) = \min(13,19; 12,04) = 12,04`$ d((AB), E) = $`\min(d(A,E), d(B,E)) = \min(6,44; 6,44) = 6,44`$ d((AB), $`F) = \min(d(A,F), d(B,F)) = \min(13,39; 10,19) = 10,19`$

A nova menor distância global na matriz atualizada passa a ser d(C, F) = 4,12.

* Ação: Fundem-se C e F criando o cluster (CF).

## 7. Implementação Computacional (Python)

```python
import matplotlib.pyplot as plt
from scipy.cluster.hierarchy import dendrogram, linkage, fcluster

# Exemplo com os pontos do exercício
X_exemplo = np.random.rand(6, 4)

# Gerando a matriz de ligação (linkage) com método de Ward
Z = linkage(X_exemplo, method='ward')

# Desenhando o dendrograma
plt.figure(figsize=(8, 4))
dendrogram(Z, labels=['A', 'B', 'C', 'D', 'E', 'F'])
plt.title("Dendrograma de Agrupamento Hierárquico")
plt.xlabel("Observações")
plt.ylabel("Distância / Altura")
plt.show()

# Efetuando o corte para obter 3 grupos
grupos = fcluster(Z, t=3, criterion='maxclust')
print("Atribuição de grupos:", grupos)
```

## 8. Erros Comuns e Como Evitá-los

* Erro: Fixar o número final de grupos k antes de executar o agrupamento hierárquico.
* Como evitar: O algoritmo hierárquico constrói a árvore completa do nível n até o nível 1. A escolha de k deve ser feita a posteriori, inspecionando o Dendrograma e efetuando um corte na altura vertical que apresenta a maior distância entre fusões sucessivas.

## 9. Resumo da Aula em 3 Pontos

1. O agrupamento aglomerativo parte de n clusters unitários e realiza n-1 fusões sucessivas.
2. Métodos de ligação definem a proximidade entre grupos: Ligação Simples (mínimo), Completa (máximo) e Ward (minimização da variância intra-cluster).
3. O Dendrograma é o recurso gráfico essencial para visualização da taxonomia e seleção do número de grupos.

Aplicações e Tomada de Decisão Executiva: Em arquiteturas de produtos e portfólios complexos, o clustering hierárquico revela a taxonomia natural de serviços, permitindo fusões estratégicas de marcas com base na proximidade de uso do consumidor.

## 10. Exercícios Práticos com Gabarito Comentado Passo a Passo

Exercício 1: Se d(A, C) = 5 e d(B, C) = 8, qual a distância do cluster (AB) ao elemento C utilizando o método da Ligação Completa (Máximo)? Gabarito Passo a Passo:

1. A Ligação Completa define a distância entre um cluster e uma observação como a distância máxima entre seus componentes.
2. d((AB), $`C) = \max(d(A, C)`$, d(B, C)).
3. d((AB), $`C) = \max(5, 8) = 8`$.

Exercício 2: Quantas fusões sucessivas são necessárias para agrupar n=10 países em um único cluster hierárquico final? Gabarito Passo a Passo:

1. Em cada etapa do algoritmo aglomerativo, exatamente dois clusters são fundidos em um único.
2. O algoritmo começa com n clusters e encerra quando resta 1 cluster.
3. O número total de fusões é n - 1 = 10 - 1 = 9.

Exercício 3: Qual métrica de similaridade é recomendada para agrupar pacientes baseando-se estritamente em dados binários de presença (1) ou ausência (0) de sintomas raros? Gabarito Passo a Passo:

1. Em sintomas raros, a co-ausência de sintomas (0-0) não representa uma semelhança clínica relevante.
2. A distância Euclidiana e a concordância simples contam pares 0-0, o que distorceria o agrupamento.
3. Utiliza-se o Coeficiente de Similaridade de Jaccard, que ignora explicitamente as co-ausências no denominador.

Alternativamente à estrutura em árvore do método hierárquico, estuda-se o algoritmo particional k-Médias.

### Aula 12: Clustering Não-Hierárquico: O Algoritmo k-Médias (k-means) e Mapeamento Geográfico

## 1. Título da Aula

Clustering Não-Hierárquico: O Algoritmo k-Médias (k-means) e Mapeamento Geográfico.

## 2. Objetivo de Aprendizagem

Compreender o funcionamento iterativo do algoritmo k-Médias, a sensibilidade às sementes iniciais, o critério do cotovelo para seleção de k e a integração de agrupamentos com mapeamento espacial.

## 3. Fonte Original

Vídeo "Aula 10b Análise de Agrupamentos - Aplicação em Python" (Profa. Cibele Russo).

## 4. Explicação Simples com Analogias

Instalar k antenas de telefonia celular em uma cidade: posicionam-se k antenas em pontos iniciais; cada morador conecta-se à antena mais próxima; em seguida, reajusta-se a posição de cada antena para o centro exato de sua comunidade de usuários. Esse processo repete-se até que as antenas não precisem mais mudar de lugar.

## 5. Diagrama Visual ASCII

```text
                 Otimização Iterativa do k-Médias

   [ Sementes Iniciais ] ---> [ Atribuição por Menor ] ---> [ Recálculo do Centroide ]
   [ (Centroides m_k)  ]      [ Distância Euclidiana ]      [ (Média dos Pontos)    ]
             ^                                                        |
             |----------------- Repete até Convergência <-------------+
```

## 6. Exemplo Numérico Resolvido Passo a Passo

#### Algoritmo do k-Médias em 4 Etapas Formais:

1. Inicialização: Fixa-se o número de clusters k e selecionam-se k centroides iniciais $`\mu_1^{(0)}, \mu_2^{(0)}, \dots, \mu_k^{(0)}`$.
2. Atribuição: Cada observação $`x_j`$ é atribuída ao cluster do centroide mais próximo: $`c_j = \arg\min_{i \in \{1, \dots, k\}} \\vert  x_j - \mu_i \\vert ^2`$
3. Atualização: Recalculam-se os k centroides como a média dos pontos atribuídos a cada grupo: $`\mu_i^{(t+1)} = \frac{1}{\vert G_i\vert } \sum_{x_j \in G_i} x_j`$
4. Convergência: Repetem-se os passos 2 e 3 até estabilização da Inércia Intra-cluster $`(SSW): \text{Inércia} = \sum_{i=1}^k \sum_{x_j \in G_i} \\vert  x_j - \mu_i \\vert ^2`$

#### Estudo de Indicadores Socioeconômicos de 134 Países (Subconjunto de 13 Países):

* Variáveis padronizadas: Inflação, PIB per capita, Crescimento do PIB e Desemprego.
* Utilização do Método do Cotovelo com gráfico de Inércia versus k: seleções em k=3 mostram a formação de:
  * Cluster 0: Economias desenvolvidas (Alemanha, Estados Unidos, Reino Unido).
  * Cluster 1: Economias em desenvolvimento / emergentes da América do Sul (Brasil, Uruguai).
  * Cluster 2: Países em rápido crescimento ou transição (China, Paraguai, Chile, Peru, Bolívia, Equador, Colômbia, Polônia).
* Visualização cartográfica gerada pela integração com o pacote geopandas em Python.

## 7. Implementação Computacional (Python)

```python
import matplotlib.pyplot as plt
from sklearn.cluster import KMeans
from sklearn.preprocessing import StandardScaler

# X_paises: matriz contendo os indicadores dos países
scaler = StandardScaler()
X_scaled = scaler.fit_transform(X_paises)

# Método do Cotovelo para encontrar k
inercias = []
K_range = range(1, 8)
for k in K_range:
    kmeans = KMeans(n_components=k, n_init=10, random_state=42)
    kmeans.fit(X_scaled)
    inercias.append(kmeans.inertia_)

# Ajuste do modelo com k = 3
kmeans_final = KMeans(n_clusters=3, n_init=10, random_state=42)
labels = kmeans_final.fit_transform(X_scaled)
```

## 8. Erros Comuns e Como Evitá-los

* Erro: O algoritmo k-Médias é fortemente sensível à escolha inicial das sementes, correndo o risco de convergir para mínimos locais indesejados.
* Como evitar: Configure o parâmetro n_init no scikit-learn para valores elevados (ex: n_init=10 ou 20), fazendo com que o algoritmo execute múltiplas vezes com sementes diferentes e escolha a solução de menor Inércia global.

## 9. Resumo da Aula em 3 Pontos

1. O k-Médias é um algoritmo particional iterativo que exige a pré-especificação do número k de grupos.
2. A escolha ideal de k é respaldada pela minimização da Inércia intra-cluster via Método do Cotovelo.
3. A padronização previa dos dados é obrigatória para evitar que variáveis com amplitudes elevadas dominem as distâncias Euclidianas.

Aplicações e Tomada de Decisão Executiva: Em inteligência de mercado, o k-Médias permite segmentar bases de milhões de clientes em grupos homogêneos para personalizar ofertas de crédito, apresentando eficiência computacional exponencialmente superior aos métodos hierárquicos.

## 10. Exercícios Práticos com Gabarito Comentado Passo a Passo

Exercício 1: Dados dois centroides $`\mu_1 = \begin{bmatrix} 0 \\ 0 \end{bmatrix}`$ e $`\mu_2 = \begin{bmatrix} 10 \\ 10 \end{bmatrix}`$, a qual cluster será atribuída a observação $`x_j = \begin{bmatrix} 2 \\ 3 \end{bmatrix}?`$ Gabarito Passo a Passo:

1. Calcule a distância Euclidiana ao quadrado para o Centroide $`1: d^2(x_j, \mu_1) = (2 - 0)^2 + (3 - 0)^2 = 2^2 + 3^2 = 4 + 9 = 13`$
2. Calcule a distância Euclidiana ao quadrado para o Centroide $`2: d^2(x_j, \mu_2) = (2 - 10)^2 + (3 - 10)^2 = (-8)^2 + (-7)^2 = 64 + 49 = 113`$
3. Como 13 < 113, a observação $`x_j`$ é atribuída ao Cluster 1.

Exercício 2: Qual a complexidade computacional do k-Médias por iteração e por que ele é preferível ao Agrupamento Hierárquico para Big Data? Gabarito Passo a Passo:

1. O k-Médias possui complexidade $`O(n \cdot k \cdot p \cdot t)`$, em que t é o número de iterações.
2. O Agrupamento Hierárquico possui complexidade $`O(n^2 \cdot p)`$ e exige armazenar uma matriz de distância $`n \times n`$ na memória RAM.
3. Para grandes bases (n > 100.000), o k-Médias é linear em relação ao tamanho da base n, sendo viável computacionalmente.

Exercício 3: Se todas as variáveis já estiverem padronizadas e o número de grupos escolhido for k = n, qual o valor teórico da Inércia intra-cluster? Gabarito Passo a Passo:

1. Quando k = n, cada observação individual transforma-se em seu próprio centroide $`(\mu_i = x_i)`$.
2. A distância de cada ponto ao seu centroide correspondente é exatamente 0.
3. Logo, a Inércia intra-cluster total reduz-se a 0.

Concluído o estudo das técnicas não-supervisionadas, finaliza-se a trilha abordando técnicas de classificação supervisionada e correspondência.

## MÓDULO 7: CLASSIFICAÇÃO SUPERVISIONADA E FECHAMENTO

### Aula 13: Análise Discriminante Linear (LDA) e Regressão Logística para Classificação

## 1. Título da Aula

Análise Discriminante Linear (LDA) e Regressão Logística para Classificação.

## 2. Objetivo de Aprendizagem

Formular funções discriminantes lineares de Fisher para classificar novas observações em G grupos conhecidos e estabelecer comparações críticas entre a LDA e a Regressão Logística.

## 3. Fonte Original

Vídeos "Aula 11b Função de discriminação logística", "Aula 11c Análise discriminante linear Exemplo" e "Aula 11d Aplicação em Python" (Profa. Cibele Russo).

## 4. Explicação Simples com Analogias

* LDA: Traçar uma linha reta perfeita em um gráfico para separar espécies de plantas com base no tamanho das pétalas.
* Regressão Logística: Calcular a probabilidade percentual exata de uma transação bancária ser "Fraude" (1) ou "Lícita" (0).

## 5. Diagrama Visual ASCII

```text
                 Fronteira Linear de Decisão (LDA)
       Var X2 |
              |   Grupo 0     /   Grupo 1
              |      *       /       o
              |    *   *    /      o   o   ===> Separação Linear Maximizada
              |      *     /         o
              +-----------/---------------- Var X1
                      Fronteira LDA
```

## 6. Exemplo Numérico Resolvido Passo a Passo

Considere o clássico conjunto de dados das Flores Íris (n=150 observações, p=4 variáveis contínuas, 3 espécies de flores: Setosa, Versicolor, Virginica).

Regra Discriminante Linear de Fisher: Sob a suposição de normalidade multivariada e matrizes de covariância iguais $`(\Sigma_1 = \Sigma_2 = \dots = \Sigma_G = \Sigma)`$, a função discriminante linear $`d_k(x)`$ para o grupo k é: $`d_k(x) = x^T \Sigma^{-1} \mu_k - \frac{1}{2} \mu_k^T \Sigma^{-1} \mu_k + \ln(\pi_k)`$ em que $`\pi_k`$ é a probabilidade a priori do grupo k. A observação x é atribuída ao grupo com maior valor de $`d_k(x)`$.

Avaliação de Desempenho no Banco de Teste (20% dos dados): Ao treinar o modelo de LDA com $`80\%`$ da base e predizer as 30 observações do banco de teste invisível, obtém-se a seguinte Matriz de Confusão:

| Classe Real $`\`$ Classe Predita | Setosa | Versicolor | Virginica |
|---|---|---|---|
| Setosa | 10 | 0 | 0 |
| Versicolor | 0 | 9 | 1 |
| Virginica | 0 | 0 | 10 |

* Acurácia do Modelo no Teste: $`\text{Acurácia} = \frac{10 + 9 + 10}{30} = \frac{29}{30} \approx 96,67\%`$.

## 7. Implementação Computacional (Python)

```python
from sklearn.datasets import load_iris
from sklearn.discriminant_analysis import LinearDiscriminantAnalysis
from sklearn.model_selection import train_test_split
from sklearn.metrics import accuracy_score, confusion_matrix

# Carregamento dos dados das Flores Íris
iris = load_iris()
X, y = iris.data, iris.target

# Divisão Treino (80%) e Teste (20%)
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.20, random_state=42)

# Treinamento do Modelo LDA
lda = LinearDiscriminantAnalysis()
lda.fit(X_train, y_train)

# Predição no Banco de Teste
y_pred = lda.predict(X_test)

print("Acurácia no Teste:", accuracy_score(y_test, y_pred))
print("Matriz de Confusão:\n", confusion_matrix(y_test, y_pred))
```

## 8. Erros Comuns e Como Evitá-los

* Erro: Confundir a Análise de Componentes Principais (PCA) com a Análise Discriminante Linear (LDA).
* Como evitar: Mnemônico fundamental: PCA é NÃO-SUPERVISIONADA (ignora os rótulos de classe Y e busca maior variância total); LDA é SUPERVISIONADA (utiliza os rótulos de classe Y para maximizar a separação entre as classes em relação à variância dentro das classes).

## 9. Resumo da Aula em 3 Pontos

1. A LDA busca combinações lineares que maximizem a variabilidade entre grupos em relação à variabilidade dentro dos grupos.
2. A Regressão Logística é uma alternativa robusta quando as suposições de normalidade multivariada das covariáveis são violadas.
3. A validação de modelos de classificação deve ser conduzida separando o conjunto de dados em bases independentes de treino e teste.

Aplicações e Tomada de Decisão Executiva: Em modelos de Credit Scoring para concessoes de empréstimos, a LDA e a Regressão Logística convertem indicadores operacionais do proponente em notas de risco, permitindo a automação do processo de aprovação de crédito com controle rigoroso da inadimplência.

## 10. Exercícios Práticos com Gabarito Comentado Passo a Passo

Exercício 1: Qual o número máximo de funções discriminantes lineares que podem ser calculadas em um problema com p=4 variáveis contínuas e G=3 grupos? Gabarito Passo a Passo:

1. O número máximo de funções discriminantes é limitado por $`\min(p, G-1)`$.
2. Substituindo os valores: $`\min(4, 3 - 1) = \min(4, 2) = 2`$.

Exercício 2: Em um problema binário, se o modelo de Regressão Logística estima um logit $`z = \beta_0 + \beta_1 X_1 = 0`$, qual a probabilidade estimada P(Y=1|X)? Gabarito Passo a Passo:

1. A função logística é dada por P(Y=1|X) = $`\frac{1}{1 + e^{-z}}`$.
2. Substituindo z = 0: P(Y=1|X) = $`\frac{1}{1 + e^0} = \frac{1}{1 + 1} = \frac{1}{2} = 0,50 (50\%)`$.

Exercício 3: Se uma matriz de confusão no banco de teste apresenta 28 acertos e 2 erros em um total de 30 amostras, determine a acurácia global do classificador. Gabarito Passo a Passo:

1. A acurácia é a razão entre o total de acertos e o total de previsões efetuadas.
2. $`\text{Acurácia} = \frac{28}{28 + 2} = \frac{28}{30} \approx 0,9333 (93,33\%)`$.

Para encerrar a trilha, explora-se a análise de associação para dados categóricos e consolida-se a visão integrada do aprendizado multivariado.

### Aula 14: Introdução à Análise de Correspondência (CA) e Síntese de Aprendizado Multivariado

## 1. Título da Aula

Introdução à Análise de Correspondência (CA) e Síntese de Aprendizado Multivariado.

## 2. Objetivo de Aprendizagem

Compreender a formulação algébrica rigorosa da Análise de Correspondência Simples para associação de variáveis categóricas via Decomposição em Valores Singulares (SVD) da matriz de resíduos padronizados e integrar todas as metodologias da trilha.

## 3. Fonte Original

Vídeos "Aula 12b Análise de Correspondência aplic em Python" e visão geral do curso da Profa. Cibele Russo.

## 4. Explicação Simples com Analogias

A Análise de Correspondência é para variáveis categóricas (como nível de escolaridade e preferência política) o que a PCA é para variáveis contínuas: uma forma de mapear visualmente a "proximidade" entre as categorias em um gráfico bidimensional.

## 5. Formulação Algébrica Formal e Exemplo Numérico

Dada uma Tabela de Contingência N de dimensão $`r \times c`$, com frequência total $`n_T = \sum_{i} \sum_{j} N_{ij}`$:

1. Matriz de Correspondência (P): $`P = \frac{1}{n_T} N`$.
2. Vetores de Massas de Linha (r) e Coluna (c): $`r = P \mathbf{1}_c`$ e $`c = P^T \mathbf{1}_r`$.
3. Matrizes Diagonais de Massa: $`R = \text{diag}(r)`$ e $`C = \text{diag}(c)`$.
4. Matriz de Resíduos Padronizados (S): $`S = R^{-1/2} (P - r c^T) C^{-1/2}`$
5. Decomposição em Valores Singulares (SVD) de S: $`S = U D_\alpha V^T`$ em que os elementos de $`D_\alpha = \text{diag}(\alpha_1, \alpha_2, \dots)`$ são os valores singulares.
6. Inércia Total $`(\phi^2)`$: A Inércia Total reflete o afastamento da independência (Qui-Quadrado padronizado): $`\phi^2 = \frac{\chi^2}{n_T} = \sum_{k=1}^{\min(r-1, c-1)} \alpha_k^2`$
7. Coordenadas Principais:
  * Linhas: $`F = R^{-1/2} U D_\alpha`$.
  * Colunas: $`G = C^{-1/2} V D_\alpha`$.

As duas primeiras colunas de F e G formam o Mapa Perceptual Bidimensional.

## 6. Diagrama Visual ASCII

```text
                  MAPA MENTAL DE DECISÃO DA TRILHA MULTIVARIADA
                                        |
     +----------------------------------+----------------------------------+
     |                                                                     |
```

[VARIÁVEIS CONTÍNUAS]                                               [DADOS CATEGÓRICOS]
```text
     |                                                                     |
     +--> Reduzir Variáveis?                                               +--> Tabela Contingência?
     |    |--> Não-Supervisionado: PCA (Aula 9, 10)                             |--> Análise de
     |                                                                           Correspondência (Aula 14)
     +--> Agrupar Indivíduos?
     |    |--> Hierárquico: Dendrograma (Aula 11)
     |    |--> Particional: k-Médias (Aula 12)
     |
     +--> Comparar Grupos / Testar Médias?
     |    |--> 1 Amostra: T2 de Hotelling (Aula 4)
     |    |--> 2 Grupos: T2 Pareado / Independente (Aula 5)
     |    |--> G Grupos: MANOVA / Wilks (Aula 6)
     |
     +--> Prever / Classificar com Rótulos (Supervisionado)?
          |--> Múltiplas Respostas Contínuas: Regressão Multivariada (Aula 7)
          |--> Associação entre 2 Blocos: CCA (Aula 8)
          |--> Rótulos de Classe Discretos: LDA / Reg. Logística (Aula 13)
```

## 7. Implementação Computacional (Python)

```python
import pandas as pd
import numpy as np

def analise_correspondencia_simples(tabela_contingencia):
    N = np.array(tabela_contingencia)
    n_T = np.sum(N)

    P = N / n_T
    r = np.sum(P, axis=1)
    c = np.sum(P, axis=0)

    R_inv_sqrt = np.diag(1.0 / np.sqrt(r))
    C_inv_sqrt = np.diag(1.0 / np.sqrt(c))

    # Matriz S
    S = np.dot(R_inv_sqrt, np.dot(P - np.outer(r, c), C_inv_sqrt))

    # SVD
    U, D_alpha, Vt = np.linalg.svd(S, full_matrices=False)

    inercia_total = np.sum(D_alpha**2)
    inercia_explicada = (D_alpha**2) / inercia_total

    return D_alpha, inercia_total, inercia_explicada

# Exemplo com tabela de contingência 3x3
N_exemplo = [[50, 10, 5], [15, 45, 20], [5, 10, 60]]
D, inercia, prop = analise_correspondencia_simples(N_exemplo)
print(f"Inércia Total: {inercia:.4f}")
print("Proporção Explicada pelas Dimensões:", prop)
```

## 8. Erros Comuns e Como Evitá-los

* Erro: Tentar aplicar PCA padrão em dados estritamente categóricos não-numéricos (frequências de tabela de contingência).
* Como evitar: Para tabelas de frequência categóricas, utilize a Análise de Correspondência Simples ou Múltipla baseada na métrica do Qui-Quadrado.

## 9. Resumo da Aula em 3 Pontos

1. A Análise de Correspondência aplica-se a variáveis categóricas estruturadas em tabelas de contingência.
2. Utiliza a Decomposição em Valores Singulares (SVD) sobre a matriz de resíduos padronizados para decompor a Inércia Total $`(\phi^2 = \chi^2 / n_T)`$.
3. O domínio de toda a trilha capacita o estatístico a selecionar a ferramenta ideal conforme a natureza do dado e o objetivo de análise.

Aplicações e Tomada de Decisão Executiva: Em pesquisas de posicionamento de mercado, a Análise de Correspondência mapeia marcas e atributos qualitativos em um único gráfico 2D, orientando o reposicionamento da marca frente aos concorrentes.

## 10. Exercícios Práticos com Gabarito Comentado Passo a Passo

Exercício 1: Qual técnica multivariada deve ser selecionada para agrupar 1.000 clientes em k=4 perfis sem rótulos prévios, utilizando variáveis contínuas padronizadas? Gabarito Passo a Passo:

1. Avalie as características: dados contínuos, sem rótulos prévios (Y), objetivo de agrupar observações.
2. Trata-se de um problema de aprendizado não-supervisionado particional.
3. A técnica adequada é o algoritmo de k-Médias (k-means).

Exercício 2: Se o objetivo é prever a espécie de uma planta (variável categórica com 3 classes) a partir de 4 medidas contínuas utilizando uma base de treino rotulada, qual técnica supervisionada é a mais indicada sob suposição de normalidade? Gabarito Passo a Passo:

1. Avalie as características: dados contínuos de entrada, resposta categórica com G=3 classes, banco de treino rotulado.
2. Trata-se de um problema de classificação supervisionada.
3. Sob a suposição de normalidade multivariada, a técnica estatística ótima é a Análise Discriminante Linear (LDA).

Exercício 3: Se uma tabela de contingência possui r=3 linhas e c=4 colunas, qual o número máximo de dimensões que compõem a Inércia Total na Análise de Correspondência? Gabarito Passo a Passo:

1. O número máximo de valores singulares não-nulos na SVD da matriz S é limitado por $`K_{max} = \min(r-1, c-1)`$.
2. Substituindo os valores: $`K_{max} = \min(3-1, 4-1) = \min(2, 3) = 2`$.
3. Logo, a Inércia Total pode ser representada por no máximo 2 dimensões.

#### Mensagem de Encerramento e Parabéns!

Parabéns pela Conclusão da Trilha! Você completou com êxito toda a jornada didática de Análise Multivariada e Aprendizado Não-Supervisionado. Ao longo deste guia de estudos, você dominou desde a notação matricial fundamental, a modelagem probabilística via Normal Multivariada, a inferência rigorosa para vetores de médias ($`T^2`$, MANOVA, Teste M de Box), a redução inteligente de dimensionalidade (PCA, CCA), até os algoritmos de agrupamento (k-means, Dendrogramas), classificação (LDA) e Análise de Correspondência (CA). Você está plenamente capacitado a aplicar estes métodos estatísticos com rigor analítico, excelência computacional e alto impacto executivo na Ciência de Dados!
