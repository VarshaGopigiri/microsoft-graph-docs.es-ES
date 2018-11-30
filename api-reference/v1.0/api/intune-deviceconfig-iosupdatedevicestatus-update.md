---
title: Actualizar iosUpdateDeviceStatus
description: Actualice las propiedades de un objeto iosUpdateDeviceStatus.
ms.openlocfilehash: dcaf0d1fa8a9389280b58ed9521bfaa78271c96b
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27032450"
---
# <a name="update-iosupdatedevicestatus"></a><span data-ttu-id="7e82b-103">Actualizar iosUpdateDeviceStatus</span><span class="sxs-lookup"><span data-stu-id="7e82b-103">Update iosUpdateDeviceStatus</span></span>

> <span data-ttu-id="7e82b-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="7e82b-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="7e82b-105">Actualice las propiedades de un objeto [iosUpdateDeviceStatus](../resources/intune-deviceconfig-iosupdatedevicestatus.md).</span><span class="sxs-lookup"><span data-stu-id="7e82b-105">Update the properties of a [iosUpdateDeviceStatus](../resources/intune-deviceconfig-iosupdatedevicestatus.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="7e82b-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="7e82b-106">Prerequisites</span></span>
<span data-ttu-id="7e82b-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="7e82b-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="7e82b-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="7e82b-109">Permission type</span></span>|<span data-ttu-id="7e82b-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="7e82b-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="7e82b-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="7e82b-111">Delegated (work or school account)</span></span>|<span data-ttu-id="7e82b-112">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="7e82b-112">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="7e82b-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="7e82b-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="7e82b-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="7e82b-114">Not supported.</span></span>|
|<span data-ttu-id="7e82b-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="7e82b-115">Application</span></span>|<span data-ttu-id="7e82b-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="7e82b-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="7e82b-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="7e82b-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/iosUpdateStatuses/{iosUpdateDeviceStatusId}
```

## <a name="request-headers"></a><span data-ttu-id="7e82b-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="7e82b-118">Request headers</span></span>
|<span data-ttu-id="7e82b-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7e82b-119">Header</span></span>|<span data-ttu-id="7e82b-120">Valor</span><span class="sxs-lookup"><span data-stu-id="7e82b-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="7e82b-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="7e82b-121">Authorization</span></span>|<span data-ttu-id="7e82b-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="7e82b-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="7e82b-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="7e82b-123">Accept</span></span>|<span data-ttu-id="7e82b-124">application/json</span><span class="sxs-lookup"><span data-stu-id="7e82b-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="7e82b-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="7e82b-125">Request body</span></span>
<span data-ttu-id="7e82b-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto [iosUpdateDeviceStatus](../resources/intune-deviceconfig-iosupdatedevicestatus.md).</span><span class="sxs-lookup"><span data-stu-id="7e82b-126">In the request body, supply a JSON representation for the [iosUpdateDeviceStatus](../resources/intune-deviceconfig-iosupdatedevicestatus.md) object.</span></span>

<span data-ttu-id="7e82b-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [iosUpdateDeviceStatus](../resources/intune-deviceconfig-iosupdatedevicestatus.md).</span><span class="sxs-lookup"><span data-stu-id="7e82b-127">The following table shows the properties that are required when you create the [iosUpdateDeviceStatus](../resources/intune-deviceconfig-iosupdatedevicestatus.md).</span></span>

|<span data-ttu-id="7e82b-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="7e82b-128">Property</span></span>|<span data-ttu-id="7e82b-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="7e82b-129">Type</span></span>|<span data-ttu-id="7e82b-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="7e82b-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="7e82b-131">id</span><span class="sxs-lookup"><span data-stu-id="7e82b-131">id</span></span>|<span data-ttu-id="7e82b-132">String</span><span class="sxs-lookup"><span data-stu-id="7e82b-132">String</span></span>|<span data-ttu-id="7e82b-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="7e82b-133">Key of the entity.</span></span>|
|<span data-ttu-id="7e82b-134">installStatus</span><span class="sxs-lookup"><span data-stu-id="7e82b-134">installStatus</span></span>|[<span data-ttu-id="7e82b-135">iosUpdatesInstallStatus</span><span class="sxs-lookup"><span data-stu-id="7e82b-135">iosUpdatesInstallStatus</span></span>](../resources/intune-deviceconfig-iosupdatesinstallstatus.md)|<span data-ttu-id="7e82b-136">Estado de la instalación del informe de directiva.</span><span class="sxs-lookup"><span data-stu-id="7e82b-136">The installation status of the policy report.</span></span> <span data-ttu-id="7e82b-137">Los valores posibles son: `success`, `available`, `idle`, `unknown`, `downloading`, `downloadFailed`, `downloadRequiresComputer`, `downloadInsufficientSpace`, `downloadInsufficientPower`, `downloadInsufficientNetwork`, `installing`, `installInsufficientSpace`, `installInsufficientPower`, `installPhoneCallInProgress`, `installFailed`, `notSupportedOperation`, `sharedDeviceUserLoggedInError`.</span><span class="sxs-lookup"><span data-stu-id="7e82b-137">Possible values are: `success`, `available`, `idle`, `unknown`, `downloading`, `downloadFailed`, `downloadRequiresComputer`, `downloadInsufficientSpace`, `downloadInsufficientPower`, `downloadInsufficientNetwork`, `installing`, `installInsufficientSpace`, `installInsufficientPower`, `installPhoneCallInProgress`, `installFailed`, `notSupportedOperation`, `sharedDeviceUserLoggedInError`.</span></span>|
|<span data-ttu-id="7e82b-138">osVersion</span><span class="sxs-lookup"><span data-stu-id="7e82b-138">osVersion</span></span>|<span data-ttu-id="7e82b-139">String</span><span class="sxs-lookup"><span data-stu-id="7e82b-139">String</span></span>|<span data-ttu-id="7e82b-140">La versión del dispositivo que se está notificando.</span><span class="sxs-lookup"><span data-stu-id="7e82b-140">The device version that is being reported.</span></span>|
|<span data-ttu-id="7e82b-141">deviceId</span><span class="sxs-lookup"><span data-stu-id="7e82b-141">deviceId</span></span>|<span data-ttu-id="7e82b-142">String</span><span class="sxs-lookup"><span data-stu-id="7e82b-142">String</span></span>|<span data-ttu-id="7e82b-143">El identificador del dispositivo que se está notificando.</span><span class="sxs-lookup"><span data-stu-id="7e82b-143">The device id that is being reported.</span></span>|
|<span data-ttu-id="7e82b-144">userId</span><span class="sxs-lookup"><span data-stu-id="7e82b-144">userId</span></span>|<span data-ttu-id="7e82b-145">String</span><span class="sxs-lookup"><span data-stu-id="7e82b-145">String</span></span>|<span data-ttu-id="7e82b-146">El identificador del usuario que se está notificando.</span><span class="sxs-lookup"><span data-stu-id="7e82b-146">The User id that is being reported.</span></span>|
|<span data-ttu-id="7e82b-147">deviceDisplayName</span><span class="sxs-lookup"><span data-stu-id="7e82b-147">deviceDisplayName</span></span>|<span data-ttu-id="7e82b-148">String</span><span class="sxs-lookup"><span data-stu-id="7e82b-148">String</span></span>|<span data-ttu-id="7e82b-149">Nombre de dispositivo de DevicePolicyStatus.</span><span class="sxs-lookup"><span data-stu-id="7e82b-149">Device name of the DevicePolicyStatus.</span></span>|
|<span data-ttu-id="7e82b-150">userName</span><span class="sxs-lookup"><span data-stu-id="7e82b-150">userName</span></span>|<span data-ttu-id="7e82b-151">String</span><span class="sxs-lookup"><span data-stu-id="7e82b-151">String</span></span>|<span data-ttu-id="7e82b-152">El nombre de usuario que se está notificando</span><span class="sxs-lookup"><span data-stu-id="7e82b-152">The User Name that is being reported</span></span>|
|<span data-ttu-id="7e82b-153">deviceModel</span><span class="sxs-lookup"><span data-stu-id="7e82b-153">deviceModel</span></span>|<span data-ttu-id="7e82b-154">String</span><span class="sxs-lookup"><span data-stu-id="7e82b-154">String</span></span>|<span data-ttu-id="7e82b-155">El modelo de dispositivo que se está notificando</span><span class="sxs-lookup"><span data-stu-id="7e82b-155">The device model that is being reported</span></span>|
|<span data-ttu-id="7e82b-156">complianceGracePeriodExpirationDateTime</span><span class="sxs-lookup"><span data-stu-id="7e82b-156">complianceGracePeriodExpirationDateTime</span></span>|<span data-ttu-id="7e82b-157">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="7e82b-157">DateTimeOffset</span></span>|<span data-ttu-id="7e82b-158">La fecha y hora en que expira el período de gracia de cumplimiento del dispositivo</span><span class="sxs-lookup"><span data-stu-id="7e82b-158">The DateTime when device compliance grace period expires</span></span>|
|<span data-ttu-id="7e82b-159">status</span><span class="sxs-lookup"><span data-stu-id="7e82b-159">status</span></span>|[<span data-ttu-id="7e82b-160">complianceStatus</span><span class="sxs-lookup"><span data-stu-id="7e82b-160">complianceStatus</span></span>](../resources/intune-shared-compliancestatus.md)|<span data-ttu-id="7e82b-161">Estado de cumplimiento del informe de directiva.</span><span class="sxs-lookup"><span data-stu-id="7e82b-161">Compliance status of the policy report.</span></span> <span data-ttu-id="7e82b-162">Los valores posibles son: `unknown`, `notApplicable`, `compliant`, `remediated`, `nonCompliant`, `error`, `conflict` y `notAssigned`.</span><span class="sxs-lookup"><span data-stu-id="7e82b-162">Possible values are: `unknown`, `notApplicable`, `compliant`, `remediated`, `nonCompliant`, `error`, `conflict`, `notAssigned`.</span></span>|
|<span data-ttu-id="7e82b-163">lastReportedDateTime</span><span class="sxs-lookup"><span data-stu-id="7e82b-163">lastReportedDateTime</span></span>|<span data-ttu-id="7e82b-164">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="7e82b-164">DateTimeOffset</span></span>|<span data-ttu-id="7e82b-165">Fecha y hora de la última modificación del informe de directiva.</span><span class="sxs-lookup"><span data-stu-id="7e82b-165">Last modified date time of the policy report.</span></span>|
|<span data-ttu-id="7e82b-166">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="7e82b-166">userPrincipalName</span></span>|<span data-ttu-id="7e82b-167">String</span><span class="sxs-lookup"><span data-stu-id="7e82b-167">String</span></span>|<span data-ttu-id="7e82b-168">UserPrincipalName.</span><span class="sxs-lookup"><span data-stu-id="7e82b-168">UserPrincipalName.</span></span>|



## <a name="response"></a><span data-ttu-id="7e82b-169">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7e82b-169">Response</span></span>
<span data-ttu-id="7e82b-170">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [iosUpdateDeviceStatus](../resources/intune-deviceconfig-iosupdatedevicestatus.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7e82b-170">If successful, this method returns a `200 OK` response code and an updated [iosUpdateDeviceStatus](../resources/intune-deviceconfig-iosupdatedevicestatus.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="7e82b-171">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7e82b-171">Example</span></span>
### <a name="request"></a><span data-ttu-id="7e82b-172">Solicitud</span><span class="sxs-lookup"><span data-stu-id="7e82b-172">Request</span></span>
<span data-ttu-id="7e82b-173">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="7e82b-173">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/iosUpdateStatuses/{iosUpdateDeviceStatusId}
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

### <a name="response"></a><span data-ttu-id="7e82b-174">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7e82b-174">Response</span></span>
<span data-ttu-id="7e82b-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="7e82b-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
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



