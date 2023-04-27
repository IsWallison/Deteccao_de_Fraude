# Deteccao_de_Fraude
[![author](https://img.shields.io/badge/author-Wallison-red.svg)](https://www.linkedin.com/in/wallison-borges-48312516a/) [![](https://img.shields.io/badge/python-3.7+-blue.svg)](https://www.python.org/downloads/release/python-365/) [![GPLv3 license](https://img.shields.io/badge/License-GPLv3-blue.svg)](http://perso.crans.org/besson/LICENSE.html) [![contributions welcome](https://img.shields.io/badge/contributions-welcome-brightgreen.svg?style=flat)](https://github.com/IsWallison/Project_airbnb/issues)

<p align="center">
  <img src="high-angle-keyboard-with-credit-cards-hook-phishing.jpg" >
</p>

# Projeto
Neste projeto, iremos abordar o problema das fraudes em cartões de crédito, uma das principais preocupações das instituições financeiras como bancos e fintechs. Apenas no Brasil, cerca de 12,1 milhões de pessoas já foram vítimas de algum tipo de fraude financeira no último ano. Traduzindo em valores, os golpes financeiros ultrapassaram a cifra de R$ 1,8 bilhão de prejuízo por ano para os últimos 12 meses. Dentre essas fraudes, aquelas envolvendo cartões de crédito são de grande relevância uma vez que a sua não-detecção acaretará em prejuízos consideráveis, tanto para o consumidor quanto para a instituição financeira. Um outro fator a ser considerado é a quantidade de falsos positivos, ou seja, aquelas vezes em que você tentou fazer uma compra e teve seu cartão bloqueado preventivamente - o que provavelmente gerou estresse e constrangimento. Por todos esses motivos, o investimento na área de detecção de fraudes por meio de Inteligência Artificial vem crescendo a cada ano, representando uma grande oportunidade em Data Science. Dispondo de grandes volumes de dados como base histórica, um algoritmo de machine learning apenas um pouco melhor que os anteriores já representa uma economia de milhões de Reais. E esse é o desafio, aprimorar cada vez mais o uso de algoritmos visando inibir ou evitar transações


# Dataset
O conjunto de dados pode ser facilmente encontrado aqui: https://www.dropbox.com/s/b44o3t3ehmnx2b7/creditcard.csv?dl=1

# Bibliotecas necessárias

* Pandas
* Matplotlib
* Seaborn 
* Datetime
* numpy
* sklearn (Vários pacotes)
* imblearn (RandomUnderSampler)
Você também precisará de um software que possa executar um notebook python .ipynb

# Modelo para prevenção de fraudes

Um modelo de aprendizado de máquina para prevenção de fraudes funciona ao analisar padrões em dados financeiros ou de compra de um indivíduo ou empresa. A partir da análise desses padrões, o modelo é treinado para identificar transações suspeitas ou comportamentos atípicos que possam indicar fraude.

O modelo é treinado usando dados históricos de transações legítimas e fraudulentas, e é alimentado com informações como horário da transação, valor da transação, localização geográfica e outros fatores relevantes. A partir desse treinamento, o modelo aprende a identificar padrões e comportamentos que possam ser indicativos de fraude.

Quando uma transação é realizada, o modelo compara as informações da transação com os padrões aprendidos durante o treinamento e classifica a transação como legítima ou suspeita. Se a transação é classificada como suspeita, ela é revisada manualmente para verificar se é uma fraude ou não.

Um modelo de prevenção de fraudes bem treinado pode ajudar a detectar fraudes rapidamente, minimizando o impacto financeiro e reputacional para os indivíduos ou empresas afetados. Além disso, os modelos de aprendizado de máquina também podem ser ajustados e atualizados constantemente para se adaptarem a novos padrões e comportamentos de fraude.

4 modelos foram utilizados:

Logistic Regretion
k-nearest neighbors
Decision Tree
Naive Bayes

# Resultados

### Comparação entre os modelos
--------------------------
  Modelo  | Acc | Mae | Rsme | TP | TN | FP | FN
  ------------|-----------|-----------|-----------|-----------|-----------|-----------|-----------
  Logistic Regretion | 0.94 | 0.056 | 0.238 | 118 | 114 | 5 | 9
  k-nearest neighbors | 0.922 | 0.077 | 0.277 | 117 | 110 | 6 | 13 
  Decision Tree| 0.922 | 0.077| 0.277 | 117 | 110 | 6 | 13
  Naive Bayes | 0.91 | 0.085 | 0.29 | 118 | 107 | 5 | 16

A partir dos dados apresentados acima, é possível ver que o modelo de Regressão Logística apresentou a melhor precisão, seguido de perto pelos modelos k-nearest neighbors e Decision Tree.

Os modelos apresentam resultados similares em relação aos valores de TP (verdadeiros positivos), TN (verdadeiros negativos), FP (falsos positivos) e FN (falsos negativos). A diferença entre os modelos nesses valores não é significativa e, portanto, não afeta significativamente a precisão geral dos modelos. Entretanto, é importante levar em consideração que os valores de TP, TN, FP e FN são importantes para avaliar a performance dos modelos de prevenção de fraudes, já que eles representam, respectivamente, a quantidade de transações fraudulentas corretamente identificadas, a quantidade de transações não-fraudulentas corretamente identificadas, a quantidade de transações não-fraudulentas incorretamente identificadas como fraudes e a quantidade de transações fraudulentas incorretamente identificadas como não-fraudulentas.
