# <a name="list-people"></a><span data-ttu-id="d03f2-101">Enumerar contactos</span><span class="sxs-lookup"><span data-stu-id="d03f2-101">List people</span></span>

<span data-ttu-id="d03f2-102">Recupera una colección de objetos [person](../resources/person.md) ordenados por su relevancia para el [user](../resources/user.md), que viene determinada por las relaciones empresariales y los patrones de comunicación y colaboración del usuario.</span><span class="sxs-lookup"><span data-stu-id="d03f2-102">Retrieve a collection of [person](../resources/person.md) objects ordered by their relevance to the [user](../resources/user.md), which is determined by the user's communication and collaboration patterns and business relationships.</span></span>

<span data-ttu-id="d03f2-p101">Puede obtener esta información a través de la API de contactos. Para obtener ejemplos, vea la sección [Ejemplos](#examples) y el artículo sobre cómo [Obtener información relevante sobre los contactos](../../../concepts/people_example.md).</span><span class="sxs-lookup"><span data-stu-id="d03f2-p101">You can get this information via the People API. For examples, see the [Examples](#examples) section and the article [Get relevant information about people](../../../concepts/people_example.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="d03f2-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="d03f2-105">Permissions</span></span>
<span data-ttu-id="d03f2-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="d03f2-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="d03f2-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="d03f2-108">Permission type</span></span>      | <span data-ttu-id="d03f2-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="d03f2-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="d03f2-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d03f2-110">Delegated (work or school account)</span></span> | <span data-ttu-id="d03f2-111">People.Read, People.Read.All</span><span class="sxs-lookup"><span data-stu-id="d03f2-111">People.Read, People.Read.All</span></span>    |
|<span data-ttu-id="d03f2-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="d03f2-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="d03f2-113">People.Read</span><span class="sxs-lookup"><span data-stu-id="d03f2-113">People.Read</span></span>    |
|<span data-ttu-id="d03f2-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d03f2-114">Application</span></span> | <span data-ttu-id="d03f2-115">People.Read.All</span><span class="sxs-lookup"><span data-stu-id="d03f2-115">People.Read.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="d03f2-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d03f2-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/people
GET /users/{id | userPrincipalName}/people
```

## <a name="optional-query-parameters"></a><span data-ttu-id="d03f2-117">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="d03f2-117">Optional query parameters</span></span>
<span data-ttu-id="d03f2-118">Este método admite los [parámetros de consulta de OData](../../../concepts/people_example.md) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d03f2-118">This method supports the [OData Query Parameters](../../../concepts/people_example.md) to help customize the response.</span></span>

|<span data-ttu-id="d03f2-119">Nombre</span><span class="sxs-lookup"><span data-stu-id="d03f2-119">Name</span></span>|<span data-ttu-id="d03f2-120">Valor</span><span class="sxs-lookup"><span data-stu-id="d03f2-120">Value</span></span>|<span data-ttu-id="d03f2-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="d03f2-121">Description</span></span>| 
|:---------------|:--------|:-------| 
|<span data-ttu-id="d03f2-122">$filter</span><span class="sxs-lookup"><span data-stu-id="d03f2-122">$filter</span></span>|<span data-ttu-id="d03f2-123">string</span><span class="sxs-lookup"><span data-stu-id="d03f2-123">string</span></span>|<span data-ttu-id="d03f2-124">Limita la respuesta a solo los contactos cuyo registro contiene los criterios especificados.</span><span class="sxs-lookup"><span data-stu-id="d03f2-124">Limits the response to only those people whose record contains the specified criteria.</span></span>| 
|<span data-ttu-id="d03f2-125">$orderby</span><span class="sxs-lookup"><span data-stu-id="d03f2-125">$orderby</span></span>|<span data-ttu-id="d03f2-126">cadena</span><span class="sxs-lookup"><span data-stu-id="d03f2-126">string</span></span>|<span data-ttu-id="d03f2-127">De manera predeterminada, los contactos de la respuesta se ordenan por su relevancia para la consulta.</span><span class="sxs-lookup"><span data-stu-id="d03f2-127">By default, the people in the response are sorted by their relevance to your query. You can change the order of the people in the response using the $orderby parameter.</span></span> <span data-ttu-id="d03f2-128">Puede cambiar el orden de los contactos en la respuesta con el parámetro *$orderby*.</span><span class="sxs-lookup"><span data-stu-id="d03f2-128">By default, the people in the response are sorted by their relevance to your query. You can change the order of the people in the response using the *$orderby* parameter.</span></span>| 
|<span data-ttu-id="d03f2-129">$search</span><span class="sxs-lookup"><span data-stu-id="d03f2-129">$search</span></span>|<span data-ttu-id="d03f2-130">string</span><span class="sxs-lookup"><span data-stu-id="d03f2-130">string</span></span>|<span data-ttu-id="d03f2-131">Se buscan contactos por nombre o alias.</span><span class="sxs-lookup"><span data-stu-id="d03f2-131">Search for people by name or alias. Supports fuzzy matching.</span></span> <span data-ttu-id="d03f2-132">Admite coincidencia aproximada</span><span class="sxs-lookup"><span data-stu-id="d03f2-132">Supports Fuzzy matching</span></span>| 
|<span data-ttu-id="d03f2-133">$select</span><span class="sxs-lookup"><span data-stu-id="d03f2-133">$select</span></span>|<span data-ttu-id="d03f2-134">string</span><span class="sxs-lookup"><span data-stu-id="d03f2-134">string</span></span>|<span data-ttu-id="d03f2-p105">Lista separada por comas de las propiedades que se van a incluir en la respuesta. Para un rendimiento óptimo, seleccione solo el subconjunto de propiedades necesarias.</span><span class="sxs-lookup"><span data-stu-id="d03f2-p105">Comma-separated list of properties to include in the response. For optimal performance, only select the subset of properties needed.</span></span>| 
|<span data-ttu-id="d03f2-137">$skip</span><span class="sxs-lookup"><span data-stu-id="d03f2-137">$skip</span></span>|<span data-ttu-id="d03f2-138">int</span><span class="sxs-lookup"><span data-stu-id="d03f2-138">int</span></span>|<span data-ttu-id="d03f2-p106">Se omiten los primeros resultados n, útil para la paginación. Esta opción no se admite cuando se usa *$search*.</span><span class="sxs-lookup"><span data-stu-id="d03f2-p106">Skip the first n results, useful for paging. This is not supported when using *$search*.</span></span>| 
|<span data-ttu-id="d03f2-141">$top</span><span class="sxs-lookup"><span data-stu-id="d03f2-141">$top</span></span>|<span data-ttu-id="d03f2-142">int</span><span class="sxs-lookup"><span data-stu-id="d03f2-142">int</span></span>|<span data-ttu-id="d03f2-143">Número de resultados que se van a devolver.</span><span class="sxs-lookup"><span data-stu-id="d03f2-143">Number of results to be returned.</span></span>| 

## <a name="request-headers"></a><span data-ttu-id="d03f2-144">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d03f2-144">Request headers</span></span>
| <span data-ttu-id="d03f2-145">Nombre</span><span class="sxs-lookup"><span data-stu-id="d03f2-145">Name</span></span>      |<span data-ttu-id="d03f2-146">Descripción</span><span class="sxs-lookup"><span data-stu-id="d03f2-146">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="d03f2-147">Authorization</span><span class="sxs-lookup"><span data-stu-id="d03f2-147">Authorization</span></span>  | <span data-ttu-id="d03f2-p107">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="d03f2-p107">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="d03f2-150">Aceptar</span><span class="sxs-lookup"><span data-stu-id="d03f2-150">Accept</span></span> | <span data-ttu-id="d03f2-151">application/json</span><span class="sxs-lookup"><span data-stu-id="d03f2-151">application/json</span></span> |

## <a name="request-body"></a><span data-ttu-id="d03f2-152">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="d03f2-152">Request body</span></span>
<span data-ttu-id="d03f2-153">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="d03f2-153">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="d03f2-154">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d03f2-154">Response</span></span>
<span data-ttu-id="d03f2-p108">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [person](../resources/person.md) en el cuerpo de la respuesta. La respuesta puede contener un objeto person o una colección de objetos person.</span><span class="sxs-lookup"><span data-stu-id="d03f2-p108">If successful, this method returns a `200 OK` response code and a collection of [person](../resources/person.md) objects in the response body. The response can contain one person object or a collection of person objects.</span></span>

## <a name="examples"></a><span data-ttu-id="d03f2-157">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="d03f2-157">Examples</span></span>
#### <a name="request"></a><span data-ttu-id="d03f2-158">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d03f2-158">Request</span></span>
<span data-ttu-id="d03f2-159">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d03f2-159">The following is an example of making the request in ASP.NET that uses the TokenHelper file:</span></span>

<!-- {
  "blockType": "request",
  "name": "get_person_collection"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/people
```

#### <a name="response"></a><span data-ttu-id="d03f2-160">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d03f2-160">Response</span></span>
<span data-ttu-id="d03f2-161">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d03f2-161">Here is an example of the response.</span></span>

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
Content-length: 1370

{
    "value": [
        {
            "id": "33b43a5b-87d6-41ec-91f8-a2610048105f",
            "displayName": "Marketing",
            "givenName": null,
            "surname": null,
            "birthday": "",
            "personNotes": "",
            "isFavorite": false,
            "jobTitle": null,
            "companyName": null,
            "yomiCompany": "",
            "department": null,
            "officeLocation": null,
            "profession": "",
            "userPrincipalName": "",
            "imAddress": null,
            "scoredEmailAddresses": [
                {
                    "address": "Marketing@contoso.com",
                    "relevanceScore": 30.0
                }
            ],
            "phones": [],
            "postalAddresses": [],
            "websites": [],
            "personType": {
                "class": "Group",
                "subclass": "UnifiedGroup"
            }
        },
        {
            "id": "e3d0513b-449e-4198-ba6f-bd97ae7cae85",
            "displayName": "Isaiah Langer",
            "givenName": "Isaiah",
            "surname": "Langer",
            "birthday": "",
            "personNotes": "",
            "isFavorite": false,
            "jobTitle": "Web Marketing Manager",
            "companyName": null,
            "yomiCompany": "",
            "department": "Sales & Marketing",
            "officeLocation": "20/1101",
            "profession": "",
            "userPrincipalName": "IsaiahL@contoso.com",
            "imAddress": "sip:isaiahl@contoso.com",
            "scoredEmailAddresses": [
                {
                    "address": "IsaiahL@contoso.com",
                    "relevanceScore": 20.0
                }
            ],
            "phones": [
                {
                    "type": "business",
                    "number": "+1 918 555 0101"
                }
            ],
            "postalAddresses": [],
            "websites": [],
            "personType": {
                "class": "Person",
                "subclass": "OrganizationUser"
            }
        }
    ]
}
```

<span data-ttu-id="d03f2-162">Para obtener ejemplos, vea el artículo [Obtener información relevante sobre los contactos](../../../concepts/people_example.md).</span><span class="sxs-lookup"><span data-stu-id="d03f2-162">For more examples, see the article [Get relevant information about people](../../../concepts/people_example.md).</span></span>

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List people",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
