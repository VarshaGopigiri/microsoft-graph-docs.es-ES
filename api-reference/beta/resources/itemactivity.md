---
author: daspek
ms.author: dspektor
ms.date: 09/14/2017
title: ItemActivity
ms.openlocfilehash: 7c8cdab7adc705333d1aeaad526aeeb813de10a7
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089501"
---
# <a name="itemactivity-resource-type"></a><span data-ttu-id="699f6-102">Tipo de recurso ItemActivity</span><span class="sxs-lookup"><span data-stu-id="699f6-102">ItemActivity resource type</span></span>

> <span data-ttu-id="699f6-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="699f6-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="699f6-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="699f6-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="699f6-105">El recurso **ItemActivity** proporciona información sobre las actividades que tuvieron lugar en un elemento o contenedor.</span><span class="sxs-lookup"><span data-stu-id="699f6-105">The **ItemActivity** resource provides information about activities that took place on an item or within a container.</span></span>
<span data-ttu-id="699f6-106">Actualmente, solo está disponible en SharePoint y OneDrive para la Empresa.</span><span class="sxs-lookup"><span data-stu-id="699f6-106">Currently only available on SharePoint and OneDrive for Business.</span></span>

## <a name="json-representation"></a><span data-ttu-id="699f6-107">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="699f6-107">JSON representation</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [ ],
  "keyProperty": "id",
  "@type": "microsoft.graph.itemActivity",
  "@type.aka": "oneDrive.activityEntity"
}-->

```json
{
  "id": "string (identifier)",
  "access": "microsoft.graph.accessAction",
  "action": {"@odata.type": "microsoft.graph.itemActionSet"},
  "actor": {"@odata.type": "microsoft.graph.identitySet"},
  "driveItem": {"@odata.type": "microsoft.graph.driveItem"},
  "listItem": {"@odata.type": "microsoft.graph.listItem"},
  "location": {"@odata.type": "microsoft.graph.location"},
  "times": {"@odata.type": "microsoft.graph.itemActivityTimeSet"}
}
```

## <a name="properties"></a><span data-ttu-id="699f6-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="699f6-108">Properties</span></span>

| <span data-ttu-id="699f6-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="699f6-109">Property</span></span> | <span data-ttu-id="699f6-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="699f6-110">Type</span></span>                    | <span data-ttu-id="699f6-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="699f6-111">Description</span></span>
|:---------|:------------------------|:----------------------------------------
| <span data-ttu-id="699f6-112">id</span><span class="sxs-lookup"><span data-stu-id="699f6-112">id</span></span>       | <span data-ttu-id="699f6-113">string</span><span class="sxs-lookup"><span data-stu-id="699f6-113">string</span></span>                  | <span data-ttu-id="699f6-114">El identificador único de la actividad.</span><span class="sxs-lookup"><span data-stu-id="699f6-114">The unique identifier of the activity.</span></span> <span data-ttu-id="699f6-115">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="699f6-115">Read-only.</span></span>
| <span data-ttu-id="699f6-116">Access</span><span class="sxs-lookup"><span data-stu-id="699f6-116">access</span></span>   | <span data-ttu-id="699f6-117">[accessAction][]</span><span class="sxs-lookup"><span data-stu-id="699f6-117">[accessAction][]</span></span>        | <span data-ttu-id="699f6-118">Se tiene acceso a un elemento.</span><span class="sxs-lookup"><span data-stu-id="699f6-118">An item was accessed.</span></span>
| <span data-ttu-id="699f6-119">action</span><span class="sxs-lookup"><span data-stu-id="699f6-119">action</span></span>   | <span data-ttu-id="699f6-120">[itemActionSet][]</span><span class="sxs-lookup"><span data-stu-id="699f6-120">[itemActionSet][]</span></span>       | <span data-ttu-id="699f6-121">Detalles sobre la acción que tuvo lugar.</span><span class="sxs-lookup"><span data-stu-id="699f6-121">Details about the action that took place.</span></span> <span data-ttu-id="699f6-122">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="699f6-122">Read-only.</span></span>
| <span data-ttu-id="699f6-123">actor</span><span class="sxs-lookup"><span data-stu-id="699f6-123">actor</span></span>    | <span data-ttu-id="699f6-124">[identitySet][]</span><span class="sxs-lookup"><span data-stu-id="699f6-124">[identitySet][]</span></span>         | <span data-ttu-id="699f6-125">Identidad del usuario que ha realizado la acción.</span><span class="sxs-lookup"><span data-stu-id="699f6-125">Identity of who performed the action.</span></span> <span data-ttu-id="699f6-126">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="699f6-126">Read-only.</span></span>
| <span data-ttu-id="699f6-127">location</span><span class="sxs-lookup"><span data-stu-id="699f6-127">location</span></span> | <span data-ttu-id="699f6-128">[ubicación][]</span><span class="sxs-lookup"><span data-stu-id="699f6-128">[location][]</span></span>            | <span data-ttu-id="699f6-129">Ubicación física donde se llevó a cabo la acción.</span><span class="sxs-lookup"><span data-stu-id="699f6-129">Physical location where the action was performed.</span></span> <span data-ttu-id="699f6-130">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="699f6-130">Read-only.</span></span>
| <span data-ttu-id="699f6-131">times</span><span class="sxs-lookup"><span data-stu-id="699f6-131">times</span></span>    | <span data-ttu-id="699f6-132">[itemActivityTimeSet][]</span><span class="sxs-lookup"><span data-stu-id="699f6-132">[itemActivityTimeSet][]</span></span> | <span data-ttu-id="699f6-133">Detalles sobre cuándo tuvo lugar la actividad.</span><span class="sxs-lookup"><span data-stu-id="699f6-133">Details about when the activity took place.</span></span> <span data-ttu-id="699f6-134">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="699f6-134">Read-only.</span></span>

