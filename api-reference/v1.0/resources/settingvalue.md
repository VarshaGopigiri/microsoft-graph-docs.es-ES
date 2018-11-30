---
title: Tipo de recurso settingValue
description: Una configuración que representa un par nombre-valor.
ms.openlocfilehash: b47c5c746117390cfd59db71d832928e482403b9
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27032673"
---
# <a name="settingvalue-resource-type"></a><span data-ttu-id="8b106-103">Tipo de recurso settingValue</span><span class="sxs-lookup"><span data-stu-id="8b106-103">settingValue resource type</span></span>

<span data-ttu-id="8b106-104">Una configuración que representa un par nombre-valor.</span><span class="sxs-lookup"><span data-stu-id="8b106-104">A setting represented by a name/value pair.</span></span>

### <a name="properties"></a><span data-ttu-id="8b106-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8b106-105">Properties</span></span>

| <span data-ttu-id="8b106-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="8b106-106">Property</span></span> | <span data-ttu-id="8b106-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="8b106-107">Type</span></span> | <span data-ttu-id="8b106-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="8b106-108">Description</span></span> |
|:---------------|:--------|:----------|
|<span data-ttu-id="8b106-109">name</span><span class="sxs-lookup"><span data-stu-id="8b106-109">name</span></span>|<span data-ttu-id="8b106-110">String</span><span class="sxs-lookup"><span data-stu-id="8b106-110">String</span></span>| <span data-ttu-id="8b106-111">Nombre de la configuración (según lo definido por la plantilla [groupSettingTemplate](groupsettingtemplate.md)).</span><span class="sxs-lookup"><span data-stu-id="8b106-111">Name of the setting (as defined by the [groupSettingTemplate](groupsettingtemplate.md)).</span></span> |
|<span data-ttu-id="8b106-112">value</span><span class="sxs-lookup"><span data-stu-id="8b106-112">value</span></span>|<span data-ttu-id="8b106-113">String</span><span class="sxs-lookup"><span data-stu-id="8b106-113">String</span></span>| <span data-ttu-id="8b106-114">Valor de la configuración.</span><span class="sxs-lookup"><span data-stu-id="8b106-114">Value of the setting.</span></span> |

### <a name="json-representation"></a><span data-ttu-id="8b106-115">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="8b106-115">JSON representation</span></span>

<span data-ttu-id="8b106-116">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="8b106-116">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.settingValue"
}-->

```json
{
  "name": "String",
  "value": "String"
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