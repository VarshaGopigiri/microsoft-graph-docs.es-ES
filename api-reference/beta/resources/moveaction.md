---
author: daspek
ms.author: dspektor
ms.date: 09/14/2017
title: MoveAction
localization_priority: Normal
ms.openlocfilehash: 40049b506c72af5aacddf461b22e1ddd280d7ad4
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27852902"
---
# <a name="moveaction-resource-type"></a><span data-ttu-id="a9c5e-102">Tipo de recurso MoveAction</span><span class="sxs-lookup"><span data-stu-id="a9c5e-102">MoveAction resource type</span></span>

> <span data-ttu-id="a9c5e-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="a9c5e-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="a9c5e-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="a9c5e-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="a9c5e-105">La presencia del recurso **MoveAction** en un recurso [**itemActivity**][activity] indica que la actividad ha movido un elemento.</span><span class="sxs-lookup"><span data-stu-id="a9c5e-105">The presence of the **MoveAction** resource on an [**itemActivity**][activity] indicates that the activity moved an item.</span></span>

[activity]: itemactivity.md

## <a name="json-representation"></a><span data-ttu-id="a9c5e-106">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="a9c5e-106">JSON representation</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [ ],
  "@type": "microsoft.graph.moveAction"
}-->

```json
{
  "from": "string",
  "to": "string"
}
```

## <a name="properties"></a><span data-ttu-id="a9c5e-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a9c5e-107">Properties</span></span>

| <span data-ttu-id="a9c5e-108">Nombre de la propiedad</span><span class="sxs-lookup"><span data-stu-id="a9c5e-108">Property name</span></span> | <span data-ttu-id="a9c5e-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="a9c5e-109">Type</span></span>   | <span data-ttu-id="a9c5e-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="a9c5e-110">Description</span></span>
|:--------------|:-------|:----------------------------------------------------
| <span data-ttu-id="a9c5e-111">from</span><span class="sxs-lookup"><span data-stu-id="a9c5e-111">from</span></span>          | <span data-ttu-id="a9c5e-112">string</span><span class="sxs-lookup"><span data-stu-id="a9c5e-112">string</span></span> | <span data-ttu-id="a9c5e-113">Nombre de la ubicación desde la que se movió el elemento.</span><span class="sxs-lookup"><span data-stu-id="a9c5e-113">The name of the location the item was moved from.</span></span>
| <span data-ttu-id="a9c5e-114">to</span><span class="sxs-lookup"><span data-stu-id="a9c5e-114">to</span></span>            | <span data-ttu-id="a9c5e-115">string</span><span class="sxs-lookup"><span data-stu-id="a9c5e-115">string</span></span> | <span data-ttu-id="a9c5e-116">Nombre de la ubicación a la que se movió el elemento.</span><span class="sxs-lookup"><span data-stu-id="a9c5e-116">The name of the location the item was moved to.</span></span>

## <a name="remarks"></a><span data-ttu-id="a9c5e-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a9c5e-117">Remarks</span></span>

<span data-ttu-id="a9c5e-118">Actualmente, los registros de actividad de elementos solo están disponibles en SharePoint y OneDrive para la Empresa.</span><span class="sxs-lookup"><span data-stu-id="a9c5e-118">Item activity records are currently only available on SharePoint and OneDrive for Business.</span></span>

<!-- {
  "type": "#page.annotation",
  "description": "The MoveAction object provides information about an activity that moved an item.",
  "keywords": "activities,activity,action,move,moved",
  "section": "documentation",
  "tocPath": "Resources/MoveAction"
} -->
