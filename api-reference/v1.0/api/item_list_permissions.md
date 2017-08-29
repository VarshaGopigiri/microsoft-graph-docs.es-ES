# <a name="list-permissions-on-a-driveitem"></a><span data-ttu-id="005a7-101">Mostrar permisos en un objeto DriveItem</span><span class="sxs-lookup"><span data-stu-id="005a7-101">List permissions on a DriveItem</span></span>

<span data-ttu-id="005a7-102">Muestre los permisos efectivos de un objeto [DriveItem](../resources/driveitem.md).</span><span class="sxs-lookup"><span data-stu-id="005a7-102">List the effective permissions of on a [DriveItem](../resources/driveitem.md).</span></span>

<span data-ttu-id="005a7-p101">La relación **permisos** del objeto DriveItem no se puede expandir como parte de una llamada a [get DriveItem](item_get.md) o una colección de objetos DriveItem. Debe tener acceso a la propiedad de permisos directamente.</span><span class="sxs-lookup"><span data-stu-id="005a7-p101">The **permissions** relationship of DriveItem cannot be expanded as part of a call to [get DriveItem](item_get.md) or a collection of DriveItems. You must access the permissions property directly.</span></span>

## <a name="access-to-permissions"></a><span data-ttu-id="005a7-105">Acceso a Permisos</span><span class="sxs-lookup"><span data-stu-id="005a7-105">Access to Permissions</span></span>

<span data-ttu-id="005a7-106">La colección de permisos incluye información potencialmente confidencial y puede no estar disponible para todos los autores de llamadas.</span><span class="sxs-lookup"><span data-stu-id="005a7-106">The permissions collection includes potentially sensitive information and may not be available for every caller.</span></span>

* <span data-ttu-id="005a7-p102">Para el propietario del producto, se devolverán todos los permisos. Esto incluye los copropietarios.</span><span class="sxs-lookup"><span data-stu-id="005a7-p102">For the owner of the item, all permissions will be returned. This includes co-owners.</span></span>
* <span data-ttu-id="005a7-109">Para un autor de llamada que no sea el propietario, se devuelven solo los permisos que se aplican al autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="005a7-109">For a non-owner caller, only the permissions that apply to the caller are returned.</span></span>
* <span data-ttu-id="005a7-110">Las propiedades de permisos que contienen información confidencial (por ejemplo, `shareId` y `webUrl`) se devuelven solo a los autores de llamadas que pueden crear el permiso.</span><span class="sxs-lookup"><span data-stu-id="005a7-110">Permission properties that contain secrets (e.g. `shareId` and `webUrl`) are only returned for callers that are able to create the Permission.</span></span>

