# <a name="create-a-new-folder"></a><span data-ttu-id="77b88-101">Create a new folder</span><span class="sxs-lookup"><span data-stu-id="77b88-101">Create a new folder</span></span>

<span data-ttu-id="77b88-102">Crea una carpeta nueva o un [DriveItem](../resources/driveitem.md) en un [Drive](../resources/drive.md) con un elemento primario o una ruta de acceso especificados.</span><span class="sxs-lookup"><span data-stu-id="77b88-102">Create a new folder or [DriveItem](../resources/driveitem.md) in a [Drive](../resources/drive.md) with a specified parent item or path.</span></span>

## <a name="permissions"></a><span data-ttu-id="77b88-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="77b88-103">Permissions</span></span>
<span data-ttu-id="77b88-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="77b88-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="77b88-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="77b88-106">Permission type</span></span>      | <span data-ttu-id="77b88-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="77b88-107">Permissions (from least to most privileged)</span></span>              | 
|:--------------------|:---------------------------------------------------------| 
|<span data-ttu-id="77b88-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="77b88-108">Delegated (work or school account)</span></span> | <span data-ttu-id="77b88-109">Files.ReadWrite, Files.ReadWrite.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="77b88-109">Files.ReadWrite, Files.ReadWrite.All, Sites.ReadWrite.All</span></span>    | 
|<span data-ttu-id="77b88-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="77b88-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="77b88-111">Files.ReadWrite, Files.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="77b88-111">Files.ReadWrite, Files.ReadWrite.All</span></span>    | 
|<span data-ttu-id="77b88-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="77b88-112">Application</span></span> | <span data-ttu-id="77b88-113">Files.ReadWrite.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="77b88-113">Files.ReadWrite.All, Sites.ReadWrite.All</span></span> | 

## <a name="http-request"></a><span data-ttu-id="77b88-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="77b88-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/drive/root/children
POST /me/drive/items/{parent-item-id}/children
POST /drives/{drive-id}/items/{parent-item-id}/children
POST /groups/{group-id}/drive/items/{parent-item-id}/children
```

## <a name="request-body"></a><span data-ttu-id="77b88-115">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="77b88-115">Request body</span></span>
<span data-ttu-id="77b88-116">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [DriveItem](../resources/driveitem.md) que quiere crear.</span><span class="sxs-lookup"><span data-stu-id="77b88-116">In the request body, supply a JSON representation of the [DriveItem](../resources/driveitem.md) resource to create.</span></span>

## <a name="response"></a><span data-ttu-id="77b88-117">Respuesta</span><span class="sxs-lookup"><span data-stu-id="77b88-117">Response</span></span>

<span data-ttu-id="77b88-118">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y el recurso [DriveItem](../resources/driveitem.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="77b88-118">If successful, this method returns `201 Created` response code and a [Driveitem](../resources/driveitem.md) resource in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="77b88-119">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="77b88-119">Example</span></span>

##### <a name="request"></a><span data-ttu-id="77b88-120">Solicitud</span><span class="sxs-lookup"><span data-stu-id="77b88-120">Request</span></span>
<span data-ttu-id="77b88-121">Aquí tiene un ejemplo de la solicitud para crear una carpeta en la raíz de OneDrive del usuario.</span><span class="sxs-lookup"><span data-stu-id="77b88-121">Here is an example of the request to create a new folder in the user's OneDrive root.</span></span>

<!-- {
  "blockType": "request",
  "name": "create_item_from_item"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/root/children
Content-Type: application/json

{
  "name": "New Folder",
  "folder": { }
}
```

##### <a name="response"></a><span data-ttu-id="77b88-122">Respuesta</span><span class="sxs-lookup"><span data-stu-id="77b88-122">Response</span></span>

<span data-ttu-id="77b88-123">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="77b88-123">Here is an example of the response.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.driveItem"
} -->

```http
HTTP/1.1 201 Created
Content-Type: application/json

{
  "createdBy": {
    "user": {
      "displayName": "Ryan Gregg",
      "id": "309EC495-3E92-431D-9124-F0299633171D"
    }
  },
  "createdDateTime": "20160920T14:34:00Z",
  "eTag": "343F1FBD-E9B3-4DDE-BCA7-D61AEAFF44E5,1",
  "id": "ACEA49D1-1444-45A9-A1CB-68B1B28AE491",
  "lastModifiedBy": {
    "user": {
      "displayName": "Ryan Gregg",
      "id": "309EC495-3E92-431D-9124-F0299633171D"
    }
  },
  "lastModifiedDateTime": "20160920T14:34:00Z",
  "name": "New Folder",
  "parentReference": {
    "driveId": "5FE38E3C-051C-4D55-9B83-8A437658275B",
    "id": "E67A8F34-B0AA-46E1-8FF7-0750A29553DF",
    "path": "/drive/root:/"
  },
  "size": 0,
  "folder": {
    "childCount": 0
  }
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create children",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
