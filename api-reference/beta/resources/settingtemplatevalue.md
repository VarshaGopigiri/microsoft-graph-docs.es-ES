---
title: Tipo de recurso settingTemplateValue
description: Representa una definición de configuración de plantilla individual, incluido el valor predeterminado de la configuración, en caso de que la configuración no tenga instancias.
ms.openlocfilehash: afc872f3e3d8d02acae639b967cdaf9375bb60cb
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086473"
---
# <a name="settingtemplatevalue-resource-type"></a><span data-ttu-id="570ba-103">Tipo de recurso settingTemplateValue</span><span class="sxs-lookup"><span data-stu-id="570ba-103">settingTemplateValue resource type</span></span>

> <span data-ttu-id="570ba-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="570ba-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="570ba-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="570ba-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="570ba-106">Representa una definición de configuración de plantilla individual, incluido el valor predeterminado de la configuración, en caso de que la configuración no tenga instancias.</span><span class="sxs-lookup"><span data-stu-id="570ba-106">Represents an individual template setting definition, including the default value for the setting, if the setting is not instantiated.</span></span>


## <a name="properties"></a><span data-ttu-id="570ba-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="570ba-107">Properties</span></span>
| <span data-ttu-id="570ba-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="570ba-108">Property</span></span>     | <span data-ttu-id="570ba-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="570ba-109">Type</span></span>   |<span data-ttu-id="570ba-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="570ba-110">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="570ba-111">defaultValue</span><span class="sxs-lookup"><span data-stu-id="570ba-111">defaultValue</span></span>|<span data-ttu-id="570ba-112">string</span><span class="sxs-lookup"><span data-stu-id="570ba-112">string</span></span>|<span data-ttu-id="570ba-113">Valor predeterminado para la configuración.</span><span class="sxs-lookup"><span data-stu-id="570ba-113">Default value for the setting.</span></span> <span data-ttu-id="570ba-114">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="570ba-114">Read-only.</span></span>|
|<span data-ttu-id="570ba-115">description</span><span class="sxs-lookup"><span data-stu-id="570ba-115">description</span></span>|<span data-ttu-id="570ba-116">string</span><span class="sxs-lookup"><span data-stu-id="570ba-116">string</span></span>|<span data-ttu-id="570ba-117">Descripción de la configuración.</span><span class="sxs-lookup"><span data-stu-id="570ba-117">Description of the setting.</span></span> <span data-ttu-id="570ba-118">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="570ba-118">Read-only.</span></span>|
|<span data-ttu-id="570ba-119">name</span><span class="sxs-lookup"><span data-stu-id="570ba-119">name</span></span>|<span data-ttu-id="570ba-120">string</span><span class="sxs-lookup"><span data-stu-id="570ba-120">string</span></span>|<span data-ttu-id="570ba-121">Nombre de la configuración.</span><span class="sxs-lookup"><span data-stu-id="570ba-121">Name of the setting.</span></span> <span data-ttu-id="570ba-122">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="570ba-122">Read-only.</span></span>|
|<span data-ttu-id="570ba-123">type</span><span class="sxs-lookup"><span data-stu-id="570ba-123">type</span></span>|<span data-ttu-id="570ba-124">string</span><span class="sxs-lookup"><span data-stu-id="570ba-124">string</span></span>|<span data-ttu-id="570ba-125">Tipo de la configuración.</span><span class="sxs-lookup"><span data-stu-id="570ba-125">Type of the setting.</span></span> <span data-ttu-id="570ba-126">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="570ba-126">Read-only.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="570ba-127">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="570ba-127">JSON representation</span></span>

<span data-ttu-id="570ba-128">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="570ba-128">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.settingTemplateValue"
}-->

```json
{
  "defaultValue": "string",
  "description": "string",
  "name": "string",
  "type": "string"
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
