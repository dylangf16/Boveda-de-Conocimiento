---
Fecha de creación: <% tp.date.now("YYYY-MM-DD HH:mm") %>
Fecha de Modificación: <% tp.date.now("YYYY-MM-DD HH:mm") %>
tags: 
Tema: Ventana Contextual
---

## 📚 Idea/Concepto 
Número máximo de tokens que un Transformer puede procesar en una ejecución de auto-atención, con costo computacional cuadrático. Requiere codificación posicional y permite dependencias extensas en ruta constante. Es limitación interna del modelo, distinta del contexto de sesión expandible mediante técnicas externas.

## 📌 Puntos Claves
- Limitación computacional: escalado cuadrático O(n²)
- Restricción arquitectural interna del modelo
- Dependencias de largo alcance en ruta constante
- Diferente del contexto de sesión (expandible externamente)
- Técnicas de expansión: RAG, Session History Stitching
- Impacta directamente en capacidad de razonamiento

## 🔗 Connections
- [[Mecanismo de Atención]]
- [[Large Language Models]]
- [[Tokenización]]

## 💡 Personal Insight
La ventana contextual representa el trade-off fundamental entre capacidad de memoria y eficiencia computacional en arquitecturas actuales.

## 🧾 Recursos
-