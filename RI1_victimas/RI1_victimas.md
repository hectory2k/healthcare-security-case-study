# RI1: Identificación de las Víctimas

## Finalidad

Identificar las víctimas afectadas o potencialmente afectadas por
la amenaza, para dimensionar el impacto y priorizar la respuesta.

---

## Activos Afectados (Potenciales)

| Activo | Tipo | Criticidad | Descripción |
|--------|------|------------|-------------|
| Sistema de Historia Clínica Digital | Aplicación web | CRÍTICA | Contiene datos de salud de pacientes |
| Servidor web | Infraestructura | ALTA | Puerta de entrada al sistema |
| Active Directory (AD CS) | Infraestructura | CRÍTICA | Gestión de identidades y certificados |
| Red del proveedor | Infraestructura | ALTA | Conectividad del sistema |

---

## Víctimas Potenciales

| Tipo de víctima | Impacto |
|-----------------|---------|
| Pacientes | Exposición de datos de salud |
| Personal médico | Robo de credenciales, suplantación de identidad |
| Institución | Interrupción del servicio, pérdida de confianza |
| Autoridad sanitaria | Sanción legal, daño reputacional |
| Región | Riesgo de propagación a otros sistemas |

---

## Evidencia

- Análisis de infraestructura pública
- Fecha de análisis: 2026
- Herramientas: Shodan, Nmap, OpenSSL, Curl

---

## Conclusión

El sistema de historia clínica digital es un activo CRÍTICO por
contener datos sensibles de salud. Cualquier compromiso afecta
directamente a los pacientes y a la continuidad del servicio.