[identitySet]: identityset.md
[itemActionSet]: itemactionset.md
[itemActivityTimeSet]: itemactivitytimeset.md

## <a name="relationships"></a><span data-ttu-id="699f6-138">Relaciones</span><span class="sxs-lookup"><span data-stu-id="699f6-138">Relationships</span></span>

| <span data-ttu-id="699f6-139">Nombre de la relación</span><span class="sxs-lookup"><span data-stu-id="699f6-139">Relationship name</span></span> | <span data-ttu-id="699f6-140">Tipo</span><span class="sxs-lookup"><span data-stu-id="699f6-140">Type</span></span>          | <span data-ttu-id="699f6-141">Descripción</span><span class="sxs-lookup"><span data-stu-id="699f6-141">Description</span></span>
|:------------------|:--------------|:-----------------------------------------
| <span data-ttu-id="699f6-142">driveItem</span><span class="sxs-lookup"><span data-stu-id="699f6-142">driveItem</span></span>         | <span data-ttu-id="699f6-143">[driveItem][]</span><span class="sxs-lookup"><span data-stu-id="699f6-143">[driveItem][]</span></span> | <span data-ttu-id="699f6-144">Expone el objeto **driveItem** que era el destino de esta actividad.</span><span class="sxs-lookup"><span data-stu-id="699f6-144">Exposes the **driveItem** that was the target of this activity.</span></span>
| <span data-ttu-id="699f6-145">listItem</span><span class="sxs-lookup"><span data-stu-id="699f6-145">listItem</span></span>          | <span data-ttu-id="699f6-146">[listItem][]</span><span class="sxs-lookup"><span data-stu-id="699f6-146">[listItem][]</span></span>  | <span data-ttu-id="699f6-147">Expone el objeto **listItem** que era el destino de esta actividad.</span><span class="sxs-lookup"><span data-stu-id="699f6-147">Exposes the **listItem** that was the target of this activity.</span></span>

[driveItem]: driveitem.md
[listItem]: listitem.md

## <a name="actions"></a><span data-ttu-id="699f6-150">Acciones</span><span class="sxs-lookup"><span data-stu-id="699f6-150">Actions</span></span>

<span data-ttu-id="699f6-151">Las acciones que tuvieron lugar dentro de una actividad se detallan en la propiedad **action**.</span><span class="sxs-lookup"><span data-stu-id="699f6-151">The actions that took place within an activity are detailed in the **action** property.</span></span>
<span data-ttu-id="699f6-152">A continuación se muestran las acciones que están disponibles actualmente.</span><span class="sxs-lookup"><span data-stu-id="699f6-152">Below are the actions that are available today.</span></span>
<span data-ttu-id="699f6-153">Pueden registrarse nuevas acciones en el futuro, así que asegúrese de que su aplicación es tolerante al control de un recurso **itemActivity** sin ninguna acción que su aplicación comprenda.</span><span class="sxs-lookup"><span data-stu-id="699f6-153">New actions may get logged in the future, so make sure your app is tolerant of handling an **itemActivity** without any actions that your app understands.</span></span>

