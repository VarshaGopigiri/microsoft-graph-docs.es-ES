# <a name="calling-the-microsoft-graph-api"></a><span data-ttu-id="88099-101">Llamar a la API de Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="88099-101">Calling the Microsoft Graph API</span></span>

<span data-ttu-id="88099-102">Para tener acceso y manipular un recurso de Microsoft Graph, se debe llamar a las direcciones URL del recurso y especificarlas mediante una de las siguientes operaciones:</span><span class="sxs-lookup"><span data-stu-id="88099-102">To access and manipulate a Microsoft Graph resource, you call and specify the resource URLs using one of the following operations:</span></span>   

- <span data-ttu-id="88099-103">GET</span><span class="sxs-lookup"><span data-stu-id="88099-103">GET</span></span>
- <span data-ttu-id="88099-104">POST</span><span class="sxs-lookup"><span data-stu-id="88099-104">POST</span></span>
- <span data-ttu-id="88099-105">PATCH</span><span class="sxs-lookup"><span data-stu-id="88099-105">PATCH</span></span>
- <span data-ttu-id="88099-106">PUT</span><span class="sxs-lookup"><span data-stu-id="88099-106">PUT</span></span>
- <span data-ttu-id="88099-107">DELETE</span><span class="sxs-lookup"><span data-stu-id="88099-107">DELETE</span></span> 

<span data-ttu-id="88099-108">Todas las solicitudes de la API de Microsoft Graph usan el siguiente patrón de URL básico:</span><span class="sxs-lookup"><span data-stu-id="88099-108">All Microsoft Graph API requests use the following basic URL pattern:</span></span>

```
    https://graph.microsoft.com/{version}/{resource}?[query_parameters]
```

<span data-ttu-id="88099-109">Para esta URL:</span><span class="sxs-lookup"><span data-stu-id="88099-109">For this URL:</span></span>

- <span data-ttu-id="88099-110">`https://graph.microsoft.com` es el punto de conexión de la API de Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="88099-110">`https://graph.microsoft.com` is the Microsoft Graph API endpoint.</span></span>
- <span data-ttu-id="88099-111">`{version}` es la versión del servicio de destino; por ejemplo, `v1.0` o `beta`.</span><span class="sxs-lookup"><span data-stu-id="88099-111">`{version}` is the target service version, for example, `v1.0` or `beta`.</span></span>
- <span data-ttu-id="88099-112">`{resource}` es el segmento o la ruta de los recursos, como:</span><span class="sxs-lookup"><span data-stu-id="88099-112">`{resource}` is resource segment or path, such as:</span></span>
  - <span data-ttu-id="88099-113">`users`, `groups`, `devices`, `organization`</span><span class="sxs-lookup"><span data-stu-id="88099-113"></span></span>
  - <span data-ttu-id="88099-114">El alias `me`, que se resuelve en el usuario que inició sesión.</span><span class="sxs-lookup"><span data-stu-id="88099-114">The alias `me`, which resolves to the signed-in user</span></span>
   - <span data-ttu-id="88099-115">Los recursos que pertenecen a un usuario, tales como `me/events`, `me/drive` o `me/messages`.</span><span class="sxs-lookup"><span data-stu-id="88099-115">The resources belonging to a user, such as `me/events`, `me/drive` or `me/messages`</span></span>
  - <span data-ttu-id="88099-116">El alias `myOrganization`, que se resuelve en el espacio empresarial de la organización del usuario que haya iniciado sesión</span><span class="sxs-lookup"><span data-stu-id="88099-116">The alias `myOrganization`, which resolves to the tenant of the organization signed-in user</span></span>
- <span data-ttu-id="88099-117">`[query_parameters]` representa parámetros de consulta adicionales como `$filter` y `$select`.</span><span class="sxs-lookup"><span data-stu-id="88099-117">`[query_parameters]` represents additional query parameters such as `$filter` and `$select`.</span></span>

<span data-ttu-id="88099-p101">Opcionalmente, puede especificar también el espacio empresarial como parte de su solicitud. Si usa `me`, no especifique el espacio empresarial. Para obtener una lista de las solicitudes comunes, vea [Información general de Microsoft Graph](overview.md).</span><span class="sxs-lookup"><span data-stu-id="88099-p101">Optionally, you can also specify the tenant as part of your request. When using `me`, do not specify the tenant. For a list of common requests, see [Overview of Microsoft Graph](overview.md).</span></span>

