---
title: 'directoryObject: delta'
description: 'Get recién creado, actualizar o eliminar objetos de Active directory de los siguientes tipos: usuario, grupo y contacto organizativa, en una consulta de delta único. Vea control de cambios para obtener información detallada.'
localization_priority: Normal
ms.openlocfilehash: 823107bce56d77c4e9c29a77405ac014443f5190
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27854498"
---
# <a name="directoryobject-delta"></a>directoryObject: delta

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Get recién creado, actualizar o eliminar objetos de Active directory de los siguientes tipos: [usuario](../resources/user.md), [grupo](../resources/group.md) y [contacto organizativa](../resources/orgcontact.md), en una consulta de delta único. Para obtener información detallada, vea [control de cambios](/graph/delta-query-overview) .

## <a name="permissions"></a>Permisos

Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).

|Tipo de permiso      | Permisos (de menos a más privilegiados)              |
|:--------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa) | Directory.Read.All, Directory.AccessAsUser.All  |
|Delegado (cuenta personal de Microsoft) | No admitida.  |
|Aplicación | Directory.Read.All, Directory.ReadWrite.All |

## <a name="http-request"></a>Solicitud HTTP

Para comenzar el seguimiento de los cambios, realizar una solicitud que incluya la función delta en el recurso directoryObjects.

<!-- { "blockType": "ignored" } -->

```http
GET /directoryObjects/delta
```

## <a name="query-parameters"></a>Parámetros de consulta

Seguimiento de los cambios incurre una ronda de una o más llamadas de función de **delta** . Si usa cualquier parámetro de consulta (distinto de `$deltatoken` y `$skiptoken`), debe especificar en la solicitud inicial del **delta** . Microsoft Graph codifica automáticamente los parámetros especificados en la parte de símbolo (token) de la `nextLink` o `deltaLink` dirección URL proporcionada en la respuesta.

Solo debe especificar una vez por adelantado los parámetros de consulta deseados.

En solicitudes posteriores, copie y aplique la dirección URL `nextLink` o `deltaLink` de la respuesta anterior, dado que la dirección URL ya incluye los parámetros codificados deseados.

| Parámetro de consulta | Tipo |Descripción|
|:---------------|:--------|:----------|
| $deltatoken | string | Un [token de estado](/graph/delta-query-overview) que se devuelve en la dirección URL de `deltaLink` de la llamada de función **delta** anterior para la misma colección de usuarios. Indica el progreso de la ronda de seguimiento de cambios. Guarde y aplique toda la dirección URL `deltaLink`, incluido este token, en la primera solicitud de la siguiente ronda de seguimiento de cambios de la colección.|
| $skiptoken | string | Un [token de estado](/graph/delta-query-overview) que se devuelve en la dirección URL de `nextLink` de la llamada de función **delta**. Indica que debe realizarse el seguimiento de más cambios en la misma colección de usuarios. |

### <a name="odata-query-parameters"></a>Parámetros de consulta de OData

Este método es compatible con parámetros opcionales de consulta de OData para ayudar a personalizar la respuesta.

