# <a name="versioning-support-and-breaking-change-policies-for-microsoft-graph"></a>Control de versiones, compatibilidad y directivas de cambios importantes en Microsoft Graph 

Este artículo describe el soporte y las directivas de cambios importantes para Microsoft Graph y las versiones de la API de Microsoft Graph que están disponibles actualmente.

## <a name="support-policy-and-deprecation-information"></a>Información de degradación y directiva de soporte

Microsoft Graph sigue la [Microsoft Lifecycle Policy](https://support.microsoft.com/es-ES/lifecycle). 

A medida que vayan apareciendo nuevas versiones de los SDK de Microsoft Graph y de las API de REST de Microsoft Graph, se irán retirando las versiones anteriores. Microsoft declarará una versión en desuso con al menos 24 meses de antelación a la retirada de una API o un SDK. 

Cuando cambiamos de una versión de la API a otra posterior (por ejemplo, de v1.0 a v2.0), estamos indicando que la versión actual en ese momento (en este ejemplo, v1.0) comienza a estar en desuso y, 24 meses después de ese anuncio, ya no se admitirá. Es posible que hagamos alguna excepción a esta directiva por problemas de seguridad del servicio o de confiabilidad de su estado.  

Una vez que se indica que la API está en desuso, se recomienda encarecidamente migrar a la versión más reciente lo antes posible. En algunos casos, anunciaremos que las nuevas aplicaciones tendrán que empezar a usar las nuevas API poco después de que las API originales queden en desuso. En estos casos, únicamente las aplicaciones activas que estén utilizando las API en desuso podrán continuar utilizándolas.   

### <a name="api-contract-and-non-backward-compatible-changes"></a>Contrato de API y cambios no compatibles con versiones anteriores

Microsoft Graph tiene un registro de los cambios entre versiones. Estos cambios se enumeran en el [Registro de cambios de Microsoft Graph](changelog.md). A medida que se vayan agregando funcionalidades y datos a Microsoft Graph, se incrementará el número de versión de la API para los cambios que no sean compatibles con versiones anteriores de la API. 

Los siguientes son ejemplos de cambios que no son compatibles con versiones anteriores:

 - Cambios en la dirección URL, o en solicitudes o respuestas fundamentales asociadas a un recurso    
 - Eliminación, cambio de nombre o cambio del tipo de propiedad declarada
 - Eliminación o cambio de nombre de las API o de sus parámetros
 - Adición de un encabezado de solicitud requerido

Los siguientes son ejemplos de cambios que son compatibles con versiones anteriores:

 - Adición de propiedades que admiten valores NULL o tienen un valor predeterminado
 - Adición de un miembro de una enumeración
 - Eliminación, cambio de nombre o cambio del tipo de extensión abierta
 - Eliminación, cambio de nombre o cambio del tipo de anotación
 - Introducción de paginación en las colecciones existentes
 - Cambios en los códigos de error
 - Cambios en el orden de propiedades
 - Cambios en la longitud o el formato de cadenas opacas, como identificadores de recursos

>**Nota:** Con el tiempo, actualizaremos la lista de cambios compatibles con versiones anteriores. Si genera su propio proxy de cliente (como clientes WCF), nuestro consejo es que las aplicaciones cliente estén preparadas para recibir propiedades y tipos derivados que no estaban definidos previamente por el servicio de API de Microsoft Graph. La API de Microsoft Graph sigue las instrucciones descritas en la sección de [Versiones del modelo](https://github.com/microsoft/api-guidelines/blob/master/Guidelines.md#12-versioning) en las [directrices de la API de REST de Microsoft](https://github.com/microsoft/api-guidelines/). 

## <a name="versions"></a>Versiones

Actualmente, existen las siguientes versiones de la API de Microsoft Graph.

### <a name="beta-version"></a>Versión beta
La versión beta de la API de Microsoft Graph contiene funciones que se encuentran en su _**versión preliminar**_, según se expone en `https://graph.microsoft.com/beta`. Para consultar documentación sobre la API beta, vea [Referencia del punto de conexión de Microsoft Graph beta](../api-reference/beta/beta-overview.md). Cada cierto tiempo, se producirán cambios importantes en la versión beta. Por tanto, no establezca dependencias de producción en las API /beta.

No ofrecemos ninguna garantía de que una característica de la versión beta se incluya en la versión actual. Cuando el equipo de la API de Microsoft Graph crea que una característica de la versión beta está lista para tener disponibilidad general (GA), agregaremos esa característica a la versión más actual. Si la promoción de la característica da como resultado un cambio importante en la versión actual, se incrementará el número de versión, y la nueva versión se convertirá en la versión actual.
Nuestra comunidad de desarrolladores puede enviar una solicitud de característica en [UserVoice](https://officespdev.uservoice.com/), incluidas las solicitudes de nuevas características, así como solicitudes para promover la API beta existente a la versión actual. 

### <a name="current-version"></a>Versión actual

La versión actual de Microsoft Graph es v1.0. La versión /v1.0 de la API de Microsoft Graph contiene características que están disponibles y listas para su uso en un entorno de producción, según se expone en `https://graph.microsoft.com/v1.0`. Puede examinar la documentación de las API v1.0 en la tabla de contenido.

### <a name="deprecated-and-unsupported-versions"></a>Versiones en desuso y no admitidas

Actualmente, no hay versiones de Microsoft Graph en desuso.

## <a name="terms-of-use"></a>Condiciones de uso

Su uso de las API de Microsoft Graph implica la aceptación de las [Condiciones de uso](../misc/terms-of-use.md). 

Su opinión es importante para nosotros. Póngase en contacto con nosotros en [StackOverflow](https://stackoverflow.com/questions/tagged/microsoftgraph?sort=newest). Etiquete sus preguntas con {MicrosoftGraph}.
