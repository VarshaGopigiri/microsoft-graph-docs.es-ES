# <a name="group-delta"></a>grupo: delta
La [consulta delta](../../../concepts/delta_query_overview.md) permite a las aplicaciones detectar entidades recién creadas, actualizadas o eliminadas sin realizar una operación de lectura completa del recurso de destino con cada solicitud. Para detectar cambios en grupos, realice una solicitud usando la función *delta*. Consulte [Usar la consulta delta](../../../concepts/delta_query_overview.md) para obtener más detalles.

## <a name="permissions"></a>Permisos
Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).

|Tipo de permiso      | Permisos (de menos a más privilegiados)              |
|:--------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa) | Group.Read.All, Group.ReadWrite.All    |
|Delegado (cuenta personal de Microsoft) | No admitida.    |
|Aplicación | Group.Read.All, Group.ReadWrite.All |

## <a name="http-request"></a>Solicitud HTTP
Para comenzar los cambios, debe realizar una solicitud incluyendo la función delta en el recurso grupo.

<!-- { "blockType": "ignored" } -->
```http
GET /groups/delta
```

## <a name="query-parameters"></a>Parámetros de consulta
El seguimiento de cambios en grupos conlleva al menos una llamada de una función **delta**. Si usa cualquier parámetro de consulta (uno diferente a `$deltatoken` y `$skiptoken`), debe especificarlo en la solicitud **delta** inicial. Microsoft Graph codifica automáticamente cualquier parámetro especificado en la parte del token de la URL `nextLink` o `deltaLink` proporcionada en la respuesta.

Solo debe especificar una vez por adelantado los parámetros de consulta deseados.

En solicitudes posteriores, copie y aplique la dirección URL `nextLink` o `deltaLink` de la respuesta anterior, dado que la dirección URL ya incluye los parámetros codificados deseados.

| Parámetro de consulta      | Tipo   |Descripción|
|:---------------|:--------|:----------|
| $deltatoken | cadena | Un [token de estado](../../../concepts/delta_query_overview.md) que se devuelve en la URL de `deltaLink` de la llamada de función **delta** anterior para la misma colección de grupos. Indica el progreso de la ronda de seguimiento de cambios. Guarde y aplique toda la dirección URL `deltaLink`, incluido este token, en la primera solicitud de la siguiente ronda de seguimiento de cambios de la colección.|
| $skiptoken | cadena | Un [token de estado](../../../concepts/delta_query_overview.md) que se devuelve en la URL de `nextLink` de la llamada de función **delta**. Indica que debe realizarse el seguimiento de más cambios en la misma colección de grupos. |

### <a name="odata-query-parameters"></a>Parámetros de consulta de OData
Este método admite los parámetros opcionales de consulta de OData a modo de ayuda para personalizar la respuesta.

- Puede utilizar un parámetro de consulta `$select` como en cualquier solicitud GET para especificar solo las propiedades que necesita para un mejor rendimiento. Siempre se devuelve la propiedad _id_.
- Compatibilidad con consultas delta `$select`, `$top`, y `$expand` para los grupos.
- Hay compatibilidad limitada para `$filter` y `$orderby`:
  * La única expresión `$filter` admitida es para realizar un seguimiento de los cambios en un objeto específico: `$filter=id+eq+{value}`. Puede filtrar varios objetos. Por ejemplo, `https://graph.microsoft.com/v1.0/groups/delta/?$filter= id eq '477e9fc6-5de7-4406-bb2a-7e5c83c9ffff' or id eq '004d6a07-fe70-4b92-add5-e6e37b8affff`. Hay un límite de 50 objetos filtrados.
- No hay compatibilidad con `$search`.

## <a name="request-headers"></a>Encabezados de solicitud
| Nombre       | Descripción|
|:---------------|:----------|
| Authorization  | token&gt; de portador&gt;|
| Content-Type  | application/json |

## <a name="request-body"></a>Cuerpo de la solicitud
No proporcione un cuerpo de solicitud para este método.

## <a name="response"></a>Respuesta
Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto de colección [grupo](../resources/group.md) en el cuerpo de la respuesta. La respuesta también incluye un token de estado, que puede ser una URL de nextLink o de deltaLink.

- Si se devuelve una dirección URL nextLink, hay más páginas de datos para recuperar en la sesión. La aplicación continúa realizando solicitudes mediante la dirección URL nextLink hasta que se incluya una dirección URL deltaLink en la respuesta.

- Si se devuelve la dirección URL deltaLink, no hay que devolver más datos sobre el estado existente del recurso. En solicitudes futuras, la aplicación usa la dirección URL deltaLink para obtener información sobre los cambios en el recurso.

Vea:</br>
- [Usar la consulta delta](../../../concepts/delta_query_overview.md) para obtener más detalles.</br>
- [Obtener cambios incrementales de grupos](../../../concepts/delta_query_groups.md) para obtener una explicación más detallada.</br>

## <a name="example"></a>Ejemplo
#### <a name="request"></a>Solicitud
Aquí tiene un ejemplo de la solicitud.
<!-- {
  "blockType": "request",
  "name": "group_delta"
}-->
```http
GET https://graph.microsoft.com/v1.0/groups/delta
```

#### <a name="response"></a>Respuesta
Aquí tiene un ejemplo de la respuesta.
>**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.
>
> Tenga en cuenta la presencia de la propiedad *members@delta*, que incluye los identificadores de objetos miembros en el grupo.

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.group",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "@odata.context":"https://graph.microsoft.com/v1.0/$metadata#groups","@odata.nextLink":"https://graph.microsoft.com/v1.0/groups/delta?$skiptoken=pqwSUjGYvb3jQpbwVAwEL7yuI3dU1LecfkkfLPtnIjvY1FSSc_",
  "value":[
    {
      "classification": "classification-value",
      "createdDateTime":"datetime-value",
      "description":"Test group 1",
      "displayName":"TestGroup1",
      "groupTypes": [
        "groupTypes-value"
      ],
      "mail": "mail-value",
      "members@delta": [
               {
                   "@odata.type": "#microsoft.graph.user",
                   "id": "693acd06-2877-4339-8ade-b704261fe7a0"
               },
               {
                   "@odata.type": "#microsoft.graph.user",
                   "id": "49320844-be99-4164-8167-87ff5d047ace"
               }
      ]
    }
  ]
}
```

## <a name="see-also"></a>Vea también
- [Usar la consulta delta](../../../concepts/delta_query_overview.md) para obtener más detalles.
- [Obtener cambios incrementales de grupos](../../../concepts/delta_query_groups.md) para obtener una explicación más detallada.

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "group: delta",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
