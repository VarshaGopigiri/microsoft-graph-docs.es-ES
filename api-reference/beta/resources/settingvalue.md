---
title: Tipo de recurso settingValue
description: Una configuración que representa un par nombre-valor.
ms.openlocfilehash: fb1c249fba9506b2a4c6ad29d04f98b36c82f53f
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088532"
---
# <a name="settingvalue-resource-type"></a><span data-ttu-id="4b4fa-103">Tipo de recurso settingValue</span><span class="sxs-lookup"><span data-stu-id="4b4fa-103">settingValue resource type</span></span>

> <span data-ttu-id="4b4fa-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="4b4fa-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="4b4fa-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="4b4fa-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="4b4fa-106">Una configuración que representa un par nombre-valor.</span><span class="sxs-lookup"><span data-stu-id="4b4fa-106">A setting represented by a name/value pair.</span></span>


## <a name="properties"></a><span data-ttu-id="4b4fa-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4b4fa-107">Properties</span></span>
| <span data-ttu-id="4b4fa-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="4b4fa-108">Property</span></span>     | <span data-ttu-id="4b4fa-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="4b4fa-109">Type</span></span>   |<span data-ttu-id="4b4fa-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="4b4fa-110">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="4b4fa-111">name</span><span class="sxs-lookup"><span data-stu-id="4b4fa-111">name</span></span>|<span data-ttu-id="4b4fa-112">string</span><span class="sxs-lookup"><span data-stu-id="4b4fa-112">string</span></span>|<span data-ttu-id="4b4fa-113">Nombre de la configuración (como se define por la directorySettingTemplate).</span><span class="sxs-lookup"><span data-stu-id="4b4fa-113">Name of the setting (as defined by the directorySettingTemplate).</span></span>|
|<span data-ttu-id="4b4fa-114">valor</span><span class="sxs-lookup"><span data-stu-id="4b4fa-114">value</span></span>|<span data-ttu-id="4b4fa-115">string</span><span class="sxs-lookup"><span data-stu-id="4b4fa-115">string</span></span>|<span data-ttu-id="4b4fa-116">Valor de la configuración.</span><span class="sxs-lookup"><span data-stu-id="4b4fa-116">Value of the setting.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="4b4fa-117">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="4b4fa-117">JSON representation</span></span>

<span data-ttu-id="4b4fa-118">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="4b4fa-118">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.settingValue"
}-->

```json
{
  "name": "string",
  "value": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "settingValue resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
