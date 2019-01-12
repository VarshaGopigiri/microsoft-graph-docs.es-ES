---
title: tipo de recurso revokeAppleVppLicensesActionResult
description: Revocar el resultado de la acción de Apple Vpp licencias
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: dfb2c18f89dde36ef0fbda7a6ad3221e2ad3728f
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27944484"
---
# <a name="revokeapplevpplicensesactionresult-resource-type"></a><span data-ttu-id="b3eb3-103">tipo de recurso revokeAppleVppLicensesActionResult</span><span class="sxs-lookup"><span data-stu-id="b3eb3-103">revokeAppleVppLicensesActionResult resource type</span></span>

> <span data-ttu-id="b3eb3-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="b3eb3-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="b3eb3-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="b3eb3-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="b3eb3-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="b3eb3-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="b3eb3-107">Revocar el resultado de la acción de Apple Vpp licencias</span><span class="sxs-lookup"><span data-stu-id="b3eb3-107">Revoke Apple Vpp licenses action result</span></span>

<span data-ttu-id="b3eb3-108">Hereda de [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span><span class="sxs-lookup"><span data-stu-id="b3eb3-108">Inherits from [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span></span>

## <a name="properties"></a><span data-ttu-id="b3eb3-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b3eb3-109">Properties</span></span>
|<span data-ttu-id="b3eb3-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="b3eb3-110">Property</span></span>|<span data-ttu-id="b3eb3-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="b3eb3-111">Type</span></span>|<span data-ttu-id="b3eb3-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="b3eb3-112">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="b3eb3-113">actionName</span><span class="sxs-lookup"><span data-stu-id="b3eb3-113">actionName</span></span>|<span data-ttu-id="b3eb3-114">Cadena</span><span class="sxs-lookup"><span data-stu-id="b3eb3-114">String</span></span>|<span data-ttu-id="b3eb3-115">Nombre de la acción. Heredado de [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span><span class="sxs-lookup"><span data-stu-id="b3eb3-115">Action name Inherited from [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span></span>|
|<span data-ttu-id="b3eb3-116">actionState</span><span class="sxs-lookup"><span data-stu-id="b3eb3-116">actionState</span></span>|[<span data-ttu-id="b3eb3-117">actionState</span><span class="sxs-lookup"><span data-stu-id="b3eb3-117">actionState</span></span>](../resources/intune-shared-actionstate.md)|<span data-ttu-id="b3eb3-118">Estado de la acción Inherited desde [deviceActionResult](../resources/intune-devices-deviceactionresult.md).</span><span class="sxs-lookup"><span data-stu-id="b3eb3-118">State of the action Inherited from [deviceActionResult](../resources/intune-devices-deviceactionresult.md).</span></span> <span data-ttu-id="b3eb3-119">Los valores posibles son: `none`, `pending`, `canceled`, `active`, `done`, `failed` y `notSupported`.</span><span class="sxs-lookup"><span data-stu-id="b3eb3-119">Possible values are: `none`, `pending`, `canceled`, `active`, `done`, `failed`, `notSupported`.</span></span>|
|<span data-ttu-id="b3eb3-120">startDateTime</span><span class="sxs-lookup"><span data-stu-id="b3eb3-120">startDateTime</span></span>|<span data-ttu-id="b3eb3-121">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="b3eb3-121">DateTimeOffset</span></span>|<span data-ttu-id="b3eb3-122">Hora en la que se inició la acción. Heredado de [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span><span class="sxs-lookup"><span data-stu-id="b3eb3-122">Time the action was initiated Inherited from [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span></span>|
|<span data-ttu-id="b3eb3-123">lastUpdatedDateTime</span><span class="sxs-lookup"><span data-stu-id="b3eb3-123">lastUpdatedDateTime</span></span>|<span data-ttu-id="b3eb3-124">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="b3eb3-124">DateTimeOffset</span></span>|<span data-ttu-id="b3eb3-125">Hora en la que se actualizó por última vez el estado de acción. Heredado de [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span><span class="sxs-lookup"><span data-stu-id="b3eb3-125">Time the action state was last updated Inherited from [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span></span>|
|<span data-ttu-id="b3eb3-126">totalLicensesCount</span><span class="sxs-lookup"><span data-stu-id="b3eb3-126">totalLicensesCount</span></span>|<span data-ttu-id="b3eb3-127">Int32</span><span class="sxs-lookup"><span data-stu-id="b3eb3-127">Int32</span></span>|<span data-ttu-id="b3eb3-128">Número total de licencias de Apple Vpp asociadas</span><span class="sxs-lookup"><span data-stu-id="b3eb3-128">Total number of Apple Vpp licenses associated</span></span>|
|<span data-ttu-id="b3eb3-129">failedLicensesCount</span><span class="sxs-lookup"><span data-stu-id="b3eb3-129">failedLicensesCount</span></span>|<span data-ttu-id="b3eb3-130">Int32</span><span class="sxs-lookup"><span data-stu-id="b3eb3-130">Int32</span></span>|<span data-ttu-id="b3eb3-131">Número total de licencias de Apple Vpp que no se pudo revocar</span><span class="sxs-lookup"><span data-stu-id="b3eb3-131">Total number of Apple Vpp licenses that failed to revoke</span></span>|

## <a name="relationships"></a><span data-ttu-id="b3eb3-132">Relaciones</span><span class="sxs-lookup"><span data-stu-id="b3eb3-132">Relationships</span></span>
<span data-ttu-id="b3eb3-133">Ninguna</span><span class="sxs-lookup"><span data-stu-id="b3eb3-133">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="b3eb3-134">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="b3eb3-134">JSON Representation</span></span>
<span data-ttu-id="b3eb3-135">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="b3eb3-135">Here is a JSON representation of the resource.</span></span>
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