## <a name="microsoft-graph-api-metadata"></a><span data-ttu-id="88099-121">Metadatos de la API de Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="88099-121">Microsoft Graph API metadata</span></span>
<span data-ttu-id="88099-p102">El documento de metadatos ($metadata) se publica en la raíz del servicio. Por ejemplo, puede ver el documento de servicio para las versiones v1.0 y beta a través de las siguientes URL.</span><span class="sxs-lookup"><span data-stu-id="88099-p102">The metadata document ($metadata) is published at the service root. For example, you can view the service document for the v1.0 and beta versions via the following URLs.</span></span>

<span data-ttu-id="88099-124">Metadatos `v1.0` de la API de Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="88099-124">Microsoft Graph API `v1.0` metadata.</span></span>
```
    https://graph.microsoft.com/v1.0/$metadata
```
<span data-ttu-id="88099-125">Metadatos `beta` de la API de Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="88099-125">Microsoft Graph API `beta` metadata.</span></span>
```
    https://graph.microsoft.com/beta/$metadata
```

<span data-ttu-id="88099-126">Los metadatos le permiten ver y entender el modelo de datos de Microsoft Graph, incluidos los tipos y conjuntos de entidades, los tipos complejos y las enumeraciones que conforman los paquetes de solicitud y respuesta que Microsoft Graph envía y recibe.</span><span class="sxs-lookup"><span data-stu-id="88099-126">The metadata allows you to see and understand the data model of Microsoft Graph, including the entity types and sets, complex types, and enums that make up the request and response packets sent to and from Microsoft Graph.</span></span>
<span data-ttu-id="88099-127">Puede usar los metadatos para comprender las relaciones entre las entidades en Microsoft Graph y establecer las URL que navegarán entre entidades.</span><span class="sxs-lookup"><span data-stu-id="88099-127">You can use the metadata to understand the realtionships between entities in Microsoft Graph and establish URLs that navigate between entities.</span></span>
<span data-ttu-id="88099-128">Esta interconexión basada en la navegación proporciona a Microsoft Graph una personalidad única.</span><span class="sxs-lookup"><span data-stu-id="88099-128">This navigation-based interconnectedness gives Microsoft Graph its unique character.</span></span>

<span data-ttu-id="88099-129">Los nombres de recursos de la URL de la ruta de acceso, los parámetros de consulta, así como los parámetros de acción y los valores no distinguen mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="88099-129">Path URL resource names, query parameters, and action parameters and values are case insensitive.</span></span> <span data-ttu-id="88099-130">Sin embargo, los valores que usted asigne, los identificadores de entidad y otros valores codificados en base64 distinguen entre mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="88099-130">However, values you assign, entity IDs, and other base64-encoded values are case-sensitive.</span></span>

<span data-ttu-id="88099-131">Las siguientes secciones muestran algunas llamadas de modelo de programación básico a la API de Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="88099-131">The following sections show a few basic programming pattern calls to the Microsoft Graph API.</span></span>

## <a name="navigate-from-a-set-to-a-member"></a><span data-ttu-id="88099-132">Navegación desde un conjunto a un miembro</span><span class="sxs-lookup"><span data-stu-id="88099-132">Navigate from a set to a member</span></span>

<span data-ttu-id="88099-p105">Para ver la información de un usuario, se usa una solicitud HTTPS GET con la que se obtiene la entidad `User` de la colección `users` para el usuario concreto identificado por su identificador. Para una entidad `User`, se puede usar como identificador la propiedad `id` o la propiedad `userPrincipalName`. En la solicitud de ejemplo siguiente se usa el valor `userPrincipalName` como identificador del usuario.</span><span class="sxs-lookup"><span data-stu-id="88099-p105">To view the information about a user, you get the `User` entity from the `users` collection to the specific user identified by its identifier, using an HTTPS GET request. For a `User` entity, either the `id` or `userPrincipalName` property can be used as the identifier. The following example request uses the `userPrincipalName` value as the user's id.</span></span> 

```no-highlight 
GET https://graph.microsoft.com/v1.0/users/john.doe@contoso.onmicrosoft.com HTTP/1.1
Authorization : Bearer <access_token>
```

<span data-ttu-id="88099-136">Si es correcta, se obtiene una respuesta 200 OK que contiene la representación de recursos del usuario en la carga, como se muestra a continuación:</span><span class="sxs-lookup"><span data-stu-id="88099-136">If successful, you should get a 200 OK response containing the user resource representation in the payload, as shown as follows:</span></span>

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


## <a name="project-from-an-entity-to-properties"></a><span data-ttu-id="88099-137">Proyección desde una entidad a las propiedades</span><span class="sxs-lookup"><span data-stu-id="88099-137">Project from an entity to properties</span></span>
<span data-ttu-id="88099-p106">Para recuperar tan solo los datos biográficos del usuario, como la descripción de _Acerca de mí_ que proporcionó y su conjunto de aptitudes, puede agregar el parámetro de consulta _select_ a la solicitud anterior. Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="88099-p106">To retrieve only the user's biographical data, such as the user's provided _About me_ description and their skill set, you can add the _select_ query parameter to the previous request. For example:</span></span>

