---
title: tipo de recurso groupLifecyclePolicy
description: Representa una directiva de ciclo de vida de un grupo de Office 365. Una directiva de ciclo de vida de grupo permite a los administradores establecer un período de expiración para los grupos. Por ejemplo, después de 180 días, un grupo expira. Cuando un grupo llega a su expiración, sus propietarios deben renovar su grupo en el intervalo de tiempo definido por el administrador. Una vez renovado, la expiración del grupo se amplía por el número de días definidos en la directiva. Por ejemplo, la nueva expiración del grupo es 180 días después de la renovación. Si no se renueva el grupo, este expira y se elimina. El grupo se puede restaurar en un período de 30 días después de la eliminación.
localization_priority: Normal
author: dkershaw10
ms.prod: groups
ms.openlocfilehash: 65cf8d5d06262f1d5700de26b4c4f62b005020d2
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27964168"
---
# <a name="grouplifecyclepolicy-resource-type"></a><span data-ttu-id="05d59-110">tipo de recurso groupLifecyclePolicy</span><span class="sxs-lookup"><span data-stu-id="05d59-110">groupLifecyclePolicy resource type</span></span>

<span data-ttu-id="05d59-111">Representa una directiva de ciclo de vida de un grupo de Office 365.</span><span class="sxs-lookup"><span data-stu-id="05d59-111">Represents a a lifecycle policy for an Office 365 group.</span></span> <span data-ttu-id="05d59-112">Una directiva de ciclo de vida de grupo permite a los administradores establecer un período de expiración para los grupos.</span><span class="sxs-lookup"><span data-stu-id="05d59-112">A group lifecycle policy allows administrators to set an expiration period for groups.</span></span> <span data-ttu-id="05d59-113">Por ejemplo, después de 180 días, un grupo expira.</span><span class="sxs-lookup"><span data-stu-id="05d59-113">For example, after 180 days, a group expires.</span></span> <span data-ttu-id="05d59-114">Cuando un grupo llega a su expiración, sus propietarios deben renovar su grupo en el intervalo de tiempo definido por el administrador.</span><span class="sxs-lookup"><span data-stu-id="05d59-114">When a group reaches its expiration, owners of the group are required to renew their group within a time interval defined by the administrator.</span></span> <span data-ttu-id="05d59-115">Una vez renovado, la expiración del grupo se amplía por el número de días definidos en la directiva.</span><span class="sxs-lookup"><span data-stu-id="05d59-115">Once renewed, the group expiration is extended by the number of days defined in the policy.</span></span> <span data-ttu-id="05d59-116">Por ejemplo, la nueva expiración del grupo es 180 días después de la renovación.</span><span class="sxs-lookup"><span data-stu-id="05d59-116">For example, the group's new expiration is 180 days after renewal.</span></span> <span data-ttu-id="05d59-117">Si no se renueva el grupo, este expira y se elimina.</span><span class="sxs-lookup"><span data-stu-id="05d59-117">If the group is not renewed, it expires and is deleted.</span></span> <span data-ttu-id="05d59-118">El grupo se puede restaurar en un período de 30 días después de la eliminación.</span><span class="sxs-lookup"><span data-stu-id="05d59-118">The group can be restored within a period of 30 days from deletion.</span></span>

## <a name="methods"></a><span data-ttu-id="05d59-119">Métodos</span><span class="sxs-lookup"><span data-stu-id="05d59-119">Methods</span></span>

