---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: IdentitySet
ms.openlocfilehash: 4d2bb5d92ebe06e79a68d69b949baec19a33a4c6
ms.sourcegitcommit: 7aea7a97e36e6d146214de3a90fdbc71628aadba
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/28/2017
---
# <a name="identityset-resource-type"></a>Tipo de recurso IdentitySet

El recurso **IdentitySet** es una colección de claves de recursos [identity](identity.md). Se usa para representar un conjunto de identidades asociadas a diversos eventos para un elemento, como _creado por_ o _última modificación_.

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- { "blockType": "resource", "@odata.type": "microsoft.graph.identitySet",
       "optionalProperties": ["user", "application", "device"],
       "openType": true } -->
```json
{
  "application": {"@odata.type": "microsoft.graph.identity"},
  "device": {"@odata.type": "microsoft.graph.identity"},
  "user": {"@odata.type": "microsoft.graph.identity"}
}
```

## <a name="properties"></a>Propiedades

| Propiedad    | Tipo                    | Descripción                                            |
|:------------|:------------------------|:-------------------------------------------------------|
| application | [Identity](identity.md) | Opcional. Aplicación asociada a esta acción. |
| device      | [Identity](identity.md) | Opcional. Dispositivo asociado a esta acción.      |
| user        | [Identity](identity.md) | Opcional. Usuario asociado a esta acción.        |

## <a name="remarks"></a>Comentarios 

Consulte [DriveItem](driveitem.md) para obtener información sobre el uso de recursos **IdentitySet**.


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Identity set is a collection of identities",
  "section": "documentation",
  "tocPath": "Resources/IdentitySet"
} -->
