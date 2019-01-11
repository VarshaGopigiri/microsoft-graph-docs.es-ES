---
title: Crear iosScepCertificateProfile
description: Crear un nuevo objeto iosScepCertificateProfile.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 9ef2ab2b9d93ca5a343ecc7836a5e22f1660f899
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27842143"
---
# <a name="create-iosscepcertificateprofile"></a><span data-ttu-id="bc308-103">Crear iosScepCertificateProfile</span><span class="sxs-lookup"><span data-stu-id="bc308-103">Create iosScepCertificateProfile</span></span>

> <span data-ttu-id="bc308-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="bc308-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="bc308-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="bc308-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="bc308-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="bc308-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="bc308-107">Crear un nuevo objeto [iosScepCertificateProfile](../resources/intune-deviceconfig-iosscepcertificateprofile.md) .</span><span class="sxs-lookup"><span data-stu-id="bc308-107">Create a new [iosScepCertificateProfile](../resources/intune-deviceconfig-iosscepcertificateprofile.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="bc308-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="bc308-108">Prerequisites</span></span>
<span data-ttu-id="bc308-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="bc308-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="bc308-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="bc308-111">Permission type</span></span>|<span data-ttu-id="bc308-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="bc308-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="bc308-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="bc308-113">Delegated (work or school account)</span></span>|<span data-ttu-id="bc308-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="bc308-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="bc308-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="bc308-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="bc308-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="bc308-116">Not supported.</span></span>|
|<span data-ttu-id="bc308-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="bc308-117">Application</span></span>|<span data-ttu-id="bc308-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="bc308-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="bc308-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="bc308-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceConfigurations
POST /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsDomainJoinConfiguration/networkAccessConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="bc308-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="bc308-120">Request headers</span></span>
|<span data-ttu-id="bc308-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bc308-121">Header</span></span>|<span data-ttu-id="bc308-122">Valor</span><span class="sxs-lookup"><span data-stu-id="bc308-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="bc308-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="bc308-123">Authorization</span></span>|<span data-ttu-id="bc308-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="bc308-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="bc308-125">Accept</span><span class="sxs-lookup"><span data-stu-id="bc308-125">Accept</span></span>|<span data-ttu-id="bc308-126">application/json</span><span class="sxs-lookup"><span data-stu-id="bc308-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="bc308-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="bc308-127">Request body</span></span>
<span data-ttu-id="bc308-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto iosScepCertificateProfile.</span><span class="sxs-lookup"><span data-stu-id="bc308-128">In the request body, supply a JSON representation for the iosScepCertificateProfile object.</span></span>

<span data-ttu-id="bc308-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el iosScepCertificateProfile.</span><span class="sxs-lookup"><span data-stu-id="bc308-129">The following table shows the properties that are required when you create the iosScepCertificateProfile.</span></span>

|<span data-ttu-id="bc308-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="bc308-130">Property</span></span>|<span data-ttu-id="bc308-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="bc308-131">Type</span></span>|<span data-ttu-id="bc308-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="bc308-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="bc308-133">id</span><span class="sxs-lookup"><span data-stu-id="bc308-133">id</span></span>|<span data-ttu-id="bc308-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="bc308-134">String</span></span>|<span data-ttu-id="bc308-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="bc308-135">Key of the entity.</span></span> <span data-ttu-id="bc308-136">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="bc308-136">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="bc308-137">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="bc308-137">lastModifiedDateTime</span></span>|<span data-ttu-id="bc308-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="bc308-138">DateTimeOffset</span></span>|<span data-ttu-id="bc308-139">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="bc308-139">DateTime the object was last modified.</span></span> <span data-ttu-id="bc308-140">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="bc308-140">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="bc308-141">roleScopeTagIds</span><span class="sxs-lookup"><span data-stu-id="bc308-141">roleScopeTagIds</span></span>|<span data-ttu-id="bc308-142">Colección String</span><span class="sxs-lookup"><span data-stu-id="bc308-142">String collection</span></span>|<span data-ttu-id="bc308-143">Lista de etiquetas de ámbito para esta instancia de entidad.</span><span class="sxs-lookup"><span data-stu-id="bc308-143">List of Scope Tags for this Entity instance.</span></span> <span data-ttu-id="bc308-144">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="bc308-144">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="bc308-145">supportsScopeTags</span><span class="sxs-lookup"><span data-stu-id="bc308-145">supportsScopeTags</span></span>|<span data-ttu-id="bc308-146">Booleano</span><span class="sxs-lookup"><span data-stu-id="bc308-146">Boolean</span></span>|<span data-ttu-id="bc308-147">Indica si la configuración del dispositivo subyacente admite la asignación de etiquetas de ámbito.</span><span class="sxs-lookup"><span data-stu-id="bc308-147">Indicates whether or not the underlying Device Configuration supports the assignment of scope tags.</span></span> <span data-ttu-id="bc308-148">No se permite la asignación a la propiedad ScopeTags cuando este valor es false y entidades no estará visibles para los usuarios con ámbito.</span><span class="sxs-lookup"><span data-stu-id="bc308-148">Assigning to the ScopeTags property is not allowed when this value is false and entities will not be visible to scoped users.</span></span> <span data-ttu-id="bc308-149">Esto se produce para las directivas de heredado creadas en Silverlight y se puede resolver por eliminar y volver a crear la directiva en el Portal de Azure.</span><span class="sxs-lookup"><span data-stu-id="bc308-149">This occurs for Legacy policies created in Silverlight and can be resolved by deleting and recreating the policy in the Azure Portal.</span></span> <span data-ttu-id="bc308-150">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="bc308-150">This property is read-only.</span></span> <span data-ttu-id="bc308-151">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="bc308-151">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="bc308-152">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="bc308-152">createdDateTime</span></span>|<span data-ttu-id="bc308-153">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="bc308-153">DateTimeOffset</span></span>|<span data-ttu-id="bc308-154">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="bc308-154">DateTime the object was created.</span></span> <span data-ttu-id="bc308-155">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="bc308-155">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="bc308-156">descripción</span><span class="sxs-lookup"><span data-stu-id="bc308-156">description</span></span>|<span data-ttu-id="bc308-157">Cadena</span><span class="sxs-lookup"><span data-stu-id="bc308-157">String</span></span>|<span data-ttu-id="bc308-158">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bc308-158">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="bc308-159">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="bc308-159">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="bc308-160">displayName</span><span class="sxs-lookup"><span data-stu-id="bc308-160">displayName</span></span>|<span data-ttu-id="bc308-161">Cadena</span><span class="sxs-lookup"><span data-stu-id="bc308-161">String</span></span>|<span data-ttu-id="bc308-162">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bc308-162">Admin provided name of the device configuration.</span></span> <span data-ttu-id="bc308-163">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="bc308-163">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="bc308-164">version</span><span class="sxs-lookup"><span data-stu-id="bc308-164">version</span></span>|<span data-ttu-id="bc308-165">Int32</span><span class="sxs-lookup"><span data-stu-id="bc308-165">Int32</span></span>|<span data-ttu-id="bc308-166">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bc308-166">Version of the device configuration.</span></span> <span data-ttu-id="bc308-167">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="bc308-167">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="bc308-168">renewalThresholdPercentage</span><span class="sxs-lookup"><span data-stu-id="bc308-168">renewalThresholdPercentage</span></span>|<span data-ttu-id="bc308-169">Int32</span><span class="sxs-lookup"><span data-stu-id="bc308-169">Int32</span></span>|<span data-ttu-id="bc308-170">Porcentaje de umbral de renovación de certificado.</span><span class="sxs-lookup"><span data-stu-id="bc308-170">Certificate renewal threshold percentage.</span></span> <span data-ttu-id="bc308-171">Válido valores heredada de 1 a 99 de [iosCertificateProfileBase](../resources/intune-deviceconfig-ioscertificateprofilebase.md)</span><span class="sxs-lookup"><span data-stu-id="bc308-171">Valid values 1 to 99 Inherited from [iosCertificateProfileBase](../resources/intune-deviceconfig-ioscertificateprofilebase.md)</span></span>|
|<span data-ttu-id="bc308-172">subjectNameFormat</span><span class="sxs-lookup"><span data-stu-id="bc308-172">subjectNameFormat</span></span>|[<span data-ttu-id="bc308-173">appleSubjectNameFormat</span><span class="sxs-lookup"><span data-stu-id="bc308-173">appleSubjectNameFormat</span></span>](../resources/intune-deviceconfig-applesubjectnameformat.md)|<span data-ttu-id="bc308-174">Formato de nombre de sujeto de certificado.</span><span class="sxs-lookup"><span data-stu-id="bc308-174">Certificate Subject Name Format.</span></span> <span data-ttu-id="bc308-175">Se hereda de [iosCertificateProfileBase](../resources/intune-deviceconfig-ioscertificateprofilebase.md).</span><span class="sxs-lookup"><span data-stu-id="bc308-175">Inherited from [iosCertificateProfileBase](../resources/intune-deviceconfig-ioscertificateprofilebase.md).</span></span> <span data-ttu-id="bc308-176">Los valores posibles son: `commonName`, `commonNameAsEmail`, `custom`, `commonNameIncludingEmail`, `commonNameAsIMEI`, `commonNameAsSerialNumber`.</span><span class="sxs-lookup"><span data-stu-id="bc308-176">Possible values are: `commonName`, `commonNameAsEmail`, `custom`, `commonNameIncludingEmail`, `commonNameAsIMEI`, `commonNameAsSerialNumber`.</span></span>|
|<span data-ttu-id="bc308-177">subjectAlternativeNameType</span><span class="sxs-lookup"><span data-stu-id="bc308-177">subjectAlternativeNameType</span></span>|[<span data-ttu-id="bc308-178">subjectAlternativeNameType</span><span class="sxs-lookup"><span data-stu-id="bc308-178">subjectAlternativeNameType</span></span>](../resources/intune-deviceconfig-subjectalternativenametype.md)|<span data-ttu-id="bc308-179">Tipo de nombre alternativo del sujeto del certificado.</span><span class="sxs-lookup"><span data-stu-id="bc308-179">Certificate Subject Alternative Name type.</span></span> <span data-ttu-id="bc308-180">Se hereda de [iosCertificateProfileBase](../resources/intune-deviceconfig-ioscertificateprofilebase.md).</span><span class="sxs-lookup"><span data-stu-id="bc308-180">Inherited from [iosCertificateProfileBase](../resources/intune-deviceconfig-ioscertificateprofilebase.md).</span></span> <span data-ttu-id="bc308-181">Los valores posibles son: `none`, `emailAddress`, `userPrincipalName`, `customAzureADAttribute` y `domainNameService`.</span><span class="sxs-lookup"><span data-stu-id="bc308-181">Possible values are: `none`, `emailAddress`, `userPrincipalName`, `customAzureADAttribute`, `domainNameService`.</span></span>|
|<span data-ttu-id="bc308-182">certificateValidityPeriodValue</span><span class="sxs-lookup"><span data-stu-id="bc308-182">certificateValidityPeriodValue</span></span>|<span data-ttu-id="bc308-183">Int32</span><span class="sxs-lookup"><span data-stu-id="bc308-183">Int32</span></span>|<span data-ttu-id="bc308-184">Valor para el período de validez del certificado.</span><span class="sxs-lookup"><span data-stu-id="bc308-184">Value for the Certificate Validity Period.</span></span> <span data-ttu-id="bc308-185">Se hereda de [iosCertificateProfileBase](../resources/intune-deviceconfig-ioscertificateprofilebase.md)</span><span class="sxs-lookup"><span data-stu-id="bc308-185">Inherited from [iosCertificateProfileBase](../resources/intune-deviceconfig-ioscertificateprofilebase.md)</span></span>|
|<span data-ttu-id="bc308-186">certificateValidityPeriodScale</span><span class="sxs-lookup"><span data-stu-id="bc308-186">certificateValidityPeriodScale</span></span>|[<span data-ttu-id="bc308-187">certificateValidityPeriodScale</span><span class="sxs-lookup"><span data-stu-id="bc308-187">certificateValidityPeriodScale</span></span>](../resources/intune-deviceconfig-certificatevalidityperiodscale.md)|<span data-ttu-id="bc308-188">Escala para el período de validez del certificado.</span><span class="sxs-lookup"><span data-stu-id="bc308-188">Scale for the Certificate Validity Period.</span></span> <span data-ttu-id="bc308-189">Se hereda de [iosCertificateProfileBase](../resources/intune-deviceconfig-ioscertificateprofilebase.md).</span><span class="sxs-lookup"><span data-stu-id="bc308-189">Inherited from [iosCertificateProfileBase](../resources/intune-deviceconfig-ioscertificateprofilebase.md).</span></span> <span data-ttu-id="bc308-190">Los valores posibles son: `days`, `months` y `years`.</span><span class="sxs-lookup"><span data-stu-id="bc308-190">Possible values are: `days`, `months`, `years`.</span></span>|
|<span data-ttu-id="bc308-191">scepServerUrls</span><span class="sxs-lookup"><span data-stu-id="bc308-191">scepServerUrls</span></span>|<span data-ttu-id="bc308-192">Colección String</span><span class="sxs-lookup"><span data-stu-id="bc308-192">String collection</span></span>|<span data-ttu-id="bc308-193">Direcciones URL del servidor SCEP.</span><span class="sxs-lookup"><span data-stu-id="bc308-193">SCEP Server Url(s).</span></span>|
|<span data-ttu-id="bc308-194">subjectNameFormatString</span><span class="sxs-lookup"><span data-stu-id="bc308-194">subjectNameFormatString</span></span>|<span data-ttu-id="bc308-195">Cadena</span><span class="sxs-lookup"><span data-stu-id="bc308-195">String</span></span>|<span data-ttu-id="bc308-196">Formato personalizado para usar con SubjectNameFormat = personalizada.</span><span class="sxs-lookup"><span data-stu-id="bc308-196">Custom format to use with SubjectNameFormat = Custom.</span></span> <span data-ttu-id="bc308-197">Ejemplo: CN = {{EmailAddress}}, E = {{EmailAddress}}, OU = Users de la empresa, O = Contoso Corporation, L = Redmond, ST = WA, C = US</span><span class="sxs-lookup"><span data-stu-id="bc308-197">Example: CN={{EmailAddress}},E={{EmailAddress}},OU=Enterprise Users,O=Contoso Corporation,L=Redmond,ST=WA,C=US</span></span>|
|<span data-ttu-id="bc308-198">keyUsage</span><span class="sxs-lookup"><span data-stu-id="bc308-198">keyUsage</span></span>|[<span data-ttu-id="bc308-199">keyUsages</span><span class="sxs-lookup"><span data-stu-id="bc308-199">keyUsages</span></span>](../resources/intune-deviceconfig-keyusages.md)|<span data-ttu-id="bc308-200">Uso de la clave SCEP.</span><span class="sxs-lookup"><span data-stu-id="bc308-200">SCEP Key Usage.</span></span> <span data-ttu-id="bc308-201">Los valores posibles son: `keyEncipherment` y `digitalSignature`.</span><span class="sxs-lookup"><span data-stu-id="bc308-201">Possible values are: `keyEncipherment`, `digitalSignature`.</span></span>|
|<span data-ttu-id="bc308-202">keySize</span><span class="sxs-lookup"><span data-stu-id="bc308-202">keySize</span></span>|[<span data-ttu-id="bc308-203">keySize</span><span class="sxs-lookup"><span data-stu-id="bc308-203">keySize</span></span>](../resources/intune-deviceconfig-keysize.md)|<span data-ttu-id="bc308-204">Tamaño de la clave SCEP.</span><span class="sxs-lookup"><span data-stu-id="bc308-204">SCEP Key Size.</span></span> <span data-ttu-id="bc308-205">Los valores posibles son: `size1024` y `size2048`.</span><span class="sxs-lookup"><span data-stu-id="bc308-205">Possible values are: `size1024`, `size2048`.</span></span>|
|<span data-ttu-id="bc308-206">extendedKeyUsages</span><span class="sxs-lookup"><span data-stu-id="bc308-206">extendedKeyUsages</span></span>|<span data-ttu-id="bc308-207">colección de [ExtendeKeyUsage](../resources/intune-deviceconfig-extendedkeyusage.md)</span><span class="sxs-lookup"><span data-stu-id="bc308-207">[extendedKeyUsage](../resources/intune-deviceconfig-extendedkeyusage.md) collection</span></span>|<span data-ttu-id="bc308-208">Configuración de clave (EKU) extendida.</span><span class="sxs-lookup"><span data-stu-id="bc308-208">Extended Key Usage (EKU) settings.</span></span> <span data-ttu-id="bc308-209">Esta colección puede contener un máximo de 500 elementos.</span><span class="sxs-lookup"><span data-stu-id="bc308-209">This collection can contain a maximum of 500 elements.</span></span>|
|<span data-ttu-id="bc308-210">subjectAlternativeNameFormatString</span><span class="sxs-lookup"><span data-stu-id="bc308-210">subjectAlternativeNameFormatString</span></span>|<span data-ttu-id="bc308-211">Cadena</span><span class="sxs-lookup"><span data-stu-id="bc308-211">String</span></span>|<span data-ttu-id="bc308-212">Cadena personalizada que define el atributo AAD.</span><span class="sxs-lookup"><span data-stu-id="bc308-212">Custom String that defines the AAD Attribute.</span></span>|
|<span data-ttu-id="bc308-213">certificateStore</span><span class="sxs-lookup"><span data-stu-id="bc308-213">certificateStore</span></span>|[<span data-ttu-id="bc308-214">certificateStore</span><span class="sxs-lookup"><span data-stu-id="bc308-214">certificateStore</span></span>](../resources/intune-deviceconfig-certificatestore.md)|<span data-ttu-id="bc308-215">Certificado del almacén de destino.</span><span class="sxs-lookup"><span data-stu-id="bc308-215">Target store certificate.</span></span> <span data-ttu-id="bc308-216">Los valores posibles son: `user` y `machine`.</span><span class="sxs-lookup"><span data-stu-id="bc308-216">Possible values are: `user`, `machine`.</span></span>|
|<span data-ttu-id="bc308-217">customSubjectAlternativeNames</span><span class="sxs-lookup"><span data-stu-id="bc308-217">customSubjectAlternativeNames</span></span>|<span data-ttu-id="bc308-218">colección de [customSubjectAlternativeName](../resources/intune-deviceconfig-customsubjectalternativename.md)</span><span class="sxs-lookup"><span data-stu-id="bc308-218">[customSubjectAlternativeName](../resources/intune-deviceconfig-customsubjectalternativename.md) collection</span></span>|<span data-ttu-id="bc308-219">Configuración de Alterantive nombre de sujeto personalizado.</span><span class="sxs-lookup"><span data-stu-id="bc308-219">Custom Subject Alterantive Name Settings.</span></span> <span data-ttu-id="bc308-220">Esta colección puede contener un máximo de 500 elementos.</span><span class="sxs-lookup"><span data-stu-id="bc308-220">This collection can contain a maximum of 500 elements.</span></span>|



## <a name="response"></a><span data-ttu-id="bc308-221">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bc308-221">Response</span></span>
<span data-ttu-id="bc308-222">Si tiene éxito, este método devuelve una `201 Created` código de respuesta y un objeto [iosScepCertificateProfile](../resources/intune-deviceconfig-iosscepcertificateprofile.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="bc308-222">If successful, this method returns a `201 Created` response code and a [iosScepCertificateProfile](../resources/intune-deviceconfig-iosscepcertificateprofile.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="bc308-223">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="bc308-223">Example</span></span>
### <a name="request"></a><span data-ttu-id="bc308-224">Solicitud</span><span class="sxs-lookup"><span data-stu-id="bc308-224">Request</span></span>
<span data-ttu-id="bc308-225">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="bc308-225">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations
Content-type: application/json
Content-length: 1223

{
  "@odata.type": "#microsoft.graph.iosScepCertificateProfile",
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
  "scepServerUrls": [
    "Scep Server Urls value"
  ],
  "subjectNameFormatString": "Subject Name Format String value",
  "keyUsage": "digitalSignature",
  "keySize": "size2048",
  "extendedKeyUsages": [
    {
      "@odata.type": "microsoft.graph.extendedKeyUsage",
      "name": "Name value",
      "objectIdentifier": "Object Identifier value"
    }
  ],
  "subjectAlternativeNameFormatString": "Subject Alternative Name Format String value",
  "certificateStore": "machine",
  "customSubjectAlternativeNames": [
    {
      "@odata.type": "microsoft.graph.customSubjectAlternativeName",
      "sanType": "emailAddress",
      "name": "Name value"
    }
  ]
}
```

### <a name="response"></a><span data-ttu-id="bc308-226">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bc308-226">Response</span></span>
<span data-ttu-id="bc308-p122">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="bc308-p122">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 1331

{
  "@odata.type": "#microsoft.graph.iosScepCertificateProfile",
  "id": "0deb8dbf-8dbf-0deb-bf8d-eb0dbf8deb0d",
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
  "scepServerUrls": [
    "Scep Server Urls value"
  ],
  "subjectNameFormatString": "Subject Name Format String value",
  "keyUsage": "digitalSignature",
  "keySize": "size2048",
  "extendedKeyUsages": [
    {
      "@odata.type": "microsoft.graph.extendedKeyUsage",
      "name": "Name value",
      "objectIdentifier": "Object Identifier value"
    }
  ],
  "subjectAlternativeNameFormatString": "Subject Alternative Name Format String value",
  "certificateStore": "machine",
  "customSubjectAlternativeNames": [
    {
      "@odata.type": "microsoft.graph.customSubjectAlternativeName",
      "sanType": "emailAddress",
      "name": "Name value"
    }
  ]
}
```





