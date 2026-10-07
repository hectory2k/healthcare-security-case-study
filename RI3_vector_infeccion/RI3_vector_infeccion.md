# RI3: Identificación del Vector de Entrada y Proceso de Infección

## Finalidad

Determinar cómo un atacante podría ingresar al sistema y qué pasos
seguiría para comprometerlo.

---

## Vectores de Entrada Identificados

| Vector | Descripción | Requisito |
|--------|-------------|-----------|
| Puerto 80 (HTTP) | Redirección a HTTPS sin HSTS | Acceso a la red |
| Puerto 443 (HTTPS) | Servicio web expuesto | Acceso a la red |
| Cookies sin Secure | Interceptación en red no segura | Acceso a la red |
| AD CS vulnerable (CVE-2026-54121) | Escalada de privilegios | Usuario autenticado |

---

## Proceso de Infección (Kill Chain)

### Fase 1: Reconocimiento
- Escaneo de puertos con Nmap.
- Identificación de servicios y versiones.
- Detección de configuraciones débiles.

### Fase 2: Acceso Inicial
- Interceptación de tráfico HTTP (SSL Stripping).
- Robo de cookies de sesión.
- Phishing dirigido al personal médico.

### Fase 3: Escalada de Privilegios
- Explotación de CVE-2026-54121 (Certighost).
- Obtención de certificado de Domain Controller.
- Extracción de hash krbtgt.

### Fase 4: Persistencia
- Creación de Golden Ticket.
- Acceso a sistemas críticos.
- Exfiltración de datos de pacientes.

---

## Mapeo MITRE ATT&CK

| Táctica | Técnica | ID |
|---------|---------|-----|
| Acceso inicial | Explotación de servicio expuesto | T1190 |
| Credenciales | Robo de cookies de sesión | T1539 |
| Escalada | Explotación de AD CS | T1068 |
| Persistencia | Golden Ticket | T1550.001 |
| Exfiltración | Transferencia a C2 | T1041 |

---

## Conclusión

El vector de entrada más probable es el servicio web expuesto,
combinado con la falta de HSTS y cookies inseguras. Una vez
dentro, el atacante podría escalar privilegios usando la vulnerabilidad
Certighost y comprometer todo el dominio.

---
*Documento generado: 2026-09-15 14:03:24 -03*
