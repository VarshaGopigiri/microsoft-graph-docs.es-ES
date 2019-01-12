---
title: Tipo de recurso del usuario
description: Representa un objeto de usuario de Azure Active Directory.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 908abafa3ace358125636b2c38e4cb751536a617
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27967367"
---
# <a name="user-resource-type"></a><span data-ttu-id="56cb7-103">Tipo de recurso del usuario</span><span class="sxs-lookup"><span data-stu-id="56cb7-103">user resource type</span></span>

> <span data-ttu-id="56cb7-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="56cb7-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="56cb7-105">Representa un objeto de usuario de Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="56cb7-105">Represents an Azure Active Directory user object.</span></span>

## <a name="methods"></a><span data-ttu-id="56cb7-106">Métodos</span><span class="sxs-lookup"><span data-stu-id="56cb7-106">Methods</span></span>
|<span data-ttu-id="56cb7-107">Método</span><span class="sxs-lookup"><span data-stu-id="56cb7-107">Method</span></span>|<span data-ttu-id="56cb7-108">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="56cb7-108">Return Type</span></span>|<span data-ttu-id="56cb7-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="56cb7-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="56cb7-110">[Los usuarios de la lista](../api/intune-shared-user-list.md) de objetos.</span><span class="sxs-lookup"><span data-stu-id="56cb7-110">[List users](../api/intune-shared-user-list.md) objects.</span></span>|<span data-ttu-id="56cb7-111">Colección [user](../resources/intune-shared-user.md)</span><span class="sxs-lookup"><span data-stu-id="56cb7-111">[user](../resources/intune-shared-user.md) collection</span></span>|<span data-ttu-id="56cb7-112">Enumere las propiedades y las relaciones de los objetos [user](../resources/intune-shared-user.md).</span><span class="sxs-lookup"><span data-stu-id="56cb7-112">List properties and relationships of the [user](../resources/intune-shared-user.md) objects.</span></span>|
|<span data-ttu-id="56cb7-113">Objeto [obtener el usuario](../api/intune-shared-user-get.md) .</span><span class="sxs-lookup"><span data-stu-id="56cb7-113">[Get user](../api/intune-shared-user-get.md) object.</span></span>|<span data-ttu-id="56cb7-114">Colección [user](../resources/intune-shared-user.md)</span><span class="sxs-lookup"><span data-stu-id="56cb7-114">[user](../resources/intune-shared-user.md) collection</span></span>|<span data-ttu-id="56cb7-115">Lea las propiedades y las relaciones del objeto [user](../resources/intune-shared-user.md).</span><span class="sxs-lookup"><span data-stu-id="56cb7-115">Read properties and relationships of the [user](../resources/intune-shared-user.md) object.</span></span>|
|<span data-ttu-id="56cb7-116">Objeto de [usuario de crear](../api/intune-shared-user-create.md) .</span><span class="sxs-lookup"><span data-stu-id="56cb7-116">[Create user](../api/intune-shared-user-create.md) object.</span></span>|<span data-ttu-id="56cb7-117">Colección [user](../resources/intune-shared-user.md)</span><span class="sxs-lookup"><span data-stu-id="56cb7-117">[user](../resources/intune-shared-user.md) collection</span></span>|<span data-ttu-id="56cb7-118">Cree un objeto [user](../resources/intune-shared-user.md).</span><span class="sxs-lookup"><span data-stu-id="56cb7-118">Create a new [user](../resources/intune-shared-user.md) object.</span></span>|
|<span data-ttu-id="56cb7-119">[Eliminar el usuario](../api/intune-shared-user-delete.md).</span><span class="sxs-lookup"><span data-stu-id="56cb7-119">[Delete user](../api/intune-shared-user-delete.md).</span></span>|<span data-ttu-id="56cb7-120">Ninguna</span><span class="sxs-lookup"><span data-stu-id="56cb7-120">None</span></span>|<span data-ttu-id="56cb7-121">Elimina un [user](../resources/intune-shared-user.md).</span><span class="sxs-lookup"><span data-stu-id="56cb7-121">Deletes a [user](../resources/intune-shared-user.md).</span></span>|
|<span data-ttu-id="56cb7-122">Objeto de [usuario de actualización](../api/intune-shared-user-update.md) .</span><span class="sxs-lookup"><span data-stu-id="56cb7-122">[Update user](../api/intune-shared-user-update.md) object.</span></span>|[<span data-ttu-id="56cb7-123">user</span><span class="sxs-lookup"><span data-stu-id="56cb7-123">user</span></span>](../resources/intune-shared-user.md)|<span data-ttu-id="56cb7-124">Actualice las propiedades de un objeto [user](../resources/intune-shared-user.md).</span><span class="sxs-lookup"><span data-stu-id="56cb7-124">Update the properties of a [user](../resources/intune-shared-user.md) object.</span></span>|
|<span data-ttu-id="56cb7-125">**Administración de dispositivos**</span><span class="sxs-lookup"><span data-stu-id="56cb7-125">**Device management**</span></span>|
|[<span data-ttu-id="56cb7-126">Acción removeAllDevicesFromManagement</span><span class="sxs-lookup"><span data-stu-id="56cb7-126">removeAllDevicesFromManagement action</span></span>](../api/intune-shared-user-removealldevicesfrommanagement.md)|<span data-ttu-id="56cb7-127">Ninguna</span><span class="sxs-lookup"><span data-stu-id="56cb7-127">None</span></span>|<span data-ttu-id="56cb7-128">Retirar todos los dispositivos de la administración para este usuario</span><span class="sxs-lookup"><span data-stu-id="56cb7-128">Retire all devices from management for this user</span></span>|
|<span data-ttu-id="56cb7-129">**Administración de aplicaciones móviles (MAM)**</span><span class="sxs-lookup"><span data-stu-id="56cb7-129">**Mobile app management (MAM)**</span></span>|
|[<span data-ttu-id="56cb7-130">Función getManagedAppDiagnosticStatuses</span><span class="sxs-lookup"><span data-stu-id="56cb7-130">getManagedAppDiagnosticStatuses function</span></span>](../api/intune-shared-user-getmanagedappdiagnosticstatuses.md)|<span data-ttu-id="56cb7-131">Colección [getManagedAppDiagnosticStatus](../resources/intune-mam-managedappdiagnosticstatus.md)</span><span class="sxs-lookup"><span data-stu-id="56cb7-131">[managedAppDiagnosticStatus](../resources/intune-mam-managedappdiagnosticstatus.md) collection</span></span>|<span data-ttu-id="56cb7-132">Obtiene estados de validación de diagnósticos de un usuario determinado.</span><span class="sxs-lookup"><span data-stu-id="56cb7-132">Gets diagnostics validation status for a given user.</span></span>|
|[<span data-ttu-id="56cb7-133">Función getManagedAppPolicies</span><span class="sxs-lookup"><span data-stu-id="56cb7-133">getManagedAppPolicies function</span></span>](../api/intune-shared-user-getmanagedapppolicies.md)|<span data-ttu-id="56cb7-134">Colección [managedAppPolicy](../resources/intune-mam-managedapppolicy.md)</span><span class="sxs-lookup"><span data-stu-id="56cb7-134">[managedAppPolicy](../resources/intune-mam-managedapppolicy.md) collection</span></span>|<span data-ttu-id="56cb7-135">Obtiene las restricciones de aplicaciones de un usuario determinado.</span><span class="sxs-lookup"><span data-stu-id="56cb7-135">Gets app restrictions for a given user.</span></span>|
|[<span data-ttu-id="56cb7-136">Acción wipeManagedAppRegistrationsByDeviceTag</span><span class="sxs-lookup"><span data-stu-id="56cb7-136">wipeManagedAppRegistrationsByDeviceTag action</span></span>](../api/intune-shared-user-wipemanagedappregistrationsbydevicetag.md)|<span data-ttu-id="56cb7-137">Ninguna</span><span class="sxs-lookup"><span data-stu-id="56cb7-137">None</span></span>|<span data-ttu-id="56cb7-138">Emite una operación de borrado en un registro de la aplicación con la etiqueta del dispositivo especificado.</span><span class="sxs-lookup"><span data-stu-id="56cb7-138">Issues a wipe operation on an app registration with specified device tag.</span></span>|

