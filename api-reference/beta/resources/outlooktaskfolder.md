---
title: tipo de recurso outlookTaskFolder
description: 'Una carpeta que contiene las tareas de Outlook (colección de objetos de outlookTask). '
ms.openlocfilehash: e3fb9d73dbd9458048749331d14f933d838d4243
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088655"
---
# <a name="outlooktaskfolder-resource-type"></a><span data-ttu-id="04768-103">tipo de recurso outlookTaskFolder</span><span class="sxs-lookup"><span data-stu-id="04768-103">outlookTaskFolder resource type</span></span>

> <span data-ttu-id="04768-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="04768-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="04768-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="04768-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="04768-106">Una carpeta que contiene las tareas de Outlook (colección de objetos de [outlookTask](outlooktask.md) ).</span><span class="sxs-lookup"><span data-stu-id="04768-106">A folder that contains Outlook tasks (collection of [outlookTask](outlooktask.md) objects).</span></span> 

<span data-ttu-id="04768-107">En Outlook, el grupo de tareas de forma predeterminada, `My Tasks`, contiene una carpeta de tareas predeterminada, `Tasks`, para el buzón del usuario.</span><span class="sxs-lookup"><span data-stu-id="04768-107">In Outlook, the default task group, `My Tasks`, contains a default task folder, `Tasks`, for the user's mailbox.</span></span> <span data-ttu-id="04768-108">No se puede cambiar el nombre o eliminar estos grupo de tareas de forma predeterminada y la carpeta, pero puede crear otros grupos de tareas y carpetas de tareas.</span><span class="sxs-lookup"><span data-stu-id="04768-108">You cannot rename or delete these default task group and folder, but you can create additional task groups and task folders.</span></span>


## <a name="methods"></a><span data-ttu-id="04768-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="04768-109">Methods</span></span>

