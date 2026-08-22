# 🍷 Previsão e Classificação da Qualidade de Vinhos com Machine Learning

Projeto de Análise de Dados e Aprendizado de Máquina focado no estudo das propriedades físico-químicas de vinhos e na construção de um modelo preditivo para a avaliação da sua qualidade.

---

## 📌 Visão Geral do Projeto

Este projeto aborda o ciclo completo de Ciência de Dados, desde a ingestão, limpeza e Análise Exploratória de Dados (EDA) até o desenvolvimento, ajuste e avaliação de um modelo de classificação utilizando o algoritmo 

O objetivo principal é entender quais fatores químico-físicos mais influenciam a percepção de qualidade de um vinho e automatizar a classificação de novas amostras (vinhos inéditos) com alta precisão e sensibilidade.

---

## 🔬 Metodologia e Etapas do Pipeline

1. **Ingestão e Limpeza dos Dados**:
   - Inspeção de tipos de dados e tratamento de inconsistências ou valores nulos.
   - Verificação e remoção de registros duplicados.

2. **Análise Exploratória de Dados (EDA)**:
   - Análise de distribuições estatísticas das variáveis físico-químicas (acidez, pH, teor alcoólico, açúcar residual, sulfatos, etc.).
   - Estudo de correlações através de matrizes de calor (*heatmaps*).
   - Identificação do desbalanceamento das notas de qualidade originais.

3. **Engenharia de Recursos (Feature Engineering)**:
   - Transformação do target contínuo/discreto em uma variável binária categórica (ex.: *Vinho de Alta Qualidade* vs. *Vinho Comum/Baixo*).
   - Normalização e padronização das feutures para modelagem.

4. **Tratamento de Desbalanceamento & Divisão de Treino/Teste**:
   - Divisão dos dados em conjuntos de treino e teste (`train_test_split`) mantendo a proporção de classes.
   - Mitigação do desbalanceamento.

5. **Modelagem Preditiva**:
   - Treinamento dos classificador.
   - Ajuste de hiperparâmetros para otimização de métricas de desempenho.

6. **Avaliação do Modelo**:
   - Cálculo de métricas: **Acurácia, Precisão, Recall, F1-Score e ROC-AUC**.
   - Construção e visualização da **Matriz de Confusão**.
   - Análise do gráfico de **Importância de Variáveis (Feature Importance)** para interpretar os decisores do modelo.

7. **Simulação e Inferência**:
   - Pipeline preparado para receber dados de vinhos inéditos e realizar previsões em tempo de execução.

---

## 🛠️ Tecnologias e Bibliotecas Utilizadas

- **Linguagem**: Python
- **Manipulação de Dados**: `pandas`, `numpy`
- **Visualização de Dados**: `matplotlib`, `seaborn`
- **Machine Learning**: `scikit-learn`, `xgboost`, `Random Forest` , `KNN (K-Nearest Neighbors)`
- **Ambiente**: Jupyter Notebook / VS Code / Google Colab

---

## 📁 Estrutura do Repositório

```text
.
├── data/                  # Conjuntos de dados brutos e processados
├── notebooks/             # Notebooks Jupyter com EDA e experimentos
├── models/                # Artefatos do modelo treinado (.pkl / .json)
├── src/                   # Scripts Python de suporte (pipelines)
├── requirements.txt       # Lista de dependências do projeto
└── README.md              # Documentação principal do projeto
```

---

## 🚀 Como Executar o Projeto

### 1. Clonar o Repositório
```bash
git clone https://github.com/usuario/previsao-qualidade-vinhos.git
cd previsao-qualidade-vinhos
```

### 2. Criar e Ativar o Ambiente Virtual

Em Linux/macOS:
```bash
python3 -m venv venv
source venv/bin/activate
```

Em Windows:
```bash
python -m venv venv
venv\Scripts\activate
```

### 3. Instalar as Dependências
```bash
pip install -r requirements.txt
```

### 4. Executar os Notebooks
Inicie o Jupyter Lab ou Notebook para acompanhar a análise e a modelagem:
```bash
jupyter notebook
```

---

## 📊 Principais Insights do Projeto

- **Teor Alcoólico e Acidez Volátil**: Mostraram-se entre os fatores de maior peso na determinação da qualidade do vinho.
- **Tratamento do Desbalanceamento**: O ajuste do `scale_pos_weight` foi essencial para que o modelo não negligenciasse a classe minoritária de alta qualidade.
- **Performance do XGBoost**: Apresentou excelente capacidade de generalização e separabilidade entre as classes na matriz de confusão.

---

## ✍️ Autoria

Desenvolvido pelos alunos da Pós-Tech da FIAP em Data Analytics, como parte dos estudos avançados e aplicação prática de Ciência de Dados e Machine Learning.

João Pedro Henriques Machado
LinkedIn: https://www.linkedin.com/in/jo%C3%A3o-pedro-henriques-b784161b6/

Lucas Freitas
LinkedIn: https://www.linkedin.com/in/lucas-freitas-chaves/

Douglas Silva
LinkedIn: https://www.linkedin.com/in/douglas-souto-55880b225/

Alexandre Costa

Erick

