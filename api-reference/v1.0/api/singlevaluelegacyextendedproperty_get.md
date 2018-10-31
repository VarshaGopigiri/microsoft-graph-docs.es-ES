# <a name="get-singlevaluelegacyextendedproperty"></a>Obtener singleValueLegacyExtendedProperty

Puede expandir una única instancia de recursos con una propiedad extendida determinada o una colección de instancias de recursos que incluya propiedades extendidas que coinciden con un filtro.

El uso del parámetro de consulta `$expand` le permite expandir la instancia de recursos especificada con una propiedad extendida específica. Use un operador `$filter` y `eq` en la propiedad **id** para especificar las propiedades extendidas. Actualmente, esta es la única forma de obtener el objeto [singleValueLegacyExtendedProperty](../resources/singleValueLegacyExtendedProperty.md) que representa una propiedad extendida. 

Para obtener las instancias de recursos que tengan ciertas propiedades extendidas, use el parámetro de consulta `$filter` y aplique un operador `eq` en la propiedad **id**. Además, para las propiedades extendidas numéricas, aplique uno de los siguientes operadores en la propiedad **value**: `eq`, `ne`,`ge`, `gt`, `le` o `lt`. Para las propiedades extendidas de tipo cadena, aplique un operador `contains`, `startswith`, `eq` o `ne` en **value**.

El filtro se aplica a todas las instancias del recurso en el buzón del usuario que inició sesión. 

El filtrado del nombre de la cadena (`Name`) en el **id** de una propiedad extendida distingue mayúsculas de minúsculas. El filtrado de la propiedad **value** de una propiedad extendida no distingue mayúsculas de minúsculas.

Se admiten los siguientes recursos de usuario:

- [message](../resources/message.md)
- [mailFolder](../resources/mailfolder.md)
- [event](../resources/event.md)
- [calendar](../resources/calendar.md)
- [contact](../resources/contact.md)
- [contactFolder](../resources/contactfolder.md) 

También los siguientes recursos de grupo:

- [event](../resources/event.md) de grupo
- [calendar](../resources/calendar.md) de grupo
- [post](../resources/post.md) de grupo 

Consulte el artículo de [información general sobre las propiedades extendidas](../resources/extended-properties-overview.md) para obtener más información sobre cuándo usar las extensiones abiertas o las propiedades extendidas y cómo especificar las propiedades extendidas.

## <a name="permissions"></a>Permisos
Según el recurso que seleccione, se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).

- Mail.Read
- Calendars.Read
- Contacts.Read
- Group.Read.All 

## <a name="http-request"></a>Solicitud HTTP

