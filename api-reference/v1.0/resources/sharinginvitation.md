---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: SharingInvitation
ms.openlocfilehash: 187a7bd8fe51be57b663c215436272ee711512e4
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030477"
---
# <a name="sharinginvitation-resource-type"></a>Tipo de recurso SharingInvitation

El recurso **SharingInvitation** agrupa los elementos de datos relacionados con la invitación en una única estructura.

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
| email          | String          | Dirección de correo proporcionada para el destinatario de la invitación para compartir. Solo lectura.
| invitedBy      | [identitySet][] | Proporciona información sobre quién envió la invitación que creó este permiso, si esa información está disponible. Solo lectura.
| signInRequired | Boolean         | Si `true` el destinatario de la invitación necesita iniciar sesión para obtener acceso al elemento compartido. Solo lectura.

## <a name="remarks"></a>Comentarios

Para obtener más información sobre las facetas de un objeto DriveItem, consulte [DriveItem](driveitem.md).

[DriveItem]: driveitem.md
[IdentitySet]: identityset.md

<!-- {
  "type": "#page.annotation",
  "description": "The sharing invitation facet describes details of a sharing invitation associated with a permission.",
  "keywords": "image,width,height,item,facet",
  "section": "documentation",
  "tocPath": "Facets/SharingInvitation"
} -->