| <span data-ttu-id="05d59-120">Método</span><span class="sxs-lookup"><span data-stu-id="05d59-120">Method</span></span> | <span data-ttu-id="05d59-121">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="05d59-121">Return Type</span></span> | <span data-ttu-id="05d59-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="05d59-122">Description</span></span> |
|:---------------|:--------|:----------|
|[<span data-ttu-id="05d59-123">Obtener groupLifecyclePolicy</span><span class="sxs-lookup"><span data-stu-id="05d59-123">Get groupLifecyclePolicy</span></span>](../api/grouplifecyclepolicy-get.md) | [<span data-ttu-id="05d59-124">groupLifecyclePolicy</span><span class="sxs-lookup"><span data-stu-id="05d59-124">groupLifecyclePolicy</span></span>](grouplifecyclepolicy.md) |<span data-ttu-id="05d59-125">Lee las propiedades y relaciones de un objeto groupLifecyclePolicy.</span><span class="sxs-lookup"><span data-stu-id="05d59-125">Read properties and relationships of a groupLifecyclePolicy object.</span></span>|
|[<span data-ttu-id="05d59-126">Mostrar groupLifecyclePolicies</span><span class="sxs-lookup"><span data-stu-id="05d59-126">List groupLifecyclePolicies</span></span>](../api/grouplifecyclepolicy-list.md) | <span data-ttu-id="05d59-127">Colección de [groupLifecyclePolicy](grouplifecyclepolicy.md)</span><span class="sxs-lookup"><span data-stu-id="05d59-127">[groupLifecyclePolicy](grouplifecyclepolicy.md) collection</span></span> | <span data-ttu-id="05d59-128">Muestra todos los objetos groupLifecyclePolicies.</span><span class="sxs-lookup"><span data-stu-id="05d59-128">List all the groupLifecyclePolicies.</span></span> |
|[<span data-ttu-id="05d59-129">Actualizar groupLifecyclePolicy</span><span class="sxs-lookup"><span data-stu-id="05d59-129">Update groupLifecyclePolicy</span></span>](../api/grouplifecyclepolicy-update.md) | [<span data-ttu-id="05d59-130">groupLifecyclePolicy</span><span class="sxs-lookup"><span data-stu-id="05d59-130">groupLifecyclePolicy</span></span>](grouplifecyclepolicy.md) | <span data-ttu-id="05d59-131">Actualiza un objeto groupLifecyclePolicy.</span><span class="sxs-lookup"><span data-stu-id="05d59-131">Update a groupLifecyclePolicy object.</span></span> |
|[<span data-ttu-id="05d59-132">Eliminar groupLifecyclePolicy</span><span class="sxs-lookup"><span data-stu-id="05d59-132">Delete groupLifecyclePolicy</span></span>](../api/grouplifecyclepolicy-delete.md) | <span data-ttu-id="05d59-133">Ninguno</span><span class="sxs-lookup"><span data-stu-id="05d59-133">None</span></span> | <span data-ttu-id="05d59-134">Elimina un objeto groupLifecyclePolicy.</span><span class="sxs-lookup"><span data-stu-id="05d59-134">Delete a groupLifecyclePolicy object.</span></span> |
|[<span data-ttu-id="05d59-135">Agregar un grupo a un groupLifecyclePolicy</span><span class="sxs-lookup"><span data-stu-id="05d59-135">Add a group to a groupLifecyclePolicy</span></span>](../api/grouplifecyclepolicy-addgroup.md)|<span data-ttu-id="05d59-136">Ninguno</span><span class="sxs-lookup"><span data-stu-id="05d59-136">None</span></span>| <span data-ttu-id="05d59-137">Agrega un grupo a una directiva de ciclo de vida.</span><span class="sxs-lookup"><span data-stu-id="05d59-137">Add a group to a lifecycle policy</span></span> |
|[<span data-ttu-id="05d59-138">Quitar un grupo de un groupLifecyclePolicy</span><span class="sxs-lookup"><span data-stu-id="05d59-138">Remove a group from a groupLifecyclePolicy</span></span>](../api/grouplifecyclepolicy-removegroup.md)|<span data-ttu-id="05d59-139">Ninguno</span><span class="sxs-lookup"><span data-stu-id="05d59-139">None</span></span>| <span data-ttu-id="05d59-140">Quita un grupo a una directiva de ciclo de vida.</span><span class="sxs-lookup"><span data-stu-id="05d59-140">Remove a group to a lifecycle policy.</span></span> |

## <a name="properties"></a><span data-ttu-id="05d59-141">Propiedades</span><span class="sxs-lookup"><span data-stu-id="05d59-141">Properties</span></span>

