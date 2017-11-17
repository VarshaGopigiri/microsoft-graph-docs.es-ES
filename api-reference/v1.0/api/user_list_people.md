# <a name="list-people"></a><span data-ttu-id="310f8-101">List people</span><span class="sxs-lookup"><span data-stu-id="310f8-101">List people</span></span>

<span data-ttu-id="310f8-102">Recupera una colección de objetos [person](../resources/person.md) ordenados por su relevancia para el [user](../resources/user.md), que viene determinada por las relaciones empresariales y los patrones de comunicación y colaboración del usuario.</span><span class="sxs-lookup"><span data-stu-id="310f8-102">Retrieve a collection of [person](../resources/person.md) objects ordered by their relevance to the [user](../resources/user.md), which is determined by the user's communication and collaboration patterns and business relationships.</span></span>

<span data-ttu-id="310f8-p101">Puede obtener esta información a través de la API de contactos. Para obtener ejemplos, vea la sección [Ejemplos](#examples) y el artículo sobre cómo [Obtener información relevante sobre los contactos](../../../concepts/people_example.md).</span><span class="sxs-lookup"><span data-stu-id="310f8-p101">You can get this information via the People API. For examples, see the [Examples](#examples) section and the article [Get relevant information about people](../../../concepts/people_example.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="310f8-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="310f8-105">Permissions</span></span>
<span data-ttu-id="310f8-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="310f8-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>
 

|<span data-ttu-id="310f8-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="310f8-108">Permission type</span></span>      | <span data-ttu-id="310f8-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="310f8-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="310f8-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="310f8-110">Delegated (work or school account)</span></span> | <span data-ttu-id="310f8-111">People.Read, People.Read.All</span><span class="sxs-lookup"><span data-stu-id="310f8-111">People.Read, People.Read.All</span></span>    |
|<span data-ttu-id="310f8-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="310f8-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="310f8-113">People.Read</span><span class="sxs-lookup"><span data-stu-id="310f8-113">People.Read</span></span>    |
|<span data-ttu-id="310f8-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="310f8-114">Application</span></span> | <span data-ttu-id="310f8-115">People.Read.All</span><span class="sxs-lookup"><span data-stu-id="310f8-115">People.Read.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="310f8-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="310f8-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/people
GET /users/{id | userPrincipalName}/people
```
## <a name="optional-query-parameters"></a><span data-ttu-id="310f8-117">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="310f8-117">Optional query parameters</span></span>
|<span data-ttu-id="310f8-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="310f8-118">Name</span></span>|<span data-ttu-id="310f8-119">Valor</span><span class="sxs-lookup"><span data-stu-id="310f8-119">Value</span></span>|<span data-ttu-id="310f8-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="310f8-120">Description</span></span>|
|:---------------|:--------|:-------|
|<span data-ttu-id="310f8-121">$filter</span><span class="sxs-lookup"><span data-stu-id="310f8-121">$filter</span></span>|<span data-ttu-id="310f8-122">string</span><span class="sxs-lookup"><span data-stu-id="310f8-122">string</span></span>|<span data-ttu-id="310f8-123">Limita la respuesta a solo los contactos cuyo registro contiene los criterios especificados.</span><span class="sxs-lookup"><span data-stu-id="310f8-123">Limits the response to only those people whose record contains the specified criteria.</span></span>|
|<span data-ttu-id="310f8-124">$orderby</span><span class="sxs-lookup"><span data-stu-id="310f8-124">$orderby</span></span>|<span data-ttu-id="310f8-125">string</span><span class="sxs-lookup"><span data-stu-id="310f8-125">string</span></span>|<span data-ttu-id="310f8-p103">De manera predeterminada, los contactos de la respuesta se ordenan por su relevancia para la consulta. Puede cambiar el orden de los contactos en la respuesta con el parámetro *$orderby*.</span><span class="sxs-lookup"><span data-stu-id="310f8-p103">By default, the people in the response are sorted by their relevance to your query. You can change the order of the people in the response by using the *$orderby* parameter.</span></span>|
|<span data-ttu-id="310f8-128">$search</span><span class="sxs-lookup"><span data-stu-id="310f8-128">$search</span></span>|<span data-ttu-id="310f8-129">string</span><span class="sxs-lookup"><span data-stu-id="310f8-129">string</span></span>|<span data-ttu-id="310f8-p104">Se buscan contactos por nombre o alias. Admite coincidencia aproximada.</span><span class="sxs-lookup"><span data-stu-id="310f8-p104">Search for people by name or alias. Supports fuzzy matching.</span></span>|
|<span data-ttu-id="310f8-132">$select</span><span class="sxs-lookup"><span data-stu-id="310f8-132">$select</span></span>|<span data-ttu-id="310f8-133">string</span><span class="sxs-lookup"><span data-stu-id="310f8-133">string</span></span>|<span data-ttu-id="310f8-p105">Lista separada por comas de las propiedades que se van a incluir en la respuesta. Para un rendimiento óptimo, seleccione solo el subconjunto de propiedades necesarias.</span><span class="sxs-lookup"><span data-stu-id="310f8-p105">Comma-separated list of properties to include in the response. For optimal performance, only select the subset of properties needed.</span></span>|
|<span data-ttu-id="310f8-136">$skip</span><span class="sxs-lookup"><span data-stu-id="310f8-136">$skip</span></span>|<span data-ttu-id="310f8-137">int</span><span class="sxs-lookup"><span data-stu-id="310f8-137">int</span></span>|<span data-ttu-id="310f8-p106">Se omiten los primeros resultados n, útil para la paginación. Esta opción no se admite cuando se usa *$search*.</span><span class="sxs-lookup"><span data-stu-id="310f8-p106">Skip the first n results, useful for paging. This is not supported when using *$search*.</span></span>|
|<span data-ttu-id="310f8-140">$top</span><span class="sxs-lookup"><span data-stu-id="310f8-140">$top</span></span>|<span data-ttu-id="310f8-141">int</span><span class="sxs-lookup"><span data-stu-id="310f8-141">int</span></span>|<span data-ttu-id="310f8-142">Número de resultados que se van a devolver.</span><span class="sxs-lookup"><span data-stu-id="310f8-142">Number of results to be returned.</span></span>|

## <a name="request-headers"></a><span data-ttu-id="310f8-143">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="310f8-143">Request headers</span></span>
| <span data-ttu-id="310f8-144">Nombre</span><span class="sxs-lookup"><span data-stu-id="310f8-144">Name</span></span>      |<span data-ttu-id="310f8-145">Descripción</span><span class="sxs-lookup"><span data-stu-id="310f8-145">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="310f8-146">Authorization</span><span class="sxs-lookup"><span data-stu-id="310f8-146">Authorization</span></span>  | <span data-ttu-id="310f8-p107">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="310f8-p107">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="310f8-149">Aceptar</span><span class="sxs-lookup"><span data-stu-id="310f8-149">Accept</span></span> | <span data-ttu-id="310f8-150">application/json</span><span class="sxs-lookup"><span data-stu-id="310f8-150">application/json</span></span> |

## <a name="request-body"></a><span data-ttu-id="310f8-151">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="310f8-151">Request body</span></span>
<span data-ttu-id="310f8-152">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="310f8-152">Do not supply a request body for this method.</span></span>
## <a name="response"></a><span data-ttu-id="310f8-153">Respuesta</span><span class="sxs-lookup"><span data-stu-id="310f8-153">Response</span></span>
<span data-ttu-id="310f8-p108">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [person](../resources/person.md) en el cuerpo de la respuesta. La respuesta puede contener un objeto person o una colección de objetos person.</span><span class="sxs-lookup"><span data-stu-id="310f8-p108">If successful, this method returns a `200 OK` response code and a collection of [person](../resources/person.md) objects in the response body. The response can contain one person object or a collection of person objects.</span></span> 
## <a name="examples"></a><span data-ttu-id="310f8-156">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="310f8-156">Examples</span></span>

### <a name="get-a-collection-of-relevant-people"></a><span data-ttu-id="310f8-157">Obtener una colección de contactos relevantes</span><span class="sxs-lookup"><span data-stu-id="310f8-157">Get a collection of relevant people</span></span> 

<span data-ttu-id="310f8-158">La siguiente solicitud obtiene los contactos más relevantes para el usuario que ha iniciado sesión (`/me`), en función de las relaciones empresariales y los patrones de comunicación y colaboración del usuario.</span><span class="sxs-lookup"><span data-stu-id="310f8-158">The following request gets the people most relevant to the signed-in user (`/me`), based on communication and collaboration patterns and business relationships.</span></span> 
<!-- {
  "blockType": "request",
  "name": "get_person_collection"
}-->

```http
GET https://graph.microsoft.com/v1.0/me/people/
```

<span data-ttu-id="310f8-p109">En el ejemplo siguiente se muestra la respuesta. De manera predeterminada, cada respuesta devuelve 10 registros. Esto se puede cambiar mediante el parámetro de consulta *$top*. En este ejemplo se usa *$top* para limitar la respuesta a tres registros.</span><span class="sxs-lookup"><span data-stu-id="310f8-p109">The following example shows the response. By default, each response returns 10 records. You can change this by using the *$top* query parameter. This example uses *$top* to limit the response to three records.</span></span>
<!-- {
  "blockType": "response",
  "name": "get_person_collection",
  "truncated": true,
  "@odata.type": "microsoft.graph.person",
  "isCollection": true
} -->

```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "value": [
        {
            "id": "8CE6E1DE-CB84-4BF5-971D-D3ECF452E2B5",
            "displayName": "Lorrie Frye",
            "givenName": "Lorrie",
            "surname": "Frye",
            "birthday": "",
            "personNotes": "",
            "isFavorite": false,
            "jobTitle": "Paralegal",
            "companyName": null,
            "yomiCompany": "",
            "department": "Legal",
            "officeLocation": "20/1109",
            "profession": "",
            "userPrincipalName": "Lorrief@contoso.onmicrosoft.com",
            "imAddress": "sip:Lorrief@contoso.onmicrosoft.com",
            "scoredEmailAddresses": [
                {
                    "address": "Lorrief@contoso.onmicrosoft.com",
                    "relevanceScore": 8.0
                }
            ],
            "phones": [
                {
                    "type": "Business",
                    "number": "+1 980 555 0101"
                }
            ],
            "postalAddresses": [],
            "websites": [],
            "personType": [
                {
                    "class": "Person",
                    "subclass": "OrganizationUser"
                }
            ]
        },
        {
            "id": "5767393D-42BA-4E5C-BEE4-52BB25639CF4",
            "displayName": "Maynard Denman",
            "givenName": "Maynard",
            "surname": "Denman",
            "birthday": "",
            "personNotes": "",
            "isFavorite": false,
            "jobTitle": "Web Marketing Manager",
            "companyName": null,
            "yomiCompany": "",
            "department": "Sales & Marketing",
            "officeLocation": "20/1101",
            "profession": "",
            "userPrincipalName": "Maynardd@contoso.onmicrosoft.com",
            "imAddress": "sip:Maynardd@contoso.onmicrosoft.com",
            "scoredEmailAddresses": [
                {
                    "address": "Maynardd@contoso.onmicrosoft.com",
                    "relevanceScore": 8.0
                }
            ],
            "phones": [
                {
                    "type": "Business",
                    "number": "+1 918 555 0101"
                }
            ],
            "postalAddresses": [],
            "websites": [],
            "personType": [
                {
                    "class": "Person",
                    "subclass": "OrganizationUser"
                }
            ]
        },
        {
            "id": "914B5191-11FA-4C0B-A354-0FA8C8EFD585",
            "displayName": "Darrel Halsey",
            "givenName": "Darrel",
            "surname": "Halsey",
            "birthday": "",
            "personNotes": "",
            "isFavorite": false,
            "jobTitle": "Attorney",
            "companyName": null,
            "yomiCompany": "",
            "department": "Legal",
            "officeLocation": "14/1102",
            "profession": "",
            "userPrincipalName": "Darrelh@contoso.onmicrosoft.com",
            "imAddress": "sip:Darrelh@contoso.onmicrosoft.com",
            "scoredEmailAddresses": [
                {
                    "address": "Darrelh@contoso.onmicrosoft.com",
                    "relevanceScore": 8.0
                }
            ],
            "phones": [
                {
                    "type": "Business",
                    "number": "+1 205 555 0103"
                }
            ],
            "postalAddresses": [],
            "websites": [],
            "personType": [
                {
                    "class": "Person",
                    "subclass": "OrganizationUser"
                }
            ]
        }
    ]
}
```
### <a name="search-other-users-relevant-people"></a><span data-ttu-id="310f8-163">Buscar otros contactos relevantes para el usuario</span><span class="sxs-lookup"><span data-stu-id="310f8-163">Search other user’s relevant people</span></span>

<span data-ttu-id="310f8-p110">La siguiente solicitud obtiene los contactos más relevantes para otro contacto de la organización del usuario que ha iniciado sesión. Esta solicitud requiere el permiso People.Read.All. En este ejemplo, se muestran los contactos relevantes de Roscoe Seidel.</span><span class="sxs-lookup"><span data-stu-id="310f8-p110">The following request gets the people most relevant to another person in the signed-in user's organization. This request requires the People.Read.All permission. In this example, Roscoe Seidel's relevant people are displayed.</span></span>

<!-- {
  "blockType": "request",
  "name": "get_other_person"
}-->

```http
GET https://graph.microsoft.com/v1.0/users('roscoes@contoso.com')/people/
```

<span data-ttu-id="310f8-p111">En el ejemplo siguiente se muestra la respuesta. De manera predeterminada, cada respuesta devuelve 10 registros. Esto se puede cambiar mediante el parámetro *$top*. En este ejemplo se usa *$top* para limitar la respuesta a tres registros.</span><span class="sxs-lookup"><span data-stu-id="310f8-p111">The following example shows the response. By default, each response returns 10 records. You can change this by using the *$top* parameter. This example uses *$top* to limit the response to three records.</span></span>

<!-- {
  "blockType": "response",
  "name": "get_other_person",
  "truncated": true,
  "@odata.type": "microsoft.graph.person",
  "isCollection": true
} -->

```http
HTTP/1.1 200 OK
Content-type: application/json

