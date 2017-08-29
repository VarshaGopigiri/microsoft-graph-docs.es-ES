# <a name="get-person"></a><span data-ttu-id="54091-101">Get person</span><span class="sxs-lookup"><span data-stu-id="54091-101">Get person</span></span>

<span data-ttu-id="54091-102">Recupere las propiedades y las relaciones del objeto [person](../resources/person.md).</span><span class="sxs-lookup"><span data-stu-id="54091-102">Retrieve the properties and relationships of [plannertaskdetails](../resources/person.md) object.</span></span>

<span data-ttu-id="54091-p101">Puede obtener esta información a través de la API de contactos. Para obtener ejemplos, vea la sección [Ejemplos](#examples) y el artículo sobre cómo [Obtener información relevante sobre los contactos](../../../concepts/people_example.md).</span><span class="sxs-lookup"><span data-stu-id="54091-p101">You can get this information via the People API. For examples, see the [Examples](#examples) section and the article [Get relevant information about people](../../../concepts/people_example.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="54091-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="54091-105">Permissions</span></span>
<span data-ttu-id="54091-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="54091-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>
 

|<span data-ttu-id="54091-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="54091-108">Permission type</span></span>      | <span data-ttu-id="54091-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="54091-109">Permissions (from least to most privileged)</span></span>              | 
|:--------------------|:---------------------------------------------------------| 
|<span data-ttu-id="54091-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="54091-110">Delegated (work or school account)</span></span> | <span data-ttu-id="54091-111">People.Read, People.Read.All</span><span class="sxs-lookup"><span data-stu-id="54091-111">People.Read, People.Read.All</span></span>    | 
|<span data-ttu-id="54091-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="54091-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="54091-113">People.Read</span><span class="sxs-lookup"><span data-stu-id="54091-113">People.Read</span></span>    | 
|<span data-ttu-id="54091-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="54091-114">Application</span></span> | <span data-ttu-id="54091-115">People.Read.All</span><span class="sxs-lookup"><span data-stu-id="54091-115">People.Read.All</span></span> | 

## <a name="http-request"></a><span data-ttu-id="54091-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="54091-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->

```http
GET /me/people/?$search='{property_value}'
GET /me/people/?$filter={person_property} eq '{property_value}'
```

## <a name="optional-query-parameters"></a><span data-ttu-id="54091-117">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="54091-117">Optional query parameters</span></span>
|<span data-ttu-id="54091-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="54091-118">Name</span></span>|<span data-ttu-id="54091-119">Valor</span><span class="sxs-lookup"><span data-stu-id="54091-119">Value</span></span>|<span data-ttu-id="54091-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="54091-120">Description</span></span>|
|:---------------|:--------|:-------|
|<span data-ttu-id="54091-121">$filter</span><span class="sxs-lookup"><span data-stu-id="54091-121">$filter</span></span>|<span data-ttu-id="54091-122">string</span><span class="sxs-lookup"><span data-stu-id="54091-122">string</span></span>|<span data-ttu-id="54091-123">Limita la respuesta a solo los contactos cuyo registro contiene los criterios especificados.</span><span class="sxs-lookup"><span data-stu-id="54091-123">Limits the response to only those people whose record contains the specified criteria.</span></span>|
|<span data-ttu-id="54091-124">$orderby</span><span class="sxs-lookup"><span data-stu-id="54091-124">$orderby</span></span>|<span data-ttu-id="54091-125">string</span><span class="sxs-lookup"><span data-stu-id="54091-125">string</span></span>|<span data-ttu-id="54091-p103">De manera predeterminada, los contactos de la respuesta se ordenan por su relevancia para la consulta. Puede cambiar el orden de los contactos en la respuesta con el parámetro *$orderby*.</span><span class="sxs-lookup"><span data-stu-id="54091-p103">By default, the people in the response are sorted by their relevance to your query. You can change the order of the people in the response using the *$orderby* parameter.</span></span>|
|<span data-ttu-id="54091-128">$search</span><span class="sxs-lookup"><span data-stu-id="54091-128">$search</span></span>|<span data-ttu-id="54091-129">string</span><span class="sxs-lookup"><span data-stu-id="54091-129">string</span></span>|<span data-ttu-id="54091-p104">Se buscan contactos por nombre o alias. Admite coincidencia aproximada.</span><span class="sxs-lookup"><span data-stu-id="54091-p104">Search for people by name or alias. Supports fuzzy matching.</span></span>|
|<span data-ttu-id="54091-132">$select</span><span class="sxs-lookup"><span data-stu-id="54091-132">$select</span></span>|<span data-ttu-id="54091-133">string</span><span class="sxs-lookup"><span data-stu-id="54091-133">string</span></span>|<span data-ttu-id="54091-p105">Lista separada por comas de las propiedades que se van a incluir en la respuesta. Para un rendimiento óptimo, seleccione solo el subconjunto de propiedades necesarias.</span><span class="sxs-lookup"><span data-stu-id="54091-p105">Comma-separated list of properties to include in the response. For optimal performance, only select the subset of properties needed.</span></span>|
|<span data-ttu-id="54091-136">$skip</span><span class="sxs-lookup"><span data-stu-id="54091-136">$skip</span></span>|<span data-ttu-id="54091-137">int</span><span class="sxs-lookup"><span data-stu-id="54091-137">int</span></span>|<span data-ttu-id="54091-p106">Se omiten los primeros resultados n, útil para la paginación. Esta opción no se admite cuando se usa *$search*.</span><span class="sxs-lookup"><span data-stu-id="54091-p106">Skip the first n results, useful for paging. This is not supported when using *$search*.</span></span>|
|<span data-ttu-id="54091-140">$top</span><span class="sxs-lookup"><span data-stu-id="54091-140">$top</span></span>|<span data-ttu-id="54091-141">int</span><span class="sxs-lookup"><span data-stu-id="54091-141">int</span></span>|<span data-ttu-id="54091-142">Número de resultados que se van a devolver.</span><span class="sxs-lookup"><span data-stu-id="54091-142">Number of results to be returned.</span></span>|

## <a name="parameters"></a><span data-ttu-id="54091-143">Parámetros</span><span class="sxs-lookup"><span data-stu-id="54091-143">Parameters</span></span>
| <span data-ttu-id="54091-144">Parámetro</span><span class="sxs-lookup"><span data-stu-id="54091-144">Parameter</span></span> |<span data-ttu-id="54091-145">Tipo</span><span class="sxs-lookup"><span data-stu-id="54091-145">Type</span></span>       |<span data-ttu-id="54091-146">Descripción</span><span class="sxs-lookup"><span data-stu-id="54091-146">Description</span></span>|
|:----------|:----------|:----------|
|<span data-ttu-id="54091-147">property_value</span><span class="sxs-lookup"><span data-stu-id="54091-147">property_value</span></span>|<span data-ttu-id="54091-148">Cadena</span><span class="sxs-lookup"><span data-stu-id="54091-148">String</span></span>     |<span data-ttu-id="54091-p107">El valor de la propiedad extendida que debe coincidir. Es necesario cuando aparece en la sección de la **solicitud HTTP**.</span><span class="sxs-lookup"><span data-stu-id="54091-p107">The value of the extended property to match. Required where listed in the **HTTP request** section above.</span></span>|
|<span data-ttu-id="54091-151">person_property</span><span class="sxs-lookup"><span data-stu-id="54091-151">person_property</span></span>|<span data-ttu-id="54091-152">String</span><span class="sxs-lookup"><span data-stu-id="54091-152">String</span></span>    |<span data-ttu-id="54091-p108">La propiedad person que debe coincidir. Es necesario cuando aparece en la sección de la **solicitud HTTP**.</span><span class="sxs-lookup"><span data-stu-id="54091-p108">The value of the extended property to match. Required where listed in the **HTTP request** section above.</span></span>|

## <a name="request-headers"></a><span data-ttu-id="54091-155">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="54091-155">Request headers</span></span>
| <span data-ttu-id="54091-156">Nombre</span><span class="sxs-lookup"><span data-stu-id="54091-156">Name</span></span>      |<span data-ttu-id="54091-157">Descripción</span><span class="sxs-lookup"><span data-stu-id="54091-157">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="54091-158">Authorization</span><span class="sxs-lookup"><span data-stu-id="54091-158">Authorization</span></span>  | <span data-ttu-id="54091-p109">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="54091-p109">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="54091-161">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="54091-161">Request body</span></span>
<span data-ttu-id="54091-162">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="54091-162">Do not supply a request body for this method.</span></span>
## <a name="response"></a><span data-ttu-id="54091-163">Respuesta</span><span class="sxs-lookup"><span data-stu-id="54091-163">Response</span></span>
<span data-ttu-id="54091-p110">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [person](../resources/person.md) en el cuerpo de la respuesta. La respuesta puede contener una instancia person o una colección de instancias person.</span><span class="sxs-lookup"><span data-stu-id="54091-p110">If successful, this method returns a `200 OK` response code and a [person](../resources/person.md) object in the response body. The response can contain one person instance or a collection of person instances.</span></span> 
## <a name="examples"></a><span data-ttu-id="54091-166">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="54091-166">Examples</span></span>
### <a name="perform-a-search"></a><span data-ttu-id="54091-167">Realizar una búsqueda</span><span class="sxs-lookup"><span data-stu-id="54091-167">Perform a search for Reseller entity instances.</span></span> 
<span data-ttu-id="54091-168">La siguiente solicitud realiza una búsqueda de un contacto llamado Irene McGowan.</span><span class="sxs-lookup"><span data-stu-id="54091-168">The following request does a search for a person named Irene McGowan.</span></span> 

<!-- {
  "blockType": "request",
  "name": "get_person"
}-->

```http
GET https://graph.microsoft.com/v1.0/me/people/?$search="Irene McGowan"
```

<span data-ttu-id="54091-169">En el ejemplo siguiente se muestra la respuesta.</span><span class="sxs-lookup"><span data-stu-id="54091-169">The following example shows the formula bar</span></span> 

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.person"
} -->

