# <a name="get-person"></a><span data-ttu-id="f05c4-101">Get person</span><span class="sxs-lookup"><span data-stu-id="f05c4-101">Get person</span></span>

<span data-ttu-id="f05c4-102">Recupere las propiedades y las relaciones del objeto [person](../resources/person.md).</span><span class="sxs-lookup"><span data-stu-id="f05c4-102">Retrieve the properties and relationships of a [person](../resources/person.md) object.</span></span>

<span data-ttu-id="f05c4-p101">Puede obtener esta información a través de la API de contactos. Para obtener ejemplos, vea la sección [Ejemplos](#examples) y el artículo sobre cómo [Obtener información relevante sobre los contactos](../../../concepts/people_example.md).</span><span class="sxs-lookup"><span data-stu-id="f05c4-p101">You can get this information via the People API. For examples, see the [Examples](#examples) section and the article [Get relevant information about people](../../../concepts/people_example.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="f05c4-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="f05c4-105">Permissions</span></span>
<span data-ttu-id="f05c4-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="f05c4-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>
 

|<span data-ttu-id="f05c4-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f05c4-108">Permission type</span></span>      | <span data-ttu-id="f05c4-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f05c4-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="f05c4-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f05c4-110">Delegated (work or school account)</span></span> | <span data-ttu-id="f05c4-111">People.Read, People.Read.All</span><span class="sxs-lookup"><span data-stu-id="f05c4-111">People.Read, People.Read.All</span></span>    |
|<span data-ttu-id="f05c4-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f05c4-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="f05c4-113">People.Read</span><span class="sxs-lookup"><span data-stu-id="f05c4-113">People.Read</span></span>    |
|<span data-ttu-id="f05c4-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f05c4-114">Application</span></span> | <span data-ttu-id="f05c4-115">People.Read.All</span><span class="sxs-lookup"><span data-stu-id="f05c4-115">People.Read.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="f05c4-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f05c4-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->

```http
GET /me/people/{id}
GET /users/{id | userPrincipalName}/people/{id}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="f05c4-117">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="f05c4-117">Optional query parameters</span></span>
<span data-ttu-id="f05c4-118">Este método admite los siguientes [parámetros de consulta de OData](../../../concepts/people_example.md) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f05c4-118">This method supports the [OData Query Parameters](../../../concepts/people_example.md) to help customize the response.</span></span>

|<span data-ttu-id="f05c4-119">Nombre</span><span class="sxs-lookup"><span data-stu-id="f05c4-119">Name</span></span>|<span data-ttu-id="f05c4-120">Valor</span><span class="sxs-lookup"><span data-stu-id="f05c4-120">Value</span></span>|<span data-ttu-id="f05c4-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="f05c4-121">Description</span></span>| 
|:---------------|:--------|:-------| 
|<span data-ttu-id="f05c4-122">$filter</span><span class="sxs-lookup"><span data-stu-id="f05c4-122">$filter</span></span>|<span data-ttu-id="f05c4-123">string</span><span class="sxs-lookup"><span data-stu-id="f05c4-123">string</span></span>|<span data-ttu-id="f05c4-124">Limita la respuesta a solo los contactos cuyo registro contiene los criterios especificados.</span><span class="sxs-lookup"><span data-stu-id="f05c4-124">Limits the response to only those people whose record contains the specified criteria.</span></span>| 
|<span data-ttu-id="f05c4-125">$orderby</span><span class="sxs-lookup"><span data-stu-id="f05c4-125">$orderby</span></span>|<span data-ttu-id="f05c4-126">cadena</span><span class="sxs-lookup"><span data-stu-id="f05c4-126">string</span></span>|<span data-ttu-id="f05c4-127">De manera predeterminada, los contactos de la respuesta se ordenan por su relevancia para la consulta.</span><span class="sxs-lookup"><span data-stu-id="f05c4-127">By default, the people in the response are sorted by their relevance to your query. You can change the order of the people in the response using the $orderby parameter.</span></span> <span data-ttu-id="f05c4-128">Puede cambiar el orden de los contactos en la respuesta con el parámetro *$orderby*.</span><span class="sxs-lookup"><span data-stu-id="f05c4-128">By default, the people in the response are sorted by their relevance to your query. You can change the order of the people in the response using the *$orderby* parameter.</span></span>| 
|<span data-ttu-id="f05c4-129">$search</span><span class="sxs-lookup"><span data-stu-id="f05c4-129">$search</span></span>|<span data-ttu-id="f05c4-130">string</span><span class="sxs-lookup"><span data-stu-id="f05c4-130">string</span></span>|<span data-ttu-id="f05c4-131">Se buscan contactos por nombre o alias.</span><span class="sxs-lookup"><span data-stu-id="f05c4-131">Search for people by name or alias. Supports fuzzy matching.</span></span> <span data-ttu-id="f05c4-132">Admite coincidencia aproximada</span><span class="sxs-lookup"><span data-stu-id="f05c4-132">Supports Fuzzy matching</span></span>| 
|<span data-ttu-id="f05c4-133">$select</span><span class="sxs-lookup"><span data-stu-id="f05c4-133">$select</span></span>|<span data-ttu-id="f05c4-134">string</span><span class="sxs-lookup"><span data-stu-id="f05c4-134">string</span></span>|<span data-ttu-id="f05c4-p105">Lista separada por comas de las propiedades que se van a incluir en la respuesta. Para un rendimiento óptimo, seleccione solo el subconjunto de propiedades necesarias.</span><span class="sxs-lookup"><span data-stu-id="f05c4-p105">Comma-separated list of properties to include in the response. For optimal performance, only select the subset of properties needed.</span></span>| 
|<span data-ttu-id="f05c4-137">$skip</span><span class="sxs-lookup"><span data-stu-id="f05c4-137">$skip</span></span>|<span data-ttu-id="f05c4-138">int</span><span class="sxs-lookup"><span data-stu-id="f05c4-138">int</span></span>|<span data-ttu-id="f05c4-p106">Se omiten los primeros resultados n, útil para la paginación. Esta opción no se admite cuando se usa *$search*.</span><span class="sxs-lookup"><span data-stu-id="f05c4-p106">Skip the first n results, useful for paging. This is not supported when using *$search*.</span></span>| 
|<span data-ttu-id="f05c4-141">$top</span><span class="sxs-lookup"><span data-stu-id="f05c4-141">$top</span></span>|<span data-ttu-id="f05c4-142">int</span><span class="sxs-lookup"><span data-stu-id="f05c4-142">int</span></span>|<span data-ttu-id="f05c4-143">Número de resultados que se van a devolver.</span><span class="sxs-lookup"><span data-stu-id="f05c4-143">Number of results to be returned.</span></span>| 

## <a name="request-headers"></a><span data-ttu-id="f05c4-144">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f05c4-144">Request headers</span></span>
| <span data-ttu-id="f05c4-145">Nombre</span><span class="sxs-lookup"><span data-stu-id="f05c4-145">Name</span></span>      |<span data-ttu-id="f05c4-146">Descripción</span><span class="sxs-lookup"><span data-stu-id="f05c4-146">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="f05c4-147">Authorization</span><span class="sxs-lookup"><span data-stu-id="f05c4-147">Authorization</span></span>  | <span data-ttu-id="f05c4-p107">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="f05c4-p107">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="f05c4-150">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f05c4-150">Request body</span></span>
<span data-ttu-id="f05c4-151">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="f05c4-151">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="f05c4-152">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f05c4-152">Response</span></span>
<span data-ttu-id="f05c4-153">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [person](../resources/person.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f05c4-153">If successful, this method returns a `200 OK` response code and a [ListItemVersion](../resources/person.md) object in the response body.</span></span>

## <a name="examples"></a><span data-ttu-id="f05c4-154">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="f05c4-154">Examples</span></span>
#### <a name="request-1"></a><span data-ttu-id="f05c4-155">Solicitud 1</span><span class="sxs-lookup"><span data-stu-id="f05c4-155">Request 1</span></span>
<span data-ttu-id="f05c4-156">El siguiente es un ejemplo de la solicitud que obtiene el usuario que tiene este identificador en la organización del usuario.</span><span class="sxs-lookup"><span data-stu-id="f05c4-156">The following is an example of the request that gets the person who has this ID in the user's organization.</span></span> 

<!-- {
  "blockType": "request",
  "name": "get_person_by_id"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/people/e3d0513b-449e-4198-ba6f-bd97ae7cae85
```

#### <a name="response-1"></a><span data-ttu-id="f05c4-157">Respuesta 1</span><span class="sxs-lookup"><span data-stu-id="f05c4-157">Response 1</span></span>
<span data-ttu-id="f05c4-158">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f05c4-158">Here is an example of the response.</span></span>

><span data-ttu-id="f05c4-159">**Nota:** Se puede reducir el objeto de respuesta que se muestra aquí para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="f05c4-159">**Note:** The response object shown here might be shortened for readability.</span></span> <span data-ttu-id="f05c4-160">Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="f05c4-160">All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "name": "get_person_by_id",
  "truncated": true,
  "@odata.type": "microsoft.graph.person"
} -->

