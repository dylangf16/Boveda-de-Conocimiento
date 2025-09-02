---
Fecha de creación: <% tp.date.now("YYYY-MM-DD HH:mm") %>
Fecha de Modificación: <% tp.date.now("YYYY-MM-DD HH:mm") %>
tags:
Tema: Embeddings
---

## 📚 Idea/Concepto 
Los embeddings son representaciones vectoriales continuas que convierten tokens discretos (IDs numéricos) en vectores de alta dimensionalidad mediante una matriz de lookup entrenable. Cada fila representa un token del vocabulario y cada columna una dimensión latente que captura características semánticas, sintácticas y contextuales. Los vectores resultantes permiten operaciones aritméticas que reflejan relaciones lingüísticas análogas (ej: rey - hombre + mujer ≈ reina). Se combinan con codificaciones posicionales para preservar información de orden secuencial. En Transformers, la matriz de embeddings se comparte típicamente con la transformación lineal final (tied weights) para eficiencia de parámetros, y se aplica escalado por √d_model para estabilizar gradientes durante entrenamiento.

## 📌 Puntos Claves
- Arquitectura: Matriz de lookup entrenable (vocab_size × embedding_dim)
- Dimensiones capturadas: semántica, sintaxis, morfología, contexto
- Propiedades geométricas: distancia coseno refleja similaridad semántica
- Integración posicional: suma con encodings posicionales en Transformers
- Inicialización: típicamente aleatoria (distribución normal pequeña)

## 🔗 Connections
- [[Tokenización]]
- [[Large Language Models]]
- [[Redes Neuronales]]
- [[Mecanismo de Atención]]
- [[Ventana Contextual]]
- [[Codificación Posicional]]

## 💡 Personal Insight
Los embeddings son el puente fundamental entre símbolos discretos y matemáticas continuas, convirtiendo el lenguaje en geometría donde la distancia y dirección tienen significado semántico. Su calidad determina la capacidad representacional de todo el modelo.

## 🧾 Recursos