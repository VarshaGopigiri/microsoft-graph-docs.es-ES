---
title: Tipo de recurso referenceAttachment
description: Vínculo a un archivo (como un archivo de texto o un documento de Word) en una unidad en la nube de OneDrive para la Empresa o en otras ubicaciones de almacenamiento compatibles asociadas a un evento, mensaje o publicación.
ms.openlocfilehash: b3604791c7e06d4f765a81263e1f6afe51743390
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27032401"
---
# <a name="referenceattachment-resource-type"></a>Tipo de recurso referenceAttachment

Vínculo a un archivo (como un archivo de texto o un documento de Word) en una unidad en la nube de OneDrive para la Empresa o en otras ubicaciones de almacenamiento compatibles asociadas a un evento, mensaje o publicación.

Derivado de [attachment](attachment.md).

## <a name="methods"></a>Métodos

| Método       | Tipo de valor devuelto  |Descripción|
|:---------------|:--------|:----------|
|[Get](../api/attachment-get.md) | [referenceAttachment](referenceattachment.md) |Lee las propiedades y relaciones del objeto referenceAttachment.|
|[Delete](../api/attachment-delete.md) | None |Elimina el objeto referenceAttachment. |

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|contentType|String|El tipo de contenido de los datos adjuntos.|
|id|String|Identificador de los datos adjuntos  Solo lectura.|
|isInline|Boolean|Se establece en true si los datos adjuntos aparecen en insertados en el cuerpo del objeto embedding.|
|lastModifiedDateTime|DateTimeOffset|Fecha y hora de la última modificación de los datos adjuntos. El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC. Por ejemplo, la medianoche UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`|
|name|String|Texto que aparece debajo del icono que representa al archivo adjunto incrustado. No tiene que ser el nombre de archivo real.|
|size|Int32|Tamaño en bytes de los metadatos almacenados en el mensaje del archivo adjunto. Este valor no indica el tamaño del archivo real.|

## <a name="relationships"></a>Relaciones
Ninguno



## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso

<!--{
  "blockType": "resource",
  "optionalProperties": [],
  "baseType": "microsoft.graph.attachment",
  "@odata.type": "microsoft.graph.referenceAttachment"
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
  "description": "referenceAttachment resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
