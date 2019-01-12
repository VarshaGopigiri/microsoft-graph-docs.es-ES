---
title: Actualizar windowsDefenderAdvancedThreatProtectionConfiguration
description: Actualice las propiedades de un objeto windowsDefenderAdvancedThreatProtectionConfiguration.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: dc0d6d5225b62a21bb9fe53818562cf10aa8aa73
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27949111"
---
# <a name="update-windowsdefenderadvancedthreatprotectionconfiguration"></a><span data-ttu-id="4f658-103">Actualizar windowsDefenderAdvancedThreatProtectionConfiguration</span><span class="sxs-lookup"><span data-stu-id="4f658-103">Update windowsDefenderAdvancedThreatProtectionConfiguration</span></span>

> <span data-ttu-id="4f658-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="4f658-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="4f658-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="4f658-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="4f658-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="4f658-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="4f658-107">Actualice las propiedades de un objeto [windowsDefenderAdvancedThreatProtectionConfiguration](../resources/intune-deviceconfig-windowsdefenderadvancedthreatprotectionconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="4f658-107">Update the properties of a [windowsDefenderAdvancedThreatProtectionConfiguration](../resources/intune-deviceconfig-windowsdefenderadvancedthreatprotectionconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="4f658-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="4f658-108">Prerequisites</span></span>
<span data-ttu-id="4f658-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="4f658-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="4f658-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="4f658-111">Permission type</span></span>|<span data-ttu-id="4f658-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="4f658-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="4f658-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="4f658-113">Delegated (work or school account)</span></span>|<span data-ttu-id="4f658-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="4f658-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="4f658-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="4f658-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="4f658-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="4f658-116">Not supported.</span></span>|
|<span data-ttu-id="4f658-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="4f658-117">Application</span></span>|<span data-ttu-id="4f658-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="4f658-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="4f658-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="4f658-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/groupAssignments/{deviceConfigurationGroupAssignmentId}/deviceConfiguration
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsDomainJoinConfiguration/networkAccessConfigurations/{deviceConfigurationId}
```

## <a name="request-headers"></a><span data-ttu-id="4f658-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="4f658-120">Request headers</span></span>
|<span data-ttu-id="4f658-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4f658-121">Header</span></span>|<span data-ttu-id="4f658-122">Valor</span><span class="sxs-lookup"><span data-stu-id="4f658-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="4f658-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="4f658-123">Authorization</span></span>|<span data-ttu-id="4f658-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="4f658-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="4f658-125">Accept</span><span class="sxs-lookup"><span data-stu-id="4f658-125">Accept</span></span>|<span data-ttu-id="4f658-126">application/json</span><span class="sxs-lookup"><span data-stu-id="4f658-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="4f658-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="4f658-127">Request body</span></span>
<span data-ttu-id="4f658-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto [windowsDefenderAdvancedThreatProtectionConfiguration](../resources/intune-deviceconfig-windowsdefenderadvancedthreatprotectionconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="4f658-128">In the request body, supply a JSON representation for the [windowsDefenderAdvancedThreatProtectionConfiguration](../resources/intune-deviceconfig-windowsdefenderadvancedthreatprotectionconfiguration.md) object.</span></span>

<span data-ttu-id="4f658-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [windowsDefenderAdvancedThreatProtectionConfiguration](../resources/intune-deviceconfig-windowsdefenderadvancedthreatprotectionconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="4f658-129">The following table shows the properties that are required when you create the [windowsDefenderAdvancedThreatProtectionConfiguration](../resources/intune-deviceconfig-windowsdefenderadvancedthreatprotectionconfiguration.md).</span></span>

|<span data-ttu-id="4f658-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="4f658-130">Property</span></span>|<span data-ttu-id="4f658-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="4f658-131">Type</span></span>|<span data-ttu-id="4f658-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="4f658-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="4f658-133">id</span><span class="sxs-lookup"><span data-stu-id="4f658-133">id</span></span>|<span data-ttu-id="4f658-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="4f658-134">String</span></span>|<span data-ttu-id="4f658-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="4f658-135">Key of the entity.</span></span> <span data-ttu-id="4f658-136">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="4f658-136">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="4f658-137">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="4f658-137">lastModifiedDateTime</span></span>|<span data-ttu-id="4f658-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="4f658-138">DateTimeOffset</span></span>|<span data-ttu-id="4f658-139">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="4f658-139">DateTime the object was last modified.</span></span> <span data-ttu-id="4f658-140">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="4f658-140">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="4f658-141">roleScopeTagIds</span><span class="sxs-lookup"><span data-stu-id="4f658-141">roleScopeTagIds</span></span>|<span data-ttu-id="4f658-142">Colección String</span><span class="sxs-lookup"><span data-stu-id="4f658-142">String collection</span></span>|<span data-ttu-id="4f658-143">Lista de etiquetas de ámbito para esta instancia de entidad.</span><span class="sxs-lookup"><span data-stu-id="4f658-143">List of Scope Tags for this Entity instance.</span></span> <span data-ttu-id="4f658-144">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="4f658-144">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="4f658-145">supportsScopeTags</span><span class="sxs-lookup"><span data-stu-id="4f658-145">supportsScopeTags</span></span>|<span data-ttu-id="4f658-146">Booleano</span><span class="sxs-lookup"><span data-stu-id="4f658-146">Boolean</span></span>|<span data-ttu-id="4f658-147">Indica si la configuración del dispositivo subyacente admite la asignación de etiquetas de ámbito.</span><span class="sxs-lookup"><span data-stu-id="4f658-147">Indicates whether or not the underlying Device Configuration supports the assignment of scope tags.</span></span> <span data-ttu-id="4f658-148">No se permite la asignación a la propiedad ScopeTags cuando este valor es false y entidades no estará visibles para los usuarios con ámbito.</span><span class="sxs-lookup"><span data-stu-id="4f658-148">Assigning to the ScopeTags property is not allowed when this value is false and entities will not be visible to scoped users.</span></span> <span data-ttu-id="4f658-149">Esto se produce para las directivas de heredado creadas en Silverlight y se puede resolver por eliminar y volver a crear la directiva en el Portal de Azure.</span><span class="sxs-lookup"><span data-stu-id="4f658-149">This occurs for Legacy policies created in Silverlight and can be resolved by deleting and recreating the policy in the Azure Portal.</span></span> <span data-ttu-id="4f658-150">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="4f658-150">This property is read-only.</span></span> <span data-ttu-id="4f658-151">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="4f658-151">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="4f658-152">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="4f658-152">createdDateTime</span></span>|<span data-ttu-id="4f658-153">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="4f658-153">DateTimeOffset</span></span>|<span data-ttu-id="4f658-154">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="4f658-154">DateTime the object was created.</span></span> <span data-ttu-id="4f658-155">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="4f658-155">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="4f658-156">descripción</span><span class="sxs-lookup"><span data-stu-id="4f658-156">description</span></span>|<span data-ttu-id="4f658-157">Cadena</span><span class="sxs-lookup"><span data-stu-id="4f658-157">String</span></span>|<span data-ttu-id="4f658-158">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4f658-158">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="4f658-159">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="4f658-159">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="4f658-160">displayName</span><span class="sxs-lookup"><span data-stu-id="4f658-160">displayName</span></span>|<span data-ttu-id="4f658-161">Cadena</span><span class="sxs-lookup"><span data-stu-id="4f658-161">String</span></span>|<span data-ttu-id="4f658-162">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4f658-162">Admin provided name of the device configuration.</span></span> <span data-ttu-id="4f658-163">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="4f658-163">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="4f658-164">version</span><span class="sxs-lookup"><span data-stu-id="4f658-164">version</span></span>|<span data-ttu-id="4f658-165">Int32</span><span class="sxs-lookup"><span data-stu-id="4f658-165">Int32</span></span>|<span data-ttu-id="4f658-166">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4f658-166">Version of the device configuration.</span></span> <span data-ttu-id="4f658-167">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="4f658-167">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="4f658-168">advancedThreatProtectionOnboardingBlob</span><span class="sxs-lookup"><span data-stu-id="4f658-168">advancedThreatProtectionOnboardingBlob</span></span>|<span data-ttu-id="4f658-169">Cadena</span><span class="sxs-lookup"><span data-stu-id="4f658-169">String</span></span>|<span data-ttu-id="4f658-170">Windows Defender AdvancedThreatProtection incorporación Blob.</span><span class="sxs-lookup"><span data-stu-id="4f658-170">Windows Defender AdvancedThreatProtection Onboarding Blob.</span></span>|
|<span data-ttu-id="4f658-171">advancedThreatProtectionOnboardingFilename</span><span class="sxs-lookup"><span data-stu-id="4f658-171">advancedThreatProtectionOnboardingFilename</span></span>|<span data-ttu-id="4f658-172">Cadena</span><span class="sxs-lookup"><span data-stu-id="4f658-172">String</span></span>|<span data-ttu-id="4f658-173">Nombre del archivo desde el que se obtuvo de AdvancedThreatProtectionOnboardingBlob.</span><span class="sxs-lookup"><span data-stu-id="4f658-173">Name of the file from which AdvancedThreatProtectionOnboardingBlob was obtained.</span></span>|
|<span data-ttu-id="4f658-174">advancedThreatProtectionAutoPopulateOnboardingBlob</span><span class="sxs-lookup"><span data-stu-id="4f658-174">advancedThreatProtectionAutoPopulateOnboardingBlob</span></span>|<span data-ttu-id="4f658-175">Booleano</span><span class="sxs-lookup"><span data-stu-id="4f658-175">Boolean</span></span>|<span data-ttu-id="4f658-176">Automático rellenar blob de incorporación mediante programación desde el servicio de protección de amenaza avanzada</span><span class="sxs-lookup"><span data-stu-id="4f658-176">Auto populate onboarding blob programmatically from Advanced Threat protection service</span></span>|
|<span data-ttu-id="4f658-177">allowSampleSharing</span><span class="sxs-lookup"><span data-stu-id="4f658-177">allowSampleSharing</span></span>|<span data-ttu-id="4f658-178">Booleano</span><span class="sxs-lookup"><span data-stu-id="4f658-178">Boolean</span></span>|<span data-ttu-id="4f658-179">Regla "Permitir el uso compartido de muestras" de Windows Defender AdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="4f658-179">Windows Defender AdvancedThreatProtection "Allow Sample Sharing" Rule</span></span>|
|<span data-ttu-id="4f658-180">enableExpeditedTelemetryReporting</span><span class="sxs-lookup"><span data-stu-id="4f658-180">enableExpeditedTelemetryReporting</span></span>|<span data-ttu-id="4f658-181">Booleano</span><span class="sxs-lookup"><span data-stu-id="4f658-181">Boolean</span></span>|<span data-ttu-id="4f658-182">Acelere la frecuencia de informes de telemetría de Protección contra amenazas avanzada de Windows Defender.</span><span class="sxs-lookup"><span data-stu-id="4f658-182">Expedite Windows Defender Advanced Threat Protection telemetry reporting frequency.</span></span>|
|<span data-ttu-id="4f658-183">advancedThreatProtectionOffboardingBlob</span><span class="sxs-lookup"><span data-stu-id="4f658-183">advancedThreatProtectionOffboardingBlob</span></span>|<span data-ttu-id="4f658-184">Cadena</span><span class="sxs-lookup"><span data-stu-id="4f658-184">String</span></span>|<span data-ttu-id="4f658-185">Windows Defender AdvancedThreatProtection baja de servicio Blob.</span><span class="sxs-lookup"><span data-stu-id="4f658-185">Windows Defender AdvancedThreatProtection Offboarding Blob.</span></span>|
|<span data-ttu-id="4f658-186">advancedThreatProtectionOffboardingFilename</span><span class="sxs-lookup"><span data-stu-id="4f658-186">advancedThreatProtectionOffboardingFilename</span></span>|<span data-ttu-id="4f658-187">Cadena</span><span class="sxs-lookup"><span data-stu-id="4f658-187">String</span></span>|<span data-ttu-id="4f658-188">Nombre del archivo desde el que se obtuvo de AdvancedThreatProtectionOffboardingBlob.</span><span class="sxs-lookup"><span data-stu-id="4f658-188">Name of the file from which AdvancedThreatProtectionOffboardingBlob was obtained.</span></span>|



## <a name="response"></a><span data-ttu-id="4f658-189">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4f658-189">Response</span></span>
<span data-ttu-id="4f658-190">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [windowsDefenderAdvancedThreatProtectionConfiguration](../resources/intune-deviceconfig-windowsdefenderadvancedthreatprotectionconfiguration.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4f658-190">If successful, this method returns a `200 OK` response code and an updated [windowsDefenderAdvancedThreatProtectionConfiguration](../resources/intune-deviceconfig-windowsdefenderadvancedthreatprotectionconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="4f658-191">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="4f658-191">Example</span></span>
### <a name="request"></a><span data-ttu-id="4f658-192">Solicitud</span><span class="sxs-lookup"><span data-stu-id="4f658-192">Request</span></span>
<span data-ttu-id="4f658-193">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="4f658-193">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations/{deviceConfigurationId}
Content-type: application/json
Content-length: 803

{
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "roleScopeTagIds": [
    "Role Scope Tag Ids value"
  ],
  "supportsScopeTags": true,
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "advancedThreatProtectionOnboardingBlob": "Advanced Threat Protection Onboarding Blob value",
  "advancedThreatProtectionOnboardingFilename": "Advanced Threat Protection Onboarding Filename value",
  "advancedThreatProtectionAutoPopulateOnboardingBlob": true,
  "allowSampleSharing": true,
  "enableExpeditedTelemetryReporting": true,
  "advancedThreatProtectionOffboardingBlob": "Advanced Threat Protection Offboarding Blob value",
  "advancedThreatProtectionOffboardingFilename": "Advanced Threat Protection Offboarding Filename value"
}
```

### <a name="response"></a><span data-ttu-id="4f658-194">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4f658-194">Response</span></span>
<span data-ttu-id="4f658-p111">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="4f658-p111">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1002

{
  "@odata.type": "#microsoft.graph.windowsDefenderAdvancedThreatProtectionConfiguration",
  "id": "294373aa-73aa-2943-aa73-4329aa734329",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "roleScopeTagIds": [
    "Role Scope Tag Ids value"
  ],
  "supportsScopeTags": true,
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "advancedThreatProtectionOnboardingBlob": "Advanced Threat Protection Onboarding Blob value",
  "advancedThreatProtectionOnboardingFilename": "Advanced Threat Protection Onboarding Filename value",
  "advancedThreatProtectionAutoPopulateOnboardingBlob": true,
  "allowSampleSharing": true,
  "enableExpeditedTelemetryReporting": true,
  "advancedThreatProtectionOffboardingBlob": "Advanced Threat Protection Offboarding Blob value",
  "advancedThreatProtectionOffboardingFilename": "Advanced Threat Protection Offboarding Filename value"
}
```