{
     "value": [
        {
            "id": "56155636-703F-47F2-B657-C83F01F49BBC",
            "displayName": "Clifton Clemente",
            "givenName": "Clifton",
            "surname": "Clemente",
            "birthday": "",
            "personNotes": "",
            "isFavorite": false,
            "jobTitle": "Director",
            "companyName": null,
            "yomiCompany": "",
            "department": "Legal",
            "officeLocation": "19/2106",
            "profession": "",
            "userPrincipalName": "Cliftonc@contoso.onmicrosoft.com",
            "imAddress": "sip:Cliftonc@contoso.onmicrosoft.com",
            "scoredEmailAddresses": [
                {
                    "address": "Cliftonc@contoso.onmicrosoft.com",
                    "relevanceScore": 20.0
                }
            ],
            "phones": [
                {
                    "type": "Business",
                    "number": "+1 309 555 0101"
                }
            ],
            "postalAddresses": [],
            "websites": [],
            "personType": [
                {
                    "class": "Person",
                    "subclass": "OrganizationUser"
                }
            ]
        },
        {
            "id": "6BF27D5A-AB4F-4C43-BED0-7DAD9EB0C1C4",
            "displayName": "Sheree Mitchell",
            "givenName": "Sheree",
            "surname": "Mitchell",
            "birthday": "",
            "personNotes": "",
            "isFavorite": false,
            "jobTitle": "Product Manager",
            "companyName": null,
            "yomiCompany": "",
            "department": "Sales & Marketing",
            "officeLocation": "20/2107",
            "profession": "",
            "userPrincipalName": "Shereem@contoso.onmicrosoft.com",
            "imAddress": "sip:shereem@contoso.onmicrosoft.com",
            "scoredEmailAddresses": [
                {
                    "address": "Shereem@contoso.onmicrosoft.com",
                    "relevanceScore": 10.0
                }
            ],
            "phones": [
                {
                    "type": "Business",
                    "number": "+1 918 555 0107"
                }
            ],
            "postalAddresses": [],
            "websites": [],
            "personType": [
                {
                    "class": "Person",
                    "subclass": "OrganizationUser"
                }
            ]
        },
        {
            "id": "B3E5302D-EAF0-4E8B-8C6C-A2AE64B4B163",
            "displayName": "Vincent Matney",
            "givenName": "Vincent",
            "surname": "Matney",
            "birthday": "",
            "personNotes": "",
            "isFavorite": false,
            "jobTitle": "CVP Engineering",
            "companyName": null,
            "yomiCompany": "",
            "department": "Engineering",
            "officeLocation": "23/2102",
            "profession": "",
            "userPrincipalName": "Vincentm@contoso.onmicrosoft.com",
            "imAddress": "sip:vincentm@contoso.onmicrosoft.com",
            "scoredEmailAddresses": [
                {
                    "address": "Vincentm@contoso.onmicrosoft.com",
                    "relevanceScore": 10.0
                }
            ],
            "phones": [
                {
                    "type": "Business",
                    "number": "+1 502 555 0102"
                }
            ],
            "postalAddresses": [],
            "websites": [],
            "personType": [
                {
                    "class": "Person",
                    "subclass": "OrganizationUser"
                }
            ]
        }
    ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List people",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
