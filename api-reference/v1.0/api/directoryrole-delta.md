---
title: 'directoryRole: delta'
description: Get recién creado, actualiza o elimina roles de Active directory sin tener que realizar un acceso completo de lectura de la colección completa de recursos. Para obtener más información, vea Uso de consulta de Delta.
localization_priority: Normal
author: lleonard-msft
ms.prod: microsoft-identity-platform
ms.openlocfilehash: 6da3e8c4cf92edbf79df1b082675c36d54e81292
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27923844"
---
# <a name="directoryrole-delta"></a>directoryRole: delta

Get recién creado, actualiza o elimina roles de Active directory sin tener que realizar un acceso completo de lectura de la colección completa de recursos. Para obtener más información, vea [Uso de consulta de Delta](/graph/delta-query-overview) .

## <a name="permissions"></a>Permisos

Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).


|Tipo de permiso      | Permisos (de menos a más privilegiados)              |
|:--------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa) | Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All    |
|Delegado (cuenta personal de Microsoft) | No admitida.    |
|Aplicación | Directory.Read.All, Directory.ReadWrite.All |

## <a name="http-request"></a>Solicitud HTTP

Para comenzar el seguimiento de los cambios, realizar una solicitud que incluya la función **delta** en el recurso [directoryRole](../resources/directoryrole.md) .

<!-- { "blockType": "ignored" } -->
```http
GET /directoryRoles/delta
```

## <a name="query-parameters"></a>Parámetros de consulta

Seguimiento de los cambios incurre una ronda de una o más llamadas de función de **delta** . Si usa cualquier parámetro de consulta (distinto de `$deltatoken` y `$skiptoken`), debe especificar en la solicitud inicial del **delta** . Microsoft Graph codifica automáticamente los parámetros especificados en la parte de símbolo (token) de la `nextLink` o `deltaLink` dirección URL proporcionada en la respuesta. Solo debe especificar una vez por adelantado los parámetros de consulta deseados. En solicitudes posteriores, copie y aplique la dirección URL `nextLink` o `deltaLink` de la respuesta anterior, dado que la dirección URL ya incluye los parámetros codificados deseados.

| Parámetro de consulta      | Tipo   |Descripción|
|:---------------|:--------|:----------|
| $deltatoken | string | Un [símbolo (token) de estado](/graph/delta-query-overview) devuelto en el `deltaLink` dirección URL de la llamada de función **delta** anterior para la misma colección de recursos, que indica la finalización de ese round de seguimiento de cambios. Guardar y aplicar todo el `deltaLink` dirección URL incluido este token en la primera solicitud de la siguiente ronda de seguimiento de cambios para esa colección.|
| $skiptoken | string | Un [símbolo (token) de estado](/graph/delta-query-overview) devuelto en el `nextLink` dirección URL de la llamada de función **delta** anterior, que indica que hay más cambios para realizar un seguimiento en la misma colección de recursos. |

### <a name="odata-query-parameters"></a>Parámetros de consulta de OData

Este método es compatible con los parámetros de consulta de OData para ayudar a personalizar la respuesta.

- Puede utilizar un parámetro de consulta `$select` como en cualquier solicitud GET para especificar solo las propiedades que necesita para un mejor rendimiento. Siempre se devuelve la propiedad _id_.

- No hay compatibilidad limitada para `$filter`:

  - El único admitido `$filter` expresión es para realizar un seguimiento de cambios para recursos específicos, por su identificador: `$filter=id+eq+{value}` o `$filter=id+eq+{value1}+or+id+eq+{value2}`. El número de identificadores que puede especificar está limitado por la longitud máxima de dirección URL.

## <a name="request-headers"></a>Encabezados de solicitud

| Nombre       | Descripción|
|:---------------|:----------|
| Authorization  | &lt;token&gt; de portador|
| Content-Type  | application/json |

## <a name="request-body"></a>Cuerpo de la solicitud

No proporcione un cuerpo de solicitud para este método.

### <a name="response"></a>Respuesta

Si tiene éxito, este método devuelve `200 OK` objeto de colección de respuesta código y [directoryRole](../resources/directoryrole.md) en el cuerpo de la respuesta. La respuesta incluye también un `nextLink` dirección URL o un `deltaLink` dirección URL.

- Si un `nextLink` se devuelve la dirección URL, hay páginas adicionales de datos que se recuperarán en la sesión. La aplicación continúa realizar solicitudes mediante el `nextLink` dirección URL hasta un `deltaLink` dirección URL se incluye en la respuesta.

- Si un `deltaLink` se devuelve la dirección URL, no hay ningún dato más sobre el estado existente del recurso que se devolverá. Guardar `deltaLink` dirección URL y aplicar en la siguiente llamada **delta** para obtener más información acerca de los cambios realizados en el recurso en el futuro.

### <a name="example"></a>Ejemplo

##### <a name="request"></a>Solicitud

<!-- {
  "blockType": "request",
  "name": "directoryRole_delta"
}-->

```http
GET https://graph.microsoft.com/v1.0/directoryRoles/delta
```

##### <a name="response"></a>Respuesta

Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.
<!-- { 
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.directoryRole",
  "isCollection": true 
} --> 
```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "@odata.context":"https://graph.microsoft.com/v1.0/$metadata#directoryRoles",
  "@odata.nextLink":"https://graph.microsoft.com/v1.0/directoryRoles/delta?$skiptoken=pqwSUjGYvb3jQpbwVAwEL7yuI3dU1LecfkkfLPtnIjsXoYQp_dpA3cNJWc",
  "value": [
      {
      "description": "description-value",
      "displayName": "displayName-value",
      "roleTemplateId": "roleTemplateId-value",
      "id": "id-value"
    }
  ]
}
```

### <a name="see-also"></a>Consulte también

- [Consulta de delta de uso para realizar un seguimiento de los cambios en datos de Microsoft Graph](/graph/delta-query-overview) para obtener más detalles
- [Obtener los cambios incrementales de usuarios](/graph/delta-query-users) para obtener un ejemplo de solicitud.

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "directoryRole: delta",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
