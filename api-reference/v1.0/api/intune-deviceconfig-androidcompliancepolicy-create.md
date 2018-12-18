---
title: Crear androidCompliancePolicy
description: Cree un objeto androidCompliancePolicy.
author: tfitzmac
ms.openlocfilehash: eb7859b2bbe6cd758ed0e7c1366afde1d0420464
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27314920"
---
# <a name="create-androidcompliancepolicy"></a><span data-ttu-id="64332-103">Crear androidCompliancePolicy</span><span class="sxs-lookup"><span data-stu-id="64332-103">Create androidCompliancePolicy</span></span>

> <span data-ttu-id="64332-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="64332-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="64332-105">Cree un objeto [androidCompliancePolicy](../resources/intune-deviceconfig-androidcompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="64332-105">Create a new [androidCompliancePolicy](../resources/intune-deviceconfig-androidcompliancepolicy.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="64332-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="64332-106">Prerequisites</span></span>
<span data-ttu-id="64332-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="64332-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="64332-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="64332-109">Permission type</span></span>|<span data-ttu-id="64332-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="64332-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="64332-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="64332-111">Delegated (work or school account)</span></span>|<span data-ttu-id="64332-112">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="64332-112">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="64332-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="64332-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="64332-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="64332-114">Not supported.</span></span>|
|<span data-ttu-id="64332-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="64332-115">Application</span></span>|<span data-ttu-id="64332-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="64332-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="64332-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="64332-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceCompliancePolicies
```

## <a name="request-headers"></a><span data-ttu-id="64332-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="64332-118">Request headers</span></span>
|<span data-ttu-id="64332-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="64332-119">Header</span></span>|<span data-ttu-id="64332-120">Valor</span><span class="sxs-lookup"><span data-stu-id="64332-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="64332-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="64332-121">Authorization</span></span>|<span data-ttu-id="64332-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="64332-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="64332-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="64332-123">Accept</span></span>|<span data-ttu-id="64332-124">application/json</span><span class="sxs-lookup"><span data-stu-id="64332-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="64332-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="64332-125">Request body</span></span>
<span data-ttu-id="64332-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto androidCompliancePolicy.</span><span class="sxs-lookup"><span data-stu-id="64332-126">In the request body, supply a JSON representation for the androidCompliancePolicy object.</span></span>

<span data-ttu-id="64332-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto androidCompliancePolicy.</span><span class="sxs-lookup"><span data-stu-id="64332-127">The following table shows the properties that are required when you create the androidCompliancePolicy.</span></span>

|<span data-ttu-id="64332-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="64332-128">Property</span></span>|<span data-ttu-id="64332-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="64332-129">Type</span></span>|<span data-ttu-id="64332-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="64332-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="64332-131">id</span><span class="sxs-lookup"><span data-stu-id="64332-131">id</span></span>|<span data-ttu-id="64332-132">String</span><span class="sxs-lookup"><span data-stu-id="64332-132">String</span></span>|<span data-ttu-id="64332-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="64332-133">Key of the entity.</span></span> <span data-ttu-id="64332-134">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="64332-134">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="64332-135">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="64332-135">createdDateTime</span></span>|<span data-ttu-id="64332-136">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="64332-136">DateTimeOffset</span></span>|<span data-ttu-id="64332-137">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="64332-137">DateTime the object was created.</span></span> <span data-ttu-id="64332-138">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="64332-138">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="64332-139">descripción</span><span class="sxs-lookup"><span data-stu-id="64332-139">description</span></span>|<span data-ttu-id="64332-140">String</span><span class="sxs-lookup"><span data-stu-id="64332-140">String</span></span>|<span data-ttu-id="64332-141">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="64332-141">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="64332-142">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="64332-142">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="64332-143">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="64332-143">lastModifiedDateTime</span></span>|<span data-ttu-id="64332-144">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="64332-144">DateTimeOffset</span></span>|<span data-ttu-id="64332-145">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="64332-145">DateTime the object was last modified.</span></span> <span data-ttu-id="64332-146">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="64332-146">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="64332-147">displayName</span><span class="sxs-lookup"><span data-stu-id="64332-147">displayName</span></span>|<span data-ttu-id="64332-148">String</span><span class="sxs-lookup"><span data-stu-id="64332-148">String</span></span>|<span data-ttu-id="64332-149">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="64332-149">Admin provided name of the device configuration.</span></span> <span data-ttu-id="64332-150">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="64332-150">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="64332-151">version</span><span class="sxs-lookup"><span data-stu-id="64332-151">version</span></span>|<span data-ttu-id="64332-152">Int32</span><span class="sxs-lookup"><span data-stu-id="64332-152">Int32</span></span>|<span data-ttu-id="64332-153">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="64332-153">Version of the device configuration.</span></span> <span data-ttu-id="64332-154">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="64332-154">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="64332-155">passwordRequired</span><span class="sxs-lookup"><span data-stu-id="64332-155">passwordRequired</span></span>|<span data-ttu-id="64332-156">Booleano</span><span class="sxs-lookup"><span data-stu-id="64332-156">Boolean</span></span>|<span data-ttu-id="64332-157">Exigir una contraseña para desbloquear el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="64332-157">Require a password to unlock device.</span></span>|
|<span data-ttu-id="64332-158">passwordMinimumLength</span><span class="sxs-lookup"><span data-stu-id="64332-158">passwordMinimumLength</span></span>|<span data-ttu-id="64332-159">Int32</span><span class="sxs-lookup"><span data-stu-id="64332-159">Int32</span></span>|<span data-ttu-id="64332-160">Longitud mínima de la contraseña.</span><span class="sxs-lookup"><span data-stu-id="64332-160">Minimum password length.</span></span> <span data-ttu-id="64332-161">Valores válidos de 4 a 16</span><span class="sxs-lookup"><span data-stu-id="64332-161">Valid values 4 to 16</span></span>|
|<span data-ttu-id="64332-162">passwordRequiredType</span><span class="sxs-lookup"><span data-stu-id="64332-162">passwordRequiredType</span></span>|[<span data-ttu-id="64332-163">androidRequiredPasswordType</span><span class="sxs-lookup"><span data-stu-id="64332-163">androidRequiredPasswordType</span></span>](../resources/intune-deviceconfig-androidrequiredpasswordtype.md)|<span data-ttu-id="64332-164">Tipo de caracteres de contraseña.</span><span class="sxs-lookup"><span data-stu-id="64332-164">Type of characters in password.</span></span> <span data-ttu-id="64332-165">Los valores posibles son: `deviceDefault`, `alphabetic`, `alphanumeric`, `alphanumericWithSymbols`, `lowSecurityBiometric`, `numeric`, `numericComplex` y `any`.</span><span class="sxs-lookup"><span data-stu-id="64332-165">Possible values are: `deviceDefault`, `alphabetic`, `alphanumeric`, `alphanumericWithSymbols`, `lowSecurityBiometric`, `numeric`, `numericComplex`, `any`.</span></span>|
|<span data-ttu-id="64332-166">passwordMinutesOfInactivityBeforeLock</span><span class="sxs-lookup"><span data-stu-id="64332-166">passwordMinutesOfInactivityBeforeLock</span></span>|<span data-ttu-id="64332-167">Int32</span><span class="sxs-lookup"><span data-stu-id="64332-167">Int32</span></span>|<span data-ttu-id="64332-168">Minutos de inactividad antes de que sea necesaria una contraseña.</span><span class="sxs-lookup"><span data-stu-id="64332-168">Minutes of inactivity before a password is required.</span></span>|
|<span data-ttu-id="64332-169">passwordExpirationDays</span><span class="sxs-lookup"><span data-stu-id="64332-169">passwordExpirationDays</span></span>|<span data-ttu-id="64332-170">Int32</span><span class="sxs-lookup"><span data-stu-id="64332-170">Int32</span></span>|<span data-ttu-id="64332-171">Número de días antes de que expire la contraseña.</span><span class="sxs-lookup"><span data-stu-id="64332-171">Number of days before the password expires.</span></span> <span data-ttu-id="64332-172">Valores válidos de 1 a 65535</span><span class="sxs-lookup"><span data-stu-id="64332-172">Valid values 1 to 65535</span></span>|
|<span data-ttu-id="64332-173">passwordPreviousPasswordBlockCount</span><span class="sxs-lookup"><span data-stu-id="64332-173">passwordPreviousPasswordBlockCount</span></span>|<span data-ttu-id="64332-174">Int32</span><span class="sxs-lookup"><span data-stu-id="64332-174">Int32</span></span>|<span data-ttu-id="64332-175">Número de contraseñas anteriores que bloquear.</span><span class="sxs-lookup"><span data-stu-id="64332-175">Number of previous passwords to block.</span></span>|
|<span data-ttu-id="64332-176">securityPreventInstallAppsFromUnknownSources</span><span class="sxs-lookup"><span data-stu-id="64332-176">securityPreventInstallAppsFromUnknownSources</span></span>|<span data-ttu-id="64332-177">Boolean</span><span class="sxs-lookup"><span data-stu-id="64332-177">Boolean</span></span>|<span data-ttu-id="64332-178">Exigir que los dispositivos impidan la instalación de aplicaciones de orígenes desconocidos.</span><span class="sxs-lookup"><span data-stu-id="64332-178">Require that devices disallow installation of apps from unknown sources.</span></span>|
|<span data-ttu-id="64332-179">securityDisableUsbDebugging</span><span class="sxs-lookup"><span data-stu-id="64332-179">securityDisableUsbDebugging</span></span>|<span data-ttu-id="64332-180">Booleano</span><span class="sxs-lookup"><span data-stu-id="64332-180">Boolean</span></span>|<span data-ttu-id="64332-181">Deshabilitar la depuración USB en dispositivos Android.</span><span class="sxs-lookup"><span data-stu-id="64332-181">Disable USB debugging on Android devices.</span></span>|
|<span data-ttu-id="64332-182">securityRequireVerifyApps</span><span class="sxs-lookup"><span data-stu-id="64332-182">securityRequireVerifyApps</span></span>|<span data-ttu-id="64332-183">Boolean</span><span class="sxs-lookup"><span data-stu-id="64332-183">Boolean</span></span>|<span data-ttu-id="64332-184">Exigir que la característica Verificar aplicaciones de Android esté activada.</span><span class="sxs-lookup"><span data-stu-id="64332-184">Require the Android Verify apps feature is turned on.</span></span>|
|<span data-ttu-id="64332-185">deviceThreatProtectionEnabled</span><span class="sxs-lookup"><span data-stu-id="64332-185">deviceThreatProtectionEnabled</span></span>|<span data-ttu-id="64332-186">Booleano</span><span class="sxs-lookup"><span data-stu-id="64332-186">Boolean</span></span>|<span data-ttu-id="64332-187">Exigir que los dispositivos hayan habilitado la protección contra amenazas de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="64332-187">Require that devices have enabled device threat protection.</span></span>|
|<span data-ttu-id="64332-188">deviceThreatProtectionRequiredSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="64332-188">deviceThreatProtectionRequiredSecurityLevel</span></span>|[<span data-ttu-id="64332-189">deviceThreatProtectionLevel</span><span class="sxs-lookup"><span data-stu-id="64332-189">deviceThreatProtectionLevel</span></span>](../resources/intune-deviceconfig-devicethreatprotectionlevel.md)|<span data-ttu-id="64332-190">Exigir que el nivel de riesgo mínimo de Mobile Threat Protection informe del no cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="64332-190">Require Mobile Threat Protection minimum risk level to report noncompliance.</span></span> <span data-ttu-id="64332-191">Los valores posibles son: `unavailable`, `secured`, `low`, `medium`, `high` y `notSet`.</span><span class="sxs-lookup"><span data-stu-id="64332-191">Possible values are: `unavailable`, `secured`, `low`, `medium`, `high`, `notSet`.</span></span>|
|<span data-ttu-id="64332-192">securityBlockJailbrokenDevices</span><span class="sxs-lookup"><span data-stu-id="64332-192">securityBlockJailbrokenDevices</span></span>|<span data-ttu-id="64332-193">Boolean</span><span class="sxs-lookup"><span data-stu-id="64332-193">Boolean</span></span>|<span data-ttu-id="64332-194">No pueden usarse dispositivos con jailbreak o rooting.</span><span class="sxs-lookup"><span data-stu-id="64332-194">Devices must not be jailbroken or rooted.</span></span>|
|<span data-ttu-id="64332-195">osMinimumVersion</span><span class="sxs-lookup"><span data-stu-id="64332-195">osMinimumVersion</span></span>|<span data-ttu-id="64332-196">String</span><span class="sxs-lookup"><span data-stu-id="64332-196">String</span></span>|<span data-ttu-id="64332-197">Versión mínima de Android.</span><span class="sxs-lookup"><span data-stu-id="64332-197">Minimum Android version.</span></span>|
|<span data-ttu-id="64332-198">osMaximumVersion</span><span class="sxs-lookup"><span data-stu-id="64332-198">osMaximumVersion</span></span>|<span data-ttu-id="64332-199">String</span><span class="sxs-lookup"><span data-stu-id="64332-199">String</span></span>|<span data-ttu-id="64332-200">Versión máxima de Android.</span><span class="sxs-lookup"><span data-stu-id="64332-200">Maximum Android version.</span></span>|
|<span data-ttu-id="64332-201">minAndroidSecurityPatchLevel</span><span class="sxs-lookup"><span data-stu-id="64332-201">minAndroidSecurityPatchLevel</span></span>|<span data-ttu-id="64332-202">String</span><span class="sxs-lookup"><span data-stu-id="64332-202">String</span></span>|<span data-ttu-id="64332-203">Nivel de revisión de seguridad mínimo de Android.</span><span class="sxs-lookup"><span data-stu-id="64332-203">Minimum Android security patch level.</span></span>|
|<span data-ttu-id="64332-204">storageRequireEncryption</span><span class="sxs-lookup"><span data-stu-id="64332-204">storageRequireEncryption</span></span>|<span data-ttu-id="64332-205">Booleano</span><span class="sxs-lookup"><span data-stu-id="64332-205">Boolean</span></span>|<span data-ttu-id="64332-206">Exigir cifrado en dispositivos Android.</span><span class="sxs-lookup"><span data-stu-id="64332-206">Require encryption on Android devices.</span></span>|
|<span data-ttu-id="64332-207">securityRequireSafetyNetAttestationBasicIntegrity</span><span class="sxs-lookup"><span data-stu-id="64332-207">securityRequireSafetyNetAttestationBasicIntegrity</span></span>|<span data-ttu-id="64332-208">Boolean</span><span class="sxs-lookup"><span data-stu-id="64332-208">Boolean</span></span>|<span data-ttu-id="64332-209">Exigir que el dispositivo supere la comprobación de integridad básica de SafetyNet.</span><span class="sxs-lookup"><span data-stu-id="64332-209">Require the device to pass the SafetyNet basic integrity check.</span></span>|
|<span data-ttu-id="64332-210">securityRequireSafetyNetAttestationCertifiedDevice</span><span class="sxs-lookup"><span data-stu-id="64332-210">securityRequireSafetyNetAttestationCertifiedDevice</span></span>|<span data-ttu-id="64332-211">Booleano</span><span class="sxs-lookup"><span data-stu-id="64332-211">Boolean</span></span>|<span data-ttu-id="64332-212">Exigir que el dispositivo supere la comprobación de dispositivos certificados de SafetyNet.</span><span class="sxs-lookup"><span data-stu-id="64332-212">Require the device to pass the SafetyNet certified device check.</span></span>|
|<span data-ttu-id="64332-213">securityRequireGooglePlayServices</span><span class="sxs-lookup"><span data-stu-id="64332-213">securityRequireGooglePlayServices</span></span>|<span data-ttu-id="64332-214">Boolean</span><span class="sxs-lookup"><span data-stu-id="64332-214">Boolean</span></span>|<span data-ttu-id="64332-215">Exigir que Google Play Services esté instalado y habilitado en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="64332-215">Require Google Play Services to be installed and enabled on the device.</span></span>|
|<span data-ttu-id="64332-216">securityRequireUpToDateSecurityProviders</span><span class="sxs-lookup"><span data-stu-id="64332-216">securityRequireUpToDateSecurityProviders</span></span>|<span data-ttu-id="64332-217">Booleano</span><span class="sxs-lookup"><span data-stu-id="64332-217">Boolean</span></span>|<span data-ttu-id="64332-218">Exigir que el dispositivo tenga los proveedores de seguridad actualizados.</span><span class="sxs-lookup"><span data-stu-id="64332-218">Require the device to have up to date security providers.</span></span> <span data-ttu-id="64332-219">El dispositivo requerirá que Google Play Services esté instalado y habilitado.</span><span class="sxs-lookup"><span data-stu-id="64332-219">The device will require Google Play Services to be enabled and up to date.</span></span>|
|<span data-ttu-id="64332-220">securityRequireCompanyPortalAppIntegrity</span><span class="sxs-lookup"><span data-stu-id="64332-220">securityRequireCompanyPortalAppIntegrity</span></span>|<span data-ttu-id="64332-221">Boolean</span><span class="sxs-lookup"><span data-stu-id="64332-221">Boolean</span></span>|<span data-ttu-id="64332-222">Exigir que el dispositivo supere la comprobación de integridad en tiempo de ejecución de la aplicación cliente del Portal de empresa.</span><span class="sxs-lookup"><span data-stu-id="64332-222">Require the device to pass the Company Portal client app runtime integrity check.</span></span>|



## <a name="response"></a><span data-ttu-id="64332-223">Respuesta</span><span class="sxs-lookup"><span data-stu-id="64332-223">Response</span></span>
<span data-ttu-id="64332-224">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [androidCompliancePolicy](../resources/intune-deviceconfig-androidcompliancepolicy.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="64332-224">If successful, this method returns a `201 Created` response code and a [androidCompliancePolicy](../resources/intune-deviceconfig-androidcompliancepolicy.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="64332-225">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="64332-225">Example</span></span>
### <a name="request"></a><span data-ttu-id="64332-226">Solicitud</span><span class="sxs-lookup"><span data-stu-id="64332-226">Request</span></span>
<span data-ttu-id="64332-227">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="64332-227">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceManagement/deviceCompliancePolicies
Content-type: application/json
Content-length: 1159

{
  "@odata.type": "#microsoft.graph.androidCompliancePolicy",
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

### <a name="response"></a><span data-ttu-id="64332-228">Respuesta</span><span class="sxs-lookup"><span data-stu-id="64332-228">Response</span></span>
<span data-ttu-id="64332-p113">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="64332-p113">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 1331

{
  "@odata.type": "#microsoft.graph.androidCompliancePolicy",
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
  "securityRequireCompanyPortalAppIntegrity": true
}
```



