# <a name="create-open-extension"></a>Crear extensión abierta

Cree una extensión abierta (objeto [openTypeExtension](../resources/openTypeExtension.md)) y agregue propiedades personalizadas en una instancia nueva o existente de un recurso. 

## <a name="prerequisites"></a>Requisitos previos

Según el recurso en el que se cree la extensión, se requiere uno de los siguientes **permisos** para ejecutar esta API:

|**Recurso admitido**|**Permiso**|**Recurso admitido**|**Permiso** |
|:-----|:-----|:-----|:-----|
| [device](../resources/device.md) | _Device.ReadWrite.All_ | [event](../resources/event.md) | _Calendars.ReadWrite_ |
| [group](../resources/group.md) | _Group.ReadWrite.All_ | [group event](../resources/event.md) | _Group.ReadWrite.All_ |
| [group post](../resources/post.md) | _Group.ReadWrite.All_ | [mensaje](../resources/message.md) | _Mail.ReadWrite_ |
| [organization](../resources/organization.md) | _Directory.AccessAsUser.All_ | [personal contact](../resources/contact.md) | _Contacts.ReadWrite_ |
| [user](../resources/user.md) | _Directory.AccessAsUser.All_ | | |


 
## <a name="http-request"></a>Solicitud HTTP

### <a name="create-an-extension-in-a-new-resource-instance"></a>Crear una extensión en una instancia de recurso nueva

Utilice la misma solicitud REST que al crear la instancia. 

<!-- { "blockType": "ignored" } -->
```http
POST /users/{id|userPrincipalName}/events
POST /users/{id|userPrincipalName}/messages
POST /groups/{id}/events
POST /groups/{id}/threads/{id}/posts/{id}/reply
POST /users/{id|userPrincipalName}/contacts
```

>**Nota:** La sintaxis anterior muestra algunas maneras comunes para crear las instancias de recursos admitidos. Todas las otras formas de sintaxis POST que le permiten crear estas instancias de recursos admiten la creación de extensiones abiertas en ellas de una manera similar.

