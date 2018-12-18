---
title: Actualizar macOSImportedPFXCertificateProfile
description: Actualizar las propiedades de un objeto macOSImportedPFXCertificateProfile.
author: tfitzmac
ms.openlocfilehash: 842b680ad6f8d2337bfecfcd270252d216499807
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27321969"
---
# <a name="update-macosimportedpfxcertificateprofile"></a><span data-ttu-id="40aa2-103">Actualizar macOSImportedPFXCertificateProfile</span><span class="sxs-lookup"><span data-stu-id="40aa2-103">Update macOSImportedPFXCertificateProfile</span></span>

> <span data-ttu-id="40aa2-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="40aa2-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="40aa2-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="40aa2-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="40aa2-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="40aa2-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="40aa2-107">Actualizar las propiedades de un objeto [macOSImportedPFXCertificateProfile](../resources/intune-deviceconfig-macosimportedpfxcertificateprofile.md) .</span><span class="sxs-lookup"><span data-stu-id="40aa2-107">Update the properties of a [macOSImportedPFXCertificateProfile](../resources/intune-deviceconfig-macosimportedpfxcertificateprofile.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="40aa2-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="40aa2-108">Prerequisites</span></span>
<span data-ttu-id="40aa2-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="40aa2-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="40aa2-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="40aa2-111">Permission type</span></span>|<span data-ttu-id="40aa2-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="40aa2-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="40aa2-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="40aa2-113">Delegated (work or school account)</span></span>|<span data-ttu-id="40aa2-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="40aa2-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="40aa2-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="40aa2-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="40aa2-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="40aa2-116">Not supported.</span></span>|
|<span data-ttu-id="40aa2-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="40aa2-117">Application</span></span>|<span data-ttu-id="40aa2-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="40aa2-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="40aa2-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="40aa2-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/groupAssignments/{deviceConfigurationGroupAssignmentId}/deviceConfiguration
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsDomainJoinConfiguration/networkAccessConfigurations/{deviceConfigurationId}
```

## <a name="request-headers"></a><span data-ttu-id="40aa2-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="40aa2-120">Request headers</span></span>
|<span data-ttu-id="40aa2-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="40aa2-121">Header</span></span>|<span data-ttu-id="40aa2-122">Valor</span><span class="sxs-lookup"><span data-stu-id="40aa2-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="40aa2-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="40aa2-123">Authorization</span></span>|<span data-ttu-id="40aa2-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="40aa2-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="40aa2-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="40aa2-125">Accept</span></span>|<span data-ttu-id="40aa2-126">application/json</span><span class="sxs-lookup"><span data-stu-id="40aa2-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="40aa2-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="40aa2-127">Request body</span></span>
<span data-ttu-id="40aa2-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto [macOSImportedPFXCertificateProfile](../resources/intune-deviceconfig-macosimportedpfxcertificateprofile.md) .</span><span class="sxs-lookup"><span data-stu-id="40aa2-128">In the request body, supply a JSON representation for the [macOSImportedPFXCertificateProfile](../resources/intune-deviceconfig-macosimportedpfxcertificateprofile.md) object.</span></span>

<span data-ttu-id="40aa2-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el [macOSImportedPFXCertificateProfile](../resources/intune-deviceconfig-macosimportedpfxcertificateprofile.md).</span><span class="sxs-lookup"><span data-stu-id="40aa2-129">The following table shows the properties that are required when you create the [macOSImportedPFXCertificateProfile](../resources/intune-deviceconfig-macosimportedpfxcertificateprofile.md).</span></span>

|<span data-ttu-id="40aa2-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="40aa2-130">Property</span></span>|<span data-ttu-id="40aa2-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="40aa2-131">Type</span></span>|<span data-ttu-id="40aa2-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="40aa2-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="40aa2-133">id</span><span class="sxs-lookup"><span data-stu-id="40aa2-133">id</span></span>|<span data-ttu-id="40aa2-134">String</span><span class="sxs-lookup"><span data-stu-id="40aa2-134">String</span></span>|<span data-ttu-id="40aa2-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="40aa2-135">Key of the entity.</span></span> <span data-ttu-id="40aa2-136">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="40aa2-136">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="40aa2-137">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="40aa2-137">lastModifiedDateTime</span></span>|<span data-ttu-id="40aa2-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="40aa2-138">DateTimeOffset</span></span>|<span data-ttu-id="40aa2-139">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="40aa2-139">DateTime the object was last modified.</span></span> <span data-ttu-id="40aa2-140">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="40aa2-140">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="40aa2-141">roleScopeTagIds</span><span class="sxs-lookup"><span data-stu-id="40aa2-141">roleScopeTagIds</span></span>|<span data-ttu-id="40aa2-142">Colección String</span><span class="sxs-lookup"><span data-stu-id="40aa2-142">String collection</span></span>|<span data-ttu-id="40aa2-143">Lista de etiquetas de ámbito para esta instancia de entidad.</span><span class="sxs-lookup"><span data-stu-id="40aa2-143">List of Scope Tags for this Entity instance.</span></span> <span data-ttu-id="40aa2-144">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="40aa2-144">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="40aa2-145">supportsScopeTags</span><span class="sxs-lookup"><span data-stu-id="40aa2-145">supportsScopeTags</span></span>|<span data-ttu-id="40aa2-146">Boolean</span><span class="sxs-lookup"><span data-stu-id="40aa2-146">Boolean</span></span>|<span data-ttu-id="40aa2-147">Indica si la configuración del dispositivo subyacente admite la asignación de etiquetas de ámbito.</span><span class="sxs-lookup"><span data-stu-id="40aa2-147">Indicates whether or not the underlying Device Configuration supports the assignment of scope tags.</span></span> <span data-ttu-id="40aa2-148">No se permite la asignación a la propiedad ScopeTags cuando este valor es false y entidades no estará visibles para los usuarios con ámbito.</span><span class="sxs-lookup"><span data-stu-id="40aa2-148">Assigning to the ScopeTags property is not allowed when this value is false and entities will not be visible to scoped users.</span></span> <span data-ttu-id="40aa2-149">Esto se produce para las directivas de heredado creadas en Silverlight y se puede resolver por eliminar y volver a crear la directiva en el Portal de Azure.</span><span class="sxs-lookup"><span data-stu-id="40aa2-149">This occurs for Legacy policies created in Silverlight and can be resolved by deleting and recreating the policy in the Azure Portal.</span></span> <span data-ttu-id="40aa2-150">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="40aa2-150">This property is read-only.</span></span> <span data-ttu-id="40aa2-151">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="40aa2-151">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="40aa2-152">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="40aa2-152">createdDateTime</span></span>|<span data-ttu-id="40aa2-153">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="40aa2-153">DateTimeOffset</span></span>|<span data-ttu-id="40aa2-154">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="40aa2-154">DateTime the object was created.</span></span> <span data-ttu-id="40aa2-155">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="40aa2-155">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="40aa2-156">descripción</span><span class="sxs-lookup"><span data-stu-id="40aa2-156">description</span></span>|<span data-ttu-id="40aa2-157">String</span><span class="sxs-lookup"><span data-stu-id="40aa2-157">String</span></span>|<span data-ttu-id="40aa2-158">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="40aa2-158">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="40aa2-159">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="40aa2-159">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="40aa2-160">displayName</span><span class="sxs-lookup"><span data-stu-id="40aa2-160">displayName</span></span>|<span data-ttu-id="40aa2-161">String</span><span class="sxs-lookup"><span data-stu-id="40aa2-161">String</span></span>|<span data-ttu-id="40aa2-162">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="40aa2-162">Admin provided name of the device configuration.</span></span> <span data-ttu-id="40aa2-163">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="40aa2-163">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="40aa2-164">version</span><span class="sxs-lookup"><span data-stu-id="40aa2-164">version</span></span>|<span data-ttu-id="40aa2-165">Int32</span><span class="sxs-lookup"><span data-stu-id="40aa2-165">Int32</span></span>|<span data-ttu-id="40aa2-166">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="40aa2-166">Version of the device configuration.</span></span> <span data-ttu-id="40aa2-167">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="40aa2-167">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="40aa2-168">renewalThresholdPercentage</span><span class="sxs-lookup"><span data-stu-id="40aa2-168">renewalThresholdPercentage</span></span>|<span data-ttu-id="40aa2-169">Int32</span><span class="sxs-lookup"><span data-stu-id="40aa2-169">Int32</span></span>|<span data-ttu-id="40aa2-170">Porcentaje de umbral de renovación de certificado.</span><span class="sxs-lookup"><span data-stu-id="40aa2-170">Certificate renewal threshold percentage.</span></span> <span data-ttu-id="40aa2-171">Se hereda de [macOSCertificateProfileBase](../resources/intune-deviceconfig-macoscertificateprofilebase.md)</span><span class="sxs-lookup"><span data-stu-id="40aa2-171">Inherited from [macOSCertificateProfileBase](../resources/intune-deviceconfig-macoscertificateprofilebase.md)</span></span>|
|<span data-ttu-id="40aa2-172">subjectNameFormat</span><span class="sxs-lookup"><span data-stu-id="40aa2-172">subjectNameFormat</span></span>|[<span data-ttu-id="40aa2-173">appleSubjectNameFormat</span><span class="sxs-lookup"><span data-stu-id="40aa2-173">appleSubjectNameFormat</span></span>](../resources/intune-deviceconfig-applesubjectnameformat.md)|<span data-ttu-id="40aa2-174">Formato de nombre de sujeto de certificado.</span><span class="sxs-lookup"><span data-stu-id="40aa2-174">Certificate Subject Name Format.</span></span> <span data-ttu-id="40aa2-175">Se hereda de [macOSCertificateProfileBase](../resources/intune-deviceconfig-macoscertificateprofilebase.md).</span><span class="sxs-lookup"><span data-stu-id="40aa2-175">Inherited from [macOSCertificateProfileBase](../resources/intune-deviceconfig-macoscertificateprofilebase.md).</span></span> <span data-ttu-id="40aa2-176">Los valores posibles son: `commonName`, `commonNameAsEmail`, `custom`, `commonNameIncludingEmail`, `commonNameAsIMEI`, `commonNameAsSerialNumber`.</span><span class="sxs-lookup"><span data-stu-id="40aa2-176">Possible values are: `commonName`, `commonNameAsEmail`, `custom`, `commonNameIncludingEmail`, `commonNameAsIMEI`, `commonNameAsSerialNumber`.</span></span>|
|<span data-ttu-id="40aa2-177">subjectAlternativeNameType</span><span class="sxs-lookup"><span data-stu-id="40aa2-177">subjectAlternativeNameType</span></span>|[<span data-ttu-id="40aa2-178">subjectAlternativeNameType</span><span class="sxs-lookup"><span data-stu-id="40aa2-178">subjectAlternativeNameType</span></span>](../resources/intune-deviceconfig-subjectalternativenametype.md)|<span data-ttu-id="40aa2-179">Tipo de nombre alternativo de sujeto de certificado.</span><span class="sxs-lookup"><span data-stu-id="40aa2-179">Certificate Subject Alternative Name Type.</span></span> <span data-ttu-id="40aa2-180">Se hereda de [macOSCertificateProfileBase](../resources/intune-deviceconfig-macoscertificateprofilebase.md).</span><span class="sxs-lookup"><span data-stu-id="40aa2-180">Inherited from [macOSCertificateProfileBase](../resources/intune-deviceconfig-macoscertificateprofilebase.md).</span></span> <span data-ttu-id="40aa2-181">Los valores posibles son: `none`, `emailAddress`, `userPrincipalName`, `customAzureADAttribute` y `domainNameService`.</span><span class="sxs-lookup"><span data-stu-id="40aa2-181">Possible values are: `none`, `emailAddress`, `userPrincipalName`, `customAzureADAttribute`, `domainNameService`.</span></span>|
|<span data-ttu-id="40aa2-182">certificateValidityPeriodValue</span><span class="sxs-lookup"><span data-stu-id="40aa2-182">certificateValidityPeriodValue</span></span>|<span data-ttu-id="40aa2-183">Int32</span><span class="sxs-lookup"><span data-stu-id="40aa2-183">Int32</span></span>|<span data-ttu-id="40aa2-184">Valor para el período de validez del certificado.</span><span class="sxs-lookup"><span data-stu-id="40aa2-184">Value for the Certificate Validity Period.</span></span> <span data-ttu-id="40aa2-185">Se hereda de [macOSCertificateProfileBase](../resources/intune-deviceconfig-macoscertificateprofilebase.md)</span><span class="sxs-lookup"><span data-stu-id="40aa2-185">Inherited from [macOSCertificateProfileBase](../resources/intune-deviceconfig-macoscertificateprofilebase.md)</span></span>|
|<span data-ttu-id="40aa2-186">certificateValidityPeriodScale</span><span class="sxs-lookup"><span data-stu-id="40aa2-186">certificateValidityPeriodScale</span></span>|[<span data-ttu-id="40aa2-187">certificateValidityPeriodScale</span><span class="sxs-lookup"><span data-stu-id="40aa2-187">certificateValidityPeriodScale</span></span>](../resources/intune-deviceconfig-certificatevalidityperiodscale.md)|<span data-ttu-id="40aa2-188">Escala para el período de validez del certificado.</span><span class="sxs-lookup"><span data-stu-id="40aa2-188">Scale for the Certificate Validity Period.</span></span> <span data-ttu-id="40aa2-189">Se hereda de [macOSCertificateProfileBase](../resources/intune-deviceconfig-macoscertificateprofilebase.md).</span><span class="sxs-lookup"><span data-stu-id="40aa2-189">Inherited from [macOSCertificateProfileBase](../resources/intune-deviceconfig-macoscertificateprofilebase.md).</span></span> <span data-ttu-id="40aa2-190">Los valores posibles son: `days`, `months` y `years`.</span><span class="sxs-lookup"><span data-stu-id="40aa2-190">Possible values are: `days`, `months`, `years`.</span></span>|
|<span data-ttu-id="40aa2-191">intendedPurpose</span><span class="sxs-lookup"><span data-stu-id="40aa2-191">intendedPurpose</span></span>|[<span data-ttu-id="40aa2-192">intendedPurpose</span><span class="sxs-lookup"><span data-stu-id="40aa2-192">intendedPurpose</span></span>](../resources/intune-deviceconfig-intendedpurpose.md)|<span data-ttu-id="40aa2-193">Todavía no está documentada.</span><span class="sxs-lookup"><span data-stu-id="40aa2-193">Not yet documented.</span></span> <span data-ttu-id="40aa2-194">Los valores posibles son: `unassigned`, `smimeEncryption`, `smimeSigning`, `vpn` y `wifi`.</span><span class="sxs-lookup"><span data-stu-id="40aa2-194">Possible values are: `unassigned`, `smimeEncryption`, `smimeSigning`, `vpn`, `wifi`.</span></span>|



## <a name="response"></a><span data-ttu-id="40aa2-195">Respuesta</span><span class="sxs-lookup"><span data-stu-id="40aa2-195">Response</span></span>
<span data-ttu-id="40aa2-196">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto actualizado [macOSImportedPFXCertificateProfile](../resources/intune-deviceconfig-macosimportedpfxcertificateprofile.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="40aa2-196">If successful, this method returns a `200 OK` response code and an updated [macOSImportedPFXCertificateProfile](../resources/intune-deviceconfig-macosimportedpfxcertificateprofile.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="40aa2-197">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="40aa2-197">Example</span></span>
### <a name="request"></a><span data-ttu-id="40aa2-198">Solicitud</span><span class="sxs-lookup"><span data-stu-id="40aa2-198">Request</span></span>
<span data-ttu-id="40aa2-199">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="40aa2-199">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations/{deviceConfigurationId}
Content-type: application/json
Content-length: 515

{
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "roleScopeTagIds": [
    "Role Scope Tag Ids value"
  ],
  "supportsScopeTags": true,
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "renewalThresholdPercentage": 10,
  "subjectNameFormat": "commonNameAsEmail",
  "subjectAlternativeNameType": "emailAddress",
  "certificateValidityPeriodValue": 14,
  "certificateValidityPeriodScale": "months",
  "intendedPurpose": "smimeEncryption"
}
```

### <a name="response"></a><span data-ttu-id="40aa2-200">Respuesta</span><span class="sxs-lookup"><span data-stu-id="40aa2-200">Response</span></span>
<span data-ttu-id="40aa2-p117">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="40aa2-p117">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 696

{
  "@odata.type": "#microsoft.graph.macOSImportedPFXCertificateProfile",
  "id": "4175bd8c-bd8c-4175-8cbd-75418cbd7541",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "roleScopeTagIds": [
    "Role Scope Tag Ids value"
  ],
  "supportsScopeTags": true,
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "renewalThresholdPercentage": 10,
  "subjectNameFormat": "commonNameAsEmail",
  "subjectAlternativeNameType": "emailAddress",
  "certificateValidityPeriodValue": 14,
  "certificateValidityPeriodScale": "months",
  "intendedPurpose": "smimeEncryption"
}
```





