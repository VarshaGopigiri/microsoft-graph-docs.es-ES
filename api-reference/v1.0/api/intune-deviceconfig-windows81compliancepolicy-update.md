---
title: Actualizar windows81CompliancePolicy
description: Actualice las propiedades de un objeto windows81CompliancePolicy.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 68e74069a00748a6e94f096dc483061be9ce4b78
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27987261"
---
# <a name="update-windows81compliancepolicy"></a><span data-ttu-id="63e85-103">Actualizar windows81CompliancePolicy</span><span class="sxs-lookup"><span data-stu-id="63e85-103">Update windows81CompliancePolicy</span></span>

> <span data-ttu-id="63e85-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="63e85-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="63e85-105">Actualice las propiedades de un objeto [windows81CompliancePolicy](../resources/intune-deviceconfig-windows81compliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="63e85-105">Update the properties of a [windows81CompliancePolicy](../resources/intune-deviceconfig-windows81compliancepolicy.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="63e85-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="63e85-106">Prerequisites</span></span>
<span data-ttu-id="63e85-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="63e85-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="63e85-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="63e85-109">Permission type</span></span>|<span data-ttu-id="63e85-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="63e85-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="63e85-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="63e85-111">Delegated (work or school account)</span></span>|<span data-ttu-id="63e85-112">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="63e85-112">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="63e85-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="63e85-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="63e85-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="63e85-114">Not supported.</span></span>|
|<span data-ttu-id="63e85-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="63e85-115">Application</span></span>|<span data-ttu-id="63e85-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="63e85-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="63e85-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="63e85-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}
```

## <a name="request-headers"></a><span data-ttu-id="63e85-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="63e85-118">Request headers</span></span>
|<span data-ttu-id="63e85-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="63e85-119">Header</span></span>|<span data-ttu-id="63e85-120">Valor</span><span class="sxs-lookup"><span data-stu-id="63e85-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="63e85-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="63e85-121">Authorization</span></span>|<span data-ttu-id="63e85-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="63e85-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="63e85-123">Accept</span><span class="sxs-lookup"><span data-stu-id="63e85-123">Accept</span></span>|<span data-ttu-id="63e85-124">application/json</span><span class="sxs-lookup"><span data-stu-id="63e85-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="63e85-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="63e85-125">Request body</span></span>
<span data-ttu-id="63e85-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto [windows81CompliancePolicy](../resources/intune-deviceconfig-windows81compliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="63e85-126">In the request body, supply a JSON representation for the [windows81CompliancePolicy](../resources/intune-deviceconfig-windows81compliancepolicy.md) object.</span></span>

<span data-ttu-id="63e85-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [windows81CompliancePolicy](../resources/intune-deviceconfig-windows81compliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="63e85-127">The following table shows the properties that are required when you create the [windows81CompliancePolicy](../resources/intune-deviceconfig-windows81compliancepolicy.md).</span></span>

|<span data-ttu-id="63e85-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="63e85-128">Property</span></span>|<span data-ttu-id="63e85-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="63e85-129">Type</span></span>|<span data-ttu-id="63e85-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="63e85-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="63e85-131">id</span><span class="sxs-lookup"><span data-stu-id="63e85-131">id</span></span>|<span data-ttu-id="63e85-132">Cadena</span><span class="sxs-lookup"><span data-stu-id="63e85-132">String</span></span>|<span data-ttu-id="63e85-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="63e85-133">Key of the entity.</span></span> <span data-ttu-id="63e85-134">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="63e85-134">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="63e85-135">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="63e85-135">createdDateTime</span></span>|<span data-ttu-id="63e85-136">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="63e85-136">DateTimeOffset</span></span>|<span data-ttu-id="63e85-137">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="63e85-137">DateTime the object was created.</span></span> <span data-ttu-id="63e85-138">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="63e85-138">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="63e85-139">descripción</span><span class="sxs-lookup"><span data-stu-id="63e85-139">description</span></span>|<span data-ttu-id="63e85-140">Cadena</span><span class="sxs-lookup"><span data-stu-id="63e85-140">String</span></span>|<span data-ttu-id="63e85-141">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="63e85-141">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="63e85-142">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="63e85-142">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="63e85-143">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="63e85-143">lastModifiedDateTime</span></span>|<span data-ttu-id="63e85-144">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="63e85-144">DateTimeOffset</span></span>|<span data-ttu-id="63e85-145">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="63e85-145">DateTime the object was last modified.</span></span> <span data-ttu-id="63e85-146">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="63e85-146">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="63e85-147">displayName</span><span class="sxs-lookup"><span data-stu-id="63e85-147">displayName</span></span>|<span data-ttu-id="63e85-148">Cadena</span><span class="sxs-lookup"><span data-stu-id="63e85-148">String</span></span>|<span data-ttu-id="63e85-149">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="63e85-149">Admin provided name of the device configuration.</span></span> <span data-ttu-id="63e85-150">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="63e85-150">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="63e85-151">version</span><span class="sxs-lookup"><span data-stu-id="63e85-151">version</span></span>|<span data-ttu-id="63e85-152">Int32</span><span class="sxs-lookup"><span data-stu-id="63e85-152">Int32</span></span>|<span data-ttu-id="63e85-153">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="63e85-153">Version of the device configuration.</span></span> <span data-ttu-id="63e85-154">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="63e85-154">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="63e85-155">passwordRequired</span><span class="sxs-lookup"><span data-stu-id="63e85-155">passwordRequired</span></span>|<span data-ttu-id="63e85-156">Booleano</span><span class="sxs-lookup"><span data-stu-id="63e85-156">Boolean</span></span>|<span data-ttu-id="63e85-157">Exige una contraseña para desbloquear el dispositivo Windows.</span><span class="sxs-lookup"><span data-stu-id="63e85-157">Require a password to unlock Windows device.</span></span>|
|<span data-ttu-id="63e85-158">passwordBlockSimple</span><span class="sxs-lookup"><span data-stu-id="63e85-158">passwordBlockSimple</span></span>|<span data-ttu-id="63e85-159">Booleano</span><span class="sxs-lookup"><span data-stu-id="63e85-159">Boolean</span></span>|<span data-ttu-id="63e85-160">Indica si quiere bloquear o no la contraseña simple.</span><span class="sxs-lookup"><span data-stu-id="63e85-160">Indicates whether or not to block simple password.</span></span>|
|<span data-ttu-id="63e85-161">passwordExpirationDays</span><span class="sxs-lookup"><span data-stu-id="63e85-161">passwordExpirationDays</span></span>|<span data-ttu-id="63e85-162">Int32</span><span class="sxs-lookup"><span data-stu-id="63e85-162">Int32</span></span>|<span data-ttu-id="63e85-163">Expiración de la contraseña en días.</span><span class="sxs-lookup"><span data-stu-id="63e85-163">Password expiration in days.</span></span>|
|<span data-ttu-id="63e85-164">passwordMinimumLength</span><span class="sxs-lookup"><span data-stu-id="63e85-164">passwordMinimumLength</span></span>|<span data-ttu-id="63e85-165">Int32</span><span class="sxs-lookup"><span data-stu-id="63e85-165">Int32</span></span>|<span data-ttu-id="63e85-166">La longitud mínima de contraseña.</span><span class="sxs-lookup"><span data-stu-id="63e85-166">The minimum password length.</span></span>|
|<span data-ttu-id="63e85-167">passwordMinutesOfInactivityBeforeLock</span><span class="sxs-lookup"><span data-stu-id="63e85-167">passwordMinutesOfInactivityBeforeLock</span></span>|<span data-ttu-id="63e85-168">Int32</span><span class="sxs-lookup"><span data-stu-id="63e85-168">Int32</span></span>|<span data-ttu-id="63e85-169">Minutos de inactividad antes de que sea necesaria una contraseña.</span><span class="sxs-lookup"><span data-stu-id="63e85-169">Minutes of inactivity before a password is required.</span></span>|
|<span data-ttu-id="63e85-170">passwordMinimumCharacterSetCount</span><span class="sxs-lookup"><span data-stu-id="63e85-170">passwordMinimumCharacterSetCount</span></span>|<span data-ttu-id="63e85-171">Int32</span><span class="sxs-lookup"><span data-stu-id="63e85-171">Int32</span></span>|<span data-ttu-id="63e85-172">Número de juegos de caracteres necesarios en la contraseña.</span><span class="sxs-lookup"><span data-stu-id="63e85-172">The number of character sets required in the password.</span></span>|
|<span data-ttu-id="63e85-173">passwordRequiredType</span><span class="sxs-lookup"><span data-stu-id="63e85-173">passwordRequiredType</span></span>|[<span data-ttu-id="63e85-174">requiredPasswordType</span><span class="sxs-lookup"><span data-stu-id="63e85-174">requiredPasswordType</span></span>](../resources/intune-deviceconfig-requiredpasswordtype.md)|<span data-ttu-id="63e85-175">Tipo de contraseña necesaria.</span><span class="sxs-lookup"><span data-stu-id="63e85-175">The required password type.</span></span> <span data-ttu-id="63e85-176">Los valores posibles son: `deviceDefault`, `alphanumeric` y `numeric`.</span><span class="sxs-lookup"><span data-stu-id="63e85-176">Possible values are: `deviceDefault`, `alphanumeric`, `numeric`.</span></span>|
|<span data-ttu-id="63e85-177">passwordPreviousPasswordBlockCount</span><span class="sxs-lookup"><span data-stu-id="63e85-177">passwordPreviousPasswordBlockCount</span></span>|<span data-ttu-id="63e85-178">Int32</span><span class="sxs-lookup"><span data-stu-id="63e85-178">Int32</span></span>|<span data-ttu-id="63e85-179">Número de contraseñas anteriores que impide su reutilización.</span><span class="sxs-lookup"><span data-stu-id="63e85-179">The number of previous passwords to prevent re-use of.</span></span> <span data-ttu-id="63e85-180">Valores válidos de 0 a 24</span><span class="sxs-lookup"><span data-stu-id="63e85-180">Valid values 0 to 24</span></span>|
|<span data-ttu-id="63e85-181">osMinimumVersion</span><span class="sxs-lookup"><span data-stu-id="63e85-181">osMinimumVersion</span></span>|<span data-ttu-id="63e85-182">Cadena</span><span class="sxs-lookup"><span data-stu-id="63e85-182">String</span></span>|<span data-ttu-id="63e85-183">Versión mínima de Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="63e85-183">Minimum Windows 8.1 version.</span></span>|
|<span data-ttu-id="63e85-184">osMaximumVersion</span><span class="sxs-lookup"><span data-stu-id="63e85-184">osMaximumVersion</span></span>|<span data-ttu-id="63e85-185">Cadena</span><span class="sxs-lookup"><span data-stu-id="63e85-185">String</span></span>|<span data-ttu-id="63e85-186">Versión máxima de Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="63e85-186">Maximum Windows 8.1 version.</span></span>|
|<span data-ttu-id="63e85-187">storageRequireEncryption</span><span class="sxs-lookup"><span data-stu-id="63e85-187">storageRequireEncryption</span></span>|<span data-ttu-id="63e85-188">Booleano</span><span class="sxs-lookup"><span data-stu-id="63e85-188">Boolean</span></span>|<span data-ttu-id="63e85-189">Indica si quiere requerir o no el cifrado en un dispositivo Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="63e85-189">Indicates whether or not to require encryption on a windows 8.1 device.</span></span>|



## <a name="response"></a><span data-ttu-id="63e85-190">Respuesta</span><span class="sxs-lookup"><span data-stu-id="63e85-190">Response</span></span>
<span data-ttu-id="63e85-191">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [windows81CompliancePolicy](../resources/intune-deviceconfig-windows81compliancepolicy.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="63e85-191">If successful, this method returns a `200 OK` response code and an updated [windows81CompliancePolicy](../resources/intune-deviceconfig-windows81compliancepolicy.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="63e85-192">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="63e85-192">Example</span></span>
### <a name="request"></a><span data-ttu-id="63e85-193">Solicitud</span><span class="sxs-lookup"><span data-stu-id="63e85-193">Request</span></span>
<span data-ttu-id="63e85-194">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="63e85-194">Here is an example of the request.</span></span>
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

### <a name="response"></a><span data-ttu-id="63e85-195">Respuesta</span><span class="sxs-lookup"><span data-stu-id="63e85-195">Response</span></span>
<span data-ttu-id="63e85-p110">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="63e85-p110">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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



