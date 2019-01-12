---
title: Actualizar windows10MobileCompliancePolicy
description: Actualice las propiedades de un objeto windows10MobileCompliancePolicy.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 1b036b4c73800e647e6617413fc330f4c6d40dea
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27966828"
---
# <a name="update-windows10mobilecompliancepolicy"></a><span data-ttu-id="8a94f-103">Actualizar windows10MobileCompliancePolicy</span><span class="sxs-lookup"><span data-stu-id="8a94f-103">Update windows10MobileCompliancePolicy</span></span>

> <span data-ttu-id="8a94f-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="8a94f-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="8a94f-105">Actualice las propiedades de un objeto [windows10MobileCompliancePolicy](../resources/intune-deviceconfig-windows10mobilecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="8a94f-105">Update the properties of a [windows10MobileCompliancePolicy](../resources/intune-deviceconfig-windows10mobilecompliancepolicy.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="8a94f-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="8a94f-106">Prerequisites</span></span>
<span data-ttu-id="8a94f-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="8a94f-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="8a94f-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="8a94f-109">Permission type</span></span>|<span data-ttu-id="8a94f-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="8a94f-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="8a94f-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="8a94f-111">Delegated (work or school account)</span></span>|<span data-ttu-id="8a94f-112">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="8a94f-112">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="8a94f-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="8a94f-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="8a94f-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8a94f-114">Not supported.</span></span>|
|<span data-ttu-id="8a94f-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="8a94f-115">Application</span></span>|<span data-ttu-id="8a94f-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8a94f-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="8a94f-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="8a94f-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}
```

## <a name="request-headers"></a><span data-ttu-id="8a94f-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="8a94f-118">Request headers</span></span>
|<span data-ttu-id="8a94f-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8a94f-119">Header</span></span>|<span data-ttu-id="8a94f-120">Valor</span><span class="sxs-lookup"><span data-stu-id="8a94f-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="8a94f-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="8a94f-121">Authorization</span></span>|<span data-ttu-id="8a94f-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="8a94f-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="8a94f-123">Accept</span><span class="sxs-lookup"><span data-stu-id="8a94f-123">Accept</span></span>|<span data-ttu-id="8a94f-124">application/json</span><span class="sxs-lookup"><span data-stu-id="8a94f-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="8a94f-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="8a94f-125">Request body</span></span>
<span data-ttu-id="8a94f-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto [windows10MobileCompliancePolicy](../resources/intune-deviceconfig-windows10mobilecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="8a94f-126">In the request body, supply a JSON representation for the [windows10MobileCompliancePolicy](../resources/intune-deviceconfig-windows10mobilecompliancepolicy.md) object.</span></span>

<span data-ttu-id="8a94f-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [windows10MobileCompliancePolicy](../resources/intune-deviceconfig-windows10mobilecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="8a94f-127">The following table shows the properties that are required when you create the [windows10MobileCompliancePolicy](../resources/intune-deviceconfig-windows10mobilecompliancepolicy.md).</span></span>

|<span data-ttu-id="8a94f-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="8a94f-128">Property</span></span>|<span data-ttu-id="8a94f-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="8a94f-129">Type</span></span>|<span data-ttu-id="8a94f-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="8a94f-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="8a94f-131">id</span><span class="sxs-lookup"><span data-stu-id="8a94f-131">id</span></span>|<span data-ttu-id="8a94f-132">Cadena</span><span class="sxs-lookup"><span data-stu-id="8a94f-132">String</span></span>|<span data-ttu-id="8a94f-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="8a94f-133">Key of the entity.</span></span> <span data-ttu-id="8a94f-134">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="8a94f-134">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="8a94f-135">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="8a94f-135">createdDateTime</span></span>|<span data-ttu-id="8a94f-136">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="8a94f-136">DateTimeOffset</span></span>|<span data-ttu-id="8a94f-137">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="8a94f-137">DateTime the object was created.</span></span> <span data-ttu-id="8a94f-138">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="8a94f-138">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="8a94f-139">descripción</span><span class="sxs-lookup"><span data-stu-id="8a94f-139">description</span></span>|<span data-ttu-id="8a94f-140">Cadena</span><span class="sxs-lookup"><span data-stu-id="8a94f-140">String</span></span>|<span data-ttu-id="8a94f-141">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8a94f-141">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="8a94f-142">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="8a94f-142">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="8a94f-143">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="8a94f-143">lastModifiedDateTime</span></span>|<span data-ttu-id="8a94f-144">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="8a94f-144">DateTimeOffset</span></span>|<span data-ttu-id="8a94f-145">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="8a94f-145">DateTime the object was last modified.</span></span> <span data-ttu-id="8a94f-146">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="8a94f-146">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="8a94f-147">displayName</span><span class="sxs-lookup"><span data-stu-id="8a94f-147">displayName</span></span>|<span data-ttu-id="8a94f-148">Cadena</span><span class="sxs-lookup"><span data-stu-id="8a94f-148">String</span></span>|<span data-ttu-id="8a94f-149">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8a94f-149">Admin provided name of the device configuration.</span></span> <span data-ttu-id="8a94f-150">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="8a94f-150">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="8a94f-151">version</span><span class="sxs-lookup"><span data-stu-id="8a94f-151">version</span></span>|<span data-ttu-id="8a94f-152">Int32</span><span class="sxs-lookup"><span data-stu-id="8a94f-152">Int32</span></span>|<span data-ttu-id="8a94f-153">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8a94f-153">Version of the device configuration.</span></span> <span data-ttu-id="8a94f-154">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="8a94f-154">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="8a94f-155">passwordRequired</span><span class="sxs-lookup"><span data-stu-id="8a94f-155">passwordRequired</span></span>|<span data-ttu-id="8a94f-156">Booleano</span><span class="sxs-lookup"><span data-stu-id="8a94f-156">Boolean</span></span>|<span data-ttu-id="8a94f-157">Exigir una contraseña para desbloquear el dispositivo de Windows Phone.</span><span class="sxs-lookup"><span data-stu-id="8a94f-157">Require a password to unlock Windows Phone device.</span></span>|
|<span data-ttu-id="8a94f-158">passwordBlockSimple</span><span class="sxs-lookup"><span data-stu-id="8a94f-158">passwordBlockSimple</span></span>|<span data-ttu-id="8a94f-159">Booleano</span><span class="sxs-lookup"><span data-stu-id="8a94f-159">Boolean</span></span>|<span data-ttu-id="8a94f-160">Si quiere bloquear o no la sincronización del calendario.</span><span class="sxs-lookup"><span data-stu-id="8a94f-160">Whether or not to block syncing the calendar.</span></span>|
|<span data-ttu-id="8a94f-161">passwordMinimumLength</span><span class="sxs-lookup"><span data-stu-id="8a94f-161">passwordMinimumLength</span></span>|<span data-ttu-id="8a94f-162">Int32</span><span class="sxs-lookup"><span data-stu-id="8a94f-162">Int32</span></span>|<span data-ttu-id="8a94f-163">Longitud mínima de la contraseña.</span><span class="sxs-lookup"><span data-stu-id="8a94f-163">Minimum password length.</span></span> <span data-ttu-id="8a94f-164">Valores válidos de 4 a 16</span><span class="sxs-lookup"><span data-stu-id="8a94f-164">Valid values 4 to 16</span></span>|
|<span data-ttu-id="8a94f-165">passwordMinimumCharacterSetCount</span><span class="sxs-lookup"><span data-stu-id="8a94f-165">passwordMinimumCharacterSetCount</span></span>|<span data-ttu-id="8a94f-166">Int32</span><span class="sxs-lookup"><span data-stu-id="8a94f-166">Int32</span></span>|<span data-ttu-id="8a94f-167">Número de juegos de caracteres necesarios en la contraseña.</span><span class="sxs-lookup"><span data-stu-id="8a94f-167">The number of character sets required in the password.</span></span>|
|<span data-ttu-id="8a94f-168">passwordRequiredType</span><span class="sxs-lookup"><span data-stu-id="8a94f-168">passwordRequiredType</span></span>|[<span data-ttu-id="8a94f-169">requiredPasswordType</span><span class="sxs-lookup"><span data-stu-id="8a94f-169">requiredPasswordType</span></span>](../resources/intune-deviceconfig-requiredpasswordtype.md)|<span data-ttu-id="8a94f-170">Tipo de contraseña necesaria.</span><span class="sxs-lookup"><span data-stu-id="8a94f-170">The required password type.</span></span> <span data-ttu-id="8a94f-171">Los valores posibles son: `deviceDefault`, `alphanumeric` y `numeric`.</span><span class="sxs-lookup"><span data-stu-id="8a94f-171">Possible values are: `deviceDefault`, `alphanumeric`, `numeric`.</span></span>|
|<span data-ttu-id="8a94f-172">passwordPreviousPasswordBlockCount</span><span class="sxs-lookup"><span data-stu-id="8a94f-172">passwordPreviousPasswordBlockCount</span></span>|<span data-ttu-id="8a94f-173">Int32</span><span class="sxs-lookup"><span data-stu-id="8a94f-173">Int32</span></span>|<span data-ttu-id="8a94f-174">Número de contraseñas anteriores que impide su reutilización.</span><span class="sxs-lookup"><span data-stu-id="8a94f-174">The number of previous passwords to prevent re-use of.</span></span>|
|<span data-ttu-id="8a94f-175">passwordExpirationDays</span><span class="sxs-lookup"><span data-stu-id="8a94f-175">passwordExpirationDays</span></span>|<span data-ttu-id="8a94f-176">Int32</span><span class="sxs-lookup"><span data-stu-id="8a94f-176">Int32</span></span>|<span data-ttu-id="8a94f-177">Número de días antes de que expire la contraseña.</span><span class="sxs-lookup"><span data-stu-id="8a94f-177">Number of days before password expiration.</span></span> <span data-ttu-id="8a94f-178">Valores válidos de 1 a 255</span><span class="sxs-lookup"><span data-stu-id="8a94f-178">Valid values 1 to 255</span></span>|
|<span data-ttu-id="8a94f-179">passwordMinutesOfInactivityBeforeLock</span><span class="sxs-lookup"><span data-stu-id="8a94f-179">passwordMinutesOfInactivityBeforeLock</span></span>|<span data-ttu-id="8a94f-180">Int32</span><span class="sxs-lookup"><span data-stu-id="8a94f-180">Int32</span></span>|<span data-ttu-id="8a94f-181">Minutos de inactividad antes de que sea necesaria una contraseña.</span><span class="sxs-lookup"><span data-stu-id="8a94f-181">Minutes of inactivity before a password is required.</span></span>|
|<span data-ttu-id="8a94f-182">passwordRequireToUnlockFromIdle</span><span class="sxs-lookup"><span data-stu-id="8a94f-182">passwordRequireToUnlockFromIdle</span></span>|<span data-ttu-id="8a94f-183">Booleano</span><span class="sxs-lookup"><span data-stu-id="8a94f-183">Boolean</span></span>|<span data-ttu-id="8a94f-184">Exige una contraseña para desbloquear el dispositivo inactivo.</span><span class="sxs-lookup"><span data-stu-id="8a94f-184">Require a password to unlock an idle device.</span></span>|
|<span data-ttu-id="8a94f-185">osMinimumVersion</span><span class="sxs-lookup"><span data-stu-id="8a94f-185">osMinimumVersion</span></span>|<span data-ttu-id="8a94f-186">Cadena</span><span class="sxs-lookup"><span data-stu-id="8a94f-186">String</span></span>|<span data-ttu-id="8a94f-187">Versión mínima de Windows Phone.</span><span class="sxs-lookup"><span data-stu-id="8a94f-187">Minimum Windows Phone version.</span></span>|
|<span data-ttu-id="8a94f-188">osMaximumVersion</span><span class="sxs-lookup"><span data-stu-id="8a94f-188">osMaximumVersion</span></span>|<span data-ttu-id="8a94f-189">Cadena</span><span class="sxs-lookup"><span data-stu-id="8a94f-189">String</span></span>|<span data-ttu-id="8a94f-190">Versión máxima de Windows Phone.</span><span class="sxs-lookup"><span data-stu-id="8a94f-190">Maximum Windows Phone version.</span></span>|
|<span data-ttu-id="8a94f-191">earlyLaunchAntiMalwareDriverEnabled</span><span class="sxs-lookup"><span data-stu-id="8a94f-191">earlyLaunchAntiMalwareDriverEnabled</span></span>|<span data-ttu-id="8a94f-192">Booleano</span><span class="sxs-lookup"><span data-stu-id="8a94f-192">Boolean</span></span>|<span data-ttu-id="8a94f-193">Exige que la atestación de estado de dispositivo Windows notifique los dispositivos como correctos; el controlador antimalware de inicio temprano está habilitado.</span><span class="sxs-lookup"><span data-stu-id="8a94f-193">Require devices to be reported as healthy by Windows Device Health Attestation - early launch antimalware driver is enabled.</span></span>|
|<span data-ttu-id="8a94f-194">bitLockerEnabled</span><span class="sxs-lookup"><span data-stu-id="8a94f-194">bitLockerEnabled</span></span>|<span data-ttu-id="8a94f-195">Booleano</span><span class="sxs-lookup"><span data-stu-id="8a94f-195">Boolean</span></span>|<span data-ttu-id="8a94f-196">Exige que la atestación de estado de dispositivo Windows notifique los dispositivos como correctos; BitLocker está habilitado.</span><span class="sxs-lookup"><span data-stu-id="8a94f-196">Require devices to be reported healthy by Windows Device Health Attestation - bit locker is enabled</span></span>|
|<span data-ttu-id="8a94f-197">secureBootEnabled</span><span class="sxs-lookup"><span data-stu-id="8a94f-197">secureBootEnabled</span></span>|<span data-ttu-id="8a94f-198">Booleano</span><span class="sxs-lookup"><span data-stu-id="8a94f-198">Boolean</span></span>|<span data-ttu-id="8a94f-199">Exige que la atestación de estado de dispositivo Windows notifique los dispositivos como correctos; el arranque seguro está habilitado.</span><span class="sxs-lookup"><span data-stu-id="8a94f-199">Require devices to be reported as healthy by Windows Device Health Attestation - secure boot is enabled.</span></span>|
|<span data-ttu-id="8a94f-200">codeIntegrityEnabled</span><span class="sxs-lookup"><span data-stu-id="8a94f-200">codeIntegrityEnabled</span></span>|<span data-ttu-id="8a94f-201">Booleano</span><span class="sxs-lookup"><span data-stu-id="8a94f-201">Boolean</span></span>|<span data-ttu-id="8a94f-202">Exige que la atestación de estado de dispositivo Windows notifique los dispositivos como correctos.</span><span class="sxs-lookup"><span data-stu-id="8a94f-202">Require devices to be reported as healthy by Windows Device Health Attestation.</span></span>|
|<span data-ttu-id="8a94f-203">storageRequireEncryption</span><span class="sxs-lookup"><span data-stu-id="8a94f-203">storageRequireEncryption</span></span>|<span data-ttu-id="8a94f-204">Booleano</span><span class="sxs-lookup"><span data-stu-id="8a94f-204">Boolean</span></span>|<span data-ttu-id="8a94f-205">Exige el cifrado en dispositivos Windows.</span><span class="sxs-lookup"><span data-stu-id="8a94f-205">Require encryption on windows devices.</span></span>|



## <a name="response"></a><span data-ttu-id="8a94f-206">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8a94f-206">Response</span></span>
<span data-ttu-id="8a94f-207">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [windows10MobileCompliancePolicy](../resources/intune-deviceconfig-windows10mobilecompliancepolicy.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8a94f-207">If successful, this method returns a `200 OK` response code and an updated [windows10MobileCompliancePolicy](../resources/intune-deviceconfig-windows10mobilecompliancepolicy.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="8a94f-208">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="8a94f-208">Example</span></span>
### <a name="request"></a><span data-ttu-id="8a94f-209">Solicitud</span><span class="sxs-lookup"><span data-stu-id="8a94f-209">Request</span></span>
<span data-ttu-id="8a94f-210">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="8a94f-210">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}
Content-type: application/json
Content-length: 792

{
  "@odata.type": "#microsoft.graph.windows10MobileCompliancePolicy",
  "description": "Description value",
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
  "storageRequireEncryption": true
}
```

### <a name="response"></a><span data-ttu-id="8a94f-211">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8a94f-211">Response</span></span>
<span data-ttu-id="8a94f-p111">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="8a94f-p111">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 964

{
  "@odata.type": "#microsoft.graph.windows10MobileCompliancePolicy",
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
  "storageRequireEncryption": true
}
```



