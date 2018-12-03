---
author: daspek
ms.author: dspektor
ms.date: 09/14/2017
title: EditAction
ms.openlocfilehash: 5ff2580f21f09a88b4747114e6070a5c7b523728
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090162"
---
# <a name="editaction-resource-type"></a><span data-ttu-id="635cd-102">Tipo de recurso EditAction</span><span class="sxs-lookup"><span data-stu-id="635cd-102">EditAction resource type</span></span>

> <span data-ttu-id="635cd-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="635cd-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="635cd-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="635cd-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="635cd-105">La presencia del recurso **EditAction** en un recurso [**itemActivity**][activity] indica que la actividad ha editado un elemento.</span><span class="sxs-lookup"><span data-stu-id="635cd-105">The presence of the **EditAction** resource on an [**itemActivity**][activity] indicates that the activity edited an item.</span></span>

<span data-ttu-id="635cd-106">**Nota**: Aunque actualmente este recurso está vacío, en futuras revisiones de la API, puede rellenarse con propiedades adicionales.</span><span class="sxs-lookup"><span data-stu-id="635cd-106">**Note**: While this resource is empty today, in future API revisions it may be populated with additional properties.</span></span>

[activity]: itemactivity.md

## <a name="json-representation"></a><span data-ttu-id="635cd-107">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="635cd-107">JSON representation</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [ ],
  "@type": "microsoft.graph.editAction"
}-->

```json
{
}
```

## <a name="properties"></a><span data-ttu-id="635cd-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="635cd-108">Properties</span></span>

<span data-ttu-id="635cd-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="635cd-109">None.</span></span> <span data-ttu-id="635cd-110">Esta faceta es un valor NULL o no NULL y no contiene propiedades.</span><span class="sxs-lookup"><span data-stu-id="635cd-110">This facet is a null or not-null value and contains no properties.</span></span>

## <a name="remarks"></a><span data-ttu-id="635cd-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="635cd-111">Remarks</span></span>

<span data-ttu-id="635cd-112">Actualmente, los registros de actividad de elementos solo están disponibles en SharePoint y OneDrive para la Empresa.</span><span class="sxs-lookup"><span data-stu-id="635cd-112">Item activity records are currently only available on SharePoint and OneDrive for Business.</span></span>

<!-- {
  "type": "#page.annotation",
  "description": "The EditAction object provides information about an activity that edited an item.",
  "keywords": "activities,activity,action,edit,modify",
  "section": "documentation",
  "tocPath": "Resources/EditAction"
} -->