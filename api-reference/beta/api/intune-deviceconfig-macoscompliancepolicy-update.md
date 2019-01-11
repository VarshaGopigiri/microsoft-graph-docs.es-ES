---
title: Actualizar macOSCompliancePolicy
description: Actualice las propiedades de un objeto macOSCompliancePolicy.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 93bf199d9024ebadd9a8960d53d9185a3dadd10c
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27852244"
---
# <a name="update-macoscompliancepolicy"></a><span data-ttu-id="47801-103">Actualizar macOSCompliancePolicy</span><span class="sxs-lookup"><span data-stu-id="47801-103">Update macOSCompliancePolicy</span></span>

> <span data-ttu-id="47801-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="47801-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="47801-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="47801-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="47801-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="47801-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="47801-107">Actualice las propiedades de un objeto [macOSCompliancePolicy](../resources/intune-deviceconfig-macoscompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="47801-107">Update the properties of a [macOSCompliancePolicy](../resources/intune-deviceconfig-macoscompliancepolicy.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="47801-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="47801-108">Prerequisites</span></span>
<span data-ttu-id="47801-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="47801-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="47801-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="47801-111">Permission type</span></span>|<span data-ttu-id="47801-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="47801-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="47801-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="47801-113">Delegated (work or school account)</span></span>|<span data-ttu-id="47801-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="47801-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="47801-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="47801-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="47801-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="47801-116">Not supported.</span></span>|
|<span data-ttu-id="47801-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="47801-117">Application</span></span>|<span data-ttu-id="47801-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="47801-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="47801-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="47801-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}
```

## <a name="request-headers"></a><span data-ttu-id="47801-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="47801-120">Request headers</span></span>
|<span data-ttu-id="47801-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="47801-121">Header</span></span>|<span data-ttu-id="47801-122">Valor</span><span class="sxs-lookup"><span data-stu-id="47801-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="47801-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="47801-123">Authorization</span></span>|<span data-ttu-id="47801-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="47801-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="47801-125">Accept</span><span class="sxs-lookup"><span data-stu-id="47801-125">Accept</span></span>|<span data-ttu-id="47801-126">application/json</span><span class="sxs-lookup"><span data-stu-id="47801-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="47801-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="47801-127">Request body</span></span>
<span data-ttu-id="47801-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto [macOSCompliancePolicy](../resources/intune-deviceconfig-macoscompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="47801-128">In the request body, supply a JSON representation for the [macOSCompliancePolicy](../resources/intune-deviceconfig-macoscompliancepolicy.md) object.</span></span>

<span data-ttu-id="47801-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [macOSCompliancePolicy](../resources/intune-deviceconfig-macoscompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="47801-129">The following table shows the properties that are required when you create the [macOSCompliancePolicy](../resources/intune-deviceconfig-macoscompliancepolicy.md).</span></span>

|<span data-ttu-id="47801-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="47801-130">Property</span></span>|<span data-ttu-id="47801-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="47801-131">Type</span></span>|<span data-ttu-id="47801-132">Description</span><span class="sxs-lookup"><span data-stu-id="47801-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="47801-133">roleScopeTagIds</span><span class="sxs-lookup"><span data-stu-id="47801-133">roleScopeTagIds</span></span>|<span data-ttu-id="47801-134">Colección String</span><span class="sxs-lookup"><span data-stu-id="47801-134">String collection</span></span>|<span data-ttu-id="47801-135">Lista de etiquetas de ámbito para esta instancia de entidad.</span><span class="sxs-lookup"><span data-stu-id="47801-135">List of Scope Tags for this Entity instance.</span></span> <span data-ttu-id="47801-136">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="47801-136">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="47801-137">id</span><span class="sxs-lookup"><span data-stu-id="47801-137">id</span></span>|<span data-ttu-id="47801-138">Cadena</span><span class="sxs-lookup"><span data-stu-id="47801-138">String</span></span>|<span data-ttu-id="47801-139">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="47801-139">Key of the entity.</span></span> <span data-ttu-id="47801-140">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="47801-140">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="47801-141">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="47801-141">createdDateTime</span></span>|<span data-ttu-id="47801-142">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="47801-142">DateTimeOffset</span></span>|<span data-ttu-id="47801-143">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="47801-143">DateTime the object was created.</span></span> <span data-ttu-id="47801-144">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="47801-144">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="47801-145">descripción</span><span class="sxs-lookup"><span data-stu-id="47801-145">description</span></span>|<span data-ttu-id="47801-146">Cadena</span><span class="sxs-lookup"><span data-stu-id="47801-146">String</span></span>|<span data-ttu-id="47801-147">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="47801-147">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="47801-148">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="47801-148">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="47801-149">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="47801-149">lastModifiedDateTime</span></span>|<span data-ttu-id="47801-150">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="47801-150">DateTimeOffset</span></span>|<span data-ttu-id="47801-151">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="47801-151">DateTime the object was last modified.</span></span> <span data-ttu-id="47801-152">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="47801-152">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="47801-153">displayName</span><span class="sxs-lookup"><span data-stu-id="47801-153">displayName</span></span>|<span data-ttu-id="47801-154">Cadena</span><span class="sxs-lookup"><span data-stu-id="47801-154">String</span></span>|<span data-ttu-id="47801-155">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="47801-155">Admin provided name of the device configuration.</span></span> <span data-ttu-id="47801-156">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="47801-156">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="47801-157">version</span><span class="sxs-lookup"><span data-stu-id="47801-157">version</span></span>|<span data-ttu-id="47801-158">Int32</span><span class="sxs-lookup"><span data-stu-id="47801-158">Int32</span></span>|<span data-ttu-id="47801-159">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="47801-159">Version of the device configuration.</span></span> <span data-ttu-id="47801-160">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="47801-160">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="47801-161">passwordRequired</span><span class="sxs-lookup"><span data-stu-id="47801-161">passwordRequired</span></span>|<span data-ttu-id="47801-162">Booleano</span><span class="sxs-lookup"><span data-stu-id="47801-162">Boolean</span></span>|<span data-ttu-id="47801-163">Si quiere requerir o no una contraseña.</span><span class="sxs-lookup"><span data-stu-id="47801-163">Whether or not to require a password.</span></span>|
|<span data-ttu-id="47801-164">passwordBlockSimple</span><span class="sxs-lookup"><span data-stu-id="47801-164">passwordBlockSimple</span></span>|<span data-ttu-id="47801-165">Booleano</span><span class="sxs-lookup"><span data-stu-id="47801-165">Boolean</span></span>|<span data-ttu-id="47801-166">Indica si se van a bloquear las contraseñas simples.</span><span class="sxs-lookup"><span data-stu-id="47801-166">Indicates whether or not to block simple passwords.</span></span>|
|<span data-ttu-id="47801-167">passwordExpirationDays</span><span class="sxs-lookup"><span data-stu-id="47801-167">passwordExpirationDays</span></span>|<span data-ttu-id="47801-168">Int32</span><span class="sxs-lookup"><span data-stu-id="47801-168">Int32</span></span>|<span data-ttu-id="47801-169">Número de días antes de que expire la contraseña.</span><span class="sxs-lookup"><span data-stu-id="47801-169">Number of days before the password expires.</span></span> <span data-ttu-id="47801-170">Valores válidos de 1 a 65535</span><span class="sxs-lookup"><span data-stu-id="47801-170">Valid values 1 to 65535</span></span>|
|<span data-ttu-id="47801-171">passwordMinimumLength</span><span class="sxs-lookup"><span data-stu-id="47801-171">passwordMinimumLength</span></span>|<span data-ttu-id="47801-172">Int32</span><span class="sxs-lookup"><span data-stu-id="47801-172">Int32</span></span>|<span data-ttu-id="47801-173">Longitud mínima de la contraseña.</span><span class="sxs-lookup"><span data-stu-id="47801-173">Minimum length of password.</span></span> <span data-ttu-id="47801-174">Valores válidos de 4 a 14</span><span class="sxs-lookup"><span data-stu-id="47801-174">Valid values 4 to 14</span></span>|
|<span data-ttu-id="47801-175">passwordMinutesOfInactivityBeforeLock</span><span class="sxs-lookup"><span data-stu-id="47801-175">passwordMinutesOfInactivityBeforeLock</span></span>|<span data-ttu-id="47801-176">Int32</span><span class="sxs-lookup"><span data-stu-id="47801-176">Int32</span></span>|<span data-ttu-id="47801-177">Minutos de inactividad antes de que sea necesaria una contraseña.</span><span class="sxs-lookup"><span data-stu-id="47801-177">Minutes of inactivity before a password is required.</span></span>|
|<span data-ttu-id="47801-178">passwordPreviousPasswordBlockCount</span><span class="sxs-lookup"><span data-stu-id="47801-178">passwordPreviousPasswordBlockCount</span></span>|<span data-ttu-id="47801-179">Int32</span><span class="sxs-lookup"><span data-stu-id="47801-179">Int32</span></span>|<span data-ttu-id="47801-180">Número de contraseñas anteriores que bloquear.</span><span class="sxs-lookup"><span data-stu-id="47801-180">Number of previous passwords to block.</span></span> <span data-ttu-id="47801-181">Valores válidos de 1 a 24.</span><span class="sxs-lookup"><span data-stu-id="47801-181">Valid values 1 to 24</span></span>|
|<span data-ttu-id="47801-182">passwordMinimumCharacterSetCount</span><span class="sxs-lookup"><span data-stu-id="47801-182">passwordMinimumCharacterSetCount</span></span>|<span data-ttu-id="47801-183">Int32</span><span class="sxs-lookup"><span data-stu-id="47801-183">Int32</span></span>|<span data-ttu-id="47801-184">Número de juegos de caracteres necesarios en la contraseña.</span><span class="sxs-lookup"><span data-stu-id="47801-184">The number of character sets required in the password.</span></span>|
|<span data-ttu-id="47801-185">passwordRequiredType</span><span class="sxs-lookup"><span data-stu-id="47801-185">passwordRequiredType</span></span>|[<span data-ttu-id="47801-186">requiredPasswordType</span><span class="sxs-lookup"><span data-stu-id="47801-186">requiredPasswordType</span></span>](../resources/intune-deviceconfig-requiredpasswordtype.md)|<span data-ttu-id="47801-187">Tipo de contraseña necesaria.</span><span class="sxs-lookup"><span data-stu-id="47801-187">The required password type.</span></span> <span data-ttu-id="47801-188">Los valores posibles son: `deviceDefault`, `alphanumeric` y `numeric`.</span><span class="sxs-lookup"><span data-stu-id="47801-188">Possible values are: `deviceDefault`, `alphanumeric`, `numeric`.</span></span>|
|<span data-ttu-id="47801-189">osMinimumVersion</span><span class="sxs-lookup"><span data-stu-id="47801-189">osMinimumVersion</span></span>|<span data-ttu-id="47801-190">Cadena</span><span class="sxs-lookup"><span data-stu-id="47801-190">String</span></span>|<span data-ttu-id="47801-191">Versión mínima de iOS.</span><span class="sxs-lookup"><span data-stu-id="47801-191">Minimum IOS version.</span></span>|
|<span data-ttu-id="47801-192">osMaximumVersion</span><span class="sxs-lookup"><span data-stu-id="47801-192">osMaximumVersion</span></span>|<span data-ttu-id="47801-193">Cadena</span><span class="sxs-lookup"><span data-stu-id="47801-193">String</span></span>|<span data-ttu-id="47801-194">Versión máxima de iOS.</span><span class="sxs-lookup"><span data-stu-id="47801-194">Maximum IOS version.</span></span>|
|<span data-ttu-id="47801-195">systemIntegrityProtectionEnabled</span><span class="sxs-lookup"><span data-stu-id="47801-195">systemIntegrityProtectionEnabled</span></span>|<span data-ttu-id="47801-196">Booleano</span><span class="sxs-lookup"><span data-stu-id="47801-196">Boolean</span></span>|<span data-ttu-id="47801-197">Requiere que los dispositivos hayan habilitado la protección de integridad del sistema.</span><span class="sxs-lookup"><span data-stu-id="47801-197">Require that devices have enabled system integrity protection.</span></span>|
|<span data-ttu-id="47801-198">deviceThreatProtectionEnabled</span><span class="sxs-lookup"><span data-stu-id="47801-198">deviceThreatProtectionEnabled</span></span>|<span data-ttu-id="47801-199">Booleano</span><span class="sxs-lookup"><span data-stu-id="47801-199">Boolean</span></span>|<span data-ttu-id="47801-200">Requiere que los dispositivos hayan habilitado la protección contra amenazas de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="47801-200">Require that devices have enabled device threat protection .</span></span>|
|<span data-ttu-id="47801-201">deviceThreatProtectionRequiredSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="47801-201">deviceThreatProtectionRequiredSecurityLevel</span></span>|[<span data-ttu-id="47801-202">deviceThreatProtectionLevel</span><span class="sxs-lookup"><span data-stu-id="47801-202">deviceThreatProtectionLevel</span></span>](../resources/intune-deviceconfig-devicethreatprotectionlevel.md)|<span data-ttu-id="47801-203">Exigir que el nivel de riesgo mínimo de Mobile Threat Protection informe del no cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="47801-203">Require Mobile Threat Protection minimum risk level to report noncompliance.</span></span> <span data-ttu-id="47801-204">Los valores posibles son: `unavailable`, `secured`, `low`, `medium`, `high` y `notSet`.</span><span class="sxs-lookup"><span data-stu-id="47801-204">Possible values are: `unavailable`, `secured`, `low`, `medium`, `high`, `notSet`.</span></span>|
|<span data-ttu-id="47801-205">storageRequireEncryption</span><span class="sxs-lookup"><span data-stu-id="47801-205">storageRequireEncryption</span></span>|<span data-ttu-id="47801-206">Booleano</span><span class="sxs-lookup"><span data-stu-id="47801-206">Boolean</span></span>|<span data-ttu-id="47801-207">Exige el cifrado en dispositivos Mac OS.</span><span class="sxs-lookup"><span data-stu-id="47801-207">Require encryption on Mac OS devices.</span></span>|
|<span data-ttu-id="47801-208">gatekeeperAllowedAppSource</span><span class="sxs-lookup"><span data-stu-id="47801-208">gatekeeperAllowedAppSource</span></span>|[<span data-ttu-id="47801-209">macOSGatekeeperAppSources</span><span class="sxs-lookup"><span data-stu-id="47801-209">macOSGatekeeperAppSources</span></span>](../resources/intune-deviceconfig-macosgatekeeperappsources.md)|<span data-ttu-id="47801-210">Del sistema y la configuración de privacidad que determina qué aplicaciones de ubicaciones de descarga se pueden ejecutar desde un dispositivo de Mac OS.</span><span class="sxs-lookup"><span data-stu-id="47801-210">System and Privacy setting that determines which download locations apps can be run from on a macOS device.</span></span> <span data-ttu-id="47801-211">Los valores posibles son: `notConfigured`, `macAppStore`, `macAppStoreAndIdentifiedDevelopers` y `anywhere`.</span><span class="sxs-lookup"><span data-stu-id="47801-211">Possible values are: `notConfigured`, `macAppStore`, `macAppStoreAndIdentifiedDevelopers`, `anywhere`.</span></span>|
|<span data-ttu-id="47801-212">firewallEnabled</span><span class="sxs-lookup"><span data-stu-id="47801-212">firewallEnabled</span></span>|<span data-ttu-id="47801-213">Booleano</span><span class="sxs-lookup"><span data-stu-id="47801-213">Boolean</span></span>|<span data-ttu-id="47801-214">Si el firewall se debe habilitar o no.</span><span class="sxs-lookup"><span data-stu-id="47801-214">Whether the firewall should be enabled or not.</span></span>|
|<span data-ttu-id="47801-215">firewallBlockAllIncoming</span><span class="sxs-lookup"><span data-stu-id="47801-215">firewallBlockAllIncoming</span></span>|<span data-ttu-id="47801-216">Booleano</span><span class="sxs-lookup"><span data-stu-id="47801-216">Boolean</span></span>|<span data-ttu-id="47801-217">Corresponde a la opción "Bloquear todas las conexiones entrantes".</span><span class="sxs-lookup"><span data-stu-id="47801-217">Corresponds to the “Block all incoming connections” option.</span></span>|
|<span data-ttu-id="47801-218">firewallEnableStealthMode</span><span class="sxs-lookup"><span data-stu-id="47801-218">firewallEnableStealthMode</span></span>|<span data-ttu-id="47801-219">Booleano</span><span class="sxs-lookup"><span data-stu-id="47801-219">Boolean</span></span>|<span data-ttu-id="47801-220">Corresponde a "Habilitar modo silencioso".</span><span class="sxs-lookup"><span data-stu-id="47801-220">Corresponds to “Enable stealth mode.”</span></span>|



## <a name="response"></a><span data-ttu-id="47801-221">Respuesta</span><span class="sxs-lookup"><span data-stu-id="47801-221">Response</span></span>
<span data-ttu-id="47801-222">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [macOSCompliancePolicy](../resources/intune-deviceconfig-macoscompliancepolicy.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="47801-222">If successful, this method returns a `200 OK` response code and an updated [macOSCompliancePolicy](../resources/intune-deviceconfig-macoscompliancepolicy.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="47801-223">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="47801-223">Example</span></span>
### <a name="request"></a><span data-ttu-id="47801-224">Solicitud</span><span class="sxs-lookup"><span data-stu-id="47801-224">Request</span></span>
<span data-ttu-id="47801-225">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="47801-225">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}
Content-type: application/json
Content-length: 963

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
  "gatekeeperAllowedAppSource": "macAppStore",
  "firewallEnabled": true,
  "firewallBlockAllIncoming": true,
  "firewallEnableStealthMode": true
}
```

### <a name="response"></a><span data-ttu-id="47801-226">Respuesta</span><span class="sxs-lookup"><span data-stu-id="47801-226">Response</span></span>
<span data-ttu-id="47801-p116">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="47801-p116">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1131

{
  "@odata.type": "#microsoft.graph.macOSCompliancePolicy",
  "roleScopeTagIds": [
    "Role Scope Tag Ids value"
  ],
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
  "gatekeeperAllowedAppSource": "macAppStore",
  "firewallEnabled": true,
  "firewallBlockAllIncoming": true,
  "firewallEnableStealthMode": true
}
```





