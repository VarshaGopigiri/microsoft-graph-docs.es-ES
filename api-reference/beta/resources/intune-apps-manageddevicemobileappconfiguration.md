---
title: Tipo de recurso managedDeviceMobileAppConfiguration
description: Una clase abstracta para la configuración de aplicaciones móviles para dispositivos inscritos.
ms.openlocfilehash: c829e720e8d998428e778e5b7bf20e5fe465dfd6
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083036"
---
# <a name="manageddevicemobileappconfiguration-resource-type"></a><span data-ttu-id="78c77-103">Tipo de recurso managedDeviceMobileAppConfiguration</span><span class="sxs-lookup"><span data-stu-id="78c77-103">managedDeviceMobileAppConfiguration resource type</span></span>

> <span data-ttu-id="78c77-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="78c77-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="78c77-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="78c77-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="78c77-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="78c77-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="78c77-107">Una clase abstracta para la configuración de aplicaciones móviles para dispositivos inscritos.</span><span class="sxs-lookup"><span data-stu-id="78c77-107">An abstract class for Mobile app configuration for enrolled devices.</span></span>
## <a name="methods"></a><span data-ttu-id="78c77-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="78c77-108">Methods</span></span>
|<span data-ttu-id="78c77-109">Método</span><span class="sxs-lookup"><span data-stu-id="78c77-109">Method</span></span>|<span data-ttu-id="78c77-110">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="78c77-110">Return Type</span></span>|<span data-ttu-id="78c77-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="78c77-111">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="78c77-112">Enumerar managedDeviceMobileAppConfigurations</span><span class="sxs-lookup"><span data-stu-id="78c77-112">List managedDeviceMobileAppConfigurations</span></span>](../api/intune-apps-manageddevicemobileappconfiguration-list.md)|<span data-ttu-id="78c77-113">Colección [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="78c77-113">[managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md) collection</span></span>|<span data-ttu-id="78c77-114">Enumere las propiedades y las relaciones de los objetos [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="78c77-114">List properties and relationships of the [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md) objects.</span></span>|
|[<span data-ttu-id="78c77-115">Obtener managedDeviceMobileAppConfiguration</span><span class="sxs-lookup"><span data-stu-id="78c77-115">Get managedDeviceMobileAppConfiguration</span></span>](../api/intune-apps-manageddevicemobileappconfiguration-get.md)|[<span data-ttu-id="78c77-116">managedDeviceMobileAppConfiguration</span><span class="sxs-lookup"><span data-stu-id="78c77-116">managedDeviceMobileAppConfiguration</span></span>](../resources/intune-apps-manageddevicemobileappconfiguration.md)|<span data-ttu-id="78c77-117">Lea las propiedades y las relaciones del objeto [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="78c77-117">Read properties and relationships of the [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md) object.</span></span>|
|[<span data-ttu-id="78c77-118">Acción assign</span><span class="sxs-lookup"><span data-stu-id="78c77-118">assign action</span></span>](../api/intune-apps-manageddevicemobileappconfiguration-assign.md)|<span data-ttu-id="78c77-119">Ninguno</span><span class="sxs-lookup"><span data-stu-id="78c77-119">None</span></span>|<span data-ttu-id="78c77-120">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="78c77-120">Not yet documented</span></span>|

## <a name="properties"></a><span data-ttu-id="78c77-121">Propiedades</span><span class="sxs-lookup"><span data-stu-id="78c77-121">Properties</span></span>
|<span data-ttu-id="78c77-122">Propiedad</span><span class="sxs-lookup"><span data-stu-id="78c77-122">Property</span></span>|<span data-ttu-id="78c77-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="78c77-123">Type</span></span>|<span data-ttu-id="78c77-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="78c77-124">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="78c77-125">id</span><span class="sxs-lookup"><span data-stu-id="78c77-125">id</span></span>|<span data-ttu-id="78c77-126">String</span><span class="sxs-lookup"><span data-stu-id="78c77-126">String</span></span>|<span data-ttu-id="78c77-127">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="78c77-127">Key of the entity.</span></span>|
|<span data-ttu-id="78c77-128">targetedMobileApps</span><span class="sxs-lookup"><span data-stu-id="78c77-128">targetedMobileApps</span></span>|<span data-ttu-id="78c77-129">Colección string</span><span class="sxs-lookup"><span data-stu-id="78c77-129">String collection</span></span>|<span data-ttu-id="78c77-130">La aplicación asociada.</span><span class="sxs-lookup"><span data-stu-id="78c77-130">the associated app.</span></span>|
|<span data-ttu-id="78c77-131">roleScopeTagIds</span><span class="sxs-lookup"><span data-stu-id="78c77-131">roleScopeTagIds</span></span>|<span data-ttu-id="78c77-132">Colección String</span><span class="sxs-lookup"><span data-stu-id="78c77-132">String collection</span></span>|<span data-ttu-id="78c77-133">Lista de etiquetas de ámbito para esta entidad de configuración de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="78c77-133">List of Scope Tags for this App configuration entity.</span></span>|
|<span data-ttu-id="78c77-134">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="78c77-134">createdDateTime</span></span>|<span data-ttu-id="78c77-135">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="78c77-135">DateTimeOffset</span></span>|<span data-ttu-id="78c77-136">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="78c77-136">DateTime the object was created.</span></span>|
|<span data-ttu-id="78c77-137">descripción</span><span class="sxs-lookup"><span data-stu-id="78c77-137">description</span></span>|<span data-ttu-id="78c77-138">String</span><span class="sxs-lookup"><span data-stu-id="78c77-138">String</span></span>|<span data-ttu-id="78c77-139">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="78c77-139">Admin provided description of the Device Configuration.</span></span>|
|<span data-ttu-id="78c77-140">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="78c77-140">lastModifiedDateTime</span></span>|<span data-ttu-id="78c77-141">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="78c77-141">DateTimeOffset</span></span>|<span data-ttu-id="78c77-142">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="78c77-142">DateTime the object was last modified.</span></span>|
|<span data-ttu-id="78c77-143">displayName</span><span class="sxs-lookup"><span data-stu-id="78c77-143">displayName</span></span>|<span data-ttu-id="78c77-144">String</span><span class="sxs-lookup"><span data-stu-id="78c77-144">String</span></span>|<span data-ttu-id="78c77-145">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="78c77-145">Admin provided name of the device configuration.</span></span>|
|<span data-ttu-id="78c77-146">versión</span><span class="sxs-lookup"><span data-stu-id="78c77-146">version</span></span>|<span data-ttu-id="78c77-147">Int32</span><span class="sxs-lookup"><span data-stu-id="78c77-147">Int32</span></span>|<span data-ttu-id="78c77-148">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="78c77-148">Version of the device configuration.</span></span>|

## <a name="relationships"></a><span data-ttu-id="78c77-149">Relaciones</span><span class="sxs-lookup"><span data-stu-id="78c77-149">Relationships</span></span>
|<span data-ttu-id="78c77-150">Relación</span><span class="sxs-lookup"><span data-stu-id="78c77-150">Relationship</span></span>|<span data-ttu-id="78c77-151">Tipo</span><span class="sxs-lookup"><span data-stu-id="78c77-151">Type</span></span>|<span data-ttu-id="78c77-152">Descripción</span><span class="sxs-lookup"><span data-stu-id="78c77-152">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="78c77-153">asignaciones</span><span class="sxs-lookup"><span data-stu-id="78c77-153">assignments</span></span>|<span data-ttu-id="78c77-154">Colección [managedDeviceMobileAppConfigurationAssignment](../resources/intune-apps-manageddevicemobileappconfigurationassignment.md)</span><span class="sxs-lookup"><span data-stu-id="78c77-154">[managedDeviceMobileAppConfigurationAssignment](../resources/intune-apps-manageddevicemobileappconfigurationassignment.md) collection</span></span>|<span data-ttu-id="78c77-155">La lista de asignaciones de grupo para la configuración de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="78c77-155">The list of group assignemenets for app configration.</span></span>|
|<span data-ttu-id="78c77-156">deviceStatuses</span><span class="sxs-lookup"><span data-stu-id="78c77-156">deviceStatuses</span></span>|<span data-ttu-id="78c77-157">colección de [managedDeviceMobileAppConfigurationDeviceStatus](../resources/intune-apps-manageddevicemobileappconfigurationdevicestatus.md)</span><span class="sxs-lookup"><span data-stu-id="78c77-157">[managedDeviceMobileAppConfigurationDeviceStatus](../resources/intune-apps-manageddevicemobileappconfigurationdevicestatus.md) collection</span></span>|<span data-ttu-id="78c77-158">Lista de ManagedDeviceMobileAppConfigurationDeviceStatus.</span><span class="sxs-lookup"><span data-stu-id="78c77-158">List of ManagedDeviceMobileAppConfigurationDeviceStatus.</span></span>|
|<span data-ttu-id="78c77-159">userStatuses</span><span class="sxs-lookup"><span data-stu-id="78c77-159">userStatuses</span></span>|<span data-ttu-id="78c77-160">Colección [managedDeviceMobileAppConfigurationUserStatus](../resources/intune-apps-manageddevicemobileappconfigurationuserstatus.md)</span><span class="sxs-lookup"><span data-stu-id="78c77-160">[managedDeviceMobileAppConfigurationUserStatus](../resources/intune-apps-manageddevicemobileappconfigurationuserstatus.md) collection</span></span>|<span data-ttu-id="78c77-161">Lista de ManagedDeviceMobileAppConfigurationUserStatus.</span><span class="sxs-lookup"><span data-stu-id="78c77-161">List of ManagedDeviceMobileAppConfigurationUserStatus.</span></span>|
|<span data-ttu-id="78c77-162">deviceStatusSummary</span><span class="sxs-lookup"><span data-stu-id="78c77-162">deviceStatusSummary</span></span>|[<span data-ttu-id="78c77-163">managedDeviceMobileAppConfigurationDeviceSummary</span><span class="sxs-lookup"><span data-stu-id="78c77-163">managedDeviceMobileAppConfigurationDeviceSummary</span></span>](../resources/intune-apps-manageddevicemobileappconfigurationdevicesummary.md)|<span data-ttu-id="78c77-164">Resumen del estado del dispositivo de la configuración de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="78c77-164">App configuration device status summary.</span></span>|
|<span data-ttu-id="78c77-165">userStatusSummary</span><span class="sxs-lookup"><span data-stu-id="78c77-165">userStatusSummary</span></span>|[<span data-ttu-id="78c77-166">managedDeviceMobileAppConfigurationUserSummary</span><span class="sxs-lookup"><span data-stu-id="78c77-166">managedDeviceMobileAppConfigurationUserSummary</span></span>](../resources/intune-apps-manageddevicemobileappconfigurationusersummary.md)|<span data-ttu-id="78c77-167">Resumen del estado del usuario de la configuración de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="78c77-167">App configuration user status summary.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="78c77-168">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="78c77-168">JSON Representation</span></span>
<span data-ttu-id="78c77-169">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="78c77-169">Here is a JSON representation of the resource.</span></span>
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
  "roleScopeTagIds": [
    "String"
  ],
  "createdDateTime": "String (timestamp)",
  "description": "String",
  "lastModifiedDateTime": "String (timestamp)",
  "displayName": "String",
  "version": 1024
}
```





