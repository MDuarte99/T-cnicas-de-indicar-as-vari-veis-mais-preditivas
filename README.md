# Implementação de Técnicas e Algoritmos para Seleção de Variáveis Preditivas
Esse repositório propõe diversas técnicas   de apontar em seu modelo as variáveis mais preditivas em seu modelos por meio de "Feature Engineering".
Visão Geral

Este repositório contém a implementação de técnicas de seleção de variáveis mais preditivas para análise de dados relacionados a doenças cardíacas. O objetivo é identificar quais variáveis têm maior impacto na previsão de problemas cardíacos.

Dados Utilizados

O banco de dados utilizado no projeto é o "heart.csv", que contém informações sobre pacientes e diversas variáveis clínicas.

Descrição das Variáveis

Age: Idade do paciente

Sex: Sexo do paciente (M: Masculino, F: Feminino)

ChestPainType: Tipo de dor no peito (TA: Angina típica, ATA: Angina atípica, NAP: Dor não anginal, ASY: Assintomático)

RestingBP: Pressão sanguínea em repouso (mmHg)

Cholesterol: Colesterol sérico (mm/dl)

FastingBS: Açúcar no sangue em jejum (0: < 120 mg/dl, 1: >= 120 mg/dl)

RestingECG: Resultado do eletrocardiograma em repouso (Normal, ST, LVH)

MaxHR: Frequência cardíaca máxima alcançada

ExerciseAngina: Angina induzida por exercícios (Y: Sim, N: Não)

Oldpeak: Depressão do segmento ST

ST_Slope: Inclinação do segmento ST (Up, Flat, Down)

HeartDisease: Presença de doença cardíaca (0: Não, 1: Sim)

O primeiro arquivo "Tratamento_Dados_heart" Faz análise exploratoria dos dado e trata dados faltantes Gerando o arquivo .csv "Tratamento_Dados_heart.csv"

Depois pode-se proceder ao arquivo "Importancia_var_hear" nele será feita as:

Técnicas de Seleção de Variáveis

Neste projeto, utilizamos diversas técnicas para determinar a importância das variáveis:

Seleção K-Best: Método que seleciona as melhores variáveis com base em testes estatísticos, como qui-quadrado ou ANOVA.

Regressão Logística: Algoritmo estatístico que mede a contribuição de cada variável na previsão do resultado.

Random Forest Feature Importance: Mede a importância das variáveis com base na redução de impureza nas árvores de decisão dentro de um modelo Random Forest.

LightGBM: Algoritmo baseado em gradient boosting que usa histogramas para otimizar a seleção de variáveis importantes.

XGBoost: Técnica avançada de gradient boosting que calcula a importância das variáveis através da melhoria do modelo.

Boruta: Método baseado em Random Forest que compara a importância das variáveis reais com variáveis artificiais (shadow features) para identificar as mais relevantes.

Mutual Information: Avalia a dependência entre as variáveis preditoras e a variável alvo, identificando quais carregam mais informação relevante para a previsão.

Tecnologias Utilizadas

Python

Pandas

Scikit-learn

Matplotlib

Seaborn


