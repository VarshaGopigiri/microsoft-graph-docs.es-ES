---
title: Tipo de recurso managedAppDiagnosticStatus
description: Representa el estado de diagnóstico.
ms.openlocfilehash: 44284b54692e4a123b1837bbfb0f5f04a2b01a2b
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090610"
---
# <a name="managedappdiagnosticstatus-resource-type"></a><span data-ttu-id="ebf09-103">Tipo de recurso managedAppDiagnosticStatus</span><span class="sxs-lookup"><span data-stu-id="ebf09-103">managedAppDiagnosticStatus resource type</span></span>

> <span data-ttu-id="ebf09-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="ebf09-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="ebf09-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="ebf09-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="ebf09-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="ebf09-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="ebf09-107">Representa el estado de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="ebf09-107">Represents diagnostics status.</span></span>
## <a name="properties"></a><span data-ttu-id="ebf09-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ebf09-108">Properties</span></span>
|<span data-ttu-id="ebf09-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ebf09-109">Property</span></span>|<span data-ttu-id="ebf09-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="ebf09-110">Type</span></span>|<span data-ttu-id="ebf09-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="ebf09-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="ebf09-112">validationName</span><span class="sxs-lookup"><span data-stu-id="ebf09-112">validationName</span></span>|<span data-ttu-id="ebf09-113">cadena</span><span class="sxs-lookup"><span data-stu-id="ebf09-113">String</span></span>|<span data-ttu-id="ebf09-114">El nombre descriptivo de validación</span><span class="sxs-lookup"><span data-stu-id="ebf09-114">The validation friendly name</span></span>|
|<span data-ttu-id="ebf09-115">estado</span><span class="sxs-lookup"><span data-stu-id="ebf09-115">state</span></span>|<span data-ttu-id="ebf09-116">cadena</span><span class="sxs-lookup"><span data-stu-id="ebf09-116">String</span></span>|<span data-ttu-id="ebf09-117">El estado actual de la operación.</span><span class="sxs-lookup"><span data-stu-id="ebf09-117">The state of the operation</span></span>|
|<span data-ttu-id="ebf09-118">mitigationInstruction</span><span class="sxs-lookup"><span data-stu-id="ebf09-118">mitigationInstruction</span></span>|<span data-ttu-id="ebf09-119">cadena</span><span class="sxs-lookup"><span data-stu-id="ebf09-119">String</span></span>|<span data-ttu-id="ebf09-120">Instrucciones sobre cómo reducir un error de validación</span><span class="sxs-lookup"><span data-stu-id="ebf09-120">Instruction on how to mitigate a failed validation</span></span>|

## <a name="relationships"></a><span data-ttu-id="ebf09-121">Relaciones</span><span class="sxs-lookup"><span data-stu-id="ebf09-121">Relationships</span></span>
<span data-ttu-id="ebf09-122">Ninguna</span><span class="sxs-lookup"><span data-stu-id="ebf09-122">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="ebf09-123">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="ebf09-123">JSON Representation</span></span>
<span data-ttu-id="ebf09-124">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="ebf09-124">Here is a JSON representation of the resource.</span></span>
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





