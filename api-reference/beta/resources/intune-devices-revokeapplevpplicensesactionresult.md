---
title: tipo de recurso revokeAppleVppLicensesActionResult
description: Revocar el resultado de la acción de Apple Vpp licencias
author: tfitzmac
ms.openlocfilehash: b45a2ddec46ddc5cac47937cb776d0f0da6c64a8
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27361050"
---
# <a name="revokeapplevpplicensesactionresult-resource-type"></a><span data-ttu-id="65176-103">tipo de recurso revokeAppleVppLicensesActionResult</span><span class="sxs-lookup"><span data-stu-id="65176-103">revokeAppleVppLicensesActionResult resource type</span></span>

> <span data-ttu-id="65176-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="65176-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="65176-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="65176-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="65176-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="65176-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="65176-107">Revocar el resultado de la acción de Apple Vpp licencias</span><span class="sxs-lookup"><span data-stu-id="65176-107">Revoke Apple Vpp licenses action result</span></span>

<span data-ttu-id="65176-108">Hereda de [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span><span class="sxs-lookup"><span data-stu-id="65176-108">Inherits from [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span></span>

## <a name="properties"></a><span data-ttu-id="65176-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="65176-109">Properties</span></span>
|<span data-ttu-id="65176-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="65176-110">Property</span></span>|<span data-ttu-id="65176-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="65176-111">Type</span></span>|<span data-ttu-id="65176-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="65176-112">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="65176-113">actionName</span><span class="sxs-lookup"><span data-stu-id="65176-113">actionName</span></span>|<span data-ttu-id="65176-114">Cadena</span><span class="sxs-lookup"><span data-stu-id="65176-114">String</span></span>|<span data-ttu-id="65176-115">Nombre de la acción. Heredado de [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span><span class="sxs-lookup"><span data-stu-id="65176-115">Action name Inherited from [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span></span>|
|<span data-ttu-id="65176-116">actionState</span><span class="sxs-lookup"><span data-stu-id="65176-116">actionState</span></span>|[<span data-ttu-id="65176-117">actionState</span><span class="sxs-lookup"><span data-stu-id="65176-117">actionState</span></span>](../resources/intune-shared-actionstate.md)|<span data-ttu-id="65176-118">Estado de la acción Inherited desde [deviceActionResult](../resources/intune-devices-deviceactionresult.md).</span><span class="sxs-lookup"><span data-stu-id="65176-118">State of the action Inherited from [deviceActionResult](../resources/intune-devices-deviceactionresult.md).</span></span> <span data-ttu-id="65176-119">Los valores posibles son: `none`, `pending`, `canceled`, `active`, `done`, `failed` y `notSupported`.</span><span class="sxs-lookup"><span data-stu-id="65176-119">Possible values are: `none`, `pending`, `canceled`, `active`, `done`, `failed`, `notSupported`.</span></span>|
|<span data-ttu-id="65176-120">startDateTime</span><span class="sxs-lookup"><span data-stu-id="65176-120">startDateTime</span></span>|<span data-ttu-id="65176-121">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="65176-121">DateTimeOffset</span></span>|<span data-ttu-id="65176-122">Hora en la que se inició la acción. Heredado de [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span><span class="sxs-lookup"><span data-stu-id="65176-122">Time the action was initiated Inherited from [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span></span>|
|<span data-ttu-id="65176-123">lastUpdatedDateTime</span><span class="sxs-lookup"><span data-stu-id="65176-123">lastUpdatedDateTime</span></span>|<span data-ttu-id="65176-124">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="65176-124">DateTimeOffset</span></span>|<span data-ttu-id="65176-125">Hora en la que se actualizó por última vez el estado de acción. Heredado de [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span><span class="sxs-lookup"><span data-stu-id="65176-125">Time the action state was last updated Inherited from [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span></span>|
|<span data-ttu-id="65176-126">totalLicensesCount</span><span class="sxs-lookup"><span data-stu-id="65176-126">totalLicensesCount</span></span>|<span data-ttu-id="65176-127">Int32</span><span class="sxs-lookup"><span data-stu-id="65176-127">Int32</span></span>|<span data-ttu-id="65176-128">Número total de licencias de Apple Vpp asociadas</span><span class="sxs-lookup"><span data-stu-id="65176-128">Total number of Apple Vpp licenses associated</span></span>|
|<span data-ttu-id="65176-129">failedLicensesCount</span><span class="sxs-lookup"><span data-stu-id="65176-129">failedLicensesCount</span></span>|<span data-ttu-id="65176-130">Int32</span><span class="sxs-lookup"><span data-stu-id="65176-130">Int32</span></span>|<span data-ttu-id="65176-131">Número total de licencias de Apple Vpp que no se pudo revocar</span><span class="sxs-lookup"><span data-stu-id="65176-131">Total number of Apple Vpp licenses that failed to revoke</span></span>|

## <a name="relationships"></a><span data-ttu-id="65176-132">Relaciones</span><span class="sxs-lookup"><span data-stu-id="65176-132">Relationships</span></span>
<span data-ttu-id="65176-133">Ninguna</span><span class="sxs-lookup"><span data-stu-id="65176-133">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="65176-134">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="65176-134">JSON Representation</span></span>
<span data-ttu-id="65176-135">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="65176-135">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.revokeAppleVppLicensesActionResult"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.revokeAppleVppLicensesActionResult",
  "actionName": "String",
  "actionState": "String",
  "startDateTime": "String (timestamp)",
  "lastUpdatedDateTime": "String (timestamp)",
  "totalLicensesCount": 1024,
  "failedLicensesCount": 1024
}
```





