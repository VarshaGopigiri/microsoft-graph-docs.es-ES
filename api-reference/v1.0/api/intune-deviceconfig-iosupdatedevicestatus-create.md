---
title: Crear iosUpdateDeviceStatus
description: Cree un objeto iosUpdateDeviceStatus.
ms.openlocfilehash: 87c1d092d87ed2279d19f8f35f717501add37389
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030966"
---
# <a name="create-iosupdatedevicestatus"></a><span data-ttu-id="d28ca-103">Crear iosUpdateDeviceStatus</span><span class="sxs-lookup"><span data-stu-id="d28ca-103">Create iosUpdateDeviceStatus</span></span>

> <span data-ttu-id="d28ca-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="d28ca-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="d28ca-105">Cree un objeto [iosUpdateDeviceStatus](../resources/intune-deviceconfig-iosupdatedevicestatus.md).</span><span class="sxs-lookup"><span data-stu-id="d28ca-105">Create a new [iosUpdateDeviceStatus](../resources/intune-deviceconfig-iosupdatedevicestatus.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="d28ca-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="d28ca-106">Prerequisites</span></span>
<span data-ttu-id="d28ca-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="d28ca-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="d28ca-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="d28ca-109">Permission type</span></span>|<span data-ttu-id="d28ca-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="d28ca-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="d28ca-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d28ca-111">Delegated (work or school account)</span></span>|<span data-ttu-id="d28ca-112">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d28ca-112">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="d28ca-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="d28ca-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="d28ca-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d28ca-114">Not supported.</span></span>|
|<span data-ttu-id="d28ca-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d28ca-115">Application</span></span>|<span data-ttu-id="d28ca-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d28ca-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="d28ca-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d28ca-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/iosUpdateStatuses
```

## <a name="request-headers"></a><span data-ttu-id="d28ca-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d28ca-118">Request headers</span></span>
|<span data-ttu-id="d28ca-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d28ca-119">Header</span></span>|<span data-ttu-id="d28ca-120">Valor</span><span class="sxs-lookup"><span data-stu-id="d28ca-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="d28ca-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="d28ca-121">Authorization</span></span>|<span data-ttu-id="d28ca-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="d28ca-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="d28ca-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="d28ca-123">Accept</span></span>|<span data-ttu-id="d28ca-124">application/json</span><span class="sxs-lookup"><span data-stu-id="d28ca-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="d28ca-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="d28ca-125">Request body</span></span>
<span data-ttu-id="d28ca-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto iosUpdateDeviceStatus.</span><span class="sxs-lookup"><span data-stu-id="d28ca-126">In the request body, supply a JSON representation for the iosUpdateDeviceStatus object.</span></span>

<span data-ttu-id="d28ca-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto iosUpdateDeviceStatus.</span><span class="sxs-lookup"><span data-stu-id="d28ca-127">The following table shows the properties that are required when you create the iosUpdateDeviceStatus.</span></span>

|<span data-ttu-id="d28ca-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d28ca-128">Property</span></span>|<span data-ttu-id="d28ca-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="d28ca-129">Type</span></span>|<span data-ttu-id="d28ca-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="d28ca-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="d28ca-131">id</span><span class="sxs-lookup"><span data-stu-id="d28ca-131">id</span></span>|<span data-ttu-id="d28ca-132">String</span><span class="sxs-lookup"><span data-stu-id="d28ca-132">String</span></span>|<span data-ttu-id="d28ca-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="d28ca-133">Key of the entity.</span></span>|
|<span data-ttu-id="d28ca-134">installStatus</span><span class="sxs-lookup"><span data-stu-id="d28ca-134">installStatus</span></span>|[<span data-ttu-id="d28ca-135">iosUpdatesInstallStatus</span><span class="sxs-lookup"><span data-stu-id="d28ca-135">iosUpdatesInstallStatus</span></span>](../resources/intune-deviceconfig-iosupdatesinstallstatus.md)|<span data-ttu-id="d28ca-136">Estado de la instalación del informe de directiva.</span><span class="sxs-lookup"><span data-stu-id="d28ca-136">The installation status of the policy report.</span></span> <span data-ttu-id="d28ca-137">Los valores posibles son: `success`, `available`, `idle`, `unknown`, `downloading`, `downloadFailed`, `downloadRequiresComputer`, `downloadInsufficientSpace`, `downloadInsufficientPower`, `downloadInsufficientNetwork`, `installing`, `installInsufficientSpace`, `installInsufficientPower`, `installPhoneCallInProgress`, `installFailed`, `notSupportedOperation`, `sharedDeviceUserLoggedInError`.</span><span class="sxs-lookup"><span data-stu-id="d28ca-137">Possible values are: `success`, `available`, `idle`, `unknown`, `downloading`, `downloadFailed`, `downloadRequiresComputer`, `downloadInsufficientSpace`, `downloadInsufficientPower`, `downloadInsufficientNetwork`, `installing`, `installInsufficientSpace`, `installInsufficientPower`, `installPhoneCallInProgress`, `installFailed`, `notSupportedOperation`, `sharedDeviceUserLoggedInError`.</span></span>|
|<span data-ttu-id="d28ca-138">osVersion</span><span class="sxs-lookup"><span data-stu-id="d28ca-138">osVersion</span></span>|<span data-ttu-id="d28ca-139">String</span><span class="sxs-lookup"><span data-stu-id="d28ca-139">String</span></span>|<span data-ttu-id="d28ca-140">La versión del dispositivo que se está notificando.</span><span class="sxs-lookup"><span data-stu-id="d28ca-140">The device version that is being reported.</span></span>|
|<span data-ttu-id="d28ca-141">deviceId</span><span class="sxs-lookup"><span data-stu-id="d28ca-141">deviceId</span></span>|<span data-ttu-id="d28ca-142">String</span><span class="sxs-lookup"><span data-stu-id="d28ca-142">String</span></span>|<span data-ttu-id="d28ca-143">El identificador del dispositivo que se está notificando.</span><span class="sxs-lookup"><span data-stu-id="d28ca-143">The device id that is being reported.</span></span>|
|<span data-ttu-id="d28ca-144">userId</span><span class="sxs-lookup"><span data-stu-id="d28ca-144">userId</span></span>|<span data-ttu-id="d28ca-145">String</span><span class="sxs-lookup"><span data-stu-id="d28ca-145">String</span></span>|<span data-ttu-id="d28ca-146">El identificador del usuario que se está notificando.</span><span class="sxs-lookup"><span data-stu-id="d28ca-146">The User id that is being reported.</span></span>|
|<span data-ttu-id="d28ca-147">deviceDisplayName</span><span class="sxs-lookup"><span data-stu-id="d28ca-147">deviceDisplayName</span></span>|<span data-ttu-id="d28ca-148">String</span><span class="sxs-lookup"><span data-stu-id="d28ca-148">String</span></span>|<span data-ttu-id="d28ca-149">Nombre de dispositivo de DevicePolicyStatus.</span><span class="sxs-lookup"><span data-stu-id="d28ca-149">Device name of the DevicePolicyStatus.</span></span>|
|<span data-ttu-id="d28ca-150">userName</span><span class="sxs-lookup"><span data-stu-id="d28ca-150">userName</span></span>|<span data-ttu-id="d28ca-151">String</span><span class="sxs-lookup"><span data-stu-id="d28ca-151">String</span></span>|<span data-ttu-id="d28ca-152">El nombre de usuario que se está notificando</span><span class="sxs-lookup"><span data-stu-id="d28ca-152">The User Name that is being reported</span></span>|
|<span data-ttu-id="d28ca-153">deviceModel</span><span class="sxs-lookup"><span data-stu-id="d28ca-153">deviceModel</span></span>|<span data-ttu-id="d28ca-154">String</span><span class="sxs-lookup"><span data-stu-id="d28ca-154">String</span></span>|<span data-ttu-id="d28ca-155">El modelo de dispositivo que se está notificando</span><span class="sxs-lookup"><span data-stu-id="d28ca-155">The device model that is being reported</span></span>|
|<span data-ttu-id="d28ca-156">complianceGracePeriodExpirationDateTime</span><span class="sxs-lookup"><span data-stu-id="d28ca-156">complianceGracePeriodExpirationDateTime</span></span>|<span data-ttu-id="d28ca-157">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="d28ca-157">DateTimeOffset</span></span>|<span data-ttu-id="d28ca-158">La fecha y hora en que expira el período de gracia de cumplimiento del dispositivo</span><span class="sxs-lookup"><span data-stu-id="d28ca-158">The DateTime when device compliance grace period expires</span></span>|
|<span data-ttu-id="d28ca-159">status</span><span class="sxs-lookup"><span data-stu-id="d28ca-159">status</span></span>|[<span data-ttu-id="d28ca-160">complianceStatus</span><span class="sxs-lookup"><span data-stu-id="d28ca-160">complianceStatus</span></span>](../resources/intune-shared-compliancestatus.md)|<span data-ttu-id="d28ca-161">Estado de cumplimiento del informe de directiva.</span><span class="sxs-lookup"><span data-stu-id="d28ca-161">Compliance status of the policy report.</span></span> <span data-ttu-id="d28ca-162">Los valores posibles son: `unknown`, `notApplicable`, `compliant`, `remediated`, `nonCompliant`, `error`, `conflict` y `notAssigned`.</span><span class="sxs-lookup"><span data-stu-id="d28ca-162">Possible values are: `unknown`, `notApplicable`, `compliant`, `remediated`, `nonCompliant`, `error`, `conflict`, `notAssigned`.</span></span>|
|<span data-ttu-id="d28ca-163">lastReportedDateTime</span><span class="sxs-lookup"><span data-stu-id="d28ca-163">lastReportedDateTime</span></span>|<span data-ttu-id="d28ca-164">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="d28ca-164">DateTimeOffset</span></span>|<span data-ttu-id="d28ca-165">Fecha y hora de la última modificación del informe de directiva.</span><span class="sxs-lookup"><span data-stu-id="d28ca-165">Last modified date time of the policy report.</span></span>|
|<span data-ttu-id="d28ca-166">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="d28ca-166">userPrincipalName</span></span>|<span data-ttu-id="d28ca-167">String</span><span class="sxs-lookup"><span data-stu-id="d28ca-167">String</span></span>|<span data-ttu-id="d28ca-168">UserPrincipalName.</span><span class="sxs-lookup"><span data-stu-id="d28ca-168">UserPrincipalName.</span></span>|



## <a name="response"></a><span data-ttu-id="d28ca-169">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d28ca-169">Response</span></span>
<span data-ttu-id="d28ca-170">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [iosUpdateDeviceStatus](../resources/intune-deviceconfig-iosupdatedevicestatus.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d28ca-170">If successful, this method returns a `201 Created` response code and a [iosUpdateDeviceStatus](../resources/intune-deviceconfig-iosupdatedevicestatus.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="d28ca-171">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d28ca-171">Example</span></span>
### <a name="request"></a><span data-ttu-id="d28ca-172">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d28ca-172">Request</span></span>
<span data-ttu-id="d28ca-173">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d28ca-173">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceManagement/iosUpdateStatuses
Content-type: application/json
Content-length: 552

{
  "@odata.type": "#microsoft.graph.iosUpdateDeviceStatus",
  "installStatus": "available",
  "osVersion": "Os Version value",
  "deviceId": "Device Id value",
  "userId": "User Id value",
  "deviceDisplayName": "Device Display Name value",
  "userName": "User Name value",
  "deviceModel": "Device Model value",
  "complianceGracePeriodExpirationDateTime": "2016-12-31T23:56:44.951111-08:00",
  "status": "notApplicable",
  "lastReportedDateTime": "2017-01-01T00:00:17.7769392-08:00",
  "userPrincipalName": "User Principal Name value"
}
```

### <a name="response"></a><span data-ttu-id="d28ca-174">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d28ca-174">Response</span></span>
<span data-ttu-id="d28ca-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="d28ca-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 601

{
  "@odata.type": "#microsoft.graph.iosUpdateDeviceStatus",
  "id": "63a79499-9499-63a7-9994-a7639994a763",
  "installStatus": "available",
  "osVersion": "Os Version value",
  "deviceId": "Device Id value",
  "userId": "User Id value",
  "deviceDisplayName": "Device Display Name value",
  "userName": "User Name value",
  "deviceModel": "Device Model value",
  "complianceGracePeriodExpirationDateTime": "2016-12-31T23:56:44.951111-08:00",
  "status": "notApplicable",
  "lastReportedDateTime": "2017-01-01T00:00:17.7769392-08:00",
  "userPrincipalName": "User Principal Name value"
}
```


