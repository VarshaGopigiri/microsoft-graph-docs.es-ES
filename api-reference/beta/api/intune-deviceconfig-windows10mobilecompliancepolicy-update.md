---
title: Actualizar windows10MobileCompliancePolicy
description: Actualice las propiedades de un objeto windows10MobileCompliancePolicy.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 3956af618a5d6ed52e5385a0d09b4326ac9ef367
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27849451"
---
# <a name="update-windows10mobilecompliancepolicy"></a><span data-ttu-id="b9419-103">Actualizar windows10MobileCompliancePolicy</span><span class="sxs-lookup"><span data-stu-id="b9419-103">Update windows10MobileCompliancePolicy</span></span>

> <span data-ttu-id="b9419-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="b9419-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="b9419-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="b9419-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="b9419-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="b9419-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="b9419-107">Actualice las propiedades de un objeto [windows10MobileCompliancePolicy](../resources/intune-deviceconfig-windows10mobilecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="b9419-107">Update the properties of a [windows10MobileCompliancePolicy](../resources/intune-deviceconfig-windows10mobilecompliancepolicy.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="b9419-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="b9419-108">Prerequisites</span></span>
<span data-ttu-id="b9419-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="b9419-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="b9419-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b9419-111">Permission type</span></span>|<span data-ttu-id="b9419-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b9419-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="b9419-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b9419-113">Delegated (work or school account)</span></span>|<span data-ttu-id="b9419-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="b9419-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="b9419-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b9419-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="b9419-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b9419-116">Not supported.</span></span>|
|<span data-ttu-id="b9419-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b9419-117">Application</span></span>|<span data-ttu-id="b9419-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b9419-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="b9419-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b9419-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}
```

## <a name="request-headers"></a><span data-ttu-id="b9419-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b9419-120">Request headers</span></span>
|<span data-ttu-id="b9419-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b9419-121">Header</span></span>|<span data-ttu-id="b9419-122">Valor</span><span class="sxs-lookup"><span data-stu-id="b9419-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="b9419-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="b9419-123">Authorization</span></span>|<span data-ttu-id="b9419-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="b9419-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="b9419-125">Accept</span><span class="sxs-lookup"><span data-stu-id="b9419-125">Accept</span></span>|<span data-ttu-id="b9419-126">application/json</span><span class="sxs-lookup"><span data-stu-id="b9419-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="b9419-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b9419-127">Request body</span></span>
<span data-ttu-id="b9419-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto [windows10MobileCompliancePolicy](../resources/intune-deviceconfig-windows10mobilecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="b9419-128">In the request body, supply a JSON representation for the [windows10MobileCompliancePolicy](../resources/intune-deviceconfig-windows10mobilecompliancepolicy.md) object.</span></span>

<span data-ttu-id="b9419-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [windows10MobileCompliancePolicy](../resources/intune-deviceconfig-windows10mobilecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="b9419-129">The following table shows the properties that are required when you create the [windows10MobileCompliancePolicy](../resources/intune-deviceconfig-windows10mobilecompliancepolicy.md).</span></span>

|<span data-ttu-id="b9419-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="b9419-130">Property</span></span>|<span data-ttu-id="b9419-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="b9419-131">Type</span></span>|<span data-ttu-id="b9419-132">Description</span><span class="sxs-lookup"><span data-stu-id="b9419-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="b9419-133">roleScopeTagIds</span><span class="sxs-lookup"><span data-stu-id="b9419-133">roleScopeTagIds</span></span>|<span data-ttu-id="b9419-134">Colección String</span><span class="sxs-lookup"><span data-stu-id="b9419-134">String collection</span></span>|<span data-ttu-id="b9419-135">Lista de etiquetas de ámbito para esta instancia de entidad.</span><span class="sxs-lookup"><span data-stu-id="b9419-135">List of Scope Tags for this Entity instance.</span></span> <span data-ttu-id="b9419-136">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="b9419-136">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="b9419-137">id</span><span class="sxs-lookup"><span data-stu-id="b9419-137">id</span></span>|<span data-ttu-id="b9419-138">Cadena</span><span class="sxs-lookup"><span data-stu-id="b9419-138">String</span></span>|<span data-ttu-id="b9419-139">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="b9419-139">Key of the entity.</span></span> <span data-ttu-id="b9419-140">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="b9419-140">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="b9419-141">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="b9419-141">createdDateTime</span></span>|<span data-ttu-id="b9419-142">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="b9419-142">DateTimeOffset</span></span>|<span data-ttu-id="b9419-143">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="b9419-143">DateTime the object was created.</span></span> <span data-ttu-id="b9419-144">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="b9419-144">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="b9419-145">descripción</span><span class="sxs-lookup"><span data-stu-id="b9419-145">description</span></span>|<span data-ttu-id="b9419-146">Cadena</span><span class="sxs-lookup"><span data-stu-id="b9419-146">String</span></span>|<span data-ttu-id="b9419-147">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b9419-147">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="b9419-148">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="b9419-148">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="b9419-149">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="b9419-149">lastModifiedDateTime</span></span>|<span data-ttu-id="b9419-150">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="b9419-150">DateTimeOffset</span></span>|<span data-ttu-id="b9419-151">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="b9419-151">DateTime the object was last modified.</span></span> <span data-ttu-id="b9419-152">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="b9419-152">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="b9419-153">displayName</span><span class="sxs-lookup"><span data-stu-id="b9419-153">displayName</span></span>|<span data-ttu-id="b9419-154">Cadena</span><span class="sxs-lookup"><span data-stu-id="b9419-154">String</span></span>|<span data-ttu-id="b9419-155">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b9419-155">Admin provided name of the device configuration.</span></span> <span data-ttu-id="b9419-156">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="b9419-156">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="b9419-157">version</span><span class="sxs-lookup"><span data-stu-id="b9419-157">version</span></span>|<span data-ttu-id="b9419-158">Int32</span><span class="sxs-lookup"><span data-stu-id="b9419-158">Int32</span></span>|<span data-ttu-id="b9419-159">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b9419-159">Version of the device configuration.</span></span> <span data-ttu-id="b9419-160">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="b9419-160">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="b9419-161">passwordRequired</span><span class="sxs-lookup"><span data-stu-id="b9419-161">passwordRequired</span></span>|<span data-ttu-id="b9419-162">Booleano</span><span class="sxs-lookup"><span data-stu-id="b9419-162">Boolean</span></span>|<span data-ttu-id="b9419-163">Exigir una contraseña para desbloquear el dispositivo de Windows Phone.</span><span class="sxs-lookup"><span data-stu-id="b9419-163">Require a password to unlock Windows Phone device.</span></span>|
|<span data-ttu-id="b9419-164">passwordBlockSimple</span><span class="sxs-lookup"><span data-stu-id="b9419-164">passwordBlockSimple</span></span>|<span data-ttu-id="b9419-165">Booleano</span><span class="sxs-lookup"><span data-stu-id="b9419-165">Boolean</span></span>|<span data-ttu-id="b9419-166">Si quiere bloquear o no la sincronización del calendario.</span><span class="sxs-lookup"><span data-stu-id="b9419-166">Whether or not to block syncing the calendar.</span></span>|
|<span data-ttu-id="b9419-167">passwordMinimumLength</span><span class="sxs-lookup"><span data-stu-id="b9419-167">passwordMinimumLength</span></span>|<span data-ttu-id="b9419-168">Int32</span><span class="sxs-lookup"><span data-stu-id="b9419-168">Int32</span></span>|<span data-ttu-id="b9419-169">Longitud mínima de la contraseña.</span><span class="sxs-lookup"><span data-stu-id="b9419-169">Minimum password length.</span></span> <span data-ttu-id="b9419-170">Valores válidos de 4 a 16</span><span class="sxs-lookup"><span data-stu-id="b9419-170">Valid values 4 to 16</span></span>|
|<span data-ttu-id="b9419-171">passwordMinimumCharacterSetCount</span><span class="sxs-lookup"><span data-stu-id="b9419-171">passwordMinimumCharacterSetCount</span></span>|<span data-ttu-id="b9419-172">Int32</span><span class="sxs-lookup"><span data-stu-id="b9419-172">Int32</span></span>|<span data-ttu-id="b9419-173">Número de juegos de caracteres necesarios en la contraseña.</span><span class="sxs-lookup"><span data-stu-id="b9419-173">The number of character sets required in the password.</span></span>|
|<span data-ttu-id="b9419-174">passwordRequiredType</span><span class="sxs-lookup"><span data-stu-id="b9419-174">passwordRequiredType</span></span>|[<span data-ttu-id="b9419-175">requiredPasswordType</span><span class="sxs-lookup"><span data-stu-id="b9419-175">requiredPasswordType</span></span>](../resources/intune-deviceconfig-requiredpasswordtype.md)|<span data-ttu-id="b9419-176">Tipo de contraseña necesaria.</span><span class="sxs-lookup"><span data-stu-id="b9419-176">The required password type.</span></span> <span data-ttu-id="b9419-177">Los valores posibles son: `deviceDefault`, `alphanumeric` y `numeric`.</span><span class="sxs-lookup"><span data-stu-id="b9419-177">Possible values are: `deviceDefault`, `alphanumeric`, `numeric`.</span></span>|
|<span data-ttu-id="b9419-178">passwordPreviousPasswordBlockCount</span><span class="sxs-lookup"><span data-stu-id="b9419-178">passwordPreviousPasswordBlockCount</span></span>|<span data-ttu-id="b9419-179">Int32</span><span class="sxs-lookup"><span data-stu-id="b9419-179">Int32</span></span>|<span data-ttu-id="b9419-180">Número de contraseñas anteriores que impide su reutilización.</span><span class="sxs-lookup"><span data-stu-id="b9419-180">The number of previous passwords to prevent re-use of.</span></span>|
|<span data-ttu-id="b9419-181">passwordExpirationDays</span><span class="sxs-lookup"><span data-stu-id="b9419-181">passwordExpirationDays</span></span>|<span data-ttu-id="b9419-182">Int32</span><span class="sxs-lookup"><span data-stu-id="b9419-182">Int32</span></span>|<span data-ttu-id="b9419-183">Número de días antes de que expire la contraseña.</span><span class="sxs-lookup"><span data-stu-id="b9419-183">Number of days before password expiration.</span></span> <span data-ttu-id="b9419-184">Valores válidos de 1 a 255</span><span class="sxs-lookup"><span data-stu-id="b9419-184">Valid values 1 to 255</span></span>|
|<span data-ttu-id="b9419-185">passwordMinutesOfInactivityBeforeLock</span><span class="sxs-lookup"><span data-stu-id="b9419-185">passwordMinutesOfInactivityBeforeLock</span></span>|<span data-ttu-id="b9419-186">Int32</span><span class="sxs-lookup"><span data-stu-id="b9419-186">Int32</span></span>|<span data-ttu-id="b9419-187">Minutos de inactividad antes de que sea necesaria una contraseña.</span><span class="sxs-lookup"><span data-stu-id="b9419-187">Minutes of inactivity before a password is required.</span></span>|
|<span data-ttu-id="b9419-188">passwordRequireToUnlockFromIdle</span><span class="sxs-lookup"><span data-stu-id="b9419-188">passwordRequireToUnlockFromIdle</span></span>|<span data-ttu-id="b9419-189">Booleano</span><span class="sxs-lookup"><span data-stu-id="b9419-189">Boolean</span></span>|<span data-ttu-id="b9419-190">Exige una contraseña para desbloquear el dispositivo inactivo.</span><span class="sxs-lookup"><span data-stu-id="b9419-190">Require a password to unlock an idle device.</span></span>|
|<span data-ttu-id="b9419-191">osMinimumVersion</span><span class="sxs-lookup"><span data-stu-id="b9419-191">osMinimumVersion</span></span>|<span data-ttu-id="b9419-192">Cadena</span><span class="sxs-lookup"><span data-stu-id="b9419-192">String</span></span>|<span data-ttu-id="b9419-193">Versión mínima de Windows Phone.</span><span class="sxs-lookup"><span data-stu-id="b9419-193">Minimum Windows Phone version.</span></span>|
|<span data-ttu-id="b9419-194">osMaximumVersion</span><span class="sxs-lookup"><span data-stu-id="b9419-194">osMaximumVersion</span></span>|<span data-ttu-id="b9419-195">Cadena</span><span class="sxs-lookup"><span data-stu-id="b9419-195">String</span></span>|<span data-ttu-id="b9419-196">Versión máxima de Windows Phone.</span><span class="sxs-lookup"><span data-stu-id="b9419-196">Maximum Windows Phone version.</span></span>|
|<span data-ttu-id="b9419-197">earlyLaunchAntiMalwareDriverEnabled</span><span class="sxs-lookup"><span data-stu-id="b9419-197">earlyLaunchAntiMalwareDriverEnabled</span></span>|<span data-ttu-id="b9419-198">Booleano</span><span class="sxs-lookup"><span data-stu-id="b9419-198">Boolean</span></span>|<span data-ttu-id="b9419-199">Exige que la atestación de estado de dispositivo Windows notifique los dispositivos como correctos; el controlador antimalware de inicio temprano está habilitado.</span><span class="sxs-lookup"><span data-stu-id="b9419-199">Require devices to be reported as healthy by Windows Device Health Attestation - early launch antimalware driver is enabled.</span></span>|
|<span data-ttu-id="b9419-200">bitLockerEnabled</span><span class="sxs-lookup"><span data-stu-id="b9419-200">bitLockerEnabled</span></span>|<span data-ttu-id="b9419-201">Booleano</span><span class="sxs-lookup"><span data-stu-id="b9419-201">Boolean</span></span>|<span data-ttu-id="b9419-202">Exige que la atestación de estado de dispositivo Windows notifique los dispositivos como correctos; BitLocker está habilitado.</span><span class="sxs-lookup"><span data-stu-id="b9419-202">Require devices to be reported healthy by Windows Device Health Attestation - bit locker is enabled</span></span>|
|<span data-ttu-id="b9419-203">secureBootEnabled</span><span class="sxs-lookup"><span data-stu-id="b9419-203">secureBootEnabled</span></span>|<span data-ttu-id="b9419-204">Booleano</span><span class="sxs-lookup"><span data-stu-id="b9419-204">Boolean</span></span>|<span data-ttu-id="b9419-205">Exige que la atestación de estado de dispositivo Windows notifique los dispositivos como correctos; el arranque seguro está habilitado.</span><span class="sxs-lookup"><span data-stu-id="b9419-205">Require devices to be reported as healthy by Windows Device Health Attestation - secure boot is enabled.</span></span>|
|<span data-ttu-id="b9419-206">codeIntegrityEnabled</span><span class="sxs-lookup"><span data-stu-id="b9419-206">codeIntegrityEnabled</span></span>|<span data-ttu-id="b9419-207">Booleano</span><span class="sxs-lookup"><span data-stu-id="b9419-207">Boolean</span></span>|<span data-ttu-id="b9419-208">Exige que la atestación de estado de dispositivo Windows notifique los dispositivos como correctos.</span><span class="sxs-lookup"><span data-stu-id="b9419-208">Require devices to be reported as healthy by Windows Device Health Attestation.</span></span>|
|<span data-ttu-id="b9419-209">storageRequireEncryption</span><span class="sxs-lookup"><span data-stu-id="b9419-209">storageRequireEncryption</span></span>|<span data-ttu-id="b9419-210">Booleano</span><span class="sxs-lookup"><span data-stu-id="b9419-210">Boolean</span></span>|<span data-ttu-id="b9419-211">Exige el cifrado en dispositivos Windows.</span><span class="sxs-lookup"><span data-stu-id="b9419-211">Require encryption on windows devices.</span></span>|
|<span data-ttu-id="b9419-212">activeFirewallRequired</span><span class="sxs-lookup"><span data-stu-id="b9419-212">activeFirewallRequired</span></span>|<span data-ttu-id="b9419-213">Booleano</span><span class="sxs-lookup"><span data-stu-id="b9419-213">Boolean</span></span>|<span data-ttu-id="b9419-214">Requiere un servidor de seguridad activo en los dispositivos de Windows.</span><span class="sxs-lookup"><span data-stu-id="b9419-214">Require active firewall on Windows devices.</span></span>|
|<span data-ttu-id="b9419-215">validOperatingSystemBuildRanges</span><span class="sxs-lookup"><span data-stu-id="b9419-215">validOperatingSystemBuildRanges</span></span>|<span data-ttu-id="b9419-216">colección de [operatingSystemVersionRange](../resources/intune-deviceconfig-operatingsystemversionrange.md)</span><span class="sxs-lookup"><span data-stu-id="b9419-216">[operatingSystemVersionRange](../resources/intune-deviceconfig-operatingsystemversionrange.md) collection</span></span>|<span data-ttu-id="b9419-217">El sistema operativo válido crear rangos en los dispositivos de Windows.</span><span class="sxs-lookup"><span data-stu-id="b9419-217">The valid operating system build ranges on Windows devices.</span></span> <span data-ttu-id="b9419-218">Esta colección puede contener un máximo de 10 000 elementos.</span><span class="sxs-lookup"><span data-stu-id="b9419-218">This collection can contain a maximum of 10000 elements.</span></span>|



## <a name="response"></a><span data-ttu-id="b9419-219">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b9419-219">Response</span></span>
<span data-ttu-id="b9419-220">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [windows10MobileCompliancePolicy](../resources/intune-deviceconfig-windows10mobilecompliancepolicy.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b9419-220">If successful, this method returns a `200 OK` response code and an updated [windows10MobileCompliancePolicy](../resources/intune-deviceconfig-windows10mobilecompliancepolicy.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="b9419-221">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b9419-221">Example</span></span>
### <a name="request"></a><span data-ttu-id="b9419-222">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b9419-222">Request</span></span>
<span data-ttu-id="b9419-223">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b9419-223">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}
Content-type: application/json
Content-length: 1152

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
  "passwordMinimumLength": 5,
  "passwordMinimumCharacterSetCount": 0,
  "passwordRequiredType": "alphanumeric",
  "passwordPreviousPasswordBlockCount": 2,
  "passwordExpirationDays": 6,
  "passwordMinutesOfInactivityBeforeLock": 5,
  "passwordRequireToUnlockFromIdle": true,
  "osMinimumVersion": "Os Minimum Version value",
  "osMaximumVersion": "Os Maximum Version value",
  "earlyLaunchAntiMalwareDriverEnabled": true,
  "bitLockerEnabled": true,
  "secureBootEnabled": true,
  "codeIntegrityEnabled": true,
  "storageRequireEncryption": true,
  "activeFirewallRequired": true,
  "validOperatingSystemBuildRanges": [
    {
      "@odata.type": "microsoft.graph.operatingSystemVersionRange",
      "description": "Description value",
      "lowestVersion": "Lowest Version value",
      "highestVersion": "Highest Version value"
    }
  ]
}
```

### <a name="response"></a><span data-ttu-id="b9419-224">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b9419-224">Response</span></span>
<span data-ttu-id="b9419-p114">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="b9419-p114">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1330

{
  "@odata.type": "#microsoft.graph.windows10MobileCompliancePolicy",
  "roleScopeTagIds": [
    "Role Scope Tag Ids value"
  ],
  "id": "3d4237b0-37b0-3d42-b037-423db037423d",
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "description": "Description value",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "displayName": "Display Name value",
  "version": 7,
  "passwordRequired": true,
  "passwordBlockSimple": true,
  "passwordMinimumLength": 5,
  "passwordMinimumCharacterSetCount": 0,
  "passwordRequiredType": "alphanumeric",
  "passwordPreviousPasswordBlockCount": 2,
  "passwordExpirationDays": 6,
  "passwordMinutesOfInactivityBeforeLock": 5,
  "passwordRequireToUnlockFromIdle": true,
  "osMinimumVersion": "Os Minimum Version value",
  "osMaximumVersion": "Os Maximum Version value",
  "earlyLaunchAntiMalwareDriverEnabled": true,
  "bitLockerEnabled": true,
  "secureBootEnabled": true,
  "codeIntegrityEnabled": true,
  "storageRequireEncryption": true,
  "activeFirewallRequired": true,
  "validOperatingSystemBuildRanges": [
    {
      "@odata.type": "microsoft.graph.operatingSystemVersionRange",
      "description": "Description value",
      "lowestVersion": "Lowest Version value",
      "highestVersion": "Highest Version value"
    }
  ]
}
```





