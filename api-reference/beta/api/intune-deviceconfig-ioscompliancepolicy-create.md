---
title: Crear iosCompliancePolicy
description: Crear un objeto iosCompliancePolicy.
ms.openlocfilehash: 7dc80454e1b801ef22d02bd9955de681baaf3e9e
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084248"
---
# <a name="create-ioscompliancepolicy"></a><span data-ttu-id="bdd7c-103">Crear iosCompliancePolicy</span><span class="sxs-lookup"><span data-stu-id="bdd7c-103">Create iosCompliancePolicy</span></span>

> <span data-ttu-id="bdd7c-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="bdd7c-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="bdd7c-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="bdd7c-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="bdd7c-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="bdd7c-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="bdd7c-107">Crear un objeto [iosCompliancePolicy](../resources/intune-deviceconfig-ioscompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="bdd7c-107">Create a new [iosCompliancePolicy](../resources/intune-deviceconfig-ioscompliancepolicy.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="bdd7c-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="bdd7c-108">Prerequisites</span></span>
<span data-ttu-id="bdd7c-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="bdd7c-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="bdd7c-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="bdd7c-111">Permission type</span></span>|<span data-ttu-id="bdd7c-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="bdd7c-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="bdd7c-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="bdd7c-113">Delegated (work or school account)</span></span>|<span data-ttu-id="bdd7c-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="bdd7c-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="bdd7c-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="bdd7c-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="bdd7c-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="bdd7c-116">Not supported.</span></span>|
|<span data-ttu-id="bdd7c-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="bdd7c-117">Application</span></span>|<span data-ttu-id="bdd7c-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="bdd7c-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="bdd7c-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="bdd7c-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceCompliancePolicies
```

## <a name="request-headers"></a><span data-ttu-id="bdd7c-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="bdd7c-120">Request headers</span></span>
|<span data-ttu-id="bdd7c-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bdd7c-121">Header</span></span>|<span data-ttu-id="bdd7c-122">Valor</span><span class="sxs-lookup"><span data-stu-id="bdd7c-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="bdd7c-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="bdd7c-123">Authorization</span></span>|<span data-ttu-id="bdd7c-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="bdd7c-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="bdd7c-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="bdd7c-125">Accept</span></span>|<span data-ttu-id="bdd7c-126">application/json</span><span class="sxs-lookup"><span data-stu-id="bdd7c-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="bdd7c-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="bdd7c-127">Request body</span></span>
<span data-ttu-id="bdd7c-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto iosCompliancePolicy.</span><span class="sxs-lookup"><span data-stu-id="bdd7c-128">In the request body, supply a JSON representation for the iosCompliancePolicy object.</span></span>

<span data-ttu-id="bdd7c-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto iosCompliancePolicy.</span><span class="sxs-lookup"><span data-stu-id="bdd7c-129">The following table shows the properties that are required when you create the iosCompliancePolicy.</span></span>

|<span data-ttu-id="bdd7c-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="bdd7c-130">Property</span></span>|<span data-ttu-id="bdd7c-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="bdd7c-131">Type</span></span>|<span data-ttu-id="bdd7c-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="bdd7c-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="bdd7c-133">roleScopeTagIds</span><span class="sxs-lookup"><span data-stu-id="bdd7c-133">roleScopeTagIds</span></span>|<span data-ttu-id="bdd7c-134">Colección String</span><span class="sxs-lookup"><span data-stu-id="bdd7c-134">String collection</span></span>|<span data-ttu-id="bdd7c-135">Lista de etiquetas de ámbito para esta instancia de entidad.</span><span class="sxs-lookup"><span data-stu-id="bdd7c-135">List of Scope Tags for this Entity instance.</span></span> <span data-ttu-id="bdd7c-136">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="bdd7c-136">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="bdd7c-137">id</span><span class="sxs-lookup"><span data-stu-id="bdd7c-137">id</span></span>|<span data-ttu-id="bdd7c-138">String</span><span class="sxs-lookup"><span data-stu-id="bdd7c-138">String</span></span>|<span data-ttu-id="bdd7c-139">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="bdd7c-139">Key of the entity.</span></span> <span data-ttu-id="bdd7c-140">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="bdd7c-140">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="bdd7c-141">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="bdd7c-141">createdDateTime</span></span>|<span data-ttu-id="bdd7c-142">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="bdd7c-142">DateTimeOffset</span></span>|<span data-ttu-id="bdd7c-143">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="bdd7c-143">DateTime the object was created.</span></span> <span data-ttu-id="bdd7c-144">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="bdd7c-144">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="bdd7c-145">descripción</span><span class="sxs-lookup"><span data-stu-id="bdd7c-145">description</span></span>|<span data-ttu-id="bdd7c-146">String</span><span class="sxs-lookup"><span data-stu-id="bdd7c-146">String</span></span>|<span data-ttu-id="bdd7c-147">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bdd7c-147">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="bdd7c-148">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="bdd7c-148">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="bdd7c-149">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="bdd7c-149">lastModifiedDateTime</span></span>|<span data-ttu-id="bdd7c-150">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="bdd7c-150">DateTimeOffset</span></span>|<span data-ttu-id="bdd7c-151">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="bdd7c-151">DateTime the object was last modified.</span></span> <span data-ttu-id="bdd7c-152">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="bdd7c-152">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="bdd7c-153">displayName</span><span class="sxs-lookup"><span data-stu-id="bdd7c-153">displayName</span></span>|<span data-ttu-id="bdd7c-154">String</span><span class="sxs-lookup"><span data-stu-id="bdd7c-154">String</span></span>|<span data-ttu-id="bdd7c-155">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bdd7c-155">Admin provided name of the device configuration.</span></span> <span data-ttu-id="bdd7c-156">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="bdd7c-156">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="bdd7c-157">version</span><span class="sxs-lookup"><span data-stu-id="bdd7c-157">version</span></span>|<span data-ttu-id="bdd7c-158">Int32</span><span class="sxs-lookup"><span data-stu-id="bdd7c-158">Int32</span></span>|<span data-ttu-id="bdd7c-159">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bdd7c-159">Version of the device configuration.</span></span> <span data-ttu-id="bdd7c-160">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="bdd7c-160">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="bdd7c-161">passcodeBlockSimple</span><span class="sxs-lookup"><span data-stu-id="bdd7c-161">passcodeBlockSimple</span></span>|<span data-ttu-id="bdd7c-162">Booleano</span><span class="sxs-lookup"><span data-stu-id="bdd7c-162">Boolean</span></span>|<span data-ttu-id="bdd7c-163">Indica si se van a bloquear los códigos de acceso simples.</span><span class="sxs-lookup"><span data-stu-id="bdd7c-163">Indicates whether or not to block simple passcodes.</span></span>|
|<span data-ttu-id="bdd7c-164">passcodeExpirationDays</span><span class="sxs-lookup"><span data-stu-id="bdd7c-164">passcodeExpirationDays</span></span>|<span data-ttu-id="bdd7c-165">Int32</span><span class="sxs-lookup"><span data-stu-id="bdd7c-165">Int32</span></span>|<span data-ttu-id="bdd7c-166">Número de días antes de que expire el código de acceso.</span><span class="sxs-lookup"><span data-stu-id="bdd7c-166">Number of days before the passcode expires.</span></span> <span data-ttu-id="bdd7c-167">Valores válidos de 1 a 65535</span><span class="sxs-lookup"><span data-stu-id="bdd7c-167">Valid values 1 to 65535</span></span>|
|<span data-ttu-id="bdd7c-168">passcodeMinimumLength</span><span class="sxs-lookup"><span data-stu-id="bdd7c-168">passcodeMinimumLength</span></span>|<span data-ttu-id="bdd7c-169">Int32</span><span class="sxs-lookup"><span data-stu-id="bdd7c-169">Int32</span></span>|<span data-ttu-id="bdd7c-170">Longitud mínima de los códigos de acceso.</span><span class="sxs-lookup"><span data-stu-id="bdd7c-170">Minimum length of passcode.</span></span> <span data-ttu-id="bdd7c-171">Valores válidos de 4 a 14</span><span class="sxs-lookup"><span data-stu-id="bdd7c-171">Valid values 4 to 14</span></span>|
|<span data-ttu-id="bdd7c-172">passcodeMinutesOfInactivityBeforeLock</span><span class="sxs-lookup"><span data-stu-id="bdd7c-172">passcodeMinutesOfInactivityBeforeLock</span></span>|<span data-ttu-id="bdd7c-173">Int32</span><span class="sxs-lookup"><span data-stu-id="bdd7c-173">Int32</span></span>|<span data-ttu-id="bdd7c-174">Minutos de inactividad antes de que sea necesario un código de acceso.</span><span class="sxs-lookup"><span data-stu-id="bdd7c-174">Minutes of inactivity before a passcode is required.</span></span>|
|<span data-ttu-id="bdd7c-175">passcodeMinutesOfInactivityBeforeScreenTimeout</span><span class="sxs-lookup"><span data-stu-id="bdd7c-175">passcodeMinutesOfInactivityBeforeScreenTimeout</span></span>|<span data-ttu-id="bdd7c-176">Int32</span><span class="sxs-lookup"><span data-stu-id="bdd7c-176">Int32</span></span>|<span data-ttu-id="bdd7c-177">Minutos de inactividad antes de que se agote el tiempo de espera de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="bdd7c-177">Minutes of inactivity before the screen times out.</span></span>|
|<span data-ttu-id="bdd7c-178">passcodePreviousPasscodeBlockCount</span><span class="sxs-lookup"><span data-stu-id="bdd7c-178">passcodePreviousPasscodeBlockCount</span></span>|<span data-ttu-id="bdd7c-179">Int32</span><span class="sxs-lookup"><span data-stu-id="bdd7c-179">Int32</span></span>|<span data-ttu-id="bdd7c-180">Número de códigos de acceso anteriores que bloquear.</span><span class="sxs-lookup"><span data-stu-id="bdd7c-180">Number of previous passcodes to block.</span></span> <span data-ttu-id="bdd7c-181">Valores válidos de 1 a 24.</span><span class="sxs-lookup"><span data-stu-id="bdd7c-181">Valid values 1 to 24</span></span>|
|<span data-ttu-id="bdd7c-182">passcodeMinimumCharacterSetCount</span><span class="sxs-lookup"><span data-stu-id="bdd7c-182">passcodeMinimumCharacterSetCount</span></span>|<span data-ttu-id="bdd7c-183">Int32</span><span class="sxs-lookup"><span data-stu-id="bdd7c-183">Int32</span></span>|<span data-ttu-id="bdd7c-184">Número de juegos de caracteres necesarios en la contraseña.</span><span class="sxs-lookup"><span data-stu-id="bdd7c-184">The number of character sets required in the password.</span></span>|
|<span data-ttu-id="bdd7c-185">passcodeRequiredType</span><span class="sxs-lookup"><span data-stu-id="bdd7c-185">passcodeRequiredType</span></span>|[<span data-ttu-id="bdd7c-186">requiredPasswordType</span><span class="sxs-lookup"><span data-stu-id="bdd7c-186">requiredPasswordType</span></span>](../resources/intune-deviceconfig-requiredpasswordtype.md)|<span data-ttu-id="bdd7c-187">Tipo de código de acceso necesario.</span><span class="sxs-lookup"><span data-stu-id="bdd7c-187">The required passcode type.</span></span> <span data-ttu-id="bdd7c-188">Los valores posibles son: `deviceDefault`, `alphanumeric` y `numeric`.</span><span class="sxs-lookup"><span data-stu-id="bdd7c-188">Possible values are: `deviceDefault`, `alphanumeric`, `numeric`.</span></span>|
|<span data-ttu-id="bdd7c-189">passcodeRequired</span><span class="sxs-lookup"><span data-stu-id="bdd7c-189">passcodeRequired</span></span>|<span data-ttu-id="bdd7c-190">Booleano</span><span class="sxs-lookup"><span data-stu-id="bdd7c-190">Boolean</span></span>|<span data-ttu-id="bdd7c-191">Indica si se va a requerir un código de acceso.</span><span class="sxs-lookup"><span data-stu-id="bdd7c-191">Indicates whether or not to require a passcode.</span></span>|
|<span data-ttu-id="bdd7c-192">osMinimumVersion</span><span class="sxs-lookup"><span data-stu-id="bdd7c-192">osMinimumVersion</span></span>|<span data-ttu-id="bdd7c-193">String</span><span class="sxs-lookup"><span data-stu-id="bdd7c-193">String</span></span>|<span data-ttu-id="bdd7c-194">Versión mínima de iOS.</span><span class="sxs-lookup"><span data-stu-id="bdd7c-194">Minimum IOS version.</span></span>|
|<span data-ttu-id="bdd7c-195">osMaximumVersion</span><span class="sxs-lookup"><span data-stu-id="bdd7c-195">osMaximumVersion</span></span>|<span data-ttu-id="bdd7c-196">String</span><span class="sxs-lookup"><span data-stu-id="bdd7c-196">String</span></span>|<span data-ttu-id="bdd7c-197">Versión máxima de iOS.</span><span class="sxs-lookup"><span data-stu-id="bdd7c-197">Maximum IOS version.</span></span>|
|<span data-ttu-id="bdd7c-198">securityBlockJailbrokenDevices</span><span class="sxs-lookup"><span data-stu-id="bdd7c-198">securityBlockJailbrokenDevices</span></span>|<span data-ttu-id="bdd7c-199">Booleano</span><span class="sxs-lookup"><span data-stu-id="bdd7c-199">Boolean</span></span>|<span data-ttu-id="bdd7c-200">No pueden usarse dispositivos con jailbreak o rooting.</span><span class="sxs-lookup"><span data-stu-id="bdd7c-200">Devices must not be jailbroken or rooted.</span></span>|
|<span data-ttu-id="bdd7c-201">deviceThreatProtectionEnabled</span><span class="sxs-lookup"><span data-stu-id="bdd7c-201">deviceThreatProtectionEnabled</span></span>|<span data-ttu-id="bdd7c-202">Booleano</span><span class="sxs-lookup"><span data-stu-id="bdd7c-202">Boolean</span></span>|<span data-ttu-id="bdd7c-203">Requiere que los dispositivos hayan habilitado la protección contra amenazas de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bdd7c-203">Require that devices have enabled device threat protection .</span></span>|
|<span data-ttu-id="bdd7c-204">deviceThreatProtectionRequiredSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="bdd7c-204">deviceThreatProtectionRequiredSecurityLevel</span></span>|[<span data-ttu-id="bdd7c-205">deviceThreatProtectionLevel</span><span class="sxs-lookup"><span data-stu-id="bdd7c-205">deviceThreatProtectionLevel</span></span>](../resources/intune-deviceconfig-devicethreatprotectionlevel.md)|<span data-ttu-id="bdd7c-206">Exigir que el nivel de riesgo mínimo de Mobile Threat Protection informe del no cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="bdd7c-206">Require Mobile Threat Protection minimum risk level to report noncompliance.</span></span> <span data-ttu-id="bdd7c-207">Los valores posibles son: `unavailable`, `secured`, `low`, `medium`, `high` y `notSet`.</span><span class="sxs-lookup"><span data-stu-id="bdd7c-207">Possible values are: `unavailable`, `secured`, `low`, `medium`, `high`, `notSet`.</span></span>|
|<span data-ttu-id="bdd7c-208">managedEmailProfileRequired</span><span class="sxs-lookup"><span data-stu-id="bdd7c-208">managedEmailProfileRequired</span></span>|<span data-ttu-id="bdd7c-209">Booleano</span><span class="sxs-lookup"><span data-stu-id="bdd7c-209">Boolean</span></span>|<span data-ttu-id="bdd7c-210">Indica si se va a requerir un perfil de correo electrónico administrado.</span><span class="sxs-lookup"><span data-stu-id="bdd7c-210">Indicates whether or not to require a managed email profile.</span></span>|
|<span data-ttu-id="bdd7c-211">restrictedApps</span><span class="sxs-lookup"><span data-stu-id="bdd7c-211">restrictedApps</span></span>|<span data-ttu-id="bdd7c-212">Colección [appListItem](../resources/intune-deviceconfig-applistitem.md)</span><span class="sxs-lookup"><span data-stu-id="bdd7c-212">[appListItem](../resources/intune-deviceconfig-applistitem.md) collection</span></span>|<span data-ttu-id="bdd7c-213">Requiere que el dispositivo no contar con las aplicaciones especificadas instaladas.</span><span class="sxs-lookup"><span data-stu-id="bdd7c-213">Require the device to not have the specified apps installed.</span></span> <span data-ttu-id="bdd7c-214">Esta colección puede contener un máximo de 10 000 elementos.</span><span class="sxs-lookup"><span data-stu-id="bdd7c-214">This collection can contain a maximum of 10000 elements.</span></span>|



## <a name="response"></a><span data-ttu-id="bdd7c-215">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bdd7c-215">Response</span></span>
<span data-ttu-id="bdd7c-216">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [iosCompliancePolicy](../resources/intune-deviceconfig-ioscompliancepolicy.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="bdd7c-216">If successful, this method returns a `201 Created` response code and a [iosCompliancePolicy](../resources/intune-deviceconfig-ioscompliancepolicy.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="bdd7c-217">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="bdd7c-217">Example</span></span>
### <a name="request"></a><span data-ttu-id="bdd7c-218">Solicitud</span><span class="sxs-lookup"><span data-stu-id="bdd7c-218">Request</span></span>
<span data-ttu-id="bdd7c-219">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="bdd7c-219">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/deviceCompliancePolicies
Content-type: application/json
Content-length: 1181

{
  "@odata.type": "#microsoft.graph.iosCompliancePolicy",
  "roleScopeTagIds": [
    "Role Scope Tag Ids value"
  ],
  "description": "Description value",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "displayName": "Display Name value",
  "version": 7,
  "passcodeBlockSimple": true,
  "passcodeExpirationDays": 6,
  "passcodeMinimumLength": 5,
  "passcodeMinutesOfInactivityBeforeLock": 5,
  "passcodeMinutesOfInactivityBeforeScreenTimeout": 14,
  "passcodePreviousPasscodeBlockCount": 2,
  "passcodeMinimumCharacterSetCount": 0,
  "passcodeRequiredType": "alphanumeric",
  "passcodeRequired": true,
  "osMinimumVersion": "Os Minimum Version value",
  "osMaximumVersion": "Os Maximum Version value",
  "securityBlockJailbrokenDevices": true,
  "deviceThreatProtectionEnabled": true,
  "deviceThreatProtectionRequiredSecurityLevel": "secured",
  "managedEmailProfileRequired": true,
  "restrictedApps": [
    {
      "@odata.type": "microsoft.graph.appListItem",
      "name": "Name value",
      "publisher": "Publisher value",
      "appStoreUrl": "https://example.com/appStoreUrl/",
      "appId": "App Id value"
    }
  ]
}
```

### <a name="response"></a><span data-ttu-id="bdd7c-220">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bdd7c-220">Response</span></span>
<span data-ttu-id="bdd7c-p116">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="bdd7c-p116">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 1289

{
  "@odata.type": "#microsoft.graph.iosCompliancePolicy",
  "roleScopeTagIds": [
    "Role Scope Tag Ids value"
  ],
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
  "passcodeMinutesOfInactivityBeforeScreenTimeout": 14,
  "passcodePreviousPasscodeBlockCount": 2,
  "passcodeMinimumCharacterSetCount": 0,
  "passcodeRequiredType": "alphanumeric",
  "passcodeRequired": true,
  "osMinimumVersion": "Os Minimum Version value",
  "osMaximumVersion": "Os Maximum Version value",
  "securityBlockJailbrokenDevices": true,
  "deviceThreatProtectionEnabled": true,
  "deviceThreatProtectionRequiredSecurityLevel": "secured",
  "managedEmailProfileRequired": true,
  "restrictedApps": [
    {
      "@odata.type": "microsoft.graph.appListItem",
      "name": "Name value",
      "publisher": "Publisher value",
      "appStoreUrl": "https://example.com/appStoreUrl/",
      "appId": "App Id value"
    }
  ]
}
```





