---
title: Enumerar las aplicaciones y entidades de seguridad de servicio con específico directiva asignada
description: Recuperar la aplicación y objetos del servicio de entidad de seguridad con la directiva especificada asignada.
localization_priority: Normal
ms.openlocfilehash: 21a5a9ba4260e306553f53866657a482d814b5f7
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27875610"
---
# <a name="list-applications-and-service-principals-with-specific-policy-assigned"></a>Enumerar las aplicaciones y entidades de seguridad de servicio con específico directiva asignada

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Recupere los objetos de [aplicación](../resources/application.md) y [servicio de entidad de seguridad](../resources/serviceprincipal.md) con la directiva especificada asignada.

## <a name="permissions"></a>Permisos
Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).

|Tipo de permiso      | Permisos (de menos a más privilegiados)              |
|:--------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa) | Directory.AccessAsUser.All    |
|Delegado (cuenta personal de Microsoft) | No admitida.    |
|Aplicación | No admitida. |

## <a name="http-request"></a>Solicitud HTTP
```http
GET /policies/{id}/appliesTo
```

## <a name="request-headers"></a>Encabezados de solicitud
| Nombre       | Tipo | Descripción|
|:---------------|:--------|:----------|
| Autorización  | string  | {token} de portador. Obligatorio. |

## <a name="request-body"></a>Cuerpo de la solicitud
No proporcione un cuerpo de solicitud para este método.

## <a name="response"></a>Respuesta

Si tiene éxito, este método devuelve `200 OK` objetos de código y la [aplicación](../resources/application.md) y la [entidad de seguridad del servicio](../resources/serviceprincipal.md) de respuesta en el cuerpo de la respuesta. Si no lo consigue, un `4xx` se devolverá el error con detalles específicos.

## <a name="example"></a>Ejemplo
En el ejemplo siguiente se recupera las aplicaciones y entidades de seguridad de servicio con asignada una directiva específica.

##### <a name="request"></a>Solicitud
Aquí tiene un ejemplo de la solicitud.

```http
GET https://graph.microsoft.com/beta/policies/{id}/appliesTo
```

##### <a name="response"></a>Respuesta
Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.

```http
HTTP/1.1 200 OK
Content-Type: application/json

{
    "value":[
        {
            "@odata.type"="#microsoft.graph.application",
            "appId":"appId-value",
            "displayName":"displayName-value",
            "errorUrl":"errorUrl-value",
            "groupMembershipClaims":"groupMembershipClaims-value",
            "homepage":"homepage-value",
            "id":"id-value",
            "keyCredentials":[key-credentials],
            "logoutUrl":"logoutUrl-value",
            "replyUrls":["replyUrls-value"]
        }
    ]
}
```