```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "value": [
       {
           "id": "C0BD1BA1-A84E-4796-9C65-F8A0293741D1",
           "displayName": "Irene McGowan",
           "givenName": "Irene",
           "surname": "McGowan",
           "birthday": "",
           "personNotes": "",
           "isFavorite": false,
           "jobTitle": "Auditor",
           "companyName": null,
           "yomiCompany": "",
           "department": "Finance",
           "officeLocation": "12/1110",
           "profession": "",
           "userPrincipalName": "irenem@contoso.onmicrosoft.com",
           "imAddress": "sip:irenem@contoso.onmicrosoft.com",
           "scoredEmailAddresses": [
               {
                   "address": "irenem@contoso.onmicrosoft.com",
                   "relevanceScore": -16.446060612802224
               }
           ],
           "phones": [
               {
                   "type": "Business",
                   "number": "+1 412 555 0109"
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
### <a name="select-the-fields-to-return-in-a-filtered-response"></a><span data-ttu-id="54091-170">Seleccionar los campos que se van a devolver en una respuesta filtrada</span><span class="sxs-lookup"><span data-stu-id="54091-170">Select the fields to return in a filtered response</span></span> 
<span data-ttu-id="54091-171">Puede combinar los parámetros *$select* y *$filter* para crear una lista personalizada de contactos relevantes para el usuario y obtener solo los campos que la aplicación necesita.</span><span class="sxs-lookup"><span data-stu-id="54091-171">You can combine the *$select* and *$filter* parameters to create a custom list of people relevant to the user and get only the fields that your application needs.</span></span> 

<span data-ttu-id="54091-p111">En el ejemplo siguiente se obtiene el **displayName** y el **scoredEmailAddresses** de los contactos cuyo nombre para mostrar es igual al nombre especificado. En este ejemplo, solo se devuelven los contactos cuyo nombre para mostrar es igual a "Lorrie Frye".</span><span class="sxs-lookup"><span data-stu-id="54091-p111">The following example gets the **displayName** and **scoredEmailAddresses** of people whose display name equals the specified name. In this example, only people whose display name equals "Lorrie Frye" are returned.</span></span> 

<!-- {
  "blockType": "request",
  "name": "get_person"
}-->

```http
GET https://graph.microsoft.com/v1.0/me/people/?$select=displayName,scoredEmailAddresses&$filter=displayName eq 'Lorrie Frye'
```

<span data-ttu-id="54091-174">En el ejemplo siguiente se muestra la respuesta.</span><span class="sxs-lookup"><span data-stu-id="54091-174">The following example shows the formula bar</span></span> 

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.person"
} -->

```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "value": [
        {
            "id": "8CE6E1DE-CB84-4BF5-971D-D3ECF452E2B5",
            "displayName": "Lorrie Frye",
            "scoredEmailAddresses": [
                {
                    "address": "Lorrief@contoso.onmicrosoft.com",
                    "relevanceScore": 8
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
  "description": "Get person",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
