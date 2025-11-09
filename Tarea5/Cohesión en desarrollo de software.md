---
Fecha de creación: 2025-11-09 14:29
Fecha de Modificación: 2025-11-09 14:45
tags:
Tema: Cohesión en desarrollo de software
---

## 📚 Idea/Concepto 
**Cohesión** mide la fuerza de asociación entre elementos de un módulo trabajando para un único propósito. Se busca **alta cohesión** (preferiblemente **cohesión funcional**, donde elementos colaboran para una tarea específica) porque materializa **Separación de Intereses (SoC)** dentro del módulo y se complementa con **Bajo Acoplamiento** entre módulos para mejorar Mantenibilidad. Mantiene juntas las cosas que cambian juntas, reduce duplicación y Carga Cognitiva. La baja cohesión causa **Cambios Divergentes**. Otros tipos de cohesión incluyen secuencial (salida de uno es entrada de otro) y temporal (relacionados por tiempo de ejecución). **Prueba**: verificar si todos los elementos se relacionan con el nombre del módulo.

## 📌 Puntos Claves
- **Definición**: Fuerza de asociación entre elementos de un módulo para un único propósito
- **Objetivo**: Alta cohesión, idealmente cohesión funcional (tarea específica)
- **Principio**: Materializa Separación de Intereses (SoC) dentro del módulo
- **Complemento**: Se combina con Bajo Acoplamiento entre módulos
- **Beneficios**: Mantiene juntas cosas que cambian juntas, reduce duplicación y Carga Cognitiva
- **Riesgo**: Baja cohesión causa Cambios Divergentes
- **Tipos**: Funcional, secuencial, temporal
- **Heurística**: Todos los elementos deben relacionarse con el nombre del módulo

## 🔗 Connections
- [[Acoplamiento en desarrollo de software]]
- [[Arquitectura en Capas]]
- [[Arquitectura Microkernel]]
- [[04_Implementación - Estándares de Programación]]

## 💡 Personal Insight
La cohesión no es un ideal abstracto sino una métrica pragmática de cuán bien un módulo resiste al cambio. Alta cohesión significa que cuando los requisitos cambian, el impacto se localiza: las modificaciones están contenidas en un solo lugar. La prueba del nombre es reveladora: si no puedes explicar coherentemente por qué todos los elementos están juntos bajo el nombre del módulo, la cohesión es débil. La cohesión y el acoplamiento son las dos caras de la modularización efectiva: mantener junto lo que debe cambiar junto, separar lo que debe cambiar independientemente.

## 🧾 Recursos
