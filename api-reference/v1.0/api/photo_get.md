# <a name="get-photo"></a><span data-ttu-id="28210-101">Get photo</span><span class="sxs-lookup"><span data-stu-id="28210-101">Get photo</span></span>

<span data-ttu-id="28210-102">Recupera las propiedades y las relaciones del objeto photo.</span><span class="sxs-lookup"><span data-stu-id="28210-102">Retrieve the properties and relationships of photo object.</span></span>
## <a name="permissions"></a><span data-ttu-id="28210-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="28210-103">Permissions</span></span>
<span data-ttu-id="28210-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="28210-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="28210-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="28210-106">Permission type</span></span>      | <span data-ttu-id="28210-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="28210-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="28210-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="28210-108">Delegated (work or school account)</span></span> | <span data-ttu-id="28210-109">Files.Read</span><span class="sxs-lookup"><span data-stu-id="28210-109">Files.Read</span></span>    |
|<span data-ttu-id="28210-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="28210-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="28210-111">Files.Read</span><span class="sxs-lookup"><span data-stu-id="28210-111">Files.Read</span></span>    |
|<span data-ttu-id="28210-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="28210-112">Application</span></span> | <span data-ttu-id="28210-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="28210-113">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="28210-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="28210-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /users/{id | userPrincipalName}/photo
GET /groups/{id}/photo
GET /drive/root/createdByUser/photo
```
## <a name="optional-query-parameters"></a><span data-ttu-id="28210-115">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="28210-115">Optional query parameters</span></span>
<span data-ttu-id="28210-116">Este método admite los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="28210-116">This method supports the [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="28210-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="28210-117">Request headers</span></span>
| <span data-ttu-id="28210-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="28210-118">Name</span></span>       | <span data-ttu-id="28210-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="28210-119">Type</span></span> | <span data-ttu-id="28210-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="28210-120">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="28210-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="28210-121">Authorization</span></span>  | <span data-ttu-id="28210-122">cadena</span><span class="sxs-lookup"><span data-stu-id="28210-122">string</span></span>  | <span data-ttu-id="28210-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="28210-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="28210-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="28210-125">Request body</span></span>
<span data-ttu-id="28210-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="28210-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="28210-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="28210-127">Response</span></span>

<span data-ttu-id="28210-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [photo](../resources/photo.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="28210-128">If successful, this method returns a `200 OK` response code and [photo](../resources/photo.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="28210-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="28210-129">Example</span></span>
##### <a name="request"></a><span data-ttu-id="28210-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="28210-130">Request</span></span>
<span data-ttu-id="28210-131">Este es un ejemplo de la solicitud de metadatos de fotos.</span><span class="sxs-lookup"><span data-stu-id="28210-131">Here is an example of the request for photo metadata.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_photo"
}-->
```http
GET https://graph.microsoft.com/v1.0/users/{id|userPrincipalName}/photo
```
##### <a name="response"></a><span data-ttu-id="28210-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="28210-132">Response</span></span>
<span data-ttu-id="28210-133">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="28210-133">Here is an example of the response.</span></span>
<!-- {
  "blockType": "response",
  "truncated": false,
  "@odata.type": "microsoft.graph.profilePhoto"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 53

{
  "height": 99,
  "width": 99,
  "id": "id-value"
}
```
##### <a name="request"></a><span data-ttu-id="28210-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="28210-134">Request</span></span>
<span data-ttu-id="28210-135">Este es un ejemplo de la solicitud de bytes de fotos.</span><span class="sxs-lookup"><span data-stu-id="28210-135">Here is an example of the request for the photo bytes.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_photo_value"
}-->
```http
GET https://graph.microsoft.com/v1.0/users/{id|userPrincipalName}/photo/$value
```
##### <a name="response"></a><span data-ttu-id="28210-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="28210-136">Response</span></span>
<span data-ttu-id="28210-137">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="28210-137">Here is an example of the response.</span></span>

<!-- { "blockType": "response", "@odata.type": "Edm.Stream" } -->

```http
HTTP/1.1 200 OK
Cache-Control: private
Content-Type: image/jpeg
ETag: "A19A6498"
request-id: 16e1bff0-6d74-47d6-944c-61707916a74c
client-request-id: 16e1bff0-6d74-47d6-944c-61707916a74c
x-ms-ags-diagnostic: {"ServerInfo":{"DataCenter":"West US","Slice":"SliceA","Ring":"5","ScaleUnit":"003","Host":"AGSFE_IN_14","ADSiteName":"WST"}}
Access-Control-Allow-Origin: *
Access-Control-Expose-Headers: ETag, Location, Preference-Applied, Content-Range, request-id, client-request-id
Duration: 125.9389
Date: Wed, 13 Dec 2017 22:02:17 GMT
Content-Length: 250526

<binary image data>
```
<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get photo",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
