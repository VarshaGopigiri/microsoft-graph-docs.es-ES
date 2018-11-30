---
title: Tipo de recurso settingTemplateValue
description: Representa una definición de configuración de plantilla individual, incluido el valor predeterminado de la configuración, en caso de que la configuración no tenga instancias.
ms.openlocfilehash: 00e424e36338855d8ef603d06c7a9ee52a99c621
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27032080"
---
# <a name="settingtemplatevalue-resource-type"></a><span data-ttu-id="ebbbc-103">Tipo de recurso settingTemplateValue</span><span class="sxs-lookup"><span data-stu-id="ebbbc-103">settingTemplateValue resource type</span></span>

<span data-ttu-id="ebbbc-104">Representa una definición de configuración de plantilla individual, incluido el valor predeterminado de la configuración, en caso de que la configuración no tenga instancias.</span><span class="sxs-lookup"><span data-stu-id="ebbbc-104">Represents an individual template setting definition, including the default value for the setting, if the setting is not instantiated.</span></span>

### <a name="properties"></a><span data-ttu-id="ebbbc-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ebbbc-105">Properties</span></span>

| <span data-ttu-id="ebbbc-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ebbbc-106">Property</span></span> | <span data-ttu-id="ebbbc-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="ebbbc-107">Type</span></span> | <span data-ttu-id="ebbbc-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="ebbbc-108">Description</span></span> |
|:---------------|:--------|:----------|
|<span data-ttu-id="ebbbc-109">defaultValue</span><span class="sxs-lookup"><span data-stu-id="ebbbc-109">defaultValue</span></span>|<span data-ttu-id="ebbbc-110">String</span><span class="sxs-lookup"><span data-stu-id="ebbbc-110">String</span></span>| <span data-ttu-id="ebbbc-111">Valor predeterminado para la configuración.</span><span class="sxs-lookup"><span data-stu-id="ebbbc-111">Default value for the setting.</span></span> |
|<span data-ttu-id="ebbbc-112">description</span><span class="sxs-lookup"><span data-stu-id="ebbbc-112">description</span></span>|<span data-ttu-id="ebbbc-113">String</span><span class="sxs-lookup"><span data-stu-id="ebbbc-113">String</span></span>| <span data-ttu-id="ebbbc-114">Descripción de la configuración.</span><span class="sxs-lookup"><span data-stu-id="ebbbc-114">Description of the setting.</span></span> |
|<span data-ttu-id="ebbbc-115">nombre</span><span class="sxs-lookup"><span data-stu-id="ebbbc-115">name</span></span>|<span data-ttu-id="ebbbc-116">String</span><span class="sxs-lookup"><span data-stu-id="ebbbc-116">String</span></span>| <span data-ttu-id="ebbbc-117">Nombre de la configuración.</span><span class="sxs-lookup"><span data-stu-id="ebbbc-117">Name of the setting.</span></span> |
|<span data-ttu-id="ebbbc-118">tipo</span><span class="sxs-lookup"><span data-stu-id="ebbbc-118">type</span></span>|<span data-ttu-id="ebbbc-119">String</span><span class="sxs-lookup"><span data-stu-id="ebbbc-119">String</span></span>| <span data-ttu-id="ebbbc-120">Tipo de la configuración.</span><span class="sxs-lookup"><span data-stu-id="ebbbc-120">Type of the setting.</span></span> |

### <a name="json-representation"></a><span data-ttu-id="ebbbc-121">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="ebbbc-121">JSON representation</span></span>

<span data-ttu-id="ebbbc-122">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="ebbbc-122">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.settingTemplateValue"
}-->

```json
{
  "defaultValue": "String",
  "description": "String",
  "name": "String",
  "type": "String"
}

```


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "settingTemplateValue resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->