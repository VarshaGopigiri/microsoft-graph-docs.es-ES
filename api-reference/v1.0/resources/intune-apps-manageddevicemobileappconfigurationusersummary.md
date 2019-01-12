---
title: Tipo de recurso managedDeviceMobileAppConfigurationUserSummary
description: Contiene las propiedades, las propiedades heredadas y las acciones para un resumen de estado de usuario de la configuración de aplicaciones móviles de MDM.
localization_priority: Normal
author: tfitzmac
ms.prod: intune
ms.openlocfilehash: 385e9ac51b10d97e425cf19acb10007402eeeeb4
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27934894"
---
# <a name="manageddevicemobileappconfigurationusersummary-resource-type"></a><span data-ttu-id="79138-103">Tipo de recurso managedDeviceMobileAppConfigurationUserSummary</span><span class="sxs-lookup"><span data-stu-id="79138-103">managedDeviceMobileAppConfigurationUserSummary resource type</span></span>

> <span data-ttu-id="79138-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="79138-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="79138-105">Contiene las propiedades, las propiedades heredadas y las acciones para un resumen de estado de usuario de la configuración de aplicaciones móviles de MDM.</span><span class="sxs-lookup"><span data-stu-id="79138-105">Contains properties, inherited properties and actions for an MDM mobile app configuration user status summary.</span></span>
## <a name="methods"></a><span data-ttu-id="79138-106">Métodos</span><span class="sxs-lookup"><span data-stu-id="79138-106">Methods</span></span>
|<span data-ttu-id="79138-107">Método</span><span class="sxs-lookup"><span data-stu-id="79138-107">Method</span></span>|<span data-ttu-id="79138-108">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="79138-108">Return Type</span></span>|<span data-ttu-id="79138-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="79138-109">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="79138-110">Obtener managedDeviceMobileAppConfigurationUserSummary</span><span class="sxs-lookup"><span data-stu-id="79138-110">Get managedDeviceMobileAppConfigurationUserSummary</span></span>](../api/intune-apps-manageddevicemobileappconfigurationusersummary-get.md)|[<span data-ttu-id="79138-111">managedDeviceMobileAppConfigurationUserSummary</span><span class="sxs-lookup"><span data-stu-id="79138-111">managedDeviceMobileAppConfigurationUserSummary</span></span>](../resources/intune-apps-manageddevicemobileappconfigurationusersummary.md)|<span data-ttu-id="79138-112">Lea las propiedades y las relaciones del objeto [managedDeviceMobileAppConfigurationUserSummary](../resources/intune-apps-manageddevicemobileappconfigurationusersummary.md).</span><span class="sxs-lookup"><span data-stu-id="79138-112">Read properties and relationships of the [managedDeviceMobileAppConfigurationUserSummary](../resources/intune-apps-manageddevicemobileappconfigurationusersummary.md) object.</span></span>|
|[<span data-ttu-id="79138-113">Actualizar managedDeviceMobileAppConfigurationUserSummary</span><span class="sxs-lookup"><span data-stu-id="79138-113">Update managedDeviceMobileAppConfigurationUserSummary</span></span>](../api/intune-apps-manageddevicemobileappconfigurationusersummary-update.md)|[<span data-ttu-id="79138-114">managedDeviceMobileAppConfigurationUserSummary</span><span class="sxs-lookup"><span data-stu-id="79138-114">managedDeviceMobileAppConfigurationUserSummary</span></span>](../resources/intune-apps-manageddevicemobileappconfigurationusersummary.md)|<span data-ttu-id="79138-115">Actualice las propiedades de un objeto [managedDeviceMobileAppConfigurationUserSummary](../resources/intune-apps-manageddevicemobileappconfigurationusersummary.md).</span><span class="sxs-lookup"><span data-stu-id="79138-115">Update the properties of a [managedDeviceMobileAppConfigurationUserSummary](../resources/intune-apps-manageddevicemobileappconfigurationusersummary.md) object.</span></span>|

