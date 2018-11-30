---
title: Crear windows10PkcsCertificateProfile
description: Crear un nuevo objeto windows10PkcsCertificateProfile.
ms.openlocfilehash: 507188fd0556480efde976e69b0717f85c6a407f
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084246"
---
# <a name="create-windows10pkcscertificateprofile"></a><span data-ttu-id="274d6-103">Crear windows10PkcsCertificateProfile</span><span class="sxs-lookup"><span data-stu-id="274d6-103">Create windows10PkcsCertificateProfile</span></span>

> <span data-ttu-id="274d6-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="274d6-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="274d6-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="274d6-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="274d6-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="274d6-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="274d6-107">Crear un nuevo objeto [windows10PkcsCertificateProfile](../resources/intune-deviceconfig-windows10pkcscertificateprofile.md) .</span><span class="sxs-lookup"><span data-stu-id="274d6-107">Create a new [windows10PkcsCertificateProfile](../resources/intune-deviceconfig-windows10pkcscertificateprofile.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="274d6-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="274d6-108">Prerequisites</span></span>
<span data-ttu-id="274d6-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="274d6-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="274d6-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="274d6-111">Permission type</span></span>|<span data-ttu-id="274d6-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="274d6-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="274d6-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="274d6-113">Delegated (work or school account)</span></span>|<span data-ttu-id="274d6-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="274d6-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="274d6-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="274d6-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="274d6-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="274d6-116">Not supported.</span></span>|
|<span data-ttu-id="274d6-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="274d6-117">Application</span></span>|<span data-ttu-id="274d6-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="274d6-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="274d6-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="274d6-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceConfigurations
POST /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsDomainJoinConfiguration/networkAccessConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="274d6-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="274d6-120">Request headers</span></span>
|<span data-ttu-id="274d6-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="274d6-121">Header</span></span>|<span data-ttu-id="274d6-122">Valor</span><span class="sxs-lookup"><span data-stu-id="274d6-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="274d6-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="274d6-123">Authorization</span></span>|<span data-ttu-id="274d6-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="274d6-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="274d6-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="274d6-125">Accept</span></span>|<span data-ttu-id="274d6-126">application/json</span><span class="sxs-lookup"><span data-stu-id="274d6-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="274d6-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="274d6-127">Request body</span></span>
<span data-ttu-id="274d6-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto windows10PkcsCertificateProfile.</span><span class="sxs-lookup"><span data-stu-id="274d6-128">In the request body, supply a JSON representation for the windows10PkcsCertificateProfile object.</span></span>

<span data-ttu-id="274d6-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el windows10PkcsCertificateProfile.</span><span class="sxs-lookup"><span data-stu-id="274d6-129">The following table shows the properties that are required when you create the windows10PkcsCertificateProfile.</span></span>

|<span data-ttu-id="274d6-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="274d6-130">Property</span></span>|<span data-ttu-id="274d6-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="274d6-131">Type</span></span>|<span data-ttu-id="274d6-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="274d6-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="274d6-133">id</span><span class="sxs-lookup"><span data-stu-id="274d6-133">id</span></span>|<span data-ttu-id="274d6-134">String</span><span class="sxs-lookup"><span data-stu-id="274d6-134">String</span></span>|<span data-ttu-id="274d6-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="274d6-135">Key of the entity.</span></span> <span data-ttu-id="274d6-136">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="274d6-136">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="274d6-137">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="274d6-137">lastModifiedDateTime</span></span>|<span data-ttu-id="274d6-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="274d6-138">DateTimeOffset</span></span>|<span data-ttu-id="274d6-139">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="274d6-139">DateTime the object was last modified.</span></span> <span data-ttu-id="274d6-140">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="274d6-140">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="274d6-141">roleScopeTagIds</span><span class="sxs-lookup"><span data-stu-id="274d6-141">roleScopeTagIds</span></span>|<span data-ttu-id="274d6-142">Colección String</span><span class="sxs-lookup"><span data-stu-id="274d6-142">String collection</span></span>|<span data-ttu-id="274d6-143">Lista de etiquetas de ámbito para esta instancia de entidad.</span><span class="sxs-lookup"><span data-stu-id="274d6-143">List of Scope Tags for this Entity instance.</span></span> <span data-ttu-id="274d6-144">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="274d6-144">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="274d6-145">supportsScopeTags</span><span class="sxs-lookup"><span data-stu-id="274d6-145">supportsScopeTags</span></span>|<span data-ttu-id="274d6-146">Booleano</span><span class="sxs-lookup"><span data-stu-id="274d6-146">Boolean</span></span>|<span data-ttu-id="274d6-147">Indica si la configuración del dispositivo subyacente admite la asignación de etiquetas de ámbito.</span><span class="sxs-lookup"><span data-stu-id="274d6-147">Indicates whether or not the underlying Device Configuration supports the assignment of scope tags.</span></span> <span data-ttu-id="274d6-148">No se permite la asignación a la propiedad ScopeTags cuando este valor es false y entidades no estará visibles para los usuarios con ámbito.</span><span class="sxs-lookup"><span data-stu-id="274d6-148">Assigning to the ScopeTags property is not allowed when this value is false and entities will not be visible to scoped users.</span></span> <span data-ttu-id="274d6-149">Esto se produce para las directivas de heredado creadas en Silverlight y se puede resolver por eliminar y volver a crear la directiva en el Portal de Azure.</span><span class="sxs-lookup"><span data-stu-id="274d6-149">This occurs for Legacy policies created in Silverlight and can be resolved by deleting and recreating the policy in the Azure Portal.</span></span> <span data-ttu-id="274d6-150">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="274d6-150">This property is read-only.</span></span> <span data-ttu-id="274d6-151">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="274d6-151">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="274d6-152">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="274d6-152">createdDateTime</span></span>|<span data-ttu-id="274d6-153">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="274d6-153">DateTimeOffset</span></span>|<span data-ttu-id="274d6-154">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="274d6-154">DateTime the object was created.</span></span> <span data-ttu-id="274d6-155">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="274d6-155">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="274d6-156">descripción</span><span class="sxs-lookup"><span data-stu-id="274d6-156">description</span></span>|<span data-ttu-id="274d6-157">String</span><span class="sxs-lookup"><span data-stu-id="274d6-157">String</span></span>|<span data-ttu-id="274d6-158">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="274d6-158">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="274d6-159">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="274d6-159">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="274d6-160">displayName</span><span class="sxs-lookup"><span data-stu-id="274d6-160">displayName</span></span>|<span data-ttu-id="274d6-161">String</span><span class="sxs-lookup"><span data-stu-id="274d6-161">String</span></span>|<span data-ttu-id="274d6-162">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="274d6-162">Admin provided name of the device configuration.</span></span> <span data-ttu-id="274d6-163">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="274d6-163">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="274d6-164">version</span><span class="sxs-lookup"><span data-stu-id="274d6-164">version</span></span>|<span data-ttu-id="274d6-165">Int32</span><span class="sxs-lookup"><span data-stu-id="274d6-165">Int32</span></span>|<span data-ttu-id="274d6-166">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="274d6-166">Version of the device configuration.</span></span> <span data-ttu-id="274d6-167">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="274d6-167">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="274d6-168">renewalThresholdPercentage</span><span class="sxs-lookup"><span data-stu-id="274d6-168">renewalThresholdPercentage</span></span>|<span data-ttu-id="274d6-169">Int32</span><span class="sxs-lookup"><span data-stu-id="274d6-169">Int32</span></span>|<span data-ttu-id="274d6-170">Porcentaje de umbral de renovación de certificado.</span><span class="sxs-lookup"><span data-stu-id="274d6-170">Certificate renewal threshold percentage.</span></span> <span data-ttu-id="274d6-171">Válido valores heredada de 1 a 99 de [windowsCertificateProfileBase](../resources/intune-deviceconfig-windowscertificateprofilebase.md)</span><span class="sxs-lookup"><span data-stu-id="274d6-171">Valid values 1 to 99 Inherited from [windowsCertificateProfileBase](../resources/intune-deviceconfig-windowscertificateprofilebase.md)</span></span>|
|<span data-ttu-id="274d6-172">keyStorageProvider</span><span class="sxs-lookup"><span data-stu-id="274d6-172">keyStorageProvider</span></span>|[<span data-ttu-id="274d6-173">keyStorageProviderOption</span><span class="sxs-lookup"><span data-stu-id="274d6-173">keyStorageProviderOption</span></span>](../resources/intune-deviceconfig-keystorageprovideroption.md)|<span data-ttu-id="274d6-174">Proveedor de almacenamiento de claves (KSP) Inherited desde [windowsCertificateProfileBase](../resources/intune-deviceconfig-windowscertificateprofilebase.md).</span><span class="sxs-lookup"><span data-stu-id="274d6-174">Key Storage Provider (KSP) Inherited from [windowsCertificateProfileBase](../resources/intune-deviceconfig-windowscertificateprofilebase.md).</span></span> <span data-ttu-id="274d6-175">Los valores posibles son: `useTpmKspOtherwiseUseSoftwareKsp`, `useTpmKspOtherwiseFail`, `usePassportForWorkKspOtherwiseFail` y `useSoftwareKsp`.</span><span class="sxs-lookup"><span data-stu-id="274d6-175">Possible values are: `useTpmKspOtherwiseUseSoftwareKsp`, `useTpmKspOtherwiseFail`, `usePassportForWorkKspOtherwiseFail`, `useSoftwareKsp`.</span></span>|
|<span data-ttu-id="274d6-176">subjectNameFormat</span><span class="sxs-lookup"><span data-stu-id="274d6-176">subjectNameFormat</span></span>|[<span data-ttu-id="274d6-177">subjectNameFormat</span><span class="sxs-lookup"><span data-stu-id="274d6-177">subjectNameFormat</span></span>](../resources/intune-deviceconfig-subjectnameformat.md)|<span data-ttu-id="274d6-178">Certificado heredado de formato de nombre de sujeto de [windowsCertificateProfileBase](../resources/intune-deviceconfig-windowscertificateprofilebase.md).</span><span class="sxs-lookup"><span data-stu-id="274d6-178">Certificate Subject Name Format Inherited from [windowsCertificateProfileBase](../resources/intune-deviceconfig-windowscertificateprofilebase.md).</span></span> <span data-ttu-id="274d6-179">Los valores posibles son: `commonName`, `commonNameIncludingEmail`, `commonNameAsEmail`, `custom`, `commonNameAsIMEI`, `commonNameAsSerialNumber`, `commonNameAsAadDeviceId`, `commonNameAsIntuneDeviceId` y `commonNameAsDurableDeviceId`.</span><span class="sxs-lookup"><span data-stu-id="274d6-179">Possible values are: `commonName`, `commonNameIncludingEmail`, `commonNameAsEmail`, `custom`, `commonNameAsIMEI`, `commonNameAsSerialNumber`, `commonNameAsAadDeviceId`, `commonNameAsIntuneDeviceId`, `commonNameAsDurableDeviceId`.</span></span>|
|<span data-ttu-id="274d6-180">subjectAlternativeNameType</span><span class="sxs-lookup"><span data-stu-id="274d6-180">subjectAlternativeNameType</span></span>|[<span data-ttu-id="274d6-181">subjectAlternativeNameType</span><span class="sxs-lookup"><span data-stu-id="274d6-181">subjectAlternativeNameType</span></span>](../resources/intune-deviceconfig-subjectalternativenametype.md)|<span data-ttu-id="274d6-182">Certificado asunto alternativa nombre tipo hereda de [windowsCertificateProfileBase](../resources/intune-deviceconfig-windowscertificateprofilebase.md).</span><span class="sxs-lookup"><span data-stu-id="274d6-182">Certificate Subject Alternative Name Type Inherited from [windowsCertificateProfileBase](../resources/intune-deviceconfig-windowscertificateprofilebase.md).</span></span> <span data-ttu-id="274d6-183">Los valores posibles son: `none`, `emailAddress`, `userPrincipalName`, `customAzureADAttribute` y `domainNameService`.</span><span class="sxs-lookup"><span data-stu-id="274d6-183">Possible values are: `none`, `emailAddress`, `userPrincipalName`, `customAzureADAttribute`, `domainNameService`.</span></span>|
|<span data-ttu-id="274d6-184">certificateValidityPeriodValue</span><span class="sxs-lookup"><span data-stu-id="274d6-184">certificateValidityPeriodValue</span></span>|<span data-ttu-id="274d6-185">Int32</span><span class="sxs-lookup"><span data-stu-id="274d6-185">Int32</span></span>|<span data-ttu-id="274d6-186">Valor para el heredado de período de validez de certificado de [windowsCertificateProfileBase](../resources/intune-deviceconfig-windowscertificateprofilebase.md)</span><span class="sxs-lookup"><span data-stu-id="274d6-186">Value for the Certificate Validity Period Inherited from [windowsCertificateProfileBase](../resources/intune-deviceconfig-windowscertificateprofilebase.md)</span></span>|
|<span data-ttu-id="274d6-187">certificateValidityPeriodScale</span><span class="sxs-lookup"><span data-stu-id="274d6-187">certificateValidityPeriodScale</span></span>|[<span data-ttu-id="274d6-188">certificateValidityPeriodScale</span><span class="sxs-lookup"><span data-stu-id="274d6-188">certificateValidityPeriodScale</span></span>](../resources/intune-deviceconfig-certificatevalidityperiodscale.md)|<span data-ttu-id="274d6-189">Escala para la heredada de período de validez de certificado de [windowsCertificateProfileBase](../resources/intune-deviceconfig-windowscertificateprofilebase.md).</span><span class="sxs-lookup"><span data-stu-id="274d6-189">Scale for the Certificate Validity Period Inherited from [windowsCertificateProfileBase](../resources/intune-deviceconfig-windowscertificateprofilebase.md).</span></span> <span data-ttu-id="274d6-190">Los valores posibles son: `days`, `months` y `years`.</span><span class="sxs-lookup"><span data-stu-id="274d6-190">Possible values are: `days`, `months`, `years`.</span></span>|
|<span data-ttu-id="274d6-191">certificationAuthority</span><span class="sxs-lookup"><span data-stu-id="274d6-191">certificationAuthority</span></span>|<span data-ttu-id="274d6-192">String</span><span class="sxs-lookup"><span data-stu-id="274d6-192">String</span></span>|<span data-ttu-id="274d6-193">Entidad de certificación PKCS</span><span class="sxs-lookup"><span data-stu-id="274d6-193">PKCS Certification Authority</span></span>|
|<span data-ttu-id="274d6-194">certificationAuthorityName</span><span class="sxs-lookup"><span data-stu-id="274d6-194">certificationAuthorityName</span></span>|<span data-ttu-id="274d6-195">String</span><span class="sxs-lookup"><span data-stu-id="274d6-195">String</span></span>|<span data-ttu-id="274d6-196">Nombre de entidad de certificación PKCS</span><span class="sxs-lookup"><span data-stu-id="274d6-196">PKCS Certification Authority Name</span></span>|
|<span data-ttu-id="274d6-197">certificateTemplateName</span><span class="sxs-lookup"><span data-stu-id="274d6-197">certificateTemplateName</span></span>|<span data-ttu-id="274d6-198">String</span><span class="sxs-lookup"><span data-stu-id="274d6-198">String</span></span>|<span data-ttu-id="274d6-199">Nombre de plantilla de certificado PKCS</span><span class="sxs-lookup"><span data-stu-id="274d6-199">PKCS Certificate Template Name</span></span>|
|<span data-ttu-id="274d6-200">subjectAlternativeNameFormatString</span><span class="sxs-lookup"><span data-stu-id="274d6-200">subjectAlternativeNameFormatString</span></span>|<span data-ttu-id="274d6-201">String</span><span class="sxs-lookup"><span data-stu-id="274d6-201">String</span></span>|<span data-ttu-id="274d6-202">Cadena personalizada que define el atributo AAD.</span><span class="sxs-lookup"><span data-stu-id="274d6-202">Custom String that defines the AAD Attribute.</span></span>|
|<span data-ttu-id="274d6-203">extendedKeyUsages</span><span class="sxs-lookup"><span data-stu-id="274d6-203">extendedKeyUsages</span></span>|<span data-ttu-id="274d6-204">colección de [ExtendeKeyUsage](../resources/intune-deviceconfig-extendedkeyusage.md)</span><span class="sxs-lookup"><span data-stu-id="274d6-204">[extendedKeyUsage](../resources/intune-deviceconfig-extendedkeyusage.md) collection</span></span>|<span data-ttu-id="274d6-205">Configuración de clave (EKU) extendida.</span><span class="sxs-lookup"><span data-stu-id="274d6-205">Extended Key Usage (EKU) settings.</span></span> <span data-ttu-id="274d6-206">Esta colección puede contener un máximo de 500 elementos.</span><span class="sxs-lookup"><span data-stu-id="274d6-206">This collection can contain a maximum of 500 elements.</span></span>|



## <a name="response"></a><span data-ttu-id="274d6-207">Respuesta</span><span class="sxs-lookup"><span data-stu-id="274d6-207">Response</span></span>
<span data-ttu-id="274d6-208">Si tiene éxito, este método devuelve una `201 Created` código de respuesta y un objeto [windows10PkcsCertificateProfile](../resources/intune-deviceconfig-windows10pkcscertificateprofile.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="274d6-208">If successful, this method returns a `201 Created` response code and a [windows10PkcsCertificateProfile](../resources/intune-deviceconfig-windows10pkcscertificateprofile.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="274d6-209">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="274d6-209">Example</span></span>
### <a name="request"></a><span data-ttu-id="274d6-210">Solicitud</span><span class="sxs-lookup"><span data-stu-id="274d6-210">Request</span></span>
<span data-ttu-id="274d6-211">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="274d6-211">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations
Content-type: application/json
Content-length: 1075

{
  "@odata.type": "#microsoft.graph.windows10PkcsCertificateProfile",
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
  "certificationAuthority": "Certification Authority value",
  "certificationAuthorityName": "Certification Authority Name value",
  "certificateTemplateName": "Certificate Template Name value",
  "subjectAlternativeNameFormatString": "Subject Alternative Name Format String value",
  "extendedKeyUsages": [
    {
      "@odata.type": "microsoft.graph.extendedKeyUsage",
      "name": "Name value",
      "objectIdentifier": "Object Identifier value"
    }
  ]
}
```

### <a name="response"></a><span data-ttu-id="274d6-212">Respuesta</span><span class="sxs-lookup"><span data-stu-id="274d6-212">Response</span></span>
<span data-ttu-id="274d6-p117">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="274d6-p117">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 1183

{
  "@odata.type": "#microsoft.graph.windows10PkcsCertificateProfile",
  "id": "414c69c0-69c0-414c-c069-4c41c0694c41",
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
  "certificationAuthority": "Certification Authority value",
  "certificationAuthorityName": "Certification Authority Name value",
  "certificateTemplateName": "Certificate Template Name value",
  "subjectAlternativeNameFormatString": "Subject Alternative Name Format String value",
  "extendedKeyUsages": [
    {
      "@odata.type": "microsoft.graph.extendedKeyUsage",
      "name": "Name value",
      "objectIdentifier": "Object Identifier value"
    }
  ]
}
```