Consulte la sección [Cuerpo de la solicitud](#request-body) para obtener información sobre cómo incluir las propiedades de la nueva instancia de recurso _y la extensión_ en el cuerpo de la solicitud.

### <a name="create-an-extension-in-an-existing-resource-instance"></a>Crear una extensión en una instancia de recurso existente

Identifique la instancia del recurso en la solicitud y haga una `POST` a la propiedad de navegación de **extensiones**.

<!-- { "blockType": "ignored" } -->
```http
POST /devices/{id}/extensions
POST /users/{id|userPrincipalName}/events/{id}/extensions
POST /groups/{id}/extensions
POST /groups/{id}/events/{id}/extensions
POST /groups/{id}/threads/{id}/posts/{id}/extensions
POST /users/{id|userPrincipalName}/messages/{id}/extensions
POST /organization/{id}/extensions
POST /users/{id|userPrincipalName}/contacts/{id}/extensions
POST /users/{id|userPrincipalName}/extensions
```

>**Nota:** La sintaxis anterior muestra algunas formas comunes para identificar una instancia del recurso, con el fin de crear una extensión en él. Todas las otras formas de sintaxis que le permiten identificar estas instancias de recursos admiten la creación de extensiones abiertas en ellas de una manera similar.

Consulte la sección [Cuerpo de la solicitud](#request-body) para obtener información sobre cómo incluir _la extensión_ en el cuerpo de la solicitud.

## <a name="parameters"></a>Parámetros
|**Parámetro**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|_Parámetros de dirección URL_|
|id|string|Un identificador único para un objeto en la colección correspondiente. Necesario.|


## <a name="request-headers"></a>Encabezados de solicitud
| Nombre       | Valor |
|:---------------|:----------|
| Authorization | {token} de portador. Obligatorio. |
| Content-Type | application/json |

## <a name="request-body"></a>Cuerpo de la solicitud

Proporcione un cuerpo JSON de [openTypeExtension](../resources/openTypeExtension.md) con los siguientes pares de nombre y valor necesarios y con cualquier dato personalizado adicional. Los datos de la carga JSON pueden ser de tipo primitivo o matrices de tipo primitivo.

| Nombre       | Valor |
|:---------------|:----------|
| @odata.type | Microsoft.Graph.OpenTypeExtension |
| extensionName | %unique_string% |

Al crear una extensión en una instancia de recurso _nueva_, además del nuevo objeto **openTypeExtension**, proporcione una representación JSON de las propiedades relevantes para crear esa instancia de recurso.

## <a name="response"></a>Respuesta

#### <a name="response-code"></a>Código de respuesta
Dependiendo de la operación, el código de respuesta puede ser `201 Created` o `202 Accepted`.

Al crear una extensión en la misma operación en la que se crea una instancia de recurso, una operación con éxito devuelve el mismo código de respuesta que cuando la operación se utiliza para crear la instancia de recurso sin la extensión. Consulte los temas correspondientes para crear la instancia, como se muestra [arriba](#create-an-extension-in-a-new-resource-instance).

#### <a name="response-body"></a>Cuerpo de la respuesta
| Escenario       | Recurso  | Cuerpo de la respuesta |
|:---------------|:----------|:--------------|
| Crear una extensión al crear explícitamente una _nueva_ instancia de recursos | [contacto](../resources/contact.md), [evento](../resources/event.md), [mensaje](../resources/message.md) | Incluye la nueva instancia ampliada con el objeto [openTypeExtension](../resources/openTypeExtension.md). |
| Crear una extensión al crear implícitamente una instancia de recursos | [post](../resources/post.md) | La respuesta incluye sólo un código de respuesta, pero no un cuerpo de respuesta. |
| Crear una extensión en una instancia de recurso _existente_ | Todos los recursos admitidos | Incluye el objeto **openTypeExtension**. |
 


## <a name="example"></a>Ejemplo
##### <a name="request-1"></a>Solicitud 1

El primer ejemplo crea un mensaje y una extensión en la misma llamada. El cuerpo de la solicitud incluye:

- Las propiedades **subject**, **body** y **toRecipients** típicas de un nuevo mensaje. 
- Y en cuanto a la extensión:

  - El tipo `Microsoft.Graph.OpenTypeExtension`. 
  - El nombre de la extensión "Com.Contoso.Referral". 
  - Los datos adicionales se almacenan como 3 propiedades personalizadas en la carga JSON: `companyName`, `expirationDate` y `dealValue`.  

<!-- {
  "blockType": "request",
  "name": "post_opentypeextension_1"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/messages

{
  "subject": "Annual review",
  "body": {
    "contentType": "HTML",
    "content": "You should be proud!"
  },
  "toRecipients": [
    {
      "emailAddress": {
        "address": "rufus@contoso.com"
      }
    }
  ],
  "extensions": [
    {
      "@odata.type": "Microsoft.Graph.OpenTypeExtension",
      "extensionName": "Com.Contoso.Referral",
      "companyName": "Wingtip Toys",
      "expirationDate": "2015-12-30T11:00:00.000Z",
      "dealValue": 10000
    }
  ]
}
```

##### <a name="response-1"></a>Respuesta 1

Aquí tiene la respuesta del primer ejemplo. El cuerpo de la respuesta incluye las propiedades del mensaje nuevo y lo siguiente para la nueva extensión:

- La propiedad **id** con el nombre completo `Microsoft.OutlookServices.OpenTypeExtension.Com.Contoso.Referral`. 
- La propiedad predeterminada **extensionName** especificada en la solicitud.
- Los datos personalizados especificados en la solicitud y almacenados como 3 propiedades personalizadas.

Nota: Puede que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Se devolverán todas las propiedades de una llamada real.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.message"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json

{
  "@odata.context": "https://graph.microsoft.com/v1.0/$metadata#Me/messages/$entity",
  "@odata.id": "https://graph.microsoft.com/v1.0/users('ddfc984d-b826-40d7-b48b-57002df800e5@1717f226-49d1-4d0c-9d74-709fad664b77')/messages
('AAMkAGEbs88AAB84uLuAAA=')",
  "@odata.etag": "W/\"CQAAABYAAACY4MQpaFz9SbqUDe4+bs88AAB88LOj\"",
  "id": "AAMkAGEbs88AAB84uLuAAA=",
  "createdDateTime": "2015-10-30T03:03:43Z",
  "lastModifiedDateTime": "2015-10-30T03:03:43Z",
  "changeKey": "CQAAABYAAACY4MQpaFz9SbqUDe4+bs88AAB88LOj",
  "categories": [ ],
  "receivedDateTime": "2015-10-30T03:03:43Z",
  "sentDateTime": "2015-10-30T03:03:43Z",
  "hasAttachments": false,
  "subject": "Annual review",
  "body": {
    "contentType": "HTML",
    "content": "<html>\r\n<head>\r\n<meta http-equiv=\"Content-Type\" content=\"text/html; charset=utf-8\">\r
\n<meta content=\"text/html; charset=us-ascii\">\r\n</head>\r\n<body>\r\nYou should be proud!\r\n</body>\r
\n</html>\r\n"
  },
  "bodyPreview": "You should be proud!",
  "importance": "Normal",
  "parentFolderId": "AQMkAGEwAAAIBDwAAAA==",
  "sender": null,
  "from": null,
  "toRecipients": [
    {
      "emailAddress": {
        "address": "rufus@contoso.com",
        "name": "John Doe"
      }
    }
  ],
  "ccRecipients": [ ],
  "bccRecipients": [ ],
  "replyTo": [ ],
  "conversationId": "AAQkAGEFGugh3SVdMzzc=",
  "isDeliveryReceiptRequested": false,
  "isReadReceiptRequested": false,
  "isRead": true,
  "isDraft": true,
  "webLink": "https://outlook.office.com/owa/?
ItemID=AAMkAGEbs88AAB84uLuAAA%3D&exvsurl=1&viewmodel=ReadMessageItem",
  "inferenceClassification": "Focused",
  "extensions@odata.context": "https://graph.microsoft.com/v1.0/$metadata#Me/messages
('AAMkAGEbs88AAB84uLuAAA%3D')/extensions",
  "extensions": [
    {
      "@odata.type": "#Microsoft.Graph.OpenTypeExtension",
      "@odata.id": "https://graph.microsoft.com/v1.0/users('ddfc984d-b826-40d7-b48b-57002df800e5@1717f226-49d1-4d0c-9d74-709fad664b77')/messages
('AAMkAGEbs88AAB84uLuAAA=')/extensions('Microsoft.OutlookServices.OpenTypeExtension.Com.Contoso.Referral')",
      "id": "Microsoft.OutlookServices.OpenTypeExtension.Com.Contoso.Referral",
      "extensionName": "Com.Contoso.Referral",
      "companyName": "Wingtip Toys",
      "expirationDate": "2015-12-30T11:00:00.000Z",
      "dealValue": 10000
    }
  ]
}
```


****

##### <a name="request-2"></a>Solicitud 2

El segundo ejemplo crea una extensión en el mensaje especificado. El cuerpo de la solicitud incluye lo siguiente para la extensión:

- El tipo `Microsoft.Graph.OpenTypeExtension`. 
- El nombre de la extensión "Com.Contoso.Referral".
- Los datos adicionales se almacenan como 3 propiedades personalizadas en la carga JSON: `companyName`, `dealValue` y `expirationDate`.  

<!-- {
  "blockType": "request",
  "name": "post_opentypeextension_2"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/messages('AAMkAGE1M2IyNGNmLTI5MTktNDUyZi1iOTVl===')/extensions

{ 
  "@odata.type" : "Microsoft.Graph.OpenTypeExtension", 
  "extensionName" : "Com.Contoso.Referral", 
  "companyName" : "Wingtip Toys", 
  "dealValue" : 500050, 
  "expirationDate" : "2015-12-03T10:00:00.000Z" 
} 
```

##### <a name="response-2"></a>Respuesta 2

Aquí tiene la respuesta del segundo ejemplo. El cuerpo de la respuesta incluye lo siguiente para la nueva extensión:

- La propiedad predeterminada **extensionName**.
- La propiedad **id** con el nombre completo `Microsoft.OutlookServices.OpenTypeExtension.Com.Contoso.Referral`. 
- Los datos personalizados que se almacenarán.  

<!-- {
  "blockType": "response",
  "truncated": false,
  "@odata.type": "microsoft.graph.opentypeextension"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json

{
    "@odata.context": "https://graph.microsoft.com/v1.0/$metadata#Me/messages('AAMkAGE1M2IyNGNmLTI5MTktNDUyZi1iOTVl===')/extensions/$entity",
    "@odata.type": "#Microsoft.Graph.OpenTypeExtension",
    "@odata.id": "https://graph.microsoft.com/v1.0/users('ddfc984d-b826-40d7-b48b-57002df85e00@1717f226-49d1-4d0c-9d74-709fad6677b4')/messages('AAMkAGE1M2IyNGNmLTI5MTktNDUyZi1iOTVl===')/extensions
('Microsoft.OutlookServices.OpenTypeExtension.Com.Contoso.Referral')",
    "extensionName": "Com.Contoso.Referral",
    "id": "Microsoft.OutlookServices.OpenTypeExtension.Com.Contoso.Referral",
    "companyName": "Wingtip Toys",
    "dealValue": 500050,
    "expirationDate": "2015-12-03T10:00:00.000Z"
}
```

****

##### <a name="request-3"></a>Solicitud 3

El tercer ejemplo crea una extensión en el evento de grupo especificado. El cuerpo de la solicitud incluye lo siguiente para la extensión:

- El tipo `Microsoft.Graph.OpenTypeExtension`. 
- El nombre de la extensión "Com.Contoso.Deal".
- Los datos adicionales se almacenan como 3 propiedades personalizadas en la carga JSON: `companyName`, `dealValue` y `expirationDate`.  

<!-- {
  "blockType": "request",
  "name": "post_opentypeextension_3"
}-->
```http
POST https://graph.microsoft.com/v1.0/groups('f5480dfd-7d77-4d0b-ba2e-3391953cc74a')/events('AAMkADVl17IsAAA=')/extensions 

{
  "@odata.type" : "Microsoft.Graph.OpenTypeExtension",
  "extensionName" : "Com.Contoso.Deal",
  "companyName" : "Alpine Skis",
  "dealValue" : 1010100,
  "expirationDate" : "2015-07-03T13:04:00.000Z"
}
```

##### <a name="response-3"></a>Respuesta 3

Aquí tiene la respuesta del tercer ejemplo de solicitud.

<!-- {
  "blockType": "response",
  "truncated": false,
  "@odata.type": "microsoft.graph.opentypeextension"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json

{
    "@odata.context": "https://graph.microsoft.com/v1.0/$metadata#groups('f5480dfd-7d77-4d0b-ba2e-3391953cc74a')/events('AAMkADVl7IsAAA%3D')/extensions/$entity",
    "@odata.type": "#Microsoft.Graph.OpenTypeExtension",
    "id": "Microsoft.OutlookServices.OpenTypeExtension.Com.Contoso.Deal",
    "extensionName": "Com.Contoso.Deal",
    "companyName": "Alpine Skis",
    "dealValue": 1010100,
    "expirationDate": "2015-07-03T13:04:00Z"
}
```

****

##### <a name="request-4"></a>Solicitud 4

El cuarto ejemplo crea una extensión en una nueva publicación de grupo mediante la misma llamada de acción de **respuesta** a una publicación de grupo existente. La acción de **respuesta** crea una nueva publicación y una nueva extensión insertada en la publicación. El cuerpo de la solicitud contiene una propiedad **post** que, a su vez, contiene el **cuerpo** de la nueva publicación y los siguientes datos de la nueva extensión:

- El tipo `Microsoft.Graph.OpenTypeExtension`. 
- El nombre de la extensión "Com.Contoso.HR".
- Los datos adicionales se almacenan como 3 propiedades personalizadas en la carga JSON: `companyName`, `expirationDate` y la matriz de cadenas `topPicks`.

<!-- {
  "blockType": "request",
  "name": "post_opentypeextension_4"
}-->
```http
POST https://graph.microsoft.com/v1.0/groups('37df2ff0-0de0-4c33-8aee-75289364aef6')/threads('AAQkADJizZJpEWwqDHsEpV_KA==')/posts('AAMkADJiUg96QZUkA-ICwMubAAC1heiSAAA=')/microsoft.graph.reply 

{
  "post": {
    "body": {
      "contentType": "html",
      "content": "<html><body><div><div><div><div>When and where? </div></div></div></div></body></html>"
    },
  "extensions": [
    {
      "@odata.type": "Microsoft.OutlookServices.OpenTypeExtension",
      "extensionName": "Com.Contoso.HR",
      "companyName": "Contoso",
      "expirationDate": "2015-07-03T13:04:00.000Z",
      "topPicks": [
        "Employees only",
        "Add spouse or guest",
        "Add family"
      ]
    }
  ]        
  }
}
```

##### <a name="response-4"></a>Respuesta 4

Aquí tiene la respuesta del cuarto ejemplo. Si se crea correctamente una extensión en una nueva publicación de grupo, el resultado es solo el código de respuesta HTTP 202.

<!-- {
  "blockType": "response",
  "truncated": true
} -->
```http
HTTP/1.1 202 Accepted
Content-type: text/plain
Content-Length: 0
```


****

##### <a name="request-5"></a>Solicitud 5

El quinto ejemplo crea una extensión en una nueva publicación de grupo mediante la misma operación POST que para crear una conversación. La operación POST crea una nueva conversación, un nuevo hilo, una nueva publicación e inserta una nueva extensión en la publicación. El cuerpo de la solicitud incluye las propiedades **Topic** y **Threads** y un objeto **post** de elemento secundario para la nueva conversación. El objeto **post** contiene a su vez el **cuerpo** de la nueva publicación y los siguientes datos de la extensión:

- El tipo `Microsoft.Graph.OpenTypeExtension`. 
- El nombre de la extensión "Com.Contoso.HR".
- Los datos adicionales se almacenan como 3 propiedades personalizadas en la carga JSON: `companyName`, `expirationDate` y la matriz de cadenas `topPicks`.

<!-- {
  "blockType": "request",
  "name": "post_opentypeextension_5"
}-->
```http
POST https://graph.microsoft.com/v1.0/groups('37df2ff0-0de0-4c33-8aee-75289364aef6')/conversations

{
  "Topic": "Does anyone have a second?",
  "Threads": [
    {
      "Posts": [
        {
          "Body": {
            "ContentType": "HTML",
            "Content": "This is urgent!"
          },
          "Extensions": [
            {
              "@odata.type": "Microsoft.OutlookServices.OpenTypeExtension",
              "extensionName": "Com.Contoso.Benefits",
              "companyName": "Contoso",
              "expirationDate": "2016-08-03T11:00:00.000Z",
              "topPicks": [
                "Employees only",
                "Add spouse or guest",
                "Add family"
              ]  
            }  
          ] 
        } 
      ]  
    } 
  ]
}
```

##### <a name="response-5"></a>Respuesta 5

Aquí está la respuesta del quinto ejemplo que contiene la nueva conversación y un identificador del hilo. Este nuevo hilo contiene una publicación creada automáticamente, que a su vez contiene la nueva extensión. 

Nota: Puede que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Se devolverán todas las propiedades de una llamada real.

Para obtener la nueva extensión, primero debe [obtener todas las publicaciones](../api/conversationthread_list_posts.md) de este hilo, inicialmente debería haber solo una. A continuación, aplique el identificador de la publicación y el nombre de la extensión `Com.Contoso.Benefits` para [obtener la extensión](../api/opentypeextension_get.md).

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.conversation"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json

{
    "@odata.context": "https://graph.microsoft.com/v1.0/$metadata#groups('37df2ff0-0de0-4c33-8aee-75289364aef6')/conversations/$entity",
    "id": "AAQkADJToRlbJ5Mg7TFM7H-j3Y=",
    "threads@odata.context": "https://graph.microsoft.com/v1.0/$metadata#groups('37df2ff0-0de0-4c33-8aee-75289364aef6')/conversations('AAQkADJToRlbJ5Mg7TFM7H-j3Y%3D')/threads",
    "threads": [
        {
            "id": "AAQkADJDtMUzsf_PdhAAswJOhGVsnkyDtMUzsf_Pdg=="
        }
    ]
}

```


<!-- This page was manually created. -->
<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create extension",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
