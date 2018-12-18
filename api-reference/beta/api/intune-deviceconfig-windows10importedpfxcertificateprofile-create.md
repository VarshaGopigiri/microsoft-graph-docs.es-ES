---
title: Crear windows10ImportedPFXCertificateProfile
description: Crear un nuevo objeto windows10ImportedPFXCertificateProfile.
author: tfitzmac
ms.openlocfilehash: 896a09c69c3341e60a1e367cdf8521d5371842ac
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27330026"
---
# <a name="create-windows10importedpfxcertificateprofile"></a><span data-ttu-id="48352-103">Crear windows10ImportedPFXCertificateProfile</span><span class="sxs-lookup"><span data-stu-id="48352-103">Create windows10ImportedPFXCertificateProfile</span></span>

> <span data-ttu-id="48352-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="48352-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="48352-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="48352-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="48352-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="48352-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="48352-107">Crear un nuevo objeto [windows10ImportedPFXCertificateProfile](../resources/intune-deviceconfig-windows10importedpfxcertificateprofile.md) .</span><span class="sxs-lookup"><span data-stu-id="48352-107">Create a new [windows10ImportedPFXCertificateProfile](../resources/intune-deviceconfig-windows10importedpfxcertificateprofile.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="48352-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="48352-108">Prerequisites</span></span>
<span data-ttu-id="48352-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="48352-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="48352-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="48352-111">Permission type</span></span>|<span data-ttu-id="48352-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="48352-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="48352-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="48352-113">Delegated (work or school account)</span></span>|<span data-ttu-id="48352-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="48352-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="48352-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="48352-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="48352-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="48352-116">Not supported.</span></span>|
|<span data-ttu-id="48352-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="48352-117">Application</span></span>|<span data-ttu-id="48352-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="48352-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="48352-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="48352-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceConfigurations
POST /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsDomainJoinConfiguration/networkAccessConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="48352-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="48352-120">Request headers</span></span>
|<span data-ttu-id="48352-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="48352-121">Header</span></span>|<span data-ttu-id="48352-122">Valor</span><span class="sxs-lookup"><span data-stu-id="48352-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="48352-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="48352-123">Authorization</span></span>|<span data-ttu-id="48352-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="48352-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="48352-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="48352-125">Accept</span></span>|<span data-ttu-id="48352-126">application/json</span><span class="sxs-lookup"><span data-stu-id="48352-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="48352-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="48352-127">Request body</span></span>
<span data-ttu-id="48352-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto windows10ImportedPFXCertificateProfile.</span><span class="sxs-lookup"><span data-stu-id="48352-128">In the request body, supply a JSON representation for the windows10ImportedPFXCertificateProfile object.</span></span>

<span data-ttu-id="48352-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el windows10ImportedPFXCertificateProfile.</span><span class="sxs-lookup"><span data-stu-id="48352-129">The following table shows the properties that are required when you create the windows10ImportedPFXCertificateProfile.</span></span>

|<span data-ttu-id="48352-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="48352-130">Property</span></span>|<span data-ttu-id="48352-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="48352-131">Type</span></span>|<span data-ttu-id="48352-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="48352-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="48352-133">id</span><span class="sxs-lookup"><span data-stu-id="48352-133">id</span></span>|<span data-ttu-id="48352-134">String</span><span class="sxs-lookup"><span data-stu-id="48352-134">String</span></span>|<span data-ttu-id="48352-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="48352-135">Key of the entity.</span></span> <span data-ttu-id="48352-136">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="48352-136">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="48352-137">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="48352-137">lastModifiedDateTime</span></span>|<span data-ttu-id="48352-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="48352-138">DateTimeOffset</span></span>|<span data-ttu-id="48352-139">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="48352-139">DateTime the object was last modified.</span></span> <span data-ttu-id="48352-140">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="48352-140">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="48352-141">roleScopeTagIds</span><span class="sxs-lookup"><span data-stu-id="48352-141">roleScopeTagIds</span></span>|<span data-ttu-id="48352-142">Colección String</span><span class="sxs-lookup"><span data-stu-id="48352-142">String collection</span></span>|<span data-ttu-id="48352-143">Lista de etiquetas de ámbito para esta instancia de entidad.</span><span class="sxs-lookup"><span data-stu-id="48352-143">List of Scope Tags for this Entity instance.</span></span> <span data-ttu-id="48352-144">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="48352-144">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="48352-145">supportsScopeTags</span><span class="sxs-lookup"><span data-stu-id="48352-145">supportsScopeTags</span></span>|<span data-ttu-id="48352-146">Boolean</span><span class="sxs-lookup"><span data-stu-id="48352-146">Boolean</span></span>|<span data-ttu-id="48352-147">Indica si la configuración del dispositivo subyacente admite la asignación de etiquetas de ámbito.</span><span class="sxs-lookup"><span data-stu-id="48352-147">Indicates whether or not the underlying Device Configuration supports the assignment of scope tags.</span></span> <span data-ttu-id="48352-148">No se permite la asignación a la propiedad ScopeTags cuando este valor es false y entidades no estará visibles para los usuarios con ámbito.</span><span class="sxs-lookup"><span data-stu-id="48352-148">Assigning to the ScopeTags property is not allowed when this value is false and entities will not be visible to scoped users.</span></span> <span data-ttu-id="48352-149">Esto se produce para las directivas de heredado creadas en Silverlight y se puede resolver por eliminar y volver a crear la directiva en el Portal de Azure.</span><span class="sxs-lookup"><span data-stu-id="48352-149">This occurs for Legacy policies created in Silverlight and can be resolved by deleting and recreating the policy in the Azure Portal.</span></span> <span data-ttu-id="48352-150">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="48352-150">This property is read-only.</span></span> <span data-ttu-id="48352-151">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="48352-151">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="48352-152">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="48352-152">createdDateTime</span></span>|<span data-ttu-id="48352-153">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="48352-153">DateTimeOffset</span></span>|<span data-ttu-id="48352-154">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="48352-154">DateTime the object was created.</span></span> <span data-ttu-id="48352-155">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="48352-155">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="48352-156">descripción</span><span class="sxs-lookup"><span data-stu-id="48352-156">description</span></span>|<span data-ttu-id="48352-157">String</span><span class="sxs-lookup"><span data-stu-id="48352-157">String</span></span>|<span data-ttu-id="48352-158">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="48352-158">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="48352-159">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="48352-159">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="48352-160">displayName</span><span class="sxs-lookup"><span data-stu-id="48352-160">displayName</span></span>|<span data-ttu-id="48352-161">String</span><span class="sxs-lookup"><span data-stu-id="48352-161">String</span></span>|<span data-ttu-id="48352-162">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="48352-162">Admin provided name of the device configuration.</span></span> <span data-ttu-id="48352-163">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="48352-163">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="48352-164">version</span><span class="sxs-lookup"><span data-stu-id="48352-164">version</span></span>|<span data-ttu-id="48352-165">Int32</span><span class="sxs-lookup"><span data-stu-id="48352-165">Int32</span></span>|<span data-ttu-id="48352-166">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="48352-166">Version of the device configuration.</span></span> <span data-ttu-id="48352-167">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="48352-167">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="48352-168">renewalThresholdPercentage</span><span class="sxs-lookup"><span data-stu-id="48352-168">renewalThresholdPercentage</span></span>|<span data-ttu-id="48352-169">Int32</span><span class="sxs-lookup"><span data-stu-id="48352-169">Int32</span></span>|<span data-ttu-id="48352-170">Porcentaje de umbral de renovación de certificado.</span><span class="sxs-lookup"><span data-stu-id="48352-170">Certificate renewal threshold percentage.</span></span> <span data-ttu-id="48352-171">Válido valores heredada de 1 a 99 de [windowsCertificateProfileBase](../resources/intune-deviceconfig-windowscertificateprofilebase.md)</span><span class="sxs-lookup"><span data-stu-id="48352-171">Valid values 1 to 99 Inherited from [windowsCertificateProfileBase](../resources/intune-deviceconfig-windowscertificateprofilebase.md)</span></span>|
|<span data-ttu-id="48352-172">keyStorageProvider</span><span class="sxs-lookup"><span data-stu-id="48352-172">keyStorageProvider</span></span>|[<span data-ttu-id="48352-173">keyStorageProviderOption</span><span class="sxs-lookup"><span data-stu-id="48352-173">keyStorageProviderOption</span></span>](../resources/intune-deviceconfig-keystorageprovideroption.md)|<span data-ttu-id="48352-174">Proveedor de almacenamiento de claves (KSP) Inherited desde [windowsCertificateProfileBase](../resources/intune-deviceconfig-windowscertificateprofilebase.md).</span><span class="sxs-lookup"><span data-stu-id="48352-174">Key Storage Provider (KSP) Inherited from [windowsCertificateProfileBase](../resources/intune-deviceconfig-windowscertificateprofilebase.md).</span></span> <span data-ttu-id="48352-175">Los valores posibles son: `useTpmKspOtherwiseUseSoftwareKsp`, `useTpmKspOtherwiseFail`, `usePassportForWorkKspOtherwiseFail` y `useSoftwareKsp`.</span><span class="sxs-lookup"><span data-stu-id="48352-175">Possible values are: `useTpmKspOtherwiseUseSoftwareKsp`, `useTpmKspOtherwiseFail`, `usePassportForWorkKspOtherwiseFail`, `useSoftwareKsp`.</span></span>|
|<span data-ttu-id="48352-176">subjectNameFormat</span><span class="sxs-lookup"><span data-stu-id="48352-176">subjectNameFormat</span></span>|[<span data-ttu-id="48352-177">subjectNameFormat</span><span class="sxs-lookup"><span data-stu-id="48352-177">subjectNameFormat</span></span>](../resources/intune-deviceconfig-subjectnameformat.md)|<span data-ttu-id="48352-178">Certificado heredado de formato de nombre de sujeto de [windowsCertificateProfileBase](../resources/intune-deviceconfig-windowscertificateprofilebase.md).</span><span class="sxs-lookup"><span data-stu-id="48352-178">Certificate Subject Name Format Inherited from [windowsCertificateProfileBase](../resources/intune-deviceconfig-windowscertificateprofilebase.md).</span></span> <span data-ttu-id="48352-179">Los valores posibles son: `commonName`, `commonNameIncludingEmail`, `commonNameAsEmail`, `custom`, `commonNameAsIMEI`, `commonNameAsSerialNumber`, `commonNameAsAadDeviceId`, `commonNameAsIntuneDeviceId` y `commonNameAsDurableDeviceId`.</span><span class="sxs-lookup"><span data-stu-id="48352-179">Possible values are: `commonName`, `commonNameIncludingEmail`, `commonNameAsEmail`, `custom`, `commonNameAsIMEI`, `commonNameAsSerialNumber`, `commonNameAsAadDeviceId`, `commonNameAsIntuneDeviceId`, `commonNameAsDurableDeviceId`.</span></span>|
|<span data-ttu-id="48352-180">subjectAlternativeNameType</span><span class="sxs-lookup"><span data-stu-id="48352-180">subjectAlternativeNameType</span></span>|[<span data-ttu-id="48352-181">subjectAlternativeNameType</span><span class="sxs-lookup"><span data-stu-id="48352-181">subjectAlternativeNameType</span></span>](../resources/intune-deviceconfig-subjectalternativenametype.md)|<span data-ttu-id="48352-182">Certificado asunto alternativa nombre tipo hereda de [windowsCertificateProfileBase](../resources/intune-deviceconfig-windowscertificateprofilebase.md).</span><span class="sxs-lookup"><span data-stu-id="48352-182">Certificate Subject Alternative Name Type Inherited from [windowsCertificateProfileBase](../resources/intune-deviceconfig-windowscertificateprofilebase.md).</span></span> <span data-ttu-id="48352-183">Los valores posibles son: `none`, `emailAddress`, `userPrincipalName`, `customAzureADAttribute` y `domainNameService`.</span><span class="sxs-lookup"><span data-stu-id="48352-183">Possible values are: `none`, `emailAddress`, `userPrincipalName`, `customAzureADAttribute`, `domainNameService`.</span></span>|
|<span data-ttu-id="48352-184">certificateValidityPeriodValue</span><span class="sxs-lookup"><span data-stu-id="48352-184">certificateValidityPeriodValue</span></span>|<span data-ttu-id="48352-185">Int32</span><span class="sxs-lookup"><span data-stu-id="48352-185">Int32</span></span>|<span data-ttu-id="48352-186">Valor para el heredado de período de validez de certificado de [windowsCertificateProfileBase](../resources/intune-deviceconfig-windowscertificateprofilebase.md)</span><span class="sxs-lookup"><span data-stu-id="48352-186">Value for the Certificate Validity Period Inherited from [windowsCertificateProfileBase](../resources/intune-deviceconfig-windowscertificateprofilebase.md)</span></span>|
|<span data-ttu-id="48352-187">certificateValidityPeriodScale</span><span class="sxs-lookup"><span data-stu-id="48352-187">certificateValidityPeriodScale</span></span>|[<span data-ttu-id="48352-188">certificateValidityPeriodScale</span><span class="sxs-lookup"><span data-stu-id="48352-188">certificateValidityPeriodScale</span></span>](../resources/intune-deviceconfig-certificatevalidityperiodscale.md)|<span data-ttu-id="48352-189">Escala para la heredada de período de validez de certificado de [windowsCertificateProfileBase](../resources/intune-deviceconfig-windowscertificateprofilebase.md).</span><span class="sxs-lookup"><span data-stu-id="48352-189">Scale for the Certificate Validity Period Inherited from [windowsCertificateProfileBase](../resources/intune-deviceconfig-windowscertificateprofilebase.md).</span></span> <span data-ttu-id="48352-190">Los valores posibles son: `days`, `months` y `years`.</span><span class="sxs-lookup"><span data-stu-id="48352-190">Possible values are: `days`, `months`, `years`.</span></span>|
|<span data-ttu-id="48352-191">intendedPurpose</span><span class="sxs-lookup"><span data-stu-id="48352-191">intendedPurpose</span></span>|[<span data-ttu-id="48352-192">intendedPurpose</span><span class="sxs-lookup"><span data-stu-id="48352-192">intendedPurpose</span></span>](../resources/intune-deviceconfig-intendedpurpose.md)|<span data-ttu-id="48352-193">Todavía no está documentada.</span><span class="sxs-lookup"><span data-stu-id="48352-193">Not yet documented.</span></span> <span data-ttu-id="48352-194">Los valores posibles son: `unassigned`, `smimeEncryption`, `smimeSigning`, `vpn` y `wifi`.</span><span class="sxs-lookup"><span data-stu-id="48352-194">Possible values are: `unassigned`, `smimeEncryption`, `smimeSigning`, `vpn`, `wifi`.</span></span>|



## <a name="response"></a><span data-ttu-id="48352-195">Respuesta</span><span class="sxs-lookup"><span data-stu-id="48352-195">Response</span></span>
<span data-ttu-id="48352-196">Si tiene éxito, este método devuelve una `201 Created` código de respuesta y un objeto [windows10ImportedPFXCertificateProfile](../resources/intune-deviceconfig-windows10importedpfxcertificateprofile.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="48352-196">If successful, this method returns a `201 Created` response code and a [windows10ImportedPFXCertificateProfile](../resources/intune-deviceconfig-windows10importedpfxcertificateprofile.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="48352-197">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="48352-197">Example</span></span>
### <a name="request"></a><span data-ttu-id="48352-198">Solicitud</span><span class="sxs-lookup"><span data-stu-id="48352-198">Request</span></span>
<span data-ttu-id="48352-199">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="48352-199">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations
Content-type: application/json
Content-length: 650

{
  "@odata.type": "#microsoft.graph.windows10ImportedPFXCertificateProfile",
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
  "intendedPurpose": "smimeEncryption"
}
```

### <a name="response"></a><span data-ttu-id="48352-200">Respuesta</span><span class="sxs-lookup"><span data-stu-id="48352-200">Response</span></span>
<span data-ttu-id="48352-p117">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="48352-p117">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 758

{
  "@odata.type": "#microsoft.graph.windows10ImportedPFXCertificateProfile",
  "id": "b582514b-514b-b582-4b51-82b54b5182b5",
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
  "intendedPurpose": "smimeEncryption"
}
```





