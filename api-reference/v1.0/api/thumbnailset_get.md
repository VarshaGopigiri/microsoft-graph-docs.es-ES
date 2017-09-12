# <a name="get-thumbnailset"></a><span data-ttu-id="73c68-101">Get thumbnailSet</span><span class="sxs-lookup"><span data-stu-id="73c68-101">Get thumbnailSet</span></span>

<span data-ttu-id="73c68-102">Recupera las propiedades y relaciones de un objeto [thumbnailSet](../resources/thumbnailset.md).</span><span class="sxs-lookup"><span data-stu-id="73c68-102">Retrieve the properties and relationships of a [thumbnailSet](../resources/thumbnailset.md) object.</span></span>

<span data-ttu-id="73c68-103">Para más información, vea [List thumbnails](item_list_thumbnails.md) (Enumerar miniaturas).</span><span class="sxs-lookup"><span data-stu-id="73c68-103">For more info, see [List thumbnails](item_list_thumbnails.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="73c68-104">Permisos</span><span class="sxs-lookup"><span data-stu-id="73c68-104">Permissions</span></span>
<span data-ttu-id="73c68-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="73c68-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="73c68-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="73c68-107">Permission type</span></span>      | <span data-ttu-id="73c68-108">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="73c68-108">Permissions (from least to most privileged)</span></span>              | 
|:--------------------|:---------------------------------------------------------| 
|<span data-ttu-id="73c68-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="73c68-109">Delegated (work or school account)</span></span> | <span data-ttu-id="73c68-110">Files.Read</span><span class="sxs-lookup"><span data-stu-id="73c68-110">Files.Read</span></span>    | 
|<span data-ttu-id="73c68-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="73c68-111">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="73c68-112">Files.Read</span><span class="sxs-lookup"><span data-stu-id="73c68-112">Files.Read</span></span>    | 
|<span data-ttu-id="73c68-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="73c68-113">Application</span></span> | <span data-ttu-id="73c68-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="73c68-114">Not supported.</span></span> | 

## <a name="http-request"></a><span data-ttu-id="73c68-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="73c68-115">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /drive/root/thumbnails/{id}
GET /drive/items/{id}/thumbnails/{id}
GET /drives/{id}/root/thumbnails/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="73c68-116">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="73c68-116">Optional query parameters</span></span>
<span data-ttu-id="73c68-117">Este método admite los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="73c68-117">This method supports the [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="73c68-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="73c68-118">Request headers</span></span>
| <span data-ttu-id="73c68-119">Nombre</span><span class="sxs-lookup"><span data-stu-id="73c68-119">Name</span></span>       | <span data-ttu-id="73c68-120">Tipo</span><span class="sxs-lookup"><span data-stu-id="73c68-120">Type</span></span> | <span data-ttu-id="73c68-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="73c68-121">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="73c68-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="73c68-122">Authorization</span></span>  | <span data-ttu-id="73c68-123">string</span><span class="sxs-lookup"><span data-stu-id="73c68-123">string</span></span>  | <span data-ttu-id="73c68-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="73c68-p102">Bearer {token}. Required.</span></span> |


## <a name="request-body"></a><span data-ttu-id="73c68-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="73c68-126">Request body</span></span>
<span data-ttu-id="73c68-127">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="73c68-127">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="73c68-128">Respuesta</span><span class="sxs-lookup"><span data-stu-id="73c68-128">Response</span></span>

<span data-ttu-id="73c68-129">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [thumbnailSet](../resources/thumbnailset.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="73c68-129">If successful, this method returns a `200 OK` response code and [thumbnailSet](../resources/thumbnailset.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="73c68-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="73c68-130">Example</span></span>
##### <a name="request"></a><span data-ttu-id="73c68-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="73c68-131">Request</span></span>
<span data-ttu-id="73c68-132">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="73c68-132">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_thumbnailset"
}-->
```http
GET https://graph.microsoft.com/v1.0/drive/root/thumbnails/{id}
```
##### <a name="response"></a><span data-ttu-id="73c68-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="73c68-133">Response</span></span>
<span data-ttu-id="73c68-134">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="73c68-134">Here is an example of the response.</span></span>
<!-- {
  "blockType": "response",
  "truncated": false,
  "@odata.type": "microsoft.graph.thumbnailSet"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 456

{
  "id": "id-value",
  "large": {
    "height": 99,
    "url": "url-value",
    "width": 99
  },
  "medium": {
    "height": 99,
    "url": "url-value",
    "width": 99
  },
  "small": {
    "height": 99,
    "url": "url-value",
    "width": 99
  },
  "source": {
    "height": 99,
    "url": "url-value",
    "width": 99
  }
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get thumbnailSet",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
