---
title: Tipo de recurso attachment
description: Puede agregar contenido relacionado a un evento
localization_priority: Normal
ms.openlocfilehash: 5648194b0f636c8757d1b20c492abc099dce377d
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27842794"
---
# <a name="attachment-resource-type"></a>Tipo de recurso attachment

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Puede agregar contenido relacionado a un [evento](../resources/event.md), [mensaje](../resources/message.md), [tarea de Outlook](../resources/outlooktask.md)o [registrar](../resources/post.md) en el formulario de datos adjuntos.

**datos adjuntos** es el recurso base para los siguientes tipos de datos adjuntos derivados:

* Un archivo (recurso [fileAttachment](../resources/fileattachment.md))
* Un elemento (contacto, evento o mensaje, representado por un recurso [itemAttachment](../resources/itemattachment.md))
* Un vínculo a un archivo (recurso [referenceAttachment](../resources/referenceattachment.md))

## <a name="methods"></a>Métodos

Los métodos siguientes se aplican a cualquiera de los tipos derivados de los datos adjuntos (**fileAttachment**, **itemAttachment** o **referenceAttachment**).

| Método       | Tipo de valor devuelto  |Descripción|
|:---------------|:--------|:----------|
|[Obtener datos adjuntos](../api/attachment-get.md) | [dato adjunto](attachment.md) |Lea las propiedades y relaciones de los datos adjuntos, conectado a un evento, mensaje, tarea de Outlook o posterior.|
|[Agregar datos adjuntos a un evento](../api/event-post-attachments.md) | [attachment](attachment.md) |Agregue un archivo, elemento o vínculo adjunto a un evento.|
|[Agregar datos adjuntos a un mensaje](../api/message-post-attachments.md) | [attachment](attachment.md) |Agregue un archivo, elemento o vínculo adjunto a un mensaje.|
|[Agregar datos adjuntos a una tarea de Outlook](../api/outlooktask-post-attachments.md) | [attachment](attachment.md) |Agregar un archivo, el elemento o los datos adjuntos de vínculo a una tarea de Outlook.|
|[Agregar datos adjuntos a una publicación](../api/post-post-attachments.md) | [attachment](attachment.md) |Agregue un archivo, elemento o vínculo adjunto a una publicación.|
|[Mostrar los datos adjuntos de un evento](../api/event-list-attachments.md) | Colección [attachment](attachment.md) | Obtenga una lista de los datos adjuntos de un evento. |
|[Mostrar los datos adjuntos de un mensaje](../api/message-list-attachments.md) | Colección [attachment](attachment.md) | Obtenga una lista de los datos adjuntos de un mensaje. |
|[Datos adjuntos de la lista de una tarea de Outlook](../api/outlooktask-list-attachments.md) | Colección de [datos adjuntos](attachment.md) | Obtener una lista de datos adjuntos para una tarea de Outlook. |
|[Mostrar los datos adjuntos de una publicación](../api/post-list-attachments.md) | Colección [attachment](attachment.md) | Obtenga una lista de los datos adjuntos de una publicación. |
|[Eliminar](../api/attachment-delete.md) | Ninguno |Eliminar un dato adjunto en un evento, el mensaje, la tarea de Outlook o el post. |

## <a name="properties"></a>Propiedades

A continuación se muestran las propiedades base de cualquier recurso de datos adjuntos. Haga referencia al tipo específico de dato adjunto ([fileAttachment](../resources/fileattachment.md), [itemAttachment](../resources/itemattachment.md) o [referenceAttachment](../resources/referenceattachment.md)) para ver propiedades adicionales.

| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|contentType|String|El tipo MIME.|
|id|Cadena| Solo lectura.|
|isInline|Boolean|`true` si los datos adjuntos son datos adjuntos en línea; de lo contrario, `false`.|
|lastModifiedDateTime|DateTimeOffset|El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC. Por ejemplo, medianoche UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`|
|name|String|Nombre para mostrar de los datos adjuntos. Esto no necesita ser el nombre de archivo real.|
|size|Int32|La longitud en bytes de los datos adjuntos.|

## <a name="relationships"></a>Relaciones
Ninguno

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso

<!-- {
  "blockType": "resource",
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
