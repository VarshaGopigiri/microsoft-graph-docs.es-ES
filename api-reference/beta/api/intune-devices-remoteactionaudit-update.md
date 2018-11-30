---
title: Actualizar remoteActionAudit
description: Actualizar las propiedades de un objeto remoteActionAudit.
ms.openlocfilehash: f7b72ce26617b3ba370e5135c31b98c7c33cbd97
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088547"
---
# <a name="update-remoteactionaudit"></a><span data-ttu-id="36a23-103">Actualizar remoteActionAudit</span><span class="sxs-lookup"><span data-stu-id="36a23-103">Update remoteActionAudit</span></span>

> <span data-ttu-id="36a23-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="36a23-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="36a23-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="36a23-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="36a23-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="36a23-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="36a23-107">Actualizar las propiedades de un objeto [remoteActionAudit](../resources/intune-devices-remoteactionaudit.md) .</span><span class="sxs-lookup"><span data-stu-id="36a23-107">Update the properties of a [remoteActionAudit](../resources/intune-devices-remoteactionaudit.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="36a23-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="36a23-108">Prerequisites</span></span>
<span data-ttu-id="36a23-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="36a23-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="36a23-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="36a23-111">Permission type</span></span>|<span data-ttu-id="36a23-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="36a23-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="36a23-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="36a23-113">Delegated (work or school account)</span></span>|<span data-ttu-id="36a23-114">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="36a23-114">DeviceManagementManagedDevices.ReadWrite.All</span></span>|
|<span data-ttu-id="36a23-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="36a23-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="36a23-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="36a23-116">Not supported.</span></span>|
|<span data-ttu-id="36a23-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="36a23-117">Application</span></span>|<span data-ttu-id="36a23-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="36a23-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="36a23-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="36a23-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/remoteActionAudits/{remoteActionAuditId}
```

## <a name="request-headers"></a><span data-ttu-id="36a23-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="36a23-120">Request headers</span></span>
|<span data-ttu-id="36a23-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="36a23-121">Header</span></span>|<span data-ttu-id="36a23-122">Valor</span><span class="sxs-lookup"><span data-stu-id="36a23-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="36a23-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="36a23-123">Authorization</span></span>|<span data-ttu-id="36a23-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="36a23-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="36a23-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="36a23-125">Accept</span></span>|<span data-ttu-id="36a23-126">application/json</span><span class="sxs-lookup"><span data-stu-id="36a23-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="36a23-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="36a23-127">Request body</span></span>
<span data-ttu-id="36a23-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto [remoteActionAudit](../resources/intune-devices-remoteactionaudit.md) .</span><span class="sxs-lookup"><span data-stu-id="36a23-128">In the request body, supply a JSON representation for the [remoteActionAudit](../resources/intune-devices-remoteactionaudit.md) object.</span></span>

<span data-ttu-id="36a23-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el [remoteActionAudit](../resources/intune-devices-remoteactionaudit.md).</span><span class="sxs-lookup"><span data-stu-id="36a23-129">The following table shows the properties that are required when you create the [remoteActionAudit](../resources/intune-devices-remoteactionaudit.md).</span></span>

|<span data-ttu-id="36a23-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="36a23-130">Property</span></span>|<span data-ttu-id="36a23-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="36a23-131">Type</span></span>|<span data-ttu-id="36a23-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="36a23-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="36a23-133">id</span><span class="sxs-lookup"><span data-stu-id="36a23-133">id</span></span>|<span data-ttu-id="36a23-134">String</span><span class="sxs-lookup"><span data-stu-id="36a23-134">String</span></span>|<span data-ttu-id="36a23-135">ID de informe.</span><span class="sxs-lookup"><span data-stu-id="36a23-135">Report Id.</span></span>|
|<span data-ttu-id="36a23-136">deviceDisplayName</span><span class="sxs-lookup"><span data-stu-id="36a23-136">deviceDisplayName</span></span>|<span data-ttu-id="36a23-137">String</span><span class="sxs-lookup"><span data-stu-id="36a23-137">String</span></span>|<span data-ttu-id="36a23-138">Nombre del dispositivo Intune.</span><span class="sxs-lookup"><span data-stu-id="36a23-138">Intune device name.</span></span>|
|<span data-ttu-id="36a23-139">userName</span><span class="sxs-lookup"><span data-stu-id="36a23-139">userName</span></span>|<span data-ttu-id="36a23-140">String</span><span class="sxs-lookup"><span data-stu-id="36a23-140">String</span></span>|<span data-ttu-id="36a23-141">\[en desuso\] use InitiatedByUserPrincipalName en su lugar.</span><span class="sxs-lookup"><span data-stu-id="36a23-141">\[deprecated\] Please use InitiatedByUserPrincipalName instead.</span></span>|
|<span data-ttu-id="36a23-142">initiatedByUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="36a23-142">initiatedByUserPrincipalName</span></span>|<span data-ttu-id="36a23-143">String</span><span class="sxs-lookup"><span data-stu-id="36a23-143">String</span></span>|<span data-ttu-id="36a23-144">Usuario que inició la acción de dispositivo, formato es UPN.</span><span class="sxs-lookup"><span data-stu-id="36a23-144">User who initiated the device action, format is UPN.</span></span>|
|<span data-ttu-id="36a23-145">action</span><span class="sxs-lookup"><span data-stu-id="36a23-145">action</span></span>|[<span data-ttu-id="36a23-146">remoteAction</span><span class="sxs-lookup"><span data-stu-id="36a23-146">remoteAction</span></span>](../resources/intune-devices-remoteaction.md)|<span data-ttu-id="36a23-147">El nombre de la acción.</span><span class="sxs-lookup"><span data-stu-id="36a23-147">The action name.</span></span> <span data-ttu-id="36a23-148">Los valores posibles son: `unknown`, `factoryReset`, `removeCompanyData`, `resetPasscode`, `remoteLock`, `enableLostMode`, `disableLostMode`, `locateDevice`, `rebootNow`, `recoverPasscode`, `cleanWindowsDevice`, `logoutSharedAppleDeviceActiveUser`, `quickScan`, `fullScan`, `windowsDefenderUpdateSignatures`, `factoryResetKeepEnrollmentData`, `updateDeviceAccount`, `automaticRedeployment`, `shutDown` .</span><span class="sxs-lookup"><span data-stu-id="36a23-148">Possible values are: `unknown`, `factoryReset`, `removeCompanyData`, `resetPasscode`, `remoteLock`, `enableLostMode`, `disableLostMode`, `locateDevice`, `rebootNow`, `recoverPasscode`, `cleanWindowsDevice`, `logoutSharedAppleDeviceActiveUser`, `quickScan`, `fullScan`, `windowsDefenderUpdateSignatures`, `factoryResetKeepEnrollmentData`, `updateDeviceAccount`, `automaticRedeployment`, `shutDown`.</span></span>|
|<span data-ttu-id="36a23-149">requestDateTime</span><span class="sxs-lookup"><span data-stu-id="36a23-149">requestDateTime</span></span>|<span data-ttu-id="36a23-150">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="36a23-150">DateTimeOffset</span></span>|<span data-ttu-id="36a23-151">Hora en que se emitió la acción, dado en UTC.</span><span class="sxs-lookup"><span data-stu-id="36a23-151">Time when the action was issued, given in UTC.</span></span>|
|<span data-ttu-id="36a23-152">deviceOwnerUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="36a23-152">deviceOwnerUserPrincipalName</span></span>|<span data-ttu-id="36a23-153">String</span><span class="sxs-lookup"><span data-stu-id="36a23-153">String</span></span>|<span data-ttu-id="36a23-154">UPN del propietario del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="36a23-154">Upn of the device owner.</span></span>|
|<span data-ttu-id="36a23-155">deviceIMEI</span><span class="sxs-lookup"><span data-stu-id="36a23-155">deviceIMEI</span></span>|<span data-ttu-id="36a23-156">String</span><span class="sxs-lookup"><span data-stu-id="36a23-156">String</span></span>|<span data-ttu-id="36a23-157">IMEI del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="36a23-157">IMEI of the device.</span></span>|
|<span data-ttu-id="36a23-158">actionState</span><span class="sxs-lookup"><span data-stu-id="36a23-158">actionState</span></span>|[<span data-ttu-id="36a23-159">actionState</span><span class="sxs-lookup"><span data-stu-id="36a23-159">actionState</span></span>](../resources/intune-shared-actionstate.md)|<span data-ttu-id="36a23-160">Estado de acción.</span><span class="sxs-lookup"><span data-stu-id="36a23-160">Action state.</span></span> <span data-ttu-id="36a23-161">Los valores posibles son: `none`, `pending`, `canceled`, `active`, `done`, `failed` y `notSupported`.</span><span class="sxs-lookup"><span data-stu-id="36a23-161">Possible values are: `none`, `pending`, `canceled`, `active`, `done`, `failed`, `notSupported`.</span></span>|



## <a name="response"></a><span data-ttu-id="36a23-162">Respuesta</span><span class="sxs-lookup"><span data-stu-id="36a23-162">Response</span></span>
<span data-ttu-id="36a23-163">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto actualizado [remoteActionAudit](../resources/intune-devices-remoteactionaudit.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="36a23-163">If successful, this method returns a `200 OK` response code and an updated [remoteActionAudit](../resources/intune-devices-remoteactionaudit.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="36a23-164">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="36a23-164">Example</span></span>
### <a name="request"></a><span data-ttu-id="36a23-165">Solicitud</span><span class="sxs-lookup"><span data-stu-id="36a23-165">Request</span></span>
<span data-ttu-id="36a23-166">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="36a23-166">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/remoteActionAudits/{remoteActionAuditId}
Content-type: application/json
Content-length: 399

{
  "deviceDisplayName": "Device Display Name value",
  "userName": "User Name value",
  "initiatedByUserPrincipalName": "Initiated By User Principal Name value",
  "action": "factoryReset",
  "requestDateTime": "2017-01-01T00:03:07.1589002-08:00",
  "deviceOwnerUserPrincipalName": "Device Owner User Principal Name value",
  "deviceIMEI": "Device IMEI value",
  "actionState": "pending"
}
```

### <a name="response"></a><span data-ttu-id="36a23-167">Respuesta</span><span class="sxs-lookup"><span data-stu-id="36a23-167">Response</span></span>
<span data-ttu-id="36a23-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="36a23-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 504

{
  "@odata.type": "#microsoft.graph.remoteActionAudit",
  "id": "477f8d24-8d24-477f-248d-7f47248d7f47",
  "deviceDisplayName": "Device Display Name value",
  "userName": "User Name value",
  "initiatedByUserPrincipalName": "Initiated By User Principal Name value",
  "action": "factoryReset",
  "requestDateTime": "2017-01-01T00:03:07.1589002-08:00",
  "deviceOwnerUserPrincipalName": "Device Owner User Principal Name value",
  "deviceIMEI": "Device IMEI value",
  "actionState": "pending"
}
```





