---
Fecha de creación: 2025-10-11 11:14
Fecha de Modificación: 2025-10-11 11:17
tags:
Tema: Throughput (Caudal)
---

## 📚 Idea/Concepto 
**Throughput (Caudal)** es la cantidad de trabajo que un sistema realiza por unidad de tiempo, medida en Transacciones Por Segundo (TPS). Mide "cuánto" se procesa, complementario e inverso a latencia que mide "qué tan rápido". Se optimiza mediante escalado horizontal, aumento de concurrencia, y reducción de cuellos de botella (locks, contención de recursos, limitaciones de software como GIL). Está limitado por recursos físicos y restricciones de diseño de software. Se mide usando percentiles (P90/P99) bajo carga extrema para definir límites operacionales máximos. Requiere balancear throughput-latencia según requisitos del negocio.

## 📌 Puntos Claves
- **Métrica**: Transacciones Por Segundo (TPS) u operaciones/segundo
- **Contraste**: "Cuánto" se procesa vs. "qué tan rápido" (latencia)
- **Optimización**: Escalado horizontal, concurrencia, reducción de cuellos botella
- **Cuellos botella**: Locks, contención de recursos, GIL (limitaciones software)
- **Limitaciones**: Recursos físicos (CPU, memoria, I/O) y restricciones software
- **Medición**: Percentiles P90/P99 bajo carga extrema para límites operacionales

## 🔗 Connections
- [[04_Implementación - Estándares de Programación]]
- [[06_Despliegue e Infraestructura - Azure DevOps]]

## 💡 Personal Insight
El throughput no solo depende de recursos físicos sino también de limitaciones de software (locks, contención, interpretadores). El arquitecto debe optimizar ambas dimensiones de cuellos de botella considerando trade-offs con latencia y requisitos del negocio para lograr rendimiento integral.

## 🧾 Recursos