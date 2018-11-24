# <a name="create-educationuser"></a><span data-ttu-id="8ac8c-101">Crear educationUser</span><span class="sxs-lookup"><span data-stu-id="8ac8c-101">Create educationUser</span></span>

<span data-ttu-id="8ac8c-102">Cree otro usuario.</span><span class="sxs-lookup"><span data-stu-id="8ac8c-102">Create a new user.</span></span>

<!-- Add some additional text to better distinguish this method from the user_post_users (https://developer.microsoft.com/graph/docs/api-reference/v1.0/api/user_post_users) topic. -->

## <a name="permissions"></a><span data-ttu-id="8ac8c-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="8ac8c-103">Permissions</span></span>
<span data-ttu-id="8ac8c-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="8ac8c-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="8ac8c-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="8ac8c-106">Permission type</span></span>      | <span data-ttu-id="8ac8c-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="8ac8c-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="8ac8c-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="8ac8c-108">Delegated (work or school account)</span></span> |  <span data-ttu-id="8ac8c-109">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8ac8c-109">Not supported.</span></span>  |
|<span data-ttu-id="8ac8c-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="8ac8c-110">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="8ac8c-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8ac8c-111">Not supported.</span></span>  |
|<span data-ttu-id="8ac8c-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="8ac8c-112">Application</span></span> | <span data-ttu-id="8ac8c-113">EduRoster.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="8ac8c-113">EduRoster.ReadWrite.All</span></span> | 

## <a name="http-request"></a><span data-ttu-id="8ac8c-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="8ac8c-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /education/users
```
## <a name="request-headers"></a><span data-ttu-id="8ac8c-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="8ac8c-115">Request headers</span></span>
| <span data-ttu-id="8ac8c-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8ac8c-116">Header</span></span>       | <span data-ttu-id="8ac8c-117">Valor</span><span class="sxs-lookup"><span data-stu-id="8ac8c-117">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="8ac8c-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="8ac8c-118">Authorization</span></span>  | <span data-ttu-id="8ac8c-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="8ac8c-p102">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="8ac8c-121">Content-Type</span><span class="sxs-lookup"><span data-stu-id="8ac8c-121">Content-Type</span></span>  | <span data-ttu-id="8ac8c-122">application/json</span><span class="sxs-lookup"><span data-stu-id="8ac8c-122">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="8ac8c-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="8ac8c-123">Request body</span></span>
<span data-ttu-id="8ac8c-124">En el cuerpo de la solicitud, especifique una representación JSON de un objeto [educationUser](../resources/educationuser.md).</span><span class="sxs-lookup"><span data-stu-id="8ac8c-124">In the request body, supply a JSON representation of an [educationUser](../resources/educationuser.md) object.</span></span>


## <a name="response"></a><span data-ttu-id="8ac8c-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8ac8c-125">Response</span></span>
<span data-ttu-id="8ac8c-126">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [educationUser](../resources/educationuser.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8ac8c-126">If successful, this method returns a `201 Created` response code and an [educationUser](../resources/educationuser.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="8ac8c-127">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="8ac8c-127">Example</span></span>
##### <a name="request"></a><span data-ttu-id="8ac8c-128">Solicitud</span><span class="sxs-lookup"><span data-stu-id="8ac8c-128">Request</span></span>
<span data-ttu-id="8ac8c-129">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="8ac8c-129">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_educationuser_from_educationroot"
}-->
```http
POST https://graph.microsoft.com/v1.0/education/users
Content-type: application/json
Content-length: 508

{
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
```

##### <a name="response"></a><span data-ttu-id="8ac8c-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8ac8c-130">Response</span></span>
<span data-ttu-id="8ac8c-131">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8ac8c-131">The following is an example of the response.</span></span> 

><span data-ttu-id="8ac8c-p103">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="8ac8c-p103">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.educationUser"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json
Content-length: 508

{
  "id": "13012",
  "displayName": "Dion Matheson",
  "givenName": "Dion",
  "middleName": " ",
  "surname": "Matheson",
  "mail": "DionM@contoso.com",
  "mobilePhone": "+1 (253) 555-0101",
  "createdBy": {
    "user": {
      "displayName": "Susana Rocha",
      "id": "14012",
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
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create educationUser",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->