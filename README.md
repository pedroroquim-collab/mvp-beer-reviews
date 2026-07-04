# MVP — Predição de Avaliação de Cervejas 🍺

MVP de Machine Learning & Analytics: predição da avaliação geral de cervejas
(dataset Beer Reviews / BeerAdvocate) a partir de características sensoriais e
teor alcoólico, utilizando modelos de regressão e análise não supervisionada
(PCA e K-Means).

## Notebook

▶️ [Abrir no Google Colab](https://colab.research.google.com/drive/1ceObKtabAbhBvFhyQ-l7uIuN80yDAgtj?usp=sharing)

O notebook também está disponível neste repositório:
[`MVP_PREDIÇÃO_DE_AVALIAÇÃO_DE_CERVEJAS.ipynb`](./MVP_PREDIÇÃO_DE_AVALIAÇÃO_DE_CERVEJAS.ipynb)

## Dataset

- **Fonte original:** [Beer Reviews — Kaggle](https://www.kaggle.com/datasets/rdoume/beerreviews) (BeerAdvocate)
- **Hospedagem para reprodutibilidade:** arquivo compactado (gzip, ~26 MB) na
  [Release v1.0](https://github.com/pedroroquim-collab/mvp-beer-reviews/releases/tag/v1.0),
  carregado diretamente pelo notebook via URL pública
- 1.586.614 registros e 13 atributos (amostra de 300 mil utilizada na modelagem)

## Resumo dos resultados

- **Problema:** regressão — prever `review_overall` (escala 0–5)
- **Baseline:** DummyRegressor (média)
- **Modelos comparados:** Regressão Linear, KNN, Árvore de Decisão e Random Forest
- **Melhor modelo:** Random Forest otimizada via GridSearchCV
  (`n_estimators=200`, `max_depth=10`) — **R² = 0,6838** no conjunto de teste
- **Análise complementar:** PCA (77,6% da variância em 2 componentes) e
  K-Means com 4 clusters (Silhouette ≈ 0,36)
- **Tempo de execução:** ~23 minutos no Google Colab gratuito (CPU)
