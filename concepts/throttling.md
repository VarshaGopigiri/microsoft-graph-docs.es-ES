# <a name="microsoft-graph-throttling-guidance"></a>Guía de limitación de Microsoft Graph


La limitación restringe el número de llamadas simultáneas a un servicio para evitar el uso excesivo de los recursos. Microsoft Graph está diseñado para admitir un gran volumen de solicitudes. Si se produce un número abrumador de solicitudes, la limitación ayuda a mantener un rendimiento y fiabilidad óptimos del servicio Microsoft Graph.

Los márgenes de la limitación varían en función del escenario. Por ejemplo, si va a realizar un gran volumen de escrituras, la posibilidad de limitación es mayor que si solo va a realizar lecturas.

## <a name="what-happens-when-throttling-occurs"></a>¿Qué sucede cuando se produce la limitación?

Cuando se supera un umbral límite, Microsoft Graph limita las solicitudes sucesivas de ese cliente durante un período de tiempo. Cuando se produce la limitación, Microsoft Graph devuelve el código de estado HTTP 429 (demasiadas solicitudes) y las solicitudes proporcionan errores. Se devuelve un tiempo de espera sugerido en el encabezado de la respuesta de la solicitud con errores. El comportamiento de la limitación puede depender del tipo y el número de solicitudes. Por ejemplo, si tiene un gran volumen de solicitudes, se regulan todos los tipos de estas. Los límites del umbral varían según el tipo de solicitud. Por lo tanto, podría encontrarse un escenario donde se limiten las escrituras pero se sigan permitiendo las lecturas. 

## <a name="common-throttling-scenarios"></a>Escenarios de limitación comunes

Las causas más comunes de limitación de los clientes incluyen:

* Un gran número de solicitudes en todas las aplicaciones de un espacio empresarial.
* Un gran número de solicitudes de una aplicación determinada a través de todos los espacios empresariales.

## <a name="best-practices-to-handle-throttling"></a>Procedimientos recomendados para tratar la limitación

Las siguientes son recomendaciones para el tratamiento de la limitación:

* Reduzca el número de operaciones por solicitud.
* Reduzca la frecuencia de llamadas.
* Evite los reintentos inmediatos, dado que todas las solicitudes se acumulan contra los límites de uso.

Cuando se implementa el control de errores, utilice el código de error HTTP 429 para detectar la limitación. La respuesta de error incluye el campo *Retry-After* en el encabezado de la respuesta. Interrumpir las solicitudes mediante el retraso *Retry-After* es la forma más rápida de recuperar la limitación, ya que Microsoft Graph sigue registrando el uso de recursos durante la limitación de un cliente.

1. Espere el número de segundos especificado en el campo *Retry-After*.
2. Vuelva a intentar realizar la solicitud.
3. Si la solicitud vuelve a proporcionar errores con un código de error 429, todavía se le está limitando. Siga utilizando el retraso recomendado Retry-After y vuelva a intentar la solicitud hasta que lo logre.

Actualmente, los siguientes recursos proporcionan un encabezado retry-after:
- [Usuario](../api-reference/v1.0/resources/user.md)
- [Foto](../api-reference/v1.0/resources/profilephoto.md)
- [Correo](../api-reference/v1.0/resources/message.md)
- [Calendario (usuarios y grupos)](../api-reference/v1.0/resources/event.md)
- [Contacto](../api-reference/v1.0/resources/contact.md)
- [Datos adjuntos](../api-reference/v1.0/resources/attachment.md)
- [Conversaciones de grupo](../api-reference/v1.0/resources/conversation.md)
- [Contactos y redes sociales](../api-reference/beta/resources/social_overview.md)
- [Unidad (OneDrive)](../api-reference/v1.0/resources/drive.md)

Para obtener una explicación más amplia de la limitación en Microsoft Cloud, vea [Patrón Throttling]((https://msdn.microsoft.com/es-ES/library/office/dn589798.aspx)).