```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 629

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
```

#### <a name="request-2"></a><span data-ttu-id="f05c4-161">Solicitud 2</span><span class="sxs-lookup"><span data-stu-id="f05c4-161">Request 2</span></span>
<span data-ttu-id="f05c4-162">El siguiente es un ejemplo de la solicitud que obtiene la persona que tenga este identificador en la organización del usuario y restringe la respuesta a las propiedades seleccionadas.</span><span class="sxs-lookup"><span data-stu-id="f05c4-162">The following is an example of the request that gets the person who has this ID in the user's organization and restricts the response to the selected properties.</span></span>

<!-- {
  "blockType": "request",
  "name": "get_person_by_id_with_select"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/people/e3d0513b-449e-4198-ba6f-bd97ae7cae85?$select=displayName
```
#### <a name="response-2"></a><span data-ttu-id="f05c4-163">Respuesta 2</span><span class="sxs-lookup"><span data-stu-id="f05c4-163">Response 2</span></span>
<span data-ttu-id="f05c4-164">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f05c4-164">Here is an example of the response.</span></span>

><span data-ttu-id="f05c4-165">**Nota:** Se puede reducir el objeto de respuesta que se muestra aquí para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="f05c4-165">**Note:** The response object shown here might be shortened for readability.</span></span> <span data-ttu-id="f05c4-166">Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="f05c4-166">All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "name": "get_person_by_id_with_select",
  "truncated": true,
  "@odata.type": "microsoft.graph.person"
} -->

```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 305

{
  "id": "e3d0513b-449e-4198-ba6f-bd97ae7cae85",
  "displayName": "Isaiah Langer"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get person",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
