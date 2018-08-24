---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: SiteCollection
ms.openlocfilehash: 84de2a8aa6796051b3b11ebec0d0f8f5934ea1fc
ms.sourcegitcommit: abf4b739257e3ffd9d045f783ec595d846172590
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2018
ms.locfileid: "19069346"
---
# <a name="sitecollection-resource"></a>Recurso SiteCollection

El recurso **SiteCollection** proporciona más información acerca de una colección de sitios.

Si un recurso [**site**](site.md) tiene una propiedad **siteCollection** que no es NULL, site es un sitio raíz de una colección de sitios.

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [
  ],
  "@odata.type": "microsoft.graph.siteCollection"
}-->

```json
{
  "hostname": "contoso.sharepoint.com",
  "root": { "@odata.type": "microsoft.graph.root" }
}
```

## <a name="properties"></a>Propiedades

| Nombre de propiedad        | Tipo     | Descripción
|:---------------------|:---------|:---------------------------------------------------
| **hostname**         | cadena   | Nombre de host de la colección de sitios. Solo lectura.
| **root**             | [root][] | Si está presente, indica que se trata de una colección de sitios raíz en SharePoint. Solo lectura.

[root]: root.md

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "",
  "keywords": "",
  "section": "documentation",
  "tocPath": "Facets/SiteCollection"
}-->
