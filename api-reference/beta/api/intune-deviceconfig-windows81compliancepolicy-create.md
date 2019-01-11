---
title: Crear windows81CompliancePolicy
description: Cree un objeto windows81CompliancePolicy.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: bee3e80b08b19009f61fa82ba334dcf962c993c9
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27822606"
---
# <a name="create-windows81compliancepolicy"></a><span data-ttu-id="e2449-103">Crear windows81CompliancePolicy</span><span class="sxs-lookup"><span data-stu-id="e2449-103">Create windows81CompliancePolicy</span></span>

> <span data-ttu-id="e2449-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="e2449-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="e2449-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="e2449-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="e2449-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="e2449-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="e2449-107">Cree un objeto [windows81CompliancePolicy](../resources/intune-deviceconfig-windows81compliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="e2449-107">Create a new [windows81CompliancePolicy](../resources/intune-deviceconfig-windows81compliancepolicy.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="e2449-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="e2449-108">Prerequisites</span></span>
<span data-ttu-id="e2449-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="e2449-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="e2449-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e2449-111">Permission type</span></span>|<span data-ttu-id="e2449-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e2449-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="e2449-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e2449-113">Delegated (work or school account)</span></span>|<span data-ttu-id="e2449-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="e2449-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="e2449-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e2449-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="e2449-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e2449-116">Not supported.</span></span>|
|<span data-ttu-id="e2449-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e2449-117">Application</span></span>|<span data-ttu-id="e2449-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e2449-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="e2449-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e2449-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceCompliancePolicies
```

## <a name="request-headers"></a><span data-ttu-id="e2449-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e2449-120">Request headers</span></span>
|<span data-ttu-id="e2449-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e2449-121">Header</span></span>|<span data-ttu-id="e2449-122">Valor</span><span class="sxs-lookup"><span data-stu-id="e2449-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="e2449-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="e2449-123">Authorization</span></span>|<span data-ttu-id="e2449-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="e2449-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="e2449-125">Accept</span><span class="sxs-lookup"><span data-stu-id="e2449-125">Accept</span></span>|<span data-ttu-id="e2449-126">application/json</span><span class="sxs-lookup"><span data-stu-id="e2449-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="e2449-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="e2449-127">Request body</span></span>
<span data-ttu-id="e2449-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto windows81CompliancePolicy.</span><span class="sxs-lookup"><span data-stu-id="e2449-128">In the request body, supply a JSON representation for the windows81CompliancePolicy object.</span></span>

<span data-ttu-id="e2449-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto windows81CompliancePolicy.</span><span class="sxs-lookup"><span data-stu-id="e2449-129">The following table shows the properties that are required when you create the windows81CompliancePolicy.</span></span>

|<span data-ttu-id="e2449-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e2449-130">Property</span></span>|<span data-ttu-id="e2449-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="e2449-131">Type</span></span>|<span data-ttu-id="e2449-132">Description</span><span class="sxs-lookup"><span data-stu-id="e2449-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="e2449-133">roleScopeTagIds</span><span class="sxs-lookup"><span data-stu-id="e2449-133">roleScopeTagIds</span></span>|<span data-ttu-id="e2449-134">Colección String</span><span class="sxs-lookup"><span data-stu-id="e2449-134">String collection</span></span>|<span data-ttu-id="e2449-135">Lista de etiquetas de ámbito para esta instancia de entidad.</span><span class="sxs-lookup"><span data-stu-id="e2449-135">List of Scope Tags for this Entity instance.</span></span> <span data-ttu-id="e2449-136">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="e2449-136">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="e2449-137">id</span><span class="sxs-lookup"><span data-stu-id="e2449-137">id</span></span>|<span data-ttu-id="e2449-138">Cadena</span><span class="sxs-lookup"><span data-stu-id="e2449-138">String</span></span>|<span data-ttu-id="e2449-139">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="e2449-139">Key of the entity.</span></span> <span data-ttu-id="e2449-140">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="e2449-140">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="e2449-141">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="e2449-141">createdDateTime</span></span>|<span data-ttu-id="e2449-142">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="e2449-142">DateTimeOffset</span></span>|<span data-ttu-id="e2449-143">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="e2449-143">DateTime the object was created.</span></span> <span data-ttu-id="e2449-144">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="e2449-144">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="e2449-145">descripción</span><span class="sxs-lookup"><span data-stu-id="e2449-145">description</span></span>|<span data-ttu-id="e2449-146">Cadena</span><span class="sxs-lookup"><span data-stu-id="e2449-146">String</span></span>|<span data-ttu-id="e2449-147">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e2449-147">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="e2449-148">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="e2449-148">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="e2449-149">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="e2449-149">lastModifiedDateTime</span></span>|<span data-ttu-id="e2449-150">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="e2449-150">DateTimeOffset</span></span>|<span data-ttu-id="e2449-151">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="e2449-151">DateTime the object was last modified.</span></span> <span data-ttu-id="e2449-152">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="e2449-152">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="e2449-153">displayName</span><span class="sxs-lookup"><span data-stu-id="e2449-153">displayName</span></span>|<span data-ttu-id="e2449-154">Cadena</span><span class="sxs-lookup"><span data-stu-id="e2449-154">String</span></span>|<span data-ttu-id="e2449-155">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e2449-155">Admin provided name of the device configuration.</span></span> <span data-ttu-id="e2449-156">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="e2449-156">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="e2449-157">version</span><span class="sxs-lookup"><span data-stu-id="e2449-157">version</span></span>|<span data-ttu-id="e2449-158">Int32</span><span class="sxs-lookup"><span data-stu-id="e2449-158">Int32</span></span>|<span data-ttu-id="e2449-159">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e2449-159">Version of the device configuration.</span></span> <span data-ttu-id="e2449-160">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="e2449-160">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="e2449-161">passwordRequired</span><span class="sxs-lookup"><span data-stu-id="e2449-161">passwordRequired</span></span>|<span data-ttu-id="e2449-162">Booleano</span><span class="sxs-lookup"><span data-stu-id="e2449-162">Boolean</span></span>|<span data-ttu-id="e2449-163">Exige una contraseña para desbloquear el dispositivo Windows.</span><span class="sxs-lookup"><span data-stu-id="e2449-163">Require a password to unlock Windows device.</span></span>|
|<span data-ttu-id="e2449-164">passwordBlockSimple</span><span class="sxs-lookup"><span data-stu-id="e2449-164">passwordBlockSimple</span></span>|<span data-ttu-id="e2449-165">Booleano</span><span class="sxs-lookup"><span data-stu-id="e2449-165">Boolean</span></span>|<span data-ttu-id="e2449-166">Indica si quiere bloquear o no la contraseña simple.</span><span class="sxs-lookup"><span data-stu-id="e2449-166">Indicates whether or not to block simple password.</span></span>|
|<span data-ttu-id="e2449-167">passwordExpirationDays</span><span class="sxs-lookup"><span data-stu-id="e2449-167">passwordExpirationDays</span></span>|<span data-ttu-id="e2449-168">Int32</span><span class="sxs-lookup"><span data-stu-id="e2449-168">Int32</span></span>|<span data-ttu-id="e2449-169">Expiración de la contraseña en días.</span><span class="sxs-lookup"><span data-stu-id="e2449-169">Password expiration in days.</span></span>|
|<span data-ttu-id="e2449-170">passwordMinimumLength</span><span class="sxs-lookup"><span data-stu-id="e2449-170">passwordMinimumLength</span></span>|<span data-ttu-id="e2449-171">Int32</span><span class="sxs-lookup"><span data-stu-id="e2449-171">Int32</span></span>|<span data-ttu-id="e2449-172">La longitud mínima de contraseña.</span><span class="sxs-lookup"><span data-stu-id="e2449-172">The minimum password length.</span></span>|
|<span data-ttu-id="e2449-173">passwordMinutesOfInactivityBeforeLock</span><span class="sxs-lookup"><span data-stu-id="e2449-173">passwordMinutesOfInactivityBeforeLock</span></span>|<span data-ttu-id="e2449-174">Int32</span><span class="sxs-lookup"><span data-stu-id="e2449-174">Int32</span></span>|<span data-ttu-id="e2449-175">Minutos de inactividad antes de que sea necesaria una contraseña.</span><span class="sxs-lookup"><span data-stu-id="e2449-175">Minutes of inactivity before a password is required.</span></span>|
|<span data-ttu-id="e2449-176">passwordMinimumCharacterSetCount</span><span class="sxs-lookup"><span data-stu-id="e2449-176">passwordMinimumCharacterSetCount</span></span>|<span data-ttu-id="e2449-177">Int32</span><span class="sxs-lookup"><span data-stu-id="e2449-177">Int32</span></span>|<span data-ttu-id="e2449-178">Número de juegos de caracteres necesarios en la contraseña.</span><span class="sxs-lookup"><span data-stu-id="e2449-178">The number of character sets required in the password.</span></span>|
|<span data-ttu-id="e2449-179">passwordRequiredType</span><span class="sxs-lookup"><span data-stu-id="e2449-179">passwordRequiredType</span></span>|[<span data-ttu-id="e2449-180">requiredPasswordType</span><span class="sxs-lookup"><span data-stu-id="e2449-180">requiredPasswordType</span></span>](../resources/intune-deviceconfig-requiredpasswordtype.md)|<span data-ttu-id="e2449-181">Tipo de contraseña necesaria.</span><span class="sxs-lookup"><span data-stu-id="e2449-181">The required password type.</span></span> <span data-ttu-id="e2449-182">Los valores posibles son: `deviceDefault`, `alphanumeric` y `numeric`.</span><span class="sxs-lookup"><span data-stu-id="e2449-182">Possible values are: `deviceDefault`, `alphanumeric`, `numeric`.</span></span>|
|<span data-ttu-id="e2449-183">passwordPreviousPasswordBlockCount</span><span class="sxs-lookup"><span data-stu-id="e2449-183">passwordPreviousPasswordBlockCount</span></span>|<span data-ttu-id="e2449-184">Int32</span><span class="sxs-lookup"><span data-stu-id="e2449-184">Int32</span></span>|<span data-ttu-id="e2449-185">Número de contraseñas anteriores que impide su reutilización.</span><span class="sxs-lookup"><span data-stu-id="e2449-185">The number of previous passwords to prevent re-use of.</span></span> <span data-ttu-id="e2449-186">Valores válidos de 0 a 24</span><span class="sxs-lookup"><span data-stu-id="e2449-186">Valid values 0 to 24</span></span>|
|<span data-ttu-id="e2449-187">osMinimumVersion</span><span class="sxs-lookup"><span data-stu-id="e2449-187">osMinimumVersion</span></span>|<span data-ttu-id="e2449-188">Cadena</span><span class="sxs-lookup"><span data-stu-id="e2449-188">String</span></span>|<span data-ttu-id="e2449-189">Versión mínima de Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="e2449-189">Minimum Windows 8.1 version.</span></span>|
|<span data-ttu-id="e2449-190">osMaximumVersion</span><span class="sxs-lookup"><span data-stu-id="e2449-190">osMaximumVersion</span></span>|<span data-ttu-id="e2449-191">Cadena</span><span class="sxs-lookup"><span data-stu-id="e2449-191">String</span></span>|<span data-ttu-id="e2449-192">Versión máxima de Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="e2449-192">Maximum Windows 8.1 version.</span></span>|
|<span data-ttu-id="e2449-193">storageRequireEncryption</span><span class="sxs-lookup"><span data-stu-id="e2449-193">storageRequireEncryption</span></span>|<span data-ttu-id="e2449-194">Booleano</span><span class="sxs-lookup"><span data-stu-id="e2449-194">Boolean</span></span>|<span data-ttu-id="e2449-195">Indica si quiere requerir o no el cifrado en un dispositivo Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="e2449-195">Indicates whether or not to require encryption on a windows 8.1 device.</span></span>|



## <a name="response"></a><span data-ttu-id="e2449-196">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e2449-196">Response</span></span>
<span data-ttu-id="e2449-197">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [windows81CompliancePolicy](../resources/intune-deviceconfig-windows81compliancepolicy.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e2449-197">If successful, this method returns a `201 Created` response code and a [windows81CompliancePolicy](../resources/intune-deviceconfig-windows81compliancepolicy.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="e2449-198">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e2449-198">Example</span></span>
### <a name="request"></a><span data-ttu-id="e2449-199">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e2449-199">Request</span></span>
<span data-ttu-id="e2449-200">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e2449-200">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/deviceCompliancePolicies
Content-type: application/json
Content-length: 728

{
  "@odata.type": "#microsoft.graph.windows81CompliancePolicy",
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
  "passwordMinimumCharacterSetCount": 0,
  "passwordRequiredType": "alphanumeric",
  "passwordPreviousPasswordBlockCount": 2,
  "osMinimumVersion": "Os Minimum Version value",
  "osMaximumVersion": "Os Maximum Version value",
  "storageRequireEncryption": true
}
```

### <a name="response"></a><span data-ttu-id="e2449-201">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e2449-201">Response</span></span>
<span data-ttu-id="e2449-p112">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="e2449-p112">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 836

{
  "@odata.type": "#microsoft.graph.windows81CompliancePolicy",
  "roleScopeTagIds": [
    "Role Scope Tag Ids value"
  ],
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





