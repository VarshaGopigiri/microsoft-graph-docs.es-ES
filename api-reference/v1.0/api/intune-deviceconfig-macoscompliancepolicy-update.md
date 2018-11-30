---
title: Actualizar macOSCompliancePolicy
description: Actualice las propiedades de un objeto macOSCompliancePolicy.
ms.openlocfilehash: 99b4586ee0651a34630b25719425290cf700fef3
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029501"
---
# <a name="update-macoscompliancepolicy"></a><span data-ttu-id="5c3bf-103">Actualizar macOSCompliancePolicy</span><span class="sxs-lookup"><span data-stu-id="5c3bf-103">Update macOSCompliancePolicy</span></span>

> <span data-ttu-id="5c3bf-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="5c3bf-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="5c3bf-105">Actualice las propiedades de un objeto [macOSCompliancePolicy](../resources/intune-deviceconfig-macoscompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="5c3bf-105">Update the properties of a [macOSCompliancePolicy](../resources/intune-deviceconfig-macoscompliancepolicy.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="5c3bf-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="5c3bf-106">Prerequisites</span></span>
<span data-ttu-id="5c3bf-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="5c3bf-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="5c3bf-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="5c3bf-109">Permission type</span></span>|<span data-ttu-id="5c3bf-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="5c3bf-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="5c3bf-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="5c3bf-111">Delegated (work or school account)</span></span>|<span data-ttu-id="5c3bf-112">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="5c3bf-112">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="5c3bf-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="5c3bf-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="5c3bf-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5c3bf-114">Not supported.</span></span>|
|<span data-ttu-id="5c3bf-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="5c3bf-115">Application</span></span>|<span data-ttu-id="5c3bf-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5c3bf-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="5c3bf-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="5c3bf-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}
```

## <a name="request-headers"></a><span data-ttu-id="5c3bf-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="5c3bf-118">Request headers</span></span>
|<span data-ttu-id="5c3bf-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5c3bf-119">Header</span></span>|<span data-ttu-id="5c3bf-120">Valor</span><span class="sxs-lookup"><span data-stu-id="5c3bf-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="5c3bf-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="5c3bf-121">Authorization</span></span>|<span data-ttu-id="5c3bf-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="5c3bf-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="5c3bf-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="5c3bf-123">Accept</span></span>|<span data-ttu-id="5c3bf-124">application/json</span><span class="sxs-lookup"><span data-stu-id="5c3bf-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="5c3bf-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="5c3bf-125">Request body</span></span>
<span data-ttu-id="5c3bf-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto [macOSCompliancePolicy](../resources/intune-deviceconfig-macoscompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="5c3bf-126">In the request body, supply a JSON representation for the [macOSCompliancePolicy](../resources/intune-deviceconfig-macoscompliancepolicy.md) object.</span></span>

<span data-ttu-id="5c3bf-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [macOSCompliancePolicy](../resources/intune-deviceconfig-macoscompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="5c3bf-127">The following table shows the properties that are required when you create the [macOSCompliancePolicy](../resources/intune-deviceconfig-macoscompliancepolicy.md).</span></span>

|<span data-ttu-id="5c3bf-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="5c3bf-128">Property</span></span>|<span data-ttu-id="5c3bf-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="5c3bf-129">Type</span></span>|<span data-ttu-id="5c3bf-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="5c3bf-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="5c3bf-131">id</span><span class="sxs-lookup"><span data-stu-id="5c3bf-131">id</span></span>|<span data-ttu-id="5c3bf-132">String</span><span class="sxs-lookup"><span data-stu-id="5c3bf-132">String</span></span>|<span data-ttu-id="5c3bf-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="5c3bf-133">Key of the entity.</span></span> <span data-ttu-id="5c3bf-134">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="5c3bf-134">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="5c3bf-135">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="5c3bf-135">createdDateTime</span></span>|<span data-ttu-id="5c3bf-136">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="5c3bf-136">DateTimeOffset</span></span>|<span data-ttu-id="5c3bf-137">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="5c3bf-137">DateTime the object was created.</span></span> <span data-ttu-id="5c3bf-138">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="5c3bf-138">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="5c3bf-139">descripción</span><span class="sxs-lookup"><span data-stu-id="5c3bf-139">description</span></span>|<span data-ttu-id="5c3bf-140">String</span><span class="sxs-lookup"><span data-stu-id="5c3bf-140">String</span></span>|<span data-ttu-id="5c3bf-141">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5c3bf-141">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="5c3bf-142">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="5c3bf-142">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="5c3bf-143">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="5c3bf-143">lastModifiedDateTime</span></span>|<span data-ttu-id="5c3bf-144">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="5c3bf-144">DateTimeOffset</span></span>|<span data-ttu-id="5c3bf-145">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="5c3bf-145">DateTime the object was last modified.</span></span> <span data-ttu-id="5c3bf-146">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="5c3bf-146">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="5c3bf-147">displayName</span><span class="sxs-lookup"><span data-stu-id="5c3bf-147">displayName</span></span>|<span data-ttu-id="5c3bf-148">String</span><span class="sxs-lookup"><span data-stu-id="5c3bf-148">String</span></span>|<span data-ttu-id="5c3bf-149">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5c3bf-149">Admin provided name of the device configuration.</span></span> <span data-ttu-id="5c3bf-150">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="5c3bf-150">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="5c3bf-151">version</span><span class="sxs-lookup"><span data-stu-id="5c3bf-151">version</span></span>|<span data-ttu-id="5c3bf-152">Int32</span><span class="sxs-lookup"><span data-stu-id="5c3bf-152">Int32</span></span>|<span data-ttu-id="5c3bf-153">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5c3bf-153">Version of the device configuration.</span></span> <span data-ttu-id="5c3bf-154">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="5c3bf-154">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="5c3bf-155">passwordRequired</span><span class="sxs-lookup"><span data-stu-id="5c3bf-155">passwordRequired</span></span>|<span data-ttu-id="5c3bf-156">Booleano</span><span class="sxs-lookup"><span data-stu-id="5c3bf-156">Boolean</span></span>|<span data-ttu-id="5c3bf-157">Si quiere requerir o no una contraseña.</span><span class="sxs-lookup"><span data-stu-id="5c3bf-157">Whether or not to require a password.</span></span>|
|<span data-ttu-id="5c3bf-158">passwordBlockSimple</span><span class="sxs-lookup"><span data-stu-id="5c3bf-158">passwordBlockSimple</span></span>|<span data-ttu-id="5c3bf-159">Booleano</span><span class="sxs-lookup"><span data-stu-id="5c3bf-159">Boolean</span></span>|<span data-ttu-id="5c3bf-160">Indica si se van a bloquear las contraseñas simples.</span><span class="sxs-lookup"><span data-stu-id="5c3bf-160">Indicates whether or not to block simple passwords.</span></span>|
|<span data-ttu-id="5c3bf-161">passwordExpirationDays</span><span class="sxs-lookup"><span data-stu-id="5c3bf-161">passwordExpirationDays</span></span>|<span data-ttu-id="5c3bf-162">Int32</span><span class="sxs-lookup"><span data-stu-id="5c3bf-162">Int32</span></span>|<span data-ttu-id="5c3bf-163">Número de días antes de que expire la contraseña.</span><span class="sxs-lookup"><span data-stu-id="5c3bf-163">Number of days before the password expires.</span></span> <span data-ttu-id="5c3bf-164">Valores válidos de 1 a 65535</span><span class="sxs-lookup"><span data-stu-id="5c3bf-164">Valid values 1 to 65535</span></span>|
|<span data-ttu-id="5c3bf-165">passwordMinimumLength</span><span class="sxs-lookup"><span data-stu-id="5c3bf-165">passwordMinimumLength</span></span>|<span data-ttu-id="5c3bf-166">Int32</span><span class="sxs-lookup"><span data-stu-id="5c3bf-166">Int32</span></span>|<span data-ttu-id="5c3bf-167">Longitud mínima de la contraseña.</span><span class="sxs-lookup"><span data-stu-id="5c3bf-167">Minimum length of password.</span></span> <span data-ttu-id="5c3bf-168">Valores válidos de 4 a 14</span><span class="sxs-lookup"><span data-stu-id="5c3bf-168">Valid values 4 to 14</span></span>|
|<span data-ttu-id="5c3bf-169">passwordMinutesOfInactivityBeforeLock</span><span class="sxs-lookup"><span data-stu-id="5c3bf-169">passwordMinutesOfInactivityBeforeLock</span></span>|<span data-ttu-id="5c3bf-170">Int32</span><span class="sxs-lookup"><span data-stu-id="5c3bf-170">Int32</span></span>|<span data-ttu-id="5c3bf-171">Minutos de inactividad antes de que sea necesaria una contraseña.</span><span class="sxs-lookup"><span data-stu-id="5c3bf-171">Minutes of inactivity before a password is required.</span></span>|
|<span data-ttu-id="5c3bf-172">passwordPreviousPasswordBlockCount</span><span class="sxs-lookup"><span data-stu-id="5c3bf-172">passwordPreviousPasswordBlockCount</span></span>|<span data-ttu-id="5c3bf-173">Int32</span><span class="sxs-lookup"><span data-stu-id="5c3bf-173">Int32</span></span>|<span data-ttu-id="5c3bf-174">Número de contraseñas anteriores que bloquear.</span><span class="sxs-lookup"><span data-stu-id="5c3bf-174">Number of previous passwords to block.</span></span> <span data-ttu-id="5c3bf-175">Valores válidos de 1 a 24.</span><span class="sxs-lookup"><span data-stu-id="5c3bf-175">Valid values 1 to 24</span></span>|
|<span data-ttu-id="5c3bf-176">passwordMinimumCharacterSetCount</span><span class="sxs-lookup"><span data-stu-id="5c3bf-176">passwordMinimumCharacterSetCount</span></span>|<span data-ttu-id="5c3bf-177">Int32</span><span class="sxs-lookup"><span data-stu-id="5c3bf-177">Int32</span></span>|<span data-ttu-id="5c3bf-178">Número de juegos de caracteres necesarios en la contraseña.</span><span class="sxs-lookup"><span data-stu-id="5c3bf-178">The number of character sets required in the password.</span></span>|
|<span data-ttu-id="5c3bf-179">passwordRequiredType</span><span class="sxs-lookup"><span data-stu-id="5c3bf-179">passwordRequiredType</span></span>|[<span data-ttu-id="5c3bf-180">requiredPasswordType</span><span class="sxs-lookup"><span data-stu-id="5c3bf-180">requiredPasswordType</span></span>](../resources/intune-deviceconfig-requiredpasswordtype.md)|<span data-ttu-id="5c3bf-181">Tipo de contraseña necesaria.</span><span class="sxs-lookup"><span data-stu-id="5c3bf-181">The required password type.</span></span> <span data-ttu-id="5c3bf-182">Los valores posibles son: `deviceDefault`, `alphanumeric` y `numeric`.</span><span class="sxs-lookup"><span data-stu-id="5c3bf-182">Possible values are: `deviceDefault`, `alphanumeric`, `numeric`.</span></span>|
|<span data-ttu-id="5c3bf-183">osMinimumVersion</span><span class="sxs-lookup"><span data-stu-id="5c3bf-183">osMinimumVersion</span></span>|<span data-ttu-id="5c3bf-184">String</span><span class="sxs-lookup"><span data-stu-id="5c3bf-184">String</span></span>|<span data-ttu-id="5c3bf-185">Versión mínima de iOS.</span><span class="sxs-lookup"><span data-stu-id="5c3bf-185">Minimum IOS version.</span></span>|
|<span data-ttu-id="5c3bf-186">osMaximumVersion</span><span class="sxs-lookup"><span data-stu-id="5c3bf-186">osMaximumVersion</span></span>|<span data-ttu-id="5c3bf-187">String</span><span class="sxs-lookup"><span data-stu-id="5c3bf-187">String</span></span>|<span data-ttu-id="5c3bf-188">Versión máxima de iOS.</span><span class="sxs-lookup"><span data-stu-id="5c3bf-188">Maximum IOS version.</span></span>|
|<span data-ttu-id="5c3bf-189">systemIntegrityProtectionEnabled</span><span class="sxs-lookup"><span data-stu-id="5c3bf-189">systemIntegrityProtectionEnabled</span></span>|<span data-ttu-id="5c3bf-190">Booleano</span><span class="sxs-lookup"><span data-stu-id="5c3bf-190">Boolean</span></span>|<span data-ttu-id="5c3bf-191">Requiere que los dispositivos hayan habilitado la protección de integridad del sistema.</span><span class="sxs-lookup"><span data-stu-id="5c3bf-191">Require that devices have enabled system integrity protection.</span></span>|
|<span data-ttu-id="5c3bf-192">deviceThreatProtectionEnabled</span><span class="sxs-lookup"><span data-stu-id="5c3bf-192">deviceThreatProtectionEnabled</span></span>|<span data-ttu-id="5c3bf-193">Booleano</span><span class="sxs-lookup"><span data-stu-id="5c3bf-193">Boolean</span></span>|<span data-ttu-id="5c3bf-194">Requiere que los dispositivos hayan habilitado la protección contra amenazas de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5c3bf-194">Require that devices have enabled device threat protection .</span></span>|
|<span data-ttu-id="5c3bf-195">deviceThreatProtectionRequiredSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="5c3bf-195">deviceThreatProtectionRequiredSecurityLevel</span></span>|[<span data-ttu-id="5c3bf-196">deviceThreatProtectionLevel</span><span class="sxs-lookup"><span data-stu-id="5c3bf-196">deviceThreatProtectionLevel</span></span>](../resources/intune-deviceconfig-devicethreatprotectionlevel.md)|<span data-ttu-id="5c3bf-197">Exigir que el nivel de riesgo mínimo de Mobile Threat Protection informe del no cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="5c3bf-197">Require Mobile Threat Protection minimum risk level to report noncompliance.</span></span> <span data-ttu-id="5c3bf-198">Los valores posibles son: `unavailable`, `secured`, `low`, `medium`, `high` y `notSet`.</span><span class="sxs-lookup"><span data-stu-id="5c3bf-198">Possible values are: `unavailable`, `secured`, `low`, `medium`, `high`, `notSet`.</span></span>|
|<span data-ttu-id="5c3bf-199">storageRequireEncryption</span><span class="sxs-lookup"><span data-stu-id="5c3bf-199">storageRequireEncryption</span></span>|<span data-ttu-id="5c3bf-200">Booleano</span><span class="sxs-lookup"><span data-stu-id="5c3bf-200">Boolean</span></span>|<span data-ttu-id="5c3bf-201">Exige el cifrado en dispositivos Mac OS.</span><span class="sxs-lookup"><span data-stu-id="5c3bf-201">Require encryption on Mac OS devices.</span></span>|
|<span data-ttu-id="5c3bf-202">firewallEnabled</span><span class="sxs-lookup"><span data-stu-id="5c3bf-202">firewallEnabled</span></span>|<span data-ttu-id="5c3bf-203">Booleano</span><span class="sxs-lookup"><span data-stu-id="5c3bf-203">Boolean</span></span>|<span data-ttu-id="5c3bf-204">Si el firewall se debe habilitar o no.</span><span class="sxs-lookup"><span data-stu-id="5c3bf-204">Whether the firewall should be enabled or not.</span></span>|
|<span data-ttu-id="5c3bf-205">firewallBlockAllIncoming</span><span class="sxs-lookup"><span data-stu-id="5c3bf-205">firewallBlockAllIncoming</span></span>|<span data-ttu-id="5c3bf-206">Booleano</span><span class="sxs-lookup"><span data-stu-id="5c3bf-206">Boolean</span></span>|<span data-ttu-id="5c3bf-207">Corresponde a la opción "Bloquear todas las conexiones entrantes".</span><span class="sxs-lookup"><span data-stu-id="5c3bf-207">Corresponds to the “Block all incoming connections” option.</span></span>|
|<span data-ttu-id="5c3bf-208">firewallEnableStealthMode</span><span class="sxs-lookup"><span data-stu-id="5c3bf-208">firewallEnableStealthMode</span></span>|<span data-ttu-id="5c3bf-209">Booleano</span><span class="sxs-lookup"><span data-stu-id="5c3bf-209">Boolean</span></span>|<span data-ttu-id="5c3bf-210">Corresponde a "Habilitar modo silencioso".</span><span class="sxs-lookup"><span data-stu-id="5c3bf-210">Corresponds to “Enable stealth mode.”</span></span>|



## <a name="response"></a><span data-ttu-id="5c3bf-211">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5c3bf-211">Response</span></span>
<span data-ttu-id="5c3bf-212">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [macOSCompliancePolicy](../resources/intune-deviceconfig-macoscompliancepolicy.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5c3bf-212">If successful, this method returns a `200 OK` response code and an updated [macOSCompliancePolicy](../resources/intune-deviceconfig-macoscompliancepolicy.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="5c3bf-213">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="5c3bf-213">Example</span></span>
### <a name="request"></a><span data-ttu-id="5c3bf-214">Solicitud</span><span class="sxs-lookup"><span data-stu-id="5c3bf-214">Request</span></span>
<span data-ttu-id="5c3bf-215">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="5c3bf-215">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}
Content-type: application/json
Content-length: 849

{
  "@odata.type": "#microsoft.graph.macOSCompliancePolicy",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "passwordRequired": true,
  "passwordBlockSimple": true,
  "passwordExpirationDays": 6,
  "passwordMinimumLength": 5,
  "passwordMinutesOfInactivityBeforeLock": 5,
  "passwordPreviousPasswordBlockCount": 2,
  "passwordMinimumCharacterSetCount": 0,
  "passwordRequiredType": "alphanumeric",
  "osMinimumVersion": "Os Minimum Version value",
  "osMaximumVersion": "Os Maximum Version value",
  "systemIntegrityProtectionEnabled": true,
  "deviceThreatProtectionEnabled": true,
  "deviceThreatProtectionRequiredSecurityLevel": "secured",
  "storageRequireEncryption": true,
  "firewallEnabled": true,
  "firewallBlockAllIncoming": true,
  "firewallEnableStealthMode": true
}
```

### <a name="response"></a><span data-ttu-id="5c3bf-216">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5c3bf-216">Response</span></span>
<span data-ttu-id="5c3bf-p113">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="5c3bf-p113">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1021

{
  "@odata.type": "#microsoft.graph.macOSCompliancePolicy",
  "id": "ddbadff3-dff3-ddba-f3df-baddf3dfbadd",
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "description": "Description value",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "displayName": "Display Name value",
  "version": 7,
  "passwordRequired": true,
  "passwordBlockSimple": true,
  "passwordExpirationDays": 6,
  "passwordMinimumLength": 5,
  "passwordMinutesOfInactivityBeforeLock": 5,
  "passwordPreviousPasswordBlockCount": 2,
  "passwordMinimumCharacterSetCount": 0,
  "passwordRequiredType": "alphanumeric",
  "osMinimumVersion": "Os Minimum Version value",
  "osMaximumVersion": "Os Maximum Version value",
  "systemIntegrityProtectionEnabled": true,
  "deviceThreatProtectionEnabled": true,
  "deviceThreatProtectionRequiredSecurityLevel": "secured",
  "storageRequireEncryption": true,
  "firewallEnabled": true,
  "firewallBlockAllIncoming": true,
  "firewallEnableStealthMode": true
}
```



