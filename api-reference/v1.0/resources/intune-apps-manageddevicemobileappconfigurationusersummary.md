---
title: Tipo de recurso managedDeviceMobileAppConfigurationUserSummary
description: Contiene las propiedades, las propiedades heredadas y las acciones para un resumen de estado de usuario de la configuración de aplicaciones móviles de MDM.
ms.openlocfilehash: 7d49218220854b2d8bba38b74d2103adace810ab
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029464"
---
# <a name="manageddevicemobileappconfigurationusersummary-resource-type"></a><span data-ttu-id="65d25-103">Tipo de recurso managedDeviceMobileAppConfigurationUserSummary</span><span class="sxs-lookup"><span data-stu-id="65d25-103">managedDeviceMobileAppConfigurationUserSummary resource type</span></span>

> <span data-ttu-id="65d25-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="65d25-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="65d25-105">Contiene las propiedades, las propiedades heredadas y las acciones para un resumen de estado de usuario de la configuración de aplicaciones móviles de MDM.</span><span class="sxs-lookup"><span data-stu-id="65d25-105">Contains properties, inherited properties and actions for an MDM mobile app configuration user status summary.</span></span>
## <a name="methods"></a><span data-ttu-id="65d25-106">Métodos</span><span class="sxs-lookup"><span data-stu-id="65d25-106">Methods</span></span>
|<span data-ttu-id="65d25-107">Método</span><span class="sxs-lookup"><span data-stu-id="65d25-107">Method</span></span>|<span data-ttu-id="65d25-108">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="65d25-108">Return Type</span></span>|<span data-ttu-id="65d25-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="65d25-109">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="65d25-110">Obtener managedDeviceMobileAppConfigurationUserSummary</span><span class="sxs-lookup"><span data-stu-id="65d25-110">Get managedDeviceMobileAppConfigurationUserSummary</span></span>](../api/intune-apps-manageddevicemobileappconfigurationusersummary-get.md)|[<span data-ttu-id="65d25-111">managedDeviceMobileAppConfigurationUserSummary</span><span class="sxs-lookup"><span data-stu-id="65d25-111">managedDeviceMobileAppConfigurationUserSummary</span></span>](../resources/intune-apps-manageddevicemobileappconfigurationusersummary.md)|<span data-ttu-id="65d25-112">Lea las propiedades y las relaciones del objeto [managedDeviceMobileAppConfigurationUserSummary](../resources/intune-apps-manageddevicemobileappconfigurationusersummary.md).</span><span class="sxs-lookup"><span data-stu-id="65d25-112">Read properties and relationships of the [managedDeviceMobileAppConfigurationUserSummary](../resources/intune-apps-manageddevicemobileappconfigurationusersummary.md) object.</span></span>|
|[<span data-ttu-id="65d25-113">Actualizar managedDeviceMobileAppConfigurationUserSummary</span><span class="sxs-lookup"><span data-stu-id="65d25-113">Update managedDeviceMobileAppConfigurationUserSummary</span></span>](../api/intune-apps-manageddevicemobileappconfigurationusersummary-update.md)|[<span data-ttu-id="65d25-114">managedDeviceMobileAppConfigurationUserSummary</span><span class="sxs-lookup"><span data-stu-id="65d25-114">managedDeviceMobileAppConfigurationUserSummary</span></span>](../resources/intune-apps-manageddevicemobileappconfigurationusersummary.md)|<span data-ttu-id="65d25-115">Actualice las propiedades de un objeto [managedDeviceMobileAppConfigurationUserSummary](../resources/intune-apps-manageddevicemobileappconfigurationusersummary.md).</span><span class="sxs-lookup"><span data-stu-id="65d25-115">Update the properties of a [managedDeviceMobileAppConfigurationUserSummary](../resources/intune-apps-manageddevicemobileappconfigurationusersummary.md) object.</span></span>|

