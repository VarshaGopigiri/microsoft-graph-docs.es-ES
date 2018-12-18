---
title: Tipo de recurso managedAppDiagnosticStatus
description: Representa el estado de diagnóstico.
author: tfitzmac
ms.openlocfilehash: 7f0cd0d5b11c4d902f51dd422add2373e8e8df9e
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27340687"
---
# <a name="managedappdiagnosticstatus-resource-type"></a><span data-ttu-id="f1a29-103">Tipo de recurso managedAppDiagnosticStatus</span><span class="sxs-lookup"><span data-stu-id="f1a29-103">managedAppDiagnosticStatus resource type</span></span>

> <span data-ttu-id="f1a29-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="f1a29-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="f1a29-105">Representa el estado de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="f1a29-105">Represents diagnostics status.</span></span>
## <a name="properties"></a><span data-ttu-id="f1a29-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f1a29-106">Properties</span></span>
|<span data-ttu-id="f1a29-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f1a29-107">Property</span></span>|<span data-ttu-id="f1a29-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="f1a29-108">Type</span></span>|<span data-ttu-id="f1a29-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="f1a29-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="f1a29-110">validationName</span><span class="sxs-lookup"><span data-stu-id="f1a29-110">validationName</span></span>|<span data-ttu-id="f1a29-111">cadena</span><span class="sxs-lookup"><span data-stu-id="f1a29-111">String</span></span>|<span data-ttu-id="f1a29-112">El nombre descriptivo de validación</span><span class="sxs-lookup"><span data-stu-id="f1a29-112">The validation friendly name</span></span>|
|<span data-ttu-id="f1a29-113">estado</span><span class="sxs-lookup"><span data-stu-id="f1a29-113">state</span></span>|<span data-ttu-id="f1a29-114">cadena</span><span class="sxs-lookup"><span data-stu-id="f1a29-114">String</span></span>|<span data-ttu-id="f1a29-115">El estado actual de la operación.</span><span class="sxs-lookup"><span data-stu-id="f1a29-115">The state of the operation</span></span>|
|<span data-ttu-id="f1a29-116">mitigationInstruction</span><span class="sxs-lookup"><span data-stu-id="f1a29-116">mitigationInstruction</span></span>|<span data-ttu-id="f1a29-117">cadena</span><span class="sxs-lookup"><span data-stu-id="f1a29-117">String</span></span>|<span data-ttu-id="f1a29-118">Instrucciones sobre cómo reducir un error de validación</span><span class="sxs-lookup"><span data-stu-id="f1a29-118">Instruction on how to mitigate a failed validation</span></span>|

## <a name="relationships"></a><span data-ttu-id="f1a29-119">Relaciones</span><span class="sxs-lookup"><span data-stu-id="f1a29-119">Relationships</span></span>
<span data-ttu-id="f1a29-120">Ninguna</span><span class="sxs-lookup"><span data-stu-id="f1a29-120">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="f1a29-121">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="f1a29-121">JSON Representation</span></span>
<span data-ttu-id="f1a29-122">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="f1a29-122">Here is a JSON representation of the resource.</span></span>
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



