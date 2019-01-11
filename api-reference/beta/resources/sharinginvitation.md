---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: SharingInvitation
localization_priority: Normal
ms.openlocfilehash: 3ba92573aaef89b1be431ade33caa6ed465917a9
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27835976"
---
# <a name="sharinginvitation-resource-type"></a>Tipo de recurso SharingInvitation

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

El recurso **SharingInvitation** agrupa en una sola estructura los elementos de datos relacionados con invitaciones.

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso

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

| Nombre de la propiedad  | Tipo                          | Descripción                                                                                                                   |
|:---------------|:------------------------------|:------------------------------------------------------------------------------------------------------------------------------|
| email          | String                        | Dirección de correo proporcionada para el destinatario de la invitación para compartir. Solo lectura.                                          |
| invitedBy      | [identitySet](identityset.md) | Proporciona información sobre quién envió la invitación que creó este permiso, si esa información está disponible. Solo lectura. |
| signInRequired | Boolean                       | Si `true` el destinatario de la invitación necesita iniciar sesión para obtener acceso al elemento compartido. Solo lectura.                     |

## <a name="remarks"></a>Comentarios 

Para obtener más información sobre las facetas de un objeto DriveItem, consulte [DriveItem](driveitem.md).


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "The sharing invitation facet describes details of a sharing invitation associated with a permission.",
  "keywords": "image,width,height,item,facet",
  "section": "documentation",
  "tocPath": ""
}-->
