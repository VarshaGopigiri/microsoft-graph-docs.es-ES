---
title: Trabajar con las llamadas y API de reuniones en línea en Microsoft Graph
description: Llama la Microsoft Graph y API de reuniones en línea, agrega una nueva dimensión a cómo las aplicaciones y los servicios pueden interactuar con los usuarios mediante la habilitación de características de vídeo y voz. La API permite crear llamadas y recibir llamadas de usuarios y aplicaciones en Microsoft Teams. Puede usar estas API para crear una aplicación de servicio (bot) que pueda actuar como un participante en una llamada o una reunión.
author: VinodRavichandran
ms.openlocfilehash: 1b7efc774dfee0e0617d5c4f99ba08351c9f2a1f
ms.sourcegitcommit: 0b3a57ac8b99871e56389f9be15e4f96e219f635
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/20/2018
ms.locfileid: "27380565"
---
# <a name="working-with-the-calls-and-online-meetings-api-in-microsoft-graph"></a>Trabajar con las llamadas y API de reuniones en línea en Microsoft Graph

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Llama la Microsoft Graph y API de reuniones en línea, agrega una nueva dimensión a cómo las aplicaciones y los servicios pueden interactuar con los usuarios mediante la habilitación de características de vídeo y voz. La API permite crear llamadas y recibir llamadas de usuarios y aplicaciones en Microsoft Teams. Puede usar estas API para crear una aplicación de servicio (bot) que pueda actuar como un participante en una llamada o una reunión.

## <a name="call-types"></a>Tipos de llamada

Las llamadas se clasifican como llamadas de punto a punto o más participantes. Un usuario puede iniciar una llamada punto a punto con su robot o invitar a su bot en una conferencia con varios participantes existente. No hay permisos son necesarios cuando el usuario está invitando el robot a una llamada punto a punto. Para que su bot a participar en una llamada con varios participantes, el robot debe tener permisos desde el Administrador de inquilinos para unirse a una llamada de un grupo.

