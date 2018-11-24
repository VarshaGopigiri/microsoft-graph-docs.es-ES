# <a name="user-delta"></a>user: delta

Get recién creado, actualiza o elimina los usuarios sin tener que realizar un acceso completo de lectura de la colección completa de usuario. Para obtener información detallada, vea [control de cambios](../../../concepts/delta_query_overview.md) .

## <a name="permissions"></a>Permisos

Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).


|Tipo de permiso      | Permisos (de menos a más privilegiados)              |
|:--------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa) | User.Read, User.ReadWrite, User.ReadBasic.All, User.Read.All, User.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All    |
|Delegado (cuenta personal de Microsoft) | User.Read, User.ReadWrite    |
|Aplicación | User.Read.All, User.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All |

## <a name="http-request"></a>Solicitud HTTP

Para comenzar los cambios, debe realizar una solicitud incluyendo la función delta en el recurso de los usuarios.

<!-- { "blockType": "ignored" } -->
```http
GET /users/delta
```

## <a name="query-parameters"></a>Parámetros de consulta

Seguimiento de los cambios en los usuarios incurre en una ronda de una o más llamadas de función de **delta** . Si usa cualquier parámetro de consulta (distinto de `$deltatoken` y `$skiptoken`), debe especificar en la solicitud inicial del **delta** . Microsoft Graph codifica automáticamente los parámetros especificados en la parte de símbolo (token) de la `nextLink` o `deltaLink` dirección URL proporcionada en la respuesta.

Solo debe especificar una vez por adelantado los parámetros de consulta deseados.

En solicitudes posteriores, copie y aplique la dirección URL `nextLink` o `deltaLink` de la respuesta anterior, dado que la dirección URL ya incluye los parámetros codificados deseados.

| Parámetro de consulta      | Tipo   |Descripción|
|:---------------|:--------|:----------|
| $deltatoken | string | Un [token de estado](../../../concepts/delta_query_overview.md) que se devuelve en la dirección URL de `deltaLink` de la llamada de función **delta** anterior para la misma colección de usuarios. Indica el progreso de la ronda de seguimiento de cambios. Guarde y aplique toda la dirección URL `deltaLink`, incluido este token, en la primera solicitud de la siguiente ronda de seguimiento de cambios de la colección.|
| $skiptoken | string | Un [token de estado](../../../concepts/delta_query_overview.md) que se devuelve en la dirección URL de `nextLink` de la llamada de función **delta**. Indica que debe realizarse el seguimiento de más cambios en la misma colección de usuarios. |

### <a name="odata-query-parameters"></a>Parámetros de consulta de OData

Este método es compatible con parámetros opcionales de consulta de OData para ayudar a personalizar la respuesta.

- Puede utilizar un parámetro de consulta `$select` como en cualquier solicitud GET para especificar solo las propiedades que necesita para un mejor rendimiento. Siempre se devuelve la propiedad *id*.
- No hay compatibilidad limitada para `$filter`:
  - La única expresión `$filter` admitida es para realizar un seguimiento de los cambios en un objeto específico: `$filter=id+eq+{value}`. Puede filtrar varios objetos. Por ejemplo, `https://graph.microsoft.com/v1.0/users/delta/?$filter= id eq '477e9fc6-5de7-4406-bb2a-7e5c83c9ffff' or id eq '004d6a07-fe70-4b92-add5-e6e37b8affff'`. Hay un límite de 50 objetos filtrados.

## <a name="request-headers"></a>Encabezados de solicitud
| Nombre       | Descripción|
|:---------------|:----------|
| Authorization  | &lt;token&gt; de portador|
| Content-Type  | application/json |
| Prefer | devolver = mínimo <br><br>Si se especifica este encabezado con una solicitud que utiliza un `deltaLink` devolvería sólo las propiedades del objeto que han cambiado desde la última round. Opcional. |

## <a name="request-body"></a>Cuerpo de la solicitud
No proporcione un cuerpo de solicitud para este método.

### <a name="response"></a>Respuesta

Si tiene éxito, este método devuelve `200 OK` objeto de colección de respuesta código y [usuario](../resources/user.md) en el cuerpo de la respuesta. La respuesta incluye también un `nextLink` dirección URL o un `deltaLink` dirección URL.

- Si un `nextLink` se devuelve la dirección URL:
  - Esto indica que hay páginas adicionales de datos que se recuperarán en la sesión. La aplicación continúa realizar solicitudes mediante el `nextLink` dirección URL hasta un `deltaLink` dirección URL se incluye en la respuesta.
  - La respuesta incluye el mismo conjunto de propiedades como se muestra en la solicitud de consulta delta inicial. Esto le permite capturar el estado actual y completa de los objetos al iniciar el ciclo de delta.

- Si un `deltaLink` se devuelve la dirección URL:
  - Esto indica que no hay ningún dato más sobre el estado existente del recurso que se devolverá. Guardar y utilizar el `deltaLink` dirección URL para obtener más información acerca de cambia para el recurso en la ronda siguiente.
  - Tiene una opción para especificar el `Prefer:return=minimal` encabezado, que se incluirá en los valores de respuesta sólo para las propiedades que han cambiado desde el momento en que el `deltaLink` se emitió.

#### <a name="default-return-the-same-properties-as-initial-delta-request"></a>Valor predeterminado: devolver las mismas propiedades que la solicitud inicial del delta

De forma predeterminada, las solicitudes con un `deltaLink` o `nextLink` devolver las mismas propiedades como seleccionado en la consulta inicial del delta de las siguientes maneras:

- Si la propiedad ha cambiado, devuelva la propiedad en la respuesta JSON.
- Si se ha establecido la propiedad en un valor vacío, devuelve el valor de la propiedad como null.
- Si la propiedad no ha cambiado, devolver el valor como null.

