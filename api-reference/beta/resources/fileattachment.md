---
title: Tipo de recurso fileAttachment
description: Un archivo (como un archivo de texto o un documento de Word) adjunto a un evento
localization_priority: Normal
ms.openlocfilehash: 7f7270bd5392e2d880daeb45491f4c65e9fca198
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27869282"
---
# <a name="fileattachment-resource-type"></a>Tipo de recurso fileAttachment

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Un archivo (como un archivo de texto o un documento de Word) adjunto a un [evento](../resources/event.md), [mensaje](../resources/message.md), [tarea de Outlook](../resources/outlooktask.md)o [Publicar](../resources/post.md). La propiedad **contentBytes** contiene el contenido con codificación base64 del archivo.  

Al crear un archivo adjunto, incluya lo siguiente en el cuerpo de la solicitud:

* `"@odata.type": "#microsoft.graph.fileAttachment"`
* Las propiedades requeridas **name** y **contentBytes**.

Derivadas de [attachment](attachment.md).

## <a name="methods"></a>Métodos

| Método       | Tipo de valor devuelto  |Descripción|
|:---------------|:--------|:----------|
|[Get](../api/attachment-get.md) | [fileAttachment](fileattachment.md) |Lea las propiedades y las relaciones del objeto fileAttachment.|
|[Eliminar](../api/attachment-delete.md) | Ninguno |Elimine el objeto fileAttachment. |

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|contentBytes|Binario|El contenido del archivo codificado en base64.|
|contentId|String|El identificador de los datos de adjuntos del almacén de Exchange.|
|contentLocation|String|El identificador uniforme de recursos (URI) que corresponde a la ubicación del contenido de los datos adjuntos.|
|contentType|String|El tipo de contenido de los datos adjuntos.|
|id|String|El identificador de los datos adjuntos.|
|isInline|Boolean|Se establece en true si se trata de datos adjuntos en línea.|
|lastModifiedDateTime|DateTimeOffset|La fecha y hora de la última modificación de los datos adjuntos.|
|name|String|El nombre que representa el texto que aparece debajo del icono que representa el archivo adjunto insertado. No tiene que ser el nombre de archivo real.|
|size|Int32|El tamaño en bytes de los datos adjuntos.|

## <a name="relationships"></a>Relaciones
Ninguno


## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.fileAttachment"
}-->

```json
{
  "contentBytes": "binary",
  "contentId": "string",
  "contentLocation": "string",
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
  "description": "fileAttachment resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
