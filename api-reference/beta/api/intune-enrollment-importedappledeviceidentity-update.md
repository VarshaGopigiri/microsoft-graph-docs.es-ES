---
title: Actualizar importedAppleDeviceIdentity
description: Actualizar las propiedades de un objeto importedAppleDeviceIdentity.
ms.openlocfilehash: 48fbcd38e7e74734b069b9a0b8db6d675fe26a96
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089426"
---
# <a name="update-importedappledeviceidentity"></a><span data-ttu-id="1def8-103">Actualizar importedAppleDeviceIdentity</span><span class="sxs-lookup"><span data-stu-id="1def8-103">Update importedAppleDeviceIdentity</span></span>

> <span data-ttu-id="1def8-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="1def8-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="1def8-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="1def8-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="1def8-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="1def8-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="1def8-107">Actualizar las propiedades de un objeto [importedAppleDeviceIdentity](../resources/intune-enrollment-importedappledeviceidentity.md) .</span><span class="sxs-lookup"><span data-stu-id="1def8-107">Update the properties of a [importedAppleDeviceIdentity](../resources/intune-enrollment-importedappledeviceidentity.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="1def8-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="1def8-108">Prerequisites</span></span>
<span data-ttu-id="1def8-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="1def8-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="1def8-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="1def8-111">Permission type</span></span>|<span data-ttu-id="1def8-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="1def8-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="1def8-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="1def8-113">Delegated (work or school account)</span></span>|<span data-ttu-id="1def8-114">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="1def8-114">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="1def8-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="1def8-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="1def8-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1def8-116">Not supported.</span></span>|
|<span data-ttu-id="1def8-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="1def8-117">Application</span></span>|<span data-ttu-id="1def8-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1def8-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="1def8-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="1def8-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/depOnboardingSettings/{depOnboardingSettingId}/importedAppleDeviceIdentities/{importedAppleDeviceIdentityId}
```

## <a name="request-headers"></a><span data-ttu-id="1def8-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="1def8-120">Request headers</span></span>
|<span data-ttu-id="1def8-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1def8-121">Header</span></span>|<span data-ttu-id="1def8-122">Valor</span><span class="sxs-lookup"><span data-stu-id="1def8-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="1def8-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="1def8-123">Authorization</span></span>|<span data-ttu-id="1def8-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="1def8-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="1def8-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="1def8-125">Accept</span></span>|<span data-ttu-id="1def8-126">application/json</span><span class="sxs-lookup"><span data-stu-id="1def8-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="1def8-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="1def8-127">Request body</span></span>
<span data-ttu-id="1def8-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto [importedAppleDeviceIdentity](../resources/intune-enrollment-importedappledeviceidentity.md) .</span><span class="sxs-lookup"><span data-stu-id="1def8-128">In the request body, supply a JSON representation for the [importedAppleDeviceIdentity](../resources/intune-enrollment-importedappledeviceidentity.md) object.</span></span>

<span data-ttu-id="1def8-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el [importedAppleDeviceIdentity](../resources/intune-enrollment-importedappledeviceidentity.md).</span><span class="sxs-lookup"><span data-stu-id="1def8-129">The following table shows the properties that are required when you create the [importedAppleDeviceIdentity](../resources/intune-enrollment-importedappledeviceidentity.md).</span></span>

|<span data-ttu-id="1def8-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="1def8-130">Property</span></span>|<span data-ttu-id="1def8-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="1def8-131">Type</span></span>|<span data-ttu-id="1def8-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="1def8-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="1def8-133">id</span><span class="sxs-lookup"><span data-stu-id="1def8-133">id</span></span>|<span data-ttu-id="1def8-134">String</span><span class="sxs-lookup"><span data-stu-id="1def8-134">String</span></span>|<span data-ttu-id="1def8-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="1def8-135">Key of the entity.</span></span>|
|<span data-ttu-id="1def8-136">serialNumber</span><span class="sxs-lookup"><span data-stu-id="1def8-136">serialNumber</span></span>|<span data-ttu-id="1def8-137">String</span><span class="sxs-lookup"><span data-stu-id="1def8-137">String</span></span>|<span data-ttu-id="1def8-138">Número de serie del dispositivo</span><span class="sxs-lookup"><span data-stu-id="1def8-138">Device serial number</span></span>|
|<span data-ttu-id="1def8-139">requestedEnrollmentProfileId</span><span class="sxs-lookup"><span data-stu-id="1def8-139">requestedEnrollmentProfileId</span></span>|<span data-ttu-id="1def8-140">String</span><span class="sxs-lookup"><span data-stu-id="1def8-140">String</span></span>|<span data-ttu-id="1def8-141">Administración de identificador de perfil de inscripción tenga la intención de aplicar al dispositivo durante la inscripción siguiente</span><span class="sxs-lookup"><span data-stu-id="1def8-141">Enrollment profile Id admin intends to apply to the device during next enrollment</span></span>|
|<span data-ttu-id="1def8-142">requestedEnrollmentProfileAssignmentDateTime</span><span class="sxs-lookup"><span data-stu-id="1def8-142">requestedEnrollmentProfileAssignmentDateTime</span></span>|<span data-ttu-id="1def8-143">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="1def8-143">DateTimeOffset</span></span>|<span data-ttu-id="1def8-144">El perfil de tiempo de inscripción se asignó al dispositivo</span><span class="sxs-lookup"><span data-stu-id="1def8-144">The time enrollment profile was assigned to the device</span></span>|
|<span data-ttu-id="1def8-145">isSupervised</span><span class="sxs-lookup"><span data-stu-id="1def8-145">isSupervised</span></span>|<span data-ttu-id="1def8-146">Booleano</span><span class="sxs-lookup"><span data-stu-id="1def8-146">Boolean</span></span>|<span data-ttu-id="1def8-147">Indica si el dispositivo de Apple es supervisado.</span><span class="sxs-lookup"><span data-stu-id="1def8-147">Indicates if the Apple device is supervised.</span></span> <span data-ttu-id="1def8-148">Es más información en:https://support.apple.com/en-us/HT202837</span><span class="sxs-lookup"><span data-stu-id="1def8-148">More information is at: https://support.apple.com/en-us/HT202837</span></span>|
|<span data-ttu-id="1def8-149">discoverySource</span><span class="sxs-lookup"><span data-stu-id="1def8-149">discoverySource</span></span>|[<span data-ttu-id="1def8-150">discoverySource</span><span class="sxs-lookup"><span data-stu-id="1def8-150">discoverySource</span></span>](../resources/intune-enrollment-discoverysource.md)|<span data-ttu-id="1def8-151">Origen de detección del dispositivo de Apple.</span><span class="sxs-lookup"><span data-stu-id="1def8-151">Apple device discovery source.</span></span> <span data-ttu-id="1def8-152">Los valores posibles son: `unknown`, `adminImport` y `deviceEnrollmentProgram`.</span><span class="sxs-lookup"><span data-stu-id="1def8-152">Possible values are: `unknown`, `adminImport`, `deviceEnrollmentProgram`.</span></span>|
|<span data-ttu-id="1def8-153">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="1def8-153">createdDateTime</span></span>|<span data-ttu-id="1def8-154">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="1def8-154">DateTimeOffset</span></span>|<span data-ttu-id="1def8-155">Crear fecha hora del dispositivo</span><span class="sxs-lookup"><span data-stu-id="1def8-155">Created Date Time of the device</span></span>|
|<span data-ttu-id="1def8-156">lastContactedDateTime</span><span class="sxs-lookup"><span data-stu-id="1def8-156">lastContactedDateTime</span></span>|<span data-ttu-id="1def8-157">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="1def8-157">DateTimeOffset</span></span>|<span data-ttu-id="1def8-158">Última vez fecha ponerse en contacto del dispositivo</span><span class="sxs-lookup"><span data-stu-id="1def8-158">Last Contacted Date Time of the device</span></span>|
|<span data-ttu-id="1def8-159">descripción</span><span class="sxs-lookup"><span data-stu-id="1def8-159">description</span></span>|<span data-ttu-id="1def8-160">String</span><span class="sxs-lookup"><span data-stu-id="1def8-160">String</span></span>|<span data-ttu-id="1def8-161">La descripción del dispositivo</span><span class="sxs-lookup"><span data-stu-id="1def8-161">The description of the device</span></span>|
|<span data-ttu-id="1def8-162">enrollmentState</span><span class="sxs-lookup"><span data-stu-id="1def8-162">enrollmentState</span></span>|[<span data-ttu-id="1def8-163">enrollmentState</span><span class="sxs-lookup"><span data-stu-id="1def8-163">enrollmentState</span></span>](../resources/intune-enrollment-enrollmentstate.md)|<span data-ttu-id="1def8-164">El estado del dispositivo en Intune.</span><span class="sxs-lookup"><span data-stu-id="1def8-164">The state of the device in Intune.</span></span> <span data-ttu-id="1def8-165">Los valores posibles son: `unknown`, `enrolled`, `pendingReset`, `failed`, `notContacted`, `blocked`.</span><span class="sxs-lookup"><span data-stu-id="1def8-165">Possible values are: `unknown`, `enrolled`, `pendingReset`, `failed`, `notContacted`, `blocked`.</span></span>|
|<span data-ttu-id="1def8-166">platform</span><span class="sxs-lookup"><span data-stu-id="1def8-166">platform</span></span>|[<span data-ttu-id="1def8-167">plataforma</span><span class="sxs-lookup"><span data-stu-id="1def8-167">platform</span></span>](../resources/intune-enrollment-platform.md)|<span data-ttu-id="1def8-168">La plataforma del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1def8-168">The platform of the Device.</span></span> <span data-ttu-id="1def8-169">Los valores posibles son: `unknown`, `ios`, `android`, `windows`, `windowsMobile`, `macOS`.</span><span class="sxs-lookup"><span data-stu-id="1def8-169">Possible values are: `unknown`, `ios`, `android`, `windows`, `windowsMobile`, `macOS`.</span></span>|



## <a name="response"></a><span data-ttu-id="1def8-170">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1def8-170">Response</span></span>
<span data-ttu-id="1def8-171">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto actualizado [importedAppleDeviceIdentity](../resources/intune-enrollment-importedappledeviceidentity.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1def8-171">If successful, this method returns a `200 OK` response code and an updated [importedAppleDeviceIdentity](../resources/intune-enrollment-importedappledeviceidentity.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="1def8-172">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1def8-172">Example</span></span>
### <a name="request"></a><span data-ttu-id="1def8-173">Solicitud</span><span class="sxs-lookup"><span data-stu-id="1def8-173">Request</span></span>
<span data-ttu-id="1def8-174">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="1def8-174">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/depOnboardingSettings/{depOnboardingSettingId}/importedAppleDeviceIdentities/{importedAppleDeviceIdentityId}
Content-type: application/json
Content-length: 431

{
  "serialNumber": "Serial Number value",
  "requestedEnrollmentProfileId": "Requested Enrollment Profile Id value",
  "requestedEnrollmentProfileAssignmentDateTime": "2017-01-01T00:02:32.8167841-08:00",
  "isSupervised": true,
  "discoverySource": "adminImport",
  "lastContactedDateTime": "2016-12-31T23:58:44.2908994-08:00",
  "description": "Description value",
  "enrollmentState": "enrolled",
  "platform": "ios"
}
```

### <a name="response"></a><span data-ttu-id="1def8-175">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1def8-175">Response</span></span>
<span data-ttu-id="1def8-p107">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="1def8-p107">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 605

{
  "@odata.type": "#microsoft.graph.importedAppleDeviceIdentity",
  "id": "352e3c2f-3c2f-352e-2f3c-2e352f3c2e35",
  "serialNumber": "Serial Number value",
  "requestedEnrollmentProfileId": "Requested Enrollment Profile Id value",
  "requestedEnrollmentProfileAssignmentDateTime": "2017-01-01T00:02:32.8167841-08:00",
  "isSupervised": true,
  "discoverySource": "adminImport",
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "lastContactedDateTime": "2016-12-31T23:58:44.2908994-08:00",
  "description": "Description value",
  "enrollmentState": "enrolled",
  "platform": "ios"
}
```





