# Caso de la clase: Checklist de Cumplimiento para GobData

Nombres: Héctor Guzmán, Bryam Diaz, Juan Abril

## Introducción
GobData es un portal estatal para trámites ciudadanos que procesa datos personales y sensibles (identificación, salud, direcciones, certificados). A continuación se presenta la evaluación por criterio del checklist (resultado del Excel) con la evidencia, explicación del impacto legal/técnico y recomendaciones prácticas.

---

### 1. Consentimiento
- **Nivel de cumplimiento:** Parcial
- **Evidencia / Justificación:** El portal solicita autenticación y permisos, pero no muestra un aviso de privacidad previo ni una opción clara de revocación.
- **Explicación:** El consentimiento informado exige que el titular conozca qué datos se recogen, con qué finalidad y cómo revocar permisos. Sin aviso previo, el consentimiento puede considerarse viciado o implícito.
- **Recomendación:** Implementar un aviso de privacidad antes de cada trámite, con opción explícita de aceptar/revocar y registro de la fecha/hora del consentimiento.

### 2. Finalidad
- **Nivel de cumplimiento:** Cumple
- **Evidencia / Justificación:** Los datos se usan exclusivamente para trámites estatales, no con fines comerciales.
- **Explicación:** La finalidad específica y legítima limita el tratamiento y es requisito legal; tenerla clara facilita auditorías y defensa legal.
- **Recomendación:** Publicar la finalidad específica por trámite y documentar procesos que impidan usos secundarios no autorizados.

### 3. Minimización
- **Nivel de cumplimiento:** Parcial
- **Evidencia / Justificación:** Algunos trámites solicitan documentos completos cuando bastarían atributos puntuales.
- **Explicación:** Recoger solo los datos necesarios reduce riesgo de exposición y facilita cumplimiento de retención mínima.
- **Recomendación:** Rediseñar formularios para solicitar únicamente los atributos estrictamente necesarios por operación.

### 4. Derechos ARCO (Acceso, Rectificación, Cancelación, Oposición)
- **Nivel de cumplimiento:** Parcial
- **Evidencia / Justificación:** No hay módulo visible para solicitudes de corrección o actualización de datos.
- **Explicación:** Debe existir un mecanismo accesible para que titulares ejerzan sus derechos; su ausencia implica incumplimiento legal.
- **Recomendación:** Crear un módulo ARCO en el portal con flujos, plazos de respuesta y registro de solicitudes.

### 5. Seguridad (ISO 27001)
- **Nivel de cumplimiento:** Parcial
- **Evidencia / Justificación:** Se observan controles básicos, pero no segregación de roles, gestión de incidentes ni cifrado explícito documentado.
- **Explicación:** Un SGSI conforme a ISO 27001 obliga a controles técnicos y organizacionales (control de accesos, cifrado, gestión de incidentes) para proteger la confidencialidad, integridad y disponibilidad.
- **Recomendación:** Implementar controles clave (5.36, 8.2, 8.16 según mapeo), cifrado en tránsito y reposo, y formalizar un SGSI con políticas y evidencias.

### 6. Retención
- **Nivel de cumplimiento:** Parcial
- **Evidencia / Justificación:** No existe calendario de retención publicado ni tabla por tipo de trámite.
- **Explicación:** La retención conforme a normativas (Archivo General, sectorales) reduce riesgos y obliga a eliminación segura de datos fuera de plazo.
- **Recomendación:** Definir y publicar la tabla de retención por tipo de trámite y automatizar su cumplimiento (borrado seguro o anonimización).

### 7. Roles y Accesos
- **Nivel de cumplimiento:** Parcial
- **Evidencia / Justificación:** No se evidencia RBAC completo, MFA ni logs inmutables.
- **Explicación:** Gestión de privilegios y trazabilidad son esenciales para prevenir accesos indebidos y demostrar cumplimiento en auditorías.
- **Recomendación:** Implementar RBAC, MFA para administradores y auditoría continua con registros inmutables.

### 8. Transferencia
- **Nivel de cumplimiento:** Parcial
- **Evidencia / Justificación:** No se identifican convenios públicos o visibles para transmisión interinstitucional.
- **Explicación:** Las transferencias de datos entre entidades deben estar soportadas por acuerdos que especifiquen finalidades, responsabilidades y medidas de seguridad.
- **Recomendación:** Formalizar convenios y acuerdos interinstitucionales con cláusulas de protección de datos y medidas técnicas.

### 9. Prevención de Fugas (DLP)
- **Nivel de cumplimiento:** No cumple
- **Evidencia / Justificación:** No hay evidencia de monitoreo DLP o controles anti-fuga.
- **Explicación:** Sin controles de prevención de exfiltración, los datos sensibles corren mayor riesgo de fuga, incumpliendo requisitos de protección técnica.
- **Recomendación:** Implementar DLP, monitoreo de tráfico, alertas y controles de exfiltración para activos críticos.

### 10. Gestión de Incidentes
- **Nivel de cumplimiento:** Parcial
- **Evidencia / Justificación:** No se evidencia proceso documentado en el caso base.
- **Explicación:** Contar con un proceso formal de reporte y respuesta reduce impacto de incidentes y es clave para obligaciones de notificación a autoridades y titulares.
- **Recomendación:** Documentar y publicar el proceso de gestión de incidentes con SLAs, roles responsables y canales de comunicación.

---

## Conclusión y próximos pasos
- **Resumen:** GobData muestra cumplimiento parcial en la mayoría de criterios; áreas críticas: DLP, ARCO visible, retención y gestión de accesos.
- **Prioridad inmediata:** Implementar aviso de privacidad y módulo ARCO, DLP básico y políticas de retención.
- **Siguiente entregable:** Diligenciar checklist del cliente real, generar informe técnico con hallazgos y plan de mitigación (acciones, responsables, fechas).

---

Documento elaborado a partir del checklist de referencia (archivo Excel proporcionado en clase).

