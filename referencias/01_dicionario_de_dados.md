# 📖 Dicionário de Dados - Iris Species Dataset

Este documento descreve as variáveis presentes no conjunto de dados original utilizado para a análise e treinamento dos modelos neste projeto.

A base de dados contém 150 amostras de flores da planta *Iris*, divididas igualmente entre três espécies. Para cada amostra, foram registradas quatro características morfológicas (em centímetros).

## 🗂️ Estrutura das Variáveis

| Variável | Tipo de Dado | Descrição |
| :--- | :--- | :--- |
| **`Id`** | Numérico (Int) | Identificador único sequencial para cada amostra da base de dados. (Geralmente removido durante a modelagem, pois não possui valor preditivo). |
| **`SepalLengthCm`** | Numérico (Float) | Comprimento da sépala da flor, medido em centímetros. |
| **`SepalWidthCm`** | Numérico (Float) | Largura da sépala da flor, medida em centímetros. |
| **`PetalLengthCm`** | Numérico (Float) | Comprimento da pétala da flor, medido em centímetros. |
| **`PetalWidthCm`** | Numérico (Float) | Largura da pétala da flor, medida em centímetros. *(Nota: Esta foi a variável identificada com maior importância preditiva no modelo final do projeto).* |
| **`Species`** | Categórico (String) | A espécie da flor de Iris à qual a amostra pertence. Esta é a nossa **variável alvo (target)**. |

## 🎯 Variável Alvo (`Species`)

A variável dependente que os modelos de *Machine Learning* buscam prever possui três classes possíveis. O dataset é perfeitamente balanceado, contendo 50 registros de cada classe:

1. `Iris-setosa`
2. `Iris-versicolor`
3. `Iris-virginica`

---
*Fonte dos dados: [Kaggle - Iris Species Dataset](https://www.kaggle.com/datasets/uciml/iris/data)*
