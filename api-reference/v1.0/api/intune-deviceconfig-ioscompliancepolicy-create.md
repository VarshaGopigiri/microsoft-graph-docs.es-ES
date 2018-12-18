---
title: Crear iosCompliancePolicy
description: Crear un objeto iosCompliancePolicy.
author: tfitzmac
ms.openlocfilehash: fd039005455c94cf55fa1afe21eee33fde9b4588
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27346176"
---
# <a name="create-ioscompliancepolicy"></a><span data-ttu-id="1436e-103">Crear iosCompliancePolicy</span><span class="sxs-lookup"><span data-stu-id="1436e-103">Create iosCompliancePolicy</span></span>

> <span data-ttu-id="1436e-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="1436e-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="1436e-105">Crear un objeto [iosCompliancePolicy](../resources/intune-deviceconfig-ioscompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="1436e-105">Create a new [iosCompliancePolicy](../resources/intune-deviceconfig-ioscompliancepolicy.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="1436e-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="1436e-106">Prerequisites</span></span>
<span data-ttu-id="1436e-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="1436e-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="1436e-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="1436e-109">Permission type</span></span>|<span data-ttu-id="1436e-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="1436e-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="1436e-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="1436e-111">Delegated (work or school account)</span></span>|<span data-ttu-id="1436e-112">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="1436e-112">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="1436e-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="1436e-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="1436e-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1436e-114">Not supported.</span></span>|
|<span data-ttu-id="1436e-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="1436e-115">Application</span></span>|<span data-ttu-id="1436e-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1436e-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="1436e-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="1436e-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceCompliancePolicies
```

## <a name="request-headers"></a><span data-ttu-id="1436e-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="1436e-118">Request headers</span></span>
|<span data-ttu-id="1436e-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1436e-119">Header</span></span>|<span data-ttu-id="1436e-120">Valor</span><span class="sxs-lookup"><span data-stu-id="1436e-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="1436e-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="1436e-121">Authorization</span></span>|<span data-ttu-id="1436e-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="1436e-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="1436e-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="1436e-123">Accept</span></span>|<span data-ttu-id="1436e-124">application/json</span><span class="sxs-lookup"><span data-stu-id="1436e-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="1436e-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="1436e-125">Request body</span></span>
<span data-ttu-id="1436e-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto iosCompliancePolicy.</span><span class="sxs-lookup"><span data-stu-id="1436e-126">In the request body, supply a JSON representation for the iosCompliancePolicy object.</span></span>

<span data-ttu-id="1436e-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto iosCompliancePolicy.</span><span class="sxs-lookup"><span data-stu-id="1436e-127">The following table shows the properties that are required when you create the iosCompliancePolicy.</span></span>

|<span data-ttu-id="1436e-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="1436e-128">Property</span></span>|<span data-ttu-id="1436e-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="1436e-129">Type</span></span>|<span data-ttu-id="1436e-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="1436e-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="1436e-131">id</span><span class="sxs-lookup"><span data-stu-id="1436e-131">id</span></span>|<span data-ttu-id="1436e-132">String</span><span class="sxs-lookup"><span data-stu-id="1436e-132">String</span></span>|<span data-ttu-id="1436e-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="1436e-133">Key of the entity.</span></span> <span data-ttu-id="1436e-134">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="1436e-134">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="1436e-135">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="1436e-135">createdDateTime</span></span>|<span data-ttu-id="1436e-136">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="1436e-136">DateTimeOffset</span></span>|<span data-ttu-id="1436e-137">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="1436e-137">DateTime the object was created.</span></span> <span data-ttu-id="1436e-138">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="1436e-138">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="1436e-139">descripción</span><span class="sxs-lookup"><span data-stu-id="1436e-139">description</span></span>|<span data-ttu-id="1436e-140">String</span><span class="sxs-lookup"><span data-stu-id="1436e-140">String</span></span>|<span data-ttu-id="1436e-141">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1436e-141">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="1436e-142">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="1436e-142">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="1436e-143">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="1436e-143">lastModifiedDateTime</span></span>|<span data-ttu-id="1436e-144">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="1436e-144">DateTimeOffset</span></span>|<span data-ttu-id="1436e-145">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="1436e-145">DateTime the object was last modified.</span></span> <span data-ttu-id="1436e-146">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="1436e-146">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="1436e-147">displayName</span><span class="sxs-lookup"><span data-stu-id="1436e-147">displayName</span></span>|<span data-ttu-id="1436e-148">String</span><span class="sxs-lookup"><span data-stu-id="1436e-148">String</span></span>|<span data-ttu-id="1436e-149">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1436e-149">Admin provided name of the device configuration.</span></span> <span data-ttu-id="1436e-150">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="1436e-150">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="1436e-151">version</span><span class="sxs-lookup"><span data-stu-id="1436e-151">version</span></span>|<span data-ttu-id="1436e-152">Int32</span><span class="sxs-lookup"><span data-stu-id="1436e-152">Int32</span></span>|<span data-ttu-id="1436e-153">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1436e-153">Version of the device configuration.</span></span> <span data-ttu-id="1436e-154">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="1436e-154">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="1436e-155">passcodeBlockSimple</span><span class="sxs-lookup"><span data-stu-id="1436e-155">passcodeBlockSimple</span></span>|<span data-ttu-id="1436e-156">Boolean</span><span class="sxs-lookup"><span data-stu-id="1436e-156">Boolean</span></span>|<span data-ttu-id="1436e-157">Indica si se van a bloquear los códigos de acceso simples.</span><span class="sxs-lookup"><span data-stu-id="1436e-157">Indicates whether or not to block simple passcodes.</span></span>|
|<span data-ttu-id="1436e-158">passcodeExpirationDays</span><span class="sxs-lookup"><span data-stu-id="1436e-158">passcodeExpirationDays</span></span>|<span data-ttu-id="1436e-159">Int32</span><span class="sxs-lookup"><span data-stu-id="1436e-159">Int32</span></span>|<span data-ttu-id="1436e-160">Número de días antes de que expire el código de acceso.</span><span class="sxs-lookup"><span data-stu-id="1436e-160">Number of days before the passcode expires.</span></span> <span data-ttu-id="1436e-161">Valores válidos de 1 a 65535</span><span class="sxs-lookup"><span data-stu-id="1436e-161">Valid values 1 to 65535</span></span>|
|<span data-ttu-id="1436e-162">passcodeMinimumLength</span><span class="sxs-lookup"><span data-stu-id="1436e-162">passcodeMinimumLength</span></span>|<span data-ttu-id="1436e-163">Int32</span><span class="sxs-lookup"><span data-stu-id="1436e-163">Int32</span></span>|<span data-ttu-id="1436e-164">Longitud mínima de los códigos de acceso.</span><span class="sxs-lookup"><span data-stu-id="1436e-164">Minimum length of passcode.</span></span> <span data-ttu-id="1436e-165">Valores válidos de 4 a 14</span><span class="sxs-lookup"><span data-stu-id="1436e-165">Valid values 4 to 14</span></span>|
|<span data-ttu-id="1436e-166">passcodeMinutesOfInactivityBeforeLock</span><span class="sxs-lookup"><span data-stu-id="1436e-166">passcodeMinutesOfInactivityBeforeLock</span></span>|<span data-ttu-id="1436e-167">Int32</span><span class="sxs-lookup"><span data-stu-id="1436e-167">Int32</span></span>|<span data-ttu-id="1436e-168">Minutos de inactividad antes de que sea necesario un código de acceso.</span><span class="sxs-lookup"><span data-stu-id="1436e-168">Minutes of inactivity before a passcode is required.</span></span>|
|<span data-ttu-id="1436e-169">passcodePreviousPasscodeBlockCount</span><span class="sxs-lookup"><span data-stu-id="1436e-169">passcodePreviousPasscodeBlockCount</span></span>|<span data-ttu-id="1436e-170">Int32</span><span class="sxs-lookup"><span data-stu-id="1436e-170">Int32</span></span>|<span data-ttu-id="1436e-171">Número de códigos de acceso anteriores que bloquear.</span><span class="sxs-lookup"><span data-stu-id="1436e-171">Number of previous passcodes to block.</span></span> <span data-ttu-id="1436e-172">Valores válidos de 1 a 24.</span><span class="sxs-lookup"><span data-stu-id="1436e-172">Valid values 1 to 24</span></span>|
|<span data-ttu-id="1436e-173">passcodeMinimumCharacterSetCount</span><span class="sxs-lookup"><span data-stu-id="1436e-173">passcodeMinimumCharacterSetCount</span></span>|<span data-ttu-id="1436e-174">Int32</span><span class="sxs-lookup"><span data-stu-id="1436e-174">Int32</span></span>|<span data-ttu-id="1436e-175">Número de juegos de caracteres necesarios en la contraseña.</span><span class="sxs-lookup"><span data-stu-id="1436e-175">The number of character sets required in the password.</span></span>|
|<span data-ttu-id="1436e-176">passcodeRequiredType</span><span class="sxs-lookup"><span data-stu-id="1436e-176">passcodeRequiredType</span></span>|[<span data-ttu-id="1436e-177">requiredPasswordType</span><span class="sxs-lookup"><span data-stu-id="1436e-177">requiredPasswordType</span></span>](../resources/intune-deviceconfig-requiredpasswordtype.md)|<span data-ttu-id="1436e-178">Tipo de código de acceso necesario.</span><span class="sxs-lookup"><span data-stu-id="1436e-178">The required passcode type.</span></span> <span data-ttu-id="1436e-179">Los valores posibles son: `deviceDefault`, `alphanumeric` y `numeric`.</span><span class="sxs-lookup"><span data-stu-id="1436e-179">Possible values are: `deviceDefault`, `alphanumeric`, `numeric`.</span></span>|
|<span data-ttu-id="1436e-180">passcodeRequired</span><span class="sxs-lookup"><span data-stu-id="1436e-180">passcodeRequired</span></span>|<span data-ttu-id="1436e-181">Boolean</span><span class="sxs-lookup"><span data-stu-id="1436e-181">Boolean</span></span>|<span data-ttu-id="1436e-182">Indica si se va a requerir un código de acceso.</span><span class="sxs-lookup"><span data-stu-id="1436e-182">Indicates whether or not to require a passcode.</span></span>|
|<span data-ttu-id="1436e-183">osMinimumVersion</span><span class="sxs-lookup"><span data-stu-id="1436e-183">osMinimumVersion</span></span>|<span data-ttu-id="1436e-184">String</span><span class="sxs-lookup"><span data-stu-id="1436e-184">String</span></span>|<span data-ttu-id="1436e-185">Versión mínima de iOS.</span><span class="sxs-lookup"><span data-stu-id="1436e-185">Minimum IOS version.</span></span>|
|<span data-ttu-id="1436e-186">osMaximumVersion</span><span class="sxs-lookup"><span data-stu-id="1436e-186">osMaximumVersion</span></span>|<span data-ttu-id="1436e-187">String</span><span class="sxs-lookup"><span data-stu-id="1436e-187">String</span></span>|<span data-ttu-id="1436e-188">Versión máxima de iOS.</span><span class="sxs-lookup"><span data-stu-id="1436e-188">Maximum IOS version.</span></span>|
|<span data-ttu-id="1436e-189">securityBlockJailbrokenDevices</span><span class="sxs-lookup"><span data-stu-id="1436e-189">securityBlockJailbrokenDevices</span></span>|<span data-ttu-id="1436e-190">Boolean</span><span class="sxs-lookup"><span data-stu-id="1436e-190">Boolean</span></span>|<span data-ttu-id="1436e-191">No pueden usarse dispositivos con jailbreak o rooting.</span><span class="sxs-lookup"><span data-stu-id="1436e-191">Devices must not be jailbroken or rooted.</span></span>|
|<span data-ttu-id="1436e-192">deviceThreatProtectionEnabled</span><span class="sxs-lookup"><span data-stu-id="1436e-192">deviceThreatProtectionEnabled</span></span>|<span data-ttu-id="1436e-193">Booleano</span><span class="sxs-lookup"><span data-stu-id="1436e-193">Boolean</span></span>|<span data-ttu-id="1436e-194">Requiere que los dispositivos hayan habilitado la protección contra amenazas de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1436e-194">Require that devices have enabled device threat protection .</span></span>|
|<span data-ttu-id="1436e-195">deviceThreatProtectionRequiredSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="1436e-195">deviceThreatProtectionRequiredSecurityLevel</span></span>|[<span data-ttu-id="1436e-196">deviceThreatProtectionLevel</span><span class="sxs-lookup"><span data-stu-id="1436e-196">deviceThreatProtectionLevel</span></span>](../resources/intune-deviceconfig-devicethreatprotectionlevel.md)|<span data-ttu-id="1436e-197">Exigir que el nivel de riesgo mínimo de Mobile Threat Protection informe del no cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="1436e-197">Require Mobile Threat Protection minimum risk level to report noncompliance.</span></span> <span data-ttu-id="1436e-198">Los valores posibles son: `unavailable`, `secured`, `low`, `medium`, `high` y `notSet`.</span><span class="sxs-lookup"><span data-stu-id="1436e-198">Possible values are: `unavailable`, `secured`, `low`, `medium`, `high`, `notSet`.</span></span>|
|<span data-ttu-id="1436e-199">managedEmailProfileRequired</span><span class="sxs-lookup"><span data-stu-id="1436e-199">managedEmailProfileRequired</span></span>|<span data-ttu-id="1436e-200">Booleano</span><span class="sxs-lookup"><span data-stu-id="1436e-200">Boolean</span></span>|<span data-ttu-id="1436e-201">Indica si se va a requerir un perfil de correo electrónico administrado.</span><span class="sxs-lookup"><span data-stu-id="1436e-201">Indicates whether or not to require a managed email profile.</span></span>|



## <a name="response"></a><span data-ttu-id="1436e-202">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1436e-202">Response</span></span>
<span data-ttu-id="1436e-203">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [iosCompliancePolicy](../resources/intune-deviceconfig-ioscompliancepolicy.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1436e-203">If successful, this method returns a `201 Created` response code and a [iosCompliancePolicy](../resources/intune-deviceconfig-ioscompliancepolicy.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="1436e-204">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1436e-204">Example</span></span>
### <a name="request"></a><span data-ttu-id="1436e-205">Solicitud</span><span class="sxs-lookup"><span data-stu-id="1436e-205">Request</span></span>
<span data-ttu-id="1436e-206">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="1436e-206">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceManagement/deviceCompliancePolicies
Content-type: application/json
Content-length: 745

{
  "@odata.type": "#microsoft.graph.iosCompliancePolicy",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "passcodeBlockSimple": true,
  "passcodeExpirationDays": 6,
  "passcodeMinimumLength": 5,
  "passcodeMinutesOfInactivityBeforeLock": 5,
  "passcodePreviousPasscodeBlockCount": 2,
  "passcodeMinimumCharacterSetCount": 0,
  "passcodeRequiredType": "alphanumeric",
  "passcodeRequired": true,
  "osMinimumVersion": "Os Minimum Version value",
  "osMaximumVersion": "Os Maximum Version value",
  "securityBlockJailbrokenDevices": true,
  "deviceThreatProtectionEnabled": true,
  "deviceThreatProtectionRequiredSecurityLevel": "secured",
  "managedEmailProfileRequired": true
}
```

### <a name="response"></a><span data-ttu-id="1436e-207">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1436e-207">Response</span></span>
<span data-ttu-id="1436e-p113">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="1436e-p113">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 917

{
  "@odata.type": "#microsoft.graph.iosCompliancePolicy",
  "id": "4f501351-1351-4f50-5113-504f5113504f",
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "description": "Description value",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "displayName": "Display Name value",
  "version": 7,
  "passcodeBlockSimple": true,
  "passcodeExpirationDays": 6,
  "passcodeMinimumLength": 5,
  "passcodeMinutesOfInactivityBeforeLock": 5,
  "passcodePreviousPasscodeBlockCount": 2,
  "passcodeMinimumCharacterSetCount": 0,
  "passcodeRequiredType": "alphanumeric",
  "passcodeRequired": true,
  "osMinimumVersion": "Os Minimum Version value",
  "osMaximumVersion": "Os Maximum Version value",
  "securityBlockJailbrokenDevices": true,
  "deviceThreatProtectionEnabled": true,
  "deviceThreatProtectionRequiredSecurityLevel": "secured",
  "managedEmailProfileRequired": true
}
```



