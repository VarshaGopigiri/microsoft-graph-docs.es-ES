---
title: Actualizar macOSScepCertificateProfile
description: Actualizar las propiedades de un objeto macOSScepCertificateProfile.
author: tfitzmac
ms.openlocfilehash: 1ab735b6c9d2703512a97080bc5500111c455764
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27352447"
---
# <a name="update-macosscepcertificateprofile"></a><span data-ttu-id="8ad8c-103">Actualizar macOSScepCertificateProfile</span><span class="sxs-lookup"><span data-stu-id="8ad8c-103">Update macOSScepCertificateProfile</span></span>

> <span data-ttu-id="8ad8c-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="8ad8c-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="8ad8c-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="8ad8c-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="8ad8c-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="8ad8c-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="8ad8c-107">Actualizar las propiedades de un objeto [macOSScepCertificateProfile](../resources/intune-deviceconfig-macosscepcertificateprofile.md) .</span><span class="sxs-lookup"><span data-stu-id="8ad8c-107">Update the properties of a [macOSScepCertificateProfile](../resources/intune-deviceconfig-macosscepcertificateprofile.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="8ad8c-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="8ad8c-108">Prerequisites</span></span>
<span data-ttu-id="8ad8c-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="8ad8c-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="8ad8c-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="8ad8c-111">Permission type</span></span>|<span data-ttu-id="8ad8c-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="8ad8c-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="8ad8c-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="8ad8c-113">Delegated (work or school account)</span></span>|<span data-ttu-id="8ad8c-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="8ad8c-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="8ad8c-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="8ad8c-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="8ad8c-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8ad8c-116">Not supported.</span></span>|
|<span data-ttu-id="8ad8c-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="8ad8c-117">Application</span></span>|<span data-ttu-id="8ad8c-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8ad8c-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="8ad8c-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="8ad8c-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/groupAssignments/{deviceConfigurationGroupAssignmentId}/deviceConfiguration
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsDomainJoinConfiguration/networkAccessConfigurations/{deviceConfigurationId}
```

## <a name="request-headers"></a><span data-ttu-id="8ad8c-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="8ad8c-120">Request headers</span></span>
|<span data-ttu-id="8ad8c-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8ad8c-121">Header</span></span>|<span data-ttu-id="8ad8c-122">Valor</span><span class="sxs-lookup"><span data-stu-id="8ad8c-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="8ad8c-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="8ad8c-123">Authorization</span></span>|<span data-ttu-id="8ad8c-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="8ad8c-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="8ad8c-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="8ad8c-125">Accept</span></span>|<span data-ttu-id="8ad8c-126">application/json</span><span class="sxs-lookup"><span data-stu-id="8ad8c-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="8ad8c-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="8ad8c-127">Request body</span></span>
<span data-ttu-id="8ad8c-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto [macOSScepCertificateProfile](../resources/intune-deviceconfig-macosscepcertificateprofile.md) .</span><span class="sxs-lookup"><span data-stu-id="8ad8c-128">In the request body, supply a JSON representation for the [macOSScepCertificateProfile](../resources/intune-deviceconfig-macosscepcertificateprofile.md) object.</span></span>

<span data-ttu-id="8ad8c-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el [macOSScepCertificateProfile](../resources/intune-deviceconfig-macosscepcertificateprofile.md).</span><span class="sxs-lookup"><span data-stu-id="8ad8c-129">The following table shows the properties that are required when you create the [macOSScepCertificateProfile](../resources/intune-deviceconfig-macosscepcertificateprofile.md).</span></span>

|<span data-ttu-id="8ad8c-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="8ad8c-130">Property</span></span>|<span data-ttu-id="8ad8c-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="8ad8c-131">Type</span></span>|<span data-ttu-id="8ad8c-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="8ad8c-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="8ad8c-133">id</span><span class="sxs-lookup"><span data-stu-id="8ad8c-133">id</span></span>|<span data-ttu-id="8ad8c-134">String</span><span class="sxs-lookup"><span data-stu-id="8ad8c-134">String</span></span>|<span data-ttu-id="8ad8c-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="8ad8c-135">Key of the entity.</span></span> <span data-ttu-id="8ad8c-136">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="8ad8c-136">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="8ad8c-137">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="8ad8c-137">lastModifiedDateTime</span></span>|<span data-ttu-id="8ad8c-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="8ad8c-138">DateTimeOffset</span></span>|<span data-ttu-id="8ad8c-139">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="8ad8c-139">DateTime the object was last modified.</span></span> <span data-ttu-id="8ad8c-140">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="8ad8c-140">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="8ad8c-141">roleScopeTagIds</span><span class="sxs-lookup"><span data-stu-id="8ad8c-141">roleScopeTagIds</span></span>|<span data-ttu-id="8ad8c-142">Colección String</span><span class="sxs-lookup"><span data-stu-id="8ad8c-142">String collection</span></span>|<span data-ttu-id="8ad8c-143">Lista de etiquetas de ámbito para esta instancia de entidad.</span><span class="sxs-lookup"><span data-stu-id="8ad8c-143">List of Scope Tags for this Entity instance.</span></span> <span data-ttu-id="8ad8c-144">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="8ad8c-144">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="8ad8c-145">supportsScopeTags</span><span class="sxs-lookup"><span data-stu-id="8ad8c-145">supportsScopeTags</span></span>|<span data-ttu-id="8ad8c-146">Boolean</span><span class="sxs-lookup"><span data-stu-id="8ad8c-146">Boolean</span></span>|<span data-ttu-id="8ad8c-147">Indica si la configuración del dispositivo subyacente admite la asignación de etiquetas de ámbito.</span><span class="sxs-lookup"><span data-stu-id="8ad8c-147">Indicates whether or not the underlying Device Configuration supports the assignment of scope tags.</span></span> <span data-ttu-id="8ad8c-148">No se permite la asignación a la propiedad ScopeTags cuando este valor es false y entidades no estará visibles para los usuarios con ámbito.</span><span class="sxs-lookup"><span data-stu-id="8ad8c-148">Assigning to the ScopeTags property is not allowed when this value is false and entities will not be visible to scoped users.</span></span> <span data-ttu-id="8ad8c-149">Esto se produce para las directivas de heredado creadas en Silverlight y se puede resolver por eliminar y volver a crear la directiva en el Portal de Azure.</span><span class="sxs-lookup"><span data-stu-id="8ad8c-149">This occurs for Legacy policies created in Silverlight and can be resolved by deleting and recreating the policy in the Azure Portal.</span></span> <span data-ttu-id="8ad8c-150">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="8ad8c-150">This property is read-only.</span></span> <span data-ttu-id="8ad8c-151">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="8ad8c-151">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="8ad8c-152">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="8ad8c-152">createdDateTime</span></span>|<span data-ttu-id="8ad8c-153">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="8ad8c-153">DateTimeOffset</span></span>|<span data-ttu-id="8ad8c-154">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="8ad8c-154">DateTime the object was created.</span></span> <span data-ttu-id="8ad8c-155">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="8ad8c-155">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="8ad8c-156">descripción</span><span class="sxs-lookup"><span data-stu-id="8ad8c-156">description</span></span>|<span data-ttu-id="8ad8c-157">String</span><span class="sxs-lookup"><span data-stu-id="8ad8c-157">String</span></span>|<span data-ttu-id="8ad8c-158">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8ad8c-158">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="8ad8c-159">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="8ad8c-159">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="8ad8c-160">displayName</span><span class="sxs-lookup"><span data-stu-id="8ad8c-160">displayName</span></span>|<span data-ttu-id="8ad8c-161">String</span><span class="sxs-lookup"><span data-stu-id="8ad8c-161">String</span></span>|<span data-ttu-id="8ad8c-162">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8ad8c-162">Admin provided name of the device configuration.</span></span> <span data-ttu-id="8ad8c-163">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="8ad8c-163">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="8ad8c-164">version</span><span class="sxs-lookup"><span data-stu-id="8ad8c-164">version</span></span>|<span data-ttu-id="8ad8c-165">Int32</span><span class="sxs-lookup"><span data-stu-id="8ad8c-165">Int32</span></span>|<span data-ttu-id="8ad8c-166">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8ad8c-166">Version of the device configuration.</span></span> <span data-ttu-id="8ad8c-167">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="8ad8c-167">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="8ad8c-168">renewalThresholdPercentage</span><span class="sxs-lookup"><span data-stu-id="8ad8c-168">renewalThresholdPercentage</span></span>|<span data-ttu-id="8ad8c-169">Int32</span><span class="sxs-lookup"><span data-stu-id="8ad8c-169">Int32</span></span>|<span data-ttu-id="8ad8c-170">Porcentaje de umbral de renovación de certificado.</span><span class="sxs-lookup"><span data-stu-id="8ad8c-170">Certificate renewal threshold percentage.</span></span> <span data-ttu-id="8ad8c-171">Se hereda de [macOSCertificateProfileBase](../resources/intune-deviceconfig-macoscertificateprofilebase.md)</span><span class="sxs-lookup"><span data-stu-id="8ad8c-171">Inherited from [macOSCertificateProfileBase](../resources/intune-deviceconfig-macoscertificateprofilebase.md)</span></span>|
|<span data-ttu-id="8ad8c-172">subjectNameFormat</span><span class="sxs-lookup"><span data-stu-id="8ad8c-172">subjectNameFormat</span></span>|[<span data-ttu-id="8ad8c-173">appleSubjectNameFormat</span><span class="sxs-lookup"><span data-stu-id="8ad8c-173">appleSubjectNameFormat</span></span>](../resources/intune-deviceconfig-applesubjectnameformat.md)|<span data-ttu-id="8ad8c-174">Formato de nombre de sujeto de certificado.</span><span class="sxs-lookup"><span data-stu-id="8ad8c-174">Certificate Subject Name Format.</span></span> <span data-ttu-id="8ad8c-175">Se hereda de [macOSCertificateProfileBase](../resources/intune-deviceconfig-macoscertificateprofilebase.md).</span><span class="sxs-lookup"><span data-stu-id="8ad8c-175">Inherited from [macOSCertificateProfileBase](../resources/intune-deviceconfig-macoscertificateprofilebase.md).</span></span> <span data-ttu-id="8ad8c-176">Los valores posibles son: `commonName`, `commonNameAsEmail`, `custom`, `commonNameIncludingEmail`, `commonNameAsIMEI`, `commonNameAsSerialNumber`.</span><span class="sxs-lookup"><span data-stu-id="8ad8c-176">Possible values are: `commonName`, `commonNameAsEmail`, `custom`, `commonNameIncludingEmail`, `commonNameAsIMEI`, `commonNameAsSerialNumber`.</span></span>|
|<span data-ttu-id="8ad8c-177">subjectAlternativeNameType</span><span class="sxs-lookup"><span data-stu-id="8ad8c-177">subjectAlternativeNameType</span></span>|[<span data-ttu-id="8ad8c-178">subjectAlternativeNameType</span><span class="sxs-lookup"><span data-stu-id="8ad8c-178">subjectAlternativeNameType</span></span>](../resources/intune-deviceconfig-subjectalternativenametype.md)|<span data-ttu-id="8ad8c-179">Tipo de nombre alternativo de sujeto de certificado.</span><span class="sxs-lookup"><span data-stu-id="8ad8c-179">Certificate Subject Alternative Name Type.</span></span> <span data-ttu-id="8ad8c-180">Se hereda de [macOSCertificateProfileBase](../resources/intune-deviceconfig-macoscertificateprofilebase.md).</span><span class="sxs-lookup"><span data-stu-id="8ad8c-180">Inherited from [macOSCertificateProfileBase](../resources/intune-deviceconfig-macoscertificateprofilebase.md).</span></span> <span data-ttu-id="8ad8c-181">Los valores posibles son: `none`, `emailAddress`, `userPrincipalName`, `customAzureADAttribute` y `domainNameService`.</span><span class="sxs-lookup"><span data-stu-id="8ad8c-181">Possible values are: `none`, `emailAddress`, `userPrincipalName`, `customAzureADAttribute`, `domainNameService`.</span></span>|
|<span data-ttu-id="8ad8c-182">certificateValidityPeriodValue</span><span class="sxs-lookup"><span data-stu-id="8ad8c-182">certificateValidityPeriodValue</span></span>|<span data-ttu-id="8ad8c-183">Int32</span><span class="sxs-lookup"><span data-stu-id="8ad8c-183">Int32</span></span>|<span data-ttu-id="8ad8c-184">Valor para el período de validez del certificado.</span><span class="sxs-lookup"><span data-stu-id="8ad8c-184">Value for the Certificate Validity Period.</span></span> <span data-ttu-id="8ad8c-185">Se hereda de [macOSCertificateProfileBase](../resources/intune-deviceconfig-macoscertificateprofilebase.md)</span><span class="sxs-lookup"><span data-stu-id="8ad8c-185">Inherited from [macOSCertificateProfileBase](../resources/intune-deviceconfig-macoscertificateprofilebase.md)</span></span>|
|<span data-ttu-id="8ad8c-186">certificateValidityPeriodScale</span><span class="sxs-lookup"><span data-stu-id="8ad8c-186">certificateValidityPeriodScale</span></span>|[<span data-ttu-id="8ad8c-187">certificateValidityPeriodScale</span><span class="sxs-lookup"><span data-stu-id="8ad8c-187">certificateValidityPeriodScale</span></span>](../resources/intune-deviceconfig-certificatevalidityperiodscale.md)|<span data-ttu-id="8ad8c-188">Escala para el período de validez del certificado.</span><span class="sxs-lookup"><span data-stu-id="8ad8c-188">Scale for the Certificate Validity Period.</span></span> <span data-ttu-id="8ad8c-189">Se hereda de [macOSCertificateProfileBase](../resources/intune-deviceconfig-macoscertificateprofilebase.md).</span><span class="sxs-lookup"><span data-stu-id="8ad8c-189">Inherited from [macOSCertificateProfileBase](../resources/intune-deviceconfig-macoscertificateprofilebase.md).</span></span> <span data-ttu-id="8ad8c-190">Los valores posibles son: `days`, `months` y `years`.</span><span class="sxs-lookup"><span data-stu-id="8ad8c-190">Possible values are: `days`, `months`, `years`.</span></span>|
|<span data-ttu-id="8ad8c-191">scepServerUrls</span><span class="sxs-lookup"><span data-stu-id="8ad8c-191">scepServerUrls</span></span>|<span data-ttu-id="8ad8c-192">Colección String</span><span class="sxs-lookup"><span data-stu-id="8ad8c-192">String collection</span></span>|<span data-ttu-id="8ad8c-193">Direcciones URL del servidor SCEP.</span><span class="sxs-lookup"><span data-stu-id="8ad8c-193">SCEP Server Url(s).</span></span>|
|<span data-ttu-id="8ad8c-194">subjectNameFormatString</span><span class="sxs-lookup"><span data-stu-id="8ad8c-194">subjectNameFormatString</span></span>|<span data-ttu-id="8ad8c-195">String</span><span class="sxs-lookup"><span data-stu-id="8ad8c-195">String</span></span>|<span data-ttu-id="8ad8c-196">Formato personalizado para usar con SubjectNameFormat = personalizada.</span><span class="sxs-lookup"><span data-stu-id="8ad8c-196">Custom format to use with SubjectNameFormat = Custom.</span></span> <span data-ttu-id="8ad8c-197">Ejemplo: CN = {{EmailAddress}}, E = {{EmailAddress}}, OU = Users de la empresa, O = Contoso Corporation, L = Redmond, ST = WA, C = US</span><span class="sxs-lookup"><span data-stu-id="8ad8c-197">Example: CN={{EmailAddress}},E={{EmailAddress}},OU=Enterprise Users,O=Contoso Corporation,L=Redmond,ST=WA,C=US</span></span>|
|<span data-ttu-id="8ad8c-198">keyUsage</span><span class="sxs-lookup"><span data-stu-id="8ad8c-198">keyUsage</span></span>|[<span data-ttu-id="8ad8c-199">keyUsages</span><span class="sxs-lookup"><span data-stu-id="8ad8c-199">keyUsages</span></span>](../resources/intune-deviceconfig-keyusages.md)|<span data-ttu-id="8ad8c-200">Uso de la clave SCEP.</span><span class="sxs-lookup"><span data-stu-id="8ad8c-200">SCEP Key Usage.</span></span> <span data-ttu-id="8ad8c-201">Los valores posibles son: `keyEncipherment` y `digitalSignature`.</span><span class="sxs-lookup"><span data-stu-id="8ad8c-201">Possible values are: `keyEncipherment`, `digitalSignature`.</span></span>|
|<span data-ttu-id="8ad8c-202">keySize</span><span class="sxs-lookup"><span data-stu-id="8ad8c-202">keySize</span></span>|[<span data-ttu-id="8ad8c-203">keySize</span><span class="sxs-lookup"><span data-stu-id="8ad8c-203">keySize</span></span>](../resources/intune-deviceconfig-keysize.md)|<span data-ttu-id="8ad8c-204">Tamaño de la clave SCEP.</span><span class="sxs-lookup"><span data-stu-id="8ad8c-204">SCEP Key Size.</span></span> <span data-ttu-id="8ad8c-205">Los valores posibles son: `size1024` y `size2048`.</span><span class="sxs-lookup"><span data-stu-id="8ad8c-205">Possible values are: `size1024`, `size2048`.</span></span>|
|<span data-ttu-id="8ad8c-206">hashAlgorithm</span><span class="sxs-lookup"><span data-stu-id="8ad8c-206">hashAlgorithm</span></span>|[<span data-ttu-id="8ad8c-207">hashAlgorithms</span><span class="sxs-lookup"><span data-stu-id="8ad8c-207">hashAlgorithms</span></span>](../resources/intune-deviceconfig-hashalgorithms.md)|<span data-ttu-id="8ad8c-208">Algoritmo de Hash SCEP.</span><span class="sxs-lookup"><span data-stu-id="8ad8c-208">SCEP Hash Algorithm.</span></span> <span data-ttu-id="8ad8c-209">Los valores posibles son: `sha1` y `sha2`.</span><span class="sxs-lookup"><span data-stu-id="8ad8c-209">Possible values are: `sha1`, `sha2`.</span></span>|
|<span data-ttu-id="8ad8c-210">extendedKeyUsages</span><span class="sxs-lookup"><span data-stu-id="8ad8c-210">extendedKeyUsages</span></span>|<span data-ttu-id="8ad8c-211">colección de [ExtendeKeyUsage](../resources/intune-deviceconfig-extendedkeyusage.md)</span><span class="sxs-lookup"><span data-stu-id="8ad8c-211">[extendedKeyUsage](../resources/intune-deviceconfig-extendedkeyusage.md) collection</span></span>|<span data-ttu-id="8ad8c-212">Configuración de clave (EKU) extendida.</span><span class="sxs-lookup"><span data-stu-id="8ad8c-212">Extended Key Usage (EKU) settings.</span></span> <span data-ttu-id="8ad8c-213">Esta colección puede contener un máximo de 500 elementos.</span><span class="sxs-lookup"><span data-stu-id="8ad8c-213">This collection can contain a maximum of 500 elements.</span></span>|
|<span data-ttu-id="8ad8c-214">subjectAlternativeNameFormatString</span><span class="sxs-lookup"><span data-stu-id="8ad8c-214">subjectAlternativeNameFormatString</span></span>|<span data-ttu-id="8ad8c-215">String</span><span class="sxs-lookup"><span data-stu-id="8ad8c-215">String</span></span>|<span data-ttu-id="8ad8c-216">Cadena personalizada que define el atributo AAD.</span><span class="sxs-lookup"><span data-stu-id="8ad8c-216">Custom String that defines the AAD Attribute.</span></span>|



## <a name="response"></a><span data-ttu-id="8ad8c-217">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8ad8c-217">Response</span></span>
<span data-ttu-id="8ad8c-218">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto actualizado [macOSScepCertificateProfile](../resources/intune-deviceconfig-macosscepcertificateprofile.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8ad8c-218">If successful, this method returns a `200 OK` response code and an updated [macOSScepCertificateProfile](../resources/intune-deviceconfig-macosscepcertificateprofile.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="8ad8c-219">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="8ad8c-219">Example</span></span>
### <a name="request"></a><span data-ttu-id="8ad8c-220">Solicitud</span><span class="sxs-lookup"><span data-stu-id="8ad8c-220">Request</span></span>
<span data-ttu-id="8ad8c-221">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="8ad8c-221">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations/{deviceConfigurationId}
Content-type: application/json
Content-length: 963

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
  "scepServerUrls": [
    "Scep Server Urls value"
  ],
  "subjectNameFormatString": "Subject Name Format String value",
  "keyUsage": "digitalSignature",
  "keySize": "size2048",
  "hashAlgorithm": "sha2",
  "extendedKeyUsages": [
    {
      "@odata.type": "microsoft.graph.extendedKeyUsage",
      "name": "Name value",
      "objectIdentifier": "Object Identifier value"
    }
  ],
  "subjectAlternativeNameFormatString": "Subject Alternative Name Format String value"
}
```

### <a name="response"></a><span data-ttu-id="8ad8c-222">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8ad8c-222">Response</span></span>
<span data-ttu-id="8ad8c-p121">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="8ad8c-p121">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1137

{
  "@odata.type": "#microsoft.graph.macOSScepCertificateProfile",
  "id": "78c3929d-929d-78c3-9d92-c3789d92c378",
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
  "hashAlgorithm": "sha2",
  "extendedKeyUsages": [
    {
      "@odata.type": "microsoft.graph.extendedKeyUsage",
      "name": "Name value",
      "objectIdentifier": "Object Identifier value"
    }
  ],
  "subjectAlternativeNameFormatString": "Subject Alternative Name Format String value"
}
```





