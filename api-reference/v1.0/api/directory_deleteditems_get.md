# <a name="get-deleted-item"></a><span data-ttu-id="cfa44-101">Obtener elemento eliminado</span><span class="sxs-lookup"><span data-stu-id="cfa44-101">Get deleted item</span></span>

<span data-ttu-id="cfa44-102">Recuperar las propiedades de un elemento eliminado recientemente en [elementos eliminados](../resources/directory.md).</span><span class="sxs-lookup"><span data-stu-id="cfa44-102">Retrieve the properties of a recently deleted item in [deleted items](../resources/directory.md).</span></span>

<span data-ttu-id="cfa44-103">Actualmente, la funcionalidad de elementos eliminados solo es compatible con los recursos [group](../resources/group.md) y [user](../resources/user.md).</span><span class="sxs-lookup"><span data-stu-id="cfa44-103">Currently, deleted items functionality is only supported for the [group](../resources/group.md) and [user](../resources/user.md) resources.</span></span>

## <a name="permissions"></a><span data-ttu-id="cfa44-104">Permisos</span><span class="sxs-lookup"><span data-stu-id="cfa44-104">Permissions</span></span>
<span data-ttu-id="cfa44-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="cfa44-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

### <a name="for-users"></a><span data-ttu-id="cfa44-107">Para los usuarios:</span><span class="sxs-lookup"><span data-stu-id="cfa44-107">For users:</span></span>

|<span data-ttu-id="cfa44-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="cfa44-108">Permission type</span></span>      | <span data-ttu-id="cfa44-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="cfa44-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="cfa44-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="cfa44-110">Delegated (work or school account)</span></span> | <span data-ttu-id="cfa44-111">User.Read.All, User.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All, Directory AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="cfa44-111">User.Read.All, User.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span> |
|<span data-ttu-id="cfa44-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="cfa44-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="cfa44-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="cfa44-113">Not supported.</span></span> |
|<span data-ttu-id="cfa44-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="cfa44-114">Application</span></span> | <span data-ttu-id="cfa44-115">User.Read.All, User.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="cfa44-115">User.Read.All, User.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All</span></span> |

### <a name="for-groups"></a><span data-ttu-id="cfa44-116">Para los grupos:</span><span class="sxs-lookup"><span data-stu-id="cfa44-116">For groups:</span></span>

|<span data-ttu-id="cfa44-117">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="cfa44-117">Permission type</span></span>      | <span data-ttu-id="cfa44-118">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="cfa44-118">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="cfa44-119">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="cfa44-119">Delegated (work or school account)</span></span> | <span data-ttu-id="cfa44-120">Group.Read.All, Group.ReadWrite.All, Directory.Read.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="cfa44-120">Group.Read.All, Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span> |
|<span data-ttu-id="cfa44-121">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="cfa44-121">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="cfa44-122">No admitida.</span><span class="sxs-lookup"><span data-stu-id="cfa44-122">Not supported.</span></span>    |
|<span data-ttu-id="cfa44-123">Aplicación</span><span class="sxs-lookup"><span data-stu-id="cfa44-123">Application</span></span> | <span data-ttu-id="cfa44-124">Group.Read.All, Group.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="cfa44-124">Group.Read.All, Directory.Read.All, Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="cfa44-125">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="cfa44-125">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /directory/deleteditems/{id}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="cfa44-126">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="cfa44-126">Optional query parameters</span></span>
<span data-ttu-id="cfa44-127">Este método admite los [parámetros de consulta de OData](http://graph.microsoft.io/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="cfa44-127">This method supports the [OData Query Parameters](http://graph.microsoft.io/docs/overview/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="cfa44-128">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="cfa44-128">Request headers</span></span>
| <span data-ttu-id="cfa44-129">Nombre</span><span class="sxs-lookup"><span data-stu-id="cfa44-129">Name</span></span>      |<span data-ttu-id="cfa44-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="cfa44-130">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="cfa44-131">Authorization</span><span class="sxs-lookup"><span data-stu-id="cfa44-131">Authorization</span></span>  | <span data-ttu-id="cfa44-132">&lt;Código&gt; de portador *necesario*</span><span class="sxs-lookup"><span data-stu-id="cfa44-132">Bearer &lt;code&gt; *Required*</span></span>|
| <span data-ttu-id="cfa44-133">Accept</span><span class="sxs-lookup"><span data-stu-id="cfa44-133">Accept</span></span>  | <span data-ttu-id="cfa44-134">application/json</span><span class="sxs-lookup"><span data-stu-id="cfa44-134">application/json</span></span> |

## <a name="request-body"></a><span data-ttu-id="cfa44-135">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="cfa44-135">Request body</span></span>
<span data-ttu-id="cfa44-136">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="cfa44-136">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="cfa44-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cfa44-137">Response</span></span>

<span data-ttu-id="cfa44-138">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [directoryObject](../resources/directoryobject.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="cfa44-138">If successful, this method returns a `200 OK` response code and [directoryObject](../resources/directoryobject.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="cfa44-139">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="cfa44-139">Example</span></span>
##### <a name="request"></a><span data-ttu-id="cfa44-140">Solicitud</span><span class="sxs-lookup"><span data-stu-id="cfa44-140">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "get_directory"
}-->
```http
GET https://graph.microsoft.com/v1.0/directory/deleteditems/46cc6179-19d0-473e-97ad-6ff84347bbbb
```
##### <a name="response"></a><span data-ttu-id="cfa44-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cfa44-141">Response</span></span>
<span data-ttu-id="cfa44-p102">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="cfa44-p102">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.directory"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "@odata.context":"https://graph.microsoft.com/v1.0/$metadata#directoryObjects/$entity",
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
  "description": "Get directory",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->