---
title: Tipo de recurso remoteLockActionResult
description: Bloquear el resultado de la acción con un PIN de desbloqueo
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 0ed8931153c70cea877e8db82ed794301664cbd6
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27937778"
---
# <a name="remotelockactionresult-resource-type"></a><span data-ttu-id="123f8-103">Tipo de recurso remoteLockActionResult</span><span class="sxs-lookup"><span data-stu-id="123f8-103">remoteLockActionResult resource type</span></span>

> <span data-ttu-id="123f8-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="123f8-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="123f8-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="123f8-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="123f8-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="123f8-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="123f8-107">Bloquear el resultado de la acción con un PIN de desbloqueo</span><span class="sxs-lookup"><span data-stu-id="123f8-107">Lock action result with a pin to unlock</span></span>

<span data-ttu-id="123f8-108">Hereda de [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span><span class="sxs-lookup"><span data-stu-id="123f8-108">Inherits from [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span></span>

## <a name="properties"></a><span data-ttu-id="123f8-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="123f8-109">Properties</span></span>
|<span data-ttu-id="123f8-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="123f8-110">Property</span></span>|<span data-ttu-id="123f8-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="123f8-111">Type</span></span>|<span data-ttu-id="123f8-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="123f8-112">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="123f8-113">actionName</span><span class="sxs-lookup"><span data-stu-id="123f8-113">actionName</span></span>|<span data-ttu-id="123f8-114">Cadena</span><span class="sxs-lookup"><span data-stu-id="123f8-114">String</span></span>|<span data-ttu-id="123f8-115">Nombre de la acción. Heredado de [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span><span class="sxs-lookup"><span data-stu-id="123f8-115">Action name Inherited from [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span></span>|
|<span data-ttu-id="123f8-116">actionState</span><span class="sxs-lookup"><span data-stu-id="123f8-116">actionState</span></span>|[<span data-ttu-id="123f8-117">actionState</span><span class="sxs-lookup"><span data-stu-id="123f8-117">actionState</span></span>](../resources/intune-shared-actionstate.md)|<span data-ttu-id="123f8-118">Estado de la acción Inherited desde [deviceActionResult](../resources/intune-devices-deviceactionresult.md).</span><span class="sxs-lookup"><span data-stu-id="123f8-118">State of the action Inherited from [deviceActionResult](../resources/intune-devices-deviceactionresult.md).</span></span> <span data-ttu-id="123f8-119">Los valores posibles son: `none`, `pending`, `canceled`, `active`, `done`, `failed` y `notSupported`.</span><span class="sxs-lookup"><span data-stu-id="123f8-119">Possible values are: `none`, `pending`, `canceled`, `active`, `done`, `failed`, `notSupported`.</span></span>|
|<span data-ttu-id="123f8-120">startDateTime</span><span class="sxs-lookup"><span data-stu-id="123f8-120">startDateTime</span></span>|<span data-ttu-id="123f8-121">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="123f8-121">DateTimeOffset</span></span>|<span data-ttu-id="123f8-122">Hora en la que se inició la acción. Heredado de [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span><span class="sxs-lookup"><span data-stu-id="123f8-122">Time the action was initiated Inherited from [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span></span>|
|<span data-ttu-id="123f8-123">lastUpdatedDateTime</span><span class="sxs-lookup"><span data-stu-id="123f8-123">lastUpdatedDateTime</span></span>|<span data-ttu-id="123f8-124">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="123f8-124">DateTimeOffset</span></span>|<span data-ttu-id="123f8-125">Hora en la que se actualizó por última vez el estado de acción. Heredado de [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span><span class="sxs-lookup"><span data-stu-id="123f8-125">Time the action state was last updated Inherited from [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span></span>|
|<span data-ttu-id="123f8-126">unlockPin</span><span class="sxs-lookup"><span data-stu-id="123f8-126">unlockPin</span></span>|<span data-ttu-id="123f8-127">cadena</span><span class="sxs-lookup"><span data-stu-id="123f8-127">String</span></span>|<span data-ttu-id="123f8-128">PIN para desbloquear el cliente</span><span class="sxs-lookup"><span data-stu-id="123f8-128">Pin to unlock the client</span></span>|

## <a name="relationships"></a><span data-ttu-id="123f8-129">Relaciones</span><span class="sxs-lookup"><span data-stu-id="123f8-129">Relationships</span></span>
<span data-ttu-id="123f8-130">Ninguna</span><span class="sxs-lookup"><span data-stu-id="123f8-130">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="123f8-131">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="123f8-131">JSON Representation</span></span>
<span data-ttu-id="123f8-132">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="123f8-132">Here is a JSON representation of the resource.</span></span>
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





