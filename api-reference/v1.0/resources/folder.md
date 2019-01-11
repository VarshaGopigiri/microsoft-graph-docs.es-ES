---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Carpeta
localization_priority: Normal
ms.openlocfilehash: fab5db026b47aa84f7d097a19782b70eac6b6064
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27821423"
---
# <a name="folder-resource-type"></a>Tipo de recurso Folder

El recurso **Folder** agrupa en una sola estructura los datos relacionados con carpetas de un elemento. [**DriveItems**](driveitem.md) con una faceta **folder** no null son contenedores para otros DriveItems.

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
| **childCount** | Int32          | Número de elementos secundarios que se incluyen inmediatamente dentro de este contenedor.
| **view**       | [folderView][] | Una colección de propiedades que definen la vista recomendada de la carpeta.

## <a name="remarks"></a>Comentarios 

Para obtener más información sobre las facetas de un objeto DriveItem, consulte [DriveItem][].

[folderView]: folderview.md
[DriveItem]: driveitem.md

<!-- {
  "type": "#page.annotation",
  "description": "The Folder facet describes properties of a folder",
  "keywords": "folder,item,facet",
  "section": "documentation",
  "tocPath": "Facets/Folder"
} -->