#### <a name="get-a-resource-instance-expanded-with-an-extended-property-that-matches-a-filter"></a>Expandir una instancia de recurso con una propiedad extendida que coincide con un filtro
Expanda una instancia de recurso con la propiedad extendida que coincida con un filtro en la propiedad **id**. Asegúrese de aplicar [la codificación de direcciones URL](http://www.w3schools.com/tags/ref_urlencode.asp) a los caracteres de espacio de la cadena de filtro.

Obtener una instancia de **message**: <!-- { "blockType": "ignored" } -->
```http
GET /me/messages/{id}?$expand=singleValueExtendedProperties($filter=id eq '{id_value}')
GET /users/{id|userPrincipalName}/messages/{id}?$expand=singleValueExtendedProperties($filter=id eq '{id_value}')
GET /me/mailFolders/{id}/messages/{id}?$expand=singleValueExtendedProperties($filter=id eq '{id_value}')
```
Obtener una instancia de **mailFolder**: <!-- { "blockType": "ignored" } -->
```http
GET /me/mailFolders/{id}?$expand=singleValueExtendedProperties($filter=id eq '{id_value}')
GET /users/{id|userPrincipalName}/mailFolders/{id}?$expand=singleValueExtendedProperties($filter=id eq '{id_value}')
```

Obtener una instancia de **event**: <!-- { "blockType": "ignored" } -->
```http
GET /me/events/{id}?$expand=singleValueExtendedProperties($filter=id eq '{id_value}')
GET /users/{id|userPrincipalName}/events/{id}?$expand=singleValueExtendedProperties($filter=id eq '{id_value}')
```
Obtener una instancia de **calendar**: <!-- { "blockType": "ignored" } -->
```http
GET /me/calendars/{id}?$expand=singleValueExtendedProperties($filter=id eq '{id_value}')
GET /users/{id|userPrincipalName}/calendars/{id}?$expand=singleValueExtendedProperties($filter=id eq '{id_value}')
```
Obtener una instancia de **contact**: <!-- { "blockType": "ignored" } -->
```http
GET /me/contacts/{id}?$expand=singleValueExtendedProperties($filter=id eq '{id_value}')
GET /users/{id|userPrincipalName}/contacts/{id}?$expand=singleValueExtendedProperties($filter=id eq '{id_value}')
GET /me/contactFolders/{id}/contacts/{id}?$expand=singleValueExtendedProperties($filter=id eq '{id_value}')
GET /users/{id|userPrincipalName}/contactFolders/{id}/contacts/{id}?$expand=singleValueExtendedProperties($filter=id eq '{id_value}')
```
Obtener una instancia de **contactFolder**: <!-- { "blockType": "ignored" } -->
```http
GET /me/contactfolders/{id}?$expand=singleValueExtendedProperties($filter=id eq '{id_value}')
GET /users/{id|userPrincipalName}/contactFolders/{id}?$expand=singleValueExtendedProperties($filter=id eq '{id_value}')
```
Obtener una instancia de **event** de grupo: <!-- { "blockType": "ignored" } -->
```http
GET /groups/{id}/events/{id}?$expand=singleValueExtendedProperties($filter=id eq '{id_value}')
```

Obtener una instancia de **post** de grupo: <!-- { "blockType": "ignored" } -->
```http
GET /groups/{id}/threads/{id}/posts/{id}?$expand=singleValueExtendedProperties($filter=id eq '{id_value}')
GET /groups/{id}/conversations/{id}/threads/{id}/posts/{id}?$expand=singleValueExtendedProperties($filter=id eq '{id_value}')
```

#### <a name="get-resource-instances-that-include-numeric-extended-properties-matching-a-filter"></a>Obtener instancias de recursos que incluyan propiedades extendidas numéricas que coinciden con un filtro

Obtenga instancias de un recurso compatible que tenga una propiedad extendida numérica que coincide con un filtro. El filtro usa un operador `eq` en la propiedad **id** y uno de los siguientes operadores en la propiedad **value**: `eq`, `ne`,`ge`, `gt` , `le` o `lt`. Asegúrese de aplicar [la codificación de direcciones URL](http://www.w3schools.com/tags/ref_urlencode.asp) a los siguientes caracteres de la cadena de filtro: dos puntos, barra diagonal y espacio.

Las líneas de sintaxis siguientes muestran un filtro que usa un operador `eq` en el Id. y otro operador `eq` en el valor de propiedad. Puede sustituir el operador `eq` en el **valor** por alguno de los otros operadores (`ne`, `ge`, `gt`, `le` o `lt`) que se aplican a los valores numéricos.

Obtener instancias de **message**: <!-- { "blockType": "ignored" } -->
```http
GET /me/messages?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and ep/value eq '{property_value}')
GET /users/{id|userPrincipalName}/messages?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and ep/value eq '{property_value}')
GET /me/mailFolders/{id}/messages?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and ep/value eq '{property_value}')
```
Obtener instancias de **mailFolder**: <!-- { "blockType": "ignored" } -->
```http
GET /me/mailFolders?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and ep/value eq '{property_value}')
GET /users/{id|userPrincipalName}/mailFolders?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and ep/value eq '{property_value}')
```

Obtener instancias de **event**: <!-- { "blockType": "ignored" } -->
```http
GET /me/events?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and ep/value eq '{property_value}')
GET /users/{id|userPrincipalName}/events?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and ep/value eq '{property_value}')
```
Obtener instancias de **calendar**: <!-- { "blockType": "ignored" } -->
```http
GET /me/calendars?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and ep/value eq '{property_value}')
GET /users/{id|userPrincipalName}/calendars?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and ep/value eq '{property_value}')
```
Obtener instancias de **contact**: <!-- { "blockType": "ignored" } -->
```http
GET /me/contacts?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and ep/value eq '{property_value}')
GET /users/{id|userPrincipalName}/contacts?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and ep/value eq '{property_value}')
GET /me/contactFolders/{id}/contacts?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and ep/value eq '{property_value}')
GET /users/{id|userPrincipalName}/contactFolders/{id}/contacts?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and ep/value eq '{property_value}')
```
Obtener instancias de **contactFolder**: <!-- { "blockType": "ignored" } -->
```http
GET /me/contactfolders?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and ep/value eq '{property_value}')
GET /users/{id|userPrincipalName}/contactFolders?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and ep/value eq '{property_value}')
```
Obtener instancias de **event** de grupo: <!-- { "blockType": "ignored" } -->
```http
GET /groups/{id}/events?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and ep/value eq '{property_value}')
```

Obtener instancias de **post** de grupo: <!-- { "blockType": "ignored" } -->
```http
GET /groups/{id}/threads/{id}/posts?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and ep/value eq '{property_value}')
GET /groups/{id}/conversations/{id}/threads/{id}/posts?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and ep/value eq '{property_value}')
```

#### <a name="get-resource-instances-with-string-typed-extended-properties-matching-a-filter"></a>Obtener instancias de recursos con propiedades extendidas de tipo cadena que coinciden con un filtro

Obtenga instancias del recurso **mensaje** o **evento** recursos que tienen una propiedad extendida de tipo cadena que coincide con un filtro. El filtro usa un operador `eq` en la propiedad **id** y uno de los siguientes operadores en la propiedad **value**: `contains`, `startswith`,`eq` o `ne`. Asegúrese de aplicar [la codificación de direcciones URL](http://www.w3schools.com/tags/ref_urlencode.asp) a los siguientes caracteres de la cadena de filtro: dos puntos, barra diagonal y espacio.


Obtener instancias de **message**: <!-- { "blockType": "ignored" } -->
```http
GET /me/messages?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and contains(ep/value, '{property_value}'))
GET /users/{id|userPrincipalName}/messages?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and contains(ep/value, '{property_value}'))
GET /me/mailFolders/{id}/messages?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and contains(ep/value, '{property_value}'))

GET /me/messages?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and startswith(ep/value, '{property_value}'))
GET /users/{id|userPrincipalName}/messages?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and startswith(ep/value, '{property_value}'))
GET /me/mailFolders/{id}/messages?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and startswith(ep/value, '{property_value}'))

GET /me/messages?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and ep/value eq '{property_value}')
GET /users/{id|userPrincipalName}/messages?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and ep/value eq '{property_value}')
GET /me/mailFolders/{id}/messages?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and ep/value eq '{property_value}')

GET /me/messages?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and ep/value ne '{property_value}')
GET /users/{id|userPrincipalName}/messages?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and ep/value ne '{property_value}')
GET /me/mailFolders/{id}/messages?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and ep/value ne '{property_value}')
```

Obtener instancias de **event**: <!-- { "blockType": "ignored" } -->
```http
GET /me/events?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and contains(ep/value, '{property_value}'))
GET /users/{id|userPrincipalName}/events?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and contains(ep/value, '{property_value}'))

GET /me/events?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and startswith(ep/value, '{property_value}'))
GET /users/{id|userPrincipalName}/events?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and startswith(ep/value, '{property_value}'))

GET /me/events?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and ep/value eq '{property_value}')
GET /users/{id|userPrincipalName}/events?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and ep/value eq '{property_value}')

GET /me/events?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and ep/value ne '{property_value}')
GET /users/{id|userPrincipalName}/events?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and ep/value ne '{property_value}')
```

Obtener instancias de **event** de grupo: <!-- { "blockType": "ignored" } -->
```http
GET /groups/{id}/events?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and contains(ep/value, '{property_value}'))
GET /groups/{id}/events?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and startswith(ep/value, '{property_value}'))
GET /groups/{id}/events?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and ep/value eq '{property_value}')
GET /groups/{id}/events?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and ep/value ne '{property_value}')
```

## <a name="parameters"></a>Parámetros
|Parámetro|Tipo|Descripción|
|:-----|:-----|:-----|
|id_value|Cadena|El identificador de la propiedad extendida que debe coincidir. Debe tener uno de los formatos compatibles. Consulte la [Información general de las propiedades extendidas de Outlook](../resources/extended-properties-overview.md) para obtener más información. Necesario.|
|property_value |Cadena|El valor de la propiedad extendida que debe coincidir. Es necesario donde aparece en la sección anterior **Solicitud HTTP**. Si {property_value} no es una cadena, asegúrese de convertir explícitamente `ep/value` en el tipo de datos Edm apropiado cuando se compare con {property_value}. Vea la [solicitud 4](#request-4) a continuación para obtener ejemplos. |

## <a name="request-headers"></a>Encabezados de solicitud
| Nombre      |Descripción|
|:----------|:----------|
| Authorization  | {token} de portador. Obligatorio. |

## <a name="request-body"></a>Cuerpo de la solicitud
No proporcione un cuerpo de solicitud para este método.

## <a name="response"></a>Respuesta

Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK`.

#### <a name="get-resource-instance-expanded-with-a-matching-extended-property"></a>Expandir una instancia de recurso con una propiedad extendida coincidente
El cuerpo de la respuesta incluye un objeto que representa la instancia de recurso solicitada y expandida con el objeto coincidente [singleValueLegacyExtendedProperty](../resources/singlevaluelegacyextendedproperty.md).
  
#### <a name="get-resource-instances-that-contain-an-extended-property-matching-a-filter"></a>Obtener instancias de recurso que contienen una propiedad extendida que coincide con un filtro
El cuerpo de la respuesta incluye uno o varios objetos que representan las instancias de recurso que contienen una propiedad extendida coincidente. El cuerpo de la respuesta no incluye la propiedad extendida.

## <a name="example"></a>Ejemplo
#### <a name="request-1"></a>Solicitud 1

El primer ejemplo obtiene y expande el mensaje especificado al incluir una propiedad extendida de valor único. El filtro devuelve la propiedad extendida cuyo **identificador** coincide con la cadena `String {66f5a359-4659-4830-9070-00047ec6ac6e} Name Color` (la codificación de dirección URL se ha eliminado aquí para facilitar la lectura).

<!-- {
  "blockType": "request",
  "sampleKeys": ["AAMkAGE1M2_bs88AACHsLqWAAA="],
  "name": "get_singlevaluelegacyextendedproperty_1"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/messages/AAMkAGE1M2_bs88AACHsLqWAAA=?$expand=singleValueExtendedProperties($filter=id%20eq%20'String%20{66f5a359-4659-4830-9070-00047ec6ac6e}%20Name%20Color')
```
#### <a name="response-1"></a>Respuesta 1
El cuerpo de la respuesta incluye todas las propiedades del mensaje especificado y devuelve la propiedad extendida del filtro.

Nota: El objeto del **mensaje** que aparece aquí está truncado para abreviar. Se devolverán todas las propiedades de una llamada real.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.message"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "@odata.context": "https://graph.microsoft.com/v1.0/$metadata#Me/messages/$entity",
    "@odata.id": "https://graph.microsoft.com/v1.0/users('ddfcd489-628b-40d7-b48b-57002df800e5@1717622f-1d94-4d0c-9d74-709fad664b77')/messages('AAMkAGE1M2_bs88AACHsLqWAAA=')",
    "@odata.etag": "W/\"CQAAABYAAACY4MQpaFz9SbqUDe4+bs88AACbyS4H\"",
    "id": "AAMkAGE1M2_bs88AACHsLqWAAA=",
    "subject": "RE: Talk about emergency prep",
    "sender": {
        "emailAddress": {
            "name": "Christine Irwin",
            "address": "christine@contoso.com"
        }
    },
    "from": null,
    "toRecipients": [
        {
            "emailAddress": {
                "name": "Christine Irwin",
                "address": "christine@contoso.com"
            }
        }
    ],
    "singleValueExtendedProperties@odata.context": "https://graph.microsoft.com/v1.0/$metadata#Me/messages('AAMkAGE1M2_bs88AACHsLqWAAA%3D')/singleValueExtendedProperties",
    "singleValueExtendedProperties": [
        {
            "id": "String {66f5a359-4659-4830-9070-00047ec6ac6e} Name Color",
            "value": "Green"
        }
    ]
}
```

#### <a name="request-2"></a>Solicitud 2

En el segundo ejemplo, se obtienen mensajes con la propiedad extendida de valor único de tipo cadena especificada en el filtro. El filtro busca una propiedad extendida que tenga lo siguiente:

- Un **id.** igual a la cadena `String {66f5a359-4659-4830-9070-00047ec6ac6e} Name Color` (con la codificación de direcciones URL quitada aquí para facilitar la lectura).

- Un **valor** igual a la cadena `Green`.

<!-- { "blockType": "ignored" } -->
```http
GET https://graph.microsoft.com/v1.0/me/messages?$filter=singleValueExtendedProperties%2FAny(ep%3A%20ep%2Fid%20eq%20'String%20{66f5a359-4659-4830-9070-00047ec6ac6e}%20Name%20Color'%20and%20ep%2Fvalue%20eq%20'Green')
```

#### <a name="response-2"></a>Respuesta 2

Un código de respuesta `HTTP 200 OK` indica una respuesta correcta y el cuerpo de la respuesta incluye todas las propiedades de los mensajes cuya propiedad extendida coincide con el filtro. El cuerpo de la respuesta es similar a la respuesta al [obtener una colección de mensajes](../api/user_list_messages.md). El cuerpo de la respuesta no incluye la propiedad extendida coincidente.


#### <a name="request-3"></a>Solicitud 3

En el tercer ejemplo, se obtienen mensajes con la propiedad extendida de valor único de tipo cadena especificada en el filtro. El filtro busca una propiedad extendida que tenga lo siguiente:

- Un **id.** igual a la cadena `String {66f5a359-4659-4830-9070-00047ec6ac6e} Name Color` (con la codificación de direcciones URL quitada aquí para facilitar la lectura).

- Su **valor** que contiene la cadena `green`. 

<!-- { "blockType": "ignored" } -->
```http
GET https://graph.microsoft.com/v1.0/Me/messages?$filter=singleValueExtendedProperties/any(ep:ep/Id eq 'String {66f5a359-4659-4830-9070-00047ec6ac6e} Name Color' and contains(ep/Value, 'green'))
```

#### <a name="response-3"></a>Respuesta 3

Un código de respuesta `HTTP 200 OK` indica una respuesta correcta y el cuerpo de la respuesta incluye todas las propiedades de los mensajes cuya propiedad extendida coincide con el filtro. Por ejemplo, un mensaje que tiene una propiedad extendida de valor único con el **id** igual a la cadena `String {66f5a359-4659-4830-9070-00047ec6ac6e} Name Color` y el **valor** `Light green`, debería coincidir con el filtro y se incluye en la respuesta.

El cuerpo de la respuesta es similar a la respuesta de la [obtención de una colección de mensajes](../api/user_list_messages.md). El cuerpo de la respuesta no incluye la propiedad extendida coincidente.


#### <a name="request-4"></a>Solicitud 4

En los siguientes dos ejemplos, se muestra cómo obtener mensajes que tengan propiedades extendidas de valor único que no sean de tipo cadena. Para facilitar la lectura, no incluyen la codificación de direcciones URL necesaria.

En el siguiente ejemplo, se muestra un filtro que busca una propiedad extendida que tenga lo siguiente:

- Un **id.** coincidente con la cadena `CLSID {00062008-0000-0000-C000-000000000046} Name ConnectorSenderGuid`.

- El GUID `b9cf8971-7d55-4b73-9ffa-a584611b600b` como **valor**. Para comparar el valor de propiedad con un GUID, convierta `ep/value` en `Edm.Guid`.


<!-- { "blockType": "ignored" } -->
```http
GET https://graph.microsoft.com/v1.0/me/messages?$filter=singleValueExtendedProperties/any(ep:ep/id eq 'CLSID {00062008-0000-0000-C000-000000000046} Name ConnectorSenderGuid' and cast(ep/value, Edm.Guid) eq (b9cf8971-7d55-4b73-9ffa-a584611b600b))
```

En el siguiente ejemplo, se muestra un filtro que busca una propiedad extendida que tenga lo siguiente:

- Un **id.** coincidente con la cadena `Integer {66f5a359-4659-4830-9070-00047ec6ac6e} Name Pallete`.

- Un **valor** igual que el número entero 12. Para comparar el valor de propiedad con un número entero, convierta `ep/value` en `Edm.Int32`.


<!-- { "blockType": "ignored" } -->
```http
GET https://graph.microsoft.com/v1.0/me/messages?$filter=singleValueExtendedProperties/any(ep:ep/id eq 'Integer {66f5a359-4659-4830-9070-00047ec6ac6e} Name Pallete' and cast(ep/value, Edm.Int32) eq 12)
```


#### <a name="response-4"></a>Respuesta 4

Para cada uno de los dos ejemplos anteriores, un código de respuesta `HTTP 200 OK` indica una respuesta correcta y el cuerpo de la respuesta incluye todas las propiedades de los mensajes cuya propiedad extendida coincide con el filtro correspondiente. El cuerpo de la respuesta es similar a la respuesta de la [obtención de una colección de mensajes](../api/user_list_messages.md). El cuerpo de la respuesta no incluye la propiedad extendida coincidente.

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get singleValueLegacyExtendedProperty",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->