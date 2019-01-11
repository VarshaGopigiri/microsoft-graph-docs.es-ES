---
title: Actualizar windows10CompliancePolicy
description: Actualice las propiedades de un objeto windows10CompliancePolicy.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: cd56f1f808a16bc05aa3e4f2c3fc4fb4da74a5a4
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27892207"
---
# <a name="update-windows10compliancepolicy"></a><span data-ttu-id="62b50-103">Actualizar windows10CompliancePolicy</span><span class="sxs-lookup"><span data-stu-id="62b50-103">Update windows10CompliancePolicy</span></span>

> <span data-ttu-id="62b50-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="62b50-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="62b50-105">Actualice las propiedades de un objeto [windows10CompliancePolicy](../resources/intune-deviceconfig-windows10compliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="62b50-105">Update the properties of a [windows10CompliancePolicy](../resources/intune-deviceconfig-windows10compliancepolicy.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="62b50-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="62b50-106">Prerequisites</span></span>
<span data-ttu-id="62b50-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="62b50-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="62b50-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="62b50-109">Permission type</span></span>|<span data-ttu-id="62b50-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="62b50-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="62b50-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="62b50-111">Delegated (work or school account)</span></span>|<span data-ttu-id="62b50-112">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="62b50-112">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="62b50-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="62b50-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="62b50-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="62b50-114">Not supported.</span></span>|
|<span data-ttu-id="62b50-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="62b50-115">Application</span></span>|<span data-ttu-id="62b50-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="62b50-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="62b50-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="62b50-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}
```

## <a name="request-headers"></a><span data-ttu-id="62b50-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="62b50-118">Request headers</span></span>
|<span data-ttu-id="62b50-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="62b50-119">Header</span></span>|<span data-ttu-id="62b50-120">Valor</span><span class="sxs-lookup"><span data-stu-id="62b50-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="62b50-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="62b50-121">Authorization</span></span>|<span data-ttu-id="62b50-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="62b50-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="62b50-123">Accept</span><span class="sxs-lookup"><span data-stu-id="62b50-123">Accept</span></span>|<span data-ttu-id="62b50-124">application/json</span><span class="sxs-lookup"><span data-stu-id="62b50-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="62b50-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="62b50-125">Request body</span></span>
<span data-ttu-id="62b50-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto [windows10CompliancePolicy](../resources/intune-deviceconfig-windows10compliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="62b50-126">In the request body, supply a JSON representation for the [windows10CompliancePolicy](../resources/intune-deviceconfig-windows10compliancepolicy.md) object.</span></span>

<span data-ttu-id="62b50-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [windows10CompliancePolicy](../resources/intune-deviceconfig-windows10compliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="62b50-127">The following table shows the properties that are required when you create the [windows10CompliancePolicy](../resources/intune-deviceconfig-windows10compliancepolicy.md).</span></span>

|<span data-ttu-id="62b50-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="62b50-128">Property</span></span>|<span data-ttu-id="62b50-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="62b50-129">Type</span></span>|<span data-ttu-id="62b50-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="62b50-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="62b50-131">id</span><span class="sxs-lookup"><span data-stu-id="62b50-131">id</span></span>|<span data-ttu-id="62b50-132">Cadena</span><span class="sxs-lookup"><span data-stu-id="62b50-132">String</span></span>|<span data-ttu-id="62b50-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="62b50-133">Key of the entity.</span></span> <span data-ttu-id="62b50-134">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="62b50-134">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="62b50-135">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="62b50-135">createdDateTime</span></span>|<span data-ttu-id="62b50-136">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="62b50-136">DateTimeOffset</span></span>|<span data-ttu-id="62b50-137">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="62b50-137">DateTime the object was created.</span></span> <span data-ttu-id="62b50-138">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="62b50-138">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="62b50-139">descripción</span><span class="sxs-lookup"><span data-stu-id="62b50-139">description</span></span>|<span data-ttu-id="62b50-140">Cadena</span><span class="sxs-lookup"><span data-stu-id="62b50-140">String</span></span>|<span data-ttu-id="62b50-141">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="62b50-141">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="62b50-142">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="62b50-142">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="62b50-143">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="62b50-143">lastModifiedDateTime</span></span>|<span data-ttu-id="62b50-144">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="62b50-144">DateTimeOffset</span></span>|<span data-ttu-id="62b50-145">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="62b50-145">DateTime the object was last modified.</span></span> <span data-ttu-id="62b50-146">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="62b50-146">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="62b50-147">displayName</span><span class="sxs-lookup"><span data-stu-id="62b50-147">displayName</span></span>|<span data-ttu-id="62b50-148">Cadena</span><span class="sxs-lookup"><span data-stu-id="62b50-148">String</span></span>|<span data-ttu-id="62b50-149">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="62b50-149">Admin provided name of the device configuration.</span></span> <span data-ttu-id="62b50-150">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="62b50-150">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="62b50-151">version</span><span class="sxs-lookup"><span data-stu-id="62b50-151">version</span></span>|<span data-ttu-id="62b50-152">Int32</span><span class="sxs-lookup"><span data-stu-id="62b50-152">Int32</span></span>|<span data-ttu-id="62b50-153">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="62b50-153">Version of the device configuration.</span></span> <span data-ttu-id="62b50-154">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="62b50-154">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="62b50-155">passwordRequired</span><span class="sxs-lookup"><span data-stu-id="62b50-155">passwordRequired</span></span>|<span data-ttu-id="62b50-156">Booleano</span><span class="sxs-lookup"><span data-stu-id="62b50-156">Boolean</span></span>|<span data-ttu-id="62b50-157">Exige una contraseña para desbloquear el dispositivo Windows.</span><span class="sxs-lookup"><span data-stu-id="62b50-157">Require a password to unlock Windows device.</span></span>|
|<span data-ttu-id="62b50-158">passwordBlockSimple</span><span class="sxs-lookup"><span data-stu-id="62b50-158">passwordBlockSimple</span></span>|<span data-ttu-id="62b50-159">Booleano</span><span class="sxs-lookup"><span data-stu-id="62b50-159">Boolean</span></span>|<span data-ttu-id="62b50-160">Indica si quiere bloquear o no la contraseña simple.</span><span class="sxs-lookup"><span data-stu-id="62b50-160">Indicates whether or not to block simple password.</span></span>|
|<span data-ttu-id="62b50-161">passwordRequiredToUnlockFromIdle</span><span class="sxs-lookup"><span data-stu-id="62b50-161">passwordRequiredToUnlockFromIdle</span></span>|<span data-ttu-id="62b50-162">Booleano</span><span class="sxs-lookup"><span data-stu-id="62b50-162">Boolean</span></span>|<span data-ttu-id="62b50-163">Exige una contraseña para desbloquear el dispositivo inactivo.</span><span class="sxs-lookup"><span data-stu-id="62b50-163">Require a password to unlock an idle device.</span></span>|
|<span data-ttu-id="62b50-164">passwordMinutesOfInactivityBeforeLock</span><span class="sxs-lookup"><span data-stu-id="62b50-164">passwordMinutesOfInactivityBeforeLock</span></span>|<span data-ttu-id="62b50-165">Int32</span><span class="sxs-lookup"><span data-stu-id="62b50-165">Int32</span></span>|<span data-ttu-id="62b50-166">Minutos de inactividad antes de que sea necesaria una contraseña.</span><span class="sxs-lookup"><span data-stu-id="62b50-166">Minutes of inactivity before a password is required.</span></span>|
|<span data-ttu-id="62b50-167">passwordExpirationDays</span><span class="sxs-lookup"><span data-stu-id="62b50-167">passwordExpirationDays</span></span>|<span data-ttu-id="62b50-168">Int32</span><span class="sxs-lookup"><span data-stu-id="62b50-168">Int32</span></span>|<span data-ttu-id="62b50-169">La expiración de la contraseña en días.</span><span class="sxs-lookup"><span data-stu-id="62b50-169">The password expiration in days.</span></span>|
|<span data-ttu-id="62b50-170">passwordMinimumLength</span><span class="sxs-lookup"><span data-stu-id="62b50-170">passwordMinimumLength</span></span>|<span data-ttu-id="62b50-171">Int32</span><span class="sxs-lookup"><span data-stu-id="62b50-171">Int32</span></span>|<span data-ttu-id="62b50-172">La longitud mínima de contraseña.</span><span class="sxs-lookup"><span data-stu-id="62b50-172">The minimum password length.</span></span>|
|<span data-ttu-id="62b50-173">passwordMinimumCharacterSetCount</span><span class="sxs-lookup"><span data-stu-id="62b50-173">passwordMinimumCharacterSetCount</span></span>|<span data-ttu-id="62b50-174">Int32</span><span class="sxs-lookup"><span data-stu-id="62b50-174">Int32</span></span>|<span data-ttu-id="62b50-175">Número de juegos de caracteres necesarios en la contraseña.</span><span class="sxs-lookup"><span data-stu-id="62b50-175">The number of character sets required in the password.</span></span>|
|<span data-ttu-id="62b50-176">passwordRequiredType</span><span class="sxs-lookup"><span data-stu-id="62b50-176">passwordRequiredType</span></span>|[<span data-ttu-id="62b50-177">requiredPasswordType</span><span class="sxs-lookup"><span data-stu-id="62b50-177">requiredPasswordType</span></span>](../resources/intune-deviceconfig-requiredpasswordtype.md)|<span data-ttu-id="62b50-178">Tipo de contraseña necesaria.</span><span class="sxs-lookup"><span data-stu-id="62b50-178">The required password type.</span></span> <span data-ttu-id="62b50-179">Los valores posibles son: `deviceDefault`, `alphanumeric` y `numeric`.</span><span class="sxs-lookup"><span data-stu-id="62b50-179">Possible values are: `deviceDefault`, `alphanumeric`, `numeric`.</span></span>|
|<span data-ttu-id="62b50-180">passwordPreviousPasswordBlockCount</span><span class="sxs-lookup"><span data-stu-id="62b50-180">passwordPreviousPasswordBlockCount</span></span>|<span data-ttu-id="62b50-181">Int32</span><span class="sxs-lookup"><span data-stu-id="62b50-181">Int32</span></span>|<span data-ttu-id="62b50-182">Número de contraseñas anteriores que impide su reutilización.</span><span class="sxs-lookup"><span data-stu-id="62b50-182">The number of previous passwords to prevent re-use of.</span></span>|
|<span data-ttu-id="62b50-183">requireHealthyDeviceReport</span><span class="sxs-lookup"><span data-stu-id="62b50-183">requireHealthyDeviceReport</span></span>|<span data-ttu-id="62b50-184">Booleano</span><span class="sxs-lookup"><span data-stu-id="62b50-184">Boolean</span></span>|<span data-ttu-id="62b50-185">Exige que la atestación de estado de dispositivo Windows notifique los dispositivos como correctos.</span><span class="sxs-lookup"><span data-stu-id="62b50-185">Require devices to be reported as healthy by Windows Device Health Attestation.</span></span>|
|<span data-ttu-id="62b50-186">osMinimumVersion</span><span class="sxs-lookup"><span data-stu-id="62b50-186">osMinimumVersion</span></span>|<span data-ttu-id="62b50-187">Cadena</span><span class="sxs-lookup"><span data-stu-id="62b50-187">String</span></span>|<span data-ttu-id="62b50-188">Versión mínima de Windows 10.</span><span class="sxs-lookup"><span data-stu-id="62b50-188">Minimum Windows 10 version.</span></span>|
|<span data-ttu-id="62b50-189">osMaximumVersion</span><span class="sxs-lookup"><span data-stu-id="62b50-189">osMaximumVersion</span></span>|<span data-ttu-id="62b50-190">Cadena</span><span class="sxs-lookup"><span data-stu-id="62b50-190">String</span></span>|<span data-ttu-id="62b50-191">Versión máxima de Windows 10.</span><span class="sxs-lookup"><span data-stu-id="62b50-191">Maximum Windows 10 version.</span></span>|
|<span data-ttu-id="62b50-192">mobileOsMinimumVersion</span><span class="sxs-lookup"><span data-stu-id="62b50-192">mobileOsMinimumVersion</span></span>|<span data-ttu-id="62b50-193">Cadena</span><span class="sxs-lookup"><span data-stu-id="62b50-193">String</span></span>|<span data-ttu-id="62b50-194">Versión mínima de Windows Phone.</span><span class="sxs-lookup"><span data-stu-id="62b50-194">Minimum Windows Phone version.</span></span>|
|<span data-ttu-id="62b50-195">mobileOsMaximumVersion</span><span class="sxs-lookup"><span data-stu-id="62b50-195">mobileOsMaximumVersion</span></span>|<span data-ttu-id="62b50-196">Cadena</span><span class="sxs-lookup"><span data-stu-id="62b50-196">String</span></span>|<span data-ttu-id="62b50-197">Versión máxima de Windows Phone.</span><span class="sxs-lookup"><span data-stu-id="62b50-197">Maximum Windows Phone version.</span></span>|
|<span data-ttu-id="62b50-198">earlyLaunchAntiMalwareDriverEnabled</span><span class="sxs-lookup"><span data-stu-id="62b50-198">earlyLaunchAntiMalwareDriverEnabled</span></span>|<span data-ttu-id="62b50-199">Booleano</span><span class="sxs-lookup"><span data-stu-id="62b50-199">Boolean</span></span>|<span data-ttu-id="62b50-200">Exige que la atestación de estado de dispositivo Windows notifique los dispositivos como correctos; el controlador antimalware de inicio temprano está habilitado.</span><span class="sxs-lookup"><span data-stu-id="62b50-200">Require devices to be reported as healthy by Windows Device Health Attestation - early launch antimalware driver is enabled.</span></span>|
|<span data-ttu-id="62b50-201">bitLockerEnabled</span><span class="sxs-lookup"><span data-stu-id="62b50-201">bitLockerEnabled</span></span>|<span data-ttu-id="62b50-202">Booleano</span><span class="sxs-lookup"><span data-stu-id="62b50-202">Boolean</span></span>|<span data-ttu-id="62b50-203">Exige que la atestación de estado de dispositivo Windows notifique los dispositivos como correctos; BitLocker está habilitado.</span><span class="sxs-lookup"><span data-stu-id="62b50-203">Require devices to be reported healthy by Windows Device Health Attestation - bit locker is enabled</span></span>|
|<span data-ttu-id="62b50-204">secureBootEnabled</span><span class="sxs-lookup"><span data-stu-id="62b50-204">secureBootEnabled</span></span>|<span data-ttu-id="62b50-205">Booleano</span><span class="sxs-lookup"><span data-stu-id="62b50-205">Boolean</span></span>|<span data-ttu-id="62b50-206">Exige que la atestación de estado de dispositivo Windows notifique los dispositivos como correctos; el arranque seguro está habilitado.</span><span class="sxs-lookup"><span data-stu-id="62b50-206">Require devices to be reported as healthy by Windows Device Health Attestation - secure boot is enabled.</span></span>|
|<span data-ttu-id="62b50-207">codeIntegrityEnabled</span><span class="sxs-lookup"><span data-stu-id="62b50-207">codeIntegrityEnabled</span></span>|<span data-ttu-id="62b50-208">Booleano</span><span class="sxs-lookup"><span data-stu-id="62b50-208">Boolean</span></span>|<span data-ttu-id="62b50-209">Exige que la atestación de estado de dispositivo Windows notifique los dispositivos como correctos.</span><span class="sxs-lookup"><span data-stu-id="62b50-209">Require devices to be reported as healthy by Windows Device Health Attestation.</span></span>|
|<span data-ttu-id="62b50-210">storageRequireEncryption</span><span class="sxs-lookup"><span data-stu-id="62b50-210">storageRequireEncryption</span></span>|<span data-ttu-id="62b50-211">Booleano</span><span class="sxs-lookup"><span data-stu-id="62b50-211">Boolean</span></span>|<span data-ttu-id="62b50-212">Exige el cifrado en dispositivos Windows.</span><span class="sxs-lookup"><span data-stu-id="62b50-212">Require encryption on windows devices.</span></span>|



## <a name="response"></a><span data-ttu-id="62b50-213">Respuesta</span><span class="sxs-lookup"><span data-stu-id="62b50-213">Response</span></span>
<span data-ttu-id="62b50-214">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [windows10CompliancePolicy](../resources/intune-deviceconfig-windows10compliancepolicy.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="62b50-214">If successful, this method returns a `200 OK` response code and an updated [windows10CompliancePolicy](../resources/intune-deviceconfig-windows10compliancepolicy.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="62b50-215">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="62b50-215">Example</span></span>
### <a name="request"></a><span data-ttu-id="62b50-216">Solicitud</span><span class="sxs-lookup"><span data-stu-id="62b50-216">Request</span></span>
<span data-ttu-id="62b50-217">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="62b50-217">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}
Content-type: application/json
Content-length: 954

{
  "@odata.type": "#microsoft.graph.windows10CompliancePolicy",
  "description": "Description value",
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
  "storageRequireEncryption": true
}
```

### <a name="response"></a><span data-ttu-id="62b50-218">Respuesta</span><span class="sxs-lookup"><span data-stu-id="62b50-218">Response</span></span>
<span data-ttu-id="62b50-p109">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="62b50-p109">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1126

{
  "@odata.type": "#microsoft.graph.windows10CompliancePolicy",
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
  "storageRequireEncryption": true
}
```



