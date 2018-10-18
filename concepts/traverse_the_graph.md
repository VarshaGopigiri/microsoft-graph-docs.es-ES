# <a name="traverse-microsoft-graph"></a><span data-ttu-id="fc066-101">Recorrido por Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="fc066-101">Traverse Microsoft Graph</span></span>

<span data-ttu-id="fc066-p101">Además de utilizar la API de Microsoft Graph para leer y escribir datos, puede utilizar una serie de modelos de solicitud para realizar un recorrido entre los recursos de Microsoft Graph. El documento de metadatos también le ayuda a entender el modelo de datos de los recursos y las relaciones en Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="fc066-p101">In addition to using the Microsoft Graph API to read and write data, you can use a number of request patterns to traverse through the resources in Microsoft Graph. The metadata document also helps you to understand the data model of the resources and relationships in Microsoft Graph.</span></span>

## <a name="microsoft-graph-api-metadata"></a><span data-ttu-id="fc066-104">Metadatos de la API de Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="fc066-104">Microsoft Graph API metadata</span></span>

<span data-ttu-id="fc066-p102">El documento de metadatos ($metadata) se publica en la raíz del servicio. Puede ver el documento de servicio para las versiones v1.0 y beta de la API de Microsoft Graph a través de las siguientes URL.</span><span class="sxs-lookup"><span data-stu-id="fc066-p102">The metadata document ($metadata) is published at the service root. You can view the service document for the v1.0 and beta versions of the Microsoft Graph API via the following URLs.</span></span>

<span data-ttu-id="fc066-107">**Metadatos de Microsoft Graph API v1.0**</span><span class="sxs-lookup"><span data-stu-id="fc066-107">**Microsoft Graph API v1.0 metadata**</span></span>
```
    https://graph.microsoft.com/v1.0/$metadata
```

<span data-ttu-id="fc066-108">**Metadatos beta de la API de Microsoft Graph**</span><span class="sxs-lookup"><span data-stu-id="fc066-108">**Microsoft Graph API beta metadata**</span></span>

```
    https://graph.microsoft.com/beta/$metadata
```

<span data-ttu-id="fc066-109">Los metadatos le permiten ver y entender el modelo de datos de Microsoft Graph, incluidos los tipos de entidades, los tipos complejos y las enumeraciones que conforman los recursos que se representan en los paquetes de respuesta y solicitud.</span><span class="sxs-lookup"><span data-stu-id="fc066-109">The metadata allows you to see and understand the Microsoft Graph data model, including the entity types, complex types, and enumerations that make up the resources represented in the request and response packets.</span></span>

<span data-ttu-id="fc066-110">Puede usar los metadatos para conocer las relaciones entre las entidades en Microsoft Graph y establecer las URL que navegarán entre dichas entidades.</span><span class="sxs-lookup"><span data-stu-id="fc066-110">You can use the metadata to learn the realtionships between entities in Microsoft Graph and establish URLs that navigate between those entities.</span></span>

<span data-ttu-id="fc066-p103">Los nombres de recursos de la URL de la ruta de acceso, los parámetros de consulta, así como los parámetros de acción y los valores no distinguen mayúsculas de minúsculas. Sin embargo, los valores que usted asigne, los identificadores de entidad y otros valores codificados en base64 distinguen entre mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="fc066-p103">Path URL resource names, query parameters, and action parameters and values are not case-sensitive. However, values you assign, entity IDs, and other base-64-encoded values are case-sensitive.</span></span>

## <a name="view-a-collection-of-resources"></a><span data-ttu-id="fc066-113">Ver una colección de recursos</span><span class="sxs-lookup"><span data-stu-id="fc066-113">View a collection of resources</span></span>

<span data-ttu-id="fc066-p104">Microsoft Graph permite ver recursos en un arrendatario mediante consultas HTTP GET. La respuesta a la consulta incluye las propiedades de cada recurso, con cada recurso identificado por su identificador. El formato de un identificador de recurso puede ser un GUID y por lo general varía según el tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="fc066-p104">Microsoft Graph lets you view resources in a tenant using HTTP GET queries. The query response includes properties of each resource, with each resource identified by its ID. The format of a resource ID can be a GUID, and generally varies according to the resource type.</span></span> 

