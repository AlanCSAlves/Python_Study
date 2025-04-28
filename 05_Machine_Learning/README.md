# Inteligência Artificial, Machine Learning e Deep Learning

## Inteligência Artificial (IA)

A Inteligência Artificial (IA) é o campo da ciência da computação que busca criar sistemas capazes de realizar tarefas que normalmente requerem inteligência humana, como raciocínio, percepção, tomada de decisão e adaptação a novas informações.  
Seu principal objetivo é **automatizar processos**, aumentar a **eficiência** e permitir que máquinas **executem funções complexas** de maneira autônoma ou semiautônoma.

---

## Machine Learning (ML)

O Machine Learning é um subcampo da IA focado no desenvolvimento de algoritmos que permitem às máquinas **aprender a partir de dados**.  
Em vez de serem explicitamente programadas para cada tarefa, as máquinas identificam padrões e **ajustam seus comportamentos** com base na experiência.

ML é o motor que impulsiona muitos dos sistemas inteligentes que usamos no dia a dia, desde filtros de spam até predições de consumo de energia.

---

## Deep Learning (DL)

O Deep Learning é uma área específica dentro do Machine Learning que se baseia em **redes neurais artificiais profundas** para aprender representações complexas de dados.  
Inspirado na estrutura do cérebro humano, o Deep Learning é capaz de realizar tarefas que exigem **interpretação avançada de informações**, como visão computacional e processamento de linguagem natural.

### Características do Deep Learning:
- Trabalha com grandes volumes de dados (Big Data).
- Aprendizado contínuo e autônomo sem necessidade intensa de intervenção humana.
- Capaz de detectar automaticamente características relevantes dos dados, sem precisar de programação explícita.

Exemplos de aplicações:
- Reconhecimento facial
- Traduções automáticas de idiomas
- Diagnóstico de imagens médicas (ex: tumores em radiografias)
- Modelos generativos (ex: criação de imagens, textos e músicas)

---

## Resumo da Relação entre IA, ML e DL

- **IA** é o conceito geral de máquinas inteligentes.
- **ML** é uma abordagem prática para alcançar IA, focada em aprendizado baseado em dados.
- **DL** é uma técnica especializada dentro do ML que utiliza redes neurais profundas para resolver problemas altamente complexos.

---

O processo de Machine Learning pode ser dividido em duas grandes vertentes:

## Machine Learning Supervisionado
- Ocorre quando possuímos uma base de dados rotulada para treinar o modelo.
- Cada entrada de dados tem um "rótulo" associado, permitindo que o algoritmo aprenda a fazer associações corretas entre inputs e outputs.
- O sistema realiza cálculos com base nos dados de entrada e define previsões para os dados de saída, comparando essas previsões com os valores reais para calcular a **função de perda** (*loss function*).

### Divisão da massa de dados:
- **80%** dos dados são utilizados para **treinamento** do modelo (*Train Data Set*).
- **20%** dos dados são utilizados para **teste** e **validação** da eficiência do modelo (*Test Data Set*).

### Exemplos de Machine Learning Supervisionado:
- Previsão do preço de imóveis (*regressão*).
- Classificação de e-mails como spam ou não spam.
- Diagnóstico médico baseado em exames clínicos.

---

## Machine Learning Não Supervisionado
- Utilizado quando não possuímos rótulos nos dados.
- O objetivo é identificar **padrões ocultos**, **agrupamentos** ou **anomalias** dentro dos dados sem supervisão humana.
- O modelo aprende por conta própria como organizar as informações, detectando **similaridades** e **diferenças** entre os exemplos.

### Exemplos de Machine Learning Não Supervisionado:
- Clusterização de clientes para campanhas de marketing.
- Detecção de anomalias em transações financeiras.
- Agrupamento de documentos por tema.

---

### Problemas comuns (precisamos evitar)

- **Underfitting:**
  - Modelo fraco, incapaz de capturar padrões dos dados.
  - Baixo desempenho tanto em treino quanto em teste.

- **Overfitting:**
  - Modelo muito ajustado ao conjunto de treino.
  - Alto desempenho em treino, mas baixo em dados novos.

**Objetivo:** Ter um modelo **robusto** e **maleável**, capaz de generalizar bem para novos dados, mesmo que não seja perfeito.

