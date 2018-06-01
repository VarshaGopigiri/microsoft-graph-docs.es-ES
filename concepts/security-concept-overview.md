# <a name="overview-of-security-in-microsoft-graph-preview"></a>Información general sobre la seguridad de Microsoft Graph (versión preliminar) 

Puede usar Microsoft Graph para conectarse con Intelligent Security Graph para aprovechar las ventajas de Microsoft y los recursos de partners de seguridad, y crear mejores soluciones de respuesta de amenazas. Microsoft Graph también proporciona acceso a riesgos de usuario y cuenta detectados por el servicio Identity Protection en Azure Active Directory (Azure AD), lo que le permite integrar datos de riesgo de la cuenta en las aplicaciones de seguridad.

## <a name="why-use-the-security-api-and-connect-with-microsoft-intelligent-security-graph"></a>¿Por qué debería usar la API de seguridad y conectar con Microsoft Intelligent Security Graph?

Intelligent Security Graph es una plataforma unificada para combatir ciberamenazas. Permite obtener una protección contra amenazas en tiempo real para productos y servicios de Microsoft y es compatible con un ecosistema de soluciones integradas.

La [API de seguridad de Microsoft Graph](https://aka.ms/graphsecuritydocs) le permite conectarse con esas soluciones en Intelligent Security Graph. Le permite materializar y enriquecer más fácilmente el valor de estas soluciones.

### <a name="unify-and-standardize-alert-management"></a>Unificar y estandarice la administración de alertas

Correlacione alertas en soluciones de seguridad más fácilmente con un esquema de alertas común. Escriba código una vez para integrar las alertas de cualquier solución de seguridad integrada de Microsoft Graph y mantenga sincronizados los estados de alerta y las tareas en todas las soluciones. También puede transmitir alertas a soluciones de Administración de eventos e información de seguridad (SIEM) como Splunk y IBM QRadar mediante [Azure Monitor](https://docs.microsoft.com/es-ES/azure/monitoring-and-diagnostics/monitor-stream-monitoring-data-event-hubs#what-can-i-do-with-the-monitoring-data-being-sent-to-my-event-hub).

### <a name="federated-security-aggregation-service"></a>Servicio de agregación de seguridad federado

Use la API de seguridad como un servicio de agregación de seguridad federado para enviar consultas a todos los proveedores de seguridad incorporados y obtener respuestas agregadas.

### <a name="unlock-security-context-to-drive-investigation"></a>Desbloquear el contexto de seguridad a la investigación de unidad

Profundice en inventario relacionada con la seguridad (como los usuarios, los host y las aplicaciones), después, agregue contexto organizativo de otros proveedores de Microsoft Graph (Azure AD, Microsoft Intune, Office 365) para unir los contextos de seguridad y de la empresa y mejorar la respuesta contra amenazas.

## <a name="why-use-azure-ad-to-protect-identities-in-your-organization"></a>¿Por qué debería usar Azure AD para proteger las identidades de su organización?

La mayoría de las infracciones de seguridad son el resultado de que los atacantes roben la identidad del usuario, y se han vuelto terriblemente eficaces a la hora de aprovechar las infracciones de terceros y realizar ataques de difusión contraseña y ataques de suplantación sofisticados. Esto significa que debe proteger todas las cuentas de usuario de estos ataques e impedir proactivamente que se aprovechen las identidades en peligro.

Azure AD usa algoritmos de aprendizaje automático adaptable y heurística para detectar anomalías que indican cuentas potencialmente en peligro. Con estos datos, Identity Protection protege a los usuarios con directivas de acceso condicional basadas en riesgo y genera informes y alertas en su detección.

En la actualidad, Microsoft Graph ofrece acceso fácil a los clientes de Azure AD Premium P1 y P2 a consultas de detección de riesgos mediante Identity Protection y usa esos eventos en aplicaciones de seguridad y sistemas SIEM.

## <a name="next-steps"></a>Siguientes pasos

- [Usar la API de seguridad](../api-reference/beta/resources/security-api-overview.md)
- [Usar la API de Identity Protection de Azure AD](../api-reference/beta/resources/identityprotection_root.md)

