---
title: Tipo de recurso remoteLockActionResult
description: Bloquear el resultado de la acción con un PIN de desbloqueo
ms.openlocfilehash: e0fff0a9ee389a1a73db1ad19ea3eba55a04989d
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031208"
---
# <a name="remotelockactionresult-resource-type"></a><span data-ttu-id="641f1-103">Tipo de recurso remoteLockActionResult</span><span class="sxs-lookup"><span data-stu-id="641f1-103">remoteLockActionResult resource type</span></span>

> <span data-ttu-id="641f1-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="641f1-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="641f1-105">Bloquear el resultado de la acción con un PIN de desbloqueo</span><span class="sxs-lookup"><span data-stu-id="641f1-105">Lock action result with a pin to unlock</span></span>

<span data-ttu-id="641f1-106">Hereda de [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span><span class="sxs-lookup"><span data-stu-id="641f1-106">Inherits from [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span></span>

## <a name="properties"></a><span data-ttu-id="641f1-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="641f1-107">Properties</span></span>
|<span data-ttu-id="641f1-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="641f1-108">Property</span></span>|<span data-ttu-id="641f1-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="641f1-109">Type</span></span>|<span data-ttu-id="641f1-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="641f1-110">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="641f1-111">actionName</span><span class="sxs-lookup"><span data-stu-id="641f1-111">actionName</span></span>|<span data-ttu-id="641f1-112">Cadena</span><span class="sxs-lookup"><span data-stu-id="641f1-112">String</span></span>|<span data-ttu-id="641f1-113">Nombre de la acción. Heredado de [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span><span class="sxs-lookup"><span data-stu-id="641f1-113">Action name Inherited from [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span></span>|
|<span data-ttu-id="641f1-114">actionState</span><span class="sxs-lookup"><span data-stu-id="641f1-114">actionState</span></span>|[<span data-ttu-id="641f1-115">actionState</span><span class="sxs-lookup"><span data-stu-id="641f1-115">actionState</span></span>](../resources/intune-devices-actionstate.md)|<span data-ttu-id="641f1-116">Estado de la acción Inherited desde [deviceActionResult](../resources/intune-devices-deviceactionresult.md).</span><span class="sxs-lookup"><span data-stu-id="641f1-116">State of the action Inherited from [deviceActionResult](../resources/intune-devices-deviceactionresult.md).</span></span> <span data-ttu-id="641f1-117">Los valores posibles son: `none`, `pending`, `canceled`, `active`, `done`, `failed` y `notSupported`.</span><span class="sxs-lookup"><span data-stu-id="641f1-117">Possible values are: `none`, `pending`, `canceled`, `active`, `done`, `failed`, `notSupported`.</span></span>|
|<span data-ttu-id="641f1-118">startDateTime</span><span class="sxs-lookup"><span data-stu-id="641f1-118">startDateTime</span></span>|<span data-ttu-id="641f1-119">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="641f1-119">DateTimeOffset</span></span>|<span data-ttu-id="641f1-120">Hora en la que se inició la acción. Heredado de [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span><span class="sxs-lookup"><span data-stu-id="641f1-120">Time the action was initiated Inherited from [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span></span>|
|<span data-ttu-id="641f1-121">lastUpdatedDateTime</span><span class="sxs-lookup"><span data-stu-id="641f1-121">lastUpdatedDateTime</span></span>|<span data-ttu-id="641f1-122">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="641f1-122">DateTimeOffset</span></span>|<span data-ttu-id="641f1-123">Hora en la que se actualizó por última vez el estado de acción. Heredado de [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span><span class="sxs-lookup"><span data-stu-id="641f1-123">Time the action state was last updated Inherited from [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span></span>|
|<span data-ttu-id="641f1-124">unlockPin</span><span class="sxs-lookup"><span data-stu-id="641f1-124">unlockPin</span></span>|<span data-ttu-id="641f1-125">cadena</span><span class="sxs-lookup"><span data-stu-id="641f1-125">String</span></span>|<span data-ttu-id="641f1-126">PIN para desbloquear el cliente</span><span class="sxs-lookup"><span data-stu-id="641f1-126">Pin to unlock the client</span></span>|

## <a name="relationships"></a><span data-ttu-id="641f1-127">Relaciones</span><span class="sxs-lookup"><span data-stu-id="641f1-127">Relationships</span></span>
<span data-ttu-id="641f1-128">Ninguna</span><span class="sxs-lookup"><span data-stu-id="641f1-128">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="641f1-129">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="641f1-129">JSON Representation</span></span>
<span data-ttu-id="641f1-130">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="641f1-130">Here is a JSON representation of the resource.</span></span>
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



