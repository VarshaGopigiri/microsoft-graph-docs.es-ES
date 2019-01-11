---
title: Tipo de recurso managedDeviceMobileAppConfigurationUserSummary
description: Contiene las propiedades, las propiedades heredadas y las acciones para un resumen de estado de usuario de la configuración de aplicaciones móviles de MDM.
localization_priority: Normal
ms.openlocfilehash: e543c6d70906b678e90ba1598c46a039430745e4
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27836228"
---
# <a name="manageddevicemobileappconfigurationusersummary-resource-type"></a><span data-ttu-id="5085b-103">Tipo de recurso managedDeviceMobileAppConfigurationUserSummary</span><span class="sxs-lookup"><span data-stu-id="5085b-103">managedDeviceMobileAppConfigurationUserSummary resource type</span></span>

> <span data-ttu-id="5085b-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="5085b-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="5085b-105">Contiene las propiedades, las propiedades heredadas y las acciones para un resumen de estado de usuario de la configuración de aplicaciones móviles de MDM.</span><span class="sxs-lookup"><span data-stu-id="5085b-105">Contains properties, inherited properties and actions for an MDM mobile app configuration user status summary.</span></span>
## <a name="methods"></a><span data-ttu-id="5085b-106">Métodos</span><span class="sxs-lookup"><span data-stu-id="5085b-106">Methods</span></span>
|<span data-ttu-id="5085b-107">Método</span><span class="sxs-lookup"><span data-stu-id="5085b-107">Method</span></span>|<span data-ttu-id="5085b-108">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5085b-108">Return Type</span></span>|<span data-ttu-id="5085b-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="5085b-109">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="5085b-110">Obtener managedDeviceMobileAppConfigurationUserSummary</span><span class="sxs-lookup"><span data-stu-id="5085b-110">Get managedDeviceMobileAppConfigurationUserSummary</span></span>](../api/intune-apps-manageddevicemobileappconfigurationusersummary-get.md)|[<span data-ttu-id="5085b-111">managedDeviceMobileAppConfigurationUserSummary</span><span class="sxs-lookup"><span data-stu-id="5085b-111">managedDeviceMobileAppConfigurationUserSummary</span></span>](../resources/intune-apps-manageddevicemobileappconfigurationusersummary.md)|<span data-ttu-id="5085b-112">Lea las propiedades y las relaciones del objeto [managedDeviceMobileAppConfigurationUserSummary](../resources/intune-apps-manageddevicemobileappconfigurationusersummary.md).</span><span class="sxs-lookup"><span data-stu-id="5085b-112">Read properties and relationships of the [managedDeviceMobileAppConfigurationUserSummary](../resources/intune-apps-manageddevicemobileappconfigurationusersummary.md) object.</span></span>|
|[<span data-ttu-id="5085b-113">Actualizar managedDeviceMobileAppConfigurationUserSummary</span><span class="sxs-lookup"><span data-stu-id="5085b-113">Update managedDeviceMobileAppConfigurationUserSummary</span></span>](../api/intune-apps-manageddevicemobileappconfigurationusersummary-update.md)|[<span data-ttu-id="5085b-114">managedDeviceMobileAppConfigurationUserSummary</span><span class="sxs-lookup"><span data-stu-id="5085b-114">managedDeviceMobileAppConfigurationUserSummary</span></span>](../resources/intune-apps-manageddevicemobileappconfigurationusersummary.md)|<span data-ttu-id="5085b-115">Actualice las propiedades de un objeto [managedDeviceMobileAppConfigurationUserSummary](../resources/intune-apps-manageddevicemobileappconfigurationusersummary.md).</span><span class="sxs-lookup"><span data-stu-id="5085b-115">Update the properties of a [managedDeviceMobileAppConfigurationUserSummary](../resources/intune-apps-manageddevicemobileappconfigurationusersummary.md) object.</span></span>|

