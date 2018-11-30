---
title: Crear androidWorkProfileCompliancePolicy
description: Crear un nuevo objeto androidWorkProfileCompliancePolicy.
ms.openlocfilehash: c823ef27ecd3e55646f010746b577f549510c1bf
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030094"
---
# <a name="create-androidworkprofilecompliancepolicy"></a><span data-ttu-id="5c507-103">Crear androidWorkProfileCompliancePolicy</span><span class="sxs-lookup"><span data-stu-id="5c507-103">Create androidWorkProfileCompliancePolicy</span></span>

> <span data-ttu-id="5c507-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="5c507-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="5c507-105">Crear un nuevo objeto [androidWorkProfileCompliancePolicy](../resources/intune-deviceconfig-androidworkprofilecompliancepolicy.md) .</span><span class="sxs-lookup"><span data-stu-id="5c507-105">Create a new [androidWorkProfileCompliancePolicy](../resources/intune-deviceconfig-androidworkprofilecompliancepolicy.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="5c507-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="5c507-106">Prerequisites</span></span>
<span data-ttu-id="5c507-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="5c507-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="5c507-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="5c507-109">Permission type</span></span>|<span data-ttu-id="5c507-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="5c507-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="5c507-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="5c507-111">Delegated (work or school account)</span></span>|<span data-ttu-id="5c507-112">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="5c507-112">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="5c507-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="5c507-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="5c507-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5c507-114">Not supported.</span></span>|
|<span data-ttu-id="5c507-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="5c507-115">Application</span></span>|<span data-ttu-id="5c507-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5c507-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="5c507-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="5c507-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceCompliancePolicies
```

## <a name="request-headers"></a><span data-ttu-id="5c507-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="5c507-118">Request headers</span></span>
|<span data-ttu-id="5c507-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5c507-119">Header</span></span>|<span data-ttu-id="5c507-120">Valor</span><span class="sxs-lookup"><span data-stu-id="5c507-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="5c507-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="5c507-121">Authorization</span></span>|<span data-ttu-id="5c507-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="5c507-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="5c507-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="5c507-123">Accept</span></span>|<span data-ttu-id="5c507-124">application/json</span><span class="sxs-lookup"><span data-stu-id="5c507-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="5c507-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="5c507-125">Request body</span></span>
<span data-ttu-id="5c507-126">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto androidWorkProfileCompliancePolicy.</span><span class="sxs-lookup"><span data-stu-id="5c507-126">In the request body, supply a JSON representation for the androidWorkProfileCompliancePolicy object.</span></span>

<span data-ttu-id="5c507-127">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el androidWorkProfileCompliancePolicy.</span><span class="sxs-lookup"><span data-stu-id="5c507-127">The following table shows the properties that are required when you create the androidWorkProfileCompliancePolicy.</span></span>

|<span data-ttu-id="5c507-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="5c507-128">Property</span></span>|<span data-ttu-id="5c507-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="5c507-129">Type</span></span>|<span data-ttu-id="5c507-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="5c507-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="5c507-131">id</span><span class="sxs-lookup"><span data-stu-id="5c507-131">id</span></span>|<span data-ttu-id="5c507-132">String</span><span class="sxs-lookup"><span data-stu-id="5c507-132">String</span></span>|<span data-ttu-id="5c507-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="5c507-133">Key of the entity.</span></span> <span data-ttu-id="5c507-134">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="5c507-134">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="5c507-135">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="5c507-135">createdDateTime</span></span>|<span data-ttu-id="5c507-136">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="5c507-136">DateTimeOffset</span></span>|<span data-ttu-id="5c507-137">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="5c507-137">DateTime the object was created.</span></span> <span data-ttu-id="5c507-138">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="5c507-138">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="5c507-139">descripción</span><span class="sxs-lookup"><span data-stu-id="5c507-139">description</span></span>|<span data-ttu-id="5c507-140">String</span><span class="sxs-lookup"><span data-stu-id="5c507-140">String</span></span>|<span data-ttu-id="5c507-141">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5c507-141">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="5c507-142">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="5c507-142">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="5c507-143">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="5c507-143">lastModifiedDateTime</span></span>|<span data-ttu-id="5c507-144">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="5c507-144">DateTimeOffset</span></span>|<span data-ttu-id="5c507-145">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="5c507-145">DateTime the object was last modified.</span></span> <span data-ttu-id="5c507-146">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="5c507-146">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="5c507-147">displayName</span><span class="sxs-lookup"><span data-stu-id="5c507-147">displayName</span></span>|<span data-ttu-id="5c507-148">String</span><span class="sxs-lookup"><span data-stu-id="5c507-148">String</span></span>|<span data-ttu-id="5c507-149">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5c507-149">Admin provided name of the device configuration.</span></span> <span data-ttu-id="5c507-150">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="5c507-150">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="5c507-151">version</span><span class="sxs-lookup"><span data-stu-id="5c507-151">version</span></span>|<span data-ttu-id="5c507-152">Int32</span><span class="sxs-lookup"><span data-stu-id="5c507-152">Int32</span></span>|<span data-ttu-id="5c507-153">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5c507-153">Version of the device configuration.</span></span> <span data-ttu-id="5c507-154">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="5c507-154">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="5c507-155">passwordRequired</span><span class="sxs-lookup"><span data-stu-id="5c507-155">passwordRequired</span></span>|<span data-ttu-id="5c507-156">Booleano</span><span class="sxs-lookup"><span data-stu-id="5c507-156">Boolean</span></span>|<span data-ttu-id="5c507-157">Exigir una contraseña para desbloquear el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5c507-157">Require a password to unlock device.</span></span>|
|<span data-ttu-id="5c507-158">passwordMinimumLength</span><span class="sxs-lookup"><span data-stu-id="5c507-158">passwordMinimumLength</span></span>|<span data-ttu-id="5c507-159">Int32</span><span class="sxs-lookup"><span data-stu-id="5c507-159">Int32</span></span>|<span data-ttu-id="5c507-160">Longitud mínima de la contraseña.</span><span class="sxs-lookup"><span data-stu-id="5c507-160">Minimum password length.</span></span> <span data-ttu-id="5c507-161">Valores válidos de 4 a 16</span><span class="sxs-lookup"><span data-stu-id="5c507-161">Valid values 4 to 16</span></span>|
|<span data-ttu-id="5c507-162">passwordRequiredType</span><span class="sxs-lookup"><span data-stu-id="5c507-162">passwordRequiredType</span></span>|[<span data-ttu-id="5c507-163">androidRequiredPasswordType</span><span class="sxs-lookup"><span data-stu-id="5c507-163">androidRequiredPasswordType</span></span>](../resources/intune-deviceconfig-androidrequiredpasswordtype.md)|<span data-ttu-id="5c507-164">Tipo de caracteres de contraseña.</span><span class="sxs-lookup"><span data-stu-id="5c507-164">Type of characters in password.</span></span> <span data-ttu-id="5c507-165">Los valores posibles son: `deviceDefault`, `alphabetic`, `alphanumeric`, `alphanumericWithSymbols`, `lowSecurityBiometric`, `numeric`, `numericComplex` y `any`.</span><span class="sxs-lookup"><span data-stu-id="5c507-165">Possible values are: `deviceDefault`, `alphabetic`, `alphanumeric`, `alphanumericWithSymbols`, `lowSecurityBiometric`, `numeric`, `numericComplex`, `any`.</span></span>|
|<span data-ttu-id="5c507-166">passwordMinutesOfInactivityBeforeLock</span><span class="sxs-lookup"><span data-stu-id="5c507-166">passwordMinutesOfInactivityBeforeLock</span></span>|<span data-ttu-id="5c507-167">Int32</span><span class="sxs-lookup"><span data-stu-id="5c507-167">Int32</span></span>|<span data-ttu-id="5c507-168">Minutos de inactividad antes de que sea necesaria una contraseña.</span><span class="sxs-lookup"><span data-stu-id="5c507-168">Minutes of inactivity before a password is required.</span></span>|
|<span data-ttu-id="5c507-169">passwordExpirationDays</span><span class="sxs-lookup"><span data-stu-id="5c507-169">passwordExpirationDays</span></span>|<span data-ttu-id="5c507-170">Int32</span><span class="sxs-lookup"><span data-stu-id="5c507-170">Int32</span></span>|<span data-ttu-id="5c507-171">Número de días antes de que expire la contraseña.</span><span class="sxs-lookup"><span data-stu-id="5c507-171">Number of days before the password expires.</span></span> <span data-ttu-id="5c507-172">Valores válidos de 1 a 365</span><span class="sxs-lookup"><span data-stu-id="5c507-172">Valid values 1 to 365</span></span>|
|<span data-ttu-id="5c507-173">passwordPreviousPasswordBlockCount</span><span class="sxs-lookup"><span data-stu-id="5c507-173">passwordPreviousPasswordBlockCount</span></span>|<span data-ttu-id="5c507-174">Int32</span><span class="sxs-lookup"><span data-stu-id="5c507-174">Int32</span></span>|<span data-ttu-id="5c507-175">Número de contraseñas anteriores que bloquear.</span><span class="sxs-lookup"><span data-stu-id="5c507-175">Number of previous passwords to block.</span></span>|
|<span data-ttu-id="5c507-176">securityPreventInstallAppsFromUnknownSources</span><span class="sxs-lookup"><span data-stu-id="5c507-176">securityPreventInstallAppsFromUnknownSources</span></span>|<span data-ttu-id="5c507-177">Booleano</span><span class="sxs-lookup"><span data-stu-id="5c507-177">Boolean</span></span>|<span data-ttu-id="5c507-178">Exigir que los dispositivos impidan la instalación de aplicaciones de orígenes desconocidos.</span><span class="sxs-lookup"><span data-stu-id="5c507-178">Require that devices disallow installation of apps from unknown sources.</span></span>|
|<span data-ttu-id="5c507-179">securityDisableUsbDebugging</span><span class="sxs-lookup"><span data-stu-id="5c507-179">securityDisableUsbDebugging</span></span>|<span data-ttu-id="5c507-180">Booleano</span><span class="sxs-lookup"><span data-stu-id="5c507-180">Boolean</span></span>|<span data-ttu-id="5c507-181">Deshabilitar la depuración USB en dispositivos Android.</span><span class="sxs-lookup"><span data-stu-id="5c507-181">Disable USB debugging on Android devices.</span></span>|
|<span data-ttu-id="5c507-182">securityRequireVerifyApps</span><span class="sxs-lookup"><span data-stu-id="5c507-182">securityRequireVerifyApps</span></span>|<span data-ttu-id="5c507-183">Booleano</span><span class="sxs-lookup"><span data-stu-id="5c507-183">Boolean</span></span>|<span data-ttu-id="5c507-184">Exigir que la característica Verificar aplicaciones de Android esté activada.</span><span class="sxs-lookup"><span data-stu-id="5c507-184">Require the Android Verify apps feature is turned on.</span></span>|
|<span data-ttu-id="5c507-185">deviceThreatProtectionEnabled</span><span class="sxs-lookup"><span data-stu-id="5c507-185">deviceThreatProtectionEnabled</span></span>|<span data-ttu-id="5c507-186">Booleano</span><span class="sxs-lookup"><span data-stu-id="5c507-186">Boolean</span></span>|<span data-ttu-id="5c507-187">Exigir que los dispositivos hayan habilitado la protección contra amenazas de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5c507-187">Require that devices have enabled device threat protection.</span></span>|
|<span data-ttu-id="5c507-188">deviceThreatProtectionRequiredSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="5c507-188">deviceThreatProtectionRequiredSecurityLevel</span></span>|[<span data-ttu-id="5c507-189">deviceThreatProtectionLevel</span><span class="sxs-lookup"><span data-stu-id="5c507-189">deviceThreatProtectionLevel</span></span>](../resources/intune-deviceconfig-devicethreatprotectionlevel.md)|<span data-ttu-id="5c507-190">Exigir que el nivel de riesgo mínimo de Mobile Threat Protection informe del no cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="5c507-190">Require Mobile Threat Protection minimum risk level to report noncompliance.</span></span> <span data-ttu-id="5c507-191">Los valores posibles son: `unavailable`, `secured`, `low`, `medium`, `high` y `notSet`.</span><span class="sxs-lookup"><span data-stu-id="5c507-191">Possible values are: `unavailable`, `secured`, `low`, `medium`, `high`, `notSet`.</span></span>|
|<span data-ttu-id="5c507-192">securityBlockJailbrokenDevices</span><span class="sxs-lookup"><span data-stu-id="5c507-192">securityBlockJailbrokenDevices</span></span>|<span data-ttu-id="5c507-193">Booleano</span><span class="sxs-lookup"><span data-stu-id="5c507-193">Boolean</span></span>|<span data-ttu-id="5c507-194">No pueden usarse dispositivos con jailbreak o rooting.</span><span class="sxs-lookup"><span data-stu-id="5c507-194">Devices must not be jailbroken or rooted.</span></span>|
|<span data-ttu-id="5c507-195">osMinimumVersion</span><span class="sxs-lookup"><span data-stu-id="5c507-195">osMinimumVersion</span></span>|<span data-ttu-id="5c507-196">String</span><span class="sxs-lookup"><span data-stu-id="5c507-196">String</span></span>|<span data-ttu-id="5c507-197">Versión mínima de Android.</span><span class="sxs-lookup"><span data-stu-id="5c507-197">Minimum Android version.</span></span>|
|<span data-ttu-id="5c507-198">osMaximumVersion</span><span class="sxs-lookup"><span data-stu-id="5c507-198">osMaximumVersion</span></span>|<span data-ttu-id="5c507-199">String</span><span class="sxs-lookup"><span data-stu-id="5c507-199">String</span></span>|<span data-ttu-id="5c507-200">Versión máxima de Android.</span><span class="sxs-lookup"><span data-stu-id="5c507-200">Maximum Android version.</span></span>|
|<span data-ttu-id="5c507-201">minAndroidSecurityPatchLevel</span><span class="sxs-lookup"><span data-stu-id="5c507-201">minAndroidSecurityPatchLevel</span></span>|<span data-ttu-id="5c507-202">String</span><span class="sxs-lookup"><span data-stu-id="5c507-202">String</span></span>|<span data-ttu-id="5c507-203">Nivel de revisión de seguridad mínimo de Android.</span><span class="sxs-lookup"><span data-stu-id="5c507-203">Minimum Android security patch level.</span></span>|
|<span data-ttu-id="5c507-204">storageRequireEncryption</span><span class="sxs-lookup"><span data-stu-id="5c507-204">storageRequireEncryption</span></span>|<span data-ttu-id="5c507-205">Booleano</span><span class="sxs-lookup"><span data-stu-id="5c507-205">Boolean</span></span>|<span data-ttu-id="5c507-206">Exigir cifrado en dispositivos Android.</span><span class="sxs-lookup"><span data-stu-id="5c507-206">Require encryption on Android devices.</span></span>|
|<span data-ttu-id="5c507-207">securityRequireSafetyNetAttestationBasicIntegrity</span><span class="sxs-lookup"><span data-stu-id="5c507-207">securityRequireSafetyNetAttestationBasicIntegrity</span></span>|<span data-ttu-id="5c507-208">Booleano</span><span class="sxs-lookup"><span data-stu-id="5c507-208">Boolean</span></span>|<span data-ttu-id="5c507-209">Exigir que el dispositivo supere la comprobación de integridad básica de SafetyNet.</span><span class="sxs-lookup"><span data-stu-id="5c507-209">Require the device to pass the SafetyNet basic integrity check.</span></span>|
|<span data-ttu-id="5c507-210">securityRequireSafetyNetAttestationCertifiedDevice</span><span class="sxs-lookup"><span data-stu-id="5c507-210">securityRequireSafetyNetAttestationCertifiedDevice</span></span>|<span data-ttu-id="5c507-211">Booleano</span><span class="sxs-lookup"><span data-stu-id="5c507-211">Boolean</span></span>|<span data-ttu-id="5c507-212">Exigir que el dispositivo supere la comprobación de dispositivos certificados de SafetyNet.</span><span class="sxs-lookup"><span data-stu-id="5c507-212">Require the device to pass the SafetyNet certified device check.</span></span>|
|<span data-ttu-id="5c507-213">securityRequireGooglePlayServices</span><span class="sxs-lookup"><span data-stu-id="5c507-213">securityRequireGooglePlayServices</span></span>|<span data-ttu-id="5c507-214">Booleano</span><span class="sxs-lookup"><span data-stu-id="5c507-214">Boolean</span></span>|<span data-ttu-id="5c507-215">Exigir que Google Play Services esté instalado y habilitado en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5c507-215">Require Google Play Services to be installed and enabled on the device.</span></span>|
|<span data-ttu-id="5c507-216">securityRequireUpToDateSecurityProviders</span><span class="sxs-lookup"><span data-stu-id="5c507-216">securityRequireUpToDateSecurityProviders</span></span>|<span data-ttu-id="5c507-217">Booleano</span><span class="sxs-lookup"><span data-stu-id="5c507-217">Boolean</span></span>|<span data-ttu-id="5c507-218">Exigir que el dispositivo tenga los proveedores de seguridad actualizados.</span><span class="sxs-lookup"><span data-stu-id="5c507-218">Require the device to have up to date security providers.</span></span> <span data-ttu-id="5c507-219">El dispositivo requerirá que Google Play Services esté instalado y habilitado.</span><span class="sxs-lookup"><span data-stu-id="5c507-219">The device will require Google Play Services to be enabled and up to date.</span></span>|
|<span data-ttu-id="5c507-220">securityRequireCompanyPortalAppIntegrity</span><span class="sxs-lookup"><span data-stu-id="5c507-220">securityRequireCompanyPortalAppIntegrity</span></span>|<span data-ttu-id="5c507-221">Booleano</span><span class="sxs-lookup"><span data-stu-id="5c507-221">Boolean</span></span>|<span data-ttu-id="5c507-222">Exigir que el dispositivo supere la comprobación de integridad en tiempo de ejecución de la aplicación cliente del Portal de empresa.</span><span class="sxs-lookup"><span data-stu-id="5c507-222">Require the device to pass the Company Portal client app runtime integrity check.</span></span>|



## <a name="response"></a><span data-ttu-id="5c507-223">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5c507-223">Response</span></span>
<span data-ttu-id="5c507-224">Si tiene éxito, este método devuelve una `201 Created` código de respuesta y un objeto [androidWorkProfileCompliancePolicy](../resources/intune-deviceconfig-androidworkprofilecompliancepolicy.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5c507-224">If successful, this method returns a `201 Created` response code and a [androidWorkProfileCompliancePolicy](../resources/intune-deviceconfig-androidworkprofilecompliancepolicy.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="5c507-225">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="5c507-225">Example</span></span>
### <a name="request"></a><span data-ttu-id="5c507-226">Solicitud</span><span class="sxs-lookup"><span data-stu-id="5c507-226">Request</span></span>
<span data-ttu-id="5c507-227">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="5c507-227">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceManagement/deviceCompliancePolicies
Content-type: application/json
Content-length: 1170

{
  "@odata.type": "#microsoft.graph.androidWorkProfileCompliancePolicy",
  "description": "Description value",
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
  "securityRequireCompanyPortalAppIntegrity": true
}
```

### <a name="response"></a><span data-ttu-id="5c507-228">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5c507-228">Response</span></span>
<span data-ttu-id="5c507-p113">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="5c507-p113">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 1342

{
  "@odata.type": "#microsoft.graph.androidWorkProfileCompliancePolicy",
  "id": "4e385271-5271-4e38-7152-384e7152384e",
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
  "securityRequireCompanyPortalAppIntegrity": true
}
```



