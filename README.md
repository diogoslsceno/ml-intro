# Introdução à Machine Learning

Repositório com os notebooks e exercícios práticos desenvolvidos ao longo do curso de Introdução à Machine Learning. O conteúdo cobre desde os fundamentos do aprendizado supervisionado e não supervisionado até redes neurais e Processamento de Linguagem Natural (PLN), utilizando Python, scikit-learn, TensorFlow/Keras e NLTK.

## Tópicos abordados

- Fundamentos de Machine Learning (aprendizado supervisionado x não supervisionado)
- Regressão linear simples e múltipla
- Classificação binária e multiclasses
- K-Nearest Neighbors (KNN)
- Árvores de Decisão
- Clusterização (K-means, métodos hierárquicos e não hierárquicos)
- Overfitting, Underfitting e Tradeoff Viés/Variância
- Redes Neurais (Perceptron, MLP) e Deep Learning com TensorFlow/Keras
- Processamento de Linguagem Natural (Tokenização, Stopwords, TF-IDF)

## Tecnologias utilizadas

- **scikit-learn** (regressão, classificação, clustering, redes neurais)
- **TensorFlow / Keras** (redes neurais profundas)
- **NLTK** (Processamento de Linguagem Natural)
- **Pandas / NumPy** (manipulação de dados)
- **Matplotlib** (visualização de dados)

## Conteúdo do curso

| Pasta | Tópico | Descrição |
|---|---|---|
| `Oficina_ML/` | Regressão Linear Múltipla | Previsão de preço de carros usados com `LinearRegression`, incluindo tratamento de variáveis categóricas e separação treino/teste. |
| `MachineLearningDell/` | KNN (K-Nearest Neighbors) | Cálculo manual de distância euclidiana, classificação de frutas (`KNeighborsClassifier`) e regressão (`KNeighborsRegressor`) com o dataset Boston. |
| `DecisionsTrees/` | Árvores de Decisão | Classificação (Iris) e regressão (Boston) com `DecisionTreeClassifier`/`DecisionTreeRegressor`, controle de `max_depth` para evitar overfitting e análise de `feature_importances_`. |
| `aula3-2/` e `aula3-2Oficina/` | Clusterização (K-means) | Agrupamento de clientes de shopping (`Mall_Customers.csv`) por renda e score de gastos usando `KMeans`. |
| `mlp/` | Redes Neurais (MLP) | Implementação de um `MLPRegressor` no scikit-learn para prever preços de imóveis (Boston), ajustando camadas ocultas e número de neurônios. |
| `1-Tensorflow/` | Redes Neurais com TensorFlow/Keras | Classificação de imagens do dataset Fashion MNIST, com normalização, construção de rede sequencial (`Flatten`, `Dense`, `ReLU`, `Softmax`) e avaliação de acurácia. |
| `aula5.3/` | Processamento de Linguagem Natural (PLN) | Tokenização e remoção de stopwords com NLTK, e cálculo de relevância de termos com `TfidfVectorizer` (TF-IDF). |

## Requisitos de versão

| Componente | Versão |
| --- | ---: |
| **Python** | **3.10.x** |
| **Jupyter Notebook** | versão atual compatível |
| **TensorFlow** | **2.x** |
| **Keras** | incluído no TensorFlow |
| **NumPy** | versão compatível com TensorFlow |
| **Pandas** | versão atual compatível |
| **Scikit-learn** | versão atual |
| **NLTK** | **3.10.2** |
| **Matplotlib** | versão atual |
| **pip** | pode ser atualizado |

## Como executar

1. Clone o repositório:
   ```bash
   git clone <url-do-repositorio>
   ```
2. Certifique-se de estar usando **Python 3.10.x** e instale as dependências necessárias (recomenda-se um ambiente virtual):
   ```bash
   pip install --upgrade pip
   pip install scikit-learn "tensorflow>=2.0,<3.0" "nltk==3.10.2" pandas numpy matplotlib jupyter
   ```
3. Abra os notebooks com Jupyter:
   ```bash
   jupyter notebook
   ```
4. Navegue até a pasta do tópico desejado e execute as células.

---

Projeto desenvolvido como parte do curso de Introdução à Machine Learning.