## <a name="properties"></a><span data-ttu-id="5085b-116">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5085b-116">Properties</span></span>
|<span data-ttu-id="5085b-117">Propiedad</span><span class="sxs-lookup"><span data-stu-id="5085b-117">Property</span></span>|<span data-ttu-id="5085b-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="5085b-118">Type</span></span>|<span data-ttu-id="5085b-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="5085b-119">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="5085b-120">id</span><span class="sxs-lookup"><span data-stu-id="5085b-120">id</span></span>|<span data-ttu-id="5085b-121">Cadena</span><span class="sxs-lookup"><span data-stu-id="5085b-121">String</span></span>|<span data-ttu-id="5085b-122">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="5085b-122">Key of the entity.</span></span>|
|<span data-ttu-id="5085b-123">pendingCount</span><span class="sxs-lookup"><span data-stu-id="5085b-123">pendingCount</span></span>|<span data-ttu-id="5085b-124">Int32</span><span class="sxs-lookup"><span data-stu-id="5085b-124">Int32</span></span>|<span data-ttu-id="5085b-125">Número de usuarios pendientes</span><span class="sxs-lookup"><span data-stu-id="5085b-125">Number of pending Users</span></span>|
|<span data-ttu-id="5085b-126">notApplicableCount</span><span class="sxs-lookup"><span data-stu-id="5085b-126">notApplicableCount</span></span>|<span data-ttu-id="5085b-127">Int32</span><span class="sxs-lookup"><span data-stu-id="5085b-127">Int32</span></span>|<span data-ttu-id="5085b-128">Número de usuarios no es aplicable.</span><span class="sxs-lookup"><span data-stu-id="5085b-128">Number of not applicable users</span></span>|
|<span data-ttu-id="5085b-129">successCount</span><span class="sxs-lookup"><span data-stu-id="5085b-129">successCount</span></span>|<span data-ttu-id="5085b-130">Int32</span><span class="sxs-lookup"><span data-stu-id="5085b-130">Int32</span></span>|<span data-ttu-id="5085b-131">Número de usuarios correctos</span><span class="sxs-lookup"><span data-stu-id="5085b-131">Number of succeeded Users</span></span>|
|<span data-ttu-id="5085b-132">errorCount</span><span class="sxs-lookup"><span data-stu-id="5085b-132">errorCount</span></span>|<span data-ttu-id="5085b-133">Int32</span><span class="sxs-lookup"><span data-stu-id="5085b-133">Int32</span></span>|<span data-ttu-id="5085b-134">Número de usuarios con error</span><span class="sxs-lookup"><span data-stu-id="5085b-134">Number of error Users</span></span>|
|<span data-ttu-id="5085b-135">failedCount</span><span class="sxs-lookup"><span data-stu-id="5085b-135">failedCount</span></span>|<span data-ttu-id="5085b-136">Int32</span><span class="sxs-lookup"><span data-stu-id="5085b-136">Int32</span></span>|<span data-ttu-id="5085b-137">Número de usuarios erróneos</span><span class="sxs-lookup"><span data-stu-id="5085b-137">Number of failed Users</span></span>|
|<span data-ttu-id="5085b-138">lastUpdateDateTime</span><span class="sxs-lookup"><span data-stu-id="5085b-138">lastUpdateDateTime</span></span>|<span data-ttu-id="5085b-139">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="5085b-139">DateTimeOffset</span></span>|<span data-ttu-id="5085b-140">Última hora de actualización</span><span class="sxs-lookup"><span data-stu-id="5085b-140">Last update time</span></span>|
|<span data-ttu-id="5085b-141">configurationVersion</span><span class="sxs-lookup"><span data-stu-id="5085b-141">configurationVersion</span></span>|<span data-ttu-id="5085b-142">Int32</span><span class="sxs-lookup"><span data-stu-id="5085b-142">Int32</span></span>|<span data-ttu-id="5085b-143">Versión de la directiva para esa información general</span><span class="sxs-lookup"><span data-stu-id="5085b-143">Version of the policy for that overview</span></span>|

## <a name="relationships"></a><span data-ttu-id="5085b-144">Relaciones</span><span class="sxs-lookup"><span data-stu-id="5085b-144">Relationships</span></span>
<span data-ttu-id="5085b-145">Ninguna</span><span class="sxs-lookup"><span data-stu-id="5085b-145">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="5085b-146">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="5085b-146">JSON Representation</span></span>
<span data-ttu-id="5085b-147">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="5085b-147">Here is a JSON representation of the resource.</span></span>
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



