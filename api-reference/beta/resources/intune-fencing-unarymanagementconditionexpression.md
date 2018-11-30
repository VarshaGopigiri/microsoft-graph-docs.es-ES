---
title: tipo de recurso unaryManagementConditionExpression
description: Una expresión de condición de administración que se evalúa mediante una operación unario.
ms.openlocfilehash: 958c180e52a268f849eca1fe0d2a2b75ff81333b
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087193"
---
# <a name="unarymanagementconditionexpression-resource-type"></a><span data-ttu-id="2cebc-103">tipo de recurso unaryManagementConditionExpression</span><span class="sxs-lookup"><span data-stu-id="2cebc-103">unaryManagementConditionExpression resource type</span></span>

> <span data-ttu-id="2cebc-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="2cebc-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="2cebc-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="2cebc-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="2cebc-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="2cebc-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="2cebc-107">Una expresión de condición de administración que se evalúa mediante una operación unario.</span><span class="sxs-lookup"><span data-stu-id="2cebc-107">A management condition expression that is evaluated using a unary operation.</span></span>

<span data-ttu-id="2cebc-108">Hereda de [managementConditionExpressionModel](../resources/intune-fencing-managementconditionexpressionmodel.md)</span><span class="sxs-lookup"><span data-stu-id="2cebc-108">Inherits from [managementConditionExpressionModel](../resources/intune-fencing-managementconditionexpressionmodel.md)</span></span>

## <a name="properties"></a><span data-ttu-id="2cebc-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2cebc-109">Properties</span></span>
|<span data-ttu-id="2cebc-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="2cebc-110">Property</span></span>|<span data-ttu-id="2cebc-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="2cebc-111">Type</span></span>|<span data-ttu-id="2cebc-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="2cebc-112">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="2cebc-113">operator</span><span class="sxs-lookup"><span data-stu-id="2cebc-113">operator</span></span>|[<span data-ttu-id="2cebc-114">unaryManagementConditionExpressionOperatorType</span><span class="sxs-lookup"><span data-stu-id="2cebc-114">unaryManagementConditionExpressionOperatorType</span></span>](../resources/intune-fencing-unarymanagementconditionexpressionoperatortype.md)|<span data-ttu-id="2cebc-115">El operador utilizado en la evaluación de la operación unario.</span><span class="sxs-lookup"><span data-stu-id="2cebc-115">The operator used in the evaluation of the unary operation.</span></span> <span data-ttu-id="2cebc-116">Los valores posibles son: `not`.</span><span class="sxs-lookup"><span data-stu-id="2cebc-116">Possible values are: `not`.</span></span>|
|<span data-ttu-id="2cebc-117">operando</span><span class="sxs-lookup"><span data-stu-id="2cebc-117">operand</span></span>|[<span data-ttu-id="2cebc-118">managementConditionExpressionModel</span><span class="sxs-lookup"><span data-stu-id="2cebc-118">managementConditionExpressionModel</span></span>](../resources/intune-fencing-managementconditionexpressionmodel.md)|<span data-ttu-id="2cebc-119">El operando de la operación unario.</span><span class="sxs-lookup"><span data-stu-id="2cebc-119">The operand of the unary operation.</span></span>|

## <a name="relationships"></a><span data-ttu-id="2cebc-120">Relaciones</span><span class="sxs-lookup"><span data-stu-id="2cebc-120">Relationships</span></span>
<span data-ttu-id="2cebc-121">Ninguna</span><span class="sxs-lookup"><span data-stu-id="2cebc-121">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="2cebc-122">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="2cebc-122">JSON Representation</span></span>
<span data-ttu-id="2cebc-123">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="2cebc-123">Here is a JSON representation of the resource.</span></span>
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





