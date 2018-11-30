---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: SiteCollection
ms.openlocfilehash: 98f7b9d930ccf7f1f0e1a6a0e1ad0353d49cf2bf
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030805"
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

| Nombre de la propiedad        | Tipo     | Descripción
|:---------------------|:---------|:---------------------------------------------------
| **hostname**         | string   | Nombre de host de la colección de sitios. Solo lectura.
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