- Puede usar `$filter` con especial `isOf` operador que se debe filtrar un subconjunto de tipos derivados de directoryObject.
  - Puede combinar varias expresiones con una `or`, que le permite tener una consulta delta único varios tipos de seguimiento. Vea el [tercer ejemplo](#request-3) para obtener información detallada.

## <a name="request-headers"></a>Encabezados de solicitud

| Nombre       | Descripción|
|:---------------|:----------|
| Authorization  | &lt;token&gt; de portador|
| Content-Type  | application/json |
| Prefer | devolver = mínimo <br><br>Si se especifica este encabezado con una solicitud que utiliza un `deltaLink` devolvería sólo las propiedades del objeto que han cambiado desde la última round. Opcional. |

## <a name="request-body"></a>Cuerpo de la solicitud

No proporcione un cuerpo de solicitud para este método.

### <a name="response"></a>Respuesta

Si tiene éxito, este método devuelve `200 OK` objeto de colección de respuesta código y [usuario](../resources/directoryobject.md) en el cuerpo de la respuesta. La respuesta incluye también un `nextLink` dirección URL o un `deltaLink` dirección URL.

- Si un `nextLink` se devuelve la dirección URL:
  - Esto indica que hay páginas adicionales de datos que se recuperarán en la sesión. La aplicación continúa realizar solicitudes mediante el `nextLink` dirección URL hasta un `deltaLink` dirección URL se incluye en la respuesta.
  - La respuesta incluye el mismo conjunto de propiedades como se muestra en la solicitud de consulta delta inicial. Esto le permite capturar el estado actual y completa de los objetos al iniciar el ciclo de delta.

- Si un `deltaLink` se devuelve la dirección URL:
  - Esto indica que no hay ningún dato más sobre el estado existente del recurso que se devolverá. Guardar y utilizar el `deltaLink` dirección URL para obtener más información acerca de cambia para el recurso en la ronda siguiente.
  - Tiene una opción para especificar el `Prefer:return=minimal` encabezado, que se incluirá en los valores de respuesta sólo para las propiedades que han cambiado desde el momento en que el `deltaLink` se emitió.

#### <a name="default-return-the-same-properties-as-initial-delta-request"></a>Valor predeterminado: devolver las mismas propiedades que la solicitud inicial del delta

De forma predeterminada, las solicitudes con un `deltaLink` o `nextLink` devolver las mismas propiedades como seleccionado en la consulta inicial del delta de las siguientes maneras:

- Si la propiedad ha cambiado, el nuevo valor se incluye en la respuesta. Esto incluye las propiedades que se establezca en un valor null.
- Si no ha cambiado la propiedad, el valor anterior se incluye en la respuesta.
- Si nunca se ha establecido la propiedad antes de no se incluirá en la respuesta en absoluto.


> **Nota:** Con este comportamiento observando la respuesta no es posible saber si va a cambiar de una propiedad o no. Además, las respuestas de delta tienden a ser grandes porque contienen todos los valores de propiedad.

#### <a name="alternative-return-only-the-changed-properties"></a>Alternativa: devolver sólo las propiedades modificadas

Adición de un encabezado de solicitud opcional - `prefer:return=minimal` -da como resultado el siguiente comportamiento:

- Si la propiedad ha cambiado, el nuevo valor se incluye en la respuesta. Esto incluye las propiedades que se establezca en un valor null.
- Si no ha cambiado la propiedad, la propiedad no se incluye en la respuesta en absoluto. (Distinto del comportamiento predeterminado).

> **Nota:** El encabezado puede agregarse a un `deltaLink` solicitud en cualquier momento en el ciclo de delta. El encabezado sólo afecta el conjunto de propiedades que se incluyen en la respuesta y no afecta a cómo se ejecuta la consulta de delta.

## <a name="example"></a>Ejemplo

### <a name="request-1"></a>Solicitud 1

Aquí tiene un ejemplo de la solicitud. No hay ningún `$select` parámetro, por lo que se realiza un seguimiento y devuelve un conjunto predeterminado de propiedades.
<!-- {
  "blockType": "request",
  "name": "user_delta"
}-->

```http
GET https://graph.microsoft.com/beta/directoryObjects/delta
```

### <a name="response-1"></a>Respuesta 1

El siguiente es un ejemplo de la respuesta al usar `deltaLink` obtenido de la inicialización de la consulta. No `isOf` utiliza filtro, por lo que se devuelven todos los tipos derivados de directoryObject.

>**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.directoryObject",
  "isCollection": true
} -->

```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "@odata.context":"https://graph.microsoft.com/beta/$metadata#directoryObjects",
  "@odata.nextLink":"https://graph.microsoft.com/beta/directoryObjects/delta?$skiptoken=pqwSUjGYvb3jQpbwVAwEL7yuI3dU1LecfkkfLPtnIjsXoYQp_dpA3cNJWc",
  "value": [
    {
      "@odata.type": "#microsoft.graph.user",
      "id": "01754bb5-89de-4003-be72-9106a9fb16f2",
      "deletedDateTime": null,
      "accountEnabled": true,
      "ageGroup": null,
      "city": null,
      "companyName": null,
      "consentProvidedForMinor": null,
      "country": null,
      "createdDateTime": null,
      "department": null,
      "displayName": "John Smith",
      "givenName": null,
      "jobTitle": null,
      <...response trimmed for brevity...>
    },
    {
      "@odata.type": "#microsoft.graph.group",
      "id": "cf33844a-b6f8-4d4d-84f4-54e8d45094f0",
      "deletedDateTime": null,
      "classification": null,
      "createdDateTime": "2018-06-20T16:50:09Z",
      "description": null,
      "displayName": "testgp",
      <...response trimmed for brevity...>
    },
    {
      "@odata.type": "#microsoft.graph.orgContact",
      "id": "8f301319-4b4e-493f-8067-bce1dec76e7a",
      "businessPhones": ["string"],
      "city": "string",
      "companyName": "string",
      "country": "string",
      "department": "string",
      "displayName": "string",
      "givenName": "string",
      "id": "string (identifier)",
      "jobTitle": "string",
      <...response trimmed for brevity...>
    },
    <...response trimmed for brevity...>
  ]
}
```

