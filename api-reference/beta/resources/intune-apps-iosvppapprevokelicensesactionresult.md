---
title: tipo de recurso iosVppAppRevokeLicensesActionResult
description: Define los resultados de acciones en iOS aplicaciones Vpp, contiene propiedades heredadas para ActionResult.
ms.openlocfilehash: 1c6c1486d63ba5ce7c866dc2697d1a3eb2ee8e38
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089895"
---
# <a name="iosvppapprevokelicensesactionresult-resource-type"></a><span data-ttu-id="d8513-103">tipo de recurso iosVppAppRevokeLicensesActionResult</span><span class="sxs-lookup"><span data-stu-id="d8513-103">iosVppAppRevokeLicensesActionResult resource type</span></span>

> <span data-ttu-id="d8513-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="d8513-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="d8513-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="d8513-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="d8513-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="d8513-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="d8513-107">Define los resultados de acciones en iOS aplicaciones Vpp, contiene propiedades heredadas para ActionResult.</span><span class="sxs-lookup"><span data-stu-id="d8513-107">Defines results for actions on iOS Vpp Apps, contains inherited properties for ActionResult.</span></span>
## <a name="properties"></a><span data-ttu-id="d8513-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d8513-108">Properties</span></span>
|<span data-ttu-id="d8513-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d8513-109">Property</span></span>|<span data-ttu-id="d8513-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="d8513-110">Type</span></span>|<span data-ttu-id="d8513-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="d8513-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="d8513-112">userId</span><span class="sxs-lookup"><span data-stu-id="d8513-112">userId</span></span>|<span data-ttu-id="d8513-113">String</span><span class="sxs-lookup"><span data-stu-id="d8513-113">String</span></span>|<span data-ttu-id="d8513-114">Identificador de usuario asociado con la acción.</span><span class="sxs-lookup"><span data-stu-id="d8513-114">UserId associated with the action.</span></span>|
|<span data-ttu-id="d8513-115">managedDeviceId</span><span class="sxs-lookup"><span data-stu-id="d8513-115">managedDeviceId</span></span>|<span data-ttu-id="d8513-116">String</span><span class="sxs-lookup"><span data-stu-id="d8513-116">String</span></span>|<span data-ttu-id="d8513-117">DeviceId asociado con la acción.</span><span class="sxs-lookup"><span data-stu-id="d8513-117">DeviceId associated with the action.</span></span>|
|<span data-ttu-id="d8513-118">totalLicensesCount</span><span class="sxs-lookup"><span data-stu-id="d8513-118">totalLicensesCount</span></span>|<span data-ttu-id="d8513-119">Int32</span><span class="sxs-lookup"><span data-stu-id="d8513-119">Int32</span></span>|<span data-ttu-id="d8513-120">Un recuento del número de licencias para el que se ha intentado establecer revoke.</span><span class="sxs-lookup"><span data-stu-id="d8513-120">A count of the number of licenses for which revoke was attempted.</span></span>|
|<span data-ttu-id="d8513-121">failedLicensesCount</span><span class="sxs-lookup"><span data-stu-id="d8513-121">failedLicensesCount</span></span>|<span data-ttu-id="d8513-122">Int32</span><span class="sxs-lookup"><span data-stu-id="d8513-122">Int32</span></span>|<span data-ttu-id="d8513-123">Un recuento del número de licencias para qué revoke no se pudo.</span><span class="sxs-lookup"><span data-stu-id="d8513-123">A count of the number of licenses for which revoke failed.</span></span>|
|<span data-ttu-id="d8513-124">actionFailureReason</span><span class="sxs-lookup"><span data-stu-id="d8513-124">actionFailureReason</span></span>|[<span data-ttu-id="d8513-125">vppTokenActionFailureReason</span><span class="sxs-lookup"><span data-stu-id="d8513-125">vppTokenActionFailureReason</span></span>](../resources/intune-shared-vpptokenactionfailurereason.md)|<span data-ttu-id="d8513-126">El motivo del error de acción de licencias revoke.</span><span class="sxs-lookup"><span data-stu-id="d8513-126">The reason for the revoke licenses action failure.</span></span> <span data-ttu-id="d8513-127">Los valores posibles son: `none`, `appleFailure`, `internalError`, `expiredVppToken` y `expiredApplePushNotificationCertificate`.</span><span class="sxs-lookup"><span data-stu-id="d8513-127">Possible values are: `none`, `appleFailure`, `internalError`, `expiredVppToken`, `expiredApplePushNotificationCertificate`.</span></span>|
|<span data-ttu-id="d8513-128">actionName</span><span class="sxs-lookup"><span data-stu-id="d8513-128">actionName</span></span>|<span data-ttu-id="d8513-129">cadena</span><span class="sxs-lookup"><span data-stu-id="d8513-129">String</span></span>|<span data-ttu-id="d8513-130">Nombre de acción</span><span class="sxs-lookup"><span data-stu-id="d8513-130">Action name</span></span>|
|<span data-ttu-id="d8513-131">actionState</span><span class="sxs-lookup"><span data-stu-id="d8513-131">actionState</span></span>|[<span data-ttu-id="d8513-132">actionState</span><span class="sxs-lookup"><span data-stu-id="d8513-132">actionState</span></span>](../resources/intune-shared-actionstate.md)|<span data-ttu-id="d8513-133">Estado de la acción.</span><span class="sxs-lookup"><span data-stu-id="d8513-133">State of the action.</span></span> <span data-ttu-id="d8513-134">Los valores posibles son: `none`, `pending`, `canceled`, `active`, `done`, `failed` y `notSupported`.</span><span class="sxs-lookup"><span data-stu-id="d8513-134">Possible values are: `none`, `pending`, `canceled`, `active`, `done`, `failed`, `notSupported`.</span></span>|
|<span data-ttu-id="d8513-135">startDateTime</span><span class="sxs-lookup"><span data-stu-id="d8513-135">startDateTime</span></span>|<span data-ttu-id="d8513-136">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="d8513-136">DateTimeOffset</span></span>|<span data-ttu-id="d8513-137">Hora a la que se inició la acción</span><span class="sxs-lookup"><span data-stu-id="d8513-137">Time the action was initiated</span></span>|
|<span data-ttu-id="d8513-138">lastUpdatedDateTime</span><span class="sxs-lookup"><span data-stu-id="d8513-138">lastUpdatedDateTime</span></span>|<span data-ttu-id="d8513-139">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="d8513-139">DateTimeOffset</span></span>|<span data-ttu-id="d8513-140">Hora en la que se actualizó por última vez el estado de la acción</span><span class="sxs-lookup"><span data-stu-id="d8513-140">Time the action state was last updated</span></span>|

## <a name="relationships"></a><span data-ttu-id="d8513-141">Relaciones</span><span class="sxs-lookup"><span data-stu-id="d8513-141">Relationships</span></span>
<span data-ttu-id="d8513-142">Ninguna</span><span class="sxs-lookup"><span data-stu-id="d8513-142">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="d8513-143">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="d8513-143">JSON Representation</span></span>
<span data-ttu-id="d8513-144">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="d8513-144">Here is a JSON representation of the resource.</span></span>
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





