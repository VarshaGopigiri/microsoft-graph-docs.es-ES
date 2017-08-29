# <a name="get-a-driveitem-resource"></a><span data-ttu-id="55ea1-101">Get a DriveItem resource</span><span class="sxs-lookup"><span data-stu-id="55ea1-101">Get a DriveItem resource</span></span>

<span data-ttu-id="55ea1-102">Recupera los metadatos de un [DriveItem](../resources/driveitem.md) en un [Drive](../resources/drive.md) a través del identificador o ruta de acceso del sistema.</span><span class="sxs-lookup"><span data-stu-id="55ea1-102">Retrieve the metadata for a [DriveItem](../resources/driveitem.md) in a [Drive](../resources/drive.md) by file system path or ID.</span></span>

## <a name="permissions"></a><span data-ttu-id="55ea1-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="55ea1-103">Permissions</span></span>
<span data-ttu-id="55ea1-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="55ea1-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="55ea1-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="55ea1-106">Permission type</span></span>      | <span data-ttu-id="55ea1-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="55ea1-107">Permissions (from least to most privileged)</span></span>              | 
|:--------------------|:---------------------------------------------------------| 
|<span data-ttu-id="55ea1-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="55ea1-108">Delegated (work or school account)</span></span> | <span data-ttu-id="55ea1-109">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="55ea1-109">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span></span>    | 
|<span data-ttu-id="55ea1-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="55ea1-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="55ea1-111">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="55ea1-111">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All</span></span>    | 
|<span data-ttu-id="55ea1-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="55ea1-112">Application</span></span> | <span data-ttu-id="55ea1-113">Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="55ea1-113">Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span></span> | 

## <a name="http-request"></a><span data-ttu-id="55ea1-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="55ea1-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/drive/items/{item-id}
GET /me/drive/root:/{item-path}
GET /drives/{drive-id}/items/{item-id}
GET /groups/{group-id}/drive/items/{item-id}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="55ea1-115">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="55ea1-115">Optional query parameters</span></span>
<span data-ttu-id="55ea1-116">Este método admite los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="55ea1-116">This method supports the [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="55ea1-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="55ea1-117">Request headers</span></span>

| <span data-ttu-id="55ea1-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="55ea1-118">Name</span></span>          | <span data-ttu-id="55ea1-119">Valor</span><span class="sxs-lookup"><span data-stu-id="55ea1-119">Value</span></span>  | <span data-ttu-id="55ea1-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="55ea1-120">Description</span></span>                                                                                                                                              |
|:--------------|:-------|:---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55ea1-121">if-none-match</span><span class="sxs-lookup"><span data-stu-id="55ea1-121">if-none-match</span></span> | <span data-ttu-id="55ea1-122">String</span><span class="sxs-lookup"><span data-stu-id="55ea1-122">String</span></span> | <span data-ttu-id="55ea1-123">Si se incluye el encabezado de la solicitud y la eTag (o cTag) proporcionada coincide con la etiqueta actual del archivo, se devuelve una respuesta `HTTP 304 Not Modified`.</span><span class="sxs-lookup"><span data-stu-id="55ea1-123">If this request header is included and the eTag (or cTag) provided matches the current tag on the file, an `HTTP 304 Not Modified` response is returned.</span></span> |


## <a name="request-body"></a><span data-ttu-id="55ea1-124">Cuerpo de solicitud</span><span class="sxs-lookup"><span data-stu-id="55ea1-124">Request body</span></span>
<span data-ttu-id="55ea1-125">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="55ea1-125">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="55ea1-126">Respuesta</span><span class="sxs-lookup"><span data-stu-id="55ea1-126">Response</span></span>

<span data-ttu-id="55ea1-127">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el recurso [DriveItem](../resources/driveitem.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="55ea1-127">If successful, this method returns a `200 OK` response code and the [DriveItem](../resources/driveitem.md) resource in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="55ea1-128">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="55ea1-128">Example</span></span>

##### <a name="request"></a><span data-ttu-id="55ea1-129">Solicitud</span><span class="sxs-lookup"><span data-stu-id="55ea1-129">Request</span></span>

<span data-ttu-id="55ea1-130">Aquí tiene un ejemplo de la solicitud a la carpeta raíz de OneDrive del usuario.</span><span class="sxs-lookup"><span data-stu-id="55ea1-130">Here is an example of the request to the root folder of the user's OneDrive.</span></span>

<!-- {
  "blockType": "request",
  "name": "get_item"
}-->
```
GET https://graph.microsoft.com/v1.0//me/drive/root
```

##### <a name="response"></a><span data-ttu-id="55ea1-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="55ea1-131">Response</span></span>
<span data-ttu-id="55ea1-132">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="55ea1-132">Here is an example of the response.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.driveItem"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "createdBy": {
      "user": {
          "id": "efee1b77-fb3b-4f65-99d6-274c11914d12",
          "displayName": "Ryan Gregg"
      }
  },
  "createdDateTime": "2016-03-21T20:01:37Z",
  "cTag": "\"c:{86EB4C8E-D20D-46B9-AD41-23B8868DDA8A},0\"",
  "eTag": "\"{86EB4C8E-D20D-46B9-AD41-23B8868DDA8A},1\"",
  "folder": { "childCount": 120 },
  "id": "01NKDM7HMOJTVYMDOSXFDK2QJDXCDI3WUK",
  "lastModifiedBy": {
      "user": {
          "id": "efee1b77-fb3b-4f65-99d6-274c11914d12",
          "displayName": "Ryan Gregg"
      }
  },
  "lastModifiedDateTime": "2016-03-21T20:01:37Z",
  "name": "OneDrive",
  "root": { },
  "size": 157286400,
  "webUrl": "https://contoso-my.sharepoint.com/personal/rgregg_contoso_com/Documents"
}
```

## <a name="notes"></a><span data-ttu-id="55ea1-133">Notas</span><span class="sxs-lookup"><span data-stu-id="55ea1-133">Notes</span></span>

<span data-ttu-id="55ea1-134">Puede usar el [parámetro de cadena de consulta `$expand`](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) para incluir los elementos secundarios de un elemento en la misma llamada al recuperar los metadatos de un elemento si el elemento tiene una relación **children**.</span><span class="sxs-lookup"><span data-stu-id="55ea1-134">You can use the [`$expand` query string parameter](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to include the children of an item in the same call as retrieving the metadata of an item if the item has a **children** relationship.</span></span>

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get item",
  "keywords": "",
  "section": "documentation",
  "tocPath": "OneDrive/Item/Get item"
}-->
