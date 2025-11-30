---
Fecha de creación: 2025-11-30 11:00
Fecha de Modificación: 2025-11-30 12:45
tags:
Tema: Public IP en el cloud
---

## 📚 Idea/Concepto 
Una **IP Pública** es una dirección IP enrutable globalmente que permite la comunicación entre recursos internos de la VPC e Internet. El tráfico saliente utiliza NAT (Network Address Translation) para traducir IPs privadas a la IP pública, permitiendo además que múltiples recursos privados compartan una única IP pública saliente (conservación de direcciones). Se clasifica en: **Dinámica** (asignada temporalmente; cambia al desasignar el recurso, sin costo adicional en algunos proveedores) y **Estática** (IP reservada que persiste independientemente del estado del recurso, tiene costo adicional pero es crítica para Disaster Recovery (DR), permitiendo reasignación rápida durante failover sin propagación de cambios DNS). Debe asegurarse mediante Network Security Groups (NSG) para restringir acceso a puertos específicos (principio de mínimo privilegio). Sirve como front-end para Load Balancers (L4) (distribución TCP/UDP) y Application Gateways (L7) (distribución HTTP/HTTPS con capacidades avanzadas como WAF y SSL Termination). Sin IP pública, los recursos permanecen aislados dentro de la red privada sin accesibilidad externa directa.

## 📌 Puntos Claves
- **Definición**: Dirección IP globalmente enrutable para comunicación VPC-Internet
- **NAT**: Traduce IPs privadas a pública; múltiples recursos comparten una IP saliente
- **Dinámica**: Temporal, cambia al desasignar recurso; sin costo adicional (algunos proveedores)
- **Estática**: Persiste independiente del recurso; costo adicional; crítica para DR (failover rápido sin DNS)
- **Seguridad**: NSG para restringir puertos (mínimo privilegio)
- **Load Balancer (L4)**: Front-end para distribución TCP/UDP
- **Application Gateway (L7)**: Front-end HTTP/HTTPS con WAF y SSL Termination
- **Sin IP pública**: Recursos aislados en red privada sin acceso externo directo

## 🔗 Connections
- [[Virtual Private Cloud (VPC)]]
- [[Almacenamiento geo-redundante (GRS)]]
- [[Escalamiento horizontal y vertical en el cloud]]
- [[Disponibilidad de la aplicación]]
- [[Latencia]]

## 💡 Personal Insight
La IP pública es el punto de contacto crítico entre la infraestructura privada cloud y el Internet público, pero su gestión refleja trade-offs arquitectónicos profundos. Las IPs dinámicas son económicas pero introducen fragilidad: cada reasignación requiere propagación DNS, creando ventanas de inaccesibilidad. Las estáticas cuestan más pero son inversión en resiliencia: durante DR, la reasignación instantánea a instancias de backup elimina dependencia en TTLs de DNS, reduciendo RTO dramáticamente. El NAT permite que múltiples recursos compartan una IP, conservando el espacio de direcciones IPv4 cada vez más escaso. La seguridad mediante NSG no es opcional sino obligatoria: exponer IPs públicas sin filtrado es exponerse a todo Internet. Los Load Balancers y Application Gateways como front-ends transforman IPs públicas de puntos únicos de falla a distribuidores de tráfico resilientes.

## 🧾 Recursos
