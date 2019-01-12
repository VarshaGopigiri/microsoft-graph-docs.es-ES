---
title: Tipo de recurso ListItemVersion
description: El recurso **listItemVersion** representa una versión anterior de un recurso ListItem.
localization_priority: Normal
ms.prod: sharepoint
ms.openlocfilehash: 6e21be59b71a8f348931603c799ebbbe225e5d3f
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27951848"
---
# <a name="listitemversion-resource-type"></a>Tipo de recurso ListItemVersion

El recurso **listItemVersion** representa una versión anterior de un recurso [ListItem](listitem.md).

## <a name="tasks-on-listitemversion-resources"></a>Tareas en recursos ListItemVersion

Las tareas siguientes están disponibles para los recursos listItemVersion.

|            Tarea común             |         Método HTTP         |
| :--------------------------------- | :-------------------------- |
| [Enumerar versiones][version-list]      | `GET /sites/{site-id}/items/{item-id}/versions`  |
| [Obtener versión][version-get]         | `GET /sites/{site-id}/items/{item-id}/versions/{version-id}`     |
| [Restaurar versión][version-restore] | `POST /sites/{site-id}/items/{item-id}/versions/{version-id}/restore` |

[version-list]: ../api/listitem-list-versions.md
[version-get]: ../api/listitemversion-get.md
[version-restore]: ../api/listitemversion-restore.md


## <a name="json-representation"></a>Representación JSON

<!--{
  "blockType": "resource",
  "baseType": "microsoft.graph.baseItemVersion",
  "@odata.type": "microsoft.graph.listItemVersion",
  "@type.aka": "oneDrive.baseItemVersion"
}-->

```json
{
  "fields": { "@odata.type": "microsoft.graph.fieldValueSet" },
  "id": "string",
  "lastModifiedBy": { "@odata.type": "microsoft.graph.identitySet" },
  "lastModifiedDateTime": "2016-01-01T15:20:01.125Z",
  "published": { "@odata.type": "microsoft.graph.publicationFacet" }
}
```

## <a name="properties"></a>Propiedades

|      Nombre de la propiedad       |                         Tipo                         |                               Descripción                               |
| :----------------------- | :--------------------------------------------------- | :---------------------------------------------------------------------- |
| **id**                   | string                                               | El identificador de la versión. Solo lectura.                                       |
| **lastModifiedBy**       | [IdentitySet](../resources/identityset.md)           | Identidad del usuario que modificó por última vez la versión. Solo lectura.        |
| **lastModifiedDateTime** | [DateTimeOffset](../resources/timestamp.md)          | Fecha y hora de la última modificación de la versión. Solo lectura.                 |
| **published**            | [PublicationFacet](../resources/publicationfacet.md) | Indica el estado de publicación de esta versión concreta. Solo lectura. |


## <a name="relationships"></a>Relaciones

En la tabla siguiente, se definen las relaciones que tiene el recurso **driveItemVersion** con otros recursos.

| Nombre de la relación |                      Tipo                      |                               Descripción                                |
| :---------------- | :--------------------------------------------- | :----------------------------------------------------------------------- |
| **fields**        | [FieldValueSet](../resources/fieldvalueset.md) | Una colección de los campos y valores para esta versión del elemento de lista. |


<!-- {
  "type": "#page.annotation",
  "description": "The version facet provides information about the properties of a file version.",
  "keywords": "version,versions,version-history,history",
  "section": "documentation",
  "tocPath": "Facets/Version"
} -->