## <a name="properties"></a><span data-ttu-id="56cb7-139">Propiedades</span><span class="sxs-lookup"><span data-stu-id="56cb7-139">Properties</span></span>
|<span data-ttu-id="56cb7-140">Propiedad</span><span class="sxs-lookup"><span data-stu-id="56cb7-140">Property</span></span>|<span data-ttu-id="56cb7-141">Tipo</span><span class="sxs-lookup"><span data-stu-id="56cb7-141">Type</span></span>|<span data-ttu-id="56cb7-142">Descripción</span><span class="sxs-lookup"><span data-stu-id="56cb7-142">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="56cb7-143">id</span><span class="sxs-lookup"><span data-stu-id="56cb7-143">id</span></span>|<span data-ttu-id="56cb7-144">String</span><span class="sxs-lookup"><span data-stu-id="56cb7-144">String</span></span>|<span data-ttu-id="56cb7-145">Identificador único del usuario.</span><span class="sxs-lookup"><span data-stu-id="56cb7-145">Unique identifier of the user.</span></span>|
|<span data-ttu-id="56cb7-146">**Incorporación de redes**</span><span class="sxs-lookup"><span data-stu-id="56cb7-146">**Onboarding**</span></span>|
|<span data-ttu-id="56cb7-147">deviceEnrollmentLimit</span><span class="sxs-lookup"><span data-stu-id="56cb7-147">deviceEnrollmentLimit</span></span>|<span data-ttu-id="56cb7-148">Int32</span><span class="sxs-lookup"><span data-stu-id="56cb7-148">Int32</span></span>|<span data-ttu-id="56cb7-149">El límite del número máximo de dispositivos que el usuario puede inscribir.</span><span class="sxs-lookup"><span data-stu-id="56cb7-149">The limit on the maximum number of devices that the user is permitted to enroll.</span></span> <span data-ttu-id="56cb7-150">Los valores permitidos son 5 o 1000.</span><span class="sxs-lookup"><span data-stu-id="56cb7-150">Allowed values are 5 or 1000.</span></span>|


