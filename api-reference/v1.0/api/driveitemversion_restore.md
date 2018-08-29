# <a name="restore-a-previous-version-of-a-driveitem"></a><span data-ttu-id="efa5e-101">Restaurar una versión anterior de un objeto DriveItem</span><span class="sxs-lookup"><span data-stu-id="efa5e-101">Restore a previous version of a DriveItem</span></span>

<span data-ttu-id="efa5e-102">Restaure una versión anterior de un objeto DriveItem para que sea la versión actual.</span><span class="sxs-lookup"><span data-stu-id="efa5e-102">Restore a previous version of a DriveItem to be the current version.</span></span> <span data-ttu-id="efa5e-103">Esto creará una versión con el contenido de la versión anterior, pero conservará todas las versiones existentes del archivo.</span><span class="sxs-lookup"><span data-stu-id="efa5e-103">This will create a new version with the contents of the previous version, but preserves all existing versions of the file.</span></span>

## <a name="permissions"></a><span data-ttu-id="efa5e-104">Permisos</span><span class="sxs-lookup"><span data-stu-id="efa5e-104">Permissions</span></span>

<span data-ttu-id="efa5e-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="efa5e-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="efa5e-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="efa5e-107">Permission type</span></span>      | <span data-ttu-id="efa5e-108">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="efa5e-108">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="efa5e-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="efa5e-109">Delegated (work or school account)</span></span> | <span data-ttu-id="efa5e-110">Files.ReadWrite, Files.ReadWrite.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="efa5e-110">Files.ReadWrite, Files.ReadWrite.All, Sites.ReadWrite.All</span></span>    |
|<span data-ttu-id="efa5e-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="efa5e-111">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="efa5e-112">Files.ReadWrite, Files.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="efa5e-112">Files.ReadWrite, Files.ReadWrite.All</span></span>    |
|<span data-ttu-id="efa5e-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="efa5e-113">Application</span></span> | <span data-ttu-id="efa5e-114">Files.ReadWrite.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="efa5e-114">Files.ReadWrite.All, Sites.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="efa5e-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="efa5e-115">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
POST /drives/{driveId}/items/{itemId}/versions/{version-id}/restoreVersion
POST /groups/{groupId}/drive/items/{itemId}/versions/{version-id}/restoreVersion
POST /me/drive/items/{item-id}/versions/{version-id}/restoreVersion
POST /sites/{siteId}/drive/items/{itemId}/versions/{version-id}/restoreVersion
POST /users/{userId}/drive/items/{itemId}/versions/{version-id}/restoreVersion
```

### <a name="request-body"></a><span data-ttu-id="efa5e-116">Cuerpo de solicitud</span><span class="sxs-lookup"><span data-stu-id="efa5e-116">Request body</span></span>

<span data-ttu-id="efa5e-117">No es necesario ningún cuerpo de solicitud.</span><span class="sxs-lookup"><span data-stu-id="efa5e-117">No request body is required.</span></span>

## <a name="example"></a><span data-ttu-id="efa5e-118">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="efa5e-118">Example</span></span>

<span data-ttu-id="efa5e-119">En este ejemplo, se restaura una versión de un archivo identificado por `{item-id}` y `{version-id}`.</span><span class="sxs-lookup"><span data-stu-id="efa5e-119">This example restores a version of a file identified by `{item-id}` and `{version-id}`.</span></span>

<!-- { "blockType": "request", "name": "restore-item-version", "scopes": "files.readwrite", "target": "action" } -->

```http
POST /drives/{drive-id}/items/{item-id}/versions/{version-id}/restoreVersion
```

## <a name="response"></a><span data-ttu-id="efa5e-120">Respuesta</span><span class="sxs-lookup"><span data-stu-id="efa5e-120">Response</span></span>

<span data-ttu-id="efa5e-121">Si se realiza correctamente, la llamada API devuelve `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="efa5e-121">If successful, the API call returns a `204 No Content`.</span></span>

<!-- { "blockType": "response" } -->

```http
HTTP/1.1 204 No Content
```

[item-resource]: ../resources/driveitem.md

<!-- {
  "type": "#page.annotation",
  "description": "Create a copy of an existing item.",
  "keywords": "copy existing item",
  "section": "documentation",
  "tocPath": "Items/Copy"
} -->
