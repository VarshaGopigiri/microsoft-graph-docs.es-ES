---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Archivo
ms.openlocfilehash: 2201533457863c3cac6b7a9463f80e37bd5a569a
ms.sourcegitcommit: abf4b739257e3ffd9d045f783ec595d846172590
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2018
ms.locfileid: "23267468"
---
# <a name="file-resource-type"></a>Tipo de recurso File

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
| hashes   | [Hashes](hashes.md) | Algoritmos hash de contenido binario del archivo, si están disponibles. Solo lectura.                                                                                    |
| mimeType | cadena                  | Tipo MIME para el archivo. Viene determinado por la lógica del servidor y puede que no sea el valor proporcionado cuando el archivo se cargó. Solo lectura. |

## <a name="remarks"></a>Comentarios 

Para obtener más información sobre las facetas de un objeto DriveItem, consulte [DriveItem](driveitem.md).

<!-- {
  "type": "#page.annotation",
  "description": "The file facet describes properties of a file",
  "keywords": "file,item,facet",
  "section": "documentation",
  "tocPath": "Facets/File"
} -->
