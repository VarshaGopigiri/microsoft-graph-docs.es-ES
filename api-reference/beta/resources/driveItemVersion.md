---
author: rgregg
ms.author: rgregg
ms.date: 09/17/2017
title: DriveItemVersion
ms.openlocfilehash: 6abe10a14a4995231b12cf0c828325259775ffd8
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083872"
---
# <a name="driveitemversion-resource-type"></a>Tipo de recurso DriveItemVersion

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

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

<!-- { "blockType": "resource", "@odata.type": "microsoft.graph.driveItemVersion", "@type.aka": "oneDrive.driveItemVersion" } -->

```json
{
  "content": { "@odata.type": "Edm.Stream" },
  "id": "string",
  "lastModifiedBy": { "@odata.type": "microsoft.graph.identitySet" },
  "lastModifiedDateTime": "2016-01-01T15:20:01.125Z",
  "publication": { "@odata.type": "microsoft.graph.publicationFacet" }
}
```

## <a name="properties"></a>Propiedades

|      Nombre de propiedad       |                         Tipo                         |                               Descripción                               |
| :----------------------- | :--------------------------------------------------- | :---------------------------------------------------------------------- |
| **id**                   | string                                               | El identificador de la versión. Solo lectura.                                       |
| **lastModifiedBy**       | [IdentitySet](../resources/identityset.md)           | Identidad del usuario que modificó por última vez la versión. Solo lectura.        |
| **lastModifiedDateTime** | [DateTimeOffset](../resources/timestamp.md)          | Fecha y hora de la última modificación de la versión. Solo lectura.                 |
| **publication**          | [PublicationFacet](../resources/publicationfacet.md) | Indica el estado de publicación de esta versión concreta. Solo lectura. |
| **size**                 | Int64                                                | Indica el tamaño de la secuencia de contenido para esta versión del elemento.  |

## <a name="relationships"></a>Relaciones

En la tabla siguiente, se definen las relaciones que tiene el recurso **driveItemVersion** con otros recursos.

| Nombre de la relación |  Tipo  |            Descripción             |
| :---------------- | :----- | :--------------------------------- |
| **content**       | Secuencia | La secuencia de contenido de la versión. |

<!-- {
  "type": "#page.annotation",
  "description": "The version facet provides information about the properties of a file version.",
  "keywords": "version,versions,version-history,history",
  "section": "documentation",
  "tocPath": "Facets/Version"
} -->