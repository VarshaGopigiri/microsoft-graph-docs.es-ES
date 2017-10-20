---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: DriveRecipient
ms.openlocfilehash: 53f6a5559cb90142a88b839a996cb2eedfd1037a
ms.sourcegitcommit: 7aea7a97e36e6d146214de3a90fdbc71628aadba
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/28/2017
---
# <a name="driverecipient-resource"></a>Recurso DriveRecipient

El recurso **DriveRecipient** representa una persona, grupo u otro destinatario con el que se va a compartir mediante el uso de la acción [invite](../api/driveitem_invite.md).

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

Si se usa [invite](../api/driveitem_invite.md) para agregar permisos, el objeto DriveRecipient puede especificar **email**, **alias** u **objectId**.
Solo se requiere uno de estos valores.

<!-- {
  "type": "#page.annotation",
  "description": "Recipients resource defines a single recipient for the sharing invitation and permissions collection.",
  "keywords": "sharing,share,permissions,action.invite,invite,email",
  "section": "documentation",
  "tocPath": "Resources/Recipients"
} -->
