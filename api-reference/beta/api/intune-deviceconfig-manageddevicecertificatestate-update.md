---
title: Actualizar managedDeviceCertificateState
description: Actualizar las propiedades de un objeto managedDeviceCertificateState.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 3e890649f3efbe6f5eb1e22a3c4274dab09d1e88
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27970566"
---
# <a name="update-manageddevicecertificatestate"></a><span data-ttu-id="6ba65-103">Actualizar managedDeviceCertificateState</span><span class="sxs-lookup"><span data-stu-id="6ba65-103">Update managedDeviceCertificateState</span></span>

> <span data-ttu-id="6ba65-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="6ba65-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="6ba65-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="6ba65-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="6ba65-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="6ba65-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="6ba65-107">Actualizar las propiedades de un objeto [managedDeviceCertificateState](../resources/intune-deviceconfig-manageddevicecertificatestate.md) .</span><span class="sxs-lookup"><span data-stu-id="6ba65-107">Update the properties of a [managedDeviceCertificateState](../resources/intune-deviceconfig-manageddevicecertificatestate.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="6ba65-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="6ba65-108">Prerequisites</span></span>
<span data-ttu-id="6ba65-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="6ba65-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="6ba65-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="6ba65-111">Permission type</span></span>|<span data-ttu-id="6ba65-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="6ba65-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="6ba65-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="6ba65-113">Delegated (work or school account)</span></span>|<span data-ttu-id="6ba65-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="6ba65-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="6ba65-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="6ba65-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="6ba65-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6ba65-116">Not supported.</span></span>|
|<span data-ttu-id="6ba65-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="6ba65-117">Application</span></span>|<span data-ttu-id="6ba65-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6ba65-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="6ba65-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="6ba65-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.iosPkcsCertificateProfile/managedDeviceCertificateStates/{managedDeviceCertificateStateId}
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.iosScepCertificateProfile/managedDeviceCertificateStates/{managedDeviceCertificateStateId}
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.macOSScepCertificateProfile/managedDeviceCertificateStates/{managedDeviceCertificateStateId}
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.androidPkcsCertificateProfile/managedDeviceCertificateStates/{managedDeviceCertificateStateId}
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.androidScepCertificateProfile/managedDeviceCertificateStates/{managedDeviceCertificateStateId}
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.iosImportedPFXCertificateProfile/managedDeviceCertificateStates/{managedDeviceCertificateStateId}
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.macOSImportedPFXCertificateProfile/managedDeviceCertificateStates/{managedDeviceCertificateStateId}
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.androidImportedPFXCertificateProfile/managedDeviceCertificateStates/{managedDeviceCertificateStateId}
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.androidWorkProfileScepCertificateProfile/managedDeviceCertificateStates/{managedDeviceCertificateStateId}
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.androidForWorkImportedPFXCertificateProfile/managedDeviceCertificateStates/{managedDeviceCertificateStateId}
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/identityCertificate/microsoft.graph.androidForWorkPkcsCertificateProfile/managedDeviceCertificateStates/{managedDeviceCertificateStateId}
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/identityCertificate/microsoft.graph.androidForWorkScepCertificateProfile/managedDeviceCertificateStates/{managedDeviceCertificateStateId}
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsPhone81VpnConfiguration/identityCertificate/microsoft.graph.windowsPhone81SCEPCertificateProfile/managedDeviceCertificateStates/{managedDeviceCertificateStateId}
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsWifiEnterpriseEAPConfiguration/identityCertificateForClientAuthentication/microsoft.graph.windows10PkcsCertificateProfile/managedDeviceCertificateStates/{managedDeviceCertificateStateId}
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsWifiEnterpriseEAPConfiguration/identityCertificateForClientAuthentication/microsoft.graph.windows81SCEPCertificateProfile/managedDeviceCertificateStates/{managedDeviceCertificateStateId}
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsWifiEnterpriseEAPConfiguration/identityCertificateForClientAuthentication/microsoft.graph.windows10ImportedPFXCertificateProfile/managedDeviceCertificateStates/{managedDeviceCertificateStateId}
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsWifiEnterpriseEAPConfiguration/identityCertificateForClientAuthentication/microsoft.graph.windowsPhone81ImportedPFXCertificateProfile/managedDeviceCertificateStates/{managedDeviceCertificateStateId}
```

## <a name="request-headers"></a><span data-ttu-id="6ba65-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="6ba65-120">Request headers</span></span>
|<span data-ttu-id="6ba65-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6ba65-121">Header</span></span>|<span data-ttu-id="6ba65-122">Valor</span><span class="sxs-lookup"><span data-stu-id="6ba65-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="6ba65-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="6ba65-123">Authorization</span></span>|<span data-ttu-id="6ba65-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="6ba65-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="6ba65-125">Accept</span><span class="sxs-lookup"><span data-stu-id="6ba65-125">Accept</span></span>|<span data-ttu-id="6ba65-126">application/json</span><span class="sxs-lookup"><span data-stu-id="6ba65-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="6ba65-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="6ba65-127">Request body</span></span>
<span data-ttu-id="6ba65-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto [managedDeviceCertificateState](../resources/intune-deviceconfig-manageddevicecertificatestate.md) .</span><span class="sxs-lookup"><span data-stu-id="6ba65-128">In the request body, supply a JSON representation for the [managedDeviceCertificateState](../resources/intune-deviceconfig-manageddevicecertificatestate.md) object.</span></span>

<span data-ttu-id="6ba65-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el [managedDeviceCertificateState](../resources/intune-deviceconfig-manageddevicecertificatestate.md).</span><span class="sxs-lookup"><span data-stu-id="6ba65-129">The following table shows the properties that are required when you create the [managedDeviceCertificateState](../resources/intune-deviceconfig-manageddevicecertificatestate.md).</span></span>

|<span data-ttu-id="6ba65-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="6ba65-130">Property</span></span>|<span data-ttu-id="6ba65-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="6ba65-131">Type</span></span>|<span data-ttu-id="6ba65-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="6ba65-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="6ba65-133">id</span><span class="sxs-lookup"><span data-stu-id="6ba65-133">id</span></span>|<span data-ttu-id="6ba65-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="6ba65-134">String</span></span>|<span data-ttu-id="6ba65-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="6ba65-135">Key of the entity.</span></span>|
|<span data-ttu-id="6ba65-136">devicePlatform</span><span class="sxs-lookup"><span data-stu-id="6ba65-136">devicePlatform</span></span>|[<span data-ttu-id="6ba65-137">devicePlatformType</span><span class="sxs-lookup"><span data-stu-id="6ba65-137">devicePlatformType</span></span>](../resources/intune-shared-deviceplatformtype.md)|<span data-ttu-id="6ba65-138">Plataforma de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6ba65-138">Device platform.</span></span> <span data-ttu-id="6ba65-139">Los valores posibles son: `android`, `androidForWork`, `iOS`, `macOS`, `windowsPhone81`, `windows81AndLater`, `windows10AndLater` y `androidWorkProfile`.</span><span class="sxs-lookup"><span data-stu-id="6ba65-139">Possible values are: `android`, `androidForWork`, `iOS`, `macOS`, `windowsPhone81`, `windows81AndLater`, `windows10AndLater`, `androidWorkProfile`.</span></span>|
|<span data-ttu-id="6ba65-140">certificateKeyUsage</span><span class="sxs-lookup"><span data-stu-id="6ba65-140">certificateKeyUsage</span></span>|[<span data-ttu-id="6ba65-141">keyUsages</span><span class="sxs-lookup"><span data-stu-id="6ba65-141">keyUsages</span></span>](../resources/intune-deviceconfig-keyusages.md)|<span data-ttu-id="6ba65-142">Uso de la clave.</span><span class="sxs-lookup"><span data-stu-id="6ba65-142">Key usage.</span></span> <span data-ttu-id="6ba65-143">Los valores posibles son: `keyEncipherment` y `digitalSignature`.</span><span class="sxs-lookup"><span data-stu-id="6ba65-143">Possible values are: `keyEncipherment`, `digitalSignature`.</span></span>|
|<span data-ttu-id="6ba65-144">certificateValidityPeriodUnits</span><span class="sxs-lookup"><span data-stu-id="6ba65-144">certificateValidityPeriodUnits</span></span>|[<span data-ttu-id="6ba65-145">certificateValidityPeriodScale</span><span class="sxs-lookup"><span data-stu-id="6ba65-145">certificateValidityPeriodScale</span></span>](../resources/intune-deviceconfig-certificatevalidityperiodscale.md)|<span data-ttu-id="6ba65-146">Unidades del período de validez.</span><span class="sxs-lookup"><span data-stu-id="6ba65-146">Validity period units.</span></span> <span data-ttu-id="6ba65-147">Los valores posibles son: `days`, `months` y `years`.</span><span class="sxs-lookup"><span data-stu-id="6ba65-147">Possible values are: `days`, `months`, `years`.</span></span>|
|<span data-ttu-id="6ba65-148">certificateIssuanceState</span><span class="sxs-lookup"><span data-stu-id="6ba65-148">certificateIssuanceState</span></span>|[<span data-ttu-id="6ba65-149">certificateIssuanceStates</span><span class="sxs-lookup"><span data-stu-id="6ba65-149">certificateIssuanceStates</span></span>](../resources/intune-deviceconfig-certificateissuancestates.md)|<span data-ttu-id="6ba65-150">Estado de emisión.</span><span class="sxs-lookup"><span data-stu-id="6ba65-150">Issuance State.</span></span> <span data-ttu-id="6ba65-151">Los valores posibles son: `unknown`, `challengeIssued`, `challengeIssueFailed`, `requestCreationFailed`, `requestSubmitFailed`, `challengeValidationSucceeded`, `challengeValidationFailed`, `issueFailed`, `issuePending`, `issued`, `responseProcessingFailed`, `responsePending`, `enrollmentSucceeded`, `enrollmentNotNeeded`, `revoked`, `removedFromCollection`, `renewVerified`, `installFailed`, `installed` , `deleteFailed`, `deleted`, `renewalRequested`, `requested`.</span><span class="sxs-lookup"><span data-stu-id="6ba65-151">Possible values are: `unknown`, `challengeIssued`, `challengeIssueFailed`, `requestCreationFailed`, `requestSubmitFailed`, `challengeValidationSucceeded`, `challengeValidationFailed`, `issueFailed`, `issuePending`, `issued`, `responseProcessingFailed`, `responsePending`, `enrollmentSucceeded`, `enrollmentNotNeeded`, `revoked`, `removedFromCollection`, `renewVerified`, `installFailed`, `installed`, `deleteFailed`, `deleted`, `renewalRequested`, `requested`.</span></span>|
|<span data-ttu-id="6ba65-152">certificateKeyStorageProvider</span><span class="sxs-lookup"><span data-stu-id="6ba65-152">certificateKeyStorageProvider</span></span>|[<span data-ttu-id="6ba65-153">keyStorageProviderOption</span><span class="sxs-lookup"><span data-stu-id="6ba65-153">keyStorageProviderOption</span></span>](../resources/intune-deviceconfig-keystorageprovideroption.md)|<span data-ttu-id="6ba65-154">Proveedor de almacenamiento de claves.</span><span class="sxs-lookup"><span data-stu-id="6ba65-154">Key Storage Provider.</span></span> <span data-ttu-id="6ba65-155">Los valores posibles son: `useTpmKspOtherwiseUseSoftwareKsp`, `useTpmKspOtherwiseFail`, `usePassportForWorkKspOtherwiseFail` y `useSoftwareKsp`.</span><span class="sxs-lookup"><span data-stu-id="6ba65-155">Possible values are: `useTpmKspOtherwiseUseSoftwareKsp`, `useTpmKspOtherwiseFail`, `usePassportForWorkKspOtherwiseFail`, `useSoftwareKsp`.</span></span>|
|<span data-ttu-id="6ba65-156">certificateSubjectNameFormat</span><span class="sxs-lookup"><span data-stu-id="6ba65-156">certificateSubjectNameFormat</span></span>|[<span data-ttu-id="6ba65-157">subjectNameFormat</span><span class="sxs-lookup"><span data-stu-id="6ba65-157">subjectNameFormat</span></span>](../resources/intune-deviceconfig-subjectnameformat.md)|<span data-ttu-id="6ba65-158">Formato de nombre de sujeto.</span><span class="sxs-lookup"><span data-stu-id="6ba65-158">Subject name format.</span></span> <span data-ttu-id="6ba65-159">Los valores posibles son: `commonName`, `commonNameIncludingEmail`, `commonNameAsEmail`, `custom`, `commonNameAsIMEI`, `commonNameAsSerialNumber`, `commonNameAsAadDeviceId`, `commonNameAsIntuneDeviceId` y `commonNameAsDurableDeviceId`.</span><span class="sxs-lookup"><span data-stu-id="6ba65-159">Possible values are: `commonName`, `commonNameIncludingEmail`, `commonNameAsEmail`, `custom`, `commonNameAsIMEI`, `commonNameAsSerialNumber`, `commonNameAsAadDeviceId`, `commonNameAsIntuneDeviceId`, `commonNameAsDurableDeviceId`.</span></span>|
|<span data-ttu-id="6ba65-160">certificateSubjectAlternativeNameFormat</span><span class="sxs-lookup"><span data-stu-id="6ba65-160">certificateSubjectAlternativeNameFormat</span></span>|[<span data-ttu-id="6ba65-161">subjectAlternativeNameType</span><span class="sxs-lookup"><span data-stu-id="6ba65-161">subjectAlternativeNameType</span></span>](../resources/intune-deviceconfig-subjectalternativenametype.md)|<span data-ttu-id="6ba65-162">Formato de nombre alternativo de sujeto.</span><span class="sxs-lookup"><span data-stu-id="6ba65-162">Subject alternative name format.</span></span> <span data-ttu-id="6ba65-163">Los valores posibles son: `none`, `emailAddress`, `userPrincipalName`, `customAzureADAttribute` y `domainNameService`.</span><span class="sxs-lookup"><span data-stu-id="6ba65-163">Possible values are: `none`, `emailAddress`, `userPrincipalName`, `customAzureADAttribute`, `domainNameService`.</span></span>|
|<span data-ttu-id="6ba65-164">certificateRevokeStatus</span><span class="sxs-lookup"><span data-stu-id="6ba65-164">certificateRevokeStatus</span></span>|[<span data-ttu-id="6ba65-165">certificateRevocationStatus</span><span class="sxs-lookup"><span data-stu-id="6ba65-165">certificateRevocationStatus</span></span>](../resources/intune-deviceconfig-certificaterevocationstatus.md)|<span data-ttu-id="6ba65-166">Revocar el estado.</span><span class="sxs-lookup"><span data-stu-id="6ba65-166">Revoke status.</span></span> <span data-ttu-id="6ba65-167">Los valores posibles son: `none`, `pending`, `issued`, `failed` y `revoked`.</span><span class="sxs-lookup"><span data-stu-id="6ba65-167">Possible values are: `none`, `pending`, `issued`, `failed`, `revoked`.</span></span>|
|<span data-ttu-id="6ba65-168">certificateProfileDisplayName</span><span class="sxs-lookup"><span data-stu-id="6ba65-168">certificateProfileDisplayName</span></span>|<span data-ttu-id="6ba65-169">Cadena</span><span class="sxs-lookup"><span data-stu-id="6ba65-169">String</span></span>|<span data-ttu-id="6ba65-170">Nombre para mostrar de perfil de certificado</span><span class="sxs-lookup"><span data-stu-id="6ba65-170">Certificate profile display name</span></span>|
|<span data-ttu-id="6ba65-171">deviceDisplayName</span><span class="sxs-lookup"><span data-stu-id="6ba65-171">deviceDisplayName</span></span>|<span data-ttu-id="6ba65-172">String</span><span class="sxs-lookup"><span data-stu-id="6ba65-172">String</span></span>|<span data-ttu-id="6ba65-173">Nombre para mostrar del dispositivo</span><span class="sxs-lookup"><span data-stu-id="6ba65-173">Device display name</span></span>|
|<span data-ttu-id="6ba65-174">userDisplayName</span><span class="sxs-lookup"><span data-stu-id="6ba65-174">userDisplayName</span></span>|<span data-ttu-id="6ba65-175">Cadena</span><span class="sxs-lookup"><span data-stu-id="6ba65-175">String</span></span>|<span data-ttu-id="6ba65-176">Nombre para mostrar del usuario.</span><span class="sxs-lookup"><span data-stu-id="6ba65-176">User display name</span></span>|
|<span data-ttu-id="6ba65-177">certificateExpirationDateTime</span><span class="sxs-lookup"><span data-stu-id="6ba65-177">certificateExpirationDateTime</span></span>|<span data-ttu-id="6ba65-178">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="6ba65-178">DateTimeOffset</span></span>|<span data-ttu-id="6ba65-179">Fecha de caducidad del certificado</span><span class="sxs-lookup"><span data-stu-id="6ba65-179">Certificate expiry date</span></span>|
|<span data-ttu-id="6ba65-180">certificateLastIssuanceStateChangedDateTime</span><span class="sxs-lookup"><span data-stu-id="6ba65-180">certificateLastIssuanceStateChangedDateTime</span></span>|<span data-ttu-id="6ba65-181">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="6ba65-181">DateTimeOffset</span></span>|<span data-ttu-id="6ba65-182">Último cambio de estado de emisión de certificado</span><span class="sxs-lookup"><span data-stu-id="6ba65-182">Last certificate issuance state change</span></span>|
|<span data-ttu-id="6ba65-183">lastCertificateStateChangeDateTime</span><span class="sxs-lookup"><span data-stu-id="6ba65-183">lastCertificateStateChangeDateTime</span></span>|<span data-ttu-id="6ba65-184">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="6ba65-184">DateTimeOffset</span></span>|<span data-ttu-id="6ba65-185">Último cambio de estado de emisión de certificado</span><span class="sxs-lookup"><span data-stu-id="6ba65-185">Last certificate issuance state change</span></span>|
|<span data-ttu-id="6ba65-186">certificateIssuer</span><span class="sxs-lookup"><span data-stu-id="6ba65-186">certificateIssuer</span></span>|<span data-ttu-id="6ba65-187">Cadena</span><span class="sxs-lookup"><span data-stu-id="6ba65-187">String</span></span>|<span data-ttu-id="6ba65-188">Emisor</span><span class="sxs-lookup"><span data-stu-id="6ba65-188">Issuer</span></span>|
|<span data-ttu-id="6ba65-189">certificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="6ba65-189">certificateThumbprint</span></span>|<span data-ttu-id="6ba65-190">Cadena</span><span class="sxs-lookup"><span data-stu-id="6ba65-190">String</span></span>|<span data-ttu-id="6ba65-191">Huella digital</span><span class="sxs-lookup"><span data-stu-id="6ba65-191">Thumbprint</span></span>|
|<span data-ttu-id="6ba65-192">númeroSerieCertificado</span><span class="sxs-lookup"><span data-stu-id="6ba65-192">certificateSerialNumber</span></span>|<span data-ttu-id="6ba65-193">Cadena</span><span class="sxs-lookup"><span data-stu-id="6ba65-193">String</span></span>|<span data-ttu-id="6ba65-194">Número de serie</span><span class="sxs-lookup"><span data-stu-id="6ba65-194">Serial number</span></span>|
|<span data-ttu-id="6ba65-195">certificateKeyLength</span><span class="sxs-lookup"><span data-stu-id="6ba65-195">certificateKeyLength</span></span>|<span data-ttu-id="6ba65-196">Int32</span><span class="sxs-lookup"><span data-stu-id="6ba65-196">Int32</span></span>|<span data-ttu-id="6ba65-197">Longitud de clave</span><span class="sxs-lookup"><span data-stu-id="6ba65-197">Key length</span></span>|
|<span data-ttu-id="6ba65-198">certificateEnhancedKeyUsage</span><span class="sxs-lookup"><span data-stu-id="6ba65-198">certificateEnhancedKeyUsage</span></span>|<span data-ttu-id="6ba65-199">Cadena</span><span class="sxs-lookup"><span data-stu-id="6ba65-199">String</span></span>|<span data-ttu-id="6ba65-200">Uso mejorado de clave</span><span class="sxs-lookup"><span data-stu-id="6ba65-200">Extended key usage</span></span>|
|<span data-ttu-id="6ba65-201">certificateValidityPeriod</span><span class="sxs-lookup"><span data-stu-id="6ba65-201">certificateValidityPeriod</span></span>|<span data-ttu-id="6ba65-202">Int32</span><span class="sxs-lookup"><span data-stu-id="6ba65-202">Int32</span></span>|<span data-ttu-id="6ba65-203">Período de validez</span><span class="sxs-lookup"><span data-stu-id="6ba65-203">Validity period</span></span>|
|<span data-ttu-id="6ba65-204">certificateSubjectNameFormatString</span><span class="sxs-lookup"><span data-stu-id="6ba65-204">certificateSubjectNameFormatString</span></span>|<span data-ttu-id="6ba65-205">Cadena</span><span class="sxs-lookup"><span data-stu-id="6ba65-205">String</span></span>|<span data-ttu-id="6ba65-206">Cadena de formato de nombre de sujeto para formatos de nombre de sujeto personalizado</span><span class="sxs-lookup"><span data-stu-id="6ba65-206">Subject name format string for custom subject name formats</span></span>|
|<span data-ttu-id="6ba65-207">certificateSubjectAlternativeNameFormatString</span><span class="sxs-lookup"><span data-stu-id="6ba65-207">certificateSubjectAlternativeNameFormatString</span></span>|<span data-ttu-id="6ba65-208">Cadena</span><span class="sxs-lookup"><span data-stu-id="6ba65-208">String</span></span>|<span data-ttu-id="6ba65-209">Cadena de formato de nombre alternativo de sujeto para formatos personalizados</span><span class="sxs-lookup"><span data-stu-id="6ba65-209">Subject alternative name format string for custom formats</span></span>|
|<span data-ttu-id="6ba65-210">certificateIssuanceDateTime</span><span class="sxs-lookup"><span data-stu-id="6ba65-210">certificateIssuanceDateTime</span></span>|<span data-ttu-id="6ba65-211">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="6ba65-211">DateTimeOffset</span></span>|<span data-ttu-id="6ba65-212">Fecha de emisión</span><span class="sxs-lookup"><span data-stu-id="6ba65-212">Issuance date</span></span>|
|<span data-ttu-id="6ba65-213">certificateErrorCode</span><span class="sxs-lookup"><span data-stu-id="6ba65-213">certificateErrorCode</span></span>|<span data-ttu-id="6ba65-214">Int32</span><span class="sxs-lookup"><span data-stu-id="6ba65-214">Int32</span></span>|<span data-ttu-id="6ba65-215">Código de error</span><span class="sxs-lookup"><span data-stu-id="6ba65-215">Error code</span></span>|



## <a name="response"></a><span data-ttu-id="6ba65-216">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6ba65-216">Response</span></span>
<span data-ttu-id="6ba65-217">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto actualizado [managedDeviceCertificateState](../resources/intune-deviceconfig-manageddevicecertificatestate.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6ba65-217">If successful, this method returns a `200 OK` response code and an updated [managedDeviceCertificateState](../resources/intune-deviceconfig-manageddevicecertificatestate.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="6ba65-218">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6ba65-218">Example</span></span>
### <a name="request"></a><span data-ttu-id="6ba65-219">Solicitud</span><span class="sxs-lookup"><span data-stu-id="6ba65-219">Request</span></span>
<span data-ttu-id="6ba65-220">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6ba65-220">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.iosPkcsCertificateProfile/managedDeviceCertificateStates/{managedDeviceCertificateStateId}
Content-type: application/json
Content-length: 1449

{
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

### <a name="response"></a><span data-ttu-id="6ba65-221">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6ba65-221">Response</span></span>
<span data-ttu-id="6ba65-p111">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="6ba65-p111">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
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





