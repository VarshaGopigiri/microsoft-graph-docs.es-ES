---
title: Recorrido por Microsoft Graph
description: Además de utilizar la API de Microsoft Graph para leer y escribir datos, puede utilizar una serie de modelos de solicitud para realizar un recorrido entre los recursos de Microsoft Graph. El documento de metadatos también le ayuda a entender el modelo de datos de los recursos y las relaciones en Microsoft Graph.
localization_priority: Priority
ms.openlocfilehash: dc4cafc00516f4222ba6ec860dd45ff96d608dd8
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27863836"
---
# <a name="traverse-microsoft-graph"></a>Recorrido por Microsoft Graph

Además de utilizar la API de Microsoft Graph para leer y escribir datos, puede utilizar una serie de modelos de solicitud para realizar un recorrido entre los recursos de Microsoft Graph. El documento de metadatos también le ayuda a entender el modelo de datos de los recursos y las relaciones en Microsoft Graph.

## <a name="microsoft-graph-api-metadata"></a>Metadatos de la API de Microsoft Graph

El documento de metadatos ($metadata) se publica en la raíz del servicio. Puede ver el documento de servicio para las versiones v1.0 y beta de la API de Microsoft Graph a través de las siguientes URL.

**Metadatos de Microsoft Graph API v1.0**
```
    https://graph.microsoft.com/v1.0/$metadata
```

**Metadatos beta de la API de Microsoft Graph**

```
    https://graph.microsoft.com/beta/$metadata
```

Los metadatos le permiten ver y entender el modelo de datos de Microsoft Graph, incluidos los tipos de entidades, los tipos complejos y las enumeraciones que conforman los recursos que se representan en los paquetes de respuesta y solicitud.

Puede usar los metadatos para conocer las relaciones entre las entidades en Microsoft Graph y establecer las URL que navegarán entre dichas entidades.

Los nombres de recursos de la URL de la ruta de acceso, los parámetros de consulta, así como los parámetros de acción y los valores no distinguen mayúsculas de minúsculas. Sin embargo, los valores que usted asigne, los identificadores de entidad y otros valores codificados en base64 distinguen entre mayúsculas y minúsculas.

## <a name="view-a-collection-of-resources"></a>Ver una colección de recursos

Microsoft Graph permite ver recursos en un arrendatario mediante consultas HTTP GET. La respuesta a la consulta incluye las propiedades de cada recurso, con cada recurso identificado por su identificador. El formato de un identificador de recurso puede ser un GUID y por lo general varía según el tipo de recurso. 

Por ejemplo, se puede obtener la colección de usuarios definidos en un arrendatario:

```no-highlight 
GET https://graph.microsoft.com/v1.0/users HTTP/1.1
Authorization : Bearer {access_token}
```

Si es correcto, se obtendrá una respuesta 200 OK que contiene la colección de recursos del [usuario](/graph/api/resources/user?view=graph-rest-1.0) en la carga. Cada usuario está identificado por la propiedad **id** y va acompañado de sus propiedades predeterminadas. Para una mayor brevedad, la carga que se muestra a continuación se trunca.

```no-highlight 
HTTP/1.1 200 OK
Content-type: application/json

{
  "@odata.context":"https://graph.microsoft.com/v1.0/$metadata#users",
  "value":[
    {
      "id":"f71f1f74-bf1f-4e6b-b266-c777ea76e2c7",
      "businessPhones":[

      ],
      "displayName":"CIE Administrator",
      "givenName":"CIE",
      "jobTitle":null,
      "mail":"admin@contoso.onmicrosoft.com",
      "mobilePhone":"+1 3528700812",
      "officeLocation":null,
      "preferredLanguage":"en-US",
      "surname":"Administrator",
      "userPrincipalName":"admin@contoso.onmicrosoft.com"
    },
    {
      "id":"d66f2902-9d12-4ff8-ab01-21ec6706079f",
      "businessPhones":[

      ],
      "displayName":"Alan Steiner",
      "givenName":"Alan",
      "jobTitle":"VP Corporate Marketing",
      "mail":"alans@contoso.onmicrosoft.com",
      "mobilePhone":null,
      "officeLocation":null,
      "preferredLanguage":"en-US",
      "surname":"Steiner",
      "userPrincipalName":"alans@contoso.onmicrosoft.com"
    }
  ]
}
```

