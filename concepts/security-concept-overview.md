# <a name="microsoft-graph-security-api-overview"></a>Introducción a la API de seguridad de Microsoft Graph

Puede usar la API de seguridad de Microsoft Graph para conectar los productos, servicios y socios de seguridad de Microsoft para optimizar las operaciones de seguridad y mejorar las prestaciones de protección, detección y respuesta a amenazas. La API de seguridad de Microsoft Graph es un servicio intermediario (o agente) que proporciona una única interfaz programática para la conexión a múltiples [proveedores de seguridad de Microsoft Graph](../api-reference/v1.0/resources/securityvendorinformation.md) (también denominados proveedores de seguridad o proveedores). Las solicitudes a la API de seguridad de Microsoft Graph se federan para todos los proveedores de seguridad aplicables. Los resultados se suman y se devuelven a la aplicación solicitante en un esquema común, tal como se muestra en el siguiente diagrama. Para obtener información detallada, consulte [Flujo de datos de seguridad de Microsoft Graph](security-dataflow.md).

![security_overview_diagram_1.png](./images/security_overview_diagram_1.png)

Para obtener información acerca de la autorización, consulte [La API de seguridad y autorización](security-authorization.md). Para obtener más información sobre los permisos, incluidos los permisos delegados y de aplicación, consulte [Permisos](permissions_reference.md#security-permissions).

## <a name="why-use-the-microsoft-graph-security-api"></a>¿Por qué usar la API de seguridad de Microsoft Graph?

La [API de seguridad de Microsoft Graph](../api-reference/v1.0/resources/security-api-overview.md) facilita la conexión a distintos productos y servicios de seguridad de Microsoft y de asociados de Microsoft. Le permite materializar y enriquecer más fácilmente el valor de estas soluciones.

### <a name="unify-and-standardize-alert-tracking"></a>Unificar y estandarizar el seguimiento de alertas

Escriba código una vez para integrar las alertas de cualquier solución de seguridad integrada de Microsoft Graph y mantenga sincronizados los estados de alerta y las asignaciones en todas las soluciones. También puede transmitir alertas a soluciones de Administración de eventos e información de seguridad (SIEM) como Splunk e IBM QRadar mediante [Azure Monitor](https://docs.microsoft.com/en-us/azure/monitoring-and-diagnostics/monitor-stream-monitoring-data-event-hubs#what-can-i-do-with-the-monitoring-data-being-sent-to-my-event-hub). Para obtener información detallada acerca de la integración de SIEM con las entidades de la API de seguridad, consulte [Integración con un SIEM](security_siemintegration.md).

### <a name="correlate-security-alerts-to-improve-threat-protection-and-response"></a>Correlacionar las alertas de seguridad para mejorar la protección y la respuesta antes amenazas

Correlacione alertas en soluciones de seguridad más fácilmente con un esquema de alertas unificado. Esto no sólo le permite recibir información de alertas sobre las que puede actuar, sino que también permite a los analistas de seguridad pivotar y enriquecer las alertas con información de activos y usuarios, lo que permite una respuesta más rápida a las amenazas y la protección de los activos.  

### <a name="update-alert-tags-status-and-assignments"></a>Actualizar las etiquetas de alertas, el estado y las asignaciones

Etiquete las alertas con información adicional del contexto o amenaza para una mejor respuesta y corrección. Asegúrese de que se capturan los comentarios en las alertas para tener visibilidad de todos los flujos de trabajo. Mantenga sincronizados los estados de alerta y las asignaciones para que todas las soluciones integradas reflejan el estado actual. Utilice suscripciones de webhook para recibir notificación de cambios.  

### <a name="unlock-security-context-to-drive-investigation"></a>Desbloquear el contexto de seguridad para impulsar la investigación

Profundice en inventario relacionada con la seguridad (como los usuarios, los host y las aplicaciones), después, agregue contexto organizativo de otros proveedores de Microsoft Graph (Azure AD, Microsoft Intune, Office 365) para unir los contextos de seguridad y de la empresa y mejorar la respuesta contra amenazas.

### <a name="proactively-manage-security-risks-preview"></a>Administrar de manera proactiva los riesgos de seguridad (versión preliminar)

Use Microsoft Secure Score (versión preliminar) para proporcionar visibilidad de las necesidades de seguridad de su organización y obtener sugerencias sobre cómo mejorarla, y proyecte una puntuación mejorada tras la incorporación de estas sugerencias. Mida fácilmente el progreso a lo largo del tiempo y obtenga conocimientos sobre cambios específicos que han llevado a una mejora de la puntuación.

## <a name="benefits-of-using-the-microsoft-graph-security-api"></a>Ventajas del uso de la API de seguridad de Microsoft Graph

En la siguiente tabla se enumeran las ventajas a las que pueden acceder distintas soluciones de seguridad mediante la integración con la API de seguridad de Microsoft Graph.  

|**Área**     | **Ventajas**|
|:---------------|:---------|
|**Proveedores de servicios de seguridad administrados (MSSP)**|<ul><li>Integración optimizada con servicios y herramientas de operaciones de seguridad.</li> <li>Menos tiempo y esfuerzos de implementación y mantenimiento.</li> <li>Capacidad para ofrecer más valor a los clientes MSSP.</li></ul>|
|**Soluciones de administración de riesgos de TI y SIEM**|<ul><li>Perfecta integración con soluciones de seguridad y asociados del ecosistema de Microsoft.</li> <li>Metadatos de alerta enriquecidos.</li> <li>Mejor correlación de alertas.</li></ul>|
|**Aplicaciones** <br> (información sobre amenazas, móvil, nube, IdC, detección de fraudes, identidad y acceso, riesgo y cumplimiento, cortafuegos, etc.)|<ul><li>Administración unificada de amenazas, prevención y administración de riesgos en varias soluciones de seguridad.</li> <li>Alertas, inventario, configuración y acciones que se exponen mediante Microsoft Graph.</li> <li>Integración instantánea con soluciones compatibles con Microsoft Graph.</li></ul>|

## <a name="next-steps"></a>Pasos siguientes

- [Utilizar la API de seguridad de Microsoft Graph](../api-reference/v1.0/resources/security-api-overview.md)
- ¿Está interesado en convertirse en un proveedor de seguridad? Póngase en contacto con [graphsecfeedback](mailto:graphsecfeedback@microsoft.com).
