---
title: Crear windowsPhone81SCEPCertificateProfile
description: Crear un nuevo objeto windowsPhone81SCEPCertificateProfile.
ms.openlocfilehash: 16e06b5b323fb0ce12593e7ec5561a92f1fe2b80
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085116"
---
# <a name="create-windowsphone81scepcertificateprofile"></a><span data-ttu-id="13c62-103">Crear windowsPhone81SCEPCertificateProfile</span><span class="sxs-lookup"><span data-stu-id="13c62-103">Create windowsPhone81SCEPCertificateProfile</span></span>

> <span data-ttu-id="13c62-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="13c62-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="13c62-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="13c62-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="13c62-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="13c62-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="13c62-107">Crear un nuevo objeto [windowsPhone81SCEPCertificateProfile](../resources/intune-deviceconfig-windowsphone81scepcertificateprofile.md) .</span><span class="sxs-lookup"><span data-stu-id="13c62-107">Create a new [windowsPhone81SCEPCertificateProfile](../resources/intune-deviceconfig-windowsphone81scepcertificateprofile.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="13c62-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="13c62-108">Prerequisites</span></span>
<span data-ttu-id="13c62-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="13c62-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="13c62-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="13c62-111">Permission type</span></span>|<span data-ttu-id="13c62-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="13c62-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="13c62-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="13c62-113">Delegated (work or school account)</span></span>|<span data-ttu-id="13c62-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="13c62-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="13c62-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="13c62-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="13c62-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="13c62-116">Not supported.</span></span>|
|<span data-ttu-id="13c62-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="13c62-117">Application</span></span>|<span data-ttu-id="13c62-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="13c62-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="13c62-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="13c62-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceConfigurations
POST /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsDomainJoinConfiguration/networkAccessConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="13c62-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="13c62-120">Request headers</span></span>
|<span data-ttu-id="13c62-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="13c62-121">Header</span></span>|<span data-ttu-id="13c62-122">Valor</span><span class="sxs-lookup"><span data-stu-id="13c62-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="13c62-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="13c62-123">Authorization</span></span>|<span data-ttu-id="13c62-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="13c62-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="13c62-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="13c62-125">Accept</span></span>|<span data-ttu-id="13c62-126">application/json</span><span class="sxs-lookup"><span data-stu-id="13c62-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="13c62-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="13c62-127">Request body</span></span>
<span data-ttu-id="13c62-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto windowsPhone81SCEPCertificateProfile.</span><span class="sxs-lookup"><span data-stu-id="13c62-128">In the request body, supply a JSON representation for the windowsPhone81SCEPCertificateProfile object.</span></span>

<span data-ttu-id="13c62-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el windowsPhone81SCEPCertificateProfile.</span><span class="sxs-lookup"><span data-stu-id="13c62-129">The following table shows the properties that are required when you create the windowsPhone81SCEPCertificateProfile.</span></span>

|<span data-ttu-id="13c62-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="13c62-130">Property</span></span>|<span data-ttu-id="13c62-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="13c62-131">Type</span></span>|<span data-ttu-id="13c62-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="13c62-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="13c62-133">id</span><span class="sxs-lookup"><span data-stu-id="13c62-133">id</span></span>|<span data-ttu-id="13c62-134">String</span><span class="sxs-lookup"><span data-stu-id="13c62-134">String</span></span>|<span data-ttu-id="13c62-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="13c62-135">Key of the entity.</span></span> <span data-ttu-id="13c62-136">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="13c62-136">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="13c62-137">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="13c62-137">lastModifiedDateTime</span></span>|<span data-ttu-id="13c62-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="13c62-138">DateTimeOffset</span></span>|<span data-ttu-id="13c62-139">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="13c62-139">DateTime the object was last modified.</span></span> <span data-ttu-id="13c62-140">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="13c62-140">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="13c62-141">roleScopeTagIds</span><span class="sxs-lookup"><span data-stu-id="13c62-141">roleScopeTagIds</span></span>|<span data-ttu-id="13c62-142">Colección String</span><span class="sxs-lookup"><span data-stu-id="13c62-142">String collection</span></span>|<span data-ttu-id="13c62-143">Lista de etiquetas de ámbito para esta instancia de entidad.</span><span class="sxs-lookup"><span data-stu-id="13c62-143">List of Scope Tags for this Entity instance.</span></span> <span data-ttu-id="13c62-144">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="13c62-144">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="13c62-145">supportsScopeTags</span><span class="sxs-lookup"><span data-stu-id="13c62-145">supportsScopeTags</span></span>|<span data-ttu-id="13c62-146">Booleano</span><span class="sxs-lookup"><span data-stu-id="13c62-146">Boolean</span></span>|<span data-ttu-id="13c62-147">Indica si la configuración del dispositivo subyacente admite la asignación de etiquetas de ámbito.</span><span class="sxs-lookup"><span data-stu-id="13c62-147">Indicates whether or not the underlying Device Configuration supports the assignment of scope tags.</span></span> <span data-ttu-id="13c62-148">No se permite la asignación a la propiedad ScopeTags cuando este valor es false y entidades no estará visibles para los usuarios con ámbito.</span><span class="sxs-lookup"><span data-stu-id="13c62-148">Assigning to the ScopeTags property is not allowed when this value is false and entities will not be visible to scoped users.</span></span> <span data-ttu-id="13c62-149">Esto se produce para las directivas de heredado creadas en Silverlight y se puede resolver por eliminar y volver a crear la directiva en el Portal de Azure.</span><span class="sxs-lookup"><span data-stu-id="13c62-149">This occurs for Legacy policies created in Silverlight and can be resolved by deleting and recreating the policy in the Azure Portal.</span></span> <span data-ttu-id="13c62-150">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="13c62-150">This property is read-only.</span></span> <span data-ttu-id="13c62-151">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="13c62-151">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="13c62-152">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="13c62-152">createdDateTime</span></span>|<span data-ttu-id="13c62-153">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="13c62-153">DateTimeOffset</span></span>|<span data-ttu-id="13c62-154">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="13c62-154">DateTime the object was created.</span></span> <span data-ttu-id="13c62-155">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="13c62-155">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="13c62-156">descripción</span><span class="sxs-lookup"><span data-stu-id="13c62-156">description</span></span>|<span data-ttu-id="13c62-157">String</span><span class="sxs-lookup"><span data-stu-id="13c62-157">String</span></span>|<span data-ttu-id="13c62-158">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="13c62-158">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="13c62-159">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="13c62-159">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="13c62-160">displayName</span><span class="sxs-lookup"><span data-stu-id="13c62-160">displayName</span></span>|<span data-ttu-id="13c62-161">String</span><span class="sxs-lookup"><span data-stu-id="13c62-161">String</span></span>|<span data-ttu-id="13c62-162">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="13c62-162">Admin provided name of the device configuration.</span></span> <span data-ttu-id="13c62-163">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="13c62-163">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="13c62-164">version</span><span class="sxs-lookup"><span data-stu-id="13c62-164">version</span></span>|<span data-ttu-id="13c62-165">Int32</span><span class="sxs-lookup"><span data-stu-id="13c62-165">Int32</span></span>|<span data-ttu-id="13c62-166">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="13c62-166">Version of the device configuration.</span></span> <span data-ttu-id="13c62-167">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="13c62-167">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="13c62-168">renewalThresholdPercentage</span><span class="sxs-lookup"><span data-stu-id="13c62-168">renewalThresholdPercentage</span></span>|<span data-ttu-id="13c62-169">Int32</span><span class="sxs-lookup"><span data-stu-id="13c62-169">Int32</span></span>|<span data-ttu-id="13c62-170">Porcentaje de umbral de renovación de certificado.</span><span class="sxs-lookup"><span data-stu-id="13c62-170">Certificate renewal threshold percentage.</span></span> <span data-ttu-id="13c62-171">Se hereda de [windowsPhone81CertificateProfileBase](../resources/intune-deviceconfig-windowsphone81certificateprofilebase.md)</span><span class="sxs-lookup"><span data-stu-id="13c62-171">Inherited from [windowsPhone81CertificateProfileBase](../resources/intune-deviceconfig-windowsphone81certificateprofilebase.md)</span></span>|
|<span data-ttu-id="13c62-172">keyStorageProvider</span><span class="sxs-lookup"><span data-stu-id="13c62-172">keyStorageProvider</span></span>|[<span data-ttu-id="13c62-173">keyStorageProviderOption</span><span class="sxs-lookup"><span data-stu-id="13c62-173">keyStorageProviderOption</span></span>](../resources/intune-deviceconfig-keystorageprovideroption.md)|<span data-ttu-id="13c62-174">Proveedor de almacenamiento de claves (KSP).</span><span class="sxs-lookup"><span data-stu-id="13c62-174">Key Storage Provider (KSP).</span></span> <span data-ttu-id="13c62-175">Se hereda de [windowsPhone81CertificateProfileBase](../resources/intune-deviceconfig-windowsphone81certificateprofilebase.md).</span><span class="sxs-lookup"><span data-stu-id="13c62-175">Inherited from [windowsPhone81CertificateProfileBase](../resources/intune-deviceconfig-windowsphone81certificateprofilebase.md).</span></span> <span data-ttu-id="13c62-176">Los valores posibles son: `useTpmKspOtherwiseUseSoftwareKsp`, `useTpmKspOtherwiseFail`, `usePassportForWorkKspOtherwiseFail` y `useSoftwareKsp`.</span><span class="sxs-lookup"><span data-stu-id="13c62-176">Possible values are: `useTpmKspOtherwiseUseSoftwareKsp`, `useTpmKspOtherwiseFail`, `usePassportForWorkKspOtherwiseFail`, `useSoftwareKsp`.</span></span>|
|<span data-ttu-id="13c62-177">subjectNameFormat</span><span class="sxs-lookup"><span data-stu-id="13c62-177">subjectNameFormat</span></span>|[<span data-ttu-id="13c62-178">subjectNameFormat</span><span class="sxs-lookup"><span data-stu-id="13c62-178">subjectNameFormat</span></span>](../resources/intune-deviceconfig-subjectnameformat.md)|<span data-ttu-id="13c62-179">Formato de nombre de sujeto de certificado.</span><span class="sxs-lookup"><span data-stu-id="13c62-179">Certificate Subject Name Format.</span></span> <span data-ttu-id="13c62-180">Se hereda de [windowsPhone81CertificateProfileBase](../resources/intune-deviceconfig-windowsphone81certificateprofilebase.md).</span><span class="sxs-lookup"><span data-stu-id="13c62-180">Inherited from [windowsPhone81CertificateProfileBase](../resources/intune-deviceconfig-windowsphone81certificateprofilebase.md).</span></span> <span data-ttu-id="13c62-181">Los valores posibles son: `commonName`, `commonNameIncludingEmail`, `commonNameAsEmail`, `custom`, `commonNameAsIMEI`, `commonNameAsSerialNumber`, `commonNameAsAadDeviceId`, `commonNameAsIntuneDeviceId` y `commonNameAsDurableDeviceId`.</span><span class="sxs-lookup"><span data-stu-id="13c62-181">Possible values are: `commonName`, `commonNameIncludingEmail`, `commonNameAsEmail`, `custom`, `commonNameAsIMEI`, `commonNameAsSerialNumber`, `commonNameAsAadDeviceId`, `commonNameAsIntuneDeviceId`, `commonNameAsDurableDeviceId`.</span></span>|
|<span data-ttu-id="13c62-182">subjectAlternativeNameType</span><span class="sxs-lookup"><span data-stu-id="13c62-182">subjectAlternativeNameType</span></span>|[<span data-ttu-id="13c62-183">subjectAlternativeNameType</span><span class="sxs-lookup"><span data-stu-id="13c62-183">subjectAlternativeNameType</span></span>](../resources/intune-deviceconfig-subjectalternativenametype.md)|<span data-ttu-id="13c62-184">Tipo de nombre alternativo de sujeto de certificado.</span><span class="sxs-lookup"><span data-stu-id="13c62-184">Certificate Subject Alternative Name Type.</span></span> <span data-ttu-id="13c62-185">Se hereda de [windowsPhone81CertificateProfileBase](../resources/intune-deviceconfig-windowsphone81certificateprofilebase.md).</span><span class="sxs-lookup"><span data-stu-id="13c62-185">Inherited from [windowsPhone81CertificateProfileBase](../resources/intune-deviceconfig-windowsphone81certificateprofilebase.md).</span></span> <span data-ttu-id="13c62-186">Los valores posibles son: `none`, `emailAddress`, `userPrincipalName`, `customAzureADAttribute` y `domainNameService`.</span><span class="sxs-lookup"><span data-stu-id="13c62-186">Possible values are: `none`, `emailAddress`, `userPrincipalName`, `customAzureADAttribute`, `domainNameService`.</span></span>|
|<span data-ttu-id="13c62-187">certificateValidityPeriodValue</span><span class="sxs-lookup"><span data-stu-id="13c62-187">certificateValidityPeriodValue</span></span>|<span data-ttu-id="13c62-188">Int32</span><span class="sxs-lookup"><span data-stu-id="13c62-188">Int32</span></span>|<span data-ttu-id="13c62-189">Valor para el período de Validtiy de certificado.</span><span class="sxs-lookup"><span data-stu-id="13c62-189">Value for the Certificate Validtiy Period.</span></span> <span data-ttu-id="13c62-190">Se hereda de [windowsPhone81CertificateProfileBase](../resources/intune-deviceconfig-windowsphone81certificateprofilebase.md)</span><span class="sxs-lookup"><span data-stu-id="13c62-190">Inherited from [windowsPhone81CertificateProfileBase](../resources/intune-deviceconfig-windowsphone81certificateprofilebase.md)</span></span>|
|<span data-ttu-id="13c62-191">certificateValidityPeriodScale</span><span class="sxs-lookup"><span data-stu-id="13c62-191">certificateValidityPeriodScale</span></span>|[<span data-ttu-id="13c62-192">certificateValidityPeriodScale</span><span class="sxs-lookup"><span data-stu-id="13c62-192">certificateValidityPeriodScale</span></span>](../resources/intune-deviceconfig-certificatevalidityperiodscale.md)|<span data-ttu-id="13c62-193">Escala para el período de validez del certificado.</span><span class="sxs-lookup"><span data-stu-id="13c62-193">Scale for the Certificate Validity Period.</span></span> <span data-ttu-id="13c62-194">Se hereda de [windowsPhone81CertificateProfileBase](../resources/intune-deviceconfig-windowsphone81certificateprofilebase.md).</span><span class="sxs-lookup"><span data-stu-id="13c62-194">Inherited from [windowsPhone81CertificateProfileBase](../resources/intune-deviceconfig-windowsphone81certificateprofilebase.md).</span></span> <span data-ttu-id="13c62-195">Los valores posibles son: `days`, `months` y `years`.</span><span class="sxs-lookup"><span data-stu-id="13c62-195">Possible values are: `days`, `months`, `years`.</span></span>|
|<span data-ttu-id="13c62-196">extendedKeyUsages</span><span class="sxs-lookup"><span data-stu-id="13c62-196">extendedKeyUsages</span></span>|<span data-ttu-id="13c62-197">colección de [ExtendeKeyUsage](../resources/intune-deviceconfig-extendedkeyusage.md)</span><span class="sxs-lookup"><span data-stu-id="13c62-197">[extendedKeyUsage](../resources/intune-deviceconfig-extendedkeyusage.md) collection</span></span>|<span data-ttu-id="13c62-198">Configuración de clave (EKU) extendida.</span><span class="sxs-lookup"><span data-stu-id="13c62-198">Extended Key Usage (EKU) settings.</span></span> <span data-ttu-id="13c62-199">Esta colección puede contener un máximo de 500 elementos.</span><span class="sxs-lookup"><span data-stu-id="13c62-199">This collection can contain a maximum of 500 elements.</span></span> <span data-ttu-id="13c62-200">Se hereda de [windowsPhone81CertificateProfileBase](../resources/intune-deviceconfig-windowsphone81certificateprofilebase.md)</span><span class="sxs-lookup"><span data-stu-id="13c62-200">Inherited from [windowsPhone81CertificateProfileBase](../resources/intune-deviceconfig-windowsphone81certificateprofilebase.md)</span></span>|
|<span data-ttu-id="13c62-201">scepServerUrls</span><span class="sxs-lookup"><span data-stu-id="13c62-201">scepServerUrls</span></span>|<span data-ttu-id="13c62-202">Colección String</span><span class="sxs-lookup"><span data-stu-id="13c62-202">String collection</span></span>|<span data-ttu-id="13c62-203">Direcciones URL del servidor SCEP.</span><span class="sxs-lookup"><span data-stu-id="13c62-203">SCEP Server Url(s).</span></span>|
|<span data-ttu-id="13c62-204">subjectNameFormatString</span><span class="sxs-lookup"><span data-stu-id="13c62-204">subjectNameFormatString</span></span>|<span data-ttu-id="13c62-205">String</span><span class="sxs-lookup"><span data-stu-id="13c62-205">String</span></span>|<span data-ttu-id="13c62-206">Formato personalizado para usar con SubjectNameFormat = personalizada.</span><span class="sxs-lookup"><span data-stu-id="13c62-206">Custom format to use with SubjectNameFormat = Custom.</span></span> <span data-ttu-id="13c62-207">Ejemplo: CN = {{EmailAddress}}, E = {{EmailAddress}}, OU = Users de la empresa, O = Contoso Corporation, L = Redmond, ST = WA, C = US</span><span class="sxs-lookup"><span data-stu-id="13c62-207">Example: CN={{EmailAddress}},E={{EmailAddress}},OU=Enterprise Users,O=Contoso Corporation,L=Redmond,ST=WA,C=US</span></span>|
|<span data-ttu-id="13c62-208">keyUsage</span><span class="sxs-lookup"><span data-stu-id="13c62-208">keyUsage</span></span>|[<span data-ttu-id="13c62-209">keyUsages</span><span class="sxs-lookup"><span data-stu-id="13c62-209">keyUsages</span></span>](../resources/intune-deviceconfig-keyusages.md)|<span data-ttu-id="13c62-210">Uso de la clave SCEP.</span><span class="sxs-lookup"><span data-stu-id="13c62-210">SCEP Key Usage.</span></span> <span data-ttu-id="13c62-211">Los valores posibles son: `keyEncipherment` y `digitalSignature`.</span><span class="sxs-lookup"><span data-stu-id="13c62-211">Possible values are: `keyEncipherment`, `digitalSignature`.</span></span>|
|<span data-ttu-id="13c62-212">keySize</span><span class="sxs-lookup"><span data-stu-id="13c62-212">keySize</span></span>|[<span data-ttu-id="13c62-213">keySize</span><span class="sxs-lookup"><span data-stu-id="13c62-213">keySize</span></span>](../resources/intune-deviceconfig-keysize.md)|<span data-ttu-id="13c62-214">Tamaño de la clave SCEP.</span><span class="sxs-lookup"><span data-stu-id="13c62-214">SCEP Key Size.</span></span> <span data-ttu-id="13c62-215">Los valores posibles son: `size1024` y `size2048`.</span><span class="sxs-lookup"><span data-stu-id="13c62-215">Possible values are: `size1024`, `size2048`.</span></span>|
|<span data-ttu-id="13c62-216">hashAlgorithm</span><span class="sxs-lookup"><span data-stu-id="13c62-216">hashAlgorithm</span></span>|[<span data-ttu-id="13c62-217">hashAlgorithms</span><span class="sxs-lookup"><span data-stu-id="13c62-217">hashAlgorithms</span></span>](../resources/intune-deviceconfig-hashalgorithms.md)|<span data-ttu-id="13c62-218">Algoritmo de Hash SCEP.</span><span class="sxs-lookup"><span data-stu-id="13c62-218">SCEP Hash Algorithm.</span></span> <span data-ttu-id="13c62-219">Los valores posibles son: `sha1` y `sha2`.</span><span class="sxs-lookup"><span data-stu-id="13c62-219">Possible values are: `sha1`, `sha2`.</span></span>|
|<span data-ttu-id="13c62-220">subjectAlternativeNameFormatString</span><span class="sxs-lookup"><span data-stu-id="13c62-220">subjectAlternativeNameFormatString</span></span>|<span data-ttu-id="13c62-221">String</span><span class="sxs-lookup"><span data-stu-id="13c62-221">String</span></span>|<span data-ttu-id="13c62-222">Cadena personalizada que define el atributo AAD.</span><span class="sxs-lookup"><span data-stu-id="13c62-222">Custom String that defines the AAD Attribute.</span></span>|



## <a name="response"></a><span data-ttu-id="13c62-223">Respuesta</span><span class="sxs-lookup"><span data-stu-id="13c62-223">Response</span></span>
<span data-ttu-id="13c62-224">Si tiene éxito, este método devuelve una `201 Created` código de respuesta y un objeto [windowsPhone81SCEPCertificateProfile](../resources/intune-deviceconfig-windowsphone81scepcertificateprofile.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="13c62-224">If successful, this method returns a `201 Created` response code and a [windowsPhone81SCEPCertificateProfile](../resources/intune-deviceconfig-windowsphone81scepcertificateprofile.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="13c62-225">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="13c62-225">Example</span></span>
### <a name="request"></a><span data-ttu-id="13c62-226">Solicitud</span><span class="sxs-lookup"><span data-stu-id="13c62-226">Request</span></span>
<span data-ttu-id="13c62-227">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="13c62-227">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations
Content-type: application/json
Content-length: 1096

{
  "@odata.type": "#microsoft.graph.windowsPhone81SCEPCertificateProfile",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "roleScopeTagIds": [
    "Role Scope Tag Ids value"
  ],
  "supportsScopeTags": true,
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "renewalThresholdPercentage": 10,
  "keyStorageProvider": "useTpmKspOtherwiseFail",
  "subjectNameFormat": "commonNameIncludingEmail",
  "subjectAlternativeNameType": "emailAddress",
  "certificateValidityPeriodValue": 14,
  "certificateValidityPeriodScale": "months",
  "extendedKeyUsages": [
    {
      "@odata.type": "microsoft.graph.extendedKeyUsage",
      "name": "Name value",
      "objectIdentifier": "Object Identifier value"
    }
  ],
  "scepServerUrls": [
    "Scep Server Urls value"
  ],
  "subjectNameFormatString": "Subject Name Format String value",
  "keyUsage": "digitalSignature",
  "keySize": "size2048",
  "hashAlgorithm": "sha2",
  "subjectAlternativeNameFormatString": "Subject Alternative Name Format String value"
}
```

### <a name="response"></a><span data-ttu-id="13c62-228">Respuesta</span><span class="sxs-lookup"><span data-stu-id="13c62-228">Response</span></span>
<span data-ttu-id="13c62-p122">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="13c62-p122">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 1204

{
  "@odata.type": "#microsoft.graph.windowsPhone81SCEPCertificateProfile",
  "id": "f070e30e-e30e-f070-0ee3-70f00ee370f0",
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
  "keyStorageProvider": "useTpmKspOtherwiseFail",
  "subjectNameFormat": "commonNameIncludingEmail",
  "subjectAlternativeNameType": "emailAddress",
  "certificateValidityPeriodValue": 14,
  "certificateValidityPeriodScale": "months",
  "extendedKeyUsages": [
    {
      "@odata.type": "microsoft.graph.extendedKeyUsage",
      "name": "Name value",
      "objectIdentifier": "Object Identifier value"
    }
  ],
  "scepServerUrls": [
    "Scep Server Urls value"
  ],
  "subjectNameFormatString": "Subject Name Format String value",
  "keyUsage": "digitalSignature",
  "keySize": "size2048",
  "hashAlgorithm": "sha2",
  "subjectAlternativeNameFormatString": "Subject Alternative Name Format String value"
}
```





