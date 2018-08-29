# <a name="grouplifecyclepolicy-resource-type"></a><span data-ttu-id="eca2f-101">tipo de recurso groupLifecyclePolicy</span><span class="sxs-lookup"><span data-stu-id="eca2f-101">groupLifecyclePolicy resource type</span></span>

<span data-ttu-id="eca2f-102">Representa una directiva de ciclo de vida de un grupo de Office 365.</span><span class="sxs-lookup"><span data-stu-id="eca2f-102">Represents a a lifecycle policy for an Office 365 group.</span></span> <span data-ttu-id="eca2f-103">Una directiva de ciclo de vida de grupo permite a los administradores establecer un período de expiración para los grupos.</span><span class="sxs-lookup"><span data-stu-id="eca2f-103">A group lifecycle policy allows administrators to set an expiration period for groups.</span></span> <span data-ttu-id="eca2f-104">Por ejemplo, después de 180 días, un grupo expira.</span><span class="sxs-lookup"><span data-stu-id="eca2f-104">For example, after 180 days, a group expires.</span></span> <span data-ttu-id="eca2f-105">Cuando un grupo llega a su expiración, sus propietarios deben renovar su grupo en el intervalo de tiempo definido por el administrador.</span><span class="sxs-lookup"><span data-stu-id="eca2f-105">When a group reaches its expiration, owners of the group are required to renew their group within a time interval defined by the administrator.</span></span> <span data-ttu-id="eca2f-106">Una vez renovado, la expiración del grupo se amplía por el número de días definidos en la directiva.</span><span class="sxs-lookup"><span data-stu-id="eca2f-106">Once renewed, the group expiration is extended by the number of days defined in the policy.</span></span> <span data-ttu-id="eca2f-107">Por ejemplo, la nueva expiración del grupo es 180 días después de la renovación.</span><span class="sxs-lookup"><span data-stu-id="eca2f-107">For example, the group's new expiration is 180 days after renewal.</span></span> <span data-ttu-id="eca2f-108">Si no se renueva el grupo, este expira y se elimina.</span><span class="sxs-lookup"><span data-stu-id="eca2f-108">If the group is not renewed, it expires and is deleted.</span></span> <span data-ttu-id="eca2f-109">El grupo se puede restaurar en un período de 30 días después de la eliminación.</span><span class="sxs-lookup"><span data-stu-id="eca2f-109">The group can be restored within a period of 30 days from deletion.</span></span>

## <a name="methods"></a><span data-ttu-id="eca2f-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="eca2f-110">Methods</span></span>

