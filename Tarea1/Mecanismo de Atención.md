---
Fecha de creación: <% tp.date.now("YYYY-MM-DD HH:mm") %>
Fecha de Modificación: <% tp.date.now("YYYY-MM-DD HH:mm") %>
tags: 
Tema: Mecanismo de Atención
---

## 📚 Idea/Concepto 
Mecanismo en Transformers que calcula relaciones entre tokens simultáneamente mediante proyecciones Query-Key-Value. Calcula compatibilidades con producto punto escalado, normaliza con softmax y pondera Values. Multi-Head Attention ejecuta esto en paralelo, permitiendo procesamiento completo vs. secuencial de RNNs.

## 📌 Puntos Claves
- Proyecciones paralelas: Q, K, V para cada token
- Producto punto escalado: compatibilidad Query-Key / √dk
- Softmax para normalización de pesos de atención
- Multi-Head: múltiples subespacios de representación
- Procesamiento paralelo completo vs. RNNs secuenciales
- Requiere codificación posicional explícita

## 🔗 Connections
- [[Large Language Models]]
- [[Ventana Contextual]]
- [[Embeddings]]
- [[Redes Neuronales]]

## 💡 Personal Insight
La atención permite que cada token "mire" a todos los demás simultáneamente, creando representaciones verdaderamente contextualizadas en tiempo constante.

## 🧾 Recursos
-