---
title: 'servicePrincipal: delta'
description: Get recién creado, actualizados o eliminados de entidades de seguridad de servicio sin tener que realizar un acceso completo de lectura de la colección completa de recursos. Para obtener más información, vea Uso de consulta de Delta.
ms.openlocfilehash: 27653df1444ca83ef819d51813a813b169f3ad7e
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087924"
---
# <a name="serviceprincipal-delta"></a>servicePrincipal: delta

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Get recién creado, actualizados o eliminados de entidades de seguridad de servicio sin tener que realizar un acceso completo de lectura de la colección completa de recursos. Para obtener más información, vea [Uso de consulta de Delta](/graph/delta-query-overview) .

## <a name="permissions"></a>Permisos

Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).


|Tipo de permiso      | Permisos (de menos a más privilegiados)              |
|:--------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa) | Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All    |
|Delegado (cuenta personal de Microsoft) | No admitida.    |
|Aplicación | Application.ReadWrite.All, Directory.Read.All |

## <a name="http-request"></a>Solicitud HTTP

Para comenzar el seguimiento de los cambios, realizar una solicitud que incluya la función delta en el recurso servicePrincipal. 

<!-- { "blockType": "ignored" } -->
```http
GET /servicePrincipals/delta
```

### <a name="query-parameters"></a>Parámetros de consulta

Seguimiento de los cambios incurre una ronda de una o más llamadas de función de **delta** . Si usa cualquier parámetro de consulta (distinto de `$deltatoken` y `$skiptoken`), debe especificar en la solicitud inicial del **delta** . Microsoft Graph codifica automáticamente los parámetros especificados en la parte de símbolo (token) de la `nextLink` o `deltaLink` dirección URL proporcionada en la respuesta. Solo debe especificar una vez por adelantado los parámetros de consulta deseados. En solicitudes posteriores, copie y aplique la dirección URL `nextLink` o `deltaLink` de la respuesta anterior, dado que la dirección URL ya incluye los parámetros codificados deseados.

| Parámetro de consulta      | Tipo   |Descripción|
|:---------------|:--------|:----------|
| $deltatoken | string | Un [símbolo (token) de estado](/graph/delta-query-overview) devuelto en el `deltaLink` dirección URL de la llamada de función **delta** anterior para la misma colección de recursos, que indica la finalización de ese round de seguimiento de cambios. Guardar y aplicar todo el `deltaLink` dirección URL incluido este token en la primera solicitud de la siguiente ronda de seguimiento de cambios para esa colección.|
| $skiptoken | string | Un [símbolo (token) de estado](/graph/delta-query-overview) devuelto en el `nextLink` dirección URL de la llamada de función **delta** anterior, que indica que hay más cambios para realizar un seguimiento en la misma colección de recursos. |

## <a name="optional-query-parameters"></a>Parámetros de consulta opcionales

Este método admite parámetros de consulta de OData a modo de ayuda para personalizar la respuesta.

- Puede utilizar un parámetro de consulta `$select` como en cualquier solicitud GET para especificar solo las propiedades que necesita para un mejor rendimiento. Siempre se devuelve la propiedad _id_. 

- No hay compatibilidad limitada para `$filter`:
  * El único admitido `$filter` expresión es para realizar un seguimiento de cambios para recursos específicos, por su identificador: `$filter=id+eq+{value}` o `$filter=id+eq+{value1}+or+id+eq+{value2}`. El número de identificadores que puede especificar está limitado por la longitud máxima de dirección URL.


## <a name="request-headers"></a>Encabezados de solicitud
| Nombre       | Descripción|
|:---------------|:----------|
| Authorization  | &lt;token&gt; de portador|
| Content-Type  | application/json |

## <a name="request-body"></a>Cuerpo de la solicitud
No proporcione un cuerpo de solicitud para este método.

### <a name="response"></a>Respuesta

Si tiene éxito, este método devuelve `200 OK` objeto de colección de respuesta código y [servicePrincipal](../resources/serviceprincipal.md) en el cuerpo de la respuesta. La respuesta incluye también una dirección URL de nextLink o una dirección URL de deltaLink. 

- Si un `nextLink` se devuelve la dirección URL, hay páginas adicionales de datos que se recuperarán en la sesión. La aplicación continúa realizar solicitudes mediante el `nextLink` dirección URL hasta un `deltaLink` dirección URL se incluye en la respuesta.

- Si un `deltaLink` se devuelve la dirección URL, no hay ningún dato más sobre el estado existente del recurso que se devolverá. Conservar y utilizar el `deltaLink` dirección URL para obtener más información acerca de los cambios realizados en el recurso en el futuro.

Vea:</br>
- [Usar la consulta delta](/graph/delta-query-overview) para obtener más detalles.</br>
- [Obtener los cambios incrementales de usuarios](/graph/delta-query-users) para obtener un ejemplo de solicitud.</br>

### <a name="example"></a>Ejemplo
##### <a name="request"></a>Solicitud
<!-- {
  "blockType": "request",
  "name": "servicePrincipal_delta"
}-->
```http
GET https://graph.microsoft.com/beta/servicePrincipals/delta
```

##### <a name="response"></a>Respuesta
Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.
<!-- { 
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.servicePrincipal",
  "isCollection": true 
} --> 
```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "@odata.context":"https://graph.microsoft.com/beta/$metadata#servicePrincipals",
  "@odata.nextLink":"https://graph.microsoft.com/beta/servicePrincipals/delta?$skiptoken=pqwSUjGYvb3jQpbwVAwEL7yuI3dU1LecfkkfLPtnIjsXoYQp_dpA3cNJWc",
  "value": [
     {
      "accountEnabled": true,
      "addIns": [
        {
          "id": "id-value",
          "type": "type-value",
          "properties": [
            {
              "key": "key-value",
              "value": "value-value"
            }
          ]
        }
      ],
      "appDisplayName": "appDisplayName-value",
      "appId": "appId-value",
      "appOwnerOrganizationId": "appOwnerOrganizationId-value",
      "appRoleAssignmentRequired": true
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "servicePrincipal: delta",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->