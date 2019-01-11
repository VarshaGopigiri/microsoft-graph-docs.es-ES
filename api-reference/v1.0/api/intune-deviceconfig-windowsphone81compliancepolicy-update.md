---
title: Actualizar windowsPhone81CompliancePolicy
description: Actualice las propiedades de un objeto windowsPhone81CompliancePolicy.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 4032364954e6b38e35915d24959f194fdb3344cf
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27815627"
---
# <a name="update-windowsphone81compliancepolicy"></a><span data-ttu-id="1dbd0-103">Actualizar windowsPhone81CompliancePolicy</span><span class="sxs-lookup"><span data-stu-id="1dbd0-103">Update windowsPhone81CompliancePolicy</span></span>

> <span data-ttu-id="1dbd0-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="1dbd0-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="1dbd0-105">Actualice las propiedades de un objeto [windowsPhone81CompliancePolicy](../resources/intune-deviceconfig-windowsphone81compliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="1dbd0-105">Update the properties of a [windowsPhone81CompliancePolicy](../resources/intune-deviceconfig-windowsphone81compliancepolicy.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="1dbd0-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="1dbd0-106">Prerequisites</span></span>
<span data-ttu-id="1dbd0-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="1dbd0-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="1dbd0-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="1dbd0-109">Permission type</span></span>|<span data-ttu-id="1dbd0-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="1dbd0-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="1dbd0-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="1dbd0-111">Delegated (work or school account)</span></span>|<span data-ttu-id="1dbd0-112">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="1dbd0-112">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="1dbd0-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="1dbd0-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="1dbd0-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1dbd0-114">Not supported.</span></span>|
|<span data-ttu-id="1dbd0-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="1dbd0-115">Application</span></span>|<span data-ttu-id="1dbd0-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1dbd0-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="1dbd0-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="1dbd0-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}
```

## <a name="request-headers"></a><span data-ttu-id="1dbd0-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="1dbd0-118">Request headers</span></span>
|<span data-ttu-id="1dbd0-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1dbd0-119">Header</span></span>|<span data-ttu-id="1dbd0-120">Valor</span><span class="sxs-lookup"><span data-stu-id="1dbd0-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="1dbd0-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="1dbd0-121">Authorization</span></span>|<span data-ttu-id="1dbd0-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="1dbd0-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="1dbd0-123">Accept</span><span class="sxs-lookup"><span data-stu-id="1dbd0-123">Accept</span></span>|<span data-ttu-id="1dbd0-124">application/json</span><span class="sxs-lookup"><span data-stu-id="1dbd0-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="1dbd0-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="1dbd0-125">Request body</span></span>
<span data-ttu-id="1dbd0-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto [windowsPhone81CompliancePolicy](../resources/intune-deviceconfig-windowsphone81compliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="1dbd0-126">In the request body, supply a JSON representation for the [windowsPhone81CompliancePolicy](../resources/intune-deviceconfig-windowsphone81compliancepolicy.md) object.</span></span>

<span data-ttu-id="1dbd0-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [windowsPhone81CompliancePolicy](../resources/intune-deviceconfig-windowsphone81compliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="1dbd0-127">The following table shows the properties that are required when you create the [windowsPhone81CompliancePolicy](../resources/intune-deviceconfig-windowsphone81compliancepolicy.md).</span></span>

|<span data-ttu-id="1dbd0-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="1dbd0-128">Property</span></span>|<span data-ttu-id="1dbd0-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="1dbd0-129">Type</span></span>|<span data-ttu-id="1dbd0-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="1dbd0-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="1dbd0-131">id</span><span class="sxs-lookup"><span data-stu-id="1dbd0-131">id</span></span>|<span data-ttu-id="1dbd0-132">Cadena</span><span class="sxs-lookup"><span data-stu-id="1dbd0-132">String</span></span>|<span data-ttu-id="1dbd0-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="1dbd0-133">Key of the entity.</span></span> <span data-ttu-id="1dbd0-134">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="1dbd0-134">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="1dbd0-135">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="1dbd0-135">createdDateTime</span></span>|<span data-ttu-id="1dbd0-136">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="1dbd0-136">DateTimeOffset</span></span>|<span data-ttu-id="1dbd0-137">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="1dbd0-137">DateTime the object was created.</span></span> <span data-ttu-id="1dbd0-138">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="1dbd0-138">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="1dbd0-139">descripción</span><span class="sxs-lookup"><span data-stu-id="1dbd0-139">description</span></span>|<span data-ttu-id="1dbd0-140">Cadena</span><span class="sxs-lookup"><span data-stu-id="1dbd0-140">String</span></span>|<span data-ttu-id="1dbd0-141">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1dbd0-141">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="1dbd0-142">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="1dbd0-142">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="1dbd0-143">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="1dbd0-143">lastModifiedDateTime</span></span>|<span data-ttu-id="1dbd0-144">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="1dbd0-144">DateTimeOffset</span></span>|<span data-ttu-id="1dbd0-145">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="1dbd0-145">DateTime the object was last modified.</span></span> <span data-ttu-id="1dbd0-146">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="1dbd0-146">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="1dbd0-147">displayName</span><span class="sxs-lookup"><span data-stu-id="1dbd0-147">displayName</span></span>|<span data-ttu-id="1dbd0-148">Cadena</span><span class="sxs-lookup"><span data-stu-id="1dbd0-148">String</span></span>|<span data-ttu-id="1dbd0-149">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1dbd0-149">Admin provided name of the device configuration.</span></span> <span data-ttu-id="1dbd0-150">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="1dbd0-150">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="1dbd0-151">version</span><span class="sxs-lookup"><span data-stu-id="1dbd0-151">version</span></span>|<span data-ttu-id="1dbd0-152">Int32</span><span class="sxs-lookup"><span data-stu-id="1dbd0-152">Int32</span></span>|<span data-ttu-id="1dbd0-153">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1dbd0-153">Version of the device configuration.</span></span> <span data-ttu-id="1dbd0-154">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="1dbd0-154">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="1dbd0-155">passwordBlockSimple</span><span class="sxs-lookup"><span data-stu-id="1dbd0-155">passwordBlockSimple</span></span>|<span data-ttu-id="1dbd0-156">Booleano</span><span class="sxs-lookup"><span data-stu-id="1dbd0-156">Boolean</span></span>|<span data-ttu-id="1dbd0-157">Si quiere bloquear o no la sincronización del calendario.</span><span class="sxs-lookup"><span data-stu-id="1dbd0-157">Whether or not to block syncing the calendar.</span></span>|
|<span data-ttu-id="1dbd0-158">passwordExpirationDays</span><span class="sxs-lookup"><span data-stu-id="1dbd0-158">passwordExpirationDays</span></span>|<span data-ttu-id="1dbd0-159">Int32</span><span class="sxs-lookup"><span data-stu-id="1dbd0-159">Int32</span></span>|<span data-ttu-id="1dbd0-160">Número de días antes de que expire la contraseña.</span><span class="sxs-lookup"><span data-stu-id="1dbd0-160">Number of days before the password expires.</span></span>|
|<span data-ttu-id="1dbd0-161">passwordMinimumLength</span><span class="sxs-lookup"><span data-stu-id="1dbd0-161">passwordMinimumLength</span></span>|<span data-ttu-id="1dbd0-162">Int32</span><span class="sxs-lookup"><span data-stu-id="1dbd0-162">Int32</span></span>|<span data-ttu-id="1dbd0-163">Longitud mínima de las contraseñas.</span><span class="sxs-lookup"><span data-stu-id="1dbd0-163">Minimum length of passwords.</span></span>|
|<span data-ttu-id="1dbd0-164">passwordMinutesOfInactivityBeforeLock</span><span class="sxs-lookup"><span data-stu-id="1dbd0-164">passwordMinutesOfInactivityBeforeLock</span></span>|<span data-ttu-id="1dbd0-165">Int32</span><span class="sxs-lookup"><span data-stu-id="1dbd0-165">Int32</span></span>|<span data-ttu-id="1dbd0-166">Minutos de inactividad antes de que sea necesaria una contraseña.</span><span class="sxs-lookup"><span data-stu-id="1dbd0-166">Minutes of inactivity before a password is required.</span></span>|
|<span data-ttu-id="1dbd0-167">passwordMinimumCharacterSetCount</span><span class="sxs-lookup"><span data-stu-id="1dbd0-167">passwordMinimumCharacterSetCount</span></span>|<span data-ttu-id="1dbd0-168">Int32</span><span class="sxs-lookup"><span data-stu-id="1dbd0-168">Int32</span></span>|<span data-ttu-id="1dbd0-169">Número de juegos de caracteres necesarios en la contraseña.</span><span class="sxs-lookup"><span data-stu-id="1dbd0-169">The number of character sets required in the password.</span></span>|
|<span data-ttu-id="1dbd0-170">passwordRequiredType</span><span class="sxs-lookup"><span data-stu-id="1dbd0-170">passwordRequiredType</span></span>|[<span data-ttu-id="1dbd0-171">requiredPasswordType</span><span class="sxs-lookup"><span data-stu-id="1dbd0-171">requiredPasswordType</span></span>](../resources/intune-deviceconfig-requiredpasswordtype.md)|<span data-ttu-id="1dbd0-172">Tipo de contraseña necesaria.</span><span class="sxs-lookup"><span data-stu-id="1dbd0-172">The required password type.</span></span> <span data-ttu-id="1dbd0-173">Los valores posibles son: `deviceDefault`, `alphanumeric` y `numeric`.</span><span class="sxs-lookup"><span data-stu-id="1dbd0-173">Possible values are: `deviceDefault`, `alphanumeric`, `numeric`.</span></span>|
|<span data-ttu-id="1dbd0-174">passwordPreviousPasswordBlockCount</span><span class="sxs-lookup"><span data-stu-id="1dbd0-174">passwordPreviousPasswordBlockCount</span></span>|<span data-ttu-id="1dbd0-175">Int32</span><span class="sxs-lookup"><span data-stu-id="1dbd0-175">Int32</span></span>|<span data-ttu-id="1dbd0-176">Número de contraseñas anteriores que bloquear.</span><span class="sxs-lookup"><span data-stu-id="1dbd0-176">Number of previous passwords to block.</span></span> <span data-ttu-id="1dbd0-177">Valores válidos de 0 a 24</span><span class="sxs-lookup"><span data-stu-id="1dbd0-177">Valid values 0 to 24</span></span>|
|<span data-ttu-id="1dbd0-178">passwordRequired</span><span class="sxs-lookup"><span data-stu-id="1dbd0-178">passwordRequired</span></span>|<span data-ttu-id="1dbd0-179">Booleano</span><span class="sxs-lookup"><span data-stu-id="1dbd0-179">Boolean</span></span>|<span data-ttu-id="1dbd0-180">Si quiere requerir o no una contraseña.</span><span class="sxs-lookup"><span data-stu-id="1dbd0-180">Whether or not to require a password.</span></span>|
|<span data-ttu-id="1dbd0-181">osMinimumVersion</span><span class="sxs-lookup"><span data-stu-id="1dbd0-181">osMinimumVersion</span></span>|<span data-ttu-id="1dbd0-182">Cadena</span><span class="sxs-lookup"><span data-stu-id="1dbd0-182">String</span></span>|<span data-ttu-id="1dbd0-183">Versión mínima de Windows Phone.</span><span class="sxs-lookup"><span data-stu-id="1dbd0-183">Minimum Windows Phone version.</span></span>|
|<span data-ttu-id="1dbd0-184">osMaximumVersion</span><span class="sxs-lookup"><span data-stu-id="1dbd0-184">osMaximumVersion</span></span>|<span data-ttu-id="1dbd0-185">Cadena</span><span class="sxs-lookup"><span data-stu-id="1dbd0-185">String</span></span>|<span data-ttu-id="1dbd0-186">Versión máxima de Windows Phone.</span><span class="sxs-lookup"><span data-stu-id="1dbd0-186">Maximum Windows Phone version.</span></span>|
|<span data-ttu-id="1dbd0-187">storageRequireEncryption</span><span class="sxs-lookup"><span data-stu-id="1dbd0-187">storageRequireEncryption</span></span>|<span data-ttu-id="1dbd0-188">Booleano</span><span class="sxs-lookup"><span data-stu-id="1dbd0-188">Boolean</span></span>|<span data-ttu-id="1dbd0-189">Requerir el cifrado en dispositivos de Windows Phone.</span><span class="sxs-lookup"><span data-stu-id="1dbd0-189">Require encryption on windows phone devices.</span></span>|



## <a name="response"></a><span data-ttu-id="1dbd0-190">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1dbd0-190">Response</span></span>
<span data-ttu-id="1dbd0-191">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [windowsPhone81CompliancePolicy](../resources/intune-deviceconfig-windowsphone81compliancepolicy.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1dbd0-191">If successful, this method returns a `200 OK` response code and an updated [windowsPhone81CompliancePolicy](../resources/intune-deviceconfig-windowsphone81compliancepolicy.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="1dbd0-192">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1dbd0-192">Example</span></span>
### <a name="request"></a><span data-ttu-id="1dbd0-193">Solicitud</span><span class="sxs-lookup"><span data-stu-id="1dbd0-193">Request</span></span>
<span data-ttu-id="1dbd0-194">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="1dbd0-194">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}
Content-type: application/json
Content-length: 607

{
  "@odata.type": "#microsoft.graph.windowsPhone81CompliancePolicy",
  "description": "Description value",
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

### <a name="response"></a><span data-ttu-id="1dbd0-195">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1dbd0-195">Response</span></span>
<span data-ttu-id="1dbd0-p110">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="1dbd0-p110">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 779

{
  "@odata.type": "#microsoft.graph.windowsPhone81CompliancePolicy",
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



