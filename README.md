# Ensaio de Machine Learning
## 1.0. Descrição
A empresa Data Money acredita que a expertise no treinamento e ajuste
fino dos algoritmos, feito pelos Cientistas de Dados da empresa, é a
principal motivo dos ótimos resultados que as consultorias vem
entregando aos seus clientes.
## 2.0. Objetivo
O objetivo desse projeto será realizar ensaios com algoritmos de
Classificação, Regressão e Clusterização, para estudar a mudança do
comportamento da performance, a medida que os valores dos principais
parâmetros de controle de overfitting e underfitting mudam.
# 3.0. Planejamento da solução
## 3.1. Produto final
O produto final será 7 tabelas mostrando a performance dos algoritmos,
avaliados usando múltiplas métricas, para 3 conjuntos de dados
diferentes: Treinamento, validação e teste.
## 3.2. Algoritmos ensaiados
### Classificação:
**Algoritmos:** KNN, Decision Tree, Random Forest e Logistic Regression

**Métricas de performance:** Accuracy, Precision, Recall e F1-Score
### Regressão:
**Algoritmos:** Linear Regression, Decision Tree Regressor, Random Forest
Regressor, Polinomial Regression, Linear Regression Lasso, Linear
Regression Ridge, Linear Regression Elastic Net, Polinomial Regression
Lasso, Polinomial Regression Ridge e Polinomial Regression Elastic Net

**Métricas de performance:** R2, MSE, RMSE, MAE e MAPE
### Agrupamento:
**Algoritmos:** K-Means e Affinity Propagation

**Métricas de performance:** Silhouette Score
## 4.0. Ferramentas utilizadas
Python 3.8 e Scikit-learn
# 5.0. Desenvolvimento
## Estratégia da solução
Para o objetivo de ensaiar os algoritmos de Machine Learning, eu vou
escrever os códigos utilizando a linguagem Python, para treinar cada um
dos algoritmos e vou variar seus principais parâmetros de ajuste de
overfitting e observar a métrica final.
O conjunto de valores que fizerem os algoritmos alcançarem a melhor
performance, serão aqueles escolhidos para o treinamento final do
algoritmo.
## O passo a passo
**Passo 1:** Divisão dos dados em treino, teste e validação.

**Passo 2:** Treinamento dos algoritmos com os dados de treinamento,
utilizando os parâmetros “default”.

**Passo 3:** Medir a performance dos algoritmos treinados com o parâmetro
default, utilizando o conjunto de dados de treinamento.

**Passo 4:** Medir a performance dos algoritmos treinados com o parâmetro
“default”, utilizando o conjunto de dados de validação.

**Passo 5:** Alternar os valores dos principais parâmetros que controlam o
overfitting do algoritmo até encontrar o conjunto de parâmetros apresente
a melhor performance dos algoritmos.

**Passo 6:** Unir os dados de treinamento e validação

**Passo 7:** Retreinar o algoritmo com a união dos dados de treinamento e
validação, utilizando os melhores valores para os parâmetros de controle
do algoritmo.

**Passo 8:** Medir a performance dos algoritmos treinados com os melhores
parâmetro, utilizando o conjunto de dados de teste.

**Passo 9:** Avaliar os ensaios e anotar os 3 principais Insights que se
destacaram.

# 6.0. Os top 3 Insights
### 6.1. Insight Top 1
Os algoritmos baseado em árvores possuem uma performance melhores
em todas as métricas, quando aplicados sobre os dados de teste, no
ensaio de Classificação.
## 6.2. Insight Top 2
A performance dos algoritmos de classificação sobre os dados de
validação ficou bem próxima da performance sobre os dados de teste.
## 6.3. Insight Top 3
Todos os algoritmo de regressão não apresentaram boas métricas de
performance, o que mostra uma necessidade de uma seleção de atributos
e uma preparação melhor das variáveis independentes do conjunto de
dados.
# 7.0. Resultados
## 7.1. Ensaio de classificação:
### Sobre os dados de treinamento
Model Name |	Accuracy |	Precision |	Recall | F1-Score
---------- |  -------- | ---------- | ------ | --------
KNN |	0.832 |	0.812 |	0.797 |	0.805
Decision Tree |	0.966 |	0.977 |	0.945 |	0.961
Random Forest |	1.000 |	1.000 |	1.000 |	1.000
Logistic Regression |	0.567 |	0.636 |	0.000 |	0.000


### Sobre os dados de validação

Model Name |	Accuracy |	Precision |	Recall | F1-Score
---------- |  -------- | ---------- | ------ | --------
KNN |	0.676 |	0.628 |	0.621 | 0.625
Decision Tree |	0.952 |	0.959 |	0.929 |	0.943
Random Forest |	0.965 |	0.974 |	0.945 |	0.959
Logistic Regression |	0.567 |	0.750 |	0.000 |	0.000

### Sobre os dados de teste

Model Name |	Accuracy |	Precision |	Recall | F1-Score
---------- |  -------- | ---------- | ------ | --------
KNN |	0.672 |	0.630 |	0.612 |	0.621
Decision Tree |	0.950 |	0.957 |	0.927 |	0.942
Random Forest |	0.964 |	0.972 |	0.946 |	0.958
Logistic Regression |	0.561 |	0.000 |	0.000 |	0.000


