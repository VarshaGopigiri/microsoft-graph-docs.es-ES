# <a name="versioning-support-and-breaking-change-policies-for-microsoft-graph"></a>Control de versiones, compatibilidad y políticas de cambios importantes de Microsoft Graph 

Este artículo describe el soporte y las políticas de cambios importantes para Microsoft Graph y las versiones de la API de Microsoft Graph que están disponibles actualmente.

## <a name="support-policy-and-deprecation-information"></a>Información de degradación y directiva de soporte

Microsoft Graph sigue la [Microsoft Lifecycle Policy](https://support.microsoft.com/en-us/lifecycle). 

Como se han lanzado nuevas versiones de los SDK de Microsoft Graph y API de REST de Microsoft Graph, se retirarán las versiones anteriores. Microsoft declarará una versión en desuso con al menos 24 meses antes de la retirada de una API o un SDK. 

Cuando se incrementa la versión principal de la API (por ejemplo, de v1.0 a v2.0), anunciamos que la versión actual (en este ejemplo, v1.0) en ese momento comienza a estar en desuso y, 24 meses después de ese anuncio, ya no se admitirá. Cuando una API se marcada como en desuso, se recomienda encarecidamente que migre a la versión más reciente tan pronto como sea posible para evitar que se vea afectada. Podríamos realizar excepciones a esta directiva para la seguridad del servicio o problemas de confiabilidad del mantenimiento. 

### <a name="api-contract-and-non-backward-compatible-changes"></a>Contrato de API y cambios no compatibles con versiones anteriores

Microsoft Graph tiene un registro de los cambios entre las versiones. Estos cambios se enumeran en el [Registro de cambios de Microsoft Graph](changelog.md). Al agregar datos y una nueva funcionalidad a Microsoft Graph, se incrementará el número de versiones de la API los cambios a la API que no son compatibles con versiones anteriores. 

Los siguientes son ejemplos de cambios que no son compatibles con versiones anteriores:

 - Cambios en la dirección URL o solicitud o respuesta fundamental asociados a un recurso    
 - Eliminación, cambio de nombre o cambio del tipo de propiedad declarada
 - Eliminación o cambio de nombre de los parámetros de las API o de las API
 - Adición de un encabezado de solicitud requerido

Los siguientes son ejemplos de cambios que son compatibles con versiones anteriores:

 - Adición de propiedades que admiten valores NULL o tienen un valor predeterminado
 - Adición de un miembro de una enumeración
 - Eliminación, cambio de nombre o cambio del tipo de extensión abierta
 - Eliminación, cambio de nombre o cambio del tipo de anotación
 - Introducción de paginación a las colecciones existentes
 - Cambios en los códigos de error
 - Cambios en el orden de propiedades
 - Cambios en la longitud o el formato de cadenas opacas, como identificadores de recursos

>**Nota:** Con el tiempo, actualizaremos la lista de cambios compatibles con versiones anteriores. Si genera su propio proxy de cliente (como clientes WCF), nuestras instrucciones son que las aplicaciones del cliente deben estar preparadas para recibir propiedades y tipos derivados que no están definidos previamente por el servicio de API de Microsoft Graph API. La API de Microsoft Graph sigue las instrucciones descritas en la sección del [Control de versiones modelo](https://github.com/Microsoft/api-guidelines/blob/master/Guidelines.md#12-versioning) en las [directrices de la API de REST de Microsoft](https://github.com/microsoft/api-guidelines/). 

## <a name="versions"></a>Versiones

Actualmente existen las siguientes versiones de la API de Microsoft Graph.

### <a name="beta-version"></a>Versión beta
La versión beta de la API de Microsoft Graph contiene características que se encuentran en la vista previa, según se expone en `https://graph.microsoft.com/beta`. Para la API beta, consulte [Referencia del punto de conexión de Microsoft Graph beta](../api-reference/beta/beta-overview.md). Espere cambios importantes en la versión beta de vez en cuando. No tienen una dependencia de producción en las API de /beta.

No ofrecemos ninguna garantía de que una característica de la versión beta promueva a la versión actual. Cuando el equipo de API de Microsoft Graph crea que una característica de la versión beta está lista para tener disponibilidad general (GA), agregaremos esa característica a la versión más actual. Si la promoción de la función da como resultado un cambio importante en la versión actual, se incrementará el número de versión, con la nueva versión que se convertirá en la versión actual. Nuestra comunidad de desarrolladores puede enviar una solicitud de característica en [UserVoice](https://officespdev.uservoice.com/), incluidas las solicitudes de nuevas características, así como solicitudes para promover la API beta existente a la versión actual. 

### <a name="current-version"></a>Versión actual

La versión actual de Microsoft Graph es v1.0. La versión /v1.0 de la API de Microsoft Graph contiene características que se encuentran en la vista previa, según se expone en `https://graph.microsoft.com/v1.0`. Puede examinar la documentación de las API v1.0 en la tabla de contenido.

### <a name="deprecated-and-unsupported-versions"></a>Versiones en desuso y no admitidas

Actualmente no hay versiones de Microsoft Graph en desuso.

## <a name="terms-of-use"></a>Términos de uso

Mediante el uso de las API de Microsoft Graph, acepta las [Condiciones de uso](https://msdn.microsoft.com/en-us/cc300389). 

Su opinión es importante para nosotros. Póngase en contacto con nosotros en [StackOverflow](https://stackoverflow.com/questions/tagged/microsoftgraph?sort=newest). Etiquete sus preguntas con {MicrosoftGraph}.
