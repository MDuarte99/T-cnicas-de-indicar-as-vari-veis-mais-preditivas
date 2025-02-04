Implementação de Técnicas e Algoritmos para Seleção de Variáveis Preditivas

Visão Geral

Este repositório propõe diversas técnicas de seleção de variáveis preditivas por meio de Feature Engineering, permitindo identificar quais variáveis têm maior impacto na previsão de problemas cardíacos. O foco está na análise de dados relacionados a doenças cardíacas, utilizando diferentes abordagens estatísticas e de aprendizado de máquina para melhorar a interpretação e desempenho dos modelos preditivos.

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

Processamento dos Dados

O primeiro passo do projeto é a análise exploratória e o tratamento dos dados. Isso é feito no arquivo "Tratamento_Dados_heart", onde:

Os dados são analisados estatisticamente para detectar padrões e inconsistências.

Dados faltantes são tratados adequadamente.

O conjunto de dados limpo é salvo como "Tratamento_Dados_heart.csv".

Após a preparação dos dados, passamos para o arquivo "Importancia_var_hear", onde são aplicadas as seguintes técnicas de seleção de variáveis:

Técnicas de Seleção de Variáveis

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

Como Executar

Clone este repositório:

git clone https://github.com/seu-usuario/seu-repositorio.git

Instale as dependências:

pip install -r requirements.txt

Execute o notebook no Jupyter Notebook ou Google Colab.

Contribuição

Contribuições são bem-vindas! Sinta-se à vontade para abrir uma issue ou enviar um pull request.

Licença

Este projeto está licenciado sob a MIT License.
