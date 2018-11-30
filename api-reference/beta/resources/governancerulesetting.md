---
title: tipo de recurso governanceRuleSetting
description: Representa las reglas que consta de la configuración de las funciones.
ms.openlocfilehash: 486b5163c59772c971cfc1d61a98817b7f0c16f5
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087346"
---
# <a name="governancerulesetting-resource-type"></a><span data-ttu-id="ed0ff-103">tipo de recurso governanceRuleSetting</span><span class="sxs-lookup"><span data-stu-id="ed0ff-103">governanceRuleSetting resource type</span></span>

> <span data-ttu-id="ed0ff-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="ed0ff-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="ed0ff-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="ed0ff-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="ed0ff-106">Representa las reglas que consta de la configuración de las funciones.</span><span class="sxs-lookup"><span data-stu-id="ed0ff-106">Represents the rules that the role settings are composed of.</span></span>


## <a name="properties"></a><span data-ttu-id="ed0ff-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ed0ff-107">Properties</span></span>
|<span data-ttu-id="ed0ff-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ed0ff-108">Property</span></span>      | <span data-ttu-id="ed0ff-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="ed0ff-109">Type</span></span>         |<span data-ttu-id="ed0ff-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="ed0ff-110">Description</span></span>|
|:-------------|:-------------|:----------|
|<span data-ttu-id="ed0ff-111">ruleIdentifier</span><span class="sxs-lookup"><span data-stu-id="ed0ff-111">ruleIdentifier</span></span>|<span data-ttu-id="ed0ff-112">String</span><span class="sxs-lookup"><span data-stu-id="ed0ff-112">String</span></span>        |<span data-ttu-id="ed0ff-113">El identificador de la regla.</span><span class="sxs-lookup"><span data-stu-id="ed0ff-113">The id of the rule.</span></span> <span data-ttu-id="ed0ff-114">Por ejemplo, ``ExpirationRule`` y ``MfaRule``.</span><span class="sxs-lookup"><span data-stu-id="ed0ff-114">For example, ``ExpirationRule`` and ``MfaRule``.</span></span>|
|<span data-ttu-id="ed0ff-115">ajustes</span><span class="sxs-lookup"><span data-stu-id="ed0ff-115">setting</span></span>       |<span data-ttu-id="ed0ff-116">String</span><span class="sxs-lookup"><span data-stu-id="ed0ff-116">String</span></span>        |<span data-ttu-id="ed0ff-117">La configuración de la regla.</span><span class="sxs-lookup"><span data-stu-id="ed0ff-117">The settings of the rule.</span></span> <span data-ttu-id="ed0ff-118">El valor es una cadena JSON con una lista de pares de en el formato de Parameter_Name:Parameter_Value.</span><span class="sxs-lookup"><span data-stu-id="ed0ff-118">The value is a JSON string with a list of pairs in the format of Parameter_Name:Parameter_Value.</span></span> <span data-ttu-id="ed0ff-119">Por ejemplo: `{"permanentAssignment":false,"maximumGrantPeriodInMinutes":129600}`</span><span class="sxs-lookup"><span data-stu-id="ed0ff-119">For example, `{"permanentAssignment":false,"maximumGrantPeriodInMinutes":129600}`</span></span>|

## <a name="json-representation"></a><span data-ttu-id="ed0ff-120">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="ed0ff-120">JSON representation</span></span>

<span data-ttu-id="ed0ff-121">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="ed0ff-121">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.governanceRuleSetting"
}-->


```json
{
  "ruleIdentifier": "String",
  "setting": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "governanceRuleSetting",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->