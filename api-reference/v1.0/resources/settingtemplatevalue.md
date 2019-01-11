---
title: Tipo de recurso settingTemplateValue
description: Representa una definición de configuración de plantilla individual, incluido el valor predeterminado de la configuración, en caso de que la configuración no tenga instancias.
localization_priority: Normal
ms.openlocfilehash: 0cb3376177e3a4efcae54a591a083914db6b56d7
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27828325"
---
# <a name="settingtemplatevalue-resource-type"></a><span data-ttu-id="7b4dd-103">Tipo de recurso settingTemplateValue</span><span class="sxs-lookup"><span data-stu-id="7b4dd-103">settingTemplateValue resource type</span></span>

<span data-ttu-id="7b4dd-104">Representa una definición de configuración de plantilla individual, incluido el valor predeterminado de la configuración, en caso de que la configuración no tenga instancias.</span><span class="sxs-lookup"><span data-stu-id="7b4dd-104">Represents an individual template setting definition, including the default value for the setting, if the setting is not instantiated.</span></span>

### <a name="properties"></a><span data-ttu-id="7b4dd-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7b4dd-105">Properties</span></span>

| <span data-ttu-id="7b4dd-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="7b4dd-106">Property</span></span> | <span data-ttu-id="7b4dd-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="7b4dd-107">Type</span></span> | <span data-ttu-id="7b4dd-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="7b4dd-108">Description</span></span> |
|:---------------|:--------|:----------|
|<span data-ttu-id="7b4dd-109">defaultValue</span><span class="sxs-lookup"><span data-stu-id="7b4dd-109">defaultValue</span></span>|<span data-ttu-id="7b4dd-110">String</span><span class="sxs-lookup"><span data-stu-id="7b4dd-110">String</span></span>| <span data-ttu-id="7b4dd-111">Valor predeterminado para la configuración.</span><span class="sxs-lookup"><span data-stu-id="7b4dd-111">Default value for the setting.</span></span> |
|<span data-ttu-id="7b4dd-112">description</span><span class="sxs-lookup"><span data-stu-id="7b4dd-112">description</span></span>|<span data-ttu-id="7b4dd-113">String</span><span class="sxs-lookup"><span data-stu-id="7b4dd-113">String</span></span>| <span data-ttu-id="7b4dd-114">Descripción de la configuración.</span><span class="sxs-lookup"><span data-stu-id="7b4dd-114">Description of the setting.</span></span> |
|<span data-ttu-id="7b4dd-115">nombre</span><span class="sxs-lookup"><span data-stu-id="7b4dd-115">name</span></span>|<span data-ttu-id="7b4dd-116">String</span><span class="sxs-lookup"><span data-stu-id="7b4dd-116">String</span></span>| <span data-ttu-id="7b4dd-117">Nombre de la configuración.</span><span class="sxs-lookup"><span data-stu-id="7b4dd-117">Name of the setting.</span></span> |
|<span data-ttu-id="7b4dd-118">tipo</span><span class="sxs-lookup"><span data-stu-id="7b4dd-118">type</span></span>|<span data-ttu-id="7b4dd-119">String</span><span class="sxs-lookup"><span data-stu-id="7b4dd-119">String</span></span>| <span data-ttu-id="7b4dd-120">Tipo de la configuración.</span><span class="sxs-lookup"><span data-stu-id="7b4dd-120">Type of the setting.</span></span> |

### <a name="json-representation"></a><span data-ttu-id="7b4dd-121">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="7b4dd-121">JSON representation</span></span>

<span data-ttu-id="7b4dd-122">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="7b4dd-122">Here is a JSON representation of the resource.</span></span>

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
