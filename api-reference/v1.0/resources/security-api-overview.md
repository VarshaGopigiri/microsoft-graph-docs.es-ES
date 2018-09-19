# <a name="use-the-microsoft-graph-security-api"></a>Utilizar la API de seguridad de Microsoft Graph

La API de seguridad de Microsoft Graph proporciona una interfaz y un esquema unificados para integrarse con soluciones de seguridad de Microsoft y su ecosistema de partners. Esto permite a los clientes simplificar las operaciones de seguridad y defenderse mejor contra las crecientes ciberamenazas. La API de seguridad de Microsoft Graph puede usarse como un servicio de agregación de seguridad federada con que enviar consultas a todos los proveedores de seguridad incorporados para obtener respuestas agregadas. Use la API de seguridad de Microsoft Graph para crear aplicaciones que:

- Consoliden y pongan en correlación alertas de seguridad de varios orígenes
- Desbloqueen datos contextuales para documentar investigaciones
- Automaticen las operaciones de seguridad para aumentar la eficiencia
- Proporcionen visibilidad a los datos de seguridad para permitir una administración de riesgos proactiva

La API de seguridad de Microsoft Graph incluye las siguientes entidades clave.

## <a name="alerts"></a>Alertas

Las alertas son problemas de seguridad potenciales de la cuenta empresarial de un cliente que han identificado las soluciones de seguridad de Microsoft o de un partner y que se han marcado para proceder a una acción o notificación. Con la entidad de [alertas](alert.md) de seguridad de Microsoft Graph, puede unificar y simplificar los problemas de seguridad en todas las soluciones integradas. Eso también permite que las aplicaciones pongan en correlación las alertas y el contexto para mejorar la protección contra amenazas y la respuesta. Estas desbloquean las eficiencias operativas de la seguridad al reducir el tiempo de investigación y el que lleva resolver los incidentes. Con la capacidad de actualizarse de la alerta, puede sincronizar el estado de alertas específicas en distintos productos y servicios de seguridad que se integran con la API de seguridad de Microsoft Graph mediante la actualización de su entidad de [alertas](alert.md).

Las soluciones de seguridad integradas de Microsoft Graph recibirán alertas de los siguientes proveedores de seguridad:

- Centro de seguridad de Azure
- Protección de identidad de Azure Active Directory
- Azure Information Protection
- Seguridad de aplicaciones en la nube de Microsoft
- Protección avanzada contra amenazas de Windows Defender
- Microsoft Intune (versión preliminar privada)
- Office 365 (próximamente)
- Soluciones de socios, como el marco de aplicación de Palo Alto Networks

> **Nota:** hay proveedores nuevos incorporándose continuamente al ecosistema de seguridad de Microsoft Graph.

## <a name="common-use-cases"></a>Casos de uso común

Las siguientes solicitudes son algunas de las más populares a la hora de trabajar con la API de seguridad de Microsoft Graph:

| **Casos de uso**   | **Recursos de REST** | **Probarlo en el Probador de Graph** |
|:---------------|:--------|:----------|
| Alertas de lista | [Alertas de lista](../api/alert_list.md) | [https://graph.microsoft.com/v1.0/security/alerts](https://developer.microsoft.com/en-us/graph/graph-explorer?request=security/alerts&method=GET&version=v1.0&GraphUrl=https://graph.microsoft.com) |
| Actualización de alertas | [Actualización de alertas](../api/alert_update.md) | [https://graph.microsoft.com/v1.0/security/alerts/{alert-id}](https://developer.microsoft.com/en-us/graph/graph-explorer?request=security/alerts/{alert-id}&method=PATCH&version=v1.0&GraphUrl=https://graph.microsoft.com) |

Puede utilizar los [webhooks](../../../concepts/webhooks.md) de Microsoft Graph para suscribirse a notificaciones sobre las actualizaciones de las entidades de seguridad de Microsoft Graph y recibir esas notificaciones.

## <a name="resources"></a>Recursos

Código y contribuciones a estas muestras de la API de seguridad de Microsoft Graph:

- [Muestra de ASP.NET (C#)](https://github.com/microsoftgraph/aspnet-security-api-sample)
- [Muestra de Python](https://github.com/microsoftgraph/python-security-rest-sample)
- [Muestra de Node.js (JavaScript)](https://github.com/microsoftgraph/nodejs-security-sample)

Interactúe con la comunidad:

- [Únase a la comunidad técnica](https://aka.ms/graphsecuritycommunity)
- [Discusión en StackOverflow](https://stackoverflow.com/questions/tagged/microsoft-graph-security)

## <a name="next-steps"></a>Pasos siguientes

La API de seguridad de Microsoft Graph puede abrirle nuevas vías de interacción con diferentes soluciones de seguridad de Microsoft y sus partners. Siga estos pasos para comenzar:

- Explore las [alertas](alert.md) en profundidad.
- Pruebe la API en el [Probador de Graph](https://developer.microsoft.com/graph/graph-explorer). En las **consultas de muestra**, elija **Mostrar más muestras** y establezca la categoría de seguridad como **on** (activada).
- Pruebe a [suscribirse para recibir notificaciones](../../../concepts/webhooks.md) sobre cambios de la entidad.

¿Necesita más ideas? Consulte [Cómo usan Microsoft Graph algunos de nuestros partners](https://developer.microsoft.com/graph/graph/examples#partners).
