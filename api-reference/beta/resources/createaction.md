---
author: daspek
ms.author: dspektor
ms.date: 09/14/2017
title: CreateAction
ms.openlocfilehash: 4b5d6a50c37c04b1c708e798820b8295d89ebf80
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084478"
---
# <a name="createaction-resource-type"></a><span data-ttu-id="ab071-102">Tipo de recurso CreateAction</span><span class="sxs-lookup"><span data-stu-id="ab071-102">CreateAction resource type</span></span>

> <span data-ttu-id="ab071-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="ab071-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="ab071-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="ab071-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="ab071-105">La presencia del recurso **CreateAction** en un recurso [**itemActivity**][activity] indica que la actividad ha creado un elemento.</span><span class="sxs-lookup"><span data-stu-id="ab071-105">The presence of the **CreateAction** resource on an [**itemActivity**][activity] indicates that the activity created an item.</span></span>

<span data-ttu-id="ab071-106">**Nota**: Aunque actualmente este recurso está vacío, en futuras revisiones de la API, puede rellenarse con propiedades adicionales.</span><span class="sxs-lookup"><span data-stu-id="ab071-106">**Note**: While this resource is empty today, in future API revisions it may be populated with additional properties.</span></span>

[activity]: itemactivity.md

## <a name="json-representation"></a><span data-ttu-id="ab071-107">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="ab071-107">JSON representation</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [ ],
  "@type": "microsoft.graph.createAction"
}-->

```json
{
}
```

## <a name="properties"></a><span data-ttu-id="ab071-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ab071-108">Properties</span></span>

<span data-ttu-id="ab071-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="ab071-109">None.</span></span> <span data-ttu-id="ab071-110">Esta faceta es un valor NULL o no NULL y no contiene propiedades.</span><span class="sxs-lookup"><span data-stu-id="ab071-110">This facet is a null or not-null value and contains no properties.</span></span>

## <a name="remarks"></a><span data-ttu-id="ab071-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ab071-111">Remarks</span></span>

<span data-ttu-id="ab071-112">Actualmente, los registros de actividad de elementos solo están disponibles en SharePoint y OneDrive para la Empresa.</span><span class="sxs-lookup"><span data-stu-id="ab071-112">Item activity records are currently only available on SharePoint and OneDrive for Business.</span></span>

<!-- {
  "type": "#page.annotation",
  "description": "The CreateAction object provides information about the creation of an item.",
  "keywords": "activities,activity,action,create,creation",
  "section": "documentation",
  "tocPath": "Resources/CreateAction"
} -->
