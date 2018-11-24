# <a name="list-schools"></a><span data-ttu-id="1e7a8-101">Enumerar centros educativos</span><span class="sxs-lookup"><span data-stu-id="1e7a8-101">List schools</span></span>

<span data-ttu-id="1e7a8-102">Recupere una lista de los centros educativos en los que se imparte la clase.</span><span class="sxs-lookup"><span data-stu-id="1e7a8-102">Retrieve a list of schools in which the class is taught.</span></span>

## <a name="permissions"></a><span data-ttu-id="1e7a8-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="1e7a8-103">Permissions</span></span>
<span data-ttu-id="1e7a8-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="1e7a8-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="1e7a8-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="1e7a8-106">Permission type</span></span>      | <span data-ttu-id="1e7a8-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="1e7a8-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="1e7a8-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="1e7a8-108">Delegated (work or school account)</span></span> |  <span data-ttu-id="1e7a8-109">EduRoster.ReadBasic</span><span class="sxs-lookup"><span data-stu-id="1e7a8-109">EduRoster.ReadBasic</span></span>  |
|<span data-ttu-id="1e7a8-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="1e7a8-110">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="1e7a8-111">No admitido</span><span class="sxs-lookup"><span data-stu-id="1e7a8-111">Not supported</span></span>  |
|<span data-ttu-id="1e7a8-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="1e7a8-112">Application</span></span> | <span data-ttu-id="1e7a8-113">EduRoster.Read.All, EduRoster.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="1e7a8-113">EduRoster.Read.All, EduRoster.ReadWrite.All</span></span> | 

## <a name="http-request"></a><span data-ttu-id="1e7a8-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="1e7a8-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /education/classes/{id}/schools
```
## <a name="optional-query-parameters"></a><span data-ttu-id="1e7a8-115">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="1e7a8-115">Optional query parameters</span></span>
<span data-ttu-id="1e7a8-116">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1e7a8-116">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="1e7a8-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="1e7a8-117">Request headers</span></span>
| <span data-ttu-id="1e7a8-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1e7a8-118">Header</span></span>       | <span data-ttu-id="1e7a8-119">Valor</span><span class="sxs-lookup"><span data-stu-id="1e7a8-119">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="1e7a8-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="1e7a8-120">Authorization</span></span>  | <span data-ttu-id="1e7a8-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="1e7a8-p102">Bearer {token}. Required.</span></span>  |


## <a name="request-body"></a><span data-ttu-id="1e7a8-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="1e7a8-123">Request body</span></span>
<span data-ttu-id="1e7a8-124">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="1e7a8-124">Do not supply a request body for this method.</span></span>
## <a name="response"></a><span data-ttu-id="1e7a8-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1e7a8-125">Response</span></span>
<span data-ttu-id="1e7a8-126">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [educationSchool](../resources/educationschool.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1e7a8-126">If successful, this method returns a `200 OK` response code and a collection of [educationSchool](../resources/educationschool.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="1e7a8-127">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1e7a8-127">Example</span></span>
##### <a name="request"></a><span data-ttu-id="1e7a8-128">Solicitud</span><span class="sxs-lookup"><span data-stu-id="1e7a8-128">Request</span></span>
<span data-ttu-id="1e7a8-129">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="1e7a8-129">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_schools"
}-->
```http
GET https://graph.microsoft.com/v1.0/education/classes/{class-id}/schools
```
##### <a name="response"></a><span data-ttu-id="1e7a8-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1e7a8-130">Response</span></span>
<span data-ttu-id="1e7a8-131">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1e7a8-131">The following is an example of the response.</span></span> 

><span data-ttu-id="1e7a8-p103">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="1e7a8-p103">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.educationSchool",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 892

{
  "value": [
    {
      "id": "10002",
      "displayName": "Fabrikam High School",
      "description": "Magnate school for the arts. Los Angeles School District",
      "status": "String",
      "externalSource": "String",
      "principalEmail": "AmyR@fabrikam.com",
      "principalName": "Amy Roebuck",
      "externalPrincipalId": "14007",
      "highestGrade": "12",
      "lowestGrade": "9",
      "schoolNumber": "10002",
      "address": {
        "city": "Los Angeles",
        "countryOrRegion": "United States",
        "postalCode": "98055",
        "state": "CA",
        "street": "12345 Main St."
      },
      "createdBy": {
        "user": {
          "displayName": "Susana Rocha",
          "id": "14012",
        }
      },
      "externalId": "10002",
      "fax": "+1 (253) 555-0101",
      "phone": "+1 (253) 555-0102",
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List schools",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
