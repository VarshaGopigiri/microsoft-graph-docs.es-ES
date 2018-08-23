---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: UploadSession
ms.openlocfilehash: 6c0ffebf0d973afe72ab82de9782c1f54e2342dd
ms.sourcegitcommit: abf4b739257e3ffd9d045f783ec595d846172590
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2018
ms.locfileid: "20502128"
---
# <a name="uploadsession-resource"></a>Recurso UploadSession

El recurso **UploadSession** proporciona información sobre cómo cargar archivos grandes en las bibliotecas de documentos de OneDrive, OneDrive para la Empresa o SharePoint.

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [ "uploadUrl", "nextExpectedRanges" ],
  "@odata.type": "microsoft.graph.uploadSession"
}-->

```json
{
  "uploadUrl": "https://sn3302.up.1drv.com/up/fe6987415ace7X4e1eF866337",
  "expirationDateTime": "2015-01-29T09:21:55.523Z",
  "nextExpectedRanges": ["0-"]
}
```

## <a name="properties"></a>Propiedades


| Propiedad       | Tipo              |Descripción
|:-------------------|:------------------|:------------------------------------
| expirationDateTime | DateTimeOffset    | La fecha y hora en UTC en que caducará la sesión de carga. Debe cargarse el archivo completo antes de esta fecha de expiración.
| nextExpectedRanges | Colección String | Una colección de intervalos de bytes que el servidor no encuentra para el archivo. Estos intervalos están indexados con cero y tienen el formato "inicio-fin" (p. ej. "0-26" para indicar los 27 primeros bytes del archivo).
| uploadUrl          | Cadena            | El extremo de la dirección URL que acepta las solicitudes PUT de los intervalos de bytes del archivo.

## <a name="see-also"></a>Consulte también

- [Cargar archivos de gran tamaño con una sesión de carga](../api/driveitem_createuploadsession.md)

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "UploadSession is used to provide information about large file uploads.",
  "section": "documentation",
  "tocPath": "Resources/UploadSession"
} -->
