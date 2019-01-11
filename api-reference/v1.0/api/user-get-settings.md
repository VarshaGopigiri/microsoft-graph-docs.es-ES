---
title: Obtener la configuración
description: Leer el objeto de configuración de usuario y de organización.
author: dkershaw10
localization_priority: Priority
ms.openlocfilehash: ace7c43b27860832968572628838484bc8c91c84
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27815494"
---
# <a name="get-settings"></a>Obtener la configuración

Leer el objeto de [configuración de](../resources/user-settings.md) usuario y de organización.
Para obtener más información acerca de cómo actualizar las propiedades del objeto de [configuración](../resources/user-settings.md) , consulte [actualización de la configuración de usuario](user-update-settings.md).

## <a name="permissions"></a>Permisos

Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).

|Tipo de permiso      | Permisos (de menos a más privilegiados)              |
|:--------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa) | User.Read.All, User.ReadWrite.All    |
|Delegado (cuenta personal de Microsoft) | No admitida.    |
|Aplicación | User.Read.All,User.ReadWrite.All |

## <a name="http-request"></a>Solicitud HTTP

```http
GET /me/settings/
```

Solicitar a un 'id' o 'userPrincipalName' sólo es accesible por el usuario o por un usuario con los permisos de User.ReadWrite.All. Para obtener más información, vea [permisos](/graph/permissions-reference).

```http
GET /users/{id | userPrincipalName}/settings/
```

## <a name="request-body"></a>Cuerpo de la solicitud

No proporcione un cuerpo de solicitud para este método.

## <a name="response"></a>Respuesta

Si tiene éxito, este método devuelve una `200 OK` objeto de [configuración de usuario](../resources/user-settings.md) y el código de respuesta en el cuerpo de la respuesta.

## <a name="example"></a>Ejemplo

##### <a name="request"></a>Solicitud

```http
GET https://graph.microsoft.com/v1.0/me/settings
```

##### <a name="response"></a>Respuesta

Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.

```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 72

{
  "contributionToContentDiscoveryAsOrganizationDisabled": false,
  "contributionToContentDiscoveryDisabled": false
}
```

