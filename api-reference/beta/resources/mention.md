---
title: Mencione el tipo de recurso
description: 'Representa una notificación a una persona en función de la dirección de correo electrónico de la persona. Este tipo de notificación es también conocida como '
ms.openlocfilehash: 7e70c6a84665b474ea4d8421f60e78687ebb49b6
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083891"
---
# <a name="mention-resource-type"></a>Mencione el tipo de recurso

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Representa una notificación a una persona en función de la dirección de correo electrónico de la persona. Este tipo de notificación es también conocida como @ menciones.

El recurso de [mensaje](../resources/message.md) admite **mencione**. Incluye una propiedad **mentionsPreview** que indica si el usuario ha iniciado sesión se menciona en esa instancia de mensaje. También incluye la propiedad de navegación **menciones** , que admite obtener detalles de una mención o eliminación de una mención en esa instancia.

Al crear un mensaje, una aplicación puede crear una mención en la misma `POST` solicitud mediante la inclusión de la mención en la propiedad **menciones** . Uso de un `GET` solicitar con la `$filter` parámetro de consulta, una aplicación puede devolver todos los mensajes en el buzón del usuario que ha iniciado sesión que indiquen el usuario. A `GET` solicitar con la `$expand` consulta parámetro permite que la aplicación expanda todas las menciones en un mensaje específico.

Este mecanismo de permitir a una aplicación establecer y obtener menciones en los mensajes permite notificaciones ligero, donde el usuario que realiza la mención puede permanecer en el contexto existente (por ejemplo, para redactar el cuerpo de un mensaje) mientras la aplicación establece la propiedad **menciones** subyacente . Mencionado personas pueden descubrir fácilmente si y donde se mencionan a través de `GET` las solicitudes con la `$filter` o `$expand` parámetro de consulta.  

Por ejemplo, en el cliente de correo de Outlook, cuando un usuario escribe `@` al escribir un mensaje, Outlook permite al usuario seleccionar o escribir un nombre para llevar a cabo la mención @. Outlook establece la propiedad **menciones** antes de que se crea y se envía el mensaje o el evento. Outlook también usa `GET` operaciones con `$filter` y `$expand` para permitir que el usuario ha iniciado sesión buscar mensajes que indiquen el usuario, alertar al usuario a elementos de acción o discusiones, lo que permite una respuesta más rápida.


## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.mention"
}-->

```json
{
  "application": "string",
  "clientReference": "string",
  "createdBy": {"@odata.type": "microsoft.graph.emailAddress"},
  "createdDateTime": "DateTimeOffset",
  "deepLink": "string",
  "id": "string (identifier)",
  "mentioned": {"@odata.type": "microsoft.graph.emailAddress"},
  "mentionText": "string",
  "serverCreatedDateTime": "DateTimeOffset"
}

```
## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|aplicación | String | El nombre de la aplicación donde se creó la mención. Opcional. No utilizado y el valor predeterminado como null para el **mensaje**. |
|clientReference | String | Un identificador único que representa a un elemento primario de la instancia de recurso. Opcional. No utilizado y el valor predeterminado como null para el **mensaje**. |
|createdBy  | [emailAddress](../resources/emailaddress.md) | La información de correo electrónico del usuario que realizó la mención. |
|createdDateTime  |DateTimeOffset |La fecha y hora en que se creó la mención en el cliente. |
|deepLink | String | Un vínculo web profundo para el contexto de la mención en la instancia de recurso. Opcional. No utilizado y el valor predeterminado como null para el **mensaje**. |
|id | String| El identificador único de una mención en una instancia de recursos.|
|mencionado | [emailAddress](../resources/emailaddress.md) | La información de correo electrónico de la persona se ha mencionado. Obligatorio. |
|mentionText | Cadena | Opcional. No utilizado y el valor predeterminado como null para el **mensaje**. Para obtener las menciones que en un mensaje, vea la propiedad **bodyPreview** del mensaje en su lugar. |
|serverCreatedDateTime | DateTimeOffset | La fecha y hora en que se creó la mención en el servidor. Opcional. No utilizado y el valor predeterminado como null para el **mensaje**. |

## <a name="relationships"></a>Relaciones
Ninguno


## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[POST](../api/user-sendmail.md#request-2) y enviar | Ninguno | Crear y enviar menciones como parte de un nuevo mensaje.|
|[Post](../api/user-post-messages.md#request-2) a un borrador de la nueva | [mensaje](../resources/message.md) que contiene uno o más objetos de **mencionar** . | Crear un borrador de un nuevo mensaje e incluir uno o más objetos de **mencionar** .|
|[Obtener](../api/user-list-messages.md#request-2) mensajes mencionarme | Colección [message](../resources/message.md) | Obtener todos los mensajes en el buzón del usuario que ha iniciado sesión que contienen un **indiquen** de este usuario.|
|[Obtener](../api/message-get.md#request-2) un mensaje y sus menciones | Colección [message](../resources/message.md) | Recibe un mensaje y expanda los detalles de cada **mencionar** en el mensaje.|
|[Eliminar](../api/message-delete.md#request-2) una mención | Ninguno |Elimina la mención especificada en el mensaje especificado en el buzón del usuario que ha iniciado sesión. |

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "mention resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->