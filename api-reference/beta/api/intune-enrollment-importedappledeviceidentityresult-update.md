---
title: Actualizar importedAppleDeviceIdentityResult
description: Actualizar las propiedades de un objeto importedAppleDeviceIdentityResult.
author: tfitzmac
ms.openlocfilehash: 283626d0b3f87faccfac4531e060debc6ba210fc
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27355639"
---
# <a name="update-importedappledeviceidentityresult"></a><span data-ttu-id="10bab-103">Actualizar importedAppleDeviceIdentityResult</span><span class="sxs-lookup"><span data-stu-id="10bab-103">Update importedAppleDeviceIdentityResult</span></span>

> <span data-ttu-id="10bab-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="10bab-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="10bab-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="10bab-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="10bab-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="10bab-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="10bab-107">Actualizar las propiedades de un objeto [importedAppleDeviceIdentityResult](../resources/intune-enrollment-importedappledeviceidentityresult.md) .</span><span class="sxs-lookup"><span data-stu-id="10bab-107">Update the properties of a [importedAppleDeviceIdentityResult](../resources/intune-enrollment-importedappledeviceidentityresult.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="10bab-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="10bab-108">Prerequisites</span></span>
<span data-ttu-id="10bab-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="10bab-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="10bab-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="10bab-111">Permission type</span></span>|<span data-ttu-id="10bab-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="10bab-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="10bab-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="10bab-113">Delegated (work or school account)</span></span>|<span data-ttu-id="10bab-114">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="10bab-114">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="10bab-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="10bab-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="10bab-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="10bab-116">Not supported.</span></span>|
|<span data-ttu-id="10bab-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="10bab-117">Application</span></span>|<span data-ttu-id="10bab-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="10bab-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="10bab-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="10bab-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/depOnboardingSettings/{depOnboardingSettingId}/importedAppleDeviceIdentities/{importedAppleDeviceIdentityId}
```

## <a name="request-headers"></a><span data-ttu-id="10bab-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="10bab-120">Request headers</span></span>
|<span data-ttu-id="10bab-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="10bab-121">Header</span></span>|<span data-ttu-id="10bab-122">Valor</span><span class="sxs-lookup"><span data-stu-id="10bab-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="10bab-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="10bab-123">Authorization</span></span>|<span data-ttu-id="10bab-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="10bab-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="10bab-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="10bab-125">Accept</span></span>|<span data-ttu-id="10bab-126">application/json</span><span class="sxs-lookup"><span data-stu-id="10bab-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="10bab-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="10bab-127">Request body</span></span>
<span data-ttu-id="10bab-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto [importedAppleDeviceIdentityResult](../resources/intune-enrollment-importedappledeviceidentityresult.md) .</span><span class="sxs-lookup"><span data-stu-id="10bab-128">In the request body, supply a JSON representation for the [importedAppleDeviceIdentityResult](../resources/intune-enrollment-importedappledeviceidentityresult.md) object.</span></span>

<span data-ttu-id="10bab-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el [importedAppleDeviceIdentityResult](../resources/intune-enrollment-importedappledeviceidentityresult.md).</span><span class="sxs-lookup"><span data-stu-id="10bab-129">The following table shows the properties that are required when you create the [importedAppleDeviceIdentityResult](../resources/intune-enrollment-importedappledeviceidentityresult.md).</span></span>

|<span data-ttu-id="10bab-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="10bab-130">Property</span></span>|<span data-ttu-id="10bab-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="10bab-131">Type</span></span>|<span data-ttu-id="10bab-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="10bab-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="10bab-133">id</span><span class="sxs-lookup"><span data-stu-id="10bab-133">id</span></span>|<span data-ttu-id="10bab-134">String</span><span class="sxs-lookup"><span data-stu-id="10bab-134">String</span></span>|<span data-ttu-id="10bab-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="10bab-135">Key of the entity.</span></span> <span data-ttu-id="10bab-136">Se hereda de [importedAppleDeviceIdentity](../resources/intune-enrollment-importedappledeviceidentity.md)</span><span class="sxs-lookup"><span data-stu-id="10bab-136">Inherited from [importedAppleDeviceIdentity](../resources/intune-enrollment-importedappledeviceidentity.md)</span></span>|
|<span data-ttu-id="10bab-137">serialNumber</span><span class="sxs-lookup"><span data-stu-id="10bab-137">serialNumber</span></span>|<span data-ttu-id="10bab-138">String</span><span class="sxs-lookup"><span data-stu-id="10bab-138">String</span></span>|<span data-ttu-id="10bab-139">Número de serie del dispositivo Inherited desde [importedAppleDeviceIdentity](../resources/intune-enrollment-importedappledeviceidentity.md)</span><span class="sxs-lookup"><span data-stu-id="10bab-139">Device serial number Inherited from [importedAppleDeviceIdentity](../resources/intune-enrollment-importedappledeviceidentity.md)</span></span>|
|<span data-ttu-id="10bab-140">requestedEnrollmentProfileId</span><span class="sxs-lookup"><span data-stu-id="10bab-140">requestedEnrollmentProfileId</span></span>|<span data-ttu-id="10bab-141">String</span><span class="sxs-lookup"><span data-stu-id="10bab-141">String</span></span>|<span data-ttu-id="10bab-142">Administración de identificador de perfil de inscripción tenga la intención de aplicar al dispositivo durante la inscripción siguiente Inherited de [importedAppleDeviceIdentity](../resources/intune-enrollment-importedappledeviceidentity.md)</span><span class="sxs-lookup"><span data-stu-id="10bab-142">Enrollment profile Id admin intends to apply to the device during next enrollment Inherited from [importedAppleDeviceIdentity](../resources/intune-enrollment-importedappledeviceidentity.md)</span></span>|
|<span data-ttu-id="10bab-143">requestedEnrollmentProfileAssignmentDateTime</span><span class="sxs-lookup"><span data-stu-id="10bab-143">requestedEnrollmentProfileAssignmentDateTime</span></span>|<span data-ttu-id="10bab-144">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="10bab-144">DateTimeOffset</span></span>|<span data-ttu-id="10bab-145">El perfil de tiempo de inscripción se asignó al dispositivo Inherited desde [importedAppleDeviceIdentity](../resources/intune-enrollment-importedappledeviceidentity.md)</span><span class="sxs-lookup"><span data-stu-id="10bab-145">The time enrollment profile was assigned to the device Inherited from [importedAppleDeviceIdentity](../resources/intune-enrollment-importedappledeviceidentity.md)</span></span>|
|<span data-ttu-id="10bab-146">isSupervised</span><span class="sxs-lookup"><span data-stu-id="10bab-146">isSupervised</span></span>|<span data-ttu-id="10bab-147">Boolean</span><span class="sxs-lookup"><span data-stu-id="10bab-147">Boolean</span></span>|<span data-ttu-id="10bab-148">Indica si el dispositivo de Apple es supervisado.</span><span class="sxs-lookup"><span data-stu-id="10bab-148">Indicates if the Apple device is supervised.</span></span> <span data-ttu-id="10bab-149">Obtener más información se encuentra en: https://support.apple.com/en-us/HT202837 se hereda de [importedAppleDeviceIdentity](../resources/intune-enrollment-importedappledeviceidentity.md)</span><span class="sxs-lookup"><span data-stu-id="10bab-149">More information is at: https://support.apple.com/en-us/HT202837 Inherited from [importedAppleDeviceIdentity](../resources/intune-enrollment-importedappledeviceidentity.md)</span></span>|
|<span data-ttu-id="10bab-150">discoverySource</span><span class="sxs-lookup"><span data-stu-id="10bab-150">discoverySource</span></span>|[<span data-ttu-id="10bab-151">discoverySource</span><span class="sxs-lookup"><span data-stu-id="10bab-151">discoverySource</span></span>](../resources/intune-enrollment-discoverysource.md)|<span data-ttu-id="10bab-152">Origen de detección del dispositivo de Apple.</span><span class="sxs-lookup"><span data-stu-id="10bab-152">Apple device discovery source.</span></span> <span data-ttu-id="10bab-153">Se hereda de [importedAppleDeviceIdentity](../resources/intune-enrollment-importedappledeviceidentity.md).</span><span class="sxs-lookup"><span data-stu-id="10bab-153">Inherited from [importedAppleDeviceIdentity](../resources/intune-enrollment-importedappledeviceidentity.md).</span></span> <span data-ttu-id="10bab-154">Los valores posibles son: `unknown`, `adminImport` y `deviceEnrollmentProgram`.</span><span class="sxs-lookup"><span data-stu-id="10bab-154">Possible values are: `unknown`, `adminImport`, `deviceEnrollmentProgram`.</span></span>|
|<span data-ttu-id="10bab-155">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="10bab-155">createdDateTime</span></span>|<span data-ttu-id="10bab-156">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="10bab-156">DateTimeOffset</span></span>|<span data-ttu-id="10bab-157">Crear fecha hora del dispositivo Inherited desde [importedAppleDeviceIdentity](../resources/intune-enrollment-importedappledeviceidentity.md)</span><span class="sxs-lookup"><span data-stu-id="10bab-157">Created Date Time of the device Inherited from [importedAppleDeviceIdentity](../resources/intune-enrollment-importedappledeviceidentity.md)</span></span>|
|<span data-ttu-id="10bab-158">lastContactedDateTime</span><span class="sxs-lookup"><span data-stu-id="10bab-158">lastContactedDateTime</span></span>|<span data-ttu-id="10bab-159">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="10bab-159">DateTimeOffset</span></span>|<span data-ttu-id="10bab-160">Última vez fecha ponerse en contacto del dispositivo Inherited desde [importedAppleDeviceIdentity](../resources/intune-enrollment-importedappledeviceidentity.md)</span><span class="sxs-lookup"><span data-stu-id="10bab-160">Last Contacted Date Time of the device Inherited from [importedAppleDeviceIdentity](../resources/intune-enrollment-importedappledeviceidentity.md)</span></span>|
|<span data-ttu-id="10bab-161">descripción</span><span class="sxs-lookup"><span data-stu-id="10bab-161">description</span></span>|<span data-ttu-id="10bab-162">String</span><span class="sxs-lookup"><span data-stu-id="10bab-162">String</span></span>|<span data-ttu-id="10bab-163">La descripción del dispositivo Inherited desde [importedAppleDeviceIdentity](../resources/intune-enrollment-importedappledeviceidentity.md)</span><span class="sxs-lookup"><span data-stu-id="10bab-163">The description of the device Inherited from [importedAppleDeviceIdentity](../resources/intune-enrollment-importedappledeviceidentity.md)</span></span>|
|<span data-ttu-id="10bab-164">enrollmentState</span><span class="sxs-lookup"><span data-stu-id="10bab-164">enrollmentState</span></span>|[<span data-ttu-id="10bab-165">enrollmentState</span><span class="sxs-lookup"><span data-stu-id="10bab-165">enrollmentState</span></span>](../resources/intune-enrollment-enrollmentstate.md)|<span data-ttu-id="10bab-166">El estado del dispositivo en Intune se hereda de [importedAppleDeviceIdentity](../resources/intune-enrollment-importedappledeviceidentity.md).</span><span class="sxs-lookup"><span data-stu-id="10bab-166">The state of the device in Intune Inherited from [importedAppleDeviceIdentity](../resources/intune-enrollment-importedappledeviceidentity.md).</span></span> <span data-ttu-id="10bab-167">Los valores posibles son: `unknown`, `enrolled`, `pendingReset`, `failed`, `notContacted`, `blocked`.</span><span class="sxs-lookup"><span data-stu-id="10bab-167">Possible values are: `unknown`, `enrolled`, `pendingReset`, `failed`, `notContacted`, `blocked`.</span></span>|
|<span data-ttu-id="10bab-168">platform</span><span class="sxs-lookup"><span data-stu-id="10bab-168">platform</span></span>|[<span data-ttu-id="10bab-169">plataforma</span><span class="sxs-lookup"><span data-stu-id="10bab-169">platform</span></span>](../resources/intune-enrollment-platform.md)|<span data-ttu-id="10bab-170">La plataforma del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="10bab-170">The platform of the Device.</span></span> <span data-ttu-id="10bab-171">Se hereda de [importedAppleDeviceIdentity](../resources/intune-enrollment-importedappledeviceidentity.md).</span><span class="sxs-lookup"><span data-stu-id="10bab-171">Inherited from [importedAppleDeviceIdentity](../resources/intune-enrollment-importedappledeviceidentity.md).</span></span> <span data-ttu-id="10bab-172">Los valores posibles son: `unknown`, `ios`, `android`, `windows`, `windowsMobile`, `macOS`.</span><span class="sxs-lookup"><span data-stu-id="10bab-172">Possible values are: `unknown`, `ios`, `android`, `windows`, `windowsMobile`, `macOS`.</span></span>|
|<span data-ttu-id="10bab-173">status</span><span class="sxs-lookup"><span data-stu-id="10bab-173">status</span></span>|<span data-ttu-id="10bab-174">Boolean</span><span class="sxs-lookup"><span data-stu-id="10bab-174">Boolean</span></span>|<span data-ttu-id="10bab-175">Estado de identidad de dispositivo importada</span><span class="sxs-lookup"><span data-stu-id="10bab-175">Status of imported device identity</span></span>|



## <a name="response"></a><span data-ttu-id="10bab-176">Respuesta</span><span class="sxs-lookup"><span data-stu-id="10bab-176">Response</span></span>
<span data-ttu-id="10bab-177">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto actualizado [importedAppleDeviceIdentityResult](../resources/intune-enrollment-importedappledeviceidentityresult.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="10bab-177">If successful, this method returns a `200 OK` response code and an updated [importedAppleDeviceIdentityResult](../resources/intune-enrollment-importedappledeviceidentityresult.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="10bab-178">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="10bab-178">Example</span></span>
### <a name="request"></a><span data-ttu-id="10bab-179">Solicitud</span><span class="sxs-lookup"><span data-stu-id="10bab-179">Request</span></span>
<span data-ttu-id="10bab-180">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="10bab-180">Here is an example of the request.</span></span>
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

### <a name="response"></a><span data-ttu-id="10bab-181">Respuesta</span><span class="sxs-lookup"><span data-stu-id="10bab-181">Response</span></span>
<span data-ttu-id="10bab-p108">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="10bab-p108">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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





