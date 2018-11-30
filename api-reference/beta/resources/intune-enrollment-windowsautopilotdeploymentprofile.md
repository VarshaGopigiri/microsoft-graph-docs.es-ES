---
title: tipo de recurso windowsAutopilotDeploymentProfile
description: Perfil de implementación piloto automático de Windows
ms.openlocfilehash: ed109af370d73d22d46198b206ba42dc4ebab2da
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084513"
---
# <a name="windowsautopilotdeploymentprofile-resource-type"></a><span data-ttu-id="cf410-103">tipo de recurso windowsAutopilotDeploymentProfile</span><span class="sxs-lookup"><span data-stu-id="cf410-103">windowsAutopilotDeploymentProfile resource type</span></span>

> <span data-ttu-id="cf410-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="cf410-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="cf410-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="cf410-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="cf410-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="cf410-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="cf410-107">Perfil de implementación piloto automático de Windows</span><span class="sxs-lookup"><span data-stu-id="cf410-107">Windows Autopilot Deployment Profile</span></span>
## <a name="methods"></a><span data-ttu-id="cf410-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="cf410-108">Methods</span></span>
|<span data-ttu-id="cf410-109">Método</span><span class="sxs-lookup"><span data-stu-id="cf410-109">Method</span></span>|<span data-ttu-id="cf410-110">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cf410-110">Return Type</span></span>|<span data-ttu-id="cf410-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="cf410-111">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="cf410-112">Obtener windowsAutopilotDeploymentProfile</span><span class="sxs-lookup"><span data-stu-id="cf410-112">Get windowsAutopilotDeploymentProfile</span></span>](../api/intune-enrollment-windowsautopilotdeploymentprofile-get.md)|[<span data-ttu-id="cf410-113">windowsAutopilotDeploymentProfile</span><span class="sxs-lookup"><span data-stu-id="cf410-113">windowsAutopilotDeploymentProfile</span></span>](../resources/intune-enrollment-windowsautopilotdeploymentprofile.md)|<span data-ttu-id="cf410-114">Leer las propiedades y las relaciones del objeto [windowsAutopilotDeploymentProfile](../resources/intune-enrollment-windowsautopilotdeploymentprofile.md) .</span><span class="sxs-lookup"><span data-stu-id="cf410-114">Read properties and relationships of the [windowsAutopilotDeploymentProfile](../resources/intune-enrollment-windowsautopilotdeploymentprofile.md) object.</span></span>|
|[<span data-ttu-id="cf410-115">Acción assign</span><span class="sxs-lookup"><span data-stu-id="cf410-115">assign action</span></span>](../api/intune-enrollment-windowsautopilotdeploymentprofile-assign.md)|<span data-ttu-id="cf410-116">Ninguno</span><span class="sxs-lookup"><span data-stu-id="cf410-116">None</span></span>|<span data-ttu-id="cf410-117">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="cf410-117">Not yet documented</span></span>|

