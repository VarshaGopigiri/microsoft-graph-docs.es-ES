# <a name="grouplifecyclepolicy-addgroup"></a><span data-ttu-id="2cc4b-101">groupLifecyclePolicy: addGroup</span><span class="sxs-lookup"><span data-stu-id="2cc4b-101">groupLifecyclePolicy: addGroup</span></span>

<span data-ttu-id="2cc4b-102">Agrega un grupo a una directiva de ciclo de vida.</span><span class="sxs-lookup"><span data-stu-id="2cc4b-102">Adds a group to a lifecycle policy.</span></span>

## <a name="permissions"></a><span data-ttu-id="2cc4b-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="2cc4b-103">Permissions</span></span>

<span data-ttu-id="2cc4b-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="2cc4b-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>


|<span data-ttu-id="2cc4b-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="2cc4b-106">Permission type</span></span>      | <span data-ttu-id="2cc4b-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="2cc4b-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="2cc4b-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="2cc4b-108">Delegated (work or school account)</span></span> | <span data-ttu-id="2cc4b-109">Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="2cc4b-109">Directory.ReadWrite.All</span></span>    |
|<span data-ttu-id="2cc4b-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="2cc4b-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="2cc4b-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2cc4b-111">Not supported.</span></span>    |
|<span data-ttu-id="2cc4b-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="2cc4b-112">Application</span></span> | <span data-ttu-id="2cc4b-113">Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="2cc4b-113">Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="2cc4b-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="2cc4b-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /groupLifecyclePolicies/{id}/addGroup
```

## <a name="request-headers"></a><span data-ttu-id="2cc4b-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="2cc4b-115">Request headers</span></span>

| <span data-ttu-id="2cc4b-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="2cc4b-116">Name</span></span> | <span data-ttu-id="2cc4b-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="2cc4b-117">Description</span></span> |
|:---------------|:----------|
| <span data-ttu-id="2cc4b-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="2cc4b-118">Authorization</span></span> | <span data-ttu-id="2cc4b-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="2cc4b-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="2cc4b-121">Content-Type</span><span class="sxs-lookup"><span data-stu-id="2cc4b-121">Content-Type</span></span>  | <span data-ttu-id="2cc4b-122">application/json</span><span class="sxs-lookup"><span data-stu-id="2cc4b-122">application/json</span></span> |

## <a name="request-body"></a><span data-ttu-id="2cc4b-123">Cuerpo de solicitud</span><span class="sxs-lookup"><span data-stu-id="2cc4b-123">Request body</span></span>
<span data-ttu-id="2cc4b-124">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="2cc4b-124">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="2cc4b-125">Parámetro</span><span class="sxs-lookup"><span data-stu-id="2cc4b-125">Parameter</span></span> | <span data-ttu-id="2cc4b-126">Tipo</span><span class="sxs-lookup"><span data-stu-id="2cc4b-126">Type</span></span> | <span data-ttu-id="2cc4b-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="2cc4b-127">Description</span></span> |
|:---------------|:--------|:----------|
|<span data-ttu-id="2cc4b-128">groupId</span><span class="sxs-lookup"><span data-stu-id="2cc4b-128">groupId</span></span>|<span data-ttu-id="2cc4b-129">Guid</span><span class="sxs-lookup"><span data-stu-id="2cc4b-129">Guid</span></span>| <span data-ttu-id="2cc4b-130">El id. del grupo para agregar a la directiva.</span><span class="sxs-lookup"><span data-stu-id="2cc4b-130">The id of the group to add to the policy.</span></span> |

## <a name="response"></a><span data-ttu-id="2cc4b-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2cc4b-131">Response</span></span>

<span data-ttu-id="2cc4b-132">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK`.</span><span class="sxs-lookup"><span data-stu-id="2cc4b-132">If successful, this method returns `200 OK` response code.</span></span> <span data-ttu-id="2cc4b-133">Si el grupo se agrega a la directiva, se devuelve un valor **true** en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2cc4b-133">If the group is added to the policy, a **true** value is returned in the response body.</span></span> <span data-ttu-id="2cc4b-134">En caso contrario, se devuelve un valor **false** en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2cc4b-134">Otherwise, a **false** value is returned in the reponse body.</span></span>

## <a name="example"></a><span data-ttu-id="2cc4b-135">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2cc4b-135">Example</span></span>

#### <a name="request"></a><span data-ttu-id="2cc4b-136">Solicitud</span><span class="sxs-lookup"><span data-stu-id="2cc4b-136">Request</span></span>

<!-- {
  "blockType": "ignored",
  "name": "grouplifecyclepolicy_addgroup"
} -->
```http
POST https://graph.microsoft.com/v1.0/groupLifecyclePolicies/{id}/addGroup
Content-type: application/json
Content-length: 57

{
  "groupId": "ffffffff-ffff-ffff-ffff-ffffffffffff"
}
```

#### <a name="response"></a><span data-ttu-id="2cc4b-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2cc4b-137">Response</span></span>
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
  "description": "groupLifecyclePolicy: addgroup",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->