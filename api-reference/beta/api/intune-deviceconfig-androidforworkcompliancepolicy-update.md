---
title: Actualizar androidForWorkCompliancePolicy
description: Actualizar las propiedades de un objeto androidForWorkCompliancePolicy.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: b02e7f54d5281478c2489dd86eb4f2d25f27fc7a
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27812736"
---
# <a name="update-androidforworkcompliancepolicy"></a><span data-ttu-id="c7e78-103">Actualizar androidForWorkCompliancePolicy</span><span class="sxs-lookup"><span data-stu-id="c7e78-103">Update androidForWorkCompliancePolicy</span></span>

> <span data-ttu-id="c7e78-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="c7e78-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="c7e78-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="c7e78-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="c7e78-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="c7e78-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="c7e78-107">Actualizar las propiedades de un objeto [androidForWorkCompliancePolicy](../resources/intune-deviceconfig-androidforworkcompliancepolicy.md) .</span><span class="sxs-lookup"><span data-stu-id="c7e78-107">Update the properties of a [androidForWorkCompliancePolicy](../resources/intune-deviceconfig-androidforworkcompliancepolicy.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="c7e78-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="c7e78-108">Prerequisites</span></span>
<span data-ttu-id="c7e78-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="c7e78-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="c7e78-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="c7e78-111">Permission type</span></span>|<span data-ttu-id="c7e78-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="c7e78-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="c7e78-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="c7e78-113">Delegated (work or school account)</span></span>|<span data-ttu-id="c7e78-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="c7e78-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="c7e78-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="c7e78-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="c7e78-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c7e78-116">Not supported.</span></span>|
|<span data-ttu-id="c7e78-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="c7e78-117">Application</span></span>|<span data-ttu-id="c7e78-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c7e78-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="c7e78-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c7e78-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}
```

## <a name="request-headers"></a><span data-ttu-id="c7e78-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c7e78-120">Request headers</span></span>
|<span data-ttu-id="c7e78-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c7e78-121">Header</span></span>|<span data-ttu-id="c7e78-122">Valor</span><span class="sxs-lookup"><span data-stu-id="c7e78-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="c7e78-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="c7e78-123">Authorization</span></span>|<span data-ttu-id="c7e78-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="c7e78-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="c7e78-125">Accept</span><span class="sxs-lookup"><span data-stu-id="c7e78-125">Accept</span></span>|<span data-ttu-id="c7e78-126">application/json</span><span class="sxs-lookup"><span data-stu-id="c7e78-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="c7e78-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c7e78-127">Request body</span></span>
<span data-ttu-id="c7e78-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto [androidForWorkCompliancePolicy](../resources/intune-deviceconfig-androidforworkcompliancepolicy.md) .</span><span class="sxs-lookup"><span data-stu-id="c7e78-128">In the request body, supply a JSON representation for the [androidForWorkCompliancePolicy](../resources/intune-deviceconfig-androidforworkcompliancepolicy.md) object.</span></span>

<span data-ttu-id="c7e78-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el [androidForWorkCompliancePolicy](../resources/intune-deviceconfig-androidforworkcompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="c7e78-129">The following table shows the properties that are required when you create the [androidForWorkCompliancePolicy](../resources/intune-deviceconfig-androidforworkcompliancepolicy.md).</span></span>

|<span data-ttu-id="c7e78-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="c7e78-130">Property</span></span>|<span data-ttu-id="c7e78-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="c7e78-131">Type</span></span>|<span data-ttu-id="c7e78-132">Description</span><span class="sxs-lookup"><span data-stu-id="c7e78-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="c7e78-133">roleScopeTagIds</span><span class="sxs-lookup"><span data-stu-id="c7e78-133">roleScopeTagIds</span></span>|<span data-ttu-id="c7e78-134">Colección String</span><span class="sxs-lookup"><span data-stu-id="c7e78-134">String collection</span></span>|<span data-ttu-id="c7e78-135">Lista de etiquetas de ámbito para esta instancia de entidad.</span><span class="sxs-lookup"><span data-stu-id="c7e78-135">List of Scope Tags for this Entity instance.</span></span> <span data-ttu-id="c7e78-136">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="c7e78-136">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="c7e78-137">id</span><span class="sxs-lookup"><span data-stu-id="c7e78-137">id</span></span>|<span data-ttu-id="c7e78-138">Cadena</span><span class="sxs-lookup"><span data-stu-id="c7e78-138">String</span></span>|<span data-ttu-id="c7e78-139">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="c7e78-139">Key of the entity.</span></span> <span data-ttu-id="c7e78-140">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="c7e78-140">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="c7e78-141">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="c7e78-141">createdDateTime</span></span>|<span data-ttu-id="c7e78-142">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="c7e78-142">DateTimeOffset</span></span>|<span data-ttu-id="c7e78-143">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="c7e78-143">DateTime the object was created.</span></span> <span data-ttu-id="c7e78-144">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="c7e78-144">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="c7e78-145">descripción</span><span class="sxs-lookup"><span data-stu-id="c7e78-145">description</span></span>|<span data-ttu-id="c7e78-146">Cadena</span><span class="sxs-lookup"><span data-stu-id="c7e78-146">String</span></span>|<span data-ttu-id="c7e78-147">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c7e78-147">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="c7e78-148">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="c7e78-148">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="c7e78-149">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="c7e78-149">lastModifiedDateTime</span></span>|<span data-ttu-id="c7e78-150">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="c7e78-150">DateTimeOffset</span></span>|<span data-ttu-id="c7e78-151">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="c7e78-151">DateTime the object was last modified.</span></span> <span data-ttu-id="c7e78-152">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="c7e78-152">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="c7e78-153">displayName</span><span class="sxs-lookup"><span data-stu-id="c7e78-153">displayName</span></span>|<span data-ttu-id="c7e78-154">Cadena</span><span class="sxs-lookup"><span data-stu-id="c7e78-154">String</span></span>|<span data-ttu-id="c7e78-155">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c7e78-155">Admin provided name of the device configuration.</span></span> <span data-ttu-id="c7e78-156">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="c7e78-156">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="c7e78-157">version</span><span class="sxs-lookup"><span data-stu-id="c7e78-157">version</span></span>|<span data-ttu-id="c7e78-158">Int32</span><span class="sxs-lookup"><span data-stu-id="c7e78-158">Int32</span></span>|<span data-ttu-id="c7e78-159">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c7e78-159">Version of the device configuration.</span></span> <span data-ttu-id="c7e78-160">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="c7e78-160">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="c7e78-161">passwordRequired</span><span class="sxs-lookup"><span data-stu-id="c7e78-161">passwordRequired</span></span>|<span data-ttu-id="c7e78-162">Booleano</span><span class="sxs-lookup"><span data-stu-id="c7e78-162">Boolean</span></span>|<span data-ttu-id="c7e78-163">Exigir una contraseña para desbloquear el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c7e78-163">Require a password to unlock device.</span></span>|
|<span data-ttu-id="c7e78-164">passwordMinimumLength</span><span class="sxs-lookup"><span data-stu-id="c7e78-164">passwordMinimumLength</span></span>|<span data-ttu-id="c7e78-165">Int32</span><span class="sxs-lookup"><span data-stu-id="c7e78-165">Int32</span></span>|<span data-ttu-id="c7e78-166">Longitud mínima de la contraseña.</span><span class="sxs-lookup"><span data-stu-id="c7e78-166">Minimum password length.</span></span> <span data-ttu-id="c7e78-167">Valores válidos de 4 a 16</span><span class="sxs-lookup"><span data-stu-id="c7e78-167">Valid values 4 to 16</span></span>|
|<span data-ttu-id="c7e78-168">passwordRequiredType</span><span class="sxs-lookup"><span data-stu-id="c7e78-168">passwordRequiredType</span></span>|[<span data-ttu-id="c7e78-169">androidRequiredPasswordType</span><span class="sxs-lookup"><span data-stu-id="c7e78-169">androidRequiredPasswordType</span></span>](../resources/intune-deviceconfig-androidrequiredpasswordtype.md)|<span data-ttu-id="c7e78-170">Tipo de caracteres de contraseña.</span><span class="sxs-lookup"><span data-stu-id="c7e78-170">Type of characters in password.</span></span> <span data-ttu-id="c7e78-171">Los valores posibles son: `deviceDefault`, `alphabetic`, `alphanumeric`, `alphanumericWithSymbols`, `lowSecurityBiometric`, `numeric`, `numericComplex` y `any`.</span><span class="sxs-lookup"><span data-stu-id="c7e78-171">Possible values are: `deviceDefault`, `alphabetic`, `alphanumeric`, `alphanumericWithSymbols`, `lowSecurityBiometric`, `numeric`, `numericComplex`, `any`.</span></span>|
|<span data-ttu-id="c7e78-172">passwordMinutesOfInactivityBeforeLock</span><span class="sxs-lookup"><span data-stu-id="c7e78-172">passwordMinutesOfInactivityBeforeLock</span></span>|<span data-ttu-id="c7e78-173">Int32</span><span class="sxs-lookup"><span data-stu-id="c7e78-173">Int32</span></span>|<span data-ttu-id="c7e78-174">Minutos de inactividad antes de que sea necesaria una contraseña.</span><span class="sxs-lookup"><span data-stu-id="c7e78-174">Minutes of inactivity before a password is required.</span></span>|
|<span data-ttu-id="c7e78-175">passwordExpirationDays</span><span class="sxs-lookup"><span data-stu-id="c7e78-175">passwordExpirationDays</span></span>|<span data-ttu-id="c7e78-176">Int32</span><span class="sxs-lookup"><span data-stu-id="c7e78-176">Int32</span></span>|<span data-ttu-id="c7e78-177">Número de días antes de que expire la contraseña.</span><span class="sxs-lookup"><span data-stu-id="c7e78-177">Number of days before the password expires.</span></span> <span data-ttu-id="c7e78-178">Valores válidos de 1 a 365</span><span class="sxs-lookup"><span data-stu-id="c7e78-178">Valid values 1 to 365</span></span>|
|<span data-ttu-id="c7e78-179">passwordPreviousPasswordBlockCount</span><span class="sxs-lookup"><span data-stu-id="c7e78-179">passwordPreviousPasswordBlockCount</span></span>|<span data-ttu-id="c7e78-180">Int32</span><span class="sxs-lookup"><span data-stu-id="c7e78-180">Int32</span></span>|<span data-ttu-id="c7e78-181">Número de contraseñas anteriores que bloquear.</span><span class="sxs-lookup"><span data-stu-id="c7e78-181">Number of previous passwords to block.</span></span>|
|<span data-ttu-id="c7e78-182">securityPreventInstallAppsFromUnknownSources</span><span class="sxs-lookup"><span data-stu-id="c7e78-182">securityPreventInstallAppsFromUnknownSources</span></span>|<span data-ttu-id="c7e78-183">Booleano</span><span class="sxs-lookup"><span data-stu-id="c7e78-183">Boolean</span></span>|<span data-ttu-id="c7e78-184">Exigir que los dispositivos impidan la instalación de aplicaciones de orígenes desconocidos.</span><span class="sxs-lookup"><span data-stu-id="c7e78-184">Require that devices disallow installation of apps from unknown sources.</span></span>|
|<span data-ttu-id="c7e78-185">securityDisableUsbDebugging</span><span class="sxs-lookup"><span data-stu-id="c7e78-185">securityDisableUsbDebugging</span></span>|<span data-ttu-id="c7e78-186">Booleano</span><span class="sxs-lookup"><span data-stu-id="c7e78-186">Boolean</span></span>|<span data-ttu-id="c7e78-187">Deshabilitar la depuración USB en dispositivos Android.</span><span class="sxs-lookup"><span data-stu-id="c7e78-187">Disable USB debugging on Android devices.</span></span>|
|<span data-ttu-id="c7e78-188">securityRequireVerifyApps</span><span class="sxs-lookup"><span data-stu-id="c7e78-188">securityRequireVerifyApps</span></span>|<span data-ttu-id="c7e78-189">Booleano</span><span class="sxs-lookup"><span data-stu-id="c7e78-189">Boolean</span></span>|<span data-ttu-id="c7e78-190">Exigir que la característica Verificar aplicaciones de Android esté activada.</span><span class="sxs-lookup"><span data-stu-id="c7e78-190">Require the Android Verify apps feature is turned on.</span></span>|
|<span data-ttu-id="c7e78-191">deviceThreatProtectionEnabled</span><span class="sxs-lookup"><span data-stu-id="c7e78-191">deviceThreatProtectionEnabled</span></span>|<span data-ttu-id="c7e78-192">Booleano</span><span class="sxs-lookup"><span data-stu-id="c7e78-192">Boolean</span></span>|<span data-ttu-id="c7e78-193">Exigir que los dispositivos hayan habilitado la protección contra amenazas de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c7e78-193">Require that devices have enabled device threat protection.</span></span>|
|<span data-ttu-id="c7e78-194">deviceThreatProtectionRequiredSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="c7e78-194">deviceThreatProtectionRequiredSecurityLevel</span></span>|[<span data-ttu-id="c7e78-195">deviceThreatProtectionLevel</span><span class="sxs-lookup"><span data-stu-id="c7e78-195">deviceThreatProtectionLevel</span></span>](../resources/intune-deviceconfig-devicethreatprotectionlevel.md)|<span data-ttu-id="c7e78-196">Exigir que el nivel de riesgo mínimo de Mobile Threat Protection informe del no cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="c7e78-196">Require Mobile Threat Protection minimum risk level to report noncompliance.</span></span> <span data-ttu-id="c7e78-197">Los valores posibles son: `unavailable`, `secured`, `low`, `medium`, `high` y `notSet`.</span><span class="sxs-lookup"><span data-stu-id="c7e78-197">Possible values are: `unavailable`, `secured`, `low`, `medium`, `high`, `notSet`.</span></span>|
|<span data-ttu-id="c7e78-198">securityBlockJailbrokenDevices</span><span class="sxs-lookup"><span data-stu-id="c7e78-198">securityBlockJailbrokenDevices</span></span>|<span data-ttu-id="c7e78-199">Booleano</span><span class="sxs-lookup"><span data-stu-id="c7e78-199">Boolean</span></span>|<span data-ttu-id="c7e78-200">No pueden usarse dispositivos con jailbreak o rooting.</span><span class="sxs-lookup"><span data-stu-id="c7e78-200">Devices must not be jailbroken or rooted.</span></span>|
|<span data-ttu-id="c7e78-201">osMinimumVersion</span><span class="sxs-lookup"><span data-stu-id="c7e78-201">osMinimumVersion</span></span>|<span data-ttu-id="c7e78-202">Cadena</span><span class="sxs-lookup"><span data-stu-id="c7e78-202">String</span></span>|<span data-ttu-id="c7e78-203">Versión mínima de Android.</span><span class="sxs-lookup"><span data-stu-id="c7e78-203">Minimum Android version.</span></span>|
|<span data-ttu-id="c7e78-204">osMaximumVersion</span><span class="sxs-lookup"><span data-stu-id="c7e78-204">osMaximumVersion</span></span>|<span data-ttu-id="c7e78-205">Cadena</span><span class="sxs-lookup"><span data-stu-id="c7e78-205">String</span></span>|<span data-ttu-id="c7e78-206">Versión máxima de Android.</span><span class="sxs-lookup"><span data-stu-id="c7e78-206">Maximum Android version.</span></span>|
|<span data-ttu-id="c7e78-207">minAndroidSecurityPatchLevel</span><span class="sxs-lookup"><span data-stu-id="c7e78-207">minAndroidSecurityPatchLevel</span></span>|<span data-ttu-id="c7e78-208">Cadena</span><span class="sxs-lookup"><span data-stu-id="c7e78-208">String</span></span>|<span data-ttu-id="c7e78-209">Nivel de revisión de seguridad mínimo de Android.</span><span class="sxs-lookup"><span data-stu-id="c7e78-209">Minimum Android security patch level.</span></span>|
|<span data-ttu-id="c7e78-210">storageRequireEncryption</span><span class="sxs-lookup"><span data-stu-id="c7e78-210">storageRequireEncryption</span></span>|<span data-ttu-id="c7e78-211">Booleano</span><span class="sxs-lookup"><span data-stu-id="c7e78-211">Boolean</span></span>|<span data-ttu-id="c7e78-212">Exigir cifrado en dispositivos Android.</span><span class="sxs-lookup"><span data-stu-id="c7e78-212">Require encryption on Android devices.</span></span>|
|<span data-ttu-id="c7e78-213">securityRequireSafetyNetAttestationBasicIntegrity</span><span class="sxs-lookup"><span data-stu-id="c7e78-213">securityRequireSafetyNetAttestationBasicIntegrity</span></span>|<span data-ttu-id="c7e78-214">Booleano</span><span class="sxs-lookup"><span data-stu-id="c7e78-214">Boolean</span></span>|<span data-ttu-id="c7e78-215">Exigir que el dispositivo supere la comprobación de integridad básica de SafetyNet.</span><span class="sxs-lookup"><span data-stu-id="c7e78-215">Require the device to pass the SafetyNet basic integrity check.</span></span>|
|<span data-ttu-id="c7e78-216">securityRequireSafetyNetAttestationCertifiedDevice</span><span class="sxs-lookup"><span data-stu-id="c7e78-216">securityRequireSafetyNetAttestationCertifiedDevice</span></span>|<span data-ttu-id="c7e78-217">Booleano</span><span class="sxs-lookup"><span data-stu-id="c7e78-217">Boolean</span></span>|<span data-ttu-id="c7e78-218">Exigir que el dispositivo supere la comprobación de dispositivos certificados de SafetyNet.</span><span class="sxs-lookup"><span data-stu-id="c7e78-218">Require the device to pass the SafetyNet certified device check.</span></span>|
|<span data-ttu-id="c7e78-219">securityRequireGooglePlayServices</span><span class="sxs-lookup"><span data-stu-id="c7e78-219">securityRequireGooglePlayServices</span></span>|<span data-ttu-id="c7e78-220">Booleano</span><span class="sxs-lookup"><span data-stu-id="c7e78-220">Boolean</span></span>|<span data-ttu-id="c7e78-221">Exigir que Google Play Services esté instalado y habilitado en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c7e78-221">Require Google Play Services to be installed and enabled on the device.</span></span>|
|<span data-ttu-id="c7e78-222">securityRequireUpToDateSecurityProviders</span><span class="sxs-lookup"><span data-stu-id="c7e78-222">securityRequireUpToDateSecurityProviders</span></span>|<span data-ttu-id="c7e78-223">Booleano</span><span class="sxs-lookup"><span data-stu-id="c7e78-223">Boolean</span></span>|<span data-ttu-id="c7e78-224">Exigir que el dispositivo tenga los proveedores de seguridad actualizados.</span><span class="sxs-lookup"><span data-stu-id="c7e78-224">Require the device to have up to date security providers.</span></span> <span data-ttu-id="c7e78-225">El dispositivo requerirá que Google Play Services esté instalado y habilitado.</span><span class="sxs-lookup"><span data-stu-id="c7e78-225">The device will require Google Play Services to be enabled and up to date.</span></span>|
|<span data-ttu-id="c7e78-226">securityRequireCompanyPortalAppIntegrity</span><span class="sxs-lookup"><span data-stu-id="c7e78-226">securityRequireCompanyPortalAppIntegrity</span></span>|<span data-ttu-id="c7e78-227">Booleano</span><span class="sxs-lookup"><span data-stu-id="c7e78-227">Boolean</span></span>|<span data-ttu-id="c7e78-228">Exigir que el dispositivo supere la comprobación de integridad en tiempo de ejecución de la aplicación cliente del Portal de empresa.</span><span class="sxs-lookup"><span data-stu-id="c7e78-228">Require the device to pass the Company Portal client app runtime integrity check.</span></span>|



## <a name="response"></a><span data-ttu-id="c7e78-229">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c7e78-229">Response</span></span>
<span data-ttu-id="c7e78-230">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto actualizado [androidForWorkCompliancePolicy](../resources/intune-deviceconfig-androidforworkcompliancepolicy.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c7e78-230">If successful, this method returns a `200 OK` response code and an updated [androidForWorkCompliancePolicy](../resources/intune-deviceconfig-androidforworkcompliancepolicy.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="c7e78-231">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c7e78-231">Example</span></span>
### <a name="request"></a><span data-ttu-id="c7e78-232">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c7e78-232">Request</span></span>
<span data-ttu-id="c7e78-233">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c7e78-233">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}
Content-type: application/json
Content-length: 1223

{
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
  "securityRequireCompanyPortalAppIntegrity": true
}
```

### <a name="response"></a><span data-ttu-id="c7e78-234">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c7e78-234">Response</span></span>
<span data-ttu-id="c7e78-p115">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="c7e78-p115">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1400

{
  "@odata.type": "#microsoft.graph.androidForWorkCompliancePolicy",
  "roleScopeTagIds": [
    "Role Scope Tag Ids value"
  ],
  "id": "a8d667bd-67bd-a8d6-bd67-d6a8bd67d6a8",
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





