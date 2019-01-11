---
title: Tipo de recurso remoteLockActionResult
description: Bloquear el resultado de la acción con un PIN de desbloqueo
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 0feb3c4474e543b4da462ddab499c4e8fff5f0cf
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27875344"
---
# <a name="remotelockactionresult-resource-type"></a><span data-ttu-id="a7107-103">Tipo de recurso remoteLockActionResult</span><span class="sxs-lookup"><span data-stu-id="a7107-103">remoteLockActionResult resource type</span></span>

> <span data-ttu-id="a7107-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="a7107-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="a7107-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="a7107-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="a7107-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="a7107-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="a7107-107">Bloquear el resultado de la acción con un PIN de desbloqueo</span><span class="sxs-lookup"><span data-stu-id="a7107-107">Lock action result with a pin to unlock</span></span>

<span data-ttu-id="a7107-108">Hereda de [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span><span class="sxs-lookup"><span data-stu-id="a7107-108">Inherits from [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span></span>

## <a name="properties"></a><span data-ttu-id="a7107-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a7107-109">Properties</span></span>
|<span data-ttu-id="a7107-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a7107-110">Property</span></span>|<span data-ttu-id="a7107-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="a7107-111">Type</span></span>|<span data-ttu-id="a7107-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="a7107-112">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="a7107-113">actionName</span><span class="sxs-lookup"><span data-stu-id="a7107-113">actionName</span></span>|<span data-ttu-id="a7107-114">Cadena</span><span class="sxs-lookup"><span data-stu-id="a7107-114">String</span></span>|<span data-ttu-id="a7107-115">Nombre de la acción. Heredado de [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span><span class="sxs-lookup"><span data-stu-id="a7107-115">Action name Inherited from [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span></span>|
|<span data-ttu-id="a7107-116">actionState</span><span class="sxs-lookup"><span data-stu-id="a7107-116">actionState</span></span>|[<span data-ttu-id="a7107-117">actionState</span><span class="sxs-lookup"><span data-stu-id="a7107-117">actionState</span></span>](../resources/intune-shared-actionstate.md)|<span data-ttu-id="a7107-118">Estado de la acción Inherited desde [deviceActionResult](../resources/intune-devices-deviceactionresult.md).</span><span class="sxs-lookup"><span data-stu-id="a7107-118">State of the action Inherited from [deviceActionResult](../resources/intune-devices-deviceactionresult.md).</span></span> <span data-ttu-id="a7107-119">Los valores posibles son: `none`, `pending`, `canceled`, `active`, `done`, `failed` y `notSupported`.</span><span class="sxs-lookup"><span data-stu-id="a7107-119">Possible values are: `none`, `pending`, `canceled`, `active`, `done`, `failed`, `notSupported`.</span></span>|
|<span data-ttu-id="a7107-120">startDateTime</span><span class="sxs-lookup"><span data-stu-id="a7107-120">startDateTime</span></span>|<span data-ttu-id="a7107-121">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="a7107-121">DateTimeOffset</span></span>|<span data-ttu-id="a7107-122">Hora en la que se inició la acción. Heredado de [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span><span class="sxs-lookup"><span data-stu-id="a7107-122">Time the action was initiated Inherited from [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span></span>|
|<span data-ttu-id="a7107-123">lastUpdatedDateTime</span><span class="sxs-lookup"><span data-stu-id="a7107-123">lastUpdatedDateTime</span></span>|<span data-ttu-id="a7107-124">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="a7107-124">DateTimeOffset</span></span>|<span data-ttu-id="a7107-125">Hora en la que se actualizó por última vez el estado de acción. Heredado de [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span><span class="sxs-lookup"><span data-stu-id="a7107-125">Time the action state was last updated Inherited from [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span></span>|
|<span data-ttu-id="a7107-126">unlockPin</span><span class="sxs-lookup"><span data-stu-id="a7107-126">unlockPin</span></span>|<span data-ttu-id="a7107-127">cadena</span><span class="sxs-lookup"><span data-stu-id="a7107-127">String</span></span>|<span data-ttu-id="a7107-128">PIN para desbloquear el cliente</span><span class="sxs-lookup"><span data-stu-id="a7107-128">Pin to unlock the client</span></span>|

## <a name="relationships"></a><span data-ttu-id="a7107-129">Relaciones</span><span class="sxs-lookup"><span data-stu-id="a7107-129">Relationships</span></span>
<span data-ttu-id="a7107-130">Ninguna</span><span class="sxs-lookup"><span data-stu-id="a7107-130">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="a7107-131">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="a7107-131">JSON Representation</span></span>
<span data-ttu-id="a7107-132">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="a7107-132">Here is a JSON representation of the resource.</span></span>
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