<span data-ttu-id="fc066-117">Por ejemplo, se puede obtener la colección de usuarios definidos en un arrendatario:</span><span class="sxs-lookup"><span data-stu-id="fc066-117">For example, you can get the collection of users defined in a tenant:</span></span>

```no-highlight 
GET https://graph.microsoft.com/v1.0/users HTTP/1.1
Authorization : Bearer {access_token}
```

<span data-ttu-id="fc066-p105">Si es correcto, se obtendrá una respuesta 200 OK que contiene la colección de recursos del [usuario](../api-reference/v1.0/resources/user.md) en la carga. Cada usuario está identificado por la propiedad **id** y va acompañado de sus propiedades predeterminadas. Para una mayor brevedad, la carga que se muestra a continuación se trunca.</span><span class="sxs-lookup"><span data-stu-id="fc066-p105">If successful, you'll get a 200 OK response that contains the collection of [user](../api-reference/v1.0/resources/user.md) resources in the payload. Each user is identified by the **id** property and accompanied by its default properties. The payload shown below is truncated for brevity.</span></span>

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

<span data-ttu-id="fc066-p106">Microsoft Graph también permite ver las colecciones mediante la exploración de las relaciones entre recursos. Por ejemplo, a través de la propiedad de navegación **mailFolders** de un usuario, se puede realizar una consulta en la colección de recursos [mailFolder](../api-reference/v1.0/resources/mailfolder.md) del buzón de correo del usuario:</span><span class="sxs-lookup"><span data-stu-id="fc066-p106">Microsoft Graph also lets you view collections by navigating the relationships of one resource with another. For example, through a user's **mailFolders** navigation property, you can query for the collection of [mailFolder](../api-reference/v1.0/resources/mailfolder.md) resources in the user's mailbox:</span></span>

```no-highlight 
GET https://graph.microsoft.com/v1.0/me/mailfolders HTTP/1.1
Authorization : Bearer {access_token}
```

<span data-ttu-id="fc066-p107">Si es correcta, se obtendrá una respuesta 200 OK que contiene la colección de recursos de [mailFolder](../api-reference/v1.0/resources/user.md) en la carga. Cada **mailFolder** está identificada por la propiedad **id** y va acompañada de sus propiedades predeterminadas. Para una mayor brevedad, la carga que se muestra a continuación se trunca.</span><span class="sxs-lookup"><span data-stu-id="fc066-p107">If successful, you'll get a 200 OK response that contains the collection of [mailFolder](../api-reference/v1.0/resources/user.md) resources in the payload. Each **mailFolder** is identified by the **id** property and accompanied by its properties. The payload shown below is truncated for brevity.</span></span>

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




## <a name="view-a-specific-resource-from-a-collection-by-id"></a><span data-ttu-id="fc066-126">Ver un recurso específico de una colección por id.</span><span class="sxs-lookup"><span data-stu-id="fc066-126">View a specific resource from a collection by ID</span></span>

<span data-ttu-id="fc066-p108">Continuando con el ejemplo de **user**, si se quiere ver la información sobre un usuario, se utiliza una solicitud HTTPS GET para obtener un usuario específico por id. de usuario. Para una entidad **user**, el identificador puede ser la propiedad **id** o la propiedad **userPrincipalName**. En la solicitud de ejemplo siguiente se usa el valor **userPrincipalName** como identificador del usuario.</span><span class="sxs-lookup"><span data-stu-id="fc066-p108">Continuing with using **user** as an example - to view the information about a user, use an HTTPS GET request to get a specific user by the user's ID. For a **user** entity, you can use either the **id** or **userPrincipalName** property as the identifier. The following request example uses the **userPrincipalName** value as the user's ID.</span></span> 

```no-highlight 
GET https://graph.microsoft.com/v1.0/users/john.doe@contoso.onmicrosoft.com HTTP/1.1
Authorization : Bearer {access_token}
```

<span data-ttu-id="fc066-130">Si es correcto, se obtendrá una respuesta 200 OK que contiene la representación de recursos del usuario en la carga, como se muestra.</span><span class="sxs-lookup"><span data-stu-id="fc066-130">If successful, you'll get a 200 OK response that contains the user resource representation in the payload, as shown.</span></span>

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

