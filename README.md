# Implementação de Técnicas e Algoritmos para Seleção de Variáveis Preditivas

## Visão Geral
Este repositório propõe diversas técnicas de seleção de variáveis preditivas por meio de **Feature Engineering**, permitindo identificar quais variáveis têm maior impacto na previsão de problemas cardíacos. O foco está na análise de dados relacionados a doenças cardíacas, utilizando diferentes abordagens estatísticas e de aprendizado de máquina para melhorar a interpretação e desempenho dos modelos preditivos.

## Dados Utilizados
O banco de dados utilizado no projeto é o **"heart.csv"**, que contém informações sobre pacientes e diversas variáveis clínicas.

### Descrição das Variáveis
- **Age**: Idade do paciente
- **Sex**: Sexo do paciente (M: Masculino, F: Feminino)
- **ChestPainType**: Tipo de dor no peito (TA: Angina típica, ATA: Angina atípica, NAP: Dor não anginal, ASY: Assintomático)
- **RestingBP**: Pressão sanguínea em repouso (mmHg)
- **Cholesterol**: Colesterol sérico (mm/dl)
- **FastingBS**: Açúcar no sangue em jejum (0: < 120 mg/dl, 1: >= 120 mg/dl)
- **RestingECG**: Resultado do eletrocardiograma em repouso (Normal, ST, LVH)
- **MaxHR**: Frequência cardíaca máxima alcançada
- **ExerciseAngina**: Angina induzida por exercícios (Y: Sim, N: Não)
- **Oldpeak**: Depressão do segmento ST
- **ST_Slope**: Inclinação do segmento ST (Up, Flat, Down)
- **HeartDisease**: Presença de doença cardíaca (0: Não, 1: Sim)

## Processamento dos Dados
O primeiro passo do projeto é a análise exploratória e o tratamento dos dados. Isso é feito no arquivo **"Tratamento_Dados_heart"**, onde:
1. Os dados são analisados estatisticamente para detectar padrões e inconsistências.
2. Dados faltantes são tratados adequadamente.
3. O conjunto de dados limpo é salvo como **"Tratamento_Dados_heart.csv"**.

Após a preparação dos dados, passamos para o arquivo **"Importancia_var_hear"**, onde são aplicadas as seguintes técnicas de seleção de variáveis:

## Técnicas de Seleção de Variáveis
1. **Seleção K-Best**: Seleção K-Best: Método de seleção de variáveis que escolhe as k melhores características com base em testes estatísticos, como qui-quadrado (para variáveis categóricas) ou ANOVA (para variáveis numéricas), medindo a relação entre cada variável independente e a variável alvo.
2. **Regressão Logística**: Modelo estatístico que estima a probabilidade de um evento ocorrer com base nas variáveis preditoras, atribuindo coeficientes que indicam a influência de cada variável na previsão do resultado.
3. **Random Forest Feature Importance**: Mede a importância das variáveis em um modelo Random Forest analisando a redução da impureza (exemplo: Gini ou entropia) ao longo das divisões nas árvores de decisão, ou pela diminuição da acurácia ao permutar aleatoriamente os valores das variáveis.
4. **LightGBM**: Algoritmo baseado em gradient boosting que utiliza histogramas para acelerar a busca por divisões ótimas, atribuindo importância às variáveis com base no ganho de informação que elas proporcionam durante o treinamento do modelo..
5. **XGBoost**: Método avançado de gradient boosting que calcula a importância das variáveis avaliando o ganho de informação, a cobertura (quantidade de amostras impactadas) e a frequência com que cada variável é usada para dividir os nós das árvores.
6. **Boruta**: Algoritmo baseado em Random Forest que compara a importância das variáveis reais com a de variáveis sintéticas (shadow features), eliminando aquelas que não demonstram uma contribuição estatisticamente significativa na previsão do modelo.
7. **Mutual Information**: Técnica que mede a dependência estatística entre variáveis preditoras e a variável alvo, capturando relações lineares e não lineares para determinar quais variáveis carregam mais informação útil para a previsão.

## Tecnologias Utilizadas
- Python
- Pandas
- Scikit-learn
- Matplotlib
- Seaborn

## Como Executar
1. Clone este repositório:
   ```sh
   git clone https://github.com/seu-usuario/seu-repositorio.git
   ```
2. Instale as dependências:
   ```sh
   pip install -r requirements.txt
   ```
3. Execute o notebook no Jupyter Notebook ou Google Colab.

## Contribuição
Contribuições são bem-vindas! Sinta-se à vontade para abrir uma issue ou enviar um pull request.

## Licença
Este projeto está licenciado sob a MIT License.
