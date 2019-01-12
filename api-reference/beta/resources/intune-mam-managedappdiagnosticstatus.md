---
title: Tipo de recurso managedAppDiagnosticStatus
description: Representa el estado de diagnóstico.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 210edaf8eb039db928d612337aa7c8e0642c9ee3
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27987191"
---
# <a name="managedappdiagnosticstatus-resource-type"></a><span data-ttu-id="0ba84-103">Tipo de recurso managedAppDiagnosticStatus</span><span class="sxs-lookup"><span data-stu-id="0ba84-103">managedAppDiagnosticStatus resource type</span></span>

> <span data-ttu-id="0ba84-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="0ba84-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="0ba84-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="0ba84-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="0ba84-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="0ba84-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="0ba84-107">Representa el estado de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="0ba84-107">Represents diagnostics status.</span></span>
## <a name="properties"></a><span data-ttu-id="0ba84-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0ba84-108">Properties</span></span>
|<span data-ttu-id="0ba84-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="0ba84-109">Property</span></span>|<span data-ttu-id="0ba84-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="0ba84-110">Type</span></span>|<span data-ttu-id="0ba84-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="0ba84-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="0ba84-112">validationName</span><span class="sxs-lookup"><span data-stu-id="0ba84-112">validationName</span></span>|<span data-ttu-id="0ba84-113">cadena</span><span class="sxs-lookup"><span data-stu-id="0ba84-113">String</span></span>|<span data-ttu-id="0ba84-114">El nombre descriptivo de validación</span><span class="sxs-lookup"><span data-stu-id="0ba84-114">The validation friendly name</span></span>|
|<span data-ttu-id="0ba84-115">estado</span><span class="sxs-lookup"><span data-stu-id="0ba84-115">state</span></span>|<span data-ttu-id="0ba84-116">cadena</span><span class="sxs-lookup"><span data-stu-id="0ba84-116">String</span></span>|<span data-ttu-id="0ba84-117">El estado actual de la operación.</span><span class="sxs-lookup"><span data-stu-id="0ba84-117">The state of the operation</span></span>|
|<span data-ttu-id="0ba84-118">mitigationInstruction</span><span class="sxs-lookup"><span data-stu-id="0ba84-118">mitigationInstruction</span></span>|<span data-ttu-id="0ba84-119">cadena</span><span class="sxs-lookup"><span data-stu-id="0ba84-119">String</span></span>|<span data-ttu-id="0ba84-120">Instrucciones sobre cómo reducir un error de validación</span><span class="sxs-lookup"><span data-stu-id="0ba84-120">Instruction on how to mitigate a failed validation</span></span>|

## <a name="relationships"></a><span data-ttu-id="0ba84-121">Relaciones</span><span class="sxs-lookup"><span data-stu-id="0ba84-121">Relationships</span></span>
<span data-ttu-id="0ba84-122">Ninguna</span><span class="sxs-lookup"><span data-stu-id="0ba84-122">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="0ba84-123">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="0ba84-123">JSON Representation</span></span>
<span data-ttu-id="0ba84-124">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="0ba84-124">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.managedAppDiagnosticStatus"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.managedAppDiagnosticStatus",
  "validationName": "String",
  "state": "String",
  "mitigationInstruction": "String"
}
```