## <a name="properties"></a><span data-ttu-id="79138-116">Propiedades</span><span class="sxs-lookup"><span data-stu-id="79138-116">Properties</span></span>
|<span data-ttu-id="79138-117">Propiedad</span><span class="sxs-lookup"><span data-stu-id="79138-117">Property</span></span>|<span data-ttu-id="79138-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="79138-118">Type</span></span>|<span data-ttu-id="79138-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="79138-119">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="79138-120">id</span><span class="sxs-lookup"><span data-stu-id="79138-120">id</span></span>|<span data-ttu-id="79138-121">String</span><span class="sxs-lookup"><span data-stu-id="79138-121">String</span></span>|<span data-ttu-id="79138-122">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="79138-122">Key of the entity.</span></span>|
|<span data-ttu-id="79138-123">pendingCount</span><span class="sxs-lookup"><span data-stu-id="79138-123">pendingCount</span></span>|<span data-ttu-id="79138-124">Int32</span><span class="sxs-lookup"><span data-stu-id="79138-124">Int32</span></span>|<span data-ttu-id="79138-125">Número de usuarios pendientes</span><span class="sxs-lookup"><span data-stu-id="79138-125">Number of pending Users</span></span>|
|<span data-ttu-id="79138-126">notApplicableCount</span><span class="sxs-lookup"><span data-stu-id="79138-126">notApplicableCount</span></span>|<span data-ttu-id="79138-127">Int32</span><span class="sxs-lookup"><span data-stu-id="79138-127">Int32</span></span>|<span data-ttu-id="79138-128">Número de usuarios no es aplicable.</span><span class="sxs-lookup"><span data-stu-id="79138-128">Number of not applicable users</span></span>|
|<span data-ttu-id="79138-129">successCount</span><span class="sxs-lookup"><span data-stu-id="79138-129">successCount</span></span>|<span data-ttu-id="79138-130">Int32</span><span class="sxs-lookup"><span data-stu-id="79138-130">Int32</span></span>|<span data-ttu-id="79138-131">Número de usuarios correctos</span><span class="sxs-lookup"><span data-stu-id="79138-131">Number of succeeded Users</span></span>|
|<span data-ttu-id="79138-132">errorCount</span><span class="sxs-lookup"><span data-stu-id="79138-132">errorCount</span></span>|<span data-ttu-id="79138-133">Int32</span><span class="sxs-lookup"><span data-stu-id="79138-133">Int32</span></span>|<span data-ttu-id="79138-134">Número de usuarios con error</span><span class="sxs-lookup"><span data-stu-id="79138-134">Number of error Users</span></span>|
|<span data-ttu-id="79138-135">failedCount</span><span class="sxs-lookup"><span data-stu-id="79138-135">failedCount</span></span>|<span data-ttu-id="79138-136">Int32</span><span class="sxs-lookup"><span data-stu-id="79138-136">Int32</span></span>|<span data-ttu-id="79138-137">Número de usuarios erróneos</span><span class="sxs-lookup"><span data-stu-id="79138-137">Number of failed Users</span></span>|
|<span data-ttu-id="79138-138">lastUpdateDateTime</span><span class="sxs-lookup"><span data-stu-id="79138-138">lastUpdateDateTime</span></span>|<span data-ttu-id="79138-139">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="79138-139">DateTimeOffset</span></span>|<span data-ttu-id="79138-140">Última hora de actualización</span><span class="sxs-lookup"><span data-stu-id="79138-140">Last update time</span></span>|
|<span data-ttu-id="79138-141">configurationVersion</span><span class="sxs-lookup"><span data-stu-id="79138-141">configurationVersion</span></span>|<span data-ttu-id="79138-142">Int32</span><span class="sxs-lookup"><span data-stu-id="79138-142">Int32</span></span>|<span data-ttu-id="79138-143">Versión de la directiva para esa información general</span><span class="sxs-lookup"><span data-stu-id="79138-143">Version of the policy for that overview</span></span>|

## <a name="relationships"></a><span data-ttu-id="79138-144">Relaciones</span><span class="sxs-lookup"><span data-stu-id="79138-144">Relationships</span></span>
<span data-ttu-id="79138-145">Ninguna</span><span class="sxs-lookup"><span data-stu-id="79138-145">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="79138-146">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="79138-146">JSON Representation</span></span>
<span data-ttu-id="79138-147">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="79138-147">Here is a JSON representation of the resource.</span></span>
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



