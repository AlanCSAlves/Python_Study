# Processamento de Linguagem Natural (NLP) e Processamento de Áudio

## NLP - Processamento de Linguagem Natural
Permite que máquinas interpretem, analisem e gerem texto de forma inteligente. Pode ser implementado on‑premises ou na nuvem, utilizando bibliotecas especializadas.

### Aplicações Comuns
- **Análise de Sentimento**: polaridade de opiniões em redes sociais ou avaliações.
- **Tradução Automática**: ferramentas como Google Translate ou modelos Transformers.
- **Classificação de Texto**: spam vs. não spam, categorias de notícias.
- **Extração de Entidades Nomeadas (NER)**: identificação de pessoas, organizações, datas.
- **Outras**: resumo automático, resposta a perguntas (QA), geração de texto.

### Bibliotecas e Serviços Populares
- **Python**: spaCy, NLTK, Gensim, Hugging Face Transformers.
- **Cloud**: AWS Comprehend, Google Cloud NLP, Azure Cognitive Services.

---

## Pré‑processamento de Texto
Passos padrão para limpar e estruturar dados textuais antes de alimentar modelos.

1. **Tokenização**: separar texto em palavras ou sentenças.
- Analisando por palavra = **Eu sou o negro**
- Aplicando a Tokenização = ArrayFrase = ['Eu','sou', 'o','negro'] - **Cada palavra é um token**.

- Analisando por frase = **Eu sou negro, porque nasci negro. Meus pais são negros**.
- Aplicando a Tokenização = ArrayTexto = ['Eu sou negro', 'porque nasci negro.' , 'Meus pais são negros.'] - **Cada frase é um token**.

 
3. **Remoção de Stopwords**: eliminar palavras sem peso semântico (artigos, preposições).
4. **Stemming vs. Lemmatização**:
   - **Stemming**: reduz ao radical bruto (`colaboradores` → `colaborad`).
   - **Lemmatização**: retorna forma canônica (`colaboradoras` → `colaboradora`).
5. **Lowercasing / Uppercasing**: uniformizar caixa (todo em MAIÚSCULO, ou em minúsculo).
6. **Remoção de Ruído**: URLs, números, pontuação.
7. **POS Tagging e Parsing** (opcional): extrair estrutura gramatical.
8. **Word Embeddings**: representar tokens como vetores (Word2Vec, FastText, GloVe, Transformers).

> **Dica:** escolha as etapas conforme o objetivo: classificação simples requer menos limpeza; geração de texto ou NER exige pipelines mais completos.

---

## NLC - Classificação de Texto (Natural Language Classification)
Treina-se um modelo para atribuir um *rótulo* a cada texto de entrada.

1. Coleta e rotulagem do *dataset*.
2. Pré‑processamento.
3. Treinamento (ex.: Naive Bayes, SVM, BERT).
4. Avaliação (Acurácia, Precision, Recall, F1-Score).

**Exemplo de classes**:
O treinamento de classificação é aplicado e são definidas as seguintes classes:.
- Classe A: peso 99.5–100
- Classe B: peso 70–80
- Classe C: peso 19–20

- É feito o input das informações de modo que o faça a depuração da frase, a fim de atribuir um valor para cada um de seus elementos, o que permite que a frase possua um peso de 85 por exemplo.
- A Classificação é feita com base na aproximação entre os valores das classes, de modo que seja definida pelo valor que mais se aproxima na escala.
- Neste exemplo, o input se enquadraria mais na 2º Classe, por possuir um valor mais aproximado dentro do modelo.
- Quanto menor a distancia entre a frase a classe, maior é a confiança de que o sistema está classificando corretamente. 

> Modelos modernos baseados em Transformers (BERT, RoBERTa, DistilBERT) obtêm alta performance sem engenharia manual de features.

---

## NER - Extração de Entidades Nomeadas
Identifica e classifica termos relevantes em categorias pré‑definidas.

**Fluxo**:
1. Treinamento com *corpus* anotado.
2. Pipeline: tokenização → vetorização → predição.
3. Classificação de entidades (Pessoa, Produto, Local etc.).

**Exemplos**:
- "Solicitar um **CARTÃO** de **CRÉDITO**" → CARTÃO (Produto), CRÉDITO (Tipo)
- "Contrato **CRÉDITO PESSOAL**" → CRÉDITO (Produto), PESSOAL (Categoria)

- Ao identificar essas entidades, o sistema irá encaminhar o input para um determinado conjunto de classes ja cadastrado.

- Nos casos acima, ele irá encaminhar o usuário para uma resposta previamente cadastrada para cada um dos questionamentos, mediante a interpretação dos conjuntos.

> **Fuzzy Matching (ex.: `fuzzywuzzy`)** - corrige erros simples de digitação.

---

## Processamento de Áudio
Reconhecimento e síntese de voz para interações mais naturais.

### SST – Speech to Text
- Reconhece fala e converte em texto.
- Modelo precisa estar codificado com o idioma de fala.
- Métricas: WER (Word Error Rate), CER (Character Error Rate).
- Ferramentas: Google Speech‑to‑Text, Mozilla DeepSpeech, Whisper.

### TTS – Text to Speech
- Converte texto em fala.
- Aspectos: prosódia, naturalidade, voz personalizada.
- Ferramentas: Amazon Polly, Google TTS, Tacotron, FastSpeech.

### Voice Recognition (Identificação Biométrica)
- Reconhece ou autentica usuários pela voz.
- Aplicações de segurança e personalização.
- Modelos: i‑vector, x‑vector, redes neurais convolucionais.

> **Use Cases**: chatbots por voz, assistentes virtuais, ditado de texto, autenticação bancária.

> É possível aplicar o modelo para o reconhecimento de determinados sinais de modo que uma maquina possa interpretar um determinado som e assim definir uma ação.

---

## Considerações Finais
- Defina claramente os requisitos: rapidez, precisão, privacidade.
- Avalie custos de treinamento vs. uso de APIs prontas.
- Monitore vieses e desempenho em produção.