> **Nota:** Con el comportamiento anterior, no es posible diferenciar entre una propiedad que no ha cambiado y uno que ha cambiado a un `null` valor. Vea el [segundo ejemplo](#request-2) siguiente. Si esto es importante, se recomienda usar el comportamiento alternativo que se describen en la siguiente sección.

#### <a name="alternative-return-only-the-changed-properties"></a>Alternativa: devolver sólo las propiedades modificadas

Adición de un encabezado de solicitud opcional - `prefer:return=minimal` -da como resultado el siguiente comportamiento:

- Si la propiedad ha cambiado, devuelva la propiedad en la respuesta JSON.
- Si se ha establecido la propiedad en un valor vacío, devuelve el valor de la propiedad como null.
- Si la propiedad no ha cambiado, no incluya la propiedad en la respuesta JSON. (Distinto del comportamiento predeterminado).

> **Nota:** El encabezado puede agregarse a un `deltaLink` solicitud en cualquier momento en el ciclo de delta. El encabezado sólo afecta el conjunto de propiedades que se incluyen en la respuesta y no afecta a cómo se ejecuta la consulta de delta. Vea el [tercer ejemplo](#request-3) siguiente.

### <a name="example"></a>Ejemplo

#### <a name="request-1"></a>Solicitud 1

Aquí tiene un ejemplo de la solicitud. No hay ningún `$select` parámetro, por lo que se realiza un seguimiento y devuelve un conjunto predeterminado de propiedades.
<!-- {
  "blockType": "request",
  "name": "user_delta"
}-->

```http
GET https://graph.microsoft.com/v1.0/users/delta
```

#### <a name="response-1"></a>Respuesta 1

El siguiente es un ejemplo de la respuesta al usar `deltaLink` obtenido de la inicialización de la consulta.

>**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.user",
  "isCollection": true
} -->

```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "@odata.context":"https://graph.microsoft.com/v1.0/$metadata#users",
  "@odata.nextLink":"https://graph.microsoft.com/v1.0/users/delta?$skiptoken=pqwSUjGYvb3jQpbwVAwEL7yuI3dU1LecfkkfLPtnIjsXoYQp_dpA3cNJWc",
  "value": [
    {
      "businessPhones": [
          "businessPhones-value"
      ],
      "displayName": "displayName-value",
      "givenName": "givenName-value",
      "jobTitle": "jobTitle-value",
      "mail": "mail-value",
      "mobilePhone": "mobilePhone-value",
      "officeLocation": "officeLocation-value",
      "preferredLanguage": "preferredLanguage-value",
      "surname": "surname-value",
      "userPrincipalName": "userPrincipalName-value",
      "id": "id-value"
    }
  ]
}
```

#### <a name="request-2"></a>Solicitud 2

En el ejemplo siguiente se muestra la solicitud inicial seleccionando 3 propiedades para el seguimiento de cambios, con comportamiento de respuesta predeterminado:
<!-- {
  "blockType": "request",
  "name": "user_delta"
}-->

```http
GET https://graph.microsoft.com/v1.0/users/delta?$select=displayName,jobTitle,mobilePhone
```

#### <a name="response-2"></a>Respuesta 2

El siguiente es un ejemplo de la respuesta al usar `deltaLink` obtenido de la inicialización de la consulta. Tenga en cuenta que `jobTitle` y `mobilePhone` tienen el valor de `null` lo que significa que es posible que no se han cambiado o se han establecido en un valor vacío.

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.user",
  "isCollection": true
} -->

```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "@odata.context":"https://graph.microsoft.com/v1.0/$metadata#users",
  "@odata.nextLink":"https://graph.microsoft.com/v1.0/users/delta?$skiptoken=pqwSUjGYvb3jQpbwVAwEL7yuI3dU1LecfkkfLPtnIjsXoYQp_dpA3cNJWc",
  "value": [
    {
      "displayName": "displayName-value",
      "jobTitle": null,
      "mobilePhone": null
    }
  ]
}
```

#### <a name="request-3"></a>Solicitud 3

En el ejemplo siguiente se muestra la solicitud inicial seleccionando 3 propiedades para el seguimiento de cambios, con el comportamiento de respuesta mínimo alternativo:
<!-- {
  "blockType": "request",
  "name": "user_delta"
}-->

```http
GET https://graph.microsoft.com/v1.0/users/delta?$select=displayName,jobTitle,mobilePhone
Prefer: return=minimal
```

#### <a name="response-3"></a>Respuesta 3

El siguiente es un ejemplo de la respuesta al usar `deltaLink` obtenido de la inicialización de la consulta. Tenga en cuenta que el `mobilePhone` (propiedad) no se incluye, lo que significa que no ha cambiado desde la última consulta delta; `displayName` y `jobTitle` se incluyen lo que significa que se han cambiado sus valores.

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.user",
  "isCollection": true
} -->

```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "@odata.context":"https://graph.microsoft.com/v1.0/$metadata#users",
  "@odata.nextLink":"https://graph.microsoft.com/v1.0/users/delta?$skiptoken=pqwSUjGYvb3jQpbwVAwEL7yuI3dU1LecfkkfLPtnIjsXoYQp_dpA3cNJWc",
  "value": [
    {
      "displayName": "displayName-value",
      "jobTitle": null
    }
  ]
}
```

- [Consulta de delta de uso para realizar un seguimiento de los cambios en datos de Microsoft Graph](../../../concepts/delta_query_overview.md).
- [Obtener cambios incrementales para los usuarios](../../../concepts/delta_query_users.md).

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "user: delta",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->