| <span data-ttu-id="699f6-154">Nombre de acción</span><span class="sxs-lookup"><span data-stu-id="699f6-154">Action name</span></span> | <span data-ttu-id="699f6-155">Tipo</span><span class="sxs-lookup"><span data-stu-id="699f6-155">Type</span></span>              | <span data-ttu-id="699f6-156">Descripción</span><span class="sxs-lookup"><span data-stu-id="699f6-156">Description</span></span>
|:------------|:------------------|:-------------------------------------------
| <span data-ttu-id="699f6-157">comment</span><span class="sxs-lookup"><span data-stu-id="699f6-157">comment</span></span>     | <span data-ttu-id="699f6-158">[commentAction][]</span><span class="sxs-lookup"><span data-stu-id="699f6-158">[commentAction][]</span></span> | <span data-ttu-id="699f6-159">Se ha agregado un comentario al elemento.</span><span class="sxs-lookup"><span data-stu-id="699f6-159">A comment was added to the item.</span></span>
| <span data-ttu-id="699f6-160">create</span><span class="sxs-lookup"><span data-stu-id="699f6-160">create</span></span>      | <span data-ttu-id="699f6-161">[createAction][]</span><span class="sxs-lookup"><span data-stu-id="699f6-161">[createAction][]</span></span>  | <span data-ttu-id="699f6-162">Se ha creado un elemento.</span><span class="sxs-lookup"><span data-stu-id="699f6-162">An item was created.</span></span>
| <span data-ttu-id="699f6-163">delete</span><span class="sxs-lookup"><span data-stu-id="699f6-163">delete</span></span>      | <span data-ttu-id="699f6-164">[deleteAction][]</span><span class="sxs-lookup"><span data-stu-id="699f6-164">[deleteAction][]</span></span>  | <span data-ttu-id="699f6-165">Se ha eliminado un elemento.</span><span class="sxs-lookup"><span data-stu-id="699f6-165">An item was deleted.</span></span>
| <span data-ttu-id="699f6-166">edit</span><span class="sxs-lookup"><span data-stu-id="699f6-166">edit</span></span>        | <span data-ttu-id="699f6-167">[editAction][]</span><span class="sxs-lookup"><span data-stu-id="699f6-167">[editAction][]</span></span>    | <span data-ttu-id="699f6-168">Se ha editado un elemento.</span><span class="sxs-lookup"><span data-stu-id="699f6-168">An item was edited.</span></span>
| <span data-ttu-id="699f6-169">mention</span><span class="sxs-lookup"><span data-stu-id="699f6-169">mention</span></span>     | <span data-ttu-id="699f6-170">[mentionAction][]</span><span class="sxs-lookup"><span data-stu-id="699f6-170">[mentionAction][]</span></span> | <span data-ttu-id="699f6-171">Se ha mencionado a un usuario en el elemento.</span><span class="sxs-lookup"><span data-stu-id="699f6-171">A user was mentioned in the item.</span></span>
| <span data-ttu-id="699f6-172">move</span><span class="sxs-lookup"><span data-stu-id="699f6-172">move</span></span>        | <span data-ttu-id="699f6-173">[moveAction][]</span><span class="sxs-lookup"><span data-stu-id="699f6-173">[moveAction][]</span></span>    | <span data-ttu-id="699f6-174">Se ha movido un elemento.</span><span class="sxs-lookup"><span data-stu-id="699f6-174">An item was moved.</span></span>
| <span data-ttu-id="699f6-175">rename</span><span class="sxs-lookup"><span data-stu-id="699f6-175">rename</span></span>      | <span data-ttu-id="699f6-176">[renameAction][]</span><span class="sxs-lookup"><span data-stu-id="699f6-176">[renameAction][]</span></span>  | <span data-ttu-id="699f6-177">Se ha cambiado el nombre de un elemento.</span><span class="sxs-lookup"><span data-stu-id="699f6-177">An item was renamed.</span></span>
| <span data-ttu-id="699f6-178">restore</span><span class="sxs-lookup"><span data-stu-id="699f6-178">restore</span></span>     | <span data-ttu-id="699f6-179">[restoreAction][]</span><span class="sxs-lookup"><span data-stu-id="699f6-179">[restoreAction][]</span></span> | <span data-ttu-id="699f6-180">Se ha restaurado un elemento.</span><span class="sxs-lookup"><span data-stu-id="699f6-180">An item was restored.</span></span>
| <span data-ttu-id="699f6-181">share</span><span class="sxs-lookup"><span data-stu-id="699f6-181">share</span></span>       | <span data-ttu-id="699f6-182">[shareAction][]</span><span class="sxs-lookup"><span data-stu-id="699f6-182">[shareAction][]</span></span>   | <span data-ttu-id="699f6-183">Se ha compartido un elemento.</span><span class="sxs-lookup"><span data-stu-id="699f6-183">An item was shared.</span></span>
| <span data-ttu-id="699f6-184">version</span><span class="sxs-lookup"><span data-stu-id="699f6-184">version</span></span>     | <span data-ttu-id="699f6-185">[versionAction][]</span><span class="sxs-lookup"><span data-stu-id="699f6-185">[versionAction][]</span></span> | <span data-ttu-id="699f6-186">Se ha cambiado la versión de un elemento.</span><span class="sxs-lookup"><span data-stu-id="699f6-186">An item was versioned.</span></span>

[accessAction]: accessaction.md
[commentAction]: commentaction.md
[createAction]: createaction.md
[deleteAction]: deleteaction.md
[editAction]: editaction.md
[location]: location.md
[mentionAction]: mentionaction.md
[moveAction]: moveaction.md
[renameAction]: renameaction.md
[restoreAction]: restoreaction.md
[shareAction]: shareaction.md
[versionAction]: versionaction.md

## <a name="remarks"></a><span data-ttu-id="699f6-199">Comentarios</span><span class="sxs-lookup"><span data-stu-id="699f6-199">Remarks</span></span>

<span data-ttu-id="699f6-200">Actualmente, **ItemActivity** solo está disponible en SharePoint y OneDrive para la Empresa.</span><span class="sxs-lookup"><span data-stu-id="699f6-200">**ItemActivity** is currently only available on SharePoint and OneDrive for Business.</span></span>

<!-- {
  "type": "#page.annotation",
  "description": "The ItemActivity object provides information about an activity that took place on an item.",
  "keywords": "activities,activity,action",
  "section": "documentation",
  "tocPath": "Resources/ItemActivity"
} -->
