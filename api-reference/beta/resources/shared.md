---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Compartidos
localization_priority: Normal
ms.openlocfilehash: cae69a60691d388570d29176fc20aac429907f8a
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27838993"
---
# <a name="shared-resource-type"></a>Tipo de recurso Shared

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

El recurso **Shared** indica que se ha compartido un objeto DriveItem con otros usuarios. El recurso incluye información sobre cómo se comparte el elemento.

Si un objeto [**DriveItem**](driveitem.md) tiene una faceta **shared** que no es null, el elemento se ha compartido.

## <a name="json-representation"></a>Representación JSON

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.shared",
  "optionalProperties": [ "sharedBy", "sharedDateTime" ]
}-->

```json
{
  "owner": { "@odata.type": "microsoft.graph.identitySet" },
  "scope": "anonymous | organization | users",
  "sharedBy": { "@odata.type": "microsoft.graph.identitySet" },
  "sharedDateTime": "datetime"
}
```

## <a name="properties"></a>Propiedades

| Propiedad       | Tipo                          | Descripción
| :------------- |:------------------------------|:----------------------------
| owner          | [IdentitySet](identityset.md) | La identidad del propietario del elemento compartido. Solo lectura.
| scope          | String                        | Indica el ámbito sobre cómo se comparte el elemento: `anonymous`, `organization` o `users`. Solo lectura.
| sharedBy       | [identitySet](identityset.md) | La identidad del usuario que ha compartido el elemento. Solo lectura.
| sharedDateTime | DateTimeOffset                | Fecha y hora UTC de la última vez que se compartió el elemento. Solo lectura.

## <a name="scope-values"></a>Valores del ámbito

| Valor          | Descripción                                                                           |
|:---------------|:--------------------------------------------------------------------------------------|
| `anonymous`    | El elemento se comparte mediante un vínculo que le funciona a cualquier usuario con el vínculo.               |
| `organization` | El elemento se comparte mediante un vínculo que le funciona a cualquier usuario de la organización del propietario. |
| `users`        | El elemento se comparte solo con usuarios específicos.                                          |

## <a name="remarks"></a>Observaciones

Para obtener más información sobre las facetas de **driveItem**, consulte [**driveItem**](driveitem.md).

<!-- {
  "type": "#page.annotation",
  "description": "The shared facet provides info about shared items.",
  "keywords": "shared,share,item,facet,onedrive",
  "section": "documentation",
  "tocPath": "Facets/Shared"
} -->
