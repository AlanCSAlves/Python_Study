### Métricas de Avaliação de Modelos de Regressão

- **R² (R Square):** Mede o quanto o modelo consegue se ajustar às mudanças das variáveis de entrada.
  - Muito abaixo de 1: Indica *underfitting*.
  - Muito próximo ou igual a 1: Indica *overfitting*.
- **Adjusted R²:** Penaliza o modelo para evitar que ele se ajuste excessivamente aos dados de treino.
- **MSE (Mean Squared Error):** Média dos erros ao quadrado.
- **RMSE (Root Mean Squared Error):** Raiz quadrada do MSE, para facilitar a interpretação.
- **MAE (Mean Absolute Error):** Média absoluta dos erros, tratando todos igualmente.

#### Quando usar cada métrica
- **R² / Adjusted R²:** Para apresentação de resultados de maneira interpretável.
- **MSE/RMSE/MAE:** Para avaliação e comparação da performance entre diferentes modelos.
  - **MSE/RMSE:** Penalizam erros maiores.
  - **MAE:** Menos sensível a grandes erros.