## <a name="permissions"></a><span data-ttu-id="005a7-111">Permisos</span><span class="sxs-lookup"><span data-stu-id="005a7-111">Permissions</span></span>
<span data-ttu-id="005a7-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="005a7-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="005a7-114">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="005a7-114">Permission type</span></span>      | <span data-ttu-id="005a7-115">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="005a7-115">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="005a7-116">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="005a7-116">Delegated (work or school account)</span></span> | <span data-ttu-id="005a7-117">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="005a7-117">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span></span>    |
|<span data-ttu-id="005a7-118">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="005a7-118">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="005a7-119">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="005a7-119">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All</span></span>    |
|<span data-ttu-id="005a7-120">Aplicación</span><span class="sxs-lookup"><span data-stu-id="005a7-120">Application</span></span> | <span data-ttu-id="005a7-121">Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="005a7-121">Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="005a7-122">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="005a7-122">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/drive/items/{item-id}/permissions
GET /me/drive/root:/{path}:/permissions
GET /drives/{drive-id}/items/{item-id}/permissions
GET /groups/{group-id}/drive/items/{item-id}/permissions
```

## <a name="request-headers"></a><span data-ttu-id="005a7-123">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="005a7-123">Request headers</span></span>

| <span data-ttu-id="005a7-124">Nombre</span><span class="sxs-lookup"><span data-stu-id="005a7-124">Name</span></span>          | <span data-ttu-id="005a7-125">Tipo</span><span class="sxs-lookup"><span data-stu-id="005a7-125">Type</span></span>   | <span data-ttu-id="005a7-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="005a7-126">Description</span></span>                                                                                                                                     |
|:--------------|:-------|:------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="005a7-127">if-none-match</span><span class="sxs-lookup"><span data-stu-id="005a7-127">if-none-match</span></span> | <span data-ttu-id="005a7-128">string</span><span class="sxs-lookup"><span data-stu-id="005a7-128">string</span></span> | <span data-ttu-id="005a7-129">Si se incluye este encabezado de la solicitud y el ETag proporcionado coincide con el ETag actual del elemento, se devuelve una respuesta `HTTP 304 Not Modified`.</span><span class="sxs-lookup"><span data-stu-id="005a7-129">If this request header is included and the etag provided matches the current etag on the item, an `HTTP 304 Not Modified` response is returned.</span></span> |

## <a name="optional-query-parameters"></a><span data-ttu-id="005a7-130">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="005a7-130">Optional query parameters</span></span>
<span data-ttu-id="005a7-131">Este método admite los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="005a7-131">This method supports the [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>

## <a name="request-body"></a><span data-ttu-id="005a7-132">Cuerpo de solicitud</span><span class="sxs-lookup"><span data-stu-id="005a7-132">Request body</span></span>
<span data-ttu-id="005a7-133">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="005a7-133">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="005a7-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="005a7-134">Response</span></span>

<span data-ttu-id="005a7-135">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de recursos de [Permission](../resources/permission.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="005a7-135">If successful, this method returns a `200 OK` response code and collection of [Permission](../resources/permission.md) resources in the response body.</span></span>

<span data-ttu-id="005a7-136">Los permisos efectivos de un elemento pueden provenir de dos orígenes:</span><span class="sxs-lookup"><span data-stu-id="005a7-136">Effective permissions of an item can come from two sources:</span></span>

* <span data-ttu-id="005a7-137">Permisos que se aplican directamente en el propio elemento</span><span class="sxs-lookup"><span data-stu-id="005a7-137">Permissions applied directly on the item itself</span></span>
* <span data-ttu-id="005a7-138">Permisos heredados de los antecesores del elemento</span><span class="sxs-lookup"><span data-stu-id="005a7-138">Permissions inherited from the item's ancestors</span></span>

<span data-ttu-id="005a7-p104">Los autores de llamadas pueden distinguir si el permiso se hereda o no comprobando la propiedad **inheritedFrom**. Esta propiedad es un recurso [**itemReference**](../resources/itemreference.md) que hace referencia al antecesor del que se hereda el permiso.</span><span class="sxs-lookup"><span data-stu-id="005a7-p104">Callers can differentiate if the permission is inherited or not by checking the **inheritedFrom** property. This property is an [**itemReference**](../resources/itemreference.md) resource referencing the ancestor that the permission is inherited from.</span></span>

## <a name="example"></a><span data-ttu-id="005a7-141">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="005a7-141">Example</span></span>
##### <a name="request"></a><span data-ttu-id="005a7-142">Solicitud</span><span class="sxs-lookup"><span data-stu-id="005a7-142">Request</span></span>
<span data-ttu-id="005a7-143">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="005a7-143">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_permissions"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/drive/items/{item-id}/permissions
```


##### <a name="response"></a><span data-ttu-id="005a7-144">Respuesta</span><span class="sxs-lookup"><span data-stu-id="005a7-144">Response</span></span>
<span data-ttu-id="005a7-145">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="005a7-145">Here is an example of the response.</span></span>
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

<span data-ttu-id="005a7-146">Consulte [Obtener permiso](permission_get.md) para obtener más información sobre cómo recuperar un solo recurso de permiso.</span><span class="sxs-lookup"><span data-stu-id="005a7-146">See [Get permission](permission_get.md) for more details on retrieving a single permission resource.</span></span>


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List permissions",
  "keywords": "",
  "section": "documentation",
  "tocPath": "OneDrive/Item/List permissions"
}-->