## <a name="properties"></a><span data-ttu-id="65d25-116">Propiedades</span><span class="sxs-lookup"><span data-stu-id="65d25-116">Properties</span></span>
|<span data-ttu-id="65d25-117">Propiedad</span><span class="sxs-lookup"><span data-stu-id="65d25-117">Property</span></span>|<span data-ttu-id="65d25-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="65d25-118">Type</span></span>|<span data-ttu-id="65d25-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="65d25-119">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="65d25-120">id</span><span class="sxs-lookup"><span data-stu-id="65d25-120">id</span></span>|<span data-ttu-id="65d25-121">String</span><span class="sxs-lookup"><span data-stu-id="65d25-121">String</span></span>|<span data-ttu-id="65d25-122">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="65d25-122">Key of the entity.</span></span>|
|<span data-ttu-id="65d25-123">pendingCount</span><span class="sxs-lookup"><span data-stu-id="65d25-123">pendingCount</span></span>|<span data-ttu-id="65d25-124">Int32</span><span class="sxs-lookup"><span data-stu-id="65d25-124">Int32</span></span>|<span data-ttu-id="65d25-125">Número de usuarios pendientes</span><span class="sxs-lookup"><span data-stu-id="65d25-125">Number of pending Users</span></span>|
|<span data-ttu-id="65d25-126">notApplicableCount</span><span class="sxs-lookup"><span data-stu-id="65d25-126">notApplicableCount</span></span>|<span data-ttu-id="65d25-127">Int32</span><span class="sxs-lookup"><span data-stu-id="65d25-127">Int32</span></span>|<span data-ttu-id="65d25-128">Número de usuarios no es aplicable.</span><span class="sxs-lookup"><span data-stu-id="65d25-128">Number of not applicable users</span></span>|
|<span data-ttu-id="65d25-129">successCount</span><span class="sxs-lookup"><span data-stu-id="65d25-129">successCount</span></span>|<span data-ttu-id="65d25-130">Int32</span><span class="sxs-lookup"><span data-stu-id="65d25-130">Int32</span></span>|<span data-ttu-id="65d25-131">Número de usuarios correctos</span><span class="sxs-lookup"><span data-stu-id="65d25-131">Number of succeeded Users</span></span>|
|<span data-ttu-id="65d25-132">errorCount</span><span class="sxs-lookup"><span data-stu-id="65d25-132">errorCount</span></span>|<span data-ttu-id="65d25-133">Int32</span><span class="sxs-lookup"><span data-stu-id="65d25-133">Int32</span></span>|<span data-ttu-id="65d25-134">Número de usuarios con error</span><span class="sxs-lookup"><span data-stu-id="65d25-134">Number of error Users</span></span>|
|<span data-ttu-id="65d25-135">failedCount</span><span class="sxs-lookup"><span data-stu-id="65d25-135">failedCount</span></span>|<span data-ttu-id="65d25-136">Int32</span><span class="sxs-lookup"><span data-stu-id="65d25-136">Int32</span></span>|<span data-ttu-id="65d25-137">Número de usuarios erróneos</span><span class="sxs-lookup"><span data-stu-id="65d25-137">Number of failed Users</span></span>|
|<span data-ttu-id="65d25-138">lastUpdateDateTime</span><span class="sxs-lookup"><span data-stu-id="65d25-138">lastUpdateDateTime</span></span>|<span data-ttu-id="65d25-139">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="65d25-139">DateTimeOffset</span></span>|<span data-ttu-id="65d25-140">Última hora de actualización</span><span class="sxs-lookup"><span data-stu-id="65d25-140">Last update time</span></span>|
|<span data-ttu-id="65d25-141">configurationVersion</span><span class="sxs-lookup"><span data-stu-id="65d25-141">configurationVersion</span></span>|<span data-ttu-id="65d25-142">Int32</span><span class="sxs-lookup"><span data-stu-id="65d25-142">Int32</span></span>|<span data-ttu-id="65d25-143">Versión de la directiva para esa información general</span><span class="sxs-lookup"><span data-stu-id="65d25-143">Version of the policy for that overview</span></span>|

## <a name="relationships"></a><span data-ttu-id="65d25-144">Relaciones</span><span class="sxs-lookup"><span data-stu-id="65d25-144">Relationships</span></span>
<span data-ttu-id="65d25-145">Ninguna</span><span class="sxs-lookup"><span data-stu-id="65d25-145">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="65d25-146">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="65d25-146">JSON Representation</span></span>
<span data-ttu-id="65d25-147">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="65d25-147">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.managedDeviceMobileAppConfigurationUserSummary"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.managedDeviceMobileAppConfigurationUserSummary",
  "id": "String (identifier)",
  "pendingCount": 1024,
  "notApplicableCount": 1024,
  "successCount": 1024,
  "errorCount": 1024,
  "failedCount": 1024,
  "lastUpdateDateTime": "String (timestamp)",
  "configurationVersion": 1024
}
```