## <a name="read-specific-properties-of-a-resource"></a><span data-ttu-id="fc066-131">Lea las propiedades específicas de un recurso</span><span class="sxs-lookup"><span data-stu-id="fc066-131">Read specific properties of a resource</span></span>
<span data-ttu-id="fc066-132">Para recuperar tan solo los datos biográficos del usuario, como la descripción de _Acerca de mí_ que proporcionó y su conjunto de aptitudes, puede agregar el parámetro de consulta [$select](query_parameters.md) a la solicitud anterior, como se muestra en el ejemplo siguiente:</span><span class="sxs-lookup"><span data-stu-id="fc066-132">To retrieve only the user's biographical data, such as the user's provided _About me_ description and their skill set, you can add the [$select](query_parameters.md) query parameter to the previous request, as shown in the following example.</span></span> 

```no-highlight 
GET https://graph.microsoft.com/v1.0/users/john.doe@contoso.onmicrosoft.com?$select=displayName,aboutMe,skills HTTP/1.1
Authorization : Bearer {access_token}
```

<span data-ttu-id="fc066-133">La respuesta correcta devuelve el estado 200 OK y una carga en el formato siguiente, como se muestra.</span><span class="sxs-lookup"><span data-stu-id="fc066-133">The successful response returns the 200 OK status and a payload, as shown.</span></span>

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
<span data-ttu-id="fc066-134">Aquí, en lugar de todos los conjuntos de propiedades de la entidad **user**, solo se devuelven las propiedades básicas **aboutMe**, **displayName** y **skills**.</span><span class="sxs-lookup"><span data-stu-id="fc066-134">Here, instead of the entire property sets on the **user** entity, only the **aboutMe**, **displayName**, and **skills** basic properties are returned.</span></span>

## <a name="read-specific-properties-of-the-resources-in-a-collection"></a><span data-ttu-id="fc066-135">Leer las propiedades específicas de los recursos de una colección</span><span class="sxs-lookup"><span data-stu-id="fc066-135">Read specific properties of the resources in a collection</span></span>
<span data-ttu-id="fc066-p109">Además de leer las propiedades específicas de un único recurso, también puede aplicar el parámetro de consulta similar [$select](query_parameters.md) a una colección para obtener de nuevo todos los recursos en la colección con tan solo las propiedades específicas en cada uno. Por ejemplo, para consultar el nombre de los elementos de la unidad del usuario que ha iniciado sesión, se puede enviar la siguiente solicitud HTTPS GET:</span><span class="sxs-lookup"><span data-stu-id="fc066-p109">In addition to reading specific properties of a single resource, you can also apply the similar [$select](query_parameters.md) query parameter to a collection to get back all resources in the collection with just the specific properties returned on each. For example, to query the name of the signed-in user's drive items, you can submit the following HTTPS GET request.</span></span>

```no-highlight 
GET https://graph.microsoft.com/v1.0/me/drive/root/children?$select=name HTTP/1.1
Authorization : Bearer {access_token}
```

<span data-ttu-id="fc066-138">La respuesta correcta devuelve un código de estado 200 OK y una carga que contiene solamente los nombres y los tipos de los archivos compartidos, tal como se muestra en el ejemplo siguiente:</span><span class="sxs-lookup"><span data-stu-id="fc066-138">The successful response returns a 200 OK status code and a payload that contains only the names of the shared files, as shown in the following example.</span></span>

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

## <a name="traverse-from-one-resource-to-another-via-relationship"></a><span data-ttu-id="fc066-139">Recorrido desde un recurso a otro a través de la relación</span><span class="sxs-lookup"><span data-stu-id="fc066-139">Traverse from one resource to another via relationship</span></span>
<span data-ttu-id="fc066-p110">Un administrador mantiene una relación **directReports** con el resto de los usuarios a su cargo. Para consultar la lista de relaciones directas de un usuario, se puede usar la siguiente solicitud HTTPS GET para navegar hasta el destino deseado mediante un recorrido de relaciones.</span><span class="sxs-lookup"><span data-stu-id="fc066-p110">A manager holds a **directReports** relationship with the other users reporting to him or her. To query the list of the direct reports of a user, you can use the following HTTPS GET request to navigate to the intended target via relationship traversal.</span></span> 

```no-highlight 
GET https://graph.microsoft.com/v1.0/users/john.doe@contoso.onmicrosoft.com/directReports HTTP/1.1
Authorization : Bearer {access_token}
```

