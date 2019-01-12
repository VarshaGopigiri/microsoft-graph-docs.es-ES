---
title: tipo de recurso managementConditionExpressionString
description: Una cadena de expresión de condición de administración es una representación de cadena de una expresión de condición de administración.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 872282914dc57be4e8e9bc7d476e7767907ec913
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27968851"
---
# <a name="managementconditionexpressionstring-resource-type"></a><span data-ttu-id="2ca8c-103">tipo de recurso managementConditionExpressionString</span><span class="sxs-lookup"><span data-stu-id="2ca8c-103">managementConditionExpressionString resource type</span></span>

> <span data-ttu-id="2ca8c-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="2ca8c-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="2ca8c-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="2ca8c-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="2ca8c-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="2ca8c-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="2ca8c-107">Una cadena de expresión de condición de administración es una representación de cadena de una expresión de condición de administración.</span><span class="sxs-lookup"><span data-stu-id="2ca8c-107">A management condition expression string is a string representation of a management condition expression.</span></span>

<span data-ttu-id="2ca8c-108">Hereda de [managementConditionExpression](../resources/intune-fencing-managementconditionexpression.md)</span><span class="sxs-lookup"><span data-stu-id="2ca8c-108">Inherits from [managementConditionExpression](../resources/intune-fencing-managementconditionexpression.md)</span></span>

## <a name="properties"></a><span data-ttu-id="2ca8c-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2ca8c-109">Properties</span></span>
|<span data-ttu-id="2ca8c-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="2ca8c-110">Property</span></span>|<span data-ttu-id="2ca8c-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="2ca8c-111">Type</span></span>|<span data-ttu-id="2ca8c-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="2ca8c-112">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="2ca8c-113">valor</span><span class="sxs-lookup"><span data-stu-id="2ca8c-113">value</span></span>|<span data-ttu-id="2ca8c-114">String</span><span class="sxs-lookup"><span data-stu-id="2ca8c-114">String</span></span>|<span data-ttu-id="2ca8c-115">El valor de cadena de expresión de administración condición instrucción.</span><span class="sxs-lookup"><span data-stu-id="2ca8c-115">The management condition statement expression string value.</span></span>|

## <a name="relationships"></a><span data-ttu-id="2ca8c-116">Relaciones</span><span class="sxs-lookup"><span data-stu-id="2ca8c-116">Relationships</span></span>
<span data-ttu-id="2ca8c-117">Ninguna</span><span class="sxs-lookup"><span data-stu-id="2ca8c-117">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="2ca8c-118">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="2ca8c-118">JSON Representation</span></span>
<span data-ttu-id="2ca8c-119">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="2ca8c-119">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.managementConditionExpressionString"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.managementConditionExpressionString",
  "value": "String"
}
```





