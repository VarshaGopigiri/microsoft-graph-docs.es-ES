---
title: Actualizar windowsAutopilotDeviceIdentity
description: Actualizar las propiedades de un objeto windowsAutopilotDeviceIdentity.
author: tfitzmac
ms.openlocfilehash: b1ec7e17602becbf70d825711f2e2ea55b278fb5
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27356353"
---
# <a name="update-windowsautopilotdeviceidentity"></a><span data-ttu-id="8f97e-103">Actualizar windowsAutopilotDeviceIdentity</span><span class="sxs-lookup"><span data-stu-id="8f97e-103">Update windowsAutopilotDeviceIdentity</span></span>

> <span data-ttu-id="8f97e-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="8f97e-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="8f97e-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="8f97e-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="8f97e-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="8f97e-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="8f97e-107">Actualizar las propiedades de un objeto [windowsAutopilotDeviceIdentity](../resources/intune-enrollment-windowsautopilotdeviceidentity.md) .</span><span class="sxs-lookup"><span data-stu-id="8f97e-107">Update the properties of a [windowsAutopilotDeviceIdentity](../resources/intune-enrollment-windowsautopilotdeviceidentity.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="8f97e-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="8f97e-108">Prerequisites</span></span>
<span data-ttu-id="8f97e-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="8f97e-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="8f97e-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="8f97e-111">Permission type</span></span>|<span data-ttu-id="8f97e-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="8f97e-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="8f97e-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="8f97e-113">Delegated (work or school account)</span></span>|<span data-ttu-id="8f97e-114">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="8f97e-114">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="8f97e-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="8f97e-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="8f97e-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8f97e-116">Not supported.</span></span>|
|<span data-ttu-id="8f97e-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="8f97e-117">Application</span></span>|<span data-ttu-id="8f97e-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8f97e-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="8f97e-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="8f97e-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/windowsAutopilotDeviceIdentities/{windowsAutopilotDeviceIdentityId}
PATCH /deviceManagement/windowsAutopilotDeviceIdentities/{windowsAutopilotDeviceIdentityId}/deploymentProfile/assignedDevices/{windowsAutopilotDeviceIdentityId}
```

## <a name="request-headers"></a><span data-ttu-id="8f97e-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="8f97e-120">Request headers</span></span>
|<span data-ttu-id="8f97e-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8f97e-121">Header</span></span>|<span data-ttu-id="8f97e-122">Valor</span><span class="sxs-lookup"><span data-stu-id="8f97e-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="8f97e-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="8f97e-123">Authorization</span></span>|<span data-ttu-id="8f97e-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="8f97e-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="8f97e-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="8f97e-125">Accept</span></span>|<span data-ttu-id="8f97e-126">application/json</span><span class="sxs-lookup"><span data-stu-id="8f97e-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="8f97e-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="8f97e-127">Request body</span></span>
<span data-ttu-id="8f97e-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto [windowsAutopilotDeviceIdentity](../resources/intune-enrollment-windowsautopilotdeviceidentity.md) .</span><span class="sxs-lookup"><span data-stu-id="8f97e-128">In the request body, supply a JSON representation for the [windowsAutopilotDeviceIdentity](../resources/intune-enrollment-windowsautopilotdeviceidentity.md) object.</span></span>

<span data-ttu-id="8f97e-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el [windowsAutopilotDeviceIdentity](../resources/intune-enrollment-windowsautopilotdeviceidentity.md).</span><span class="sxs-lookup"><span data-stu-id="8f97e-129">The following table shows the properties that are required when you create the [windowsAutopilotDeviceIdentity](../resources/intune-enrollment-windowsautopilotdeviceidentity.md).</span></span>

|<span data-ttu-id="8f97e-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="8f97e-130">Property</span></span>|<span data-ttu-id="8f97e-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="8f97e-131">Type</span></span>|<span data-ttu-id="8f97e-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="8f97e-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="8f97e-133">id</span><span class="sxs-lookup"><span data-stu-id="8f97e-133">id</span></span>|<span data-ttu-id="8f97e-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="8f97e-134">String</span></span>|<span data-ttu-id="8f97e-135">El GUID para el objeto</span><span class="sxs-lookup"><span data-stu-id="8f97e-135">The GUID for the object</span></span>|
|<span data-ttu-id="8f97e-136">deploymentProfileAssignmentStatus</span><span class="sxs-lookup"><span data-stu-id="8f97e-136">deploymentProfileAssignmentStatus</span></span>|[<span data-ttu-id="8f97e-137">windowsAutopilotProfileAssignmentStatus</span><span class="sxs-lookup"><span data-stu-id="8f97e-137">windowsAutopilotProfileAssignmentStatus</span></span>](../resources/intune-enrollment-windowsautopilotprofileassignmentstatus.md)|<span data-ttu-id="8f97e-138">Estado de asignación de perfiles del dispositivo de piloto automático de Windows.</span><span class="sxs-lookup"><span data-stu-id="8f97e-138">Profile assignment status of the Windows autopilot device.</span></span> <span data-ttu-id="8f97e-139">Los valores posibles son: `unknown`, `assignedInSync`, `assignedOutOfSync`, `assignedUnkownSyncState`, `notAssigned`, `pending` y `failed`.</span><span class="sxs-lookup"><span data-stu-id="8f97e-139">Possible values are: `unknown`, `assignedInSync`, `assignedOutOfSync`, `assignedUnkownSyncState`, `notAssigned`, `pending`, `failed`.</span></span>|
|<span data-ttu-id="8f97e-140">deploymentProfileAssignmentDetailedStatus</span><span class="sxs-lookup"><span data-stu-id="8f97e-140">deploymentProfileAssignmentDetailedStatus</span></span>|[<span data-ttu-id="8f97e-141">windowsAutopilotProfileAssignmentDetailedStatus</span><span class="sxs-lookup"><span data-stu-id="8f97e-141">windowsAutopilotProfileAssignmentDetailedStatus</span></span>](../resources/intune-enrollment-windowsautopilotprofileassignmentdetailedstatus.md)|<span data-ttu-id="8f97e-142">Asignación de perfiles el estado detallado de los dispositivos de piloto automático de Windows.</span><span class="sxs-lookup"><span data-stu-id="8f97e-142">Profile assignment detailed status of the Windows autopilot device.</span></span> <span data-ttu-id="8f97e-143">Los valores posibles son: `none` y `hardwareRequirementsNotMet`.</span><span class="sxs-lookup"><span data-stu-id="8f97e-143">Possible values are: `none`, `hardwareRequirementsNotMet`.</span></span>|
|<span data-ttu-id="8f97e-144">deploymentProfileAssignedDateTime</span><span class="sxs-lookup"><span data-stu-id="8f97e-144">deploymentProfileAssignedDateTime</span></span>|<span data-ttu-id="8f97e-145">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="8f97e-145">DateTimeOffset</span></span>|<span data-ttu-id="8f97e-146">Perfil de establece la hora del dispositivo de piloto automático de Windows.</span><span class="sxs-lookup"><span data-stu-id="8f97e-146">Profile set time of the Windows autopilot device.</span></span>|
|<span data-ttu-id="8f97e-147">orderIdentifier</span><span class="sxs-lookup"><span data-stu-id="8f97e-147">orderIdentifier</span></span>|<span data-ttu-id="8f97e-148">Cadena</span><span class="sxs-lookup"><span data-stu-id="8f97e-148">String</span></span>|<span data-ttu-id="8f97e-149">Identificador del pedido del dispositivo de piloto automático de Windows.</span><span class="sxs-lookup"><span data-stu-id="8f97e-149">Order Identifier of the Windows autopilot device.</span></span>|
|<span data-ttu-id="8f97e-150">purchaseOrderIdentifier</span><span class="sxs-lookup"><span data-stu-id="8f97e-150">purchaseOrderIdentifier</span></span>|<span data-ttu-id="8f97e-151">String</span><span class="sxs-lookup"><span data-stu-id="8f97e-151">String</span></span>|<span data-ttu-id="8f97e-152">Identificador del pedido de compra del dispositivo de piloto automático de Windows.</span><span class="sxs-lookup"><span data-stu-id="8f97e-152">Purchase Order Identifier of the Windows autopilot device.</span></span>|
|<span data-ttu-id="8f97e-153">serialNumber</span><span class="sxs-lookup"><span data-stu-id="8f97e-153">serialNumber</span></span>|<span data-ttu-id="8f97e-154">Cadena</span><span class="sxs-lookup"><span data-stu-id="8f97e-154">String</span></span>|<span data-ttu-id="8f97e-155">Número de serie del dispositivo Windows Autopilot.</span><span class="sxs-lookup"><span data-stu-id="8f97e-155">Serial number of the Windows autopilot device.</span></span>|
|<span data-ttu-id="8f97e-156">productKey</span><span class="sxs-lookup"><span data-stu-id="8f97e-156">productKey</span></span>|<span data-ttu-id="8f97e-157">Cadena</span><span class="sxs-lookup"><span data-stu-id="8f97e-157">String</span></span>|<span data-ttu-id="8f97e-158">Clave de producto del dispositivo Windows Autopilot.</span><span class="sxs-lookup"><span data-stu-id="8f97e-158">Product Key of the Windows autopilot device.</span></span>|
|<span data-ttu-id="8f97e-159">manufacturer</span><span class="sxs-lookup"><span data-stu-id="8f97e-159">manufacturer</span></span>|<span data-ttu-id="8f97e-160">String</span><span class="sxs-lookup"><span data-stu-id="8f97e-160">String</span></span>|<span data-ttu-id="8f97e-161">Fabricante OEM del dispositivo de piloto automático de Windows.</span><span class="sxs-lookup"><span data-stu-id="8f97e-161">Oem manufacturer of the Windows autopilot device.</span></span>|
|<span data-ttu-id="8f97e-162">model</span><span class="sxs-lookup"><span data-stu-id="8f97e-162">model</span></span>|<span data-ttu-id="8f97e-163">String</span><span class="sxs-lookup"><span data-stu-id="8f97e-163">String</span></span>|<span data-ttu-id="8f97e-164">Nombre del modelo del dispositivo de piloto automático de Windows.</span><span class="sxs-lookup"><span data-stu-id="8f97e-164">Model name of the Windows autopilot device.</span></span>|
|<span data-ttu-id="8f97e-165">enrollmentState</span><span class="sxs-lookup"><span data-stu-id="8f97e-165">enrollmentState</span></span>|[<span data-ttu-id="8f97e-166">enrollmentState</span><span class="sxs-lookup"><span data-stu-id="8f97e-166">enrollmentState</span></span>](../resources/intune-enrollment-enrollmentstate.md)|<span data-ttu-id="8f97e-167">Estado de inscripción Intune del dispositivo de piloto automático de Windows.</span><span class="sxs-lookup"><span data-stu-id="8f97e-167">Intune enrollment state of the Windows autopilot device.</span></span> <span data-ttu-id="8f97e-168">Los valores posibles son: `unknown`, `enrolled`, `pendingReset`, `failed`, `notContacted`, `blocked`.</span><span class="sxs-lookup"><span data-stu-id="8f97e-168">Possible values are: `unknown`, `enrolled`, `pendingReset`, `failed`, `notContacted`, `blocked`.</span></span>|
|<span data-ttu-id="8f97e-169">lastContactedDateTime</span><span class="sxs-lookup"><span data-stu-id="8f97e-169">lastContactedDateTime</span></span>|<span data-ttu-id="8f97e-170">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="8f97e-170">DateTimeOffset</span></span>|<span data-ttu-id="8f97e-171">Intune última contactado fecha hora del dispositivo de piloto automático de Windows.</span><span class="sxs-lookup"><span data-stu-id="8f97e-171">Intune Last Contacted Date Time of the Windows autopilot device.</span></span>|
|<span data-ttu-id="8f97e-172">addressableUserName</span><span class="sxs-lookup"><span data-stu-id="8f97e-172">addressableUserName</span></span>|<span data-ttu-id="8f97e-173">String</span><span class="sxs-lookup"><span data-stu-id="8f97e-173">String</span></span>|<span data-ttu-id="8f97e-174">Nombre de usuario direccionable.</span><span class="sxs-lookup"><span data-stu-id="8f97e-174">Addressable user name.</span></span>|
|<span data-ttu-id="8f97e-175">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="8f97e-175">userPrincipalName</span></span>|<span data-ttu-id="8f97e-176">String</span><span class="sxs-lookup"><span data-stu-id="8f97e-176">String</span></span>|<span data-ttu-id="8f97e-177">Nombre Principal de usuario.</span><span class="sxs-lookup"><span data-stu-id="8f97e-177">User Principal Name.</span></span>|



## <a name="response"></a><span data-ttu-id="8f97e-178">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8f97e-178">Response</span></span>
<span data-ttu-id="8f97e-179">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto actualizado [windowsAutopilotDeviceIdentity](../resources/intune-enrollment-windowsautopilotdeviceidentity.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8f97e-179">If successful, this method returns a `200 OK` response code and an updated [windowsAutopilotDeviceIdentity](../resources/intune-enrollment-windowsautopilotdeviceidentity.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="8f97e-180">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="8f97e-180">Example</span></span>
### <a name="request"></a><span data-ttu-id="8f97e-181">Solicitud</span><span class="sxs-lookup"><span data-stu-id="8f97e-181">Request</span></span>
<span data-ttu-id="8f97e-182">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="8f97e-182">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/windowsAutopilotDeviceIdentities/{windowsAutopilotDeviceIdentityId}
Content-type: application/json
Content-length: 686

{
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

### <a name="response"></a><span data-ttu-id="8f97e-183">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8f97e-183">Response</span></span>
<span data-ttu-id="8f97e-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="8f97e-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
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





