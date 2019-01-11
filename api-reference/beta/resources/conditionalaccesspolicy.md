---
title: tipo de recurso conditionalAccessPolicy
description: Indica los atributos relacionados con una directiva de acceso condicional o las directivas que se desencadena la actividad de inicio de sesión correspondiente
localization_priority: Normal
ms.openlocfilehash: 7b043e739f84715fb02fbdbd25599e5cfccc284a
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27820646"
---
# <a name="conditionalaccesspolicy-resource-type"></a><span data-ttu-id="8746b-103">tipo de recurso conditionalAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="8746b-103">conditionalAccessPolicy resource type</span></span>
<span data-ttu-id="8746b-104">Indica los atributos relacionados con una directiva de acceso condicional o las directivas que se desencadena la actividad de inicio de sesión correspondiente</span><span class="sxs-lookup"><span data-stu-id="8746b-104">Indicates the attributes related a conditional access policy or policies that's triggered by the corresponding sign-in activity</span></span>



## <a name="properties"></a><span data-ttu-id="8746b-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8746b-105">Properties</span></span>
| <span data-ttu-id="8746b-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="8746b-106">Property</span></span>     | <span data-ttu-id="8746b-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="8746b-107">Type</span></span>   |<span data-ttu-id="8746b-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="8746b-108">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="8746b-109">displayName</span><span class="sxs-lookup"><span data-stu-id="8746b-109">displayName</span></span>|<span data-ttu-id="8746b-110">Cadena</span><span class="sxs-lookup"><span data-stu-id="8746b-110">String</span></span>|<span data-ttu-id="8746b-111">Hace referencia al nombre de la directiva de acceso condicional (ejemplo: "Requieren MFA para fuerza de ventas").</span><span class="sxs-lookup"><span data-stu-id="8746b-111">Refers to the Name of the conditional access policy (example: “Require MFA for Salesforce”).</span></span>|
|<span data-ttu-id="8746b-112">enforcedGrantControls</span><span class="sxs-lookup"><span data-stu-id="8746b-112">enforcedGrantControls</span></span>|<span data-ttu-id="8746b-113">Colección String</span><span class="sxs-lookup"><span data-stu-id="8746b-113">String collection</span></span>|<span data-ttu-id="8746b-114">Hace referencia a los controles de grant aplicados por la directiva de acceso condicional (ejemplo: "Requieren autenticación multifactor").</span><span class="sxs-lookup"><span data-stu-id="8746b-114">Refers to the grant controls enforced by the conditional access policy (example: “Require multi-factor authentication”).</span></span>|
|<span data-ttu-id="8746b-115">enforcedSessionControls</span><span class="sxs-lookup"><span data-stu-id="8746b-115">enforcedSessionControls</span></span>|<span data-ttu-id="8746b-116">Colección String</span><span class="sxs-lookup"><span data-stu-id="8746b-116">String collection</span></span>|<span data-ttu-id="8746b-117">Hace referencia a los controles de sesión aplicados por la directiva de acceso condicional (ejemplo: "Requiere un control aplicación exigido").</span><span class="sxs-lookup"><span data-stu-id="8746b-117">Refers to the session controls enforced by the conditional access policy (example: “Require app enforced controls”).</span></span>|
|<span data-ttu-id="8746b-118">id</span><span class="sxs-lookup"><span data-stu-id="8746b-118">id</span></span>|<span data-ttu-id="8746b-119">Cadena</span><span class="sxs-lookup"><span data-stu-id="8746b-119">String</span></span>|<span data-ttu-id="8746b-120">GUID único de la directiva de acceso condicional</span><span class="sxs-lookup"><span data-stu-id="8746b-120">Unique GUID of the conditional access policy</span></span>|
|<span data-ttu-id="8746b-121">Resultado</span><span class="sxs-lookup"><span data-stu-id="8746b-121">result</span></span>|<span data-ttu-id="8746b-122">Cadena</span><span class="sxs-lookup"><span data-stu-id="8746b-122">String</span></span>| <span data-ttu-id="8746b-123">Indica el resultado de la directiva de entidad emisora de certificados que se desencadenó. Los valores posibles son:</span><span class="sxs-lookup"><span data-stu-id="8746b-123">Indicates the result of the CA policy that was triggered.Possible values are:</span></span><br/> `success` <br/> `failure` <br/> <span data-ttu-id="8746b-124">`notApplied`-Directiva no se aplica porque no se cumplieron las condiciones de la directiva.</span><span class="sxs-lookup"><span data-stu-id="8746b-124">`notApplied` - Policy isn't applied because policy conditions were not met.</span></span> <br/> <span data-ttu-id="8746b-125">`notEnabled`-Esto es debido a la directiva en estado deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="8746b-125">`notEnabled` - This is due to the policy in disabled state.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="8746b-126">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="8746b-126">JSON representation</span></span>

<span data-ttu-id="8746b-127">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="8746b-127">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.conditionalAccessPolicy"
}-->

```json
{
  "displayName": "String",
  "enforcedGrantControls": ["String"],
  "enforcedSessionControls": ["String"],
  "id": "String",
  "result": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "conditionalAccessPolicy resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
