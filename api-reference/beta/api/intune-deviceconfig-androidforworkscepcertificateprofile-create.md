---
title: Crear androidForWorkScepCertificateProfile
description: Crear un nuevo objeto androidForWorkScepCertificateProfile.
ms.openlocfilehash: 8d780cb50ef7fc272bb34f4112f8adfe9b596ad0
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084565"
---
# <a name="create-androidforworkscepcertificateprofile"></a><span data-ttu-id="d226f-103">Crear androidForWorkScepCertificateProfile</span><span class="sxs-lookup"><span data-stu-id="d226f-103">Create androidForWorkScepCertificateProfile</span></span>

> <span data-ttu-id="d226f-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="d226f-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="d226f-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="d226f-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="d226f-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="d226f-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="d226f-107">Crear un nuevo objeto [androidForWorkScepCertificateProfile](../resources/intune-deviceconfig-androidforworkscepcertificateprofile.md) .</span><span class="sxs-lookup"><span data-stu-id="d226f-107">Create a new [androidForWorkScepCertificateProfile](../resources/intune-deviceconfig-androidforworkscepcertificateprofile.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="d226f-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="d226f-108">Prerequisites</span></span>
<span data-ttu-id="d226f-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="d226f-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="d226f-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="d226f-111">Permission type</span></span>|<span data-ttu-id="d226f-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="d226f-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="d226f-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d226f-113">Delegated (work or school account)</span></span>|<span data-ttu-id="d226f-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d226f-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="d226f-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="d226f-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="d226f-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d226f-116">Not supported.</span></span>|
|<span data-ttu-id="d226f-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d226f-117">Application</span></span>|<span data-ttu-id="d226f-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d226f-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="d226f-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d226f-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceConfigurations
POST /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsDomainJoinConfiguration/networkAccessConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="d226f-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d226f-120">Request headers</span></span>
|<span data-ttu-id="d226f-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d226f-121">Header</span></span>|<span data-ttu-id="d226f-122">Valor</span><span class="sxs-lookup"><span data-stu-id="d226f-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="d226f-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="d226f-123">Authorization</span></span>|<span data-ttu-id="d226f-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="d226f-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="d226f-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="d226f-125">Accept</span></span>|<span data-ttu-id="d226f-126">application/json</span><span class="sxs-lookup"><span data-stu-id="d226f-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="d226f-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="d226f-127">Request body</span></span>
<span data-ttu-id="d226f-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto androidForWorkScepCertificateProfile.</span><span class="sxs-lookup"><span data-stu-id="d226f-128">In the request body, supply a JSON representation for the androidForWorkScepCertificateProfile object.</span></span>

<span data-ttu-id="d226f-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el androidForWorkScepCertificateProfile.</span><span class="sxs-lookup"><span data-stu-id="d226f-129">The following table shows the properties that are required when you create the androidForWorkScepCertificateProfile.</span></span>

|<span data-ttu-id="d226f-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d226f-130">Property</span></span>|<span data-ttu-id="d226f-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="d226f-131">Type</span></span>|<span data-ttu-id="d226f-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="d226f-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="d226f-133">id</span><span class="sxs-lookup"><span data-stu-id="d226f-133">id</span></span>|<span data-ttu-id="d226f-134">String</span><span class="sxs-lookup"><span data-stu-id="d226f-134">String</span></span>|<span data-ttu-id="d226f-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="d226f-135">Key of the entity.</span></span> <span data-ttu-id="d226f-136">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="d226f-136">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="d226f-137">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="d226f-137">lastModifiedDateTime</span></span>|<span data-ttu-id="d226f-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="d226f-138">DateTimeOffset</span></span>|<span data-ttu-id="d226f-139">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="d226f-139">DateTime the object was last modified.</span></span> <span data-ttu-id="d226f-140">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="d226f-140">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="d226f-141">roleScopeTagIds</span><span class="sxs-lookup"><span data-stu-id="d226f-141">roleScopeTagIds</span></span>|<span data-ttu-id="d226f-142">Colección String</span><span class="sxs-lookup"><span data-stu-id="d226f-142">String collection</span></span>|<span data-ttu-id="d226f-143">Lista de etiquetas de ámbito para esta instancia de entidad.</span><span class="sxs-lookup"><span data-stu-id="d226f-143">List of Scope Tags for this Entity instance.</span></span> <span data-ttu-id="d226f-144">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="d226f-144">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="d226f-145">supportsScopeTags</span><span class="sxs-lookup"><span data-stu-id="d226f-145">supportsScopeTags</span></span>|<span data-ttu-id="d226f-146">Booleano</span><span class="sxs-lookup"><span data-stu-id="d226f-146">Boolean</span></span>|<span data-ttu-id="d226f-147">Indica si la configuración del dispositivo subyacente admite la asignación de etiquetas de ámbito.</span><span class="sxs-lookup"><span data-stu-id="d226f-147">Indicates whether or not the underlying Device Configuration supports the assignment of scope tags.</span></span> <span data-ttu-id="d226f-148">No se permite la asignación a la propiedad ScopeTags cuando este valor es false y entidades no estará visibles para los usuarios con ámbito.</span><span class="sxs-lookup"><span data-stu-id="d226f-148">Assigning to the ScopeTags property is not allowed when this value is false and entities will not be visible to scoped users.</span></span> <span data-ttu-id="d226f-149">Esto se produce para las directivas de heredado creadas en Silverlight y se puede resolver por eliminar y volver a crear la directiva en el Portal de Azure.</span><span class="sxs-lookup"><span data-stu-id="d226f-149">This occurs for Legacy policies created in Silverlight and can be resolved by deleting and recreating the policy in the Azure Portal.</span></span> <span data-ttu-id="d226f-150">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="d226f-150">This property is read-only.</span></span> <span data-ttu-id="d226f-151">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="d226f-151">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="d226f-152">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="d226f-152">createdDateTime</span></span>|<span data-ttu-id="d226f-153">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="d226f-153">DateTimeOffset</span></span>|<span data-ttu-id="d226f-154">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="d226f-154">DateTime the object was created.</span></span> <span data-ttu-id="d226f-155">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="d226f-155">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="d226f-156">descripción</span><span class="sxs-lookup"><span data-stu-id="d226f-156">description</span></span>|<span data-ttu-id="d226f-157">String</span><span class="sxs-lookup"><span data-stu-id="d226f-157">String</span></span>|<span data-ttu-id="d226f-158">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d226f-158">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="d226f-159">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="d226f-159">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="d226f-160">displayName</span><span class="sxs-lookup"><span data-stu-id="d226f-160">displayName</span></span>|<span data-ttu-id="d226f-161">String</span><span class="sxs-lookup"><span data-stu-id="d226f-161">String</span></span>|<span data-ttu-id="d226f-162">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d226f-162">Admin provided name of the device configuration.</span></span> <span data-ttu-id="d226f-163">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="d226f-163">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="d226f-164">version</span><span class="sxs-lookup"><span data-stu-id="d226f-164">version</span></span>|<span data-ttu-id="d226f-165">Int32</span><span class="sxs-lookup"><span data-stu-id="d226f-165">Int32</span></span>|<span data-ttu-id="d226f-166">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d226f-166">Version of the device configuration.</span></span> <span data-ttu-id="d226f-167">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="d226f-167">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="d226f-168">renewalThresholdPercentage</span><span class="sxs-lookup"><span data-stu-id="d226f-168">renewalThresholdPercentage</span></span>|<span data-ttu-id="d226f-169">Int32</span><span class="sxs-lookup"><span data-stu-id="d226f-169">Int32</span></span>|<span data-ttu-id="d226f-170">Porcentaje de umbral de renovación de certificado.</span><span class="sxs-lookup"><span data-stu-id="d226f-170">Certificate renewal threshold percentage.</span></span> <span data-ttu-id="d226f-171">Válido valores heredada de 1 a 99 de [androidForWorkCertificateProfileBase](../resources/intune-deviceconfig-androidforworkcertificateprofilebase.md)</span><span class="sxs-lookup"><span data-stu-id="d226f-171">Valid values 1 to 99 Inherited from [androidForWorkCertificateProfileBase](../resources/intune-deviceconfig-androidforworkcertificateprofilebase.md)</span></span>|
|<span data-ttu-id="d226f-172">subjectNameFormat</span><span class="sxs-lookup"><span data-stu-id="d226f-172">subjectNameFormat</span></span>|[<span data-ttu-id="d226f-173">subjectNameFormat</span><span class="sxs-lookup"><span data-stu-id="d226f-173">subjectNameFormat</span></span>](../resources/intune-deviceconfig-subjectnameformat.md)|<span data-ttu-id="d226f-174">Formato de nombre de sujeto de certificado.</span><span class="sxs-lookup"><span data-stu-id="d226f-174">Certificate Subject Name Format.</span></span> <span data-ttu-id="d226f-175">Se hereda de [androidForWorkCertificateProfileBase](../resources/intune-deviceconfig-androidforworkcertificateprofilebase.md).</span><span class="sxs-lookup"><span data-stu-id="d226f-175">Inherited from [androidForWorkCertificateProfileBase](../resources/intune-deviceconfig-androidforworkcertificateprofilebase.md).</span></span> <span data-ttu-id="d226f-176">Los valores posibles son: `commonName`, `commonNameIncludingEmail`, `commonNameAsEmail`, `custom`, `commonNameAsIMEI`, `commonNameAsSerialNumber`, `commonNameAsAadDeviceId`, `commonNameAsIntuneDeviceId` y `commonNameAsDurableDeviceId`.</span><span class="sxs-lookup"><span data-stu-id="d226f-176">Possible values are: `commonName`, `commonNameIncludingEmail`, `commonNameAsEmail`, `custom`, `commonNameAsIMEI`, `commonNameAsSerialNumber`, `commonNameAsAadDeviceId`, `commonNameAsIntuneDeviceId`, `commonNameAsDurableDeviceId`.</span></span>|
|<span data-ttu-id="d226f-177">certificateValidityPeriodValue</span><span class="sxs-lookup"><span data-stu-id="d226f-177">certificateValidityPeriodValue</span></span>|<span data-ttu-id="d226f-178">Int32</span><span class="sxs-lookup"><span data-stu-id="d226f-178">Int32</span></span>|<span data-ttu-id="d226f-179">Valor para el período de validez del certificado.</span><span class="sxs-lookup"><span data-stu-id="d226f-179">Value for the Certificate Validity Period.</span></span> <span data-ttu-id="d226f-180">Se hereda de [androidForWorkCertificateProfileBase](../resources/intune-deviceconfig-androidforworkcertificateprofilebase.md)</span><span class="sxs-lookup"><span data-stu-id="d226f-180">Inherited from [androidForWorkCertificateProfileBase](../resources/intune-deviceconfig-androidforworkcertificateprofilebase.md)</span></span>|
|<span data-ttu-id="d226f-181">certificateValidityPeriodScale</span><span class="sxs-lookup"><span data-stu-id="d226f-181">certificateValidityPeriodScale</span></span>|[<span data-ttu-id="d226f-182">certificateValidityPeriodScale</span><span class="sxs-lookup"><span data-stu-id="d226f-182">certificateValidityPeriodScale</span></span>](../resources/intune-deviceconfig-certificatevalidityperiodscale.md)|<span data-ttu-id="d226f-183">Escala para el período de validez del certificado.</span><span class="sxs-lookup"><span data-stu-id="d226f-183">Scale for the Certificate Validity Period.</span></span> <span data-ttu-id="d226f-184">Se hereda de [androidForWorkCertificateProfileBase](../resources/intune-deviceconfig-androidforworkcertificateprofilebase.md).</span><span class="sxs-lookup"><span data-stu-id="d226f-184">Inherited from [androidForWorkCertificateProfileBase](../resources/intune-deviceconfig-androidforworkcertificateprofilebase.md).</span></span> <span data-ttu-id="d226f-185">Los valores posibles son: `days`, `months` y `years`.</span><span class="sxs-lookup"><span data-stu-id="d226f-185">Possible values are: `days`, `months`, `years`.</span></span>|
|<span data-ttu-id="d226f-186">extendedKeyUsages</span><span class="sxs-lookup"><span data-stu-id="d226f-186">extendedKeyUsages</span></span>|<span data-ttu-id="d226f-187">colección de [ExtendeKeyUsage](../resources/intune-deviceconfig-extendedkeyusage.md)</span><span class="sxs-lookup"><span data-stu-id="d226f-187">[extendedKeyUsage](../resources/intune-deviceconfig-extendedkeyusage.md) collection</span></span>|<span data-ttu-id="d226f-188">Configuración de clave (EKU) extendida.</span><span class="sxs-lookup"><span data-stu-id="d226f-188">Extended Key Usage (EKU) settings.</span></span> <span data-ttu-id="d226f-189">Esta colección puede contener un máximo de 500 elementos.</span><span class="sxs-lookup"><span data-stu-id="d226f-189">This collection can contain a maximum of 500 elements.</span></span> <span data-ttu-id="d226f-190">Se hereda de [androidForWorkCertificateProfileBase](../resources/intune-deviceconfig-androidforworkcertificateprofilebase.md)</span><span class="sxs-lookup"><span data-stu-id="d226f-190">Inherited from [androidForWorkCertificateProfileBase](../resources/intune-deviceconfig-androidforworkcertificateprofilebase.md)</span></span>|
|<span data-ttu-id="d226f-191">scepServerUrls</span><span class="sxs-lookup"><span data-stu-id="d226f-191">scepServerUrls</span></span>|<span data-ttu-id="d226f-192">Colección String</span><span class="sxs-lookup"><span data-stu-id="d226f-192">String collection</span></span>|<span data-ttu-id="d226f-193">Direcciones URL de servidor SCEP</span><span class="sxs-lookup"><span data-stu-id="d226f-193">SCEP Server Url(s)</span></span>|
|<span data-ttu-id="d226f-194">subjectNameFormatString</span><span class="sxs-lookup"><span data-stu-id="d226f-194">subjectNameFormatString</span></span>|<span data-ttu-id="d226f-195">String</span><span class="sxs-lookup"><span data-stu-id="d226f-195">String</span></span>|<span data-ttu-id="d226f-196">Formato personalizado para usar con SubjectNameFormat = personalizada.</span><span class="sxs-lookup"><span data-stu-id="d226f-196">Custom format to use with SubjectNameFormat = Custom.</span></span> <span data-ttu-id="d226f-197">Ejemplo: CN = {{EmailAddress}}, E = {{EmailAddress}}, OU = Users de la empresa, O = Contoso Corporation, L = Redmond, ST = WA, C = US</span><span class="sxs-lookup"><span data-stu-id="d226f-197">Example: CN={{EmailAddress}},E={{EmailAddress}},OU=Enterprise Users,O=Contoso Corporation,L=Redmond,ST=WA,C=US</span></span>|
|<span data-ttu-id="d226f-198">keyUsage</span><span class="sxs-lookup"><span data-stu-id="d226f-198">keyUsage</span></span>|[<span data-ttu-id="d226f-199">keyUsages</span><span class="sxs-lookup"><span data-stu-id="d226f-199">keyUsages</span></span>](../resources/intune-deviceconfig-keyusages.md)|<span data-ttu-id="d226f-200">Uso de la clave SCEP.</span><span class="sxs-lookup"><span data-stu-id="d226f-200">SCEP Key Usage.</span></span> <span data-ttu-id="d226f-201">Los valores posibles son: `keyEncipherment` y `digitalSignature`.</span><span class="sxs-lookup"><span data-stu-id="d226f-201">Possible values are: `keyEncipherment`, `digitalSignature`.</span></span>|
|<span data-ttu-id="d226f-202">keySize</span><span class="sxs-lookup"><span data-stu-id="d226f-202">keySize</span></span>|[<span data-ttu-id="d226f-203">keySize</span><span class="sxs-lookup"><span data-stu-id="d226f-203">keySize</span></span>](../resources/intune-deviceconfig-keysize.md)|<span data-ttu-id="d226f-204">Tamaño de la clave SCEP.</span><span class="sxs-lookup"><span data-stu-id="d226f-204">SCEP Key Size.</span></span> <span data-ttu-id="d226f-205">Los valores posibles son: `size1024` y `size2048`.</span><span class="sxs-lookup"><span data-stu-id="d226f-205">Possible values are: `size1024`, `size2048`.</span></span>|
|<span data-ttu-id="d226f-206">hashAlgorithm</span><span class="sxs-lookup"><span data-stu-id="d226f-206">hashAlgorithm</span></span>|[<span data-ttu-id="d226f-207">hashAlgorithms</span><span class="sxs-lookup"><span data-stu-id="d226f-207">hashAlgorithms</span></span>](../resources/intune-deviceconfig-hashalgorithms.md)|<span data-ttu-id="d226f-208">Algoritmo de Hash SCEP.</span><span class="sxs-lookup"><span data-stu-id="d226f-208">SCEP Hash Algorithm.</span></span> <span data-ttu-id="d226f-209">Los valores posibles son: `sha1` y `sha2`.</span><span class="sxs-lookup"><span data-stu-id="d226f-209">Possible values are: `sha1`, `sha2`.</span></span>|
|<span data-ttu-id="d226f-210">subjectAlternativeNameFormatString</span><span class="sxs-lookup"><span data-stu-id="d226f-210">subjectAlternativeNameFormatString</span></span>|<span data-ttu-id="d226f-211">String</span><span class="sxs-lookup"><span data-stu-id="d226f-211">String</span></span>|<span data-ttu-id="d226f-212">Cadena personalizada que define el atributo AAD.</span><span class="sxs-lookup"><span data-stu-id="d226f-212">Custom String that defines the AAD Attribute.</span></span>|
|<span data-ttu-id="d226f-213">certificateStore</span><span class="sxs-lookup"><span data-stu-id="d226f-213">certificateStore</span></span>|[<span data-ttu-id="d226f-214">certificateStore</span><span class="sxs-lookup"><span data-stu-id="d226f-214">certificateStore</span></span>](../resources/intune-deviceconfig-certificatestore.md)|<span data-ttu-id="d226f-215">Certificado del almacén de destino.</span><span class="sxs-lookup"><span data-stu-id="d226f-215">Target store certificate.</span></span> <span data-ttu-id="d226f-216">Los valores posibles son: `user` y `machine`.</span><span class="sxs-lookup"><span data-stu-id="d226f-216">Possible values are: `user`, `machine`.</span></span>|
|<span data-ttu-id="d226f-217">customSubjectAlternativeNames</span><span class="sxs-lookup"><span data-stu-id="d226f-217">customSubjectAlternativeNames</span></span>|<span data-ttu-id="d226f-218">colección de [customSubjectAlternativeName](../resources/intune-deviceconfig-customsubjectalternativename.md)</span><span class="sxs-lookup"><span data-stu-id="d226f-218">[customSubjectAlternativeName](../resources/intune-deviceconfig-customsubjectalternativename.md) collection</span></span>|<span data-ttu-id="d226f-219">Configuración de Alterantive nombre de sujeto personalizado.</span><span class="sxs-lookup"><span data-stu-id="d226f-219">Custom Subject Alterantive Name Settings.</span></span> <span data-ttu-id="d226f-220">Esta colección puede contener un máximo de 500 elementos.</span><span class="sxs-lookup"><span data-stu-id="d226f-220">This collection can contain a maximum of 500 elements.</span></span>|
|<span data-ttu-id="d226f-221">subjectAlternativeNameType</span><span class="sxs-lookup"><span data-stu-id="d226f-221">subjectAlternativeNameType</span></span>|[<span data-ttu-id="d226f-222">subjectAlternativeNameType</span><span class="sxs-lookup"><span data-stu-id="d226f-222">subjectAlternativeNameType</span></span>](../resources/intune-deviceconfig-subjectalternativenametype.md)|<span data-ttu-id="d226f-223">Tipo de nombre alternativo de sujeto de certificado.</span><span class="sxs-lookup"><span data-stu-id="d226f-223">Certificate Subject Alternative Name Type.</span></span> <span data-ttu-id="d226f-224">Los valores posibles son: `none`, `emailAddress`, `userPrincipalName`, `customAzureADAttribute` y `domainNameService`.</span><span class="sxs-lookup"><span data-stu-id="d226f-224">Possible values are: `none`, `emailAddress`, `userPrincipalName`, `customAzureADAttribute`, `domainNameService`.</span></span>|



## <a name="response"></a><span data-ttu-id="d226f-225">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d226f-225">Response</span></span>
<span data-ttu-id="d226f-226">Si tiene éxito, este método devuelve una `201 Created` código de respuesta y un objeto [androidForWorkScepCertificateProfile](../resources/intune-deviceconfig-androidforworkscepcertificateprofile.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d226f-226">If successful, this method returns a `201 Created` response code and a [androidForWorkScepCertificateProfile](../resources/intune-deviceconfig-androidforworkscepcertificateprofile.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="d226f-227">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d226f-227">Example</span></span>
### <a name="request"></a><span data-ttu-id="d226f-228">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d226f-228">Request</span></span>
<span data-ttu-id="d226f-229">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d226f-229">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations
Content-type: application/json
Content-length: 1269

{
  "@odata.type": "#microsoft.graph.androidForWorkScepCertificateProfile",
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
  "scepServerUrls": [
    "Scep Server Urls value"
  ],
  "subjectNameFormatString": "Subject Name Format String value",
  "keyUsage": "digitalSignature",
  "keySize": "size2048",
  "hashAlgorithm": "sha2",
  "subjectAlternativeNameFormatString": "Subject Alternative Name Format String value",
  "certificateStore": "machine",
  "customSubjectAlternativeNames": [
    {
      "@odata.type": "microsoft.graph.customSubjectAlternativeName",
      "sanType": "emailAddress",
      "name": "Name value"
    }
  ],
  "subjectAlternativeNameType": "emailAddress"
}
```

### <a name="response"></a><span data-ttu-id="d226f-230">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d226f-230">Response</span></span>
<span data-ttu-id="d226f-p123">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="d226f-p123">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 1377

{
  "@odata.type": "#microsoft.graph.androidForWorkScepCertificateProfile",
  "id": "09e532af-32af-09e5-af32-e509af32e509",
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
  "scepServerUrls": [
    "Scep Server Urls value"
  ],
  "subjectNameFormatString": "Subject Name Format String value",
  "keyUsage": "digitalSignature",
  "keySize": "size2048",
  "hashAlgorithm": "sha2",
  "subjectAlternativeNameFormatString": "Subject Alternative Name Format String value",
  "certificateStore": "machine",
  "customSubjectAlternativeNames": [
    {
      "@odata.type": "microsoft.graph.customSubjectAlternativeName",
      "sanType": "emailAddress",
      "name": "Name value"
    }
  ],
  "subjectAlternativeNameType": "emailAddress"
}
```




