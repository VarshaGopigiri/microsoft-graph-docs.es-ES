---
title: Crear windowsPhone81GeneralConfiguration
description: Crear un objeto windowsPhone81GeneralConfiguration.
author: tfitzmac
ms.openlocfilehash: 23e98acd93fc5851df690b7f06ee0bac3a16ce70
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27307087"
---
# <a name="create-windowsphone81generalconfiguration"></a><span data-ttu-id="d309a-103">Crear windowsPhone81GeneralConfiguration</span><span class="sxs-lookup"><span data-stu-id="d309a-103">Create windowsPhone81GeneralConfiguration</span></span>

> <span data-ttu-id="d309a-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="d309a-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="d309a-105">Crear un objeto [windowsPhone81GeneralConfiguration](../resources/intune-deviceconfig-windowsphone81generalconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="d309a-105">Create a new [windowsPhone81GeneralConfiguration](../resources/intune-deviceconfig-windowsphone81generalconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="d309a-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="d309a-106">Prerequisites</span></span>
<span data-ttu-id="d309a-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="d309a-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="d309a-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="d309a-109">Permission type</span></span>|<span data-ttu-id="d309a-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="d309a-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="d309a-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d309a-111">Delegated (work or school account)</span></span>|<span data-ttu-id="d309a-112">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d309a-112">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="d309a-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="d309a-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="d309a-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d309a-114">Not supported.</span></span>|
|<span data-ttu-id="d309a-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d309a-115">Application</span></span>|<span data-ttu-id="d309a-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d309a-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="d309a-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d309a-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="d309a-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d309a-118">Request headers</span></span>
|<span data-ttu-id="d309a-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d309a-119">Header</span></span>|<span data-ttu-id="d309a-120">Valor</span><span class="sxs-lookup"><span data-stu-id="d309a-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="d309a-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="d309a-121">Authorization</span></span>|<span data-ttu-id="d309a-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="d309a-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="d309a-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="d309a-123">Accept</span></span>|<span data-ttu-id="d309a-124">application/json</span><span class="sxs-lookup"><span data-stu-id="d309a-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="d309a-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="d309a-125">Request body</span></span>
<span data-ttu-id="d309a-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto windowsPhone81GeneralConfiguration.</span><span class="sxs-lookup"><span data-stu-id="d309a-126">In the request body, supply a JSON representation for the windowsPhone81GeneralConfiguration object.</span></span>

<span data-ttu-id="d309a-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto windowsPhone81GeneralConfiguration.</span><span class="sxs-lookup"><span data-stu-id="d309a-127">The following table shows the properties that are required when you create the windowsPhone81GeneralConfiguration.</span></span>

|<span data-ttu-id="d309a-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d309a-128">Property</span></span>|<span data-ttu-id="d309a-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="d309a-129">Type</span></span>|<span data-ttu-id="d309a-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="d309a-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="d309a-131">id</span><span class="sxs-lookup"><span data-stu-id="d309a-131">id</span></span>|<span data-ttu-id="d309a-132">String</span><span class="sxs-lookup"><span data-stu-id="d309a-132">String</span></span>|<span data-ttu-id="d309a-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="d309a-133">Key of the entity.</span></span> <span data-ttu-id="d309a-134">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="d309a-134">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="d309a-135">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="d309a-135">lastModifiedDateTime</span></span>|<span data-ttu-id="d309a-136">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="d309a-136">DateTimeOffset</span></span>|<span data-ttu-id="d309a-137">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="d309a-137">DateTime the object was last modified.</span></span> <span data-ttu-id="d309a-138">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="d309a-138">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="d309a-139">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="d309a-139">createdDateTime</span></span>|<span data-ttu-id="d309a-140">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="d309a-140">DateTimeOffset</span></span>|<span data-ttu-id="d309a-141">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="d309a-141">DateTime the object was created.</span></span> <span data-ttu-id="d309a-142">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="d309a-142">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="d309a-143">descripción</span><span class="sxs-lookup"><span data-stu-id="d309a-143">description</span></span>|<span data-ttu-id="d309a-144">String</span><span class="sxs-lookup"><span data-stu-id="d309a-144">String</span></span>|<span data-ttu-id="d309a-145">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d309a-145">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="d309a-146">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="d309a-146">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="d309a-147">displayName</span><span class="sxs-lookup"><span data-stu-id="d309a-147">displayName</span></span>|<span data-ttu-id="d309a-148">String</span><span class="sxs-lookup"><span data-stu-id="d309a-148">String</span></span>|<span data-ttu-id="d309a-149">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d309a-149">Admin provided name of the device configuration.</span></span> <span data-ttu-id="d309a-150">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="d309a-150">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="d309a-151">version</span><span class="sxs-lookup"><span data-stu-id="d309a-151">version</span></span>|<span data-ttu-id="d309a-152">Int32</span><span class="sxs-lookup"><span data-stu-id="d309a-152">Int32</span></span>|<span data-ttu-id="d309a-153">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d309a-153">Version of the device configuration.</span></span> <span data-ttu-id="d309a-154">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="d309a-154">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="d309a-155">applyOnlyToWindowsPhone81</span><span class="sxs-lookup"><span data-stu-id="d309a-155">applyOnlyToWindowsPhone81</span></span>|<span data-ttu-id="d309a-156">Boolean</span><span class="sxs-lookup"><span data-stu-id="d309a-156">Boolean</span></span>|<span data-ttu-id="d309a-157">Valor que indica si esta directiva se aplica solo a Windows Phone 8.1.</span><span class="sxs-lookup"><span data-stu-id="d309a-157">Value indicating whether this policy only applies to Windows Phone 8.1.</span></span> <span data-ttu-id="d309a-158">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="d309a-158">This property is read-only.</span></span>|
|<span data-ttu-id="d309a-159">appsBlockCopyPaste</span><span class="sxs-lookup"><span data-stu-id="d309a-159">appsBlockCopyPaste</span></span>|<span data-ttu-id="d309a-160">Booleano</span><span class="sxs-lookup"><span data-stu-id="d309a-160">Boolean</span></span>|<span data-ttu-id="d309a-161">Indica si se va a impedir cortar y pegar.</span><span class="sxs-lookup"><span data-stu-id="d309a-161">Indicates whether or not to block copy paste.</span></span>|
|<span data-ttu-id="d309a-162">bluetoothBlocked</span><span class="sxs-lookup"><span data-stu-id="d309a-162">bluetoothBlocked</span></span>|<span data-ttu-id="d309a-163">Boolean</span><span class="sxs-lookup"><span data-stu-id="d309a-163">Boolean</span></span>|<span data-ttu-id="d309a-164">Indica si se va a bloquear Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="d309a-164">Indicates whether or not to block bluetooth.</span></span>|
|<span data-ttu-id="d309a-165">cameraBlocked</span><span class="sxs-lookup"><span data-stu-id="d309a-165">cameraBlocked</span></span>|<span data-ttu-id="d309a-166">Booleano</span><span class="sxs-lookup"><span data-stu-id="d309a-166">Boolean</span></span>|<span data-ttu-id="d309a-167">Indica si se va a bloquear la cámara.</span><span class="sxs-lookup"><span data-stu-id="d309a-167">Indicates whether or not to block camera.</span></span>|
|<span data-ttu-id="d309a-168">cellularBlockWifiTethering</span><span class="sxs-lookup"><span data-stu-id="d309a-168">cellularBlockWifiTethering</span></span>|<span data-ttu-id="d309a-169">Booleano</span><span class="sxs-lookup"><span data-stu-id="d309a-169">Boolean</span></span>|<span data-ttu-id="d309a-170">Indica si se va a bloquear el tethering Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="d309a-170">Indicates whether or not to block Wi-Fi tethering.</span></span> <span data-ttu-id="d309a-171">No tiene impacto si se bloquea el Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="d309a-171">Has no impact if Wi-Fi is blocked.</span></span>|
|<span data-ttu-id="d309a-172">compliantAppsList</span><span class="sxs-lookup"><span data-stu-id="d309a-172">compliantAppsList</span></span>|<span data-ttu-id="d309a-173">Colección [appListItem](../resources/intune-deviceconfig-applistitem.md)</span><span class="sxs-lookup"><span data-stu-id="d309a-173">[appListItem](../resources/intune-deviceconfig-applistitem.md) collection</span></span>|<span data-ttu-id="d309a-174">Lista de aplicaciones en el cumplimiento (sea lista de permitidos o de bloqueados, controlado por CompliantAppListType).</span><span class="sxs-lookup"><span data-stu-id="d309a-174">List of apps in the compliance (either allow list or block list, controlled by CompliantAppListType).</span></span> <span data-ttu-id="d309a-175">Esta colección puede contener un máximo de 10 000 elementos.</span><span class="sxs-lookup"><span data-stu-id="d309a-175">This collection can contain a maximum of 10000 elements.</span></span>|
|<span data-ttu-id="d309a-176">compliantAppListType</span><span class="sxs-lookup"><span data-stu-id="d309a-176">compliantAppListType</span></span>|[<span data-ttu-id="d309a-177">appListType</span><span class="sxs-lookup"><span data-stu-id="d309a-177">appListType</span></span>](../resources/intune-deviceconfig-applisttype.md)|<span data-ttu-id="d309a-178">Lista que se encuentra en la AppComplianceList.</span><span class="sxs-lookup"><span data-stu-id="d309a-178">List that is in the AppComplianceList.</span></span> <span data-ttu-id="d309a-179">Los valores posibles son: `none`, `appsInListCompliant` y `appsNotInListCompliant`.</span><span class="sxs-lookup"><span data-stu-id="d309a-179">Possible values are: `none`, `appsInListCompliant`, `appsNotInListCompliant`.</span></span>|
|<span data-ttu-id="d309a-180">diagnosticDataBlockSubmission</span><span class="sxs-lookup"><span data-stu-id="d309a-180">diagnosticDataBlockSubmission</span></span>|<span data-ttu-id="d309a-181">Boolean</span><span class="sxs-lookup"><span data-stu-id="d309a-181">Boolean</span></span>|<span data-ttu-id="d309a-182">Indica si se va a bloquear el envío de datos de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="d309a-182">Indicates whether or not to block diagnostic data submission.</span></span>|
|<span data-ttu-id="d309a-183">emailBlockAddingAccounts</span><span class="sxs-lookup"><span data-stu-id="d309a-183">emailBlockAddingAccounts</span></span>|<span data-ttu-id="d309a-184">Boolean</span><span class="sxs-lookup"><span data-stu-id="d309a-184">Boolean</span></span>|<span data-ttu-id="d309a-185">Indica si se van a bloquear las cuentas de correo electrónico personalizadas.</span><span class="sxs-lookup"><span data-stu-id="d309a-185">Indicates whether or not to block custom email accounts.</span></span>|
|<span data-ttu-id="d309a-186">locationServicesBlocked</span><span class="sxs-lookup"><span data-stu-id="d309a-186">locationServicesBlocked</span></span>|<span data-ttu-id="d309a-187">Booleano</span><span class="sxs-lookup"><span data-stu-id="d309a-187">Boolean</span></span>|<span data-ttu-id="d309a-188">Indica si se van a bloquear los servicios de ubicación.</span><span class="sxs-lookup"><span data-stu-id="d309a-188">Indicates whether or not to block location services.</span></span>|
|<span data-ttu-id="d309a-189">microsoftAccountBlocked</span><span class="sxs-lookup"><span data-stu-id="d309a-189">microsoftAccountBlocked</span></span>|<span data-ttu-id="d309a-190">Boolean</span><span class="sxs-lookup"><span data-stu-id="d309a-190">Boolean</span></span>|<span data-ttu-id="d309a-191">Indica si se va a bloquear el uso de una cuenta de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="d309a-191">Indicates whether or not to block using a Microsoft Account.</span></span>|
|<span data-ttu-id="d309a-192">nfcBlocked</span><span class="sxs-lookup"><span data-stu-id="d309a-192">nfcBlocked</span></span>|<span data-ttu-id="d309a-193">Boolean</span><span class="sxs-lookup"><span data-stu-id="d309a-193">Boolean</span></span>|<span data-ttu-id="d309a-194">Indica si se va a bloquear la transmisión de datos en proximidad.</span><span class="sxs-lookup"><span data-stu-id="d309a-194">Indicates whether or not to block Near-Field Communication.</span></span>|
|<span data-ttu-id="d309a-195">passwordBlockSimple</span><span class="sxs-lookup"><span data-stu-id="d309a-195">passwordBlockSimple</span></span>|<span data-ttu-id="d309a-196">Boolean</span><span class="sxs-lookup"><span data-stu-id="d309a-196">Boolean</span></span>|<span data-ttu-id="d309a-197">Indica si se va a bloquear la sincronización del calendario.</span><span class="sxs-lookup"><span data-stu-id="d309a-197">Indicates whether or not to block syncing the calendar.</span></span>|
|<span data-ttu-id="d309a-198">passwordExpirationDays</span><span class="sxs-lookup"><span data-stu-id="d309a-198">passwordExpirationDays</span></span>|<span data-ttu-id="d309a-199">Int32</span><span class="sxs-lookup"><span data-stu-id="d309a-199">Int32</span></span>|<span data-ttu-id="d309a-200">Número de días antes de que expire la contraseña.</span><span class="sxs-lookup"><span data-stu-id="d309a-200">Number of days before the password expires.</span></span>|
|<span data-ttu-id="d309a-201">passwordMinimumLength</span><span class="sxs-lookup"><span data-stu-id="d309a-201">passwordMinimumLength</span></span>|<span data-ttu-id="d309a-202">Int32</span><span class="sxs-lookup"><span data-stu-id="d309a-202">Int32</span></span>|<span data-ttu-id="d309a-203">Longitud mínima de las contraseñas.</span><span class="sxs-lookup"><span data-stu-id="d309a-203">Minimum length of passwords.</span></span>|
|<span data-ttu-id="d309a-204">passwordMinutesOfInactivityBeforeScreenTimeout</span><span class="sxs-lookup"><span data-stu-id="d309a-204">passwordMinutesOfInactivityBeforeScreenTimeout</span></span>|<span data-ttu-id="d309a-205">Int32</span><span class="sxs-lookup"><span data-stu-id="d309a-205">Int32</span></span>|<span data-ttu-id="d309a-206">Minutos de inactividad antes de que se agote el tiempo de espera de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="d309a-206">Minutes of inactivity before screen timeout.</span></span>|
|<span data-ttu-id="d309a-207">passwordMinimumCharacterSetCount</span><span class="sxs-lookup"><span data-stu-id="d309a-207">passwordMinimumCharacterSetCount</span></span>|<span data-ttu-id="d309a-208">Int32</span><span class="sxs-lookup"><span data-stu-id="d309a-208">Int32</span></span>|<span data-ttu-id="d309a-209">Número de juegos de caracteres que debe contener una contraseña.</span><span class="sxs-lookup"><span data-stu-id="d309a-209">Number of character sets a password must contain.</span></span>|
|<span data-ttu-id="d309a-210">passwordPreviousPasswordBlockCount</span><span class="sxs-lookup"><span data-stu-id="d309a-210">passwordPreviousPasswordBlockCount</span></span>|<span data-ttu-id="d309a-211">Int32</span><span class="sxs-lookup"><span data-stu-id="d309a-211">Int32</span></span>|<span data-ttu-id="d309a-212">Número de contraseñas anteriores que bloquear.</span><span class="sxs-lookup"><span data-stu-id="d309a-212">Number of previous passwords to block.</span></span> <span data-ttu-id="d309a-213">Valores válidos de 0 a 24</span><span class="sxs-lookup"><span data-stu-id="d309a-213">Valid values 0 to 24</span></span>|
|<span data-ttu-id="d309a-214">passwordSignInFailureCountBeforeFactoryReset</span><span class="sxs-lookup"><span data-stu-id="d309a-214">passwordSignInFailureCountBeforeFactoryReset</span></span>|<span data-ttu-id="d309a-215">Int32</span><span class="sxs-lookup"><span data-stu-id="d309a-215">Int32</span></span>|<span data-ttu-id="d309a-216">Número de errores de inicio de sesión permitidos antes del restablecimiento de fábrica.</span><span class="sxs-lookup"><span data-stu-id="d309a-216">Number of sign in failures allowed before factory reset.</span></span>|
|<span data-ttu-id="d309a-217">passwordRequiredType</span><span class="sxs-lookup"><span data-stu-id="d309a-217">passwordRequiredType</span></span>|[<span data-ttu-id="d309a-218">requiredPasswordType</span><span class="sxs-lookup"><span data-stu-id="d309a-218">requiredPasswordType</span></span>](../resources/intune-deviceconfig-requiredpasswordtype.md)|<span data-ttu-id="d309a-219">Tipo de contraseña que es necesario.</span><span class="sxs-lookup"><span data-stu-id="d309a-219">Password type that is required.</span></span> <span data-ttu-id="d309a-220">Los valores posibles son: `deviceDefault`, `alphanumeric` y `numeric`.</span><span class="sxs-lookup"><span data-stu-id="d309a-220">Possible values are: `deviceDefault`, `alphanumeric`, `numeric`.</span></span>|
|<span data-ttu-id="d309a-221">passwordRequired</span><span class="sxs-lookup"><span data-stu-id="d309a-221">passwordRequired</span></span>|<span data-ttu-id="d309a-222">Boolean</span><span class="sxs-lookup"><span data-stu-id="d309a-222">Boolean</span></span>|<span data-ttu-id="d309a-223">Indica si se va a requerir una contraseña.</span><span class="sxs-lookup"><span data-stu-id="d309a-223">Indicates whether or not to require a password.</span></span>|
|<span data-ttu-id="d309a-224">screenCaptureBlocked</span><span class="sxs-lookup"><span data-stu-id="d309a-224">screenCaptureBlocked</span></span>|<span data-ttu-id="d309a-225">Boolean</span><span class="sxs-lookup"><span data-stu-id="d309a-225">Boolean</span></span>|<span data-ttu-id="d309a-226">Indica si se van a impedir las capturas de pantalla.</span><span class="sxs-lookup"><span data-stu-id="d309a-226">Indicates whether or not to block screenshots.</span></span>|
|<span data-ttu-id="d309a-227">storageBlockRemovableStorage</span><span class="sxs-lookup"><span data-stu-id="d309a-227">storageBlockRemovableStorage</span></span>|<span data-ttu-id="d309a-228">Booleano</span><span class="sxs-lookup"><span data-stu-id="d309a-228">Boolean</span></span>|<span data-ttu-id="d309a-229">Indica si se va a impedir el almacenamiento extraíble.</span><span class="sxs-lookup"><span data-stu-id="d309a-229">Indicates whether or not to block removable storage.</span></span>|
|<span data-ttu-id="d309a-230">storageRequireEncryption</span><span class="sxs-lookup"><span data-stu-id="d309a-230">storageRequireEncryption</span></span>|<span data-ttu-id="d309a-231">Boolean</span><span class="sxs-lookup"><span data-stu-id="d309a-231">Boolean</span></span>|<span data-ttu-id="d309a-232">Indica si se va a requerir cifrado.</span><span class="sxs-lookup"><span data-stu-id="d309a-232">Indicates whether or not to require encryption.</span></span>|
|<span data-ttu-id="d309a-233">webBrowserBlocked</span><span class="sxs-lookup"><span data-stu-id="d309a-233">webBrowserBlocked</span></span>|<span data-ttu-id="d309a-234">Boolean</span><span class="sxs-lookup"><span data-stu-id="d309a-234">Boolean</span></span>|<span data-ttu-id="d309a-235">Indica si se va a bloquear el explorador web.</span><span class="sxs-lookup"><span data-stu-id="d309a-235">Indicates whether or not to block the web browser.</span></span>|
|<span data-ttu-id="d309a-236">wifiBlocked</span><span class="sxs-lookup"><span data-stu-id="d309a-236">wifiBlocked</span></span>|<span data-ttu-id="d309a-237">Booleano</span><span class="sxs-lookup"><span data-stu-id="d309a-237">Boolean</span></span>|<span data-ttu-id="d309a-238">Indica si se va a bloquear el uso de Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="d309a-238">Indicates whether or not to block Wi-Fi.</span></span>|
|<span data-ttu-id="d309a-239">wifiBlockAutomaticConnectHotspots</span><span class="sxs-lookup"><span data-stu-id="d309a-239">wifiBlockAutomaticConnectHotspots</span></span>|<span data-ttu-id="d309a-240">Booleano</span><span class="sxs-lookup"><span data-stu-id="d309a-240">Boolean</span></span>|<span data-ttu-id="d309a-241">Indica si se va a bloquear automáticamente la conexión a zonas Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="d309a-241">Indicates whether or not to block automatically connecting to Wi-Fi hotspots.</span></span> <span data-ttu-id="d309a-242">No tiene impacto si se bloquea el Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="d309a-242">Has no impact if Wi-Fi is blocked.</span></span>|
|<span data-ttu-id="d309a-243">wifiBlockHotspotReporting</span><span class="sxs-lookup"><span data-stu-id="d309a-243">wifiBlockHotspotReporting</span></span>|<span data-ttu-id="d309a-244">Booleano</span><span class="sxs-lookup"><span data-stu-id="d309a-244">Boolean</span></span>|<span data-ttu-id="d309a-245">Indica si se van a bloquear los informes de zona Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="d309a-245">Indicates whether or not to block Wi-Fi hotspot reporting.</span></span> <span data-ttu-id="d309a-246">No tiene impacto si se bloquea el Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="d309a-246">Has no impact if Wi-Fi is blocked.</span></span>|
|<span data-ttu-id="d309a-247">windowsStoreBlocked</span><span class="sxs-lookup"><span data-stu-id="d309a-247">windowsStoreBlocked</span></span>|<span data-ttu-id="d309a-248">Boolean</span><span class="sxs-lookup"><span data-stu-id="d309a-248">Boolean</span></span>|<span data-ttu-id="d309a-249">Indica si se va a bloquear la Tienda Windows.</span><span class="sxs-lookup"><span data-stu-id="d309a-249">Indicates whether or not to block the Windows Store.</span></span>|



## <a name="response"></a><span data-ttu-id="d309a-250">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d309a-250">Response</span></span>
<span data-ttu-id="d309a-251">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [windowsPhone81GeneralConfiguration](../resources/intune-deviceconfig-windowsphone81generalconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d309a-251">If successful, this method returns a `201 Created` response code and a [windowsPhone81GeneralConfiguration](../resources/intune-deviceconfig-windowsphone81generalconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="d309a-252">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d309a-252">Example</span></span>
### <a name="request"></a><span data-ttu-id="d309a-253">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d309a-253">Request</span></span>
<span data-ttu-id="d309a-254">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d309a-254">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceManagement/deviceConfigurations
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

### <a name="response"></a><span data-ttu-id="d309a-255">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d309a-255">Response</span></span>
<span data-ttu-id="d309a-p116">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="d309a-p116">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
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



