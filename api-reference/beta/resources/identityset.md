---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: IdentitySet
localization_priority: Normal
ms.openlocfilehash: 63178fc9add3d097b7e8aaf0c5c2a697a91eaeed
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27807024"
---
# <a name="identityset-resource-type"></a>tipo de recurso identitySet

El recurso **IdentitySet** es una colección de claves de recursos [identity](identity.md). Se usa para representar un conjunto de identidades asociadas a diversos eventos para un elemento, como _creado por_ o _última modificación_.

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.identitySet",
  "optionalProperties": [
    "application",
    "applicationInstance",
    "device",
    "encrypted",
    "guest",
    "phone",
    "user"
  ],
  "openType": true
} -->
```json
{
  "application": {"@odata.type": "#microsoft.graph.identity"},
  "applicationInstance": {"@odata.type": "#microsoft.graph.identity"},
  "device": {"@odata.type": "#microsoft.graph.identity"},
  "encrypted": {"@odata.type": "#microsoft.graph.identity"},
  "guest": {"@odata.type": "#microsoft.graph.identity"},
  "phone": {"@odata.type": "#microsoft.graph.identity"},
  "user": {"@odata.type": "#microsoft.graph.identity"}
}
```

## <a name="properties"></a>Propiedades

| Propiedad    | Tipo                    | Descripción                                             |
|:------------|:------------------------|:--------------------------------------------------------|
| application | [Identity](identity.md) | Opcional. Aplicación asociada a esta acción.  |
| Dispositivo      | [Identity](identity.md) | Opcional. Dispositivo asociado a esta acción.       |
| phone       | [identity](identity.md) | Opcional. El número de teléfono asociado con esta acción. |
| usuario        | [Identity](identity.md) | Opcional. Usuario asociado a esta acción.         |

## <a name="remarks"></a>Observaciones 

Vea la [llamada](call.md) para el uso de recursos de **IdentitySet** .


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Identity set is a collection of identities",
  "section": "documentation",
  "tocPath": "Resources/IdentitySet"
} -->
