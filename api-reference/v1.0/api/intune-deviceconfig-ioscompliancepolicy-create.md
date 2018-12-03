---
title: Crear iosCompliancePolicy
description: Crear un objeto iosCompliancePolicy.
ms.openlocfilehash: f21334d888a0885359e7caa4028bf8f1dea44cf1
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030687"
---
# <a name="create-ioscompliancepolicy"></a><span data-ttu-id="b52b5-103">Crear iosCompliancePolicy</span><span class="sxs-lookup"><span data-stu-id="b52b5-103">Create iosCompliancePolicy</span></span>

> <span data-ttu-id="b52b5-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="b52b5-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="b52b5-105">Crear un objeto [iosCompliancePolicy](../resources/intune-deviceconfig-ioscompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="b52b5-105">Create a new [iosCompliancePolicy](../resources/intune-deviceconfig-ioscompliancepolicy.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="b52b5-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="b52b5-106">Prerequisites</span></span>
<span data-ttu-id="b52b5-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="b52b5-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="b52b5-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b52b5-109">Permission type</span></span>|<span data-ttu-id="b52b5-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b52b5-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="b52b5-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b52b5-111">Delegated (work or school account)</span></span>|<span data-ttu-id="b52b5-112">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="b52b5-112">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="b52b5-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b52b5-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="b52b5-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b52b5-114">Not supported.</span></span>|
|<span data-ttu-id="b52b5-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b52b5-115">Application</span></span>|<span data-ttu-id="b52b5-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b52b5-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="b52b5-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b52b5-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceCompliancePolicies
```

## <a name="request-headers"></a><span data-ttu-id="b52b5-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b52b5-118">Request headers</span></span>
|<span data-ttu-id="b52b5-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b52b5-119">Header</span></span>|<span data-ttu-id="b52b5-120">Valor</span><span class="sxs-lookup"><span data-stu-id="b52b5-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="b52b5-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="b52b5-121">Authorization</span></span>|<span data-ttu-id="b52b5-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="b52b5-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="b52b5-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="b52b5-123">Accept</span></span>|<span data-ttu-id="b52b5-124">application/json</span><span class="sxs-lookup"><span data-stu-id="b52b5-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="b52b5-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b52b5-125">Request body</span></span>
<span data-ttu-id="b52b5-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto iosCompliancePolicy.</span><span class="sxs-lookup"><span data-stu-id="b52b5-126">In the request body, supply a JSON representation for the iosCompliancePolicy object.</span></span>

<span data-ttu-id="b52b5-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto iosCompliancePolicy.</span><span class="sxs-lookup"><span data-stu-id="b52b5-127">The following table shows the properties that are required when you create the iosCompliancePolicy.</span></span>

|<span data-ttu-id="b52b5-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="b52b5-128">Property</span></span>|<span data-ttu-id="b52b5-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="b52b5-129">Type</span></span>|<span data-ttu-id="b52b5-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="b52b5-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="b52b5-131">id</span><span class="sxs-lookup"><span data-stu-id="b52b5-131">id</span></span>|<span data-ttu-id="b52b5-132">String</span><span class="sxs-lookup"><span data-stu-id="b52b5-132">String</span></span>|<span data-ttu-id="b52b5-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="b52b5-133">Key of the entity.</span></span> <span data-ttu-id="b52b5-134">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="b52b5-134">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="b52b5-135">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="b52b5-135">createdDateTime</span></span>|<span data-ttu-id="b52b5-136">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="b52b5-136">DateTimeOffset</span></span>|<span data-ttu-id="b52b5-137">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="b52b5-137">DateTime the object was created.</span></span> <span data-ttu-id="b52b5-138">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="b52b5-138">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="b52b5-139">descripción</span><span class="sxs-lookup"><span data-stu-id="b52b5-139">description</span></span>|<span data-ttu-id="b52b5-140">String</span><span class="sxs-lookup"><span data-stu-id="b52b5-140">String</span></span>|<span data-ttu-id="b52b5-141">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b52b5-141">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="b52b5-142">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="b52b5-142">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="b52b5-143">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="b52b5-143">lastModifiedDateTime</span></span>|<span data-ttu-id="b52b5-144">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="b52b5-144">DateTimeOffset</span></span>|<span data-ttu-id="b52b5-145">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="b52b5-145">DateTime the object was last modified.</span></span> <span data-ttu-id="b52b5-146">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="b52b5-146">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="b52b5-147">displayName</span><span class="sxs-lookup"><span data-stu-id="b52b5-147">displayName</span></span>|<span data-ttu-id="b52b5-148">String</span><span class="sxs-lookup"><span data-stu-id="b52b5-148">String</span></span>|<span data-ttu-id="b52b5-149">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b52b5-149">Admin provided name of the device configuration.</span></span> <span data-ttu-id="b52b5-150">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="b52b5-150">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="b52b5-151">version</span><span class="sxs-lookup"><span data-stu-id="b52b5-151">version</span></span>|<span data-ttu-id="b52b5-152">Int32</span><span class="sxs-lookup"><span data-stu-id="b52b5-152">Int32</span></span>|<span data-ttu-id="b52b5-153">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b52b5-153">Version of the device configuration.</span></span> <span data-ttu-id="b52b5-154">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="b52b5-154">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="b52b5-155">passcodeBlockSimple</span><span class="sxs-lookup"><span data-stu-id="b52b5-155">passcodeBlockSimple</span></span>|<span data-ttu-id="b52b5-156">Booleano</span><span class="sxs-lookup"><span data-stu-id="b52b5-156">Boolean</span></span>|<span data-ttu-id="b52b5-157">Indica si se van a bloquear los códigos de acceso simples.</span><span class="sxs-lookup"><span data-stu-id="b52b5-157">Indicates whether or not to block simple passcodes.</span></span>|
|<span data-ttu-id="b52b5-158">passcodeExpirationDays</span><span class="sxs-lookup"><span data-stu-id="b52b5-158">passcodeExpirationDays</span></span>|<span data-ttu-id="b52b5-159">Int32</span><span class="sxs-lookup"><span data-stu-id="b52b5-159">Int32</span></span>|<span data-ttu-id="b52b5-160">Número de días antes de que expire el código de acceso.</span><span class="sxs-lookup"><span data-stu-id="b52b5-160">Number of days before the passcode expires.</span></span> <span data-ttu-id="b52b5-161">Valores válidos de 1 a 65535</span><span class="sxs-lookup"><span data-stu-id="b52b5-161">Valid values 1 to 65535</span></span>|
|<span data-ttu-id="b52b5-162">passcodeMinimumLength</span><span class="sxs-lookup"><span data-stu-id="b52b5-162">passcodeMinimumLength</span></span>|<span data-ttu-id="b52b5-163">Int32</span><span class="sxs-lookup"><span data-stu-id="b52b5-163">Int32</span></span>|<span data-ttu-id="b52b5-164">Longitud mínima de los códigos de acceso.</span><span class="sxs-lookup"><span data-stu-id="b52b5-164">Minimum length of passcode.</span></span> <span data-ttu-id="b52b5-165">Valores válidos de 4 a 14</span><span class="sxs-lookup"><span data-stu-id="b52b5-165">Valid values 4 to 14</span></span>|
|<span data-ttu-id="b52b5-166">passcodeMinutesOfInactivityBeforeLock</span><span class="sxs-lookup"><span data-stu-id="b52b5-166">passcodeMinutesOfInactivityBeforeLock</span></span>|<span data-ttu-id="b52b5-167">Int32</span><span class="sxs-lookup"><span data-stu-id="b52b5-167">Int32</span></span>|<span data-ttu-id="b52b5-168">Minutos de inactividad antes de que sea necesario un código de acceso.</span><span class="sxs-lookup"><span data-stu-id="b52b5-168">Minutes of inactivity before a passcode is required.</span></span>|
|<span data-ttu-id="b52b5-169">passcodePreviousPasscodeBlockCount</span><span class="sxs-lookup"><span data-stu-id="b52b5-169">passcodePreviousPasscodeBlockCount</span></span>|<span data-ttu-id="b52b5-170">Int32</span><span class="sxs-lookup"><span data-stu-id="b52b5-170">Int32</span></span>|<span data-ttu-id="b52b5-171">Número de códigos de acceso anteriores que bloquear.</span><span class="sxs-lookup"><span data-stu-id="b52b5-171">Number of previous passcodes to block.</span></span> <span data-ttu-id="b52b5-172">Valores válidos de 1 a 24.</span><span class="sxs-lookup"><span data-stu-id="b52b5-172">Valid values 1 to 24</span></span>|
|<span data-ttu-id="b52b5-173">passcodeMinimumCharacterSetCount</span><span class="sxs-lookup"><span data-stu-id="b52b5-173">passcodeMinimumCharacterSetCount</span></span>|<span data-ttu-id="b52b5-174">Int32</span><span class="sxs-lookup"><span data-stu-id="b52b5-174">Int32</span></span>|<span data-ttu-id="b52b5-175">Número de juegos de caracteres necesarios en la contraseña.</span><span class="sxs-lookup"><span data-stu-id="b52b5-175">The number of character sets required in the password.</span></span>|
|<span data-ttu-id="b52b5-176">passcodeRequiredType</span><span class="sxs-lookup"><span data-stu-id="b52b5-176">passcodeRequiredType</span></span>|[<span data-ttu-id="b52b5-177">requiredPasswordType</span><span class="sxs-lookup"><span data-stu-id="b52b5-177">requiredPasswordType</span></span>](../resources/intune-deviceconfig-requiredpasswordtype.md)|<span data-ttu-id="b52b5-178">Tipo de código de acceso necesario.</span><span class="sxs-lookup"><span data-stu-id="b52b5-178">The required passcode type.</span></span> <span data-ttu-id="b52b5-179">Los valores posibles son: `deviceDefault`, `alphanumeric` y `numeric`.</span><span class="sxs-lookup"><span data-stu-id="b52b5-179">Possible values are: `deviceDefault`, `alphanumeric`, `numeric`.</span></span>|
|<span data-ttu-id="b52b5-180">passcodeRequired</span><span class="sxs-lookup"><span data-stu-id="b52b5-180">passcodeRequired</span></span>|<span data-ttu-id="b52b5-181">Booleano</span><span class="sxs-lookup"><span data-stu-id="b52b5-181">Boolean</span></span>|<span data-ttu-id="b52b5-182">Indica si se va a requerir un código de acceso.</span><span class="sxs-lookup"><span data-stu-id="b52b5-182">Indicates whether or not to require a passcode.</span></span>|
|<span data-ttu-id="b52b5-183">osMinimumVersion</span><span class="sxs-lookup"><span data-stu-id="b52b5-183">osMinimumVersion</span></span>|<span data-ttu-id="b52b5-184">String</span><span class="sxs-lookup"><span data-stu-id="b52b5-184">String</span></span>|<span data-ttu-id="b52b5-185">Versión mínima de iOS.</span><span class="sxs-lookup"><span data-stu-id="b52b5-185">Minimum IOS version.</span></span>|
|<span data-ttu-id="b52b5-186">osMaximumVersion</span><span class="sxs-lookup"><span data-stu-id="b52b5-186">osMaximumVersion</span></span>|<span data-ttu-id="b52b5-187">String</span><span class="sxs-lookup"><span data-stu-id="b52b5-187">String</span></span>|<span data-ttu-id="b52b5-188">Versión máxima de iOS.</span><span class="sxs-lookup"><span data-stu-id="b52b5-188">Maximum IOS version.</span></span>|
|<span data-ttu-id="b52b5-189">securityBlockJailbrokenDevices</span><span class="sxs-lookup"><span data-stu-id="b52b5-189">securityBlockJailbrokenDevices</span></span>|<span data-ttu-id="b52b5-190">Booleano</span><span class="sxs-lookup"><span data-stu-id="b52b5-190">Boolean</span></span>|<span data-ttu-id="b52b5-191">No pueden usarse dispositivos con jailbreak o rooting.</span><span class="sxs-lookup"><span data-stu-id="b52b5-191">Devices must not be jailbroken or rooted.</span></span>|
|<span data-ttu-id="b52b5-192">deviceThreatProtectionEnabled</span><span class="sxs-lookup"><span data-stu-id="b52b5-192">deviceThreatProtectionEnabled</span></span>|<span data-ttu-id="b52b5-193">Booleano</span><span class="sxs-lookup"><span data-stu-id="b52b5-193">Boolean</span></span>|<span data-ttu-id="b52b5-194">Requiere que los dispositivos hayan habilitado la protección contra amenazas de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b52b5-194">Require that devices have enabled device threat protection .</span></span>|
|<span data-ttu-id="b52b5-195">deviceThreatProtectionRequiredSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="b52b5-195">deviceThreatProtectionRequiredSecurityLevel</span></span>|[<span data-ttu-id="b52b5-196">deviceThreatProtectionLevel</span><span class="sxs-lookup"><span data-stu-id="b52b5-196">deviceThreatProtectionLevel</span></span>](../resources/intune-deviceconfig-devicethreatprotectionlevel.md)|<span data-ttu-id="b52b5-197">Exigir que el nivel de riesgo mínimo de Mobile Threat Protection informe del no cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="b52b5-197">Require Mobile Threat Protection minimum risk level to report noncompliance.</span></span> <span data-ttu-id="b52b5-198">Los valores posibles son: `unavailable`, `secured`, `low`, `medium`, `high` y `notSet`.</span><span class="sxs-lookup"><span data-stu-id="b52b5-198">Possible values are: `unavailable`, `secured`, `low`, `medium`, `high`, `notSet`.</span></span>|
|<span data-ttu-id="b52b5-199">managedEmailProfileRequired</span><span class="sxs-lookup"><span data-stu-id="b52b5-199">managedEmailProfileRequired</span></span>|<span data-ttu-id="b52b5-200">Booleano</span><span class="sxs-lookup"><span data-stu-id="b52b5-200">Boolean</span></span>|<span data-ttu-id="b52b5-201">Indica si se va a requerir un perfil de correo electrónico administrado.</span><span class="sxs-lookup"><span data-stu-id="b52b5-201">Indicates whether or not to require a managed email profile.</span></span>|



## <a name="response"></a><span data-ttu-id="b52b5-202">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b52b5-202">Response</span></span>
<span data-ttu-id="b52b5-203">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [iosCompliancePolicy](../resources/intune-deviceconfig-ioscompliancepolicy.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b52b5-203">If successful, this method returns a `201 Created` response code and a [iosCompliancePolicy](../resources/intune-deviceconfig-ioscompliancepolicy.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="b52b5-204">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b52b5-204">Example</span></span>
### <a name="request"></a><span data-ttu-id="b52b5-205">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b52b5-205">Request</span></span>
<span data-ttu-id="b52b5-206">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b52b5-206">Here is an example of the request.</span></span>
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

### <a name="response"></a><span data-ttu-id="b52b5-207">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b52b5-207">Response</span></span>
<span data-ttu-id="b52b5-p113">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="b52b5-p113">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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



