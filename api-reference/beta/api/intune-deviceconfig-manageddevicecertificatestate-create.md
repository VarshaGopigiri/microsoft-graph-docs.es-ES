---
title: Crear managedDeviceCertificateState
description: Crear un nuevo objeto managedDeviceCertificateState.
author: tfitzmac
ms.openlocfilehash: 22b8a0db82e86b9136ee997a821223afe608b51a
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27305960"
---
# <a name="create-manageddevicecertificatestate"></a><span data-ttu-id="42eba-103">Crear managedDeviceCertificateState</span><span class="sxs-lookup"><span data-stu-id="42eba-103">Create managedDeviceCertificateState</span></span>

> <span data-ttu-id="42eba-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="42eba-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="42eba-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="42eba-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="42eba-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="42eba-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="42eba-107">Crear un nuevo objeto [managedDeviceCertificateState](../resources/intune-deviceconfig-manageddevicecertificatestate.md) .</span><span class="sxs-lookup"><span data-stu-id="42eba-107">Create a new [managedDeviceCertificateState](../resources/intune-deviceconfig-manageddevicecertificatestate.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="42eba-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="42eba-108">Prerequisites</span></span>
<span data-ttu-id="42eba-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="42eba-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="42eba-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="42eba-111">Permission type</span></span>|<span data-ttu-id="42eba-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="42eba-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="42eba-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="42eba-113">Delegated (work or school account)</span></span>|<span data-ttu-id="42eba-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="42eba-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="42eba-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="42eba-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="42eba-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="42eba-116">Not supported.</span></span>|
|<span data-ttu-id="42eba-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="42eba-117">Application</span></span>|<span data-ttu-id="42eba-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="42eba-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="42eba-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="42eba-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.iosPkcsCertificateProfile/managedDeviceCertificateStates
POST /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.iosScepCertificateProfile/managedDeviceCertificateStates
POST /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.macOSScepCertificateProfile/managedDeviceCertificateStates
POST /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.androidPkcsCertificateProfile/managedDeviceCertificateStates
POST /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.androidScepCertificateProfile/managedDeviceCertificateStates
POST /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.iosImportedPFXCertificateProfile/managedDeviceCertificateStates
POST /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.macOSImportedPFXCertificateProfile/managedDeviceCertificateStates
POST /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.androidImportedPFXCertificateProfile/managedDeviceCertificateStates
POST /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.androidWorkProfileScepCertificateProfile/managedDeviceCertificateStates
POST /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.androidForWorkImportedPFXCertificateProfile/managedDeviceCertificateStates
POST /deviceManagement/deviceConfigurations/{deviceConfigurationId}/identityCertificate/microsoft.graph.androidForWorkPkcsCertificateProfile/managedDeviceCertificateStates
POST /deviceManagement/deviceConfigurations/{deviceConfigurationId}/identityCertificate/microsoft.graph.androidForWorkScepCertificateProfile/managedDeviceCertificateStates
POST /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsPhone81VpnConfiguration/identityCertificate/microsoft.graph.windowsPhone81SCEPCertificateProfile/managedDeviceCertificateStates
POST /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsWifiEnterpriseEAPConfiguration/identityCertificateForClientAuthentication/microsoft.graph.windows10PkcsCertificateProfile/managedDeviceCertificateStates
POST /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsWifiEnterpriseEAPConfiguration/identityCertificateForClientAuthentication/microsoft.graph.windows81SCEPCertificateProfile/managedDeviceCertificateStates
POST /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsWifiEnterpriseEAPConfiguration/identityCertificateForClientAuthentication/microsoft.graph.windows10ImportedPFXCertificateProfile/managedDeviceCertificateStates
POST /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsWifiEnterpriseEAPConfiguration/identityCertificateForClientAuthentication/microsoft.graph.windowsPhone81ImportedPFXCertificateProfile/managedDeviceCertificateStates
```

## <a name="request-headers"></a><span data-ttu-id="42eba-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="42eba-120">Request headers</span></span>
|<span data-ttu-id="42eba-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="42eba-121">Header</span></span>|<span data-ttu-id="42eba-122">Valor</span><span class="sxs-lookup"><span data-stu-id="42eba-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="42eba-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="42eba-123">Authorization</span></span>|<span data-ttu-id="42eba-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="42eba-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="42eba-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="42eba-125">Accept</span></span>|<span data-ttu-id="42eba-126">application/json</span><span class="sxs-lookup"><span data-stu-id="42eba-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="42eba-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="42eba-127">Request body</span></span>
<span data-ttu-id="42eba-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto managedDeviceCertificateState.</span><span class="sxs-lookup"><span data-stu-id="42eba-128">In the request body, supply a JSON representation for the managedDeviceCertificateState object.</span></span>

<span data-ttu-id="42eba-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el managedDeviceCertificateState.</span><span class="sxs-lookup"><span data-stu-id="42eba-129">The following table shows the properties that are required when you create the managedDeviceCertificateState.</span></span>

|<span data-ttu-id="42eba-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="42eba-130">Property</span></span>|<span data-ttu-id="42eba-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="42eba-131">Type</span></span>|<span data-ttu-id="42eba-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="42eba-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="42eba-133">id</span><span class="sxs-lookup"><span data-stu-id="42eba-133">id</span></span>|<span data-ttu-id="42eba-134">String</span><span class="sxs-lookup"><span data-stu-id="42eba-134">String</span></span>|<span data-ttu-id="42eba-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="42eba-135">Key of the entity.</span></span>|
|<span data-ttu-id="42eba-136">devicePlatform</span><span class="sxs-lookup"><span data-stu-id="42eba-136">devicePlatform</span></span>|[<span data-ttu-id="42eba-137">devicePlatformType</span><span class="sxs-lookup"><span data-stu-id="42eba-137">devicePlatformType</span></span>](../resources/intune-shared-deviceplatformtype.md)|<span data-ttu-id="42eba-138">Plataforma de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="42eba-138">Device platform.</span></span> <span data-ttu-id="42eba-139">Los valores posibles son: `android`, `androidForWork`, `iOS`, `macOS`, `windowsPhone81`, `windows81AndLater`, `windows10AndLater` y `androidWorkProfile`.</span><span class="sxs-lookup"><span data-stu-id="42eba-139">Possible values are: `android`, `androidForWork`, `iOS`, `macOS`, `windowsPhone81`, `windows81AndLater`, `windows10AndLater`, `androidWorkProfile`.</span></span>|
|<span data-ttu-id="42eba-140">certificateKeyUsage</span><span class="sxs-lookup"><span data-stu-id="42eba-140">certificateKeyUsage</span></span>|[<span data-ttu-id="42eba-141">keyUsages</span><span class="sxs-lookup"><span data-stu-id="42eba-141">keyUsages</span></span>](../resources/intune-deviceconfig-keyusages.md)|<span data-ttu-id="42eba-142">Uso de la clave.</span><span class="sxs-lookup"><span data-stu-id="42eba-142">Key usage.</span></span> <span data-ttu-id="42eba-143">Los valores posibles son: `keyEncipherment` y `digitalSignature`.</span><span class="sxs-lookup"><span data-stu-id="42eba-143">Possible values are: `keyEncipherment`, `digitalSignature`.</span></span>|
|<span data-ttu-id="42eba-144">certificateValidityPeriodUnits</span><span class="sxs-lookup"><span data-stu-id="42eba-144">certificateValidityPeriodUnits</span></span>|[<span data-ttu-id="42eba-145">certificateValidityPeriodScale</span><span class="sxs-lookup"><span data-stu-id="42eba-145">certificateValidityPeriodScale</span></span>](../resources/intune-deviceconfig-certificatevalidityperiodscale.md)|<span data-ttu-id="42eba-146">Unidades del período de validez.</span><span class="sxs-lookup"><span data-stu-id="42eba-146">Validity period units.</span></span> <span data-ttu-id="42eba-147">Los valores posibles son: `days`, `months` y `years`.</span><span class="sxs-lookup"><span data-stu-id="42eba-147">Possible values are: `days`, `months`, `years`.</span></span>|
|<span data-ttu-id="42eba-148">certificateIssuanceState</span><span class="sxs-lookup"><span data-stu-id="42eba-148">certificateIssuanceState</span></span>|[<span data-ttu-id="42eba-149">certificateIssuanceStates</span><span class="sxs-lookup"><span data-stu-id="42eba-149">certificateIssuanceStates</span></span>](../resources/intune-deviceconfig-certificateissuancestates.md)|<span data-ttu-id="42eba-150">Estado de emisión.</span><span class="sxs-lookup"><span data-stu-id="42eba-150">Issuance State.</span></span> <span data-ttu-id="42eba-151">Los valores posibles son: `unknown`, `challengeIssued`, `challengeIssueFailed`, `requestCreationFailed`, `requestSubmitFailed`, `challengeValidationSucceeded`, `challengeValidationFailed`, `issueFailed`, `issuePending`, `issued`, `responseProcessingFailed`, `responsePending`, `enrollmentSucceeded`, `enrollmentNotNeeded`, `revoked`, `removedFromCollection`, `renewVerified`, `installFailed`, `installed` , `deleteFailed`, `deleted`, `renewalRequested`, `requested`.</span><span class="sxs-lookup"><span data-stu-id="42eba-151">Possible values are: `unknown`, `challengeIssued`, `challengeIssueFailed`, `requestCreationFailed`, `requestSubmitFailed`, `challengeValidationSucceeded`, `challengeValidationFailed`, `issueFailed`, `issuePending`, `issued`, `responseProcessingFailed`, `responsePending`, `enrollmentSucceeded`, `enrollmentNotNeeded`, `revoked`, `removedFromCollection`, `renewVerified`, `installFailed`, `installed`, `deleteFailed`, `deleted`, `renewalRequested`, `requested`.</span></span>|
|<span data-ttu-id="42eba-152">certificateKeyStorageProvider</span><span class="sxs-lookup"><span data-stu-id="42eba-152">certificateKeyStorageProvider</span></span>|[<span data-ttu-id="42eba-153">keyStorageProviderOption</span><span class="sxs-lookup"><span data-stu-id="42eba-153">keyStorageProviderOption</span></span>](../resources/intune-deviceconfig-keystorageprovideroption.md)|<span data-ttu-id="42eba-154">Proveedor de almacenamiento de claves.</span><span class="sxs-lookup"><span data-stu-id="42eba-154">Key Storage Provider.</span></span> <span data-ttu-id="42eba-155">Los valores posibles son: `useTpmKspOtherwiseUseSoftwareKsp`, `useTpmKspOtherwiseFail`, `usePassportForWorkKspOtherwiseFail` y `useSoftwareKsp`.</span><span class="sxs-lookup"><span data-stu-id="42eba-155">Possible values are: `useTpmKspOtherwiseUseSoftwareKsp`, `useTpmKspOtherwiseFail`, `usePassportForWorkKspOtherwiseFail`, `useSoftwareKsp`.</span></span>|
|<span data-ttu-id="42eba-156">certificateSubjectNameFormat</span><span class="sxs-lookup"><span data-stu-id="42eba-156">certificateSubjectNameFormat</span></span>|[<span data-ttu-id="42eba-157">subjectNameFormat</span><span class="sxs-lookup"><span data-stu-id="42eba-157">subjectNameFormat</span></span>](../resources/intune-deviceconfig-subjectnameformat.md)|<span data-ttu-id="42eba-158">Formato de nombre de sujeto.</span><span class="sxs-lookup"><span data-stu-id="42eba-158">Subject name format.</span></span> <span data-ttu-id="42eba-159">Los valores posibles son: `commonName`, `commonNameIncludingEmail`, `commonNameAsEmail`, `custom`, `commonNameAsIMEI`, `commonNameAsSerialNumber`, `commonNameAsAadDeviceId`, `commonNameAsIntuneDeviceId` y `commonNameAsDurableDeviceId`.</span><span class="sxs-lookup"><span data-stu-id="42eba-159">Possible values are: `commonName`, `commonNameIncludingEmail`, `commonNameAsEmail`, `custom`, `commonNameAsIMEI`, `commonNameAsSerialNumber`, `commonNameAsAadDeviceId`, `commonNameAsIntuneDeviceId`, `commonNameAsDurableDeviceId`.</span></span>|
|<span data-ttu-id="42eba-160">certificateSubjectAlternativeNameFormat</span><span class="sxs-lookup"><span data-stu-id="42eba-160">certificateSubjectAlternativeNameFormat</span></span>|[<span data-ttu-id="42eba-161">subjectAlternativeNameType</span><span class="sxs-lookup"><span data-stu-id="42eba-161">subjectAlternativeNameType</span></span>](../resources/intune-deviceconfig-subjectalternativenametype.md)|<span data-ttu-id="42eba-162">Formato de nombre alternativo de sujeto.</span><span class="sxs-lookup"><span data-stu-id="42eba-162">Subject alternative name format.</span></span> <span data-ttu-id="42eba-163">Los valores posibles son: `none`, `emailAddress`, `userPrincipalName`, `customAzureADAttribute` y `domainNameService`.</span><span class="sxs-lookup"><span data-stu-id="42eba-163">Possible values are: `none`, `emailAddress`, `userPrincipalName`, `customAzureADAttribute`, `domainNameService`.</span></span>|
|<span data-ttu-id="42eba-164">certificateRevokeStatus</span><span class="sxs-lookup"><span data-stu-id="42eba-164">certificateRevokeStatus</span></span>|[<span data-ttu-id="42eba-165">certificateRevocationStatus</span><span class="sxs-lookup"><span data-stu-id="42eba-165">certificateRevocationStatus</span></span>](../resources/intune-deviceconfig-certificaterevocationstatus.md)|<span data-ttu-id="42eba-166">Revocar el estado.</span><span class="sxs-lookup"><span data-stu-id="42eba-166">Revoke status.</span></span> <span data-ttu-id="42eba-167">Los valores posibles son: `none`, `pending`, `issued`, `failed` y `revoked`.</span><span class="sxs-lookup"><span data-stu-id="42eba-167">Possible values are: `none`, `pending`, `issued`, `failed`, `revoked`.</span></span>|
|<span data-ttu-id="42eba-168">certificateProfileDisplayName</span><span class="sxs-lookup"><span data-stu-id="42eba-168">certificateProfileDisplayName</span></span>|<span data-ttu-id="42eba-169">String</span><span class="sxs-lookup"><span data-stu-id="42eba-169">String</span></span>|<span data-ttu-id="42eba-170">Nombre para mostrar de perfil de certificado</span><span class="sxs-lookup"><span data-stu-id="42eba-170">Certificate profile display name</span></span>|
|<span data-ttu-id="42eba-171">deviceDisplayName</span><span class="sxs-lookup"><span data-stu-id="42eba-171">deviceDisplayName</span></span>|<span data-ttu-id="42eba-172">String</span><span class="sxs-lookup"><span data-stu-id="42eba-172">String</span></span>|<span data-ttu-id="42eba-173">Nombre para mostrar del dispositivo</span><span class="sxs-lookup"><span data-stu-id="42eba-173">Device display name</span></span>|
|<span data-ttu-id="42eba-174">userDisplayName</span><span class="sxs-lookup"><span data-stu-id="42eba-174">userDisplayName</span></span>|<span data-ttu-id="42eba-175">String</span><span class="sxs-lookup"><span data-stu-id="42eba-175">String</span></span>|<span data-ttu-id="42eba-176">Nombre para mostrar del usuario.</span><span class="sxs-lookup"><span data-stu-id="42eba-176">User display name</span></span>|
|<span data-ttu-id="42eba-177">certificateExpirationDateTime</span><span class="sxs-lookup"><span data-stu-id="42eba-177">certificateExpirationDateTime</span></span>|<span data-ttu-id="42eba-178">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="42eba-178">DateTimeOffset</span></span>|<span data-ttu-id="42eba-179">Fecha de caducidad del certificado</span><span class="sxs-lookup"><span data-stu-id="42eba-179">Certificate expiry date</span></span>|
|<span data-ttu-id="42eba-180">certificateLastIssuanceStateChangedDateTime</span><span class="sxs-lookup"><span data-stu-id="42eba-180">certificateLastIssuanceStateChangedDateTime</span></span>|<span data-ttu-id="42eba-181">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="42eba-181">DateTimeOffset</span></span>|<span data-ttu-id="42eba-182">Último cambio de estado de emisión de certificado</span><span class="sxs-lookup"><span data-stu-id="42eba-182">Last certificate issuance state change</span></span>|
|<span data-ttu-id="42eba-183">lastCertificateStateChangeDateTime</span><span class="sxs-lookup"><span data-stu-id="42eba-183">lastCertificateStateChangeDateTime</span></span>|<span data-ttu-id="42eba-184">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="42eba-184">DateTimeOffset</span></span>|<span data-ttu-id="42eba-185">Último cambio de estado de emisión de certificado</span><span class="sxs-lookup"><span data-stu-id="42eba-185">Last certificate issuance state change</span></span>|
|<span data-ttu-id="42eba-186">certificateIssuer</span><span class="sxs-lookup"><span data-stu-id="42eba-186">certificateIssuer</span></span>|<span data-ttu-id="42eba-187">String</span><span class="sxs-lookup"><span data-stu-id="42eba-187">String</span></span>|<span data-ttu-id="42eba-188">Emisor</span><span class="sxs-lookup"><span data-stu-id="42eba-188">Issuer</span></span>|
|<span data-ttu-id="42eba-189">certificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="42eba-189">certificateThumbprint</span></span>|<span data-ttu-id="42eba-190">String</span><span class="sxs-lookup"><span data-stu-id="42eba-190">String</span></span>|<span data-ttu-id="42eba-191">Huella digital</span><span class="sxs-lookup"><span data-stu-id="42eba-191">Thumbprint</span></span>|
|<span data-ttu-id="42eba-192">númeroSerieCertificado</span><span class="sxs-lookup"><span data-stu-id="42eba-192">certificateSerialNumber</span></span>|<span data-ttu-id="42eba-193">String</span><span class="sxs-lookup"><span data-stu-id="42eba-193">String</span></span>|<span data-ttu-id="42eba-194">Número de serie</span><span class="sxs-lookup"><span data-stu-id="42eba-194">Serial number</span></span>|
|<span data-ttu-id="42eba-195">certificateKeyLength</span><span class="sxs-lookup"><span data-stu-id="42eba-195">certificateKeyLength</span></span>|<span data-ttu-id="42eba-196">Int32</span><span class="sxs-lookup"><span data-stu-id="42eba-196">Int32</span></span>|<span data-ttu-id="42eba-197">Longitud de clave</span><span class="sxs-lookup"><span data-stu-id="42eba-197">Key length</span></span>|
|<span data-ttu-id="42eba-198">certificateEnhancedKeyUsage</span><span class="sxs-lookup"><span data-stu-id="42eba-198">certificateEnhancedKeyUsage</span></span>|<span data-ttu-id="42eba-199">String</span><span class="sxs-lookup"><span data-stu-id="42eba-199">String</span></span>|<span data-ttu-id="42eba-200">Uso mejorado de clave</span><span class="sxs-lookup"><span data-stu-id="42eba-200">Extended key usage</span></span>|
|<span data-ttu-id="42eba-201">certificateValidityPeriod</span><span class="sxs-lookup"><span data-stu-id="42eba-201">certificateValidityPeriod</span></span>|<span data-ttu-id="42eba-202">Int32</span><span class="sxs-lookup"><span data-stu-id="42eba-202">Int32</span></span>|<span data-ttu-id="42eba-203">Período de validez</span><span class="sxs-lookup"><span data-stu-id="42eba-203">Validity period</span></span>|
|<span data-ttu-id="42eba-204">certificateSubjectNameFormatString</span><span class="sxs-lookup"><span data-stu-id="42eba-204">certificateSubjectNameFormatString</span></span>|<span data-ttu-id="42eba-205">String</span><span class="sxs-lookup"><span data-stu-id="42eba-205">String</span></span>|<span data-ttu-id="42eba-206">Cadena de formato de nombre de sujeto para formatos de nombre de sujeto personalizado</span><span class="sxs-lookup"><span data-stu-id="42eba-206">Subject name format string for custom subject name formats</span></span>|
|<span data-ttu-id="42eba-207">certificateSubjectAlternativeNameFormatString</span><span class="sxs-lookup"><span data-stu-id="42eba-207">certificateSubjectAlternativeNameFormatString</span></span>|<span data-ttu-id="42eba-208">String</span><span class="sxs-lookup"><span data-stu-id="42eba-208">String</span></span>|<span data-ttu-id="42eba-209">Cadena de formato de nombre alternativo de sujeto para formatos personalizados</span><span class="sxs-lookup"><span data-stu-id="42eba-209">Subject alternative name format string for custom formats</span></span>|
|<span data-ttu-id="42eba-210">certificateIssuanceDateTime</span><span class="sxs-lookup"><span data-stu-id="42eba-210">certificateIssuanceDateTime</span></span>|<span data-ttu-id="42eba-211">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="42eba-211">DateTimeOffset</span></span>|<span data-ttu-id="42eba-212">Fecha de emisión</span><span class="sxs-lookup"><span data-stu-id="42eba-212">Issuance date</span></span>|
|<span data-ttu-id="42eba-213">certificateErrorCode</span><span class="sxs-lookup"><span data-stu-id="42eba-213">certificateErrorCode</span></span>|<span data-ttu-id="42eba-214">Int32</span><span class="sxs-lookup"><span data-stu-id="42eba-214">Int32</span></span>|<span data-ttu-id="42eba-215">Código de error</span><span class="sxs-lookup"><span data-stu-id="42eba-215">Error code</span></span>|



## <a name="response"></a><span data-ttu-id="42eba-216">Respuesta</span><span class="sxs-lookup"><span data-stu-id="42eba-216">Response</span></span>
<span data-ttu-id="42eba-217">Si tiene éxito, este método devuelve una `201 Created` código de respuesta y un objeto [managedDeviceCertificateState](../resources/intune-deviceconfig-manageddevicecertificatestate.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="42eba-217">If successful, this method returns a `201 Created` response code and a [managedDeviceCertificateState](../resources/intune-deviceconfig-manageddevicecertificatestate.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="42eba-218">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="42eba-218">Example</span></span>
### <a name="request"></a><span data-ttu-id="42eba-219">Solicitud</span><span class="sxs-lookup"><span data-stu-id="42eba-219">Request</span></span>
<span data-ttu-id="42eba-220">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="42eba-220">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.iosPkcsCertificateProfile/managedDeviceCertificateStates
Content-type: application/json
Content-length: 1517

{
  "@odata.type": "#microsoft.graph.managedDeviceCertificateState",
  "devicePlatform": "androidForWork",
  "certificateKeyUsage": "digitalSignature",
  "certificateValidityPeriodUnits": "months",
  "certificateIssuanceState": "challengeIssued",
  "certificateKeyStorageProvider": "useTpmKspOtherwiseFail",
  "certificateSubjectNameFormat": "commonNameIncludingEmail",
  "certificateSubjectAlternativeNameFormat": "emailAddress",
  "certificateRevokeStatus": "pending",
  "certificateProfileDisplayName": "Certificate Profile Display Name value",
  "deviceDisplayName": "Device Display Name value",
  "userDisplayName": "User Display Name value",
  "certificateExpirationDateTime": "2017-01-01T00:02:14.9489247-08:00",
  "certificateLastIssuanceStateChangedDateTime": "2017-01-01T00:00:27.7468732-08:00",
  "lastCertificateStateChangeDateTime": "2017-01-01T00:01:10.7144639-08:00",
  "certificateIssuer": "Certificate Issuer value",
  "certificateThumbprint": "Certificate Thumbprint value",
  "certificateSerialNumber": "Certificate Serial Number value",
  "certificateKeyLength": 4,
  "certificateEnhancedKeyUsage": "Certificate Enhanced Key Usage value",
  "certificateValidityPeriod": 9,
  "certificateSubjectNameFormatString": "Certificate Subject Name Format String value",
  "certificateSubjectAlternativeNameFormatString": "Certificate Subject Alternative Name Format String value",
  "certificateIssuanceDateTime": "2016-12-31T23:59:41.5044473-08:00",
  "certificateErrorCode": 4
}
```

### <a name="response"></a><span data-ttu-id="42eba-221">Respuesta</span><span class="sxs-lookup"><span data-stu-id="42eba-221">Response</span></span>
<span data-ttu-id="42eba-p111">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="42eba-p111">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 1566

{
  "@odata.type": "#microsoft.graph.managedDeviceCertificateState",
  "id": "d99bc884-c884-d99b-84c8-9bd984c89bd9",
  "devicePlatform": "androidForWork",
  "certificateKeyUsage": "digitalSignature",
  "certificateValidityPeriodUnits": "months",
  "certificateIssuanceState": "challengeIssued",
  "certificateKeyStorageProvider": "useTpmKspOtherwiseFail",
  "certificateSubjectNameFormat": "commonNameIncludingEmail",
  "certificateSubjectAlternativeNameFormat": "emailAddress",
  "certificateRevokeStatus": "pending",
  "certificateProfileDisplayName": "Certificate Profile Display Name value",
  "deviceDisplayName": "Device Display Name value",
  "userDisplayName": "User Display Name value",
  "certificateExpirationDateTime": "2017-01-01T00:02:14.9489247-08:00",
  "certificateLastIssuanceStateChangedDateTime": "2017-01-01T00:00:27.7468732-08:00",
  "lastCertificateStateChangeDateTime": "2017-01-01T00:01:10.7144639-08:00",
  "certificateIssuer": "Certificate Issuer value",
  "certificateThumbprint": "Certificate Thumbprint value",
  "certificateSerialNumber": "Certificate Serial Number value",
  "certificateKeyLength": 4,
  "certificateEnhancedKeyUsage": "Certificate Enhanced Key Usage value",
  "certificateValidityPeriod": 9,
  "certificateSubjectNameFormatString": "Certificate Subject Name Format String value",
  "certificateSubjectAlternativeNameFormatString": "Certificate Subject Alternative Name Format String value",
  "certificateIssuanceDateTime": "2016-12-31T23:59:41.5044473-08:00",
  "certificateErrorCode": 4
}
```





