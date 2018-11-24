# <a name="list-educationclasses"></a><span data-ttu-id="8e4ba-101">Enumerar educationClasses</span><span class="sxs-lookup"><span data-stu-id="8e4ba-101">List educationClasses</span></span>

<span data-ttu-id="8e4ba-102">Recupere una lista de las clases de un centro educativo.</span><span class="sxs-lookup"><span data-stu-id="8e4ba-102">Retrieve a list of classes owned by a school.</span></span>

## <a name="permissions"></a><span data-ttu-id="8e4ba-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="8e4ba-103">Permissions</span></span>
<span data-ttu-id="8e4ba-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="8e4ba-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="8e4ba-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="8e4ba-106">Permission type</span></span>      | <span data-ttu-id="8e4ba-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="8e4ba-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="8e4ba-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="8e4ba-108">Delegated (work or school account)</span></span> |  <span data-ttu-id="8e4ba-109">EduRoster.ReadBasic</span><span class="sxs-lookup"><span data-stu-id="8e4ba-109">EduRoster.ReadBasic</span></span>  |
|<span data-ttu-id="8e4ba-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="8e4ba-110">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="8e4ba-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8e4ba-111">Not supported.</span></span>  |
|<span data-ttu-id="8e4ba-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="8e4ba-112">Application</span></span> | <span data-ttu-id="8e4ba-113">EduRoster.Read.All, EduRoster.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="8e4ba-113">EduRoster.Read.All, EduRoster.ReadWrite.All</span></span> | 

## <a name="http-request"></a><span data-ttu-id="8e4ba-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="8e4ba-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /education/schools/{id}/classes
```
## <a name="optional-query-parameters"></a><span data-ttu-id="8e4ba-115">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="8e4ba-115">Optional query parameters</span></span>
<span data-ttu-id="8e4ba-116">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8e4ba-116">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="8e4ba-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="8e4ba-117">Request headers</span></span>
| <span data-ttu-id="8e4ba-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8e4ba-118">Header</span></span>       | <span data-ttu-id="8e4ba-119">Valor</span><span class="sxs-lookup"><span data-stu-id="8e4ba-119">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="8e4ba-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="8e4ba-120">Authorization</span></span>  | <span data-ttu-id="8e4ba-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="8e4ba-p102">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="8e4ba-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="8e4ba-123">Request body</span></span>
<span data-ttu-id="8e4ba-124">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="8e4ba-124">Do not supply a request body for this method.</span></span>
## <a name="response"></a><span data-ttu-id="8e4ba-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8e4ba-125">Response</span></span>
<span data-ttu-id="8e4ba-126">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [educationClass](../resources/educationclass.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8e4ba-126">If successful, this method returns a `200 OK` response code and a collection of [educationClass](../resources/educationclass.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="8e4ba-127">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="8e4ba-127">Example</span></span>
##### <a name="request"></a><span data-ttu-id="8e4ba-128">Solicitud</span><span class="sxs-lookup"><span data-stu-id="8e4ba-128">Request</span></span>
<span data-ttu-id="8e4ba-129">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="8e4ba-129">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_classes"
}-->
```http
GET https://graph.microsoft.com/v1.0/education/schools/{school-id}/classes
```
##### <a name="response"></a><span data-ttu-id="8e4ba-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8e4ba-130">Response</span></span>
<span data-ttu-id="8e4ba-131">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8e4ba-131">The following is an example of the response.</span></span> 

><span data-ttu-id="8e4ba-p103">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="8e4ba-p103">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

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
