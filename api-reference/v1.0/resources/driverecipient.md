---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: DriveRecipient
localization_priority: Normal
ms.openlocfilehash: 94870893549e65399df5aae0ea1c409749ce1331
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27822263"
---
# <a name="driverecipient-resource"></a>Recurso DriveRecipient

El recurso **DriveRecipient** representa una persona, grupo u otro destinatario con el que se va a compartir mediante el uso de la acción [invite](../api/driveitem-invite.md).

## <a name="json-representation"></a>Representación JSON

<!-- { 
  "blockType": "resource", 
  "@odata.type": "microsoft.graph.driveRecipient", 
  "optionalProperties": ["alias", "objectId", "email"] } -->
```json
{
  "email": "string",
  "alias": "string",
  "objectId": "string",
}
```

## <a name="properties"></a>Propiedades
El recurso recipients tiene estas propiedades.

| Nombre de la propiedad | Tipo   | Descripción                                                                                             |
|:--------------|:-------|:--------------------------------------------------------------------------------------------------------|
| email         | String | Dirección de correo del destinatario, si este tiene una dirección de correo asociada.                  |
| alias         | String | Alias del objeto de dominio, para los casos en que una dirección de correo no está disponible (por ejemplo, los grupos de seguridad). |
| objectId      | String | Identificador único del destinatario en el directorio.                                               |

## <a name="remarks"></a>Comentarios

Si se usa [invite](../api/driveitem-invite.md) para agregar permisos, el objeto DriveRecipient puede especificar **email**, **alias** u **objectId**. Solo se requiere uno de estos valores.

<!-- {
  "type": "#page.annotation",
  "description": "Recipients resource defines a single recipient for the sharing invitation and permissions collection.",
  "keywords": "sharing,share,permissions,action.invite,invite,email",
  "section": "documentation",
  "tocPath": "Resources/Recipients"
} -->
