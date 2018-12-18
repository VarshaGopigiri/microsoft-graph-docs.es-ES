---
title: Actualizar windows81SCEPCertificateProfile
description: Actualizar las propiedades de un objeto windows81SCEPCertificateProfile.
author: tfitzmac
ms.openlocfilehash: 39571d85a1eb7d9a2d5d0a18f178fb2cb1be7e02
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27338223"
---
# <a name="update-windows81scepcertificateprofile"></a><span data-ttu-id="b3a28-103">Actualizar windows81SCEPCertificateProfile</span><span class="sxs-lookup"><span data-stu-id="b3a28-103">Update windows81SCEPCertificateProfile</span></span>

> <span data-ttu-id="b3a28-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="b3a28-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="b3a28-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="b3a28-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="b3a28-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="b3a28-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="b3a28-107">Actualizar las propiedades de un objeto [windows81SCEPCertificateProfile](../resources/intune-deviceconfig-windows81scepcertificateprofile.md) .</span><span class="sxs-lookup"><span data-stu-id="b3a28-107">Update the properties of a [windows81SCEPCertificateProfile](../resources/intune-deviceconfig-windows81scepcertificateprofile.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="b3a28-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="b3a28-108">Prerequisites</span></span>
<span data-ttu-id="b3a28-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="b3a28-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="b3a28-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b3a28-111">Permission type</span></span>|<span data-ttu-id="b3a28-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b3a28-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="b3a28-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b3a28-113">Delegated (work or school account)</span></span>|<span data-ttu-id="b3a28-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="b3a28-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="b3a28-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b3a28-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="b3a28-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b3a28-116">Not supported.</span></span>|
|<span data-ttu-id="b3a28-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b3a28-117">Application</span></span>|<span data-ttu-id="b3a28-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b3a28-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="b3a28-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b3a28-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/groupAssignments/{deviceConfigurationGroupAssignmentId}/deviceConfiguration
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsDomainJoinConfiguration/networkAccessConfigurations/{deviceConfigurationId}
```

## <a name="request-headers"></a><span data-ttu-id="b3a28-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b3a28-120">Request headers</span></span>
|<span data-ttu-id="b3a28-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b3a28-121">Header</span></span>|<span data-ttu-id="b3a28-122">Valor</span><span class="sxs-lookup"><span data-stu-id="b3a28-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="b3a28-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="b3a28-123">Authorization</span></span>|<span data-ttu-id="b3a28-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="b3a28-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="b3a28-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="b3a28-125">Accept</span></span>|<span data-ttu-id="b3a28-126">application/json</span><span class="sxs-lookup"><span data-stu-id="b3a28-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="b3a28-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b3a28-127">Request body</span></span>
<span data-ttu-id="b3a28-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto [windows81SCEPCertificateProfile](../resources/intune-deviceconfig-windows81scepcertificateprofile.md) .</span><span class="sxs-lookup"><span data-stu-id="b3a28-128">In the request body, supply a JSON representation for the [windows81SCEPCertificateProfile](../resources/intune-deviceconfig-windows81scepcertificateprofile.md) object.</span></span>

<span data-ttu-id="b3a28-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el [windows81SCEPCertificateProfile](../resources/intune-deviceconfig-windows81scepcertificateprofile.md).</span><span class="sxs-lookup"><span data-stu-id="b3a28-129">The following table shows the properties that are required when you create the [windows81SCEPCertificateProfile](../resources/intune-deviceconfig-windows81scepcertificateprofile.md).</span></span>

|<span data-ttu-id="b3a28-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="b3a28-130">Property</span></span>|<span data-ttu-id="b3a28-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="b3a28-131">Type</span></span>|<span data-ttu-id="b3a28-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="b3a28-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="b3a28-133">id</span><span class="sxs-lookup"><span data-stu-id="b3a28-133">id</span></span>|<span data-ttu-id="b3a28-134">String</span><span class="sxs-lookup"><span data-stu-id="b3a28-134">String</span></span>|<span data-ttu-id="b3a28-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="b3a28-135">Key of the entity.</span></span> <span data-ttu-id="b3a28-136">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="b3a28-136">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="b3a28-137">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="b3a28-137">lastModifiedDateTime</span></span>|<span data-ttu-id="b3a28-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="b3a28-138">DateTimeOffset</span></span>|<span data-ttu-id="b3a28-139">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="b3a28-139">DateTime the object was last modified.</span></span> <span data-ttu-id="b3a28-140">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="b3a28-140">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="b3a28-141">roleScopeTagIds</span><span class="sxs-lookup"><span data-stu-id="b3a28-141">roleScopeTagIds</span></span>|<span data-ttu-id="b3a28-142">Colección String</span><span class="sxs-lookup"><span data-stu-id="b3a28-142">String collection</span></span>|<span data-ttu-id="b3a28-143">Lista de etiquetas de ámbito para esta instancia de entidad.</span><span class="sxs-lookup"><span data-stu-id="b3a28-143">List of Scope Tags for this Entity instance.</span></span> <span data-ttu-id="b3a28-144">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="b3a28-144">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="b3a28-145">supportsScopeTags</span><span class="sxs-lookup"><span data-stu-id="b3a28-145">supportsScopeTags</span></span>|<span data-ttu-id="b3a28-146">Boolean</span><span class="sxs-lookup"><span data-stu-id="b3a28-146">Boolean</span></span>|<span data-ttu-id="b3a28-147">Indica si la configuración del dispositivo subyacente admite la asignación de etiquetas de ámbito.</span><span class="sxs-lookup"><span data-stu-id="b3a28-147">Indicates whether or not the underlying Device Configuration supports the assignment of scope tags.</span></span> <span data-ttu-id="b3a28-148">No se permite la asignación a la propiedad ScopeTags cuando este valor es false y entidades no estará visibles para los usuarios con ámbito.</span><span class="sxs-lookup"><span data-stu-id="b3a28-148">Assigning to the ScopeTags property is not allowed when this value is false and entities will not be visible to scoped users.</span></span> <span data-ttu-id="b3a28-149">Esto se produce para las directivas de heredado creadas en Silverlight y se puede resolver por eliminar y volver a crear la directiva en el Portal de Azure.</span><span class="sxs-lookup"><span data-stu-id="b3a28-149">This occurs for Legacy policies created in Silverlight and can be resolved by deleting and recreating the policy in the Azure Portal.</span></span> <span data-ttu-id="b3a28-150">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="b3a28-150">This property is read-only.</span></span> <span data-ttu-id="b3a28-151">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="b3a28-151">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="b3a28-152">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="b3a28-152">createdDateTime</span></span>|<span data-ttu-id="b3a28-153">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="b3a28-153">DateTimeOffset</span></span>|<span data-ttu-id="b3a28-154">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="b3a28-154">DateTime the object was created.</span></span> <span data-ttu-id="b3a28-155">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="b3a28-155">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="b3a28-156">descripción</span><span class="sxs-lookup"><span data-stu-id="b3a28-156">description</span></span>|<span data-ttu-id="b3a28-157">String</span><span class="sxs-lookup"><span data-stu-id="b3a28-157">String</span></span>|<span data-ttu-id="b3a28-158">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b3a28-158">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="b3a28-159">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="b3a28-159">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="b3a28-160">displayName</span><span class="sxs-lookup"><span data-stu-id="b3a28-160">displayName</span></span>|<span data-ttu-id="b3a28-161">String</span><span class="sxs-lookup"><span data-stu-id="b3a28-161">String</span></span>|<span data-ttu-id="b3a28-162">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b3a28-162">Admin provided name of the device configuration.</span></span> <span data-ttu-id="b3a28-163">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="b3a28-163">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="b3a28-164">version</span><span class="sxs-lookup"><span data-stu-id="b3a28-164">version</span></span>|<span data-ttu-id="b3a28-165">Int32</span><span class="sxs-lookup"><span data-stu-id="b3a28-165">Int32</span></span>|<span data-ttu-id="b3a28-166">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b3a28-166">Version of the device configuration.</span></span> <span data-ttu-id="b3a28-167">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="b3a28-167">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="b3a28-168">renewalThresholdPercentage</span><span class="sxs-lookup"><span data-stu-id="b3a28-168">renewalThresholdPercentage</span></span>|<span data-ttu-id="b3a28-169">Int32</span><span class="sxs-lookup"><span data-stu-id="b3a28-169">Int32</span></span>|<span data-ttu-id="b3a28-170">Porcentaje de umbral de renovación de certificado.</span><span class="sxs-lookup"><span data-stu-id="b3a28-170">Certificate renewal threshold percentage.</span></span> <span data-ttu-id="b3a28-171">Válido valores heredada de 1 a 99 de [windowsCertificateProfileBase](../resources/intune-deviceconfig-windowscertificateprofilebase.md)</span><span class="sxs-lookup"><span data-stu-id="b3a28-171">Valid values 1 to 99 Inherited from [windowsCertificateProfileBase](../resources/intune-deviceconfig-windowscertificateprofilebase.md)</span></span>|
|<span data-ttu-id="b3a28-172">keyStorageProvider</span><span class="sxs-lookup"><span data-stu-id="b3a28-172">keyStorageProvider</span></span>|[<span data-ttu-id="b3a28-173">keyStorageProviderOption</span><span class="sxs-lookup"><span data-stu-id="b3a28-173">keyStorageProviderOption</span></span>](../resources/intune-deviceconfig-keystorageprovideroption.md)|<span data-ttu-id="b3a28-174">Proveedor de almacenamiento de claves (KSP) Inherited desde [windowsCertificateProfileBase](../resources/intune-deviceconfig-windowscertificateprofilebase.md).</span><span class="sxs-lookup"><span data-stu-id="b3a28-174">Key Storage Provider (KSP) Inherited from [windowsCertificateProfileBase](../resources/intune-deviceconfig-windowscertificateprofilebase.md).</span></span> <span data-ttu-id="b3a28-175">Los valores posibles son: `useTpmKspOtherwiseUseSoftwareKsp`, `useTpmKspOtherwiseFail`, `usePassportForWorkKspOtherwiseFail` y `useSoftwareKsp`.</span><span class="sxs-lookup"><span data-stu-id="b3a28-175">Possible values are: `useTpmKspOtherwiseUseSoftwareKsp`, `useTpmKspOtherwiseFail`, `usePassportForWorkKspOtherwiseFail`, `useSoftwareKsp`.</span></span>|
|<span data-ttu-id="b3a28-176">subjectNameFormat</span><span class="sxs-lookup"><span data-stu-id="b3a28-176">subjectNameFormat</span></span>|[<span data-ttu-id="b3a28-177">subjectNameFormat</span><span class="sxs-lookup"><span data-stu-id="b3a28-177">subjectNameFormat</span></span>](../resources/intune-deviceconfig-subjectnameformat.md)|<span data-ttu-id="b3a28-178">Certificado heredado de formato de nombre de sujeto de [windowsCertificateProfileBase](../resources/intune-deviceconfig-windowscertificateprofilebase.md).</span><span class="sxs-lookup"><span data-stu-id="b3a28-178">Certificate Subject Name Format Inherited from [windowsCertificateProfileBase](../resources/intune-deviceconfig-windowscertificateprofilebase.md).</span></span> <span data-ttu-id="b3a28-179">Los valores posibles son: `commonName`, `commonNameIncludingEmail`, `commonNameAsEmail`, `custom`, `commonNameAsIMEI`, `commonNameAsSerialNumber`, `commonNameAsAadDeviceId`, `commonNameAsIntuneDeviceId` y `commonNameAsDurableDeviceId`.</span><span class="sxs-lookup"><span data-stu-id="b3a28-179">Possible values are: `commonName`, `commonNameIncludingEmail`, `commonNameAsEmail`, `custom`, `commonNameAsIMEI`, `commonNameAsSerialNumber`, `commonNameAsAadDeviceId`, `commonNameAsIntuneDeviceId`, `commonNameAsDurableDeviceId`.</span></span>|
|<span data-ttu-id="b3a28-180">subjectAlternativeNameType</span><span class="sxs-lookup"><span data-stu-id="b3a28-180">subjectAlternativeNameType</span></span>|[<span data-ttu-id="b3a28-181">subjectAlternativeNameType</span><span class="sxs-lookup"><span data-stu-id="b3a28-181">subjectAlternativeNameType</span></span>](../resources/intune-deviceconfig-subjectalternativenametype.md)|<span data-ttu-id="b3a28-182">Certificado asunto alternativa nombre tipo hereda de [windowsCertificateProfileBase](../resources/intune-deviceconfig-windowscertificateprofilebase.md).</span><span class="sxs-lookup"><span data-stu-id="b3a28-182">Certificate Subject Alternative Name Type Inherited from [windowsCertificateProfileBase](../resources/intune-deviceconfig-windowscertificateprofilebase.md).</span></span> <span data-ttu-id="b3a28-183">Los valores posibles son: `none`, `emailAddress`, `userPrincipalName`, `customAzureADAttribute` y `domainNameService`.</span><span class="sxs-lookup"><span data-stu-id="b3a28-183">Possible values are: `none`, `emailAddress`, `userPrincipalName`, `customAzureADAttribute`, `domainNameService`.</span></span>|
|<span data-ttu-id="b3a28-184">certificateValidityPeriodValue</span><span class="sxs-lookup"><span data-stu-id="b3a28-184">certificateValidityPeriodValue</span></span>|<span data-ttu-id="b3a28-185">Int32</span><span class="sxs-lookup"><span data-stu-id="b3a28-185">Int32</span></span>|<span data-ttu-id="b3a28-186">Valor para el heredado de período de validez de certificado de [windowsCertificateProfileBase](../resources/intune-deviceconfig-windowscertificateprofilebase.md)</span><span class="sxs-lookup"><span data-stu-id="b3a28-186">Value for the Certificate Validity Period Inherited from [windowsCertificateProfileBase](../resources/intune-deviceconfig-windowscertificateprofilebase.md)</span></span>|
|<span data-ttu-id="b3a28-187">certificateValidityPeriodScale</span><span class="sxs-lookup"><span data-stu-id="b3a28-187">certificateValidityPeriodScale</span></span>|[<span data-ttu-id="b3a28-188">certificateValidityPeriodScale</span><span class="sxs-lookup"><span data-stu-id="b3a28-188">certificateValidityPeriodScale</span></span>](../resources/intune-deviceconfig-certificatevalidityperiodscale.md)|<span data-ttu-id="b3a28-189">Escala para la heredada de período de validez de certificado de [windowsCertificateProfileBase](../resources/intune-deviceconfig-windowscertificateprofilebase.md).</span><span class="sxs-lookup"><span data-stu-id="b3a28-189">Scale for the Certificate Validity Period Inherited from [windowsCertificateProfileBase](../resources/intune-deviceconfig-windowscertificateprofilebase.md).</span></span> <span data-ttu-id="b3a28-190">Los valores posibles son: `days`, `months` y `years`.</span><span class="sxs-lookup"><span data-stu-id="b3a28-190">Possible values are: `days`, `months`, `years`.</span></span>|
|<span data-ttu-id="b3a28-191">extendedKeyUsages</span><span class="sxs-lookup"><span data-stu-id="b3a28-191">extendedKeyUsages</span></span>|<span data-ttu-id="b3a28-192">colección de [ExtendeKeyUsage](../resources/intune-deviceconfig-extendedkeyusage.md)</span><span class="sxs-lookup"><span data-stu-id="b3a28-192">[extendedKeyUsage](../resources/intune-deviceconfig-extendedkeyusage.md) collection</span></span>|<span data-ttu-id="b3a28-193">Configuración de clave (EKU) extendida.</span><span class="sxs-lookup"><span data-stu-id="b3a28-193">Extended Key Usage (EKU) settings.</span></span> <span data-ttu-id="b3a28-194">Esta colección puede contener un máximo de 500 elementos.</span><span class="sxs-lookup"><span data-stu-id="b3a28-194">This collection can contain a maximum of 500 elements.</span></span> <span data-ttu-id="b3a28-195">Se hereda de [windows81CertificateProfileBase](../resources/intune-deviceconfig-windows81certificateprofilebase.md)</span><span class="sxs-lookup"><span data-stu-id="b3a28-195">Inherited from [windows81CertificateProfileBase](../resources/intune-deviceconfig-windows81certificateprofilebase.md)</span></span>|
|<span data-ttu-id="b3a28-196">customSubjectAlternativeNames</span><span class="sxs-lookup"><span data-stu-id="b3a28-196">customSubjectAlternativeNames</span></span>|<span data-ttu-id="b3a28-197">colección de [customSubjectAlternativeName](../resources/intune-deviceconfig-customsubjectalternativename.md)</span><span class="sxs-lookup"><span data-stu-id="b3a28-197">[customSubjectAlternativeName](../resources/intune-deviceconfig-customsubjectalternativename.md) collection</span></span>|<span data-ttu-id="b3a28-198">Configuración de Alterantive nombre de sujeto personalizado.</span><span class="sxs-lookup"><span data-stu-id="b3a28-198">Custom Subject Alterantive Name Settings.</span></span> <span data-ttu-id="b3a28-199">Esta colección puede contener un máximo de 500 elementos.</span><span class="sxs-lookup"><span data-stu-id="b3a28-199">This collection can contain a maximum of 500 elements.</span></span> <span data-ttu-id="b3a28-200">Se hereda de [windows81CertificateProfileBase](../resources/intune-deviceconfig-windows81certificateprofilebase.md)</span><span class="sxs-lookup"><span data-stu-id="b3a28-200">Inherited from [windows81CertificateProfileBase](../resources/intune-deviceconfig-windows81certificateprofilebase.md)</span></span>|
|<span data-ttu-id="b3a28-201">scepServerUrls</span><span class="sxs-lookup"><span data-stu-id="b3a28-201">scepServerUrls</span></span>|<span data-ttu-id="b3a28-202">Colección String</span><span class="sxs-lookup"><span data-stu-id="b3a28-202">String collection</span></span>|<span data-ttu-id="b3a28-203">Direcciones URL del servidor SCEP.</span><span class="sxs-lookup"><span data-stu-id="b3a28-203">SCEP Server Url(s).</span></span>|
|<span data-ttu-id="b3a28-204">subjectNameFormatString</span><span class="sxs-lookup"><span data-stu-id="b3a28-204">subjectNameFormatString</span></span>|<span data-ttu-id="b3a28-205">String</span><span class="sxs-lookup"><span data-stu-id="b3a28-205">String</span></span>|<span data-ttu-id="b3a28-206">Formato personalizado para usar con SubjectNameFormat = personalizada.</span><span class="sxs-lookup"><span data-stu-id="b3a28-206">Custom format to use with SubjectNameFormat = Custom.</span></span> <span data-ttu-id="b3a28-207">Ejemplo: CN = {{EmailAddress}}, E = {{EmailAddress}}, OU = Users de la empresa, O = Contoso Corporation, L = Redmond, ST = WA, C = US</span><span class="sxs-lookup"><span data-stu-id="b3a28-207">Example: CN={{EmailAddress}},E={{EmailAddress}},OU=Enterprise Users,O=Contoso Corporation,L=Redmond,ST=WA,C=US</span></span>|
|<span data-ttu-id="b3a28-208">keyUsage</span><span class="sxs-lookup"><span data-stu-id="b3a28-208">keyUsage</span></span>|[<span data-ttu-id="b3a28-209">keyUsages</span><span class="sxs-lookup"><span data-stu-id="b3a28-209">keyUsages</span></span>](../resources/intune-deviceconfig-keyusages.md)|<span data-ttu-id="b3a28-210">Uso de la clave SCEP.</span><span class="sxs-lookup"><span data-stu-id="b3a28-210">SCEP Key Usage.</span></span> <span data-ttu-id="b3a28-211">Los valores posibles son: `keyEncipherment` y `digitalSignature`.</span><span class="sxs-lookup"><span data-stu-id="b3a28-211">Possible values are: `keyEncipherment`, `digitalSignature`.</span></span>|
|<span data-ttu-id="b3a28-212">keySize</span><span class="sxs-lookup"><span data-stu-id="b3a28-212">keySize</span></span>|[<span data-ttu-id="b3a28-213">keySize</span><span class="sxs-lookup"><span data-stu-id="b3a28-213">keySize</span></span>](../resources/intune-deviceconfig-keysize.md)|<span data-ttu-id="b3a28-214">Tamaño de la clave SCEP.</span><span class="sxs-lookup"><span data-stu-id="b3a28-214">SCEP Key Size.</span></span> <span data-ttu-id="b3a28-215">Los valores posibles son: `size1024` y `size2048`.</span><span class="sxs-lookup"><span data-stu-id="b3a28-215">Possible values are: `size1024`, `size2048`.</span></span>|
|<span data-ttu-id="b3a28-216">hashAlgorithm</span><span class="sxs-lookup"><span data-stu-id="b3a28-216">hashAlgorithm</span></span>|[<span data-ttu-id="b3a28-217">hashAlgorithms</span><span class="sxs-lookup"><span data-stu-id="b3a28-217">hashAlgorithms</span></span>](../resources/intune-deviceconfig-hashalgorithms.md)|<span data-ttu-id="b3a28-218">Algoritmo de Hash SCEP.</span><span class="sxs-lookup"><span data-stu-id="b3a28-218">SCEP Hash Algorithm.</span></span> <span data-ttu-id="b3a28-219">Los valores posibles son: `sha1` y `sha2`.</span><span class="sxs-lookup"><span data-stu-id="b3a28-219">Possible values are: `sha1`, `sha2`.</span></span>|
|<span data-ttu-id="b3a28-220">subjectAlternativeNameFormatString</span><span class="sxs-lookup"><span data-stu-id="b3a28-220">subjectAlternativeNameFormatString</span></span>|<span data-ttu-id="b3a28-221">String</span><span class="sxs-lookup"><span data-stu-id="b3a28-221">String</span></span>|<span data-ttu-id="b3a28-222">Cadena personalizada que define el atributo AAD.</span><span class="sxs-lookup"><span data-stu-id="b3a28-222">Custom String that defines the AAD Attribute.</span></span>|
|<span data-ttu-id="b3a28-223">certificateStore</span><span class="sxs-lookup"><span data-stu-id="b3a28-223">certificateStore</span></span>|[<span data-ttu-id="b3a28-224">certificateStore</span><span class="sxs-lookup"><span data-stu-id="b3a28-224">certificateStore</span></span>](../resources/intune-deviceconfig-certificatestore.md)|<span data-ttu-id="b3a28-225">Certificado del almacén de destino.</span><span class="sxs-lookup"><span data-stu-id="b3a28-225">Target store certificate.</span></span> <span data-ttu-id="b3a28-226">Los valores posibles son: `user` y `machine`.</span><span class="sxs-lookup"><span data-stu-id="b3a28-226">Possible values are: `user`, `machine`.</span></span>|



## <a name="response"></a><span data-ttu-id="b3a28-227">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b3a28-227">Response</span></span>
<span data-ttu-id="b3a28-228">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto actualizado [windows81SCEPCertificateProfile](../resources/intune-deviceconfig-windows81scepcertificateprofile.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b3a28-228">If successful, this method returns a `200 OK` response code and an updated [windows81SCEPCertificateProfile](../resources/intune-deviceconfig-windows81scepcertificateprofile.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="b3a28-229">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b3a28-229">Example</span></span>
### <a name="request"></a><span data-ttu-id="b3a28-230">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b3a28-230">Request</span></span>
<span data-ttu-id="b3a28-231">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b3a28-231">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations/{deviceConfigurationId}
Content-type: application/json
Content-length: 1245

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
  "customSubjectAlternativeNames": [
    {
      "@odata.type": "microsoft.graph.customSubjectAlternativeName",
      "sanType": "emailAddress",
      "name": "Name value"
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
  "certificateStore": "machine"
}
```

### <a name="response"></a><span data-ttu-id="b3a28-232">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b3a28-232">Response</span></span>
<span data-ttu-id="b3a28-p123">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="b3a28-p123">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1423

{
  "@odata.type": "#microsoft.graph.windows81SCEPCertificateProfile",
  "id": "2daf8af2-8af2-2daf-f28a-af2df28aaf2d",
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
  "customSubjectAlternativeNames": [
    {
      "@odata.type": "microsoft.graph.customSubjectAlternativeName",
      "sanType": "emailAddress",
      "name": "Name value"
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
  "certificateStore": "machine"
}
```