Microsoft Graph también permite ver las colecciones mediante la exploración de las relaciones entre recursos. Por ejemplo, a través de la propiedad de navegación **mailFolders** de un usuario, se puede realizar una consulta en la colección de recursos [mailFolder](/graph/api/resources/mailfolder?view=graph-rest-1.0) del buzón de correo del usuario:

```no-highlight 
GET https://graph.microsoft.com/v1.0/me/mailfolders HTTP/1.1
Authorization : Bearer {access_token}
```

Si es correcta, se obtendrá una respuesta 200 OK que contiene la colección de recursos de [mailFolder](/graph/api/resources/user?view=graph-rest-1.0) en la carga. Cada **mailFolder** está identificada por la propiedad **id** y va acompañada de sus propiedades predeterminadas. Para una mayor brevedad, la carga que se muestra a continuación se trunca.

```no-highlight 
HTTP/1.1 200 OK
Content-type: application/json

{
  "@odata.context":"https://graph.microsoft.com/v1.0/$metadata#users('16f5a7b6-5a15-4568-aa5a-31bb117e9967')/mailFolders",
  "value":[
    {
      "id":"AAMkADRm9AABDGisXAAA=",
      "displayName":"Archive",
      "parentFolderId":"AQMkADRmZWj0AAAIBCAAAAA==",
      "childFolderCount":0,
      "unreadItemCount":0,
      "totalItemCount":0
    },
    {
      "id":"AQMkADRm0AAAIBXAAAAA==",
      "displayName":"Sales reports",
      "parentFolderId":"AQMkADRmZWj0AAAIBCAAAAA==",
      "childFolderCount":0,
      "unreadItemCount":0,
      "totalItemCount":0
    },
    {
      "id":"AAMkADRCxI9AAAT6CAIAAA=",
      "displayName":"Conversation History",
      "parentFolderId":"AQMkADRmZWj0AAAIBCAAAAA==",
      "childFolderCount":1,
      "unreadItemCount":0,
      "totalItemCount":0
    }
  ]
}
```




## <a name="view-a-specific-resource-from-a-collection-by-id"></a>Ver un recurso específico de una colección por id.

Continuando con el ejemplo de **user**, si se quiere ver la información sobre un usuario, se utiliza una solicitud HTTPS GET para obtener un usuario específico por id. de usuario. Para una entidad **user**, el identificador puede ser la propiedad **id** o la propiedad **userPrincipalName**. En la solicitud de ejemplo siguiente se usa el valor **userPrincipalName** como identificador del usuario. 

```no-highlight 
GET https://graph.microsoft.com/v1.0/users/john.doe@contoso.onmicrosoft.com HTTP/1.1
Authorization : Bearer {access_token}
```

Si es correcto, se obtendrá una respuesta 200 OK que contiene la representación de recursos del usuario en la carga, como se muestra.

```no-highlight 
HTTP/1.1 200 OK
content-type: application/json;odata.metadata=minimal
content-length: 982

{
    "@odata.context": "https://graph.microsoft.com/v1.0/$metadata#users/$entity",
    "id": "c95e3b3a-c33b-48da-a6e9-eb101e8a4205",
    "city": "Redmond",
    "country": "USA",
    "department": "Help Center",
    "displayName": "John Doe",
    "givenName": "John",
    "userPrincipalName": "john.doe@contoso.onmicrosoft.com",

    ... 
}
```

