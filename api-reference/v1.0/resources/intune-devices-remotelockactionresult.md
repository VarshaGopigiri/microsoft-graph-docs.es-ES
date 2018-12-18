---
title: Tipo de recurso remoteLockActionResult
description: Bloquear el resultado de la acción con un PIN de desbloqueo
author: tfitzmac
ms.openlocfilehash: 44d56b2ee20629d1cefbf965c72e5f6cc17fb0a2
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27353693"
---
# <a name="remotelockactionresult-resource-type"></a><span data-ttu-id="0208d-103">Tipo de recurso remoteLockActionResult</span><span class="sxs-lookup"><span data-stu-id="0208d-103">remoteLockActionResult resource type</span></span>

> <span data-ttu-id="0208d-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="0208d-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="0208d-105">Bloquear el resultado de la acción con un PIN de desbloqueo</span><span class="sxs-lookup"><span data-stu-id="0208d-105">Lock action result with a pin to unlock</span></span>

<span data-ttu-id="0208d-106">Hereda de [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span><span class="sxs-lookup"><span data-stu-id="0208d-106">Inherits from [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span></span>

## <a name="properties"></a><span data-ttu-id="0208d-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0208d-107">Properties</span></span>
|<span data-ttu-id="0208d-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="0208d-108">Property</span></span>|<span data-ttu-id="0208d-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="0208d-109">Type</span></span>|<span data-ttu-id="0208d-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="0208d-110">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="0208d-111">actionName</span><span class="sxs-lookup"><span data-stu-id="0208d-111">actionName</span></span>|<span data-ttu-id="0208d-112">Cadena</span><span class="sxs-lookup"><span data-stu-id="0208d-112">String</span></span>|<span data-ttu-id="0208d-113">Nombre de la acción. Heredado de [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span><span class="sxs-lookup"><span data-stu-id="0208d-113">Action name Inherited from [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span></span>|
|<span data-ttu-id="0208d-114">actionState</span><span class="sxs-lookup"><span data-stu-id="0208d-114">actionState</span></span>|[<span data-ttu-id="0208d-115">actionState</span><span class="sxs-lookup"><span data-stu-id="0208d-115">actionState</span></span>](../resources/intune-devices-actionstate.md)|<span data-ttu-id="0208d-116">Estado de la acción Inherited desde [deviceActionResult](../resources/intune-devices-deviceactionresult.md).</span><span class="sxs-lookup"><span data-stu-id="0208d-116">State of the action Inherited from [deviceActionResult](../resources/intune-devices-deviceactionresult.md).</span></span> <span data-ttu-id="0208d-117">Los valores posibles son: `none`, `pending`, `canceled`, `active`, `done`, `failed` y `notSupported`.</span><span class="sxs-lookup"><span data-stu-id="0208d-117">Possible values are: `none`, `pending`, `canceled`, `active`, `done`, `failed`, `notSupported`.</span></span>|
|<span data-ttu-id="0208d-118">startDateTime</span><span class="sxs-lookup"><span data-stu-id="0208d-118">startDateTime</span></span>|<span data-ttu-id="0208d-119">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="0208d-119">DateTimeOffset</span></span>|<span data-ttu-id="0208d-120">Hora en la que se inició la acción. Heredado de [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span><span class="sxs-lookup"><span data-stu-id="0208d-120">Time the action was initiated Inherited from [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span></span>|
|<span data-ttu-id="0208d-121">lastUpdatedDateTime</span><span class="sxs-lookup"><span data-stu-id="0208d-121">lastUpdatedDateTime</span></span>|<span data-ttu-id="0208d-122">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="0208d-122">DateTimeOffset</span></span>|<span data-ttu-id="0208d-123">Hora en la que se actualizó por última vez el estado de acción. Heredado de [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span><span class="sxs-lookup"><span data-stu-id="0208d-123">Time the action state was last updated Inherited from [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span></span>|
|<span data-ttu-id="0208d-124">unlockPin</span><span class="sxs-lookup"><span data-stu-id="0208d-124">unlockPin</span></span>|<span data-ttu-id="0208d-125">cadena</span><span class="sxs-lookup"><span data-stu-id="0208d-125">String</span></span>|<span data-ttu-id="0208d-126">PIN para desbloquear el cliente</span><span class="sxs-lookup"><span data-stu-id="0208d-126">Pin to unlock the client</span></span>|

## <a name="relationships"></a><span data-ttu-id="0208d-127">Relaciones</span><span class="sxs-lookup"><span data-stu-id="0208d-127">Relationships</span></span>
<span data-ttu-id="0208d-128">Ninguna</span><span class="sxs-lookup"><span data-stu-id="0208d-128">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="0208d-129">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="0208d-129">JSON Representation</span></span>
<span data-ttu-id="0208d-130">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="0208d-130">Here is a JSON representation of the resource.</span></span>
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



