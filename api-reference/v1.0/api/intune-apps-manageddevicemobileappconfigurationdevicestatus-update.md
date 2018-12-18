---
title: Actualizar managedDeviceMobileAppConfigurationDeviceStatus
description: Actualizar las propiedades de un objeto managedDeviceMobileAppConfigurationDeviceStatus.
author: tfitzmac
ms.openlocfilehash: 9891581e7692f3450340df3b25bebc503094a080
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27306611"
---
# <a name="update-manageddevicemobileappconfigurationdevicestatus"></a><span data-ttu-id="5f6a1-103">Actualizar managedDeviceMobileAppConfigurationDeviceStatus</span><span class="sxs-lookup"><span data-stu-id="5f6a1-103">Update managedDeviceMobileAppConfigurationDeviceStatus</span></span>

> <span data-ttu-id="5f6a1-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="5f6a1-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="5f6a1-105">Actualizar las propiedades de un objeto [managedDeviceMobileAppConfigurationDeviceStatus](../resources/intune-apps-manageddevicemobileappconfigurationdevicestatus.md) .</span><span class="sxs-lookup"><span data-stu-id="5f6a1-105">Update the properties of a [managedDeviceMobileAppConfigurationDeviceStatus](../resources/intune-apps-manageddevicemobileappconfigurationdevicestatus.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="5f6a1-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="5f6a1-106">Prerequisites</span></span>
<span data-ttu-id="5f6a1-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="5f6a1-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="5f6a1-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="5f6a1-109">Permission type</span></span>|<span data-ttu-id="5f6a1-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="5f6a1-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="5f6a1-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="5f6a1-111">Delegated (work or school account)</span></span>|<span data-ttu-id="5f6a1-112">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="5f6a1-112">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="5f6a1-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="5f6a1-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="5f6a1-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5f6a1-114">Not supported.</span></span>|
|<span data-ttu-id="5f6a1-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="5f6a1-115">Application</span></span>|<span data-ttu-id="5f6a1-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5f6a1-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="5f6a1-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="5f6a1-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/mobileAppConfigurations/{managedDeviceMobileAppConfigurationId}/deviceStatuses/{managedDeviceMobileAppConfigurationDeviceStatusId}
```

## <a name="request-headers"></a><span data-ttu-id="5f6a1-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="5f6a1-118">Request headers</span></span>
|<span data-ttu-id="5f6a1-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5f6a1-119">Header</span></span>|<span data-ttu-id="5f6a1-120">Valor</span><span class="sxs-lookup"><span data-stu-id="5f6a1-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="5f6a1-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="5f6a1-121">Authorization</span></span>|<span data-ttu-id="5f6a1-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="5f6a1-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="5f6a1-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="5f6a1-123">Accept</span></span>|<span data-ttu-id="5f6a1-124">application/json</span><span class="sxs-lookup"><span data-stu-id="5f6a1-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="5f6a1-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="5f6a1-125">Request body</span></span>
<span data-ttu-id="5f6a1-126">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto [managedDeviceMobileAppConfigurationDeviceStatus](../resources/intune-apps-manageddevicemobileappconfigurationdevicestatus.md) .</span><span class="sxs-lookup"><span data-stu-id="5f6a1-126">In the request body, supply a JSON representation for the [managedDeviceMobileAppConfigurationDeviceStatus](../resources/intune-apps-manageddevicemobileappconfigurationdevicestatus.md) object.</span></span>

<span data-ttu-id="5f6a1-127">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el [managedDeviceMobileAppConfigurationDeviceStatus](../resources/intune-apps-manageddevicemobileappconfigurationdevicestatus.md).</span><span class="sxs-lookup"><span data-stu-id="5f6a1-127">The following table shows the properties that are required when you create the [managedDeviceMobileAppConfigurationDeviceStatus](../resources/intune-apps-manageddevicemobileappconfigurationdevicestatus.md).</span></span>

|<span data-ttu-id="5f6a1-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="5f6a1-128">Property</span></span>|<span data-ttu-id="5f6a1-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="5f6a1-129">Type</span></span>|<span data-ttu-id="5f6a1-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="5f6a1-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="5f6a1-131">id</span><span class="sxs-lookup"><span data-stu-id="5f6a1-131">id</span></span>|<span data-ttu-id="5f6a1-132">String</span><span class="sxs-lookup"><span data-stu-id="5f6a1-132">String</span></span>|<span data-ttu-id="5f6a1-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="5f6a1-133">Key of the entity.</span></span>|
|<span data-ttu-id="5f6a1-134">deviceDisplayName</span><span class="sxs-lookup"><span data-stu-id="5f6a1-134">deviceDisplayName</span></span>|<span data-ttu-id="5f6a1-135">String</span><span class="sxs-lookup"><span data-stu-id="5f6a1-135">String</span></span>|<span data-ttu-id="5f6a1-136">Nombre de dispositivo de DevicePolicyStatus.</span><span class="sxs-lookup"><span data-stu-id="5f6a1-136">Device name of the DevicePolicyStatus.</span></span>|
|<span data-ttu-id="5f6a1-137">userName</span><span class="sxs-lookup"><span data-stu-id="5f6a1-137">userName</span></span>|<span data-ttu-id="5f6a1-138">String</span><span class="sxs-lookup"><span data-stu-id="5f6a1-138">String</span></span>|<span data-ttu-id="5f6a1-139">El nombre de usuario que se está notificando</span><span class="sxs-lookup"><span data-stu-id="5f6a1-139">The User Name that is being reported</span></span>|
|<span data-ttu-id="5f6a1-140">deviceModel</span><span class="sxs-lookup"><span data-stu-id="5f6a1-140">deviceModel</span></span>|<span data-ttu-id="5f6a1-141">String</span><span class="sxs-lookup"><span data-stu-id="5f6a1-141">String</span></span>|<span data-ttu-id="5f6a1-142">El modelo de dispositivo que se está notificando</span><span class="sxs-lookup"><span data-stu-id="5f6a1-142">The device model that is being reported</span></span>|
|<span data-ttu-id="5f6a1-143">complianceGracePeriodExpirationDateTime</span><span class="sxs-lookup"><span data-stu-id="5f6a1-143">complianceGracePeriodExpirationDateTime</span></span>|<span data-ttu-id="5f6a1-144">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="5f6a1-144">DateTimeOffset</span></span>|<span data-ttu-id="5f6a1-145">La fecha y hora en que expira el período de gracia de cumplimiento del dispositivo</span><span class="sxs-lookup"><span data-stu-id="5f6a1-145">The DateTime when device compliance grace period expires</span></span>|
|<span data-ttu-id="5f6a1-146">status</span><span class="sxs-lookup"><span data-stu-id="5f6a1-146">status</span></span>|[<span data-ttu-id="5f6a1-147">complianceStatus</span><span class="sxs-lookup"><span data-stu-id="5f6a1-147">complianceStatus</span></span>](../resources/intune-shared-compliancestatus.md)|<span data-ttu-id="5f6a1-148">Estado de cumplimiento del informe de directiva.</span><span class="sxs-lookup"><span data-stu-id="5f6a1-148">Compliance status of the policy report.</span></span> <span data-ttu-id="5f6a1-149">Los valores posibles son: `unknown`, `notApplicable`, `compliant`, `remediated`, `nonCompliant`, `error`, `conflict` y `notAssigned`.</span><span class="sxs-lookup"><span data-stu-id="5f6a1-149">Possible values are: `unknown`, `notApplicable`, `compliant`, `remediated`, `nonCompliant`, `error`, `conflict`, `notAssigned`.</span></span>|
|<span data-ttu-id="5f6a1-150">lastReportedDateTime</span><span class="sxs-lookup"><span data-stu-id="5f6a1-150">lastReportedDateTime</span></span>|<span data-ttu-id="5f6a1-151">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="5f6a1-151">DateTimeOffset</span></span>|<span data-ttu-id="5f6a1-152">Fecha y hora de la última modificación del informe de directiva.</span><span class="sxs-lookup"><span data-stu-id="5f6a1-152">Last modified date time of the policy report.</span></span>|
|<span data-ttu-id="5f6a1-153">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="5f6a1-153">userPrincipalName</span></span>|<span data-ttu-id="5f6a1-154">String</span><span class="sxs-lookup"><span data-stu-id="5f6a1-154">String</span></span>|<span data-ttu-id="5f6a1-155">UserPrincipalName.</span><span class="sxs-lookup"><span data-stu-id="5f6a1-155">UserPrincipalName.</span></span>|



## <a name="response"></a><span data-ttu-id="5f6a1-156">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5f6a1-156">Response</span></span>
<span data-ttu-id="5f6a1-157">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto actualizado [managedDeviceMobileAppConfigurationDeviceStatus](../resources/intune-apps-manageddevicemobileappconfigurationdevicestatus.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5f6a1-157">If successful, this method returns a `200 OK` response code and an updated [managedDeviceMobileAppConfigurationDeviceStatus](../resources/intune-apps-manageddevicemobileappconfigurationdevicestatus.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="5f6a1-158">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="5f6a1-158">Example</span></span>
### <a name="request"></a><span data-ttu-id="5f6a1-159">Solicitud</span><span class="sxs-lookup"><span data-stu-id="5f6a1-159">Request</span></span>
<span data-ttu-id="5f6a1-160">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="5f6a1-160">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceAppManagement/mobileAppConfigurations/{managedDeviceMobileAppConfigurationId}/deviceStatuses/{managedDeviceMobileAppConfigurationDeviceStatusId}
Content-type: application/json
Content-length: 445

{
  "@odata.type": "#microsoft.graph.managedDeviceMobileAppConfigurationDeviceStatus",
  "deviceDisplayName": "Device Display Name value",
  "userName": "User Name value",
  "deviceModel": "Device Model value",
  "complianceGracePeriodExpirationDateTime": "2016-12-31T23:56:44.951111-08:00",
  "status": "notApplicable",
  "lastReportedDateTime": "2017-01-01T00:00:17.7769392-08:00",
  "userPrincipalName": "User Principal Name value"
}
```

### <a name="response"></a><span data-ttu-id="5f6a1-161">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5f6a1-161">Response</span></span>
<span data-ttu-id="5f6a1-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="5f6a1-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 494

{
  "@odata.type": "#microsoft.graph.managedDeviceMobileAppConfigurationDeviceStatus",
  "id": "477d3651-3651-477d-5136-7d4751367d47",
  "deviceDisplayName": "Device Display Name value",
  "userName": "User Name value",
  "deviceModel": "Device Model value",
  "complianceGracePeriodExpirationDateTime": "2016-12-31T23:56:44.951111-08:00",
  "status": "notApplicable",
  "lastReportedDateTime": "2017-01-01T00:00:17.7769392-08:00",
  "userPrincipalName": "User Principal Name value"
}
```