## <a name="read-specific-properties-of-a-resource"></a>Lea las propiedades específicas de un recurso
Para recuperar tan solo los datos biográficos del usuario, como la descripción de _Acerca de mí_ que proporcionó y su conjunto de aptitudes, puede agregar el parámetro de consulta [$select](query-parameters.md) a la solicitud anterior, como se muestra en el ejemplo siguiente: 

```no-highlight 
GET https://graph.microsoft.com/v1.0/users/john.doe@contoso.onmicrosoft.com?$select=displayName,aboutMe,skills HTTP/1.1
Authorization : Bearer {access_token}
```

La respuesta correcta devuelve el estado 200 OK y una carga en el formato siguiente, como se muestra.

```no-highlight 
HTTP/1.1 200 OK
content-type: application/json;odata.metadata=minimal
content-length: 169

{
    "@odata.context": "https://graph.microsoft.com/v1.0/$metadata#users/$entity",
    "aboutMe": "A cool and nice guy.",
    "displayName": "John Doe",
    "skills": [
        "n-Lingual",
        "public speaking",
        "doodling"
    ]
}
```
Aquí, en lugar de todos los conjuntos de propiedades de la entidad **user**, solo se devuelven las propiedades básicas **aboutMe**, **displayName** y **skills**.

## <a name="read-specific-properties-of-the-resources-in-a-collection"></a>Leer las propiedades específicas de los recursos de una colección
Además de leer las propiedades específicas de un único recurso, también puede aplicar el parámetro de consulta similar [$select](query-parameters.md) a una colección para obtener de nuevo todos los recursos en la colección con tan solo las propiedades específicas en cada uno. Por ejemplo, para consultar el nombre de los elementos de la unidad del usuario que ha iniciado sesión, se puede enviar la siguiente solicitud HTTPS GET:

```no-highlight 
GET https://graph.microsoft.com/v1.0/me/drive/root/children?$select=name HTTP/1.1
Authorization : Bearer {access_token}
```

La respuesta correcta devuelve un código de estado 200 OK y una carga que contiene solamente los nombres y los tipos de los archivos compartidos, tal como se muestra en el ejemplo siguiente:

```no-highlight 
{
  "@odata.context": "https://graph.microsoft.com/v1.0/$metadata#users('john.doe%40contoso.onmicrosoft.com')/drive/root/children(name,type)",
  "value": [
    {
      "@odata.etag": "\"{896A8E4D-27BF-424B-A0DA-F073AE6570E2},2\"",
      "name": "Shared with Everyone"
    },
    {
      "@odata.etag": "\"{B39D5D2E-E968-491A-B0EB-D5D0431CB423},1\"",
      "name": "Documents"
    },
    {
      "@odata.etag": "\"{9B51EA38-3EE6-4DC1-96A6-230E325EF054},2\"",
      "name": "newFile.txt"
    }
  ]
}
```

## <a name="traverse-from-one-resource-to-another-via-relationship"></a>Recorrido desde un recurso a otro a través de la relación
Un administrador mantiene una relación **directReports** con el resto de los usuarios a su cargo. Para consultar la lista de relaciones directas de un usuario, se puede usar la siguiente solicitud HTTPS GET para navegar hasta el destino deseado mediante un recorrido de relaciones. 

```no-highlight 
GET https://graph.microsoft.com/v1.0/users/john.doe@contoso.onmicrosoft.com/directReports HTTP/1.1
Authorization : Bearer {access_token}
```

La respuesta correcta devuelve el estado 200 OK y una carga, como se muestra.

```no-highlight 
HTTP/1.1 200 OK
content-type: application/json;odata.metadata=minimal
content-length: 152
    
{
    "@odata.context": "https://graph.microsoft.com/v1.0/$metadata#directoryObjects/$entity",
    "@odata.type": "#microsoft.graph.user",
    "id": "c37b074d-fe9d-4e68-83ad-b4401d3be174",
    "department": "Sales & Marketing",
    "displayName": "Bonnie Kearney",

    ...
}
```

