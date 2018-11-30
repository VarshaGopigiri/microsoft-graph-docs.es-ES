---
title: Crear androidCompliancePolicy
description: Cree un objeto androidCompliancePolicy.
ms.openlocfilehash: dd483b057379f6f3c5fbf27c42507da0cd54f9b7
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090619"
---
# <a name="create-androidcompliancepolicy"></a><span data-ttu-id="027b1-103">Crear androidCompliancePolicy</span><span class="sxs-lookup"><span data-stu-id="027b1-103">Create androidCompliancePolicy</span></span>

> <span data-ttu-id="027b1-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="027b1-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="027b1-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="027b1-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="027b1-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="027b1-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="027b1-107">Cree un objeto [androidCompliancePolicy](../resources/intune-deviceconfig-androidcompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="027b1-107">Create a new [androidCompliancePolicy](../resources/intune-deviceconfig-androidcompliancepolicy.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="027b1-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="027b1-108">Prerequisites</span></span>
<span data-ttu-id="027b1-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="027b1-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="027b1-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="027b1-111">Permission type</span></span>|<span data-ttu-id="027b1-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="027b1-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="027b1-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="027b1-113">Delegated (work or school account)</span></span>|<span data-ttu-id="027b1-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="027b1-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="027b1-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="027b1-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="027b1-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="027b1-116">Not supported.</span></span>|
|<span data-ttu-id="027b1-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="027b1-117">Application</span></span>|<span data-ttu-id="027b1-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="027b1-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="027b1-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="027b1-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceCompliancePolicies
```

## <a name="request-headers"></a><span data-ttu-id="027b1-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="027b1-120">Request headers</span></span>
|<span data-ttu-id="027b1-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="027b1-121">Header</span></span>|<span data-ttu-id="027b1-122">Valor</span><span class="sxs-lookup"><span data-stu-id="027b1-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="027b1-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="027b1-123">Authorization</span></span>|<span data-ttu-id="027b1-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="027b1-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="027b1-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="027b1-125">Accept</span></span>|<span data-ttu-id="027b1-126">application/json</span><span class="sxs-lookup"><span data-stu-id="027b1-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="027b1-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="027b1-127">Request body</span></span>
<span data-ttu-id="027b1-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto androidCompliancePolicy.</span><span class="sxs-lookup"><span data-stu-id="027b1-128">In the request body, supply a JSON representation for the androidCompliancePolicy object.</span></span>

<span data-ttu-id="027b1-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto androidCompliancePolicy.</span><span class="sxs-lookup"><span data-stu-id="027b1-129">The following table shows the properties that are required when you create the androidCompliancePolicy.</span></span>

|<span data-ttu-id="027b1-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="027b1-130">Property</span></span>|<span data-ttu-id="027b1-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="027b1-131">Type</span></span>|<span data-ttu-id="027b1-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="027b1-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="027b1-133">roleScopeTagIds</span><span class="sxs-lookup"><span data-stu-id="027b1-133">roleScopeTagIds</span></span>|<span data-ttu-id="027b1-134">Colección String</span><span class="sxs-lookup"><span data-stu-id="027b1-134">String collection</span></span>|<span data-ttu-id="027b1-135">Lista de etiquetas de ámbito para esta instancia de entidad.</span><span class="sxs-lookup"><span data-stu-id="027b1-135">List of Scope Tags for this Entity instance.</span></span> <span data-ttu-id="027b1-136">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="027b1-136">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="027b1-137">id</span><span class="sxs-lookup"><span data-stu-id="027b1-137">id</span></span>|<span data-ttu-id="027b1-138">String</span><span class="sxs-lookup"><span data-stu-id="027b1-138">String</span></span>|<span data-ttu-id="027b1-139">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="027b1-139">Key of the entity.</span></span> <span data-ttu-id="027b1-140">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="027b1-140">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="027b1-141">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="027b1-141">createdDateTime</span></span>|<span data-ttu-id="027b1-142">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="027b1-142">DateTimeOffset</span></span>|<span data-ttu-id="027b1-143">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="027b1-143">DateTime the object was created.</span></span> <span data-ttu-id="027b1-144">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="027b1-144">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="027b1-145">descripción</span><span class="sxs-lookup"><span data-stu-id="027b1-145">description</span></span>|<span data-ttu-id="027b1-146">String</span><span class="sxs-lookup"><span data-stu-id="027b1-146">String</span></span>|<span data-ttu-id="027b1-147">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="027b1-147">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="027b1-148">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="027b1-148">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="027b1-149">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="027b1-149">lastModifiedDateTime</span></span>|<span data-ttu-id="027b1-150">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="027b1-150">DateTimeOffset</span></span>|<span data-ttu-id="027b1-151">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="027b1-151">DateTime the object was last modified.</span></span> <span data-ttu-id="027b1-152">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="027b1-152">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="027b1-153">displayName</span><span class="sxs-lookup"><span data-stu-id="027b1-153">displayName</span></span>|<span data-ttu-id="027b1-154">String</span><span class="sxs-lookup"><span data-stu-id="027b1-154">String</span></span>|<span data-ttu-id="027b1-155">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="027b1-155">Admin provided name of the device configuration.</span></span> <span data-ttu-id="027b1-156">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="027b1-156">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="027b1-157">version</span><span class="sxs-lookup"><span data-stu-id="027b1-157">version</span></span>|<span data-ttu-id="027b1-158">Int32</span><span class="sxs-lookup"><span data-stu-id="027b1-158">Int32</span></span>|<span data-ttu-id="027b1-159">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="027b1-159">Version of the device configuration.</span></span> <span data-ttu-id="027b1-160">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="027b1-160">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="027b1-161">passwordRequired</span><span class="sxs-lookup"><span data-stu-id="027b1-161">passwordRequired</span></span>|<span data-ttu-id="027b1-162">Booleano</span><span class="sxs-lookup"><span data-stu-id="027b1-162">Boolean</span></span>|<span data-ttu-id="027b1-163">Exigir una contraseña para desbloquear el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="027b1-163">Require a password to unlock device.</span></span>|
|<span data-ttu-id="027b1-164">passwordMinimumLength</span><span class="sxs-lookup"><span data-stu-id="027b1-164">passwordMinimumLength</span></span>|<span data-ttu-id="027b1-165">Int32</span><span class="sxs-lookup"><span data-stu-id="027b1-165">Int32</span></span>|<span data-ttu-id="027b1-166">Longitud mínima de la contraseña.</span><span class="sxs-lookup"><span data-stu-id="027b1-166">Minimum password length.</span></span> <span data-ttu-id="027b1-167">Valores válidos de 4 a 16</span><span class="sxs-lookup"><span data-stu-id="027b1-167">Valid values 4 to 16</span></span>|
|<span data-ttu-id="027b1-168">passwordRequiredType</span><span class="sxs-lookup"><span data-stu-id="027b1-168">passwordRequiredType</span></span>|[<span data-ttu-id="027b1-169">androidRequiredPasswordType</span><span class="sxs-lookup"><span data-stu-id="027b1-169">androidRequiredPasswordType</span></span>](../resources/intune-deviceconfig-androidrequiredpasswordtype.md)|<span data-ttu-id="027b1-170">Tipo de caracteres de contraseña.</span><span class="sxs-lookup"><span data-stu-id="027b1-170">Type of characters in password.</span></span> <span data-ttu-id="027b1-171">Los valores posibles son: `deviceDefault`, `alphabetic`, `alphanumeric`, `alphanumericWithSymbols`, `lowSecurityBiometric`, `numeric`, `numericComplex` y `any`.</span><span class="sxs-lookup"><span data-stu-id="027b1-171">Possible values are: `deviceDefault`, `alphabetic`, `alphanumeric`, `alphanumericWithSymbols`, `lowSecurityBiometric`, `numeric`, `numericComplex`, `any`.</span></span>|
|<span data-ttu-id="027b1-172">passwordMinutesOfInactivityBeforeLock</span><span class="sxs-lookup"><span data-stu-id="027b1-172">passwordMinutesOfInactivityBeforeLock</span></span>|<span data-ttu-id="027b1-173">Int32</span><span class="sxs-lookup"><span data-stu-id="027b1-173">Int32</span></span>|<span data-ttu-id="027b1-174">Minutos de inactividad antes de que sea necesaria una contraseña.</span><span class="sxs-lookup"><span data-stu-id="027b1-174">Minutes of inactivity before a password is required.</span></span>|
|<span data-ttu-id="027b1-175">passwordExpirationDays</span><span class="sxs-lookup"><span data-stu-id="027b1-175">passwordExpirationDays</span></span>|<span data-ttu-id="027b1-176">Int32</span><span class="sxs-lookup"><span data-stu-id="027b1-176">Int32</span></span>|<span data-ttu-id="027b1-177">Número de días antes de que expire la contraseña.</span><span class="sxs-lookup"><span data-stu-id="027b1-177">Number of days before the password expires.</span></span> <span data-ttu-id="027b1-178">Valores válidos de 1 a 65535</span><span class="sxs-lookup"><span data-stu-id="027b1-178">Valid values 1 to 65535</span></span>|
|<span data-ttu-id="027b1-179">passwordPreviousPasswordBlockCount</span><span class="sxs-lookup"><span data-stu-id="027b1-179">passwordPreviousPasswordBlockCount</span></span>|<span data-ttu-id="027b1-180">Int32</span><span class="sxs-lookup"><span data-stu-id="027b1-180">Int32</span></span>|<span data-ttu-id="027b1-181">Número de contraseñas anteriores que bloquear.</span><span class="sxs-lookup"><span data-stu-id="027b1-181">Number of previous passwords to block.</span></span>|
|<span data-ttu-id="027b1-182">securityPreventInstallAppsFromUnknownSources</span><span class="sxs-lookup"><span data-stu-id="027b1-182">securityPreventInstallAppsFromUnknownSources</span></span>|<span data-ttu-id="027b1-183">Booleano</span><span class="sxs-lookup"><span data-stu-id="027b1-183">Boolean</span></span>|<span data-ttu-id="027b1-184">Exigir que los dispositivos impidan la instalación de aplicaciones de orígenes desconocidos.</span><span class="sxs-lookup"><span data-stu-id="027b1-184">Require that devices disallow installation of apps from unknown sources.</span></span>|
|<span data-ttu-id="027b1-185">securityDisableUsbDebugging</span><span class="sxs-lookup"><span data-stu-id="027b1-185">securityDisableUsbDebugging</span></span>|<span data-ttu-id="027b1-186">Booleano</span><span class="sxs-lookup"><span data-stu-id="027b1-186">Boolean</span></span>|<span data-ttu-id="027b1-187">Deshabilitar la depuración USB en dispositivos Android.</span><span class="sxs-lookup"><span data-stu-id="027b1-187">Disable USB debugging on Android devices.</span></span>|
|<span data-ttu-id="027b1-188">securityRequireVerifyApps</span><span class="sxs-lookup"><span data-stu-id="027b1-188">securityRequireVerifyApps</span></span>|<span data-ttu-id="027b1-189">Booleano</span><span class="sxs-lookup"><span data-stu-id="027b1-189">Boolean</span></span>|<span data-ttu-id="027b1-190">Exigir que la característica Verificar aplicaciones de Android esté activada.</span><span class="sxs-lookup"><span data-stu-id="027b1-190">Require the Android Verify apps feature is turned on.</span></span>|
|<span data-ttu-id="027b1-191">deviceThreatProtectionEnabled</span><span class="sxs-lookup"><span data-stu-id="027b1-191">deviceThreatProtectionEnabled</span></span>|<span data-ttu-id="027b1-192">Booleano</span><span class="sxs-lookup"><span data-stu-id="027b1-192">Boolean</span></span>|<span data-ttu-id="027b1-193">Exigir que los dispositivos hayan habilitado la protección contra amenazas de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="027b1-193">Require that devices have enabled device threat protection.</span></span>|
|<span data-ttu-id="027b1-194">deviceThreatProtectionRequiredSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="027b1-194">deviceThreatProtectionRequiredSecurityLevel</span></span>|[<span data-ttu-id="027b1-195">deviceThreatProtectionLevel</span><span class="sxs-lookup"><span data-stu-id="027b1-195">deviceThreatProtectionLevel</span></span>](../resources/intune-deviceconfig-devicethreatprotectionlevel.md)|<span data-ttu-id="027b1-196">Exigir que el nivel de riesgo mínimo de Mobile Threat Protection informe del no cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="027b1-196">Require Mobile Threat Protection minimum risk level to report noncompliance.</span></span> <span data-ttu-id="027b1-197">Los valores posibles son: `unavailable`, `secured`, `low`, `medium`, `high` y `notSet`.</span><span class="sxs-lookup"><span data-stu-id="027b1-197">Possible values are: `unavailable`, `secured`, `low`, `medium`, `high`, `notSet`.</span></span>|
|<span data-ttu-id="027b1-198">securityBlockJailbrokenDevices</span><span class="sxs-lookup"><span data-stu-id="027b1-198">securityBlockJailbrokenDevices</span></span>|<span data-ttu-id="027b1-199">Booleano</span><span class="sxs-lookup"><span data-stu-id="027b1-199">Boolean</span></span>|<span data-ttu-id="027b1-200">No pueden usarse dispositivos con jailbreak o rooting.</span><span class="sxs-lookup"><span data-stu-id="027b1-200">Devices must not be jailbroken or rooted.</span></span>|
|<span data-ttu-id="027b1-201">osMinimumVersion</span><span class="sxs-lookup"><span data-stu-id="027b1-201">osMinimumVersion</span></span>|<span data-ttu-id="027b1-202">String</span><span class="sxs-lookup"><span data-stu-id="027b1-202">String</span></span>|<span data-ttu-id="027b1-203">Versión mínima de Android.</span><span class="sxs-lookup"><span data-stu-id="027b1-203">Minimum Android version.</span></span>|
|<span data-ttu-id="027b1-204">osMaximumVersion</span><span class="sxs-lookup"><span data-stu-id="027b1-204">osMaximumVersion</span></span>|<span data-ttu-id="027b1-205">String</span><span class="sxs-lookup"><span data-stu-id="027b1-205">String</span></span>|<span data-ttu-id="027b1-206">Versión máxima de Android.</span><span class="sxs-lookup"><span data-stu-id="027b1-206">Maximum Android version.</span></span>|
|<span data-ttu-id="027b1-207">minAndroidSecurityPatchLevel</span><span class="sxs-lookup"><span data-stu-id="027b1-207">minAndroidSecurityPatchLevel</span></span>|<span data-ttu-id="027b1-208">String</span><span class="sxs-lookup"><span data-stu-id="027b1-208">String</span></span>|<span data-ttu-id="027b1-209">Nivel de revisión de seguridad mínimo de Android.</span><span class="sxs-lookup"><span data-stu-id="027b1-209">Minimum Android security patch level.</span></span>|
|<span data-ttu-id="027b1-210">storageRequireEncryption</span><span class="sxs-lookup"><span data-stu-id="027b1-210">storageRequireEncryption</span></span>|<span data-ttu-id="027b1-211">Booleano</span><span class="sxs-lookup"><span data-stu-id="027b1-211">Boolean</span></span>|<span data-ttu-id="027b1-212">Exigir cifrado en dispositivos Android.</span><span class="sxs-lookup"><span data-stu-id="027b1-212">Require encryption on Android devices.</span></span>|
|<span data-ttu-id="027b1-213">securityRequireSafetyNetAttestationBasicIntegrity</span><span class="sxs-lookup"><span data-stu-id="027b1-213">securityRequireSafetyNetAttestationBasicIntegrity</span></span>|<span data-ttu-id="027b1-214">Booleano</span><span class="sxs-lookup"><span data-stu-id="027b1-214">Boolean</span></span>|<span data-ttu-id="027b1-215">Exigir que el dispositivo supere la comprobación de integridad básica de SafetyNet.</span><span class="sxs-lookup"><span data-stu-id="027b1-215">Require the device to pass the SafetyNet basic integrity check.</span></span>|
|<span data-ttu-id="027b1-216">securityRequireSafetyNetAttestationCertifiedDevice</span><span class="sxs-lookup"><span data-stu-id="027b1-216">securityRequireSafetyNetAttestationCertifiedDevice</span></span>|<span data-ttu-id="027b1-217">Booleano</span><span class="sxs-lookup"><span data-stu-id="027b1-217">Boolean</span></span>|<span data-ttu-id="027b1-218">Exigir que el dispositivo supere la comprobación de dispositivos certificados de SafetyNet.</span><span class="sxs-lookup"><span data-stu-id="027b1-218">Require the device to pass the SafetyNet certified device check.</span></span>|
|<span data-ttu-id="027b1-219">securityRequireGooglePlayServices</span><span class="sxs-lookup"><span data-stu-id="027b1-219">securityRequireGooglePlayServices</span></span>|<span data-ttu-id="027b1-220">Booleano</span><span class="sxs-lookup"><span data-stu-id="027b1-220">Boolean</span></span>|<span data-ttu-id="027b1-221">Exigir que Google Play Services esté instalado y habilitado en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="027b1-221">Require Google Play Services to be installed and enabled on the device.</span></span>|
|<span data-ttu-id="027b1-222">securityRequireUpToDateSecurityProviders</span><span class="sxs-lookup"><span data-stu-id="027b1-222">securityRequireUpToDateSecurityProviders</span></span>|<span data-ttu-id="027b1-223">Booleano</span><span class="sxs-lookup"><span data-stu-id="027b1-223">Boolean</span></span>|<span data-ttu-id="027b1-224">Exigir que el dispositivo tenga los proveedores de seguridad actualizados.</span><span class="sxs-lookup"><span data-stu-id="027b1-224">Require the device to have up to date security providers.</span></span> <span data-ttu-id="027b1-225">El dispositivo requerirá que Google Play Services esté instalado y habilitado.</span><span class="sxs-lookup"><span data-stu-id="027b1-225">The device will require Google Play Services to be enabled and up to date.</span></span>|
|<span data-ttu-id="027b1-226">securityRequireCompanyPortalAppIntegrity</span><span class="sxs-lookup"><span data-stu-id="027b1-226">securityRequireCompanyPortalAppIntegrity</span></span>|<span data-ttu-id="027b1-227">Booleano</span><span class="sxs-lookup"><span data-stu-id="027b1-227">Boolean</span></span>|<span data-ttu-id="027b1-228">Exigir que el dispositivo supere la comprobación de integridad en tiempo de ejecución de la aplicación cliente del Portal de empresa.</span><span class="sxs-lookup"><span data-stu-id="027b1-228">Require the device to pass the Company Portal client app runtime integrity check.</span></span>|
|<span data-ttu-id="027b1-229">conditionStatementId</span><span class="sxs-lookup"><span data-stu-id="027b1-229">conditionStatementId</span></span>|<span data-ttu-id="027b1-230">String</span><span class="sxs-lookup"><span data-stu-id="027b1-230">String</span></span>|<span data-ttu-id="027b1-231">Identificador de instrucción de condición.</span><span class="sxs-lookup"><span data-stu-id="027b1-231">Condition statement id.</span></span>|
|<span data-ttu-id="027b1-232">restrictedApps</span><span class="sxs-lookup"><span data-stu-id="027b1-232">restrictedApps</span></span>|<span data-ttu-id="027b1-233">Colección [appListItem](../resources/intune-deviceconfig-applistitem.md)</span><span class="sxs-lookup"><span data-stu-id="027b1-233">[appListItem](../resources/intune-deviceconfig-applistitem.md) collection</span></span>|<span data-ttu-id="027b1-234">Requiere que el dispositivo no contar con las aplicaciones especificadas instaladas.</span><span class="sxs-lookup"><span data-stu-id="027b1-234">Require the device to not have the specified apps installed.</span></span> <span data-ttu-id="027b1-235">Esta colección puede contener un máximo de 10 000 elementos.</span><span class="sxs-lookup"><span data-stu-id="027b1-235">This collection can contain a maximum of 10000 elements.</span></span>|



## <a name="response"></a><span data-ttu-id="027b1-236">Respuesta</span><span class="sxs-lookup"><span data-stu-id="027b1-236">Response</span></span>
<span data-ttu-id="027b1-237">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [androidCompliancePolicy](../resources/intune-deviceconfig-androidcompliancepolicy.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="027b1-237">If successful, this method returns a `201 Created` response code and a [androidCompliancePolicy](../resources/intune-deviceconfig-androidcompliancepolicy.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="027b1-238">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="027b1-238">Example</span></span>
### <a name="request"></a><span data-ttu-id="027b1-239">Solicitud</span><span class="sxs-lookup"><span data-stu-id="027b1-239">Request</span></span>
<span data-ttu-id="027b1-240">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="027b1-240">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/deviceCompliancePolicies
Content-type: application/json
Content-length: 1597

{
  "@odata.type": "#microsoft.graph.androidCompliancePolicy",
  "roleScopeTagIds": [
    "Role Scope Tag Ids value"
  ],
  "description": "Description value",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "displayName": "Display Name value",
  "version": 7,
  "passwordRequired": true,
  "passwordMinimumLength": 5,
  "passwordRequiredType": "alphabetic",
  "passwordMinutesOfInactivityBeforeLock": 5,
  "passwordExpirationDays": 6,
  "passwordPreviousPasswordBlockCount": 2,
  "securityPreventInstallAppsFromUnknownSources": true,
  "securityDisableUsbDebugging": true,
  "securityRequireVerifyApps": true,
  "deviceThreatProtectionEnabled": true,
  "deviceThreatProtectionRequiredSecurityLevel": "secured",
  "securityBlockJailbrokenDevices": true,
  "osMinimumVersion": "Os Minimum Version value",
  "osMaximumVersion": "Os Maximum Version value",
  "minAndroidSecurityPatchLevel": "Min Android Security Patch Level value",
  "storageRequireEncryption": true,
  "securityRequireSafetyNetAttestationBasicIntegrity": true,
  "securityRequireSafetyNetAttestationCertifiedDevice": true,
  "securityRequireGooglePlayServices": true,
  "securityRequireUpToDateSecurityProviders": true,
  "securityRequireCompanyPortalAppIntegrity": true,
  "conditionStatementId": "Condition Statement Id value",
  "restrictedApps": [
    {
      "@odata.type": "microsoft.graph.appListItem",
      "name": "Name value",
      "publisher": "Publisher value",
      "appStoreUrl": "https://example.com/appStoreUrl/",
      "appId": "App Id value"
    }
  ]
}
```

### <a name="response"></a><span data-ttu-id="027b1-241">Respuesta</span><span class="sxs-lookup"><span data-stu-id="027b1-241">Response</span></span>
<span data-ttu-id="027b1-p116">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="027b1-p116">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 1705

{
  "@odata.type": "#microsoft.graph.androidCompliancePolicy",
  "roleScopeTagIds": [
    "Role Scope Tag Ids value"
  ],
  "id": "752c820f-820f-752c-0f82-2c750f822c75",
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "description": "Description value",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "displayName": "Display Name value",
  "version": 7,
  "passwordRequired": true,
  "passwordMinimumLength": 5,
  "passwordRequiredType": "alphabetic",
  "passwordMinutesOfInactivityBeforeLock": 5,
  "passwordExpirationDays": 6,
  "passwordPreviousPasswordBlockCount": 2,
  "securityPreventInstallAppsFromUnknownSources": true,
  "securityDisableUsbDebugging": true,
  "securityRequireVerifyApps": true,
  "deviceThreatProtectionEnabled": true,
  "deviceThreatProtectionRequiredSecurityLevel": "secured",
  "securityBlockJailbrokenDevices": true,
  "osMinimumVersion": "Os Minimum Version value",
  "osMaximumVersion": "Os Maximum Version value",
  "minAndroidSecurityPatchLevel": "Min Android Security Patch Level value",
  "storageRequireEncryption": true,
  "securityRequireSafetyNetAttestationBasicIntegrity": true,
  "securityRequireSafetyNetAttestationCertifiedDevice": true,
  "securityRequireGooglePlayServices": true,
  "securityRequireUpToDateSecurityProviders": true,
  "securityRequireCompanyPortalAppIntegrity": true,
  "conditionStatementId": "Condition Statement Id value",
  "restrictedApps": [
    {
      "@odata.type": "microsoft.graph.appListItem",
      "name": "Name value",
      "publisher": "Publisher value",
      "appStoreUrl": "https://example.com/appStoreUrl/",
      "appId": "App Id value"
    }
  ]
}
```




