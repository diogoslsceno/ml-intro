# 🤖 Introdução à Machine Learning

Repositório com os notebooks e exercícios práticos desenvolvidos ao longo do curso de Introdução à Machine Learning. Da regressão linear até redes neurais e PLN, tudo em Python 🐍, com scikit-learn, TensorFlow/Keras e NLTK.

## 📑 Sumário

- [Tópicos abordados](#tópicos-abordados)
- [Tecnologias utilizadas](#tecnologias-utilizadas)
- [Conteúdo do curso](#conteúdo-do-curso)
- [Requisitos de versão](#requisitos-de-versão)
- [Como executar](#como-executar)
- [Configuração do NLTK](#configuração-do-nltk)
- [Verificação das versões](#verificação-das-versões)
- [Bibliotecas principais utilizadas](#bibliotecas-principais-utilizadas)
- [Observações](#observações)
- [Estrutura geral](#estrutura-geral)

## 📚 Tópicos abordados

- ✅ Fundamentos de Machine Learning, aprendizado supervisionado x não supervisionado
- ✅ Regressão linear simples e múltipla
- ✅ Classificação binária e multiclasses
- ✅ K-Nearest Neighbors (KNN)
- ✅ Árvores de Decisão
- ✅ Clusterização, K-means, métodos hierárquicos e não hierárquicos
- ✅ Overfitting, Underfitting e Tradeoff Viés/Variância
- ✅ Redes Neurais, Perceptron, MLP e Deep Learning com TensorFlow/Keras
- ✅ Processamento de Linguagem Natural, tokenização, stopwords e TF-IDF

## 🛠️ Tecnologias utilizadas

- **Python 3.10**
- **scikit-learn** (regressão, classificação, clustering e redes neurais)
- **TensorFlow / Keras** (redes neurais e Deep Learning)
- **NLTK** (Processamento de Linguagem Natural)
- **Pandas / NumPy** (manipulação e processamento de dados)
- **SciPy** (computação científica)
- **Matplotlib** (visualização de dados)
- **Jupyter Notebook** (desenvolvimento dos notebooks)

## 🗂️ Conteúdo do curso

| Pasta | Tópico | Descrição |
| --- | --- | --- |
| `Oficina_ML/` | Regressão Linear Múltipla | Previsão de preço de carros usados com `LinearRegression`, incluindo tratamento de variáveis categóricas e separação treino/teste. |
| `MachineLearningDell/` | KNN (K-Nearest Neighbors) | Cálculo manual de distância euclidiana, classificação de frutas (`KNeighborsClassifier`) e regressão (`KNeighborsRegressor`) com o dataset Boston. |
| `DecisionsTrees/` | Árvores de Decisão | Classificação (Iris) e regressão (Boston) com `DecisionTreeClassifier`/`DecisionTreeRegressor`, controle de `max_depth` para evitar overfitting e análise de `feature_importances_`. |
| `aula3-2/` e `aula3-2Oficina/` | Clusterização (K-means) | Agrupamento de clientes de shopping (`Mall_Customers.csv`) por renda e score de gastos usando `KMeans`. |
| `mlp/` | Redes Neurais (MLP) | Implementação de um `MLPRegressor` no scikit-learn para prever preços de imóveis (Boston), ajustando camadas ocultas e número de neurônios. |
| `1-Tensorflow/` | Redes Neurais com TensorFlow/Keras | Classificação de imagens do dataset Fashion MNIST, com normalização, construção de rede sequencial (`Flatten`, `Dense`, `ReLU`, `Softmax`) e avaliação de acurácia. |
| `aula5.3/` | Processamento de Linguagem Natural (PLN) | Tokenização e remoção de stopwords com NLTK, e cálculo de relevância de termos com `TfidfVectorizer` (TF-IDF). |

## 🧩 Requisitos de versão

| Componente | Versão |
| --- | :---: |
| **Python** | **3.10.x** |
| **NumPy** | **1.23.5** |
| **SciPy** | **1.10.1** |
| **Pandas** | **1.5.3** |
| **Matplotlib** | **3.7.2** |
| **Scikit-learn** | **1.1.3** |
| **TensorFlow** | **2.13.1** |
| **Keras** | incluído no TensorFlow |
| **NLTK** | **3.10.2** |
| **Jupyter Notebook** | compatível com Python 3.10 |
| **ipykernel** | compatível com Python 3.10 |
| **pip** | versão atual |

## 🚀 Como executar

### 1️⃣ Clonar o repositório

```bash
git clone <url-do-repositorio>
cd <pasta-do-projeto>
```

### 2️⃣ Criar o ambiente virtual

O projeto utiliza um ambiente virtual Python (`.venv`) para manter as dependências isoladas do restante do sistema.

```powershell
py -3.10 -m venv .venv
```

### 3️⃣ Ativar o ambiente virtual

```powershell
.\.venv\Scripts\Activate.ps1
```

Após a ativação, o terminal deverá apresentar `(.venv)` no início da linha.

### 4️⃣ Atualizar o pip

```powershell
python -m pip install --upgrade pip
```

### 5️⃣ Instalar as dependências

```powershell
pip install numpy==1.23.5 scipy==1.10.1 pandas==1.5.3 matplotlib==3.7.2 scikit-learn==1.1.3 tensorflow==2.13.1 nltk==3.10.2 jupyter notebook ipykernel
```

### 6️⃣ Iniciar o Jupyter Notebook

```powershell
jupyter notebook
```

Navegue até a pasta do tópico desejado e execute as células.

Para verificar se o Jupyter está utilizando o ambiente virtual correto, execute dentro do notebook:

```python
import sys

print(sys.version)
print(sys.executable)
```

O caminho do Python deverá apontar para:

```text
.venv\Scripts\python.exe
```

## 🗣️ Configuração do NLTK

O NLTK utiliza alguns recursos adicionais para processamento de linguagem natural. Eles devem ser baixados após a instalação da biblioteca, no próprio Jupyter Notebook:

```python
import nltk

nltk.download('stopwords')
nltk.download('punkt')
nltk.download('punkt_tab')
```

Os recursos utilizados nos notebooks incluem:

- `stopwords`: identificação de palavras sem relevância semântica para determinadas tarefas.
- `punkt`: tokenização de textos.
- `punkt_tab`: recurso utilizado pelas versões atuais do NLTK na tokenização.

## 🔍 Verificação das versões

Para verificar se as principais bibliotecas foram instaladas corretamente:

```powershell
python -c "import sys,numpy,pandas,scipy,sklearn,tensorflow,nltk; print('Python:',sys.version.split()[0]); print('NumPy:',numpy.__version__); print('Pandas:',pandas.__version__); print('SciPy:',scipy.__version__); print('Scikit-learn:',sklearn.__version__); print('TensorFlow:',tensorflow.__version__); print('Keras:',tensorflow.keras.__version__); print('NLTK:',nltk.__version__)"
```

O ambiente deverá apresentar versões compatíveis com as especificadas na seção [Requisitos de versão](#requisitos-de-versão).

## 📦 Bibliotecas principais utilizadas

### 🔢 NumPy

Utilizado para manipulação de arrays, operações matemáticas e processamento numérico.

```python
import numpy as np
```

### 🐼 Pandas

Utilizado para manipulação de dados e criação de DataFrames.

```python
import pandas as pd
```

### 📊 Matplotlib

Utilizado para visualização gráfica dos dados e resultados.

```python
import matplotlib.pyplot as plt
```

### 🧠 Scikit-learn

Utilizado em diferentes etapas do curso, incluindo:

- Regressão Linear
- KNN
- Árvores de Decisão
- K-means
- MLP
- Pré-processamento
- Separação entre treino e teste
- Métricas de avaliação

Exemplo:

```python
from sklearn.feature_extraction.text import TfidfVectorizer
```

### 🔶 TensorFlow / Keras

Utilizado na construção e treinamento de redes neurais. Não é necessário instalar o Keras separadamente, ele já vem integrado ao TensorFlow.

```python
import tensorflow as tf
from tensorflow import keras
```

O TensorFlow é utilizado principalmente na construção e treinamento de redes neurais, incluindo a classificação do dataset Fashion MNIST.

### 💬 NLTK

Utilizado no Processamento de Linguagem Natural.

```python
import nltk

nltk.download('stopwords')
nltk.download('punkt')
nltk.download('punkt_tab')
```

### 🧮 SciPy

Utilizado como biblioteca de computação científica e como dependência de ferramentas utilizadas no curso.

## ⚠️ Observações

### 🖥️ TensorFlow no Windows

O TensorFlow utilizado neste projeto funciona em CPU no Windows nativamente. O aviso relacionado à ausência de suporte à GPU em versões recentes do TensorFlow no Windows não impede a execução dos notebooks.

### 🔄 API atual do Scikit-learn

Para obter os nomes das características utilizadas pelo `TfidfVectorizer`, utilize a API atual:

```python
nomes = tf_idf.get_feature_names_out()
```

em vez da API antiga:

```python
nomes = tf_idf.get_feature_names()
```

Para converter uma matriz esparsa em uma matriz NumPy:

```python
vetor = vetor.toarray()
```

## 🌳 Estrutura geral

```text
IntroducaoMachineLearningDell/
│
├── Oficina_ML/
├── MachineLearningDell/
├── DecisionsTrees/
├── aula3-2/
├── aula3-2Oficina/
├── mlp/
├── 1-Tensorflow/
├── aula5.3/
│
├── .venv/
└── README.md
```

> 🚫 O diretório `.venv/` deve permanecer apenas no ambiente local e não deve ser enviado para o GitHub.

---

Projeto desenvolvido como parte do curso de Introdução à Machine Learning, reunindo exercícios, oficinas e notebooks práticos desenvolvidos ao longo das aulas.
