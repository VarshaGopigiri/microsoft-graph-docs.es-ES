# <a name="mailfolder-delta"></a>mailFolder: delta

Obtenga un conjunto de carpetas de correo que se hayan agregado, eliminado o quitado del buzón del usuario.

Las llamadas de una función **delta** para las carpetas de correo de un buzón funcionan de forma similar a una solicitud GET, salvo que, al aplicar correctamente [tokens de estado](../../../concepts/delta_query_overview.md) en al menos una de estas llamadas, puede realizar una consulta para obtener los cambios incrementales en las carpetas de correo. Esto permite mantener y sincronizar un almacén local de carpetas de correo de un usuario, sin tener que capturar cada vez todas las carpetas de correo de ese buzón desde el servidor.

## <a name="permissions"></a>Permisos
Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).


|Tipo de permiso      | Permisos (de menos a más privilegiados)              |
|:--------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa) | Mail.Read, Mail.ReadWrite    |
|Delegado (cuenta personal de Microsoft) | Mail.Read, Mail.ReadWrite    |
|Aplicación | Mail.Read, Mail.ReadWrite |

## <a name="http-request"></a>Solicitud HTTP
<!-- { "blockType": "ignored" } -->
```http
GET /me/mailFolders/delta
GET /users/{id}/mailFolders/delta
```

## <a name="query-parameters"></a>Parámetros de consulta

El seguimiento de cambios en las carpetas de correo conlleva al menos una llamada de una función **delta**. Si usa cualquier parámetro de consulta (distinto de `$deltatoken` y `$skiptoken`), debe especificarlo en la solicitud **delta** inicial. Microsoft Graph codifica automáticamente cualquier parámetro especificado en la parte del token de la URL `nextLink` o `deltaLink` proporcionada en la respuesta. Solo debe especificar los parámetros de consulta deseados una vez por adelantado. En solicitudes posteriores, basta con copiar y aplicar la dirección URL `nextLink` o `deltaLink` de la respuesta anterior, dado que la dirección URL ya incluye los parámetros codificados deseados.

| Parámetro de consulta      | Tipo   |Descripción|
|:---------------|:--------|:----------|
| $deltatoken | string | Un [token de estado](../../../concepts/delta_query_overview.md) que se devuelve en la dirección URL de `deltaLink` de la llamada de función **delta** anterior para la misma colección de carpetas de correo. Indica el progreso de la ronda de seguimiento de cambios. Guarde y aplique toda la dirección URL `deltaLink`, incluido este token, en la primera solicitud de la siguiente ronda de seguimiento de cambios de la colección.|
| $skiptoken | string | Un [token de estado](../../../concepts/delta_query_overview.md) que se devuelve en la dirección URL de `nextLink` de la llamada de función **delta**. Indica que debe realizarse el seguimiento de más cambios en la misma colección de carpetas de correo. |

### <a name="odata-query-parameters"></a>Parámetros de consulta de OData

Puede utilizar un parámetro de consulta `$select` como en cualquier solicitud GET para especificar solo las propiedades que necesita para un mejor rendimiento. Siempre se devuelve la propiedad _id_. 

## <a name="request-headers"></a>Encabezados de solicitud
| Nombre       | Tipo | Descripción |
|:---------------|:----------|:----------|
| Authorization  | string  | {token} de portador. Obligatorio. |
| Content-Type  | string  | application/json. Obligatorio. |
| Prefer | string  | odata.maxpagesize={x}. Opcional. |

## <a name="response"></a>Respuesta

Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto de colección [mailFolder](../resources/mailfolder.md) en el cuerpo de la respuesta.

## <a name="example"></a>Ejemplo
##### <a name="request"></a>Solicitud
En el ejemplo siguiente se muestra cómo realizar una llamada de función **delta** única y limitar el número máximo de carpetas de correo en el cuerpo de la respuesta a 2.

Para realizar un seguimiento de los cambios de las carpetas de correo de un buzón, debería realizar al menos una llamada de función **delta**, con unos tokens de estado adecuados, para obtener el conjunto de cambios incrementales desde la última consulta delta. 

Encontrará un ejemplo similar en el que se muestra cómo usar los tokens de estado para realizar un seguimiento de los cambios en los mensajes de una carpeta de correo: [Obtener los cambios incrementales en los mensajes de una carpeta](../../../concepts/delta_query_messages.md). Las diferencias principales entre realizar un seguimiento de las carpetas de correo y realizar un seguimiento de los mensajes en una carpeta están en las direcciones URL de consulta delta. Además, las respuestas de consulta devuelven colecciones **mailFolder** en lugar de colecciones **message**.

<!-- {
  "blockType": "request",
  "name": "mailfolder_delta"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/mailFolders/delta

Prefer: odata.maxpagesize=2
```

##### <a name="response"></a>Respuesta

Si la solicitud es correcta, la respuesta debería incluir un símbolo de estado, que puede ser un _skipToken_  
(en un encabezado de respuesta de _@odata.nextLink_) o un _deltaToken_ (en un encabezado de respuesta de _@odata.deltaLink_). Respectivamente, indican si debe continuar con la ronda, o bien si ha terminado de obtener todos los cambios de la ronda.

La respuesta siguiente muestra un _skipToken_ en un encabezado de respuesta de _@odata.nextLink_.

Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.mailFolder",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 254

{
  "@odata.nextLink":"https://graph.microsoft.com/v1.0/me/mailfolders/delta?$skiptoken={_skipToken_}",
  "value": [
    {
      "displayName": "displayName-value",
      "parentFolderId": "parentFolderId-value",
      "childFolderCount": 99,
      "unreadItemCount": 99,
      "totalItemCount": 99
    }
  ]
}
```

### <a name="see-also"></a>Recursos adicionales

- [Usar la consulta delta para realizar el seguimiento de los cambios en datos de Microsoft Graph](../../../concepts/delta_query_overview.md)
- [Obtener los cambios incrementales en los mensajes de una carpeta](../../../concepts/delta_query_messages.md)

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "mailFolder: delta",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
