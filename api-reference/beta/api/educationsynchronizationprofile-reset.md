---
title: Restablecer la sincronización en un educationSynchronizationProfile
description: Restablecer la sincronización de un perfil de sincronización de datos de school específicos en el inquilino.
author: mmast-msft
ms.openlocfilehash: 29d21318737ceba3bd380eaf20a9500a6a711857
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27362443"
---
# <a name="reset-sync-on-an-educationsynchronizationprofile"></a>Restablecer la sincronización en un educationSynchronizationProfile

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Restablecer la sincronización de escuela específico datos en un [perfil de sincronización](../resources/educationsynchronizationprofile.md) del inquilino.

> **Nota:** Esta operación hará que la sincronización para reiniciar. Se eliminarán todos los errores detectados. Datos no se eliminarán de Azure Active Directory (AD Azure). 

## <a name="permissions"></a>Permisos
Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).

| Tipo de permiso | Permisos |
|:-----------|:----------|
| Delegado (cuenta profesional o educativa) | EduAdministration.ReadWrite |
|Delegado (cuenta Microsoft personal|No admitida.|
|Aplicación|No admitida.|

## <a name="http-request"></a>Solicitud HTTP
<!-- { "blockType": "ignored" } -->
```http
POST /synchronizationProfiles/{id}/reset
```

## <a name="request-headers"></a>Encabezados de solicitud
| Nombre       | Type | Descripción|
|:-----------|:------|:----------|
| Autorización  | string  | {token} de portador. Obligatorio.  |

## <a name="request-body"></a>Cuerpo de la solicitud
No proporcione un cuerpo de solicitud para este método.
## <a name="response"></a>Respuesta
Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK`.

## <a name="example"></a>Ejemplo
##### <a name="request"></a>Solicitud
Aquí tiene un ejemplo de la solicitud.
<!-- {
  "blockType": "request",
  "name": "post_educationSynchronizationProfile_reset"
}-->
```http
POST https://graph.microsoft.com/beta/education/synchronizationProfiles/{id}/reset
```

##### <a name="response"></a>Respuesta

No hay ningún cuerpo de la respuesta.

<!-- {
  "blockType": "response",
  "name": "post_educationSynchronizationProfile_reset"
}-->
```
HTTP/1.1 200 OK
```