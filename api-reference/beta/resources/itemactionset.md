---
author: daspek
ms.author: dspektor
ms.date: 09/14/2017
title: ItemActionSet
ms.openlocfilehash: 3b2f77ea21f2352b0a8fa647af84d9b0af08a2ab
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083458"
---
# <a name="itemactionset-resource-type"></a><span data-ttu-id="d7f62-102">Tipo de recurso ItemActionSet</span><span class="sxs-lookup"><span data-stu-id="d7f62-102">ItemActionSet resource type</span></span>

> <span data-ttu-id="d7f62-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="d7f62-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="d7f62-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="d7f62-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="d7f62-105">El recurso **ItemActionSet** proporciona información sobre las acciones que constituyeron una [actividad][itemActivity] en un elemento.</span><span class="sxs-lookup"><span data-stu-id="d7f62-105">The **ItemActionSet** resource provides information about the actions that made up an [activity][itemActivity] on an item.</span></span>

[itemActivity]: itemactivity.md

## <a name="json-representation"></a><span data-ttu-id="d7f62-106">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="d7f62-106">JSON representation</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [ ],
  "keyProperty": "id",
  "@type": "microsoft.graph.itemActionSet",
  "@type.aka": "oneDrive.action"
}-->

```json
{
  "comment": {"@odata.type": "microsoft.graph.commentAction"},
  "create": {"@odata.type": "microsoft.graph.createAction"},
  "delete": {"@odata.type": "microsoft.graph.deleteAction"},
  "edit": {"@odata.type": "microsoft.graph.editAction"},
  "mention": {"@odata.type": "microsoft.graph.mentionAction"},
  "move": {"@odata.type": "microsoft.graph.moveAction"},
  "rename": {"@odata.type": "microsoft.graph.renameAction"},
  "restore": {"@odata.type": "microsoft.graph.restoreAction"},
  "share": {"@odata.type": "microsoft.graph.shareAction"},
  "version": {"@odata.type": "microsoft.graph.versionAction"},
  
}
```

## <a name="properties"></a><span data-ttu-id="d7f62-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d7f62-107">Properties</span></span>

<span data-ttu-id="d7f62-108">A continuación se muestran las acciones que están disponibles actualmente.</span><span class="sxs-lookup"><span data-stu-id="d7f62-108">Below are the actions that are available today.</span></span>
<span data-ttu-id="d7f62-109">Pueden registrarse nuevas acciones en el futuro, así que asegúrese de que su aplicación es tolerante al control de un recurso **itemActionSet** sin ninguna acción que su aplicación comprenda.</span><span class="sxs-lookup"><span data-stu-id="d7f62-109">New actions may get logged in the future, so make sure your app is tolerant of handling an **itemActionSet** without any actions that your app understands.</span></span>

