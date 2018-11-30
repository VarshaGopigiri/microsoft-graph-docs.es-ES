---
author: daspek
ms.author: dspektor
ms.date: 09/14/2017
title: RenameAction
ms.openlocfilehash: 12956ab51923f6d9f175b25203bf2921a64a8a6b
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086479"
---
# <a name="renameaction-resource-type"></a><span data-ttu-id="27752-102">Tipo de recurso RenameAction</span><span class="sxs-lookup"><span data-stu-id="27752-102">RenameAction resource type</span></span>

> <span data-ttu-id="27752-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="27752-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="27752-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="27752-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="27752-105">La presencia del recurso **RenameAction** en un recurso [**itemActivity**][activity] indica que la actividad ha cambiado el nombre de un elemento.</span><span class="sxs-lookup"><span data-stu-id="27752-105">The presence of the **RenameAction** resource on an [**itemActivity**][activity] indicates that the activity renamed an item.</span></span>

[activity]: itemactivity.md

## <a name="json-representation"></a><span data-ttu-id="27752-106">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="27752-106">JSON representation</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [ ],
  "@type": "microsoft.graph.renameAction"
}-->

```json
{
  "oldName": "string",
  "newName": "string"
}
```

## <a name="properties"></a><span data-ttu-id="27752-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="27752-107">Properties</span></span>

| <span data-ttu-id="27752-108">Nombre de propiedad</span><span class="sxs-lookup"><span data-stu-id="27752-108">Property name</span></span> | <span data-ttu-id="27752-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="27752-109">Type</span></span>   | <span data-ttu-id="27752-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="27752-110">Description</span></span>
|:--------------|:-------|:----------------------------------------------------
| <span data-ttu-id="27752-111">oldName</span><span class="sxs-lookup"><span data-stu-id="27752-111">oldName</span></span>       | <span data-ttu-id="27752-112">string</span><span class="sxs-lookup"><span data-stu-id="27752-112">string</span></span> | <span data-ttu-id="27752-113">El nombre anterior del elemento.</span><span class="sxs-lookup"><span data-stu-id="27752-113">The previous name of the item.</span></span>
| <span data-ttu-id="27752-114">newName</span><span class="sxs-lookup"><span data-stu-id="27752-114">newName</span></span>       | <span data-ttu-id="27752-115">string</span><span class="sxs-lookup"><span data-stu-id="27752-115">string</span></span> | <span data-ttu-id="27752-116">El nuevo nombre del elemento.</span><span class="sxs-lookup"><span data-stu-id="27752-116">The new name of the item.</span></span>

## <a name="remarks"></a><span data-ttu-id="27752-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="27752-117">Remarks</span></span>

<span data-ttu-id="27752-118">Actualmente, los registros de actividad de elementos solo están disponibles en SharePoint y OneDrive para la Empresa.</span><span class="sxs-lookup"><span data-stu-id="27752-118">Item activity records are currently only available on SharePoint and OneDrive for Business.</span></span>

<!-- {
  "type": "#page.annotation",
  "description": "The RenameAction object provides information about an activity that renamed an item.",
  "keywords": "activities,activity,action,rename,renamed",
  "section": "documentation",
  "tocPath": "Resources/RenameAction"
} -->
