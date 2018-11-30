---
title: Tipo de recurso managedDeviceMobileAppConfiguration
description: Una clase abstracta para la configuración de aplicaciones móviles para dispositivos inscritos.
ms.openlocfilehash: dd3b77b3e53c1eacc049af35274e20c5bbaa8e14
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27028657"
---
# <a name="manageddevicemobileappconfiguration-resource-type"></a><span data-ttu-id="efee3-103">Tipo de recurso managedDeviceMobileAppConfiguration</span><span class="sxs-lookup"><span data-stu-id="efee3-103">managedDeviceMobileAppConfiguration resource type</span></span>

> <span data-ttu-id="efee3-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="efee3-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="efee3-105">Una clase abstracta para la configuración de aplicaciones móviles para dispositivos inscritos.</span><span class="sxs-lookup"><span data-stu-id="efee3-105">An abstract class for Mobile app configuration for enrolled devices.</span></span>
## <a name="methods"></a><span data-ttu-id="efee3-106">Métodos</span><span class="sxs-lookup"><span data-stu-id="efee3-106">Methods</span></span>
|<span data-ttu-id="efee3-107">Método</span><span class="sxs-lookup"><span data-stu-id="efee3-107">Method</span></span>|<span data-ttu-id="efee3-108">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="efee3-108">Return Type</span></span>|<span data-ttu-id="efee3-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="efee3-109">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="efee3-110">Enumerar managedDeviceMobileAppConfigurations</span><span class="sxs-lookup"><span data-stu-id="efee3-110">List managedDeviceMobileAppConfigurations</span></span>](../api/intune-apps-manageddevicemobileappconfiguration-list.md)|<span data-ttu-id="efee3-111">Colección [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="efee3-111">[managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md) collection</span></span>|<span data-ttu-id="efee3-112">Enumere las propiedades y las relaciones de los objetos [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="efee3-112">List properties and relationships of the [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md) objects.</span></span>|
|[<span data-ttu-id="efee3-113">Obtener managedDeviceMobileAppConfiguration</span><span class="sxs-lookup"><span data-stu-id="efee3-113">Get managedDeviceMobileAppConfiguration</span></span>](../api/intune-apps-manageddevicemobileappconfiguration-get.md)|[<span data-ttu-id="efee3-114">managedDeviceMobileAppConfiguration</span><span class="sxs-lookup"><span data-stu-id="efee3-114">managedDeviceMobileAppConfiguration</span></span>](../resources/intune-apps-manageddevicemobileappconfiguration.md)|<span data-ttu-id="efee3-115">Lea las propiedades y las relaciones del objeto [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="efee3-115">Read properties and relationships of the [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md) object.</span></span>|
|[<span data-ttu-id="efee3-116">Acción assign</span><span class="sxs-lookup"><span data-stu-id="efee3-116">assign action</span></span>](../api/intune-apps-manageddevicemobileappconfiguration-assign.md)|<span data-ttu-id="efee3-117">Ninguno</span><span class="sxs-lookup"><span data-stu-id="efee3-117">None</span></span>|<span data-ttu-id="efee3-118">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="efee3-118">Not yet documented</span></span>|

## <a name="properties"></a><span data-ttu-id="efee3-119">Propiedades</span><span class="sxs-lookup"><span data-stu-id="efee3-119">Properties</span></span>
|<span data-ttu-id="efee3-120">Propiedad</span><span class="sxs-lookup"><span data-stu-id="efee3-120">Property</span></span>|<span data-ttu-id="efee3-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="efee3-121">Type</span></span>|<span data-ttu-id="efee3-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="efee3-122">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="efee3-123">id</span><span class="sxs-lookup"><span data-stu-id="efee3-123">id</span></span>|<span data-ttu-id="efee3-124">String</span><span class="sxs-lookup"><span data-stu-id="efee3-124">String</span></span>|<span data-ttu-id="efee3-125">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="efee3-125">Key of the entity.</span></span>|
|<span data-ttu-id="efee3-126">targetedMobileApps</span><span class="sxs-lookup"><span data-stu-id="efee3-126">targetedMobileApps</span></span>|<span data-ttu-id="efee3-127">Colección string</span><span class="sxs-lookup"><span data-stu-id="efee3-127">String collection</span></span>|<span data-ttu-id="efee3-128">La aplicación asociada.</span><span class="sxs-lookup"><span data-stu-id="efee3-128">the associated app.</span></span>|
|<span data-ttu-id="efee3-129">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="efee3-129">createdDateTime</span></span>|<span data-ttu-id="efee3-130">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="efee3-130">DateTimeOffset</span></span>|<span data-ttu-id="efee3-131">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="efee3-131">DateTime the object was created.</span></span>|
|<span data-ttu-id="efee3-132">descripción</span><span class="sxs-lookup"><span data-stu-id="efee3-132">description</span></span>|<span data-ttu-id="efee3-133">String</span><span class="sxs-lookup"><span data-stu-id="efee3-133">String</span></span>|<span data-ttu-id="efee3-134">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="efee3-134">Admin provided description of the Device Configuration.</span></span>|
|<span data-ttu-id="efee3-135">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="efee3-135">lastModifiedDateTime</span></span>|<span data-ttu-id="efee3-136">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="efee3-136">DateTimeOffset</span></span>|<span data-ttu-id="efee3-137">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="efee3-137">DateTime the object was last modified.</span></span>|
|<span data-ttu-id="efee3-138">displayName</span><span class="sxs-lookup"><span data-stu-id="efee3-138">displayName</span></span>|<span data-ttu-id="efee3-139">String</span><span class="sxs-lookup"><span data-stu-id="efee3-139">String</span></span>|<span data-ttu-id="efee3-140">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="efee3-140">Admin provided name of the device configuration.</span></span>|
|<span data-ttu-id="efee3-141">versión</span><span class="sxs-lookup"><span data-stu-id="efee3-141">version</span></span>|<span data-ttu-id="efee3-142">Int32</span><span class="sxs-lookup"><span data-stu-id="efee3-142">Int32</span></span>|<span data-ttu-id="efee3-143">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="efee3-143">Version of the device configuration.</span></span>|

## <a name="relationships"></a><span data-ttu-id="efee3-144">Relaciones</span><span class="sxs-lookup"><span data-stu-id="efee3-144">Relationships</span></span>
|<span data-ttu-id="efee3-145">Relación</span><span class="sxs-lookup"><span data-stu-id="efee3-145">Relationship</span></span>|<span data-ttu-id="efee3-146">Tipo</span><span class="sxs-lookup"><span data-stu-id="efee3-146">Type</span></span>|<span data-ttu-id="efee3-147">Descripción</span><span class="sxs-lookup"><span data-stu-id="efee3-147">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="efee3-148">asignaciones</span><span class="sxs-lookup"><span data-stu-id="efee3-148">assignments</span></span>|<span data-ttu-id="efee3-149">Colección [managedDeviceMobileAppConfigurationAssignment](../resources/intune-apps-manageddevicemobileappconfigurationassignment.md)</span><span class="sxs-lookup"><span data-stu-id="efee3-149">[managedDeviceMobileAppConfigurationAssignment](../resources/intune-apps-manageddevicemobileappconfigurationassignment.md) collection</span></span>|<span data-ttu-id="efee3-150">La lista de asignaciones de grupo para la configuración de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="efee3-150">The list of group assignemenets for app configration.</span></span>|
|<span data-ttu-id="efee3-151">deviceStatuses</span><span class="sxs-lookup"><span data-stu-id="efee3-151">deviceStatuses</span></span>|<span data-ttu-id="efee3-152">colección de [managedDeviceMobileAppConfigurationDeviceStatus](../resources/intune-apps-manageddevicemobileappconfigurationdevicestatus.md)</span><span class="sxs-lookup"><span data-stu-id="efee3-152">[managedDeviceMobileAppConfigurationDeviceStatus](../resources/intune-apps-manageddevicemobileappconfigurationdevicestatus.md) collection</span></span>|<span data-ttu-id="efee3-153">Lista de ManagedDeviceMobileAppConfigurationDeviceStatus.</span><span class="sxs-lookup"><span data-stu-id="efee3-153">List of ManagedDeviceMobileAppConfigurationDeviceStatus.</span></span>|
|<span data-ttu-id="efee3-154">userStatuses</span><span class="sxs-lookup"><span data-stu-id="efee3-154">userStatuses</span></span>|<span data-ttu-id="efee3-155">Colección [managedDeviceMobileAppConfigurationUserStatus](../resources/intune-apps-manageddevicemobileappconfigurationuserstatus.md)</span><span class="sxs-lookup"><span data-stu-id="efee3-155">[managedDeviceMobileAppConfigurationUserStatus](../resources/intune-apps-manageddevicemobileappconfigurationuserstatus.md) collection</span></span>|<span data-ttu-id="efee3-156">Lista de ManagedDeviceMobileAppConfigurationUserStatus.</span><span class="sxs-lookup"><span data-stu-id="efee3-156">List of ManagedDeviceMobileAppConfigurationUserStatus.</span></span>|
|<span data-ttu-id="efee3-157">deviceStatusSummary</span><span class="sxs-lookup"><span data-stu-id="efee3-157">deviceStatusSummary</span></span>|[<span data-ttu-id="efee3-158">managedDeviceMobileAppConfigurationDeviceSummary</span><span class="sxs-lookup"><span data-stu-id="efee3-158">managedDeviceMobileAppConfigurationDeviceSummary</span></span>](../resources/intune-apps-manageddevicemobileappconfigurationdevicesummary.md)|<span data-ttu-id="efee3-159">Resumen del estado del dispositivo de la configuración de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="efee3-159">App configuration device status summary.</span></span>|
|<span data-ttu-id="efee3-160">userStatusSummary</span><span class="sxs-lookup"><span data-stu-id="efee3-160">userStatusSummary</span></span>|[<span data-ttu-id="efee3-161">managedDeviceMobileAppConfigurationUserSummary</span><span class="sxs-lookup"><span data-stu-id="efee3-161">managedDeviceMobileAppConfigurationUserSummary</span></span>](../resources/intune-apps-manageddevicemobileappconfigurationusersummary.md)|<span data-ttu-id="efee3-162">Resumen del estado del usuario de la configuración de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="efee3-162">App configuration user status summary.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="efee3-163">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="efee3-163">JSON Representation</span></span>
<span data-ttu-id="efee3-164">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="efee3-164">Here is a JSON representation of the resource.</span></span>
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



