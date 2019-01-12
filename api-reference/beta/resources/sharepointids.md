---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: SharePointIds
localization_priority: Normal
ms.prod: sharepoint
ms.openlocfilehash: 641b4f5b8d78a38324b7b19c9136e8a53532a9d4
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27979939"
---
# <a name="sharepointids-resource-type"></a>Tipo de recurso SharePointIds

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

El recurso **SharePointIds** agrupa en una sola estructura los distintos identificadores de un elemento almacenado en un sitio de SharePoint o en OneDrive para la Empresa.

**Nota:** los elementos devueltos de OneDrive Personal no incluyen una faceta **SharePointIds**.

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [ "listId", "listItemId", "listItemUniqueId", "siteId", "siteUrl", "webId" ],
  "@odata.type": "microsoft.graph.sharepointIds"
}-->

```json
{
    "listId": "string",
    "listItemId": "string",
    "listItemUniqueId": "string",
    "siteId": "string",
    "siteUrl": "url",
    "tenantId": "string",
    "webId": "string"
}
```

## <a name="properties"></a>Propiedades

| Propiedad         | Tipo         | Descripción
|:-----------------|:-------------|:-------------------------------------------
| listId           | string       | Identificador único (guid) de la lista del elemento en SharePoint.
| listItemId       | string       | Identificador entero del elemento en la lista que lo contiene.
| listItemUniqueId | string       | Identificador único (GUID) del elemento contenido en OneDrive para la Empresa o en un sitio de SharePoint.
| siteId           | string       | Identificador único (guid) de la colección de sitios del elemento (SPSite).
| siteUrl          | string (URL) | La URL de SharePoint del sitio que contiene el elemento.
| tenantId         | string       | Identificador único (guid) del arrendamiento.
| webId            | string       | Identificador único (guid) del sitio del elemento (SPWeb).

## <a name="remarks"></a>Observaciones

Para obtener más información sobre las facetas de **driveItem**, consulte [**driveItem**](driveitem.md).



<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "The SharepointIds facet provides Sharepoint ids associated with an item.",
  "keywords": "item, unique, id, csom, facet",
  "section": "documentation",
  "tocPath": "Facets/SharepointIds"
} -->
