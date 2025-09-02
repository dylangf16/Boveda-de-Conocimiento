---
Fecha de creación: <% tp.date.now("YYYY-MM-DD HH:mm") %>
Fecha de Modificación: <% tp.date.now("YYYY-MM-DD HH:mm") %>
tags: #tokenization #preprocessing #nlp #bpe #subword #vocabulary
Tema: Tokenización
---

## 📚 Idea/Concepto 
La tokenización es el proceso de preprocesamiento que segmenta texto crudo en unidades atómicas (tokens) y las mapea a identificadores numéricos únicos que el modelo puede procesar. Utiliza algoritmos de tokenización subword como Byte-Pair Encoding (BPE), WordPiece o SentencePiece para balancear granularidad y eficiencia del vocabulario. Maneja palabras fuera del vocabulario (OOV) descomponiéndolas en subpalabras conocidas. Incluye tokens especiales para funcionalidades específicas: [CLS] (clasificación), [SEP] (separación), <EOS> (fin de secuencia), <PAD> (relleno), <UNK> (desconocido), <BOS> (inicio). Los IDs resultantes sirven como índices directos para la matriz de embeddings, determinando la representación inicial y la eficiencia computacional del procesamiento secuencial.

## 📌 Puntos Claves
- Pipeline: Texto crudo → Normalización → Segmentación → Tokens → IDs numéricos
- Algoritmos principales:
  - SentencePiece: Trata texto como secuencia de Unicode, incluye espacios
- Manejo de vocabulario: Tamaño fijo (típico: 30K-50K tokens)
- Impacto downstream: Determina límites de la ventana contextual efectiva
- Reversibilidad: Detokenización debe preservar texto original

## 🔗 Connections
- [[Embeddings]]
- [[Large Language Models]]
- [[Ventana Contextual]]
- [[Redes Neuronales]]
- [[Preprocessing de Texto]]
- [[Vocabulario y OOV]]

## 💡 Personal Insight
La tokenización es el primer cuello de botella informacional del pipeline de NLP. Su diseño determina qué granularidad lingüística puede capturar el modelo y cómo de eficientemente puede procesarla. Es el arte de encontrar las "unidades naturales" del lenguaje que optimicen tanto la expresividad como la computación.

## 🧾 Recursos