| <span data-ttu-id="eca2f-111">Método</span><span class="sxs-lookup"><span data-stu-id="eca2f-111">Method</span></span> | <span data-ttu-id="eca2f-112">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="eca2f-112">Return Type</span></span> | <span data-ttu-id="eca2f-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="eca2f-113">Description</span></span> |
|:---------------|:--------|:----------|
|[<span data-ttu-id="eca2f-114">Obtener groupLifecyclePolicy</span><span class="sxs-lookup"><span data-stu-id="eca2f-114">Get groupLifecyclePolicy</span></span>](../api/grouplifecyclepolicy_get.md) | [<span data-ttu-id="eca2f-115">groupLifecyclePolicy</span><span class="sxs-lookup"><span data-stu-id="eca2f-115">groupLifecyclePolicy</span></span>](grouplifecyclepolicy.md) |<span data-ttu-id="eca2f-116">Lee las propiedades y relaciones de un objeto groupLifecyclePolicy.</span><span class="sxs-lookup"><span data-stu-id="eca2f-116">Read properties and relationships of a groupLifecyclePolicy object.</span></span>|
|[<span data-ttu-id="eca2f-117">Mostrar groupLifecyclePolicies</span><span class="sxs-lookup"><span data-stu-id="eca2f-117">List groupLifecyclePolicies</span></span>](../api/grouplifecyclepolicy_list.md) | <span data-ttu-id="eca2f-118">Colección de [groupLifecyclePolicy](grouplifecyclepolicy.md)</span><span class="sxs-lookup"><span data-stu-id="eca2f-118">[groupLifecyclePolicy](grouplifecyclepolicy.md) collection</span></span> | <span data-ttu-id="eca2f-119">Muestra todos los objetos groupLifecyclePolicies.</span><span class="sxs-lookup"><span data-stu-id="eca2f-119">List all the groupLifecyclePolicies.</span></span> |
|[<span data-ttu-id="eca2f-120">Actualizar groupLifecyclePolicy</span><span class="sxs-lookup"><span data-stu-id="eca2f-120">Update groupLifecyclePolicy</span></span>](../api/grouplifecyclepolicy_update.md) | [<span data-ttu-id="eca2f-121">groupLifecyclePolicy</span><span class="sxs-lookup"><span data-stu-id="eca2f-121">groupLifecyclePolicy</span></span>](grouplifecyclepolicy.md) | <span data-ttu-id="eca2f-122">Actualiza un objeto groupLifecyclePolicy.</span><span class="sxs-lookup"><span data-stu-id="eca2f-122">Update a groupLifecyclePolicy object.</span></span> |
|[<span data-ttu-id="eca2f-123">Eliminar groupLifecyclePolicy</span><span class="sxs-lookup"><span data-stu-id="eca2f-123">Delete groupLifecyclePolicy</span></span>](../api/grouplifecyclepolicy_delete.md) | <span data-ttu-id="eca2f-124">Ninguno</span><span class="sxs-lookup"><span data-stu-id="eca2f-124">None</span></span> | <span data-ttu-id="eca2f-125">Elimina un objeto groupLifecyclePolicy.</span><span class="sxs-lookup"><span data-stu-id="eca2f-125">Delete a groupLifecyclePolicy object.</span></span> |
|[<span data-ttu-id="eca2f-126">Agregar un grupo a un groupLifecyclePolicy</span><span class="sxs-lookup"><span data-stu-id="eca2f-126">Add a group to a groupLifecyclePolicy</span></span>](../api/grouplifecyclepolicy_addgroup.md)|<span data-ttu-id="eca2f-127">Ninguno</span><span class="sxs-lookup"><span data-stu-id="eca2f-127">None</span></span>| <span data-ttu-id="eca2f-128">Agrega un grupo a una directiva de ciclo de vida.</span><span class="sxs-lookup"><span data-stu-id="eca2f-128">Add a group to a lifecycle policy</span></span> |
|[<span data-ttu-id="eca2f-129">Quitar un grupo de un groupLifecyclePolicy</span><span class="sxs-lookup"><span data-stu-id="eca2f-129">Remove a group from a groupLifecyclePolicy</span></span>](../api/grouplifecyclepolicy_removegroup.md)|<span data-ttu-id="eca2f-130">Ninguno</span><span class="sxs-lookup"><span data-stu-id="eca2f-130">None</span></span>| <span data-ttu-id="eca2f-131">Quita un grupo a una directiva de ciclo de vida.</span><span class="sxs-lookup"><span data-stu-id="eca2f-131">Remove a group to a lifecycle policy.</span></span> |

## <a name="properties"></a><span data-ttu-id="eca2f-132">Propiedades</span><span class="sxs-lookup"><span data-stu-id="eca2f-132">Properties</span></span>

