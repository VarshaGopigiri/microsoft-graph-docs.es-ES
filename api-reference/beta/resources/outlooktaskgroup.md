---
title: tipo de recurso outlookTaskGroup
description: 'Un grupo de carpetas (outlookTaskFolder) que contienen las tareas de Outlook (colección de objetos de outlookTask). '
author: angelgolfer-ms
localization_priority: Normal
ms.prod: outlook
ms.openlocfilehash: d1392e07f76d508fe30307294a54429a692f34e8
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27923911"
---
# <a name="outlooktaskgroup-resource-type"></a><span data-ttu-id="2de12-103">tipo de recurso outlookTaskGroup</span><span class="sxs-lookup"><span data-stu-id="2de12-103">outlookTaskGroup resource type</span></span>

> <span data-ttu-id="2de12-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="2de12-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="2de12-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="2de12-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="2de12-106">Un grupo de carpetas ([outlookTaskFolder](outlooktaskfolder.md)) que contienen las tareas de Outlook (colección de objetos de [outlookTask](outlooktask.md) ).</span><span class="sxs-lookup"><span data-stu-id="2de12-106">A group of folders ([outlookTaskFolder](outlooktaskfolder.md)) that contain Outlook tasks (collection of [outlookTask](outlooktask.md) objects).</span></span> 

<span data-ttu-id="2de12-107">En Outlook, hay un grupo de tareas predeterminada `My Tasks` que no se puede cambiar el nombre o eliminar.</span><span class="sxs-lookup"><span data-stu-id="2de12-107">In Outlook, there is a default task group `My Tasks` which you cannot rename or delete.</span></span> <span data-ttu-id="2de12-108">Sin embargo, puede crear grupos de tareas adicionales.</span><span class="sxs-lookup"><span data-stu-id="2de12-108">You can, however, create additional task groups.</span></span> 


## <a name="methods"></a><span data-ttu-id="2de12-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="2de12-109">Methods</span></span>

| <span data-ttu-id="2de12-110">Método</span><span class="sxs-lookup"><span data-stu-id="2de12-110">Method</span></span>           | <span data-ttu-id="2de12-111">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2de12-111">Return Type</span></span>    |<span data-ttu-id="2de12-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="2de12-112">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="2de12-113">Obtener outlookTaskGroup</span><span class="sxs-lookup"><span data-stu-id="2de12-113">Get outlookTaskGroup</span></span>](../api/outlooktaskgroup-get.md) | [<span data-ttu-id="2de12-114">outlookTaskGroup</span><span class="sxs-lookup"><span data-stu-id="2de12-114">outlookTaskGroup</span></span>](outlooktaskgroup.md) |<span data-ttu-id="2de12-115">Obtener las propiedades y relaciones del grupo de tareas de Outlook especificado.</span><span class="sxs-lookup"><span data-stu-id="2de12-115">Get the properties and relationships of the specified Outlook task group.</span></span>|
|[<span data-ttu-id="2de12-116">Crear outlookTaskFolder</span><span class="sxs-lookup"><span data-stu-id="2de12-116">Create outlookTaskFolder</span></span>](../api/outlooktaskgroup-post-taskfolders.md) |[<span data-ttu-id="2de12-117">outlookTaskFolder</span><span class="sxs-lookup"><span data-stu-id="2de12-117">outlookTaskFolder</span></span>](outlooktaskfolder.md)| <span data-ttu-id="2de12-118">Crear una carpeta de tareas de Outlook.</span><span class="sxs-lookup"><span data-stu-id="2de12-118">Create an Outlook task folder.</span></span>|
|[<span data-ttu-id="2de12-119">Lista taskFolders</span><span class="sxs-lookup"><span data-stu-id="2de12-119">List taskFolders</span></span>](../api/outlooktaskgroup-list-taskfolders.md) |<span data-ttu-id="2de12-120">colección de [outlookTaskFolder](outlooktaskfolder.md)</span><span class="sxs-lookup"><span data-stu-id="2de12-120">[outlookTaskFolder](outlooktaskfolder.md) collection</span></span>| <span data-ttu-id="2de12-121">Obtener una colección de carpetas de tareas de Outlook.</span><span class="sxs-lookup"><span data-stu-id="2de12-121">Get a collection of Outlook task folders.</span></span>|
|[<span data-ttu-id="2de12-122">Update</span><span class="sxs-lookup"><span data-stu-id="2de12-122">Update</span></span>](../api/outlooktaskgroup-update.md) | [<span data-ttu-id="2de12-123">outlookTaskGroup</span><span class="sxs-lookup"><span data-stu-id="2de12-123">outlookTaskGroup</span></span>](outlooktaskgroup.md)  |<span data-ttu-id="2de12-124">Actualizar las propiedades modificables de un grupo de tareas de Outlook.</span><span class="sxs-lookup"><span data-stu-id="2de12-124">Update the writable properties of an Outlook task group.</span></span> |
|[<span data-ttu-id="2de12-125">Delete</span><span class="sxs-lookup"><span data-stu-id="2de12-125">Delete</span></span>](../api/outlooktaskgroup-delete.md) | <span data-ttu-id="2de12-126">Ninguno</span><span class="sxs-lookup"><span data-stu-id="2de12-126">None</span></span> |<span data-ttu-id="2de12-127">Eliminar el grupo de tareas de Outlook especificado.</span><span class="sxs-lookup"><span data-stu-id="2de12-127">Delete the specified Outlook task group.</span></span> |

