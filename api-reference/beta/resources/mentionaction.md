---
author: daspek
ms.author: dspektor
ms.date: 09/14/2017
title: MentionAction
localization_priority: Normal
ms.openlocfilehash: 7843feebd8ebca2022b276007d21a89b754217a0
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27804973"
---
# <a name="mentionaction-resource-type"></a><span data-ttu-id="70eb2-102">Tipo de recurso MentionAction</span><span class="sxs-lookup"><span data-stu-id="70eb2-102">MentionAction resource type</span></span>

> <span data-ttu-id="70eb2-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="70eb2-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="70eb2-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="70eb2-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="70eb2-105">El recurso **MentionAction** proporciona información sobre un recurso [activity][] que mencionó a usuarios.</span><span class="sxs-lookup"><span data-stu-id="70eb2-105">The **MentionAction** resource provides information about an [activity][] that mentioned people.</span></span>

[activity]: itemactivity.md

## <a name="json-representation"></a><span data-ttu-id="70eb2-107">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="70eb2-107">JSON representation</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [ ],
  "@type": "microsoft.graph.mentionAction"
}-->

```json
{
  "mentionees": [{"@odata.type": "microsoft.graph.identitySet"}]
}
```

## <a name="properties"></a><span data-ttu-id="70eb2-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="70eb2-108">Properties</span></span>

| <span data-ttu-id="70eb2-109">Nombre de la propiedad</span><span class="sxs-lookup"><span data-stu-id="70eb2-109">Property name</span></span> | <span data-ttu-id="70eb2-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="70eb2-110">Type</span></span>                       | <span data-ttu-id="70eb2-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="70eb2-111">Description</span></span>
|:--------------|:---------------------------|:-----------------------------
| <span data-ttu-id="70eb2-112">mentionees</span><span class="sxs-lookup"><span data-stu-id="70eb2-112">mentionees</span></span>    | <span data-ttu-id="70eb2-113">Colección [identitySet][]</span><span class="sxs-lookup"><span data-stu-id="70eb2-113">[identitySet][] collection</span></span> | <span data-ttu-id="70eb2-114">Las identidades de los usuarios mencionados en esta acción.</span><span class="sxs-lookup"><span data-stu-id="70eb2-114">The identities of the users mentioned in this action.</span></span>

[identitySet]: identityset.md

## <a name="remarks"></a><span data-ttu-id="70eb2-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="70eb2-116">Remarks</span></span>

<span data-ttu-id="70eb2-117">Actualmente, los registros de actividad de elementos solo están disponibles en SharePoint y OneDrive para la Empresa.</span><span class="sxs-lookup"><span data-stu-id="70eb2-117">Item activity records are currently only available on SharePoint and OneDrive for Business.</span></span>

<!-- {
  "type": "#page.annotation",
  "description": "The MentionAction object provides information about who was mentioned during an activity.",
  "keywords": "activities,activity,action,mention",
  "section": "documentation",
  "tocPath": "Resources/MentionAction"
} -->