| <span data-ttu-id="eca2f-133">Propiedad</span><span class="sxs-lookup"><span data-stu-id="eca2f-133">Property</span></span> | <span data-ttu-id="eca2f-134">Tipo</span><span class="sxs-lookup"><span data-stu-id="eca2f-134">Type</span></span> | <span data-ttu-id="eca2f-135">Descripción</span><span class="sxs-lookup"><span data-stu-id="eca2f-135">Description</span></span> |
|:---------------|:--------|:----------|
|<span data-ttu-id="eca2f-136">alternateNotificationEmails</span><span class="sxs-lookup"><span data-stu-id="eca2f-136">alternateNotificationEmails</span></span>|<span data-ttu-id="eca2f-137">String</span><span class="sxs-lookup"><span data-stu-id="eca2f-137">String</span></span>| <span data-ttu-id="eca2f-138">Lista de direcciones de correo electrónico para enviar notificaciones para grupos sin propietarios.</span><span class="sxs-lookup"><span data-stu-id="eca2f-138">List of email address to send notifications for groups without owners.</span></span> <span data-ttu-id="eca2f-139">Se pueden definir varias direcciones de correo electrónico separando una de la otra con un punto y coma.</span><span class="sxs-lookup"><span data-stu-id="eca2f-139">Multiple email address can be defined by separating email address with a semicolon.</span></span> |
|<span data-ttu-id="eca2f-140">groupLifetimeInDays</span><span class="sxs-lookup"><span data-stu-id="eca2f-140">groupLifetimeInDays</span></span>|<span data-ttu-id="eca2f-141">Int32</span><span class="sxs-lookup"><span data-stu-id="eca2f-141">Int32</span></span>| <span data-ttu-id="eca2f-142">Número de días que faltan para que un grupo expire y necesite renovarse.</span><span class="sxs-lookup"><span data-stu-id="eca2f-142">Number of days before a group expires and needs to be renewed.</span></span> <span data-ttu-id="eca2f-143">Una vez renovado, la expiración del grupo se amplía por el número de días definidos.</span><span class="sxs-lookup"><span data-stu-id="eca2f-143">Once renewed, the group expiration is extended by the number of days defined.</span></span> |
|<span data-ttu-id="eca2f-144">id</span><span class="sxs-lookup"><span data-stu-id="eca2f-144">id</span></span>|<span data-ttu-id="eca2f-145">Guid</span><span class="sxs-lookup"><span data-stu-id="eca2f-145">Guid</span></span>| <span data-ttu-id="eca2f-146">Identificador único para una directiva.</span><span class="sxs-lookup"><span data-stu-id="eca2f-146">A unique identifier for a policy.</span></span> <span data-ttu-id="eca2f-147">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="eca2f-147">Read-only.</span></span>|
|<span data-ttu-id="eca2f-148">managedGroupTypes</span><span class="sxs-lookup"><span data-stu-id="eca2f-148">managedGroupTypes</span></span>|<span data-ttu-id="eca2f-149">String</span><span class="sxs-lookup"><span data-stu-id="eca2f-149">String</span></span>| <span data-ttu-id="eca2f-150">El tipo de grupo al que se aplica la directiva de expiración.</span><span class="sxs-lookup"><span data-stu-id="eca2f-150">The group type for which the expiration policy applies.</span></span> <span data-ttu-id="eca2f-151">Los valores posibles son **Todos**, **Seleccionados** o **Ninguno**.</span><span class="sxs-lookup"><span data-stu-id="eca2f-151">Possible values are **All**, **Selected** or **None**.</span></span> |

## <a name="relationships"></a><span data-ttu-id="eca2f-152">Relaciones</span><span class="sxs-lookup"><span data-stu-id="eca2f-152">Relationships</span></span>

<span data-ttu-id="eca2f-153">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="eca2f-153">None.</span></span>

## <a name="json-representation"></a><span data-ttu-id="eca2f-154">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="eca2f-154">JSON representation</span></span>

<span data-ttu-id="eca2f-155">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="eca2f-155">Here is a JSON representation of the resource.</span></span>

<!--{
  "blockType": "resource",
  "optionalProperties": [],
  "keyProperty": "id",
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.groupLifecyclePolicy"
}-->

```json
{
  "alternateNotificationEmails": "String",
  "groupLifetimeInDays": 180,
  "id": "Guid (identifier)",
  "managedGroupTypes": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "groupLifecyclePolicy resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->