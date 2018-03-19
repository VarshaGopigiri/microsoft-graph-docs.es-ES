# <a name="grouplifecyclepolicy-removegroup"></a><span data-ttu-id="46f06-101">groupLifecyclePolicy: removeGroup</span><span class="sxs-lookup"><span data-stu-id="46f06-101">groupLifecyclePolicy: removeGroup</span></span>

<span data-ttu-id="46f06-102">Quita un grupo de una directiva de ciclo de vida.</span><span class="sxs-lookup"><span data-stu-id="46f06-102">Removes a group from a lifecycle policy.</span></span>

## <a name="permissions"></a><span data-ttu-id="46f06-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="46f06-103">Permissions</span></span>

<span data-ttu-id="46f06-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="46f06-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="46f06-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="46f06-106">Permission type</span></span>      | <span data-ttu-id="46f06-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="46f06-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="46f06-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="46f06-108">Delegated (work or school account)</span></span> | <span data-ttu-id="46f06-109">Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="46f06-109">Directory.ReadWrite.All</span></span>    |
|<span data-ttu-id="46f06-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="46f06-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="46f06-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="46f06-111">Not supported.</span></span>    |
|<span data-ttu-id="46f06-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="46f06-112">Application</span></span> | <span data-ttu-id="46f06-113">Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="46f06-113">Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="46f06-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="46f06-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /groupLifecyclePolicies/{id}/removeGroup
```

## <a name="request-headers"></a><span data-ttu-id="46f06-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="46f06-115">Request headers</span></span>

| <span data-ttu-id="46f06-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="46f06-116">Name</span></span> | <span data-ttu-id="46f06-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="46f06-117">Description</span></span> |
|:---------------|:----------|
| <span data-ttu-id="46f06-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="46f06-118">Authorization</span></span> | <span data-ttu-id="46f06-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="46f06-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="46f06-121">Content-Type</span><span class="sxs-lookup"><span data-stu-id="46f06-121">Content-Type</span></span>  | <span data-ttu-id="46f06-122">application/json</span><span class="sxs-lookup"><span data-stu-id="46f06-122">application/json</span></span> |

## <a name="request-body"></a><span data-ttu-id="46f06-123">Cuerpo de solicitud</span><span class="sxs-lookup"><span data-stu-id="46f06-123">Request body</span></span>
<span data-ttu-id="46f06-124">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="46f06-124">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="46f06-125">Parámetro</span><span class="sxs-lookup"><span data-stu-id="46f06-125">Parameter</span></span> | <span data-ttu-id="46f06-126">Tipo</span><span class="sxs-lookup"><span data-stu-id="46f06-126">Type</span></span> | <span data-ttu-id="46f06-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="46f06-127">Description</span></span> |
|:---------------|:--------|:----------|
|<span data-ttu-id="46f06-128">groupId</span><span class="sxs-lookup"><span data-stu-id="46f06-128">groupId</span></span>|<span data-ttu-id="46f06-129">Guid</span><span class="sxs-lookup"><span data-stu-id="46f06-129">Guid</span></span>| <span data-ttu-id="46f06-130">El id. del grupo para quitar de la directiva.</span><span class="sxs-lookup"><span data-stu-id="46f06-130">The id of the group to remove from the policy.</span></span>|

## <a name="response"></a><span data-ttu-id="46f06-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="46f06-131">Response</span></span>

<span data-ttu-id="46f06-132">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK`.</span><span class="sxs-lookup"><span data-stu-id="46f06-132">If successful, this method returns `200 OK` response code.</span></span> <span data-ttu-id="46f06-133">Si el grupo se quita de la directiva, se devuelve un valor **true** en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="46f06-133">If the group is removed from the policy, a **true** value is returned in the response body.</span></span> <span data-ttu-id="46f06-134">En caso contrario, se devuelve un valor **false** en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="46f06-134">Otherwise, a **false** value is returned in the reponse body.</span></span>

## <a name="example"></a><span data-ttu-id="46f06-135">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="46f06-135">Example</span></span>

##### <a name="request"></a><span data-ttu-id="46f06-136">Solicitud</span><span class="sxs-lookup"><span data-stu-id="46f06-136">Request</span></span>

<!-- {
  "blockType": "ignored",
  "name": "grouplifecyclepolicy_removegroup"
} -->
```http
POST https://graph.microsoft.com/v1.0/groupLifecyclePolicies/{id}/removeGroup
Content-type: application/json
Content-length: 57

{
  "groupId": "ffffffff-ffff-ffff-ffff-ffffffffffff"
}
```

##### <a name="response"></a><span data-ttu-id="46f06-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="46f06-137">Response</span></span>
<!-- { "blockType": "ignored" } -->

```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 21

{
  "value": true
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "groupLifecyclePolicy: removegroup",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->