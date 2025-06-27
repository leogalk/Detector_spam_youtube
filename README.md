# Detector_spam_youtube
Classificação binária de comentários no youtube como spam ou "ham" com algoritmos supervisionados.


📝 Descrição do Projeto
Este projeto implementa uma solução completa de detecção de spam em comentários do YouTube utilizando técnicas de Machine Learning. O objetivo é classificar comentários como SPAM ou HAM (não-spam) através da comparação de diferentes algoritmos de aprendizado supervisionado.
🎬 Dataset
O projeto utiliza o YouTube Spam Collection Dataset, que contém:

1.956 comentários reais extraídos de 5 vídeos populares do YouTube
5 datasets separados por artista/vídeo:

Youtube01-Psy.csv (350 comentários)
Youtube02-KatyPerry.csv (350 comentários)
Youtube03-LMFAO.csv (438 comentários)
Youtube04-Eminem.csv (448 comentários)
Youtube05-Shakira.csv (370 comentários)



Estrutura dos Dados
ColunaTipoDescriçãoCOMMENT_IDIDIdentificador único do comentárioAUTHORCategoricalAutor do comentárioDATECategoricalData do comentárioCONTENTTextConteúdo textual do comentárioCLASSBinaryClasse target (0=HAM, 1=SPAM)
🚀 Como Executar no Google Colab
1. Preparação dos Dados

Faça o download dos arquivos CSV do dataset do repositório
No Google Colab, faça upload dos 5 arquivos CSV:

Youtube01-Psy.csv
Youtube02-KatyPerry.csv
Youtube03-LMFAO.csv
Youtube04-Eminem.csv
Youtube05-Shakira.csv



2. Execução do Código

Abra o notebook YouTube_Spam_Detection.ipynb no Google Colab
Execute as células sequencialmente
O código automaticamente:

Carregará e concatenará todos os datasets
Realizará a análise exploratória
Treinará os modelos de ML
Comparará os resultados



🔬 Metodologia Implementada
1. Análise Exploratória de Dados (EDA)

Distribuição das classes por vídeo
Análise do comprimento dos comentários
Identificação de padrões entre SPAM e HAM
Visualizações interativas

2. Pré-processamento de Texto

Limpeza textual (remoção de pontuação, números, normalização)
Extração de features com TF-IDF
Análise das palavras mais discriminativas

3. Estratégia de Divisão dos Dados

Divisão por vídeo para evitar data leakage
4 vídeos para treino + 1 vídeo para teste
Validação cruzada estratificada

4. Algoritmos de Machine Learning
Implementação e otimização de 3 algoritmos:

XGBoost - Gradient Boosting otimizado
Random Forest - Ensemble de árvores de decisão
Support Vector Machine (SVM) - Classificação por margem máxima

5. Avaliação e Comparação

Métricas: Accuracy, Precision, Recall, F1-Score, AUC-ROC
Grid Search para otimização de hiperparâmetros
Visualizações comparativas (ROC curves, matriz de confusão)

6. Redução de Dimensionalidade

Aplicação de técnicas (PCA, t-SNE, UMAP)
Análise do impacto na performance
Comparação antes/depois da redução

📊 Principais Features do Código
🎨 Visualizações Incluídas

Distribuição de classes por vídeo
Análise do comprimento dos comentários
Top features mais discriminativas
Curvas ROC comparativas
Matrizes de confusão
Gráficos de comparação de performance

⚙️ Configurações Técnicas

TF-IDF Vectorizer: max_features=5000, n-grams(1,2), stop_words='english'
Validação Cruzada: 5-fold estratificada
Grid Search: Otimização automática de hiperparâmetros
Métricas: Foco em F1-Score para dados balanceados

📁 Estrutura do Repositório
├── datasets/
│   ├── Youtube01-Psy.csv
│   ├── Youtube02-KatyPerry.csv
│   ├── Youtube03-LMFAO.csv
│   ├── Youtube04-Eminem.csv
│   └── Youtube05-Shakira.csv
├── YouTube_Spam_Detection.ipynb
└── README.md
🎯 Resultados Esperados
O projeto gera uma análise completa comparando os três algoritmos, identificando o modelo com melhor performance baseado em F1-Score, e fornece insights sobre:

Padrões de spam em comentários do YouTube
Eficácia de diferentes algoritmos para classificação de texto
Impacto da redução de dimensionalidade na performance

🛠️ Dependências
pythonpandas
numpy
matplotlib
seaborn
scikit-learn
xgboost
scipy
👤 Autor
Leonardo Correia Santos Galvão
Projeto desenvolvido como trabalho final da disciplina de Inteligência Artificial, focado na aplicação prática de algoritmos de Machine Learning para solução de problemas reais.
