---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Compartidos
ms.openlocfilehash: 1d828310a226edd0443ff3b5f60156df1e7c98cb
ms.sourcegitcommit: 7aea7a97e36e6d146214de3a90fdbc71628aadba
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/28/2017
---
# <a name="shared-resource-type"></a>Tipo de recurso Shared

El recurso **Shared** indica que se ha compartido un objeto DriveItem con otros usuarios.
El recurso incluye información sobre cómo se comparte el elemento.

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
