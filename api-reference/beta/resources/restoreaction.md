---
author: daspek
ms.author: dspektor
ms.date: 09/14/2017
title: RestoreAction
ms.openlocfilehash: ce8f964b336f648cd1432532eb85a69629eb2207
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088537"
---
# <a name="restoreaction-resource-type"></a><span data-ttu-id="e5ed8-102">Tipo de recurso RestoreAction</span><span class="sxs-lookup"><span data-stu-id="e5ed8-102">RestoreAction resource type</span></span>

> <span data-ttu-id="e5ed8-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="e5ed8-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="e5ed8-105">La presencia del recurso **RestoreAction** en un recurso [**itemActivity**][activity] indica que la actividad ha restaurado un elemento.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-105">The presence of the **RestoreAction** resource on an [**itemActivity**][activity] indicates that the activity restored an item.</span></span>

<span data-ttu-id="e5ed8-106">**Nota**: Aunque actualmente este recurso está vacío, en futuras revisiones de la API, puede rellenarse con propiedades adicionales.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-106">**Note**: While this resource is empty today, in future API revisions it may be populated with additional properties.</span></span>

[activity]: itemactivity.md

## <a name="json-representation"></a><span data-ttu-id="e5ed8-107">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="e5ed8-107">JSON representation</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [ ],
  "@type": "microsoft.graph.restoreAction"
}-->

```json
{
}
```

## <a name="properties"></a><span data-ttu-id="e5ed8-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e5ed8-108">Properties</span></span>

<span data-ttu-id="e5ed8-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-109">None.</span></span> <span data-ttu-id="e5ed8-110">Esta faceta es un valor NULL o no NULL y no contiene propiedades.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-110">This facet is a null or not-null value and contains no properties.</span></span>

## <a name="remarks"></a><span data-ttu-id="e5ed8-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e5ed8-111">Remarks</span></span>

<span data-ttu-id="e5ed8-112">Actualmente, los registros de actividad de elementos solo están disponibles en SharePoint y OneDrive para la Empresa.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-112">Item activity records are currently only available on SharePoint and OneDrive for Business.</span></span>

<!-- {
  "type": "#page.annotation",
  "description": "The RestoreAction object provides information about an activity that restored an item.",
  "keywords": "activities,activity,action,restore,undelete",
  "section": "documentation",
  "tocPath": "Resources/RestoreAction"
} -->
