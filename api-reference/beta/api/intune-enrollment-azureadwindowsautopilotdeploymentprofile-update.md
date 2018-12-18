---
title: Actualizar azureADWindowsAutopilotDeploymentProfile
description: Actualizar las propiedades de un objeto azureADWindowsAutopilotDeploymentProfile.
author: tfitzmac
ms.openlocfilehash: e47ef4aa80254ca7f08ef40c9bda9d43006f0d49
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27315214"
---
# <a name="update-azureadwindowsautopilotdeploymentprofile"></a><span data-ttu-id="d4454-103">Actualizar azureADWindowsAutopilotDeploymentProfile</span><span class="sxs-lookup"><span data-stu-id="d4454-103">Update azureADWindowsAutopilotDeploymentProfile</span></span>

> <span data-ttu-id="d4454-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="d4454-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="d4454-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="d4454-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="d4454-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="d4454-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="d4454-107">Actualizar las propiedades de un objeto [azureADWindowsAutopilotDeploymentProfile](../resources/intune-enrollment-azureadwindowsautopilotdeploymentprofile.md) .</span><span class="sxs-lookup"><span data-stu-id="d4454-107">Update the properties of a [azureADWindowsAutopilotDeploymentProfile](../resources/intune-enrollment-azureadwindowsautopilotdeploymentprofile.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="d4454-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="d4454-108">Prerequisites</span></span>
<span data-ttu-id="d4454-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="d4454-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="d4454-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="d4454-111">Permission type</span></span>|<span data-ttu-id="d4454-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="d4454-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="d4454-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d4454-113">Delegated (work or school account)</span></span>|<span data-ttu-id="d4454-114">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d4454-114">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="d4454-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="d4454-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="d4454-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d4454-116">Not supported.</span></span>|
|<span data-ttu-id="d4454-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d4454-117">Application</span></span>|<span data-ttu-id="d4454-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d4454-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="d4454-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d4454-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/windowsAutopilotDeploymentProfiles/{windowsAutopilotDeploymentProfileId}
PATCH /deviceManagement/windowsAutopilotDeviceIdentities/{windowsAutopilotDeviceIdentityId}/deploymentProfile
PATCH /deviceManagement/windowsAutopilotDeviceIdentities/{windowsAutopilotDeviceIdentityId}/intendedDeploymentProfile
```

## <a name="request-headers"></a><span data-ttu-id="d4454-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d4454-120">Request headers</span></span>
|<span data-ttu-id="d4454-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d4454-121">Header</span></span>|<span data-ttu-id="d4454-122">Valor</span><span class="sxs-lookup"><span data-stu-id="d4454-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="d4454-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="d4454-123">Authorization</span></span>|<span data-ttu-id="d4454-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="d4454-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="d4454-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="d4454-125">Accept</span></span>|<span data-ttu-id="d4454-126">application/json</span><span class="sxs-lookup"><span data-stu-id="d4454-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="d4454-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="d4454-127">Request body</span></span>
<span data-ttu-id="d4454-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto [azureADWindowsAutopilotDeploymentProfile](../resources/intune-enrollment-azureadwindowsautopilotdeploymentprofile.md) .</span><span class="sxs-lookup"><span data-stu-id="d4454-128">In the request body, supply a JSON representation for the [azureADWindowsAutopilotDeploymentProfile](../resources/intune-enrollment-azureadwindowsautopilotdeploymentprofile.md) object.</span></span>

<span data-ttu-id="d4454-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el [azureADWindowsAutopilotDeploymentProfile](../resources/intune-enrollment-azureadwindowsautopilotdeploymentprofile.md).</span><span class="sxs-lookup"><span data-stu-id="d4454-129">The following table shows the properties that are required when you create the [azureADWindowsAutopilotDeploymentProfile](../resources/intune-enrollment-azureadwindowsautopilotdeploymentprofile.md).</span></span>

|<span data-ttu-id="d4454-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d4454-130">Property</span></span>|<span data-ttu-id="d4454-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="d4454-131">Type</span></span>|<span data-ttu-id="d4454-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="d4454-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="d4454-133">id</span><span class="sxs-lookup"><span data-stu-id="d4454-133">id</span></span>|<span data-ttu-id="d4454-134">String</span><span class="sxs-lookup"><span data-stu-id="d4454-134">String</span></span>|<span data-ttu-id="d4454-135">Clave de perfil se hereda de [windowsAutopilotDeploymentProfile](../resources/intune-enrollment-windowsautopilotdeploymentprofile.md)</span><span class="sxs-lookup"><span data-stu-id="d4454-135">Profile Key Inherited from [windowsAutopilotDeploymentProfile](../resources/intune-enrollment-windowsautopilotdeploymentprofile.md)</span></span>|
|<span data-ttu-id="d4454-136">displayName</span><span class="sxs-lookup"><span data-stu-id="d4454-136">displayName</span></span>|<span data-ttu-id="d4454-137">String</span><span class="sxs-lookup"><span data-stu-id="d4454-137">String</span></span>|<span data-ttu-id="d4454-138">Nombre del perfil Inherited desde [windowsAutopilotDeploymentProfile](../resources/intune-enrollment-windowsautopilotdeploymentprofile.md)</span><span class="sxs-lookup"><span data-stu-id="d4454-138">Name of the profile Inherited from [windowsAutopilotDeploymentProfile](../resources/intune-enrollment-windowsautopilotdeploymentprofile.md)</span></span>|
|<span data-ttu-id="d4454-139">descripción</span><span class="sxs-lookup"><span data-stu-id="d4454-139">description</span></span>|<span data-ttu-id="d4454-140">String</span><span class="sxs-lookup"><span data-stu-id="d4454-140">String</span></span>|<span data-ttu-id="d4454-141">Descripción del perfil Inherited desde [windowsAutopilotDeploymentProfile](../resources/intune-enrollment-windowsautopilotdeploymentprofile.md)</span><span class="sxs-lookup"><span data-stu-id="d4454-141">Description of the profile Inherited from [windowsAutopilotDeploymentProfile](../resources/intune-enrollment-windowsautopilotdeploymentprofile.md)</span></span>|
|<span data-ttu-id="d4454-142">language</span><span class="sxs-lookup"><span data-stu-id="d4454-142">language</span></span>|<span data-ttu-id="d4454-143">String</span><span class="sxs-lookup"><span data-stu-id="d4454-143">String</span></span>|<span data-ttu-id="d4454-144">Idioma configurado en el dispositivo Inherited desde [windowsAutopilotDeploymentProfile](../resources/intune-enrollment-windowsautopilotdeploymentprofile.md)</span><span class="sxs-lookup"><span data-stu-id="d4454-144">Language configured on the device Inherited from [windowsAutopilotDeploymentProfile](../resources/intune-enrollment-windowsautopilotdeploymentprofile.md)</span></span>|
|<span data-ttu-id="d4454-145">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="d4454-145">createdDateTime</span></span>|<span data-ttu-id="d4454-146">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="d4454-146">DateTimeOffset</span></span>|<span data-ttu-id="d4454-147">Hora de creación del perfil Inherited desde [windowsAutopilotDeploymentProfile](../resources/intune-enrollment-windowsautopilotdeploymentprofile.md)</span><span class="sxs-lookup"><span data-stu-id="d4454-147">Profile creation time Inherited from [windowsAutopilotDeploymentProfile](../resources/intune-enrollment-windowsautopilotdeploymentprofile.md)</span></span>|
|<span data-ttu-id="d4454-148">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="d4454-148">lastModifiedDateTime</span></span>|<span data-ttu-id="d4454-149">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="d4454-149">DateTimeOffset</span></span>|<span data-ttu-id="d4454-150">Perfil modificó por última vez tiempo Inherited desde [windowsAutopilotDeploymentProfile](../resources/intune-enrollment-windowsautopilotdeploymentprofile.md)</span><span class="sxs-lookup"><span data-stu-id="d4454-150">Profile last modified time Inherited from [windowsAutopilotDeploymentProfile](../resources/intune-enrollment-windowsautopilotdeploymentprofile.md)</span></span>|
|<span data-ttu-id="d4454-151">outOfBoxExperienceSettings</span><span class="sxs-lookup"><span data-stu-id="d4454-151">outOfBoxExperienceSettings</span></span>|[<span data-ttu-id="d4454-152">outOfBoxExperienceSettings</span><span class="sxs-lookup"><span data-stu-id="d4454-152">outOfBoxExperienceSettings</span></span>](../resources/intune-enrollment-outofboxexperiencesettings.md)|<span data-ttu-id="d4454-153">Rápida configuración Inherited desde [windowsAutopilotDeploymentProfile](../resources/intune-enrollment-windowsautopilotdeploymentprofile.md)</span><span class="sxs-lookup"><span data-stu-id="d4454-153">Out of box experience setting Inherited from [windowsAutopilotDeploymentProfile](../resources/intune-enrollment-windowsautopilotdeploymentprofile.md)</span></span>|
|<span data-ttu-id="d4454-154">enrollmentStatusScreenSettings</span><span class="sxs-lookup"><span data-stu-id="d4454-154">enrollmentStatusScreenSettings</span></span>|[<span data-ttu-id="d4454-155">windowsEnrollmentStatusScreenSettings</span><span class="sxs-lookup"><span data-stu-id="d4454-155">windowsEnrollmentStatusScreenSettings</span></span>](../resources/intune-enrollment-windowsenrollmentstatusscreensettings.md)|<span data-ttu-id="d4454-156">Pantalla de estado de inscripción configuración Inherited desde [windowsAutopilotDeploymentProfile](../resources/intune-enrollment-windowsautopilotdeploymentprofile.md)</span><span class="sxs-lookup"><span data-stu-id="d4454-156">Enrollment status screen setting Inherited from [windowsAutopilotDeploymentProfile](../resources/intune-enrollment-windowsautopilotdeploymentprofile.md)</span></span>|
|<span data-ttu-id="d4454-157">extractHardwareHash</span><span class="sxs-lookup"><span data-stu-id="d4454-157">extractHardwareHash</span></span>|<span data-ttu-id="d4454-158">Boolean</span><span class="sxs-lookup"><span data-stu-id="d4454-158">Boolean</span></span>|<span data-ttu-id="d4454-159">Extracción de HardwareHash para el perfil Inherited desde [windowsAutopilotDeploymentProfile](../resources/intune-enrollment-windowsautopilotdeploymentprofile.md)</span><span class="sxs-lookup"><span data-stu-id="d4454-159">HardwareHash Extraction for the profile Inherited from [windowsAutopilotDeploymentProfile](../resources/intune-enrollment-windowsautopilotdeploymentprofile.md)</span></span>|
|<span data-ttu-id="d4454-160">deviceNameTemplate</span><span class="sxs-lookup"><span data-stu-id="d4454-160">deviceNameTemplate</span></span>|<span data-ttu-id="d4454-161">String</span><span class="sxs-lookup"><span data-stu-id="d4454-161">String</span></span>|<span data-ttu-id="d4454-162">La plantilla usada para el nombre del dispositivo de piloto automático.</span><span class="sxs-lookup"><span data-stu-id="d4454-162">The template used to name the AutoPilot Device.</span></span> <span data-ttu-id="d4454-163">Esto puede ser un texto personalizado y también puede contener el número de serie del dispositivo, o bien un número generado aleatoriamente.</span><span class="sxs-lookup"><span data-stu-id="d4454-163">This can be a custom text and can also contain either the serial number of the device, or a randomly generated number.</span></span> <span data-ttu-id="d4454-164">La longitud total del texto generado por la plantilla puede ser no más de 15 caracteres.</span><span class="sxs-lookup"><span data-stu-id="d4454-164">The total length of the text generated by the template can be no more than 15 characters.</span></span> <span data-ttu-id="d4454-165">Se hereda de [windowsAutopilotDeploymentProfile](../resources/intune-enrollment-windowsautopilotdeploymentprofile.md)</span><span class="sxs-lookup"><span data-stu-id="d4454-165">Inherited from [windowsAutopilotDeploymentProfile](../resources/intune-enrollment-windowsautopilotdeploymentprofile.md)</span></span>|



## <a name="response"></a><span data-ttu-id="d4454-166">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d4454-166">Response</span></span>
<span data-ttu-id="d4454-167">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto actualizado [azureADWindowsAutopilotDeploymentProfile](../resources/intune-enrollment-azureadwindowsautopilotdeploymentprofile.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d4454-167">If successful, this method returns a `200 OK` response code and an updated [azureADWindowsAutopilotDeploymentProfile](../resources/intune-enrollment-azureadwindowsautopilotdeploymentprofile.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="d4454-168">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d4454-168">Example</span></span>
### <a name="request"></a><span data-ttu-id="d4454-169">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d4454-169">Request</span></span>
<span data-ttu-id="d4454-170">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d4454-170">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/windowsAutopilotDeploymentProfiles/{windowsAutopilotDeploymentProfileId}
Content-type: application/json
Content-length: 1021

{
  "displayName": "Display Name value",
  "description": "Description value",
  "language": "Language value",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "outOfBoxExperienceSettings": {
    "@odata.type": "microsoft.graph.outOfBoxExperienceSettings",
    "hidePrivacySettings": true,
    "hideEULA": true,
    "userType": "standard",
    "deviceUsageType": "shared",
    "skipKeyboardSelectionPage": true,
    "hideEscapeLink": true
  },
  "enrollmentStatusScreenSettings": {
    "@odata.type": "microsoft.graph.windowsEnrollmentStatusScreenSettings",
    "hideInstallationProgress": true,
    "allowDeviceUseBeforeProfileAndAppInstallComplete": true,
    "blockDeviceSetupRetryByUser": true,
    "allowLogCollectionOnInstallFailure": true,
    "customErrorMessage": "Custom Error Message value",
    "installProgressTimeoutInMinutes": 15,
    "allowDeviceUseOnInstallFailure": true
  },
  "extractHardwareHash": true,
  "deviceNameTemplate": "Device Name Template value"
}
```

### <a name="response"></a><span data-ttu-id="d4454-171">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d4454-171">Response</span></span>
<span data-ttu-id="d4454-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="d4454-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1208

{
  "@odata.type": "#microsoft.graph.azureADWindowsAutopilotDeploymentProfile",
  "id": "e2ec4e69-4e69-e2ec-694e-ece2694eece2",
  "displayName": "Display Name value",
  "description": "Description value",
  "language": "Language value",
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "outOfBoxExperienceSettings": {
    "@odata.type": "microsoft.graph.outOfBoxExperienceSettings",
    "hidePrivacySettings": true,
    "hideEULA": true,
    "userType": "standard",
    "deviceUsageType": "shared",
    "skipKeyboardSelectionPage": true,
    "hideEscapeLink": true
  },
  "enrollmentStatusScreenSettings": {
    "@odata.type": "microsoft.graph.windowsEnrollmentStatusScreenSettings",
    "hideInstallationProgress": true,
    "allowDeviceUseBeforeProfileAndAppInstallComplete": true,
    "blockDeviceSetupRetryByUser": true,
    "allowLogCollectionOnInstallFailure": true,
    "customErrorMessage": "Custom Error Message value",
    "installProgressTimeoutInMinutes": 15,
    "allowDeviceUseOnInstallFailure": true
  },
  "extractHardwareHash": true,
  "deviceNameTemplate": "Device Name Template value"
}
```





