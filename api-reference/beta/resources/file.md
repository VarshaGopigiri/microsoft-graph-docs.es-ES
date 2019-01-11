---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Archivo
localization_priority: Normal
ms.openlocfilehash: bd2b0fba75ef54586dcfe8b69043669b0681f6b2
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27816329"
---
# <a name="file-resource-type"></a>Tipo de recurso File

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

El recurso **File** agrupa en una sola estructura los elementos de datos relacionados con archivos.

Si un [**DriveItem**](driveitem.md) tiene una faceta **file** no null, el elemento representa un archivo. Además de otras propiedades, los archivos tienen una relación **content** que contiene la secuencia de bytes del archivo.

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [ ],
  "@odata.type": "microsoft.graph.file"
}-->

```json
{
  "hashes": {"@odata.type": "microsoft.graph.hashes"},
  "mimeType": "string"
}
```

## <a name="properties"></a>Propiedades

| Propiedad | Tipo                    | Descripción                                                                                                                                      |
|:---------|:------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------|
| algoritmos hash   | [HashesType](hashes.md) | Algoritmos hash de contenido binario del archivo, si están disponibles. Solo lectura.                                                                                    |
| mimeType | string                  | Tipo MIME para el archivo. Viene determinado por la lógica del servidor y puede que no sea el valor proporcionado cuando el archivo se cargó. Solo lectura. |

## <a name="remarks"></a>Observaciones 

Para obtener más información sobre las facetas de un objeto DriveItem, consulte [DriveItem](driveitem.md).

<!-- {
  "type": "#page.annotation",
  "description": "The file facet describes properties of a file",
  "keywords": "file,item,facet",
  "section": "documentation",
  "tocPath": "Facets/File"
} -->