## 7.2. Ensaio de regressão:

### Sobre os dados de treinamento

Model Name |	R2 |	MSE |	RMSE |	MAE |	MAPE
---------- |  -- | ---- | ---- | ---- | ----
Linear Regression | 0.046 |	455.996 |	21.354 |	16.998 |	865.319
Decision Tree Regressor |	0.114 |	423.747 |	20.585 |	16.369 |	786.954
Random Forest Regressor |	0.904 |	45.741 |	6.763 |	4.845 |	261.395
Polinomial Regression |	0.094 |	432.986 |	20.808 |	16.458 |	835.054
Linear Regression Lasso |	0.046 |	456.057 |	21.355 |	17.002 |	866.067
Linear Regression Ridge |	0.046 |	456.020 |	21.355 |	16.999 |	865.525
Linear Regression Elastic Net |	0.027 |	465.046 |	21.565 |	17.153 |	868.619
Polinomial Regression Lasso |	0.087 |	436.505 |	20.893 |	16.543 |	842.795
Polinomial Regression Ridge |	0.094 |	432.987 |	20.808 |	16.458 |	835.056
Polinomial Regression Elastic Net |	0.087 |	436.505 |	20.893 |	16.543 |	842.795

### Sobre os dados de validação

Model Name |	R2 |	MSE |	RMSE |	MAE |	MAPE
---------- |  -- | ---- | ---- | ---- | ----
Linear Regression |	0.040 |	458.447 |	21.411 |	17.040 |	868.254
Decision Tree Regressor |	0.064 |	447.161 |	21.146 |	16.843 |	839.578
Random Forest Regressor |	0.337 |	316.541 |	17.792 |	12.989 |	700.538
Polinomial Regression |	0.066 |	445.768 |	21.113 |	16.750 |	854.793
Linear Regression Lasso |	0.040 |	458.445 |	21.411 |	17.038 |	868.621
Linear Regression Ridge |	0.040 |	458.441 |	21.411 |	17.038 |	868.134
Linear Regression Elastic Net |	0.026 |	465.307 |	21.571 |	17.121 |	867.703
Polinomial Regression Lasso |	0.068 |	444.933 |	21.093 |	16.732 |	858.740
Polinomial Regression Ridge |	0.067 |	445.709 |	21.112 |	16.749 |	854.876
Polinomial Regression Elastic Net |	0.068 |	444.933 |	21.093 |	16.732 |	858.740

### Sobre os dados de teste

Model Name |	R2 |	MSE |	RMSE |	MAE |	MAPE
---------- |  -- | ---- | ---- | ---- | ----
Linear Regression |	0.052 |	461.428 |	21.481 |	17.130 |	852.186
Decision Tree Regressor |	0.072	| 451.756 |	21.255 |	17.011 |	783.395
Random Forest Regressor |	0.351 |	315.835	| 17.772	| 13.068	| 663.328
Polinomial Regression	| 0.090	| 443.041	| 21.049	| 16.721	| 824.246
Linear Regression Lasso |	0.052	| 461.592	| 21.485	| 17.130	| 853.947
Linear Regression Ridge	| 0.052	| 461.495	| 21.482	| 17.128	| 853.066
Linear Regression Elastic Net	| 0.028	| 473.107	| 21.751	| 17.298	| 868.867
Polinomial Regression Lasso	| 0.086	| 445.017	| 21.095	| 16.759	| 832.238
Polinomial Regression Ridge	| 0.090	| 443.025	| 21.048	| 16.720	| 824.366
Polinomial Regression Elastic Net	| 0.086	| 445.017	| 21.095	| 16.759	| 832.238

## 7.3. Ensaio de clusterização:

Model Name	| SS	| Clusters
----------  | --  | --------
K-MEANS	| 0.233	| 3
AFFINITY PROPAGATION	| 0.215	| 3

# 8.0. Conclusão
Nesse ensaio de Machine Learning, consegui adquirir experiência e
entender melhor sobre os limites dos algoritmos entre os estados de
underffiting e overfitting.
Algoritmos baseados em árvores são sensível quanto a profundidade do
crescimento e do número de árvores na floresta, fazendo com que a
escolha correta dos valores desses parâmetros impeçam os algoritmos de
entrar no estado de overfitting.
Os algoritmos de regressão, por outro lado, são sensíveis ao grau do
polinômio. Esse parâmetro controla o limite entre o estado de underfitting
e overfitting desses algoritmos.
Esse ensaio de Machine Learning foi muito importante para aprofundar o
entendimento sobre o funcionamento de diversos algoritmos de
classificação, regressão e clusterização e quais os principais parâmetros
de controle entre os estados de underfitting e overfitting.
# 9.0. Próximos passos
Como próximos passos desse ensaio, pretendo ensaiar novos algoritmos
de Machine Learning e usar diferentes conjuntos de dados para aumentar
o conhecimento sobre os algoritmos e quais cenários são mais favoráveis
para o aumento da performance dos mesmos.

