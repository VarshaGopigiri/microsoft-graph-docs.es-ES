---
title: tipo de recurso unaryManagementConditionExpression
description: Una expresión de condición de administración que se evalúa mediante una operación unario.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 06a379a53d6d85956a54bede444714e082196ba3
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27949426"
---
# <a name="unarymanagementconditionexpression-resource-type"></a><span data-ttu-id="343a6-103">tipo de recurso unaryManagementConditionExpression</span><span class="sxs-lookup"><span data-stu-id="343a6-103">unaryManagementConditionExpression resource type</span></span>

> <span data-ttu-id="343a6-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="343a6-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="343a6-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="343a6-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="343a6-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="343a6-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="343a6-107">Una expresión de condición de administración que se evalúa mediante una operación unario.</span><span class="sxs-lookup"><span data-stu-id="343a6-107">A management condition expression that is evaluated using a unary operation.</span></span>

<span data-ttu-id="343a6-108">Hereda de [managementConditionExpressionModel](../resources/intune-fencing-managementconditionexpressionmodel.md)</span><span class="sxs-lookup"><span data-stu-id="343a6-108">Inherits from [managementConditionExpressionModel](../resources/intune-fencing-managementconditionexpressionmodel.md)</span></span>

## <a name="properties"></a><span data-ttu-id="343a6-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="343a6-109">Properties</span></span>
|<span data-ttu-id="343a6-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="343a6-110">Property</span></span>|<span data-ttu-id="343a6-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="343a6-111">Type</span></span>|<span data-ttu-id="343a6-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="343a6-112">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="343a6-113">operator</span><span class="sxs-lookup"><span data-stu-id="343a6-113">operator</span></span>|[<span data-ttu-id="343a6-114">unaryManagementConditionExpressionOperatorType</span><span class="sxs-lookup"><span data-stu-id="343a6-114">unaryManagementConditionExpressionOperatorType</span></span>](../resources/intune-fencing-unarymanagementconditionexpressionoperatortype.md)|<span data-ttu-id="343a6-115">El operador utilizado en la evaluación de la operación unario.</span><span class="sxs-lookup"><span data-stu-id="343a6-115">The operator used in the evaluation of the unary operation.</span></span> <span data-ttu-id="343a6-116">Los valores posibles son: `not`.</span><span class="sxs-lookup"><span data-stu-id="343a6-116">Possible values are: `not`.</span></span>|
|<span data-ttu-id="343a6-117">operando</span><span class="sxs-lookup"><span data-stu-id="343a6-117">operand</span></span>|[<span data-ttu-id="343a6-118">managementConditionExpressionModel</span><span class="sxs-lookup"><span data-stu-id="343a6-118">managementConditionExpressionModel</span></span>](../resources/intune-fencing-managementconditionexpressionmodel.md)|<span data-ttu-id="343a6-119">El operando de la operación unario.</span><span class="sxs-lookup"><span data-stu-id="343a6-119">The operand of the unary operation.</span></span>|

## <a name="relationships"></a><span data-ttu-id="343a6-120">Relaciones</span><span class="sxs-lookup"><span data-stu-id="343a6-120">Relationships</span></span>
<span data-ttu-id="343a6-121">Ninguna</span><span class="sxs-lookup"><span data-stu-id="343a6-121">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="343a6-122">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="343a6-122">JSON Representation</span></span>
<span data-ttu-id="343a6-123">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="343a6-123">Here is a JSON representation of the resource.</span></span>
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





