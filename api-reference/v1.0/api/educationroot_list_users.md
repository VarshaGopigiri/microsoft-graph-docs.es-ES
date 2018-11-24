# <a name="list-users"></a><span data-ttu-id="9ac81-101">List users</span><span class="sxs-lookup"><span data-stu-id="9ac81-101">List users</span></span>

<span data-ttu-id="9ac81-102">Recupera una lista de objetos de usuario.</span><span class="sxs-lookup"><span data-stu-id="9ac81-102">Retrieve a list of user objects.</span></span> <span data-ttu-id="9ac81-103">Estos objetos de usuario incluirán propiedades específicas del ámbito educativo.</span><span class="sxs-lookup"><span data-stu-id="9ac81-103">These user objects will include education-specific properties.</span></span>

## <a name="permissions"></a><span data-ttu-id="9ac81-104">Permisos</span><span class="sxs-lookup"><span data-stu-id="9ac81-104">Permissions</span></span>
<span data-ttu-id="9ac81-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="9ac81-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="9ac81-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="9ac81-107">Permission type</span></span>      | <span data-ttu-id="9ac81-108">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="9ac81-108">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="9ac81-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="9ac81-109">Delegated (work or school account)</span></span> |  <span data-ttu-id="9ac81-110">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9ac81-110">Not supported.</span></span>  |
|<span data-ttu-id="9ac81-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="9ac81-111">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="9ac81-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9ac81-112">Not supported.</span></span>  |
|<span data-ttu-id="9ac81-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="9ac81-113">Application</span></span> | <span data-ttu-id="9ac81-114">EduRoster.Read.All, EduRoster.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="9ac81-114">EduRoster.Read.All, EduRoster.ReadWrite.All</span></span> | 

## <a name="http-request"></a><span data-ttu-id="9ac81-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="9ac81-115">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /education/users
```
## <a name="optional-query-parameters"></a><span data-ttu-id="9ac81-116">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="9ac81-116">Optional query parameters</span></span>
<span data-ttu-id="9ac81-117">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9ac81-117">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="9ac81-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="9ac81-118">Request headers</span></span>
| <span data-ttu-id="9ac81-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9ac81-119">Header</span></span>       | <span data-ttu-id="9ac81-120">Valor</span><span class="sxs-lookup"><span data-stu-id="9ac81-120">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="9ac81-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="9ac81-121">Authorization</span></span>  | <span data-ttu-id="9ac81-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="9ac81-p103">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="9ac81-124">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="9ac81-124">Request body</span></span>
<span data-ttu-id="9ac81-125">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="9ac81-125">Do not supply a request body for this method.</span></span>
## <a name="response"></a><span data-ttu-id="9ac81-126">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9ac81-126">Response</span></span>
<span data-ttu-id="9ac81-127">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [educationUser](../resources/educationuser.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9ac81-127">If successful, this method returns a `200 OK` response code and a collection of [educationUser](../resources/educationuser.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="9ac81-128">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9ac81-128">Example</span></span>
##### <a name="request"></a><span data-ttu-id="9ac81-129">Solicitud</span><span class="sxs-lookup"><span data-stu-id="9ac81-129">Request</span></span>
<span data-ttu-id="9ac81-130">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="9ac81-130">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_users"
}-->
```http
GET https://graph.microsoft.com/v1.0/education/users
```
##### <a name="response"></a><span data-ttu-id="9ac81-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9ac81-131">Response</span></span>
<span data-ttu-id="9ac81-132">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9ac81-132">The following is an example of the response.</span></span> 

><span data-ttu-id="9ac81-p104">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="9ac81-p104">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.educationUser",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 593

{
  "value": [
    {
      "id": "13012",
      "displayName": "Dion Matheson",
      "givenName": "Dion",
      "middleName": null,
      "surname": "Matheson",
      "mail": "DionM@contoso.com",
      "mobilePhone": "+1 (253) 555-0101",
      "createdBy": {
        "user": {
          "displayName": "Susana Rocha",
          "id": "14012"
        }
      },
      "externalSource": "sis",
      "mailingAddress": {
        "city": "Los Angeles",
        "countryOrRegion": "United States",
        "postalCode": "98055",
        "state": "CA",
        "street": "12345 Main St."
      },
      "primaryRole": "student",
      "residenceAddress": {
        "city": "Los Angeles",
        "countryOrRegion": "United States",
        "postalCode": "98055",
        "state": "CA",
        "street": "12345 Main St."
      }
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List users",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
