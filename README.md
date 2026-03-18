# 🤖 Classificação de Espécies Iris - Machine Learning

Este repositório contém um projeto completo de ciência de dados aplicado ao clássico [Iris Species Dataset](https://www.kaggle.com/datasets/uciml/iris/data). O objetivo é explorar as características morfológicas das flores e desenvolver modelos de aprendizagem automática capazes de classificar as espécies com precisão.

## 📊 Visão Geral do Projeto

O projeto está estruturado em etapas que cobrem desde a análise estatística inicial até a implementação de pipelines de machine learning robustos. Foram analisadas três espécies: *Iris-setosa*, *Iris-versicolor* e *Iris-virginica*.

### Estrutura dos Notebooks
* **`01_gd_eda.ipynb`**: Análise Exploratória de Dados (EDA). Focado em limpeza, estatística descritiva e visualizações para entender o comportamento das variáveis.
* **`02_gd_modelos.ipynb`**: Experimentação inicial de modelos de classificação e avaliação de fronteiras de decisão.
* **`02_gd_modelos_parte_02.ipynb`**: Refinamento da abordagem utilizando técnicas avançadas como padronização, validação cruzada estratificada e pipelines.

## 📈 Análise Exploratória (EDA)
Principais descobertas:
* **Balanceamento:** O conjunto de dados possui 50 amostras para cada classe, eliminando a necessidade de técnicas de reamostragem.
* **Separação Linear:** A espécie *Iris-setosa* apresenta características únicas (especialmente no tamanho das pétalas) que permitem a sua separação clara das demais.
* **Correlações:** Identificou-se uma forte correlação entre o comprimento e a largura da pétala, sendo estes os atributos mais importantes para a classificação.

## ⚙️ Modelagem e Resultados

Para garantir a fiabilidade dos resultados, a modelagem seguiu as melhores práticas da área:

### Metodologia
1. **Pré-processamento:** Escalonamento de atributos com `StandardScaler` e codificação de labels com `LabelEncoder`.
2. **Validação:** Implementação de `StratifiedKFold` para garantir que todas as classes estivessem representadas em cada fold da validação.
3. **Robustez:** Uso de `Pipeline` do Scikit-Learn para evitar o vazamento de dados durante o treino.

### Desempenho dos Modelos
Foram comparados modelos de base (*baseline*) com modelos lineares otimizados:

| Modelo | Acurácia Média (CV) | F1-Score (Weighted) |
| :--- | :---: | :---: |
| **Logistic Regression** | **95.3%** | **0.95** |
| Dummy Classifier | 34.0% | 0.33 |

O modelo de **Regressão Logística** demonstrou um excelente poder preditivo, sendo uma solução eficaz e interpretável para este problema.

## 🛠️ Tecnologias Utilizadas
* **Python**
* **Bibliotecas de Dados:** Pandas, NumPy.
* **Visualização:** Matplotlib, Seaborn.
* **Machine Learning:** Scikit-Learn.

---

## Organização do projeto

```
├── .gitignore         <- Arquivos e diretórios a serem ignorados pelo Git
├── IrisSpecies.yml       <- O arquivo de requisitos para reproduzir o ambiente de análise
├── LICENSE            <- Licença de código aberto se uma for escolhida
├── README.md          <- README principal para desenvolvedores que usam este projeto.
|
├── dados              <- Arquivos de dados para o projeto.
|
├── modelos            <- Modelos treinados e serializados, previsões de modelos ou resumos de modelos
|
├── notebooks          <- Cadernos Jupyter. A convenção de nomenclatura é um número (para ordenação),
│                         as iniciais do criador e uma descrição curta separada por `-`, por exemplo
│                         `01-fb-exploracao-inicial-de-dados`.
│
|   └──src             <- Código-fonte para uso neste projeto.
|      │
|      ├── __init__.py  <- Torna um módulo Python
|      ├── config.py    <- Configurações básicas do projeto
|      └── graficos.py  <- Scripts para criar visualizações exploratórias e orientadas a resultados
|
├── referencias        <- Dicionários de dados, manuais e todos os outros materiais explicativos.
|
├── relatorios         <- Análises geradas em HTML, PDF, LaTeX, etc.
│   └── imagens        <- Gráficos e figuras gerados para serem usados em relatórios
```
