---
title: Actualizar iosUpdateDeviceStatus
description: Actualice las propiedades de un objeto iosUpdateDeviceStatus.
author: tfitzmac
ms.openlocfilehash: d2fab69e918d92e07ed28f3e12aa59db9d50c53b
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27350214"
---
# <a name="update-iosupdatedevicestatus"></a><span data-ttu-id="e8a48-103">Actualizar iosUpdateDeviceStatus</span><span class="sxs-lookup"><span data-stu-id="e8a48-103">Update iosUpdateDeviceStatus</span></span>

> <span data-ttu-id="e8a48-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="e8a48-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="e8a48-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="e8a48-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="e8a48-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="e8a48-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="e8a48-107">Actualice las propiedades de un objeto [iosUpdateDeviceStatus](../resources/intune-deviceconfig-iosupdatedevicestatus.md).</span><span class="sxs-lookup"><span data-stu-id="e8a48-107">Update the properties of a [iosUpdateDeviceStatus](../resources/intune-deviceconfig-iosupdatedevicestatus.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="e8a48-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="e8a48-108">Prerequisites</span></span>
<span data-ttu-id="e8a48-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="e8a48-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="e8a48-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e8a48-111">Permission type</span></span>|<span data-ttu-id="e8a48-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e8a48-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="e8a48-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e8a48-113">Delegated (work or school account)</span></span>|<span data-ttu-id="e8a48-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="e8a48-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="e8a48-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e8a48-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="e8a48-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e8a48-116">Not supported.</span></span>|
|<span data-ttu-id="e8a48-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e8a48-117">Application</span></span>|<span data-ttu-id="e8a48-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e8a48-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="e8a48-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e8a48-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/iosUpdateStatuses/{iosUpdateDeviceStatusId}
```

## <a name="request-headers"></a><span data-ttu-id="e8a48-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e8a48-120">Request headers</span></span>
|<span data-ttu-id="e8a48-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e8a48-121">Header</span></span>|<span data-ttu-id="e8a48-122">Valor</span><span class="sxs-lookup"><span data-stu-id="e8a48-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="e8a48-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="e8a48-123">Authorization</span></span>|<span data-ttu-id="e8a48-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="e8a48-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="e8a48-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="e8a48-125">Accept</span></span>|<span data-ttu-id="e8a48-126">application/json</span><span class="sxs-lookup"><span data-stu-id="e8a48-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="e8a48-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="e8a48-127">Request body</span></span>
<span data-ttu-id="e8a48-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto [iosUpdateDeviceStatus](../resources/intune-deviceconfig-iosupdatedevicestatus.md).</span><span class="sxs-lookup"><span data-stu-id="e8a48-128">In the request body, supply a JSON representation for the [iosUpdateDeviceStatus](../resources/intune-deviceconfig-iosupdatedevicestatus.md) object.</span></span>

<span data-ttu-id="e8a48-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [iosUpdateDeviceStatus](../resources/intune-deviceconfig-iosupdatedevicestatus.md).</span><span class="sxs-lookup"><span data-stu-id="e8a48-129">The following table shows the properties that are required when you create the [iosUpdateDeviceStatus](../resources/intune-deviceconfig-iosupdatedevicestatus.md).</span></span>

|<span data-ttu-id="e8a48-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e8a48-130">Property</span></span>|<span data-ttu-id="e8a48-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="e8a48-131">Type</span></span>|<span data-ttu-id="e8a48-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="e8a48-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="e8a48-133">id</span><span class="sxs-lookup"><span data-stu-id="e8a48-133">id</span></span>|<span data-ttu-id="e8a48-134">String</span><span class="sxs-lookup"><span data-stu-id="e8a48-134">String</span></span>|<span data-ttu-id="e8a48-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="e8a48-135">Key of the entity.</span></span>|
|<span data-ttu-id="e8a48-136">installStatus</span><span class="sxs-lookup"><span data-stu-id="e8a48-136">installStatus</span></span>|[<span data-ttu-id="e8a48-137">iosUpdatesInstallStatus</span><span class="sxs-lookup"><span data-stu-id="e8a48-137">iosUpdatesInstallStatus</span></span>](../resources/intune-deviceconfig-iosupdatesinstallstatus.md)|<span data-ttu-id="e8a48-138">Estado de la instalación del informe de directiva.</span><span class="sxs-lookup"><span data-stu-id="e8a48-138">The installation status of the policy report.</span></span> <span data-ttu-id="e8a48-139">Los valores posibles son: `success`, `available`, `idle`, `unknown`, `downloading`, `downloadFailed`, `downloadRequiresComputer`, `downloadInsufficientSpace`, `downloadInsufficientPower`, `downloadInsufficientNetwork`, `installing`, `installInsufficientSpace`, `installInsufficientPower`, `installPhoneCallInProgress`, `installFailed`, `notSupportedOperation`, `sharedDeviceUserLoggedInError`.</span><span class="sxs-lookup"><span data-stu-id="e8a48-139">Possible values are: `success`, `available`, `idle`, `unknown`, `downloading`, `downloadFailed`, `downloadRequiresComputer`, `downloadInsufficientSpace`, `downloadInsufficientPower`, `downloadInsufficientNetwork`, `installing`, `installInsufficientSpace`, `installInsufficientPower`, `installPhoneCallInProgress`, `installFailed`, `notSupportedOperation`, `sharedDeviceUserLoggedInError`.</span></span>|
|<span data-ttu-id="e8a48-140">osVersion</span><span class="sxs-lookup"><span data-stu-id="e8a48-140">osVersion</span></span>|<span data-ttu-id="e8a48-141">String</span><span class="sxs-lookup"><span data-stu-id="e8a48-141">String</span></span>|<span data-ttu-id="e8a48-142">La versión del dispositivo que se está notificando.</span><span class="sxs-lookup"><span data-stu-id="e8a48-142">The device version that is being reported.</span></span>|
|<span data-ttu-id="e8a48-143">deviceId</span><span class="sxs-lookup"><span data-stu-id="e8a48-143">deviceId</span></span>|<span data-ttu-id="e8a48-144">String</span><span class="sxs-lookup"><span data-stu-id="e8a48-144">String</span></span>|<span data-ttu-id="e8a48-145">El identificador del dispositivo que se está notificando.</span><span class="sxs-lookup"><span data-stu-id="e8a48-145">The device id that is being reported.</span></span>|
|<span data-ttu-id="e8a48-146">userId</span><span class="sxs-lookup"><span data-stu-id="e8a48-146">userId</span></span>|<span data-ttu-id="e8a48-147">String</span><span class="sxs-lookup"><span data-stu-id="e8a48-147">String</span></span>|<span data-ttu-id="e8a48-148">El identificador del usuario que se está notificando.</span><span class="sxs-lookup"><span data-stu-id="e8a48-148">The User id that is being reported.</span></span>|
|<span data-ttu-id="e8a48-149">deviceDisplayName</span><span class="sxs-lookup"><span data-stu-id="e8a48-149">deviceDisplayName</span></span>|<span data-ttu-id="e8a48-150">String</span><span class="sxs-lookup"><span data-stu-id="e8a48-150">String</span></span>|<span data-ttu-id="e8a48-151">Nombre de dispositivo de DevicePolicyStatus.</span><span class="sxs-lookup"><span data-stu-id="e8a48-151">Device name of the DevicePolicyStatus.</span></span>|
|<span data-ttu-id="e8a48-152">userName</span><span class="sxs-lookup"><span data-stu-id="e8a48-152">userName</span></span>|<span data-ttu-id="e8a48-153">String</span><span class="sxs-lookup"><span data-stu-id="e8a48-153">String</span></span>|<span data-ttu-id="e8a48-154">El nombre de usuario que se está notificando</span><span class="sxs-lookup"><span data-stu-id="e8a48-154">The User Name that is being reported</span></span>|
|<span data-ttu-id="e8a48-155">deviceModel</span><span class="sxs-lookup"><span data-stu-id="e8a48-155">deviceModel</span></span>|<span data-ttu-id="e8a48-156">String</span><span class="sxs-lookup"><span data-stu-id="e8a48-156">String</span></span>|<span data-ttu-id="e8a48-157">El modelo de dispositivo que se está notificando</span><span class="sxs-lookup"><span data-stu-id="e8a48-157">The device model that is being reported</span></span>|
|<span data-ttu-id="e8a48-158">platform</span><span class="sxs-lookup"><span data-stu-id="e8a48-158">platform</span></span>|<span data-ttu-id="e8a48-159">Int32</span><span class="sxs-lookup"><span data-stu-id="e8a48-159">Int32</span></span>|<span data-ttu-id="e8a48-160">Plataforma del dispositivo que se notifica</span><span class="sxs-lookup"><span data-stu-id="e8a48-160">Platform of the device that is being reported</span></span>|
|<span data-ttu-id="e8a48-161">complianceGracePeriodExpirationDateTime</span><span class="sxs-lookup"><span data-stu-id="e8a48-161">complianceGracePeriodExpirationDateTime</span></span>|<span data-ttu-id="e8a48-162">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="e8a48-162">DateTimeOffset</span></span>|<span data-ttu-id="e8a48-163">La fecha y hora en que expira el período de gracia de cumplimiento del dispositivo</span><span class="sxs-lookup"><span data-stu-id="e8a48-163">The DateTime when device compliance grace period expires</span></span>|
|<span data-ttu-id="e8a48-164">status</span><span class="sxs-lookup"><span data-stu-id="e8a48-164">status</span></span>|[<span data-ttu-id="e8a48-165">complianceStatus</span><span class="sxs-lookup"><span data-stu-id="e8a48-165">complianceStatus</span></span>](../resources/intune-shared-compliancestatus.md)|<span data-ttu-id="e8a48-166">Estado de cumplimiento del informe de directiva.</span><span class="sxs-lookup"><span data-stu-id="e8a48-166">Compliance status of the policy report.</span></span> <span data-ttu-id="e8a48-167">Los valores posibles son: `unknown`, `notApplicable`, `compliant`, `remediated`, `nonCompliant`, `error`, `conflict` y `notAssigned`.</span><span class="sxs-lookup"><span data-stu-id="e8a48-167">Possible values are: `unknown`, `notApplicable`, `compliant`, `remediated`, `nonCompliant`, `error`, `conflict`, `notAssigned`.</span></span>|
|<span data-ttu-id="e8a48-168">lastReportedDateTime</span><span class="sxs-lookup"><span data-stu-id="e8a48-168">lastReportedDateTime</span></span>|<span data-ttu-id="e8a48-169">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="e8a48-169">DateTimeOffset</span></span>|<span data-ttu-id="e8a48-170">Fecha y hora de la última modificación del informe de directiva.</span><span class="sxs-lookup"><span data-stu-id="e8a48-170">Last modified date time of the policy report.</span></span>|
|<span data-ttu-id="e8a48-171">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="e8a48-171">userPrincipalName</span></span>|<span data-ttu-id="e8a48-172">String</span><span class="sxs-lookup"><span data-stu-id="e8a48-172">String</span></span>|<span data-ttu-id="e8a48-173">UserPrincipalName.</span><span class="sxs-lookup"><span data-stu-id="e8a48-173">UserPrincipalName.</span></span>|



## <a name="response"></a><span data-ttu-id="e8a48-174">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e8a48-174">Response</span></span>
<span data-ttu-id="e8a48-175">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [iosUpdateDeviceStatus](../resources/intune-deviceconfig-iosupdatedevicestatus.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e8a48-175">If successful, this method returns a `200 OK` response code and an updated [iosUpdateDeviceStatus](../resources/intune-deviceconfig-iosupdatedevicestatus.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="e8a48-176">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e8a48-176">Example</span></span>
### <a name="request"></a><span data-ttu-id="e8a48-177">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e8a48-177">Request</span></span>
<span data-ttu-id="e8a48-178">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e8a48-178">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/iosUpdateStatuses/{iosUpdateDeviceStatusId}
Content-type: application/json
Content-length: 510

{
  "installStatus": "available",
  "osVersion": "Os Version value",
  "deviceId": "Device Id value",
  "userId": "User Id value",
  "deviceDisplayName": "Device Display Name value",
  "userName": "User Name value",
  "deviceModel": "Device Model value",
  "platform": 8,
  "complianceGracePeriodExpirationDateTime": "2016-12-31T23:56:44.951111-08:00",
  "status": "notApplicable",
  "lastReportedDateTime": "2017-01-01T00:00:17.7769392-08:00",
  "userPrincipalName": "User Principal Name value"
}
```

### <a name="response"></a><span data-ttu-id="e8a48-179">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e8a48-179">Response</span></span>
<span data-ttu-id="e8a48-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="e8a48-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 619

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
  "platform": 8,
  "complianceGracePeriodExpirationDateTime": "2016-12-31T23:56:44.951111-08:00",
  "status": "notApplicable",
  "lastReportedDateTime": "2017-01-01T00:00:17.7769392-08:00",
  "userPrincipalName": "User Principal Name value"
}
```





