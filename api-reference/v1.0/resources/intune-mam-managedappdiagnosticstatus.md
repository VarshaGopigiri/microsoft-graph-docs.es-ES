---
title: Tipo de recurso managedAppDiagnosticStatus
description: Representa el estado de diagnóstico.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: f471a71c10a225f2bb5af77399932402f154538d
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27872124"
---
# <a name="managedappdiagnosticstatus-resource-type"></a><span data-ttu-id="6361f-103">Tipo de recurso managedAppDiagnosticStatus</span><span class="sxs-lookup"><span data-stu-id="6361f-103">managedAppDiagnosticStatus resource type</span></span>

> <span data-ttu-id="6361f-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="6361f-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="6361f-105">Representa el estado de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="6361f-105">Represents diagnostics status.</span></span>
## <a name="properties"></a><span data-ttu-id="6361f-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6361f-106">Properties</span></span>
|<span data-ttu-id="6361f-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="6361f-107">Property</span></span>|<span data-ttu-id="6361f-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="6361f-108">Type</span></span>|<span data-ttu-id="6361f-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="6361f-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="6361f-110">validationName</span><span class="sxs-lookup"><span data-stu-id="6361f-110">validationName</span></span>|<span data-ttu-id="6361f-111">cadena</span><span class="sxs-lookup"><span data-stu-id="6361f-111">String</span></span>|<span data-ttu-id="6361f-112">El nombre descriptivo de validación</span><span class="sxs-lookup"><span data-stu-id="6361f-112">The validation friendly name</span></span>|
|<span data-ttu-id="6361f-113">estado</span><span class="sxs-lookup"><span data-stu-id="6361f-113">state</span></span>|<span data-ttu-id="6361f-114">cadena</span><span class="sxs-lookup"><span data-stu-id="6361f-114">String</span></span>|<span data-ttu-id="6361f-115">El estado actual de la operación.</span><span class="sxs-lookup"><span data-stu-id="6361f-115">The state of the operation</span></span>|
|<span data-ttu-id="6361f-116">mitigationInstruction</span><span class="sxs-lookup"><span data-stu-id="6361f-116">mitigationInstruction</span></span>|<span data-ttu-id="6361f-117">cadena</span><span class="sxs-lookup"><span data-stu-id="6361f-117">String</span></span>|<span data-ttu-id="6361f-118">Instrucciones sobre cómo reducir un error de validación</span><span class="sxs-lookup"><span data-stu-id="6361f-118">Instruction on how to mitigate a failed validation</span></span>|

## <a name="relationships"></a><span data-ttu-id="6361f-119">Relaciones</span><span class="sxs-lookup"><span data-stu-id="6361f-119">Relationships</span></span>
<span data-ttu-id="6361f-120">Ninguna</span><span class="sxs-lookup"><span data-stu-id="6361f-120">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="6361f-121">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="6361f-121">JSON Representation</span></span>
<span data-ttu-id="6361f-122">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="6361f-122">Here is a JSON representation of the resource.</span></span>
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



