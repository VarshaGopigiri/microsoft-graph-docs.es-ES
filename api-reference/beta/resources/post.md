---
title: Tipo de recurso post
description: Representa un elemento para exponer individuales dentro de una entidad de converstaionThread.
author: dkershaw10
localization_priority: Normal
ms.prod: groups
ms.openlocfilehash: 46e33021d0929e1bd665f8256f0874e8e8c92809
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27942419"
---
# <a name="post-resource-type"></a>Tipo de recurso post

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Representa un elemento para exponer individuales dentro de una entidad de [converstaionThread](conversationthread.md) .

Incluso aunque no pueda crear una publicación de forma explícita, cualquiera de las siguientes acciones creará una publicación:

* [Responder a una publicación existente](../api/post-reply.md) 
* [Responder a un hilo existente](../api/conversationthread-reply.md) 
* [Crear un hilo en una conversación nueva](../api/group-post-threads.md)
* [Crear una conversación](../api/group-post-conversations.md)

Este recurso le permite agregar sus propios datos a las propiedades personalizadas mediante [extensiones](/graph/extensibility-overview).

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [
    "attachments",
    "extensions",
    "inReplyTo",
    "multiValueExtendedProperties",
    "singleValueExtendedProperties"
  ],
  "@odata.type": "microsoft.graph.post"
}-->

