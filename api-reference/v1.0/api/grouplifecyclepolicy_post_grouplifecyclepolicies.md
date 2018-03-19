# <a name="create-grouplifecyclepolicy"></a><span data-ttu-id="9b6a0-101">Crear groupLifecyclePolicy</span><span class="sxs-lookup"><span data-stu-id="9b6a0-101">Create groupLifecyclePolicy</span></span>

<span data-ttu-id="9b6a0-102">Crea un nuevo objeto [groupLifecyclePolicy](../resources/grouplifecyclepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="9b6a0-102">Creates a new [groupLifecyclePolicy](../resources/grouplifecyclepolicy.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="9b6a0-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="9b6a0-103">Permissions</span></span>

<span data-ttu-id="9b6a0-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="9b6a0-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="9b6a0-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="9b6a0-106">Permission type</span></span>      | <span data-ttu-id="9b6a0-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="9b6a0-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="9b6a0-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="9b6a0-108">Delegated (work or school account)</span></span> | <span data-ttu-id="9b6a0-109">Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="9b6a0-109">Directory.ReadWrite.All</span></span>    |
|<span data-ttu-id="9b6a0-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="9b6a0-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="9b6a0-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9b6a0-111">Not supported.</span></span>    |
|<span data-ttu-id="9b6a0-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="9b6a0-112">Application</span></span> | <span data-ttu-id="9b6a0-113">Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="9b6a0-113">Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="9b6a0-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="9b6a0-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /groupLifecyclePolicies

```

## <a name="request-headers"></a><span data-ttu-id="9b6a0-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="9b6a0-115">Request headers</span></span>

| <span data-ttu-id="9b6a0-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="9b6a0-116">Name</span></span> | <span data-ttu-id="9b6a0-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="9b6a0-117">Description</span></span> |
|:---------------|:----------|
| <span data-ttu-id="9b6a0-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="9b6a0-118">Authorization</span></span> | <span data-ttu-id="9b6a0-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="9b6a0-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="9b6a0-121">Content-Type</span><span class="sxs-lookup"><span data-stu-id="9b6a0-121">Content-Type</span></span>  | <span data-ttu-id="9b6a0-122">application/json</span><span class="sxs-lookup"><span data-stu-id="9b6a0-122">application/json</span></span> |

## <a name="request-body"></a><span data-ttu-id="9b6a0-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="9b6a0-123">Request body</span></span>
<span data-ttu-id="9b6a0-124">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [groupLifecyclePolicy](../resources/grouplifecyclepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="9b6a0-124">In the request body, supply a JSON representation of [plannerPlan](../resources/grouplifecyclepolicy.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="9b6a0-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9b6a0-125">Response</span></span>

<span data-ttu-id="9b6a0-126">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [groupLifecyclePolicy](../resources/grouplifecyclepolicy.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9b6a0-126">If successful, this method returns a `201 Created` response code and [profilePhoto](../resources/grouplifecyclepolicy.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="9b6a0-127">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9b6a0-127">Example</span></span>

##### <a name="request"></a><span data-ttu-id="9b6a0-128">Solicitud</span><span class="sxs-lookup"><span data-stu-id="9b6a0-128">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "create_grouplifecyclepolicy_from_group"
}-->
```http
POST https://graph.microsoft.com/v1.0/groupLifecyclePolicies
Content-type: application/json
Content-length: 125

{
  "groupLifetimeInDays": 100,
  "managedGroupTypes": "Selected",
  "alternateNotificationEmails": "admin@contoso.com"
}
```
<span data-ttu-id="9b6a0-129">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [groupLifecyclePolicy](../resources/grouplifecyclepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="9b6a0-129">In the request body, supply a JSON representation of [plannerPlan](../resources/grouplifecyclepolicy.md) object.</span></span>
##### <a name="response"></a><span data-ttu-id="9b6a0-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9b6a0-130">Response</span></span>

<span data-ttu-id="9b6a0-p103">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="9b6a0-p103">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.groupLifecyclePolicy"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json
Content-length: 174

{
  "id": "ffffffff-ffff-ffff-ffff-ffffffffffff",
  "groupLifetimeInDays": 100,
  "managedGroupTypes": "Selected",
  "alternateNotificationEmails": "admin@contoso.com"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create groupLifecyclePolicy",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->