# Machine Learning Não Supervisionado

Quando não possuímos uma base rotulada para realizar o treinamento do modelo, o modelo por si só deve encontrar padrões e similaridades para realizar as análises. Através da detecção de anomalias, o algoritmo observa os aspectos e classifica as respostas de acordo com as similaridades.

## Principais Modelos de Machine Learning Não Supervisionado

### Clusterização
Agrupamento de dados em categorias semelhantes, identificando padrões ocultos.

**Tipos de Clusterização:**
- **Clusterização Exclusiva (Exclusive Clustering):** Um agente pertence apenas a uma categoria.
- **Clusterização Sobreposta (Overlapping Clustering):** Um agente pode pertencer a várias categorias simultaneamente.
- **Clusterização Hierárquica (Hierarchical Clustering):** Os dados são agrupados em uma estrutura de hierarquia de grupos.

**Exemplos de aplicação:**
- Segmentação de clientes.
- Agrupamento de documentos.
- Análise de redes sociais.

### Modelo de Recomendação
O algoritmo detecta padrões de comportamento dos usuários e sugere conteúdos relevantes.

**Técnicas principais:**

- **Content-Based Filtering (Filtro Baseado em Conteúdo):**
  - O sistema analisa o perfil de consumo do usuário (User Rating x Matriz de Categoria de Produtos).
  - As recomendações são baseadas apenas nas interações prévias do usuário.
  - Limitação: tende a recomendar apenas o que já foi consumido, sem novidades.

- **Collaborative Filtering (Filtro Colaborativo):**
  - Utiliza as interações de diversos usuários semelhantes para gerar recomendações.
  - Permite recomendar itens novos que usuários similares também gostaram.
  - Desafio: pode apresentar dificuldades de escalabilidade devido à complexidade do cálculo de similaridade.

- **Modelo Híbrido:**
  - Combina Content-Based e Collaborative Filtering para obter o melhor dos dois mundos.
  - Aumenta a diversidade e qualidade das recomendações.

## Métricas de Avaliação

As métricas variam bastante conforme o tipo de análise.

### Para Clusterização

- **Silhouette Score:**
  - Mede o quão semelhantes os objetos são aos seus próprios clusters em comparação com outros clusters.
  - **A** = É a distância média entre o ponto em análise e todos os outros pontos do mesmo cluster.
  - Quanto menor o valor de A, mais próximo o ponto está do seu grupo — o que é bom.
  - **B** = É a distância média entre o ponto e os pontos do cluster mais próximo (aquele que não é o seu próprio cluster, mas é o mais similar).
  - Quanto maior B, melhor, pois significa que o ponto está longe de outros grupos.
    
  - **Fórmula:**
    ```
    Silhouette = (B - A) / max(A, B)
    ```
  - Próximo de 1: O ponto está bem agrupado com seu cluster e bem separado dos outros — ótimo agrupamento.

  - Próximo de 0: O ponto está na fronteira entre dois clusters — pode ser ambíguo.

  - Próximo de -1: O ponto foi agrupado no cluster errado — mau agrupamento.

### Para Recomendadores

- **MRR (Mean Reciprocal Rank):**
  - Mede a precisão baseada na posição da primeira resposta relevante, ou seja, a métrica avalia quão cedo (em termos de posição na lista de recomendações) o sistema consegue apresentar uma resposta correta ou relevante.

- **MAP (Mean Average Precision):**
  - Avalia a precisão média considerando a relevância dos itens em toda a lista de recomendações, ou seja, ela mede a precisão média de uma lista de recomendações inteira, considerando todos os itens relevantes, não apenas o primeiro.
