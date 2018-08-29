---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: SharingInvitation
ms.openlocfilehash: 9237c401fd83a7b30303f147402262c022b820a7
ms.sourcegitcommit: abf4b739257e3ffd9d045f783ec595d846172590
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2018
ms.locfileid: "23265858"
---
# <a name="sharinginvitation-resource-type"></a>Tipo de recurso SharingInvitation

El recurso **SharingInvitation** agrupa en una sola estructura los elementos de datos relacionados con invitaciones.

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.sharingInvitation"
}-->

```json
{
  "email": "string",
  "invitedBy": {"@odata.type": "microsoft.graph.identitySet" },
  "signInRequired": true
}
```

## <a name="properties"></a>Propiedades

| Nombre de la propiedad  | Tipo            | Descripción
|:---------------|:----------------|:------------------------------------------
| email          | Cadena          | Dirección de correo proporcionada para el destinatario de la invitación para compartir. Solo lectura.
| invitedBy      | [identitySet][] | Proporciona información sobre quién envió la invitación que creó este permiso, si esa información está disponible. Solo lectura.
| signInRequired | Booleano         | Si `true` el destinatario de la invitación necesita iniciar sesión para obtener acceso al elemento compartido. Solo lectura.

## <a name="remarks"></a>Comentarios

Para obtener más información sobre las facetas de un objeto DriveItem, consulte [DriveItem](driveitem.md).

[DriveItem]: driveItem.md
[IdentitySet]: identitySet.md

<!-- {
  "type": "#page.annotation",
  "description": "The sharing invitation facet describes details of a sharing invitation associated with a permission.",
  "keywords": "image,width,height,item,facet",
  "section": "documentation",
  "tocPath": "Facets/SharingInvitation"
} -->