```no-highlight 
GET https://graph.microsoft.com/v1.0/users/john.doe@contoso.onmicrosoft.com?$select=displayName,aboutMe,skills HTTP/1.1
Authorization : Bearer <access_token>
```

<span data-ttu-id="88099-140">La respuesta correcta devuelve el estado 200 OK y una carga en el formato siguiente:</span><span class="sxs-lookup"><span data-stu-id="88099-140">The successful response returns the 200 OK status and a payload of the following format:</span></span>

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

<span data-ttu-id="88099-141">Aquí, en lugar de todo el conjunto de propiedades de la entidad `user`, solo se devuelven las propiedades `aboutMe`, `displayName` y `skills`.</span><span class="sxs-lookup"><span data-stu-id="88099-141">Here, instead of the entire property sets on the `user` entity, only the `aboutMe`, `displayName`, and `skills` properties are returned.</span></span>

## <a name="traverse-to-another-resource-via-relationship"></a><span data-ttu-id="88099-142">Recorrido a otro recurso a través de la relación</span><span class="sxs-lookup"><span data-stu-id="88099-142">Traverse to another resource via relationship</span></span>
<span data-ttu-id="88099-p107">Un administrador mantiene una relación `directReports` con el resto de los usuarios a su cargo. Para consultar la lista de relaciones directas de un usuario, se puede usar la siguiente solicitud HTTPS GET para navegar hasta el destino deseado mediante un recorrido de relaciones.</span><span class="sxs-lookup"><span data-stu-id="88099-p107">A manager holds a `directReports` relationship with the other users reporting to him or her. To query the list of the direct reports of a user, you can use the following HTTPS GET request to navigate to the intended target via relationship traversal.</span></span> 

```no-highlight 
GET https://graph.microsoft.com/v1.0/users/john.doe@contoso.onmicrosoft.com/directReports HTTP/1.1
Authorization : Bearer <access_token>
```

<span data-ttu-id="88099-145">La respuesta correcta devuelve el estado 200 OK y una carga en el formato siguiente:</span><span class="sxs-lookup"><span data-stu-id="88099-145">The successful response returns the 200 OK status and a payload of the following format:</span></span>

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

<span data-ttu-id="88099-p108">De forma similar, se puede seguir una relación para ir a los recursos relacionados. Por ejemplo, la relación `user => messages` permite un recorrido desde un usuario de Azure AD a un conjunto de mensajes de correo de Outlook. En el ejemplo siguiente, se muestra cómo realizar esta acción en una llamada de la API de REST:</span><span class="sxs-lookup"><span data-stu-id="88099-p108">Similarly, you can follow a relationship to navigate to related resources. For example, the `user => messages` relationship enables traversal from an Azure AD User to a set of Outlook mail messages. The following example shows how to do this in a REST API call:</span></span>


```no-highlight 
GET https://graph.microsoft.com/v1.0/me/messages HTTP/1.1
Authorization : Bearer <access_token>
```

    
<span data-ttu-id="88099-149">La respuesta correcta devuelve el estado 200 OK y una carga en el formato siguiente:</span><span class="sxs-lookup"><span data-stu-id="88099-149">The successful response returns the 200 OK status and a payload of the following format:</span></span>


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

## <a name="project-from-entities-to-properties"></a><span data-ttu-id="88099-150">Proyección desde entidades a las propiedades</span><span class="sxs-lookup"><span data-stu-id="88099-150">Project from entities to properties</span></span>
<span data-ttu-id="88099-p109">Además de la proyección desde una única entidad a sus propiedades, también es posible aplicar la misma opción de consulta `select` a una colección de entidades para proyectarlas a algunas de sus propiedades. Por ejemplo, para consultar el nombre de elementos de la unidad del usuario que ha iniciado sesión, se puede enviar la siguiente solicitud HTTPS GET:</span><span class="sxs-lookup"><span data-stu-id="88099-p109">In addition to projection from a single entity to its properties, you can also apply the similar `select` query option to an entity collection to project them to a collection of some of their properties. For example, to query the name of the signed-in user's drive items, you can submit the following HTTPS GET request:</span></span>

```no-highlight 
GET https://graph.microsoft.com/v1.0/me/drive/root/children?$select=name HTTP/1.1
Authorization : Bearer <access_token>
```

<span data-ttu-id="88099-153">La respuesta correcta devuelve un código de estado 200 OK y una carga que contiene los nombres y los tipos de los archivos compartidos, tal como se muestra en el ejemplo siguiente:</span><span class="sxs-lookup"><span data-stu-id="88099-153">The successful response returns a 200 OK status code and a payload containing the names and types of the shared files, as shown in the following example:</span></span>

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

