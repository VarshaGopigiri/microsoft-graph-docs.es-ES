# <a name="list-permissions-on-a-driveitem"></a><span data-ttu-id="e9e60-101">Mostrar permisos en un objeto DriveItem</span><span class="sxs-lookup"><span data-stu-id="e9e60-101">List permissions on a DriveItem</span></span>

<span data-ttu-id="e9e60-102">Muestre los permisos efectivos de un objeto [DriveItem](../resources/driveitem.md).</span><span class="sxs-lookup"><span data-stu-id="e9e60-102">List the effective permissions of on a [DriveItem](../resources/driveitem.md).</span></span>

<span data-ttu-id="e9e60-p101">La relación **permisos** del objeto DriveItem no se puede expandir como parte de una llamada a [get DriveItem](item_get.md) o una colección de objetos DriveItem. Debe tener acceso a la propiedad de permisos directamente.</span><span class="sxs-lookup"><span data-stu-id="e9e60-p101">The **permissions** relationship of DriveItem cannot be expanded as part of a call to [get DriveItem](item_get.md) or a collection of DriveItems. You must access the permissions property directly.</span></span>

## <a name="access-to-permissions"></a><span data-ttu-id="e9e60-105">Acceso a Permisos</span><span class="sxs-lookup"><span data-stu-id="e9e60-105">Access to Permissions</span></span>

<span data-ttu-id="e9e60-106">La colección de permisos incluye información potencialmente confidencial y puede no estar disponible para todos los autores de llamadas.</span><span class="sxs-lookup"><span data-stu-id="e9e60-106">The permissions collection includes potentially sensitive information and may not be available for every caller.</span></span>

* <span data-ttu-id="e9e60-p102">Para el propietario del producto, se devolverán todos los permisos. Esto incluye los copropietarios.</span><span class="sxs-lookup"><span data-stu-id="e9e60-p102">For the owner of the item, all permissions will be returned. This includes co-owners.</span></span>
* <span data-ttu-id="e9e60-109">Para un autor de llamada que no sea el propietario, se devuelven solo los permisos que se aplican al autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="e9e60-109">For a non-owner caller, only the permissions that apply to the caller are returned.</span></span>
* <span data-ttu-id="e9e60-110">Las propiedades de permisos que contienen información confidencial (por ejemplo, `shareId` y `webUrl`) se devuelven solo a los autores de llamadas que pueden crear el permiso.</span><span class="sxs-lookup"><span data-stu-id="e9e60-110">Permission properties that contain secrets (e.g. `shareId` and `webUrl`) are only returned for callers that are able to create the Permission.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="e9e60-111">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="e9e60-111">Prerequisites</span></span>
<span data-ttu-id="e9e60-112">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="e9e60-112">One of the following **scopes** is required to execute this API:</span></span>

* <span data-ttu-id="e9e60-113">Files.Read</span><span class="sxs-lookup"><span data-stu-id="e9e60-113">Files.Read</span></span>
* <span data-ttu-id="e9e60-114">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="e9e60-114">Files.ReadWrite</span></span>
* <span data-ttu-id="e9e60-115">Files.Read.All</span><span class="sxs-lookup"><span data-stu-id="e9e60-115">Files.Read.All</span></span>
* <span data-ttu-id="e9e60-116">Files.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="e9e60-116">Files.ReadWrite.All</span></span>
* <span data-ttu-id="e9e60-117">Sites.Read.All</span><span class="sxs-lookup"><span data-stu-id="e9e60-117">Sites.Read.All</span></span>
* <span data-ttu-id="e9e60-118">Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="e9e60-118">Sites.ReadWrite.All</span></span>

