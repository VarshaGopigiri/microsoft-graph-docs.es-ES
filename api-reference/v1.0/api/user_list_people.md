# <a name="list-people"></a><span data-ttu-id="9a217-101">Enumerar contactos</span><span class="sxs-lookup"><span data-stu-id="9a217-101">List people</span></span>

<span data-ttu-id="9a217-102">Recupera una colección de objetos [person](../resources/person.md) ordenados por su relevancia para el [user](../resources/user.md), que viene determinada por las relaciones empresariales y los patrones de comunicación y colaboración del usuario.</span><span class="sxs-lookup"><span data-stu-id="9a217-102">Retrieve a collection of [person](../resources/person.md) objects ordered by their relevance to the [user](../resources/user.md), which is determined by the user's communication and collaboration patterns, and business relationships.</span></span>

<span data-ttu-id="9a217-p101">Puede obtener esta información a través de la API de contactos. Para obtener ejemplos, vea la sección [Ejemplos](#examples) y el artículo sobre cómo [Obtener información relevante sobre los contactos](../../../concepts/people_example.md).</span><span class="sxs-lookup"><span data-stu-id="9a217-p101">You can get this information via the People API. For examples, see the [Examples](#examples) section and the article [Get relevant information about people](../../../concepts/people_example.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="9a217-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="9a217-105">Permissions</span></span>

<span data-ttu-id="9a217-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="9a217-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="9a217-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="9a217-108">Permission type</span></span>      | <span data-ttu-id="9a217-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="9a217-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="9a217-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="9a217-110">Delegated (work or school account)</span></span> | <span data-ttu-id="9a217-111">People.Read, People.Read.All</span><span class="sxs-lookup"><span data-stu-id="9a217-111">People.Read, People.Read.All</span></span>    |
|<span data-ttu-id="9a217-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="9a217-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="9a217-113">People.Read</span><span class="sxs-lookup"><span data-stu-id="9a217-113">People.Read</span></span>    |
|<span data-ttu-id="9a217-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="9a217-114">Application</span></span> | <span data-ttu-id="9a217-115">People.Read.All</span><span class="sxs-lookup"><span data-stu-id="9a217-115">People.Read.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="9a217-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="9a217-116">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
GET /me/people
GET /users/{id | userPrincipalName}/people
```

## <a name="optional-query-parameters"></a><span data-ttu-id="9a217-117">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="9a217-117">Optional query parameters</span></span>

<span data-ttu-id="9a217-118">Este método admite los [parámetros de consulta de OData](../../../concepts/query_parameters.md) para que le resulte más fácil personalizar la respuesta, como se muestra en los ejemplos del artículo [Obtener información relevante sobre contactos](../../../concepts/people_example.md).</span><span class="sxs-lookup"><span data-stu-id="9a217-118">This method supports the [OData query parameters](../../../concepts/query_parameters.md) to help customize the response, as shown in the examples in the article [Get relevant information about people](../../../concepts/people_example.md).</span></span>

|<span data-ttu-id="9a217-119">Nombre</span><span class="sxs-lookup"><span data-stu-id="9a217-119">Name</span></span>|<span data-ttu-id="9a217-120">Valor</span><span class="sxs-lookup"><span data-stu-id="9a217-120">Value</span></span>|<span data-ttu-id="9a217-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="9a217-121">Description</span></span>|
|:---------------|:--------|:-------|
|<span data-ttu-id="9a217-122">$filter</span><span class="sxs-lookup"><span data-stu-id="9a217-122">$filter</span></span>|<span data-ttu-id="9a217-123">cadena</span><span class="sxs-lookup"><span data-stu-id="9a217-123">string</span></span>|<span data-ttu-id="9a217-124">Limita la respuesta a solo los contactos cuyo registro contiene los criterios especificados.</span><span class="sxs-lookup"><span data-stu-id="9a217-124">Limits the response to only those people whose record contains the specified criteria.</span></span>|
|<span data-ttu-id="9a217-125">$orderby</span><span class="sxs-lookup"><span data-stu-id="9a217-125">$orderby</span></span>|<span data-ttu-id="9a217-126">cadena</span><span class="sxs-lookup"><span data-stu-id="9a217-126">string</span></span>|<span data-ttu-id="9a217-127">De manera predeterminada, los contactos de la respuesta se ordenan por su relevancia para la consulta.</span><span class="sxs-lookup"><span data-stu-id="9a217-127">By default the people in the response are sorted by their relevance to your query.</span></span> <span data-ttu-id="9a217-128">Puede cambiar el orden de los contactos en la respuesta con el parámetro *$orderby*.</span><span class="sxs-lookup"><span data-stu-id="9a217-128">You can change the order of the people in the response using the *$orderby* parameter.</span></span>|
|<span data-ttu-id="9a217-129">$search</span><span class="sxs-lookup"><span data-stu-id="9a217-129">$search</span></span>|<span data-ttu-id="9a217-130">cadena</span><span class="sxs-lookup"><span data-stu-id="9a217-130">string</span></span>|<span data-ttu-id="9a217-131">Busca contactos por nombre o alias.</span><span class="sxs-lookup"><span data-stu-id="9a217-131">Search for people by name or alias.</span></span> <span data-ttu-id="9a217-132">Admite la coincidencia aproximada.</span><span class="sxs-lookup"><span data-stu-id="9a217-132">Supports Fuzzy matching.</span></span> <span data-ttu-id="9a217-133">El parámetro solo funciona para la búsqueda de personas relevantes del usuario que ha iniciado sesión, no para buscar personas relevantes para otros usuarios.</span><span class="sxs-lookup"><span data-stu-id="9a217-133">Parameter only works for searching the signed-in user's relevant people, not for searching people relevant to other users.</span></span> <span data-ttu-id="9a217-134">También es compatible con la palabra clave `topic` para buscar personas en función de los temas que se extraen de las conversaciones de correo electrónico con esa persona.</span><span class="sxs-lookup"><span data-stu-id="9a217-134">Also supports the `topic` keyword to find people based on topics extracted from e-mail conversations with that person.</span></span> <span data-ttu-id="9a217-135">Consulte la sección *Realizar una búsqueda parcial* al [Obtener información relevante acerca de personas](../../../concepts/people_example.md#perform-a-fuzzy-search) para obtener información y ejemplos.</span><span class="sxs-lookup"><span data-stu-id="9a217-135">See the *Perform a fuzzy search* section at [Get relevant information about people](../../../concepts/people_example.md#perform-a-fuzzy-search) for information and examples.</span></span> |
|<span data-ttu-id="9a217-136">$select</span><span class="sxs-lookup"><span data-stu-id="9a217-136">$select</span></span>|<span data-ttu-id="9a217-137">cadena</span><span class="sxs-lookup"><span data-stu-id="9a217-137">string</span></span>|<span data-ttu-id="9a217-p105">Lista separada por comas de las propiedades que se van a incluir en la respuesta. Para un rendimiento óptimo, seleccione solo el subconjunto de propiedades necesarias.</span><span class="sxs-lookup"><span data-stu-id="9a217-p105">Comma-separated list of properties to include in the response. For optimal performance, only select the subset of properties needed.</span></span>|
|<span data-ttu-id="9a217-140">$skip</span><span class="sxs-lookup"><span data-stu-id="9a217-140">$skip</span></span>|<span data-ttu-id="9a217-141">entero</span><span class="sxs-lookup"><span data-stu-id="9a217-141">int</span></span>|<span data-ttu-id="9a217-p106">Se omiten los primeros resultados n, útil para la paginación. Esta opción no se admite cuando se usa *$search*.</span><span class="sxs-lookup"><span data-stu-id="9a217-p106">Skip the first n results, useful for paging. This is not supported when using *$search*.</span></span>|
|<span data-ttu-id="9a217-144">$top</span><span class="sxs-lookup"><span data-stu-id="9a217-144">$top</span></span>|<span data-ttu-id="9a217-145">entero</span><span class="sxs-lookup"><span data-stu-id="9a217-145">int</span></span>|<span data-ttu-id="9a217-146">Número de resultados que se van a devolver.</span><span class="sxs-lookup"><span data-stu-id="9a217-146">Number of results to be returned.</span></span>|

## <a name="request-headers"></a><span data-ttu-id="9a217-147">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="9a217-147">Request headers</span></span>

| <span data-ttu-id="9a217-148">Nombre</span><span class="sxs-lookup"><span data-stu-id="9a217-148">Name</span></span>      |<span data-ttu-id="9a217-149">Descripción</span><span class="sxs-lookup"><span data-stu-id="9a217-149">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="9a217-150">Authorization</span><span class="sxs-lookup"><span data-stu-id="9a217-150">Authorization</span></span>  | <span data-ttu-id="9a217-p107">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="9a217-p107">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="9a217-153">Accept</span><span class="sxs-lookup"><span data-stu-id="9a217-153">Accept</span></span> | <span data-ttu-id="9a217-154">application/json</span><span class="sxs-lookup"><span data-stu-id="9a217-154">application/json</span></span> |

## <a name="request-body"></a><span data-ttu-id="9a217-155">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="9a217-155">Request body</span></span>

<span data-ttu-id="9a217-156">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="9a217-156">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="9a217-157">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9a217-157">Response</span></span>

<span data-ttu-id="9a217-p108">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [person](../resources/person.md) en el cuerpo de la respuesta. La respuesta puede contener un objeto person o una colección de objetos person.</span><span class="sxs-lookup"><span data-stu-id="9a217-p108">If successful, this method returns a `200 OK` response code and a collection of [person](../resources/person.md) objects in the response body. The response can contain one person object or a collection of person objects.</span></span>

## <a name="examples"></a><span data-ttu-id="9a217-160">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="9a217-160">Examples</span></span>

#### <a name="request"></a><span data-ttu-id="9a217-161">Solicitud</span><span class="sxs-lookup"><span data-stu-id="9a217-161">Request</span></span>

<span data-ttu-id="9a217-162">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="9a217-162">The following is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "get_person_collection"
}-->

```http
GET https://graph.microsoft.com/v1.0/me/people
```

#### <a name="response"></a><span data-ttu-id="9a217-163">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9a217-163">Response</span></span>

<span data-ttu-id="9a217-164">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9a217-164">The following is an example of the response.</span></span>

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

<span data-ttu-id="9a217-165">Para obtener ejemplos, vea el artículo [Obtener información relevante sobre los contactos](../../../concepts/people_example.md).</span><span class="sxs-lookup"><span data-stu-id="9a217-165">For more examples, see the article [Get relevant information about people](../../../concepts/people_example.md).</span></span>

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List people",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