| <span data-ttu-id="04768-110">Método</span><span class="sxs-lookup"><span data-stu-id="04768-110">Method</span></span>           | <span data-ttu-id="04768-111">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="04768-111">Return Type</span></span>    |<span data-ttu-id="04768-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="04768-112">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="04768-113">Obtener outlookTaskFolder</span><span class="sxs-lookup"><span data-stu-id="04768-113">Get outlookTaskFolder</span></span>](../api/outlooktaskfolder-get.md) | [<span data-ttu-id="04768-114">outlookTaskFolder</span><span class="sxs-lookup"><span data-stu-id="04768-114">outlookTaskFolder</span></span>](outlooktaskfolder.md) |<span data-ttu-id="04768-115">Obtener las propiedades y relaciones de la carpeta de tareas de Outlook especificada.</span><span class="sxs-lookup"><span data-stu-id="04768-115">Get the properties and relationships of the specified Outlook task folder.</span></span>|
|[<span data-ttu-id="04768-116">Crear outlookTask</span><span class="sxs-lookup"><span data-stu-id="04768-116">Create outlookTask</span></span>](../api/outlooktaskfolder-post-tasks.md) |[<span data-ttu-id="04768-117">outlookTask</span><span class="sxs-lookup"><span data-stu-id="04768-117">outlookTask</span></span>](outlooktask.md)| <span data-ttu-id="04768-118">Crear una tarea de Outlook en la carpeta de la tarea especificada.</span><span class="sxs-lookup"><span data-stu-id="04768-118">Create an Outlook task in the specified task folder.</span></span>|
|[<span data-ttu-id="04768-119">Enumerar tareas</span><span class="sxs-lookup"><span data-stu-id="04768-119">List tasks</span></span>](../api/outlooktaskfolder-list-tasks.md) |<span data-ttu-id="04768-120">colección de [outlookTask](outlooktask.md)</span><span class="sxs-lookup"><span data-stu-id="04768-120">[outlookTask](outlooktask.md) collection</span></span>| <span data-ttu-id="04768-121">Obtenga todas las tareas de Outlook en la carpeta especificada.</span><span class="sxs-lookup"><span data-stu-id="04768-121">Get all the Outlook tasks in the specified folder.</span></span>|
|[<span data-ttu-id="04768-122">Update</span><span class="sxs-lookup"><span data-stu-id="04768-122">Update</span></span>](../api/outlooktaskfolder-update.md) | [<span data-ttu-id="04768-123">outlookTaskFolder</span><span class="sxs-lookup"><span data-stu-id="04768-123">outlookTaskFolder</span></span>](outlooktaskfolder.md)   |<span data-ttu-id="04768-124">Actualizar las propiedades modificables de una carpeta de tarea de Outlook.</span><span class="sxs-lookup"><span data-stu-id="04768-124">Update the writable properties of an Outlook task folder.</span></span> |
|[<span data-ttu-id="04768-125">Delete</span><span class="sxs-lookup"><span data-stu-id="04768-125">Delete</span></span>](../api/outlooktaskfolder-delete.md) | <span data-ttu-id="04768-126">Ninguno</span><span class="sxs-lookup"><span data-stu-id="04768-126">None</span></span> |<span data-ttu-id="04768-127">Elimine la carpeta de tareas de Outlook especificada.</span><span class="sxs-lookup"><span data-stu-id="04768-127">Delete the specified Outlook task folder.</span></span>|
|<span data-ttu-id="04768-128">**Propiedades extendidas**</span><span class="sxs-lookup"><span data-stu-id="04768-128">**Extended properties**</span></span>| | |
|[<span data-ttu-id="04768-129">Crear propiedad extendida de valor único</span><span class="sxs-lookup"><span data-stu-id="04768-129">Create single-value extended property</span></span>](../api/singlevaluelegacyextendedproperty-post-singlevalueextendedproperties.md) |[<span data-ttu-id="04768-130">outlookTaskFolder</span><span class="sxs-lookup"><span data-stu-id="04768-130">outlookTaskFolder</span></span>](outlooktaskfolder.md)  |<span data-ttu-id="04768-131">Cree una o más propiedades extendidas de valor único en una carpeta de tareas de Outlook nueva o existente.</span><span class="sxs-lookup"><span data-stu-id="04768-131">Create one or more single-value extended properties in a new or existing Outlook task folder.</span></span>   |
|[<span data-ttu-id="04768-132">Obtener la carpeta de tareas con la propiedad extendida de valor único</span><span class="sxs-lookup"><span data-stu-id="04768-132">Get task folder with single-value extended property</span></span>](../api/singlevaluelegacyextendedproperty-get.md)  | [<span data-ttu-id="04768-133">outlookTaskFolder</span><span class="sxs-lookup"><span data-stu-id="04768-133">outlookTaskFolder</span></span>](outlooktaskfolder.md) | <span data-ttu-id="04768-134">Obtener las carpetas de tareas de Outlook que contienen un valor único propiedad extendida mediante el uso de `$expand` o `$filter`.</span><span class="sxs-lookup"><span data-stu-id="04768-134">Get Outlook task folders that contain a single-value extended property by using `$expand` or `$filter`.</span></span> |
|[<span data-ttu-id="04768-135">Crear propiedad extendida de varios valores</span><span class="sxs-lookup"><span data-stu-id="04768-135">Create multi-value extended property</span></span>](../api/multivaluelegacyextendedproperty-post-multivalueextendedproperties.md) | [<span data-ttu-id="04768-136">outlookTaskFolder</span><span class="sxs-lookup"><span data-stu-id="04768-136">outlookTaskFolder</span></span>](outlooktaskfolder.md) | <span data-ttu-id="04768-137">Cree una o más propiedades extendidas de varios valores en una carpeta de tareas de Outlook nueva o existente.</span><span class="sxs-lookup"><span data-stu-id="04768-137">Create one or more multi-value extended properties in a new or existing Outlook task folder.</span></span>  |
|[<span data-ttu-id="04768-138">Obtener la carpeta de tareas con varios valores de propiedad extendida</span><span class="sxs-lookup"><span data-stu-id="04768-138">Get task folder with multi-value extended property</span></span>](../api/multivaluelegacyextendedproperty-get.md)  | [<span data-ttu-id="04768-139">outlookTaskFolder</span><span class="sxs-lookup"><span data-stu-id="04768-139">outlookTaskFolder</span></span>](outlooktaskfolder.md) | <span data-ttu-id="04768-140">Obtener una carpeta de tarea de Outlook que contiene una propiedad extendida de varios valor mediante el uso de `$expand`.</span><span class="sxs-lookup"><span data-stu-id="04768-140">Get an Outlook task folder that contains a multi-value extended property by using `$expand`.</span></span> |

## <a name="properties"></a><span data-ttu-id="04768-141">Propiedades</span><span class="sxs-lookup"><span data-stu-id="04768-141">Properties</span></span>
| <span data-ttu-id="04768-142">Propiedad</span><span class="sxs-lookup"><span data-stu-id="04768-142">Property</span></span>     | <span data-ttu-id="04768-143">Tipo</span><span class="sxs-lookup"><span data-stu-id="04768-143">Type</span></span>   |<span data-ttu-id="04768-144">Descripción</span><span class="sxs-lookup"><span data-stu-id="04768-144">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="04768-145">changeKey</span><span class="sxs-lookup"><span data-stu-id="04768-145">changeKey</span></span>|<span data-ttu-id="04768-146">String</span><span class="sxs-lookup"><span data-stu-id="04768-146">String</span></span>|<span data-ttu-id="04768-147">La versión de la carpeta de tareas.</span><span class="sxs-lookup"><span data-stu-id="04768-147">The version of the task folder.</span></span>|
|<span data-ttu-id="04768-148">id</span><span class="sxs-lookup"><span data-stu-id="04768-148">id</span></span>|<span data-ttu-id="04768-149">String</span><span class="sxs-lookup"><span data-stu-id="04768-149">String</span></span>|<span data-ttu-id="04768-150">El identificador de la carpeta de tareas, único en el buzón del usuario.</span><span class="sxs-lookup"><span data-stu-id="04768-150">The identifier of the task folder, unique in the user's mailbox.</span></span> <span data-ttu-id="04768-151">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="04768-151">Read-only.</span></span>|
|<span data-ttu-id="04768-152">isDefaultFolder</span><span class="sxs-lookup"><span data-stu-id="04768-152">isDefaultFolder</span></span>|<span data-ttu-id="04768-153">Booleano</span><span class="sxs-lookup"><span data-stu-id="04768-153">Boolean</span></span>|<span data-ttu-id="04768-154">Es True si la carpeta es la carpeta de tareas predeterminada.</span><span class="sxs-lookup"><span data-stu-id="04768-154">True if the folder is the default task folder.</span></span>|
|<span data-ttu-id="04768-155">name</span><span class="sxs-lookup"><span data-stu-id="04768-155">name</span></span>|<span data-ttu-id="04768-156">String</span><span class="sxs-lookup"><span data-stu-id="04768-156">String</span></span>|<span data-ttu-id="04768-157">El nombre de la carpeta de tareas.</span><span class="sxs-lookup"><span data-stu-id="04768-157">The name of the task folder.</span></span>|
|<span data-ttu-id="04768-158">parentGroupKey</span><span class="sxs-lookup"><span data-stu-id="04768-158">parentGroupKey</span></span>|<span data-ttu-id="04768-159">Guid</span><span class="sxs-lookup"><span data-stu-id="04768-159">Guid</span></span>|<span data-ttu-id="04768-160">El identificador GUID único para el grupo primario de la carpeta de la tarea.</span><span class="sxs-lookup"><span data-stu-id="04768-160">The unique GUID identifier for the task folder's parent group.</span></span>|

