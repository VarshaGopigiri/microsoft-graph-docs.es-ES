---
title: Crear deviceConfigurationDeviceStatus
description: Cree un objeto deviceConfigurationDeviceStatus.
author: tfitzmac
ms.openlocfilehash: 05e8280d7b4bda79feef9cd6f5055f00ee783822
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27306548"
---
# <a name="create-deviceconfigurationdevicestatus"></a><span data-ttu-id="ca3eb-103">Crear deviceConfigurationDeviceStatus</span><span class="sxs-lookup"><span data-stu-id="ca3eb-103">Create deviceConfigurationDeviceStatus</span></span>

> <span data-ttu-id="ca3eb-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="ca3eb-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="ca3eb-105">Cree un objeto [deviceConfigurationDeviceStatus](../resources/intune-deviceconfig-deviceconfigurationdevicestatus.md).</span><span class="sxs-lookup"><span data-stu-id="ca3eb-105">Create a new [deviceConfigurationDeviceStatus](../resources/intune-deviceconfig-deviceconfigurationdevicestatus.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="ca3eb-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="ca3eb-106">Prerequisites</span></span>
<span data-ttu-id="ca3eb-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="ca3eb-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="ca3eb-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ca3eb-109">Permission type</span></span>|<span data-ttu-id="ca3eb-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ca3eb-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="ca3eb-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ca3eb-111">Delegated (work or school account)</span></span>|<span data-ttu-id="ca3eb-112">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ca3eb-112">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="ca3eb-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ca3eb-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="ca3eb-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ca3eb-114">Not supported.</span></span>|
|<span data-ttu-id="ca3eb-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ca3eb-115">Application</span></span>|<span data-ttu-id="ca3eb-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ca3eb-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="ca3eb-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ca3eb-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceConfigurations/{deviceConfigurationId}/deviceStatuses
```

## <a name="request-headers"></a><span data-ttu-id="ca3eb-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ca3eb-118">Request headers</span></span>
|<span data-ttu-id="ca3eb-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ca3eb-119">Header</span></span>|<span data-ttu-id="ca3eb-120">Valor</span><span class="sxs-lookup"><span data-stu-id="ca3eb-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="ca3eb-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="ca3eb-121">Authorization</span></span>|<span data-ttu-id="ca3eb-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="ca3eb-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="ca3eb-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="ca3eb-123">Accept</span></span>|<span data-ttu-id="ca3eb-124">application/json</span><span class="sxs-lookup"><span data-stu-id="ca3eb-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="ca3eb-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ca3eb-125">Request body</span></span>
<span data-ttu-id="ca3eb-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto deviceConfigurationDeviceStatus.</span><span class="sxs-lookup"><span data-stu-id="ca3eb-126">In the request body, supply a JSON representation for the deviceConfigurationDeviceStatus object.</span></span>

<span data-ttu-id="ca3eb-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto deviceConfigurationDeviceStatus.</span><span class="sxs-lookup"><span data-stu-id="ca3eb-127">The following table shows the properties that are required when you create the deviceConfigurationDeviceStatus.</span></span>

|<span data-ttu-id="ca3eb-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ca3eb-128">Property</span></span>|<span data-ttu-id="ca3eb-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="ca3eb-129">Type</span></span>|<span data-ttu-id="ca3eb-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="ca3eb-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="ca3eb-131">id</span><span class="sxs-lookup"><span data-stu-id="ca3eb-131">id</span></span>|<span data-ttu-id="ca3eb-132">String</span><span class="sxs-lookup"><span data-stu-id="ca3eb-132">String</span></span>|<span data-ttu-id="ca3eb-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="ca3eb-133">Key of the entity.</span></span>|
|<span data-ttu-id="ca3eb-134">deviceDisplayName</span><span class="sxs-lookup"><span data-stu-id="ca3eb-134">deviceDisplayName</span></span>|<span data-ttu-id="ca3eb-135">String</span><span class="sxs-lookup"><span data-stu-id="ca3eb-135">String</span></span>|<span data-ttu-id="ca3eb-136">Nombre de dispositivo de DevicePolicyStatus.</span><span class="sxs-lookup"><span data-stu-id="ca3eb-136">Device name of the DevicePolicyStatus.</span></span>|
|<span data-ttu-id="ca3eb-137">userName</span><span class="sxs-lookup"><span data-stu-id="ca3eb-137">userName</span></span>|<span data-ttu-id="ca3eb-138">String</span><span class="sxs-lookup"><span data-stu-id="ca3eb-138">String</span></span>|<span data-ttu-id="ca3eb-139">El nombre de usuario que se está notificando</span><span class="sxs-lookup"><span data-stu-id="ca3eb-139">The User Name that is being reported</span></span>|
|<span data-ttu-id="ca3eb-140">deviceModel</span><span class="sxs-lookup"><span data-stu-id="ca3eb-140">deviceModel</span></span>|<span data-ttu-id="ca3eb-141">String</span><span class="sxs-lookup"><span data-stu-id="ca3eb-141">String</span></span>|<span data-ttu-id="ca3eb-142">El modelo de dispositivo que se está notificando</span><span class="sxs-lookup"><span data-stu-id="ca3eb-142">The device model that is being reported</span></span>|
|<span data-ttu-id="ca3eb-143">complianceGracePeriodExpirationDateTime</span><span class="sxs-lookup"><span data-stu-id="ca3eb-143">complianceGracePeriodExpirationDateTime</span></span>|<span data-ttu-id="ca3eb-144">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="ca3eb-144">DateTimeOffset</span></span>|<span data-ttu-id="ca3eb-145">La fecha y hora en que expira el período de gracia de cumplimiento del dispositivo</span><span class="sxs-lookup"><span data-stu-id="ca3eb-145">The DateTime when device compliance grace period expires</span></span>|
|<span data-ttu-id="ca3eb-146">status</span><span class="sxs-lookup"><span data-stu-id="ca3eb-146">status</span></span>|[<span data-ttu-id="ca3eb-147">complianceStatus</span><span class="sxs-lookup"><span data-stu-id="ca3eb-147">complianceStatus</span></span>](../resources/intune-shared-compliancestatus.md)|<span data-ttu-id="ca3eb-148">Estado de cumplimiento del informe de directiva.</span><span class="sxs-lookup"><span data-stu-id="ca3eb-148">Compliance status of the policy report.</span></span> <span data-ttu-id="ca3eb-149">Los valores posibles son: `unknown`, `notApplicable`, `compliant`, `remediated`, `nonCompliant`, `error`, `conflict` y `notAssigned`.</span><span class="sxs-lookup"><span data-stu-id="ca3eb-149">Possible values are: `unknown`, `notApplicable`, `compliant`, `remediated`, `nonCompliant`, `error`, `conflict`, `notAssigned`.</span></span>|
|<span data-ttu-id="ca3eb-150">lastReportedDateTime</span><span class="sxs-lookup"><span data-stu-id="ca3eb-150">lastReportedDateTime</span></span>|<span data-ttu-id="ca3eb-151">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="ca3eb-151">DateTimeOffset</span></span>|<span data-ttu-id="ca3eb-152">Fecha y hora de la última modificación del informe de directiva.</span><span class="sxs-lookup"><span data-stu-id="ca3eb-152">Last modified date time of the policy report.</span></span>|
|<span data-ttu-id="ca3eb-153">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="ca3eb-153">userPrincipalName</span></span>|<span data-ttu-id="ca3eb-154">String</span><span class="sxs-lookup"><span data-stu-id="ca3eb-154">String</span></span>|<span data-ttu-id="ca3eb-155">UserPrincipalName.</span><span class="sxs-lookup"><span data-stu-id="ca3eb-155">UserPrincipalName.</span></span>|



## <a name="response"></a><span data-ttu-id="ca3eb-156">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ca3eb-156">Response</span></span>
<span data-ttu-id="ca3eb-157">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [deviceConfigurationDeviceStatus](../resources/intune-deviceconfig-deviceconfigurationdevicestatus.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ca3eb-157">If successful, this method returns a `201 Created` response code and a [deviceConfigurationDeviceStatus](../resources/intune-deviceconfig-deviceconfigurationdevicestatus.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="ca3eb-158">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ca3eb-158">Example</span></span>
### <a name="request"></a><span data-ttu-id="ca3eb-159">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ca3eb-159">Request</span></span>
<span data-ttu-id="ca3eb-160">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ca3eb-160">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceManagement/deviceConfigurations/{deviceConfigurationId}/deviceStatuses
Content-type: application/json
Content-length: 429

{
  "@odata.type": "#microsoft.graph.deviceConfigurationDeviceStatus",
  "deviceDisplayName": "Device Display Name value",
  "userName": "User Name value",
  "deviceModel": "Device Model value",
  "complianceGracePeriodExpirationDateTime": "2016-12-31T23:56:44.951111-08:00",
  "status": "notApplicable",
  "lastReportedDateTime": "2017-01-01T00:00:17.7769392-08:00",
  "userPrincipalName": "User Principal Name value"
}
```

### <a name="response"></a><span data-ttu-id="ca3eb-161">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ca3eb-161">Response</span></span>
<span data-ttu-id="ca3eb-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="ca3eb-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 478

{
  "@odata.type": "#microsoft.graph.deviceConfigurationDeviceStatus",
  "id": "674e98e5-98e5-674e-e598-4e67e5984e67",
  "deviceDisplayName": "Device Display Name value",
  "userName": "User Name value",
  "deviceModel": "Device Model value",
  "complianceGracePeriodExpirationDateTime": "2016-12-31T23:56:44.951111-08:00",
  "status": "notApplicable",
  "lastReportedDateTime": "2017-01-01T00:00:17.7769392-08:00",
  "userPrincipalName": "User Principal Name value"
}
```



