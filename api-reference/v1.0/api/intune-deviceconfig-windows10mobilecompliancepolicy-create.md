---
title: Crear windows10MobileCompliancePolicy
description: Crear un objeto windows10MobileCompliancePolicy.
author: tfitzmac
ms.openlocfilehash: 2d0c7c4a4f27ad723f8d29a24fc20d1fddd2633f
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27324287"
---
# <a name="create-windows10mobilecompliancepolicy"></a><span data-ttu-id="e8c55-103">Crear windows10MobileCompliancePolicy</span><span class="sxs-lookup"><span data-stu-id="e8c55-103">Create windows10MobileCompliancePolicy</span></span>

> <span data-ttu-id="e8c55-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="e8c55-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="e8c55-105">Crear un objeto [windows10MobileCompliancePolicy](../resources/intune-deviceconfig-windows10mobilecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="e8c55-105">Create a new [windows10MobileCompliancePolicy](../resources/intune-deviceconfig-windows10mobilecompliancepolicy.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="e8c55-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="e8c55-106">Prerequisites</span></span>
<span data-ttu-id="e8c55-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="e8c55-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="e8c55-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e8c55-109">Permission type</span></span>|<span data-ttu-id="e8c55-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e8c55-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="e8c55-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e8c55-111">Delegated (work or school account)</span></span>|<span data-ttu-id="e8c55-112">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="e8c55-112">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="e8c55-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e8c55-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="e8c55-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e8c55-114">Not supported.</span></span>|
|<span data-ttu-id="e8c55-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e8c55-115">Application</span></span>|<span data-ttu-id="e8c55-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e8c55-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="e8c55-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e8c55-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceCompliancePolicies
```

## <a name="request-headers"></a><span data-ttu-id="e8c55-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e8c55-118">Request headers</span></span>
|<span data-ttu-id="e8c55-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e8c55-119">Header</span></span>|<span data-ttu-id="e8c55-120">Valor</span><span class="sxs-lookup"><span data-stu-id="e8c55-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="e8c55-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="e8c55-121">Authorization</span></span>|<span data-ttu-id="e8c55-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="e8c55-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="e8c55-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="e8c55-123">Accept</span></span>|<span data-ttu-id="e8c55-124">application/json</span><span class="sxs-lookup"><span data-stu-id="e8c55-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="e8c55-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="e8c55-125">Request body</span></span>
<span data-ttu-id="e8c55-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto windows10MobileCompliancePolicy.</span><span class="sxs-lookup"><span data-stu-id="e8c55-126">In the request body, supply a JSON representation for the windows10MobileCompliancePolicy object.</span></span>

<span data-ttu-id="e8c55-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto windows10MobileCompliancePolicy.</span><span class="sxs-lookup"><span data-stu-id="e8c55-127">The following table shows the properties that are required when you create the windows10MobileCompliancePolicy.</span></span>

|<span data-ttu-id="e8c55-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e8c55-128">Property</span></span>|<span data-ttu-id="e8c55-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="e8c55-129">Type</span></span>|<span data-ttu-id="e8c55-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="e8c55-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="e8c55-131">id</span><span class="sxs-lookup"><span data-stu-id="e8c55-131">id</span></span>|<span data-ttu-id="e8c55-132">String</span><span class="sxs-lookup"><span data-stu-id="e8c55-132">String</span></span>|<span data-ttu-id="e8c55-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="e8c55-133">Key of the entity.</span></span> <span data-ttu-id="e8c55-134">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="e8c55-134">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="e8c55-135">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="e8c55-135">createdDateTime</span></span>|<span data-ttu-id="e8c55-136">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="e8c55-136">DateTimeOffset</span></span>|<span data-ttu-id="e8c55-137">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="e8c55-137">DateTime the object was created.</span></span> <span data-ttu-id="e8c55-138">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="e8c55-138">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="e8c55-139">descripción</span><span class="sxs-lookup"><span data-stu-id="e8c55-139">description</span></span>|<span data-ttu-id="e8c55-140">String</span><span class="sxs-lookup"><span data-stu-id="e8c55-140">String</span></span>|<span data-ttu-id="e8c55-141">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e8c55-141">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="e8c55-142">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="e8c55-142">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="e8c55-143">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="e8c55-143">lastModifiedDateTime</span></span>|<span data-ttu-id="e8c55-144">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="e8c55-144">DateTimeOffset</span></span>|<span data-ttu-id="e8c55-145">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="e8c55-145">DateTime the object was last modified.</span></span> <span data-ttu-id="e8c55-146">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="e8c55-146">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="e8c55-147">displayName</span><span class="sxs-lookup"><span data-stu-id="e8c55-147">displayName</span></span>|<span data-ttu-id="e8c55-148">String</span><span class="sxs-lookup"><span data-stu-id="e8c55-148">String</span></span>|<span data-ttu-id="e8c55-149">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e8c55-149">Admin provided name of the device configuration.</span></span> <span data-ttu-id="e8c55-150">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="e8c55-150">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="e8c55-151">version</span><span class="sxs-lookup"><span data-stu-id="e8c55-151">version</span></span>|<span data-ttu-id="e8c55-152">Int32</span><span class="sxs-lookup"><span data-stu-id="e8c55-152">Int32</span></span>|<span data-ttu-id="e8c55-153">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e8c55-153">Version of the device configuration.</span></span> <span data-ttu-id="e8c55-154">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="e8c55-154">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="e8c55-155">passwordRequired</span><span class="sxs-lookup"><span data-stu-id="e8c55-155">passwordRequired</span></span>|<span data-ttu-id="e8c55-156">Booleano</span><span class="sxs-lookup"><span data-stu-id="e8c55-156">Boolean</span></span>|<span data-ttu-id="e8c55-157">Exigir una contraseña para desbloquear el dispositivo de Windows Phone.</span><span class="sxs-lookup"><span data-stu-id="e8c55-157">Require a password to unlock Windows Phone device.</span></span>|
|<span data-ttu-id="e8c55-158">passwordBlockSimple</span><span class="sxs-lookup"><span data-stu-id="e8c55-158">passwordBlockSimple</span></span>|<span data-ttu-id="e8c55-159">Booleano</span><span class="sxs-lookup"><span data-stu-id="e8c55-159">Boolean</span></span>|<span data-ttu-id="e8c55-160">Si quiere bloquear o no la sincronización del calendario.</span><span class="sxs-lookup"><span data-stu-id="e8c55-160">Whether or not to block syncing the calendar.</span></span>|
|<span data-ttu-id="e8c55-161">passwordMinimumLength</span><span class="sxs-lookup"><span data-stu-id="e8c55-161">passwordMinimumLength</span></span>|<span data-ttu-id="e8c55-162">Int32</span><span class="sxs-lookup"><span data-stu-id="e8c55-162">Int32</span></span>|<span data-ttu-id="e8c55-163">Longitud mínima de la contraseña.</span><span class="sxs-lookup"><span data-stu-id="e8c55-163">Minimum password length.</span></span> <span data-ttu-id="e8c55-164">Valores válidos de 4 a 16</span><span class="sxs-lookup"><span data-stu-id="e8c55-164">Valid values 4 to 16</span></span>|
|<span data-ttu-id="e8c55-165">passwordMinimumCharacterSetCount</span><span class="sxs-lookup"><span data-stu-id="e8c55-165">passwordMinimumCharacterSetCount</span></span>|<span data-ttu-id="e8c55-166">Int32</span><span class="sxs-lookup"><span data-stu-id="e8c55-166">Int32</span></span>|<span data-ttu-id="e8c55-167">Número de juegos de caracteres necesarios en la contraseña.</span><span class="sxs-lookup"><span data-stu-id="e8c55-167">The number of character sets required in the password.</span></span>|
|<span data-ttu-id="e8c55-168">passwordRequiredType</span><span class="sxs-lookup"><span data-stu-id="e8c55-168">passwordRequiredType</span></span>|[<span data-ttu-id="e8c55-169">requiredPasswordType</span><span class="sxs-lookup"><span data-stu-id="e8c55-169">requiredPasswordType</span></span>](../resources/intune-deviceconfig-requiredpasswordtype.md)|<span data-ttu-id="e8c55-170">Tipo de contraseña necesaria.</span><span class="sxs-lookup"><span data-stu-id="e8c55-170">The required password type.</span></span> <span data-ttu-id="e8c55-171">Los valores posibles son: `deviceDefault`, `alphanumeric` y `numeric`.</span><span class="sxs-lookup"><span data-stu-id="e8c55-171">Possible values are: `deviceDefault`, `alphanumeric`, `numeric`.</span></span>|
|<span data-ttu-id="e8c55-172">passwordPreviousPasswordBlockCount</span><span class="sxs-lookup"><span data-stu-id="e8c55-172">passwordPreviousPasswordBlockCount</span></span>|<span data-ttu-id="e8c55-173">Int32</span><span class="sxs-lookup"><span data-stu-id="e8c55-173">Int32</span></span>|<span data-ttu-id="e8c55-174">Número de contraseñas anteriores que impide su reutilización.</span><span class="sxs-lookup"><span data-stu-id="e8c55-174">The number of previous passwords to prevent re-use of.</span></span>|
|<span data-ttu-id="e8c55-175">passwordExpirationDays</span><span class="sxs-lookup"><span data-stu-id="e8c55-175">passwordExpirationDays</span></span>|<span data-ttu-id="e8c55-176">Int32</span><span class="sxs-lookup"><span data-stu-id="e8c55-176">Int32</span></span>|<span data-ttu-id="e8c55-177">Número de días antes de que expire la contraseña.</span><span class="sxs-lookup"><span data-stu-id="e8c55-177">Number of days before password expiration.</span></span> <span data-ttu-id="e8c55-178">Valores válidos de 1 a 255</span><span class="sxs-lookup"><span data-stu-id="e8c55-178">Valid values 1 to 255</span></span>|
|<span data-ttu-id="e8c55-179">passwordMinutesOfInactivityBeforeLock</span><span class="sxs-lookup"><span data-stu-id="e8c55-179">passwordMinutesOfInactivityBeforeLock</span></span>|<span data-ttu-id="e8c55-180">Int32</span><span class="sxs-lookup"><span data-stu-id="e8c55-180">Int32</span></span>|<span data-ttu-id="e8c55-181">Minutos de inactividad antes de que sea necesaria una contraseña.</span><span class="sxs-lookup"><span data-stu-id="e8c55-181">Minutes of inactivity before a password is required.</span></span>|
|<span data-ttu-id="e8c55-182">passwordRequireToUnlockFromIdle</span><span class="sxs-lookup"><span data-stu-id="e8c55-182">passwordRequireToUnlockFromIdle</span></span>|<span data-ttu-id="e8c55-183">Booleano</span><span class="sxs-lookup"><span data-stu-id="e8c55-183">Boolean</span></span>|<span data-ttu-id="e8c55-184">Exige una contraseña para desbloquear el dispositivo inactivo.</span><span class="sxs-lookup"><span data-stu-id="e8c55-184">Require a password to unlock an idle device.</span></span>|
|<span data-ttu-id="e8c55-185">osMinimumVersion</span><span class="sxs-lookup"><span data-stu-id="e8c55-185">osMinimumVersion</span></span>|<span data-ttu-id="e8c55-186">String</span><span class="sxs-lookup"><span data-stu-id="e8c55-186">String</span></span>|<span data-ttu-id="e8c55-187">Versión mínima de Windows Phone.</span><span class="sxs-lookup"><span data-stu-id="e8c55-187">Minimum Windows Phone version.</span></span>|
|<span data-ttu-id="e8c55-188">osMaximumVersion</span><span class="sxs-lookup"><span data-stu-id="e8c55-188">osMaximumVersion</span></span>|<span data-ttu-id="e8c55-189">String</span><span class="sxs-lookup"><span data-stu-id="e8c55-189">String</span></span>|<span data-ttu-id="e8c55-190">Versión máxima de Windows Phone.</span><span class="sxs-lookup"><span data-stu-id="e8c55-190">Maximum Windows Phone version.</span></span>|
|<span data-ttu-id="e8c55-191">earlyLaunchAntiMalwareDriverEnabled</span><span class="sxs-lookup"><span data-stu-id="e8c55-191">earlyLaunchAntiMalwareDriverEnabled</span></span>|<span data-ttu-id="e8c55-192">Booleano</span><span class="sxs-lookup"><span data-stu-id="e8c55-192">Boolean</span></span>|<span data-ttu-id="e8c55-193">Exige que la atestación de estado de dispositivo Windows notifique los dispositivos como correctos; el controlador antimalware de inicio temprano está habilitado.</span><span class="sxs-lookup"><span data-stu-id="e8c55-193">Require devices to be reported as healthy by Windows Device Health Attestation - early launch antimalware driver is enabled.</span></span>|
|<span data-ttu-id="e8c55-194">bitLockerEnabled</span><span class="sxs-lookup"><span data-stu-id="e8c55-194">bitLockerEnabled</span></span>|<span data-ttu-id="e8c55-195">Booleano</span><span class="sxs-lookup"><span data-stu-id="e8c55-195">Boolean</span></span>|<span data-ttu-id="e8c55-196">Exige que la atestación de estado de dispositivo Windows notifique los dispositivos como correctos; BitLocker está habilitado.</span><span class="sxs-lookup"><span data-stu-id="e8c55-196">Require devices to be reported healthy by Windows Device Health Attestation - bit locker is enabled</span></span>|
|<span data-ttu-id="e8c55-197">secureBootEnabled</span><span class="sxs-lookup"><span data-stu-id="e8c55-197">secureBootEnabled</span></span>|<span data-ttu-id="e8c55-198">Booleano</span><span class="sxs-lookup"><span data-stu-id="e8c55-198">Boolean</span></span>|<span data-ttu-id="e8c55-199">Exige que la atestación de estado de dispositivo Windows notifique los dispositivos como correctos; el arranque seguro está habilitado.</span><span class="sxs-lookup"><span data-stu-id="e8c55-199">Require devices to be reported as healthy by Windows Device Health Attestation - secure boot is enabled.</span></span>|
|<span data-ttu-id="e8c55-200">codeIntegrityEnabled</span><span class="sxs-lookup"><span data-stu-id="e8c55-200">codeIntegrityEnabled</span></span>|<span data-ttu-id="e8c55-201">Booleano</span><span class="sxs-lookup"><span data-stu-id="e8c55-201">Boolean</span></span>|<span data-ttu-id="e8c55-202">Exige que la atestación de estado de dispositivo Windows notifique los dispositivos como correctos.</span><span class="sxs-lookup"><span data-stu-id="e8c55-202">Require devices to be reported as healthy by Windows Device Health Attestation.</span></span>|
|<span data-ttu-id="e8c55-203">storageRequireEncryption</span><span class="sxs-lookup"><span data-stu-id="e8c55-203">storageRequireEncryption</span></span>|<span data-ttu-id="e8c55-204">Booleano</span><span class="sxs-lookup"><span data-stu-id="e8c55-204">Boolean</span></span>|<span data-ttu-id="e8c55-205">Exige el cifrado en dispositivos Windows.</span><span class="sxs-lookup"><span data-stu-id="e8c55-205">Require encryption on windows devices.</span></span>|



## <a name="response"></a><span data-ttu-id="e8c55-206">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e8c55-206">Response</span></span>
<span data-ttu-id="e8c55-207">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [windows10MobileCompliancePolicy](../resources/intune-deviceconfig-windows10mobilecompliancepolicy.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e8c55-207">If successful, this method returns a `201 Created` response code and a [windows10MobileCompliancePolicy](../resources/intune-deviceconfig-windows10mobilecompliancepolicy.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="e8c55-208">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e8c55-208">Example</span></span>
### <a name="request"></a><span data-ttu-id="e8c55-209">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e8c55-209">Request</span></span>
<span data-ttu-id="e8c55-210">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e8c55-210">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceManagement/deviceCompliancePolicies
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

### <a name="response"></a><span data-ttu-id="e8c55-211">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e8c55-211">Response</span></span>
<span data-ttu-id="e8c55-p111">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="e8c55-p111">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
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



