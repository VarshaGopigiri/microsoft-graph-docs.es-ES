---
title: Tipo de recurso DriveItemVersion
description: El recurso **DriveItemVersion** representa una versión específica de un DriveItem.
localization_priority: Normal
ms.prod: sharepoint
ms.openlocfilehash: 5b6e9ecd2c3c8ec14958cfa2645f8fb0dbfe30e8
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27949594"
---
# <a name="driveitemversion-resource-type"></a>Tipo de recurso DriveItemVersion

El recurso **DriveItemVersion** representa una versión específica de un objeto [DriveItem](driveitem.md).


## <a name="tasks-on-driveitemversion-resources"></a>Tareas en recursos DriveItemVersion

Las tareas siguientes están disponibles para los recursos driveItemVersion.

|            Tarea común             |         Método HTTP         |
| :--------------------------------- | :-------------------------- |
| [Enumerar versiones][version-list]      | `GET /drive/items/{item-id}/versions`  |
| [Obtener versión][version-get]         | `GET /drive/items/{item-id}/versions/{version-id}`     |
| [Obtener contenido][content-get]        | `GET /drive/items/{item-id}/versions/{version-id}/content` |
| [Restaurar versión][version-restore] | `POST /drive/items/{item-id}/versions/{version-id}/restore` |

[version-list]: ../api/driveitem-list-versions.md
[version-get]: ../api/driveitemversion-get.md
[content-get]: ../api/driveitemversion-get-contents.md
[version-restore]: ../api/driveitemversion-restore.md

En la tabla anterior, los ejemplos usan `/drive`, pero hay varias solicitudes válidas.

## <a name="json-representation"></a>Representación JSON

<!--{
  "blockType": "resource",
  "baseType": "microsoft.graph.baseItemVersion",
  "@odata.type": "microsoft.graph.driveItemVersion",
  "@type.aka": "oneDrive.driveItemVersion"
}-->

```json
{
  "content": { "@odata.type": "Edm.Stream" },
  "id": "string",
  "lastModifiedBy": { "@odata.type": "microsoft.graph.identitySet" },
  "lastModifiedDateTime": "2016-01-01T15:20:01.125Z",
  "publication": { "@odata.type": "microsoft.graph.publicationFacet" },
  "size": 12356
}
```

## <a name="properties"></a>Propiedades

|      Nombre de la propiedad       |                         Tipo                         |                               Descripción                               |
| :----------------------- | :--------------------------------------------------- | :---------------------------------------------------------------------- |
| **id**                   | string                                               | El identificador de la versión. Solo lectura.                                       |
| **lastModifiedBy**       | [IdentitySet](../resources/identityset.md)           | Identidad del usuario que modificó por última vez la versión. Solo lectura.        |
| **lastModifiedDateTime** | [DateTimeOffset](../resources/timestamp.md)          | Fecha y hora de la última modificación de la versión. Solo lectura.                 |
| **publication**          | [PublicationFacet](../resources/publicationfacet.md) | Indica el estado de publicación de esta versión concreta. Solo lectura. |
| **size**                 | Int64                                                | Indica el tamaño de la secuencia de contenido para esta versión del elemento.  |
| **content**              | Secuencia                                               | La secuencia de contenido para esta versión del elemento.                        |

<!-- {
  "type": "#page.annotation",
  "description": "The version facet provides information about the properties of a file version.",
  "keywords": "version,versions,version-history,history",
  "section": "documentation",
  "tocPath": "Facets/Version"
} -->
