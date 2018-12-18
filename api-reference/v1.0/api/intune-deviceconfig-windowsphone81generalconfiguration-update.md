---
title: Actualizar windowsPhone81GeneralConfiguration
description: Actualice las propiedades de un objeto windowsPhone81GeneralConfiguration.
author: tfitzmac
ms.openlocfilehash: bbc7208465f625a105bc793681bfd28f8a4f6082
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27352146"
---
# <a name="update-windowsphone81generalconfiguration"></a><span data-ttu-id="fb5c0-103">Actualizar windowsPhone81GeneralConfiguration</span><span class="sxs-lookup"><span data-stu-id="fb5c0-103">Update windowsPhone81GeneralConfiguration</span></span>

> <span data-ttu-id="fb5c0-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="fb5c0-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="fb5c0-105">Actualice las propiedades de un objeto [windowsPhone81GeneralConfiguration](../resources/intune-deviceconfig-windowsphone81generalconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="fb5c0-105">Update the properties of a [windowsPhone81GeneralConfiguration](../resources/intune-deviceconfig-windowsphone81generalconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="fb5c0-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="fb5c0-106">Prerequisites</span></span>
<span data-ttu-id="fb5c0-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="fb5c0-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="fb5c0-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="fb5c0-109">Permission type</span></span>|<span data-ttu-id="fb5c0-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="fb5c0-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="fb5c0-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="fb5c0-111">Delegated (work or school account)</span></span>|<span data-ttu-id="fb5c0-112">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="fb5c0-112">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="fb5c0-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="fb5c0-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="fb5c0-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="fb5c0-114">Not supported.</span></span>|
|<span data-ttu-id="fb5c0-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="fb5c0-115">Application</span></span>|<span data-ttu-id="fb5c0-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="fb5c0-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="fb5c0-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="fb5c0-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}
```

## <a name="request-headers"></a><span data-ttu-id="fb5c0-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="fb5c0-118">Request headers</span></span>
|<span data-ttu-id="fb5c0-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fb5c0-119">Header</span></span>|<span data-ttu-id="fb5c0-120">Valor</span><span class="sxs-lookup"><span data-stu-id="fb5c0-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="fb5c0-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="fb5c0-121">Authorization</span></span>|<span data-ttu-id="fb5c0-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="fb5c0-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="fb5c0-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="fb5c0-123">Accept</span></span>|<span data-ttu-id="fb5c0-124">application/json</span><span class="sxs-lookup"><span data-stu-id="fb5c0-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="fb5c0-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="fb5c0-125">Request body</span></span>
<span data-ttu-id="fb5c0-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto [windowsPhone81GeneralConfiguration](../resources/intune-deviceconfig-windowsphone81generalconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="fb5c0-126">In the request body, supply a JSON representation for the [windowsPhone81GeneralConfiguration](../resources/intune-deviceconfig-windowsphone81generalconfiguration.md) object.</span></span>

<span data-ttu-id="fb5c0-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [windowsPhone81GeneralConfiguration](../resources/intune-deviceconfig-windowsphone81generalconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="fb5c0-127">The following table shows the properties that are required when you create the [windowsPhone81GeneralConfiguration](../resources/intune-deviceconfig-windowsphone81generalconfiguration.md).</span></span>

|<span data-ttu-id="fb5c0-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="fb5c0-128">Property</span></span>|<span data-ttu-id="fb5c0-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="fb5c0-129">Type</span></span>|<span data-ttu-id="fb5c0-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="fb5c0-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="fb5c0-131">id</span><span class="sxs-lookup"><span data-stu-id="fb5c0-131">id</span></span>|<span data-ttu-id="fb5c0-132">String</span><span class="sxs-lookup"><span data-stu-id="fb5c0-132">String</span></span>|<span data-ttu-id="fb5c0-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="fb5c0-133">Key of the entity.</span></span> <span data-ttu-id="fb5c0-134">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="fb5c0-134">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="fb5c0-135">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="fb5c0-135">lastModifiedDateTime</span></span>|<span data-ttu-id="fb5c0-136">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="fb5c0-136">DateTimeOffset</span></span>|<span data-ttu-id="fb5c0-137">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="fb5c0-137">DateTime the object was last modified.</span></span> <span data-ttu-id="fb5c0-138">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="fb5c0-138">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="fb5c0-139">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="fb5c0-139">createdDateTime</span></span>|<span data-ttu-id="fb5c0-140">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="fb5c0-140">DateTimeOffset</span></span>|<span data-ttu-id="fb5c0-141">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="fb5c0-141">DateTime the object was created.</span></span> <span data-ttu-id="fb5c0-142">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="fb5c0-142">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="fb5c0-143">descripción</span><span class="sxs-lookup"><span data-stu-id="fb5c0-143">description</span></span>|<span data-ttu-id="fb5c0-144">String</span><span class="sxs-lookup"><span data-stu-id="fb5c0-144">String</span></span>|<span data-ttu-id="fb5c0-145">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fb5c0-145">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="fb5c0-146">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="fb5c0-146">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="fb5c0-147">displayName</span><span class="sxs-lookup"><span data-stu-id="fb5c0-147">displayName</span></span>|<span data-ttu-id="fb5c0-148">String</span><span class="sxs-lookup"><span data-stu-id="fb5c0-148">String</span></span>|<span data-ttu-id="fb5c0-149">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fb5c0-149">Admin provided name of the device configuration.</span></span> <span data-ttu-id="fb5c0-150">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="fb5c0-150">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="fb5c0-151">version</span><span class="sxs-lookup"><span data-stu-id="fb5c0-151">version</span></span>|<span data-ttu-id="fb5c0-152">Int32</span><span class="sxs-lookup"><span data-stu-id="fb5c0-152">Int32</span></span>|<span data-ttu-id="fb5c0-153">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fb5c0-153">Version of the device configuration.</span></span> <span data-ttu-id="fb5c0-154">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="fb5c0-154">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="fb5c0-155">applyOnlyToWindowsPhone81</span><span class="sxs-lookup"><span data-stu-id="fb5c0-155">applyOnlyToWindowsPhone81</span></span>|<span data-ttu-id="fb5c0-156">Boolean</span><span class="sxs-lookup"><span data-stu-id="fb5c0-156">Boolean</span></span>|<span data-ttu-id="fb5c0-157">Valor que indica si esta directiva se aplica solo a Windows Phone 8.1.</span><span class="sxs-lookup"><span data-stu-id="fb5c0-157">Value indicating whether this policy only applies to Windows Phone 8.1.</span></span> <span data-ttu-id="fb5c0-158">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="fb5c0-158">This property is read-only.</span></span>|
|<span data-ttu-id="fb5c0-159">appsBlockCopyPaste</span><span class="sxs-lookup"><span data-stu-id="fb5c0-159">appsBlockCopyPaste</span></span>|<span data-ttu-id="fb5c0-160">Booleano</span><span class="sxs-lookup"><span data-stu-id="fb5c0-160">Boolean</span></span>|<span data-ttu-id="fb5c0-161">Indica si se va a impedir cortar y pegar.</span><span class="sxs-lookup"><span data-stu-id="fb5c0-161">Indicates whether or not to block copy paste.</span></span>|
|<span data-ttu-id="fb5c0-162">bluetoothBlocked</span><span class="sxs-lookup"><span data-stu-id="fb5c0-162">bluetoothBlocked</span></span>|<span data-ttu-id="fb5c0-163">Boolean</span><span class="sxs-lookup"><span data-stu-id="fb5c0-163">Boolean</span></span>|<span data-ttu-id="fb5c0-164">Indica si se va a bloquear Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="fb5c0-164">Indicates whether or not to block bluetooth.</span></span>|
|<span data-ttu-id="fb5c0-165">cameraBlocked</span><span class="sxs-lookup"><span data-stu-id="fb5c0-165">cameraBlocked</span></span>|<span data-ttu-id="fb5c0-166">Booleano</span><span class="sxs-lookup"><span data-stu-id="fb5c0-166">Boolean</span></span>|<span data-ttu-id="fb5c0-167">Indica si se va a bloquear la cámara.</span><span class="sxs-lookup"><span data-stu-id="fb5c0-167">Indicates whether or not to block camera.</span></span>|
|<span data-ttu-id="fb5c0-168">cellularBlockWifiTethering</span><span class="sxs-lookup"><span data-stu-id="fb5c0-168">cellularBlockWifiTethering</span></span>|<span data-ttu-id="fb5c0-169">Booleano</span><span class="sxs-lookup"><span data-stu-id="fb5c0-169">Boolean</span></span>|<span data-ttu-id="fb5c0-170">Indica si se va a bloquear el tethering Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="fb5c0-170">Indicates whether or not to block Wi-Fi tethering.</span></span> <span data-ttu-id="fb5c0-171">No tiene impacto si se bloquea el Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="fb5c0-171">Has no impact if Wi-Fi is blocked.</span></span>|
|<span data-ttu-id="fb5c0-172">compliantAppsList</span><span class="sxs-lookup"><span data-stu-id="fb5c0-172">compliantAppsList</span></span>|<span data-ttu-id="fb5c0-173">Colección [appListItem](../resources/intune-deviceconfig-applistitem.md)</span><span class="sxs-lookup"><span data-stu-id="fb5c0-173">[appListItem](../resources/intune-deviceconfig-applistitem.md) collection</span></span>|<span data-ttu-id="fb5c0-174">Lista de aplicaciones en el cumplimiento (sea lista de permitidos o de bloqueados, controlado por CompliantAppListType).</span><span class="sxs-lookup"><span data-stu-id="fb5c0-174">List of apps in the compliance (either allow list or block list, controlled by CompliantAppListType).</span></span> <span data-ttu-id="fb5c0-175">Esta colección puede contener un máximo de 10 000 elementos.</span><span class="sxs-lookup"><span data-stu-id="fb5c0-175">This collection can contain a maximum of 10000 elements.</span></span>|
|<span data-ttu-id="fb5c0-176">compliantAppListType</span><span class="sxs-lookup"><span data-stu-id="fb5c0-176">compliantAppListType</span></span>|[<span data-ttu-id="fb5c0-177">appListType</span><span class="sxs-lookup"><span data-stu-id="fb5c0-177">appListType</span></span>](../resources/intune-deviceconfig-applisttype.md)|<span data-ttu-id="fb5c0-178">Lista que se encuentra en la AppComplianceList.</span><span class="sxs-lookup"><span data-stu-id="fb5c0-178">List that is in the AppComplianceList.</span></span> <span data-ttu-id="fb5c0-179">Los valores posibles son: `none`, `appsInListCompliant` y `appsNotInListCompliant`.</span><span class="sxs-lookup"><span data-stu-id="fb5c0-179">Possible values are: `none`, `appsInListCompliant`, `appsNotInListCompliant`.</span></span>|
|<span data-ttu-id="fb5c0-180">diagnosticDataBlockSubmission</span><span class="sxs-lookup"><span data-stu-id="fb5c0-180">diagnosticDataBlockSubmission</span></span>|<span data-ttu-id="fb5c0-181">Boolean</span><span class="sxs-lookup"><span data-stu-id="fb5c0-181">Boolean</span></span>|<span data-ttu-id="fb5c0-182">Indica si se va a bloquear el envío de datos de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="fb5c0-182">Indicates whether or not to block diagnostic data submission.</span></span>|
|<span data-ttu-id="fb5c0-183">emailBlockAddingAccounts</span><span class="sxs-lookup"><span data-stu-id="fb5c0-183">emailBlockAddingAccounts</span></span>|<span data-ttu-id="fb5c0-184">Boolean</span><span class="sxs-lookup"><span data-stu-id="fb5c0-184">Boolean</span></span>|<span data-ttu-id="fb5c0-185">Indica si se van a bloquear las cuentas de correo electrónico personalizadas.</span><span class="sxs-lookup"><span data-stu-id="fb5c0-185">Indicates whether or not to block custom email accounts.</span></span>|
|<span data-ttu-id="fb5c0-186">locationServicesBlocked</span><span class="sxs-lookup"><span data-stu-id="fb5c0-186">locationServicesBlocked</span></span>|<span data-ttu-id="fb5c0-187">Booleano</span><span class="sxs-lookup"><span data-stu-id="fb5c0-187">Boolean</span></span>|<span data-ttu-id="fb5c0-188">Indica si se van a bloquear los servicios de ubicación.</span><span class="sxs-lookup"><span data-stu-id="fb5c0-188">Indicates whether or not to block location services.</span></span>|
|<span data-ttu-id="fb5c0-189">microsoftAccountBlocked</span><span class="sxs-lookup"><span data-stu-id="fb5c0-189">microsoftAccountBlocked</span></span>|<span data-ttu-id="fb5c0-190">Boolean</span><span class="sxs-lookup"><span data-stu-id="fb5c0-190">Boolean</span></span>|<span data-ttu-id="fb5c0-191">Indica si se va a bloquear el uso de una cuenta de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="fb5c0-191">Indicates whether or not to block using a Microsoft Account.</span></span>|
|<span data-ttu-id="fb5c0-192">nfcBlocked</span><span class="sxs-lookup"><span data-stu-id="fb5c0-192">nfcBlocked</span></span>|<span data-ttu-id="fb5c0-193">Boolean</span><span class="sxs-lookup"><span data-stu-id="fb5c0-193">Boolean</span></span>|<span data-ttu-id="fb5c0-194">Indica si se va a bloquear la transmisión de datos en proximidad.</span><span class="sxs-lookup"><span data-stu-id="fb5c0-194">Indicates whether or not to block Near-Field Communication.</span></span>|
|<span data-ttu-id="fb5c0-195">passwordBlockSimple</span><span class="sxs-lookup"><span data-stu-id="fb5c0-195">passwordBlockSimple</span></span>|<span data-ttu-id="fb5c0-196">Boolean</span><span class="sxs-lookup"><span data-stu-id="fb5c0-196">Boolean</span></span>|<span data-ttu-id="fb5c0-197">Indica si se va a bloquear la sincronización del calendario.</span><span class="sxs-lookup"><span data-stu-id="fb5c0-197">Indicates whether or not to block syncing the calendar.</span></span>|
|<span data-ttu-id="fb5c0-198">passwordExpirationDays</span><span class="sxs-lookup"><span data-stu-id="fb5c0-198">passwordExpirationDays</span></span>|<span data-ttu-id="fb5c0-199">Int32</span><span class="sxs-lookup"><span data-stu-id="fb5c0-199">Int32</span></span>|<span data-ttu-id="fb5c0-200">Número de días antes de que expire la contraseña.</span><span class="sxs-lookup"><span data-stu-id="fb5c0-200">Number of days before the password expires.</span></span>|
|<span data-ttu-id="fb5c0-201">passwordMinimumLength</span><span class="sxs-lookup"><span data-stu-id="fb5c0-201">passwordMinimumLength</span></span>|<span data-ttu-id="fb5c0-202">Int32</span><span class="sxs-lookup"><span data-stu-id="fb5c0-202">Int32</span></span>|<span data-ttu-id="fb5c0-203">Longitud mínima de las contraseñas.</span><span class="sxs-lookup"><span data-stu-id="fb5c0-203">Minimum length of passwords.</span></span>|
|<span data-ttu-id="fb5c0-204">passwordMinutesOfInactivityBeforeScreenTimeout</span><span class="sxs-lookup"><span data-stu-id="fb5c0-204">passwordMinutesOfInactivityBeforeScreenTimeout</span></span>|<span data-ttu-id="fb5c0-205">Int32</span><span class="sxs-lookup"><span data-stu-id="fb5c0-205">Int32</span></span>|<span data-ttu-id="fb5c0-206">Minutos de inactividad antes de que se agote el tiempo de espera de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="fb5c0-206">Minutes of inactivity before screen timeout.</span></span>|
|<span data-ttu-id="fb5c0-207">passwordMinimumCharacterSetCount</span><span class="sxs-lookup"><span data-stu-id="fb5c0-207">passwordMinimumCharacterSetCount</span></span>|<span data-ttu-id="fb5c0-208">Int32</span><span class="sxs-lookup"><span data-stu-id="fb5c0-208">Int32</span></span>|<span data-ttu-id="fb5c0-209">Número de juegos de caracteres que debe contener una contraseña.</span><span class="sxs-lookup"><span data-stu-id="fb5c0-209">Number of character sets a password must contain.</span></span>|
|<span data-ttu-id="fb5c0-210">passwordPreviousPasswordBlockCount</span><span class="sxs-lookup"><span data-stu-id="fb5c0-210">passwordPreviousPasswordBlockCount</span></span>|<span data-ttu-id="fb5c0-211">Int32</span><span class="sxs-lookup"><span data-stu-id="fb5c0-211">Int32</span></span>|<span data-ttu-id="fb5c0-212">Número de contraseñas anteriores que bloquear.</span><span class="sxs-lookup"><span data-stu-id="fb5c0-212">Number of previous passwords to block.</span></span> <span data-ttu-id="fb5c0-213">Valores válidos de 0 a 24</span><span class="sxs-lookup"><span data-stu-id="fb5c0-213">Valid values 0 to 24</span></span>|
|<span data-ttu-id="fb5c0-214">passwordSignInFailureCountBeforeFactoryReset</span><span class="sxs-lookup"><span data-stu-id="fb5c0-214">passwordSignInFailureCountBeforeFactoryReset</span></span>|<span data-ttu-id="fb5c0-215">Int32</span><span class="sxs-lookup"><span data-stu-id="fb5c0-215">Int32</span></span>|<span data-ttu-id="fb5c0-216">Número de errores de inicio de sesión permitidos antes del restablecimiento de fábrica.</span><span class="sxs-lookup"><span data-stu-id="fb5c0-216">Number of sign in failures allowed before factory reset.</span></span>|
|<span data-ttu-id="fb5c0-217">passwordRequiredType</span><span class="sxs-lookup"><span data-stu-id="fb5c0-217">passwordRequiredType</span></span>|[<span data-ttu-id="fb5c0-218">requiredPasswordType</span><span class="sxs-lookup"><span data-stu-id="fb5c0-218">requiredPasswordType</span></span>](../resources/intune-deviceconfig-requiredpasswordtype.md)|<span data-ttu-id="fb5c0-219">Tipo de contraseña que es necesario.</span><span class="sxs-lookup"><span data-stu-id="fb5c0-219">Password type that is required.</span></span> <span data-ttu-id="fb5c0-220">Los valores posibles son: `deviceDefault`, `alphanumeric` y `numeric`.</span><span class="sxs-lookup"><span data-stu-id="fb5c0-220">Possible values are: `deviceDefault`, `alphanumeric`, `numeric`.</span></span>|
|<span data-ttu-id="fb5c0-221">passwordRequired</span><span class="sxs-lookup"><span data-stu-id="fb5c0-221">passwordRequired</span></span>|<span data-ttu-id="fb5c0-222">Boolean</span><span class="sxs-lookup"><span data-stu-id="fb5c0-222">Boolean</span></span>|<span data-ttu-id="fb5c0-223">Indica si se va a requerir una contraseña.</span><span class="sxs-lookup"><span data-stu-id="fb5c0-223">Indicates whether or not to require a password.</span></span>|
|<span data-ttu-id="fb5c0-224">screenCaptureBlocked</span><span class="sxs-lookup"><span data-stu-id="fb5c0-224">screenCaptureBlocked</span></span>|<span data-ttu-id="fb5c0-225">Boolean</span><span class="sxs-lookup"><span data-stu-id="fb5c0-225">Boolean</span></span>|<span data-ttu-id="fb5c0-226">Indica si se van a impedir las capturas de pantalla.</span><span class="sxs-lookup"><span data-stu-id="fb5c0-226">Indicates whether or not to block screenshots.</span></span>|
|<span data-ttu-id="fb5c0-227">storageBlockRemovableStorage</span><span class="sxs-lookup"><span data-stu-id="fb5c0-227">storageBlockRemovableStorage</span></span>|<span data-ttu-id="fb5c0-228">Booleano</span><span class="sxs-lookup"><span data-stu-id="fb5c0-228">Boolean</span></span>|<span data-ttu-id="fb5c0-229">Indica si se va a impedir el almacenamiento extraíble.</span><span class="sxs-lookup"><span data-stu-id="fb5c0-229">Indicates whether or not to block removable storage.</span></span>|
|<span data-ttu-id="fb5c0-230">storageRequireEncryption</span><span class="sxs-lookup"><span data-stu-id="fb5c0-230">storageRequireEncryption</span></span>|<span data-ttu-id="fb5c0-231">Boolean</span><span class="sxs-lookup"><span data-stu-id="fb5c0-231">Boolean</span></span>|<span data-ttu-id="fb5c0-232">Indica si se va a requerir cifrado.</span><span class="sxs-lookup"><span data-stu-id="fb5c0-232">Indicates whether or not to require encryption.</span></span>|
|<span data-ttu-id="fb5c0-233">webBrowserBlocked</span><span class="sxs-lookup"><span data-stu-id="fb5c0-233">webBrowserBlocked</span></span>|<span data-ttu-id="fb5c0-234">Boolean</span><span class="sxs-lookup"><span data-stu-id="fb5c0-234">Boolean</span></span>|<span data-ttu-id="fb5c0-235">Indica si se va a bloquear el explorador web.</span><span class="sxs-lookup"><span data-stu-id="fb5c0-235">Indicates whether or not to block the web browser.</span></span>|
|<span data-ttu-id="fb5c0-236">wifiBlocked</span><span class="sxs-lookup"><span data-stu-id="fb5c0-236">wifiBlocked</span></span>|<span data-ttu-id="fb5c0-237">Booleano</span><span class="sxs-lookup"><span data-stu-id="fb5c0-237">Boolean</span></span>|<span data-ttu-id="fb5c0-238">Indica si se va a bloquear el uso de Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="fb5c0-238">Indicates whether or not to block Wi-Fi.</span></span>|
|<span data-ttu-id="fb5c0-239">wifiBlockAutomaticConnectHotspots</span><span class="sxs-lookup"><span data-stu-id="fb5c0-239">wifiBlockAutomaticConnectHotspots</span></span>|<span data-ttu-id="fb5c0-240">Booleano</span><span class="sxs-lookup"><span data-stu-id="fb5c0-240">Boolean</span></span>|<span data-ttu-id="fb5c0-241">Indica si se va a bloquear automáticamente la conexión a zonas Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="fb5c0-241">Indicates whether or not to block automatically connecting to Wi-Fi hotspots.</span></span> <span data-ttu-id="fb5c0-242">No tiene impacto si se bloquea el Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="fb5c0-242">Has no impact if Wi-Fi is blocked.</span></span>|
|<span data-ttu-id="fb5c0-243">wifiBlockHotspotReporting</span><span class="sxs-lookup"><span data-stu-id="fb5c0-243">wifiBlockHotspotReporting</span></span>|<span data-ttu-id="fb5c0-244">Booleano</span><span class="sxs-lookup"><span data-stu-id="fb5c0-244">Boolean</span></span>|<span data-ttu-id="fb5c0-245">Indica si se van a bloquear los informes de zona Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="fb5c0-245">Indicates whether or not to block Wi-Fi hotspot reporting.</span></span> <span data-ttu-id="fb5c0-246">No tiene impacto si se bloquea el Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="fb5c0-246">Has no impact if Wi-Fi is blocked.</span></span>|
|<span data-ttu-id="fb5c0-247">windowsStoreBlocked</span><span class="sxs-lookup"><span data-stu-id="fb5c0-247">windowsStoreBlocked</span></span>|<span data-ttu-id="fb5c0-248">Boolean</span><span class="sxs-lookup"><span data-stu-id="fb5c0-248">Boolean</span></span>|<span data-ttu-id="fb5c0-249">Indica si se va a bloquear la Tienda Windows.</span><span class="sxs-lookup"><span data-stu-id="fb5c0-249">Indicates whether or not to block the Windows Store.</span></span>|



## <a name="response"></a><span data-ttu-id="fb5c0-250">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fb5c0-250">Response</span></span>
<span data-ttu-id="fb5c0-251">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [windowsPhone81GeneralConfiguration](../resources/intune-deviceconfig-windowsphone81generalconfiguration.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="fb5c0-251">If successful, this method returns a `200 OK` response code and an updated [windowsPhone81GeneralConfiguration](../resources/intune-deviceconfig-windowsphone81generalconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="fb5c0-252">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="fb5c0-252">Example</span></span>
### <a name="request"></a><span data-ttu-id="fb5c0-253">Solicitud</span><span class="sxs-lookup"><span data-stu-id="fb5c0-253">Request</span></span>
<span data-ttu-id="fb5c0-254">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="fb5c0-254">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/deviceConfigurations/{deviceConfigurationId}
Content-type: application/json
Content-length: 1461

{
  "@odata.type": "#microsoft.graph.windowsPhone81GeneralConfiguration",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "applyOnlyToWindowsPhone81": true,
  "appsBlockCopyPaste": true,
  "bluetoothBlocked": true,
  "cameraBlocked": true,
  "cellularBlockWifiTethering": true,
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
  "diagnosticDataBlockSubmission": true,
  "emailBlockAddingAccounts": true,
  "locationServicesBlocked": true,
  "microsoftAccountBlocked": true,
  "nfcBlocked": true,
  "passwordBlockSimple": true,
  "passwordExpirationDays": 6,
  "passwordMinimumLength": 5,
  "passwordMinutesOfInactivityBeforeScreenTimeout": 14,
  "passwordMinimumCharacterSetCount": 0,
  "passwordPreviousPasswordBlockCount": 2,
  "passwordSignInFailureCountBeforeFactoryReset": 12,
  "passwordRequiredType": "alphanumeric",
  "passwordRequired": true,
  "screenCaptureBlocked": true,
  "storageBlockRemovableStorage": true,
  "storageRequireEncryption": true,
  "webBrowserBlocked": true,
  "wifiBlocked": true,
  "wifiBlockAutomaticConnectHotspots": true,
  "wifiBlockHotspotReporting": true,
  "windowsStoreBlocked": true
}
```

### <a name="response"></a><span data-ttu-id="fb5c0-255">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fb5c0-255">Response</span></span>
<span data-ttu-id="fb5c0-p116">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="fb5c0-p116">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1633

{
  "@odata.type": "#microsoft.graph.windowsPhone81GeneralConfiguration",
  "id": "f5e0e34d-e34d-f5e0-4de3-e0f54de3e0f5",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "applyOnlyToWindowsPhone81": true,
  "appsBlockCopyPaste": true,
  "bluetoothBlocked": true,
  "cameraBlocked": true,
  "cellularBlockWifiTethering": true,
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
  "diagnosticDataBlockSubmission": true,
  "emailBlockAddingAccounts": true,
  "locationServicesBlocked": true,
  "microsoftAccountBlocked": true,
  "nfcBlocked": true,
  "passwordBlockSimple": true,
  "passwordExpirationDays": 6,
  "passwordMinimumLength": 5,
  "passwordMinutesOfInactivityBeforeScreenTimeout": 14,
  "passwordMinimumCharacterSetCount": 0,
  "passwordPreviousPasswordBlockCount": 2,
  "passwordSignInFailureCountBeforeFactoryReset": 12,
  "passwordRequiredType": "alphanumeric",
  "passwordRequired": true,
  "screenCaptureBlocked": true,
  "storageBlockRemovableStorage": true,
  "storageRequireEncryption": true,
  "webBrowserBlocked": true,
  "wifiBlocked": true,
  "wifiBlockAutomaticConnectHotspots": true,
  "wifiBlockHotspotReporting": true,
  "windowsStoreBlocked": true
}
```



