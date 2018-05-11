# <a name="permanently-delete-item"></a><span data-ttu-id="03665-101">Eliminar elementos permanentemente</span><span class="sxs-lookup"><span data-stu-id="03665-101">Permanently delete item</span></span>

<span data-ttu-id="03665-102">Elimina permanentemente un elemento de la carpeta [Elementos eliminados](../resources/directory.md).</span><span class="sxs-lookup"><span data-stu-id="03665-102">Permanently deletes an item from [deleted items](../resources/directory.md).</span></span>

<span data-ttu-id="03665-103">Actualmente, la funcionalidad de elementos eliminados solo es compatible con los recursos [group](../resources/group.md) y [user](../resources/user.md).</span><span class="sxs-lookup"><span data-stu-id="03665-103">Currently, deleted items functionality is only supported for the [group](../resources/group.md) and [user](../resources/user.md) resources.</span></span> <span data-ttu-id="03665-104">Puede eliminar permanentemente un elemento de elementos eliminados.</span><span class="sxs-lookup"><span data-stu-id="03665-104">You can permanently delete an item from deleted items.</span></span> <span data-ttu-id="03665-105">Pero, cuando un elemento se elimina permanentemente, **no** puede restaurarse.</span><span class="sxs-lookup"><span data-stu-id="03665-105">But, once an item is permanently deleted, it **cannot** be restored.</span></span>

## <a name="permissions"></a><span data-ttu-id="03665-106">Permisos</span><span class="sxs-lookup"><span data-stu-id="03665-106">Permissions</span></span>
<span data-ttu-id="03665-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="03665-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

### <a name="for-users"></a><span data-ttu-id="03665-109">Para los usuarios:</span><span class="sxs-lookup"><span data-stu-id="03665-109">For users:</span></span>

|<span data-ttu-id="03665-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="03665-110">Permission type</span></span>      | <span data-ttu-id="03665-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="03665-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="03665-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="03665-112">Delegated (work or school account)</span></span> | <span data-ttu-id="03665-113">User.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="03665-113">User.ReadWrite.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span> |
|<span data-ttu-id="03665-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="03665-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="03665-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="03665-115">Not supported.</span></span> |
|<span data-ttu-id="03665-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="03665-116">Application</span></span> | <span data-ttu-id="03665-117">User.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="03665-117">User.ReadWrite.All</span></span> |

### <a name="for-groups"></a><span data-ttu-id="03665-118">Para los grupos:</span><span class="sxs-lookup"><span data-stu-id="03665-118">For groups:</span></span>

|<span data-ttu-id="03665-119">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="03665-119">Permission type</span></span>      | <span data-ttu-id="03665-120">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="03665-120">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="03665-121">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="03665-121">Delegated (work or school account)</span></span> | <span data-ttu-id="03665-122">Group.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="03665-122">Group.ReadWrite.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span> |
|<span data-ttu-id="03665-123">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="03665-123">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="03665-124">No admitida.</span><span class="sxs-lookup"><span data-stu-id="03665-124">Not supported.</span></span>    |
|<span data-ttu-id="03665-125">Aplicación</span><span class="sxs-lookup"><span data-stu-id="03665-125">Application</span></span> | <span data-ttu-id="03665-126">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="03665-126">Group.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="03665-127">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="03665-127">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /directory/deleteditems/{id}
```
## <a name="request-headers"></a><span data-ttu-id="03665-128">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="03665-128">Request headers</span></span>
| <span data-ttu-id="03665-129">Nombre</span><span class="sxs-lookup"><span data-stu-id="03665-129">Name</span></span>       | <span data-ttu-id="03665-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="03665-130">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="03665-131">Authorization</span><span class="sxs-lookup"><span data-stu-id="03665-131">Authorization</span></span>  | <span data-ttu-id="03665-132">&lt;Código&gt; de portador *necesario*</span><span class="sxs-lookup"><span data-stu-id="03665-132">Bearer &lt;code&gt; *Required*</span></span>|
| <span data-ttu-id="03665-133">Accept</span><span class="sxs-lookup"><span data-stu-id="03665-133">Accept</span></span>  | <span data-ttu-id="03665-134">application/json</span><span class="sxs-lookup"><span data-stu-id="03665-134">application/json</span></span> |

## <a name="request-body"></a><span data-ttu-id="03665-135">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="03665-135">Request body</span></span>
<span data-ttu-id="03665-136">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="03665-136">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="03665-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="03665-137">Response</span></span>

<span data-ttu-id="03665-p103">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="03665-p103">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="03665-140">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="03665-140">Example</span></span>
##### <a name="request"></a><span data-ttu-id="03665-141">Solicitud</span><span class="sxs-lookup"><span data-stu-id="03665-141">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "delete_directory"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/directory/deleteditems/46cc6179-19d0-473e-97ad-6ff84347bbbb
```
##### <a name="response"></a><span data-ttu-id="03665-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="03665-142">Response</span></span>
<span data-ttu-id="03665-p104">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="03665-p104">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true
} -->
```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Delete directory",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->