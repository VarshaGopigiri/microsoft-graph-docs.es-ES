---
title: Actualizar windows81CompliancePolicy
description: Actualice las propiedades de un objeto windows81CompliancePolicy.
author: tfitzmac
ms.openlocfilehash: e212739d14b05ea8038bbeb1aeefca7660b6cc3f
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27332763"
---
# <a name="update-windows81compliancepolicy"></a><span data-ttu-id="44ff6-103">Actualizar windows81CompliancePolicy</span><span class="sxs-lookup"><span data-stu-id="44ff6-103">Update windows81CompliancePolicy</span></span>

> <span data-ttu-id="44ff6-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="44ff6-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="44ff6-105">Actualice las propiedades de un objeto [windows81CompliancePolicy](../resources/intune-deviceconfig-windows81compliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="44ff6-105">Update the properties of a [windows81CompliancePolicy](../resources/intune-deviceconfig-windows81compliancepolicy.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="44ff6-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="44ff6-106">Prerequisites</span></span>
<span data-ttu-id="44ff6-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="44ff6-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="44ff6-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="44ff6-109">Permission type</span></span>|<span data-ttu-id="44ff6-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="44ff6-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="44ff6-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="44ff6-111">Delegated (work or school account)</span></span>|<span data-ttu-id="44ff6-112">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="44ff6-112">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="44ff6-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="44ff6-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="44ff6-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="44ff6-114">Not supported.</span></span>|
|<span data-ttu-id="44ff6-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="44ff6-115">Application</span></span>|<span data-ttu-id="44ff6-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="44ff6-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="44ff6-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="44ff6-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}
```

## <a name="request-headers"></a><span data-ttu-id="44ff6-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="44ff6-118">Request headers</span></span>
|<span data-ttu-id="44ff6-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="44ff6-119">Header</span></span>|<span data-ttu-id="44ff6-120">Valor</span><span class="sxs-lookup"><span data-stu-id="44ff6-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="44ff6-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="44ff6-121">Authorization</span></span>|<span data-ttu-id="44ff6-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="44ff6-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="44ff6-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="44ff6-123">Accept</span></span>|<span data-ttu-id="44ff6-124">application/json</span><span class="sxs-lookup"><span data-stu-id="44ff6-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="44ff6-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="44ff6-125">Request body</span></span>
<span data-ttu-id="44ff6-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto [windows81CompliancePolicy](../resources/intune-deviceconfig-windows81compliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="44ff6-126">In the request body, supply a JSON representation for the [windows81CompliancePolicy](../resources/intune-deviceconfig-windows81compliancepolicy.md) object.</span></span>

<span data-ttu-id="44ff6-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [windows81CompliancePolicy](../resources/intune-deviceconfig-windows81compliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="44ff6-127">The following table shows the properties that are required when you create the [windows81CompliancePolicy](../resources/intune-deviceconfig-windows81compliancepolicy.md).</span></span>

|<span data-ttu-id="44ff6-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="44ff6-128">Property</span></span>|<span data-ttu-id="44ff6-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="44ff6-129">Type</span></span>|<span data-ttu-id="44ff6-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="44ff6-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="44ff6-131">id</span><span class="sxs-lookup"><span data-stu-id="44ff6-131">id</span></span>|<span data-ttu-id="44ff6-132">String</span><span class="sxs-lookup"><span data-stu-id="44ff6-132">String</span></span>|<span data-ttu-id="44ff6-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="44ff6-133">Key of the entity.</span></span> <span data-ttu-id="44ff6-134">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="44ff6-134">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="44ff6-135">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="44ff6-135">createdDateTime</span></span>|<span data-ttu-id="44ff6-136">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="44ff6-136">DateTimeOffset</span></span>|<span data-ttu-id="44ff6-137">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="44ff6-137">DateTime the object was created.</span></span> <span data-ttu-id="44ff6-138">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="44ff6-138">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="44ff6-139">descripción</span><span class="sxs-lookup"><span data-stu-id="44ff6-139">description</span></span>|<span data-ttu-id="44ff6-140">String</span><span class="sxs-lookup"><span data-stu-id="44ff6-140">String</span></span>|<span data-ttu-id="44ff6-141">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="44ff6-141">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="44ff6-142">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="44ff6-142">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="44ff6-143">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="44ff6-143">lastModifiedDateTime</span></span>|<span data-ttu-id="44ff6-144">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="44ff6-144">DateTimeOffset</span></span>|<span data-ttu-id="44ff6-145">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="44ff6-145">DateTime the object was last modified.</span></span> <span data-ttu-id="44ff6-146">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="44ff6-146">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="44ff6-147">displayName</span><span class="sxs-lookup"><span data-stu-id="44ff6-147">displayName</span></span>|<span data-ttu-id="44ff6-148">String</span><span class="sxs-lookup"><span data-stu-id="44ff6-148">String</span></span>|<span data-ttu-id="44ff6-149">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="44ff6-149">Admin provided name of the device configuration.</span></span> <span data-ttu-id="44ff6-150">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="44ff6-150">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="44ff6-151">version</span><span class="sxs-lookup"><span data-stu-id="44ff6-151">version</span></span>|<span data-ttu-id="44ff6-152">Int32</span><span class="sxs-lookup"><span data-stu-id="44ff6-152">Int32</span></span>|<span data-ttu-id="44ff6-153">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="44ff6-153">Version of the device configuration.</span></span> <span data-ttu-id="44ff6-154">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="44ff6-154">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="44ff6-155">passwordRequired</span><span class="sxs-lookup"><span data-stu-id="44ff6-155">passwordRequired</span></span>|<span data-ttu-id="44ff6-156">Boolean</span><span class="sxs-lookup"><span data-stu-id="44ff6-156">Boolean</span></span>|<span data-ttu-id="44ff6-157">Exige una contraseña para desbloquear el dispositivo Windows.</span><span class="sxs-lookup"><span data-stu-id="44ff6-157">Require a password to unlock Windows device.</span></span>|
|<span data-ttu-id="44ff6-158">passwordBlockSimple</span><span class="sxs-lookup"><span data-stu-id="44ff6-158">passwordBlockSimple</span></span>|<span data-ttu-id="44ff6-159">Booleano</span><span class="sxs-lookup"><span data-stu-id="44ff6-159">Boolean</span></span>|<span data-ttu-id="44ff6-160">Indica si quiere bloquear o no la contraseña simple.</span><span class="sxs-lookup"><span data-stu-id="44ff6-160">Indicates whether or not to block simple password.</span></span>|
|<span data-ttu-id="44ff6-161">passwordExpirationDays</span><span class="sxs-lookup"><span data-stu-id="44ff6-161">passwordExpirationDays</span></span>|<span data-ttu-id="44ff6-162">Int32</span><span class="sxs-lookup"><span data-stu-id="44ff6-162">Int32</span></span>|<span data-ttu-id="44ff6-163">Expiración de la contraseña en días.</span><span class="sxs-lookup"><span data-stu-id="44ff6-163">Password expiration in days.</span></span>|
|<span data-ttu-id="44ff6-164">passwordMinimumLength</span><span class="sxs-lookup"><span data-stu-id="44ff6-164">passwordMinimumLength</span></span>|<span data-ttu-id="44ff6-165">Int32</span><span class="sxs-lookup"><span data-stu-id="44ff6-165">Int32</span></span>|<span data-ttu-id="44ff6-166">La longitud mínima de contraseña.</span><span class="sxs-lookup"><span data-stu-id="44ff6-166">The minimum password length.</span></span>|
|<span data-ttu-id="44ff6-167">passwordMinutesOfInactivityBeforeLock</span><span class="sxs-lookup"><span data-stu-id="44ff6-167">passwordMinutesOfInactivityBeforeLock</span></span>|<span data-ttu-id="44ff6-168">Int32</span><span class="sxs-lookup"><span data-stu-id="44ff6-168">Int32</span></span>|<span data-ttu-id="44ff6-169">Minutos de inactividad antes de que sea necesaria una contraseña.</span><span class="sxs-lookup"><span data-stu-id="44ff6-169">Minutes of inactivity before a password is required.</span></span>|
|<span data-ttu-id="44ff6-170">passwordMinimumCharacterSetCount</span><span class="sxs-lookup"><span data-stu-id="44ff6-170">passwordMinimumCharacterSetCount</span></span>|<span data-ttu-id="44ff6-171">Int32</span><span class="sxs-lookup"><span data-stu-id="44ff6-171">Int32</span></span>|<span data-ttu-id="44ff6-172">Número de juegos de caracteres necesarios en la contraseña.</span><span class="sxs-lookup"><span data-stu-id="44ff6-172">The number of character sets required in the password.</span></span>|
|<span data-ttu-id="44ff6-173">passwordRequiredType</span><span class="sxs-lookup"><span data-stu-id="44ff6-173">passwordRequiredType</span></span>|[<span data-ttu-id="44ff6-174">requiredPasswordType</span><span class="sxs-lookup"><span data-stu-id="44ff6-174">requiredPasswordType</span></span>](../resources/intune-deviceconfig-requiredpasswordtype.md)|<span data-ttu-id="44ff6-175">Tipo de contraseña necesaria.</span><span class="sxs-lookup"><span data-stu-id="44ff6-175">The required password type.</span></span> <span data-ttu-id="44ff6-176">Los valores posibles son: `deviceDefault`, `alphanumeric` y `numeric`.</span><span class="sxs-lookup"><span data-stu-id="44ff6-176">Possible values are: `deviceDefault`, `alphanumeric`, `numeric`.</span></span>|
|<span data-ttu-id="44ff6-177">passwordPreviousPasswordBlockCount</span><span class="sxs-lookup"><span data-stu-id="44ff6-177">passwordPreviousPasswordBlockCount</span></span>|<span data-ttu-id="44ff6-178">Int32</span><span class="sxs-lookup"><span data-stu-id="44ff6-178">Int32</span></span>|<span data-ttu-id="44ff6-179">Número de contraseñas anteriores que impide su reutilización.</span><span class="sxs-lookup"><span data-stu-id="44ff6-179">The number of previous passwords to prevent re-use of.</span></span> <span data-ttu-id="44ff6-180">Valores válidos de 0 a 24</span><span class="sxs-lookup"><span data-stu-id="44ff6-180">Valid values 0 to 24</span></span>|
|<span data-ttu-id="44ff6-181">osMinimumVersion</span><span class="sxs-lookup"><span data-stu-id="44ff6-181">osMinimumVersion</span></span>|<span data-ttu-id="44ff6-182">String</span><span class="sxs-lookup"><span data-stu-id="44ff6-182">String</span></span>|<span data-ttu-id="44ff6-183">Versión mínima de Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="44ff6-183">Minimum Windows 8.1 version.</span></span>|
|<span data-ttu-id="44ff6-184">osMaximumVersion</span><span class="sxs-lookup"><span data-stu-id="44ff6-184">osMaximumVersion</span></span>|<span data-ttu-id="44ff6-185">String</span><span class="sxs-lookup"><span data-stu-id="44ff6-185">String</span></span>|<span data-ttu-id="44ff6-186">Versión máxima de Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="44ff6-186">Maximum Windows 8.1 version.</span></span>|
|<span data-ttu-id="44ff6-187">storageRequireEncryption</span><span class="sxs-lookup"><span data-stu-id="44ff6-187">storageRequireEncryption</span></span>|<span data-ttu-id="44ff6-188">Boolean</span><span class="sxs-lookup"><span data-stu-id="44ff6-188">Boolean</span></span>|<span data-ttu-id="44ff6-189">Indica si quiere requerir o no el cifrado en un dispositivo Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="44ff6-189">Indicates whether or not to require encryption on a windows 8.1 device.</span></span>|



## <a name="response"></a><span data-ttu-id="44ff6-190">Respuesta</span><span class="sxs-lookup"><span data-stu-id="44ff6-190">Response</span></span>
<span data-ttu-id="44ff6-191">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [windows81CompliancePolicy](../resources/intune-deviceconfig-windows81compliancepolicy.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="44ff6-191">If successful, this method returns a `200 OK` response code and an updated [windows81CompliancePolicy](../resources/intune-deviceconfig-windows81compliancepolicy.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="44ff6-192">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="44ff6-192">Example</span></span>
### <a name="request"></a><span data-ttu-id="44ff6-193">Solicitud</span><span class="sxs-lookup"><span data-stu-id="44ff6-193">Request</span></span>
<span data-ttu-id="44ff6-194">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="44ff6-194">Here is an example of the request.</span></span>
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

### <a name="response"></a><span data-ttu-id="44ff6-195">Respuesta</span><span class="sxs-lookup"><span data-stu-id="44ff6-195">Response</span></span>
<span data-ttu-id="44ff6-p110">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="44ff6-p110">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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



