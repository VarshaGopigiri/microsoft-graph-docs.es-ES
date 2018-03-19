# <a name="update-grouplifecyclepolicy"></a><span data-ttu-id="01c09-101">Actualizar groupLifecyclePolicy</span><span class="sxs-lookup"><span data-stu-id="01c09-101">Update groupLifecyclePolicy</span></span>

<span data-ttu-id="01c09-102">Actualiza las propiedades de un objeto groupLifecyclePolicy[tipo de recurso groupLifecyclePolicy](../resources/grouplifecyclepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="01c09-102">Update the properties of a groupLifecyclePolicy[groupLifecyclePolicy resource type](../resources/grouplifecyclepolicy.md) object.</span></span>

## <a name="permissions"></a><span data-ttu-id="01c09-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="01c09-103">Permissions</span></span>

<span data-ttu-id="01c09-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="01c09-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>
 
|<span data-ttu-id="01c09-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="01c09-106">Permission type</span></span>      | <span data-ttu-id="01c09-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="01c09-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="01c09-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="01c09-108">Delegated (work or school account)</span></span> | <span data-ttu-id="01c09-109">Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="01c09-109">Directory.ReadWrite.All</span></span>    |
|<span data-ttu-id="01c09-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="01c09-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="01c09-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="01c09-111">Not supported.</span></span>    |
|<span data-ttu-id="01c09-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="01c09-112">Application</span></span> | <span data-ttu-id="01c09-113">Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="01c09-113">Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="01c09-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="01c09-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /groupLifecyclePolicies/{id}
```
## <a name="optional-request-headers"></a><span data-ttu-id="01c09-115">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="01c09-115">Optional request headers</span></span>
| <span data-ttu-id="01c09-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="01c09-116">Name</span></span> | <span data-ttu-id="01c09-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="01c09-117">Description</span></span> |
|:-----------|:-----------|
| <span data-ttu-id="01c09-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="01c09-118">Authorization</span></span> | <span data-ttu-id="01c09-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="01c09-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="01c09-121">Content-Type</span><span class="sxs-lookup"><span data-stu-id="01c09-121">Content-Type</span></span>  | <span data-ttu-id="01c09-122">application/json</span><span class="sxs-lookup"><span data-stu-id="01c09-122">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="01c09-123">Cuerpo de solicitud</span><span class="sxs-lookup"><span data-stu-id="01c09-123">Request body</span></span>

<span data-ttu-id="01c09-124">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse.</span><span class="sxs-lookup"><span data-stu-id="01c09-124">In the request body, supply the values for relevant fields that should be updated.</span></span> <span data-ttu-id="01c09-125">Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantienen los valores anteriores o se recalculan según los cambios efectuados en otros valores de propiedad.</span><span class="sxs-lookup"><span data-stu-id="01c09-125">Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values.</span></span> <span data-ttu-id="01c09-126">Para obtener el mejor rendimiento no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="01c09-126">For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="01c09-127">Propiedad</span><span class="sxs-lookup"><span data-stu-id="01c09-127">Property</span></span> | <span data-ttu-id="01c09-128">Tipo</span><span class="sxs-lookup"><span data-stu-id="01c09-128">Type</span></span> | <span data-ttu-id="01c09-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="01c09-129">Description</span></span> |
|:---------------|:--------|:----------|
|<span data-ttu-id="01c09-130">alternateNotificationEmails</span><span class="sxs-lookup"><span data-stu-id="01c09-130">alternateNotificationEmails</span></span>|<span data-ttu-id="01c09-131">String</span><span class="sxs-lookup"><span data-stu-id="01c09-131">String</span></span>| <span data-ttu-id="01c09-132">Lista de direcciones de correo electrónico para enviar notificaciones para grupos sin propietarios.</span><span class="sxs-lookup"><span data-stu-id="01c09-132">List of email address to send notifications for groups without owners.</span></span> <span data-ttu-id="01c09-133">Se pueden definir varias direcciones de correo electrónico separando una de la otra con un punto y coma.</span><span class="sxs-lookup"><span data-stu-id="01c09-133">Multiple email address can be defined by separating email address with a semicolon.</span></span> |
|<span data-ttu-id="01c09-134">groupLifetimeInDays</span><span class="sxs-lookup"><span data-stu-id="01c09-134">groupLifetimeInDays</span></span>|<span data-ttu-id="01c09-135">Int32</span><span class="sxs-lookup"><span data-stu-id="01c09-135">Int32</span></span>| <span data-ttu-id="01c09-136">Número de días que faltan para que un grupo expire y necesite renovarse.</span><span class="sxs-lookup"><span data-stu-id="01c09-136">Number of days before a group expires and needs to be renewed.</span></span> <span data-ttu-id="01c09-137">Una vez renovado, la expiración del grupo se amplía por el número de días definidos.</span><span class="sxs-lookup"><span data-stu-id="01c09-137">Once renewed, the group expiration is extended by the number of days defined.</span></span> |
|<span data-ttu-id="01c09-138">managedGroupTypes</span><span class="sxs-lookup"><span data-stu-id="01c09-138">managedGroupTypes</span></span>|<span data-ttu-id="01c09-139">String</span><span class="sxs-lookup"><span data-stu-id="01c09-139">String</span></span>| <span data-ttu-id="01c09-140">El tipo de grupo al que se aplica la directiva de expiración.</span><span class="sxs-lookup"><span data-stu-id="01c09-140">The group type for which the expiration policy applies.</span></span> <span data-ttu-id="01c09-141">Los valores posibles son **Todos**, **Seleccionados** o **Ninguno**.</span><span class="sxs-lookup"><span data-stu-id="01c09-141">Possible values are **All**, **Selected** or **None**.</span></span> |

## <a name="response"></a><span data-ttu-id="01c09-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="01c09-142">Response</span></span>

<span data-ttu-id="01c09-143">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [groupLifecyclePolicy](../resources/grouplifecyclepolicy.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="01c09-143">If successful, this method returns a `200 OK` response code and updated [Chart](../resources/grouplifecyclepolicy.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="01c09-144">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="01c09-144">Example</span></span>

##### <a name="request"></a><span data-ttu-id="01c09-145">Solicitud</span><span class="sxs-lookup"><span data-stu-id="01c09-145">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "update_grouplifecyclepolicy"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/groupLifecyclePolicies/{id}
Content-type: application/json
Content-length: 125

{
  "groupLifetimeInDays": 180,
  "managedGroupTypes": "Selected",
  "alternateNotificationEmails": "admin@contoso.com"
}
```
##### <a name="response"></a><span data-ttu-id="01c09-146">Respuesta</span><span class="sxs-lookup"><span data-stu-id="01c09-146">Response</span></span>
<span data-ttu-id="01c09-147">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar.</span><span class="sxs-lookup"><span data-stu-id="01c09-147">Note: The response object shown here may be truncated for brevity.</span></span> 
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.groupLifecyclePolicy"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 146

{
  "id": "id-value",
  "groupLifetimeInDays": 180,
  "managedGroupTypes": "Selected",
  "alternateNotificationEmails": "admin@contoso.com"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update groupLifecyclePolicy",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->