---
title: Actualizar privilegedRoleSettings
description: Actualizar la configuración de las funciones para la configuración de rol determinado. Se devuelve un objeto privilegedRoleSettings.
localization_priority: Normal
ms.openlocfilehash: 7c117abfe774eae60e42dcbc5f748c10cacf5cd6
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27819323"
---
# <a name="update-privilegedrolesettings"></a>Actualizar privilegedRoleSettings

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Actualizar la configuración de las funciones para la configuración de rol determinado. Se devuelve un objeto [privilegedRoleSettings](../resources/privilegedrolesettings.md) .
## <a name="permissions"></a>Permisos

Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).

>**Nota:** El solicitante debe tener uno de los siguientes roles: Administrador de roles con privilegios, administrador Global, Administrador de seguridad o lector de seguridad. 

|Tipo de permiso      | Permisos (de menos a más privilegiados)              |
|:--------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa) | PrivilegedAccess.ReadWrite.AzureAD, Directory.AccessAsUser.All    |
|Delegado (cuenta personal de Microsoft) | No admitida.    |
|Aplicación | No admitida. |

## <a name="http-request"></a>Solicitud HTTP
<!-- { "blockType": "ignored" } -->
```http
PUT /privilegedRoles/{id}/settings
```

## <a name="request-headers"></a>Encabezados de solicitud
| Nombre      |Descripción|
|:----------|:----------|
| Authorization  | {token} de portador. Obligatorio. |

## <a name="request-body"></a>Cuerpo de la solicitud
En el cuerpo de la solicitud, proporcionar una representación JSON de un objeto [privilegedRoleSettings](../resources/privilegedrolesettings.md) .

En la siguiente tabla se enumera las propiedades que puede proporcionar al actualizar una configuración de rol.

|Propiedad|Tipo|Description|
|:---------------|:--------|:----------|
|elevationDuration|duration|La duración cuando se activa la función. Necesario.|
|id|string|El identificador único para la configuración de las funciones. Solo lectura. Necesario.|
|isMfaOnElevationConfigurable|boolean|**true** si mfaOnElevation es configurable. **false** si no se puede configurar mfaOnElevation. Necesario.|
|lastGlobalAdmin|Booleano|Solo para uso interno.|
|maxElavationDuration|duration|Duración máxima de la función activada. Necesario.|
|mfaOnElevation|Booleano|**true** si MFA se requiere para activar la función. **false** si no es necesario MFA para activar la función. Necesario.|
|minElevationDuration|duration|Duración mínima para la función activada. Necesario.|
|notificationToUserOnElevation|Booleano|**true** si enviar notificación para el usuario final cuando se activa la función. **false** si no enviar notificación cuando se activa la función. Necesario.|
|ticketingInfoOnElevation|Booleano|**true** si se requiere la información mediante vales cuándo activar la función. **false** si la información mediante vales no se requiere cuando se activa la función. Necesario.|
|approvalOnElevation|Booleano|**true** si se requiere la aprobación cuando se activa la función. **false** si la aprobación no se requiere cuando se activa la función. Necesario.|
|approverIds|matriz|Lista de identificadores de aprobación, si se necesita aprobación para la activación.|

## <a name="response"></a>Respuesta

Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`.

Tenga en cuenta que el inquilino debe estar registrado en PIM. De lo contrario, se devolverá el código de estado HTTP 403 Prohibido.
## <a name="example"></a>Ejemplo
##### <a name="request"></a>Solicitud
Aquí tiene un ejemplo de la solicitud.
<!-- {
  "blockType": "request",
  "name": "put_privilegedrolesettings"
}-->
```http
PUT https://graph.microsoft.com/beta/privilegedRoles/{id}/settings
Content-type: application/json

{
    "id": "9b895d92-2cd3-44c7-9d02-a6ac2d5ea5c3",
    "elevationDuration": "PT8H",
    "notificationToUserOnElevation": false,
    "ticketingInfoOnElevation": true,
    "mfaOnElevation": false,
    "maxElavationDuration": "PT0S",
    "minElevationDuration": "PT0S",
    "lastGlobalAdmin": false,
    "isMfaOnElevationConfigurable": true,
    "approvalOnElevation": false,
    "approverIds": ["e2b2a2fb-13d7-495c-adc9-941fe966793f", "22770e3f-b9b4-418e-9dea-d0e3d2f275dd"]
}
```
##### <a name="response"></a>Respuesta
Aquí tiene un ejemplo de la respuesta.

```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update privilegedRoleSettings",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
