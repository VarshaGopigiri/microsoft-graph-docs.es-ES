---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Carpeta
ms.openlocfilehash: 664597297700f7af096ef30cfbd5342a45a6c157
ms.sourcegitcommit: 7aea7a97e36e6d146214de3a90fdbc71628aadba
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/28/2017
---
# <a name="folder-resource-type"></a>Tipo de recurso Folder

El recurso **Folder** agrupa en una sola estructura los datos relacionados con carpetas de un elemento. 
Los objetos [**DriveItems**](driveitem.md) con una faceta **folder** que no sea NULL son contenedores de otros objetos DriveItems.

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.folder"
}-->

```json
{
  "childCount": 1024,
  "view": { "@odata.type": "microsoft.graph.folderView" }
}
```

## <a name="properties"></a>Propiedades

| Propiedad       | Tipo           | Descripción
|:---------------|:---------------|:-------------------------------------------
| **childCount** | Int64          | Número de elementos secundarios que se incluyen inmediatamente dentro de este contenedor.
| **view**       | [folderView][] | Una colección de propiedades que definen la vista recomendada de la carpeta.

## <a name="remarks"></a>Comentarios 

Para obtener más información sobre las facetas de un objeto DriveItem, consulte [DriveItem][].

[folderView]: folderView.md
[DriveItem]: driveItem.md

<!-- {
  "type": "#page.annotation",
  "description": "The Folder facet describes properties of a folder",
  "keywords": "folder,item,facet",
  "section": "documentation",
  "tocPath": "Facets/Folder"
} -->