## <a name="http-request"></a><span data-ttu-id="e9e60-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e9e60-119">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/drive/items/{item-id}/permissions
GET /me/drive/root:/{path}:/permissions
GET /drives/{drive-id}/items/{item-id}/permissions
GET /groups/{group-id}/drive/items/{item-id}/permissions
```

## <a name="request-headers"></a><span data-ttu-id="e9e60-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e9e60-120">Request headers</span></span>

| <span data-ttu-id="e9e60-121">Nombre</span><span class="sxs-lookup"><span data-stu-id="e9e60-121">Name</span></span>          | <span data-ttu-id="e9e60-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="e9e60-122">Type</span></span>   | <span data-ttu-id="e9e60-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="e9e60-123">Description</span></span>                                                                                                                                     |
|:--------------|:-------|:------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9e60-124">if-none-match</span><span class="sxs-lookup"><span data-stu-id="e9e60-124">if-none-match</span></span> | <span data-ttu-id="e9e60-125">string</span><span class="sxs-lookup"><span data-stu-id="e9e60-125">string</span></span> | <span data-ttu-id="e9e60-126">Si se incluye este encabezado de la solicitud y el ETag proporcionado coincide con el ETag actual del elemento, se devuelve una respuesta `HTTP 304 Not Modified`.</span><span class="sxs-lookup"><span data-stu-id="e9e60-126">If this request header is included and the etag provided matches the current etag on the item, an `HTTP 304 Not Modified` response is returned.</span></span> |


## <a name="optional-query-parameters"></a><span data-ttu-id="e9e60-127">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="e9e60-127">Optional query parameters</span></span>
<span data-ttu-id="e9e60-128">Este método admite los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e9e60-128">This method supports the [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>

## <a name="request-body"></a><span data-ttu-id="e9e60-129">Cuerpo de solicitud</span><span class="sxs-lookup"><span data-stu-id="e9e60-129">Request body</span></span>
<span data-ttu-id="e9e60-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="e9e60-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="e9e60-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e9e60-131">Response</span></span>

<span data-ttu-id="e9e60-132">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de recursos de [Permission](../resources/permission.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e9e60-132">If successful, this method returns a `200 OK` response code and collection of [Permission](../resources/permission.md) resources in the response body.</span></span>

<span data-ttu-id="e9e60-133">Los permisos efectivos de un elemento pueden provenir de dos orígenes:</span><span class="sxs-lookup"><span data-stu-id="e9e60-133">Effective permissions of an item can come from two sources:</span></span>

* <span data-ttu-id="e9e60-134">Permisos que se aplican directamente en el propio elemento</span><span class="sxs-lookup"><span data-stu-id="e9e60-134">Permissions applied directly on the item itself</span></span>
* <span data-ttu-id="e9e60-135">Permisos heredados de los antecesores del elemento</span><span class="sxs-lookup"><span data-stu-id="e9e60-135">Permissions inherited from the item's ancestors</span></span>

<span data-ttu-id="e9e60-p103">Los autores de llamadas pueden distinguir si el permiso se hereda o no comprobando la propiedad **inheritedFrom**. Esta propiedad es un recurso [**itemReference**](../resources/itemreference.md) que hace referencia al antecesor del que se hereda el permiso.</span><span class="sxs-lookup"><span data-stu-id="e9e60-p103">Callers can differentiate if the permission is inherited or not by checking the **inheritedFrom** property. This property is an [**itemReference**](../resources/itemreference.md) resource referencing the ancestor that the permission is inherited from.</span></span>

## <a name="example"></a><span data-ttu-id="e9e60-138">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e9e60-138">Example</span></span>
##### <a name="request"></a><span data-ttu-id="e9e60-139">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e9e60-139">Request</span></span>
<span data-ttu-id="e9e60-140">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e9e60-140">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_permissions"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/drive/items/{item-id}/permissions
```


##### <a name="response"></a><span data-ttu-id="e9e60-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e9e60-141">Response</span></span>
<span data-ttu-id="e9e60-142">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e9e60-142">Here is an example of the response.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.permission",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-Type: application/json

{
  "value": [
    {
      "id": "1",
      "roles": ["write"],
      "link": {
        "webUrl": "https://onedrive.live.com/redir?resid=5D33DD65C6932946!70859&authkey=!AL7N1QAfSWcjNU8&ithint=folder%2cgif",
        "type": "edit"
      }
    },
    {
      "id": "2",
      "roles": ["write"],
      "grantedTo": {
        "user": {
          "id": "5D33DD65C6932946",
          "displayName": "John Doe"
        }
      },
      "inheritedFrom": {
        "driveId": "1234567890ABD",
        "id": "1234567890ABC!123",
        "path": "/drive/root:/Documents" }
    },
    {
      "id": "3",
      "roles": ["write"],
      "link": {
        "webUrl": "https://onedrive.live.com/redir?resid=5D33DD65C6932946!70859&authkey=!AL7N1QAfSWcjNU8&ithint=folder%2cgif",
        "type": "edit",
        "application": {
          "id": "12345",
          "displayName": "TimeTravelPlus"
        }
      }
    }
  ]
}
```

<span data-ttu-id="e9e60-143">Consulte [Obtener permiso](permission_get.md) para obtener más información sobre cómo recuperar un solo recurso de permiso.</span><span class="sxs-lookup"><span data-stu-id="e9e60-143">See [Get permission](permission_get.md) for more details on retrieving a single permission resource.</span></span>


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List permissions",
  "keywords": "",
  "section": "documentation",
  "tocPath": "OneDrive/Item/List permissions"
}-->
