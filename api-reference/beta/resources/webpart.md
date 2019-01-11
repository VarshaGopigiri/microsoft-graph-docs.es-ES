---
author: rahmit
ms.author: rahmit
ms.date: 09/01/2018
title: WebPart
localization_priority: Normal
ms.openlocfilehash: f7293b986b5e6d77d0601cffb6b60edc5dfd2dd7
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27856031"
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
| **type**                | Cadena           | Un identificador único que especifica el tipo de elemento Web. Solo lectura.
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
