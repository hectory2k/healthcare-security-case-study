# RI5: Playbook para Detectar y Mitigar la Amenaza

## Finalidad

Mapear un conjunto de acciones concretas para detectar, contener,
mitigar y recuperarse ante la amenaza identificada.

---

## 1. Detección

| Acción | Herramienta | Frecuencia |
|--------|-------------|-----------|
| Monitorear puertos abiertos | Nmap | Semanal |
| Verificar headers HTTP | Curl | Semanal |
| Auditar certificados SSL | OpenSSL | Mensual |
| Revisar logs de acceso | SIEM / manual | Diario |
| Monitorear EventID 4886/4887 | Windows Event Viewer | Diario |

---

## 2. Contención

| Acción | Responsable | Plazo |
|--------|-------------|-------|
| Cerrar puertos innecesarios | Equipo de sistemas | 24 h |
| Configurar HSTS | Equipo de sistemas | 24 h |
| Asegurar cookies (Secure, HttpOnly, SameSite) | Equipo de sistemas | 48 h |
| Deshabilitar TLSv1.0 y TLSv1.1 | Equipo de sistemas | 48 h |

---

## 3. Mitigación

| Acción | Responsable | Plazo |
|--------|-------------|-------|
| Aplicar parche CVE-2026-54121 | Equipo de sistemas | 72 h |
| Rotar contraseña krbtgt (dos veces) | Administrador AD | 72 h |
| Revocar certificados sospechosos | Administrador AD | 72 h |
| Implementar entorno de datos aislado | Equipo de datos | 2 semanas |

---

## 4. Recuperación

| Acción | Responsable | Plazo |
|--------|-------------|-------|
| Restaurar desde backups verificados | Equipo de sistemas | 24 h |
| Validar integridad de datos | Equipo de datos | 48 h |
| Comunicar a autoridades | Dirección | Inmediato |
| Documentar lecciones aprendidas | Todos | 1 semana |

---

## 5. Comunicación

| Audiencia | Mensaje | Canal |
|-----------|---------|-------|
| Personal médico | Protocolo de contingencia | Reunión de servicio |
| Pacientes | Transparencia y acciones tomadas | Comunicado oficial |
| Ministerio | Reporte formal | Correo institucional |
| Prensa | Portavoz designado | Comunicado oficial |

---

## 6. Checklist Rápido

- [ ] HSTS está configurado?
- [ ] Las cookies tienen Secure, HttpOnly, SameSite?
- [ ] TLSv1.0 y TLSv1.1 están deshabilitados?
- [ ] El parche CVE-2026-54121 está aplicado?
- [ ] Se rotó krbtgt?
- [ ] Hay backups verificados?
- [ ] Existe un protocolo de contingencia clínica?
- [ ] Se comunicó a las autoridades?

---

## Conclusión

Este playbook permite detectar, contener, mitigar y recuperarse
ante la amenaza identificada. Su implementación reduce
significativamente el impacto de un ataque y garantiza la continuidad
operativa del sistema de salud.

---
*Documento generado: 2026-09-15 14:03:24 -03*
