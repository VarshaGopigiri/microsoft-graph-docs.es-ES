---
title: Eliminar un educationSynchronizationProfile
description: Eliminar un perfil de sincronización de datos de school en el inquilino según el identificador.
ms.openlocfilehash: 829b723b48eb9a15750bc9d0e00ba50d432e8ab6
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087776"
---
# <a name="delete-a-educationsynchronizationprofile"></a>Eliminar un educationSynchronizationProfile

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Eliminar school datos en un [perfil de sincronización](../resources/educationsynchronizationprofile.md) del inquilino según el identificador.

## <a name="permissions"></a>Permisos
Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).

| Tipo de permiso | Permissions |
|:-----------|:----------|
| Delegado (cuenta profesional o educativa) | EduAdministration.ReadWrite |

## <a name="http-request"></a>Solicitud HTTP
<!-- { "blockType": "ignored" } -->
```http
DELETE /synchronizationProfiles/{id}
```

## <a name="request-headers"></a>Encabezados de solicitud
| Nombre       | Tipo | Descripción|
|:-----------|:------|:----------|
| Authorization  | string  | {token} de portador. Obligatorio.  |
|Delegado (cuenta Microsoft personal|No admitida.|
|Aplicación|No admitida.|

## <a name="request-body"></a>Cuerpo de la solicitud
No proporcione un cuerpo de solicitud para este método.
## <a name="response"></a>Respuesta
Si se ejecuta correctamente, este método devuelve un código de respuesta `202 Accepted`, pero no el cuerpo de la respuesta.

## <a name="example"></a>Ejemplo
##### <a name="request"></a>Solicitud
Aquí tiene un ejemplo de la solicitud.
<!-- {
  "blockType": "request",
  "name": "get_synchronizationProfile"
}-->
```http
DELETE https://graph.microsoft.com/beta/education/synchronizationProfiles/{id}
```

##### <a name="response"></a>Respuesta
Aquí tiene un ejemplo de la respuesta.
<!-- {
  "blockType": "response",
  "truncated": true
} -->
```http
HTTP/1.1 202 Accepted
```