| <span data-ttu-id="d7f62-110">Nombre de la propiedad</span><span class="sxs-lookup"><span data-stu-id="d7f62-110">Property name</span></span> | <span data-ttu-id="d7f62-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="d7f62-111">Type</span></span>              | <span data-ttu-id="d7f62-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="d7f62-112">Description</span></span>
|:--------------|:------------------|:-----------------------------------------
| <span data-ttu-id="d7f62-113">comment</span><span class="sxs-lookup"><span data-stu-id="d7f62-113">comment</span></span>       | <span data-ttu-id="d7f62-114">[commentAction][]</span><span class="sxs-lookup"><span data-stu-id="d7f62-114">[commentAction][]</span></span> | <span data-ttu-id="d7f62-115">Se ha agregado un comentario al elemento.</span><span class="sxs-lookup"><span data-stu-id="d7f62-115">A comment was added to the item.</span></span>
| <span data-ttu-id="d7f62-116">create</span><span class="sxs-lookup"><span data-stu-id="d7f62-116">create</span></span>        | <span data-ttu-id="d7f62-117">[createAction][]</span><span class="sxs-lookup"><span data-stu-id="d7f62-117">[createAction][]</span></span>  | <span data-ttu-id="d7f62-118">Se ha creado un elemento.</span><span class="sxs-lookup"><span data-stu-id="d7f62-118">An item was created.</span></span>
| <span data-ttu-id="d7f62-119">delete</span><span class="sxs-lookup"><span data-stu-id="d7f62-119">delete</span></span>        | <span data-ttu-id="d7f62-120">[deleteAction][]</span><span class="sxs-lookup"><span data-stu-id="d7f62-120">[deleteAction][]</span></span>  | <span data-ttu-id="d7f62-121">Se ha eliminado un elemento.</span><span class="sxs-lookup"><span data-stu-id="d7f62-121">An item was deleted.</span></span>
| <span data-ttu-id="d7f62-122">edit</span><span class="sxs-lookup"><span data-stu-id="d7f62-122">edit</span></span>          | <span data-ttu-id="d7f62-123">[editAction][]</span><span class="sxs-lookup"><span data-stu-id="d7f62-123">[editAction][]</span></span>    | <span data-ttu-id="d7f62-124">Se ha editado un elemento.</span><span class="sxs-lookup"><span data-stu-id="d7f62-124">An item was edited.</span></span>
| <span data-ttu-id="d7f62-125">mention</span><span class="sxs-lookup"><span data-stu-id="d7f62-125">mention</span></span>       | <span data-ttu-id="d7f62-126">[mentionAction][]</span><span class="sxs-lookup"><span data-stu-id="d7f62-126">[mentionAction][]</span></span> | <span data-ttu-id="d7f62-127">Se ha mencionado a un usuario en el elemento.</span><span class="sxs-lookup"><span data-stu-id="d7f62-127">A user was mentioned in the item.</span></span>
| <span data-ttu-id="d7f62-128">move</span><span class="sxs-lookup"><span data-stu-id="d7f62-128">move</span></span>          | <span data-ttu-id="d7f62-129">[moveAction][]</span><span class="sxs-lookup"><span data-stu-id="d7f62-129">[moveAction][]</span></span>    | <span data-ttu-id="d7f62-130">Se ha movido un elemento.</span><span class="sxs-lookup"><span data-stu-id="d7f62-130">An item was moved.</span></span>
| <span data-ttu-id="d7f62-131">rename</span><span class="sxs-lookup"><span data-stu-id="d7f62-131">rename</span></span>        | <span data-ttu-id="d7f62-132">[renameAction][]</span><span class="sxs-lookup"><span data-stu-id="d7f62-132">[renameAction][]</span></span>  | <span data-ttu-id="d7f62-133">Se ha cambiado el nombre de un elemento.</span><span class="sxs-lookup"><span data-stu-id="d7f62-133">An item was renamed.</span></span>
| <span data-ttu-id="d7f62-134">restore</span><span class="sxs-lookup"><span data-stu-id="d7f62-134">restore</span></span>       | <span data-ttu-id="d7f62-135">[restoreAction][]</span><span class="sxs-lookup"><span data-stu-id="d7f62-135">[restoreAction][]</span></span> | <span data-ttu-id="d7f62-136">Se ha restaurado un elemento.</span><span class="sxs-lookup"><span data-stu-id="d7f62-136">An item was restored.</span></span>
| <span data-ttu-id="d7f62-137">share</span><span class="sxs-lookup"><span data-stu-id="d7f62-137">share</span></span>         | <span data-ttu-id="d7f62-138">[shareAction][]</span><span class="sxs-lookup"><span data-stu-id="d7f62-138">[shareAction][]</span></span>   | <span data-ttu-id="d7f62-139">Se ha compartido un elemento.</span><span class="sxs-lookup"><span data-stu-id="d7f62-139">An item was shared.</span></span>
| <span data-ttu-id="d7f62-140">version</span><span class="sxs-lookup"><span data-stu-id="d7f62-140">version</span></span>       | <span data-ttu-id="d7f62-141">[versionAction][]</span><span class="sxs-lookup"><span data-stu-id="d7f62-141">[versionAction][]</span></span> | <span data-ttu-id="d7f62-142">Se ha cambiado la versión de un elemento.</span><span class="sxs-lookup"><span data-stu-id="d7f62-142">An item was versioned.</span></span>

[commentAction]: commentaction.md
[createAction]: createaction.md
[deleteAction]: deleteaction.md
[editAction]: editaction.md
[mentionAction]: mentionaction.md
[moveAction]: moveaction.md
[renameAction]: renameaction.md
[restoreAction]: restoreaction.md
[shareAction]: shareaction.md
[versionAction]: versionaction.md

## <a name="remarks"></a><span data-ttu-id="d7f62-153">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d7f62-153">Remarks</span></span>

<span data-ttu-id="d7f62-154">Actualmente, los registros de actividad de elementos solo están disponibles en SharePoint y OneDrive para la Empresa.</span><span class="sxs-lookup"><span data-stu-id="d7f62-154">Item activity records are currently only available on SharePoint and OneDrive for Business.</span></span>

<!-- {
  "type": "#page.annotation",
  "description": "The ItemActionSet object provides information about the actions that took place as part of an activity on an item.",
  "keywords": "activities,activity,action",
  "section": "documentation",
  "tocPath": "Resources/ItemActionSet"
} -->
