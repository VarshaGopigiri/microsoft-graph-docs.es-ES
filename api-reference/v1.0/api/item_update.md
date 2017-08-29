# <a name="update-driveitem-properties"></a><span data-ttu-id="61bd8-101">Actualizar propiedades de DriveItem</span><span class="sxs-lookup"><span data-stu-id="61bd8-101">Update DriveItem properties</span></span>

<span data-ttu-id="61bd8-102">Actualiza los metadatos de un [DriveItem](../resources/driveitem.md) por identificador o ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="61bd8-102">Update the metadata for a [DriveItem](../resources/driveitem.md) by ID or path.</span></span>

<span data-ttu-id="61bd8-103">También puede usar una actualización para [mover un elemento](item_move.md) a otro elemento primario actualizando la propiedad **parentReference** del elemento.</span><span class="sxs-lookup"><span data-stu-id="61bd8-103">You can also use update to [move an item](item_move.md) to another parent by updating the item's **parentReference** property.</span></span>

## <a name="permissions"></a><span data-ttu-id="61bd8-104">Permisos</span><span class="sxs-lookup"><span data-stu-id="61bd8-104">Permissions</span></span>
<span data-ttu-id="61bd8-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="61bd8-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="61bd8-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="61bd8-107">Permission type</span></span>      | <span data-ttu-id="61bd8-108">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="61bd8-108">Permissions (from least to most privileged)</span></span>              | 
|:--------------------|:---------------------------------------------------------| 
|<span data-ttu-id="61bd8-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="61bd8-109">Delegated (work or school account)</span></span> | <span data-ttu-id="61bd8-110">Files.ReadWrite, Files.ReadWrite.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="61bd8-110">Files.ReadWrite, Files.ReadWrite.All, Sites.ReadWrite.All</span></span>    | 
|<span data-ttu-id="61bd8-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="61bd8-111">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="61bd8-112">Files.ReadWrite, Files.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="61bd8-112">Files.ReadWrite, Files.ReadWrite.All</span></span>    | 
|<span data-ttu-id="61bd8-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="61bd8-113">Application</span></span> | <span data-ttu-id="61bd8-114">Files.ReadWrite.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="61bd8-114">Files.ReadWrite.All, Sites.ReadWrite.All</span></span> | 

## <a name="http-request"></a><span data-ttu-id="61bd8-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="61bd8-115">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /me/drive/items/{item-id}
PATCH /me/drive/root:/{item-path}
PATCH /drives/{drive-id}/items/{item-id}
PATCH /groups/{group-id}/drive/items/{item-id}
```

## <a name="request-headers"></a><span data-ttu-id="61bd8-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="61bd8-116">Request headers</span></span>

| <span data-ttu-id="61bd8-117">Nombre</span><span class="sxs-lookup"><span data-stu-id="61bd8-117">Name</span></span>          | <span data-ttu-id="61bd8-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="61bd8-118">Type</span></span>   | <span data-ttu-id="61bd8-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="61bd8-119">Description</span></span>                                                                                                                                                         |
|:--------------|:-------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="61bd8-120">if-match</span><span class="sxs-lookup"><span data-stu-id="61bd8-120">if-match</span></span>      | <span data-ttu-id="61bd8-121">String</span><span class="sxs-lookup"><span data-stu-id="61bd8-121">String</span></span> | <span data-ttu-id="61bd8-122">Si se incluye el encabezado de la solicitud y la eTag (o cTag) proporcionada no coincide la eTag actual en la carpeta, se devuelve una respuesta `412 Precondition Failed`.</span><span class="sxs-lookup"><span data-stu-id="61bd8-122">If this request header is included and the eTag (or cTag) provided does not match the current eTag on the folder, a `412 Precondition Failed` response is returned.</span></span> |

## <a name="request-body"></a><span data-ttu-id="61bd8-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="61bd8-123">Request body</span></span>
<span data-ttu-id="61bd8-p102">En el cuerpo de la solicitud, proporcione los valores de las propiedades que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento la aplicación no debe incluir propiedades que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="61bd8-p102">In the request body, supply the values for properties that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance your app should not include properties that haven't changed.</span></span>

## <a name="response"></a><span data-ttu-id="61bd8-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="61bd8-127">Response</span></span>

<span data-ttu-id="61bd8-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el recurso [DriveItem](../resources/driveitem.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="61bd8-128">If successful, this method returns a `200 OK` response code and updated [DriveItem](../resources/driveitem.md) resource in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="61bd8-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="61bd8-129">Example</span></span>
<span data-ttu-id="61bd8-130">Este ejemplo cambia el nombre del driveItem.</span><span class="sxs-lookup"><span data-stu-id="61bd8-130">This example renames the driveItem.</span></span>

<!-- {
  "blockType": "request",
  "name": "update_item"
}-->
```http
PATCH /me/drive/items/{item-id}
Content-type: application/json

{
    "name": "new-file-name.docx"
}
```

##### <a name="response"></a><span data-ttu-id="61bd8-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="61bd8-131">Response</span></span>

<span data-ttu-id="61bd8-p103">En el ejemplo siguiente se muestra la respuesta. Esta respuesta se trunca para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="61bd8-p103">The following example shows the response. This response is truncated for readability.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.driveItem"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "id": "01NKDM7HMOJTVYMDOSXFDK2QJDXCDI3WUK",
    "name": "new-file-name.docx",
    "file": { }
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update item",
  "keywords": "",
  "section": "documentation",
  "tocPath": "OneDrive/Item/Update item"
}-->