```json
{
  "body": {"@odata.type": "microsoft.graph.itemBody"},
  "categories": ["string"],
  "changeKey": "string",
  "conversationId": "string",
  "conversationThreadId": "string",
  "createdDateTime": "String (timestamp)",
  "from": {"@odata.type": "microsoft.graph.recipient"},
  "hasAttachments": true,
  "id": "string (identifier)",
  "importance": "string",
  "lastModifiedDateTime": "String (timestamp)",
  "newParticipants": [{"@odata.type": "microsoft.graph.recipient"}],
  "receivedDateTime": "String (timestamp)",
  "sender": {"@odata.type": "microsoft.graph.recipient"}
}

```
## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|body|[itemBody](itembody.md)|Los contenidos de la publicación. Esta es la propiedad predeterminada. Esta propiedad puede ser null.|
|categories|Colección String|Las categorías asociadas a la publicación. Cada categoría corresponde a la propiedad **displayName** de un [outlookCategory](outlookcategory.md) que se ha definido para un usuario.|
|changeKey|String|Identifica la versión de la publicación. Cada vez que cambia la publicación, cambia también ChangeKey. Permite que Exchange aplique los cambios a la versión correcta del objeto.|
|conversationId|String|El identificador único de la conversación. Solo lectura.|
|conversationThreadId|String|El identificador único del hilo de la conversación. Solo lectura.|
|createdDateTime|DateTimeOffset|Especifica cuándo se ha creado la publicación. El tipo DateTimeOffset representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC. Por ejemplo, medianoche UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`|
|from|[recipient](recipient.md)|Se usa en escenarios de acceso delegado. Indica quién ha publicado el mensaje en nombre de otro usuario. Esta es la propiedad predeterminada.|
|hasAttachments|Boolean|Indica si la publicación tiene al menos un dato adjunto. Esta es la propiedad predeterminada.|
|id|Cadena| Solo lectura.|
|importance | Cadena | La importancia de una entrada de grupo: `low`, `normal`, `high`. |
|lastModifiedDateTime|DateTimeOffset|Especifica cuándo se ha modificado por última vez la publicación. El tipo DateTimeOffset representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC. Por ejemplo, medianoche UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`|
|newParticipants|Colección [recipient](recipient.md)|Participantes de la conversación que se han agregado al hilo como parte de esta publicación.|
|receivedDateTime|DateTimeOffset|Especifica cuándo se ha recibido la publicación. El tipo DateTimeOffset representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC. Por ejemplo, medianoche UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`|
|sender|[recipient](recipient.md)|Contiene la dirección del remitente. El valor de Sender se supone que es la dirección del usuario autenticado en el caso de que no se especifique ningún Sender. Esta es la propiedad predeterminada.|

## <a name="relationships"></a>Relaciones
| Relación | Tipo   |Descripción|
|:---------------|:--------|:----------|
|attachments|Colección [attachment](attachment.md)|La colección de datos adjuntos de [fileAttachment](fileattachment.md), [itemAttachment](itemattachment.md)y [referenceAttachment](referenceattachment.md) para la publicación. Solo lectura. Admite valores NULL.|
|extensions|Colección [Extension](extension.md)|La colección de extensiones abiertas definidas para la publicación. Solo lectura. Admite valores NULL.|
|inReplyTo|[Post](post.md)|La entrada anterior que esta entrada es responder en el [conversationThread](conversationthread.md). Solo lectura.|
|multiValueExtendedProperties|Colección [multiValueLegacyExtendedProperty](multivaluelegacyextendedproperty.md)| La colección de propiedades extendidas de varios valores definidas para la publicación. Solo lectura. Admite valores NULL.|
|singleValueExtendedProperties|Colección [singleValueLegacyExtendedProperty](singlevaluelegacyextendedproperty.md)| La colección de propiedades extendidas de valor único definidas para la publicación. Solo lectura. Admite valores NULL.|

## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Enumerar publicaciones](../api/conversationthread-list-posts.md) | [post](post.md) |Obtenga las publicaciones del hilo especificado. |
|[Obtener publicación](../api/post-get.md) | [post](post.md) |Obtenga las propiedades y relaciones de una publicación de un hilo determinado.|
|[Responder](../api/post-reply.md)|Ninguno|Responda a una publicación y agregue una nueva publicación al hilo especificado de una conversación de grupo.|
|[Reenviar](../api/post-forward.md)|Ninguno|Reenvíe una publicación a un destinatario.|
|**Datos adjuntos**| | |
|[Enumerar datos adjuntos](../api/post-list-attachments.md) |Colección [attachment](attachment.md)| Obtener todos los datos adjuntos en una publicación.|
|[Agregar datos adjuntos](../api/post-post-attachments.md) |[dato adjunto](attachment.md)| Agrega datos adjuntos a una publicación. |
|**Extensiones abiertas**| | |
|[Crear extensión abierta](../api/opentypeextension-post-opentypeextension.md) |[openTypeExtension](opentypeextension.md)| Crea una extensión abierta y agrega propiedades personalizadas en una instancia nueva o un recurso existente.|
|[Obtener extensión abierta](../api/opentypeextension-get.md) |Colección [openTypeExtension](opentypeextension.md)| Obtiene una extensión abierta identificada por el nombre de extensión.|
|**Extensiones de esquema**| | |
|[Agregar valores de extensión de esquema](/graph/extensibility-schema-groups) || Cree una definición de extensión de esquema y, después, úsela para agregar datos escritos personalizados a un recurso.|
|**Propiedades extendidas**| | |
|[Crear propiedad extendida de valor único](../api/singlevaluelegacyextendedproperty-post-singlevalueextendedproperties.md) |[post](post.md)  |Cree una o varias propiedades extendidas de valor único en una publicación nueva o existente.   |
|[Obtener publicación con propiedad extendida de valor único](../api/singlevaluelegacyextendedproperty-get.md)  | [post](post.md) | Obtenga publicaciones que contienen una propiedad extendida de valor único mediante el uso de `$expand` o `$filter`. |
|[Crear propiedad extendida de varios valores](../api/multivaluelegacyextendedproperty-post-multivalueextendedproperties.md) | [post](post.md) | Cree una o varias propiedades extendidas de varios valores en una publicación nueva o existente.  |
|[Obtener publicación con propiedad extendida de varios valores](../api/multivaluelegacyextendedproperty-get.md)  | [post](post.md) | Obtenga una publicación que contiene una propiedad extendida de varios valores mediante el uso de `$expand`. |

## <a name="see-also"></a>Vea también

- [Agregar datos personalizados a los recursos mediante extensiones](/graph/extensibility-overview)
- [Agregar datos personalizados a los usuarios mediante extensiones abiertas](/graph/extensibility-open-users)
- [Agregar datos personalizados a los grupos mediante extensiones de esquema](/graph/extensibility-schema-groups)


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "post resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
