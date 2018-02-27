# <a name="list-classes"></a><span data-ttu-id="6c808-101">Enumerar clases</span><span class="sxs-lookup"><span data-stu-id="6c808-101">List classes</span></span>

<span data-ttu-id="6c808-102">Recupere una lista de los objetos de clase.</span><span class="sxs-lookup"><span data-stu-id="6c808-102">Retrieve a list of chartpoints objects.</span></span> <span data-ttu-id="6c808-103">Tenga en cuenta que si se usa el token delegado, los miembros solo pueden ver información sobre sus propias clases.</span><span class="sxs-lookup"><span data-stu-id="6c808-103">Note that if the delegated token is used, members can only see information about their own classes.</span></span> 

<!-- Please verify the revision to the delegated token text. -->

## <a name="permissions"></a><span data-ttu-id="6c808-104">Permisos</span><span class="sxs-lookup"><span data-stu-id="6c808-104">Permissions</span></span>
<span data-ttu-id="6c808-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="6c808-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="6c808-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="6c808-107">Permission type</span></span>      | <span data-ttu-id="6c808-108">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="6c808-108">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="6c808-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="6c808-109">Delegated (work or school account)</span></span> |  <span data-ttu-id="6c808-110">EduRoster.ReadBasic</span><span class="sxs-lookup"><span data-stu-id="6c808-110">EduRoster.ReadBasic</span></span>  |
|<span data-ttu-id="6c808-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="6c808-111">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="6c808-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6c808-112">Not supported.</span></span>  |
|<span data-ttu-id="6c808-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="6c808-113">Application</span></span> | <span data-ttu-id="6c808-114">EduRoster.Read.All, EduRoster.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="6c808-114">EduRoster.Read.All, EduRoster.ReadWrite.All</span></span> | 

## <a name="http-request"></a><span data-ttu-id="6c808-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="6c808-115">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /education/me/classes
GET /education/users/{id}/classes
```
## <a name="optional-query-parameters"></a><span data-ttu-id="6c808-116">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="6c808-116">Optional query parameters</span></span>
<span data-ttu-id="6c808-117">Este método admite los [parámetros de consulta de OData](http://graph.microsoft.io/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6c808-117">This method supports the [OData Query Parameters](http://graph.microsoft.io/docs/overview/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="6c808-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="6c808-118">Request headers</span></span>
| <span data-ttu-id="6c808-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6c808-119">Header</span></span>       | <span data-ttu-id="6c808-120">Valor</span><span class="sxs-lookup"><span data-stu-id="6c808-120">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="6c808-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="6c808-121">Authorization</span></span>  | <span data-ttu-id="6c808-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="6c808-p103">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="6c808-124">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="6c808-124">Request body</span></span>
<span data-ttu-id="6c808-125">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="6c808-125">Do not supply a request body for this method.</span></span>
## <a name="response"></a><span data-ttu-id="6c808-126">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6c808-126">Response</span></span>
<span data-ttu-id="6c808-127">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [educationClass](../resources/educationclass.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6c808-127">If successful, this method returns a `200 OK` response code and collection of [groupSettingTemplate](../resources/educationclass.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="6c808-128">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6c808-128">Example</span></span>
##### <a name="request"></a><span data-ttu-id="6c808-129">Solicitud</span><span class="sxs-lookup"><span data-stu-id="6c808-129">Request</span></span>
<span data-ttu-id="6c808-130">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6c808-130">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_classes"
}-->
```http
GET https://graph.microsoft.com/v1.0/education/me/classes
```
##### <a name="response"></a><span data-ttu-id="6c808-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6c808-131">Response</span></span>
<span data-ttu-id="6c808-132">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6c808-132">The following is an example of the response.</span></span> 

><span data-ttu-id="6c808-p104">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="6c808-p104">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.educationClass",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 277

{
  "value": [
    {
      "id": "11019",
      "description": "Health Level 1",
      "classCode": "Health 501",
      "createdBy": {
        "user": {
          "displayName": "Susana Rocha",
          "id": "14012",
        }
      },
      "displayName": "Health 1",
      "externalId": "11019",
      "externalName": "Health Level 1",
      "externalSource": "sis",
      "mailNickname": "fineartschool.net"
    } 
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List classes",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->