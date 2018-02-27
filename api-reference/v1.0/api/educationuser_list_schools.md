# <a name="list-schools"></a><span data-ttu-id="7f0e4-101">Enumerar centros educativos</span><span class="sxs-lookup"><span data-stu-id="7f0e4-101">List schools</span></span>

<span data-ttu-id="7f0e4-102">Recupere una lista de centros educativos de un usuario.</span><span class="sxs-lookup"><span data-stu-id="7f0e4-102">Retrieve a list of licenseDetails objects for a user.</span></span>

><span data-ttu-id="7f0e4-103">**Nota:** Si se usa el token delegado, los miembros solo pueden ver información sobre sus propios centros educativos.</span><span class="sxs-lookup"><span data-stu-id="7f0e4-103">**Note:** If the delegated token is used, members can only see information about their own schools.</span></span> <span data-ttu-id="7f0e4-104">Use el recurso `...beta/education/me/schools` en este caso.</span><span class="sxs-lookup"><span data-stu-id="7f0e4-104">Use the `...beta/education/me/schools` resource in this case.</span></span>

## <a name="permissions"></a><span data-ttu-id="7f0e4-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="7f0e4-105">Permissions</span></span>
<span data-ttu-id="7f0e4-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="7f0e4-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="7f0e4-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="7f0e4-108">Permission type</span></span>      | <span data-ttu-id="7f0e4-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="7f0e4-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="7f0e4-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="7f0e4-110">Delegated (work or school account)</span></span> |  <span data-ttu-id="7f0e4-111">EduRoster.ReadBasic</span><span class="sxs-lookup"><span data-stu-id="7f0e4-111">EduRoster.ReadBasic</span></span>  |
|<span data-ttu-id="7f0e4-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="7f0e4-112">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="7f0e4-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="7f0e4-113">Not supported.</span></span>  |
|<span data-ttu-id="7f0e4-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="7f0e4-114">Application</span></span> | <span data-ttu-id="7f0e4-115">EduRoster.Read.All, EduRoster.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="7f0e4-115">EduRoster.Read.All, EduRoster.ReadWrite.All</span></span> | 

## <a name="http-request"></a><span data-ttu-id="7f0e4-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="7f0e4-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /education/me/schools
GET /education/users/{id}/schools
```
## <a name="optional-query-parameters"></a><span data-ttu-id="7f0e4-117">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="7f0e4-117">Optional query parameters</span></span>
<span data-ttu-id="7f0e4-118">Este método admite los [parámetros de consulta de OData](http://graph.microsoft.io/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7f0e4-118">This method supports the [OData Query Parameters](http://graph.microsoft.io/docs/overview/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="7f0e4-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="7f0e4-119">Request headers</span></span>
| <span data-ttu-id="7f0e4-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7f0e4-120">Header</span></span>       | <span data-ttu-id="7f0e4-121">Valor</span><span class="sxs-lookup"><span data-stu-id="7f0e4-121">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="7f0e4-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="7f0e4-122">Authorization</span></span>  | <span data-ttu-id="7f0e4-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="7f0e4-p103">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="7f0e4-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="7f0e4-125">Request body</span></span>
<span data-ttu-id="7f0e4-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="7f0e4-126">Do not supply a request body for this method.</span></span>
## <a name="response"></a><span data-ttu-id="7f0e4-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7f0e4-127">Response</span></span>
<span data-ttu-id="7f0e4-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [educationSchool](../resources/educationschool.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7f0e4-128">If successful, this method returns a `200 OK` response code and collection of [groupSettingTemplate](../resources/educationschool.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="7f0e4-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7f0e4-129">Example</span></span>
##### <a name="request"></a><span data-ttu-id="7f0e4-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="7f0e4-130">Request</span></span>
<span data-ttu-id="7f0e4-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="7f0e4-131">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_schools"
}-->
```http
GET https://graph.microsoft.com/v1.0/education/me/schools
```
##### <a name="response"></a><span data-ttu-id="7f0e4-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7f0e4-132">Response</span></span>
<span data-ttu-id="7f0e4-133">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7f0e4-133">The following is an example of the response.</span></span> 

><span data-ttu-id="7f0e4-p104">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="7f0e4-p104">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.educationSchool",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 345

{
  "value": [
    {
      "id": "10001",
      "displayName": "Contoso High School",
      "description": "Public 9-12 high school",
      "status": "active",
      "externalSource": "sis",
      "principalEmail": "amyr@contoso.com",
      "principalName": "Amy Roebuck",
      "externalPrincipalId": "14007",
      "highestGrade": "12",
      "lowestGrade": "9",
      "schoolNumber": "10001",
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
      "externalId": "10001",
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