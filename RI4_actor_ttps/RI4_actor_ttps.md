# RI4: Identificación del Actor y TTPs Asociados

## Finalidad

Determinar qué tipo de actor podría estar detrás de una amenaza y
qué tácticas, técnicas y procedimientos (TTPs) utiliza.

---

## Perfil del Actor (Estimado)

| Característica | Estimación |
|----------------|------------|
| Tipo | Cibercriminal / Ransomware-as-a-Service |
| Motivación | Económica (extorsión) |
| Sofisticación | Media a Alta |
| Recursos | Acceso a botnets, PoCs públicos |
| Objetivo | Datos de salud (alto valor en mercado negro) |

---

## TTPs Documentados (MITRE ATT&CK)

| Táctica | Técnica | Descripción |
|---------|---------|-------------|
| Reconocimiento | T1595 | Escaneo activo de puertos |
| Acceso inicial | T1190 | Explotación de servicio expuesto |
| Acceso inicial | T1566 | Phishing dirigido |
| Credenciales | T1539 | Robo de cookies de sesión |
| Escalada | T1068 | Explotación de CVE-2026-54121 |
| Persistencia | T1550.001 | Golden Ticket |
| Exfiltración | T1041 | Transferencia a C2 |

---

## Contexto Regional

Según el informe "Cybersecurity Landscape of the Health Sector in
Latin America and the Caribbean, 2022–2026", los actores que atacan
el sector salud en la región utilizan:

- Ransomware y extorsión.
- Compromiso de credenciales.
- Explotación de vulnerabilidades conocidas.
- Ataques a la cadena de suministro.

---

## Limitaciones

No se identificó un actor específico (APT o grupo criminal con nombre).
El análisis se basa en patrones de comportamiento y en el contexto
regional documentado.

---

## Conclusión

El perfil del actor corresponde a cibercriminales motivados
económicamente, con capacidad de explotar vulnerabilidades conocidas
y acceso a herramientas públicas (PoCs). El sector salud es un
objetivo prioritario por el alto valor de los datos.

---
*Documento generado: 2026-09-15 14:03:24 -03*
