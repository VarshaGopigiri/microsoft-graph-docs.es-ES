---
title: Crear windowsDefenderAdvancedThreatProtectionConfiguration
description: Cree un objeto windowsDefenderAdvancedThreatProtectionConfiguration.
author: tfitzmac
ms.openlocfilehash: ab9dbf4132c18e40e4a72194d1fe456a2777d02e
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27313310"
---
# <a name="create-windowsdefenderadvancedthreatprotectionconfiguration"></a><span data-ttu-id="d2817-103">Crear windowsDefenderAdvancedThreatProtectionConfiguration</span><span class="sxs-lookup"><span data-stu-id="d2817-103">Create windowsDefenderAdvancedThreatProtectionConfiguration</span></span>

> <span data-ttu-id="d2817-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="d2817-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="d2817-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="d2817-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="d2817-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="d2817-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="d2817-107">Cree un objeto [windowsDefenderAdvancedThreatProtectionConfiguration](../resources/intune-deviceconfig-windowsdefenderadvancedthreatprotectionconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="d2817-107">Create a new [windowsDefenderAdvancedThreatProtectionConfiguration](../resources/intune-deviceconfig-windowsdefenderadvancedthreatprotectionconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="d2817-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="d2817-108">Prerequisites</span></span>
<span data-ttu-id="d2817-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="d2817-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="d2817-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="d2817-111">Permission type</span></span>|<span data-ttu-id="d2817-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="d2817-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="d2817-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d2817-113">Delegated (work or school account)</span></span>|<span data-ttu-id="d2817-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d2817-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="d2817-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="d2817-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="d2817-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d2817-116">Not supported.</span></span>|
|<span data-ttu-id="d2817-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d2817-117">Application</span></span>|<span data-ttu-id="d2817-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d2817-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="d2817-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d2817-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceConfigurations
POST /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsDomainJoinConfiguration/networkAccessConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="d2817-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d2817-120">Request headers</span></span>
|<span data-ttu-id="d2817-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d2817-121">Header</span></span>|<span data-ttu-id="d2817-122">Valor</span><span class="sxs-lookup"><span data-stu-id="d2817-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="d2817-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="d2817-123">Authorization</span></span>|<span data-ttu-id="d2817-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="d2817-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="d2817-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="d2817-125">Accept</span></span>|<span data-ttu-id="d2817-126">application/json</span><span class="sxs-lookup"><span data-stu-id="d2817-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="d2817-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="d2817-127">Request body</span></span>
<span data-ttu-id="d2817-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto windowsDefenderAdvancedThreatProtectionConfiguration.</span><span class="sxs-lookup"><span data-stu-id="d2817-128">In the request body, supply a JSON representation for the windowsDefenderAdvancedThreatProtectionConfiguration object.</span></span>

<span data-ttu-id="d2817-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto windowsDefenderAdvancedThreatProtectionConfiguration.</span><span class="sxs-lookup"><span data-stu-id="d2817-129">The following table shows the properties that are required when you create the windowsDefenderAdvancedThreatProtectionConfiguration.</span></span>

|<span data-ttu-id="d2817-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d2817-130">Property</span></span>|<span data-ttu-id="d2817-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="d2817-131">Type</span></span>|<span data-ttu-id="d2817-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="d2817-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="d2817-133">id</span><span class="sxs-lookup"><span data-stu-id="d2817-133">id</span></span>|<span data-ttu-id="d2817-134">String</span><span class="sxs-lookup"><span data-stu-id="d2817-134">String</span></span>|<span data-ttu-id="d2817-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="d2817-135">Key of the entity.</span></span> <span data-ttu-id="d2817-136">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="d2817-136">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="d2817-137">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="d2817-137">lastModifiedDateTime</span></span>|<span data-ttu-id="d2817-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="d2817-138">DateTimeOffset</span></span>|<span data-ttu-id="d2817-139">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="d2817-139">DateTime the object was last modified.</span></span> <span data-ttu-id="d2817-140">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="d2817-140">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="d2817-141">roleScopeTagIds</span><span class="sxs-lookup"><span data-stu-id="d2817-141">roleScopeTagIds</span></span>|<span data-ttu-id="d2817-142">Colección String</span><span class="sxs-lookup"><span data-stu-id="d2817-142">String collection</span></span>|<span data-ttu-id="d2817-143">Lista de etiquetas de ámbito para esta instancia de entidad.</span><span class="sxs-lookup"><span data-stu-id="d2817-143">List of Scope Tags for this Entity instance.</span></span> <span data-ttu-id="d2817-144">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="d2817-144">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="d2817-145">supportsScopeTags</span><span class="sxs-lookup"><span data-stu-id="d2817-145">supportsScopeTags</span></span>|<span data-ttu-id="d2817-146">Boolean</span><span class="sxs-lookup"><span data-stu-id="d2817-146">Boolean</span></span>|<span data-ttu-id="d2817-147">Indica si la configuración del dispositivo subyacente admite la asignación de etiquetas de ámbito.</span><span class="sxs-lookup"><span data-stu-id="d2817-147">Indicates whether or not the underlying Device Configuration supports the assignment of scope tags.</span></span> <span data-ttu-id="d2817-148">No se permite la asignación a la propiedad ScopeTags cuando este valor es false y entidades no estará visibles para los usuarios con ámbito.</span><span class="sxs-lookup"><span data-stu-id="d2817-148">Assigning to the ScopeTags property is not allowed when this value is false and entities will not be visible to scoped users.</span></span> <span data-ttu-id="d2817-149">Esto se produce para las directivas de heredado creadas en Silverlight y se puede resolver por eliminar y volver a crear la directiva en el Portal de Azure.</span><span class="sxs-lookup"><span data-stu-id="d2817-149">This occurs for Legacy policies created in Silverlight and can be resolved by deleting and recreating the policy in the Azure Portal.</span></span> <span data-ttu-id="d2817-150">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="d2817-150">This property is read-only.</span></span> <span data-ttu-id="d2817-151">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="d2817-151">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="d2817-152">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="d2817-152">createdDateTime</span></span>|<span data-ttu-id="d2817-153">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="d2817-153">DateTimeOffset</span></span>|<span data-ttu-id="d2817-154">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="d2817-154">DateTime the object was created.</span></span> <span data-ttu-id="d2817-155">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="d2817-155">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="d2817-156">descripción</span><span class="sxs-lookup"><span data-stu-id="d2817-156">description</span></span>|<span data-ttu-id="d2817-157">String</span><span class="sxs-lookup"><span data-stu-id="d2817-157">String</span></span>|<span data-ttu-id="d2817-158">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d2817-158">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="d2817-159">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="d2817-159">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="d2817-160">displayName</span><span class="sxs-lookup"><span data-stu-id="d2817-160">displayName</span></span>|<span data-ttu-id="d2817-161">String</span><span class="sxs-lookup"><span data-stu-id="d2817-161">String</span></span>|<span data-ttu-id="d2817-162">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d2817-162">Admin provided name of the device configuration.</span></span> <span data-ttu-id="d2817-163">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="d2817-163">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="d2817-164">version</span><span class="sxs-lookup"><span data-stu-id="d2817-164">version</span></span>|<span data-ttu-id="d2817-165">Int32</span><span class="sxs-lookup"><span data-stu-id="d2817-165">Int32</span></span>|<span data-ttu-id="d2817-166">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d2817-166">Version of the device configuration.</span></span> <span data-ttu-id="d2817-167">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="d2817-167">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="d2817-168">advancedThreatProtectionOnboardingBlob</span><span class="sxs-lookup"><span data-stu-id="d2817-168">advancedThreatProtectionOnboardingBlob</span></span>|<span data-ttu-id="d2817-169">String</span><span class="sxs-lookup"><span data-stu-id="d2817-169">String</span></span>|<span data-ttu-id="d2817-170">Windows Defender AdvancedThreatProtection incorporación Blob.</span><span class="sxs-lookup"><span data-stu-id="d2817-170">Windows Defender AdvancedThreatProtection Onboarding Blob.</span></span>|
|<span data-ttu-id="d2817-171">advancedThreatProtectionOnboardingFilename</span><span class="sxs-lookup"><span data-stu-id="d2817-171">advancedThreatProtectionOnboardingFilename</span></span>|<span data-ttu-id="d2817-172">String</span><span class="sxs-lookup"><span data-stu-id="d2817-172">String</span></span>|<span data-ttu-id="d2817-173">Nombre del archivo desde el que se obtuvo de AdvancedThreatProtectionOnboardingBlob.</span><span class="sxs-lookup"><span data-stu-id="d2817-173">Name of the file from which AdvancedThreatProtectionOnboardingBlob was obtained.</span></span>|
|<span data-ttu-id="d2817-174">advancedThreatProtectionAutoPopulateOnboardingBlob</span><span class="sxs-lookup"><span data-stu-id="d2817-174">advancedThreatProtectionAutoPopulateOnboardingBlob</span></span>|<span data-ttu-id="d2817-175">Boolean</span><span class="sxs-lookup"><span data-stu-id="d2817-175">Boolean</span></span>|<span data-ttu-id="d2817-176">Automático rellenar blob de incorporación mediante programación desde el servicio de protección de amenaza avanzada</span><span class="sxs-lookup"><span data-stu-id="d2817-176">Auto populate onboarding blob programmatically from Advanced Threat protection service</span></span>|
|<span data-ttu-id="d2817-177">allowSampleSharing</span><span class="sxs-lookup"><span data-stu-id="d2817-177">allowSampleSharing</span></span>|<span data-ttu-id="d2817-178">Booleano</span><span class="sxs-lookup"><span data-stu-id="d2817-178">Boolean</span></span>|<span data-ttu-id="d2817-179">Regla "Permitir el uso compartido de muestras" de Windows Defender AdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="d2817-179">Windows Defender AdvancedThreatProtection "Allow Sample Sharing" Rule</span></span>|
|<span data-ttu-id="d2817-180">enableExpeditedTelemetryReporting</span><span class="sxs-lookup"><span data-stu-id="d2817-180">enableExpeditedTelemetryReporting</span></span>|<span data-ttu-id="d2817-181">Boolean</span><span class="sxs-lookup"><span data-stu-id="d2817-181">Boolean</span></span>|<span data-ttu-id="d2817-182">Acelere la frecuencia de informes de telemetría de Protección contra amenazas avanzada de Windows Defender.</span><span class="sxs-lookup"><span data-stu-id="d2817-182">Expedite Windows Defender Advanced Threat Protection telemetry reporting frequency.</span></span>|
|<span data-ttu-id="d2817-183">advancedThreatProtectionOffboardingBlob</span><span class="sxs-lookup"><span data-stu-id="d2817-183">advancedThreatProtectionOffboardingBlob</span></span>|<span data-ttu-id="d2817-184">String</span><span class="sxs-lookup"><span data-stu-id="d2817-184">String</span></span>|<span data-ttu-id="d2817-185">Windows Defender AdvancedThreatProtection baja de servicio Blob.</span><span class="sxs-lookup"><span data-stu-id="d2817-185">Windows Defender AdvancedThreatProtection Offboarding Blob.</span></span>|
|<span data-ttu-id="d2817-186">advancedThreatProtectionOffboardingFilename</span><span class="sxs-lookup"><span data-stu-id="d2817-186">advancedThreatProtectionOffboardingFilename</span></span>|<span data-ttu-id="d2817-187">String</span><span class="sxs-lookup"><span data-stu-id="d2817-187">String</span></span>|<span data-ttu-id="d2817-188">Nombre del archivo desde el que se obtuvo de AdvancedThreatProtectionOffboardingBlob.</span><span class="sxs-lookup"><span data-stu-id="d2817-188">Name of the file from which AdvancedThreatProtectionOffboardingBlob was obtained.</span></span>|



## <a name="response"></a><span data-ttu-id="d2817-189">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d2817-189">Response</span></span>
<span data-ttu-id="d2817-190">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [windowsDefenderAdvancedThreatProtectionConfiguration](../resources/intune-deviceconfig-windowsdefenderadvancedthreatprotectionconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d2817-190">If successful, this method returns a `201 Created` response code and a [windowsDefenderAdvancedThreatProtectionConfiguration](../resources/intune-deviceconfig-windowsdefenderadvancedthreatprotectionconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="d2817-191">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d2817-191">Example</span></span>
### <a name="request"></a><span data-ttu-id="d2817-192">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d2817-192">Request</span></span>
<span data-ttu-id="d2817-193">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d2817-193">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations
Content-type: application/json
Content-length: 894

{
  "@odata.type": "#microsoft.graph.windowsDefenderAdvancedThreatProtectionConfiguration",
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

### <a name="response"></a><span data-ttu-id="d2817-194">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d2817-194">Response</span></span>
<span data-ttu-id="d2817-p111">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="d2817-p111">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
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





