---
title: Actualizar androidForWorkPkcsCertificateProfile
description: Actualizar las propiedades de un objeto androidForWorkPkcsCertificateProfile.
ms.openlocfilehash: aa66069317ea2be9d13b21e8f909edc2a36ddc99
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088913"
---
# <a name="update-androidforworkpkcscertificateprofile"></a><span data-ttu-id="a0a72-103">Actualizar androidForWorkPkcsCertificateProfile</span><span class="sxs-lookup"><span data-stu-id="a0a72-103">Update androidForWorkPkcsCertificateProfile</span></span>

> <span data-ttu-id="a0a72-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="a0a72-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="a0a72-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="a0a72-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="a0a72-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="a0a72-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="a0a72-107">Actualizar las propiedades de un objeto [androidForWorkPkcsCertificateProfile](../resources/intune-deviceconfig-androidforworkpkcscertificateprofile.md) .</span><span class="sxs-lookup"><span data-stu-id="a0a72-107">Update the properties of a [androidForWorkPkcsCertificateProfile](../resources/intune-deviceconfig-androidforworkpkcscertificateprofile.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="a0a72-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="a0a72-108">Prerequisites</span></span>
<span data-ttu-id="a0a72-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="a0a72-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="a0a72-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a0a72-111">Permission type</span></span>|<span data-ttu-id="a0a72-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a0a72-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="a0a72-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a0a72-113">Delegated (work or school account)</span></span>|<span data-ttu-id="a0a72-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="a0a72-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="a0a72-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a0a72-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="a0a72-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a0a72-116">Not supported.</span></span>|
|<span data-ttu-id="a0a72-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a0a72-117">Application</span></span>|<span data-ttu-id="a0a72-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a0a72-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="a0a72-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a0a72-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/groupAssignments/{deviceConfigurationGroupAssignmentId}/deviceConfiguration
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsDomainJoinConfiguration/networkAccessConfigurations/{deviceConfigurationId}
```

## <a name="request-headers"></a><span data-ttu-id="a0a72-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a0a72-120">Request headers</span></span>
|<span data-ttu-id="a0a72-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a0a72-121">Header</span></span>|<span data-ttu-id="a0a72-122">Valor</span><span class="sxs-lookup"><span data-stu-id="a0a72-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="a0a72-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="a0a72-123">Authorization</span></span>|<span data-ttu-id="a0a72-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="a0a72-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="a0a72-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="a0a72-125">Accept</span></span>|<span data-ttu-id="a0a72-126">application/json</span><span class="sxs-lookup"><span data-stu-id="a0a72-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="a0a72-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a0a72-127">Request body</span></span>
<span data-ttu-id="a0a72-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto [androidForWorkPkcsCertificateProfile](../resources/intune-deviceconfig-androidforworkpkcscertificateprofile.md) .</span><span class="sxs-lookup"><span data-stu-id="a0a72-128">In the request body, supply a JSON representation for the [androidForWorkPkcsCertificateProfile](../resources/intune-deviceconfig-androidforworkpkcscertificateprofile.md) object.</span></span>

<span data-ttu-id="a0a72-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el [androidForWorkPkcsCertificateProfile](../resources/intune-deviceconfig-androidforworkpkcscertificateprofile.md).</span><span class="sxs-lookup"><span data-stu-id="a0a72-129">The following table shows the properties that are required when you create the [androidForWorkPkcsCertificateProfile](../resources/intune-deviceconfig-androidforworkpkcscertificateprofile.md).</span></span>

|<span data-ttu-id="a0a72-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a0a72-130">Property</span></span>|<span data-ttu-id="a0a72-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="a0a72-131">Type</span></span>|<span data-ttu-id="a0a72-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="a0a72-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="a0a72-133">id</span><span class="sxs-lookup"><span data-stu-id="a0a72-133">id</span></span>|<span data-ttu-id="a0a72-134">String</span><span class="sxs-lookup"><span data-stu-id="a0a72-134">String</span></span>|<span data-ttu-id="a0a72-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="a0a72-135">Key of the entity.</span></span> <span data-ttu-id="a0a72-136">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="a0a72-136">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="a0a72-137">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="a0a72-137">lastModifiedDateTime</span></span>|<span data-ttu-id="a0a72-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="a0a72-138">DateTimeOffset</span></span>|<span data-ttu-id="a0a72-139">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="a0a72-139">DateTime the object was last modified.</span></span> <span data-ttu-id="a0a72-140">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="a0a72-140">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="a0a72-141">roleScopeTagIds</span><span class="sxs-lookup"><span data-stu-id="a0a72-141">roleScopeTagIds</span></span>|<span data-ttu-id="a0a72-142">Colección String</span><span class="sxs-lookup"><span data-stu-id="a0a72-142">String collection</span></span>|<span data-ttu-id="a0a72-143">Lista de etiquetas de ámbito para esta instancia de entidad.</span><span class="sxs-lookup"><span data-stu-id="a0a72-143">List of Scope Tags for this Entity instance.</span></span> <span data-ttu-id="a0a72-144">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="a0a72-144">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="a0a72-145">supportsScopeTags</span><span class="sxs-lookup"><span data-stu-id="a0a72-145">supportsScopeTags</span></span>|<span data-ttu-id="a0a72-146">Booleano</span><span class="sxs-lookup"><span data-stu-id="a0a72-146">Boolean</span></span>|<span data-ttu-id="a0a72-147">Indica si la configuración del dispositivo subyacente admite la asignación de etiquetas de ámbito.</span><span class="sxs-lookup"><span data-stu-id="a0a72-147">Indicates whether or not the underlying Device Configuration supports the assignment of scope tags.</span></span> <span data-ttu-id="a0a72-148">No se permite la asignación a la propiedad ScopeTags cuando este valor es false y entidades no estará visibles para los usuarios con ámbito.</span><span class="sxs-lookup"><span data-stu-id="a0a72-148">Assigning to the ScopeTags property is not allowed when this value is false and entities will not be visible to scoped users.</span></span> <span data-ttu-id="a0a72-149">Esto se produce para las directivas de heredado creadas en Silverlight y se puede resolver por eliminar y volver a crear la directiva en el Portal de Azure.</span><span class="sxs-lookup"><span data-stu-id="a0a72-149">This occurs for Legacy policies created in Silverlight and can be resolved by deleting and recreating the policy in the Azure Portal.</span></span> <span data-ttu-id="a0a72-150">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="a0a72-150">This property is read-only.</span></span> <span data-ttu-id="a0a72-151">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="a0a72-151">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="a0a72-152">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="a0a72-152">createdDateTime</span></span>|<span data-ttu-id="a0a72-153">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="a0a72-153">DateTimeOffset</span></span>|<span data-ttu-id="a0a72-154">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="a0a72-154">DateTime the object was created.</span></span> <span data-ttu-id="a0a72-155">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="a0a72-155">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="a0a72-156">descripción</span><span class="sxs-lookup"><span data-stu-id="a0a72-156">description</span></span>|<span data-ttu-id="a0a72-157">String</span><span class="sxs-lookup"><span data-stu-id="a0a72-157">String</span></span>|<span data-ttu-id="a0a72-158">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a0a72-158">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="a0a72-159">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="a0a72-159">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="a0a72-160">displayName</span><span class="sxs-lookup"><span data-stu-id="a0a72-160">displayName</span></span>|<span data-ttu-id="a0a72-161">String</span><span class="sxs-lookup"><span data-stu-id="a0a72-161">String</span></span>|<span data-ttu-id="a0a72-162">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a0a72-162">Admin provided name of the device configuration.</span></span> <span data-ttu-id="a0a72-163">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="a0a72-163">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="a0a72-164">version</span><span class="sxs-lookup"><span data-stu-id="a0a72-164">version</span></span>|<span data-ttu-id="a0a72-165">Int32</span><span class="sxs-lookup"><span data-stu-id="a0a72-165">Int32</span></span>|<span data-ttu-id="a0a72-166">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a0a72-166">Version of the device configuration.</span></span> <span data-ttu-id="a0a72-167">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="a0a72-167">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="a0a72-168">renewalThresholdPercentage</span><span class="sxs-lookup"><span data-stu-id="a0a72-168">renewalThresholdPercentage</span></span>|<span data-ttu-id="a0a72-169">Int32</span><span class="sxs-lookup"><span data-stu-id="a0a72-169">Int32</span></span>|<span data-ttu-id="a0a72-170">Porcentaje de umbral de renovación de certificado.</span><span class="sxs-lookup"><span data-stu-id="a0a72-170">Certificate renewal threshold percentage.</span></span> <span data-ttu-id="a0a72-171">Válido valores heredada de 1 a 99 de [androidForWorkCertificateProfileBase](../resources/intune-deviceconfig-androidforworkcertificateprofilebase.md)</span><span class="sxs-lookup"><span data-stu-id="a0a72-171">Valid values 1 to 99 Inherited from [androidForWorkCertificateProfileBase](../resources/intune-deviceconfig-androidforworkcertificateprofilebase.md)</span></span>|
|<span data-ttu-id="a0a72-172">subjectNameFormat</span><span class="sxs-lookup"><span data-stu-id="a0a72-172">subjectNameFormat</span></span>|[<span data-ttu-id="a0a72-173">subjectNameFormat</span><span class="sxs-lookup"><span data-stu-id="a0a72-173">subjectNameFormat</span></span>](../resources/intune-deviceconfig-subjectnameformat.md)|<span data-ttu-id="a0a72-174">Formato de nombre de sujeto de certificado.</span><span class="sxs-lookup"><span data-stu-id="a0a72-174">Certificate Subject Name Format.</span></span> <span data-ttu-id="a0a72-175">Se hereda de [androidForWorkCertificateProfileBase](../resources/intune-deviceconfig-androidforworkcertificateprofilebase.md).</span><span class="sxs-lookup"><span data-stu-id="a0a72-175">Inherited from [androidForWorkCertificateProfileBase](../resources/intune-deviceconfig-androidforworkcertificateprofilebase.md).</span></span> <span data-ttu-id="a0a72-176">Los valores posibles son: `commonName`, `commonNameIncludingEmail`, `commonNameAsEmail`, `custom`, `commonNameAsIMEI`, `commonNameAsSerialNumber`, `commonNameAsAadDeviceId`, `commonNameAsIntuneDeviceId` y `commonNameAsDurableDeviceId`.</span><span class="sxs-lookup"><span data-stu-id="a0a72-176">Possible values are: `commonName`, `commonNameIncludingEmail`, `commonNameAsEmail`, `custom`, `commonNameAsIMEI`, `commonNameAsSerialNumber`, `commonNameAsAadDeviceId`, `commonNameAsIntuneDeviceId`, `commonNameAsDurableDeviceId`.</span></span>|
|<span data-ttu-id="a0a72-177">certificateValidityPeriodValue</span><span class="sxs-lookup"><span data-stu-id="a0a72-177">certificateValidityPeriodValue</span></span>|<span data-ttu-id="a0a72-178">Int32</span><span class="sxs-lookup"><span data-stu-id="a0a72-178">Int32</span></span>|<span data-ttu-id="a0a72-179">Valor para el período de validez del certificado.</span><span class="sxs-lookup"><span data-stu-id="a0a72-179">Value for the Certificate Validity Period.</span></span> <span data-ttu-id="a0a72-180">Se hereda de [androidForWorkCertificateProfileBase](../resources/intune-deviceconfig-androidforworkcertificateprofilebase.md)</span><span class="sxs-lookup"><span data-stu-id="a0a72-180">Inherited from [androidForWorkCertificateProfileBase](../resources/intune-deviceconfig-androidforworkcertificateprofilebase.md)</span></span>|
|<span data-ttu-id="a0a72-181">certificateValidityPeriodScale</span><span class="sxs-lookup"><span data-stu-id="a0a72-181">certificateValidityPeriodScale</span></span>|[<span data-ttu-id="a0a72-182">certificateValidityPeriodScale</span><span class="sxs-lookup"><span data-stu-id="a0a72-182">certificateValidityPeriodScale</span></span>](../resources/intune-deviceconfig-certificatevalidityperiodscale.md)|<span data-ttu-id="a0a72-183">Escala para el período de validez del certificado.</span><span class="sxs-lookup"><span data-stu-id="a0a72-183">Scale for the Certificate Validity Period.</span></span> <span data-ttu-id="a0a72-184">Se hereda de [androidForWorkCertificateProfileBase](../resources/intune-deviceconfig-androidforworkcertificateprofilebase.md).</span><span class="sxs-lookup"><span data-stu-id="a0a72-184">Inherited from [androidForWorkCertificateProfileBase](../resources/intune-deviceconfig-androidforworkcertificateprofilebase.md).</span></span> <span data-ttu-id="a0a72-185">Los valores posibles son: `days`, `months` y `years`.</span><span class="sxs-lookup"><span data-stu-id="a0a72-185">Possible values are: `days`, `months`, `years`.</span></span>|
|<span data-ttu-id="a0a72-186">extendedKeyUsages</span><span class="sxs-lookup"><span data-stu-id="a0a72-186">extendedKeyUsages</span></span>|<span data-ttu-id="a0a72-187">colección de [ExtendeKeyUsage](../resources/intune-deviceconfig-extendedkeyusage.md)</span><span class="sxs-lookup"><span data-stu-id="a0a72-187">[extendedKeyUsage](../resources/intune-deviceconfig-extendedkeyusage.md) collection</span></span>|<span data-ttu-id="a0a72-188">Configuración de clave (EKU) extendida.</span><span class="sxs-lookup"><span data-stu-id="a0a72-188">Extended Key Usage (EKU) settings.</span></span> <span data-ttu-id="a0a72-189">Esta colección puede contener un máximo de 500 elementos.</span><span class="sxs-lookup"><span data-stu-id="a0a72-189">This collection can contain a maximum of 500 elements.</span></span> <span data-ttu-id="a0a72-190">Se hereda de [androidForWorkCertificateProfileBase](../resources/intune-deviceconfig-androidforworkcertificateprofilebase.md)</span><span class="sxs-lookup"><span data-stu-id="a0a72-190">Inherited from [androidForWorkCertificateProfileBase](../resources/intune-deviceconfig-androidforworkcertificateprofilebase.md)</span></span>|
|<span data-ttu-id="a0a72-191">certificationAuthority</span><span class="sxs-lookup"><span data-stu-id="a0a72-191">certificationAuthority</span></span>|<span data-ttu-id="a0a72-192">String</span><span class="sxs-lookup"><span data-stu-id="a0a72-192">String</span></span>|<span data-ttu-id="a0a72-193">Entidad de certificación PKCS</span><span class="sxs-lookup"><span data-stu-id="a0a72-193">PKCS Certification Authority</span></span>|
|<span data-ttu-id="a0a72-194">certificationAuthorityName</span><span class="sxs-lookup"><span data-stu-id="a0a72-194">certificationAuthorityName</span></span>|<span data-ttu-id="a0a72-195">String</span><span class="sxs-lookup"><span data-stu-id="a0a72-195">String</span></span>|<span data-ttu-id="a0a72-196">Nombre de entidad de certificación PKCS</span><span class="sxs-lookup"><span data-stu-id="a0a72-196">PKCS Certification Authority Name</span></span>|
|<span data-ttu-id="a0a72-197">certificateTemplateName</span><span class="sxs-lookup"><span data-stu-id="a0a72-197">certificateTemplateName</span></span>|<span data-ttu-id="a0a72-198">String</span><span class="sxs-lookup"><span data-stu-id="a0a72-198">String</span></span>|<span data-ttu-id="a0a72-199">Nombre de plantilla de certificado PKCS</span><span class="sxs-lookup"><span data-stu-id="a0a72-199">PKCS Certificate Template Name</span></span>|
|<span data-ttu-id="a0a72-200">subjectAlternativeNameFormatString</span><span class="sxs-lookup"><span data-stu-id="a0a72-200">subjectAlternativeNameFormatString</span></span>|<span data-ttu-id="a0a72-201">String</span><span class="sxs-lookup"><span data-stu-id="a0a72-201">String</span></span>|<span data-ttu-id="a0a72-202">Cadena personalizada que define el atributo AAD.</span><span class="sxs-lookup"><span data-stu-id="a0a72-202">Custom String that defines the AAD Attribute.</span></span>|
|<span data-ttu-id="a0a72-203">subjectAlternativeNameType</span><span class="sxs-lookup"><span data-stu-id="a0a72-203">subjectAlternativeNameType</span></span>|[<span data-ttu-id="a0a72-204">subjectAlternativeNameType</span><span class="sxs-lookup"><span data-stu-id="a0a72-204">subjectAlternativeNameType</span></span>](../resources/intune-deviceconfig-subjectalternativenametype.md)|<span data-ttu-id="a0a72-205">Tipo de nombre alternativo de sujeto de certificado.</span><span class="sxs-lookup"><span data-stu-id="a0a72-205">Certificate Subject Alternative Name Type.</span></span> <span data-ttu-id="a0a72-206">Los valores posibles son: `none`, `emailAddress`, `userPrincipalName`, `customAzureADAttribute` y `domainNameService`.</span><span class="sxs-lookup"><span data-stu-id="a0a72-206">Possible values are: `none`, `emailAddress`, `userPrincipalName`, `customAzureADAttribute`, `domainNameService`.</span></span>|



## <a name="response"></a><span data-ttu-id="a0a72-207">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a0a72-207">Response</span></span>
<span data-ttu-id="a0a72-208">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto actualizado [androidForWorkPkcsCertificateProfile](../resources/intune-deviceconfig-androidforworkpkcscertificateprofile.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a0a72-208">If successful, this method returns a `200 OK` response code and an updated [androidForWorkPkcsCertificateProfile](../resources/intune-deviceconfig-androidforworkpkcscertificateprofile.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="a0a72-209">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a0a72-209">Example</span></span>
### <a name="request"></a><span data-ttu-id="a0a72-210">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a0a72-210">Request</span></span>
<span data-ttu-id="a0a72-211">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a0a72-211">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations/{deviceConfigurationId}
Content-type: application/json
Content-length: 954

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
  "subjectNameFormat": "commonNameIncludingEmail",
  "certificateValidityPeriodValue": 14,
  "certificateValidityPeriodScale": "months",
  "extendedKeyUsages": [
    {
      "@odata.type": "microsoft.graph.extendedKeyUsage",
      "name": "Name value",
      "objectIdentifier": "Object Identifier value"
    }
  ],
  "certificationAuthority": "Certification Authority value",
  "certificationAuthorityName": "Certification Authority Name value",
  "certificateTemplateName": "Certificate Template Name value",
  "subjectAlternativeNameFormatString": "Subject Alternative Name Format String value",
  "subjectAlternativeNameType": "emailAddress"
}
```

### <a name="response"></a><span data-ttu-id="a0a72-212">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a0a72-212">Response</span></span>
<span data-ttu-id="a0a72-p117">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="a0a72-p117">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1137

{
  "@odata.type": "#microsoft.graph.androidForWorkPkcsCertificateProfile",
  "id": "0a2d7691-7691-0a2d-9176-2d0a91762d0a",
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
  "subjectNameFormat": "commonNameIncludingEmail",
  "certificateValidityPeriodValue": 14,
  "certificateValidityPeriodScale": "months",
  "extendedKeyUsages": [
    {
      "@odata.type": "microsoft.graph.extendedKeyUsage",
      "name": "Name value",
      "objectIdentifier": "Object Identifier value"
    }
  ],
  "certificationAuthority": "Certification Authority value",
  "certificationAuthorityName": "Certification Authority Name value",
  "certificateTemplateName": "Certificate Template Name value",
  "subjectAlternativeNameFormatString": "Subject Alternative Name Format String value",
  "subjectAlternativeNameType": "emailAddress"
}
```




