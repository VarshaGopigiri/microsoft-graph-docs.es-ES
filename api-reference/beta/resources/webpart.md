---
author: rahmit
ms.author: rahmit
ms.date: 09/01/2018
title: WebPart
ms.openlocfilehash: e9bb612e20bc3d2416503f571f5abf364215efb2
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086144"
---
# <a name="webpart-resource"></a>recursos de webPart

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

El recurso de **webPart** representa el tipo y la información de representación de un elemento web en un [sitePage](sitepage.md).

## <a name="json-representation"></a>Representación JSON

<!-- {
  "blockType": "resource",
  "optionalProperties": [  ],
  "@odata.type": "microsoft.graph.webPart"
}-->

```json
{
  "type": "string (guid)",
  "data": {
    "instanceId": "string (guid) (optional)"
  }
}
```

## <a name="properties"></a>Propiedades

| Propiedad                | Tipo             | Descripción
|:------------------------|:-----------------|:----------------------------------
| **type**                | String           | Un identificador único que especifica el tipo de elemento Web. Solo lectura.
| **data**                | [sitePageData][] | Las propiedades necesarias para el elemento Web (varía según el elemento Web)

[sitePageData]: sitepagedata.md

## <a name="remarks"></a>Observaciones

Elementos Web pueden definir sus propias propiedades necesarias en los **datos**.

Para obtener más información acerca de las páginas, vea [sitePage](sitepage.md).
<!-- {
  "type": "#page.annotation",
  "description": "Defines a control resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "Control"
} -->