## <a name="properties"></a><span data-ttu-id="cf410-118">Propiedades</span><span class="sxs-lookup"><span data-stu-id="cf410-118">Properties</span></span>
|<span data-ttu-id="cf410-119">Propiedad</span><span class="sxs-lookup"><span data-stu-id="cf410-119">Property</span></span>|<span data-ttu-id="cf410-120">Tipo</span><span class="sxs-lookup"><span data-stu-id="cf410-120">Type</span></span>|<span data-ttu-id="cf410-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="cf410-121">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="cf410-122">id</span><span class="sxs-lookup"><span data-stu-id="cf410-122">id</span></span>|<span data-ttu-id="cf410-123">String</span><span class="sxs-lookup"><span data-stu-id="cf410-123">String</span></span>|<span data-ttu-id="cf410-124">Clave de perfil</span><span class="sxs-lookup"><span data-stu-id="cf410-124">Profile Key</span></span>|
|<span data-ttu-id="cf410-125">displayName</span><span class="sxs-lookup"><span data-stu-id="cf410-125">displayName</span></span>|<span data-ttu-id="cf410-126">String</span><span class="sxs-lookup"><span data-stu-id="cf410-126">String</span></span>|<span data-ttu-id="cf410-127">Nombre del perfil</span><span class="sxs-lookup"><span data-stu-id="cf410-127">Name of the profile</span></span>|
|<span data-ttu-id="cf410-128">descripción</span><span class="sxs-lookup"><span data-stu-id="cf410-128">description</span></span>|<span data-ttu-id="cf410-129">String</span><span class="sxs-lookup"><span data-stu-id="cf410-129">String</span></span>|<span data-ttu-id="cf410-130">Descripción del perfil</span><span class="sxs-lookup"><span data-stu-id="cf410-130">Description of the profile</span></span>|
|<span data-ttu-id="cf410-131">language</span><span class="sxs-lookup"><span data-stu-id="cf410-131">language</span></span>|<span data-ttu-id="cf410-132">String</span><span class="sxs-lookup"><span data-stu-id="cf410-132">String</span></span>|<span data-ttu-id="cf410-133">Idioma configurado en el dispositivo</span><span class="sxs-lookup"><span data-stu-id="cf410-133">Language configured on the device</span></span>|
|<span data-ttu-id="cf410-134">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="cf410-134">createdDateTime</span></span>|<span data-ttu-id="cf410-135">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="cf410-135">DateTimeOffset</span></span>|<span data-ttu-id="cf410-136">Hora de creación de perfiles</span><span class="sxs-lookup"><span data-stu-id="cf410-136">Profile creation time</span></span>|
|<span data-ttu-id="cf410-137">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="cf410-137">lastModifiedDateTime</span></span>|<span data-ttu-id="cf410-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="cf410-138">DateTimeOffset</span></span>|<span data-ttu-id="cf410-139">Perfil modificó por última vez el tiempo</span><span class="sxs-lookup"><span data-stu-id="cf410-139">Profile last modified time</span></span>|
|<span data-ttu-id="cf410-140">outOfBoxExperienceSettings</span><span class="sxs-lookup"><span data-stu-id="cf410-140">outOfBoxExperienceSettings</span></span>|[<span data-ttu-id="cf410-141">outOfBoxExperienceSettings</span><span class="sxs-lookup"><span data-stu-id="cf410-141">outOfBoxExperienceSettings</span></span>](../resources/intune-enrollment-outofboxexperiencesettings.md)|<span data-ttu-id="cf410-142">Fuera de la experiencia del cuadro Configuración</span><span class="sxs-lookup"><span data-stu-id="cf410-142">Out of box experience setting</span></span>|
|<span data-ttu-id="cf410-143">enrollmentStatusScreenSettings</span><span class="sxs-lookup"><span data-stu-id="cf410-143">enrollmentStatusScreenSettings</span></span>|[<span data-ttu-id="cf410-144">windowsEnrollmentStatusScreenSettings</span><span class="sxs-lookup"><span data-stu-id="cf410-144">windowsEnrollmentStatusScreenSettings</span></span>](../resources/intune-enrollment-windowsenrollmentstatusscreensettings.md)|<span data-ttu-id="cf410-145">Configuración de pantalla de estado de inscripción</span><span class="sxs-lookup"><span data-stu-id="cf410-145">Enrollment status screen setting</span></span>|
|<span data-ttu-id="cf410-146">extractHardwareHash</span><span class="sxs-lookup"><span data-stu-id="cf410-146">extractHardwareHash</span></span>|<span data-ttu-id="cf410-147">Booleano</span><span class="sxs-lookup"><span data-stu-id="cf410-147">Boolean</span></span>|<span data-ttu-id="cf410-148">Extracción de HardwareHash para el perfil</span><span class="sxs-lookup"><span data-stu-id="cf410-148">HardwareHash Extraction for the profile</span></span>|
|<span data-ttu-id="cf410-149">deviceNameTemplate</span><span class="sxs-lookup"><span data-stu-id="cf410-149">deviceNameTemplate</span></span>|<span data-ttu-id="cf410-150">String</span><span class="sxs-lookup"><span data-stu-id="cf410-150">String</span></span>|<span data-ttu-id="cf410-151">La plantilla usada para el nombre del dispositivo de piloto automático.</span><span class="sxs-lookup"><span data-stu-id="cf410-151">The template used to name the AutoPilot Device.</span></span> <span data-ttu-id="cf410-152">Esto puede ser un texto personalizado y también puede contener el número de serie del dispositivo, o bien un número generado aleatoriamente.</span><span class="sxs-lookup"><span data-stu-id="cf410-152">This can be a custom text and can also contain either the serial number of the device, or a randomly generated number.</span></span> <span data-ttu-id="cf410-153">La longitud total del texto generado por la plantilla puede ser no más de 15 caracteres.</span><span class="sxs-lookup"><span data-stu-id="cf410-153">The total length of the text generated by the template can be no more than 15 characters.</span></span>|

