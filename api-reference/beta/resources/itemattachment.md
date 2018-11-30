---
title: Tipo de recurso itemAttachment
description: Un contacto, evento o mensaje que está unido a otro evento,
ms.openlocfilehash: fd8638a7d263c2ebbe09c77f717af989e1dd5a0e
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088570"
---
# <a name="itemattachment-resource-type"></a>Tipo de recurso itemAttachment

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Un contacto, evento o mensaje que está unido a otro [evento](../resources/event.md), [mensaje](../resources/message.md), [tarea de Outlook](../resources/outlooktask.md)o [Publicar](../resources/post.md).  

Derivado de [attachment](attachment.md).

## <a name="methods"></a>Métodos

| Método       | Tipo de valor devuelto  |Descripción|
|:---------------|:--------|:----------|
|[Get](../api/attachment-get.md) | [itemAttachment](itemattachment.md) |Lee las propiedades y relaciones del objeto itemAttachment.|
|[Delete](../api/attachment-delete.md) | None |Elimina el objeto itemAttachment. |

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|contentType|String|El tipo de contenido de los datos adjuntos.|
|id|String| El identificador de los datos adjuntos.|
|isInline|Boolean|Se establece en true si los datos adjuntos están insertados, como una imagen incrustada en el cuerpo del elemento.|
|lastModifiedDateTime|DateTimeOffset|Última fecha y hora en que se modificaron los datos adjuntos.|
|name|String|Nombre para mostrar de los datos adjuntos.|
|size|Int32|El tamaño en bytes de los datos adjuntos.|

## <a name="relationships"></a>Relaciones
| Relación | Tipo   |Descripción|
|:---------------|:--------|:----------|
|item|[OutlookItem](outlookitem.md)|El contacto adjunto, mensaje o evento. Propiedad de navegación.|

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [
    "item"
  ],
  "@odata.type": "microsoft.graph.itemAttachment"
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
  "description": "itemAttachment resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