| <span data-ttu-id="05d59-142">Propiedad</span><span class="sxs-lookup"><span data-stu-id="05d59-142">Property</span></span> | <span data-ttu-id="05d59-143">Tipo</span><span class="sxs-lookup"><span data-stu-id="05d59-143">Type</span></span> | <span data-ttu-id="05d59-144">Descripción</span><span class="sxs-lookup"><span data-stu-id="05d59-144">Description</span></span> |
|:---------------|:--------|:----------|
|<span data-ttu-id="05d59-145">alternateNotificationEmails</span><span class="sxs-lookup"><span data-stu-id="05d59-145">alternateNotificationEmails</span></span>|<span data-ttu-id="05d59-146">String</span><span class="sxs-lookup"><span data-stu-id="05d59-146">String</span></span>| <span data-ttu-id="05d59-147">Lista de direcciones de correo electrónico para enviar notificaciones para grupos sin propietarios.</span><span class="sxs-lookup"><span data-stu-id="05d59-147">List of email address to send notifications for groups without owners.</span></span> <span data-ttu-id="05d59-148">Se pueden definir varias direcciones de correo electrónico separando una de la otra con un punto y coma.</span><span class="sxs-lookup"><span data-stu-id="05d59-148">Multiple email address can be defined by separating email address with a semicolon.</span></span> |
|<span data-ttu-id="05d59-149">groupLifetimeInDays</span><span class="sxs-lookup"><span data-stu-id="05d59-149">groupLifetimeInDays</span></span>|<span data-ttu-id="05d59-150">Int32</span><span class="sxs-lookup"><span data-stu-id="05d59-150">Int32</span></span>| <span data-ttu-id="05d59-151">Número de días que faltan para que un grupo expire y necesite renovarse.</span><span class="sxs-lookup"><span data-stu-id="05d59-151">Number of days before a group expires and needs to be renewed.</span></span> <span data-ttu-id="05d59-152">Una vez renovado, la expiración del grupo se amplía por el número de días definidos.</span><span class="sxs-lookup"><span data-stu-id="05d59-152">Once renewed, the group expiration is extended by the number of days defined.</span></span> |
|<span data-ttu-id="05d59-153">id</span><span class="sxs-lookup"><span data-stu-id="05d59-153">id</span></span>|<span data-ttu-id="05d59-154">Guid</span><span class="sxs-lookup"><span data-stu-id="05d59-154">Guid</span></span>| <span data-ttu-id="05d59-155">Identificador único para una directiva.</span><span class="sxs-lookup"><span data-stu-id="05d59-155">A unique identifier for a policy.</span></span> <span data-ttu-id="05d59-156">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="05d59-156">Read-only.</span></span>|
|<span data-ttu-id="05d59-157">managedGroupTypes</span><span class="sxs-lookup"><span data-stu-id="05d59-157">managedGroupTypes</span></span>|<span data-ttu-id="05d59-158">String</span><span class="sxs-lookup"><span data-stu-id="05d59-158">String</span></span>| <span data-ttu-id="05d59-159">El tipo de grupo al que se aplica la directiva de expiración.</span><span class="sxs-lookup"><span data-stu-id="05d59-159">The group type for which the expiration policy applies.</span></span> <span data-ttu-id="05d59-160">Los valores posibles son **Todos**, **Seleccionados** o **Ninguno**.</span><span class="sxs-lookup"><span data-stu-id="05d59-160">Possible values are **All**, **Selected** or **None**.</span></span> |

## <a name="relationships"></a><span data-ttu-id="05d59-161">Relaciones</span><span class="sxs-lookup"><span data-stu-id="05d59-161">Relationships</span></span>

<span data-ttu-id="05d59-162">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="05d59-162">None.</span></span>

## <a name="json-representation"></a><span data-ttu-id="05d59-163">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="05d59-163">JSON representation</span></span>

<span data-ttu-id="05d59-164">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="05d59-164">Here is a JSON representation of the resource.</span></span>

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
