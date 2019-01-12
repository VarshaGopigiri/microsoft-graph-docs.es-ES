---
title: Actualizar iosUpdateDeviceStatus
description: Actualice las propiedades de un objeto iosUpdateDeviceStatus.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 8ae033083374366a80178aac1674c4f9647bf90b
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27932178"
---
# <a name="update-iosupdatedevicestatus"></a><span data-ttu-id="bbc63-103">Actualizar iosUpdateDeviceStatus</span><span class="sxs-lookup"><span data-stu-id="bbc63-103">Update iosUpdateDeviceStatus</span></span>

> <span data-ttu-id="bbc63-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="bbc63-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="bbc63-105">Actualice las propiedades de un objeto [iosUpdateDeviceStatus](../resources/intune-deviceconfig-iosupdatedevicestatus.md).</span><span class="sxs-lookup"><span data-stu-id="bbc63-105">Update the properties of a [iosUpdateDeviceStatus](../resources/intune-deviceconfig-iosupdatedevicestatus.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="bbc63-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="bbc63-106">Prerequisites</span></span>
<span data-ttu-id="bbc63-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="bbc63-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="bbc63-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="bbc63-109">Permission type</span></span>|<span data-ttu-id="bbc63-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="bbc63-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="bbc63-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="bbc63-111">Delegated (work or school account)</span></span>|<span data-ttu-id="bbc63-112">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="bbc63-112">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="bbc63-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="bbc63-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="bbc63-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="bbc63-114">Not supported.</span></span>|
|<span data-ttu-id="bbc63-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="bbc63-115">Application</span></span>|<span data-ttu-id="bbc63-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="bbc63-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="bbc63-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="bbc63-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/iosUpdateStatuses/{iosUpdateDeviceStatusId}
```

## <a name="request-headers"></a><span data-ttu-id="bbc63-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="bbc63-118">Request headers</span></span>
|<span data-ttu-id="bbc63-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bbc63-119">Header</span></span>|<span data-ttu-id="bbc63-120">Valor</span><span class="sxs-lookup"><span data-stu-id="bbc63-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="bbc63-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="bbc63-121">Authorization</span></span>|<span data-ttu-id="bbc63-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="bbc63-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="bbc63-123">Accept</span><span class="sxs-lookup"><span data-stu-id="bbc63-123">Accept</span></span>|<span data-ttu-id="bbc63-124">application/json</span><span class="sxs-lookup"><span data-stu-id="bbc63-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="bbc63-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="bbc63-125">Request body</span></span>
<span data-ttu-id="bbc63-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto [iosUpdateDeviceStatus](../resources/intune-deviceconfig-iosupdatedevicestatus.md).</span><span class="sxs-lookup"><span data-stu-id="bbc63-126">In the request body, supply a JSON representation for the [iosUpdateDeviceStatus](../resources/intune-deviceconfig-iosupdatedevicestatus.md) object.</span></span>

<span data-ttu-id="bbc63-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [iosUpdateDeviceStatus](../resources/intune-deviceconfig-iosupdatedevicestatus.md).</span><span class="sxs-lookup"><span data-stu-id="bbc63-127">The following table shows the properties that are required when you create the [iosUpdateDeviceStatus](../resources/intune-deviceconfig-iosupdatedevicestatus.md).</span></span>

|<span data-ttu-id="bbc63-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="bbc63-128">Property</span></span>|<span data-ttu-id="bbc63-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="bbc63-129">Type</span></span>|<span data-ttu-id="bbc63-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="bbc63-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="bbc63-131">id</span><span class="sxs-lookup"><span data-stu-id="bbc63-131">id</span></span>|<span data-ttu-id="bbc63-132">Cadena</span><span class="sxs-lookup"><span data-stu-id="bbc63-132">String</span></span>|<span data-ttu-id="bbc63-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="bbc63-133">Key of the entity.</span></span>|
|<span data-ttu-id="bbc63-134">installStatus</span><span class="sxs-lookup"><span data-stu-id="bbc63-134">installStatus</span></span>|[<span data-ttu-id="bbc63-135">iosUpdatesInstallStatus</span><span class="sxs-lookup"><span data-stu-id="bbc63-135">iosUpdatesInstallStatus</span></span>](../resources/intune-deviceconfig-iosupdatesinstallstatus.md)|<span data-ttu-id="bbc63-136">Estado de la instalación del informe de directiva.</span><span class="sxs-lookup"><span data-stu-id="bbc63-136">The installation status of the policy report.</span></span> <span data-ttu-id="bbc63-137">Los valores posibles son: `success`, `available`, `idle`, `unknown`, `downloading`, `downloadFailed`, `downloadRequiresComputer`, `downloadInsufficientSpace`, `downloadInsufficientPower`, `downloadInsufficientNetwork`, `installing`, `installInsufficientSpace`, `installInsufficientPower`, `installPhoneCallInProgress`, `installFailed`, `notSupportedOperation`, `sharedDeviceUserLoggedInError`.</span><span class="sxs-lookup"><span data-stu-id="bbc63-137">Possible values are: `success`, `available`, `idle`, `unknown`, `downloading`, `downloadFailed`, `downloadRequiresComputer`, `downloadInsufficientSpace`, `downloadInsufficientPower`, `downloadInsufficientNetwork`, `installing`, `installInsufficientSpace`, `installInsufficientPower`, `installPhoneCallInProgress`, `installFailed`, `notSupportedOperation`, `sharedDeviceUserLoggedInError`.</span></span>|
|<span data-ttu-id="bbc63-138">osVersion</span><span class="sxs-lookup"><span data-stu-id="bbc63-138">osVersion</span></span>|<span data-ttu-id="bbc63-139">String</span><span class="sxs-lookup"><span data-stu-id="bbc63-139">String</span></span>|<span data-ttu-id="bbc63-140">La versión del dispositivo que se está notificando.</span><span class="sxs-lookup"><span data-stu-id="bbc63-140">The device version that is being reported.</span></span>|
|<span data-ttu-id="bbc63-141">deviceId</span><span class="sxs-lookup"><span data-stu-id="bbc63-141">deviceId</span></span>|<span data-ttu-id="bbc63-142">String</span><span class="sxs-lookup"><span data-stu-id="bbc63-142">String</span></span>|<span data-ttu-id="bbc63-143">El identificador del dispositivo que se está notificando.</span><span class="sxs-lookup"><span data-stu-id="bbc63-143">The device id that is being reported.</span></span>|
|<span data-ttu-id="bbc63-144">userId</span><span class="sxs-lookup"><span data-stu-id="bbc63-144">userId</span></span>|<span data-ttu-id="bbc63-145">String</span><span class="sxs-lookup"><span data-stu-id="bbc63-145">String</span></span>|<span data-ttu-id="bbc63-146">El identificador del usuario que se está notificando.</span><span class="sxs-lookup"><span data-stu-id="bbc63-146">The User id that is being reported.</span></span>|
|<span data-ttu-id="bbc63-147">deviceDisplayName</span><span class="sxs-lookup"><span data-stu-id="bbc63-147">deviceDisplayName</span></span>|<span data-ttu-id="bbc63-148">String</span><span class="sxs-lookup"><span data-stu-id="bbc63-148">String</span></span>|<span data-ttu-id="bbc63-149">Nombre de dispositivo de DevicePolicyStatus.</span><span class="sxs-lookup"><span data-stu-id="bbc63-149">Device name of the DevicePolicyStatus.</span></span>|
|<span data-ttu-id="bbc63-150">userName</span><span class="sxs-lookup"><span data-stu-id="bbc63-150">userName</span></span>|<span data-ttu-id="bbc63-151">Cadena</span><span class="sxs-lookup"><span data-stu-id="bbc63-151">String</span></span>|<span data-ttu-id="bbc63-152">El nombre de usuario que se está notificando</span><span class="sxs-lookup"><span data-stu-id="bbc63-152">The User Name that is being reported</span></span>|
|<span data-ttu-id="bbc63-153">deviceModel</span><span class="sxs-lookup"><span data-stu-id="bbc63-153">deviceModel</span></span>|<span data-ttu-id="bbc63-154">Cadena</span><span class="sxs-lookup"><span data-stu-id="bbc63-154">String</span></span>|<span data-ttu-id="bbc63-155">El modelo de dispositivo que se está notificando</span><span class="sxs-lookup"><span data-stu-id="bbc63-155">The device model that is being reported</span></span>|
|<span data-ttu-id="bbc63-156">complianceGracePeriodExpirationDateTime</span><span class="sxs-lookup"><span data-stu-id="bbc63-156">complianceGracePeriodExpirationDateTime</span></span>|<span data-ttu-id="bbc63-157">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="bbc63-157">DateTimeOffset</span></span>|<span data-ttu-id="bbc63-158">La fecha y hora en que expira el período de gracia de cumplimiento del dispositivo</span><span class="sxs-lookup"><span data-stu-id="bbc63-158">The DateTime when device compliance grace period expires</span></span>|
|<span data-ttu-id="bbc63-159">status</span><span class="sxs-lookup"><span data-stu-id="bbc63-159">status</span></span>|[<span data-ttu-id="bbc63-160">complianceStatus</span><span class="sxs-lookup"><span data-stu-id="bbc63-160">complianceStatus</span></span>](../resources/intune-shared-compliancestatus.md)|<span data-ttu-id="bbc63-161">Estado de cumplimiento del informe de directiva.</span><span class="sxs-lookup"><span data-stu-id="bbc63-161">Compliance status of the policy report.</span></span> <span data-ttu-id="bbc63-162">Los valores posibles son: `unknown`, `notApplicable`, `compliant`, `remediated`, `nonCompliant`, `error`, `conflict` y `notAssigned`.</span><span class="sxs-lookup"><span data-stu-id="bbc63-162">Possible values are: `unknown`, `notApplicable`, `compliant`, `remediated`, `nonCompliant`, `error`, `conflict`, `notAssigned`.</span></span>|
|<span data-ttu-id="bbc63-163">lastReportedDateTime</span><span class="sxs-lookup"><span data-stu-id="bbc63-163">lastReportedDateTime</span></span>|<span data-ttu-id="bbc63-164">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="bbc63-164">DateTimeOffset</span></span>|<span data-ttu-id="bbc63-165">Fecha y hora de la última modificación del informe de directiva.</span><span class="sxs-lookup"><span data-stu-id="bbc63-165">Last modified date time of the policy report.</span></span>|
|<span data-ttu-id="bbc63-166">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="bbc63-166">userPrincipalName</span></span>|<span data-ttu-id="bbc63-167">Cadena</span><span class="sxs-lookup"><span data-stu-id="bbc63-167">String</span></span>|<span data-ttu-id="bbc63-168">UserPrincipalName.</span><span class="sxs-lookup"><span data-stu-id="bbc63-168">UserPrincipalName.</span></span>|



## <a name="response"></a><span data-ttu-id="bbc63-169">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bbc63-169">Response</span></span>
<span data-ttu-id="bbc63-170">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [iosUpdateDeviceStatus](../resources/intune-deviceconfig-iosupdatedevicestatus.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="bbc63-170">If successful, this method returns a `200 OK` response code and an updated [iosUpdateDeviceStatus](../resources/intune-deviceconfig-iosupdatedevicestatus.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="bbc63-171">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="bbc63-171">Example</span></span>
### <a name="request"></a><span data-ttu-id="bbc63-172">Solicitud</span><span class="sxs-lookup"><span data-stu-id="bbc63-172">Request</span></span>
<span data-ttu-id="bbc63-173">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="bbc63-173">Here is an example of the request.</span></span>
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

### <a name="response"></a><span data-ttu-id="bbc63-174">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bbc63-174">Response</span></span>
<span data-ttu-id="bbc63-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="bbc63-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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



