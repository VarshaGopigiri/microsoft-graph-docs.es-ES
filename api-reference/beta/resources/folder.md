---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Carpeta
ms.openlocfilehash: 834b2cd7c81a947ca1e6d4619f39a8533677e6c3
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089207"
---
# <a name="folder-resource-type"></a>Tipo de recurso Folder

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

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
| **childCount** | Int64          | Número de elementos secundarios que se incluyen inmediatamente dentro de este contenedor.
| **view**       | [folderView][] | Una colección de propiedades que definen la vista recomendada de la carpeta.


## <a name="remarks"></a>Comentarios 

Para obtener más información sobre las facetas de un objeto DriveItem, consulte [DriveItem][].

[folderView]: folderview.md
[DriveItem]: driveitem.md

<!-- {
  "type": "#page.annotation",
  "description": "folder resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
