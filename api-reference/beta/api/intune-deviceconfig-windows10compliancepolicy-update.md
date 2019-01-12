---
title: Actualizar windows10CompliancePolicy
description: Actualice las propiedades de un objeto windows10CompliancePolicy.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: fb689181fdc22e34bb5b85ee42c1f38e4a26905a
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27970146"
---
# <a name="update-windows10compliancepolicy"></a><span data-ttu-id="8261f-103">Actualizar windows10CompliancePolicy</span><span class="sxs-lookup"><span data-stu-id="8261f-103">Update windows10CompliancePolicy</span></span>

> <span data-ttu-id="8261f-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="8261f-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="8261f-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="8261f-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="8261f-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="8261f-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="8261f-107">Actualice las propiedades de un objeto [windows10CompliancePolicy](../resources/intune-deviceconfig-windows10compliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="8261f-107">Update the properties of a [windows10CompliancePolicy](../resources/intune-deviceconfig-windows10compliancepolicy.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="8261f-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="8261f-108">Prerequisites</span></span>
<span data-ttu-id="8261f-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="8261f-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="8261f-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="8261f-111">Permission type</span></span>|<span data-ttu-id="8261f-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="8261f-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="8261f-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="8261f-113">Delegated (work or school account)</span></span>|<span data-ttu-id="8261f-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="8261f-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="8261f-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="8261f-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="8261f-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8261f-116">Not supported.</span></span>|
|<span data-ttu-id="8261f-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="8261f-117">Application</span></span>|<span data-ttu-id="8261f-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8261f-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="8261f-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="8261f-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}
```

## <a name="request-headers"></a><span data-ttu-id="8261f-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="8261f-120">Request headers</span></span>
|<span data-ttu-id="8261f-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8261f-121">Header</span></span>|<span data-ttu-id="8261f-122">Valor</span><span class="sxs-lookup"><span data-stu-id="8261f-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="8261f-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="8261f-123">Authorization</span></span>|<span data-ttu-id="8261f-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="8261f-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="8261f-125">Accept</span><span class="sxs-lookup"><span data-stu-id="8261f-125">Accept</span></span>|<span data-ttu-id="8261f-126">application/json</span><span class="sxs-lookup"><span data-stu-id="8261f-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="8261f-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="8261f-127">Request body</span></span>
<span data-ttu-id="8261f-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto [windows10CompliancePolicy](../resources/intune-deviceconfig-windows10compliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="8261f-128">In the request body, supply a JSON representation for the [windows10CompliancePolicy](../resources/intune-deviceconfig-windows10compliancepolicy.md) object.</span></span>

<span data-ttu-id="8261f-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [windows10CompliancePolicy](../resources/intune-deviceconfig-windows10compliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="8261f-129">The following table shows the properties that are required when you create the [windows10CompliancePolicy](../resources/intune-deviceconfig-windows10compliancepolicy.md).</span></span>

|<span data-ttu-id="8261f-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="8261f-130">Property</span></span>|<span data-ttu-id="8261f-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="8261f-131">Type</span></span>|<span data-ttu-id="8261f-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="8261f-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="8261f-133">roleScopeTagIds</span><span class="sxs-lookup"><span data-stu-id="8261f-133">roleScopeTagIds</span></span>|<span data-ttu-id="8261f-134">Colección String</span><span class="sxs-lookup"><span data-stu-id="8261f-134">String collection</span></span>|<span data-ttu-id="8261f-135">Lista de etiquetas de ámbito para esta instancia de entidad.</span><span class="sxs-lookup"><span data-stu-id="8261f-135">List of Scope Tags for this Entity instance.</span></span> <span data-ttu-id="8261f-136">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="8261f-136">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="8261f-137">id</span><span class="sxs-lookup"><span data-stu-id="8261f-137">id</span></span>|<span data-ttu-id="8261f-138">Cadena</span><span class="sxs-lookup"><span data-stu-id="8261f-138">String</span></span>|<span data-ttu-id="8261f-139">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="8261f-139">Key of the entity.</span></span> <span data-ttu-id="8261f-140">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="8261f-140">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="8261f-141">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="8261f-141">createdDateTime</span></span>|<span data-ttu-id="8261f-142">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="8261f-142">DateTimeOffset</span></span>|<span data-ttu-id="8261f-143">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="8261f-143">DateTime the object was created.</span></span> <span data-ttu-id="8261f-144">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="8261f-144">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="8261f-145">descripción</span><span class="sxs-lookup"><span data-stu-id="8261f-145">description</span></span>|<span data-ttu-id="8261f-146">Cadena</span><span class="sxs-lookup"><span data-stu-id="8261f-146">String</span></span>|<span data-ttu-id="8261f-147">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8261f-147">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="8261f-148">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="8261f-148">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="8261f-149">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="8261f-149">lastModifiedDateTime</span></span>|<span data-ttu-id="8261f-150">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="8261f-150">DateTimeOffset</span></span>|<span data-ttu-id="8261f-151">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="8261f-151">DateTime the object was last modified.</span></span> <span data-ttu-id="8261f-152">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="8261f-152">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="8261f-153">displayName</span><span class="sxs-lookup"><span data-stu-id="8261f-153">displayName</span></span>|<span data-ttu-id="8261f-154">Cadena</span><span class="sxs-lookup"><span data-stu-id="8261f-154">String</span></span>|<span data-ttu-id="8261f-155">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8261f-155">Admin provided name of the device configuration.</span></span> <span data-ttu-id="8261f-156">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="8261f-156">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="8261f-157">version</span><span class="sxs-lookup"><span data-stu-id="8261f-157">version</span></span>|<span data-ttu-id="8261f-158">Int32</span><span class="sxs-lookup"><span data-stu-id="8261f-158">Int32</span></span>|<span data-ttu-id="8261f-159">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8261f-159">Version of the device configuration.</span></span> <span data-ttu-id="8261f-160">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="8261f-160">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="8261f-161">passwordRequired</span><span class="sxs-lookup"><span data-stu-id="8261f-161">passwordRequired</span></span>|<span data-ttu-id="8261f-162">Booleano</span><span class="sxs-lookup"><span data-stu-id="8261f-162">Boolean</span></span>|<span data-ttu-id="8261f-163">Exige una contraseña para desbloquear el dispositivo Windows.</span><span class="sxs-lookup"><span data-stu-id="8261f-163">Require a password to unlock Windows device.</span></span>|
|<span data-ttu-id="8261f-164">passwordBlockSimple</span><span class="sxs-lookup"><span data-stu-id="8261f-164">passwordBlockSimple</span></span>|<span data-ttu-id="8261f-165">Booleano</span><span class="sxs-lookup"><span data-stu-id="8261f-165">Boolean</span></span>|<span data-ttu-id="8261f-166">Indica si quiere bloquear o no la contraseña simple.</span><span class="sxs-lookup"><span data-stu-id="8261f-166">Indicates whether or not to block simple password.</span></span>|
|<span data-ttu-id="8261f-167">passwordRequiredToUnlockFromIdle</span><span class="sxs-lookup"><span data-stu-id="8261f-167">passwordRequiredToUnlockFromIdle</span></span>|<span data-ttu-id="8261f-168">Booleano</span><span class="sxs-lookup"><span data-stu-id="8261f-168">Boolean</span></span>|<span data-ttu-id="8261f-169">Exige una contraseña para desbloquear el dispositivo inactivo.</span><span class="sxs-lookup"><span data-stu-id="8261f-169">Require a password to unlock an idle device.</span></span>|
|<span data-ttu-id="8261f-170">passwordMinutesOfInactivityBeforeLock</span><span class="sxs-lookup"><span data-stu-id="8261f-170">passwordMinutesOfInactivityBeforeLock</span></span>|<span data-ttu-id="8261f-171">Int32</span><span class="sxs-lookup"><span data-stu-id="8261f-171">Int32</span></span>|<span data-ttu-id="8261f-172">Minutos de inactividad antes de que sea necesaria una contraseña.</span><span class="sxs-lookup"><span data-stu-id="8261f-172">Minutes of inactivity before a password is required.</span></span>|
|<span data-ttu-id="8261f-173">passwordExpirationDays</span><span class="sxs-lookup"><span data-stu-id="8261f-173">passwordExpirationDays</span></span>|<span data-ttu-id="8261f-174">Int32</span><span class="sxs-lookup"><span data-stu-id="8261f-174">Int32</span></span>|<span data-ttu-id="8261f-175">La expiración de la contraseña en días.</span><span class="sxs-lookup"><span data-stu-id="8261f-175">The password expiration in days.</span></span>|
|<span data-ttu-id="8261f-176">passwordMinimumLength</span><span class="sxs-lookup"><span data-stu-id="8261f-176">passwordMinimumLength</span></span>|<span data-ttu-id="8261f-177">Int32</span><span class="sxs-lookup"><span data-stu-id="8261f-177">Int32</span></span>|<span data-ttu-id="8261f-178">La longitud mínima de contraseña.</span><span class="sxs-lookup"><span data-stu-id="8261f-178">The minimum password length.</span></span>|
|<span data-ttu-id="8261f-179">passwordMinimumCharacterSetCount</span><span class="sxs-lookup"><span data-stu-id="8261f-179">passwordMinimumCharacterSetCount</span></span>|<span data-ttu-id="8261f-180">Int32</span><span class="sxs-lookup"><span data-stu-id="8261f-180">Int32</span></span>|<span data-ttu-id="8261f-181">Número de juegos de caracteres necesarios en la contraseña.</span><span class="sxs-lookup"><span data-stu-id="8261f-181">The number of character sets required in the password.</span></span>|
|<span data-ttu-id="8261f-182">passwordRequiredType</span><span class="sxs-lookup"><span data-stu-id="8261f-182">passwordRequiredType</span></span>|[<span data-ttu-id="8261f-183">requiredPasswordType</span><span class="sxs-lookup"><span data-stu-id="8261f-183">requiredPasswordType</span></span>](../resources/intune-deviceconfig-requiredpasswordtype.md)|<span data-ttu-id="8261f-184">Tipo de contraseña necesaria.</span><span class="sxs-lookup"><span data-stu-id="8261f-184">The required password type.</span></span> <span data-ttu-id="8261f-185">Los valores posibles son: `deviceDefault`, `alphanumeric` y `numeric`.</span><span class="sxs-lookup"><span data-stu-id="8261f-185">Possible values are: `deviceDefault`, `alphanumeric`, `numeric`.</span></span>|
|<span data-ttu-id="8261f-186">passwordPreviousPasswordBlockCount</span><span class="sxs-lookup"><span data-stu-id="8261f-186">passwordPreviousPasswordBlockCount</span></span>|<span data-ttu-id="8261f-187">Int32</span><span class="sxs-lookup"><span data-stu-id="8261f-187">Int32</span></span>|<span data-ttu-id="8261f-188">Número de contraseñas anteriores que impide su reutilización.</span><span class="sxs-lookup"><span data-stu-id="8261f-188">The number of previous passwords to prevent re-use of.</span></span>|
|<span data-ttu-id="8261f-189">requireHealthyDeviceReport</span><span class="sxs-lookup"><span data-stu-id="8261f-189">requireHealthyDeviceReport</span></span>|<span data-ttu-id="8261f-190">Booleano</span><span class="sxs-lookup"><span data-stu-id="8261f-190">Boolean</span></span>|<span data-ttu-id="8261f-191">Exige que la atestación de estado de dispositivo Windows notifique los dispositivos como correctos.</span><span class="sxs-lookup"><span data-stu-id="8261f-191">Require devices to be reported as healthy by Windows Device Health Attestation.</span></span>|
|<span data-ttu-id="8261f-192">osMinimumVersion</span><span class="sxs-lookup"><span data-stu-id="8261f-192">osMinimumVersion</span></span>|<span data-ttu-id="8261f-193">Cadena</span><span class="sxs-lookup"><span data-stu-id="8261f-193">String</span></span>|<span data-ttu-id="8261f-194">Versión mínima de Windows 10.</span><span class="sxs-lookup"><span data-stu-id="8261f-194">Minimum Windows 10 version.</span></span>|
|<span data-ttu-id="8261f-195">osMaximumVersion</span><span class="sxs-lookup"><span data-stu-id="8261f-195">osMaximumVersion</span></span>|<span data-ttu-id="8261f-196">Cadena</span><span class="sxs-lookup"><span data-stu-id="8261f-196">String</span></span>|<span data-ttu-id="8261f-197">Versión máxima de Windows 10.</span><span class="sxs-lookup"><span data-stu-id="8261f-197">Maximum Windows 10 version.</span></span>|
|<span data-ttu-id="8261f-198">mobileOsMinimumVersion</span><span class="sxs-lookup"><span data-stu-id="8261f-198">mobileOsMinimumVersion</span></span>|<span data-ttu-id="8261f-199">Cadena</span><span class="sxs-lookup"><span data-stu-id="8261f-199">String</span></span>|<span data-ttu-id="8261f-200">Versión mínima de Windows Phone.</span><span class="sxs-lookup"><span data-stu-id="8261f-200">Minimum Windows Phone version.</span></span>|
|<span data-ttu-id="8261f-201">mobileOsMaximumVersion</span><span class="sxs-lookup"><span data-stu-id="8261f-201">mobileOsMaximumVersion</span></span>|<span data-ttu-id="8261f-202">Cadena</span><span class="sxs-lookup"><span data-stu-id="8261f-202">String</span></span>|<span data-ttu-id="8261f-203">Versión máxima de Windows Phone.</span><span class="sxs-lookup"><span data-stu-id="8261f-203">Maximum Windows Phone version.</span></span>|
|<span data-ttu-id="8261f-204">earlyLaunchAntiMalwareDriverEnabled</span><span class="sxs-lookup"><span data-stu-id="8261f-204">earlyLaunchAntiMalwareDriverEnabled</span></span>|<span data-ttu-id="8261f-205">Booleano</span><span class="sxs-lookup"><span data-stu-id="8261f-205">Boolean</span></span>|<span data-ttu-id="8261f-206">Exige que la atestación de estado de dispositivo Windows notifique los dispositivos como correctos; el controlador antimalware de inicio temprano está habilitado.</span><span class="sxs-lookup"><span data-stu-id="8261f-206">Require devices to be reported as healthy by Windows Device Health Attestation - early launch antimalware driver is enabled.</span></span>|
|<span data-ttu-id="8261f-207">bitLockerEnabled</span><span class="sxs-lookup"><span data-stu-id="8261f-207">bitLockerEnabled</span></span>|<span data-ttu-id="8261f-208">Booleano</span><span class="sxs-lookup"><span data-stu-id="8261f-208">Boolean</span></span>|<span data-ttu-id="8261f-209">Exige que la atestación de estado de dispositivo Windows notifique los dispositivos como correctos; BitLocker está habilitado.</span><span class="sxs-lookup"><span data-stu-id="8261f-209">Require devices to be reported healthy by Windows Device Health Attestation - bit locker is enabled</span></span>|
|<span data-ttu-id="8261f-210">secureBootEnabled</span><span class="sxs-lookup"><span data-stu-id="8261f-210">secureBootEnabled</span></span>|<span data-ttu-id="8261f-211">Booleano</span><span class="sxs-lookup"><span data-stu-id="8261f-211">Boolean</span></span>|<span data-ttu-id="8261f-212">Exige que la atestación de estado de dispositivo Windows notifique los dispositivos como correctos; el arranque seguro está habilitado.</span><span class="sxs-lookup"><span data-stu-id="8261f-212">Require devices to be reported as healthy by Windows Device Health Attestation - secure boot is enabled.</span></span>|
|<span data-ttu-id="8261f-213">codeIntegrityEnabled</span><span class="sxs-lookup"><span data-stu-id="8261f-213">codeIntegrityEnabled</span></span>|<span data-ttu-id="8261f-214">Booleano</span><span class="sxs-lookup"><span data-stu-id="8261f-214">Boolean</span></span>|<span data-ttu-id="8261f-215">Exige que la atestación de estado de dispositivo Windows notifique los dispositivos como correctos.</span><span class="sxs-lookup"><span data-stu-id="8261f-215">Require devices to be reported as healthy by Windows Device Health Attestation.</span></span>|
|<span data-ttu-id="8261f-216">storageRequireEncryption</span><span class="sxs-lookup"><span data-stu-id="8261f-216">storageRequireEncryption</span></span>|<span data-ttu-id="8261f-217">Booleano</span><span class="sxs-lookup"><span data-stu-id="8261f-217">Boolean</span></span>|<span data-ttu-id="8261f-218">Exige el cifrado en dispositivos Windows.</span><span class="sxs-lookup"><span data-stu-id="8261f-218">Require encryption on windows devices.</span></span>|
|<span data-ttu-id="8261f-219">activeFirewallRequired</span><span class="sxs-lookup"><span data-stu-id="8261f-219">activeFirewallRequired</span></span>|<span data-ttu-id="8261f-220">Booleano</span><span class="sxs-lookup"><span data-stu-id="8261f-220">Boolean</span></span>|<span data-ttu-id="8261f-221">Requiere un servidor de seguridad activo en los dispositivos de Windows.</span><span class="sxs-lookup"><span data-stu-id="8261f-221">Require active firewall on Windows devices.</span></span>|
|<span data-ttu-id="8261f-222">defenderEnabled</span><span class="sxs-lookup"><span data-stu-id="8261f-222">defenderEnabled</span></span>|<span data-ttu-id="8261f-223">Booleano</span><span class="sxs-lookup"><span data-stu-id="8261f-223">Boolean</span></span>|<span data-ttu-id="8261f-224">Requieren Windows Defender Antimalware en los dispositivos de Windows.</span><span class="sxs-lookup"><span data-stu-id="8261f-224">Require Windows Defender Antimalware on Windows devices.</span></span>|
|<span data-ttu-id="8261f-225">defenderVersion</span><span class="sxs-lookup"><span data-stu-id="8261f-225">defenderVersion</span></span>|<span data-ttu-id="8261f-226">Cadena</span><span class="sxs-lookup"><span data-stu-id="8261f-226">String</span></span>|<span data-ttu-id="8261f-227">Requiere la versión mínima de Windows Defender Antimalware en los dispositivos de Windows.</span><span class="sxs-lookup"><span data-stu-id="8261f-227">Require Windows Defender Antimalware minimum version on Windows devices.</span></span>|
|<span data-ttu-id="8261f-228">signatureOutOfDate</span><span class="sxs-lookup"><span data-stu-id="8261f-228">signatureOutOfDate</span></span>|<span data-ttu-id="8261f-229">Booleano</span><span class="sxs-lookup"><span data-stu-id="8261f-229">Boolean</span></span>|<span data-ttu-id="8261f-230">Requieren Windows Defender Antimalware firma ser actualizados en los dispositivos de Windows.</span><span class="sxs-lookup"><span data-stu-id="8261f-230">Require Windows Defender Antimalware Signature to be up to date on Windows devices.</span></span>|
|<span data-ttu-id="8261f-231">rtpEnabled</span><span class="sxs-lookup"><span data-stu-id="8261f-231">rtpEnabled</span></span>|<span data-ttu-id="8261f-232">Booleano</span><span class="sxs-lookup"><span data-stu-id="8261f-232">Boolean</span></span>|<span data-ttu-id="8261f-233">Requerir protección en tiempo real de Windows Defender Antimalware en los dispositivos de Windows.</span><span class="sxs-lookup"><span data-stu-id="8261f-233">Require Windows Defender Antimalware Real-Time Protection on Windows devices.</span></span>|
|<span data-ttu-id="8261f-234">antivirusRequired</span><span class="sxs-lookup"><span data-stu-id="8261f-234">antivirusRequired</span></span>|<span data-ttu-id="8261f-235">Booleano</span><span class="sxs-lookup"><span data-stu-id="8261f-235">Boolean</span></span>|<span data-ttu-id="8261f-236">Requieren cualquier solución Antivirus registrado con el centro de seguridad de Windows que esté en y supervisión (por ejemplo, Symantec, Windows Defender).</span><span class="sxs-lookup"><span data-stu-id="8261f-236">Require any Antivirus solution registered with Windows Decurity Center to be on and monitoring (e.g. Symantec, Windows Defender).</span></span>|
|<span data-ttu-id="8261f-237">antiSpywareRequired</span><span class="sxs-lookup"><span data-stu-id="8261f-237">antiSpywareRequired</span></span>|<span data-ttu-id="8261f-238">Booleano</span><span class="sxs-lookup"><span data-stu-id="8261f-238">Boolean</span></span>|<span data-ttu-id="8261f-239">Requieren cualquier solución de anti spyware registrado con el centro de seguridad de Windows que esté en y supervisión (por ejemplo, Symantec, Windows Defender).</span><span class="sxs-lookup"><span data-stu-id="8261f-239">Require any AntiSpyware solution registered with Windows Decurity Center to be on and monitoring (e.g. Symantec, Windows Defender).</span></span>|
|<span data-ttu-id="8261f-240">validOperatingSystemBuildRanges</span><span class="sxs-lookup"><span data-stu-id="8261f-240">validOperatingSystemBuildRanges</span></span>|<span data-ttu-id="8261f-241">colección de [operatingSystemVersionRange](../resources/intune-deviceconfig-operatingsystemversionrange.md)</span><span class="sxs-lookup"><span data-stu-id="8261f-241">[operatingSystemVersionRange](../resources/intune-deviceconfig-operatingsystemversionrange.md) collection</span></span>|<span data-ttu-id="8261f-242">El sistema operativo válido crear rangos en los dispositivos de Windows.</span><span class="sxs-lookup"><span data-stu-id="8261f-242">The valid operating system build ranges on Windows devices.</span></span> <span data-ttu-id="8261f-243">Esta colección puede contener un máximo de 10 000 elementos.</span><span class="sxs-lookup"><span data-stu-id="8261f-243">This collection can contain a maximum of 10000 elements.</span></span>|
|<span data-ttu-id="8261f-244">deviceThreatProtectionEnabled</span><span class="sxs-lookup"><span data-stu-id="8261f-244">deviceThreatProtectionEnabled</span></span>|<span data-ttu-id="8261f-245">Booleano</span><span class="sxs-lookup"><span data-stu-id="8261f-245">Boolean</span></span>|<span data-ttu-id="8261f-246">Exigir que los dispositivos hayan habilitado la protección contra amenazas de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8261f-246">Require that devices have enabled device threat protection.</span></span>|
|<span data-ttu-id="8261f-247">deviceThreatProtectionRequiredSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="8261f-247">deviceThreatProtectionRequiredSecurityLevel</span></span>|[<span data-ttu-id="8261f-248">deviceThreatProtectionLevel</span><span class="sxs-lookup"><span data-stu-id="8261f-248">deviceThreatProtectionLevel</span></span>](../resources/intune-deviceconfig-devicethreatprotectionlevel.md)|<span data-ttu-id="8261f-249">Requieren el nivel de riesgo mínimo de protección contra amenazas de dispositivo para informar de incumplimiento.</span><span class="sxs-lookup"><span data-stu-id="8261f-249">Require Device Threat Protection minimum risk level to report noncompliance.</span></span> <span data-ttu-id="8261f-250">Los valores posibles son: `unavailable`, `secured`, `low`, `medium`, `high`, `notSet`.</span><span class="sxs-lookup"><span data-stu-id="8261f-250">Possible values are: `unavailable`, `secured`, `low`, `medium`, `high`, `notSet`.</span></span>|
|<span data-ttu-id="8261f-251">configurationManagerComplianceRequired</span><span class="sxs-lookup"><span data-stu-id="8261f-251">configurationManagerComplianceRequired</span></span>|<span data-ttu-id="8261f-252">Booleano</span><span class="sxs-lookup"><span data-stu-id="8261f-252">Boolean</span></span>|<span data-ttu-id="8261f-253">Se requieren para tener en cuenta el estado de cumplimiento de SCCM en cuenta para el estado de cumplimiento Intune.</span><span class="sxs-lookup"><span data-stu-id="8261f-253">Require to consider SCCM Compliance state into consideration for Intune Compliance State.</span></span>|



## <a name="response"></a><span data-ttu-id="8261f-254">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8261f-254">Response</span></span>
<span data-ttu-id="8261f-255">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [windows10CompliancePolicy](../resources/intune-deviceconfig-windows10compliancepolicy.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8261f-255">If successful, this method returns a `200 OK` response code and an updated [windows10CompliancePolicy](../resources/intune-deviceconfig-windows10compliancepolicy.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="8261f-256">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="8261f-256">Example</span></span>
### <a name="request"></a><span data-ttu-id="8261f-257">Solicitud</span><span class="sxs-lookup"><span data-stu-id="8261f-257">Request</span></span>
<span data-ttu-id="8261f-258">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="8261f-258">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}
Content-type: application/json
Content-length: 1666

{
  "roleScopeTagIds": [
    "Role Scope Tag Ids value"
  ],
  "description": "Description value",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "displayName": "Display Name value",
  "version": 7,
  "passwordRequired": true,
  "passwordBlockSimple": true,
  "passwordRequiredToUnlockFromIdle": true,
  "passwordMinutesOfInactivityBeforeLock": 5,
  "passwordExpirationDays": 6,
  "passwordMinimumLength": 5,
  "passwordMinimumCharacterSetCount": 0,
  "passwordRequiredType": "alphanumeric",
  "passwordPreviousPasswordBlockCount": 2,
  "requireHealthyDeviceReport": true,
  "osMinimumVersion": "Os Minimum Version value",
  "osMaximumVersion": "Os Maximum Version value",
  "mobileOsMinimumVersion": "Mobile Os Minimum Version value",
  "mobileOsMaximumVersion": "Mobile Os Maximum Version value",
  "earlyLaunchAntiMalwareDriverEnabled": true,
  "bitLockerEnabled": true,
  "secureBootEnabled": true,
  "codeIntegrityEnabled": true,
  "storageRequireEncryption": true,
  "activeFirewallRequired": true,
  "defenderEnabled": true,
  "defenderVersion": "Defender Version value",
  "signatureOutOfDate": true,
  "rtpEnabled": true,
  "antivirusRequired": true,
  "antiSpywareRequired": true,
  "validOperatingSystemBuildRanges": [
    {
      "@odata.type": "microsoft.graph.operatingSystemVersionRange",
      "description": "Description value",
      "lowestVersion": "Lowest Version value",
      "highestVersion": "Highest Version value"
    }
  ],
  "deviceThreatProtectionEnabled": true,
  "deviceThreatProtectionRequiredSecurityLevel": "secured",
  "configurationManagerComplianceRequired": true
}
```

### <a name="response"></a><span data-ttu-id="8261f-259">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8261f-259">Response</span></span>
<span data-ttu-id="8261f-p113">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="8261f-p113">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1838

{
  "@odata.type": "#microsoft.graph.windows10CompliancePolicy",
  "roleScopeTagIds": [
    "Role Scope Tag Ids value"
  ],
  "id": "2919ae62-ae62-2919-62ae-192962ae1929",
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "description": "Description value",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "displayName": "Display Name value",
  "version": 7,
  "passwordRequired": true,
  "passwordBlockSimple": true,
  "passwordRequiredToUnlockFromIdle": true,
  "passwordMinutesOfInactivityBeforeLock": 5,
  "passwordExpirationDays": 6,
  "passwordMinimumLength": 5,
  "passwordMinimumCharacterSetCount": 0,
  "passwordRequiredType": "alphanumeric",
  "passwordPreviousPasswordBlockCount": 2,
  "requireHealthyDeviceReport": true,
  "osMinimumVersion": "Os Minimum Version value",
  "osMaximumVersion": "Os Maximum Version value",
  "mobileOsMinimumVersion": "Mobile Os Minimum Version value",
  "mobileOsMaximumVersion": "Mobile Os Maximum Version value",
  "earlyLaunchAntiMalwareDriverEnabled": true,
  "bitLockerEnabled": true,
  "secureBootEnabled": true,
  "codeIntegrityEnabled": true,
  "storageRequireEncryption": true,
  "activeFirewallRequired": true,
  "defenderEnabled": true,
  "defenderVersion": "Defender Version value",
  "signatureOutOfDate": true,
  "rtpEnabled": true,
  "antivirusRequired": true,
  "antiSpywareRequired": true,
  "validOperatingSystemBuildRanges": [
    {
      "@odata.type": "microsoft.graph.operatingSystemVersionRange",
      "description": "Description value",
      "lowestVersion": "Lowest Version value",
      "highestVersion": "Highest Version value"
    }
  ],
  "deviceThreatProtectionEnabled": true,
  "deviceThreatProtectionRequiredSecurityLevel": "secured",
  "configurationManagerComplianceRequired": true
}
```





