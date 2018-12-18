---
title: tipo de recurso binaryManagementConditionExpression
description: Una expresión de condición de administración que se evalúa con una operación binaria.
author: tfitzmac
ms.openlocfilehash: 6f271be2527427daaa04436899552abb4d21475e
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27357522"
---
# <a name="binarymanagementconditionexpression-resource-type"></a><span data-ttu-id="98c6e-103">tipo de recurso binaryManagementConditionExpression</span><span class="sxs-lookup"><span data-stu-id="98c6e-103">binaryManagementConditionExpression resource type</span></span>

> <span data-ttu-id="98c6e-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="98c6e-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="98c6e-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="98c6e-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="98c6e-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="98c6e-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="98c6e-107">Una expresión de condición de administración que se evalúa con una operación binaria.</span><span class="sxs-lookup"><span data-stu-id="98c6e-107">A management condition expression that is evaluated using a binary operation.</span></span>

<span data-ttu-id="98c6e-108">Hereda de [managementConditionExpressionModel](../resources/intune-fencing-managementconditionexpressionmodel.md)</span><span class="sxs-lookup"><span data-stu-id="98c6e-108">Inherits from [managementConditionExpressionModel](../resources/intune-fencing-managementconditionexpressionmodel.md)</span></span>

## <a name="properties"></a><span data-ttu-id="98c6e-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="98c6e-109">Properties</span></span>
|<span data-ttu-id="98c6e-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="98c6e-110">Property</span></span>|<span data-ttu-id="98c6e-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="98c6e-111">Type</span></span>|<span data-ttu-id="98c6e-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="98c6e-112">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="98c6e-113">operator</span><span class="sxs-lookup"><span data-stu-id="98c6e-113">operator</span></span>|[<span data-ttu-id="98c6e-114">binaryManagementConditionExpressionOperatorType</span><span class="sxs-lookup"><span data-stu-id="98c6e-114">binaryManagementConditionExpressionOperatorType</span></span>](../resources/intune-fencing-binarymanagementconditionexpressionoperatortype.md)|<span data-ttu-id="98c6e-115">El operador utilizado en la evaluación de la operación binaria.</span><span class="sxs-lookup"><span data-stu-id="98c6e-115">The operator used in the evaluation of the binary operation.</span></span> <span data-ttu-id="98c6e-116">Los valores posibles son: `or` y `and`.</span><span class="sxs-lookup"><span data-stu-id="98c6e-116">Possible values are: `or`, `and`.</span></span>|
|<span data-ttu-id="98c6e-117">firstOperand</span><span class="sxs-lookup"><span data-stu-id="98c6e-117">firstOperand</span></span>|[<span data-ttu-id="98c6e-118">managementConditionExpressionModel</span><span class="sxs-lookup"><span data-stu-id="98c6e-118">managementConditionExpressionModel</span></span>](../resources/intune-fencing-managementconditionexpressionmodel.md)|<span data-ttu-id="98c6e-119">El primer operando de la operación binaria.</span><span class="sxs-lookup"><span data-stu-id="98c6e-119">The first operand of the binary operation.</span></span>|
|<span data-ttu-id="98c6e-120">secondOperand</span><span class="sxs-lookup"><span data-stu-id="98c6e-120">secondOperand</span></span>|[<span data-ttu-id="98c6e-121">managementConditionExpressionModel</span><span class="sxs-lookup"><span data-stu-id="98c6e-121">managementConditionExpressionModel</span></span>](../resources/intune-fencing-managementconditionexpressionmodel.md)|<span data-ttu-id="98c6e-122">El segundo operando de la operación binaria.</span><span class="sxs-lookup"><span data-stu-id="98c6e-122">The second operand of the binary operation.</span></span>|

## <a name="relationships"></a><span data-ttu-id="98c6e-123">Relaciones</span><span class="sxs-lookup"><span data-stu-id="98c6e-123">Relationships</span></span>
<span data-ttu-id="98c6e-124">Ninguna</span><span class="sxs-lookup"><span data-stu-id="98c6e-124">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="98c6e-125">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="98c6e-125">JSON Representation</span></span>
<span data-ttu-id="98c6e-126">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="98c6e-126">Here is a JSON representation of the resource.</span></span>
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





