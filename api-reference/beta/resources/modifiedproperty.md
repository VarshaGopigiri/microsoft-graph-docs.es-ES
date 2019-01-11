---
title: tipo de recurso modifiedProperty
description: Indica todas las propiedades modificadas con valor anterior y el nuevo valor para cualquier recurso en Azure AD que se ha cambiado
localization_priority: Normal
ms.openlocfilehash: 91e5df357a40b2e44bb26edc5fb3bf6965a260e5
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27844460"
---
# <a name="modifiedproperty-resource-type"></a><span data-ttu-id="1aa4c-103">tipo de recurso modifiedProperty</span><span class="sxs-lookup"><span data-stu-id="1aa4c-103">modifiedProperty resource type</span></span>
<span data-ttu-id="1aa4c-104">Indica todas las propiedades modificadas con valor anterior y el nuevo valor para cualquier recurso en Azure AD que se ha cambiado</span><span class="sxs-lookup"><span data-stu-id="1aa4c-104">Indicates all the modified properties with old value and new value for any resource in Azure AD that's changed</span></span>



## <a name="properties"></a><span data-ttu-id="1aa4c-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1aa4c-105">Properties</span></span>
| <span data-ttu-id="1aa4c-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="1aa4c-106">Property</span></span>     | <span data-ttu-id="1aa4c-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="1aa4c-107">Type</span></span>   |<span data-ttu-id="1aa4c-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="1aa4c-108">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="1aa4c-109">displayName</span><span class="sxs-lookup"><span data-stu-id="1aa4c-109">displayName</span></span>|<span data-ttu-id="1aa4c-110">Cadena</span><span class="sxs-lookup"><span data-stu-id="1aa4c-110">String</span></span>|<span data-ttu-id="1aa4c-111">Indica el nombre de propiedad del atributo de destino que se ha modificado.</span><span class="sxs-lookup"><span data-stu-id="1aa4c-111">Indicates the property name of the target attribute that was changed.</span></span>|
|<span data-ttu-id="1aa4c-112">newValue</span><span class="sxs-lookup"><span data-stu-id="1aa4c-112">newValue</span></span>|<span data-ttu-id="1aa4c-113">cadena</span><span class="sxs-lookup"><span data-stu-id="1aa4c-113">String</span></span>|<span data-ttu-id="1aa4c-114">Indica el valor actualizado de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="1aa4c-114">Indicates the updated value for the propery.</span></span>|
|<span data-ttu-id="1aa4c-115">oldValue</span><span class="sxs-lookup"><span data-stu-id="1aa4c-115">oldValue</span></span>|<span data-ttu-id="1aa4c-116">cadena</span><span class="sxs-lookup"><span data-stu-id="1aa4c-116">String</span></span>|<span data-ttu-id="1aa4c-117">Indica el valor anterior (antes de la actualización) para la propiedad.</span><span class="sxs-lookup"><span data-stu-id="1aa4c-117">Indicates the previous value (before the update) for the property.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="1aa4c-118">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="1aa4c-118">JSON representation</span></span>

<span data-ttu-id="1aa4c-119">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="1aa4c-119">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.modifiedProperty"
}-->

```json
{
  "displayName": "String",
  "newValue": "String",
  "oldValue": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "modifiedProperty resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