## <a name="relationships"></a><span data-ttu-id="cf410-154">Relaciones</span><span class="sxs-lookup"><span data-stu-id="cf410-154">Relationships</span></span>
|<span data-ttu-id="cf410-155">Relación</span><span class="sxs-lookup"><span data-stu-id="cf410-155">Relationship</span></span>|<span data-ttu-id="cf410-156">Tipo</span><span class="sxs-lookup"><span data-stu-id="cf410-156">Type</span></span>|<span data-ttu-id="cf410-157">Descripción</span><span class="sxs-lookup"><span data-stu-id="cf410-157">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="cf410-158">assignedDevices</span><span class="sxs-lookup"><span data-stu-id="cf410-158">assignedDevices</span></span>|<span data-ttu-id="cf410-159">colección de [windowsAutopilotDeviceIdentity](../resources/intune-enrollment-windowsautopilotdeviceidentity.md)</span><span class="sxs-lookup"><span data-stu-id="cf410-159">[windowsAutopilotDeviceIdentity](../resources/intune-enrollment-windowsautopilotdeviceidentity.md) collection</span></span>|<span data-ttu-id="cf410-160">La lista de dispositivos asignados para el perfil.</span><span class="sxs-lookup"><span data-stu-id="cf410-160">The list of assigned devices for the profile.</span></span>|
|<span data-ttu-id="cf410-161">asignaciones</span><span class="sxs-lookup"><span data-stu-id="cf410-161">assignments</span></span>|<span data-ttu-id="cf410-162">colección de [windowsAutopilotDeploymentProfileAssignment](../resources/intune-enrollment-windowsautopilotdeploymentprofileassignment.md)</span><span class="sxs-lookup"><span data-stu-id="cf410-162">[windowsAutopilotDeploymentProfileAssignment](../resources/intune-enrollment-windowsautopilotdeploymentprofileassignment.md) collection</span></span>|<span data-ttu-id="cf410-163">La lista de las asignaciones de grupo para el perfil.</span><span class="sxs-lookup"><span data-stu-id="cf410-163">The list of group assignments for the profile.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="cf410-164">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="cf410-164">JSON Representation</span></span>
<span data-ttu-id="cf410-165">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="cf410-165">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.windowsAutopilotDeploymentProfile"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.windowsAutopilotDeploymentProfile",
  "id": "String (identifier)",
  "displayName": "String",
  "description": "String",
  "language": "String",
  "createdDateTime": "String (timestamp)",
  "lastModifiedDateTime": "String (timestamp)",
  "outOfBoxExperienceSettings": {
    "@odata.type": "microsoft.graph.outOfBoxExperienceSettings",
    "hidePrivacySettings": true,
    "hideEULA": true,
    "userType": "String",
    "deviceUsageType": "String",
    "skipKeyboardSelectionPage": true,
    "hideEscapeLink": true
  },
  "enrollmentStatusScreenSettings": {
    "@odata.type": "microsoft.graph.windowsEnrollmentStatusScreenSettings",
    "hideInstallationProgress": true,
    "allowDeviceUseBeforeProfileAndAppInstallComplete": true,
    "blockDeviceSetupRetryByUser": true,
    "allowLogCollectionOnInstallFailure": true,
    "customErrorMessage": "String",
    "installProgressTimeoutInMinutes": 1024,
    "allowDeviceUseOnInstallFailure": true
  },
  "extractHardwareHash": true,
  "deviceNameTemplate": "String"
}
```





