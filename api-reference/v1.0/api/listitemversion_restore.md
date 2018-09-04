# <a name="restore-a-previous-version-of-a-listitem"></a><span data-ttu-id="8bd2e-101">Restaurar una versión anterior de un objeto ListItem</span><span class="sxs-lookup"><span data-stu-id="8bd2e-101">Restore a previous version of a ListItem</span></span>

<span data-ttu-id="8bd2e-102">Restaure una versión anterior de un objeto ListItem para que sea la versión actual.</span><span class="sxs-lookup"><span data-stu-id="8bd2e-102">Restore a previous version of a ListItem to be the current version.</span></span> <span data-ttu-id="8bd2e-103">Esto creará una versión con el contenido de la versión anterior, pero conservará todas las versiones existentes del elemento.</span><span class="sxs-lookup"><span data-stu-id="8bd2e-103">This will create a new version with the contents of the previous version, but preserves all existing versions of the item.</span></span>

## <a name="permissions"></a><span data-ttu-id="8bd2e-104">Permisos</span><span class="sxs-lookup"><span data-stu-id="8bd2e-104">Permissions</span></span>

<span data-ttu-id="8bd2e-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="8bd2e-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|            <span data-ttu-id="8bd2e-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="8bd2e-107">Permission type</span></span>             |         <span data-ttu-id="8bd2e-108">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="8bd2e-108">Permissions (from least to most privileged)</span></span>          |
| :------------------------------------- | :----------------------------------------------------------- |
| <span data-ttu-id="8bd2e-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="8bd2e-109">Delegated (work or school account)</span></span>     | <span data-ttu-id="8bd2e-110">Sites.ReadWrite.All, Sites.Manage.All, Sites.FullControl.All</span><span class="sxs-lookup"><span data-stu-id="8bd2e-110">Sites.ReadWrite.All, Sites.Manage.All, Sites.FullControl.All</span></span> |
| <span data-ttu-id="8bd2e-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="8bd2e-111">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="8bd2e-112">N/D</span><span class="sxs-lookup"><span data-stu-id="8bd2e-112">n/a</span></span>                                                          |
| <span data-ttu-id="8bd2e-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="8bd2e-113">Application</span></span>                            | <span data-ttu-id="8bd2e-114">Sites.ReadWrite.All, Sites.Manage.All, Sites.FullControl.All</span><span class="sxs-lookup"><span data-stu-id="8bd2e-114">Sites.ReadWrite.All, Sites.Manage.All, Sites.FullControl.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="8bd2e-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="8bd2e-115">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
POST /sites/{site-id}/items/{item-id}/versions/{version-id}/restoreVersion
POST /sites/{site-id}/lists/{list-id}/items/{item-id}/versions/{version-id}/restoreVersion
```

### <a name="request-body"></a><span data-ttu-id="8bd2e-116">Cuerpo de solicitud</span><span class="sxs-lookup"><span data-stu-id="8bd2e-116">Request body</span></span>

<span data-ttu-id="8bd2e-117">No es necesario ningún cuerpo de solicitud.</span><span class="sxs-lookup"><span data-stu-id="8bd2e-117">No request body is required.</span></span>

## <a name="example"></a><span data-ttu-id="8bd2e-118">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="8bd2e-118">Example</span></span>

<span data-ttu-id="8bd2e-119">En este ejemplo, se restaura una versión de un recurso listItem identificado por `{item-id}` y `{version-id}`.</span><span class="sxs-lookup"><span data-stu-id="8bd2e-119">This example restores a version of a listItem identified by `{item-id}` and `{version-id}`.</span></span>

<!-- { "blockType": "request", "name": "restore-item-version-listItem", "scopes": "files.readwrite sites.readwrite.all", "target": "action", "tags": "service.graph service.sharepoint" } -->

```http
POST /sites/{site-id}/lists/{list-id}/items/{item-id}/versions/{version-id}/restoreVersion
```

## <a name="response"></a><span data-ttu-id="8bd2e-120">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8bd2e-120">Response</span></span>

<span data-ttu-id="8bd2e-121">Si se realiza correctamente, la llamada API devuelve `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="8bd2e-121">If successful, the API call returns a `204 No Content`.</span></span>

<!-- { "blockType": "response" } -->

```http
HTTP/1.1 204 No Content
```

<!-- {
  "type": "#page.annotation",
  "description": "Create a copy of an existing item.",
  "keywords": "copy existing item",
  "section": "documentation",
  "tocPath": "Items/Copy"
} -->
