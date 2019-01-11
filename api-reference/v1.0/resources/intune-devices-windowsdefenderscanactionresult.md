---
title: Tipo de recurso windowsDefenderScanActionResult
description: Resultado del último análisis de Windows Defender
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 407db79fa0caf333dfb092620320aeb339e1b195
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27812155"
---
# <a name="windowsdefenderscanactionresult-resource-type"></a><span data-ttu-id="688db-103">Tipo de recurso windowsDefenderScanActionResult</span><span class="sxs-lookup"><span data-stu-id="688db-103">windowsDefenderScanActionResult resource type</span></span>

> <span data-ttu-id="688db-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="688db-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="688db-105">Resultado del último análisis de Windows Defender</span><span class="sxs-lookup"><span data-stu-id="688db-105">Windows Defender last scan result</span></span>

<span data-ttu-id="688db-106">Hereda de [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span><span class="sxs-lookup"><span data-stu-id="688db-106">Inherits from [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span></span>

## <a name="properties"></a><span data-ttu-id="688db-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="688db-107">Properties</span></span>
|<span data-ttu-id="688db-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="688db-108">Property</span></span>|<span data-ttu-id="688db-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="688db-109">Type</span></span>|<span data-ttu-id="688db-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="688db-110">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="688db-111">actionName</span><span class="sxs-lookup"><span data-stu-id="688db-111">actionName</span></span>|<span data-ttu-id="688db-112">Cadena</span><span class="sxs-lookup"><span data-stu-id="688db-112">String</span></span>|<span data-ttu-id="688db-113">Nombre de la acción. Heredado de [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span><span class="sxs-lookup"><span data-stu-id="688db-113">Action name Inherited from [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span></span>|
|<span data-ttu-id="688db-114">actionState</span><span class="sxs-lookup"><span data-stu-id="688db-114">actionState</span></span>|[<span data-ttu-id="688db-115">actionState</span><span class="sxs-lookup"><span data-stu-id="688db-115">actionState</span></span>](../resources/intune-devices-actionstate.md)|<span data-ttu-id="688db-116">Estado de la acción Inherited desde [deviceActionResult](../resources/intune-devices-deviceactionresult.md).</span><span class="sxs-lookup"><span data-stu-id="688db-116">State of the action Inherited from [deviceActionResult](../resources/intune-devices-deviceactionresult.md).</span></span> <span data-ttu-id="688db-117">Los valores posibles son: `none`, `pending`, `canceled`, `active`, `done`, `failed` y `notSupported`.</span><span class="sxs-lookup"><span data-stu-id="688db-117">Possible values are: `none`, `pending`, `canceled`, `active`, `done`, `failed`, `notSupported`.</span></span>|
|<span data-ttu-id="688db-118">startDateTime</span><span class="sxs-lookup"><span data-stu-id="688db-118">startDateTime</span></span>|<span data-ttu-id="688db-119">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="688db-119">DateTimeOffset</span></span>|<span data-ttu-id="688db-120">Hora en la que se inició la acción. Heredado de [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span><span class="sxs-lookup"><span data-stu-id="688db-120">Time the action was initiated Inherited from [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span></span>|
|<span data-ttu-id="688db-121">lastUpdatedDateTime</span><span class="sxs-lookup"><span data-stu-id="688db-121">lastUpdatedDateTime</span></span>|<span data-ttu-id="688db-122">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="688db-122">DateTimeOffset</span></span>|<span data-ttu-id="688db-123">Hora en la que se actualizó por última vez el estado de acción. Heredado de [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span><span class="sxs-lookup"><span data-stu-id="688db-123">Time the action state was last updated Inherited from [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span></span>|
|<span data-ttu-id="688db-124">scanType</span><span class="sxs-lookup"><span data-stu-id="688db-124">scanType</span></span>|<span data-ttu-id="688db-125">cadena</span><span class="sxs-lookup"><span data-stu-id="688db-125">String</span></span>|<span data-ttu-id="688db-126">Tipo de análisis, sea análisis completo o análisis rápido</span><span class="sxs-lookup"><span data-stu-id="688db-126">Scan type either full scan or quick scan</span></span>|

## <a name="relationships"></a><span data-ttu-id="688db-127">Relaciones</span><span class="sxs-lookup"><span data-stu-id="688db-127">Relationships</span></span>
<span data-ttu-id="688db-128">Ninguna</span><span class="sxs-lookup"><span data-stu-id="688db-128">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="688db-129">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="688db-129">JSON Representation</span></span>
<span data-ttu-id="688db-130">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="688db-130">Here is a JSON representation of the resource.</span></span>
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



