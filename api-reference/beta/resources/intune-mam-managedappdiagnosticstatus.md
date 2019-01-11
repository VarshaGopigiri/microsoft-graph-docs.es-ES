---
title: Tipo de recurso managedAppDiagnosticStatus
description: Representa el estado de diagnóstico.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 98bd1353156c99861749bdb7eac2e686cf96532e
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27869793"
---
# <a name="managedappdiagnosticstatus-resource-type"></a><span data-ttu-id="d9614-103">Tipo de recurso managedAppDiagnosticStatus</span><span class="sxs-lookup"><span data-stu-id="d9614-103">managedAppDiagnosticStatus resource type</span></span>

> <span data-ttu-id="d9614-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="d9614-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="d9614-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="d9614-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="d9614-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="d9614-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="d9614-107">Representa el estado de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="d9614-107">Represents diagnostics status.</span></span>
## <a name="properties"></a><span data-ttu-id="d9614-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d9614-108">Properties</span></span>
|<span data-ttu-id="d9614-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d9614-109">Property</span></span>|<span data-ttu-id="d9614-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="d9614-110">Type</span></span>|<span data-ttu-id="d9614-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="d9614-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="d9614-112">validationName</span><span class="sxs-lookup"><span data-stu-id="d9614-112">validationName</span></span>|<span data-ttu-id="d9614-113">cadena</span><span class="sxs-lookup"><span data-stu-id="d9614-113">String</span></span>|<span data-ttu-id="d9614-114">El nombre descriptivo de validación</span><span class="sxs-lookup"><span data-stu-id="d9614-114">The validation friendly name</span></span>|
|<span data-ttu-id="d9614-115">estado</span><span class="sxs-lookup"><span data-stu-id="d9614-115">state</span></span>|<span data-ttu-id="d9614-116">cadena</span><span class="sxs-lookup"><span data-stu-id="d9614-116">String</span></span>|<span data-ttu-id="d9614-117">El estado actual de la operación.</span><span class="sxs-lookup"><span data-stu-id="d9614-117">The state of the operation</span></span>|
|<span data-ttu-id="d9614-118">mitigationInstruction</span><span class="sxs-lookup"><span data-stu-id="d9614-118">mitigationInstruction</span></span>|<span data-ttu-id="d9614-119">cadena</span><span class="sxs-lookup"><span data-stu-id="d9614-119">String</span></span>|<span data-ttu-id="d9614-120">Instrucciones sobre cómo reducir un error de validación</span><span class="sxs-lookup"><span data-stu-id="d9614-120">Instruction on how to mitigate a failed validation</span></span>|

## <a name="relationships"></a><span data-ttu-id="d9614-121">Relaciones</span><span class="sxs-lookup"><span data-stu-id="d9614-121">Relationships</span></span>
<span data-ttu-id="d9614-122">Ninguna</span><span class="sxs-lookup"><span data-stu-id="d9614-122">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="d9614-123">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="d9614-123">JSON Representation</span></span>
<span data-ttu-id="d9614-124">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="d9614-124">Here is a JSON representation of the resource.</span></span>
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





