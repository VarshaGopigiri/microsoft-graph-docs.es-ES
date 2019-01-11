---
title: Crear restrictedAppsViolation
description: Crear un nuevo objeto restrictedAppsViolation.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: b608a831427169215da9df4631f4562989105a2a
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27818126"
---
# <a name="create-restrictedappsviolation"></a><span data-ttu-id="9818f-103">Crear restrictedAppsViolation</span><span class="sxs-lookup"><span data-stu-id="9818f-103">Create restrictedAppsViolation</span></span>

> <span data-ttu-id="9818f-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="9818f-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="9818f-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="9818f-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="9818f-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="9818f-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="9818f-107">Crear un nuevo objeto [restrictedAppsViolation](../resources/intune-deviceconfig-restrictedappsviolation.md) .</span><span class="sxs-lookup"><span data-stu-id="9818f-107">Create a new [restrictedAppsViolation](../resources/intune-deviceconfig-restrictedappsviolation.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="9818f-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="9818f-108">Prerequisites</span></span>
<span data-ttu-id="9818f-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="9818f-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="9818f-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="9818f-111">Permission type</span></span>|<span data-ttu-id="9818f-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="9818f-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="9818f-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="9818f-113">Delegated (work or school account)</span></span>|<span data-ttu-id="9818f-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="9818f-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="9818f-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="9818f-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="9818f-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9818f-116">Not supported.</span></span>|
|<span data-ttu-id="9818f-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="9818f-117">Application</span></span>|<span data-ttu-id="9818f-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9818f-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="9818f-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="9818f-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceConfigurationRestrictedAppsViolations
```

## <a name="request-headers"></a><span data-ttu-id="9818f-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="9818f-120">Request headers</span></span>
|<span data-ttu-id="9818f-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9818f-121">Header</span></span>|<span data-ttu-id="9818f-122">Valor</span><span class="sxs-lookup"><span data-stu-id="9818f-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="9818f-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="9818f-123">Authorization</span></span>|<span data-ttu-id="9818f-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="9818f-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="9818f-125">Accept</span><span class="sxs-lookup"><span data-stu-id="9818f-125">Accept</span></span>|<span data-ttu-id="9818f-126">application/json</span><span class="sxs-lookup"><span data-stu-id="9818f-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="9818f-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="9818f-127">Request body</span></span>
<span data-ttu-id="9818f-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto restrictedAppsViolation.</span><span class="sxs-lookup"><span data-stu-id="9818f-128">In the request body, supply a JSON representation for the restrictedAppsViolation object.</span></span>

<span data-ttu-id="9818f-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el restrictedAppsViolation.</span><span class="sxs-lookup"><span data-stu-id="9818f-129">The following table shows the properties that are required when you create the restrictedAppsViolation.</span></span>

|<span data-ttu-id="9818f-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="9818f-130">Property</span></span>|<span data-ttu-id="9818f-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="9818f-131">Type</span></span>|<span data-ttu-id="9818f-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="9818f-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="9818f-133">id</span><span class="sxs-lookup"><span data-stu-id="9818f-133">id</span></span>|<span data-ttu-id="9818f-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="9818f-134">String</span></span>|<span data-ttu-id="9818f-135">Identificador único para el objeto.</span><span class="sxs-lookup"><span data-stu-id="9818f-135">Unique identifier for the object.</span></span> <span data-ttu-id="9818f-136">Creados a partir de accountId, deviceId, Id. de directiva y userId</span><span class="sxs-lookup"><span data-stu-id="9818f-136">Composed from accountId, deviceId, policyId and userId</span></span>|
|<span data-ttu-id="9818f-137">userId</span><span class="sxs-lookup"><span data-stu-id="9818f-137">userId</span></span>|<span data-ttu-id="9818f-138">Cadena</span><span class="sxs-lookup"><span data-stu-id="9818f-138">String</span></span>|<span data-ttu-id="9818f-139">Identificador único del usuario, debe ser el Guid</span><span class="sxs-lookup"><span data-stu-id="9818f-139">User unique identifier, must be Guid</span></span>|
|<span data-ttu-id="9818f-140">userName</span><span class="sxs-lookup"><span data-stu-id="9818f-140">userName</span></span>|<span data-ttu-id="9818f-141">Cadena</span><span class="sxs-lookup"><span data-stu-id="9818f-141">String</span></span>|<span data-ttu-id="9818f-142">Nombre de usuario</span><span class="sxs-lookup"><span data-stu-id="9818f-142">User name</span></span>|
|<span data-ttu-id="9818f-143">managedDeviceId</span><span class="sxs-lookup"><span data-stu-id="9818f-143">managedDeviceId</span></span>|<span data-ttu-id="9818f-144">Cadena</span><span class="sxs-lookup"><span data-stu-id="9818f-144">String</span></span>|<span data-ttu-id="9818f-145">Identificador único de dispositivos administrados, debe ser el Guid</span><span class="sxs-lookup"><span data-stu-id="9818f-145">Managed device unique identifier, must be Guid</span></span>|
|<span data-ttu-id="9818f-146">deviceName</span><span class="sxs-lookup"><span data-stu-id="9818f-146">deviceName</span></span>|<span data-ttu-id="9818f-147">Cadena</span><span class="sxs-lookup"><span data-stu-id="9818f-147">String</span></span>|<span data-ttu-id="9818f-148">Nombre de dispositivo</span><span class="sxs-lookup"><span data-stu-id="9818f-148">Device name</span></span>|
|<span data-ttu-id="9818f-149">deviceConfigurationId</span><span class="sxs-lookup"><span data-stu-id="9818f-149">deviceConfigurationId</span></span>|<span data-ttu-id="9818f-150">Cadena</span><span class="sxs-lookup"><span data-stu-id="9818f-150">String</span></span>|<span data-ttu-id="9818f-151">Identificador único de dispositivo configuración perfil, debe ser el Guid</span><span class="sxs-lookup"><span data-stu-id="9818f-151">Device configuration profile unique identifier, must be Guid</span></span>|
|<span data-ttu-id="9818f-152">deviceConfigurationName</span><span class="sxs-lookup"><span data-stu-id="9818f-152">deviceConfigurationName</span></span>|<span data-ttu-id="9818f-153">Cadena</span><span class="sxs-lookup"><span data-stu-id="9818f-153">String</span></span>|<span data-ttu-id="9818f-154">Nombre del perfil de configuración de dispositivo</span><span class="sxs-lookup"><span data-stu-id="9818f-154">Device configuration profile name</span></span>|
|<span data-ttu-id="9818f-155">platformType</span><span class="sxs-lookup"><span data-stu-id="9818f-155">platformType</span></span>|[<span data-ttu-id="9818f-156">policyPlatformType</span><span class="sxs-lookup"><span data-stu-id="9818f-156">policyPlatformType</span></span>](../resources/intune-deviceconfig-policyplatformtype.md)|<span data-ttu-id="9818f-157">Tipo de plataforma.</span><span class="sxs-lookup"><span data-stu-id="9818f-157">Platform type.</span></span> <span data-ttu-id="9818f-158">Los valores posibles son: `android`, `androidForWork`, `iOS`, `macOS`, `windowsPhone81`, `windows81AndLater`, `windows10AndLater`, `androidWorkProfile` y `all`.</span><span class="sxs-lookup"><span data-stu-id="9818f-158">Possible values are: `android`, `androidForWork`, `iOS`, `macOS`, `windowsPhone81`, `windows81AndLater`, `windows10AndLater`, `androidWorkProfile`, `all`.</span></span>|
|<span data-ttu-id="9818f-159">restrictedAppsState</span><span class="sxs-lookup"><span data-stu-id="9818f-159">restrictedAppsState</span></span>|[<span data-ttu-id="9818f-160">restrictedAppsState</span><span class="sxs-lookup"><span data-stu-id="9818f-160">restrictedAppsState</span></span>](../resources/intune-deviceconfig-restrictedappsstate.md)|<span data-ttu-id="9818f-161">Estado de aplicaciones restringidos.</span><span class="sxs-lookup"><span data-stu-id="9818f-161">Restricted apps state.</span></span> <span data-ttu-id="9818f-162">Los valores posibles son: `prohibitedApps` y `notApprovedApps`.</span><span class="sxs-lookup"><span data-stu-id="9818f-162">Possible values are: `prohibitedApps`, `notApprovedApps`.</span></span>|
|<span data-ttu-id="9818f-163">restrictedApps</span><span class="sxs-lookup"><span data-stu-id="9818f-163">restrictedApps</span></span>|<span data-ttu-id="9818f-164">colección de [managedDeviceReportedApp](../resources/intune-deviceconfig-manageddevicereportedapp.md)</span><span class="sxs-lookup"><span data-stu-id="9818f-164">[managedDeviceReportedApp](../resources/intune-deviceconfig-manageddevicereportedapp.md) collection</span></span>|<span data-ttu-id="9818f-165">Lista de aplicaciones restringidas infringidas</span><span class="sxs-lookup"><span data-stu-id="9818f-165">List of violated restricted apps</span></span>|



## <a name="response"></a><span data-ttu-id="9818f-166">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9818f-166">Response</span></span>
<span data-ttu-id="9818f-167">Si tiene éxito, este método devuelve una `201 Created` código de respuesta y un objeto [restrictedAppsViolation](../resources/intune-deviceconfig-restrictedappsviolation.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9818f-167">If successful, this method returns a `201 Created` response code and a [restrictedAppsViolation](../resources/intune-deviceconfig-restrictedappsviolation.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="9818f-168">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9818f-168">Example</span></span>
### <a name="request"></a><span data-ttu-id="9818f-169">Solicitud</span><span class="sxs-lookup"><span data-stu-id="9818f-169">Request</span></span>
<span data-ttu-id="9818f-170">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="9818f-170">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/deviceConfigurationRestrictedAppsViolations
Content-type: application/json
Content-length: 564

{
  "@odata.type": "#microsoft.graph.restrictedAppsViolation",
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

### <a name="response"></a><span data-ttu-id="9818f-171">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9818f-171">Response</span></span>
<span data-ttu-id="9818f-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="9818f-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
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





