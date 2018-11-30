---
title: Actualizar windows81CompliancePolicy
description: Actualice las propiedades de un objeto windows81CompliancePolicy.
ms.openlocfilehash: 52e76e1be627633f6bba0a78c451afb8b184d265
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030967"
---
# <a name="update-windows81compliancepolicy"></a><span data-ttu-id="b1625-103">Actualizar windows81CompliancePolicy</span><span class="sxs-lookup"><span data-stu-id="b1625-103">Update windows81CompliancePolicy</span></span>

> <span data-ttu-id="b1625-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="b1625-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="b1625-105">Actualice las propiedades de un objeto [windows81CompliancePolicy](../resources/intune-deviceconfig-windows81compliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="b1625-105">Update the properties of a [windows81CompliancePolicy](../resources/intune-deviceconfig-windows81compliancepolicy.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="b1625-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="b1625-106">Prerequisites</span></span>
<span data-ttu-id="b1625-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="b1625-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="b1625-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b1625-109">Permission type</span></span>|<span data-ttu-id="b1625-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b1625-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="b1625-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b1625-111">Delegated (work or school account)</span></span>|<span data-ttu-id="b1625-112">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="b1625-112">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="b1625-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b1625-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="b1625-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b1625-114">Not supported.</span></span>|
|<span data-ttu-id="b1625-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b1625-115">Application</span></span>|<span data-ttu-id="b1625-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b1625-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="b1625-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b1625-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}
```

## <a name="request-headers"></a><span data-ttu-id="b1625-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b1625-118">Request headers</span></span>
|<span data-ttu-id="b1625-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b1625-119">Header</span></span>|<span data-ttu-id="b1625-120">Valor</span><span class="sxs-lookup"><span data-stu-id="b1625-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="b1625-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="b1625-121">Authorization</span></span>|<span data-ttu-id="b1625-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="b1625-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="b1625-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="b1625-123">Accept</span></span>|<span data-ttu-id="b1625-124">application/json</span><span class="sxs-lookup"><span data-stu-id="b1625-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="b1625-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b1625-125">Request body</span></span>
<span data-ttu-id="b1625-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto [windows81CompliancePolicy](../resources/intune-deviceconfig-windows81compliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="b1625-126">In the request body, supply a JSON representation for the [windows81CompliancePolicy](../resources/intune-deviceconfig-windows81compliancepolicy.md) object.</span></span>

<span data-ttu-id="b1625-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [windows81CompliancePolicy](../resources/intune-deviceconfig-windows81compliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="b1625-127">The following table shows the properties that are required when you create the [windows81CompliancePolicy](../resources/intune-deviceconfig-windows81compliancepolicy.md).</span></span>

|<span data-ttu-id="b1625-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="b1625-128">Property</span></span>|<span data-ttu-id="b1625-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="b1625-129">Type</span></span>|<span data-ttu-id="b1625-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="b1625-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="b1625-131">id</span><span class="sxs-lookup"><span data-stu-id="b1625-131">id</span></span>|<span data-ttu-id="b1625-132">String</span><span class="sxs-lookup"><span data-stu-id="b1625-132">String</span></span>|<span data-ttu-id="b1625-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="b1625-133">Key of the entity.</span></span> <span data-ttu-id="b1625-134">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="b1625-134">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="b1625-135">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="b1625-135">createdDateTime</span></span>|<span data-ttu-id="b1625-136">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="b1625-136">DateTimeOffset</span></span>|<span data-ttu-id="b1625-137">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="b1625-137">DateTime the object was created.</span></span> <span data-ttu-id="b1625-138">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="b1625-138">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="b1625-139">descripción</span><span class="sxs-lookup"><span data-stu-id="b1625-139">description</span></span>|<span data-ttu-id="b1625-140">String</span><span class="sxs-lookup"><span data-stu-id="b1625-140">String</span></span>|<span data-ttu-id="b1625-141">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b1625-141">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="b1625-142">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="b1625-142">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="b1625-143">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="b1625-143">lastModifiedDateTime</span></span>|<span data-ttu-id="b1625-144">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="b1625-144">DateTimeOffset</span></span>|<span data-ttu-id="b1625-145">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="b1625-145">DateTime the object was last modified.</span></span> <span data-ttu-id="b1625-146">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="b1625-146">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="b1625-147">displayName</span><span class="sxs-lookup"><span data-stu-id="b1625-147">displayName</span></span>|<span data-ttu-id="b1625-148">String</span><span class="sxs-lookup"><span data-stu-id="b1625-148">String</span></span>|<span data-ttu-id="b1625-149">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b1625-149">Admin provided name of the device configuration.</span></span> <span data-ttu-id="b1625-150">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="b1625-150">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="b1625-151">version</span><span class="sxs-lookup"><span data-stu-id="b1625-151">version</span></span>|<span data-ttu-id="b1625-152">Int32</span><span class="sxs-lookup"><span data-stu-id="b1625-152">Int32</span></span>|<span data-ttu-id="b1625-153">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b1625-153">Version of the device configuration.</span></span> <span data-ttu-id="b1625-154">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="b1625-154">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="b1625-155">passwordRequired</span><span class="sxs-lookup"><span data-stu-id="b1625-155">passwordRequired</span></span>|<span data-ttu-id="b1625-156">Booleano</span><span class="sxs-lookup"><span data-stu-id="b1625-156">Boolean</span></span>|<span data-ttu-id="b1625-157">Exige una contraseña para desbloquear el dispositivo Windows.</span><span class="sxs-lookup"><span data-stu-id="b1625-157">Require a password to unlock Windows device.</span></span>|
|<span data-ttu-id="b1625-158">passwordBlockSimple</span><span class="sxs-lookup"><span data-stu-id="b1625-158">passwordBlockSimple</span></span>|<span data-ttu-id="b1625-159">Booleano</span><span class="sxs-lookup"><span data-stu-id="b1625-159">Boolean</span></span>|<span data-ttu-id="b1625-160">Indica si quiere bloquear o no la contraseña simple.</span><span class="sxs-lookup"><span data-stu-id="b1625-160">Indicates whether or not to block simple password.</span></span>|
|<span data-ttu-id="b1625-161">passwordExpirationDays</span><span class="sxs-lookup"><span data-stu-id="b1625-161">passwordExpirationDays</span></span>|<span data-ttu-id="b1625-162">Int32</span><span class="sxs-lookup"><span data-stu-id="b1625-162">Int32</span></span>|<span data-ttu-id="b1625-163">Expiración de la contraseña en días.</span><span class="sxs-lookup"><span data-stu-id="b1625-163">Password expiration in days.</span></span>|
|<span data-ttu-id="b1625-164">passwordMinimumLength</span><span class="sxs-lookup"><span data-stu-id="b1625-164">passwordMinimumLength</span></span>|<span data-ttu-id="b1625-165">Int32</span><span class="sxs-lookup"><span data-stu-id="b1625-165">Int32</span></span>|<span data-ttu-id="b1625-166">La longitud mínima de contraseña.</span><span class="sxs-lookup"><span data-stu-id="b1625-166">The minimum password length.</span></span>|
|<span data-ttu-id="b1625-167">passwordMinutesOfInactivityBeforeLock</span><span class="sxs-lookup"><span data-stu-id="b1625-167">passwordMinutesOfInactivityBeforeLock</span></span>|<span data-ttu-id="b1625-168">Int32</span><span class="sxs-lookup"><span data-stu-id="b1625-168">Int32</span></span>|<span data-ttu-id="b1625-169">Minutos de inactividad antes de que sea necesaria una contraseña.</span><span class="sxs-lookup"><span data-stu-id="b1625-169">Minutes of inactivity before a password is required.</span></span>|
|<span data-ttu-id="b1625-170">passwordMinimumCharacterSetCount</span><span class="sxs-lookup"><span data-stu-id="b1625-170">passwordMinimumCharacterSetCount</span></span>|<span data-ttu-id="b1625-171">Int32</span><span class="sxs-lookup"><span data-stu-id="b1625-171">Int32</span></span>|<span data-ttu-id="b1625-172">Número de juegos de caracteres necesarios en la contraseña.</span><span class="sxs-lookup"><span data-stu-id="b1625-172">The number of character sets required in the password.</span></span>|
|<span data-ttu-id="b1625-173">passwordRequiredType</span><span class="sxs-lookup"><span data-stu-id="b1625-173">passwordRequiredType</span></span>|[<span data-ttu-id="b1625-174">requiredPasswordType</span><span class="sxs-lookup"><span data-stu-id="b1625-174">requiredPasswordType</span></span>](../resources/intune-deviceconfig-requiredpasswordtype.md)|<span data-ttu-id="b1625-175">Tipo de contraseña necesaria.</span><span class="sxs-lookup"><span data-stu-id="b1625-175">The required password type.</span></span> <span data-ttu-id="b1625-176">Los valores posibles son: `deviceDefault`, `alphanumeric` y `numeric`.</span><span class="sxs-lookup"><span data-stu-id="b1625-176">Possible values are: `deviceDefault`, `alphanumeric`, `numeric`.</span></span>|
|<span data-ttu-id="b1625-177">passwordPreviousPasswordBlockCount</span><span class="sxs-lookup"><span data-stu-id="b1625-177">passwordPreviousPasswordBlockCount</span></span>|<span data-ttu-id="b1625-178">Int32</span><span class="sxs-lookup"><span data-stu-id="b1625-178">Int32</span></span>|<span data-ttu-id="b1625-179">Número de contraseñas anteriores que impide su reutilización.</span><span class="sxs-lookup"><span data-stu-id="b1625-179">The number of previous passwords to prevent re-use of.</span></span> <span data-ttu-id="b1625-180">Valores válidos de 0 a 24</span><span class="sxs-lookup"><span data-stu-id="b1625-180">Valid values 0 to 24</span></span>|
|<span data-ttu-id="b1625-181">osMinimumVersion</span><span class="sxs-lookup"><span data-stu-id="b1625-181">osMinimumVersion</span></span>|<span data-ttu-id="b1625-182">String</span><span class="sxs-lookup"><span data-stu-id="b1625-182">String</span></span>|<span data-ttu-id="b1625-183">Versión mínima de Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="b1625-183">Minimum Windows 8.1 version.</span></span>|
|<span data-ttu-id="b1625-184">osMaximumVersion</span><span class="sxs-lookup"><span data-stu-id="b1625-184">osMaximumVersion</span></span>|<span data-ttu-id="b1625-185">String</span><span class="sxs-lookup"><span data-stu-id="b1625-185">String</span></span>|<span data-ttu-id="b1625-186">Versión máxima de Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="b1625-186">Maximum Windows 8.1 version.</span></span>|
|<span data-ttu-id="b1625-187">storageRequireEncryption</span><span class="sxs-lookup"><span data-stu-id="b1625-187">storageRequireEncryption</span></span>|<span data-ttu-id="b1625-188">Booleano</span><span class="sxs-lookup"><span data-stu-id="b1625-188">Boolean</span></span>|<span data-ttu-id="b1625-189">Indica si quiere requerir o no el cifrado en un dispositivo Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="b1625-189">Indicates whether or not to require encryption on a windows 8.1 device.</span></span>|



## <a name="response"></a><span data-ttu-id="b1625-190">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b1625-190">Response</span></span>
<span data-ttu-id="b1625-191">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [windows81CompliancePolicy](../resources/intune-deviceconfig-windows81compliancepolicy.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b1625-191">If successful, this method returns a `200 OK` response code and an updated [windows81CompliancePolicy](../resources/intune-deviceconfig-windows81compliancepolicy.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="b1625-192">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b1625-192">Example</span></span>
### <a name="request"></a><span data-ttu-id="b1625-193">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b1625-193">Request</span></span>
<span data-ttu-id="b1625-194">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b1625-194">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}
Content-type: application/json
Content-length: 602

{
  "@odata.type": "#microsoft.graph.windows81CompliancePolicy",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "passwordRequired": true,
  "passwordBlockSimple": true,
  "passwordExpirationDays": 6,
  "passwordMinimumLength": 5,
  "passwordMinutesOfInactivityBeforeLock": 5,
  "passwordMinimumCharacterSetCount": 0,
  "passwordRequiredType": "alphanumeric",
  "passwordPreviousPasswordBlockCount": 2,
  "osMinimumVersion": "Os Minimum Version value",
  "osMaximumVersion": "Os Maximum Version value",
  "storageRequireEncryption": true
}
```

### <a name="response"></a><span data-ttu-id="b1625-195">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b1625-195">Response</span></span>
<span data-ttu-id="b1625-p110">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="b1625-p110">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 774

{
  "@odata.type": "#microsoft.graph.windows81CompliancePolicy",
  "id": "6bb4b7e0-b7e0-6bb4-e0b7-b46be0b7b46b",
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
  "passwordMinimumCharacterSetCount": 0,
  "passwordRequiredType": "alphanumeric",
  "passwordPreviousPasswordBlockCount": 2,
  "osMinimumVersion": "Os Minimum Version value",
  "osMaximumVersion": "Os Maximum Version value",
  "storageRequireEncryption": true
}
```



