---
author: daspek
ms.author: dspektor
ms.date: 09/14/2017
title: VersionAction
ms.openlocfilehash: f22761dd713b6d09d5e6fafb765d6d43bfc81bf9
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085075"
---
# <a name="versionaction-resource-type"></a><span data-ttu-id="aa300-102">Tipo de recurso VersionAction</span><span class="sxs-lookup"><span data-stu-id="aa300-102">VersionAction resource type</span></span>

> <span data-ttu-id="aa300-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="aa300-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="aa300-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="aa300-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="aa300-105">La presencia del recurso **VersionAction** en un recurso [**itemActivity**][activity] indica que la actividad ha provocado que se creara una versión.</span><span class="sxs-lookup"><span data-stu-id="aa300-105">The presence of the **VersionAction** resource on an [**itemActivity**][activity] indicates that the activity caused a new version to be created.</span></span>

[activity]: itemactivity.md

## <a name="json-representation"></a><span data-ttu-id="aa300-106">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="aa300-106">JSON representation</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [ ],
  "@type": "microsoft.graph.versionAction"
}-->

```json
{
  "newVersion": "string"
}
```

## <a name="properties"></a><span data-ttu-id="aa300-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="aa300-107">Properties</span></span>

| <span data-ttu-id="aa300-108">Nombre de propiedad</span><span class="sxs-lookup"><span data-stu-id="aa300-108">Property name</span></span> | <span data-ttu-id="aa300-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="aa300-109">Type</span></span>   | <span data-ttu-id="aa300-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="aa300-110">Description</span></span>
|:--------------|:-------|:----------------------------------------------------
| <span data-ttu-id="aa300-111">newVersion</span><span class="sxs-lookup"><span data-stu-id="aa300-111">newVersion</span></span>    | <span data-ttu-id="aa300-112">string</span><span class="sxs-lookup"><span data-stu-id="aa300-112">string</span></span> | <span data-ttu-id="aa300-113">El nombre de la nueva versión creada por esta acción.</span><span class="sxs-lookup"><span data-stu-id="aa300-113">The name of the new version that was created by this action.</span></span>

## <a name="remarks"></a><span data-ttu-id="aa300-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="aa300-114">Remarks</span></span>

<span data-ttu-id="aa300-115">Actualmente, los registros de actividad de elementos solo están disponibles en SharePoint y OneDrive para la Empresa.</span><span class="sxs-lookup"><span data-stu-id="aa300-115">Item activity records are currently only available on SharePoint and OneDrive for Business.</span></span>

<!-- {
  "type": "#page.annotation",
  "description": "The VersionAction object provides information about an activity that resulted in a new item version.",
  "keywords": "activities,activity,action,version",
  "section": "documentation",
  "tocPath": "Resources/VersionAction"
} -->
