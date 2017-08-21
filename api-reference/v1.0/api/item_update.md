# <a name="update-driveitem-properties"></a><span data-ttu-id="05343-101">Actualizar propiedades de DriveItem</span><span class="sxs-lookup"><span data-stu-id="05343-101">Update DriveItem properties</span></span>

<span data-ttu-id="05343-102">Actualiza los metadatos de un [DriveItem](../resources/driveitem.md) por identificador o ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="05343-102">Update the metadata for a [DriveItem](../resources/driveitem.md) by ID or path.</span></span>

<span data-ttu-id="05343-103">También puede usar una actualización para [mover un elemento](item_move.md) a otro elemento primario actualizando la propiedad **parentReference** del elemento.</span><span class="sxs-lookup"><span data-stu-id="05343-103">You can also use update to [move an item](item_move.md) to another parent by updating the item's **parentReference** property.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="05343-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="05343-104">Prerequisites</span></span>
<span data-ttu-id="05343-105">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="05343-105">One of the following **scopes** is required to execute this API:</span></span>

* <span data-ttu-id="05343-106">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="05343-106">Files.ReadWrite</span></span>
* <span data-ttu-id="05343-107">Files.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="05343-107">Files.ReadWrite.All</span></span>
* <span data-ttu-id="05343-108">Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="05343-108">Sites.ReadWrite.All</span></span>

## <a name="http-request"></a><span data-ttu-id="05343-109">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="05343-109">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /me/drive/items/{item-id}
PATCH /me/drive/root:/{item-path}
PATCH /drives/{drive-id}/items/{item-id}
PATCH /groups/{group-id}/drive/items/{item-id}
```

## <a name="request-headers"></a><span data-ttu-id="05343-110">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="05343-110">Request headers</span></span>

| <span data-ttu-id="05343-111">Nombre</span><span class="sxs-lookup"><span data-stu-id="05343-111">Name</span></span>          | <span data-ttu-id="05343-112">Tipo</span><span class="sxs-lookup"><span data-stu-id="05343-112">Type</span></span>   | <span data-ttu-id="05343-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="05343-113">Description</span></span>                                                                                                                                                         |
|:--------------|:-------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="05343-114">if-match</span><span class="sxs-lookup"><span data-stu-id="05343-114">if-match</span></span>      | <span data-ttu-id="05343-115">String</span><span class="sxs-lookup"><span data-stu-id="05343-115">String</span></span> | <span data-ttu-id="05343-116">Si se incluye el encabezado de la solicitud y la eTag (o cTag) proporcionada no coincide la eTag actual en la carpeta, se devuelve una respuesta `412 Precondition Failed`.</span><span class="sxs-lookup"><span data-stu-id="05343-116">If this request header is included and the eTag (or cTag) provided does not match the current eTag on the folder, a `412 Precondition Failed` response is returned.</span></span> |

## <a name="request-body"></a><span data-ttu-id="05343-117">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="05343-117">Request body</span></span>
<span data-ttu-id="05343-p101">En el cuerpo de la solicitud, proporcione los valores de las propiedades que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento la aplicación no debe incluir propiedades que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="05343-p101">In the request body, supply the values for properties that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance your app should not include properties that haven't changed.</span></span>

## <a name="response"></a><span data-ttu-id="05343-121">Respuesta</span><span class="sxs-lookup"><span data-stu-id="05343-121">Response</span></span>

<span data-ttu-id="05343-122">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el recurso [DriveItem](../resources/driveitem.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="05343-122">If successful, this method returns a `200 OK` response code and updated [DriveItem](../resources/driveitem.md) resource in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="05343-123">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="05343-123">Example</span></span>
<span data-ttu-id="05343-124">Este ejemplo cambia el nombre del driveItem.</span><span class="sxs-lookup"><span data-stu-id="05343-124">This example renames the driveItem.</span></span>

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

##### <a name="response"></a><span data-ttu-id="05343-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="05343-125">Response</span></span>

<span data-ttu-id="05343-p102">En el ejemplo siguiente se muestra la respuesta. Esta respuesta se trunca para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="05343-p102">The following example shows the response. This response is truncated for readability.</span></span>

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
