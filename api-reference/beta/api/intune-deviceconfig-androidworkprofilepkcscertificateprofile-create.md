---
title: Crear androidWorkProfilePkcsCertificateProfile
description: Crear un nuevo objeto androidWorkProfilePkcsCertificateProfile.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 781b6f53d5530d68c19fb205f5c8f55b44bc0588
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27849101"
---
# <a name="create-androidworkprofilepkcscertificateprofile"></a><span data-ttu-id="027f5-103">Crear androidWorkProfilePkcsCertificateProfile</span><span class="sxs-lookup"><span data-stu-id="027f5-103">Create androidWorkProfilePkcsCertificateProfile</span></span>

> <span data-ttu-id="027f5-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="027f5-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="027f5-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="027f5-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="027f5-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="027f5-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="027f5-107">Crear un nuevo objeto [androidWorkProfilePkcsCertificateProfile](../resources/intune-deviceconfig-androidworkprofilepkcscertificateprofile.md) .</span><span class="sxs-lookup"><span data-stu-id="027f5-107">Create a new [androidWorkProfilePkcsCertificateProfile](../resources/intune-deviceconfig-androidworkprofilepkcscertificateprofile.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="027f5-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="027f5-108">Prerequisites</span></span>
<span data-ttu-id="027f5-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="027f5-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="027f5-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="027f5-111">Permission type</span></span>|<span data-ttu-id="027f5-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="027f5-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="027f5-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="027f5-113">Delegated (work or school account)</span></span>|<span data-ttu-id="027f5-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="027f5-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="027f5-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="027f5-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="027f5-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="027f5-116">Not supported.</span></span>|
|<span data-ttu-id="027f5-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="027f5-117">Application</span></span>|<span data-ttu-id="027f5-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="027f5-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="027f5-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="027f5-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceConfigurations
POST /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsDomainJoinConfiguration/networkAccessConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="027f5-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="027f5-120">Request headers</span></span>
|<span data-ttu-id="027f5-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="027f5-121">Header</span></span>|<span data-ttu-id="027f5-122">Valor</span><span class="sxs-lookup"><span data-stu-id="027f5-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="027f5-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="027f5-123">Authorization</span></span>|<span data-ttu-id="027f5-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="027f5-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="027f5-125">Accept</span><span class="sxs-lookup"><span data-stu-id="027f5-125">Accept</span></span>|<span data-ttu-id="027f5-126">application/json</span><span class="sxs-lookup"><span data-stu-id="027f5-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="027f5-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="027f5-127">Request body</span></span>
<span data-ttu-id="027f5-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto androidWorkProfilePkcsCertificateProfile.</span><span class="sxs-lookup"><span data-stu-id="027f5-128">In the request body, supply a JSON representation for the androidWorkProfilePkcsCertificateProfile object.</span></span>

<span data-ttu-id="027f5-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el androidWorkProfilePkcsCertificateProfile.</span><span class="sxs-lookup"><span data-stu-id="027f5-129">The following table shows the properties that are required when you create the androidWorkProfilePkcsCertificateProfile.</span></span>

|<span data-ttu-id="027f5-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="027f5-130">Property</span></span>|<span data-ttu-id="027f5-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="027f5-131">Type</span></span>|<span data-ttu-id="027f5-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="027f5-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="027f5-133">id</span><span class="sxs-lookup"><span data-stu-id="027f5-133">id</span></span>|<span data-ttu-id="027f5-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="027f5-134">String</span></span>|<span data-ttu-id="027f5-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="027f5-135">Key of the entity.</span></span> <span data-ttu-id="027f5-136">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="027f5-136">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="027f5-137">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="027f5-137">lastModifiedDateTime</span></span>|<span data-ttu-id="027f5-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="027f5-138">DateTimeOffset</span></span>|<span data-ttu-id="027f5-139">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="027f5-139">DateTime the object was last modified.</span></span> <span data-ttu-id="027f5-140">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="027f5-140">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="027f5-141">roleScopeTagIds</span><span class="sxs-lookup"><span data-stu-id="027f5-141">roleScopeTagIds</span></span>|<span data-ttu-id="027f5-142">Colección String</span><span class="sxs-lookup"><span data-stu-id="027f5-142">String collection</span></span>|<span data-ttu-id="027f5-143">Lista de etiquetas de ámbito para esta instancia de entidad.</span><span class="sxs-lookup"><span data-stu-id="027f5-143">List of Scope Tags for this Entity instance.</span></span> <span data-ttu-id="027f5-144">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="027f5-144">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="027f5-145">supportsScopeTags</span><span class="sxs-lookup"><span data-stu-id="027f5-145">supportsScopeTags</span></span>|<span data-ttu-id="027f5-146">Booleano</span><span class="sxs-lookup"><span data-stu-id="027f5-146">Boolean</span></span>|<span data-ttu-id="027f5-147">Indica si la configuración del dispositivo subyacente admite la asignación de etiquetas de ámbito.</span><span class="sxs-lookup"><span data-stu-id="027f5-147">Indicates whether or not the underlying Device Configuration supports the assignment of scope tags.</span></span> <span data-ttu-id="027f5-148">No se permite la asignación a la propiedad ScopeTags cuando este valor es false y entidades no estará visibles para los usuarios con ámbito.</span><span class="sxs-lookup"><span data-stu-id="027f5-148">Assigning to the ScopeTags property is not allowed when this value is false and entities will not be visible to scoped users.</span></span> <span data-ttu-id="027f5-149">Esto se produce para las directivas de heredado creadas en Silverlight y se puede resolver por eliminar y volver a crear la directiva en el Portal de Azure.</span><span class="sxs-lookup"><span data-stu-id="027f5-149">This occurs for Legacy policies created in Silverlight and can be resolved by deleting and recreating the policy in the Azure Portal.</span></span> <span data-ttu-id="027f5-150">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="027f5-150">This property is read-only.</span></span> <span data-ttu-id="027f5-151">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="027f5-151">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="027f5-152">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="027f5-152">createdDateTime</span></span>|<span data-ttu-id="027f5-153">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="027f5-153">DateTimeOffset</span></span>|<span data-ttu-id="027f5-154">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="027f5-154">DateTime the object was created.</span></span> <span data-ttu-id="027f5-155">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="027f5-155">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="027f5-156">descripción</span><span class="sxs-lookup"><span data-stu-id="027f5-156">description</span></span>|<span data-ttu-id="027f5-157">Cadena</span><span class="sxs-lookup"><span data-stu-id="027f5-157">String</span></span>|<span data-ttu-id="027f5-158">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="027f5-158">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="027f5-159">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="027f5-159">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="027f5-160">displayName</span><span class="sxs-lookup"><span data-stu-id="027f5-160">displayName</span></span>|<span data-ttu-id="027f5-161">Cadena</span><span class="sxs-lookup"><span data-stu-id="027f5-161">String</span></span>|<span data-ttu-id="027f5-162">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="027f5-162">Admin provided name of the device configuration.</span></span> <span data-ttu-id="027f5-163">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="027f5-163">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="027f5-164">version</span><span class="sxs-lookup"><span data-stu-id="027f5-164">version</span></span>|<span data-ttu-id="027f5-165">Int32</span><span class="sxs-lookup"><span data-stu-id="027f5-165">Int32</span></span>|<span data-ttu-id="027f5-166">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="027f5-166">Version of the device configuration.</span></span> <span data-ttu-id="027f5-167">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="027f5-167">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="027f5-168">renewalThresholdPercentage</span><span class="sxs-lookup"><span data-stu-id="027f5-168">renewalThresholdPercentage</span></span>|<span data-ttu-id="027f5-169">Int32</span><span class="sxs-lookup"><span data-stu-id="027f5-169">Int32</span></span>|<span data-ttu-id="027f5-170">Porcentaje de umbral de renovación de certificado.</span><span class="sxs-lookup"><span data-stu-id="027f5-170">Certificate renewal threshold percentage.</span></span> <span data-ttu-id="027f5-171">Válido valores heredada de 1 a 99 de [androidWorkProfileCertificateProfileBase](../resources/intune-deviceconfig-androidworkprofilecertificateprofilebase.md)</span><span class="sxs-lookup"><span data-stu-id="027f5-171">Valid values 1 to 99 Inherited from [androidWorkProfileCertificateProfileBase](../resources/intune-deviceconfig-androidworkprofilecertificateprofilebase.md)</span></span>|
|<span data-ttu-id="027f5-172">subjectNameFormat</span><span class="sxs-lookup"><span data-stu-id="027f5-172">subjectNameFormat</span></span>|[<span data-ttu-id="027f5-173">subjectNameFormat</span><span class="sxs-lookup"><span data-stu-id="027f5-173">subjectNameFormat</span></span>](../resources/intune-deviceconfig-subjectnameformat.md)|<span data-ttu-id="027f5-174">Formato de nombre de sujeto de certificado.</span><span class="sxs-lookup"><span data-stu-id="027f5-174">Certificate Subject Name Format.</span></span> <span data-ttu-id="027f5-175">Se hereda de [androidWorkProfileCertificateProfileBase](../resources/intune-deviceconfig-androidworkprofilecertificateprofilebase.md).</span><span class="sxs-lookup"><span data-stu-id="027f5-175">Inherited from [androidWorkProfileCertificateProfileBase](../resources/intune-deviceconfig-androidworkprofilecertificateprofilebase.md).</span></span> <span data-ttu-id="027f5-176">Los valores posibles son: `commonName`, `commonNameIncludingEmail`, `commonNameAsEmail`, `custom`, `commonNameAsIMEI`, `commonNameAsSerialNumber`, `commonNameAsAadDeviceId`, `commonNameAsIntuneDeviceId` y `commonNameAsDurableDeviceId`.</span><span class="sxs-lookup"><span data-stu-id="027f5-176">Possible values are: `commonName`, `commonNameIncludingEmail`, `commonNameAsEmail`, `custom`, `commonNameAsIMEI`, `commonNameAsSerialNumber`, `commonNameAsAadDeviceId`, `commonNameAsIntuneDeviceId`, `commonNameAsDurableDeviceId`.</span></span>|
|<span data-ttu-id="027f5-177">certificateValidityPeriodValue</span><span class="sxs-lookup"><span data-stu-id="027f5-177">certificateValidityPeriodValue</span></span>|<span data-ttu-id="027f5-178">Int32</span><span class="sxs-lookup"><span data-stu-id="027f5-178">Int32</span></span>|<span data-ttu-id="027f5-179">Valor para el período de validez del certificado.</span><span class="sxs-lookup"><span data-stu-id="027f5-179">Value for the Certificate Validity Period.</span></span> <span data-ttu-id="027f5-180">Se hereda de [androidWorkProfileCertificateProfileBase](../resources/intune-deviceconfig-androidworkprofilecertificateprofilebase.md)</span><span class="sxs-lookup"><span data-stu-id="027f5-180">Inherited from [androidWorkProfileCertificateProfileBase](../resources/intune-deviceconfig-androidworkprofilecertificateprofilebase.md)</span></span>|
|<span data-ttu-id="027f5-181">certificateValidityPeriodScale</span><span class="sxs-lookup"><span data-stu-id="027f5-181">certificateValidityPeriodScale</span></span>|[<span data-ttu-id="027f5-182">certificateValidityPeriodScale</span><span class="sxs-lookup"><span data-stu-id="027f5-182">certificateValidityPeriodScale</span></span>](../resources/intune-deviceconfig-certificatevalidityperiodscale.md)|<span data-ttu-id="027f5-183">Escala para el período de validez del certificado.</span><span class="sxs-lookup"><span data-stu-id="027f5-183">Scale for the Certificate Validity Period.</span></span> <span data-ttu-id="027f5-184">Se hereda de [androidWorkProfileCertificateProfileBase](../resources/intune-deviceconfig-androidworkprofilecertificateprofilebase.md).</span><span class="sxs-lookup"><span data-stu-id="027f5-184">Inherited from [androidWorkProfileCertificateProfileBase](../resources/intune-deviceconfig-androidworkprofilecertificateprofilebase.md).</span></span> <span data-ttu-id="027f5-185">Los valores posibles son: `days`, `months` y `years`.</span><span class="sxs-lookup"><span data-stu-id="027f5-185">Possible values are: `days`, `months`, `years`.</span></span>|
|<span data-ttu-id="027f5-186">extendedKeyUsages</span><span class="sxs-lookup"><span data-stu-id="027f5-186">extendedKeyUsages</span></span>|<span data-ttu-id="027f5-187">colección de [ExtendeKeyUsage](../resources/intune-deviceconfig-extendedkeyusage.md)</span><span class="sxs-lookup"><span data-stu-id="027f5-187">[extendedKeyUsage](../resources/intune-deviceconfig-extendedkeyusage.md) collection</span></span>|<span data-ttu-id="027f5-188">Configuración de clave (EKU) extendida.</span><span class="sxs-lookup"><span data-stu-id="027f5-188">Extended Key Usage (EKU) settings.</span></span> <span data-ttu-id="027f5-189">Esta colección puede contener un máximo de 500 elementos.</span><span class="sxs-lookup"><span data-stu-id="027f5-189">This collection can contain a maximum of 500 elements.</span></span> <span data-ttu-id="027f5-190">Se hereda de [androidWorkProfileCertificateProfileBase](../resources/intune-deviceconfig-androidworkprofilecertificateprofilebase.md)</span><span class="sxs-lookup"><span data-stu-id="027f5-190">Inherited from [androidWorkProfileCertificateProfileBase](../resources/intune-deviceconfig-androidworkprofilecertificateprofilebase.md)</span></span>|
|<span data-ttu-id="027f5-191">certificationAuthority</span><span class="sxs-lookup"><span data-stu-id="027f5-191">certificationAuthority</span></span>|<span data-ttu-id="027f5-192">Cadena</span><span class="sxs-lookup"><span data-stu-id="027f5-192">String</span></span>|<span data-ttu-id="027f5-193">Entidad de certificación PKCS</span><span class="sxs-lookup"><span data-stu-id="027f5-193">PKCS Certification Authority</span></span>|
|<span data-ttu-id="027f5-194">certificationAuthorityName</span><span class="sxs-lookup"><span data-stu-id="027f5-194">certificationAuthorityName</span></span>|<span data-ttu-id="027f5-195">Cadena</span><span class="sxs-lookup"><span data-stu-id="027f5-195">String</span></span>|<span data-ttu-id="027f5-196">Nombre de entidad de certificación PKCS</span><span class="sxs-lookup"><span data-stu-id="027f5-196">PKCS Certification Authority Name</span></span>|
|<span data-ttu-id="027f5-197">certificateTemplateName</span><span class="sxs-lookup"><span data-stu-id="027f5-197">certificateTemplateName</span></span>|<span data-ttu-id="027f5-198">Cadena</span><span class="sxs-lookup"><span data-stu-id="027f5-198">String</span></span>|<span data-ttu-id="027f5-199">Nombre de plantilla de certificado PKCS</span><span class="sxs-lookup"><span data-stu-id="027f5-199">PKCS Certificate Template Name</span></span>|
|<span data-ttu-id="027f5-200">subjectAlternativeNameFormatString</span><span class="sxs-lookup"><span data-stu-id="027f5-200">subjectAlternativeNameFormatString</span></span>|<span data-ttu-id="027f5-201">Cadena</span><span class="sxs-lookup"><span data-stu-id="027f5-201">String</span></span>|<span data-ttu-id="027f5-202">Cadena personalizada que define el atributo AAD.</span><span class="sxs-lookup"><span data-stu-id="027f5-202">Custom String that defines the AAD Attribute.</span></span>|
|<span data-ttu-id="027f5-203">subjectAlternativeNameType</span><span class="sxs-lookup"><span data-stu-id="027f5-203">subjectAlternativeNameType</span></span>|[<span data-ttu-id="027f5-204">subjectAlternativeNameType</span><span class="sxs-lookup"><span data-stu-id="027f5-204">subjectAlternativeNameType</span></span>](../resources/intune-deviceconfig-subjectalternativenametype.md)|<span data-ttu-id="027f5-205">Tipo de nombre alternativo de sujeto de certificado.</span><span class="sxs-lookup"><span data-stu-id="027f5-205">Certificate Subject Alternative Name Type.</span></span> <span data-ttu-id="027f5-206">Los valores posibles son: `none`, `emailAddress`, `userPrincipalName`, `customAzureADAttribute` y `domainNameService`.</span><span class="sxs-lookup"><span data-stu-id="027f5-206">Possible values are: `none`, `emailAddress`, `userPrincipalName`, `customAzureADAttribute`, `domainNameService`.</span></span>|



## <a name="response"></a><span data-ttu-id="027f5-207">Respuesta</span><span class="sxs-lookup"><span data-stu-id="027f5-207">Response</span></span>
<span data-ttu-id="027f5-208">Si tiene éxito, este método devuelve una `201 Created` código de respuesta y un objeto [androidWorkProfilePkcsCertificateProfile](../resources/intune-deviceconfig-androidworkprofilepkcscertificateprofile.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="027f5-208">If successful, this method returns a `201 Created` response code and a [androidWorkProfilePkcsCertificateProfile](../resources/intune-deviceconfig-androidworkprofilepkcscertificateprofile.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="027f5-209">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="027f5-209">Example</span></span>
### <a name="request"></a><span data-ttu-id="027f5-210">Solicitud</span><span class="sxs-lookup"><span data-stu-id="027f5-210">Request</span></span>
<span data-ttu-id="027f5-211">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="027f5-211">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations
Content-type: application/json
Content-length: 1033

{
  "@odata.type": "#microsoft.graph.androidWorkProfilePkcsCertificateProfile",
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

### <a name="response"></a><span data-ttu-id="027f5-212">Respuesta</span><span class="sxs-lookup"><span data-stu-id="027f5-212">Response</span></span>
<span data-ttu-id="027f5-p117">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="027f5-p117">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 1141

{
  "@odata.type": "#microsoft.graph.androidWorkProfilePkcsCertificateProfile",
  "id": "a7d4a505-a505-a7d4-05a5-d4a705a5d4a7",
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





