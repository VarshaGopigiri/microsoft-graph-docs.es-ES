---
title: Actualizar restrictedAppsViolation
description: Actualizar las propiedades de un objeto restrictedAppsViolation.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 4c3d1f8b43bd3f17f2e6f92427d7e06295a808e5
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27950084"
---
# <a name="update-restrictedappsviolation"></a><span data-ttu-id="0e08d-103">Actualizar restrictedAppsViolation</span><span class="sxs-lookup"><span data-stu-id="0e08d-103">Update restrictedAppsViolation</span></span>

> <span data-ttu-id="0e08d-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="0e08d-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="0e08d-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="0e08d-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="0e08d-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="0e08d-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="0e08d-107">Actualizar las propiedades de un objeto [restrictedAppsViolation](../resources/intune-deviceconfig-restrictedappsviolation.md) .</span><span class="sxs-lookup"><span data-stu-id="0e08d-107">Update the properties of a [restrictedAppsViolation](../resources/intune-deviceconfig-restrictedappsviolation.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="0e08d-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="0e08d-108">Prerequisites</span></span>
<span data-ttu-id="0e08d-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="0e08d-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="0e08d-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="0e08d-111">Permission type</span></span>|<span data-ttu-id="0e08d-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="0e08d-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="0e08d-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="0e08d-113">Delegated (work or school account)</span></span>|<span data-ttu-id="0e08d-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="0e08d-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="0e08d-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="0e08d-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="0e08d-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="0e08d-116">Not supported.</span></span>|
|<span data-ttu-id="0e08d-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="0e08d-117">Application</span></span>|<span data-ttu-id="0e08d-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="0e08d-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="0e08d-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="0e08d-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceConfigurationRestrictedAppsViolations/{restrictedAppsViolationId}
```

## <a name="request-headers"></a><span data-ttu-id="0e08d-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="0e08d-120">Request headers</span></span>
|<span data-ttu-id="0e08d-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0e08d-121">Header</span></span>|<span data-ttu-id="0e08d-122">Valor</span><span class="sxs-lookup"><span data-stu-id="0e08d-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="0e08d-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="0e08d-123">Authorization</span></span>|<span data-ttu-id="0e08d-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="0e08d-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="0e08d-125">Accept</span><span class="sxs-lookup"><span data-stu-id="0e08d-125">Accept</span></span>|<span data-ttu-id="0e08d-126">application/json</span><span class="sxs-lookup"><span data-stu-id="0e08d-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="0e08d-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="0e08d-127">Request body</span></span>
<span data-ttu-id="0e08d-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto [restrictedAppsViolation](../resources/intune-deviceconfig-restrictedappsviolation.md) .</span><span class="sxs-lookup"><span data-stu-id="0e08d-128">In the request body, supply a JSON representation for the [restrictedAppsViolation](../resources/intune-deviceconfig-restrictedappsviolation.md) object.</span></span>

<span data-ttu-id="0e08d-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el [restrictedAppsViolation](../resources/intune-deviceconfig-restrictedappsviolation.md).</span><span class="sxs-lookup"><span data-stu-id="0e08d-129">The following table shows the properties that are required when you create the [restrictedAppsViolation](../resources/intune-deviceconfig-restrictedappsviolation.md).</span></span>

|<span data-ttu-id="0e08d-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="0e08d-130">Property</span></span>|<span data-ttu-id="0e08d-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="0e08d-131">Type</span></span>|<span data-ttu-id="0e08d-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="0e08d-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="0e08d-133">id</span><span class="sxs-lookup"><span data-stu-id="0e08d-133">id</span></span>|<span data-ttu-id="0e08d-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="0e08d-134">String</span></span>|<span data-ttu-id="0e08d-135">Identificador único para el objeto.</span><span class="sxs-lookup"><span data-stu-id="0e08d-135">Unique identifier for the object.</span></span> <span data-ttu-id="0e08d-136">Creados a partir de accountId, deviceId, Id. de directiva y userId</span><span class="sxs-lookup"><span data-stu-id="0e08d-136">Composed from accountId, deviceId, policyId and userId</span></span>|
|<span data-ttu-id="0e08d-137">userId</span><span class="sxs-lookup"><span data-stu-id="0e08d-137">userId</span></span>|<span data-ttu-id="0e08d-138">Cadena</span><span class="sxs-lookup"><span data-stu-id="0e08d-138">String</span></span>|<span data-ttu-id="0e08d-139">Identificador único del usuario, debe ser el Guid</span><span class="sxs-lookup"><span data-stu-id="0e08d-139">User unique identifier, must be Guid</span></span>|
|<span data-ttu-id="0e08d-140">userName</span><span class="sxs-lookup"><span data-stu-id="0e08d-140">userName</span></span>|<span data-ttu-id="0e08d-141">Cadena</span><span class="sxs-lookup"><span data-stu-id="0e08d-141">String</span></span>|<span data-ttu-id="0e08d-142">Nombre de usuario</span><span class="sxs-lookup"><span data-stu-id="0e08d-142">User name</span></span>|
|<span data-ttu-id="0e08d-143">managedDeviceId</span><span class="sxs-lookup"><span data-stu-id="0e08d-143">managedDeviceId</span></span>|<span data-ttu-id="0e08d-144">Cadena</span><span class="sxs-lookup"><span data-stu-id="0e08d-144">String</span></span>|<span data-ttu-id="0e08d-145">Identificador único de dispositivos administrados, debe ser el Guid</span><span class="sxs-lookup"><span data-stu-id="0e08d-145">Managed device unique identifier, must be Guid</span></span>|
|<span data-ttu-id="0e08d-146">deviceName</span><span class="sxs-lookup"><span data-stu-id="0e08d-146">deviceName</span></span>|<span data-ttu-id="0e08d-147">Cadena</span><span class="sxs-lookup"><span data-stu-id="0e08d-147">String</span></span>|<span data-ttu-id="0e08d-148">Nombre de dispositivo</span><span class="sxs-lookup"><span data-stu-id="0e08d-148">Device name</span></span>|
|<span data-ttu-id="0e08d-149">deviceConfigurationId</span><span class="sxs-lookup"><span data-stu-id="0e08d-149">deviceConfigurationId</span></span>|<span data-ttu-id="0e08d-150">Cadena</span><span class="sxs-lookup"><span data-stu-id="0e08d-150">String</span></span>|<span data-ttu-id="0e08d-151">Identificador único de dispositivo configuración perfil, debe ser el Guid</span><span class="sxs-lookup"><span data-stu-id="0e08d-151">Device configuration profile unique identifier, must be Guid</span></span>|
|<span data-ttu-id="0e08d-152">deviceConfigurationName</span><span class="sxs-lookup"><span data-stu-id="0e08d-152">deviceConfigurationName</span></span>|<span data-ttu-id="0e08d-153">Cadena</span><span class="sxs-lookup"><span data-stu-id="0e08d-153">String</span></span>|<span data-ttu-id="0e08d-154">Nombre del perfil de configuración de dispositivo</span><span class="sxs-lookup"><span data-stu-id="0e08d-154">Device configuration profile name</span></span>|
|<span data-ttu-id="0e08d-155">platformType</span><span class="sxs-lookup"><span data-stu-id="0e08d-155">platformType</span></span>|[<span data-ttu-id="0e08d-156">policyPlatformType</span><span class="sxs-lookup"><span data-stu-id="0e08d-156">policyPlatformType</span></span>](../resources/intune-deviceconfig-policyplatformtype.md)|<span data-ttu-id="0e08d-157">Tipo de plataforma.</span><span class="sxs-lookup"><span data-stu-id="0e08d-157">Platform type.</span></span> <span data-ttu-id="0e08d-158">Los valores posibles son: `android`, `androidForWork`, `iOS`, `macOS`, `windowsPhone81`, `windows81AndLater`, `windows10AndLater`, `androidWorkProfile` y `all`.</span><span class="sxs-lookup"><span data-stu-id="0e08d-158">Possible values are: `android`, `androidForWork`, `iOS`, `macOS`, `windowsPhone81`, `windows81AndLater`, `windows10AndLater`, `androidWorkProfile`, `all`.</span></span>|
|<span data-ttu-id="0e08d-159">restrictedAppsState</span><span class="sxs-lookup"><span data-stu-id="0e08d-159">restrictedAppsState</span></span>|[<span data-ttu-id="0e08d-160">restrictedAppsState</span><span class="sxs-lookup"><span data-stu-id="0e08d-160">restrictedAppsState</span></span>](../resources/intune-deviceconfig-restrictedappsstate.md)|<span data-ttu-id="0e08d-161">Estado de aplicaciones restringidos.</span><span class="sxs-lookup"><span data-stu-id="0e08d-161">Restricted apps state.</span></span> <span data-ttu-id="0e08d-162">Los valores posibles son: `prohibitedApps` y `notApprovedApps`.</span><span class="sxs-lookup"><span data-stu-id="0e08d-162">Possible values are: `prohibitedApps`, `notApprovedApps`.</span></span>|
|<span data-ttu-id="0e08d-163">restrictedApps</span><span class="sxs-lookup"><span data-stu-id="0e08d-163">restrictedApps</span></span>|<span data-ttu-id="0e08d-164">colección de [managedDeviceReportedApp](../resources/intune-deviceconfig-manageddevicereportedapp.md)</span><span class="sxs-lookup"><span data-stu-id="0e08d-164">[managedDeviceReportedApp](../resources/intune-deviceconfig-manageddevicereportedapp.md) collection</span></span>|<span data-ttu-id="0e08d-165">Lista de aplicaciones restringidas infringidas</span><span class="sxs-lookup"><span data-stu-id="0e08d-165">List of violated restricted apps</span></span>|



## <a name="response"></a><span data-ttu-id="0e08d-166">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0e08d-166">Response</span></span>
<span data-ttu-id="0e08d-167">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto actualizado [restrictedAppsViolation](../resources/intune-deviceconfig-restrictedappsviolation.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0e08d-167">If successful, this method returns a `200 OK` response code and an updated [restrictedAppsViolation](../resources/intune-deviceconfig-restrictedappsviolation.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="0e08d-168">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="0e08d-168">Example</span></span>
### <a name="request"></a><span data-ttu-id="0e08d-169">Solicitud</span><span class="sxs-lookup"><span data-stu-id="0e08d-169">Request</span></span>
<span data-ttu-id="0e08d-170">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="0e08d-170">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/deviceConfigurationRestrictedAppsViolations/{restrictedAppsViolationId}
Content-type: application/json
Content-length: 502

{
  "userId": "User Id value",
  "userName": "User Name value",
  "managedDeviceId": "Managed Device Id value",
  "deviceName": "Device Name value",
  "deviceConfigurationId": "Device Configuration Id value",
  "deviceConfigurationName": "Device Configuration Name value",
  "platformType": "androidForWork",
  "restrictedAppsState": "notApprovedApps",
  "restrictedApps": [
    {
      "@odata.type": "microsoft.graph.managedDeviceReportedApp",
      "appId": "App Id value"
    }
  ]
}
```

### <a name="response"></a><span data-ttu-id="0e08d-171">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0e08d-171">Response</span></span>
<span data-ttu-id="0e08d-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="0e08d-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 613

{
  "@odata.type": "#microsoft.graph.restrictedAppsViolation",
  "id": "53f99903-9903-53f9-0399-f9530399f953",
  "userId": "User Id value",
  "userName": "User Name value",
  "managedDeviceId": "Managed Device Id value",
  "deviceName": "Device Name value",
  "deviceConfigurationId": "Device Configuration Id value",
  "deviceConfigurationName": "Device Configuration Name value",
  "platformType": "androidForWork",
  "restrictedAppsState": "notApprovedApps",
  "restrictedApps": [
    {
      "@odata.type": "microsoft.graph.managedDeviceReportedApp",
      "appId": "App Id value"
    }
  ]
}
```





