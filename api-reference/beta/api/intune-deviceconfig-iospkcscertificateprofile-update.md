---
title: Actualizar iosPkcsCertificateProfile
description: Actualizar las propiedades de un objeto iosPkcsCertificateProfile.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 1cd5426ad8d07984ff25209326d613add09cc000
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27817804"
---
# <a name="update-iospkcscertificateprofile"></a><span data-ttu-id="2758d-103">Actualizar iosPkcsCertificateProfile</span><span class="sxs-lookup"><span data-stu-id="2758d-103">Update iosPkcsCertificateProfile</span></span>

> <span data-ttu-id="2758d-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="2758d-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="2758d-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="2758d-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="2758d-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="2758d-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="2758d-107">Actualizar las propiedades de un objeto [iosPkcsCertificateProfile](../resources/intune-deviceconfig-iospkcscertificateprofile.md) .</span><span class="sxs-lookup"><span data-stu-id="2758d-107">Update the properties of a [iosPkcsCertificateProfile](../resources/intune-deviceconfig-iospkcscertificateprofile.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="2758d-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="2758d-108">Prerequisites</span></span>
<span data-ttu-id="2758d-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="2758d-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="2758d-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="2758d-111">Permission type</span></span>|<span data-ttu-id="2758d-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="2758d-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="2758d-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="2758d-113">Delegated (work or school account)</span></span>|<span data-ttu-id="2758d-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="2758d-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="2758d-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="2758d-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="2758d-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2758d-116">Not supported.</span></span>|
|<span data-ttu-id="2758d-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="2758d-117">Application</span></span>|<span data-ttu-id="2758d-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2758d-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="2758d-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="2758d-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/groupAssignments/{deviceConfigurationGroupAssignmentId}/deviceConfiguration
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsDomainJoinConfiguration/networkAccessConfigurations/{deviceConfigurationId}
```

## <a name="request-headers"></a><span data-ttu-id="2758d-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="2758d-120">Request headers</span></span>
|<span data-ttu-id="2758d-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2758d-121">Header</span></span>|<span data-ttu-id="2758d-122">Valor</span><span class="sxs-lookup"><span data-stu-id="2758d-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="2758d-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="2758d-123">Authorization</span></span>|<span data-ttu-id="2758d-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="2758d-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="2758d-125">Accept</span><span class="sxs-lookup"><span data-stu-id="2758d-125">Accept</span></span>|<span data-ttu-id="2758d-126">application/json</span><span class="sxs-lookup"><span data-stu-id="2758d-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="2758d-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="2758d-127">Request body</span></span>
<span data-ttu-id="2758d-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto [iosPkcsCertificateProfile](../resources/intune-deviceconfig-iospkcscertificateprofile.md) .</span><span class="sxs-lookup"><span data-stu-id="2758d-128">In the request body, supply a JSON representation for the [iosPkcsCertificateProfile](../resources/intune-deviceconfig-iospkcscertificateprofile.md) object.</span></span>

<span data-ttu-id="2758d-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el [iosPkcsCertificateProfile](../resources/intune-deviceconfig-iospkcscertificateprofile.md).</span><span class="sxs-lookup"><span data-stu-id="2758d-129">The following table shows the properties that are required when you create the [iosPkcsCertificateProfile](../resources/intune-deviceconfig-iospkcscertificateprofile.md).</span></span>

|<span data-ttu-id="2758d-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="2758d-130">Property</span></span>|<span data-ttu-id="2758d-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="2758d-131">Type</span></span>|<span data-ttu-id="2758d-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="2758d-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="2758d-133">id</span><span class="sxs-lookup"><span data-stu-id="2758d-133">id</span></span>|<span data-ttu-id="2758d-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="2758d-134">String</span></span>|<span data-ttu-id="2758d-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="2758d-135">Key of the entity.</span></span> <span data-ttu-id="2758d-136">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="2758d-136">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="2758d-137">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="2758d-137">lastModifiedDateTime</span></span>|<span data-ttu-id="2758d-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="2758d-138">DateTimeOffset</span></span>|<span data-ttu-id="2758d-139">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="2758d-139">DateTime the object was last modified.</span></span> <span data-ttu-id="2758d-140">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="2758d-140">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="2758d-141">roleScopeTagIds</span><span class="sxs-lookup"><span data-stu-id="2758d-141">roleScopeTagIds</span></span>|<span data-ttu-id="2758d-142">Colección String</span><span class="sxs-lookup"><span data-stu-id="2758d-142">String collection</span></span>|<span data-ttu-id="2758d-143">Lista de etiquetas de ámbito para esta instancia de entidad.</span><span class="sxs-lookup"><span data-stu-id="2758d-143">List of Scope Tags for this Entity instance.</span></span> <span data-ttu-id="2758d-144">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="2758d-144">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="2758d-145">supportsScopeTags</span><span class="sxs-lookup"><span data-stu-id="2758d-145">supportsScopeTags</span></span>|<span data-ttu-id="2758d-146">Booleano</span><span class="sxs-lookup"><span data-stu-id="2758d-146">Boolean</span></span>|<span data-ttu-id="2758d-147">Indica si la configuración del dispositivo subyacente admite la asignación de etiquetas de ámbito.</span><span class="sxs-lookup"><span data-stu-id="2758d-147">Indicates whether or not the underlying Device Configuration supports the assignment of scope tags.</span></span> <span data-ttu-id="2758d-148">No se permite la asignación a la propiedad ScopeTags cuando este valor es false y entidades no estará visibles para los usuarios con ámbito.</span><span class="sxs-lookup"><span data-stu-id="2758d-148">Assigning to the ScopeTags property is not allowed when this value is false and entities will not be visible to scoped users.</span></span> <span data-ttu-id="2758d-149">Esto se produce para las directivas de heredado creadas en Silverlight y se puede resolver por eliminar y volver a crear la directiva en el Portal de Azure.</span><span class="sxs-lookup"><span data-stu-id="2758d-149">This occurs for Legacy policies created in Silverlight and can be resolved by deleting and recreating the policy in the Azure Portal.</span></span> <span data-ttu-id="2758d-150">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="2758d-150">This property is read-only.</span></span> <span data-ttu-id="2758d-151">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="2758d-151">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="2758d-152">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="2758d-152">createdDateTime</span></span>|<span data-ttu-id="2758d-153">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="2758d-153">DateTimeOffset</span></span>|<span data-ttu-id="2758d-154">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="2758d-154">DateTime the object was created.</span></span> <span data-ttu-id="2758d-155">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="2758d-155">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="2758d-156">descripción</span><span class="sxs-lookup"><span data-stu-id="2758d-156">description</span></span>|<span data-ttu-id="2758d-157">Cadena</span><span class="sxs-lookup"><span data-stu-id="2758d-157">String</span></span>|<span data-ttu-id="2758d-158">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2758d-158">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="2758d-159">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="2758d-159">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="2758d-160">displayName</span><span class="sxs-lookup"><span data-stu-id="2758d-160">displayName</span></span>|<span data-ttu-id="2758d-161">Cadena</span><span class="sxs-lookup"><span data-stu-id="2758d-161">String</span></span>|<span data-ttu-id="2758d-162">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2758d-162">Admin provided name of the device configuration.</span></span> <span data-ttu-id="2758d-163">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="2758d-163">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="2758d-164">version</span><span class="sxs-lookup"><span data-stu-id="2758d-164">version</span></span>|<span data-ttu-id="2758d-165">Int32</span><span class="sxs-lookup"><span data-stu-id="2758d-165">Int32</span></span>|<span data-ttu-id="2758d-166">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2758d-166">Version of the device configuration.</span></span> <span data-ttu-id="2758d-167">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="2758d-167">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="2758d-168">renewalThresholdPercentage</span><span class="sxs-lookup"><span data-stu-id="2758d-168">renewalThresholdPercentage</span></span>|<span data-ttu-id="2758d-169">Int32</span><span class="sxs-lookup"><span data-stu-id="2758d-169">Int32</span></span>|<span data-ttu-id="2758d-170">Porcentaje de umbral de renovación de certificado.</span><span class="sxs-lookup"><span data-stu-id="2758d-170">Certificate renewal threshold percentage.</span></span> <span data-ttu-id="2758d-171">Válido valores heredada de 1 a 99 de [iosCertificateProfileBase](../resources/intune-deviceconfig-ioscertificateprofilebase.md)</span><span class="sxs-lookup"><span data-stu-id="2758d-171">Valid values 1 to 99 Inherited from [iosCertificateProfileBase](../resources/intune-deviceconfig-ioscertificateprofilebase.md)</span></span>|
|<span data-ttu-id="2758d-172">subjectNameFormat</span><span class="sxs-lookup"><span data-stu-id="2758d-172">subjectNameFormat</span></span>|[<span data-ttu-id="2758d-173">appleSubjectNameFormat</span><span class="sxs-lookup"><span data-stu-id="2758d-173">appleSubjectNameFormat</span></span>](../resources/intune-deviceconfig-applesubjectnameformat.md)|<span data-ttu-id="2758d-174">Formato de nombre de sujeto de certificado.</span><span class="sxs-lookup"><span data-stu-id="2758d-174">Certificate Subject Name Format.</span></span> <span data-ttu-id="2758d-175">Se hereda de [iosCertificateProfileBase](../resources/intune-deviceconfig-ioscertificateprofilebase.md).</span><span class="sxs-lookup"><span data-stu-id="2758d-175">Inherited from [iosCertificateProfileBase](../resources/intune-deviceconfig-ioscertificateprofilebase.md).</span></span> <span data-ttu-id="2758d-176">Los valores posibles son: `commonName`, `commonNameAsEmail`, `custom`, `commonNameIncludingEmail`, `commonNameAsIMEI`, `commonNameAsSerialNumber`.</span><span class="sxs-lookup"><span data-stu-id="2758d-176">Possible values are: `commonName`, `commonNameAsEmail`, `custom`, `commonNameIncludingEmail`, `commonNameAsIMEI`, `commonNameAsSerialNumber`.</span></span>|
|<span data-ttu-id="2758d-177">subjectAlternativeNameType</span><span class="sxs-lookup"><span data-stu-id="2758d-177">subjectAlternativeNameType</span></span>|[<span data-ttu-id="2758d-178">subjectAlternativeNameType</span><span class="sxs-lookup"><span data-stu-id="2758d-178">subjectAlternativeNameType</span></span>](../resources/intune-deviceconfig-subjectalternativenametype.md)|<span data-ttu-id="2758d-179">Tipo de nombre alternativo del sujeto del certificado.</span><span class="sxs-lookup"><span data-stu-id="2758d-179">Certificate Subject Alternative Name type.</span></span> <span data-ttu-id="2758d-180">Se hereda de [iosCertificateProfileBase](../resources/intune-deviceconfig-ioscertificateprofilebase.md).</span><span class="sxs-lookup"><span data-stu-id="2758d-180">Inherited from [iosCertificateProfileBase](../resources/intune-deviceconfig-ioscertificateprofilebase.md).</span></span> <span data-ttu-id="2758d-181">Los valores posibles son: `none`, `emailAddress`, `userPrincipalName`, `customAzureADAttribute` y `domainNameService`.</span><span class="sxs-lookup"><span data-stu-id="2758d-181">Possible values are: `none`, `emailAddress`, `userPrincipalName`, `customAzureADAttribute`, `domainNameService`.</span></span>|
|<span data-ttu-id="2758d-182">certificateValidityPeriodValue</span><span class="sxs-lookup"><span data-stu-id="2758d-182">certificateValidityPeriodValue</span></span>|<span data-ttu-id="2758d-183">Int32</span><span class="sxs-lookup"><span data-stu-id="2758d-183">Int32</span></span>|<span data-ttu-id="2758d-184">Valor para el período de validez del certificado.</span><span class="sxs-lookup"><span data-stu-id="2758d-184">Value for the Certificate Validity Period.</span></span> <span data-ttu-id="2758d-185">Se hereda de [iosCertificateProfileBase](../resources/intune-deviceconfig-ioscertificateprofilebase.md)</span><span class="sxs-lookup"><span data-stu-id="2758d-185">Inherited from [iosCertificateProfileBase](../resources/intune-deviceconfig-ioscertificateprofilebase.md)</span></span>|
|<span data-ttu-id="2758d-186">certificateValidityPeriodScale</span><span class="sxs-lookup"><span data-stu-id="2758d-186">certificateValidityPeriodScale</span></span>|[<span data-ttu-id="2758d-187">certificateValidityPeriodScale</span><span class="sxs-lookup"><span data-stu-id="2758d-187">certificateValidityPeriodScale</span></span>](../resources/intune-deviceconfig-certificatevalidityperiodscale.md)|<span data-ttu-id="2758d-188">Escala para el período de validez del certificado.</span><span class="sxs-lookup"><span data-stu-id="2758d-188">Scale for the Certificate Validity Period.</span></span> <span data-ttu-id="2758d-189">Se hereda de [iosCertificateProfileBase](../resources/intune-deviceconfig-ioscertificateprofilebase.md).</span><span class="sxs-lookup"><span data-stu-id="2758d-189">Inherited from [iosCertificateProfileBase](../resources/intune-deviceconfig-ioscertificateprofilebase.md).</span></span> <span data-ttu-id="2758d-190">Los valores posibles son: `days`, `months` y `years`.</span><span class="sxs-lookup"><span data-stu-id="2758d-190">Possible values are: `days`, `months`, `years`.</span></span>|
|<span data-ttu-id="2758d-191">certificationAuthority</span><span class="sxs-lookup"><span data-stu-id="2758d-191">certificationAuthority</span></span>|<span data-ttu-id="2758d-192">Cadena</span><span class="sxs-lookup"><span data-stu-id="2758d-192">String</span></span>|<span data-ttu-id="2758d-193">Entidad de certificación PKCS.</span><span class="sxs-lookup"><span data-stu-id="2758d-193">PKCS Certification Authority.</span></span>|
|<span data-ttu-id="2758d-194">certificationAuthorityName</span><span class="sxs-lookup"><span data-stu-id="2758d-194">certificationAuthorityName</span></span>|<span data-ttu-id="2758d-195">Cadena</span><span class="sxs-lookup"><span data-stu-id="2758d-195">String</span></span>|<span data-ttu-id="2758d-196">Nombre de la autoridad de certificación PKCS.</span><span class="sxs-lookup"><span data-stu-id="2758d-196">PKCS Certification Authority Name.</span></span>|
|<span data-ttu-id="2758d-197">certificateTemplateName</span><span class="sxs-lookup"><span data-stu-id="2758d-197">certificateTemplateName</span></span>|<span data-ttu-id="2758d-198">Cadena</span><span class="sxs-lookup"><span data-stu-id="2758d-198">String</span></span>|<span data-ttu-id="2758d-199">Nombre de la plantilla de certificado PKCS.</span><span class="sxs-lookup"><span data-stu-id="2758d-199">PKCS Certificate Template Name.</span></span>|
|<span data-ttu-id="2758d-200">subjectAlternativeNameFormatString</span><span class="sxs-lookup"><span data-stu-id="2758d-200">subjectAlternativeNameFormatString</span></span>|<span data-ttu-id="2758d-201">Cadena</span><span class="sxs-lookup"><span data-stu-id="2758d-201">String</span></span>|<span data-ttu-id="2758d-202">Cadena personalizada que define el atributo AAD.</span><span class="sxs-lookup"><span data-stu-id="2758d-202">Custom String that defines the AAD Attribute.</span></span>|



## <a name="response"></a><span data-ttu-id="2758d-203">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2758d-203">Response</span></span>
<span data-ttu-id="2758d-204">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto actualizado [iosPkcsCertificateProfile](../resources/intune-deviceconfig-iospkcscertificateprofile.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2758d-204">If successful, this method returns a `200 OK` response code and an updated [iosPkcsCertificateProfile](../resources/intune-deviceconfig-iospkcscertificateprofile.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="2758d-205">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2758d-205">Example</span></span>
### <a name="request"></a><span data-ttu-id="2758d-206">Solicitud</span><span class="sxs-lookup"><span data-stu-id="2758d-206">Request</span></span>
<span data-ttu-id="2758d-207">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="2758d-207">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations/{deviceConfigurationId}
Content-type: application/json
Content-length: 761

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
  "certificationAuthority": "Certification Authority value",
  "certificationAuthorityName": "Certification Authority Name value",
  "certificateTemplateName": "Certificate Template Name value",
  "subjectAlternativeNameFormatString": "Subject Alternative Name Format String value"
}
```

### <a name="response"></a><span data-ttu-id="2758d-208">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2758d-208">Response</span></span>
<span data-ttu-id="2758d-p116">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="2758d-p116">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 933

{
  "@odata.type": "#microsoft.graph.iosPkcsCertificateProfile",
  "id": "ed0264dd-64dd-ed02-dd64-02eddd6402ed",
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
  "certificationAuthority": "Certification Authority value",
  "certificationAuthorityName": "Certification Authority Name value",
  "certificateTemplateName": "Certificate Template Name value",
  "subjectAlternativeNameFormatString": "Subject Alternative Name Format String value"
}
```





