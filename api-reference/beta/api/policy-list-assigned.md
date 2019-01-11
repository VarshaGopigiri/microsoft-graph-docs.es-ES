---
title: Directivas de la lista asignadas a la aplicación o entidad de seguridad de servicio
description: Recupere los objetos de directiva asignados a una aplicación o un servicio de entidad de seguridad.
localization_priority: Normal
ms.openlocfilehash: 3c66eece645313f7039f12aec708cba4581fb4bb
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27875358"
---
# <a name="list-policies-assigned-to-application-or-service-principal"></a>Directivas de la lista asignadas a la aplicación o entidad de seguridad de servicio

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Recupere los objetos de [Directiva](../resources/policy.md) asignados a una aplicación o un servicio de entidad de seguridad.

## <a name="permissions"></a>Permisos
Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).

|Tipo de permiso      | Permisos (de menos a más privilegiados)              |
|:--------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa) | Directory.AccessAsUser.All    |
|Delegado (cuenta personal de Microsoft) | No admitida.    |
|Aplicación | No admitida. |

## <a name="http-request"></a>Solicitud HTTP
<!-- { "blockType": "ignored" } -->
```http
GET /applications/{id}/policies
```

> Nota: El identificador de"" en la solicitud es la propiedad "id" de la aplicación o el servicio de entidad de seguridad, no la propiedad "appid".

## <a name="request-headers"></a>Encabezados de solicitud
| Nombre       | Tipo | Descripción|
|:---------------|:--------|:----------|
| Autorización  | string  | {token} de portador. Obligatorio. |

## <a name="request-body"></a>Cuerpo de la solicitud
No proporcione un cuerpo de solicitud para este método.

## <a name="response"></a>Respuesta

Si tiene éxito, este método devuelve `200 OK` objetos de código y la [Directiva](../resources/policy.md) de respuesta en el cuerpo de la respuesta. Si no lo consigue, un `4xx` se devolverá el error con detalles específicos.

## <a name="example"></a>Ejemplo
En el ejemplo siguiente se recupera las directivas asignadas a una aplicación.

##### <a name="request"></a>Solicitud
Aquí tiene un ejemplo de la solicitud.

```http
GET https://graph.microsoft.com/beta/applications/{id}/policies
```

##### <a name="response"></a>Respuesta
Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.

```http
HTTP/1.1 200 OK
Cache-Control: private
Content-Type: application/json

{
    "value":[
        {
            "@odata.type":"#microsoft.graph.policy",
            "id":"id-value",
            "alternativeIdentifier":null,
            "definition":["policy-definition"],
            "displayName":"name-value",
            "isOrganizationDefault":boolean-value,
            "keyCredentials":[key-credentials],
            "type":"type-value"
        }
    ]
}
```
