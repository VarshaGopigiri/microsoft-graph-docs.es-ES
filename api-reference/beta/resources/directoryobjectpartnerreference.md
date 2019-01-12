---
title: tipo de recurso directoryObjectPartnerReference
description: Representa una referencia a un objeto de directorio en un inquilino de socio. Se hereda de directoryObject.
author: lleonard-msft
localization_priority: Normal
ms.prod: microsoft-identity-platform
ms.openlocfilehash: 17bab72fad3e03b843975ae62261fac9c09af791
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27918542"
---
# <a name="directoryobjectpartnerreference-resource-type"></a>tipo de recurso directoryObjectPartnerReference

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Representa una referencia a un objeto de Active directory en una organización asociada. Se hereda de [directoryObject](directoryobject.md?view=graph-rest-beta).

## <a name="properties"></a>Propiedades

| Propiedad | Tipo | Descripción |
|:---------------|:--------|:----------|
|description|Cadena| Descripción del objeto devuelto. Solo lectura. |
|displayName|Cadena| Nombre del objeto de Active directory que se devuelve, al igual que el grupo o la aplicación. Solo lectura. |
|externalPartnerTenantId|Guid| El identificador de inquilino para el inquilino de socio. Solo lectura. |
|id|Cadena| El identificador único para el recurso. Heredado de [directoryObject](directoryobject.md?view=graph-rest-beta). Solo lectura. |
|objectType|String| El tipo del objeto que se hace referencia en el inquilino de socio. Solo lectura. |

## <a name="json-representation"></a>Representación JSON

Esta es una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.directoryObjectPartnerReference"
}-->

```json
{
  "description": "string ",
  "displayName": "string",
  "externalPartnerTenantId": "string (identifier)",
  "id": "string (identifier)",
  "objectType": "string"
}
```

## <a name="see-also"></a>Vea también

- [Obtener objetos de directorio a partir de una lista de identificadores](/graph/api/directoryobject-getbyids?view=graph-rest-beta)

<!-- uuid: fbec8cd7-cfe4-431d-87fc-d102cd2841a4
2018-12-06 02:01:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "directoryObjectPartnerReference resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
