---
title: Actualizar androidForWorkImportedPFXCertificateProfile
description: Actualizar las propiedades de un objeto androidForWorkImportedPFXCertificateProfile.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 4d5830d811e14131ef30fcffeef559efe34d1446
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27990932"
---
# <a name="update-androidforworkimportedpfxcertificateprofile"></a><span data-ttu-id="6211f-103">Actualizar androidForWorkImportedPFXCertificateProfile</span><span class="sxs-lookup"><span data-stu-id="6211f-103">Update androidForWorkImportedPFXCertificateProfile</span></span>

> <span data-ttu-id="6211f-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="6211f-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="6211f-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="6211f-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="6211f-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="6211f-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="6211f-107">Actualizar las propiedades de un objeto [androidForWorkImportedPFXCertificateProfile](../resources/intune-deviceconfig-androidforworkimportedpfxcertificateprofile.md) .</span><span class="sxs-lookup"><span data-stu-id="6211f-107">Update the properties of a [androidForWorkImportedPFXCertificateProfile](../resources/intune-deviceconfig-androidforworkimportedpfxcertificateprofile.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="6211f-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="6211f-108">Prerequisites</span></span>
<span data-ttu-id="6211f-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="6211f-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="6211f-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="6211f-111">Permission type</span></span>|<span data-ttu-id="6211f-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="6211f-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="6211f-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="6211f-113">Delegated (work or school account)</span></span>|<span data-ttu-id="6211f-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="6211f-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="6211f-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="6211f-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="6211f-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6211f-116">Not supported.</span></span>|
|<span data-ttu-id="6211f-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="6211f-117">Application</span></span>|<span data-ttu-id="6211f-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6211f-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="6211f-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="6211f-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/groupAssignments/{deviceConfigurationGroupAssignmentId}/deviceConfiguration
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsDomainJoinConfiguration/networkAccessConfigurations/{deviceConfigurationId}
```

## <a name="request-headers"></a><span data-ttu-id="6211f-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="6211f-120">Request headers</span></span>
|<span data-ttu-id="6211f-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6211f-121">Header</span></span>|<span data-ttu-id="6211f-122">Valor</span><span class="sxs-lookup"><span data-stu-id="6211f-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="6211f-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="6211f-123">Authorization</span></span>|<span data-ttu-id="6211f-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="6211f-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="6211f-125">Accept</span><span class="sxs-lookup"><span data-stu-id="6211f-125">Accept</span></span>|<span data-ttu-id="6211f-126">application/json</span><span class="sxs-lookup"><span data-stu-id="6211f-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="6211f-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="6211f-127">Request body</span></span>
<span data-ttu-id="6211f-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto [androidForWorkImportedPFXCertificateProfile](../resources/intune-deviceconfig-androidforworkimportedpfxcertificateprofile.md) .</span><span class="sxs-lookup"><span data-stu-id="6211f-128">In the request body, supply a JSON representation for the [androidForWorkImportedPFXCertificateProfile](../resources/intune-deviceconfig-androidforworkimportedpfxcertificateprofile.md) object.</span></span>

<span data-ttu-id="6211f-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el [androidForWorkImportedPFXCertificateProfile](../resources/intune-deviceconfig-androidforworkimportedpfxcertificateprofile.md).</span><span class="sxs-lookup"><span data-stu-id="6211f-129">The following table shows the properties that are required when you create the [androidForWorkImportedPFXCertificateProfile](../resources/intune-deviceconfig-androidforworkimportedpfxcertificateprofile.md).</span></span>

|<span data-ttu-id="6211f-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="6211f-130">Property</span></span>|<span data-ttu-id="6211f-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="6211f-131">Type</span></span>|<span data-ttu-id="6211f-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="6211f-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="6211f-133">id</span><span class="sxs-lookup"><span data-stu-id="6211f-133">id</span></span>|<span data-ttu-id="6211f-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="6211f-134">String</span></span>|<span data-ttu-id="6211f-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="6211f-135">Key of the entity.</span></span> <span data-ttu-id="6211f-136">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="6211f-136">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="6211f-137">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="6211f-137">lastModifiedDateTime</span></span>|<span data-ttu-id="6211f-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="6211f-138">DateTimeOffset</span></span>|<span data-ttu-id="6211f-139">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="6211f-139">DateTime the object was last modified.</span></span> <span data-ttu-id="6211f-140">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="6211f-140">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="6211f-141">roleScopeTagIds</span><span class="sxs-lookup"><span data-stu-id="6211f-141">roleScopeTagIds</span></span>|<span data-ttu-id="6211f-142">Colección String</span><span class="sxs-lookup"><span data-stu-id="6211f-142">String collection</span></span>|<span data-ttu-id="6211f-143">Lista de etiquetas de ámbito para esta instancia de entidad.</span><span class="sxs-lookup"><span data-stu-id="6211f-143">List of Scope Tags for this Entity instance.</span></span> <span data-ttu-id="6211f-144">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="6211f-144">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="6211f-145">supportsScopeTags</span><span class="sxs-lookup"><span data-stu-id="6211f-145">supportsScopeTags</span></span>|<span data-ttu-id="6211f-146">Booleano</span><span class="sxs-lookup"><span data-stu-id="6211f-146">Boolean</span></span>|<span data-ttu-id="6211f-147">Indica si la configuración del dispositivo subyacente admite la asignación de etiquetas de ámbito.</span><span class="sxs-lookup"><span data-stu-id="6211f-147">Indicates whether or not the underlying Device Configuration supports the assignment of scope tags.</span></span> <span data-ttu-id="6211f-148">No se permite la asignación a la propiedad ScopeTags cuando este valor es false y entidades no estará visibles para los usuarios con ámbito.</span><span class="sxs-lookup"><span data-stu-id="6211f-148">Assigning to the ScopeTags property is not allowed when this value is false and entities will not be visible to scoped users.</span></span> <span data-ttu-id="6211f-149">Esto se produce para las directivas de heredado creadas en Silverlight y se puede resolver por eliminar y volver a crear la directiva en el Portal de Azure.</span><span class="sxs-lookup"><span data-stu-id="6211f-149">This occurs for Legacy policies created in Silverlight and can be resolved by deleting and recreating the policy in the Azure Portal.</span></span> <span data-ttu-id="6211f-150">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="6211f-150">This property is read-only.</span></span> <span data-ttu-id="6211f-151">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="6211f-151">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="6211f-152">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="6211f-152">createdDateTime</span></span>|<span data-ttu-id="6211f-153">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="6211f-153">DateTimeOffset</span></span>|<span data-ttu-id="6211f-154">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="6211f-154">DateTime the object was created.</span></span> <span data-ttu-id="6211f-155">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="6211f-155">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="6211f-156">descripción</span><span class="sxs-lookup"><span data-stu-id="6211f-156">description</span></span>|<span data-ttu-id="6211f-157">Cadena</span><span class="sxs-lookup"><span data-stu-id="6211f-157">String</span></span>|<span data-ttu-id="6211f-158">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6211f-158">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="6211f-159">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="6211f-159">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="6211f-160">displayName</span><span class="sxs-lookup"><span data-stu-id="6211f-160">displayName</span></span>|<span data-ttu-id="6211f-161">Cadena</span><span class="sxs-lookup"><span data-stu-id="6211f-161">String</span></span>|<span data-ttu-id="6211f-162">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6211f-162">Admin provided name of the device configuration.</span></span> <span data-ttu-id="6211f-163">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="6211f-163">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="6211f-164">version</span><span class="sxs-lookup"><span data-stu-id="6211f-164">version</span></span>|<span data-ttu-id="6211f-165">Int32</span><span class="sxs-lookup"><span data-stu-id="6211f-165">Int32</span></span>|<span data-ttu-id="6211f-166">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6211f-166">Version of the device configuration.</span></span> <span data-ttu-id="6211f-167">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="6211f-167">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="6211f-168">renewalThresholdPercentage</span><span class="sxs-lookup"><span data-stu-id="6211f-168">renewalThresholdPercentage</span></span>|<span data-ttu-id="6211f-169">Int32</span><span class="sxs-lookup"><span data-stu-id="6211f-169">Int32</span></span>|<span data-ttu-id="6211f-170">Porcentaje de umbral de renovación de certificado.</span><span class="sxs-lookup"><span data-stu-id="6211f-170">Certificate renewal threshold percentage.</span></span> <span data-ttu-id="6211f-171">Válido valores heredada de 1 a 99 de [androidCertificateProfileBase](../resources/intune-deviceconfig-androidcertificateprofilebase.md)</span><span class="sxs-lookup"><span data-stu-id="6211f-171">Valid values 1 to 99 Inherited from [androidCertificateProfileBase](../resources/intune-deviceconfig-androidcertificateprofilebase.md)</span></span>|
|<span data-ttu-id="6211f-172">subjectNameFormat</span><span class="sxs-lookup"><span data-stu-id="6211f-172">subjectNameFormat</span></span>|[<span data-ttu-id="6211f-173">subjectNameFormat</span><span class="sxs-lookup"><span data-stu-id="6211f-173">subjectNameFormat</span></span>](../resources/intune-deviceconfig-subjectnameformat.md)|<span data-ttu-id="6211f-174">Formato de nombre de sujeto de certificado.</span><span class="sxs-lookup"><span data-stu-id="6211f-174">Certificate Subject Name Format.</span></span> <span data-ttu-id="6211f-175">Se hereda de [androidCertificateProfileBase](../resources/intune-deviceconfig-androidcertificateprofilebase.md).</span><span class="sxs-lookup"><span data-stu-id="6211f-175">Inherited from [androidCertificateProfileBase](../resources/intune-deviceconfig-androidcertificateprofilebase.md).</span></span> <span data-ttu-id="6211f-176">Los valores posibles son: `commonName`, `commonNameIncludingEmail`, `commonNameAsEmail`, `custom`, `commonNameAsIMEI`, `commonNameAsSerialNumber`, `commonNameAsAadDeviceId`, `commonNameAsIntuneDeviceId` y `commonNameAsDurableDeviceId`.</span><span class="sxs-lookup"><span data-stu-id="6211f-176">Possible values are: `commonName`, `commonNameIncludingEmail`, `commonNameAsEmail`, `custom`, `commonNameAsIMEI`, `commonNameAsSerialNumber`, `commonNameAsAadDeviceId`, `commonNameAsIntuneDeviceId`, `commonNameAsDurableDeviceId`.</span></span>|
|<span data-ttu-id="6211f-177">subjectAlternativeNameType</span><span class="sxs-lookup"><span data-stu-id="6211f-177">subjectAlternativeNameType</span></span>|[<span data-ttu-id="6211f-178">subjectAlternativeNameType</span><span class="sxs-lookup"><span data-stu-id="6211f-178">subjectAlternativeNameType</span></span>](../resources/intune-deviceconfig-subjectalternativenametype.md)|<span data-ttu-id="6211f-179">Tipo de nombre alternativo de sujeto de certificado.</span><span class="sxs-lookup"><span data-stu-id="6211f-179">Certificate Subject Alternative Name Type.</span></span> <span data-ttu-id="6211f-180">Se hereda de [androidCertificateProfileBase](../resources/intune-deviceconfig-androidcertificateprofilebase.md).</span><span class="sxs-lookup"><span data-stu-id="6211f-180">Inherited from [androidCertificateProfileBase](../resources/intune-deviceconfig-androidcertificateprofilebase.md).</span></span> <span data-ttu-id="6211f-181">Los valores posibles son: `none`, `emailAddress`, `userPrincipalName`, `customAzureADAttribute` y `domainNameService`.</span><span class="sxs-lookup"><span data-stu-id="6211f-181">Possible values are: `none`, `emailAddress`, `userPrincipalName`, `customAzureADAttribute`, `domainNameService`.</span></span>|
|<span data-ttu-id="6211f-182">certificateValidityPeriodValue</span><span class="sxs-lookup"><span data-stu-id="6211f-182">certificateValidityPeriodValue</span></span>|<span data-ttu-id="6211f-183">Int32</span><span class="sxs-lookup"><span data-stu-id="6211f-183">Int32</span></span>|<span data-ttu-id="6211f-184">Valor para el período de validez del certificado.</span><span class="sxs-lookup"><span data-stu-id="6211f-184">Value for the Certificate Validity Period.</span></span> <span data-ttu-id="6211f-185">Se hereda de [androidCertificateProfileBase](../resources/intune-deviceconfig-androidcertificateprofilebase.md)</span><span class="sxs-lookup"><span data-stu-id="6211f-185">Inherited from [androidCertificateProfileBase](../resources/intune-deviceconfig-androidcertificateprofilebase.md)</span></span>|
|<span data-ttu-id="6211f-186">certificateValidityPeriodScale</span><span class="sxs-lookup"><span data-stu-id="6211f-186">certificateValidityPeriodScale</span></span>|[<span data-ttu-id="6211f-187">certificateValidityPeriodScale</span><span class="sxs-lookup"><span data-stu-id="6211f-187">certificateValidityPeriodScale</span></span>](../resources/intune-deviceconfig-certificatevalidityperiodscale.md)|<span data-ttu-id="6211f-188">Escala para el período de validez del certificado.</span><span class="sxs-lookup"><span data-stu-id="6211f-188">Scale for the Certificate Validity Period.</span></span> <span data-ttu-id="6211f-189">Se hereda de [androidCertificateProfileBase](../resources/intune-deviceconfig-androidcertificateprofilebase.md).</span><span class="sxs-lookup"><span data-stu-id="6211f-189">Inherited from [androidCertificateProfileBase](../resources/intune-deviceconfig-androidcertificateprofilebase.md).</span></span> <span data-ttu-id="6211f-190">Los valores posibles son: `days`, `months` y `years`.</span><span class="sxs-lookup"><span data-stu-id="6211f-190">Possible values are: `days`, `months`, `years`.</span></span>|
|<span data-ttu-id="6211f-191">extendedKeyUsages</span><span class="sxs-lookup"><span data-stu-id="6211f-191">extendedKeyUsages</span></span>|<span data-ttu-id="6211f-192">colección de [ExtendeKeyUsage](../resources/intune-deviceconfig-extendedkeyusage.md)</span><span class="sxs-lookup"><span data-stu-id="6211f-192">[extendedKeyUsage](../resources/intune-deviceconfig-extendedkeyusage.md) collection</span></span>|<span data-ttu-id="6211f-193">Configuración de clave (EKU) extendida.</span><span class="sxs-lookup"><span data-stu-id="6211f-193">Extended Key Usage (EKU) settings.</span></span> <span data-ttu-id="6211f-194">Esta colección puede contener un máximo de 500 elementos.</span><span class="sxs-lookup"><span data-stu-id="6211f-194">This collection can contain a maximum of 500 elements.</span></span> <span data-ttu-id="6211f-195">Se hereda de [androidCertificateProfileBase](../resources/intune-deviceconfig-androidcertificateprofilebase.md)</span><span class="sxs-lookup"><span data-stu-id="6211f-195">Inherited from [androidCertificateProfileBase](../resources/intune-deviceconfig-androidcertificateprofilebase.md)</span></span>|
|<span data-ttu-id="6211f-196">intendedPurpose</span><span class="sxs-lookup"><span data-stu-id="6211f-196">intendedPurpose</span></span>|[<span data-ttu-id="6211f-197">intendedPurpose</span><span class="sxs-lookup"><span data-stu-id="6211f-197">intendedPurpose</span></span>](../resources/intune-deviceconfig-intendedpurpose.md)|<span data-ttu-id="6211f-198">Todavía no está documentada.</span><span class="sxs-lookup"><span data-stu-id="6211f-198">Not yet documented.</span></span> <span data-ttu-id="6211f-199">Los valores posibles son: `unassigned`, `smimeEncryption`, `smimeSigning`, `vpn` y `wifi`.</span><span class="sxs-lookup"><span data-stu-id="6211f-199">Possible values are: `unassigned`, `smimeEncryption`, `smimeSigning`, `vpn`, `wifi`.</span></span>|



## <a name="response"></a><span data-ttu-id="6211f-200">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6211f-200">Response</span></span>
<span data-ttu-id="6211f-201">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto actualizado [androidForWorkImportedPFXCertificateProfile](../resources/intune-deviceconfig-androidforworkimportedpfxcertificateprofile.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6211f-201">If successful, this method returns a `200 OK` response code and an updated [androidForWorkImportedPFXCertificateProfile](../resources/intune-deviceconfig-androidforworkimportedpfxcertificateprofile.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="6211f-202">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6211f-202">Example</span></span>
### <a name="request"></a><span data-ttu-id="6211f-203">Solicitud</span><span class="sxs-lookup"><span data-stu-id="6211f-203">Request</span></span>
<span data-ttu-id="6211f-204">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6211f-204">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations/{deviceConfigurationId}
Content-type: application/json
Content-length: 708

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
  "intendedPurpose": "smimeEncryption"
}
```

### <a name="response"></a><span data-ttu-id="6211f-205">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6211f-205">Response</span></span>
<span data-ttu-id="6211f-p118">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="6211f-p118">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 898

{
  "@odata.type": "#microsoft.graph.androidForWorkImportedPFXCertificateProfile",
  "id": "a0bfd7bc-d7bc-a0bf-bcd7-bfa0bcd7bfa0",
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
  "intendedPurpose": "smimeEncryption"
}
```





