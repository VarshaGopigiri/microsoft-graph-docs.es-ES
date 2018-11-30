---
title: Actualizar windowsPhone81SCEPCertificateProfile
description: Actualizar las propiedades de un objeto windowsPhone81SCEPCertificateProfile.
ms.openlocfilehash: eedcf43b824a8da45c79d0843551719e0f6a52aa
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085472"
---
# <a name="update-windowsphone81scepcertificateprofile"></a><span data-ttu-id="1d6b9-103">Actualizar windowsPhone81SCEPCertificateProfile</span><span class="sxs-lookup"><span data-stu-id="1d6b9-103">Update windowsPhone81SCEPCertificateProfile</span></span>

> <span data-ttu-id="1d6b9-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="1d6b9-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="1d6b9-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="1d6b9-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="1d6b9-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="1d6b9-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="1d6b9-107">Actualizar las propiedades de un objeto [windowsPhone81SCEPCertificateProfile](../resources/intune-deviceconfig-windowsphone81scepcertificateprofile.md) .</span><span class="sxs-lookup"><span data-stu-id="1d6b9-107">Update the properties of a [windowsPhone81SCEPCertificateProfile](../resources/intune-deviceconfig-windowsphone81scepcertificateprofile.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="1d6b9-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="1d6b9-108">Prerequisites</span></span>
<span data-ttu-id="1d6b9-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="1d6b9-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="1d6b9-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="1d6b9-111">Permission type</span></span>|<span data-ttu-id="1d6b9-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="1d6b9-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="1d6b9-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="1d6b9-113">Delegated (work or school account)</span></span>|<span data-ttu-id="1d6b9-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="1d6b9-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="1d6b9-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="1d6b9-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="1d6b9-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1d6b9-116">Not supported.</span></span>|
|<span data-ttu-id="1d6b9-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="1d6b9-117">Application</span></span>|<span data-ttu-id="1d6b9-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1d6b9-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="1d6b9-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="1d6b9-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/groupAssignments/{deviceConfigurationGroupAssignmentId}/deviceConfiguration
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsDomainJoinConfiguration/networkAccessConfigurations/{deviceConfigurationId}
```

## <a name="request-headers"></a><span data-ttu-id="1d6b9-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="1d6b9-120">Request headers</span></span>
|<span data-ttu-id="1d6b9-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1d6b9-121">Header</span></span>|<span data-ttu-id="1d6b9-122">Valor</span><span class="sxs-lookup"><span data-stu-id="1d6b9-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="1d6b9-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="1d6b9-123">Authorization</span></span>|<span data-ttu-id="1d6b9-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="1d6b9-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="1d6b9-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="1d6b9-125">Accept</span></span>|<span data-ttu-id="1d6b9-126">application/json</span><span class="sxs-lookup"><span data-stu-id="1d6b9-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="1d6b9-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="1d6b9-127">Request body</span></span>
<span data-ttu-id="1d6b9-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto [windowsPhone81SCEPCertificateProfile](../resources/intune-deviceconfig-windowsphone81scepcertificateprofile.md) .</span><span class="sxs-lookup"><span data-stu-id="1d6b9-128">In the request body, supply a JSON representation for the [windowsPhone81SCEPCertificateProfile](../resources/intune-deviceconfig-windowsphone81scepcertificateprofile.md) object.</span></span>

<span data-ttu-id="1d6b9-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el [windowsPhone81SCEPCertificateProfile](../resources/intune-deviceconfig-windowsphone81scepcertificateprofile.md).</span><span class="sxs-lookup"><span data-stu-id="1d6b9-129">The following table shows the properties that are required when you create the [windowsPhone81SCEPCertificateProfile](../resources/intune-deviceconfig-windowsphone81scepcertificateprofile.md).</span></span>

|<span data-ttu-id="1d6b9-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="1d6b9-130">Property</span></span>|<span data-ttu-id="1d6b9-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="1d6b9-131">Type</span></span>|<span data-ttu-id="1d6b9-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="1d6b9-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="1d6b9-133">id</span><span class="sxs-lookup"><span data-stu-id="1d6b9-133">id</span></span>|<span data-ttu-id="1d6b9-134">String</span><span class="sxs-lookup"><span data-stu-id="1d6b9-134">String</span></span>|<span data-ttu-id="1d6b9-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="1d6b9-135">Key of the entity.</span></span> <span data-ttu-id="1d6b9-136">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="1d6b9-136">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="1d6b9-137">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="1d6b9-137">lastModifiedDateTime</span></span>|<span data-ttu-id="1d6b9-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="1d6b9-138">DateTimeOffset</span></span>|<span data-ttu-id="1d6b9-139">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="1d6b9-139">DateTime the object was last modified.</span></span> <span data-ttu-id="1d6b9-140">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="1d6b9-140">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="1d6b9-141">roleScopeTagIds</span><span class="sxs-lookup"><span data-stu-id="1d6b9-141">roleScopeTagIds</span></span>|<span data-ttu-id="1d6b9-142">Colección String</span><span class="sxs-lookup"><span data-stu-id="1d6b9-142">String collection</span></span>|<span data-ttu-id="1d6b9-143">Lista de etiquetas de ámbito para esta instancia de entidad.</span><span class="sxs-lookup"><span data-stu-id="1d6b9-143">List of Scope Tags for this Entity instance.</span></span> <span data-ttu-id="1d6b9-144">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="1d6b9-144">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="1d6b9-145">supportsScopeTags</span><span class="sxs-lookup"><span data-stu-id="1d6b9-145">supportsScopeTags</span></span>|<span data-ttu-id="1d6b9-146">Booleano</span><span class="sxs-lookup"><span data-stu-id="1d6b9-146">Boolean</span></span>|<span data-ttu-id="1d6b9-147">Indica si la configuración del dispositivo subyacente admite la asignación de etiquetas de ámbito.</span><span class="sxs-lookup"><span data-stu-id="1d6b9-147">Indicates whether or not the underlying Device Configuration supports the assignment of scope tags.</span></span> <span data-ttu-id="1d6b9-148">No se permite la asignación a la propiedad ScopeTags cuando este valor es false y entidades no estará visibles para los usuarios con ámbito.</span><span class="sxs-lookup"><span data-stu-id="1d6b9-148">Assigning to the ScopeTags property is not allowed when this value is false and entities will not be visible to scoped users.</span></span> <span data-ttu-id="1d6b9-149">Esto se produce para las directivas de heredado creadas en Silverlight y se puede resolver por eliminar y volver a crear la directiva en el Portal de Azure.</span><span class="sxs-lookup"><span data-stu-id="1d6b9-149">This occurs for Legacy policies created in Silverlight and can be resolved by deleting and recreating the policy in the Azure Portal.</span></span> <span data-ttu-id="1d6b9-150">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="1d6b9-150">This property is read-only.</span></span> <span data-ttu-id="1d6b9-151">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="1d6b9-151">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="1d6b9-152">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="1d6b9-152">createdDateTime</span></span>|<span data-ttu-id="1d6b9-153">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="1d6b9-153">DateTimeOffset</span></span>|<span data-ttu-id="1d6b9-154">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="1d6b9-154">DateTime the object was created.</span></span> <span data-ttu-id="1d6b9-155">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="1d6b9-155">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="1d6b9-156">descripción</span><span class="sxs-lookup"><span data-stu-id="1d6b9-156">description</span></span>|<span data-ttu-id="1d6b9-157">String</span><span class="sxs-lookup"><span data-stu-id="1d6b9-157">String</span></span>|<span data-ttu-id="1d6b9-158">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1d6b9-158">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="1d6b9-159">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="1d6b9-159">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="1d6b9-160">displayName</span><span class="sxs-lookup"><span data-stu-id="1d6b9-160">displayName</span></span>|<span data-ttu-id="1d6b9-161">String</span><span class="sxs-lookup"><span data-stu-id="1d6b9-161">String</span></span>|<span data-ttu-id="1d6b9-162">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1d6b9-162">Admin provided name of the device configuration.</span></span> <span data-ttu-id="1d6b9-163">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="1d6b9-163">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="1d6b9-164">version</span><span class="sxs-lookup"><span data-stu-id="1d6b9-164">version</span></span>|<span data-ttu-id="1d6b9-165">Int32</span><span class="sxs-lookup"><span data-stu-id="1d6b9-165">Int32</span></span>|<span data-ttu-id="1d6b9-166">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1d6b9-166">Version of the device configuration.</span></span> <span data-ttu-id="1d6b9-167">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="1d6b9-167">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="1d6b9-168">renewalThresholdPercentage</span><span class="sxs-lookup"><span data-stu-id="1d6b9-168">renewalThresholdPercentage</span></span>|<span data-ttu-id="1d6b9-169">Int32</span><span class="sxs-lookup"><span data-stu-id="1d6b9-169">Int32</span></span>|<span data-ttu-id="1d6b9-170">Porcentaje de umbral de renovación de certificado.</span><span class="sxs-lookup"><span data-stu-id="1d6b9-170">Certificate renewal threshold percentage.</span></span> <span data-ttu-id="1d6b9-171">Se hereda de [windowsPhone81CertificateProfileBase](../resources/intune-deviceconfig-windowsphone81certificateprofilebase.md)</span><span class="sxs-lookup"><span data-stu-id="1d6b9-171">Inherited from [windowsPhone81CertificateProfileBase](../resources/intune-deviceconfig-windowsphone81certificateprofilebase.md)</span></span>|
|<span data-ttu-id="1d6b9-172">keyStorageProvider</span><span class="sxs-lookup"><span data-stu-id="1d6b9-172">keyStorageProvider</span></span>|[<span data-ttu-id="1d6b9-173">keyStorageProviderOption</span><span class="sxs-lookup"><span data-stu-id="1d6b9-173">keyStorageProviderOption</span></span>](../resources/intune-deviceconfig-keystorageprovideroption.md)|<span data-ttu-id="1d6b9-174">Proveedor de almacenamiento de claves (KSP).</span><span class="sxs-lookup"><span data-stu-id="1d6b9-174">Key Storage Provider (KSP).</span></span> <span data-ttu-id="1d6b9-175">Se hereda de [windowsPhone81CertificateProfileBase](../resources/intune-deviceconfig-windowsphone81certificateprofilebase.md).</span><span class="sxs-lookup"><span data-stu-id="1d6b9-175">Inherited from [windowsPhone81CertificateProfileBase](../resources/intune-deviceconfig-windowsphone81certificateprofilebase.md).</span></span> <span data-ttu-id="1d6b9-176">Los valores posibles son: `useTpmKspOtherwiseUseSoftwareKsp`, `useTpmKspOtherwiseFail`, `usePassportForWorkKspOtherwiseFail` y `useSoftwareKsp`.</span><span class="sxs-lookup"><span data-stu-id="1d6b9-176">Possible values are: `useTpmKspOtherwiseUseSoftwareKsp`, `useTpmKspOtherwiseFail`, `usePassportForWorkKspOtherwiseFail`, `useSoftwareKsp`.</span></span>|
|<span data-ttu-id="1d6b9-177">subjectNameFormat</span><span class="sxs-lookup"><span data-stu-id="1d6b9-177">subjectNameFormat</span></span>|[<span data-ttu-id="1d6b9-178">subjectNameFormat</span><span class="sxs-lookup"><span data-stu-id="1d6b9-178">subjectNameFormat</span></span>](../resources/intune-deviceconfig-subjectnameformat.md)|<span data-ttu-id="1d6b9-179">Formato de nombre de sujeto de certificado.</span><span class="sxs-lookup"><span data-stu-id="1d6b9-179">Certificate Subject Name Format.</span></span> <span data-ttu-id="1d6b9-180">Se hereda de [windowsPhone81CertificateProfileBase](../resources/intune-deviceconfig-windowsphone81certificateprofilebase.md).</span><span class="sxs-lookup"><span data-stu-id="1d6b9-180">Inherited from [windowsPhone81CertificateProfileBase](../resources/intune-deviceconfig-windowsphone81certificateprofilebase.md).</span></span> <span data-ttu-id="1d6b9-181">Los valores posibles son: `commonName`, `commonNameIncludingEmail`, `commonNameAsEmail`, `custom`, `commonNameAsIMEI`, `commonNameAsSerialNumber`, `commonNameAsAadDeviceId`, `commonNameAsIntuneDeviceId` y `commonNameAsDurableDeviceId`.</span><span class="sxs-lookup"><span data-stu-id="1d6b9-181">Possible values are: `commonName`, `commonNameIncludingEmail`, `commonNameAsEmail`, `custom`, `commonNameAsIMEI`, `commonNameAsSerialNumber`, `commonNameAsAadDeviceId`, `commonNameAsIntuneDeviceId`, `commonNameAsDurableDeviceId`.</span></span>|
|<span data-ttu-id="1d6b9-182">subjectAlternativeNameType</span><span class="sxs-lookup"><span data-stu-id="1d6b9-182">subjectAlternativeNameType</span></span>|[<span data-ttu-id="1d6b9-183">subjectAlternativeNameType</span><span class="sxs-lookup"><span data-stu-id="1d6b9-183">subjectAlternativeNameType</span></span>](../resources/intune-deviceconfig-subjectalternativenametype.md)|<span data-ttu-id="1d6b9-184">Tipo de nombre alternativo de sujeto de certificado.</span><span class="sxs-lookup"><span data-stu-id="1d6b9-184">Certificate Subject Alternative Name Type.</span></span> <span data-ttu-id="1d6b9-185">Se hereda de [windowsPhone81CertificateProfileBase](../resources/intune-deviceconfig-windowsphone81certificateprofilebase.md).</span><span class="sxs-lookup"><span data-stu-id="1d6b9-185">Inherited from [windowsPhone81CertificateProfileBase](../resources/intune-deviceconfig-windowsphone81certificateprofilebase.md).</span></span> <span data-ttu-id="1d6b9-186">Los valores posibles son: `none`, `emailAddress`, `userPrincipalName`, `customAzureADAttribute` y `domainNameService`.</span><span class="sxs-lookup"><span data-stu-id="1d6b9-186">Possible values are: `none`, `emailAddress`, `userPrincipalName`, `customAzureADAttribute`, `domainNameService`.</span></span>|
|<span data-ttu-id="1d6b9-187">certificateValidityPeriodValue</span><span class="sxs-lookup"><span data-stu-id="1d6b9-187">certificateValidityPeriodValue</span></span>|<span data-ttu-id="1d6b9-188">Int32</span><span class="sxs-lookup"><span data-stu-id="1d6b9-188">Int32</span></span>|<span data-ttu-id="1d6b9-189">Valor para el período de Validtiy de certificado.</span><span class="sxs-lookup"><span data-stu-id="1d6b9-189">Value for the Certificate Validtiy Period.</span></span> <span data-ttu-id="1d6b9-190">Se hereda de [windowsPhone81CertificateProfileBase](../resources/intune-deviceconfig-windowsphone81certificateprofilebase.md)</span><span class="sxs-lookup"><span data-stu-id="1d6b9-190">Inherited from [windowsPhone81CertificateProfileBase](../resources/intune-deviceconfig-windowsphone81certificateprofilebase.md)</span></span>|
|<span data-ttu-id="1d6b9-191">certificateValidityPeriodScale</span><span class="sxs-lookup"><span data-stu-id="1d6b9-191">certificateValidityPeriodScale</span></span>|[<span data-ttu-id="1d6b9-192">certificateValidityPeriodScale</span><span class="sxs-lookup"><span data-stu-id="1d6b9-192">certificateValidityPeriodScale</span></span>](../resources/intune-deviceconfig-certificatevalidityperiodscale.md)|<span data-ttu-id="1d6b9-193">Escala para el período de validez del certificado.</span><span class="sxs-lookup"><span data-stu-id="1d6b9-193">Scale for the Certificate Validity Period.</span></span> <span data-ttu-id="1d6b9-194">Se hereda de [windowsPhone81CertificateProfileBase](../resources/intune-deviceconfig-windowsphone81certificateprofilebase.md).</span><span class="sxs-lookup"><span data-stu-id="1d6b9-194">Inherited from [windowsPhone81CertificateProfileBase](../resources/intune-deviceconfig-windowsphone81certificateprofilebase.md).</span></span> <span data-ttu-id="1d6b9-195">Los valores posibles son: `days`, `months` y `years`.</span><span class="sxs-lookup"><span data-stu-id="1d6b9-195">Possible values are: `days`, `months`, `years`.</span></span>|
|<span data-ttu-id="1d6b9-196">extendedKeyUsages</span><span class="sxs-lookup"><span data-stu-id="1d6b9-196">extendedKeyUsages</span></span>|<span data-ttu-id="1d6b9-197">colección de [ExtendeKeyUsage](../resources/intune-deviceconfig-extendedkeyusage.md)</span><span class="sxs-lookup"><span data-stu-id="1d6b9-197">[extendedKeyUsage](../resources/intune-deviceconfig-extendedkeyusage.md) collection</span></span>|<span data-ttu-id="1d6b9-198">Configuración de clave (EKU) extendida.</span><span class="sxs-lookup"><span data-stu-id="1d6b9-198">Extended Key Usage (EKU) settings.</span></span> <span data-ttu-id="1d6b9-199">Esta colección puede contener un máximo de 500 elementos.</span><span class="sxs-lookup"><span data-stu-id="1d6b9-199">This collection can contain a maximum of 500 elements.</span></span> <span data-ttu-id="1d6b9-200">Se hereda de [windowsPhone81CertificateProfileBase](../resources/intune-deviceconfig-windowsphone81certificateprofilebase.md)</span><span class="sxs-lookup"><span data-stu-id="1d6b9-200">Inherited from [windowsPhone81CertificateProfileBase](../resources/intune-deviceconfig-windowsphone81certificateprofilebase.md)</span></span>|
|<span data-ttu-id="1d6b9-201">scepServerUrls</span><span class="sxs-lookup"><span data-stu-id="1d6b9-201">scepServerUrls</span></span>|<span data-ttu-id="1d6b9-202">Colección String</span><span class="sxs-lookup"><span data-stu-id="1d6b9-202">String collection</span></span>|<span data-ttu-id="1d6b9-203">Direcciones URL del servidor SCEP.</span><span class="sxs-lookup"><span data-stu-id="1d6b9-203">SCEP Server Url(s).</span></span>|
|<span data-ttu-id="1d6b9-204">subjectNameFormatString</span><span class="sxs-lookup"><span data-stu-id="1d6b9-204">subjectNameFormatString</span></span>|<span data-ttu-id="1d6b9-205">String</span><span class="sxs-lookup"><span data-stu-id="1d6b9-205">String</span></span>|<span data-ttu-id="1d6b9-206">Formato personalizado para usar con SubjectNameFormat = personalizada.</span><span class="sxs-lookup"><span data-stu-id="1d6b9-206">Custom format to use with SubjectNameFormat = Custom.</span></span> <span data-ttu-id="1d6b9-207">Ejemplo: CN = {{EmailAddress}}, E = {{EmailAddress}}, OU = Users de la empresa, O = Contoso Corporation, L = Redmond, ST = WA, C = US</span><span class="sxs-lookup"><span data-stu-id="1d6b9-207">Example: CN={{EmailAddress}},E={{EmailAddress}},OU=Enterprise Users,O=Contoso Corporation,L=Redmond,ST=WA,C=US</span></span>|
|<span data-ttu-id="1d6b9-208">keyUsage</span><span class="sxs-lookup"><span data-stu-id="1d6b9-208">keyUsage</span></span>|[<span data-ttu-id="1d6b9-209">keyUsages</span><span class="sxs-lookup"><span data-stu-id="1d6b9-209">keyUsages</span></span>](../resources/intune-deviceconfig-keyusages.md)|<span data-ttu-id="1d6b9-210">Uso de la clave SCEP.</span><span class="sxs-lookup"><span data-stu-id="1d6b9-210">SCEP Key Usage.</span></span> <span data-ttu-id="1d6b9-211">Los valores posibles son: `keyEncipherment` y `digitalSignature`.</span><span class="sxs-lookup"><span data-stu-id="1d6b9-211">Possible values are: `keyEncipherment`, `digitalSignature`.</span></span>|
|<span data-ttu-id="1d6b9-212">keySize</span><span class="sxs-lookup"><span data-stu-id="1d6b9-212">keySize</span></span>|[<span data-ttu-id="1d6b9-213">keySize</span><span class="sxs-lookup"><span data-stu-id="1d6b9-213">keySize</span></span>](../resources/intune-deviceconfig-keysize.md)|<span data-ttu-id="1d6b9-214">Tamaño de la clave SCEP.</span><span class="sxs-lookup"><span data-stu-id="1d6b9-214">SCEP Key Size.</span></span> <span data-ttu-id="1d6b9-215">Los valores posibles son: `size1024` y `size2048`.</span><span class="sxs-lookup"><span data-stu-id="1d6b9-215">Possible values are: `size1024`, `size2048`.</span></span>|
|<span data-ttu-id="1d6b9-216">hashAlgorithm</span><span class="sxs-lookup"><span data-stu-id="1d6b9-216">hashAlgorithm</span></span>|[<span data-ttu-id="1d6b9-217">hashAlgorithms</span><span class="sxs-lookup"><span data-stu-id="1d6b9-217">hashAlgorithms</span></span>](../resources/intune-deviceconfig-hashalgorithms.md)|<span data-ttu-id="1d6b9-218">Algoritmo de Hash SCEP.</span><span class="sxs-lookup"><span data-stu-id="1d6b9-218">SCEP Hash Algorithm.</span></span> <span data-ttu-id="1d6b9-219">Los valores posibles son: `sha1` y `sha2`.</span><span class="sxs-lookup"><span data-stu-id="1d6b9-219">Possible values are: `sha1`, `sha2`.</span></span>|
|<span data-ttu-id="1d6b9-220">subjectAlternativeNameFormatString</span><span class="sxs-lookup"><span data-stu-id="1d6b9-220">subjectAlternativeNameFormatString</span></span>|<span data-ttu-id="1d6b9-221">String</span><span class="sxs-lookup"><span data-stu-id="1d6b9-221">String</span></span>|<span data-ttu-id="1d6b9-222">Cadena personalizada que define el atributo AAD.</span><span class="sxs-lookup"><span data-stu-id="1d6b9-222">Custom String that defines the AAD Attribute.</span></span>|



## <a name="response"></a><span data-ttu-id="1d6b9-223">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1d6b9-223">Response</span></span>
<span data-ttu-id="1d6b9-224">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto actualizado [windowsPhone81SCEPCertificateProfile](../resources/intune-deviceconfig-windowsphone81scepcertificateprofile.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1d6b9-224">If successful, this method returns a `200 OK` response code and an updated [windowsPhone81SCEPCertificateProfile](../resources/intune-deviceconfig-windowsphone81scepcertificateprofile.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="1d6b9-225">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1d6b9-225">Example</span></span>
### <a name="request"></a><span data-ttu-id="1d6b9-226">Solicitud</span><span class="sxs-lookup"><span data-stu-id="1d6b9-226">Request</span></span>
<span data-ttu-id="1d6b9-227">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="1d6b9-227">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations/{deviceConfigurationId}
Content-type: application/json
Content-length: 1021

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

### <a name="response"></a><span data-ttu-id="1d6b9-228">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1d6b9-228">Response</span></span>
<span data-ttu-id="1d6b9-p122">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="1d6b9-p122">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
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





