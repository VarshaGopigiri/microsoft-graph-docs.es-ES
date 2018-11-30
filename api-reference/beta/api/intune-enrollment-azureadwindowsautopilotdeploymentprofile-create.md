---
title: Crear azureADWindowsAutopilotDeploymentProfile
description: Crear un nuevo objeto azureADWindowsAutopilotDeploymentProfile.
ms.openlocfilehash: 7984dd9d1221ff27937fc366289b9c3f64ef20ca
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086051"
---
# <a name="create-azureadwindowsautopilotdeploymentprofile"></a><span data-ttu-id="71e51-103">Crear azureADWindowsAutopilotDeploymentProfile</span><span class="sxs-lookup"><span data-stu-id="71e51-103">Create azureADWindowsAutopilotDeploymentProfile</span></span>

> <span data-ttu-id="71e51-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="71e51-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="71e51-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="71e51-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="71e51-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="71e51-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="71e51-107">Crear un nuevo objeto [azureADWindowsAutopilotDeploymentProfile](../resources/intune-enrollment-azureadwindowsautopilotdeploymentprofile.md) .</span><span class="sxs-lookup"><span data-stu-id="71e51-107">Create a new [azureADWindowsAutopilotDeploymentProfile](../resources/intune-enrollment-azureadwindowsautopilotdeploymentprofile.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="71e51-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="71e51-108">Prerequisites</span></span>
<span data-ttu-id="71e51-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="71e51-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="71e51-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="71e51-111">Permission type</span></span>|<span data-ttu-id="71e51-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="71e51-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="71e51-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="71e51-113">Delegated (work or school account)</span></span>|<span data-ttu-id="71e51-114">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="71e51-114">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="71e51-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="71e51-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="71e51-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="71e51-116">Not supported.</span></span>|
|<span data-ttu-id="71e51-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="71e51-117">Application</span></span>|<span data-ttu-id="71e51-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="71e51-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="71e51-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="71e51-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/windowsAutopilotDeploymentProfiles
```

## <a name="request-headers"></a><span data-ttu-id="71e51-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="71e51-120">Request headers</span></span>
|<span data-ttu-id="71e51-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="71e51-121">Header</span></span>|<span data-ttu-id="71e51-122">Valor</span><span class="sxs-lookup"><span data-stu-id="71e51-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="71e51-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="71e51-123">Authorization</span></span>|<span data-ttu-id="71e51-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="71e51-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="71e51-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="71e51-125">Accept</span></span>|<span data-ttu-id="71e51-126">application/json</span><span class="sxs-lookup"><span data-stu-id="71e51-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="71e51-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="71e51-127">Request body</span></span>
<span data-ttu-id="71e51-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto azureADWindowsAutopilotDeploymentProfile.</span><span class="sxs-lookup"><span data-stu-id="71e51-128">In the request body, supply a JSON representation for the azureADWindowsAutopilotDeploymentProfile object.</span></span>

<span data-ttu-id="71e51-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el azureADWindowsAutopilotDeploymentProfile.</span><span class="sxs-lookup"><span data-stu-id="71e51-129">The following table shows the properties that are required when you create the azureADWindowsAutopilotDeploymentProfile.</span></span>

|<span data-ttu-id="71e51-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="71e51-130">Property</span></span>|<span data-ttu-id="71e51-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="71e51-131">Type</span></span>|<span data-ttu-id="71e51-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="71e51-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="71e51-133">id</span><span class="sxs-lookup"><span data-stu-id="71e51-133">id</span></span>|<span data-ttu-id="71e51-134">String</span><span class="sxs-lookup"><span data-stu-id="71e51-134">String</span></span>|<span data-ttu-id="71e51-135">Clave de perfil se hereda de [windowsAutopilotDeploymentProfile](../resources/intune-enrollment-windowsautopilotdeploymentprofile.md)</span><span class="sxs-lookup"><span data-stu-id="71e51-135">Profile Key Inherited from [windowsAutopilotDeploymentProfile](../resources/intune-enrollment-windowsautopilotdeploymentprofile.md)</span></span>|
|<span data-ttu-id="71e51-136">displayName</span><span class="sxs-lookup"><span data-stu-id="71e51-136">displayName</span></span>|<span data-ttu-id="71e51-137">String</span><span class="sxs-lookup"><span data-stu-id="71e51-137">String</span></span>|<span data-ttu-id="71e51-138">Nombre del perfil Inherited desde [windowsAutopilotDeploymentProfile](../resources/intune-enrollment-windowsautopilotdeploymentprofile.md)</span><span class="sxs-lookup"><span data-stu-id="71e51-138">Name of the profile Inherited from [windowsAutopilotDeploymentProfile](../resources/intune-enrollment-windowsautopilotdeploymentprofile.md)</span></span>|
|<span data-ttu-id="71e51-139">descripción</span><span class="sxs-lookup"><span data-stu-id="71e51-139">description</span></span>|<span data-ttu-id="71e51-140">String</span><span class="sxs-lookup"><span data-stu-id="71e51-140">String</span></span>|<span data-ttu-id="71e51-141">Descripción del perfil Inherited desde [windowsAutopilotDeploymentProfile](../resources/intune-enrollment-windowsautopilotdeploymentprofile.md)</span><span class="sxs-lookup"><span data-stu-id="71e51-141">Description of the profile Inherited from [windowsAutopilotDeploymentProfile](../resources/intune-enrollment-windowsautopilotdeploymentprofile.md)</span></span>|
|<span data-ttu-id="71e51-142">language</span><span class="sxs-lookup"><span data-stu-id="71e51-142">language</span></span>|<span data-ttu-id="71e51-143">String</span><span class="sxs-lookup"><span data-stu-id="71e51-143">String</span></span>|<span data-ttu-id="71e51-144">Idioma configurado en el dispositivo Inherited desde [windowsAutopilotDeploymentProfile](../resources/intune-enrollment-windowsautopilotdeploymentprofile.md)</span><span class="sxs-lookup"><span data-stu-id="71e51-144">Language configured on the device Inherited from [windowsAutopilotDeploymentProfile](../resources/intune-enrollment-windowsautopilotdeploymentprofile.md)</span></span>|
|<span data-ttu-id="71e51-145">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="71e51-145">createdDateTime</span></span>|<span data-ttu-id="71e51-146">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="71e51-146">DateTimeOffset</span></span>|<span data-ttu-id="71e51-147">Hora de creación del perfil Inherited desde [windowsAutopilotDeploymentProfile](../resources/intune-enrollment-windowsautopilotdeploymentprofile.md)</span><span class="sxs-lookup"><span data-stu-id="71e51-147">Profile creation time Inherited from [windowsAutopilotDeploymentProfile](../resources/intune-enrollment-windowsautopilotdeploymentprofile.md)</span></span>|
|<span data-ttu-id="71e51-148">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="71e51-148">lastModifiedDateTime</span></span>|<span data-ttu-id="71e51-149">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="71e51-149">DateTimeOffset</span></span>|<span data-ttu-id="71e51-150">Perfil modificó por última vez tiempo Inherited desde [windowsAutopilotDeploymentProfile](../resources/intune-enrollment-windowsautopilotdeploymentprofile.md)</span><span class="sxs-lookup"><span data-stu-id="71e51-150">Profile last modified time Inherited from [windowsAutopilotDeploymentProfile](../resources/intune-enrollment-windowsautopilotdeploymentprofile.md)</span></span>|
|<span data-ttu-id="71e51-151">outOfBoxExperienceSettings</span><span class="sxs-lookup"><span data-stu-id="71e51-151">outOfBoxExperienceSettings</span></span>|[<span data-ttu-id="71e51-152">outOfBoxExperienceSettings</span><span class="sxs-lookup"><span data-stu-id="71e51-152">outOfBoxExperienceSettings</span></span>](../resources/intune-enrollment-outofboxexperiencesettings.md)|<span data-ttu-id="71e51-153">Rápida configuración Inherited desde [windowsAutopilotDeploymentProfile](../resources/intune-enrollment-windowsautopilotdeploymentprofile.md)</span><span class="sxs-lookup"><span data-stu-id="71e51-153">Out of box experience setting Inherited from [windowsAutopilotDeploymentProfile](../resources/intune-enrollment-windowsautopilotdeploymentprofile.md)</span></span>|
|<span data-ttu-id="71e51-154">enrollmentStatusScreenSettings</span><span class="sxs-lookup"><span data-stu-id="71e51-154">enrollmentStatusScreenSettings</span></span>|[<span data-ttu-id="71e51-155">windowsEnrollmentStatusScreenSettings</span><span class="sxs-lookup"><span data-stu-id="71e51-155">windowsEnrollmentStatusScreenSettings</span></span>](../resources/intune-enrollment-windowsenrollmentstatusscreensettings.md)|<span data-ttu-id="71e51-156">Pantalla de estado de inscripción configuración Inherited desde [windowsAutopilotDeploymentProfile](../resources/intune-enrollment-windowsautopilotdeploymentprofile.md)</span><span class="sxs-lookup"><span data-stu-id="71e51-156">Enrollment status screen setting Inherited from [windowsAutopilotDeploymentProfile](../resources/intune-enrollment-windowsautopilotdeploymentprofile.md)</span></span>|
|<span data-ttu-id="71e51-157">extractHardwareHash</span><span class="sxs-lookup"><span data-stu-id="71e51-157">extractHardwareHash</span></span>|<span data-ttu-id="71e51-158">Booleano</span><span class="sxs-lookup"><span data-stu-id="71e51-158">Boolean</span></span>|<span data-ttu-id="71e51-159">Extracción de HardwareHash para el perfil Inherited desde [windowsAutopilotDeploymentProfile](../resources/intune-enrollment-windowsautopilotdeploymentprofile.md)</span><span class="sxs-lookup"><span data-stu-id="71e51-159">HardwareHash Extraction for the profile Inherited from [windowsAutopilotDeploymentProfile](../resources/intune-enrollment-windowsautopilotdeploymentprofile.md)</span></span>|
|<span data-ttu-id="71e51-160">deviceNameTemplate</span><span class="sxs-lookup"><span data-stu-id="71e51-160">deviceNameTemplate</span></span>|<span data-ttu-id="71e51-161">String</span><span class="sxs-lookup"><span data-stu-id="71e51-161">String</span></span>|<span data-ttu-id="71e51-162">La plantilla usada para el nombre del dispositivo de piloto automático.</span><span class="sxs-lookup"><span data-stu-id="71e51-162">The template used to name the AutoPilot Device.</span></span> <span data-ttu-id="71e51-163">Esto puede ser un texto personalizado y también puede contener el número de serie del dispositivo, o bien un número generado aleatoriamente.</span><span class="sxs-lookup"><span data-stu-id="71e51-163">This can be a custom text and can also contain either the serial number of the device, or a randomly generated number.</span></span> <span data-ttu-id="71e51-164">La longitud total del texto generado por la plantilla puede ser no más de 15 caracteres.</span><span class="sxs-lookup"><span data-stu-id="71e51-164">The total length of the text generated by the template can be no more than 15 characters.</span></span> <span data-ttu-id="71e51-165">Se hereda de [windowsAutopilotDeploymentProfile](../resources/intune-enrollment-windowsautopilotdeploymentprofile.md)</span><span class="sxs-lookup"><span data-stu-id="71e51-165">Inherited from [windowsAutopilotDeploymentProfile](../resources/intune-enrollment-windowsautopilotdeploymentprofile.md)</span></span>|



## <a name="response"></a><span data-ttu-id="71e51-166">Respuesta</span><span class="sxs-lookup"><span data-stu-id="71e51-166">Response</span></span>
<span data-ttu-id="71e51-167">Si tiene éxito, este método devuelve una `201 Created` código de respuesta y un objeto [azureADWindowsAutopilotDeploymentProfile](../resources/intune-enrollment-azureadwindowsautopilotdeploymentprofile.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="71e51-167">If successful, this method returns a `201 Created` response code and a [azureADWindowsAutopilotDeploymentProfile](../resources/intune-enrollment-azureadwindowsautopilotdeploymentprofile.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="71e51-168">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="71e51-168">Example</span></span>
### <a name="request"></a><span data-ttu-id="71e51-169">Solicitud</span><span class="sxs-lookup"><span data-stu-id="71e51-169">Request</span></span>
<span data-ttu-id="71e51-170">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="71e51-170">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/windowsAutopilotDeploymentProfiles
Content-type: application/json
Content-length: 1100

{
  "@odata.type": "#microsoft.graph.azureADWindowsAutopilotDeploymentProfile",
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

### <a name="response"></a><span data-ttu-id="71e51-171">Respuesta</span><span class="sxs-lookup"><span data-stu-id="71e51-171">Response</span></span>
<span data-ttu-id="71e51-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="71e51-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
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





