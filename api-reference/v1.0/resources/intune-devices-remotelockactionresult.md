---
title: Tipo de recurso remoteLockActionResult
description: Bloquear el resultado de la acción con un PIN de desbloqueo
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 341d1425de71c7175346e1ba6b30fe2a81b696a4
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27922721"
---
# <a name="remotelockactionresult-resource-type"></a><span data-ttu-id="40941-103">Tipo de recurso remoteLockActionResult</span><span class="sxs-lookup"><span data-stu-id="40941-103">remoteLockActionResult resource type</span></span>

> <span data-ttu-id="40941-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="40941-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="40941-105">Bloquear el resultado de la acción con un PIN de desbloqueo</span><span class="sxs-lookup"><span data-stu-id="40941-105">Lock action result with a pin to unlock</span></span>

<span data-ttu-id="40941-106">Hereda de [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span><span class="sxs-lookup"><span data-stu-id="40941-106">Inherits from [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span></span>

## <a name="properties"></a><span data-ttu-id="40941-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="40941-107">Properties</span></span>
|<span data-ttu-id="40941-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="40941-108">Property</span></span>|<span data-ttu-id="40941-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="40941-109">Type</span></span>|<span data-ttu-id="40941-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="40941-110">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="40941-111">actionName</span><span class="sxs-lookup"><span data-stu-id="40941-111">actionName</span></span>|<span data-ttu-id="40941-112">Cadena</span><span class="sxs-lookup"><span data-stu-id="40941-112">String</span></span>|<span data-ttu-id="40941-113">Nombre de la acción. Heredado de [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span><span class="sxs-lookup"><span data-stu-id="40941-113">Action name Inherited from [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span></span>|
|<span data-ttu-id="40941-114">actionState</span><span class="sxs-lookup"><span data-stu-id="40941-114">actionState</span></span>|[<span data-ttu-id="40941-115">actionState</span><span class="sxs-lookup"><span data-stu-id="40941-115">actionState</span></span>](../resources/intune-devices-actionstate.md)|<span data-ttu-id="40941-116">Estado de la acción Inherited desde [deviceActionResult](../resources/intune-devices-deviceactionresult.md).</span><span class="sxs-lookup"><span data-stu-id="40941-116">State of the action Inherited from [deviceActionResult](../resources/intune-devices-deviceactionresult.md).</span></span> <span data-ttu-id="40941-117">Los valores posibles son: `none`, `pending`, `canceled`, `active`, `done`, `failed` y `notSupported`.</span><span class="sxs-lookup"><span data-stu-id="40941-117">Possible values are: `none`, `pending`, `canceled`, `active`, `done`, `failed`, `notSupported`.</span></span>|
|<span data-ttu-id="40941-118">startDateTime</span><span class="sxs-lookup"><span data-stu-id="40941-118">startDateTime</span></span>|<span data-ttu-id="40941-119">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="40941-119">DateTimeOffset</span></span>|<span data-ttu-id="40941-120">Hora en la que se inició la acción. Heredado de [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span><span class="sxs-lookup"><span data-stu-id="40941-120">Time the action was initiated Inherited from [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span></span>|
|<span data-ttu-id="40941-121">lastUpdatedDateTime</span><span class="sxs-lookup"><span data-stu-id="40941-121">lastUpdatedDateTime</span></span>|<span data-ttu-id="40941-122">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="40941-122">DateTimeOffset</span></span>|<span data-ttu-id="40941-123">Hora en la que se actualizó por última vez el estado de acción. Heredado de [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span><span class="sxs-lookup"><span data-stu-id="40941-123">Time the action state was last updated Inherited from [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span></span>|
|<span data-ttu-id="40941-124">unlockPin</span><span class="sxs-lookup"><span data-stu-id="40941-124">unlockPin</span></span>|<span data-ttu-id="40941-125">cadena</span><span class="sxs-lookup"><span data-stu-id="40941-125">String</span></span>|<span data-ttu-id="40941-126">PIN para desbloquear el cliente</span><span class="sxs-lookup"><span data-stu-id="40941-126">Pin to unlock the client</span></span>|

## <a name="relationships"></a><span data-ttu-id="40941-127">Relaciones</span><span class="sxs-lookup"><span data-stu-id="40941-127">Relationships</span></span>
<span data-ttu-id="40941-128">Ninguna</span><span class="sxs-lookup"><span data-stu-id="40941-128">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="40941-129">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="40941-129">JSON Representation</span></span>
<span data-ttu-id="40941-130">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="40941-130">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.remoteLockActionResult"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.remoteLockActionResult",
  "actionName": "String",
  "actionState": "String",
  "startDateTime": "String (timestamp)",
  "lastUpdatedDateTime": "String (timestamp)",
  "unlockPin": "String"
}
```



