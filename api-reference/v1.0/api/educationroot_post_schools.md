# <a name="create-educationschool"></a><span data-ttu-id="4de16-101">Crear educationSchool</span><span class="sxs-lookup"><span data-stu-id="4de16-101">Create educationSchool</span></span>

<span data-ttu-id="4de16-102">Cree un centro educativo.</span><span class="sxs-lookup"><span data-stu-id="4de16-102">Create a school.</span></span>

## <a name="permissions"></a><span data-ttu-id="4de16-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="4de16-103">Permissions</span></span>
<span data-ttu-id="4de16-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="4de16-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="4de16-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="4de16-106">Permission type</span></span>      | <span data-ttu-id="4de16-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="4de16-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="4de16-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="4de16-108">Delegated (work or school account)</span></span> |  <span data-ttu-id="4de16-109">No admitida.</span><span class="sxs-lookup"><span data-stu-id="4de16-109">Not supported.</span></span>  |
|<span data-ttu-id="4de16-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="4de16-110">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="4de16-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="4de16-111">Not supported.</span></span>  |
|<span data-ttu-id="4de16-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="4de16-112">Application</span></span> | <span data-ttu-id="4de16-113">EduRoster.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="4de16-113">EduRoster.ReadWrite.All</span></span> | 

## <a name="http-request"></a><span data-ttu-id="4de16-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="4de16-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /education/schools
```
## <a name="request-headers"></a><span data-ttu-id="4de16-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="4de16-115">Request headers</span></span>
| <span data-ttu-id="4de16-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4de16-116">Header</span></span>       | <span data-ttu-id="4de16-117">Valor</span><span class="sxs-lookup"><span data-stu-id="4de16-117">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="4de16-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="4de16-118">Authorization</span></span>  | <span data-ttu-id="4de16-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="4de16-p102">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="4de16-121">Content-Type</span><span class="sxs-lookup"><span data-stu-id="4de16-121">Content-Type</span></span>  | <span data-ttu-id="4de16-122">application/json</span><span class="sxs-lookup"><span data-stu-id="4de16-122">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="4de16-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="4de16-123">Request body</span></span>
<span data-ttu-id="4de16-124">En el cuerpo de la solicitud, especifique una representación JSON de un objeto [educationSchool](../resources/educationschool.md).</span><span class="sxs-lookup"><span data-stu-id="4de16-124">In the request body, supply a JSON representation of an [invitation](../resources/educationschool.md) object.</span></span>


## <a name="response"></a><span data-ttu-id="4de16-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4de16-125">Response</span></span>
<span data-ttu-id="4de16-126">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [educationSchool](../resources/educationschool.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4de16-126">If successful, this method returns a `201 Created` response code and an [event](../resources/educationschool.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="4de16-127">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="4de16-127">Example</span></span>
##### <a name="request"></a><span data-ttu-id="4de16-128">Solicitud</span><span class="sxs-lookup"><span data-stu-id="4de16-128">Request</span></span>
<span data-ttu-id="4de16-129">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="4de16-129">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_educationschool_from_educationroot"
}-->
```http
POST https://graph.microsoft.com/v1.0/education/schools
Content-type: application/json
Content-length: 292

{
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
  "externalId": "10002",
  "fax": "+1 (253) 555-0101",
  "phone": "+1 (253) 555-0102",
}
```

##### <a name="response"></a><span data-ttu-id="4de16-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4de16-130">Response</span></span>
<span data-ttu-id="4de16-131">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4de16-131">The following is an example of the response.</span></span> 

><span data-ttu-id="4de16-p103">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="4de16-p103">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.educationSchool"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json
Content-length: 292

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
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create educationSchool",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->