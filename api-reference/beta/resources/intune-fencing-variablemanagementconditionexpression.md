---
title: tipo de recurso variableManagementConditionExpression
description: El estado de administración de condición se evalúa como una expresión booleana.
ms.openlocfilehash: 220cb54680755461edb9dab6edf076f8ae0c6a68
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087478"
---
# <a name="variablemanagementconditionexpression-resource-type"></a><span data-ttu-id="7b97d-103">tipo de recurso variableManagementConditionExpression</span><span class="sxs-lookup"><span data-stu-id="7b97d-103">variableManagementConditionExpression resource type</span></span>

> <span data-ttu-id="7b97d-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="7b97d-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="7b97d-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="7b97d-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="7b97d-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="7b97d-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="7b97d-107">El estado de administración de condición se evalúa como una expresión booleana.</span><span class="sxs-lookup"><span data-stu-id="7b97d-107">Evaluates the management condition state as a Boolean expression.</span></span>

<span data-ttu-id="7b97d-108">Hereda de [managementConditionExpressionModel](../resources/intune-fencing-managementconditionexpressionmodel.md)</span><span class="sxs-lookup"><span data-stu-id="7b97d-108">Inherits from [managementConditionExpressionModel](../resources/intune-fencing-managementconditionexpressionmodel.md)</span></span>

## <a name="properties"></a><span data-ttu-id="7b97d-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7b97d-109">Properties</span></span>
|<span data-ttu-id="7b97d-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="7b97d-110">Property</span></span>|<span data-ttu-id="7b97d-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="7b97d-111">Type</span></span>|<span data-ttu-id="7b97d-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="7b97d-112">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="7b97d-113">managementConditionId</span><span class="sxs-lookup"><span data-stu-id="7b97d-113">managementConditionId</span></span>|<span data-ttu-id="7b97d-114">String</span><span class="sxs-lookup"><span data-stu-id="7b97d-114">String</span></span>|<span data-ttu-id="7b97d-115">El identificador de la condición de administración que se utiliza para evaluar la expresión.</span><span class="sxs-lookup"><span data-stu-id="7b97d-115">The management condition id that is used to evaluate the expression.</span></span>|

## <a name="relationships"></a><span data-ttu-id="7b97d-116">Relaciones</span><span class="sxs-lookup"><span data-stu-id="7b97d-116">Relationships</span></span>
<span data-ttu-id="7b97d-117">Ninguna</span><span class="sxs-lookup"><span data-stu-id="7b97d-117">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="7b97d-118">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="7b97d-118">JSON Representation</span></span>
<span data-ttu-id="7b97d-119">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="7b97d-119">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.variableManagementConditionExpression"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.variableManagementConditionExpression",
  "managementConditionId": "String"
}
```