## <a name="relationships"></a><span data-ttu-id="04768-161">Relaciones</span><span class="sxs-lookup"><span data-stu-id="04768-161">Relationships</span></span>
| <span data-ttu-id="04768-162">Relación</span><span class="sxs-lookup"><span data-stu-id="04768-162">Relationship</span></span> | <span data-ttu-id="04768-163">Tipo</span><span class="sxs-lookup"><span data-stu-id="04768-163">Type</span></span>   |<span data-ttu-id="04768-164">Descripción</span><span class="sxs-lookup"><span data-stu-id="04768-164">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="04768-165">multiValueExtendedProperties</span><span class="sxs-lookup"><span data-stu-id="04768-165">multiValueExtendedProperties</span></span>|<span data-ttu-id="04768-166">Colección [multiValueLegacyExtendedProperty](multivaluelegacyextendedproperty.md)</span><span class="sxs-lookup"><span data-stu-id="04768-166">[multiValueLegacyExtendedProperty](multivaluelegacyextendedproperty.md) collection</span></span>|<span data-ttu-id="04768-167">La colección de propiedades extendidas de varios valores definidos para la carpeta tareas.</span><span class="sxs-lookup"><span data-stu-id="04768-167">The collection of multi-value extended properties defined for the task folder.</span></span> <span data-ttu-id="04768-168">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="04768-168">Read-only.</span></span> <span data-ttu-id="04768-169">Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="04768-169">Nullable.</span></span>|
|<span data-ttu-id="04768-170">singleValueExtendedProperties</span><span class="sxs-lookup"><span data-stu-id="04768-170">singleValueExtendedProperties</span></span>|<span data-ttu-id="04768-171">Colección [singleValueLegacyExtendedProperty](singlevaluelegacyextendedproperty.md)</span><span class="sxs-lookup"><span data-stu-id="04768-171">[singleValueLegacyExtendedProperty](singlevaluelegacyextendedproperty.md) collection</span></span>|<span data-ttu-id="04768-172">La colección de propiedades extendidas de un solo valor definido para la carpeta tareas.</span><span class="sxs-lookup"><span data-stu-id="04768-172">The collection of single-value extended properties defined for the task folder.</span></span> <span data-ttu-id="04768-173">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="04768-173">Read-only.</span></span> <span data-ttu-id="04768-174">Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="04768-174">Nullable.</span></span>|
|<span data-ttu-id="04768-175">tasks</span><span class="sxs-lookup"><span data-stu-id="04768-175">tasks</span></span>|<span data-ttu-id="04768-176">colección de [outlookTask](outlooktask.md)</span><span class="sxs-lookup"><span data-stu-id="04768-176">[outlookTask](outlooktask.md) collection</span></span>|<span data-ttu-id="04768-177">Las tareas de esta carpeta de tareas.</span><span class="sxs-lookup"><span data-stu-id="04768-177">The tasks in this task folder.</span></span> <span data-ttu-id="04768-178">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="04768-178">Read-only.</span></span> <span data-ttu-id="04768-179">Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="04768-179">Nullable.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="04768-180">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="04768-180">JSON representation</span></span>
<span data-ttu-id="04768-181">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="04768-181">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [
    "multiValueExtendedProperties",
    "singleValueExtendedProperties",
    "tasks"
  ],
  "@odata.type": "microsoft.graph.outlookTaskFolder"
}-->

```json
{
  "changeKey": "String",
  "id": "String (identifier)",
  "isDefaultFolder": true,
  "name": "String",
  "parentGroupKey": "Guid"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "outlookTaskFolder resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->