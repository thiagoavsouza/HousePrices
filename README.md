# House Prices – Advanced Regression Techniques

Projeto de **Machine Learning** desenvolvido a partir da competição *House Prices – Advanced Regression Techniques* do Kaggle, com foco em **modelagem preditiva, boas práticas de pipeline e comparação de modelos** para estimativa do preço de imóveis.

O projeto apresenta a **evolução de um baseline simples até uma solução avançada**, utilizando técnicas amplamente aplicadas no mercado financeiro, segurador e em projetos reais de dados.

---

## Objetivo

Prever o preço de venda de imóveis (`SalePrice`) com o menor erro possível, utilizando dados tabulares com variáveis numéricas e categóricas, aplicando:

- Análise exploratória orientada a modelo (EDA)
- Tratamento adequado de valores ausentes
- Engenharia de features
- Pipelines de pré-processamento
- Modelos de Gradient Boosting
- Ensemble de modelos

---

## Evolução do Projeto

### Versão 1 – Baseline
**Notebook:** `01_Baseline_Linear_Regression.ipynb`

Modelos utilizados:
- Regressão Linear
- Árvore de Regressão
- KNeighborsRegressor (KNN)

Características:
- Uso majoritário de variáveis numéricas
- Remoção de colunas com alta proporção de valores nulos
- Pré-processamento manual (sem pipeline)
- Comparação inicial entre diferentes algoritmos clássicos

**Kaggle Score:** ~0.25

Objetivo desta versão foi criar um **baseline inicial** e entender o comportamento dos dados e dos modelos mais simples.

---

### Versão 2 – Pipeline + Gradient Boosting + Ensemble
**Notebook:** `02_Pipeline_Gradient_Boosting_Ensemble.ipynb`

Principais melhorias:
- EDA completo orientado à performance do modelo
- Tratamento de valores ausentes:
  - Numéricos → mediana
  - Categóricos → `"None"`
- Codificação de variáveis categóricas (One-Hot Encoding)
- Criação de features (idade do imóvel, área total, etc.)
- Pipeline completo de pré-processamento (evitando vazamento de dados)

Modelos utilizados:
- LightGBM
- XGBoost
- CatBoost

Avaliação:
- Validação cruzada (RMSE no log do preço)
- Comparação justa entre modelos
- Ensemble (média) entre CatBoost e XGBoost

**Kaggle Score:** **0.12843**  
**Posição no leaderboard:** ~1491 (**Top ~15%**)

Essa versão representa uma abordagem **próxima à prática profissional**, focada em generalização, robustez e performance.

---

## Métrica de Avaliação

A métrica utilizada é a mesma da competição:

- **RMSE aplicado ao log do SalePrice**

O uso do log:
- Reduz o impacto de outliers
- Melhora a estabilidade do modelo
- Alinha diretamente com o critério oficial do Kaggle

---

## Tecnologias e Bibliotecas

- Python
- pandas
- numpy
- scikit-learn
- LightGBM
- XGBoost
- CatBoost

---

## Contato

E-mail: **thiago.a.v.souza@gmail.com**\
LinkedIn: **https://www.linkedin.com/in/thiagoavsouza/**