### <a name="request-2"></a>Solicitud 2

En el ejemplo siguiente se muestra el uso del comportamiento de respuesta mínimo alternativo:
<!-- {
  "blockType": "request",
  "name": "directoryObject_delta"
}-->

```http
GET https://graph.microsoft.com/beta/directoryObjects/delta
Prefer: return=minimal
```

### <a name="response-2"></a>Respuesta 2

El siguiente es un ejemplo de la respuesta al usar `deltaLink` obtenido de la inicialización de la consulta. Tenga en cuenta sólo las propiedades que han cambiado realmente se devuelven.

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.directoryObject",
  "isCollection": true
} -->

```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "@odata.context":"https://graph.microsoft.com/beta/$metadata#directoryObjects",
  "@odata.nextLink":"https://graph.microsoft.com/beta/directoryObjects/delta?$skiptoken=pqwSUjGYvb3jQpbwVAwEL7yuI3dU1LecfkkfLPtnIjsXoYQp_dpA3cNJWc",
  "value": [
    {
      "@odata.type": "#microsoft.graph.user",
      "id": "01754bb5-89de-4003-be72-9106a9fb16f2",
      "displayName": "John Smith"
    },
    {
      "@odata.type": "#microsoft.graph.group",
      "id": "cf33844a-b6f8-4d4d-84f4-54e8d45094f0",
      "description": null,
      "displayName": "testgp"
    },
    {
      "@odata.type": "#microsoft.graph.orgContact",
      "id": "8f301319-4b4e-493f-8067-bce1dec76e7a",
      "businessPhones": "12345"
    },
    <...response trimmed for brevity...>
  ]
}
```

### <a name="request-3"></a>Solicitud 3

En el ejemplo siguiente se muestra el uso de la solicitud inicial la `isOf` operador para filtrar sólo las entidades de usuario y de grupo:
<!-- {
  "blockType": "request",
  "name": "directoryobject_delta"
}-->

```http
GET https://graph.microsoft.com/beta/directoryObjects/delta?$filter=isOf('Microsoft.Graph.User')+or+isOf('Microsoft.Graph.Group')
```

### <a name="response-3"></a>Respuesta 3

El siguiente es un ejemplo de la respuesta al usar `deltaLink` obtenido de la inicialización de la consulta. Tenga en cuenta que se devuelven sólo los objetos de usuario y de grupo:

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.directoryObject",
  "isCollection": true
} -->

```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "@odata.context":"https://graph.microsoft.com/beta/$metadata#directoryObjects",
  "@odata.nextLink":"https://graph.microsoft.com/beta/directoryObjects/delta?$skiptoken=pqwSUjGYvb3jQpbwVAwEL7yuI3dU1LecfkkfLPtnIjsXoYQp_dpA3cNJWc",
  "value": [
    {
      "@odata.type": "#microsoft.graph.user",
      "id": "01754bb5-89de-4003-be72-9106a9fb16f2",
      "deletedDateTime": null,
      "accountEnabled": true,
      "ageGroup": null,
      "city": null,
      "companyName": null,
      "consentProvidedForMinor": null,
      "country": null,
      "createdDateTime": null,
      "department": null,
      "displayName": "John Smith",
      "givenName": null,
      "jobTitle": null,
      <...response trimmed for brevity...>
    },
    {
      "@odata.type": "#microsoft.graph.group",
      "id": "cf33844a-b6f8-4d4d-84f4-54e8d45094f0",
      "deletedDateTime": null,
      "classification": null,
      "createdDateTime": "2018-06-20T16:50:09Z",
      "description": null,
      "displayName": "testgp",
      <...response trimmed for brevity...>
    },
    <...response trimmed for brevity...>
  ]
}
```

- [Consulta de delta de uso para realizar un seguimiento de los cambios en datos de Microsoft Graph](/graph/delta-query-overview).
- [Obtener cambios incrementales para los usuarios](/graph/delta-query-users).

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "user: delta",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
