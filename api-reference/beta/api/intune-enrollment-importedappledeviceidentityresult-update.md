---
title: Actualizar importedAppleDeviceIdentityResult
description: Actualizar las propiedades de un objeto importedAppleDeviceIdentityResult.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 0b977063c362646cee7051e742729f63fccecf9e
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27836543"
---
# <a name="update-importedappledeviceidentityresult"></a><span data-ttu-id="2621f-103">Actualizar importedAppleDeviceIdentityResult</span><span class="sxs-lookup"><span data-stu-id="2621f-103">Update importedAppleDeviceIdentityResult</span></span>

> <span data-ttu-id="2621f-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="2621f-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="2621f-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="2621f-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="2621f-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="2621f-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="2621f-107">Actualizar las propiedades de un objeto [importedAppleDeviceIdentityResult](../resources/intune-enrollment-importedappledeviceidentityresult.md) .</span><span class="sxs-lookup"><span data-stu-id="2621f-107">Update the properties of a [importedAppleDeviceIdentityResult](../resources/intune-enrollment-importedappledeviceidentityresult.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="2621f-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="2621f-108">Prerequisites</span></span>
<span data-ttu-id="2621f-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="2621f-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="2621f-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="2621f-111">Permission type</span></span>|<span data-ttu-id="2621f-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="2621f-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="2621f-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="2621f-113">Delegated (work or school account)</span></span>|<span data-ttu-id="2621f-114">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="2621f-114">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="2621f-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="2621f-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="2621f-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2621f-116">Not supported.</span></span>|
|<span data-ttu-id="2621f-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="2621f-117">Application</span></span>|<span data-ttu-id="2621f-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2621f-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="2621f-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="2621f-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/depOnboardingSettings/{depOnboardingSettingId}/importedAppleDeviceIdentities/{importedAppleDeviceIdentityId}
```

## <a name="request-headers"></a><span data-ttu-id="2621f-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="2621f-120">Request headers</span></span>
|<span data-ttu-id="2621f-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2621f-121">Header</span></span>|<span data-ttu-id="2621f-122">Valor</span><span class="sxs-lookup"><span data-stu-id="2621f-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="2621f-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="2621f-123">Authorization</span></span>|<span data-ttu-id="2621f-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="2621f-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="2621f-125">Accept</span><span class="sxs-lookup"><span data-stu-id="2621f-125">Accept</span></span>|<span data-ttu-id="2621f-126">application/json</span><span class="sxs-lookup"><span data-stu-id="2621f-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="2621f-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="2621f-127">Request body</span></span>
<span data-ttu-id="2621f-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto [importedAppleDeviceIdentityResult](../resources/intune-enrollment-importedappledeviceidentityresult.md) .</span><span class="sxs-lookup"><span data-stu-id="2621f-128">In the request body, supply a JSON representation for the [importedAppleDeviceIdentityResult](../resources/intune-enrollment-importedappledeviceidentityresult.md) object.</span></span>

<span data-ttu-id="2621f-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el [importedAppleDeviceIdentityResult](../resources/intune-enrollment-importedappledeviceidentityresult.md).</span><span class="sxs-lookup"><span data-stu-id="2621f-129">The following table shows the properties that are required when you create the [importedAppleDeviceIdentityResult](../resources/intune-enrollment-importedappledeviceidentityresult.md).</span></span>

|<span data-ttu-id="2621f-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="2621f-130">Property</span></span>|<span data-ttu-id="2621f-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="2621f-131">Type</span></span>|<span data-ttu-id="2621f-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="2621f-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="2621f-133">id</span><span class="sxs-lookup"><span data-stu-id="2621f-133">id</span></span>|<span data-ttu-id="2621f-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="2621f-134">String</span></span>|<span data-ttu-id="2621f-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="2621f-135">Key of the entity.</span></span> <span data-ttu-id="2621f-136">Se hereda de [importedAppleDeviceIdentity](../resources/intune-enrollment-importedappledeviceidentity.md)</span><span class="sxs-lookup"><span data-stu-id="2621f-136">Inherited from [importedAppleDeviceIdentity](../resources/intune-enrollment-importedappledeviceidentity.md)</span></span>|
|<span data-ttu-id="2621f-137">serialNumber</span><span class="sxs-lookup"><span data-stu-id="2621f-137">serialNumber</span></span>|<span data-ttu-id="2621f-138">Cadena</span><span class="sxs-lookup"><span data-stu-id="2621f-138">String</span></span>|<span data-ttu-id="2621f-139">Número de serie del dispositivo Inherited desde [importedAppleDeviceIdentity](../resources/intune-enrollment-importedappledeviceidentity.md)</span><span class="sxs-lookup"><span data-stu-id="2621f-139">Device serial number Inherited from [importedAppleDeviceIdentity](../resources/intune-enrollment-importedappledeviceidentity.md)</span></span>|
|<span data-ttu-id="2621f-140">requestedEnrollmentProfileId</span><span class="sxs-lookup"><span data-stu-id="2621f-140">requestedEnrollmentProfileId</span></span>|<span data-ttu-id="2621f-141">Cadena</span><span class="sxs-lookup"><span data-stu-id="2621f-141">String</span></span>|<span data-ttu-id="2621f-142">Administración de identificador de perfil de inscripción tenga la intención de aplicar al dispositivo durante la inscripción siguiente Inherited de [importedAppleDeviceIdentity](../resources/intune-enrollment-importedappledeviceidentity.md)</span><span class="sxs-lookup"><span data-stu-id="2621f-142">Enrollment profile Id admin intends to apply to the device during next enrollment Inherited from [importedAppleDeviceIdentity](../resources/intune-enrollment-importedappledeviceidentity.md)</span></span>|
|<span data-ttu-id="2621f-143">requestedEnrollmentProfileAssignmentDateTime</span><span class="sxs-lookup"><span data-stu-id="2621f-143">requestedEnrollmentProfileAssignmentDateTime</span></span>|<span data-ttu-id="2621f-144">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="2621f-144">DateTimeOffset</span></span>|<span data-ttu-id="2621f-145">El perfil de tiempo de inscripción se asignó al dispositivo Inherited desde [importedAppleDeviceIdentity](../resources/intune-enrollment-importedappledeviceidentity.md)</span><span class="sxs-lookup"><span data-stu-id="2621f-145">The time enrollment profile was assigned to the device Inherited from [importedAppleDeviceIdentity](../resources/intune-enrollment-importedappledeviceidentity.md)</span></span>|
|<span data-ttu-id="2621f-146">isSupervised</span><span class="sxs-lookup"><span data-stu-id="2621f-146">isSupervised</span></span>|<span data-ttu-id="2621f-147">Booleano</span><span class="sxs-lookup"><span data-stu-id="2621f-147">Boolean</span></span>|<span data-ttu-id="2621f-148">Indica si el dispositivo de Apple es supervisado.</span><span class="sxs-lookup"><span data-stu-id="2621f-148">Indicates if the Apple device is supervised.</span></span> <span data-ttu-id="2621f-149">Obtener más información se encuentra en: https://support.apple.com/en-us/HT202837 se hereda de [importedAppleDeviceIdentity](../resources/intune-enrollment-importedappledeviceidentity.md)</span><span class="sxs-lookup"><span data-stu-id="2621f-149">More information is at: https://support.apple.com/en-us/HT202837 Inherited from [importedAppleDeviceIdentity](../resources/intune-enrollment-importedappledeviceidentity.md)</span></span>|
|<span data-ttu-id="2621f-150">discoverySource</span><span class="sxs-lookup"><span data-stu-id="2621f-150">discoverySource</span></span>|[<span data-ttu-id="2621f-151">discoverySource</span><span class="sxs-lookup"><span data-stu-id="2621f-151">discoverySource</span></span>](../resources/intune-enrollment-discoverysource.md)|<span data-ttu-id="2621f-152">Origen de detección del dispositivo de Apple.</span><span class="sxs-lookup"><span data-stu-id="2621f-152">Apple device discovery source.</span></span> <span data-ttu-id="2621f-153">Se hereda de [importedAppleDeviceIdentity](../resources/intune-enrollment-importedappledeviceidentity.md).</span><span class="sxs-lookup"><span data-stu-id="2621f-153">Inherited from [importedAppleDeviceIdentity](../resources/intune-enrollment-importedappledeviceidentity.md).</span></span> <span data-ttu-id="2621f-154">Los valores posibles son: `unknown`, `adminImport` y `deviceEnrollmentProgram`.</span><span class="sxs-lookup"><span data-stu-id="2621f-154">Possible values are: `unknown`, `adminImport`, `deviceEnrollmentProgram`.</span></span>|
|<span data-ttu-id="2621f-155">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="2621f-155">createdDateTime</span></span>|<span data-ttu-id="2621f-156">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="2621f-156">DateTimeOffset</span></span>|<span data-ttu-id="2621f-157">Crear fecha hora del dispositivo Inherited desde [importedAppleDeviceIdentity](../resources/intune-enrollment-importedappledeviceidentity.md)</span><span class="sxs-lookup"><span data-stu-id="2621f-157">Created Date Time of the device Inherited from [importedAppleDeviceIdentity](../resources/intune-enrollment-importedappledeviceidentity.md)</span></span>|
|<span data-ttu-id="2621f-158">lastContactedDateTime</span><span class="sxs-lookup"><span data-stu-id="2621f-158">lastContactedDateTime</span></span>|<span data-ttu-id="2621f-159">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="2621f-159">DateTimeOffset</span></span>|<span data-ttu-id="2621f-160">Última vez fecha ponerse en contacto del dispositivo Inherited desde [importedAppleDeviceIdentity](../resources/intune-enrollment-importedappledeviceidentity.md)</span><span class="sxs-lookup"><span data-stu-id="2621f-160">Last Contacted Date Time of the device Inherited from [importedAppleDeviceIdentity](../resources/intune-enrollment-importedappledeviceidentity.md)</span></span>|
|<span data-ttu-id="2621f-161">descripción</span><span class="sxs-lookup"><span data-stu-id="2621f-161">description</span></span>|<span data-ttu-id="2621f-162">Cadena</span><span class="sxs-lookup"><span data-stu-id="2621f-162">String</span></span>|<span data-ttu-id="2621f-163">La descripción del dispositivo Inherited desde [importedAppleDeviceIdentity](../resources/intune-enrollment-importedappledeviceidentity.md)</span><span class="sxs-lookup"><span data-stu-id="2621f-163">The description of the device Inherited from [importedAppleDeviceIdentity](../resources/intune-enrollment-importedappledeviceidentity.md)</span></span>|
|<span data-ttu-id="2621f-164">enrollmentState</span><span class="sxs-lookup"><span data-stu-id="2621f-164">enrollmentState</span></span>|[<span data-ttu-id="2621f-165">enrollmentState</span><span class="sxs-lookup"><span data-stu-id="2621f-165">enrollmentState</span></span>](../resources/intune-enrollment-enrollmentstate.md)|<span data-ttu-id="2621f-166">El estado del dispositivo en Intune se hereda de [importedAppleDeviceIdentity](../resources/intune-enrollment-importedappledeviceidentity.md).</span><span class="sxs-lookup"><span data-stu-id="2621f-166">The state of the device in Intune Inherited from [importedAppleDeviceIdentity](../resources/intune-enrollment-importedappledeviceidentity.md).</span></span> <span data-ttu-id="2621f-167">Los valores posibles son: `unknown`, `enrolled`, `pendingReset`, `failed`, `notContacted`, `blocked`.</span><span class="sxs-lookup"><span data-stu-id="2621f-167">Possible values are: `unknown`, `enrolled`, `pendingReset`, `failed`, `notContacted`, `blocked`.</span></span>|
|<span data-ttu-id="2621f-168">platform</span><span class="sxs-lookup"><span data-stu-id="2621f-168">platform</span></span>|[<span data-ttu-id="2621f-169">plataforma</span><span class="sxs-lookup"><span data-stu-id="2621f-169">platform</span></span>](../resources/intune-enrollment-platform.md)|<span data-ttu-id="2621f-170">La plataforma del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2621f-170">The platform of the Device.</span></span> <span data-ttu-id="2621f-171">Se hereda de [importedAppleDeviceIdentity](../resources/intune-enrollment-importedappledeviceidentity.md).</span><span class="sxs-lookup"><span data-stu-id="2621f-171">Inherited from [importedAppleDeviceIdentity](../resources/intune-enrollment-importedappledeviceidentity.md).</span></span> <span data-ttu-id="2621f-172">Los valores posibles son: `unknown`, `ios`, `android`, `windows`, `windowsMobile`, `macOS`.</span><span class="sxs-lookup"><span data-stu-id="2621f-172">Possible values are: `unknown`, `ios`, `android`, `windows`, `windowsMobile`, `macOS`.</span></span>|
|<span data-ttu-id="2621f-173">status</span><span class="sxs-lookup"><span data-stu-id="2621f-173">status</span></span>|<span data-ttu-id="2621f-174">Booleano</span><span class="sxs-lookup"><span data-stu-id="2621f-174">Boolean</span></span>|<span data-ttu-id="2621f-175">Estado de identidad de dispositivo importada</span><span class="sxs-lookup"><span data-stu-id="2621f-175">Status of imported device identity</span></span>|



## <a name="response"></a><span data-ttu-id="2621f-176">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2621f-176">Response</span></span>
<span data-ttu-id="2621f-177">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto actualizado [importedAppleDeviceIdentityResult](../resources/intune-enrollment-importedappledeviceidentityresult.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2621f-177">If successful, this method returns a `200 OK` response code and an updated [importedAppleDeviceIdentityResult](../resources/intune-enrollment-importedappledeviceidentityresult.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="2621f-178">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2621f-178">Example</span></span>
### <a name="request"></a><span data-ttu-id="2621f-179">Solicitud</span><span class="sxs-lookup"><span data-stu-id="2621f-179">Request</span></span>
<span data-ttu-id="2621f-180">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="2621f-180">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/depOnboardingSettings/{depOnboardingSettingId}/importedAppleDeviceIdentities/{importedAppleDeviceIdentityId}
Content-type: application/json
Content-length: 450

{
  "serialNumber": "Serial Number value",
  "requestedEnrollmentProfileId": "Requested Enrollment Profile Id value",
  "requestedEnrollmentProfileAssignmentDateTime": "2017-01-01T00:02:32.8167841-08:00",
  "isSupervised": true,
  "discoverySource": "adminImport",
  "lastContactedDateTime": "2016-12-31T23:58:44.2908994-08:00",
  "description": "Description value",
  "enrollmentState": "enrolled",
  "platform": "ios",
  "status": true
}
```

### <a name="response"></a><span data-ttu-id="2621f-181">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2621f-181">Response</span></span>
<span data-ttu-id="2621f-p108">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="2621f-p108">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 630

{
  "@odata.type": "#microsoft.graph.importedAppleDeviceIdentityResult",
  "id": "557cfb4a-fb4a-557c-4afb-7c554afb7c55",
  "serialNumber": "Serial Number value",
  "requestedEnrollmentProfileId": "Requested Enrollment Profile Id value",
  "requestedEnrollmentProfileAssignmentDateTime": "2017-01-01T00:02:32.8167841-08:00",
  "isSupervised": true,
  "discoverySource": "adminImport",
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "lastContactedDateTime": "2016-12-31T23:58:44.2908994-08:00",
  "description": "Description value",
  "enrollmentState": "enrolled",
  "platform": "ios",
  "status": true
}
```





