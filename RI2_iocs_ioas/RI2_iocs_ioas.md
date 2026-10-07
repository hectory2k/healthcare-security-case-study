# RI2: Identificación de IoCs, IoAs y sus Relaciones

## Finalidad

Identificar los Indicadores de Compromiso (IoCs) y los Indicadores
de Ataque (IoAs), y establecer sus relaciones, para detectar
actividad sospechosa.

---

## Indicadores de Compromiso (IoCs)

| IoC | Tipo | Valor | Fuente |
|-----|------|-------|--------|
| Puertos abiertos | Red | 80, 443 | Nmap |
| Servicio web | Aplicación | nginx | Nmap |
| Certificado wildcard | Criptográfico | [DOMINIO_REDACTADO] | OpenSSL |
| Ausencia de HSTS | Configuración | — | Curl |
| Cookies sin Secure | Configuración | — | Curl |
| Versión TLS | Criptográfico | TLSv1.0, TLSv1.1, TLSv1.2 | Nmap |

---

## Indicadores de Ataque (IoAs)

| IoA | Descripción | Relación |
|-----|-------------|----------|
| Falta de HSTS | Permite SSL Stripping | Se relaciona con cookies sin Secure |
| Cookies sin Secure | Permite robo de sesión | Se relaciona con falta de HSTS |
| Certificado wildcard | Permite suplantación | Se relaciona con todos los subdominios |
| TLSv1.0/1.1 habilitados | Permite downgrade | Se relaciona con cifrados débiles |

---

## Relaciones entre Indicadores

    Falta de HSTS --> SSL Stripping --> Robo de credenciales
    Cookies sin Secure --> Secuestro de sesión --> Acceso no autorizado
    Certificado wildcard --> Suplantación --> Ataque a otros subdominios
    TLS obsoleto --> Downgrade --> Interceptación de tráfico

---

## Evidencia

- Salida de nmap --script ssl-enum-ciphers
- Salida de curl -I https://...
- Salida de openssl s_client

---

## Conclusión

Los indicadores detectados configuran un patrón de vulnerabilidad
estructural que facilita múltiples vectores de ataque. No son
hallazgos aislados, sino un ecosistema de riesgo interconectado.

---
*Documento generado: 2026-09-15 14:03:24 -03*
