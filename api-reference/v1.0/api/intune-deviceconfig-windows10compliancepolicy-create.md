---
title: Crear windows10CompliancePolicy
description: Cree un objeto windows10CompliancePolicy.
ms.openlocfilehash: d408c6663959c417196b54a5798317a021b1e35b
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030452"
---
# <a name="create-windows10compliancepolicy"></a><span data-ttu-id="28e1e-103">Crear windows10CompliancePolicy</span><span class="sxs-lookup"><span data-stu-id="28e1e-103">Create windows10CompliancePolicy</span></span>

> <span data-ttu-id="28e1e-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="28e1e-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="28e1e-105">Cree un objeto [windows10CompliancePolicy](../resources/intune-deviceconfig-windows10compliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="28e1e-105">Create a new [windows10CompliancePolicy](../resources/intune-deviceconfig-windows10compliancepolicy.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="28e1e-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="28e1e-106">Prerequisites</span></span>
<span data-ttu-id="28e1e-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="28e1e-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="28e1e-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="28e1e-109">Permission type</span></span>|<span data-ttu-id="28e1e-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="28e1e-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="28e1e-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="28e1e-111">Delegated (work or school account)</span></span>|<span data-ttu-id="28e1e-112">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="28e1e-112">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="28e1e-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="28e1e-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="28e1e-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="28e1e-114">Not supported.</span></span>|
|<span data-ttu-id="28e1e-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="28e1e-115">Application</span></span>|<span data-ttu-id="28e1e-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="28e1e-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="28e1e-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="28e1e-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceCompliancePolicies
```

## <a name="request-headers"></a><span data-ttu-id="28e1e-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="28e1e-118">Request headers</span></span>
|<span data-ttu-id="28e1e-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="28e1e-119">Header</span></span>|<span data-ttu-id="28e1e-120">Valor</span><span class="sxs-lookup"><span data-stu-id="28e1e-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="28e1e-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="28e1e-121">Authorization</span></span>|<span data-ttu-id="28e1e-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="28e1e-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="28e1e-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="28e1e-123">Accept</span></span>|<span data-ttu-id="28e1e-124">application/json</span><span class="sxs-lookup"><span data-stu-id="28e1e-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="28e1e-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="28e1e-125">Request body</span></span>
<span data-ttu-id="28e1e-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto windows10CompliancePolicy.</span><span class="sxs-lookup"><span data-stu-id="28e1e-126">In the request body, supply a JSON representation for the windows10CompliancePolicy object.</span></span>

<span data-ttu-id="28e1e-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto windows10CompliancePolicy.</span><span class="sxs-lookup"><span data-stu-id="28e1e-127">The following table shows the properties that are required when you create the windows10CompliancePolicy.</span></span>

|<span data-ttu-id="28e1e-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="28e1e-128">Property</span></span>|<span data-ttu-id="28e1e-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="28e1e-129">Type</span></span>|<span data-ttu-id="28e1e-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="28e1e-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="28e1e-131">id</span><span class="sxs-lookup"><span data-stu-id="28e1e-131">id</span></span>|<span data-ttu-id="28e1e-132">String</span><span class="sxs-lookup"><span data-stu-id="28e1e-132">String</span></span>|<span data-ttu-id="28e1e-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="28e1e-133">Key of the entity.</span></span> <span data-ttu-id="28e1e-134">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="28e1e-134">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="28e1e-135">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="28e1e-135">createdDateTime</span></span>|<span data-ttu-id="28e1e-136">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="28e1e-136">DateTimeOffset</span></span>|<span data-ttu-id="28e1e-137">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="28e1e-137">DateTime the object was created.</span></span> <span data-ttu-id="28e1e-138">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="28e1e-138">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="28e1e-139">descripción</span><span class="sxs-lookup"><span data-stu-id="28e1e-139">description</span></span>|<span data-ttu-id="28e1e-140">String</span><span class="sxs-lookup"><span data-stu-id="28e1e-140">String</span></span>|<span data-ttu-id="28e1e-141">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="28e1e-141">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="28e1e-142">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="28e1e-142">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="28e1e-143">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="28e1e-143">lastModifiedDateTime</span></span>|<span data-ttu-id="28e1e-144">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="28e1e-144">DateTimeOffset</span></span>|<span data-ttu-id="28e1e-145">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="28e1e-145">DateTime the object was last modified.</span></span> <span data-ttu-id="28e1e-146">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="28e1e-146">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="28e1e-147">displayName</span><span class="sxs-lookup"><span data-stu-id="28e1e-147">displayName</span></span>|<span data-ttu-id="28e1e-148">String</span><span class="sxs-lookup"><span data-stu-id="28e1e-148">String</span></span>|<span data-ttu-id="28e1e-149">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="28e1e-149">Admin provided name of the device configuration.</span></span> <span data-ttu-id="28e1e-150">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="28e1e-150">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="28e1e-151">version</span><span class="sxs-lookup"><span data-stu-id="28e1e-151">version</span></span>|<span data-ttu-id="28e1e-152">Int32</span><span class="sxs-lookup"><span data-stu-id="28e1e-152">Int32</span></span>|<span data-ttu-id="28e1e-153">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="28e1e-153">Version of the device configuration.</span></span> <span data-ttu-id="28e1e-154">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="28e1e-154">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="28e1e-155">passwordRequired</span><span class="sxs-lookup"><span data-stu-id="28e1e-155">passwordRequired</span></span>|<span data-ttu-id="28e1e-156">Booleano</span><span class="sxs-lookup"><span data-stu-id="28e1e-156">Boolean</span></span>|<span data-ttu-id="28e1e-157">Exige una contraseña para desbloquear el dispositivo Windows.</span><span class="sxs-lookup"><span data-stu-id="28e1e-157">Require a password to unlock Windows device.</span></span>|
|<span data-ttu-id="28e1e-158">passwordBlockSimple</span><span class="sxs-lookup"><span data-stu-id="28e1e-158">passwordBlockSimple</span></span>|<span data-ttu-id="28e1e-159">Booleano</span><span class="sxs-lookup"><span data-stu-id="28e1e-159">Boolean</span></span>|<span data-ttu-id="28e1e-160">Indica si quiere bloquear o no la contraseña simple.</span><span class="sxs-lookup"><span data-stu-id="28e1e-160">Indicates whether or not to block simple password.</span></span>|
|<span data-ttu-id="28e1e-161">passwordRequiredToUnlockFromIdle</span><span class="sxs-lookup"><span data-stu-id="28e1e-161">passwordRequiredToUnlockFromIdle</span></span>|<span data-ttu-id="28e1e-162">Booleano</span><span class="sxs-lookup"><span data-stu-id="28e1e-162">Boolean</span></span>|<span data-ttu-id="28e1e-163">Exige una contraseña para desbloquear el dispositivo inactivo.</span><span class="sxs-lookup"><span data-stu-id="28e1e-163">Require a password to unlock an idle device.</span></span>|
|<span data-ttu-id="28e1e-164">passwordMinutesOfInactivityBeforeLock</span><span class="sxs-lookup"><span data-stu-id="28e1e-164">passwordMinutesOfInactivityBeforeLock</span></span>|<span data-ttu-id="28e1e-165">Int32</span><span class="sxs-lookup"><span data-stu-id="28e1e-165">Int32</span></span>|<span data-ttu-id="28e1e-166">Minutos de inactividad antes de que sea necesaria una contraseña.</span><span class="sxs-lookup"><span data-stu-id="28e1e-166">Minutes of inactivity before a password is required.</span></span>|
|<span data-ttu-id="28e1e-167">passwordExpirationDays</span><span class="sxs-lookup"><span data-stu-id="28e1e-167">passwordExpirationDays</span></span>|<span data-ttu-id="28e1e-168">Int32</span><span class="sxs-lookup"><span data-stu-id="28e1e-168">Int32</span></span>|<span data-ttu-id="28e1e-169">La expiración de la contraseña en días.</span><span class="sxs-lookup"><span data-stu-id="28e1e-169">The password expiration in days.</span></span>|
|<span data-ttu-id="28e1e-170">passwordMinimumLength</span><span class="sxs-lookup"><span data-stu-id="28e1e-170">passwordMinimumLength</span></span>|<span data-ttu-id="28e1e-171">Int32</span><span class="sxs-lookup"><span data-stu-id="28e1e-171">Int32</span></span>|<span data-ttu-id="28e1e-172">La longitud mínima de contraseña.</span><span class="sxs-lookup"><span data-stu-id="28e1e-172">The minimum password length.</span></span>|
|<span data-ttu-id="28e1e-173">passwordMinimumCharacterSetCount</span><span class="sxs-lookup"><span data-stu-id="28e1e-173">passwordMinimumCharacterSetCount</span></span>|<span data-ttu-id="28e1e-174">Int32</span><span class="sxs-lookup"><span data-stu-id="28e1e-174">Int32</span></span>|<span data-ttu-id="28e1e-175">Número de juegos de caracteres necesarios en la contraseña.</span><span class="sxs-lookup"><span data-stu-id="28e1e-175">The number of character sets required in the password.</span></span>|
|<span data-ttu-id="28e1e-176">passwordRequiredType</span><span class="sxs-lookup"><span data-stu-id="28e1e-176">passwordRequiredType</span></span>|[<span data-ttu-id="28e1e-177">requiredPasswordType</span><span class="sxs-lookup"><span data-stu-id="28e1e-177">requiredPasswordType</span></span>](../resources/intune-deviceconfig-requiredpasswordtype.md)|<span data-ttu-id="28e1e-178">Tipo de contraseña necesaria.</span><span class="sxs-lookup"><span data-stu-id="28e1e-178">The required password type.</span></span> <span data-ttu-id="28e1e-179">Los valores posibles son: `deviceDefault`, `alphanumeric` y `numeric`.</span><span class="sxs-lookup"><span data-stu-id="28e1e-179">Possible values are: `deviceDefault`, `alphanumeric`, `numeric`.</span></span>|
|<span data-ttu-id="28e1e-180">passwordPreviousPasswordBlockCount</span><span class="sxs-lookup"><span data-stu-id="28e1e-180">passwordPreviousPasswordBlockCount</span></span>|<span data-ttu-id="28e1e-181">Int32</span><span class="sxs-lookup"><span data-stu-id="28e1e-181">Int32</span></span>|<span data-ttu-id="28e1e-182">Número de contraseñas anteriores que impide su reutilización.</span><span class="sxs-lookup"><span data-stu-id="28e1e-182">The number of previous passwords to prevent re-use of.</span></span>|
|<span data-ttu-id="28e1e-183">requireHealthyDeviceReport</span><span class="sxs-lookup"><span data-stu-id="28e1e-183">requireHealthyDeviceReport</span></span>|<span data-ttu-id="28e1e-184">Booleano</span><span class="sxs-lookup"><span data-stu-id="28e1e-184">Boolean</span></span>|<span data-ttu-id="28e1e-185">Exige que la atestación de estado de dispositivo Windows notifique los dispositivos como correctos.</span><span class="sxs-lookup"><span data-stu-id="28e1e-185">Require devices to be reported as healthy by Windows Device Health Attestation.</span></span>|
|<span data-ttu-id="28e1e-186">osMinimumVersion</span><span class="sxs-lookup"><span data-stu-id="28e1e-186">osMinimumVersion</span></span>|<span data-ttu-id="28e1e-187">String</span><span class="sxs-lookup"><span data-stu-id="28e1e-187">String</span></span>|<span data-ttu-id="28e1e-188">Versión mínima de Windows 10.</span><span class="sxs-lookup"><span data-stu-id="28e1e-188">Minimum Windows 10 version.</span></span>|
|<span data-ttu-id="28e1e-189">osMaximumVersion</span><span class="sxs-lookup"><span data-stu-id="28e1e-189">osMaximumVersion</span></span>|<span data-ttu-id="28e1e-190">String</span><span class="sxs-lookup"><span data-stu-id="28e1e-190">String</span></span>|<span data-ttu-id="28e1e-191">Versión máxima de Windows 10.</span><span class="sxs-lookup"><span data-stu-id="28e1e-191">Maximum Windows 10 version.</span></span>|
|<span data-ttu-id="28e1e-192">mobileOsMinimumVersion</span><span class="sxs-lookup"><span data-stu-id="28e1e-192">mobileOsMinimumVersion</span></span>|<span data-ttu-id="28e1e-193">String</span><span class="sxs-lookup"><span data-stu-id="28e1e-193">String</span></span>|<span data-ttu-id="28e1e-194">Versión mínima de Windows Phone.</span><span class="sxs-lookup"><span data-stu-id="28e1e-194">Minimum Windows Phone version.</span></span>|
|<span data-ttu-id="28e1e-195">mobileOsMaximumVersion</span><span class="sxs-lookup"><span data-stu-id="28e1e-195">mobileOsMaximumVersion</span></span>|<span data-ttu-id="28e1e-196">String</span><span class="sxs-lookup"><span data-stu-id="28e1e-196">String</span></span>|<span data-ttu-id="28e1e-197">Versión máxima de Windows Phone.</span><span class="sxs-lookup"><span data-stu-id="28e1e-197">Maximum Windows Phone version.</span></span>|
|<span data-ttu-id="28e1e-198">earlyLaunchAntiMalwareDriverEnabled</span><span class="sxs-lookup"><span data-stu-id="28e1e-198">earlyLaunchAntiMalwareDriverEnabled</span></span>|<span data-ttu-id="28e1e-199">Booleano</span><span class="sxs-lookup"><span data-stu-id="28e1e-199">Boolean</span></span>|<span data-ttu-id="28e1e-200">Exige que la atestación de estado de dispositivo Windows notifique los dispositivos como correctos; el controlador antimalware de inicio temprano está habilitado.</span><span class="sxs-lookup"><span data-stu-id="28e1e-200">Require devices to be reported as healthy by Windows Device Health Attestation - early launch antimalware driver is enabled.</span></span>|
|<span data-ttu-id="28e1e-201">bitLockerEnabled</span><span class="sxs-lookup"><span data-stu-id="28e1e-201">bitLockerEnabled</span></span>|<span data-ttu-id="28e1e-202">Booleano</span><span class="sxs-lookup"><span data-stu-id="28e1e-202">Boolean</span></span>|<span data-ttu-id="28e1e-203">Exige que la atestación de estado de dispositivo Windows notifique los dispositivos como correctos; BitLocker está habilitado.</span><span class="sxs-lookup"><span data-stu-id="28e1e-203">Require devices to be reported healthy by Windows Device Health Attestation - bit locker is enabled</span></span>|
|<span data-ttu-id="28e1e-204">secureBootEnabled</span><span class="sxs-lookup"><span data-stu-id="28e1e-204">secureBootEnabled</span></span>|<span data-ttu-id="28e1e-205">Booleano</span><span class="sxs-lookup"><span data-stu-id="28e1e-205">Boolean</span></span>|<span data-ttu-id="28e1e-206">Exige que la atestación de estado de dispositivo Windows notifique los dispositivos como correctos; el arranque seguro está habilitado.</span><span class="sxs-lookup"><span data-stu-id="28e1e-206">Require devices to be reported as healthy by Windows Device Health Attestation - secure boot is enabled.</span></span>|
|<span data-ttu-id="28e1e-207">codeIntegrityEnabled</span><span class="sxs-lookup"><span data-stu-id="28e1e-207">codeIntegrityEnabled</span></span>|<span data-ttu-id="28e1e-208">Booleano</span><span class="sxs-lookup"><span data-stu-id="28e1e-208">Boolean</span></span>|<span data-ttu-id="28e1e-209">Exige que la atestación de estado de dispositivo Windows notifique los dispositivos como correctos.</span><span class="sxs-lookup"><span data-stu-id="28e1e-209">Require devices to be reported as healthy by Windows Device Health Attestation.</span></span>|
|<span data-ttu-id="28e1e-210">storageRequireEncryption</span><span class="sxs-lookup"><span data-stu-id="28e1e-210">storageRequireEncryption</span></span>|<span data-ttu-id="28e1e-211">Booleano</span><span class="sxs-lookup"><span data-stu-id="28e1e-211">Boolean</span></span>|<span data-ttu-id="28e1e-212">Exige el cifrado en dispositivos Windows.</span><span class="sxs-lookup"><span data-stu-id="28e1e-212">Require encryption on windows devices.</span></span>|



## <a name="response"></a><span data-ttu-id="28e1e-213">Respuesta</span><span class="sxs-lookup"><span data-stu-id="28e1e-213">Response</span></span>
<span data-ttu-id="28e1e-214">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [windows10CompliancePolicy](../resources/intune-deviceconfig-windows10compliancepolicy.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="28e1e-214">If successful, this method returns a `201 Created` response code and a [windows10CompliancePolicy](../resources/intune-deviceconfig-windows10compliancepolicy.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="28e1e-215">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="28e1e-215">Example</span></span>
### <a name="request"></a><span data-ttu-id="28e1e-216">Solicitud</span><span class="sxs-lookup"><span data-stu-id="28e1e-216">Request</span></span>
<span data-ttu-id="28e1e-217">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="28e1e-217">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceManagement/deviceCompliancePolicies
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

### <a name="response"></a><span data-ttu-id="28e1e-218">Respuesta</span><span class="sxs-lookup"><span data-stu-id="28e1e-218">Response</span></span>
<span data-ttu-id="28e1e-p109">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="28e1e-p109">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
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



