---
title: Crear windowsAutopilotDeviceIdentity
description: Crear un nuevo objeto windowsAutopilotDeviceIdentity.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 56d200bd53e94715ba102f6c96bba3e3b5dd892b
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27919102"
---
# <a name="create-windowsautopilotdeviceidentity"></a><span data-ttu-id="7d017-103">Crear windowsAutopilotDeviceIdentity</span><span class="sxs-lookup"><span data-stu-id="7d017-103">Create windowsAutopilotDeviceIdentity</span></span>

> <span data-ttu-id="7d017-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="7d017-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="7d017-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="7d017-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="7d017-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="7d017-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="7d017-107">Crear un nuevo objeto [windowsAutopilotDeviceIdentity](../resources/intune-enrollment-windowsautopilotdeviceidentity.md) .</span><span class="sxs-lookup"><span data-stu-id="7d017-107">Create a new [windowsAutopilotDeviceIdentity](../resources/intune-enrollment-windowsautopilotdeviceidentity.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="7d017-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="7d017-108">Prerequisites</span></span>
<span data-ttu-id="7d017-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="7d017-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="7d017-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="7d017-111">Permission type</span></span>|<span data-ttu-id="7d017-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="7d017-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="7d017-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="7d017-113">Delegated (work or school account)</span></span>|<span data-ttu-id="7d017-114">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="7d017-114">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="7d017-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="7d017-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="7d017-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="7d017-116">Not supported.</span></span>|
|<span data-ttu-id="7d017-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="7d017-117">Application</span></span>|<span data-ttu-id="7d017-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="7d017-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="7d017-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="7d017-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/windowsAutopilotDeviceIdentities
POST /deviceManagement/windowsAutopilotDeviceIdentities/{windowsAutopilotDeviceIdentityId}/deploymentProfile/assignedDevices
```

## <a name="request-headers"></a><span data-ttu-id="7d017-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="7d017-120">Request headers</span></span>
|<span data-ttu-id="7d017-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7d017-121">Header</span></span>|<span data-ttu-id="7d017-122">Valor</span><span class="sxs-lookup"><span data-stu-id="7d017-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="7d017-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="7d017-123">Authorization</span></span>|<span data-ttu-id="7d017-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="7d017-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="7d017-125">Accept</span><span class="sxs-lookup"><span data-stu-id="7d017-125">Accept</span></span>|<span data-ttu-id="7d017-126">application/json</span><span class="sxs-lookup"><span data-stu-id="7d017-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="7d017-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="7d017-127">Request body</span></span>
<span data-ttu-id="7d017-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto windowsAutopilotDeviceIdentity.</span><span class="sxs-lookup"><span data-stu-id="7d017-128">In the request body, supply a JSON representation for the windowsAutopilotDeviceIdentity object.</span></span>

<span data-ttu-id="7d017-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el windowsAutopilotDeviceIdentity.</span><span class="sxs-lookup"><span data-stu-id="7d017-129">The following table shows the properties that are required when you create the windowsAutopilotDeviceIdentity.</span></span>

|<span data-ttu-id="7d017-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="7d017-130">Property</span></span>|<span data-ttu-id="7d017-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="7d017-131">Type</span></span>|<span data-ttu-id="7d017-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="7d017-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="7d017-133">id</span><span class="sxs-lookup"><span data-stu-id="7d017-133">id</span></span>|<span data-ttu-id="7d017-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="7d017-134">String</span></span>|<span data-ttu-id="7d017-135">El GUID para el objeto</span><span class="sxs-lookup"><span data-stu-id="7d017-135">The GUID for the object</span></span>|
|<span data-ttu-id="7d017-136">deploymentProfileAssignmentStatus</span><span class="sxs-lookup"><span data-stu-id="7d017-136">deploymentProfileAssignmentStatus</span></span>|[<span data-ttu-id="7d017-137">windowsAutopilotProfileAssignmentStatus</span><span class="sxs-lookup"><span data-stu-id="7d017-137">windowsAutopilotProfileAssignmentStatus</span></span>](../resources/intune-enrollment-windowsautopilotprofileassignmentstatus.md)|<span data-ttu-id="7d017-138">Estado de asignación de perfiles del dispositivo de piloto automático de Windows.</span><span class="sxs-lookup"><span data-stu-id="7d017-138">Profile assignment status of the Windows autopilot device.</span></span> <span data-ttu-id="7d017-139">Los valores posibles son: `unknown`, `assignedInSync`, `assignedOutOfSync`, `assignedUnkownSyncState`, `notAssigned`, `pending` y `failed`.</span><span class="sxs-lookup"><span data-stu-id="7d017-139">Possible values are: `unknown`, `assignedInSync`, `assignedOutOfSync`, `assignedUnkownSyncState`, `notAssigned`, `pending`, `failed`.</span></span>|
|<span data-ttu-id="7d017-140">deploymentProfileAssignmentDetailedStatus</span><span class="sxs-lookup"><span data-stu-id="7d017-140">deploymentProfileAssignmentDetailedStatus</span></span>|[<span data-ttu-id="7d017-141">windowsAutopilotProfileAssignmentDetailedStatus</span><span class="sxs-lookup"><span data-stu-id="7d017-141">windowsAutopilotProfileAssignmentDetailedStatus</span></span>](../resources/intune-enrollment-windowsautopilotprofileassignmentdetailedstatus.md)|<span data-ttu-id="7d017-142">Asignación de perfiles el estado detallado de los dispositivos de piloto automático de Windows.</span><span class="sxs-lookup"><span data-stu-id="7d017-142">Profile assignment detailed status of the Windows autopilot device.</span></span> <span data-ttu-id="7d017-143">Los valores posibles son: `none` y `hardwareRequirementsNotMet`.</span><span class="sxs-lookup"><span data-stu-id="7d017-143">Possible values are: `none`, `hardwareRequirementsNotMet`.</span></span>|
|<span data-ttu-id="7d017-144">deploymentProfileAssignedDateTime</span><span class="sxs-lookup"><span data-stu-id="7d017-144">deploymentProfileAssignedDateTime</span></span>|<span data-ttu-id="7d017-145">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="7d017-145">DateTimeOffset</span></span>|<span data-ttu-id="7d017-146">Perfil de establece la hora del dispositivo de piloto automático de Windows.</span><span class="sxs-lookup"><span data-stu-id="7d017-146">Profile set time of the Windows autopilot device.</span></span>|
|<span data-ttu-id="7d017-147">orderIdentifier</span><span class="sxs-lookup"><span data-stu-id="7d017-147">orderIdentifier</span></span>|<span data-ttu-id="7d017-148">Cadena</span><span class="sxs-lookup"><span data-stu-id="7d017-148">String</span></span>|<span data-ttu-id="7d017-149">Identificador del pedido del dispositivo de piloto automático de Windows.</span><span class="sxs-lookup"><span data-stu-id="7d017-149">Order Identifier of the Windows autopilot device.</span></span>|
|<span data-ttu-id="7d017-150">purchaseOrderIdentifier</span><span class="sxs-lookup"><span data-stu-id="7d017-150">purchaseOrderIdentifier</span></span>|<span data-ttu-id="7d017-151">Cadena</span><span class="sxs-lookup"><span data-stu-id="7d017-151">String</span></span>|<span data-ttu-id="7d017-152">Identificador del pedido de compra del dispositivo de piloto automático de Windows.</span><span class="sxs-lookup"><span data-stu-id="7d017-152">Purchase Order Identifier of the Windows autopilot device.</span></span>|
|<span data-ttu-id="7d017-153">serialNumber</span><span class="sxs-lookup"><span data-stu-id="7d017-153">serialNumber</span></span>|<span data-ttu-id="7d017-154">Cadena</span><span class="sxs-lookup"><span data-stu-id="7d017-154">String</span></span>|<span data-ttu-id="7d017-155">Número de serie del dispositivo Windows Autopilot.</span><span class="sxs-lookup"><span data-stu-id="7d017-155">Serial number of the Windows autopilot device.</span></span>|
|<span data-ttu-id="7d017-156">productKey</span><span class="sxs-lookup"><span data-stu-id="7d017-156">productKey</span></span>|<span data-ttu-id="7d017-157">Cadena</span><span class="sxs-lookup"><span data-stu-id="7d017-157">String</span></span>|<span data-ttu-id="7d017-158">Clave de producto del dispositivo Windows Autopilot.</span><span class="sxs-lookup"><span data-stu-id="7d017-158">Product Key of the Windows autopilot device.</span></span>|
|<span data-ttu-id="7d017-159">manufacturer</span><span class="sxs-lookup"><span data-stu-id="7d017-159">manufacturer</span></span>|<span data-ttu-id="7d017-160">Cadena</span><span class="sxs-lookup"><span data-stu-id="7d017-160">String</span></span>|<span data-ttu-id="7d017-161">Fabricante OEM del dispositivo de piloto automático de Windows.</span><span class="sxs-lookup"><span data-stu-id="7d017-161">Oem manufacturer of the Windows autopilot device.</span></span>|
|<span data-ttu-id="7d017-162">model</span><span class="sxs-lookup"><span data-stu-id="7d017-162">model</span></span>|<span data-ttu-id="7d017-163">Cadena</span><span class="sxs-lookup"><span data-stu-id="7d017-163">String</span></span>|<span data-ttu-id="7d017-164">Nombre del modelo del dispositivo de piloto automático de Windows.</span><span class="sxs-lookup"><span data-stu-id="7d017-164">Model name of the Windows autopilot device.</span></span>|
|<span data-ttu-id="7d017-165">enrollmentState</span><span class="sxs-lookup"><span data-stu-id="7d017-165">enrollmentState</span></span>|[<span data-ttu-id="7d017-166">enrollmentState</span><span class="sxs-lookup"><span data-stu-id="7d017-166">enrollmentState</span></span>](../resources/intune-enrollment-enrollmentstate.md)|<span data-ttu-id="7d017-167">Estado de inscripción Intune del dispositivo de piloto automático de Windows.</span><span class="sxs-lookup"><span data-stu-id="7d017-167">Intune enrollment state of the Windows autopilot device.</span></span> <span data-ttu-id="7d017-168">Los valores posibles son: `unknown`, `enrolled`, `pendingReset`, `failed`, `notContacted`, `blocked`.</span><span class="sxs-lookup"><span data-stu-id="7d017-168">Possible values are: `unknown`, `enrolled`, `pendingReset`, `failed`, `notContacted`, `blocked`.</span></span>|
|<span data-ttu-id="7d017-169">lastContactedDateTime</span><span class="sxs-lookup"><span data-stu-id="7d017-169">lastContactedDateTime</span></span>|<span data-ttu-id="7d017-170">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="7d017-170">DateTimeOffset</span></span>|<span data-ttu-id="7d017-171">Intune última contactado fecha hora del dispositivo de piloto automático de Windows.</span><span class="sxs-lookup"><span data-stu-id="7d017-171">Intune Last Contacted Date Time of the Windows autopilot device.</span></span>|
|<span data-ttu-id="7d017-172">addressableUserName</span><span class="sxs-lookup"><span data-stu-id="7d017-172">addressableUserName</span></span>|<span data-ttu-id="7d017-173">Cadena</span><span class="sxs-lookup"><span data-stu-id="7d017-173">String</span></span>|<span data-ttu-id="7d017-174">Nombre de usuario direccionable.</span><span class="sxs-lookup"><span data-stu-id="7d017-174">Addressable user name.</span></span>|
|<span data-ttu-id="7d017-175">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="7d017-175">userPrincipalName</span></span>|<span data-ttu-id="7d017-176">Cadena</span><span class="sxs-lookup"><span data-stu-id="7d017-176">String</span></span>|<span data-ttu-id="7d017-177">Nombre Principal de usuario.</span><span class="sxs-lookup"><span data-stu-id="7d017-177">User Principal Name.</span></span>|



## <a name="response"></a><span data-ttu-id="7d017-178">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7d017-178">Response</span></span>
<span data-ttu-id="7d017-179">Si tiene éxito, este método devuelve una `201 Created` código de respuesta y un objeto [windowsAutopilotDeviceIdentity](../resources/intune-enrollment-windowsautopilotdeviceidentity.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7d017-179">If successful, this method returns a `201 Created` response code and a [windowsAutopilotDeviceIdentity](../resources/intune-enrollment-windowsautopilotdeviceidentity.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="7d017-180">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7d017-180">Example</span></span>
### <a name="request"></a><span data-ttu-id="7d017-181">Solicitud</span><span class="sxs-lookup"><span data-stu-id="7d017-181">Request</span></span>
<span data-ttu-id="7d017-182">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="7d017-182">Here is an example of the request.</span></span>
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

### <a name="response"></a><span data-ttu-id="7d017-183">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7d017-183">Response</span></span>
<span data-ttu-id="7d017-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="7d017-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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





