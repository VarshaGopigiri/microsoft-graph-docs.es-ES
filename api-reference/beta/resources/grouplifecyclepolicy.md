---
title: tipo de recurso groupLifecyclePolicy
description: Representa una directiva de ciclo de vida de un grupo de Office 365. Una directiva de ciclo de vida de grupo permite a los administradores establecer un período de expiración para los grupos. Por ejemplo, después de 180 días, un grupo expira. Cuando un grupo llega a su expiración, sus propietarios deben renovar su grupo en el intervalo de tiempo definido por el administrador. Una vez renovado, la expiración del grupo se amplía por el número de días definidos en la directiva. Por ejemplo, la nueva expiración del grupo es 180 días después de la renovación. Si no se renueva el grupo, este expira y se elimina. El grupo se puede restaurar en un período de 30 días después de la eliminación.
localization_priority: Normal
ms.openlocfilehash: 271a3421599eaa58487cc7917c8dfaf4c382050d
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27861687"
---
# <a name="grouplifecyclepolicy-resource-type"></a><span data-ttu-id="ed24f-110">tipo de recurso groupLifecyclePolicy</span><span class="sxs-lookup"><span data-stu-id="ed24f-110">groupLifecyclePolicy resource type</span></span>

<span data-ttu-id="ed24f-111">Representa una directiva de ciclo de vida de un grupo de Office 365.</span><span class="sxs-lookup"><span data-stu-id="ed24f-111">Represents a a lifecycle policy for an Office 365 group.</span></span> <span data-ttu-id="ed24f-112">Una directiva de ciclo de vida de grupo permite a los administradores establecer un período de expiración para los grupos.</span><span class="sxs-lookup"><span data-stu-id="ed24f-112">A group lifecycle policy allows administrators to set an expiration period for groups.</span></span> <span data-ttu-id="ed24f-113">Por ejemplo, después de 180 días, un grupo expira.</span><span class="sxs-lookup"><span data-stu-id="ed24f-113">For example, after 180 days, a group expires.</span></span> <span data-ttu-id="ed24f-114">Cuando un grupo llega a su expiración, sus propietarios deben renovar su grupo en el intervalo de tiempo definido por el administrador.</span><span class="sxs-lookup"><span data-stu-id="ed24f-114">When a group reaches its expiration, owners of the group are required to renew their group within a time interval defined by the administrator.</span></span> <span data-ttu-id="ed24f-115">Una vez renovado, la expiración del grupo se amplía por el número de días definidos en la directiva.</span><span class="sxs-lookup"><span data-stu-id="ed24f-115">Once renewed, the group expiration is extended by the number of days defined in the policy.</span></span> <span data-ttu-id="ed24f-116">Por ejemplo, la nueva expiración del grupo es 180 días después de la renovación.</span><span class="sxs-lookup"><span data-stu-id="ed24f-116">For example, the group's new expiration is 180 days after renewal.</span></span> <span data-ttu-id="ed24f-117">Si no se renueva el grupo, este expira y se elimina.</span><span class="sxs-lookup"><span data-stu-id="ed24f-117">If the group is not renewed, it expires and is deleted.</span></span> <span data-ttu-id="ed24f-118">El grupo se puede restaurar en un período de 30 días después de la eliminación.</span><span class="sxs-lookup"><span data-stu-id="ed24f-118">The group can be restored within a period of 30 days from deletion.</span></span>

## <a name="methods"></a><span data-ttu-id="ed24f-119">Métodos</span><span class="sxs-lookup"><span data-stu-id="ed24f-119">Methods</span></span>

