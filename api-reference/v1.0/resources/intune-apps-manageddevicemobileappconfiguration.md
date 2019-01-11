---
title: Tipo de recurso managedDeviceMobileAppConfiguration
description: Una clase abstracta para la configuración de aplicaciones móviles para dispositivos inscritos.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 8e2ad71a4927f2b0156d085bad54cf59d45f97c8
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27811651"
---
# <a name="manageddevicemobileappconfiguration-resource-type"></a><span data-ttu-id="66a48-103">Tipo de recurso managedDeviceMobileAppConfiguration</span><span class="sxs-lookup"><span data-stu-id="66a48-103">managedDeviceMobileAppConfiguration resource type</span></span>

> <span data-ttu-id="66a48-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="66a48-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="66a48-105">Una clase abstracta para la configuración de aplicaciones móviles para dispositivos inscritos.</span><span class="sxs-lookup"><span data-stu-id="66a48-105">An abstract class for Mobile app configuration for enrolled devices.</span></span>
## <a name="methods"></a><span data-ttu-id="66a48-106">Métodos</span><span class="sxs-lookup"><span data-stu-id="66a48-106">Methods</span></span>
|<span data-ttu-id="66a48-107">Método</span><span class="sxs-lookup"><span data-stu-id="66a48-107">Method</span></span>|<span data-ttu-id="66a48-108">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="66a48-108">Return Type</span></span>|<span data-ttu-id="66a48-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="66a48-109">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="66a48-110">Enumerar managedDeviceMobileAppConfigurations</span><span class="sxs-lookup"><span data-stu-id="66a48-110">List managedDeviceMobileAppConfigurations</span></span>](../api/intune-apps-manageddevicemobileappconfiguration-list.md)|<span data-ttu-id="66a48-111">Colección [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="66a48-111">[managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md) collection</span></span>|<span data-ttu-id="66a48-112">Enumere las propiedades y las relaciones de los objetos [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="66a48-112">List properties and relationships of the [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md) objects.</span></span>|
|[<span data-ttu-id="66a48-113">Obtener managedDeviceMobileAppConfiguration</span><span class="sxs-lookup"><span data-stu-id="66a48-113">Get managedDeviceMobileAppConfiguration</span></span>](../api/intune-apps-manageddevicemobileappconfiguration-get.md)|[<span data-ttu-id="66a48-114">managedDeviceMobileAppConfiguration</span><span class="sxs-lookup"><span data-stu-id="66a48-114">managedDeviceMobileAppConfiguration</span></span>](../resources/intune-apps-manageddevicemobileappconfiguration.md)|<span data-ttu-id="66a48-115">Lea las propiedades y las relaciones del objeto [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="66a48-115">Read properties and relationships of the [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md) object.</span></span>|
|[<span data-ttu-id="66a48-116">Acción assign</span><span class="sxs-lookup"><span data-stu-id="66a48-116">assign action</span></span>](../api/intune-apps-manageddevicemobileappconfiguration-assign.md)|<span data-ttu-id="66a48-117">Ninguno</span><span class="sxs-lookup"><span data-stu-id="66a48-117">None</span></span>|<span data-ttu-id="66a48-118">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="66a48-118">Not yet documented</span></span>|

## <a name="properties"></a><span data-ttu-id="66a48-119">Propiedades</span><span class="sxs-lookup"><span data-stu-id="66a48-119">Properties</span></span>
|<span data-ttu-id="66a48-120">Propiedad</span><span class="sxs-lookup"><span data-stu-id="66a48-120">Property</span></span>|<span data-ttu-id="66a48-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="66a48-121">Type</span></span>|<span data-ttu-id="66a48-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="66a48-122">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="66a48-123">id</span><span class="sxs-lookup"><span data-stu-id="66a48-123">id</span></span>|<span data-ttu-id="66a48-124">Cadena</span><span class="sxs-lookup"><span data-stu-id="66a48-124">String</span></span>|<span data-ttu-id="66a48-125">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="66a48-125">Key of the entity.</span></span>|
|<span data-ttu-id="66a48-126">targetedMobileApps</span><span class="sxs-lookup"><span data-stu-id="66a48-126">targetedMobileApps</span></span>|<span data-ttu-id="66a48-127">Colección string</span><span class="sxs-lookup"><span data-stu-id="66a48-127">String collection</span></span>|<span data-ttu-id="66a48-128">La aplicación asociada.</span><span class="sxs-lookup"><span data-stu-id="66a48-128">the associated app.</span></span>|
|<span data-ttu-id="66a48-129">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="66a48-129">createdDateTime</span></span>|<span data-ttu-id="66a48-130">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="66a48-130">DateTimeOffset</span></span>|<span data-ttu-id="66a48-131">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="66a48-131">DateTime the object was created.</span></span>|
|<span data-ttu-id="66a48-132">descripción</span><span class="sxs-lookup"><span data-stu-id="66a48-132">description</span></span>|<span data-ttu-id="66a48-133">Cadena</span><span class="sxs-lookup"><span data-stu-id="66a48-133">String</span></span>|<span data-ttu-id="66a48-134">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="66a48-134">Admin provided description of the Device Configuration.</span></span>|
|<span data-ttu-id="66a48-135">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="66a48-135">lastModifiedDateTime</span></span>|<span data-ttu-id="66a48-136">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="66a48-136">DateTimeOffset</span></span>|<span data-ttu-id="66a48-137">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="66a48-137">DateTime the object was last modified.</span></span>|
|<span data-ttu-id="66a48-138">displayName</span><span class="sxs-lookup"><span data-stu-id="66a48-138">displayName</span></span>|<span data-ttu-id="66a48-139">Cadena</span><span class="sxs-lookup"><span data-stu-id="66a48-139">String</span></span>|<span data-ttu-id="66a48-140">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="66a48-140">Admin provided name of the device configuration.</span></span>|
|<span data-ttu-id="66a48-141">versión</span><span class="sxs-lookup"><span data-stu-id="66a48-141">version</span></span>|<span data-ttu-id="66a48-142">Int32</span><span class="sxs-lookup"><span data-stu-id="66a48-142">Int32</span></span>|<span data-ttu-id="66a48-143">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="66a48-143">Version of the device configuration.</span></span>|

## <a name="relationships"></a><span data-ttu-id="66a48-144">Relaciones</span><span class="sxs-lookup"><span data-stu-id="66a48-144">Relationships</span></span>
|<span data-ttu-id="66a48-145">Relación</span><span class="sxs-lookup"><span data-stu-id="66a48-145">Relationship</span></span>|<span data-ttu-id="66a48-146">Tipo</span><span class="sxs-lookup"><span data-stu-id="66a48-146">Type</span></span>|<span data-ttu-id="66a48-147">Descripción</span><span class="sxs-lookup"><span data-stu-id="66a48-147">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="66a48-148">asignaciones</span><span class="sxs-lookup"><span data-stu-id="66a48-148">assignments</span></span>|<span data-ttu-id="66a48-149">Colección [managedDeviceMobileAppConfigurationAssignment](../resources/intune-apps-manageddevicemobileappconfigurationassignment.md)</span><span class="sxs-lookup"><span data-stu-id="66a48-149">[managedDeviceMobileAppConfigurationAssignment](../resources/intune-apps-manageddevicemobileappconfigurationassignment.md) collection</span></span>|<span data-ttu-id="66a48-150">La lista de asignaciones de grupo para la configuración de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="66a48-150">The list of group assignemenets for app configration.</span></span>|
|<span data-ttu-id="66a48-151">deviceStatuses</span><span class="sxs-lookup"><span data-stu-id="66a48-151">deviceStatuses</span></span>|<span data-ttu-id="66a48-152">colección de [managedDeviceMobileAppConfigurationDeviceStatus](../resources/intune-apps-manageddevicemobileappconfigurationdevicestatus.md)</span><span class="sxs-lookup"><span data-stu-id="66a48-152">[managedDeviceMobileAppConfigurationDeviceStatus](../resources/intune-apps-manageddevicemobileappconfigurationdevicestatus.md) collection</span></span>|<span data-ttu-id="66a48-153">Lista de ManagedDeviceMobileAppConfigurationDeviceStatus.</span><span class="sxs-lookup"><span data-stu-id="66a48-153">List of ManagedDeviceMobileAppConfigurationDeviceStatus.</span></span>|
|<span data-ttu-id="66a48-154">userStatuses</span><span class="sxs-lookup"><span data-stu-id="66a48-154">userStatuses</span></span>|<span data-ttu-id="66a48-155">Colección [managedDeviceMobileAppConfigurationUserStatus](../resources/intune-apps-manageddevicemobileappconfigurationuserstatus.md)</span><span class="sxs-lookup"><span data-stu-id="66a48-155">[managedDeviceMobileAppConfigurationUserStatus](../resources/intune-apps-manageddevicemobileappconfigurationuserstatus.md) collection</span></span>|<span data-ttu-id="66a48-156">Lista de ManagedDeviceMobileAppConfigurationUserStatus.</span><span class="sxs-lookup"><span data-stu-id="66a48-156">List of ManagedDeviceMobileAppConfigurationUserStatus.</span></span>|
|<span data-ttu-id="66a48-157">deviceStatusSummary</span><span class="sxs-lookup"><span data-stu-id="66a48-157">deviceStatusSummary</span></span>|[<span data-ttu-id="66a48-158">managedDeviceMobileAppConfigurationDeviceSummary</span><span class="sxs-lookup"><span data-stu-id="66a48-158">managedDeviceMobileAppConfigurationDeviceSummary</span></span>](../resources/intune-apps-manageddevicemobileappconfigurationdevicesummary.md)|<span data-ttu-id="66a48-159">Resumen del estado del dispositivo de la configuración de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="66a48-159">App configuration device status summary.</span></span>|
|<span data-ttu-id="66a48-160">userStatusSummary</span><span class="sxs-lookup"><span data-stu-id="66a48-160">userStatusSummary</span></span>|[<span data-ttu-id="66a48-161">managedDeviceMobileAppConfigurationUserSummary</span><span class="sxs-lookup"><span data-stu-id="66a48-161">managedDeviceMobileAppConfigurationUserSummary</span></span>](../resources/intune-apps-manageddevicemobileappconfigurationusersummary.md)|<span data-ttu-id="66a48-162">Resumen del estado del usuario de la configuración de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="66a48-162">App configuration user status summary.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="66a48-163">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="66a48-163">JSON Representation</span></span>
<span data-ttu-id="66a48-164">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="66a48-164">Here is a JSON representation of the resource.</span></span>
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