## <a name="relationships"></a><span data-ttu-id="56cb7-151">Relaciones</span><span class="sxs-lookup"><span data-stu-id="56cb7-151">Relationships</span></span>
|<span data-ttu-id="56cb7-152">Relación</span><span class="sxs-lookup"><span data-stu-id="56cb7-152">Relationship</span></span>|<span data-ttu-id="56cb7-153">Tipo</span><span class="sxs-lookup"><span data-stu-id="56cb7-153">Type</span></span>|<span data-ttu-id="56cb7-154">Descripción</span><span class="sxs-lookup"><span data-stu-id="56cb7-154">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="56cb7-155">**Administración de dispositivos**</span><span class="sxs-lookup"><span data-stu-id="56cb7-155">**Device management**</span></span>|
|<span data-ttu-id="56cb7-156">managedDevices</span><span class="sxs-lookup"><span data-stu-id="56cb7-156">managedDevices</span></span>|<span data-ttu-id="56cb7-157">Colección [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="56cb7-157">[managedDevice](../resources/intune-devices-manageddevice.md) collection</span></span>|<span data-ttu-id="56cb7-158">Los dispositivos administrados asociados al usuario.</span><span class="sxs-lookup"><span data-stu-id="56cb7-158">The managed devices associated with the user.</span></span>|
|<span data-ttu-id="56cb7-159">**Administración de aplicaciones móviles (MAM)**</span><span class="sxs-lookup"><span data-stu-id="56cb7-159">**Mobile app management (MAM)**</span></span>|
|<span data-ttu-id="56cb7-160">managedAppRegistrations</span><span class="sxs-lookup"><span data-stu-id="56cb7-160">managedAppRegistrations</span></span>|<span data-ttu-id="56cb7-161">Colección [managedAppRegistration](../resources/intune-mam-managedappregistration.md)</span><span class="sxs-lookup"><span data-stu-id="56cb7-161">[managedAppRegistration](../resources/intune-mam-managedappregistration.md) collection</span></span>|<span data-ttu-id="56cb7-162">Cero o más registros de administración de aplicaciones administradas que pertenecen al usuario.</span><span class="sxs-lookup"><span data-stu-id="56cb7-162">Zero or more managed app registrations that belong to the user.</span></span>|
|<span data-ttu-id="56cb7-163">**Solución de problemas**</span><span class="sxs-lookup"><span data-stu-id="56cb7-163">**Troubleshooting**</span></span>|
|<span data-ttu-id="56cb7-164">deviceManagementTroubleshootingEvents</span><span class="sxs-lookup"><span data-stu-id="56cb7-164">deviceManagementTroubleshootingEvents</span></span>|<span data-ttu-id="56cb7-165">Colección [deviceManagementTroubleshootingEvent](../resources/intune-troubleshooting-devicemanagementtroubleshootingevent.md)</span><span class="sxs-lookup"><span data-stu-id="56cb7-165">[deviceManagementTroubleshootingEvent](../resources/intune-troubleshooting-devicemanagementtroubleshootingevent.md) collection</span></span>|<span data-ttu-id="56cb7-166">La lista de eventos de solución de problemas para este usuario.</span><span class="sxs-lookup"><span data-stu-id="56cb7-166">The list of troubleshooting events for this user.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="56cb7-167">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="56cb7-167">JSON Representation</span></span>
<span data-ttu-id="56cb7-168">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="56cb7-168">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "baseType": "microsoft.graph.directoryObject",
  "openType": true,
  "@odata.type": "microsoft.graph.user"
}
--> 
``` json
{
  "@odata.type": "#microsoft.graph.user",
  "id": "String (identifier)",
  "deviceEnrollmentLimit": 5
}
```

<!-- {
  "type": "#page.annotation",
  "suppressions": [
    "Warning: Resource microsoft.graph.user is defined in multiple files: /api-reference/v1.0/resources/intune_shared_user.md, /api-reference/v1.0/resources/user.md",
  ]
}-->