De forma similar, se puede seguir una relación para ir a los recursos relacionados. Por ejemplo, la relación usuario-mensajes permite un recorrido desde un usuario de Azure Active Directory (Azure AD) hasta un conjunto de mensajes de correo de Outlook. En el ejemplo siguiente se muestra cómo realizar esta acción en una llamada de la API de REST:


```no-highlight 
GET https://graph.microsoft.com/v1.0/me/messages HTTP/1.1
Authorization : Bearer {access_token}
```

    
La respuesta correcta devuelve el estado 200 OK y una carga en el formato siguiente, como se muestra.


```no-highlight 
HTTP/1.1 200 OK
content-type: application/json;odata.metadata=minimal
odata-version: 4.0
content-length: 147
    
{
  "@odata.context": "https://graph.microsoft.com/v1.0/$metadata#users('john.doe%40contoso.onmicrosoft.com')/Messages",
  "@odata.nextLink": "https://graph.microsoft.com/v1.0/me/messages?$top=1&$skip=1",
  "value": [
    {
      "@odata.etag": "W/\"FwAAABYAAABMR67yw0CmT4x0kVgQUH/3AAJL+Kej\"",
      "id": "<id-value>",
      "createdDateTime": "2015-11-14T00:24:42Z",
      "lastModifiedDateTime": "2015-11-14T00:24:42Z",
      "changeKey": "FwAAABYAAABMR67yw0CmT4x0kVgQUH/3AAJL+Kej",
      "categories": [],
      "receivedDateTime": "2015-11-14T00:24:42Z",
      "sentDateTime": "2015-11-14T00:24:28Z",
      "hasAttachments": false,
      "subject": "Did you see last night's game?",
      "body": {
        "ContentType": "HTML",
        "Content": "<content>"
      },
      "BodyPreview": "it was great!",
      "Importance": "Normal",
            
       ...
    }
  ]
}
```
Puede ver todas las relaciones de un recurso determinado en los metadatos, buscar el EntityType y buscar en todas las NavigationProperties para la EntityType.

## <a name="call-functions"></a>Funciones de llamada
Microsoft Graph también es compatible con _funciones_ para manipular los recursos de maneras que no consisten simplemente en crear, leer, actualizar y eliminar operaciones (CRUD). Suele ser en forma de solicitudes HTTPS POST para captar los argumentos de entrada para la función. Por ejemplo, la siguiente función permite al usuario que ha iniciado sesión (`me`) enviar un mensaje de correo electrónico.

```no-highlight 
POST https://graph.microsoft.com/v1.0/me/sendMail HTTP/1.1
authorization: bearer {access_token}
content-type: application/json
content-length: 96

{
  "message": {
    "subject": "Meet for lunch?",
    "body": {
      "contentType": "Text",
      "content": "The new cafeteria is open."
    },
    "toRecipients": [
      {
        "emailAddress": {
          "address": "garthf@a830edad9050849NDA1.onmicrosoft.com"
        }
      }
    ],
    "attachments": [
      {
        "@odata.type": "microsoft.graph.fileAttachment",
        "name": "menu.txt",
        "contentBytes": "bWFjIGFuZCBjaGVlc2UgdG9kYXk="
      }
    ]
  },
  "saveToSentItems": "false"
}
```

Puede ver todas las funciones que están disponibles en los metadatos. Aparecen como funciones o acciones.

## <a name="use-the-microsoft-graph-sdks"></a>Utilizar los SDK de Microsoft Graph

¿Le gustan la potencia y la facilidad de los SDK? Aunque siempre puede utilizar la API de REST para llamar a Microsoft Graph, hemos proporcionado SDK para muchas plataformas populares. Para explorar las SDK que están disponibles, consulte [Ejemplos de código y SDK](https://developer.microsoft.com/graph/code-samples-and-sdks).

## <a name="see-also"></a>Recursos adicionales

- [Usar la API de Microsoft Graph](use-the-api.md)
- [Obtener tokens de autenticación](auth-overview.md)
