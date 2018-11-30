---
title: Crear macOSGeneralDeviceConfiguration
description: Crear un objeto macOSGeneralDeviceConfiguration.
ms.openlocfilehash: 357f563efffa7d08ef0dab4a66d9b7534b5d95b2
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029567"
---
# <a name="create-macosgeneraldeviceconfiguration"></a><span data-ttu-id="8b762-103">Crear macOSGeneralDeviceConfiguration</span><span class="sxs-lookup"><span data-stu-id="8b762-103">Create macOSGeneralDeviceConfiguration</span></span>

> <span data-ttu-id="8b762-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="8b762-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="8b762-105">Crear un objeto [macOSGeneralDeviceConfiguration](../resources/intune-deviceconfig-macosgeneraldeviceconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="8b762-105">Create a new [macOSGeneralDeviceConfiguration](../resources/intune-deviceconfig-macosgeneraldeviceconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="8b762-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="8b762-106">Prerequisites</span></span>
<span data-ttu-id="8b762-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="8b762-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="8b762-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="8b762-109">Permission type</span></span>|<span data-ttu-id="8b762-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="8b762-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="8b762-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="8b762-111">Delegated (work or school account)</span></span>|<span data-ttu-id="8b762-112">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="8b762-112">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="8b762-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="8b762-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="8b762-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8b762-114">Not supported.</span></span>|
|<span data-ttu-id="8b762-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="8b762-115">Application</span></span>|<span data-ttu-id="8b762-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8b762-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="8b762-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="8b762-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="8b762-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="8b762-118">Request headers</span></span>
|<span data-ttu-id="8b762-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8b762-119">Header</span></span>|<span data-ttu-id="8b762-120">Valor</span><span class="sxs-lookup"><span data-stu-id="8b762-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="8b762-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="8b762-121">Authorization</span></span>|<span data-ttu-id="8b762-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="8b762-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="8b762-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="8b762-123">Accept</span></span>|<span data-ttu-id="8b762-124">application/json</span><span class="sxs-lookup"><span data-stu-id="8b762-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="8b762-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="8b762-125">Request body</span></span>
<span data-ttu-id="8b762-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto macOSGeneralDeviceConfiguration.</span><span class="sxs-lookup"><span data-stu-id="8b762-126">In the request body, supply a JSON representation for the macOSGeneralDeviceConfiguration object.</span></span>

<span data-ttu-id="8b762-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto macOSGeneralDeviceConfiguration.</span><span class="sxs-lookup"><span data-stu-id="8b762-127">The following table shows the properties that are required when you create the macOSGeneralDeviceConfiguration.</span></span>

|<span data-ttu-id="8b762-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="8b762-128">Property</span></span>|<span data-ttu-id="8b762-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="8b762-129">Type</span></span>|<span data-ttu-id="8b762-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="8b762-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="8b762-131">id</span><span class="sxs-lookup"><span data-stu-id="8b762-131">id</span></span>|<span data-ttu-id="8b762-132">String</span><span class="sxs-lookup"><span data-stu-id="8b762-132">String</span></span>|<span data-ttu-id="8b762-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="8b762-133">Key of the entity.</span></span> <span data-ttu-id="8b762-134">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="8b762-134">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="8b762-135">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="8b762-135">lastModifiedDateTime</span></span>|<span data-ttu-id="8b762-136">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="8b762-136">DateTimeOffset</span></span>|<span data-ttu-id="8b762-137">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="8b762-137">DateTime the object was last modified.</span></span> <span data-ttu-id="8b762-138">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="8b762-138">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="8b762-139">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="8b762-139">createdDateTime</span></span>|<span data-ttu-id="8b762-140">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="8b762-140">DateTimeOffset</span></span>|<span data-ttu-id="8b762-141">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="8b762-141">DateTime the object was created.</span></span> <span data-ttu-id="8b762-142">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="8b762-142">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="8b762-143">descripción</span><span class="sxs-lookup"><span data-stu-id="8b762-143">description</span></span>|<span data-ttu-id="8b762-144">String</span><span class="sxs-lookup"><span data-stu-id="8b762-144">String</span></span>|<span data-ttu-id="8b762-145">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8b762-145">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="8b762-146">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="8b762-146">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="8b762-147">displayName</span><span class="sxs-lookup"><span data-stu-id="8b762-147">displayName</span></span>|<span data-ttu-id="8b762-148">String</span><span class="sxs-lookup"><span data-stu-id="8b762-148">String</span></span>|<span data-ttu-id="8b762-149">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8b762-149">Admin provided name of the device configuration.</span></span> <span data-ttu-id="8b762-150">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="8b762-150">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="8b762-151">version</span><span class="sxs-lookup"><span data-stu-id="8b762-151">version</span></span>|<span data-ttu-id="8b762-152">Int32</span><span class="sxs-lookup"><span data-stu-id="8b762-152">Int32</span></span>|<span data-ttu-id="8b762-153">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8b762-153">Version of the device configuration.</span></span> <span data-ttu-id="8b762-154">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="8b762-154">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="8b762-155">compliantAppsList</span><span class="sxs-lookup"><span data-stu-id="8b762-155">compliantAppsList</span></span>|<span data-ttu-id="8b762-156">Colección [appListItem](../resources/intune-deviceconfig-applistitem.md)</span><span class="sxs-lookup"><span data-stu-id="8b762-156">[appListItem](../resources/intune-deviceconfig-applistitem.md) collection</span></span>|<span data-ttu-id="8b762-157">Lista de aplicaciones en el cumplimiento (sea lista de permitidos o de bloqueados, controlado por CompliantAppListType).</span><span class="sxs-lookup"><span data-stu-id="8b762-157">List of apps in the compliance (either allow list or block list, controlled by CompliantAppListType).</span></span> <span data-ttu-id="8b762-158">Esta colección puede contener un máximo de 10 000 elementos.</span><span class="sxs-lookup"><span data-stu-id="8b762-158">This collection can contain a maximum of 10000 elements.</span></span>|
|<span data-ttu-id="8b762-159">compliantAppListType</span><span class="sxs-lookup"><span data-stu-id="8b762-159">compliantAppListType</span></span>|[<span data-ttu-id="8b762-160">appListType</span><span class="sxs-lookup"><span data-stu-id="8b762-160">appListType</span></span>](../resources/intune-deviceconfig-applisttype.md)|<span data-ttu-id="8b762-161">Lista que se encuentra en la CompliantAppsList.</span><span class="sxs-lookup"><span data-stu-id="8b762-161">List that is in the CompliantAppsList.</span></span> <span data-ttu-id="8b762-162">Los valores posibles son: `none`, `appsInListCompliant` y `appsNotInListCompliant`.</span><span class="sxs-lookup"><span data-stu-id="8b762-162">Possible values are: `none`, `appsInListCompliant`, `appsNotInListCompliant`.</span></span>|
|<span data-ttu-id="8b762-163">emailInDomainSuffixes</span><span class="sxs-lookup"><span data-stu-id="8b762-163">emailInDomainSuffixes</span></span>|<span data-ttu-id="8b762-164">Colección String</span><span class="sxs-lookup"><span data-stu-id="8b762-164">String collection</span></span>|<span data-ttu-id="8b762-165">Una dirección de correo electrónico que carezca de un sufijo que coincida con cualquiera de estas cadenas se considerará fuera de dominio.</span><span class="sxs-lookup"><span data-stu-id="8b762-165">An email address lacking a suffix that matches any of these strings will be considered out-of-domain.</span></span>|
|<span data-ttu-id="8b762-166">passwordBlockSimple</span><span class="sxs-lookup"><span data-stu-id="8b762-166">passwordBlockSimple</span></span>|<span data-ttu-id="8b762-167">Booleano</span><span class="sxs-lookup"><span data-stu-id="8b762-167">Boolean</span></span>|<span data-ttu-id="8b762-168">Bloquear contraseñas sencillas.</span><span class="sxs-lookup"><span data-stu-id="8b762-168">Block simple passwords.</span></span>|
|<span data-ttu-id="8b762-169">passwordExpirationDays</span><span class="sxs-lookup"><span data-stu-id="8b762-169">passwordExpirationDays</span></span>|<span data-ttu-id="8b762-170">Int32</span><span class="sxs-lookup"><span data-stu-id="8b762-170">Int32</span></span>|<span data-ttu-id="8b762-171">Número de días antes de que expire la contraseña.</span><span class="sxs-lookup"><span data-stu-id="8b762-171">Number of days before the password expires.</span></span>|
|<span data-ttu-id="8b762-172">passwordMinimumCharacterSetCount</span><span class="sxs-lookup"><span data-stu-id="8b762-172">passwordMinimumCharacterSetCount</span></span>|<span data-ttu-id="8b762-173">Int32</span><span class="sxs-lookup"><span data-stu-id="8b762-173">Int32</span></span>|<span data-ttu-id="8b762-174">Número de juegos de caracteres que debe contener una contraseña.</span><span class="sxs-lookup"><span data-stu-id="8b762-174">Number of character sets a password must contain.</span></span> <span data-ttu-id="8b762-175">Valores válidos de 0 a 4.</span><span class="sxs-lookup"><span data-stu-id="8b762-175">Valid values 0 to 4</span></span>|
|<span data-ttu-id="8b762-176">passwordMinimumLength</span><span class="sxs-lookup"><span data-stu-id="8b762-176">passwordMinimumLength</span></span>|<span data-ttu-id="8b762-177">Int32</span><span class="sxs-lookup"><span data-stu-id="8b762-177">Int32</span></span>|<span data-ttu-id="8b762-178">Longitud mínima de las contraseñas.</span><span class="sxs-lookup"><span data-stu-id="8b762-178">Minimum length of passwords.</span></span>|
|<span data-ttu-id="8b762-179">passwordMinutesOfInactivityBeforeLock</span><span class="sxs-lookup"><span data-stu-id="8b762-179">passwordMinutesOfInactivityBeforeLock</span></span>|<span data-ttu-id="8b762-180">Int32</span><span class="sxs-lookup"><span data-stu-id="8b762-180">Int32</span></span>|<span data-ttu-id="8b762-181">Minutos de inactividad antes de que sea necesaria una contraseña.</span><span class="sxs-lookup"><span data-stu-id="8b762-181">Minutes of inactivity required before a password is required.</span></span>|
|<span data-ttu-id="8b762-182">passwordMinutesOfInactivityBeforeScreenTimeout</span><span class="sxs-lookup"><span data-stu-id="8b762-182">passwordMinutesOfInactivityBeforeScreenTimeout</span></span>|<span data-ttu-id="8b762-183">Int32</span><span class="sxs-lookup"><span data-stu-id="8b762-183">Int32</span></span>|<span data-ttu-id="8b762-184">Minutos de inactividad que se requieren antes de que se agote el tiempo de espera de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="8b762-184">Minutes of inactivity required before the screen times out.</span></span>|
|<span data-ttu-id="8b762-185">passwordPreviousPasswordBlockCount</span><span class="sxs-lookup"><span data-stu-id="8b762-185">passwordPreviousPasswordBlockCount</span></span>|<span data-ttu-id="8b762-186">Int32</span><span class="sxs-lookup"><span data-stu-id="8b762-186">Int32</span></span>|<span data-ttu-id="8b762-187">Número de contraseñas anteriores que bloquear.</span><span class="sxs-lookup"><span data-stu-id="8b762-187">Number of previous passwords to block.</span></span>|
|<span data-ttu-id="8b762-188">passwordRequiredType</span><span class="sxs-lookup"><span data-stu-id="8b762-188">passwordRequiredType</span></span>|[<span data-ttu-id="8b762-189">requiredPasswordType</span><span class="sxs-lookup"><span data-stu-id="8b762-189">requiredPasswordType</span></span>](../resources/intune-deviceconfig-requiredpasswordtype.md)|<span data-ttu-id="8b762-190">Tipo de contraseña que es necesario.</span><span class="sxs-lookup"><span data-stu-id="8b762-190">Type of password that is required.</span></span> <span data-ttu-id="8b762-191">Los valores posibles son: `deviceDefault`, `alphanumeric` y `numeric`.</span><span class="sxs-lookup"><span data-stu-id="8b762-191">Possible values are: `deviceDefault`, `alphanumeric`, `numeric`.</span></span>|
|<span data-ttu-id="8b762-192">passwordRequired</span><span class="sxs-lookup"><span data-stu-id="8b762-192">passwordRequired</span></span>|<span data-ttu-id="8b762-193">Booleano</span><span class="sxs-lookup"><span data-stu-id="8b762-193">Boolean</span></span>|<span data-ttu-id="8b762-194">Si quiere requerir o no una contraseña.</span><span class="sxs-lookup"><span data-stu-id="8b762-194">Whether or not to require a password.</span></span>|



## <a name="response"></a><span data-ttu-id="8b762-195">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8b762-195">Response</span></span>
<span data-ttu-id="8b762-196">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [macOSGeneralDeviceConfiguration](../resources/intune-deviceconfig-macosgeneraldeviceconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8b762-196">If successful, this method returns a `201 Created` response code and a [macOSGeneralDeviceConfiguration](../resources/intune-deviceconfig-macosgeneraldeviceconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="8b762-197">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="8b762-197">Example</span></span>
### <a name="request"></a><span data-ttu-id="8b762-198">Solicitud</span><span class="sxs-lookup"><span data-stu-id="8b762-198">Request</span></span>
<span data-ttu-id="8b762-199">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="8b762-199">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceManagement/deviceConfigurations
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

### <a name="response"></a><span data-ttu-id="8b762-200">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8b762-200">Response</span></span>
<span data-ttu-id="8b762-p112">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="8b762-p112">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
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


