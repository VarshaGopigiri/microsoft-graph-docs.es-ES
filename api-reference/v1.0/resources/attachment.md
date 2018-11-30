---
title: Tipo de recurso attachment
description: Puede agregar contenido relacionado a un evento
ms.openlocfilehash: 418d8d4e60d12fed5a54f994e14e996c65731926
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030591"
---
# <a name="attachment-resource-type"></a>Tipo de recurso attachment

Puede agregar contenido relacionado a un [evento](../resources/event.md), [mensaje](../resources/message.md) o [publicación](../resources/post.md) en forma de datos adjuntos.

**datos adjuntos** es el recurso base para los siguientes tipos de datos adjuntos derivados:

* Un archivo (recurso [fileAttachment](../resources/fileattachment.md))
* Un elemento (contacto, evento o mensaje, representado por un recurso [itemAttachment](../resources/itemattachment.md))
* Un vínculo a un archivo (recurso [referenceAttachment](../resources/referenceattachment.md))


## <a name="methods"></a>Métodos

Los métodos siguientes se aplican a cualquiera de los tipos derivados de los datos adjuntos (**fileAttachment**, **itemAttachment** o **referenceAttachment**).

| Método       | Tipo de valor devuelto  |Descripción|
|:---------------|:--------|:----------|
|[Obtener datos adjuntos](../api/attachment-get.md) | [dato adjunto](attachment.md) |Lea las propiedades y relaciones de un archivo adjunto, conectado a un evento, mensaje o publicación.|
|[Agregar datos adjuntos a un evento](../api/event-post-attachments.md) | [attachment](attachment.md) |Agregue un archivo, elemento o vínculo adjunto a un evento.|
|[Agregar datos adjuntos a un mensaje](../api/message-post-attachments.md) | [attachment](attachment.md) |Agregue un archivo, elemento o vínculo adjunto a un mensaje.|
|[Agregar datos adjuntos a una publicación](../api/post-post-attachments.md) | [attachment](attachment.md) |Agregue un archivo, elemento o vínculo adjunto a una publicación.|
|[Mostrar los datos adjuntos de un evento](../api/event-list-attachments.md) | Colección [attachment](attachment.md) | Obtenga una lista de los datos adjuntos de un evento. |
|[Mostrar los datos adjuntos de un mensaje](../api/message-list-attachments.md) | Colección [attachment](attachment.md) | Obtenga una lista de los datos adjuntos de un mensaje. |
|[Mostrar los datos adjuntos de una publicación](../api/post-list-attachments.md) | Colección [attachment](attachment.md) | Obtenga una lista de los datos adjuntos de una publicación. |
|[Eliminar](../api/attachment-delete.md) | Ninguno |Eliminar datos adjuntos en un evento, un mensaje o una publicación. |

## <a name="properties"></a>Propiedades

A continuación se muestran las propiedades base de cualquier recurso de datos adjuntos. Haga referencia al tipo específico de dato adjunto ([fileAttachment](../resources/fileattachment.md), [itemAttachment](../resources/itemattachment.md) o [referenceAttachment](../resources/referenceattachment.md)) para ver propiedades adicionales.

| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|contentType|String|El tipo MIME.|
|id|String| Solo lectura.|
|isInline|Boolean|`true` si los datos adjuntos son datos adjuntos en línea; de lo contrario, `false`.|
|lastModifiedDateTime|DateTimeOffset|El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC. Por ejemplo, medianoche UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`|
|name|String|El nombre de archivo de los datos adjuntos.|
|size|Int32|La longitud en bytes de los datos adjuntos.|

## <a name="relationships"></a>Relaciones
Ninguno

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "baseType": "microsoft.graph.entity",
  "abstract": true,
  "optionalProperties": [

  ],
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.attachment"
}-->

```json
{
  "contentType": "string",
  "id": "string (identifier)",
  "isInline": true,
  "lastModifiedDateTime": "String (timestamp)",
  "name": "string",
  "size": 1024
}

```


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "attachment resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
