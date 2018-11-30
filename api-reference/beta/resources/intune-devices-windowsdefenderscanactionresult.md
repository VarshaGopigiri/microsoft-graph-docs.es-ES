---
title: Tipo de recurso windowsDefenderScanActionResult
description: Resultado del último análisis de Windows Defender
ms.openlocfilehash: 9adfa41f21bb23f5073f0d62c1c49bc1cfea3912
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089354"
---
# <a name="windowsdefenderscanactionresult-resource-type"></a><span data-ttu-id="e6a4b-103">Tipo de recurso windowsDefenderScanActionResult</span><span class="sxs-lookup"><span data-stu-id="e6a4b-103">windowsDefenderScanActionResult resource type</span></span>

> <span data-ttu-id="e6a4b-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="e6a4b-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="e6a4b-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="e6a4b-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="e6a4b-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="e6a4b-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="e6a4b-107">Resultado del último análisis de Windows Defender</span><span class="sxs-lookup"><span data-stu-id="e6a4b-107">Windows Defender last scan result</span></span>

<span data-ttu-id="e6a4b-108">Hereda de [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span><span class="sxs-lookup"><span data-stu-id="e6a4b-108">Inherits from [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span></span>

## <a name="properties"></a><span data-ttu-id="e6a4b-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e6a4b-109">Properties</span></span>
|<span data-ttu-id="e6a4b-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e6a4b-110">Property</span></span>|<span data-ttu-id="e6a4b-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="e6a4b-111">Type</span></span>|<span data-ttu-id="e6a4b-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="e6a4b-112">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="e6a4b-113">actionName</span><span class="sxs-lookup"><span data-stu-id="e6a4b-113">actionName</span></span>|<span data-ttu-id="e6a4b-114">Cadena</span><span class="sxs-lookup"><span data-stu-id="e6a4b-114">String</span></span>|<span data-ttu-id="e6a4b-115">Nombre de la acción. Heredado de [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span><span class="sxs-lookup"><span data-stu-id="e6a4b-115">Action name Inherited from [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span></span>|
|<span data-ttu-id="e6a4b-116">actionState</span><span class="sxs-lookup"><span data-stu-id="e6a4b-116">actionState</span></span>|[<span data-ttu-id="e6a4b-117">actionState</span><span class="sxs-lookup"><span data-stu-id="e6a4b-117">actionState</span></span>](../resources/intune-shared-actionstate.md)|<span data-ttu-id="e6a4b-118">Estado de la acción Inherited desde [deviceActionResult](../resources/intune-devices-deviceactionresult.md).</span><span class="sxs-lookup"><span data-stu-id="e6a4b-118">State of the action Inherited from [deviceActionResult](../resources/intune-devices-deviceactionresult.md).</span></span> <span data-ttu-id="e6a4b-119">Los valores posibles son: `none`, `pending`, `canceled`, `active`, `done`, `failed` y `notSupported`.</span><span class="sxs-lookup"><span data-stu-id="e6a4b-119">Possible values are: `none`, `pending`, `canceled`, `active`, `done`, `failed`, `notSupported`.</span></span>|
|<span data-ttu-id="e6a4b-120">startDateTime</span><span class="sxs-lookup"><span data-stu-id="e6a4b-120">startDateTime</span></span>|<span data-ttu-id="e6a4b-121">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="e6a4b-121">DateTimeOffset</span></span>|<span data-ttu-id="e6a4b-122">Hora en la que se inició la acción. Heredado de [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span><span class="sxs-lookup"><span data-stu-id="e6a4b-122">Time the action was initiated Inherited from [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span></span>|
|<span data-ttu-id="e6a4b-123">lastUpdatedDateTime</span><span class="sxs-lookup"><span data-stu-id="e6a4b-123">lastUpdatedDateTime</span></span>|<span data-ttu-id="e6a4b-124">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="e6a4b-124">DateTimeOffset</span></span>|<span data-ttu-id="e6a4b-125">Hora en la que se actualizó por última vez el estado de acción. Heredado de [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span><span class="sxs-lookup"><span data-stu-id="e6a4b-125">Time the action state was last updated Inherited from [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span></span>|
|<span data-ttu-id="e6a4b-126">scanType</span><span class="sxs-lookup"><span data-stu-id="e6a4b-126">scanType</span></span>|<span data-ttu-id="e6a4b-127">cadena</span><span class="sxs-lookup"><span data-stu-id="e6a4b-127">String</span></span>|<span data-ttu-id="e6a4b-128">Tipo de análisis, sea análisis completo o análisis rápido</span><span class="sxs-lookup"><span data-stu-id="e6a4b-128">Scan type either full scan or quick scan</span></span>|

## <a name="relationships"></a><span data-ttu-id="e6a4b-129">Relaciones</span><span class="sxs-lookup"><span data-stu-id="e6a4b-129">Relationships</span></span>
<span data-ttu-id="e6a4b-130">Ninguna</span><span class="sxs-lookup"><span data-stu-id="e6a4b-130">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="e6a4b-131">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="e6a4b-131">JSON Representation</span></span>
<span data-ttu-id="e6a4b-132">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="e6a4b-132">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.windowsDefenderScanActionResult"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.windowsDefenderScanActionResult",
  "actionName": "String",
  "actionState": "String",
  "startDateTime": "String (timestamp)",
  "lastUpdatedDateTime": "String (timestamp)",
  "scanType": "String"
}
```





