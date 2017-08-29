# <a name="move-a-driveitem"></a><span data-ttu-id="74898-101">Mover un objeto DriveItem</span><span class="sxs-lookup"><span data-stu-id="74898-101">Move a DriveItem</span></span>

<span data-ttu-id="74898-p101">Para mover un objeto DriveItem a un nuevo elemento primario, la aplicación solicita actualizar la **parentReference** del objeto DriveItem que se moverá. Este es un caso especial del método [Update](item_update.md). La aplicación puede mover un elemento a un nuevo contenedor y actualizar otras propiedades del elemento en una sola solicitud.</span><span class="sxs-lookup"><span data-stu-id="74898-p101">To move a DriveItem to a new parent item, your app requests to update the **parentReference** of the DriveItem to move. This is a special case of the [Update](item_update.md) method. Your app can combine moving an item to a new container and updating other properties of the item into a single request.</span></span>

<span data-ttu-id="74898-105">No se pueden mover elementos entre [Drives](../resources/drive.md) con esta solicitud.</span><span class="sxs-lookup"><span data-stu-id="74898-105">Items cannot be moved between [Drives](../resources/drive.md) using this request.</span></span>

## <a name="permissions"></a><span data-ttu-id="74898-106">Permisos</span><span class="sxs-lookup"><span data-stu-id="74898-106">Permissions</span></span>
<span data-ttu-id="74898-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="74898-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="74898-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="74898-109">Permission type</span></span>      | <span data-ttu-id="74898-110">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="74898-110">Permissions (from least to most privileged)</span></span>              | 
|:--------------------|:---------------------------------------------------------| 
|<span data-ttu-id="74898-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="74898-111">Delegated (work or school account)</span></span> | <span data-ttu-id="74898-112">Files.ReadWrite, Files.ReadWrite.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="74898-112">Files.ReadWrite, Files.ReadWrite.All, Sites.ReadWrite.All</span></span>    | 
|<span data-ttu-id="74898-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="74898-113">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="74898-114">Files.ReadWrite, Files.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="74898-114">Files.ReadWrite, Files.ReadWrite.All</span></span>    | 
|<span data-ttu-id="74898-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="74898-115">Application</span></span> | <span data-ttu-id="74898-116">Files.ReadWrite.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="74898-116">Files.ReadWrite.All, Sites.ReadWrite.All</span></span> | 

## <a name="http-request"></a><span data-ttu-id="74898-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="74898-117">HTTP request</span></span>

```http
PATCH /me/drive/items/{item-id}
PATCH /me/drive/root:/{item-path}
PATCH /drives/{drive-id}/items/{item-id}
PATCH /groups/{group-id}/drive/{item-id}
```

## <a name="request-headers"></a><span data-ttu-id="74898-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="74898-118">Request headers</span></span>

| <span data-ttu-id="74898-119">Nombre</span><span class="sxs-lookup"><span data-stu-id="74898-119">Name</span></span>          | <span data-ttu-id="74898-120">Tipo</span><span class="sxs-lookup"><span data-stu-id="74898-120">Type</span></span>   | <span data-ttu-id="74898-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="74898-121">Description</span></span>                                                                                                                                                         |
|:--------------|:-------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="74898-122">if-match</span><span class="sxs-lookup"><span data-stu-id="74898-122">if-match</span></span>      | <span data-ttu-id="74898-123">String</span><span class="sxs-lookup"><span data-stu-id="74898-123">String</span></span> | <span data-ttu-id="74898-124">Si se incluye el encabezado de la solicitud y la eTag (o cTag) proporcionada no coincide la eTag actual en la carpeta, se devuelve una respuesta `412 Precondition Failed`.</span><span class="sxs-lookup"><span data-stu-id="74898-124">If this request header is included and the eTag (or cTag) provided does not match the current eTag on the folder, a `412 Precondition Failed` response is returned.</span></span> |


## <a name="request-body"></a><span data-ttu-id="74898-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="74898-125">Request body</span></span>
<span data-ttu-id="74898-p103">En el cuerpo de la solicitud, proporcione el nuevo valor de la propiedad **parentReference**. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="74898-p103">In the request body, supply the new value for the **parentReference** property. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

<span data-ttu-id="74898-p104">**Nota:** Al mover elementos a la raíz de un OneDrive, no puede usar la sintaxis `"id:" "root"`. Tendrá que usar el identificador real de la carpeta raíz o usar `{"path": "/drive/root"}` para la referencia primaria.</span><span class="sxs-lookup"><span data-stu-id="74898-p104">**Note:** When moving items to the root of a OneDrive you cannot use the `"id:" "root"` syntax. You either need to use the real ID of the root folder, or use `{"path": "/drive/root"}` for the parent reference.</span></span>

## <a name="response"></a><span data-ttu-id="74898-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="74898-131">Response</span></span>

<span data-ttu-id="74898-132">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el recurso [DriveItem](../resources/driveitem.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="74898-132">If successful, this method returns a `200 OK` response code and updated [DriveItem](../resources/driveitem.md) resource in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="74898-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="74898-133">Example</span></span>
<span data-ttu-id="74898-134">En este ejemplo, se mueve un elemento especificado mediante {item-id} a la carpeta **Documentos** del OneDrive del usuario.</span><span class="sxs-lookup"><span data-stu-id="74898-134">This example moves an item specified by {item-id} into the **Documents** folder in the user's OneDrive.</span></span>

<!-- {
  "blockType": "request",
  "name": "update_item"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/me/drive/items/{item-id}
Content-type: application/json

{
    "name": "new-item-name",
    "parentReference" : {"path": "/drive/root:/Documents"}
}
```

##### <a name="response"></a><span data-ttu-id="74898-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="74898-135">Response</span></span>

<span data-ttu-id="74898-136">En el ejemplo siguiente se muestra la respuesta.</span><span class="sxs-lookup"><span data-stu-id="74898-136">The following example shows the formula bar</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.driveItem"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "id": "0123456789abc",
    "name": "new-item-name",
    "folder": { "childCount": 3 },
  "parentReference": {
    "id": "507DE6D5-0201-496A-AA87-5E2563247982",
    "path": "/drive/root:/Documents"
  }
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Move item",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
