---
author: daspek
ms.author: dspektor
ms.date: 09/14/2017
title: ShareAction
localization_priority: Normal
ms.openlocfilehash: 16bc590fcfe14f9ce7f6f1bbe38492225cce099c
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27828661"
---
# <a name="shareaction-resource-type"></a><span data-ttu-id="616cc-102">Tipo de recurso ShareAction</span><span class="sxs-lookup"><span data-stu-id="616cc-102">ShareAction resource type</span></span>

> <span data-ttu-id="616cc-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="616cc-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="616cc-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="616cc-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="616cc-105">El recurso **ShareAction** proporciona información sobre un recurso [activity][activity] que compartió un elemento.</span><span class="sxs-lookup"><span data-stu-id="616cc-105">The **ShareAction** resource provides information about an [activity][activity] that shared an item.</span></span>

[activity]: itemactivity.md

## <a name="json-representation"></a><span data-ttu-id="616cc-106">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="616cc-106">JSON representation</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [ ],
  "@type": "microsoft.graph.shareAction"
}-->

```json
{
  "recipients": [{"@odata.type": "microsoft.graph.identitySet"}]
}
```

## <a name="properties"></a><span data-ttu-id="616cc-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="616cc-107">Properties</span></span>

| <span data-ttu-id="616cc-108">Nombre de la propiedad</span><span class="sxs-lookup"><span data-stu-id="616cc-108">Property name</span></span> | <span data-ttu-id="616cc-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="616cc-109">Type</span></span>                       | <span data-ttu-id="616cc-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="616cc-110">Description</span></span>
|:--------------|:---------------------------|:-----------------------------
| <span data-ttu-id="616cc-111">recipients</span><span class="sxs-lookup"><span data-stu-id="616cc-111">recipients</span></span>    | <span data-ttu-id="616cc-112">Colección [identitySet][]</span><span class="sxs-lookup"><span data-stu-id="616cc-112">[identitySet][] collection</span></span> | <span data-ttu-id="616cc-113">Las identidades con las que se compartió el elemento en esta acción.</span><span class="sxs-lookup"><span data-stu-id="616cc-113">The identities the item was shared with in this action.</span></span>

[identitySet]: identityset.md

## <a name="remarks"></a><span data-ttu-id="616cc-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="616cc-115">Remarks</span></span>

<span data-ttu-id="616cc-116">Actualmente, los registros de actividad de elementos solo están disponibles en SharePoint y OneDrive para la Empresa.</span><span class="sxs-lookup"><span data-stu-id="616cc-116">Item activity records are currently only available on SharePoint and OneDrive for Business.</span></span>

<!-- {
  "type": "#page.annotation",
  "description": "The ShareAction object provides information about who an item was shared to in a share action.",
  "keywords": "activities,activity,action,mention",
  "section": "documentation",
  "tocPath": "Resources/ShareAction"
} -->
