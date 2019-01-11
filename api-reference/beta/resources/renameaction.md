---
author: daspek
ms.author: dspektor
ms.date: 09/14/2017
title: RenameAction
localization_priority: Normal
ms.openlocfilehash: 88fa2738c014f028ebd2cc6e37f83151c7fc984a
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27835710"
---
# <a name="renameaction-resource-type"></a><span data-ttu-id="57491-102">Tipo de recurso RenameAction</span><span class="sxs-lookup"><span data-stu-id="57491-102">RenameAction resource type</span></span>

> <span data-ttu-id="57491-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="57491-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="57491-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="57491-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="57491-105">La presencia del recurso **RenameAction** en un recurso [**itemActivity**][activity] indica que la actividad ha cambiado el nombre de un elemento.</span><span class="sxs-lookup"><span data-stu-id="57491-105">The presence of the **RenameAction** resource on an [**itemActivity**][activity] indicates that the activity renamed an item.</span></span>

[activity]: itemactivity.md

## <a name="json-representation"></a><span data-ttu-id="57491-106">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="57491-106">JSON representation</span></span>

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

## <a name="properties"></a><span data-ttu-id="57491-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="57491-107">Properties</span></span>

| <span data-ttu-id="57491-108">Nombre de la propiedad</span><span class="sxs-lookup"><span data-stu-id="57491-108">Property name</span></span> | <span data-ttu-id="57491-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="57491-109">Type</span></span>   | <span data-ttu-id="57491-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="57491-110">Description</span></span>
|:--------------|:-------|:----------------------------------------------------
| <span data-ttu-id="57491-111">oldName</span><span class="sxs-lookup"><span data-stu-id="57491-111">oldName</span></span>       | <span data-ttu-id="57491-112">string</span><span class="sxs-lookup"><span data-stu-id="57491-112">string</span></span> | <span data-ttu-id="57491-113">El nombre anterior del elemento.</span><span class="sxs-lookup"><span data-stu-id="57491-113">The previous name of the item.</span></span>
| <span data-ttu-id="57491-114">newName</span><span class="sxs-lookup"><span data-stu-id="57491-114">newName</span></span>       | <span data-ttu-id="57491-115">string</span><span class="sxs-lookup"><span data-stu-id="57491-115">string</span></span> | <span data-ttu-id="57491-116">El nuevo nombre del elemento.</span><span class="sxs-lookup"><span data-stu-id="57491-116">The new name of the item.</span></span>

## <a name="remarks"></a><span data-ttu-id="57491-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="57491-117">Remarks</span></span>

<span data-ttu-id="57491-118">Actualmente, los registros de actividad de elementos solo están disponibles en SharePoint y OneDrive para la Empresa.</span><span class="sxs-lookup"><span data-stu-id="57491-118">Item activity records are currently only available on SharePoint and OneDrive for Business.</span></span>

<!-- {
  "type": "#page.annotation",
  "description": "The RenameAction object provides information about an activity that renamed an item.",
  "keywords": "activities,activity,action,rename,renamed",
  "section": "documentation",
  "tocPath": "Resources/RenameAction"
} -->
