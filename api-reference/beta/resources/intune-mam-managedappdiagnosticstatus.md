---
title: Tipo de recurso managedAppDiagnosticStatus
description: Representa el estado de diagnóstico.
author: tfitzmac
ms.openlocfilehash: 1618c65b46654832fc7706f01cb6d6a9f78926e4
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27314780"
---
# <a name="managedappdiagnosticstatus-resource-type"></a><span data-ttu-id="33564-103">Tipo de recurso managedAppDiagnosticStatus</span><span class="sxs-lookup"><span data-stu-id="33564-103">managedAppDiagnosticStatus resource type</span></span>

> <span data-ttu-id="33564-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="33564-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="33564-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="33564-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="33564-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="33564-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="33564-107">Representa el estado de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="33564-107">Represents diagnostics status.</span></span>
## <a name="properties"></a><span data-ttu-id="33564-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="33564-108">Properties</span></span>
|<span data-ttu-id="33564-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="33564-109">Property</span></span>|<span data-ttu-id="33564-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="33564-110">Type</span></span>|<span data-ttu-id="33564-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="33564-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="33564-112">validationName</span><span class="sxs-lookup"><span data-stu-id="33564-112">validationName</span></span>|<span data-ttu-id="33564-113">cadena</span><span class="sxs-lookup"><span data-stu-id="33564-113">String</span></span>|<span data-ttu-id="33564-114">El nombre descriptivo de validación</span><span class="sxs-lookup"><span data-stu-id="33564-114">The validation friendly name</span></span>|
|<span data-ttu-id="33564-115">estado</span><span class="sxs-lookup"><span data-stu-id="33564-115">state</span></span>|<span data-ttu-id="33564-116">cadena</span><span class="sxs-lookup"><span data-stu-id="33564-116">String</span></span>|<span data-ttu-id="33564-117">El estado actual de la operación.</span><span class="sxs-lookup"><span data-stu-id="33564-117">The state of the operation</span></span>|
|<span data-ttu-id="33564-118">mitigationInstruction</span><span class="sxs-lookup"><span data-stu-id="33564-118">mitigationInstruction</span></span>|<span data-ttu-id="33564-119">cadena</span><span class="sxs-lookup"><span data-stu-id="33564-119">String</span></span>|<span data-ttu-id="33564-120">Instrucciones sobre cómo reducir un error de validación</span><span class="sxs-lookup"><span data-stu-id="33564-120">Instruction on how to mitigate a failed validation</span></span>|

## <a name="relationships"></a><span data-ttu-id="33564-121">Relaciones</span><span class="sxs-lookup"><span data-stu-id="33564-121">Relationships</span></span>
<span data-ttu-id="33564-122">Ninguna</span><span class="sxs-lookup"><span data-stu-id="33564-122">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="33564-123">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="33564-123">JSON Representation</span></span>
<span data-ttu-id="33564-124">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="33564-124">Here is a JSON representation of the resource.</span></span>
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





