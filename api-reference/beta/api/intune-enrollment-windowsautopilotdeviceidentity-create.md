---
title: Crear windowsAutopilotDeviceIdentity
description: Crear un nuevo objeto windowsAutopilotDeviceIdentity.
author: tfitzmac
ms.openlocfilehash: 1e4a9d43755fff787efa08a8c727e6ddc35fa904
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27316019"
---
# <a name="create-windowsautopilotdeviceidentity"></a><span data-ttu-id="985ee-103">Crear windowsAutopilotDeviceIdentity</span><span class="sxs-lookup"><span data-stu-id="985ee-103">Create windowsAutopilotDeviceIdentity</span></span>

> <span data-ttu-id="985ee-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="985ee-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="985ee-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="985ee-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="985ee-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="985ee-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="985ee-107">Crear un nuevo objeto [windowsAutopilotDeviceIdentity](../resources/intune-enrollment-windowsautopilotdeviceidentity.md) .</span><span class="sxs-lookup"><span data-stu-id="985ee-107">Create a new [windowsAutopilotDeviceIdentity](../resources/intune-enrollment-windowsautopilotdeviceidentity.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="985ee-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="985ee-108">Prerequisites</span></span>
<span data-ttu-id="985ee-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="985ee-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="985ee-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="985ee-111">Permission type</span></span>|<span data-ttu-id="985ee-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="985ee-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="985ee-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="985ee-113">Delegated (work or school account)</span></span>|<span data-ttu-id="985ee-114">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="985ee-114">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="985ee-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="985ee-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="985ee-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="985ee-116">Not supported.</span></span>|
|<span data-ttu-id="985ee-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="985ee-117">Application</span></span>|<span data-ttu-id="985ee-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="985ee-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="985ee-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="985ee-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/windowsAutopilotDeviceIdentities
POST /deviceManagement/windowsAutopilotDeviceIdentities/{windowsAutopilotDeviceIdentityId}/deploymentProfile/assignedDevices
```

## <a name="request-headers"></a><span data-ttu-id="985ee-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="985ee-120">Request headers</span></span>
|<span data-ttu-id="985ee-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="985ee-121">Header</span></span>|<span data-ttu-id="985ee-122">Valor</span><span class="sxs-lookup"><span data-stu-id="985ee-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="985ee-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="985ee-123">Authorization</span></span>|<span data-ttu-id="985ee-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="985ee-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="985ee-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="985ee-125">Accept</span></span>|<span data-ttu-id="985ee-126">application/json</span><span class="sxs-lookup"><span data-stu-id="985ee-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="985ee-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="985ee-127">Request body</span></span>
<span data-ttu-id="985ee-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto windowsAutopilotDeviceIdentity.</span><span class="sxs-lookup"><span data-stu-id="985ee-128">In the request body, supply a JSON representation for the windowsAutopilotDeviceIdentity object.</span></span>

<span data-ttu-id="985ee-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el windowsAutopilotDeviceIdentity.</span><span class="sxs-lookup"><span data-stu-id="985ee-129">The following table shows the properties that are required when you create the windowsAutopilotDeviceIdentity.</span></span>

|<span data-ttu-id="985ee-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="985ee-130">Property</span></span>|<span data-ttu-id="985ee-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="985ee-131">Type</span></span>|<span data-ttu-id="985ee-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="985ee-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="985ee-133">id</span><span class="sxs-lookup"><span data-stu-id="985ee-133">id</span></span>|<span data-ttu-id="985ee-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="985ee-134">String</span></span>|<span data-ttu-id="985ee-135">El GUID para el objeto</span><span class="sxs-lookup"><span data-stu-id="985ee-135">The GUID for the object</span></span>|
|<span data-ttu-id="985ee-136">deploymentProfileAssignmentStatus</span><span class="sxs-lookup"><span data-stu-id="985ee-136">deploymentProfileAssignmentStatus</span></span>|[<span data-ttu-id="985ee-137">windowsAutopilotProfileAssignmentStatus</span><span class="sxs-lookup"><span data-stu-id="985ee-137">windowsAutopilotProfileAssignmentStatus</span></span>](../resources/intune-enrollment-windowsautopilotprofileassignmentstatus.md)|<span data-ttu-id="985ee-138">Estado de asignación de perfiles del dispositivo de piloto automático de Windows.</span><span class="sxs-lookup"><span data-stu-id="985ee-138">Profile assignment status of the Windows autopilot device.</span></span> <span data-ttu-id="985ee-139">Los valores posibles son: `unknown`, `assignedInSync`, `assignedOutOfSync`, `assignedUnkownSyncState`, `notAssigned`, `pending` y `failed`.</span><span class="sxs-lookup"><span data-stu-id="985ee-139">Possible values are: `unknown`, `assignedInSync`, `assignedOutOfSync`, `assignedUnkownSyncState`, `notAssigned`, `pending`, `failed`.</span></span>|
|<span data-ttu-id="985ee-140">deploymentProfileAssignmentDetailedStatus</span><span class="sxs-lookup"><span data-stu-id="985ee-140">deploymentProfileAssignmentDetailedStatus</span></span>|[<span data-ttu-id="985ee-141">windowsAutopilotProfileAssignmentDetailedStatus</span><span class="sxs-lookup"><span data-stu-id="985ee-141">windowsAutopilotProfileAssignmentDetailedStatus</span></span>](../resources/intune-enrollment-windowsautopilotprofileassignmentdetailedstatus.md)|<span data-ttu-id="985ee-142">Asignación de perfiles el estado detallado de los dispositivos de piloto automático de Windows.</span><span class="sxs-lookup"><span data-stu-id="985ee-142">Profile assignment detailed status of the Windows autopilot device.</span></span> <span data-ttu-id="985ee-143">Los valores posibles son: `none` y `hardwareRequirementsNotMet`.</span><span class="sxs-lookup"><span data-stu-id="985ee-143">Possible values are: `none`, `hardwareRequirementsNotMet`.</span></span>|
|<span data-ttu-id="985ee-144">deploymentProfileAssignedDateTime</span><span class="sxs-lookup"><span data-stu-id="985ee-144">deploymentProfileAssignedDateTime</span></span>|<span data-ttu-id="985ee-145">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="985ee-145">DateTimeOffset</span></span>|<span data-ttu-id="985ee-146">Perfil de establece la hora del dispositivo de piloto automático de Windows.</span><span class="sxs-lookup"><span data-stu-id="985ee-146">Profile set time of the Windows autopilot device.</span></span>|
|<span data-ttu-id="985ee-147">orderIdentifier</span><span class="sxs-lookup"><span data-stu-id="985ee-147">orderIdentifier</span></span>|<span data-ttu-id="985ee-148">Cadena</span><span class="sxs-lookup"><span data-stu-id="985ee-148">String</span></span>|<span data-ttu-id="985ee-149">Identificador del pedido del dispositivo de piloto automático de Windows.</span><span class="sxs-lookup"><span data-stu-id="985ee-149">Order Identifier of the Windows autopilot device.</span></span>|
|<span data-ttu-id="985ee-150">purchaseOrderIdentifier</span><span class="sxs-lookup"><span data-stu-id="985ee-150">purchaseOrderIdentifier</span></span>|<span data-ttu-id="985ee-151">String</span><span class="sxs-lookup"><span data-stu-id="985ee-151">String</span></span>|<span data-ttu-id="985ee-152">Identificador del pedido de compra del dispositivo de piloto automático de Windows.</span><span class="sxs-lookup"><span data-stu-id="985ee-152">Purchase Order Identifier of the Windows autopilot device.</span></span>|
|<span data-ttu-id="985ee-153">serialNumber</span><span class="sxs-lookup"><span data-stu-id="985ee-153">serialNumber</span></span>|<span data-ttu-id="985ee-154">Cadena</span><span class="sxs-lookup"><span data-stu-id="985ee-154">String</span></span>|<span data-ttu-id="985ee-155">Número de serie del dispositivo Windows Autopilot.</span><span class="sxs-lookup"><span data-stu-id="985ee-155">Serial number of the Windows autopilot device.</span></span>|
|<span data-ttu-id="985ee-156">productKey</span><span class="sxs-lookup"><span data-stu-id="985ee-156">productKey</span></span>|<span data-ttu-id="985ee-157">Cadena</span><span class="sxs-lookup"><span data-stu-id="985ee-157">String</span></span>|<span data-ttu-id="985ee-158">Clave de producto del dispositivo Windows Autopilot.</span><span class="sxs-lookup"><span data-stu-id="985ee-158">Product Key of the Windows autopilot device.</span></span>|
|<span data-ttu-id="985ee-159">manufacturer</span><span class="sxs-lookup"><span data-stu-id="985ee-159">manufacturer</span></span>|<span data-ttu-id="985ee-160">String</span><span class="sxs-lookup"><span data-stu-id="985ee-160">String</span></span>|<span data-ttu-id="985ee-161">Fabricante OEM del dispositivo de piloto automático de Windows.</span><span class="sxs-lookup"><span data-stu-id="985ee-161">Oem manufacturer of the Windows autopilot device.</span></span>|
|<span data-ttu-id="985ee-162">model</span><span class="sxs-lookup"><span data-stu-id="985ee-162">model</span></span>|<span data-ttu-id="985ee-163">String</span><span class="sxs-lookup"><span data-stu-id="985ee-163">String</span></span>|<span data-ttu-id="985ee-164">Nombre del modelo del dispositivo de piloto automático de Windows.</span><span class="sxs-lookup"><span data-stu-id="985ee-164">Model name of the Windows autopilot device.</span></span>|
|<span data-ttu-id="985ee-165">enrollmentState</span><span class="sxs-lookup"><span data-stu-id="985ee-165">enrollmentState</span></span>|[<span data-ttu-id="985ee-166">enrollmentState</span><span class="sxs-lookup"><span data-stu-id="985ee-166">enrollmentState</span></span>](../resources/intune-enrollment-enrollmentstate.md)|<span data-ttu-id="985ee-167">Estado de inscripción Intune del dispositivo de piloto automático de Windows.</span><span class="sxs-lookup"><span data-stu-id="985ee-167">Intune enrollment state of the Windows autopilot device.</span></span> <span data-ttu-id="985ee-168">Los valores posibles son: `unknown`, `enrolled`, `pendingReset`, `failed`, `notContacted`, `blocked`.</span><span class="sxs-lookup"><span data-stu-id="985ee-168">Possible values are: `unknown`, `enrolled`, `pendingReset`, `failed`, `notContacted`, `blocked`.</span></span>|
|<span data-ttu-id="985ee-169">lastContactedDateTime</span><span class="sxs-lookup"><span data-stu-id="985ee-169">lastContactedDateTime</span></span>|<span data-ttu-id="985ee-170">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="985ee-170">DateTimeOffset</span></span>|<span data-ttu-id="985ee-171">Intune última contactado fecha hora del dispositivo de piloto automático de Windows.</span><span class="sxs-lookup"><span data-stu-id="985ee-171">Intune Last Contacted Date Time of the Windows autopilot device.</span></span>|
|<span data-ttu-id="985ee-172">addressableUserName</span><span class="sxs-lookup"><span data-stu-id="985ee-172">addressableUserName</span></span>|<span data-ttu-id="985ee-173">String</span><span class="sxs-lookup"><span data-stu-id="985ee-173">String</span></span>|<span data-ttu-id="985ee-174">Nombre de usuario direccionable.</span><span class="sxs-lookup"><span data-stu-id="985ee-174">Addressable user name.</span></span>|
|<span data-ttu-id="985ee-175">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="985ee-175">userPrincipalName</span></span>|<span data-ttu-id="985ee-176">String</span><span class="sxs-lookup"><span data-stu-id="985ee-176">String</span></span>|<span data-ttu-id="985ee-177">Nombre Principal de usuario.</span><span class="sxs-lookup"><span data-stu-id="985ee-177">User Principal Name.</span></span>|



## <a name="response"></a><span data-ttu-id="985ee-178">Respuesta</span><span class="sxs-lookup"><span data-stu-id="985ee-178">Response</span></span>
<span data-ttu-id="985ee-179">Si tiene éxito, este método devuelve una `201 Created` código de respuesta y un objeto [windowsAutopilotDeviceIdentity](../resources/intune-enrollment-windowsautopilotdeviceidentity.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="985ee-179">If successful, this method returns a `201 Created` response code and a [windowsAutopilotDeviceIdentity](../resources/intune-enrollment-windowsautopilotdeviceidentity.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="985ee-180">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="985ee-180">Example</span></span>
### <a name="request"></a><span data-ttu-id="985ee-181">Solicitud</span><span class="sxs-lookup"><span data-stu-id="985ee-181">Request</span></span>
<span data-ttu-id="985ee-182">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="985ee-182">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/windowsAutopilotDeviceIdentities
Content-type: application/json
Content-length: 755

{
  "@odata.type": "#microsoft.graph.windowsAutopilotDeviceIdentity",
  "deploymentProfileAssignmentStatus": "assignedInSync",
  "deploymentProfileAssignmentDetailedStatus": "hardwareRequirementsNotMet",
  "deploymentProfileAssignedDateTime": "2016-12-31T23:58:26.2447023-08:00",
  "orderIdentifier": "Order Identifier value",
  "purchaseOrderIdentifier": "Purchase Order Identifier value",
  "serialNumber": "Serial Number value",
  "productKey": "Product Key value",
  "manufacturer": "Manufacturer value",
  "model": "Model value",
  "enrollmentState": "enrolled",
  "lastContactedDateTime": "2016-12-31T23:58:44.2908994-08:00",
  "addressableUserName": "Addressable User Name value",
  "userPrincipalName": "User Principal Name value"
}
```

### <a name="response"></a><span data-ttu-id="985ee-183">Respuesta</span><span class="sxs-lookup"><span data-stu-id="985ee-183">Response</span></span>
<span data-ttu-id="985ee-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="985ee-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 804

{
  "@odata.type": "#microsoft.graph.windowsAutopilotDeviceIdentity",
  "id": "fac6f0b1-f0b1-fac6-b1f0-c6fab1f0c6fa",
  "deploymentProfileAssignmentStatus": "assignedInSync",
  "deploymentProfileAssignmentDetailedStatus": "hardwareRequirementsNotMet",
  "deploymentProfileAssignedDateTime": "2016-12-31T23:58:26.2447023-08:00",
  "orderIdentifier": "Order Identifier value",
  "purchaseOrderIdentifier": "Purchase Order Identifier value",
  "serialNumber": "Serial Number value",
  "productKey": "Product Key value",
  "manufacturer": "Manufacturer value",
  "model": "Model value",
  "enrollmentState": "enrolled",
  "lastContactedDateTime": "2016-12-31T23:58:44.2908994-08:00",
  "addressableUserName": "Addressable User Name value",
  "userPrincipalName": "User Principal Name value"
}
```