## <a name="properties"></a><span data-ttu-id="2de12-128">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2de12-128">Properties</span></span>
| <span data-ttu-id="2de12-129">Propiedad</span><span class="sxs-lookup"><span data-stu-id="2de12-129">Property</span></span>     | <span data-ttu-id="2de12-130">Tipo</span><span class="sxs-lookup"><span data-stu-id="2de12-130">Type</span></span>   |<span data-ttu-id="2de12-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="2de12-131">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="2de12-132">changeKey</span><span class="sxs-lookup"><span data-stu-id="2de12-132">changeKey</span></span>|<span data-ttu-id="2de12-133">Cadena</span><span class="sxs-lookup"><span data-stu-id="2de12-133">String</span></span>|<span data-ttu-id="2de12-134">La versión del grupo de tareas.</span><span class="sxs-lookup"><span data-stu-id="2de12-134">The version of the task group.</span></span>|
|<span data-ttu-id="2de12-135">groupKey</span><span class="sxs-lookup"><span data-stu-id="2de12-135">groupKey</span></span>|<span data-ttu-id="2de12-136">Edm.Guid</span><span class="sxs-lookup"><span data-stu-id="2de12-136">Edm.Guid</span></span>|<span data-ttu-id="2de12-137">El identificador GUID único para el grupo de tareas.</span><span class="sxs-lookup"><span data-stu-id="2de12-137">The unique GUID identifier for the task group.</span></span>|
|<span data-ttu-id="2de12-138">id</span><span class="sxs-lookup"><span data-stu-id="2de12-138">id</span></span>|<span data-ttu-id="2de12-139">Cadena</span><span class="sxs-lookup"><span data-stu-id="2de12-139">String</span></span>|<span data-ttu-id="2de12-140">El identificador de cadena único del grupo de tareas.</span><span class="sxs-lookup"><span data-stu-id="2de12-140">The unique string identifier of the task group.</span></span> <span data-ttu-id="2de12-141">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="2de12-141">Read-only.</span></span>|
|<span data-ttu-id="2de12-142">isDefaultGroup</span><span class="sxs-lookup"><span data-stu-id="2de12-142">isDefaultGroup</span></span>|<span data-ttu-id="2de12-143">Booleano</span><span class="sxs-lookup"><span data-stu-id="2de12-143">Boolean</span></span>|<span data-ttu-id="2de12-144">Es True si el grupo de tareas es el grupo de tareas predeterminada.</span><span class="sxs-lookup"><span data-stu-id="2de12-144">True if the task group is the default task group.</span></span>|
|<span data-ttu-id="2de12-145">name</span><span class="sxs-lookup"><span data-stu-id="2de12-145">name</span></span>|<span data-ttu-id="2de12-146">Cadena</span><span class="sxs-lookup"><span data-stu-id="2de12-146">String</span></span>|<span data-ttu-id="2de12-147">El nombre del grupo de tareas.</span><span class="sxs-lookup"><span data-stu-id="2de12-147">The name of the task group.</span></span>|

## <a name="relationships"></a><span data-ttu-id="2de12-148">Relaciones</span><span class="sxs-lookup"><span data-stu-id="2de12-148">Relationships</span></span>
| <span data-ttu-id="2de12-149">Relación</span><span class="sxs-lookup"><span data-stu-id="2de12-149">Relationship</span></span> | <span data-ttu-id="2de12-150">Tipo</span><span class="sxs-lookup"><span data-stu-id="2de12-150">Type</span></span>   |<span data-ttu-id="2de12-151">Descripción</span><span class="sxs-lookup"><span data-stu-id="2de12-151">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="2de12-152">taskFolders</span><span class="sxs-lookup"><span data-stu-id="2de12-152">taskFolders</span></span>|<span data-ttu-id="2de12-153">colección de [outlookTaskFolder](outlooktaskfolder.md)</span><span class="sxs-lookup"><span data-stu-id="2de12-153">[outlookTaskFolder](outlooktaskfolder.md) collection</span></span>| <span data-ttu-id="2de12-154">La colección de carpetas de tareas en el grupo de tareas.</span><span class="sxs-lookup"><span data-stu-id="2de12-154">The collection of task folders in the task group.</span></span> <span data-ttu-id="2de12-155">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="2de12-155">Read-only.</span></span> <span data-ttu-id="2de12-156">Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="2de12-156">Nullable.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="2de12-157">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="2de12-157">JSON representation</span></span>
<span data-ttu-id="2de12-158">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="2de12-158">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.outlookTaskGroup"
}-->

```json
{
  "changeKey": "String",
  "groupKey": "Guid",
  "id": "String (identifier)",
  "isDefaultGroup": true,
  "name": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "outlookTaskGroup resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
