---
title: Crear sharedPCConfiguration
description: Crear un objeto sharedPCConfiguration.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: acf2dda24f83f577b0dc43f4b340c80b17437734
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27928461"
---
# <a name="create-sharedpcconfiguration"></a><span data-ttu-id="0b0b5-103">Crear sharedPCConfiguration</span><span class="sxs-lookup"><span data-stu-id="0b0b5-103">Create sharedPCConfiguration</span></span>

> <span data-ttu-id="0b0b5-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="0b0b5-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="0b0b5-105">Crear un objeto [sharedPCConfiguration](../resources/intune-deviceconfig-sharedpcconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="0b0b5-105">Create a new [sharedPCConfiguration](../resources/intune-deviceconfig-sharedpcconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="0b0b5-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="0b0b5-106">Prerequisites</span></span>
<span data-ttu-id="0b0b5-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="0b0b5-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="0b0b5-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="0b0b5-109">Permission type</span></span>|<span data-ttu-id="0b0b5-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="0b0b5-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="0b0b5-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="0b0b5-111">Delegated (work or school account)</span></span>|<span data-ttu-id="0b0b5-112">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="0b0b5-112">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="0b0b5-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="0b0b5-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="0b0b5-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="0b0b5-114">Not supported.</span></span>|
|<span data-ttu-id="0b0b5-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="0b0b5-115">Application</span></span>|<span data-ttu-id="0b0b5-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="0b0b5-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="0b0b5-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="0b0b5-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="0b0b5-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="0b0b5-118">Request headers</span></span>
|<span data-ttu-id="0b0b5-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0b0b5-119">Header</span></span>|<span data-ttu-id="0b0b5-120">Valor</span><span class="sxs-lookup"><span data-stu-id="0b0b5-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="0b0b5-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="0b0b5-121">Authorization</span></span>|<span data-ttu-id="0b0b5-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="0b0b5-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="0b0b5-123">Accept</span><span class="sxs-lookup"><span data-stu-id="0b0b5-123">Accept</span></span>|<span data-ttu-id="0b0b5-124">application/json</span><span class="sxs-lookup"><span data-stu-id="0b0b5-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="0b0b5-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="0b0b5-125">Request body</span></span>
<span data-ttu-id="0b0b5-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto sharedPCConfiguration.</span><span class="sxs-lookup"><span data-stu-id="0b0b5-126">In the request body, supply a JSON representation for the sharedPCConfiguration object.</span></span>

<span data-ttu-id="0b0b5-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto sharedPCConfiguration.</span><span class="sxs-lookup"><span data-stu-id="0b0b5-127">The following table shows the properties that are required when you create the sharedPCConfiguration.</span></span>

|<span data-ttu-id="0b0b5-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="0b0b5-128">Property</span></span>|<span data-ttu-id="0b0b5-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="0b0b5-129">Type</span></span>|<span data-ttu-id="0b0b5-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="0b0b5-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="0b0b5-131">id</span><span class="sxs-lookup"><span data-stu-id="0b0b5-131">id</span></span>|<span data-ttu-id="0b0b5-132">Cadena</span><span class="sxs-lookup"><span data-stu-id="0b0b5-132">String</span></span>|<span data-ttu-id="0b0b5-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="0b0b5-133">Key of the entity.</span></span> <span data-ttu-id="0b0b5-134">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="0b0b5-134">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="0b0b5-135">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="0b0b5-135">lastModifiedDateTime</span></span>|<span data-ttu-id="0b0b5-136">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="0b0b5-136">DateTimeOffset</span></span>|<span data-ttu-id="0b0b5-137">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="0b0b5-137">DateTime the object was last modified.</span></span> <span data-ttu-id="0b0b5-138">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="0b0b5-138">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="0b0b5-139">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="0b0b5-139">createdDateTime</span></span>|<span data-ttu-id="0b0b5-140">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="0b0b5-140">DateTimeOffset</span></span>|<span data-ttu-id="0b0b5-141">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="0b0b5-141">DateTime the object was created.</span></span> <span data-ttu-id="0b0b5-142">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="0b0b5-142">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="0b0b5-143">descripción</span><span class="sxs-lookup"><span data-stu-id="0b0b5-143">description</span></span>|<span data-ttu-id="0b0b5-144">Cadena</span><span class="sxs-lookup"><span data-stu-id="0b0b5-144">String</span></span>|<span data-ttu-id="0b0b5-145">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0b0b5-145">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="0b0b5-146">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="0b0b5-146">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="0b0b5-147">displayName</span><span class="sxs-lookup"><span data-stu-id="0b0b5-147">displayName</span></span>|<span data-ttu-id="0b0b5-148">Cadena</span><span class="sxs-lookup"><span data-stu-id="0b0b5-148">String</span></span>|<span data-ttu-id="0b0b5-149">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0b0b5-149">Admin provided name of the device configuration.</span></span> <span data-ttu-id="0b0b5-150">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="0b0b5-150">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="0b0b5-151">version</span><span class="sxs-lookup"><span data-stu-id="0b0b5-151">version</span></span>|<span data-ttu-id="0b0b5-152">Int32</span><span class="sxs-lookup"><span data-stu-id="0b0b5-152">Int32</span></span>|<span data-ttu-id="0b0b5-153">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0b0b5-153">Version of the device configuration.</span></span> <span data-ttu-id="0b0b5-154">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="0b0b5-154">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="0b0b5-155">accountManagerPolicy</span><span class="sxs-lookup"><span data-stu-id="0b0b5-155">accountManagerPolicy</span></span>|[<span data-ttu-id="0b0b5-156">sharedPCAccountManagerPolicy</span><span class="sxs-lookup"><span data-stu-id="0b0b5-156">sharedPCAccountManagerPolicy</span></span>](../resources/intune-deviceconfig-sharedpcaccountmanagerpolicy.md)|<span data-ttu-id="0b0b5-157">Especifica cómo se administran las cuentas en un equipo compartido.</span><span class="sxs-lookup"><span data-stu-id="0b0b5-157">Specifies how accounts are managed on a shared PC.</span></span> <span data-ttu-id="0b0b5-158">Solo se aplica cuando disableAccountManager es False.</span><span class="sxs-lookup"><span data-stu-id="0b0b5-158">Only applies when disableAccountManager is false.</span></span>|
|<span data-ttu-id="0b0b5-159">allowedAccounts</span><span class="sxs-lookup"><span data-stu-id="0b0b5-159">allowedAccounts</span></span>|[<span data-ttu-id="0b0b5-160">sharedPCAllowedAccountType</span><span class="sxs-lookup"><span data-stu-id="0b0b5-160">sharedPCAllowedAccountType</span></span>](../resources/intune-deviceconfig-sharedpcallowedaccounttype.md)|<span data-ttu-id="0b0b5-161">Indica el tipo de cuentas que se pueden usar en un equipo compartido.</span><span class="sxs-lookup"><span data-stu-id="0b0b5-161">Indicates which type of accounts are allowed to use on a shared PC.</span></span> <span data-ttu-id="0b0b5-162">Los valores posibles son: `guest` y `domain`.</span><span class="sxs-lookup"><span data-stu-id="0b0b5-162">Possible values are: `guest`, `domain`.</span></span>|
|<span data-ttu-id="0b0b5-163">allowLocalStorage</span><span class="sxs-lookup"><span data-stu-id="0b0b5-163">allowLocalStorage</span></span>|<span data-ttu-id="0b0b5-164">Booleano</span><span class="sxs-lookup"><span data-stu-id="0b0b5-164">Boolean</span></span>|<span data-ttu-id="0b0b5-165">Especifica si se permite el almacenamiento local en un equipo compartido.</span><span class="sxs-lookup"><span data-stu-id="0b0b5-165">Specifies whether local storage is allowed on a shared PC.</span></span>|
|<span data-ttu-id="0b0b5-166">disableAccountManager</span><span class="sxs-lookup"><span data-stu-id="0b0b5-166">disableAccountManager</span></span>|<span data-ttu-id="0b0b5-167">Booleano</span><span class="sxs-lookup"><span data-stu-id="0b0b5-167">Boolean</span></span>|<span data-ttu-id="0b0b5-168">Deshabilita al administrador de cuentas para el modo de equipo compartido.</span><span class="sxs-lookup"><span data-stu-id="0b0b5-168">Disables the account manager for shared PC mode.</span></span>|
|<span data-ttu-id="0b0b5-169">disableEduPolicies</span><span class="sxs-lookup"><span data-stu-id="0b0b5-169">disableEduPolicies</span></span>|<span data-ttu-id="0b0b5-170">Booleano</span><span class="sxs-lookup"><span data-stu-id="0b0b5-170">Boolean</span></span>|<span data-ttu-id="0b0b5-171">Especifica si se deben deshabilitar las directivas predeterminadas de entorno educativo de equipo compartido.</span><span class="sxs-lookup"><span data-stu-id="0b0b5-171">Specifies whether the default shared PC education environment policies should be disabled.</span></span> <span data-ttu-id="0b0b5-172">Para Windows 10 RS2 y versiones posteriores, se aplicará esta directiva sin establecer Habilitado en true.</span><span class="sxs-lookup"><span data-stu-id="0b0b5-172">For Windows 10 RS2 and later, this policy will be applied without setting Enabled to true.</span></span>|
|<span data-ttu-id="0b0b5-173">disablePowerPolicies</span><span class="sxs-lookup"><span data-stu-id="0b0b5-173">disablePowerPolicies</span></span>|<span data-ttu-id="0b0b5-174">Booleano</span><span class="sxs-lookup"><span data-stu-id="0b0b5-174">Boolean</span></span>|<span data-ttu-id="0b0b5-175">Especifica si se deben deshabilitar las directivas predeterminadas de energía de equipo compartido.</span><span class="sxs-lookup"><span data-stu-id="0b0b5-175">Specifies whether the default shared PC power policies should be disabled.</span></span>|
|<span data-ttu-id="0b0b5-176">disableSignInOnResume</span><span class="sxs-lookup"><span data-stu-id="0b0b5-176">disableSignInOnResume</span></span>|<span data-ttu-id="0b0b5-177">Booleano</span><span class="sxs-lookup"><span data-stu-id="0b0b5-177">Boolean</span></span>|<span data-ttu-id="0b0b5-178">Deshabilita el requisito de iniciar sesión siempre que el dispositivo salga del modo de suspensión.</span><span class="sxs-lookup"><span data-stu-id="0b0b5-178">Disables the requirement to sign in whenever the device wakes up from sleep mode.</span></span>|
|<span data-ttu-id="0b0b5-179">enabled</span><span class="sxs-lookup"><span data-stu-id="0b0b5-179">enabled</span></span>|<span data-ttu-id="0b0b5-180">Booleano</span><span class="sxs-lookup"><span data-stu-id="0b0b5-180">Boolean</span></span>|<span data-ttu-id="0b0b5-181">Habilita el modo de equipo compartido y se aplica a las directivas de equipo compartido.</span><span class="sxs-lookup"><span data-stu-id="0b0b5-181">Enables shared PC mode and applies the shared pc policies.</span></span>|
|<span data-ttu-id="0b0b5-182">idleTimeBeforeSleepInSeconds</span><span class="sxs-lookup"><span data-stu-id="0b0b5-182">idleTimeBeforeSleepInSeconds</span></span>|<span data-ttu-id="0b0b5-183">Int32</span><span class="sxs-lookup"><span data-stu-id="0b0b5-183">Int32</span></span>|<span data-ttu-id="0b0b5-184">Especifica el tiempo en segundos que un dispositivo debe permanecer inactivo antes de que el equipo pase al estado de suspensión.</span><span class="sxs-lookup"><span data-stu-id="0b0b5-184">Specifies the time in seconds that a device must sit idle before the PC goes to sleep.</span></span> <span data-ttu-id="0b0b5-185">Si este valor se establece en 0 impide que se produzca el tiempo de espera en suspensión.</span><span class="sxs-lookup"><span data-stu-id="0b0b5-185">Setting this value to 0 prevents the sleep timeout from occurring.</span></span>|
|<span data-ttu-id="0b0b5-186">kioskAppDisplayName</span><span class="sxs-lookup"><span data-stu-id="0b0b5-186">kioskAppDisplayName</span></span>|<span data-ttu-id="0b0b5-187">Cadena</span><span class="sxs-lookup"><span data-stu-id="0b0b5-187">String</span></span>|<span data-ttu-id="0b0b5-188">Especifica el texto para mostrar de la cuenta que se muestra en la pantalla de inicio de sesión que inicia la aplicación especificada por SetKioskAppUserModelId.</span><span class="sxs-lookup"><span data-stu-id="0b0b5-188">Specifies the display text for the account shown on the sign-in screen which launches the app specified by SetKioskAppUserModelId.</span></span> <span data-ttu-id="0b0b5-189">Solo se aplica cuando se establece KioskAppUserModelId.</span><span class="sxs-lookup"><span data-stu-id="0b0b5-189">Only applies when KioskAppUserModelId is set.</span></span>|
|<span data-ttu-id="0b0b5-190">kioskAppUserModelId</span><span class="sxs-lookup"><span data-stu-id="0b0b5-190">kioskAppUserModelId</span></span>|<span data-ttu-id="0b0b5-191">Cadena</span><span class="sxs-lookup"><span data-stu-id="0b0b5-191">String</span></span>|<span data-ttu-id="0b0b5-192">Especifica el identificador del modelo de usuario de la aplicación correspondiente a la aplicación para que se use con el acceso asignado.</span><span class="sxs-lookup"><span data-stu-id="0b0b5-192">Specifies the application user model ID of the app to use with assigned access.</span></span>|
|<span data-ttu-id="0b0b5-193">maintenanceStartTime</span><span class="sxs-lookup"><span data-stu-id="0b0b5-193">maintenanceStartTime</span></span>|<span data-ttu-id="0b0b5-194">TimeOfDay</span><span class="sxs-lookup"><span data-stu-id="0b0b5-194">TimeOfDay</span></span>|<span data-ttu-id="0b0b5-195">Especifica la hora de inicio diaria de la hora de mantenimiento.</span><span class="sxs-lookup"><span data-stu-id="0b0b5-195">Specifies the daily start time of maintenance hour.</span></span>|



## <a name="response"></a><span data-ttu-id="0b0b5-196">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0b0b5-196">Response</span></span>
<span data-ttu-id="0b0b5-197">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [sharedPCConfiguration](../resources/intune-deviceconfig-sharedpcconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0b0b5-197">If successful, this method returns a `201 Created` response code and a [sharedPCConfiguration](../resources/intune-deviceconfig-sharedpcconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="0b0b5-198">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="0b0b5-198">Example</span></span>
### <a name="request"></a><span data-ttu-id="0b0b5-199">Solicitud</span><span class="sxs-lookup"><span data-stu-id="0b0b5-199">Request</span></span>
<span data-ttu-id="0b0b5-200">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="0b0b5-200">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceManagement/deviceConfigurations
Content-type: application/json
Content-length: 860

{
  "@odata.type": "#microsoft.graph.sharedPCConfiguration",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "accountManagerPolicy": {
    "@odata.type": "microsoft.graph.sharedPCAccountManagerPolicy",
    "accountDeletionPolicy": "diskSpaceThreshold",
    "cacheAccountsAboveDiskFreePercentage": 4,
    "inactiveThresholdDays": 5,
    "removeAccountsBelowDiskFreePercentage": 5
  },
  "allowedAccounts": "domain",
  "allowLocalStorage": true,
  "disableAccountManager": true,
  "disableEduPolicies": true,
  "disablePowerPolicies": true,
  "disableSignInOnResume": true,
  "enabled": true,
  "idleTimeBeforeSleepInSeconds": 12,
  "kioskAppDisplayName": "Kiosk App Display Name value",
  "kioskAppUserModelId": "Kiosk App User Model Id value",
  "maintenanceStartTime": "11:59:24.7240000"
}
```

### <a name="response"></a><span data-ttu-id="0b0b5-201">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0b0b5-201">Response</span></span>
<span data-ttu-id="0b0b5-p113">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="0b0b5-p113">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 1032

{
  "@odata.type": "#microsoft.graph.sharedPCConfiguration",
  "id": "5206be3b-be3b-5206-3bbe-06523bbe0652",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "accountManagerPolicy": {
    "@odata.type": "microsoft.graph.sharedPCAccountManagerPolicy",
    "accountDeletionPolicy": "diskSpaceThreshold",
    "cacheAccountsAboveDiskFreePercentage": 4,
    "inactiveThresholdDays": 5,
    "removeAccountsBelowDiskFreePercentage": 5
  },
  "allowedAccounts": "domain",
  "allowLocalStorage": true,
  "disableAccountManager": true,
  "disableEduPolicies": true,
  "disablePowerPolicies": true,
  "disableSignInOnResume": true,
  "enabled": true,
  "idleTimeBeforeSleepInSeconds": 12,
  "kioskAppDisplayName": "Kiosk App Display Name value",
  "kioskAppUserModelId": "Kiosk App User Model Id value",
  "maintenanceStartTime": "11:59:24.7240000"
}
```



