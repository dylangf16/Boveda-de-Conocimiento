---
Fecha de creación: 2025-11-09 14:41
Fecha de Modificación: 2025-11-09 14:53
tags:
Tema: Acoplamiento en desarrollo de software
---

## 📚 Idea/Concepto 
**Acoplamiento** mide la interdependencia entre módulos. Se busca **bajo acoplamiento** mediante **Encapsulamiento (Information Hiding)**, ocultando detalles internos y exponiendo solo interfaces necesarias, reduciendo exposición a la complejidad. Junto con alta cohesión logra **ortogonalidad** (cambios independientes). El acoplamiento fuerte causa propagación en cascada y se manifiesta en: **Feature Envy** (usar más datos de otra clase), **Shotgun Surgery** (un cambio afecta múltiples clases), e **Inappropriate Intimacy** (conocimiento excesivo entre clases). Principios para reducirlo: **Ley de Demeter** (solo colaboradores inmediatos) y **Tell, Don't Ask** (comandar en vez de consultar estado). Mejora mantenimiento y reutilización.

## 📌 Puntos Claves
- **Definición**: Medida de interdependencia entre módulos
- **Objetivo**: Bajo acoplamiento mediante Encapsulamiento (Information Hiding)
- **Mecanismo**: Ocultar detalles internos, exponer solo interfaces necesarias
- **Ortogonalidad**: Bajo acoplamiento + alta cohesión = cambios independientes
- **Síntomas acoplamiento fuerte**: Feature Envy, Shotgun Surgery, Inappropriate Intimacy
- **Principios**: Ley de Demeter (colaboradores inmediatos), Tell Don't Ask (comandar vs. consultar)
- **Beneficios**: Mejora mantenimiento y reutilización

## 🔗 Connections
- [[Cohesión en desarrollo de software]]
- [[Arquitectura en Capas]]
- [[Arquitectura Orientada a Eventos]]
- [[Broker en arquitecturas Event Driven]]
- [[04_Implementación - Estándares de Programación]]

## 💡 Personal Insight
El acoplamiento es la deuda técnica invisible: cuando está alto, cada cambio reverbera impredeciblemente a través del sistema causando efectos en cascada. Los code smells (Feature Envy, Shotgun Surgery, Inappropriate Intimacy) no son problemas estéticos sino síntomas medibles de acoplamiento patológico. La Ley de Demeter y Tell Don't Ask no son reglas arbitrarias sino estrategias comprobadas para minimizar conocimiento transitivo entre módulos. El bajo acoplamiento permite que módulos evolucionen independientemente, haciendo el sistema genuinamente mantenible y extensible.

## 🧾 Recursos
