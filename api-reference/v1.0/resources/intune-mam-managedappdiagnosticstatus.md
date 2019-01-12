---
title: Tipo de recurso managedAppDiagnosticStatus
description: Representa el estado de diagnóstico.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 3a5204a4704eefc2d4e7c8e0d5b3b709e1750667
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27937484"
---
# <a name="managedappdiagnosticstatus-resource-type"></a><span data-ttu-id="1dc55-103">Tipo de recurso managedAppDiagnosticStatus</span><span class="sxs-lookup"><span data-stu-id="1dc55-103">managedAppDiagnosticStatus resource type</span></span>

> <span data-ttu-id="1dc55-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="1dc55-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="1dc55-105">Representa el estado de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="1dc55-105">Represents diagnostics status.</span></span>
## <a name="properties"></a><span data-ttu-id="1dc55-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1dc55-106">Properties</span></span>
|<span data-ttu-id="1dc55-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="1dc55-107">Property</span></span>|<span data-ttu-id="1dc55-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="1dc55-108">Type</span></span>|<span data-ttu-id="1dc55-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="1dc55-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="1dc55-110">validationName</span><span class="sxs-lookup"><span data-stu-id="1dc55-110">validationName</span></span>|<span data-ttu-id="1dc55-111">cadena</span><span class="sxs-lookup"><span data-stu-id="1dc55-111">String</span></span>|<span data-ttu-id="1dc55-112">El nombre descriptivo de validación</span><span class="sxs-lookup"><span data-stu-id="1dc55-112">The validation friendly name</span></span>|
|<span data-ttu-id="1dc55-113">estado</span><span class="sxs-lookup"><span data-stu-id="1dc55-113">state</span></span>|<span data-ttu-id="1dc55-114">cadena</span><span class="sxs-lookup"><span data-stu-id="1dc55-114">String</span></span>|<span data-ttu-id="1dc55-115">El estado actual de la operación.</span><span class="sxs-lookup"><span data-stu-id="1dc55-115">The state of the operation</span></span>|
|<span data-ttu-id="1dc55-116">mitigationInstruction</span><span class="sxs-lookup"><span data-stu-id="1dc55-116">mitigationInstruction</span></span>|<span data-ttu-id="1dc55-117">cadena</span><span class="sxs-lookup"><span data-stu-id="1dc55-117">String</span></span>|<span data-ttu-id="1dc55-118">Instrucciones sobre cómo reducir un error de validación</span><span class="sxs-lookup"><span data-stu-id="1dc55-118">Instruction on how to mitigate a failed validation</span></span>|

## <a name="relationships"></a><span data-ttu-id="1dc55-119">Relaciones</span><span class="sxs-lookup"><span data-stu-id="1dc55-119">Relationships</span></span>
<span data-ttu-id="1dc55-120">Ninguna</span><span class="sxs-lookup"><span data-stu-id="1dc55-120">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="1dc55-121">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="1dc55-121">JSON Representation</span></span>
<span data-ttu-id="1dc55-122">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="1dc55-122">Here is a JSON representation of the resource.</span></span>
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



