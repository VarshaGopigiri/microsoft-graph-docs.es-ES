---
title: tipo de recurso iosVppAppRevokeLicensesActionResult
description: Define los resultados de acciones en iOS aplicaciones Vpp, contiene propiedades heredadas para ActionResult.
localization_priority: Normal
ms.openlocfilehash: 8ed57465e263245cfc18ca22899c2142d949855d
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27842087"
---
# <a name="iosvppapprevokelicensesactionresult-resource-type"></a><span data-ttu-id="52f0b-103">tipo de recurso iosVppAppRevokeLicensesActionResult</span><span class="sxs-lookup"><span data-stu-id="52f0b-103">iosVppAppRevokeLicensesActionResult resource type</span></span>

> <span data-ttu-id="52f0b-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="52f0b-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="52f0b-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="52f0b-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="52f0b-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="52f0b-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="52f0b-107">Define los resultados de acciones en iOS aplicaciones Vpp, contiene propiedades heredadas para ActionResult.</span><span class="sxs-lookup"><span data-stu-id="52f0b-107">Defines results for actions on iOS Vpp Apps, contains inherited properties for ActionResult.</span></span>
## <a name="properties"></a><span data-ttu-id="52f0b-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="52f0b-108">Properties</span></span>
|<span data-ttu-id="52f0b-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="52f0b-109">Property</span></span>|<span data-ttu-id="52f0b-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="52f0b-110">Type</span></span>|<span data-ttu-id="52f0b-111">Description</span><span class="sxs-lookup"><span data-stu-id="52f0b-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="52f0b-112">userId</span><span class="sxs-lookup"><span data-stu-id="52f0b-112">userId</span></span>|<span data-ttu-id="52f0b-113">Cadena</span><span class="sxs-lookup"><span data-stu-id="52f0b-113">String</span></span>|<span data-ttu-id="52f0b-114">Identificador de usuario asociado con la acción.</span><span class="sxs-lookup"><span data-stu-id="52f0b-114">UserId associated with the action.</span></span>|
|<span data-ttu-id="52f0b-115">managedDeviceId</span><span class="sxs-lookup"><span data-stu-id="52f0b-115">managedDeviceId</span></span>|<span data-ttu-id="52f0b-116">Cadena</span><span class="sxs-lookup"><span data-stu-id="52f0b-116">String</span></span>|<span data-ttu-id="52f0b-117">DeviceId asociado con la acción.</span><span class="sxs-lookup"><span data-stu-id="52f0b-117">DeviceId associated with the action.</span></span>|
|<span data-ttu-id="52f0b-118">totalLicensesCount</span><span class="sxs-lookup"><span data-stu-id="52f0b-118">totalLicensesCount</span></span>|<span data-ttu-id="52f0b-119">Int32</span><span class="sxs-lookup"><span data-stu-id="52f0b-119">Int32</span></span>|<span data-ttu-id="52f0b-120">Un recuento del número de licencias para el que se ha intentado establecer revoke.</span><span class="sxs-lookup"><span data-stu-id="52f0b-120">A count of the number of licenses for which revoke was attempted.</span></span>|
|<span data-ttu-id="52f0b-121">failedLicensesCount</span><span class="sxs-lookup"><span data-stu-id="52f0b-121">failedLicensesCount</span></span>|<span data-ttu-id="52f0b-122">Int32</span><span class="sxs-lookup"><span data-stu-id="52f0b-122">Int32</span></span>|<span data-ttu-id="52f0b-123">Un recuento del número de licencias para qué revoke no se pudo.</span><span class="sxs-lookup"><span data-stu-id="52f0b-123">A count of the number of licenses for which revoke failed.</span></span>|
|<span data-ttu-id="52f0b-124">actionFailureReason</span><span class="sxs-lookup"><span data-stu-id="52f0b-124">actionFailureReason</span></span>|[<span data-ttu-id="52f0b-125">vppTokenActionFailureReason</span><span class="sxs-lookup"><span data-stu-id="52f0b-125">vppTokenActionFailureReason</span></span>](../resources/intune-shared-vpptokenactionfailurereason.md)|<span data-ttu-id="52f0b-126">El motivo del error de acción de licencias revoke.</span><span class="sxs-lookup"><span data-stu-id="52f0b-126">The reason for the revoke licenses action failure.</span></span> <span data-ttu-id="52f0b-127">Los valores posibles son: `none`, `appleFailure`, `internalError`, `expiredVppToken` y `expiredApplePushNotificationCertificate`.</span><span class="sxs-lookup"><span data-stu-id="52f0b-127">Possible values are: `none`, `appleFailure`, `internalError`, `expiredVppToken`, `expiredApplePushNotificationCertificate`.</span></span>|
|<span data-ttu-id="52f0b-128">actionName</span><span class="sxs-lookup"><span data-stu-id="52f0b-128">actionName</span></span>|<span data-ttu-id="52f0b-129">cadena</span><span class="sxs-lookup"><span data-stu-id="52f0b-129">String</span></span>|<span data-ttu-id="52f0b-130">Nombre de acción</span><span class="sxs-lookup"><span data-stu-id="52f0b-130">Action name</span></span>|
|<span data-ttu-id="52f0b-131">actionState</span><span class="sxs-lookup"><span data-stu-id="52f0b-131">actionState</span></span>|[<span data-ttu-id="52f0b-132">actionState</span><span class="sxs-lookup"><span data-stu-id="52f0b-132">actionState</span></span>](../resources/intune-shared-actionstate.md)|<span data-ttu-id="52f0b-133">Estado de la acción.</span><span class="sxs-lookup"><span data-stu-id="52f0b-133">State of the action.</span></span> <span data-ttu-id="52f0b-134">Los valores posibles son: `none`, `pending`, `canceled`, `active`, `done`, `failed` y `notSupported`.</span><span class="sxs-lookup"><span data-stu-id="52f0b-134">Possible values are: `none`, `pending`, `canceled`, `active`, `done`, `failed`, `notSupported`.</span></span>|
|<span data-ttu-id="52f0b-135">startDateTime</span><span class="sxs-lookup"><span data-stu-id="52f0b-135">startDateTime</span></span>|<span data-ttu-id="52f0b-136">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="52f0b-136">DateTimeOffset</span></span>|<span data-ttu-id="52f0b-137">Hora a la que se inició la acción</span><span class="sxs-lookup"><span data-stu-id="52f0b-137">Time the action was initiated</span></span>|
|<span data-ttu-id="52f0b-138">lastUpdatedDateTime</span><span class="sxs-lookup"><span data-stu-id="52f0b-138">lastUpdatedDateTime</span></span>|<span data-ttu-id="52f0b-139">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="52f0b-139">DateTimeOffset</span></span>|<span data-ttu-id="52f0b-140">Hora en la que se actualizó por última vez el estado de la acción</span><span class="sxs-lookup"><span data-stu-id="52f0b-140">Time the action state was last updated</span></span>|

## <a name="relationships"></a><span data-ttu-id="52f0b-141">Relaciones</span><span class="sxs-lookup"><span data-stu-id="52f0b-141">Relationships</span></span>
<span data-ttu-id="52f0b-142">Ninguna</span><span class="sxs-lookup"><span data-stu-id="52f0b-142">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="52f0b-143">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="52f0b-143">JSON Representation</span></span>
<span data-ttu-id="52f0b-144">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="52f0b-144">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.iosVppAppRevokeLicensesActionResult"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.iosVppAppRevokeLicensesActionResult",
  "userId": "String",
  "managedDeviceId": "String",
  "totalLicensesCount": 1024,
  "failedLicensesCount": 1024,
  "actionFailureReason": "String",
  "actionName": "String",
  "actionState": "String",
  "startDateTime": "String (timestamp)",
  "lastUpdatedDateTime": "String (timestamp)"
}
```