| <span data-ttu-id="ed24f-120">Método</span><span class="sxs-lookup"><span data-stu-id="ed24f-120">Method</span></span> | <span data-ttu-id="ed24f-121">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ed24f-121">Return Type</span></span> | <span data-ttu-id="ed24f-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="ed24f-122">Description</span></span> |
|:---------------|:--------|:----------|
|[<span data-ttu-id="ed24f-123">Obtener groupLifecyclePolicy</span><span class="sxs-lookup"><span data-stu-id="ed24f-123">Get groupLifecyclePolicy</span></span>](../api/grouplifecyclepolicy-get.md) | [<span data-ttu-id="ed24f-124">groupLifecyclePolicy</span><span class="sxs-lookup"><span data-stu-id="ed24f-124">groupLifecyclePolicy</span></span>](grouplifecyclepolicy.md) |<span data-ttu-id="ed24f-125">Lee las propiedades y relaciones de un objeto groupLifecyclePolicy.</span><span class="sxs-lookup"><span data-stu-id="ed24f-125">Read properties and relationships of a groupLifecyclePolicy object.</span></span>|
|[<span data-ttu-id="ed24f-126">Mostrar groupLifecyclePolicies</span><span class="sxs-lookup"><span data-stu-id="ed24f-126">List groupLifecyclePolicies</span></span>](../api/grouplifecyclepolicy-list.md) | <span data-ttu-id="ed24f-127">Colección de [groupLifecyclePolicy](grouplifecyclepolicy.md)</span><span class="sxs-lookup"><span data-stu-id="ed24f-127">[groupLifecyclePolicy](grouplifecyclepolicy.md) collection</span></span> | <span data-ttu-id="ed24f-128">Muestra todos los objetos groupLifecyclePolicies.</span><span class="sxs-lookup"><span data-stu-id="ed24f-128">List all the groupLifecyclePolicies.</span></span> |
|[<span data-ttu-id="ed24f-129">Actualizar groupLifecyclePolicy</span><span class="sxs-lookup"><span data-stu-id="ed24f-129">Update groupLifecyclePolicy</span></span>](../api/grouplifecyclepolicy-update.md) | [<span data-ttu-id="ed24f-130">groupLifecyclePolicy</span><span class="sxs-lookup"><span data-stu-id="ed24f-130">groupLifecyclePolicy</span></span>](grouplifecyclepolicy.md) | <span data-ttu-id="ed24f-131">Actualiza un objeto groupLifecyclePolicy.</span><span class="sxs-lookup"><span data-stu-id="ed24f-131">Update a groupLifecyclePolicy object.</span></span> |
|[<span data-ttu-id="ed24f-132">Eliminar groupLifecyclePolicy</span><span class="sxs-lookup"><span data-stu-id="ed24f-132">Delete groupLifecyclePolicy</span></span>](../api/grouplifecyclepolicy-delete.md) | <span data-ttu-id="ed24f-133">Ninguno</span><span class="sxs-lookup"><span data-stu-id="ed24f-133">None</span></span> | <span data-ttu-id="ed24f-134">Elimina un objeto groupLifecyclePolicy.</span><span class="sxs-lookup"><span data-stu-id="ed24f-134">Delete a groupLifecyclePolicy object.</span></span> |
|[<span data-ttu-id="ed24f-135">Agregar un grupo a un groupLifecyclePolicy</span><span class="sxs-lookup"><span data-stu-id="ed24f-135">Add a group to a groupLifecyclePolicy</span></span>](../api/grouplifecyclepolicy-addgroup.md)|<span data-ttu-id="ed24f-136">Ninguno</span><span class="sxs-lookup"><span data-stu-id="ed24f-136">None</span></span>| <span data-ttu-id="ed24f-137">Agrega un grupo a una directiva de ciclo de vida.</span><span class="sxs-lookup"><span data-stu-id="ed24f-137">Add a group to a lifecycle policy</span></span> |
|[<span data-ttu-id="ed24f-138">Quitar un grupo de un groupLifecyclePolicy</span><span class="sxs-lookup"><span data-stu-id="ed24f-138">Remove a group from a groupLifecyclePolicy</span></span>](../api/grouplifecyclepolicy-removegroup.md)|<span data-ttu-id="ed24f-139">Ninguno</span><span class="sxs-lookup"><span data-stu-id="ed24f-139">None</span></span>| <span data-ttu-id="ed24f-140">Quita un grupo a una directiva de ciclo de vida.</span><span class="sxs-lookup"><span data-stu-id="ed24f-140">Remove a group to a lifecycle policy.</span></span> |
|[<span data-ttu-id="ed24f-141">Renovar un grupo</span><span class="sxs-lookup"><span data-stu-id="ed24f-141">Renew a group</span></span>](../api/grouplifecyclepolicy-renewgroup.md)|<span data-ttu-id="ed24f-142">Ninguno</span><span class="sxs-lookup"><span data-stu-id="ed24f-142">None</span></span>| <span data-ttu-id="ed24f-143">Renovar la fecha de caducidad de un grupo.</span><span class="sxs-lookup"><span data-stu-id="ed24f-143">Renew a group's expiration date.</span></span> |

