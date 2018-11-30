---
title: Actualizar windowsPhone81CompliancePolicy
description: Actualice las propiedades de un objeto windowsPhone81CompliancePolicy.
ms.openlocfilehash: aa737e0c1ab528e0ff67848e687ba5ec6c427c6e
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088789"
---
# <a name="update-windowsphone81compliancepolicy"></a><span data-ttu-id="96d02-103">Actualizar windowsPhone81CompliancePolicy</span><span class="sxs-lookup"><span data-stu-id="96d02-103">Update windowsPhone81CompliancePolicy</span></span>

> <span data-ttu-id="96d02-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="96d02-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="96d02-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="96d02-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="96d02-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="96d02-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="96d02-107">Actualice las propiedades de un objeto [windowsPhone81CompliancePolicy](../resources/intune-deviceconfig-windowsphone81compliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="96d02-107">Update the properties of a [windowsPhone81CompliancePolicy](../resources/intune-deviceconfig-windowsphone81compliancepolicy.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="96d02-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="96d02-108">Prerequisites</span></span>
<span data-ttu-id="96d02-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="96d02-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="96d02-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="96d02-111">Permission type</span></span>|<span data-ttu-id="96d02-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="96d02-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="96d02-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="96d02-113">Delegated (work or school account)</span></span>|<span data-ttu-id="96d02-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="96d02-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="96d02-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="96d02-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="96d02-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="96d02-116">Not supported.</span></span>|
|<span data-ttu-id="96d02-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="96d02-117">Application</span></span>|<span data-ttu-id="96d02-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="96d02-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="96d02-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="96d02-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}
```

## <a name="request-headers"></a><span data-ttu-id="96d02-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="96d02-120">Request headers</span></span>
|<span data-ttu-id="96d02-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="96d02-121">Header</span></span>|<span data-ttu-id="96d02-122">Valor</span><span class="sxs-lookup"><span data-stu-id="96d02-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="96d02-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="96d02-123">Authorization</span></span>|<span data-ttu-id="96d02-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="96d02-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="96d02-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="96d02-125">Accept</span></span>|<span data-ttu-id="96d02-126">application/json</span><span class="sxs-lookup"><span data-stu-id="96d02-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="96d02-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="96d02-127">Request body</span></span>
<span data-ttu-id="96d02-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto [windowsPhone81CompliancePolicy](../resources/intune-deviceconfig-windowsphone81compliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="96d02-128">In the request body, supply a JSON representation for the [windowsPhone81CompliancePolicy](../resources/intune-deviceconfig-windowsphone81compliancepolicy.md) object.</span></span>

<span data-ttu-id="96d02-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [windowsPhone81CompliancePolicy](../resources/intune-deviceconfig-windowsphone81compliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="96d02-129">The following table shows the properties that are required when you create the [windowsPhone81CompliancePolicy](../resources/intune-deviceconfig-windowsphone81compliancepolicy.md).</span></span>

|<span data-ttu-id="96d02-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="96d02-130">Property</span></span>|<span data-ttu-id="96d02-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="96d02-131">Type</span></span>|<span data-ttu-id="96d02-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="96d02-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="96d02-133">roleScopeTagIds</span><span class="sxs-lookup"><span data-stu-id="96d02-133">roleScopeTagIds</span></span>|<span data-ttu-id="96d02-134">Colección String</span><span class="sxs-lookup"><span data-stu-id="96d02-134">String collection</span></span>|<span data-ttu-id="96d02-135">Lista de etiquetas de ámbito para esta instancia de entidad.</span><span class="sxs-lookup"><span data-stu-id="96d02-135">List of Scope Tags for this Entity instance.</span></span> <span data-ttu-id="96d02-136">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="96d02-136">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="96d02-137">id</span><span class="sxs-lookup"><span data-stu-id="96d02-137">id</span></span>|<span data-ttu-id="96d02-138">String</span><span class="sxs-lookup"><span data-stu-id="96d02-138">String</span></span>|<span data-ttu-id="96d02-139">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="96d02-139">Key of the entity.</span></span> <span data-ttu-id="96d02-140">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="96d02-140">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="96d02-141">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="96d02-141">createdDateTime</span></span>|<span data-ttu-id="96d02-142">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="96d02-142">DateTimeOffset</span></span>|<span data-ttu-id="96d02-143">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="96d02-143">DateTime the object was created.</span></span> <span data-ttu-id="96d02-144">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="96d02-144">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="96d02-145">descripción</span><span class="sxs-lookup"><span data-stu-id="96d02-145">description</span></span>|<span data-ttu-id="96d02-146">String</span><span class="sxs-lookup"><span data-stu-id="96d02-146">String</span></span>|<span data-ttu-id="96d02-147">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="96d02-147">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="96d02-148">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="96d02-148">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="96d02-149">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="96d02-149">lastModifiedDateTime</span></span>|<span data-ttu-id="96d02-150">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="96d02-150">DateTimeOffset</span></span>|<span data-ttu-id="96d02-151">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="96d02-151">DateTime the object was last modified.</span></span> <span data-ttu-id="96d02-152">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="96d02-152">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="96d02-153">displayName</span><span class="sxs-lookup"><span data-stu-id="96d02-153">displayName</span></span>|<span data-ttu-id="96d02-154">String</span><span class="sxs-lookup"><span data-stu-id="96d02-154">String</span></span>|<span data-ttu-id="96d02-155">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="96d02-155">Admin provided name of the device configuration.</span></span> <span data-ttu-id="96d02-156">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="96d02-156">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="96d02-157">version</span><span class="sxs-lookup"><span data-stu-id="96d02-157">version</span></span>|<span data-ttu-id="96d02-158">Int32</span><span class="sxs-lookup"><span data-stu-id="96d02-158">Int32</span></span>|<span data-ttu-id="96d02-159">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="96d02-159">Version of the device configuration.</span></span> <span data-ttu-id="96d02-160">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="96d02-160">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="96d02-161">passwordBlockSimple</span><span class="sxs-lookup"><span data-stu-id="96d02-161">passwordBlockSimple</span></span>|<span data-ttu-id="96d02-162">Booleano</span><span class="sxs-lookup"><span data-stu-id="96d02-162">Boolean</span></span>|<span data-ttu-id="96d02-163">Si quiere bloquear o no la sincronización del calendario.</span><span class="sxs-lookup"><span data-stu-id="96d02-163">Whether or not to block syncing the calendar.</span></span>|
|<span data-ttu-id="96d02-164">passwordExpirationDays</span><span class="sxs-lookup"><span data-stu-id="96d02-164">passwordExpirationDays</span></span>|<span data-ttu-id="96d02-165">Int32</span><span class="sxs-lookup"><span data-stu-id="96d02-165">Int32</span></span>|<span data-ttu-id="96d02-166">Número de días antes de que expire la contraseña.</span><span class="sxs-lookup"><span data-stu-id="96d02-166">Number of days before the password expires.</span></span>|
|<span data-ttu-id="96d02-167">passwordMinimumLength</span><span class="sxs-lookup"><span data-stu-id="96d02-167">passwordMinimumLength</span></span>|<span data-ttu-id="96d02-168">Int32</span><span class="sxs-lookup"><span data-stu-id="96d02-168">Int32</span></span>|<span data-ttu-id="96d02-169">Longitud mínima de las contraseñas.</span><span class="sxs-lookup"><span data-stu-id="96d02-169">Minimum length of passwords.</span></span>|
|<span data-ttu-id="96d02-170">passwordMinutesOfInactivityBeforeLock</span><span class="sxs-lookup"><span data-stu-id="96d02-170">passwordMinutesOfInactivityBeforeLock</span></span>|<span data-ttu-id="96d02-171">Int32</span><span class="sxs-lookup"><span data-stu-id="96d02-171">Int32</span></span>|<span data-ttu-id="96d02-172">Minutos de inactividad antes de que sea necesaria una contraseña.</span><span class="sxs-lookup"><span data-stu-id="96d02-172">Minutes of inactivity before a password is required.</span></span>|
|<span data-ttu-id="96d02-173">passwordMinimumCharacterSetCount</span><span class="sxs-lookup"><span data-stu-id="96d02-173">passwordMinimumCharacterSetCount</span></span>|<span data-ttu-id="96d02-174">Int32</span><span class="sxs-lookup"><span data-stu-id="96d02-174">Int32</span></span>|<span data-ttu-id="96d02-175">Número de juegos de caracteres necesarios en la contraseña.</span><span class="sxs-lookup"><span data-stu-id="96d02-175">The number of character sets required in the password.</span></span>|
|<span data-ttu-id="96d02-176">passwordRequiredType</span><span class="sxs-lookup"><span data-stu-id="96d02-176">passwordRequiredType</span></span>|[<span data-ttu-id="96d02-177">requiredPasswordType</span><span class="sxs-lookup"><span data-stu-id="96d02-177">requiredPasswordType</span></span>](../resources/intune-deviceconfig-requiredpasswordtype.md)|<span data-ttu-id="96d02-178">Tipo de contraseña necesaria.</span><span class="sxs-lookup"><span data-stu-id="96d02-178">The required password type.</span></span> <span data-ttu-id="96d02-179">Los valores posibles son: `deviceDefault`, `alphanumeric` y `numeric`.</span><span class="sxs-lookup"><span data-stu-id="96d02-179">Possible values are: `deviceDefault`, `alphanumeric`, `numeric`.</span></span>|
|<span data-ttu-id="96d02-180">passwordPreviousPasswordBlockCount</span><span class="sxs-lookup"><span data-stu-id="96d02-180">passwordPreviousPasswordBlockCount</span></span>|<span data-ttu-id="96d02-181">Int32</span><span class="sxs-lookup"><span data-stu-id="96d02-181">Int32</span></span>|<span data-ttu-id="96d02-182">Número de contraseñas anteriores que bloquear.</span><span class="sxs-lookup"><span data-stu-id="96d02-182">Number of previous passwords to block.</span></span> <span data-ttu-id="96d02-183">Valores válidos de 0 a 24</span><span class="sxs-lookup"><span data-stu-id="96d02-183">Valid values 0 to 24</span></span>|
|<span data-ttu-id="96d02-184">passwordRequired</span><span class="sxs-lookup"><span data-stu-id="96d02-184">passwordRequired</span></span>|<span data-ttu-id="96d02-185">Booleano</span><span class="sxs-lookup"><span data-stu-id="96d02-185">Boolean</span></span>|<span data-ttu-id="96d02-186">Si quiere requerir o no una contraseña.</span><span class="sxs-lookup"><span data-stu-id="96d02-186">Whether or not to require a password.</span></span>|
|<span data-ttu-id="96d02-187">osMinimumVersion</span><span class="sxs-lookup"><span data-stu-id="96d02-187">osMinimumVersion</span></span>|<span data-ttu-id="96d02-188">String</span><span class="sxs-lookup"><span data-stu-id="96d02-188">String</span></span>|<span data-ttu-id="96d02-189">Versión mínima de Windows Phone.</span><span class="sxs-lookup"><span data-stu-id="96d02-189">Minimum Windows Phone version.</span></span>|
|<span data-ttu-id="96d02-190">osMaximumVersion</span><span class="sxs-lookup"><span data-stu-id="96d02-190">osMaximumVersion</span></span>|<span data-ttu-id="96d02-191">String</span><span class="sxs-lookup"><span data-stu-id="96d02-191">String</span></span>|<span data-ttu-id="96d02-192">Versión máxima de Windows Phone.</span><span class="sxs-lookup"><span data-stu-id="96d02-192">Maximum Windows Phone version.</span></span>|
|<span data-ttu-id="96d02-193">storageRequireEncryption</span><span class="sxs-lookup"><span data-stu-id="96d02-193">storageRequireEncryption</span></span>|<span data-ttu-id="96d02-194">Booleano</span><span class="sxs-lookup"><span data-stu-id="96d02-194">Boolean</span></span>|<span data-ttu-id="96d02-195">Requerir el cifrado en dispositivos de Windows Phone.</span><span class="sxs-lookup"><span data-stu-id="96d02-195">Require encryption on windows phone devices.</span></span>|



## <a name="response"></a><span data-ttu-id="96d02-196">Respuesta</span><span class="sxs-lookup"><span data-stu-id="96d02-196">Response</span></span>
<span data-ttu-id="96d02-197">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [windowsPhone81CompliancePolicy](../resources/intune-deviceconfig-windowsphone81compliancepolicy.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="96d02-197">If successful, this method returns a `200 OK` response code and an updated [windowsPhone81CompliancePolicy](../resources/intune-deviceconfig-windowsphone81compliancepolicy.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="96d02-198">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="96d02-198">Example</span></span>
### <a name="request"></a><span data-ttu-id="96d02-199">Solicitud</span><span class="sxs-lookup"><span data-stu-id="96d02-199">Request</span></span>
<span data-ttu-id="96d02-200">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="96d02-200">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}
Content-type: application/json
Content-length: 664

{
  "roleScopeTagIds": [
    "Role Scope Tag Ids value"
  ],
  "description": "Description value",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "displayName": "Display Name value",
  "version": 7,
  "passwordBlockSimple": true,
  "passwordExpirationDays": 6,
  "passwordMinimumLength": 5,
  "passwordMinutesOfInactivityBeforeLock": 5,
  "passwordMinimumCharacterSetCount": 0,
  "passwordRequiredType": "alphanumeric",
  "passwordPreviousPasswordBlockCount": 2,
  "passwordRequired": true,
  "osMinimumVersion": "Os Minimum Version value",
  "osMaximumVersion": "Os Maximum Version value",
  "storageRequireEncryption": true
}
```

### <a name="response"></a><span data-ttu-id="96d02-201">Respuesta</span><span class="sxs-lookup"><span data-stu-id="96d02-201">Response</span></span>
<span data-ttu-id="96d02-p112">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="96d02-p112">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 841

{
  "@odata.type": "#microsoft.graph.windowsPhone81CompliancePolicy",
  "roleScopeTagIds": [
    "Role Scope Tag Ids value"
  ],
  "id": "e6021ad4-1ad4-e602-d41a-02e6d41a02e6",
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "description": "Description value",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "displayName": "Display Name value",
  "version": 7,
  "passwordBlockSimple": true,
  "passwordExpirationDays": 6,
  "passwordMinimumLength": 5,
  "passwordMinutesOfInactivityBeforeLock": 5,
  "passwordMinimumCharacterSetCount": 0,
  "passwordRequiredType": "alphanumeric",
  "passwordPreviousPasswordBlockCount": 2,
  "passwordRequired": true,
  "osMinimumVersion": "Os Minimum Version value",
  "osMaximumVersion": "Os Maximum Version value",
  "storageRequireEncryption": true
}
```





