### Métricas de Avaliação de Modelos de Classificação

Antes de aplicar as métricas, é importante entender a **Matriz de Confusão**:

- **Verdadeiro Positivo (VP):** Predito positivo e é positivo.
- **Verdadeiro Negativo (VN):** Predito negativo e é negativo.
- **Falso Positivo (FP):** Predito positivo e é negativo.
- **Falso Negativo (FN):** Predito negativo e é positivo.

### Principais métricas:

- **Acurácia:**
  \[ \text{Acurácia} = \frac{VP + VN}{\text{Total de Amostras}} \]
  - Mede a porcentagem de classificações corretas.

- **Precisão:**
  \[ \text{Precisão} = \frac{VP}{VP + FP} \]
  - Foco em minimizar falsos positivos.

- **Recall:**
  \[ \text{Recall} = \frac{VP}{VP + FN} \]
  - Foco em minimizar falsos negativos.

- **F1 Score:**
  \[ \text{F1} = 2 \times \frac{\text{Precisão} \times \text{Recall}}{\text{Precisão} + \text{Recall}} \]
  - Balanceia Precisão e Recall.

### Validação de Modelos: K-Fold Cross Validation

- O conjunto de dados é dividido em "K" partes iguais.
- Cada parte é usada como conjunto de teste enquanto as outras (K-1) são usadas para treino.
- O processo se repete K vezes.
- Os resultados são combinados para uma avaliação final mais robusta.

**Exemplo de divisão em 4 partes:**

| Rodada | Parte 1 | Parte 2 | Parte 3 | Parte 4 |
|:------:|:-------:|:-------:|:-------:|:-------:|
| 1      | Teste   | Treino  | Treino  | Treino  |
| 2      | Treino  | Teste   | Treino  | Treino  |
| 3      | Treino  | Treino  | Teste   | Treino  |
| 4      | Treino  | Treino  | Treino  | Teste   |
