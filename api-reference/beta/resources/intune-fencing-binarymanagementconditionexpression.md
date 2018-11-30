---
title: tipo de recurso binaryManagementConditionExpression
description: Una expresión de condición de administración que se evalúa con una operación binaria.
ms.openlocfilehash: e675a5696d545ba48fc676d1716ed49c7c0b7c65
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090116"
---
# <a name="binarymanagementconditionexpression-resource-type"></a><span data-ttu-id="69675-103">tipo de recurso binaryManagementConditionExpression</span><span class="sxs-lookup"><span data-stu-id="69675-103">binaryManagementConditionExpression resource type</span></span>

> <span data-ttu-id="69675-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="69675-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="69675-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="69675-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="69675-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="69675-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="69675-107">Una expresión de condición de administración que se evalúa con una operación binaria.</span><span class="sxs-lookup"><span data-stu-id="69675-107">A management condition expression that is evaluated using a binary operation.</span></span>

<span data-ttu-id="69675-108">Hereda de [managementConditionExpressionModel](../resources/intune-fencing-managementconditionexpressionmodel.md)</span><span class="sxs-lookup"><span data-stu-id="69675-108">Inherits from [managementConditionExpressionModel](../resources/intune-fencing-managementconditionexpressionmodel.md)</span></span>

## <a name="properties"></a><span data-ttu-id="69675-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="69675-109">Properties</span></span>
|<span data-ttu-id="69675-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="69675-110">Property</span></span>|<span data-ttu-id="69675-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="69675-111">Type</span></span>|<span data-ttu-id="69675-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="69675-112">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="69675-113">operator</span><span class="sxs-lookup"><span data-stu-id="69675-113">operator</span></span>|[<span data-ttu-id="69675-114">binaryManagementConditionExpressionOperatorType</span><span class="sxs-lookup"><span data-stu-id="69675-114">binaryManagementConditionExpressionOperatorType</span></span>](../resources/intune-fencing-binarymanagementconditionexpressionoperatortype.md)|<span data-ttu-id="69675-115">El operador utilizado en la evaluación de la operación binaria.</span><span class="sxs-lookup"><span data-stu-id="69675-115">The operator used in the evaluation of the binary operation.</span></span> <span data-ttu-id="69675-116">Los valores posibles son: `or` y `and`.</span><span class="sxs-lookup"><span data-stu-id="69675-116">Possible values are: `or`, `and`.</span></span>|
|<span data-ttu-id="69675-117">firstOperand</span><span class="sxs-lookup"><span data-stu-id="69675-117">firstOperand</span></span>|[<span data-ttu-id="69675-118">managementConditionExpressionModel</span><span class="sxs-lookup"><span data-stu-id="69675-118">managementConditionExpressionModel</span></span>](../resources/intune-fencing-managementconditionexpressionmodel.md)|<span data-ttu-id="69675-119">El primer operando de la operación binaria.</span><span class="sxs-lookup"><span data-stu-id="69675-119">The first operand of the binary operation.</span></span>|
|<span data-ttu-id="69675-120">secondOperand</span><span class="sxs-lookup"><span data-stu-id="69675-120">secondOperand</span></span>|[<span data-ttu-id="69675-121">managementConditionExpressionModel</span><span class="sxs-lookup"><span data-stu-id="69675-121">managementConditionExpressionModel</span></span>](../resources/intune-fencing-managementconditionexpressionmodel.md)|<span data-ttu-id="69675-122">El segundo operando de la operación binaria.</span><span class="sxs-lookup"><span data-stu-id="69675-122">The second operand of the binary operation.</span></span>|

## <a name="relationships"></a><span data-ttu-id="69675-123">Relaciones</span><span class="sxs-lookup"><span data-stu-id="69675-123">Relationships</span></span>
<span data-ttu-id="69675-124">Ninguna</span><span class="sxs-lookup"><span data-stu-id="69675-124">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="69675-125">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="69675-125">JSON Representation</span></span>
<span data-ttu-id="69675-126">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="69675-126">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.binaryManagementConditionExpression"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.binaryManagementConditionExpression",
  "operator": "String",
  "firstOperand": {
    "@odata.type": "microsoft.graph.managementConditionExpressionModel"
  },
  "secondOperand": {
    "@odata.type": "microsoft.graph.managementConditionExpressionModel"
  }
}
```





