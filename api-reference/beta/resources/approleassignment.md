---
title: tipo de recurso appRoleAssignment
description: Se usa para registrar cuándo un usuario o grupo se asigna a una aplicación. En este caso, la asignación de roles, se producirá un icono de aplicación visible copia de seguridad en el panel de acceso de aplicación del usuario. Esta entidad también se puede usar para conceder acceso de otra aplicación (que se modela como un entidad de seguridad de servicio) a una aplicación de recursos en una función determinada. Puede crear, leer, actualizar y eliminar las asignaciones de roles.
ms.openlocfilehash: 97155bde12735ebd8a7674e0dbf20dae30e53f14
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084604"
---
# <a name="approleassignment-resource-type"></a>tipo de recurso appRoleAssignment

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Se usa para registrar cuándo un usuario o grupo se asigna a una aplicación. En este caso, la asignación de roles, se producirá un icono de aplicación visible copia de seguridad en el panel de acceso de aplicación del usuario. Esta entidad también se puede usar para conceder acceso de otra aplicación (que se modela como un entidad de seguridad de servicio) a una aplicación de recursos en una función determinada. Puede crear, leer, actualizar y eliminar las asignaciones de roles.


## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.approleassignment"
}-->

```json
{
  "creationTimestamp": "String (timestamp)",
  "id": "guid (identifier)",
  "principalDisplayName": "string",
  "principalId": "guid",
  "principalType": "string",
  "resourceDisplayName": "string",
  "resourceId": "guid"
}

```
## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|creationTimestamp|DateTimeOffset|La hora de creación de la concesión. El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC. Por ejemplo, la medianoche UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`|
|id|Guid|El identificador de rol que se asignó a la entidad de seguridad.  Esta función se debe declarar por el de aplicación de destino recursos **resourceId** en su propiedad **appRoles** . Donde el recurso no declarar los permisos, debe especificarse un identificador predeterminado (identificador GUID cero). Clave. No admite valores NULL. |
|principalDisplayName|String|El nombre para mostrar de la entidad de seguridad que se ha concedido el acceso.|
|principalId|Guid|El identificador único (**Id.**) de la entidad de seguridad que se van a conceder el acceso. Necesarios en crear.            |
|principalType|String|El tipo de entidad de seguridad.  Esto puede ser "User", "ServicePrincipal" o "Grupo".|
|resourceDisplayName|String|El nombre para mostrar del recurso al que se realizó la asignación.|
|resourceId|Guid|El identificador único (**Id.**) para el recurso de destino (entidad de seguridad de servicio) para el que se realizó la asignación.|

## <a name="relationships"></a>Relaciones
Ninguno


## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Obtener appRoleAssignment](../api/approleassignment-get.md) | [appRoleAssignment](approleassignment.md) |Leer las propiedades y las relaciones del objeto appRoleAssignment.|
|[Update](../api/approleassignment-update.md) | [appRoleAssignment](approleassignment.md)   |Actualizar el objeto appRoleAssignment. |
|[Delete](../api/approleassignment-delete.md) | Ninguno |Eliminar el objeto appRoleAssignment. |

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "appRoleAssignment resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->