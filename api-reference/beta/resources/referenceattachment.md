---
title: Tipo de recurso referenceAttachment
description: 'Un vínculo a una carpeta o archivo (como un archivo de texto o un documento de Word) en un OneDrive para la unidad de negocio en la nube o en otras ubicaciones de almacenamiento compatibles, adjunto '
localization_priority: Normal
ms.openlocfilehash: 6a334b303bea7aff768733434b9ba882de237a12
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27880055"
---
# <a name="referenceattachment-resource-type"></a>Tipo de recurso referenceAttachment

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Un vínculo a una carpeta o archivo (como un archivo de texto o un documento de Word) en un OneDrive para la unidad de negocio en la nube, u otra compatible con ubicaciones de almacenamiento conectadas a un [evento](../resources/event.md), [mensaje](../resources/message.md), [tarea de Outlook](../resources/outlooktask.md)o [registrar](../resources/post.md) .

Derivado de [attachment](attachment.md).

## <a name="methods"></a>Métodos

| Método       | Tipo de valor devuelto  |Descripción|
|:---------------|:--------|:----------|
|[Get](../api/attachment-get.md) | [referenceAttachment](referenceattachment.md) |Lee las propiedades y relaciones del objeto referenceAttachment.|
|[Delete](../api/attachment-delete.md) | None |Elimina el objeto referenceAttachment. |

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|contentType|String|El tipo de contenido de los datos adjuntos. Opcional.|
|id|String|Identificador de los datos adjuntos  Solo lectura.|
|isFolder|Booleano|Especifica si los datos adjuntos son un vínculo a una carpeta. Debe establecer como true si **sourceUrl** es un vínculo a una carpeta. Opcional.|
|isInline|Boolean|Se establece en true si los datos adjuntos aparecen en insertados en el cuerpo del objeto embedding. Opcional.|
|lastModifiedDateTime|DateTimeOffset|La fecha y hora de la última modificación de los datos adjuntos. El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`. Opcional.|
|name|Cadena|El texto que se muestra debajo del icono que representa al archivo adjunto incrustado. Esto no necesita ser el nombre de archivo real. Necesario.|
|permiso|ReferenceAttachmentPermissions|Especifica los permisos concedidos para los datos adjuntos con el tipo de proveedor en **tipo de proveedor**. Los valores posibles son: `other`, `view`, `edit`, `anonymousView`, `anonymousEdit`, `organizationView` y `organizationEdit`. Opcional.|
|previewUrl|Cadena|Se aplica a un adjunto de referencia de una imagen - dirección URL para obtener una imagen de vista previa. Use **thumbnailUrl** y **previewUrl** sólo cuando **sourceUrl** identifica un archivo de imagen. Opcional.|
|tipo de proveedor|ReferenceAttachmentProviders|El tipo de proveedor que admite un dato adjunto de este contentType. Los valores posibles son: `other`, `oneDriveBusiness`, `oneDriveConsumer` y `dropbox`. Opcional.|
|size|Int32|El tamaño de los metadatos en bytes que se almacenan en el mensaje para los datos adjuntos de referencia. Este valor no indica el tamaño del archivo real. Opcional.|
|sourceUrl|Cadena|URL para obtener el contenido del archivo adjunto. Si se trata de una dirección URL a una carpeta, a continuación, para que la carpeta que se muestre correctamente en Outlook o Outlook en la web, establecer **isFolder** en true. Necesario.|
|thumbnailUrl|Cadena|Se aplica a un adjunto de referencia de una imagen - dirección URL para obtener una imagen en miniatura. Use **thumbnailUrl** y **previewUrl** sólo cuando **sourceUrl** identifica un archivo de imagen. Opcional.|

## <a name="relationships"></a>Relaciones
Ninguno



## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.referenceAttachment"
}-->

```json
{
  "contentType": "string",
  "id": "string (identifier)",
  "isFolder": true,
  "isInline": true,
  "lastModifiedDateTime": "String (timestamp)",
  "name": "string",
  "permission": "string",
  "previewUrl": "string",
  "providerType": "string",
  "size": 1024,
  "sourceUrl": "string",
  "thumbnailUrl": "string"
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
