---
title: Actualizar iosUpdateDeviceStatus
description: Actualice las propiedades de un objeto iosUpdateDeviceStatus.
author: tfitzmac
ms.openlocfilehash: 623417eb92a557745c9c1d1d04cc5b7f9677bd6c
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27359307"
---
# <a name="update-iosupdatedevicestatus"></a><span data-ttu-id="97a52-103">Actualizar iosUpdateDeviceStatus</span><span class="sxs-lookup"><span data-stu-id="97a52-103">Update iosUpdateDeviceStatus</span></span>

> <span data-ttu-id="97a52-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="97a52-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="97a52-105">Actualice las propiedades de un objeto [iosUpdateDeviceStatus](../resources/intune-deviceconfig-iosupdatedevicestatus.md).</span><span class="sxs-lookup"><span data-stu-id="97a52-105">Update the properties of a [iosUpdateDeviceStatus](../resources/intune-deviceconfig-iosupdatedevicestatus.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="97a52-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="97a52-106">Prerequisites</span></span>
<span data-ttu-id="97a52-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="97a52-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="97a52-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="97a52-109">Permission type</span></span>|<span data-ttu-id="97a52-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="97a52-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="97a52-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="97a52-111">Delegated (work or school account)</span></span>|<span data-ttu-id="97a52-112">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="97a52-112">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="97a52-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="97a52-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="97a52-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="97a52-114">Not supported.</span></span>|
|<span data-ttu-id="97a52-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="97a52-115">Application</span></span>|<span data-ttu-id="97a52-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="97a52-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="97a52-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="97a52-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/iosUpdateStatuses/{iosUpdateDeviceStatusId}
```

## <a name="request-headers"></a><span data-ttu-id="97a52-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="97a52-118">Request headers</span></span>
|<span data-ttu-id="97a52-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="97a52-119">Header</span></span>|<span data-ttu-id="97a52-120">Valor</span><span class="sxs-lookup"><span data-stu-id="97a52-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="97a52-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="97a52-121">Authorization</span></span>|<span data-ttu-id="97a52-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="97a52-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="97a52-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="97a52-123">Accept</span></span>|<span data-ttu-id="97a52-124">application/json</span><span class="sxs-lookup"><span data-stu-id="97a52-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="97a52-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="97a52-125">Request body</span></span>
<span data-ttu-id="97a52-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto [iosUpdateDeviceStatus](../resources/intune-deviceconfig-iosupdatedevicestatus.md).</span><span class="sxs-lookup"><span data-stu-id="97a52-126">In the request body, supply a JSON representation for the [iosUpdateDeviceStatus](../resources/intune-deviceconfig-iosupdatedevicestatus.md) object.</span></span>

<span data-ttu-id="97a52-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [iosUpdateDeviceStatus](../resources/intune-deviceconfig-iosupdatedevicestatus.md).</span><span class="sxs-lookup"><span data-stu-id="97a52-127">The following table shows the properties that are required when you create the [iosUpdateDeviceStatus](../resources/intune-deviceconfig-iosupdatedevicestatus.md).</span></span>

|<span data-ttu-id="97a52-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="97a52-128">Property</span></span>|<span data-ttu-id="97a52-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="97a52-129">Type</span></span>|<span data-ttu-id="97a52-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="97a52-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="97a52-131">id</span><span class="sxs-lookup"><span data-stu-id="97a52-131">id</span></span>|<span data-ttu-id="97a52-132">String</span><span class="sxs-lookup"><span data-stu-id="97a52-132">String</span></span>|<span data-ttu-id="97a52-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="97a52-133">Key of the entity.</span></span>|
|<span data-ttu-id="97a52-134">installStatus</span><span class="sxs-lookup"><span data-stu-id="97a52-134">installStatus</span></span>|[<span data-ttu-id="97a52-135">iosUpdatesInstallStatus</span><span class="sxs-lookup"><span data-stu-id="97a52-135">iosUpdatesInstallStatus</span></span>](../resources/intune-deviceconfig-iosupdatesinstallstatus.md)|<span data-ttu-id="97a52-136">Estado de la instalación del informe de directiva.</span><span class="sxs-lookup"><span data-stu-id="97a52-136">The installation status of the policy report.</span></span> <span data-ttu-id="97a52-137">Los valores posibles son: `success`, `available`, `idle`, `unknown`, `downloading`, `downloadFailed`, `downloadRequiresComputer`, `downloadInsufficientSpace`, `downloadInsufficientPower`, `downloadInsufficientNetwork`, `installing`, `installInsufficientSpace`, `installInsufficientPower`, `installPhoneCallInProgress`, `installFailed`, `notSupportedOperation`, `sharedDeviceUserLoggedInError`.</span><span class="sxs-lookup"><span data-stu-id="97a52-137">Possible values are: `success`, `available`, `idle`, `unknown`, `downloading`, `downloadFailed`, `downloadRequiresComputer`, `downloadInsufficientSpace`, `downloadInsufficientPower`, `downloadInsufficientNetwork`, `installing`, `installInsufficientSpace`, `installInsufficientPower`, `installPhoneCallInProgress`, `installFailed`, `notSupportedOperation`, `sharedDeviceUserLoggedInError`.</span></span>|
|<span data-ttu-id="97a52-138">osVersion</span><span class="sxs-lookup"><span data-stu-id="97a52-138">osVersion</span></span>|<span data-ttu-id="97a52-139">String</span><span class="sxs-lookup"><span data-stu-id="97a52-139">String</span></span>|<span data-ttu-id="97a52-140">La versión del dispositivo que se está notificando.</span><span class="sxs-lookup"><span data-stu-id="97a52-140">The device version that is being reported.</span></span>|
|<span data-ttu-id="97a52-141">deviceId</span><span class="sxs-lookup"><span data-stu-id="97a52-141">deviceId</span></span>|<span data-ttu-id="97a52-142">String</span><span class="sxs-lookup"><span data-stu-id="97a52-142">String</span></span>|<span data-ttu-id="97a52-143">El identificador del dispositivo que se está notificando.</span><span class="sxs-lookup"><span data-stu-id="97a52-143">The device id that is being reported.</span></span>|
|<span data-ttu-id="97a52-144">userId</span><span class="sxs-lookup"><span data-stu-id="97a52-144">userId</span></span>|<span data-ttu-id="97a52-145">String</span><span class="sxs-lookup"><span data-stu-id="97a52-145">String</span></span>|<span data-ttu-id="97a52-146">El identificador del usuario que se está notificando.</span><span class="sxs-lookup"><span data-stu-id="97a52-146">The User id that is being reported.</span></span>|
|<span data-ttu-id="97a52-147">deviceDisplayName</span><span class="sxs-lookup"><span data-stu-id="97a52-147">deviceDisplayName</span></span>|<span data-ttu-id="97a52-148">String</span><span class="sxs-lookup"><span data-stu-id="97a52-148">String</span></span>|<span data-ttu-id="97a52-149">Nombre de dispositivo de DevicePolicyStatus.</span><span class="sxs-lookup"><span data-stu-id="97a52-149">Device name of the DevicePolicyStatus.</span></span>|
|<span data-ttu-id="97a52-150">userName</span><span class="sxs-lookup"><span data-stu-id="97a52-150">userName</span></span>|<span data-ttu-id="97a52-151">String</span><span class="sxs-lookup"><span data-stu-id="97a52-151">String</span></span>|<span data-ttu-id="97a52-152">El nombre de usuario que se está notificando</span><span class="sxs-lookup"><span data-stu-id="97a52-152">The User Name that is being reported</span></span>|
|<span data-ttu-id="97a52-153">deviceModel</span><span class="sxs-lookup"><span data-stu-id="97a52-153">deviceModel</span></span>|<span data-ttu-id="97a52-154">String</span><span class="sxs-lookup"><span data-stu-id="97a52-154">String</span></span>|<span data-ttu-id="97a52-155">El modelo de dispositivo que se está notificando</span><span class="sxs-lookup"><span data-stu-id="97a52-155">The device model that is being reported</span></span>|
|<span data-ttu-id="97a52-156">complianceGracePeriodExpirationDateTime</span><span class="sxs-lookup"><span data-stu-id="97a52-156">complianceGracePeriodExpirationDateTime</span></span>|<span data-ttu-id="97a52-157">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="97a52-157">DateTimeOffset</span></span>|<span data-ttu-id="97a52-158">La fecha y hora en que expira el período de gracia de cumplimiento del dispositivo</span><span class="sxs-lookup"><span data-stu-id="97a52-158">The DateTime when device compliance grace period expires</span></span>|
|<span data-ttu-id="97a52-159">status</span><span class="sxs-lookup"><span data-stu-id="97a52-159">status</span></span>|[<span data-ttu-id="97a52-160">complianceStatus</span><span class="sxs-lookup"><span data-stu-id="97a52-160">complianceStatus</span></span>](../resources/intune-shared-compliancestatus.md)|<span data-ttu-id="97a52-161">Estado de cumplimiento del informe de directiva.</span><span class="sxs-lookup"><span data-stu-id="97a52-161">Compliance status of the policy report.</span></span> <span data-ttu-id="97a52-162">Los valores posibles son: `unknown`, `notApplicable`, `compliant`, `remediated`, `nonCompliant`, `error`, `conflict` y `notAssigned`.</span><span class="sxs-lookup"><span data-stu-id="97a52-162">Possible values are: `unknown`, `notApplicable`, `compliant`, `remediated`, `nonCompliant`, `error`, `conflict`, `notAssigned`.</span></span>|
|<span data-ttu-id="97a52-163">lastReportedDateTime</span><span class="sxs-lookup"><span data-stu-id="97a52-163">lastReportedDateTime</span></span>|<span data-ttu-id="97a52-164">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="97a52-164">DateTimeOffset</span></span>|<span data-ttu-id="97a52-165">Fecha y hora de la última modificación del informe de directiva.</span><span class="sxs-lookup"><span data-stu-id="97a52-165">Last modified date time of the policy report.</span></span>|
|<span data-ttu-id="97a52-166">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="97a52-166">userPrincipalName</span></span>|<span data-ttu-id="97a52-167">String</span><span class="sxs-lookup"><span data-stu-id="97a52-167">String</span></span>|<span data-ttu-id="97a52-168">UserPrincipalName.</span><span class="sxs-lookup"><span data-stu-id="97a52-168">UserPrincipalName.</span></span>|



## <a name="response"></a><span data-ttu-id="97a52-169">Respuesta</span><span class="sxs-lookup"><span data-stu-id="97a52-169">Response</span></span>
<span data-ttu-id="97a52-170">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [iosUpdateDeviceStatus](../resources/intune-deviceconfig-iosupdatedevicestatus.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="97a52-170">If successful, this method returns a `200 OK` response code and an updated [iosUpdateDeviceStatus](../resources/intune-deviceconfig-iosupdatedevicestatus.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="97a52-171">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="97a52-171">Example</span></span>
### <a name="request"></a><span data-ttu-id="97a52-172">Solicitud</span><span class="sxs-lookup"><span data-stu-id="97a52-172">Request</span></span>
<span data-ttu-id="97a52-173">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="97a52-173">Here is an example of the request.</span></span>
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

### <a name="response"></a><span data-ttu-id="97a52-174">Respuesta</span><span class="sxs-lookup"><span data-stu-id="97a52-174">Response</span></span>
<span data-ttu-id="97a52-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="97a52-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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



