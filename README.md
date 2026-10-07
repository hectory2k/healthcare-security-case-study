# Análisis de Seguridad en Sistemas de Salud — Caso de Estudio

**Autor:** H. L.
**Rol:** Profesional de la salud con formación en datos y seguridad
**Fecha:** 2026
**Clasificación:** Material educativo — Datos sensibles redactados

---

## Propósito

Documentar la metodología y los hallazgos de un análisis de seguridad
realizado sobre la infraestructura de un sistema de historia clínica
digital en el sector público de salud.

Este repositorio es un **caso de estudio metodológico**. No contiene
datos de pacientes, ni información que permita identificar a la
organización analizada. Todos los dominios, IPs y nombres han sido
redactados.

---

## Estructura del Análisis

Este repositorio se organiza según los **Requisitos de Información (RI)**
estándar de un análisis de inteligencia de amenazas:

| RI | Descripción | Archivo |
|----|-------------|---------|
| **RI1** | Identificación de las víctimas | [RI1_victimas.md](./RI1_victimas/RI1_victimas.md) |
| **RI2** | IoCs, IoAs y sus relaciones | [RI2_iocs_ioas.md](./RI2_iocs_ioas/RI2_iocs_ioas.md) |
| **RI3** | Vector de entrada y proceso de infección | [RI3_vector_infeccion.md](./RI3_vector_infeccion/RI3_vector_infeccion.md) |
| **RI4** | Actor y TTPs asociados | [RI4_actor_ttps.md](./RI4_actor_ttps/RI4_actor_ttps.md) |
| **RI5** | Playbook de detección y mitigación | [RI5_playbook.md](./RI5_playbook/RI5_playbook.md) |

---

## Metodología

1. **Reconocimiento pasivo** — Shodan
2. **Escaneo activo** — Nmap
3. **Análisis de configuración** — OpenSSL, Curl
4. **Contextualización de amenazas** — CVEs, informes regionales
5. **Mapeo MITRE ATT&CK**

---

## Contexto

El sector salud en América Latina es un objetivo prioritario de
ciberataques. Los datos de salud son el activo más valioso en el
mercado negro, y la mayoría de los sistemas tienen vulnerabilidades
básicas sin corregir.

Este análisis documenta una metodología replicable para identificar
esos riesgos y proponer mitigaciones concretas.

---

## Aviso Legal

Este material es **exclusivamente educativo y de investigación**.
No contiene datos sensibles ni información que comprometa la
seguridad de ningún sistema. Su uso debe ser ético y contar con
la autorización correspondiente.

---

## Licencia

MIT — Ver [LICENSE](./LICENSE)
