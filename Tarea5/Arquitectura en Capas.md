---
Fecha de creación: 2025-11-09 13:40
Fecha de Modificación: 2025-11-09 14:32
tags:
Tema: Arquitectura en Capas
---

## 📚 Idea/Concepto 
**Arquitectura en Capas** es un patrón de diseño estructural que organiza el software en capas horizontales lógicas (Layers), cada una con responsabilidad específica aplicando Separación de Intereses, buscando Alta Cohesión interna y Bajo Acoplamiento entre capas. La comunicación sigue dos estrategias: **Interacción Estricta** (solo con capa inmediatamente inferior, maximiza encapsulación) o **Interacción Suelta** (con cualquier capa inferior, introduce Acoplamiento Fuerte pero optimiza rendimiento). Incluye típicamente: Presentación, Aplicación/Servicio (orquestación), Negocio (dominio), y Datos (dividida en Capa de Acceso con ORMs/SQL y fuente física). Las Preocupaciones Transversales (Logging, Seguridad) se gestionan mediante interfaces o módulos separados que atraviesan capas. La división lógica (Layers) no implica división física (Tiers). Este patrón mejora Modificabilidad y Testabilidad mediante aislamiento de responsabilidades.

## 📌 Puntos Claves
- **Organización**: Capas horizontales lógicas con responsabilidad específica
- **Principios**: Separación de Intereses, Alta Cohesión interna, Bajo Acoplamiento entre capas
- **Estrategias comunicación**: Interacción Estricta (máxima encapsulación) vs. Suelta (optimiza rendimiento)
- **Capas típicas**: Presentación, Aplicación/Servicio, Negocio, Datos (Acceso + física)
- **Preocupaciones transversales**: Logging, Seguridad mediante interfaces que atraviesan capas
- **Distinción**: Layers (lógico) ≠ Tiers (físico)
- **Beneficios**: Mejora Modificabilidad y Testabilidad por aislamiento

## 🔗 Connections
- [[03_Arquitectura y Diseño - Microservicios]]
- [[Cohesión en desarrollo de software]]
- [[Acoplamiento en desarrollo de software]]
- [[05_Pruebas - Pruebas Unitarias]]

## 💡 Personal Insight
La arquitectura en capas materializa el principio fundamental de separación de intereses a nivel estructural. El trade-off entre interacción estricta y suelta revela que no existe una arquitectura perfecta: se debe elegir conscientemente entre pureza arquitectónica (encapsulación máxima) y pragmatismo (rendimiento optimizado). La clave está en entender que las capas son abstracciones lógicas que pueden mapearse a diversas configuraciones físicas según necesidades de despliegue.

## 🧾 Recursos
