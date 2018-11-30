---
title: Actualizar macOSGeneralDeviceConfiguration
description: Actualice las propiedades de un objeto macOSGeneralDeviceConfiguration.
ms.openlocfilehash: a2ed3f7aa939f7df18389306cc840e3afdcaf856
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27028570"
---
# <a name="update-macosgeneraldeviceconfiguration"></a><span data-ttu-id="2c8e4-103">Actualizar macOSGeneralDeviceConfiguration</span><span class="sxs-lookup"><span data-stu-id="2c8e4-103">Update macOSGeneralDeviceConfiguration</span></span>

> <span data-ttu-id="2c8e4-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="2c8e4-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="2c8e4-105">Actualice las propiedades de un objeto [macOSGeneralDeviceConfiguration](../resources/intune-deviceconfig-macosgeneraldeviceconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="2c8e4-105">Update the properties of a [macOSGeneralDeviceConfiguration](../resources/intune-deviceconfig-macosgeneraldeviceconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="2c8e4-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="2c8e4-106">Prerequisites</span></span>
<span data-ttu-id="2c8e4-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="2c8e4-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="2c8e4-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="2c8e4-109">Permission type</span></span>|<span data-ttu-id="2c8e4-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="2c8e4-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="2c8e4-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="2c8e4-111">Delegated (work or school account)</span></span>|<span data-ttu-id="2c8e4-112">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="2c8e4-112">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="2c8e4-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="2c8e4-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="2c8e4-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2c8e4-114">Not supported.</span></span>|
|<span data-ttu-id="2c8e4-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="2c8e4-115">Application</span></span>|<span data-ttu-id="2c8e4-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2c8e4-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="2c8e4-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="2c8e4-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}
```

## <a name="request-headers"></a><span data-ttu-id="2c8e4-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="2c8e4-118">Request headers</span></span>
|<span data-ttu-id="2c8e4-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2c8e4-119">Header</span></span>|<span data-ttu-id="2c8e4-120">Valor</span><span class="sxs-lookup"><span data-stu-id="2c8e4-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="2c8e4-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="2c8e4-121">Authorization</span></span>|<span data-ttu-id="2c8e4-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="2c8e4-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="2c8e4-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="2c8e4-123">Accept</span></span>|<span data-ttu-id="2c8e4-124">application/json</span><span class="sxs-lookup"><span data-stu-id="2c8e4-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="2c8e4-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="2c8e4-125">Request body</span></span>
<span data-ttu-id="2c8e4-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto [macOSGeneralDeviceConfiguration](../resources/intune-deviceconfig-macosgeneraldeviceconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="2c8e4-126">In the request body, supply a JSON representation for the [macOSGeneralDeviceConfiguration](../resources/intune-deviceconfig-macosgeneraldeviceconfiguration.md) object.</span></span>

<span data-ttu-id="2c8e4-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [macOSGeneralDeviceConfiguration](../resources/intune-deviceconfig-macosgeneraldeviceconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="2c8e4-127">The following table shows the properties that are required when you create the [macOSGeneralDeviceConfiguration](../resources/intune-deviceconfig-macosgeneraldeviceconfiguration.md).</span></span>

|<span data-ttu-id="2c8e4-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="2c8e4-128">Property</span></span>|<span data-ttu-id="2c8e4-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="2c8e4-129">Type</span></span>|<span data-ttu-id="2c8e4-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="2c8e4-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="2c8e4-131">id</span><span class="sxs-lookup"><span data-stu-id="2c8e4-131">id</span></span>|<span data-ttu-id="2c8e4-132">String</span><span class="sxs-lookup"><span data-stu-id="2c8e4-132">String</span></span>|<span data-ttu-id="2c8e4-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="2c8e4-133">Key of the entity.</span></span> <span data-ttu-id="2c8e4-134">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="2c8e4-134">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="2c8e4-135">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="2c8e4-135">lastModifiedDateTime</span></span>|<span data-ttu-id="2c8e4-136">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="2c8e4-136">DateTimeOffset</span></span>|<span data-ttu-id="2c8e4-137">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="2c8e4-137">DateTime the object was last modified.</span></span> <span data-ttu-id="2c8e4-138">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="2c8e4-138">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="2c8e4-139">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="2c8e4-139">createdDateTime</span></span>|<span data-ttu-id="2c8e4-140">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="2c8e4-140">DateTimeOffset</span></span>|<span data-ttu-id="2c8e4-141">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="2c8e4-141">DateTime the object was created.</span></span> <span data-ttu-id="2c8e4-142">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="2c8e4-142">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="2c8e4-143">descripción</span><span class="sxs-lookup"><span data-stu-id="2c8e4-143">description</span></span>|<span data-ttu-id="2c8e4-144">String</span><span class="sxs-lookup"><span data-stu-id="2c8e4-144">String</span></span>|<span data-ttu-id="2c8e4-145">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2c8e4-145">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="2c8e4-146">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="2c8e4-146">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="2c8e4-147">displayName</span><span class="sxs-lookup"><span data-stu-id="2c8e4-147">displayName</span></span>|<span data-ttu-id="2c8e4-148">String</span><span class="sxs-lookup"><span data-stu-id="2c8e4-148">String</span></span>|<span data-ttu-id="2c8e4-149">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2c8e4-149">Admin provided name of the device configuration.</span></span> <span data-ttu-id="2c8e4-150">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="2c8e4-150">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="2c8e4-151">version</span><span class="sxs-lookup"><span data-stu-id="2c8e4-151">version</span></span>|<span data-ttu-id="2c8e4-152">Int32</span><span class="sxs-lookup"><span data-stu-id="2c8e4-152">Int32</span></span>|<span data-ttu-id="2c8e4-153">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2c8e4-153">Version of the device configuration.</span></span> <span data-ttu-id="2c8e4-154">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="2c8e4-154">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="2c8e4-155">compliantAppsList</span><span class="sxs-lookup"><span data-stu-id="2c8e4-155">compliantAppsList</span></span>|<span data-ttu-id="2c8e4-156">Colección [appListItem](../resources/intune-deviceconfig-applistitem.md)</span><span class="sxs-lookup"><span data-stu-id="2c8e4-156">[appListItem](../resources/intune-deviceconfig-applistitem.md) collection</span></span>|<span data-ttu-id="2c8e4-157">Lista de aplicaciones en el cumplimiento (sea lista de permitidos o de bloqueados, controlado por CompliantAppListType).</span><span class="sxs-lookup"><span data-stu-id="2c8e4-157">List of apps in the compliance (either allow list or block list, controlled by CompliantAppListType).</span></span> <span data-ttu-id="2c8e4-158">Esta colección puede contener un máximo de 10 000 elementos.</span><span class="sxs-lookup"><span data-stu-id="2c8e4-158">This collection can contain a maximum of 10000 elements.</span></span>|
|<span data-ttu-id="2c8e4-159">compliantAppListType</span><span class="sxs-lookup"><span data-stu-id="2c8e4-159">compliantAppListType</span></span>|[<span data-ttu-id="2c8e4-160">appListType</span><span class="sxs-lookup"><span data-stu-id="2c8e4-160">appListType</span></span>](../resources/intune-deviceconfig-applisttype.md)|<span data-ttu-id="2c8e4-161">Lista que se encuentra en la CompliantAppsList.</span><span class="sxs-lookup"><span data-stu-id="2c8e4-161">List that is in the CompliantAppsList.</span></span> <span data-ttu-id="2c8e4-162">Los valores posibles son: `none`, `appsInListCompliant` y `appsNotInListCompliant`.</span><span class="sxs-lookup"><span data-stu-id="2c8e4-162">Possible values are: `none`, `appsInListCompliant`, `appsNotInListCompliant`.</span></span>|
|<span data-ttu-id="2c8e4-163">emailInDomainSuffixes</span><span class="sxs-lookup"><span data-stu-id="2c8e4-163">emailInDomainSuffixes</span></span>|<span data-ttu-id="2c8e4-164">Colección String</span><span class="sxs-lookup"><span data-stu-id="2c8e4-164">String collection</span></span>|<span data-ttu-id="2c8e4-165">Una dirección de correo electrónico que carezca de un sufijo que coincida con cualquiera de estas cadenas se considerará fuera de dominio.</span><span class="sxs-lookup"><span data-stu-id="2c8e4-165">An email address lacking a suffix that matches any of these strings will be considered out-of-domain.</span></span>|
|<span data-ttu-id="2c8e4-166">passwordBlockSimple</span><span class="sxs-lookup"><span data-stu-id="2c8e4-166">passwordBlockSimple</span></span>|<span data-ttu-id="2c8e4-167">Booleano</span><span class="sxs-lookup"><span data-stu-id="2c8e4-167">Boolean</span></span>|<span data-ttu-id="2c8e4-168">Bloquear contraseñas sencillas.</span><span class="sxs-lookup"><span data-stu-id="2c8e4-168">Block simple passwords.</span></span>|
|<span data-ttu-id="2c8e4-169">passwordExpirationDays</span><span class="sxs-lookup"><span data-stu-id="2c8e4-169">passwordExpirationDays</span></span>|<span data-ttu-id="2c8e4-170">Int32</span><span class="sxs-lookup"><span data-stu-id="2c8e4-170">Int32</span></span>|<span data-ttu-id="2c8e4-171">Número de días antes de que expire la contraseña.</span><span class="sxs-lookup"><span data-stu-id="2c8e4-171">Number of days before the password expires.</span></span>|
|<span data-ttu-id="2c8e4-172">passwordMinimumCharacterSetCount</span><span class="sxs-lookup"><span data-stu-id="2c8e4-172">passwordMinimumCharacterSetCount</span></span>|<span data-ttu-id="2c8e4-173">Int32</span><span class="sxs-lookup"><span data-stu-id="2c8e4-173">Int32</span></span>|<span data-ttu-id="2c8e4-174">Número de juegos de caracteres que debe contener una contraseña.</span><span class="sxs-lookup"><span data-stu-id="2c8e4-174">Number of character sets a password must contain.</span></span> <span data-ttu-id="2c8e4-175">Valores válidos de 0 a 4.</span><span class="sxs-lookup"><span data-stu-id="2c8e4-175">Valid values 0 to 4</span></span>|
|<span data-ttu-id="2c8e4-176">passwordMinimumLength</span><span class="sxs-lookup"><span data-stu-id="2c8e4-176">passwordMinimumLength</span></span>|<span data-ttu-id="2c8e4-177">Int32</span><span class="sxs-lookup"><span data-stu-id="2c8e4-177">Int32</span></span>|<span data-ttu-id="2c8e4-178">Longitud mínima de las contraseñas.</span><span class="sxs-lookup"><span data-stu-id="2c8e4-178">Minimum length of passwords.</span></span>|
|<span data-ttu-id="2c8e4-179">passwordMinutesOfInactivityBeforeLock</span><span class="sxs-lookup"><span data-stu-id="2c8e4-179">passwordMinutesOfInactivityBeforeLock</span></span>|<span data-ttu-id="2c8e4-180">Int32</span><span class="sxs-lookup"><span data-stu-id="2c8e4-180">Int32</span></span>|<span data-ttu-id="2c8e4-181">Minutos de inactividad antes de que sea necesaria una contraseña.</span><span class="sxs-lookup"><span data-stu-id="2c8e4-181">Minutes of inactivity required before a password is required.</span></span>|
|<span data-ttu-id="2c8e4-182">passwordMinutesOfInactivityBeforeScreenTimeout</span><span class="sxs-lookup"><span data-stu-id="2c8e4-182">passwordMinutesOfInactivityBeforeScreenTimeout</span></span>|<span data-ttu-id="2c8e4-183">Int32</span><span class="sxs-lookup"><span data-stu-id="2c8e4-183">Int32</span></span>|<span data-ttu-id="2c8e4-184">Minutos de inactividad que se requieren antes de que se agote el tiempo de espera de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="2c8e4-184">Minutes of inactivity required before the screen times out.</span></span>|
|<span data-ttu-id="2c8e4-185">passwordPreviousPasswordBlockCount</span><span class="sxs-lookup"><span data-stu-id="2c8e4-185">passwordPreviousPasswordBlockCount</span></span>|<span data-ttu-id="2c8e4-186">Int32</span><span class="sxs-lookup"><span data-stu-id="2c8e4-186">Int32</span></span>|<span data-ttu-id="2c8e4-187">Número de contraseñas anteriores que bloquear.</span><span class="sxs-lookup"><span data-stu-id="2c8e4-187">Number of previous passwords to block.</span></span>|
|<span data-ttu-id="2c8e4-188">passwordRequiredType</span><span class="sxs-lookup"><span data-stu-id="2c8e4-188">passwordRequiredType</span></span>|[<span data-ttu-id="2c8e4-189">requiredPasswordType</span><span class="sxs-lookup"><span data-stu-id="2c8e4-189">requiredPasswordType</span></span>](../resources/intune-deviceconfig-requiredpasswordtype.md)|<span data-ttu-id="2c8e4-190">Tipo de contraseña que es necesario.</span><span class="sxs-lookup"><span data-stu-id="2c8e4-190">Type of password that is required.</span></span> <span data-ttu-id="2c8e4-191">Los valores posibles son: `deviceDefault`, `alphanumeric` y `numeric`.</span><span class="sxs-lookup"><span data-stu-id="2c8e4-191">Possible values are: `deviceDefault`, `alphanumeric`, `numeric`.</span></span>|
|<span data-ttu-id="2c8e4-192">passwordRequired</span><span class="sxs-lookup"><span data-stu-id="2c8e4-192">passwordRequired</span></span>|<span data-ttu-id="2c8e4-193">Booleano</span><span class="sxs-lookup"><span data-stu-id="2c8e4-193">Boolean</span></span>|<span data-ttu-id="2c8e4-194">Si quiere requerir o no una contraseña.</span><span class="sxs-lookup"><span data-stu-id="2c8e4-194">Whether or not to require a password.</span></span>|



## <a name="response"></a><span data-ttu-id="2c8e4-195">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2c8e4-195">Response</span></span>
<span data-ttu-id="2c8e4-196">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [macOSGeneralDeviceConfiguration](../resources/intune-deviceconfig-macosgeneraldeviceconfiguration.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2c8e4-196">If successful, this method returns a `200 OK` response code and an updated [macOSGeneralDeviceConfiguration](../resources/intune-deviceconfig-macosgeneraldeviceconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="2c8e4-197">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2c8e4-197">Example</span></span>
### <a name="request"></a><span data-ttu-id="2c8e4-198">Solicitud</span><span class="sxs-lookup"><span data-stu-id="2c8e4-198">Request</span></span>
<span data-ttu-id="2c8e4-199">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="2c8e4-199">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/deviceConfigurations/{deviceConfigurationId}
Content-type: application/json
Content-length: 906

{
  "@odata.type": "#microsoft.graph.macOSGeneralDeviceConfiguration",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "compliantAppsList": [
    {
      "@odata.type": "microsoft.graph.appListItem",
      "name": "Name value",
      "publisher": "Publisher value",
      "appStoreUrl": "https://example.com/appStoreUrl/",
      "appId": "App Id value"
    }
  ],
  "compliantAppListType": "appsInListCompliant",
  "emailInDomainSuffixes": [
    "Email In Domain Suffixes value"
  ],
  "passwordBlockSimple": true,
  "passwordExpirationDays": 6,
  "passwordMinimumCharacterSetCount": 0,
  "passwordMinimumLength": 5,
  "passwordMinutesOfInactivityBeforeLock": 5,
  "passwordMinutesOfInactivityBeforeScreenTimeout": 14,
  "passwordPreviousPasswordBlockCount": 2,
  "passwordRequiredType": "alphanumeric",
  "passwordRequired": true
}
```

### <a name="response"></a><span data-ttu-id="2c8e4-200">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2c8e4-200">Response</span></span>
<span data-ttu-id="2c8e4-p112">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="2c8e4-p112">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1078

{
  "@odata.type": "#microsoft.graph.macOSGeneralDeviceConfiguration",
  "id": "dc356aee-6aee-dc35-ee6a-35dcee6a35dc",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "compliantAppsList": [
    {
      "@odata.type": "microsoft.graph.appListItem",
      "name": "Name value",
      "publisher": "Publisher value",
      "appStoreUrl": "https://example.com/appStoreUrl/",
      "appId": "App Id value"
    }
  ],
  "compliantAppListType": "appsInListCompliant",
  "emailInDomainSuffixes": [
    "Email In Domain Suffixes value"
  ],
  "passwordBlockSimple": true,
  "passwordExpirationDays": 6,
  "passwordMinimumCharacterSetCount": 0,
  "passwordMinimumLength": 5,
  "passwordMinutesOfInactivityBeforeLock": 5,
  "passwordMinutesOfInactivityBeforeScreenTimeout": 14,
  "passwordPreviousPasswordBlockCount": 2,
  "passwordRequiredType": "alphanumeric",
  "passwordRequired": true
}
```



