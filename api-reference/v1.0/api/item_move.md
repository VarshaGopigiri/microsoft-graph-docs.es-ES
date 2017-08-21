# <a name="move-a-driveitem"></a><span data-ttu-id="8f41f-101">Mover un objeto DriveItem</span><span class="sxs-lookup"><span data-stu-id="8f41f-101">Move a DriveItem</span></span>

<span data-ttu-id="8f41f-p101">Para mover un objeto DriveItem a un nuevo elemento primario, la aplicación solicita actualizar la **parentReference** del objeto DriveItem que se moverá. Este es un caso especial del método [Update](item_update.md). La aplicación puede mover un elemento a un nuevo contenedor y actualizar otras propiedades del elemento en una sola solicitud.</span><span class="sxs-lookup"><span data-stu-id="8f41f-p101">To move a DriveItem to a new parent item, your app requests to update the **parentReference** of the DriveItem to move. This is a special case of the [Update](item_update.md) method. Your app can combine moving an item to a new container and updating other properties of the item into a single request.</span></span>

<span data-ttu-id="8f41f-105">No se pueden mover elementos entre [Drives](../resources/drive.md) con esta solicitud.</span><span class="sxs-lookup"><span data-stu-id="8f41f-105">Items cannot be moved between [Drives](../resources/drive.md) using this request.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="8f41f-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="8f41f-106">Prerequisites</span></span>
<span data-ttu-id="8f41f-107">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="8f41f-107">One of the following **scopes** is required to execute this API:</span></span>

* <span data-ttu-id="8f41f-108">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="8f41f-108">Files.ReadWrite</span></span>
* <span data-ttu-id="8f41f-109">Files.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="8f41f-109">Files.ReadWrite.All</span></span>
* <span data-ttu-id="8f41f-110">Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="8f41f-110">Sites.ReadWrite.All</span></span>


## <a name="http-request"></a><span data-ttu-id="8f41f-111">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="8f41f-111">HTTP request</span></span>

```http
PATCH /me/drive/items/{item-id}
PATCH /me/drive/root:/{item-path}
PATCH /drives/{drive-id}/items/{item-id}
PATCH /groups/{group-id}/drive/{item-id}
```

## <a name="request-headers"></a><span data-ttu-id="8f41f-112">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="8f41f-112">Request headers</span></span>

| <span data-ttu-id="8f41f-113">Nombre</span><span class="sxs-lookup"><span data-stu-id="8f41f-113">Name</span></span>          | <span data-ttu-id="8f41f-114">Tipo</span><span class="sxs-lookup"><span data-stu-id="8f41f-114">Type</span></span>   | <span data-ttu-id="8f41f-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="8f41f-115">Description</span></span>                                                                                                                                                         |
|:--------------|:-------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f41f-116">if-match</span><span class="sxs-lookup"><span data-stu-id="8f41f-116">if-match</span></span>      | <span data-ttu-id="8f41f-117">String</span><span class="sxs-lookup"><span data-stu-id="8f41f-117">String</span></span> | <span data-ttu-id="8f41f-118">Si se incluye el encabezado de la solicitud y la eTag (o cTag) proporcionada no coincide la eTag actual en la carpeta, se devuelve una respuesta `412 Precondition Failed`.</span><span class="sxs-lookup"><span data-stu-id="8f41f-118">If this request header is included and the eTag (or cTag) provided does not match the current eTag on the folder, a `412 Precondition Failed` response is returned.</span></span> |


## <a name="request-body"></a><span data-ttu-id="8f41f-119">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="8f41f-119">Request body</span></span>
<span data-ttu-id="8f41f-p102">En el cuerpo de la solicitud, proporcione el nuevo valor de la propiedad **parentReference**. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="8f41f-p102">In the request body, supply the new value for the **parentReference** property. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

<span data-ttu-id="8f41f-p103">**Nota:** Al mover elementos a la raíz de un OneDrive, no puede usar la sintaxis `"id:" "root"`. Tendrá que usar el identificador real de la carpeta raíz o usar `{"path": "/drive/root"}` para la referencia primaria.</span><span class="sxs-lookup"><span data-stu-id="8f41f-p103">**Note:** When moving items to the root of a OneDrive you cannot use the `"id:" "root"` syntax. You either need to use the real ID of the root folder, or use `{"path": "/drive/root"}` for the parent reference.</span></span>

## <a name="response"></a><span data-ttu-id="8f41f-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8f41f-125">Response</span></span>

<span data-ttu-id="8f41f-126">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el recurso [DriveItem](../resources/driveitem.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8f41f-126">If successful, this method returns a `200 OK` response code and updated [DriveItem](../resources/driveitem.md) resource in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="8f41f-127">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="8f41f-127">Example</span></span>
<span data-ttu-id="8f41f-128">En este ejemplo, se mueve un elemento especificado mediante {item-id} a la carpeta **Documentos** del OneDrive del usuario.</span><span class="sxs-lookup"><span data-stu-id="8f41f-128">This example moves an item specified by {item-id} into the **Documents** folder in the user's OneDrive.</span></span>

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

##### <a name="response"></a><span data-ttu-id="8f41f-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8f41f-129">Response</span></span>

<span data-ttu-id="8f41f-130">En el ejemplo siguiente se muestra la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8f41f-130">The following example shows the response.</span></span>

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