<span data-ttu-id="fc066-142">La respuesta correcta devuelve el estado 200 OK y una carga en el formato siguiente, como se muestra.</span><span class="sxs-lookup"><span data-stu-id="fc066-142">The successful response returns the 200 OK status and a payload, as shown.</span></span>

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

<span data-ttu-id="fc066-p111">De forma similar, se puede seguir una relación para ir a los recursos relacionados. Por ejemplo, la relación usuario-mensajes permite un recorrido desde un usuario de Azure Active Directory (Azure AD) hasta un conjunto de mensajes de correo de Outlook. En el ejemplo siguiente se muestra cómo realizar esta acción en una llamada de la API de REST:</span><span class="sxs-lookup"><span data-stu-id="fc066-p111">Similarly, you can follow a relationship to navigate to related resources. For example, the user-messages relationship enables traversal from an Azure Active Directory (Azure AD) User to a set of Outlook mail messages. The following example shows how to do this in a REST API call.</span></span>


```no-highlight 
GET https://graph.microsoft.com/v1.0/me/messages HTTP/1.1
Authorization : Bearer {access_token}
```

    
<span data-ttu-id="fc066-146">La respuesta correcta devuelve el estado 200 OK y una carga en el formato siguiente, como se muestra.</span><span class="sxs-lookup"><span data-stu-id="fc066-146">The successful response returns the 200 OK status and a payload, as shown.</span></span>


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
<span data-ttu-id="fc066-147">Puede ver todas las relaciones de un recurso determinado en los metadatos, buscar el EntityType y buscar en todas las NavigationProperties para la EntityType.</span><span class="sxs-lookup"><span data-stu-id="fc066-147">You can see all the relationships on a given resource by going to the metadata, finding the EntityType, and looking at all NavigationProperties for that EntityType.</span></span>

## <a name="call-functions"></a><span data-ttu-id="fc066-148">Funciones de llamada</span><span class="sxs-lookup"><span data-stu-id="fc066-148">Call functions</span></span>
<span data-ttu-id="fc066-p112">Microsoft Graph también es compatible con _funciones_ para manipular los recursos de maneras que no consisten simplemente en crear, leer, actualizar y eliminar operaciones (CRUD). Suele ser en forma de solicitudes HTTPS POST para captar los argumentos de entrada para la función. Por ejemplo, la siguiente función permite al usuario que ha iniciado sesión (`me`) enviar un mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="fc066-p112">Microsoft Graph also supports _functions_ to manipulate resources in ways that are not simply create, read, update, and delete (CRUD) operations. They are often in the shape of HTTPS POST requests in order to intake arguments for the function. For example, the following function lets the signed-in user (`me`) send an email message.</span></span>

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

<span data-ttu-id="fc066-p113">Puede ver todas las funciones que están disponibles en los metadatos. Aparecen como funciones o acciones.</span><span class="sxs-lookup"><span data-stu-id="fc066-p113">You can see all the functions that are available in the metadata. They appear as Functions or Actions.</span></span>

## <a name="use-the-microsoft-graph-sdks"></a><span data-ttu-id="fc066-154">Utilizar los SDK de Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="fc066-154">Use the Microsoft Graph SDKs</span></span>

<span data-ttu-id="fc066-p114">¿Le gustan la potencia y la facilidad de los SDK? Aunque siempre puede utilizar la API de REST para llamar a Microsoft Graph, hemos proporcionado SDK para muchas plataformas populares. Para explorar las SDK que están disponibles, consulte [Ejemplos de código y SDK](https://graph.microsoft.io/en-us/code-samples-and-sdks).</span><span class="sxs-lookup"><span data-stu-id="fc066-p114">Like the power and ease of SDKs? While you can always use REST APIs to call Microsoft Graph, we also provide SDKs for many popular platforms. To explore the SDKs that are available, see [Code samples and SDKs](https://graph.microsoft.io/en-us/code-samples-and-sdks).</span></span>

## <a name="see-also"></a><span data-ttu-id="fc066-158">Vea también</span><span class="sxs-lookup"><span data-stu-id="fc066-158">See also</span></span>

- [<span data-ttu-id="fc066-159">Usar la API de Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="fc066-159">Use the Microsoft Graph API</span></span>](use_the_api.md)
- [<span data-ttu-id="fc066-160">Obtener tokens de autenticación</span><span class="sxs-lookup"><span data-stu-id="fc066-160">Get auth tokens</span></span>](auth_overview.md)