## <a name="query-a-subset-of-users-with-the-filtering-query-option"></a><span data-ttu-id="88099-154">Consultar un subconjunto de usuarios con la opción de consulta de filtrado</span><span class="sxs-lookup"><span data-stu-id="88099-154">Query a subset of users with the filtering query option</span></span>
<span data-ttu-id="88099-p110">Para encontrar los empleados de un puesto específico en una organización, puede navegar por la colección de usuarios y especificar una opción de consulta de _filtro_. A continuación, se muestra un ejemplo:</span><span class="sxs-lookup"><span data-stu-id="88099-p110">To find the employees of a specific job title within an organization, you can navigate from the users collection and then specify a _filter_ query option. An example is shown as follows:</span></span>

    
```no-highlight 
GET https://graph.microsoft.com/v1.0/users/?$filter=jobTitle+eq+%27Helper%27 HTTP/1.1
Authorization : Bearer <access_token>
```

<span data-ttu-id="88099-157">La respuesta correcta devuelve el código de estado 200 OK y una lista de usuarios con el puesto de trabajo especificado (`'Helper'`), como se muestra en el ejemplo siguiente:</span><span class="sxs-lookup"><span data-stu-id="88099-157">The successful response returns the 200 OK status code and a list of users with the specified job title (`'Helper'`), as shown in the following example:</span></span>

```no-highlight 
HTTP/1.1 200 OK
content-type: application/json;odata.metadata=minimal;odata.streaming=true;IEEE754Compatible=false;charset=utf-8
odata-version: 4.0
content-length: 986

{
    "@odata.context": "https://graph.microsoft.com/v1.0/contoso.onmicrosoft.com/$metadata#users",
    "value": [
        {
            "id": "c95e3b3a-c33b-48da-a6e9-eb101e8a4205",
            "city": "Redmond",
            "country": "USA",
            "department": "Help Center",
            "displayName": "Jane Doe",
            "givenName": "Jane",
            "jobTitle": "Helper",
            ......
            "mailNickname": "Jane",
            "mobile": null,
            "otherMails": [
                "jane.doe@contoso.onmicrosoft.com"
            ],
            ......
            "surname": "Doe",
            "usageLocation": "US",
            "userPrincipalName": "help@contoso.onmicrosoft.com",
            "userType": "Member"
        },
        
        ...
    ]
}
```

## <a name="call-actions-or-functions"></a><span data-ttu-id="88099-158">Llamar a acciones o a funciones</span><span class="sxs-lookup"><span data-stu-id="88099-158">Call actions or functions</span></span>
<span data-ttu-id="88099-p111">Microsoft Graph también admite _acciones_ y _funciones_ para manipular recursos de manera que no sea un simple ajuste con métodos HTTP estándares. Por ejemplo, la siguiente solicitud HTTPS POST permite al usuario que ha iniciado sesión (`me`) enviar un mensaje de correo electrónico:</span><span class="sxs-lookup"><span data-stu-id="88099-p111">Microsoft Graph also supports _actions_ and _functions_ to manipulate resources in ways that are not a simple fit with standard HTTP methods. For example, the following HTTPS POST request lets the signed-in user (`me`) send an email message:</span></span>
```no-highlight 
POST https://graph.microsoft.com/v1.0/me/sendMail HTTP/1.1
authorization: bearer <access_token>
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

<span data-ttu-id="88099-161">La carga de la solicitud contiene la entrada de la acción `sendMail`, que también está definida en $metadata.</span><span class="sxs-lookup"><span data-stu-id="88099-161">The request payload contains the input to the `sendMail` action, which is also defined in the $metadata.</span></span>

## <a name="use-microsoft-graph-client-libraries"></a><span data-ttu-id="88099-162">Usar las bibliotecas cliente .NET de Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="88099-162">Use Microsoft Graph client libraries</span></span>
<span data-ttu-id="88099-p112">Le gustan la potencia y la facilidad de los SDK? Aunque siempre puede llamar a Microsoft Graph con la API REST, hemos proporcionado SDK para muchas plataformas populares.</span><span class="sxs-lookup"><span data-stu-id="88099-p112">Like the power and ease of SDKs? While you can always call Microsoft Graph using the REST API, we also provide SDKs for many popular platforms.</span></span>

<span data-ttu-id="88099-165">Explore nuestra [SDK](https://graph.microsoft.io/en-us/code-samples-and-sdks).</span><span class="sxs-lookup"><span data-stu-id="88099-165">Explore our [SDKs](https://graph.microsoft.io/en-us/code-samples-and-sdks).</span></span>