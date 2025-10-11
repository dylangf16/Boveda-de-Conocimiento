---
Fecha de creación: 2025-10-11 11:13
Fecha de Modificación: 2025-10-11 11:16
tags:
Tema: Latencia
---

## 📚 Idea/Concepto 
**Latencia** es el tiempo entre petición y respuesta, compuesto por network overhead (limitado por leyes físicas: velocidad de luz en propagación) más latencia de procesamiento (deserialización, acceso a jerarquía de memoria—L1 Cache/Main Memory/SSD con órdenes de magnitud distintas, dependencias, lógica). Se mide mediante métricas de percentiles (P90, P99) para capturar rendimiento en peor caso y definir SLOs, independiente de Throughput ("cuánto" trabajo). Su optimización requiere entender ambas dimensiones: velocidad y volumen. Solo desagregando sus componentes se puede medir e optimizar efectivamente el impacto en la receptividad de la aplicación.

## 📌 Puntos Claves
- **Componentes**: Network overhead (leyes físicas) + Latencia procesamiento (jerarquía memoria)
- **Red**: Limitada por velocidad de luz en propagación
- **Memoria**: Órdenes de magnitud diferentes (L1 < Main < SSD)
- **Medición**: Percentiles P90, P99 para peor caso y SLOs
- **Independencia**: Distinta de Throughput; mide velocidad no volumen
- **Optimización**: Desagregación de componentes para mejora efectiva

## 🔗 Connections
- [[04_Implementación - Estándares de Programación]]
- [[06_Despliegue e Infraestructura - Azure DevOps]]

## 💡 Personal Insight
La latencia es multidimensional: vinculada a leyes físicas inmutables (velocidad de luz), afectada por arquitectura de hardware (jerarquía de memoria), y medida mediante percentiles para capturar comportamiento en peor caso. Solo considerando todas estas capas se comprende completamente el rendimiento real percibido por usuarios.

## 🧾 Recursos