![Una imagen que muestra las llamadas de punto a punto y entre varias partes](https://cdn.graph.office.net/prod/GraphDocuments/en-us/concepts/images/call-types.png)

Si el robot es crear la llamada, debe tener el inicio o el permiso de llamada del grupo de inicio. El robot tiene la opción para crear una llamada punto a punto o una llamada entre varias partes.

- Para una llamada punto a punto, el robot debe especificar un solo destino y no las coordenadas de la reunión. 
- Si su bot inicia una llamada con varios participantes, una reunión ad hoc se configura en segundo plano y todos los usuarios se une a la conferencia. Si se especifican las coordenadas de la reunión, una llamada entre varias entidades está configurada, incluso si no hay solo un destino.

Una llamada puede iniciar como punto a punto y pasar a varios participantes. Una conferencia se aprovisiona automáticamente y los medios se redestinar a la conferencia. El robot puede iniciar escalación invitando a otras personas, siempre que el robot tenga el permiso de llamada del grupo de inicio. Si se inicia la escalación por otro participante y el robot no tiene permiso de unirse a llamada de grupo, su bot se elimina de la llamada.

> **Importante:** Cuando se cambie una llamada de punto a punto a varios participantes, no todas las características de varios participantes están disponibles. Específicamente, el robot no recibirá actualizaciones de la lista de participantes.

## <a name="signaling"></a>Señalización

### <a name="incoming-call"></a>Llamada entrante

Para recibir una llamada entrante, debe registrar el robot realiza la llamada. Cuando el robot recibe la notificación entrante, tiene las siguientes opciones.

| Método                              | Descripción                                  |
|:------------------------------------|:---------------------------------------------|
| [Respuesta](../api/call-answer.md)     | Responder a la llamada entrante.                    |
| [Reject](../api/call-reject.md)     | Rechazar y colgar la llamada.                  |
| [Redirigir](../api/call-redirect.md) | Redirigir la llamada.                           |

El robot puede redirigir la llamada a otro usuario o un robot. El robot también puede redirigir al correo de voz de un usuario.

![Imagen que muestra un bot redirigir una llamada a un correo de voz](https://cdn.graph.office.net/prod/GraphDocuments/en-us/concepts/images/call-handling.png)

> **Importante:** Redirigir o realizar llamadas salientes a RTC no se admite actualmente.

### <a name="in-call"></a>En la llamada

Operaciones para el robot están disponibles en el objeto de llamada. Estos afectan al robot como del participante en la llamada.

| Método                                                            | Descripción                                  |
|:------------------------------------------------------------------|:---------------------------------------------|
| [Desactivación de audio](../api/call-mute.md)                                       | Silenciar self en la llamada.                       |
| [Reactivar audio](../api/call-unmute.md)                                   | Reactivar self en la llamada.                     |
| [UpdateMetadata](../api/call-updatemetadata.md)                   | Actualizar los metadatos para sí mismo en la lista de participantes.          |
| [ChangeScreenSharingRole](../api/call-changescreensharingrole.md) | Iniciar y detener el uso compartido de pantalla en la llamada.   |

Para interactuar con otros participantes en la llamada, utilice el objeto de los participantes.

| Método                                                            | Descripción                                  |
|:------------------------------------------------------------------|:---------------------------------------------|
| [Participantes de la lista](../api/call-list-participants.md)             | Obtener una colección de objetos de participantes.         |
| [Invitar a participantes](../api/participant-invite.md)               | Invitar a participantes a la llamada activa.      |
| [Desactivar todos los participantes](../api/participant-muteall.md)            | Silenciar a todos los participantes de la llamada.           |

## <a name="media"></a>Medio.

Procesamiento de medios se administra a través de la plataforma de multimedia en tiempo real de Microsoft. La plataforma de multimedia en tiempo real ayuda a bots participar en reuniones y llamadas de audio y vídeo de Microsoft Teams. Permite bots en tiempo real a participar en llamadas de punto a punto y entre varias partes.

Cuando el robot responde a una llamada entrante o se une a una llamada nueva o existente, debe indicar a la plataforma de multimedia en tiempo real cómo se controlarán los medios. Si va a crear un sistema de respuesta interactiva de voz (IVR), puede descargar el audio costoso los componentes de procesamiento a los medios de servicio hospedado de Microsoft. Si su bot requiere acceso directo a las secuencias multimedia, le ofrecemos una opción de medios de aplicación hospeda a través del SDK de multimedia en tiempo real.

### <a name="service-hosted-media"></a>Hospedado por el servicio de medios

Bots puede administrar el flujo de trabajo y descargar el procesamiento de audio a la plataforma de multimedia en tiempo real de Microsoft. Con medios hospedado por el servicio, tiene varias opciones para implementar y alojar el robot. Considere el uso de uno de los disponibles [SDK](https://developer.microsoft.com/graph/code-samples-and-sdks). Un robot hospedado por el servicio de medios puede implementarse como un servicio sin estado como no procesa medios localmente.

| Método                                                        | Descripción                                             |
|:--------------------------------------------------------------|:--------------------------------------------------------|
| [PlayPrompt](../api/call-playprompt.md)                       | Reproducir un clip de audio para el usuario.                         |
| [Registro](../api/call-record.md)                               | Opcionalmente, reproducir un símbolo del sistema y registre un clip de audio.      |
| [SubscribeToTone](../api/call-subscribetotone.md)             | Suscribirse a tonos DTMF desde el usuario.                  |
| [CancelMediaProcessing](../api/call-cancelmediaprocessing.md) | Cancelar cualquier media ya procesamiento en cola.             |

### <a name="application-hosted-media"></a>Aplicación hospedada de medios

Para que el robot obtener acceso directo a los medios, el robot necesita el permiso de acceso a medios. La biblioteca de medios en tiempo real y el SDK con estado le ayuda a crear multimedia en tiempo real enriquecidos bots de llamada. Un robot de aplicación hospedada debe estar hospedado en un entorno de Windows. [Aplicación hospedada ejemplos de medios](https://github.com/microsoftgraph/microsoft-graph-comms-samples) muestran cómo crear el robot en varias plataformas de Azure (incluidos los servicios de nube y servicio de Fabric).

Puede usar el [SDK de Microsoft Graph llamadas](https://microsoftgraph.github.io/microsoft-graph-comms-samples/docs/articles/index.html) para simplificar la creación de bots. El SDK proporciona funcionalidad para administrar los Estados de los recursos en la memoria y en la pila de medios de los desarrolladores de bot de extracción.

El SDK de medios permite que el robot Enviar y recibir el uso compartido de audio, vídeo y vídeo-based pantalla contenido. Uso compartido de pantalla de vídeo se modela como un canal de vídeo. El robot puede suscribirse a los canales de audio mixto y varios canales de vídeo. Para el canal de vídeo, el robot tiene una opción para enviar y recibir vídeo como una secuencia H.264 codificada o descodificadas marcos sin procesar.

> **Nota:** No puede utilizar la API Microsoft.Graph.Calls.Media para registrar o en caso contrario, conservar el contenido de medios de llamadas o reuniones que obtiene acceso su bot.

## <a name="see-also"></a>Vea también

[Las llamadas y ejemplos de API de reuniones en línea](https://github.com/microsoftgraph/microsoft-graph-comms-samples/)

[Problemas conocidos](/graph/known-issues#calls-and-online-meetings)