## <a name="properties"></a><span data-ttu-id="ed24f-144">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ed24f-144">Properties</span></span>

| <span data-ttu-id="ed24f-145">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ed24f-145">Property</span></span> | <span data-ttu-id="ed24f-146">Tipo</span><span class="sxs-lookup"><span data-stu-id="ed24f-146">Type</span></span> | <span data-ttu-id="ed24f-147">Descripción</span><span class="sxs-lookup"><span data-stu-id="ed24f-147">Description</span></span> |
|:---------------|:--------|:----------|
|<span data-ttu-id="ed24f-148">alternateNotificationEmails</span><span class="sxs-lookup"><span data-stu-id="ed24f-148">alternateNotificationEmails</span></span>|<span data-ttu-id="ed24f-149">String</span><span class="sxs-lookup"><span data-stu-id="ed24f-149">String</span></span>| <span data-ttu-id="ed24f-150">Lista de direcciones de correo electrónico para enviar notificaciones para grupos sin propietarios.</span><span class="sxs-lookup"><span data-stu-id="ed24f-150">List of email address to send notifications for groups without owners.</span></span> <span data-ttu-id="ed24f-151">Se pueden definir varias direcciones de correo electrónico separando una de la otra con un punto y coma.</span><span class="sxs-lookup"><span data-stu-id="ed24f-151">Multiple email address can be defined by separating email address with a semicolon.</span></span> |
|<span data-ttu-id="ed24f-152">groupLifetimeInDays</span><span class="sxs-lookup"><span data-stu-id="ed24f-152">groupLifetimeInDays</span></span>|<span data-ttu-id="ed24f-153">Int32</span><span class="sxs-lookup"><span data-stu-id="ed24f-153">Int32</span></span>| <span data-ttu-id="ed24f-154">Número de días que faltan para que un grupo expire y necesite renovarse.</span><span class="sxs-lookup"><span data-stu-id="ed24f-154">Number of days before a group expires and needs to be renewed.</span></span> <span data-ttu-id="ed24f-155">Una vez renovado, la expiración del grupo se amplía por el número de días definidos.</span><span class="sxs-lookup"><span data-stu-id="ed24f-155">Once renewed, the group expiration is extended by the number of days defined.</span></span> |
|<span data-ttu-id="ed24f-156">id</span><span class="sxs-lookup"><span data-stu-id="ed24f-156">id</span></span>|<span data-ttu-id="ed24f-157">Guid</span><span class="sxs-lookup"><span data-stu-id="ed24f-157">Guid</span></span>| <span data-ttu-id="ed24f-158">Identificador único para una directiva.</span><span class="sxs-lookup"><span data-stu-id="ed24f-158">A unique identifier for a policy.</span></span> <span data-ttu-id="ed24f-159">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="ed24f-159">Read-only.</span></span>|
|<span data-ttu-id="ed24f-160">managedGroupTypes</span><span class="sxs-lookup"><span data-stu-id="ed24f-160">managedGroupTypes</span></span>|<span data-ttu-id="ed24f-161">String</span><span class="sxs-lookup"><span data-stu-id="ed24f-161">String</span></span>| <span data-ttu-id="ed24f-162">El tipo de grupo al que se aplica la directiva de expiración.</span><span class="sxs-lookup"><span data-stu-id="ed24f-162">The group type for which the expiration policy applies.</span></span> <span data-ttu-id="ed24f-163">Los valores posibles son **Todos**, **Seleccionados** o **Ninguno**.</span><span class="sxs-lookup"><span data-stu-id="ed24f-163">Possible values are **All**, **Selected** or **None**.</span></span> |

## <a name="relationships"></a><span data-ttu-id="ed24f-164">Relaciones</span><span class="sxs-lookup"><span data-stu-id="ed24f-164">Relationships</span></span>

<span data-ttu-id="ed24f-165">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="ed24f-165">None.</span></span>

## <a name="json-representation"></a><span data-ttu-id="ed24f-166">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="ed24f-166">JSON representation</span></span>

<span data-ttu-id="ed24f-167">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="ed24f-167">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
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
