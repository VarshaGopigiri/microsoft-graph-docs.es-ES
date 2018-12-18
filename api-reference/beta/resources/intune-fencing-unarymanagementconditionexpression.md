---
title: tipo de recurso unaryManagementConditionExpression
description: Una expresión de condición de administración que se evalúa mediante una operación unario.
author: tfitzmac
ms.openlocfilehash: 43711e68d88bdf0854e8501377fbf3e30b25b3ec
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27344348"
---
# <a name="unarymanagementconditionexpression-resource-type"></a><span data-ttu-id="281d3-103">tipo de recurso unaryManagementConditionExpression</span><span class="sxs-lookup"><span data-stu-id="281d3-103">unaryManagementConditionExpression resource type</span></span>

> <span data-ttu-id="281d3-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="281d3-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="281d3-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="281d3-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="281d3-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="281d3-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="281d3-107">Una expresión de condición de administración que se evalúa mediante una operación unario.</span><span class="sxs-lookup"><span data-stu-id="281d3-107">A management condition expression that is evaluated using a unary operation.</span></span>

<span data-ttu-id="281d3-108">Hereda de [managementConditionExpressionModel](../resources/intune-fencing-managementconditionexpressionmodel.md)</span><span class="sxs-lookup"><span data-stu-id="281d3-108">Inherits from [managementConditionExpressionModel](../resources/intune-fencing-managementconditionexpressionmodel.md)</span></span>

## <a name="properties"></a><span data-ttu-id="281d3-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="281d3-109">Properties</span></span>
|<span data-ttu-id="281d3-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="281d3-110">Property</span></span>|<span data-ttu-id="281d3-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="281d3-111">Type</span></span>|<span data-ttu-id="281d3-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="281d3-112">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="281d3-113">operator</span><span class="sxs-lookup"><span data-stu-id="281d3-113">operator</span></span>|[<span data-ttu-id="281d3-114">unaryManagementConditionExpressionOperatorType</span><span class="sxs-lookup"><span data-stu-id="281d3-114">unaryManagementConditionExpressionOperatorType</span></span>](../resources/intune-fencing-unarymanagementconditionexpressionoperatortype.md)|<span data-ttu-id="281d3-115">El operador utilizado en la evaluación de la operación unario.</span><span class="sxs-lookup"><span data-stu-id="281d3-115">The operator used in the evaluation of the unary operation.</span></span> <span data-ttu-id="281d3-116">Los valores posibles son: `not`.</span><span class="sxs-lookup"><span data-stu-id="281d3-116">Possible values are: `not`.</span></span>|
|<span data-ttu-id="281d3-117">operando</span><span class="sxs-lookup"><span data-stu-id="281d3-117">operand</span></span>|[<span data-ttu-id="281d3-118">managementConditionExpressionModel</span><span class="sxs-lookup"><span data-stu-id="281d3-118">managementConditionExpressionModel</span></span>](../resources/intune-fencing-managementconditionexpressionmodel.md)|<span data-ttu-id="281d3-119">El operando de la operación unario.</span><span class="sxs-lookup"><span data-stu-id="281d3-119">The operand of the unary operation.</span></span>|

## <a name="relationships"></a><span data-ttu-id="281d3-120">Relaciones</span><span class="sxs-lookup"><span data-stu-id="281d3-120">Relationships</span></span>
<span data-ttu-id="281d3-121">Ninguna</span><span class="sxs-lookup"><span data-stu-id="281d3-121">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="281d3-122">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="281d3-122">JSON Representation</span></span>
<span data-ttu-id="281d3-123">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="281d3-123">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.unaryManagementConditionExpression"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.unaryManagementConditionExpression",
  "operator": "String",
  "operand": {
    "@odata.type": "microsoft.graph.managementConditionExpressionModel"
  }
}
```





