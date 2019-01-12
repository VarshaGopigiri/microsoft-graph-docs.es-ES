---
title: Tipo de recurso managedDeviceMobileAppConfiguration
description: Una clase abstracta para la configuración de aplicaciones móviles para dispositivos inscritos.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: e4ce68f96e8fbf27c60a1365f481456a96eaeda3
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27947522"
---
# <a name="manageddevicemobileappconfiguration-resource-type"></a><span data-ttu-id="e7d4b-103">Tipo de recurso managedDeviceMobileAppConfiguration</span><span class="sxs-lookup"><span data-stu-id="e7d4b-103">managedDeviceMobileAppConfiguration resource type</span></span>

> <span data-ttu-id="e7d4b-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="e7d4b-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="e7d4b-105">Una clase abstracta para la configuración de aplicaciones móviles para dispositivos inscritos.</span><span class="sxs-lookup"><span data-stu-id="e7d4b-105">An abstract class for Mobile app configuration for enrolled devices.</span></span>
## <a name="methods"></a><span data-ttu-id="e7d4b-106">Métodos</span><span class="sxs-lookup"><span data-stu-id="e7d4b-106">Methods</span></span>
|<span data-ttu-id="e7d4b-107">Método</span><span class="sxs-lookup"><span data-stu-id="e7d4b-107">Method</span></span>|<span data-ttu-id="e7d4b-108">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e7d4b-108">Return Type</span></span>|<span data-ttu-id="e7d4b-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="e7d4b-109">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="e7d4b-110">Enumerar managedDeviceMobileAppConfigurations</span><span class="sxs-lookup"><span data-stu-id="e7d4b-110">List managedDeviceMobileAppConfigurations</span></span>](../api/intune-apps-manageddevicemobileappconfiguration-list.md)|<span data-ttu-id="e7d4b-111">Colección [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="e7d4b-111">[managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md) collection</span></span>|<span data-ttu-id="e7d4b-112">Enumere las propiedades y las relaciones de los objetos [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="e7d4b-112">List properties and relationships of the [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md) objects.</span></span>|
|[<span data-ttu-id="e7d4b-113">Obtener managedDeviceMobileAppConfiguration</span><span class="sxs-lookup"><span data-stu-id="e7d4b-113">Get managedDeviceMobileAppConfiguration</span></span>](../api/intune-apps-manageddevicemobileappconfiguration-get.md)|[<span data-ttu-id="e7d4b-114">managedDeviceMobileAppConfiguration</span><span class="sxs-lookup"><span data-stu-id="e7d4b-114">managedDeviceMobileAppConfiguration</span></span>](../resources/intune-apps-manageddevicemobileappconfiguration.md)|<span data-ttu-id="e7d4b-115">Lea las propiedades y las relaciones del objeto [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="e7d4b-115">Read properties and relationships of the [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md) object.</span></span>|
|[<span data-ttu-id="e7d4b-116">Acción assign</span><span class="sxs-lookup"><span data-stu-id="e7d4b-116">assign action</span></span>](../api/intune-apps-manageddevicemobileappconfiguration-assign.md)|<span data-ttu-id="e7d4b-117">Ninguno</span><span class="sxs-lookup"><span data-stu-id="e7d4b-117">None</span></span>|<span data-ttu-id="e7d4b-118">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="e7d4b-118">Not yet documented</span></span>|

## <a name="properties"></a><span data-ttu-id="e7d4b-119">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e7d4b-119">Properties</span></span>
|<span data-ttu-id="e7d4b-120">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e7d4b-120">Property</span></span>|<span data-ttu-id="e7d4b-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="e7d4b-121">Type</span></span>|<span data-ttu-id="e7d4b-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="e7d4b-122">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="e7d4b-123">id</span><span class="sxs-lookup"><span data-stu-id="e7d4b-123">id</span></span>|<span data-ttu-id="e7d4b-124">Cadena</span><span class="sxs-lookup"><span data-stu-id="e7d4b-124">String</span></span>|<span data-ttu-id="e7d4b-125">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="e7d4b-125">Key of the entity.</span></span>|
|<span data-ttu-id="e7d4b-126">targetedMobileApps</span><span class="sxs-lookup"><span data-stu-id="e7d4b-126">targetedMobileApps</span></span>|<span data-ttu-id="e7d4b-127">Colección string</span><span class="sxs-lookup"><span data-stu-id="e7d4b-127">String collection</span></span>|<span data-ttu-id="e7d4b-128">La aplicación asociada.</span><span class="sxs-lookup"><span data-stu-id="e7d4b-128">the associated app.</span></span>|
|<span data-ttu-id="e7d4b-129">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="e7d4b-129">createdDateTime</span></span>|<span data-ttu-id="e7d4b-130">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="e7d4b-130">DateTimeOffset</span></span>|<span data-ttu-id="e7d4b-131">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="e7d4b-131">DateTime the object was created.</span></span>|
|<span data-ttu-id="e7d4b-132">descripción</span><span class="sxs-lookup"><span data-stu-id="e7d4b-132">description</span></span>|<span data-ttu-id="e7d4b-133">Cadena</span><span class="sxs-lookup"><span data-stu-id="e7d4b-133">String</span></span>|<span data-ttu-id="e7d4b-134">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e7d4b-134">Admin provided description of the Device Configuration.</span></span>|
|<span data-ttu-id="e7d4b-135">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="e7d4b-135">lastModifiedDateTime</span></span>|<span data-ttu-id="e7d4b-136">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="e7d4b-136">DateTimeOffset</span></span>|<span data-ttu-id="e7d4b-137">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="e7d4b-137">DateTime the object was last modified.</span></span>|
|<span data-ttu-id="e7d4b-138">displayName</span><span class="sxs-lookup"><span data-stu-id="e7d4b-138">displayName</span></span>|<span data-ttu-id="e7d4b-139">Cadena</span><span class="sxs-lookup"><span data-stu-id="e7d4b-139">String</span></span>|<span data-ttu-id="e7d4b-140">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e7d4b-140">Admin provided name of the device configuration.</span></span>|
|<span data-ttu-id="e7d4b-141">versión</span><span class="sxs-lookup"><span data-stu-id="e7d4b-141">version</span></span>|<span data-ttu-id="e7d4b-142">Int32</span><span class="sxs-lookup"><span data-stu-id="e7d4b-142">Int32</span></span>|<span data-ttu-id="e7d4b-143">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e7d4b-143">Version of the device configuration.</span></span>|

## <a name="relationships"></a><span data-ttu-id="e7d4b-144">Relaciones</span><span class="sxs-lookup"><span data-stu-id="e7d4b-144">Relationships</span></span>
|<span data-ttu-id="e7d4b-145">Relación</span><span class="sxs-lookup"><span data-stu-id="e7d4b-145">Relationship</span></span>|<span data-ttu-id="e7d4b-146">Tipo</span><span class="sxs-lookup"><span data-stu-id="e7d4b-146">Type</span></span>|<span data-ttu-id="e7d4b-147">Descripción</span><span class="sxs-lookup"><span data-stu-id="e7d4b-147">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="e7d4b-148">asignaciones</span><span class="sxs-lookup"><span data-stu-id="e7d4b-148">assignments</span></span>|<span data-ttu-id="e7d4b-149">Colección [managedDeviceMobileAppConfigurationAssignment](../resources/intune-apps-manageddevicemobileappconfigurationassignment.md)</span><span class="sxs-lookup"><span data-stu-id="e7d4b-149">[managedDeviceMobileAppConfigurationAssignment](../resources/intune-apps-manageddevicemobileappconfigurationassignment.md) collection</span></span>|<span data-ttu-id="e7d4b-150">La lista de asignaciones de grupo para la configuración de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e7d4b-150">The list of group assignemenets for app configration.</span></span>|
|<span data-ttu-id="e7d4b-151">deviceStatuses</span><span class="sxs-lookup"><span data-stu-id="e7d4b-151">deviceStatuses</span></span>|<span data-ttu-id="e7d4b-152">colección de [managedDeviceMobileAppConfigurationDeviceStatus](../resources/intune-apps-manageddevicemobileappconfigurationdevicestatus.md)</span><span class="sxs-lookup"><span data-stu-id="e7d4b-152">[managedDeviceMobileAppConfigurationDeviceStatus](../resources/intune-apps-manageddevicemobileappconfigurationdevicestatus.md) collection</span></span>|<span data-ttu-id="e7d4b-153">Lista de ManagedDeviceMobileAppConfigurationDeviceStatus.</span><span class="sxs-lookup"><span data-stu-id="e7d4b-153">List of ManagedDeviceMobileAppConfigurationDeviceStatus.</span></span>|
|<span data-ttu-id="e7d4b-154">userStatuses</span><span class="sxs-lookup"><span data-stu-id="e7d4b-154">userStatuses</span></span>|<span data-ttu-id="e7d4b-155">Colección [managedDeviceMobileAppConfigurationUserStatus](../resources/intune-apps-manageddevicemobileappconfigurationuserstatus.md)</span><span class="sxs-lookup"><span data-stu-id="e7d4b-155">[managedDeviceMobileAppConfigurationUserStatus](../resources/intune-apps-manageddevicemobileappconfigurationuserstatus.md) collection</span></span>|<span data-ttu-id="e7d4b-156">Lista de ManagedDeviceMobileAppConfigurationUserStatus.</span><span class="sxs-lookup"><span data-stu-id="e7d4b-156">List of ManagedDeviceMobileAppConfigurationUserStatus.</span></span>|
|<span data-ttu-id="e7d4b-157">deviceStatusSummary</span><span class="sxs-lookup"><span data-stu-id="e7d4b-157">deviceStatusSummary</span></span>|[<span data-ttu-id="e7d4b-158">managedDeviceMobileAppConfigurationDeviceSummary</span><span class="sxs-lookup"><span data-stu-id="e7d4b-158">managedDeviceMobileAppConfigurationDeviceSummary</span></span>](../resources/intune-apps-manageddevicemobileappconfigurationdevicesummary.md)|<span data-ttu-id="e7d4b-159">Resumen del estado del dispositivo de la configuración de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="e7d4b-159">App configuration device status summary.</span></span>|
|<span data-ttu-id="e7d4b-160">userStatusSummary</span><span class="sxs-lookup"><span data-stu-id="e7d4b-160">userStatusSummary</span></span>|[<span data-ttu-id="e7d4b-161">managedDeviceMobileAppConfigurationUserSummary</span><span class="sxs-lookup"><span data-stu-id="e7d4b-161">managedDeviceMobileAppConfigurationUserSummary</span></span>](../resources/intune-apps-manageddevicemobileappconfigurationusersummary.md)|<span data-ttu-id="e7d4b-162">Resumen del estado del usuario de la configuración de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="e7d4b-162">App configuration user status summary.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="e7d4b-163">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="e7d4b-163">JSON Representation</span></span>
<span data-ttu-id="e7d4b-164">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="e7d4b-164">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.managedDeviceMobileAppConfiguration"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.managedDeviceMobileAppConfiguration",
  "id": "String (identifier)",
  "targetedMobileApps": [
    "String"
  ],
  "createdDateTime": "String (timestamp)",
  "description": "String",
  "lastModifiedDateTime": "String (timestamp)",
  "displayName": "String",
  "version": 1024
}
```



