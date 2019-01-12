---
title: Crear managedDeviceMobileAppConfigurationDeviceStatus
description: Crear un nuevo objeto managedDeviceMobileAppConfigurationDeviceStatus.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 285b2ea8b5721a342f2f383ca160c64fdc931ab8
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27920999"
---
# <a name="create-manageddevicemobileappconfigurationdevicestatus"></a><span data-ttu-id="ea6f4-103">Crear managedDeviceMobileAppConfigurationDeviceStatus</span><span class="sxs-lookup"><span data-stu-id="ea6f4-103">Create managedDeviceMobileAppConfigurationDeviceStatus</span></span>

> <span data-ttu-id="ea6f4-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="ea6f4-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="ea6f4-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="ea6f4-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="ea6f4-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="ea6f4-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="ea6f4-107">Crear un nuevo objeto [managedDeviceMobileAppConfigurationDeviceStatus](../resources/intune-apps-manageddevicemobileappconfigurationdevicestatus.md) .</span><span class="sxs-lookup"><span data-stu-id="ea6f4-107">Create a new [managedDeviceMobileAppConfigurationDeviceStatus](../resources/intune-apps-manageddevicemobileappconfigurationdevicestatus.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="ea6f4-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="ea6f4-108">Prerequisites</span></span>
<span data-ttu-id="ea6f4-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="ea6f4-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="ea6f4-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ea6f4-111">Permission type</span></span>|<span data-ttu-id="ea6f4-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ea6f4-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="ea6f4-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ea6f4-113">Delegated (work or school account)</span></span>|<span data-ttu-id="ea6f4-114">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ea6f4-114">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="ea6f4-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ea6f4-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="ea6f4-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ea6f4-116">Not supported.</span></span>|
|<span data-ttu-id="ea6f4-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ea6f4-117">Application</span></span>|<span data-ttu-id="ea6f4-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ea6f4-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="ea6f4-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ea6f4-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/mobileAppConfigurations/{managedDeviceMobileAppConfigurationId}/deviceStatuses
POST /deviceAppManagement/iosLobAppProvisioningConfigurations/{iosLobAppProvisioningConfigurationId}/deviceStatuses
```

## <a name="request-headers"></a><span data-ttu-id="ea6f4-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ea6f4-120">Request headers</span></span>
|<span data-ttu-id="ea6f4-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ea6f4-121">Header</span></span>|<span data-ttu-id="ea6f4-122">Valor</span><span class="sxs-lookup"><span data-stu-id="ea6f4-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="ea6f4-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="ea6f4-123">Authorization</span></span>|<span data-ttu-id="ea6f4-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="ea6f4-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="ea6f4-125">Accept</span><span class="sxs-lookup"><span data-stu-id="ea6f4-125">Accept</span></span>|<span data-ttu-id="ea6f4-126">application/json</span><span class="sxs-lookup"><span data-stu-id="ea6f4-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="ea6f4-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ea6f4-127">Request body</span></span>
<span data-ttu-id="ea6f4-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto managedDeviceMobileAppConfigurationDeviceStatus.</span><span class="sxs-lookup"><span data-stu-id="ea6f4-128">In the request body, supply a JSON representation for the managedDeviceMobileAppConfigurationDeviceStatus object.</span></span>

<span data-ttu-id="ea6f4-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el managedDeviceMobileAppConfigurationDeviceStatus.</span><span class="sxs-lookup"><span data-stu-id="ea6f4-129">The following table shows the properties that are required when you create the managedDeviceMobileAppConfigurationDeviceStatus.</span></span>

|<span data-ttu-id="ea6f4-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ea6f4-130">Property</span></span>|<span data-ttu-id="ea6f4-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="ea6f4-131">Type</span></span>|<span data-ttu-id="ea6f4-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="ea6f4-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="ea6f4-133">id</span><span class="sxs-lookup"><span data-stu-id="ea6f4-133">id</span></span>|<span data-ttu-id="ea6f4-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="ea6f4-134">String</span></span>|<span data-ttu-id="ea6f4-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="ea6f4-135">Key of the entity.</span></span>|
|<span data-ttu-id="ea6f4-136">deviceDisplayName</span><span class="sxs-lookup"><span data-stu-id="ea6f4-136">deviceDisplayName</span></span>|<span data-ttu-id="ea6f4-137">String</span><span class="sxs-lookup"><span data-stu-id="ea6f4-137">String</span></span>|<span data-ttu-id="ea6f4-138">Nombre de dispositivo de DevicePolicyStatus.</span><span class="sxs-lookup"><span data-stu-id="ea6f4-138">Device name of the DevicePolicyStatus.</span></span>|
|<span data-ttu-id="ea6f4-139">userName</span><span class="sxs-lookup"><span data-stu-id="ea6f4-139">userName</span></span>|<span data-ttu-id="ea6f4-140">Cadena</span><span class="sxs-lookup"><span data-stu-id="ea6f4-140">String</span></span>|<span data-ttu-id="ea6f4-141">El nombre de usuario que se está notificando</span><span class="sxs-lookup"><span data-stu-id="ea6f4-141">The User Name that is being reported</span></span>|
|<span data-ttu-id="ea6f4-142">deviceModel</span><span class="sxs-lookup"><span data-stu-id="ea6f4-142">deviceModel</span></span>|<span data-ttu-id="ea6f4-143">Cadena</span><span class="sxs-lookup"><span data-stu-id="ea6f4-143">String</span></span>|<span data-ttu-id="ea6f4-144">El modelo de dispositivo que se está notificando</span><span class="sxs-lookup"><span data-stu-id="ea6f4-144">The device model that is being reported</span></span>|
|<span data-ttu-id="ea6f4-145">platform</span><span class="sxs-lookup"><span data-stu-id="ea6f4-145">platform</span></span>|<span data-ttu-id="ea6f4-146">Int32</span><span class="sxs-lookup"><span data-stu-id="ea6f4-146">Int32</span></span>|<span data-ttu-id="ea6f4-147">Plataforma del dispositivo que se notifica</span><span class="sxs-lookup"><span data-stu-id="ea6f4-147">Platform of the device that is being reported</span></span>|
|<span data-ttu-id="ea6f4-148">complianceGracePeriodExpirationDateTime</span><span class="sxs-lookup"><span data-stu-id="ea6f4-148">complianceGracePeriodExpirationDateTime</span></span>|<span data-ttu-id="ea6f4-149">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="ea6f4-149">DateTimeOffset</span></span>|<span data-ttu-id="ea6f4-150">La fecha y hora en que expira el período de gracia de cumplimiento del dispositivo</span><span class="sxs-lookup"><span data-stu-id="ea6f4-150">The DateTime when device compliance grace period expires</span></span>|
|<span data-ttu-id="ea6f4-151">status</span><span class="sxs-lookup"><span data-stu-id="ea6f4-151">status</span></span>|[<span data-ttu-id="ea6f4-152">complianceStatus</span><span class="sxs-lookup"><span data-stu-id="ea6f4-152">complianceStatus</span></span>](../resources/intune-shared-compliancestatus.md)|<span data-ttu-id="ea6f4-153">Estado de cumplimiento del informe de directiva.</span><span class="sxs-lookup"><span data-stu-id="ea6f4-153">Compliance status of the policy report.</span></span> <span data-ttu-id="ea6f4-154">Los valores posibles son: `unknown`, `notApplicable`, `compliant`, `remediated`, `nonCompliant`, `error`, `conflict` y `notAssigned`.</span><span class="sxs-lookup"><span data-stu-id="ea6f4-154">Possible values are: `unknown`, `notApplicable`, `compliant`, `remediated`, `nonCompliant`, `error`, `conflict`, `notAssigned`.</span></span>|
|<span data-ttu-id="ea6f4-155">lastReportedDateTime</span><span class="sxs-lookup"><span data-stu-id="ea6f4-155">lastReportedDateTime</span></span>|<span data-ttu-id="ea6f4-156">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="ea6f4-156">DateTimeOffset</span></span>|<span data-ttu-id="ea6f4-157">Fecha y hora de la última modificación del informe de directiva.</span><span class="sxs-lookup"><span data-stu-id="ea6f4-157">Last modified date time of the policy report.</span></span>|
|<span data-ttu-id="ea6f4-158">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="ea6f4-158">userPrincipalName</span></span>|<span data-ttu-id="ea6f4-159">Cadena</span><span class="sxs-lookup"><span data-stu-id="ea6f4-159">String</span></span>|<span data-ttu-id="ea6f4-160">UserPrincipalName.</span><span class="sxs-lookup"><span data-stu-id="ea6f4-160">UserPrincipalName.</span></span>|



## <a name="response"></a><span data-ttu-id="ea6f4-161">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ea6f4-161">Response</span></span>
<span data-ttu-id="ea6f4-162">Si tiene éxito, este método devuelve una `201 Created` código de respuesta y un objeto [managedDeviceMobileAppConfigurationDeviceStatus](../resources/intune-apps-manageddevicemobileappconfigurationdevicestatus.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ea6f4-162">If successful, this method returns a `201 Created` response code and a [managedDeviceMobileAppConfigurationDeviceStatus](../resources/intune-apps-manageddevicemobileappconfigurationdevicestatus.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="ea6f4-163">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ea6f4-163">Example</span></span>
### <a name="request"></a><span data-ttu-id="ea6f4-164">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ea6f4-164">Request</span></span>
<span data-ttu-id="ea6f4-165">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ea6f4-165">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceAppManagement/mobileAppConfigurations/{managedDeviceMobileAppConfigurationId}/deviceStatuses
Content-type: application/json
Content-length: 463

{
  "@odata.type": "#microsoft.graph.managedDeviceMobileAppConfigurationDeviceStatus",
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

### <a name="response"></a><span data-ttu-id="ea6f4-166">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ea6f4-166">Response</span></span>
<span data-ttu-id="ea6f4-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="ea6f4-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 512

{
  "@odata.type": "#microsoft.graph.managedDeviceMobileAppConfigurationDeviceStatus",
  "id": "477d3651-3651-477d-5136-7d4751367d47",
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





