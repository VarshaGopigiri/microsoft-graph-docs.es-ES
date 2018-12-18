---
title: 'llamar a: changeScreenSharingRole'
description: Iniciar y detener el uso compartido de pantalla en la llamada. Esta API se usa para permitir que las aplicaciones compartir el contenido de la pantalla con los participantes de una llamada o una reunión.
author: VinodRavichandran
ms.openlocfilehash: 4b4c7e0afa452bef414dd466086463aa16c9d9cf
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27328367"
---
# <a name="call-changescreensharingrole"></a>llamar a: changeScreenSharingRole

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Iniciar y detener el uso compartido de pantalla en la llamada. Esta API se usa para permitir que las aplicaciones compartir el contenido de la pantalla con los participantes de una llamada o una reunión.

## <a name="permissions"></a>Permisos
Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).

| Tipo de permiso                        | Permisos (de menos a más privilegiados) |
|:---------------------------------------|:--------------------------------------------|
| Delegado (cuenta profesional o educativa)     | No se admite                               |
| Delegado (cuenta personal de Microsoft) | No se admite                               |
| Aplicación                            | Calls.AccessMedia.All                       |

## <a name="http-request"></a>Solicitud HTTP
<!-- { "blockType": "ignored" } -->
```http
POST /app/calls/{id}/changeScreenSharingRole
POST /applications/{id}/calls/{id}/changeScreenSharingRole
```

## <a name="request-headers"></a>Encabezados de solicitud
| Nombre          | Descripción               |
|:--------------|:--------------------------|
| Authorization | {token} de portador. Obligatorio. |

## <a name="request-body"></a>Cuerpo de la solicitud
En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.

| Parámetro      | Type    |Descripción|
|:---------------|:--------|:----------|
|role|String|Los valores posibles son: 'Visor', 'Que comparte'|

## <a name="response"></a>Respuesta
Devuelve `202 Accepted` código de respuesta.

## <a name="example"></a>Ejemplo
En el siguiente ejemplo se muestra cómo llamar a esta API.

##### <a name="request"></a>Solicitud
En el ejemplo siguiente se muestra la solicitud.

<!-- {
  "blockType": "request",
  "name": "call_changeScreenSharingRole"
}-->
```http
POST https://graph.microsoft.com/beta/app/calls/{id}/changeScreenSharingRole
Content-Type: application/json
Content-Length: 24

{
  "role": "viewer"
}
```

##### <a name="response"></a>Respuesta
Aquí tiene un ejemplo de la respuesta. 

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.None"
} -->
```http
HTTP/1.1 202 Accepted
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "call: changeScreenSharingRole",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
