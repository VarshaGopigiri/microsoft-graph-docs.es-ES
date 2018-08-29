# <a name="restore-deleted-item"></a><span data-ttu-id="837ac-101">Restaurar elemento eliminado</span><span class="sxs-lookup"><span data-stu-id="837ac-101">Restore deleted item</span></span>

<span data-ttu-id="837ac-102">Restaura un elemento eliminado recientemente de la carpeta [Elementos eliminados](../resources/directory.md).</span><span class="sxs-lookup"><span data-stu-id="837ac-102">Restores a recently deleted item from [deleted items](../resources/directory.md).</span></span> 

<span data-ttu-id="837ac-103">Actualmente, la funcionalidad de elementos eliminados solo es compatible con los recursos [group](../resources/group.md) y [user](../resources/user.md).</span><span class="sxs-lookup"><span data-stu-id="837ac-103">Currently, deleted items functionality is only supported for the [group](../resources/group.md) and [user](../resources/user.md) resources.</span></span> <span data-ttu-id="837ac-104">Si un elemento se ha eliminado accidentalmente, puede restaurarlo por completo.</span><span class="sxs-lookup"><span data-stu-id="837ac-104">If an item was accidentally deleted, you can fully restore the item.</span></span>

<span data-ttu-id="837ac-105">Un elemento eliminado recientemente seguirá estando disponible durante 30 días.</span><span class="sxs-lookup"><span data-stu-id="837ac-105">A recently deleted item will remain available for up to 30 days.</span></span> <span data-ttu-id="837ac-106">Después de 30 días, el elemento se elimina permanentemente.</span><span class="sxs-lookup"><span data-stu-id="837ac-106">After 30 days, the item is permanently deleted.</span></span>

## <a name="permissions"></a><span data-ttu-id="837ac-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="837ac-107">Permissions</span></span>
<span data-ttu-id="837ac-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="837ac-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

### <a name="for-users"></a><span data-ttu-id="837ac-110">Para los usuarios:</span><span class="sxs-lookup"><span data-stu-id="837ac-110">For users:</span></span>

|<span data-ttu-id="837ac-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="837ac-111">Permission type</span></span>      | <span data-ttu-id="837ac-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="837ac-112">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="837ac-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="837ac-113">Delegated (work or school account)</span></span> | <span data-ttu-id="837ac-114">User.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="837ac-114">User.ReadWrite.All, Directory.AccessAsUser.All</span></span> |
|<span data-ttu-id="837ac-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="837ac-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="837ac-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="837ac-116">Not supported.</span></span> |
|<span data-ttu-id="837ac-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="837ac-117">Application</span></span> | <span data-ttu-id="837ac-118">User.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="837ac-118">User.ReadWrite.All</span></span> |

### <a name="for-groups"></a><span data-ttu-id="837ac-119">Para los grupos:</span><span class="sxs-lookup"><span data-stu-id="837ac-119">For groups:</span></span>

|<span data-ttu-id="837ac-120">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="837ac-120">Permission type</span></span>      | <span data-ttu-id="837ac-121">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="837ac-121">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="837ac-122">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="837ac-122">Delegated (work or school account)</span></span> | <span data-ttu-id="837ac-123">Group.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="837ac-123">Group.ReadWrite.All, Directory.AccessAsUser.All</span></span> |
|<span data-ttu-id="837ac-124">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="837ac-124">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="837ac-125">No admitida.</span><span class="sxs-lookup"><span data-stu-id="837ac-125">Not supported.</span></span>    |
|<span data-ttu-id="837ac-126">Aplicación</span><span class="sxs-lookup"><span data-stu-id="837ac-126">Application</span></span> | <span data-ttu-id="837ac-127">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="837ac-127">Group.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="837ac-128">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="837ac-128">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /directory/deletedItems/{id}/restore
```

## <a name="request-headers"></a><span data-ttu-id="837ac-129">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="837ac-129">Request headers</span></span>
| <span data-ttu-id="837ac-130">Nombre</span><span class="sxs-lookup"><span data-stu-id="837ac-130">Name</span></span>       | <span data-ttu-id="837ac-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="837ac-131">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="837ac-132">Authorization</span><span class="sxs-lookup"><span data-stu-id="837ac-132">Authorization</span></span>  | <span data-ttu-id="837ac-133">&lt;Código&gt; de portador *necesario*</span><span class="sxs-lookup"><span data-stu-id="837ac-133">Bearer &lt;code&gt; *Required*</span></span>|
| <span data-ttu-id="837ac-134">Accept</span><span class="sxs-lookup"><span data-stu-id="837ac-134">Accept</span></span> | <span data-ttu-id="837ac-135">application/json</span><span class="sxs-lookup"><span data-stu-id="837ac-135">application/json</span></span> |

## <a name="request-body"></a><span data-ttu-id="837ac-136">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="837ac-136">Request body</span></span>
<span data-ttu-id="837ac-137">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="837ac-137">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="837ac-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="837ac-138">Response</span></span>

<span data-ttu-id="837ac-139">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto [directoryObject](../resources/directoryobject.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="837ac-139">If successful, this method returns `200 OK` response code and [directoryObject](../resources/directoryobject.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="837ac-140">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="837ac-140">Example</span></span>
##### <a name="request"></a><span data-ttu-id="837ac-141">Solicitud</span><span class="sxs-lookup"><span data-stu-id="837ac-141">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "create_directoryobject_from_directory"
}-->
```http
POST https://graph.microsoft.com/v1.0/directory/deletedItems/{object-id}/restore
```
<span data-ttu-id="837ac-142">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [directoryObject](../resources/directoryobject.md).</span><span class="sxs-lookup"><span data-stu-id="837ac-142">In the request body, supply a JSON representation of [directoryObject](../resources/directoryobject.md) object.</span></span>
##### <a name="response"></a><span data-ttu-id="837ac-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="837ac-143">Response</span></span>
<span data-ttu-id="837ac-p104">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="837ac-p104">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.directoryObject"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "@odata.context":"https://graph.microsoft.com/v1.0/$metadata#directoryObjects/$entity",
  "@odata.type":"#microsoft.graph.group",
  "id":"46cc6179-19d0-473e-97ad-6ff84347bbbb",
  "displayName":"SampleGroup",
  "groupTypes":["Unified"],
  "mail":"example@contoso.com",
  "mailEnabled":true,
  "mailNickname":"Example",
  "securityEnabled":false,
  "visibility":"Public"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create deletedItem",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->