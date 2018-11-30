---
title: Actualizar androidWorkProfileGeneralDeviceConfiguration
description: Actualizar las propiedades de un objeto androidWorkProfileGeneralDeviceConfiguration.
ms.openlocfilehash: 12584b1569dacb0c3b84862d5f519b40a49ae3e0
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031448"
---
# <a name="update-androidworkprofilegeneraldeviceconfiguration"></a><span data-ttu-id="aa251-103">Actualizar androidWorkProfileGeneralDeviceConfiguration</span><span class="sxs-lookup"><span data-stu-id="aa251-103">Update androidWorkProfileGeneralDeviceConfiguration</span></span>

> <span data-ttu-id="aa251-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="aa251-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="aa251-105">Actualizar las propiedades de un objeto [androidWorkProfileGeneralDeviceConfiguration](../resources/intune-deviceconfig-androidworkprofilegeneraldeviceconfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="aa251-105">Update the properties of a [androidWorkProfileGeneralDeviceConfiguration](../resources/intune-deviceconfig-androidworkprofilegeneraldeviceconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="aa251-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="aa251-106">Prerequisites</span></span>
<span data-ttu-id="aa251-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="aa251-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="aa251-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="aa251-109">Permission type</span></span>|<span data-ttu-id="aa251-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="aa251-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="aa251-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="aa251-111">Delegated (work or school account)</span></span>|<span data-ttu-id="aa251-112">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="aa251-112">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="aa251-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="aa251-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="aa251-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="aa251-114">Not supported.</span></span>|
|<span data-ttu-id="aa251-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="aa251-115">Application</span></span>|<span data-ttu-id="aa251-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="aa251-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="aa251-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="aa251-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}
```

## <a name="request-headers"></a><span data-ttu-id="aa251-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="aa251-118">Request headers</span></span>
|<span data-ttu-id="aa251-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="aa251-119">Header</span></span>|<span data-ttu-id="aa251-120">Valor</span><span class="sxs-lookup"><span data-stu-id="aa251-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="aa251-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="aa251-121">Authorization</span></span>|<span data-ttu-id="aa251-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="aa251-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="aa251-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="aa251-123">Accept</span></span>|<span data-ttu-id="aa251-124">application/json</span><span class="sxs-lookup"><span data-stu-id="aa251-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="aa251-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="aa251-125">Request body</span></span>
<span data-ttu-id="aa251-126">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto [androidWorkProfileGeneralDeviceConfiguration](../resources/intune-deviceconfig-androidworkprofilegeneraldeviceconfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="aa251-126">In the request body, supply a JSON representation for the [androidWorkProfileGeneralDeviceConfiguration](../resources/intune-deviceconfig-androidworkprofilegeneraldeviceconfiguration.md) object.</span></span>

<span data-ttu-id="aa251-127">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el [androidWorkProfileGeneralDeviceConfiguration](../resources/intune-deviceconfig-androidworkprofilegeneraldeviceconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="aa251-127">The following table shows the properties that are required when you create the [androidWorkProfileGeneralDeviceConfiguration](../resources/intune-deviceconfig-androidworkprofilegeneraldeviceconfiguration.md).</span></span>

|<span data-ttu-id="aa251-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="aa251-128">Property</span></span>|<span data-ttu-id="aa251-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="aa251-129">Type</span></span>|<span data-ttu-id="aa251-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="aa251-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="aa251-131">id</span><span class="sxs-lookup"><span data-stu-id="aa251-131">id</span></span>|<span data-ttu-id="aa251-132">String</span><span class="sxs-lookup"><span data-stu-id="aa251-132">String</span></span>|<span data-ttu-id="aa251-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="aa251-133">Key of the entity.</span></span> <span data-ttu-id="aa251-134">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="aa251-134">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="aa251-135">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="aa251-135">lastModifiedDateTime</span></span>|<span data-ttu-id="aa251-136">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="aa251-136">DateTimeOffset</span></span>|<span data-ttu-id="aa251-137">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="aa251-137">DateTime the object was last modified.</span></span> <span data-ttu-id="aa251-138">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="aa251-138">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="aa251-139">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="aa251-139">createdDateTime</span></span>|<span data-ttu-id="aa251-140">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="aa251-140">DateTimeOffset</span></span>|<span data-ttu-id="aa251-141">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="aa251-141">DateTime the object was created.</span></span> <span data-ttu-id="aa251-142">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="aa251-142">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="aa251-143">descripción</span><span class="sxs-lookup"><span data-stu-id="aa251-143">description</span></span>|<span data-ttu-id="aa251-144">String</span><span class="sxs-lookup"><span data-stu-id="aa251-144">String</span></span>|<span data-ttu-id="aa251-145">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="aa251-145">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="aa251-146">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="aa251-146">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="aa251-147">displayName</span><span class="sxs-lookup"><span data-stu-id="aa251-147">displayName</span></span>|<span data-ttu-id="aa251-148">String</span><span class="sxs-lookup"><span data-stu-id="aa251-148">String</span></span>|<span data-ttu-id="aa251-149">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="aa251-149">Admin provided name of the device configuration.</span></span> <span data-ttu-id="aa251-150">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="aa251-150">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="aa251-151">version</span><span class="sxs-lookup"><span data-stu-id="aa251-151">version</span></span>|<span data-ttu-id="aa251-152">Int32</span><span class="sxs-lookup"><span data-stu-id="aa251-152">Int32</span></span>|<span data-ttu-id="aa251-153">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="aa251-153">Version of the device configuration.</span></span> <span data-ttu-id="aa251-154">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="aa251-154">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="aa251-155">passwordBlockFingerprintUnlock</span><span class="sxs-lookup"><span data-stu-id="aa251-155">passwordBlockFingerprintUnlock</span></span>|<span data-ttu-id="aa251-156">Booleano</span><span class="sxs-lookup"><span data-stu-id="aa251-156">Boolean</span></span>|<span data-ttu-id="aa251-157">Indica si se va a impedir el desbloqueo por huella dactilar.</span><span class="sxs-lookup"><span data-stu-id="aa251-157">Indicates whether or not to block fingerprint unlock.</span></span>|
|<span data-ttu-id="aa251-158">passwordBlockTrustAgents</span><span class="sxs-lookup"><span data-stu-id="aa251-158">passwordBlockTrustAgents</span></span>|<span data-ttu-id="aa251-159">Booleano</span><span class="sxs-lookup"><span data-stu-id="aa251-159">Boolean</span></span>|<span data-ttu-id="aa251-160">Indica si se van a bloquear Smart Lock y otros agentes de confianza.</span><span class="sxs-lookup"><span data-stu-id="aa251-160">Indicates whether or not to block Smart Lock and other trust agents.</span></span>|
|<span data-ttu-id="aa251-161">passwordExpirationDays</span><span class="sxs-lookup"><span data-stu-id="aa251-161">passwordExpirationDays</span></span>|<span data-ttu-id="aa251-162">Int32</span><span class="sxs-lookup"><span data-stu-id="aa251-162">Int32</span></span>|<span data-ttu-id="aa251-163">Número de días antes de que expire la contraseña.</span><span class="sxs-lookup"><span data-stu-id="aa251-163">Number of days before the password expires.</span></span> <span data-ttu-id="aa251-164">Valores válidos de 1 a 365</span><span class="sxs-lookup"><span data-stu-id="aa251-164">Valid values 1 to 365</span></span>|
|<span data-ttu-id="aa251-165">passwordMinimumLength</span><span class="sxs-lookup"><span data-stu-id="aa251-165">passwordMinimumLength</span></span>|<span data-ttu-id="aa251-166">Int32</span><span class="sxs-lookup"><span data-stu-id="aa251-166">Int32</span></span>|<span data-ttu-id="aa251-167">Longitud mínima de las contraseñas.</span><span class="sxs-lookup"><span data-stu-id="aa251-167">Minimum length of passwords.</span></span> <span data-ttu-id="aa251-168">Valores válidos de 4 a 16</span><span class="sxs-lookup"><span data-stu-id="aa251-168">Valid values 4 to 16</span></span>|
|<span data-ttu-id="aa251-169">passwordMinutesOfInactivityBeforeScreenTimeout</span><span class="sxs-lookup"><span data-stu-id="aa251-169">passwordMinutesOfInactivityBeforeScreenTimeout</span></span>|<span data-ttu-id="aa251-170">Int32</span><span class="sxs-lookup"><span data-stu-id="aa251-170">Int32</span></span>|<span data-ttu-id="aa251-171">Minutos de inactividad antes de que se agote el tiempo de espera de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="aa251-171">Minutes of inactivity before the screen times out.</span></span>|
|<span data-ttu-id="aa251-172">passwordPreviousPasswordBlockCount</span><span class="sxs-lookup"><span data-stu-id="aa251-172">passwordPreviousPasswordBlockCount</span></span>|<span data-ttu-id="aa251-173">Int32</span><span class="sxs-lookup"><span data-stu-id="aa251-173">Int32</span></span>|<span data-ttu-id="aa251-174">Número de contraseñas anteriores que bloquear.</span><span class="sxs-lookup"><span data-stu-id="aa251-174">Number of previous passwords to block.</span></span> <span data-ttu-id="aa251-175">Valores válidos de 0 a 24</span><span class="sxs-lookup"><span data-stu-id="aa251-175">Valid values 0 to 24</span></span>|
|<span data-ttu-id="aa251-176">passwordSignInFailureCountBeforeFactoryReset</span><span class="sxs-lookup"><span data-stu-id="aa251-176">passwordSignInFailureCountBeforeFactoryReset</span></span>|<span data-ttu-id="aa251-177">Int32</span><span class="sxs-lookup"><span data-stu-id="aa251-177">Int32</span></span>|<span data-ttu-id="aa251-178">Número de errores de inicio de sesión permitidos antes del restablecimiento de fábrica.</span><span class="sxs-lookup"><span data-stu-id="aa251-178">Number of sign in failures allowed before factory reset.</span></span> <span data-ttu-id="aa251-179">Valores válidos de 4 a 11</span><span class="sxs-lookup"><span data-stu-id="aa251-179">Valid values 4 to 11</span></span>|
|<span data-ttu-id="aa251-180">passwordRequiredType</span><span class="sxs-lookup"><span data-stu-id="aa251-180">passwordRequiredType</span></span>|[<span data-ttu-id="aa251-181">androidWorkProfileRequiredPasswordType</span><span class="sxs-lookup"><span data-stu-id="aa251-181">androidWorkProfileRequiredPasswordType</span></span>](../resources/intune-deviceconfig-androidworkprofilerequiredpasswordtype.md)|<span data-ttu-id="aa251-182">Tipo de contraseña que es necesario.</span><span class="sxs-lookup"><span data-stu-id="aa251-182">Type of password that is required.</span></span> <span data-ttu-id="aa251-183">Los valores posibles son: `deviceDefault`, `lowSecurityBiometric`, `required`, `atLeastNumeric`, `numericComplex`, `atLeastAlphabetic`, `atLeastAlphanumeric` y `alphanumericWithSymbols`.</span><span class="sxs-lookup"><span data-stu-id="aa251-183">Possible values are: `deviceDefault`, `lowSecurityBiometric`, `required`, `atLeastNumeric`, `numericComplex`, `atLeastAlphabetic`, `atLeastAlphanumeric`, `alphanumericWithSymbols`.</span></span>|
|<span data-ttu-id="aa251-184">workProfileDataSharingType</span><span class="sxs-lookup"><span data-stu-id="aa251-184">workProfileDataSharingType</span></span>|[<span data-ttu-id="aa251-185">androidWorkProfileCrossProfileDataSharingType</span><span class="sxs-lookup"><span data-stu-id="aa251-185">androidWorkProfileCrossProfileDataSharingType</span></span>](../resources/intune-deviceconfig-androidworkprofilecrossprofiledatasharingtype.md)|<span data-ttu-id="aa251-186">Tipo de datos de uso compartido está permitido.</span><span class="sxs-lookup"><span data-stu-id="aa251-186">Type of data sharing that is allowed.</span></span> <span data-ttu-id="aa251-187">Los valores posibles son: `deviceDefault`, `preventAny`, `allowPersonalToWork` y `noRestrictions`.</span><span class="sxs-lookup"><span data-stu-id="aa251-187">Possible values are: `deviceDefault`, `preventAny`, `allowPersonalToWork`, `noRestrictions`.</span></span>|
|<span data-ttu-id="aa251-188">workProfileBlockNotificationsWhileDeviceLocked</span><span class="sxs-lookup"><span data-stu-id="aa251-188">workProfileBlockNotificationsWhileDeviceLocked</span></span>|<span data-ttu-id="aa251-189">Booleano</span><span class="sxs-lookup"><span data-stu-id="aa251-189">Boolean</span></span>|<span data-ttu-id="aa251-190">Indica si se deben bloquear las notificaciones al dispositivo bloqueado.</span><span class="sxs-lookup"><span data-stu-id="aa251-190">Indicates whether or not to block notifications while device locked.</span></span>|
|<span data-ttu-id="aa251-191">workProfileBlockAddingAccounts</span><span class="sxs-lookup"><span data-stu-id="aa251-191">workProfileBlockAddingAccounts</span></span>|<span data-ttu-id="aa251-192">Booleano</span><span class="sxs-lookup"><span data-stu-id="aa251-192">Boolean</span></span>|<span data-ttu-id="aa251-193">Impedir que los usuarios agregar o quitar cuentas en el perfil de trabajo.</span><span class="sxs-lookup"><span data-stu-id="aa251-193">Block users from adding/removing accounts in work profile.</span></span>|
|<span data-ttu-id="aa251-194">workProfileBluetoothEnableContactSharing</span><span class="sxs-lookup"><span data-stu-id="aa251-194">workProfileBluetoothEnableContactSharing</span></span>|<span data-ttu-id="aa251-195">Booleano</span><span class="sxs-lookup"><span data-stu-id="aa251-195">Boolean</span></span>|<span data-ttu-id="aa251-196">Permitir que los dispositivos bluetooth tener acceso a los contactos de la empresa.</span><span class="sxs-lookup"><span data-stu-id="aa251-196">Allow bluetooth devices to access enterprise contacts.</span></span>|
|<span data-ttu-id="aa251-197">workProfileBlockScreenCapture</span><span class="sxs-lookup"><span data-stu-id="aa251-197">workProfileBlockScreenCapture</span></span>|<span data-ttu-id="aa251-198">Booleano</span><span class="sxs-lookup"><span data-stu-id="aa251-198">Boolean</span></span>|<span data-ttu-id="aa251-199">Captura de pantalla de bloque en el perfil de trabajo.</span><span class="sxs-lookup"><span data-stu-id="aa251-199">Block screen capture in work profile.</span></span>|
|<span data-ttu-id="aa251-200">workProfileBlockCrossProfileCallerId</span><span class="sxs-lookup"><span data-stu-id="aa251-200">workProfileBlockCrossProfileCallerId</span></span>|<span data-ttu-id="aa251-201">Booleano</span><span class="sxs-lookup"><span data-stu-id="aa251-201">Boolean</span></span>|<span data-ttu-id="aa251-202">Identificador de autor de la llamada de perfil bloque para mostrar trabajo en perfil personal.</span><span class="sxs-lookup"><span data-stu-id="aa251-202">Block display work profile caller ID in personal profile.</span></span>|
|<span data-ttu-id="aa251-203">workProfileBlockCamera</span><span class="sxs-lookup"><span data-stu-id="aa251-203">workProfileBlockCamera</span></span>|<span data-ttu-id="aa251-204">Booleano</span><span class="sxs-lookup"><span data-stu-id="aa251-204">Boolean</span></span>|<span data-ttu-id="aa251-205">Cámara de perfil de trabajo de bloque.</span><span class="sxs-lookup"><span data-stu-id="aa251-205">Block work profile camera.</span></span>|
|<span data-ttu-id="aa251-206">workProfileBlockCrossProfileContactsSearch</span><span class="sxs-lookup"><span data-stu-id="aa251-206">workProfileBlockCrossProfileContactsSearch</span></span>|<span data-ttu-id="aa251-207">Booleano</span><span class="sxs-lookup"><span data-stu-id="aa251-207">Boolean</span></span>|<span data-ttu-id="aa251-208">Disponibilidad de los contactos del perfil de trabajo bloque en perfil personal.</span><span class="sxs-lookup"><span data-stu-id="aa251-208">Block work profile contacts availability in personal profile.</span></span>|
|<span data-ttu-id="aa251-209">workProfileBlockCrossProfileCopyPaste</span><span class="sxs-lookup"><span data-stu-id="aa251-209">workProfileBlockCrossProfileCopyPaste</span></span>|<span data-ttu-id="aa251-210">Booleano</span><span class="sxs-lookup"><span data-stu-id="aa251-210">Boolean</span></span>|<span data-ttu-id="aa251-211">Valor booleano que indica si la opción no permitir la entre perfil copiado y pegado está habilitado.</span><span class="sxs-lookup"><span data-stu-id="aa251-211">Boolean that indicates if the setting disallow cross profile copy/paste is enabled.</span></span>|
|<span data-ttu-id="aa251-212">workProfileDefaultAppPermissionPolicy</span><span class="sxs-lookup"><span data-stu-id="aa251-212">workProfileDefaultAppPermissionPolicy</span></span>|[<span data-ttu-id="aa251-213">androidWorkProfileDefaultAppPermissionPolicyType</span><span class="sxs-lookup"><span data-stu-id="aa251-213">androidWorkProfileDefaultAppPermissionPolicyType</span></span>](../resources/intune-deviceconfig-androidworkprofiledefaultapppermissionpolicytype.md)|<span data-ttu-id="aa251-214">Tipo de contraseña que es necesario.</span><span class="sxs-lookup"><span data-stu-id="aa251-214">Type of password that is required.</span></span> <span data-ttu-id="aa251-215">Los valores posibles son: `deviceDefault`, `prompt`, `autoGrant` y `autoDeny`.</span><span class="sxs-lookup"><span data-stu-id="aa251-215">Possible values are: `deviceDefault`, `prompt`, `autoGrant`, `autoDeny`.</span></span>|
|<span data-ttu-id="aa251-216">workProfilePasswordBlockFingerprintUnlock</span><span class="sxs-lookup"><span data-stu-id="aa251-216">workProfilePasswordBlockFingerprintUnlock</span></span>|<span data-ttu-id="aa251-217">Booleano</span><span class="sxs-lookup"><span data-stu-id="aa251-217">Boolean</span></span>|<span data-ttu-id="aa251-218">Indica si se deben bloquear la huella digital de desbloqueo para el perfil de trabajo.</span><span class="sxs-lookup"><span data-stu-id="aa251-218">Indicates whether or not to block fingerprint unlock for work profile.</span></span>|
|<span data-ttu-id="aa251-219">workProfilePasswordBlockTrustAgents</span><span class="sxs-lookup"><span data-stu-id="aa251-219">workProfilePasswordBlockTrustAgents</span></span>|<span data-ttu-id="aa251-220">Booleano</span><span class="sxs-lookup"><span data-stu-id="aa251-220">Boolean</span></span>|<span data-ttu-id="aa251-221">Indica si se deben bloquear bloqueo inteligentes y otros agentes de confianza para el perfil de trabajo.</span><span class="sxs-lookup"><span data-stu-id="aa251-221">Indicates whether or not to block Smart Lock and other trust agents for work profile.</span></span>|
|<span data-ttu-id="aa251-222">workProfilePasswordExpirationDays</span><span class="sxs-lookup"><span data-stu-id="aa251-222">workProfilePasswordExpirationDays</span></span>|<span data-ttu-id="aa251-223">Int32</span><span class="sxs-lookup"><span data-stu-id="aa251-223">Int32</span></span>|<span data-ttu-id="aa251-224">Expira el número de días antes de la contraseña de perfil de trabajo.</span><span class="sxs-lookup"><span data-stu-id="aa251-224">Number of days before the work profile password expires.</span></span> <span data-ttu-id="aa251-225">Valores válidos de 1 a 365</span><span class="sxs-lookup"><span data-stu-id="aa251-225">Valid values 1 to 365</span></span>|
|<span data-ttu-id="aa251-226">workProfilePasswordMinimumLength</span><span class="sxs-lookup"><span data-stu-id="aa251-226">workProfilePasswordMinimumLength</span></span>|<span data-ttu-id="aa251-227">Int32</span><span class="sxs-lookup"><span data-stu-id="aa251-227">Int32</span></span>|<span data-ttu-id="aa251-228">Longitud mínima de contraseña de perfil de trabajo.</span><span class="sxs-lookup"><span data-stu-id="aa251-228">Minimum length of work profile password.</span></span> <span data-ttu-id="aa251-229">Valores válidos de 4 a 16</span><span class="sxs-lookup"><span data-stu-id="aa251-229">Valid values 4 to 16</span></span>|
|<span data-ttu-id="aa251-230">workProfilePasswordMinNumericCharacters</span><span class="sxs-lookup"><span data-stu-id="aa251-230">workProfilePasswordMinNumericCharacters</span></span>|<span data-ttu-id="aa251-231">Int32</span><span class="sxs-lookup"><span data-stu-id="aa251-231">Int32</span></span>|<span data-ttu-id="aa251-232">Nº mínimo de caracteres numéricos que requiere en contraseña de perfil de trabajo.</span><span class="sxs-lookup"><span data-stu-id="aa251-232">Minimum # of numeric characters required in work profile password.</span></span> <span data-ttu-id="aa251-233">Valores válidos de 1 a 10</span><span class="sxs-lookup"><span data-stu-id="aa251-233">Valid values 1 to 10</span></span>|
|<span data-ttu-id="aa251-234">workProfilePasswordMinNonLetterCharacters</span><span class="sxs-lookup"><span data-stu-id="aa251-234">workProfilePasswordMinNonLetterCharacters</span></span>|<span data-ttu-id="aa251-235">Int32</span><span class="sxs-lookup"><span data-stu-id="aa251-235">Int32</span></span>|<span data-ttu-id="aa251-236">Nº mínimo de caracteres que no sea una letra requeridas contraseña de perfil de trabajo.</span><span class="sxs-lookup"><span data-stu-id="aa251-236">Minimum # of non-letter characters required in work profile password.</span></span> <span data-ttu-id="aa251-237">Valores válidos de 1 a 10</span><span class="sxs-lookup"><span data-stu-id="aa251-237">Valid values 1 to 10</span></span>|
|<span data-ttu-id="aa251-238">workProfilePasswordMinLetterCharacters</span><span class="sxs-lookup"><span data-stu-id="aa251-238">workProfilePasswordMinLetterCharacters</span></span>|<span data-ttu-id="aa251-239">Int32</span><span class="sxs-lookup"><span data-stu-id="aa251-239">Int32</span></span>|<span data-ttu-id="aa251-240">Nº mínimo de caracteres de letra requeridas contraseña de perfil de trabajo.</span><span class="sxs-lookup"><span data-stu-id="aa251-240">Minimum # of letter characters required in work profile password.</span></span> <span data-ttu-id="aa251-241">Valores válidos de 1 a 10</span><span class="sxs-lookup"><span data-stu-id="aa251-241">Valid values 1 to 10</span></span>|
|<span data-ttu-id="aa251-242">workProfilePasswordMinLowerCaseCharacters</span><span class="sxs-lookup"><span data-stu-id="aa251-242">workProfilePasswordMinLowerCaseCharacters</span></span>|<span data-ttu-id="aa251-243">Int32</span><span class="sxs-lookup"><span data-stu-id="aa251-243">Int32</span></span>|<span data-ttu-id="aa251-244">Nº mínimo de caracteres minúsculas requeridas contraseña de perfil de trabajo.</span><span class="sxs-lookup"><span data-stu-id="aa251-244">Minimum # of lower-case characters required in work profile password.</span></span> <span data-ttu-id="aa251-245">Valores válidos de 1 a 10</span><span class="sxs-lookup"><span data-stu-id="aa251-245">Valid values 1 to 10</span></span>|
|<span data-ttu-id="aa251-246">workProfilePasswordMinUpperCaseCharacters</span><span class="sxs-lookup"><span data-stu-id="aa251-246">workProfilePasswordMinUpperCaseCharacters</span></span>|<span data-ttu-id="aa251-247">Int32</span><span class="sxs-lookup"><span data-stu-id="aa251-247">Int32</span></span>|<span data-ttu-id="aa251-248">Nº mínimo de caracteres en mayúsculas requeridas contraseña de perfil de trabajo.</span><span class="sxs-lookup"><span data-stu-id="aa251-248">Minimum # of upper-case characters required in work profile password.</span></span> <span data-ttu-id="aa251-249">Valores válidos de 1 a 10</span><span class="sxs-lookup"><span data-stu-id="aa251-249">Valid values 1 to 10</span></span>|
|<span data-ttu-id="aa251-250">workProfilePasswordMinSymbolCharacters</span><span class="sxs-lookup"><span data-stu-id="aa251-250">workProfilePasswordMinSymbolCharacters</span></span>|<span data-ttu-id="aa251-251">Int32</span><span class="sxs-lookup"><span data-stu-id="aa251-251">Int32</span></span>|<span data-ttu-id="aa251-252">Nº mínimo de símbolos requeridas contraseña de perfil de trabajo.</span><span class="sxs-lookup"><span data-stu-id="aa251-252">Minimum # of symbols required in work profile password.</span></span> <span data-ttu-id="aa251-253">Valores válidos de 1 a 10</span><span class="sxs-lookup"><span data-stu-id="aa251-253">Valid values 1 to 10</span></span>|
|<span data-ttu-id="aa251-254">workProfilePasswordMinutesOfInactivityBeforeScreenTimeout</span><span class="sxs-lookup"><span data-stu-id="aa251-254">workProfilePasswordMinutesOfInactivityBeforeScreenTimeout</span></span>|<span data-ttu-id="aa251-255">Int32</span><span class="sxs-lookup"><span data-stu-id="aa251-255">Int32</span></span>|<span data-ttu-id="aa251-256">Minutos de inactividad antes de que se agote el tiempo de espera de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="aa251-256">Minutes of inactivity before the screen times out.</span></span>|
|<span data-ttu-id="aa251-257">workProfilePasswordPreviousPasswordBlockCount</span><span class="sxs-lookup"><span data-stu-id="aa251-257">workProfilePasswordPreviousPasswordBlockCount</span></span>|<span data-ttu-id="aa251-258">Int32</span><span class="sxs-lookup"><span data-stu-id="aa251-258">Int32</span></span>|<span data-ttu-id="aa251-259">Número de contraseñas de perfil de trabajo anterior a bloquear.</span><span class="sxs-lookup"><span data-stu-id="aa251-259">Number of previous work profile passwords to block.</span></span> <span data-ttu-id="aa251-260">Valores válidos de 0 a 24</span><span class="sxs-lookup"><span data-stu-id="aa251-260">Valid values 0 to 24</span></span>|
|<span data-ttu-id="aa251-261">workProfilePasswordSignInFailureCountBeforeFactoryReset</span><span class="sxs-lookup"><span data-stu-id="aa251-261">workProfilePasswordSignInFailureCountBeforeFactoryReset</span></span>|<span data-ttu-id="aa251-262">Int32</span><span class="sxs-lookup"><span data-stu-id="aa251-262">Int32</span></span>|<span data-ttu-id="aa251-263">Número de errores permitidos antes de que se ha quitado el perfil de trabajo y todos los datos corporativos eliminados de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="aa251-263">Number of sign in failures allowed before work profile is removed and all corporate data deleted.</span></span> <span data-ttu-id="aa251-264">Valores válidos de 4 a 11</span><span class="sxs-lookup"><span data-stu-id="aa251-264">Valid values 4 to 11</span></span>|
|<span data-ttu-id="aa251-265">workProfilePasswordRequiredType</span><span class="sxs-lookup"><span data-stu-id="aa251-265">workProfilePasswordRequiredType</span></span>|[<span data-ttu-id="aa251-266">androidWorkProfileRequiredPasswordType</span><span class="sxs-lookup"><span data-stu-id="aa251-266">androidWorkProfileRequiredPasswordType</span></span>](../resources/intune-deviceconfig-androidworkprofilerequiredpasswordtype.md)|<span data-ttu-id="aa251-267">Tipo de contraseña de perfil de trabajo que se requiere.</span><span class="sxs-lookup"><span data-stu-id="aa251-267">Type of work profile password that is required.</span></span> <span data-ttu-id="aa251-268">Los valores posibles son: `deviceDefault`, `lowSecurityBiometric`, `required`, `atLeastNumeric`, `numericComplex`, `atLeastAlphabetic`, `atLeastAlphanumeric` y `alphanumericWithSymbols`.</span><span class="sxs-lookup"><span data-stu-id="aa251-268">Possible values are: `deviceDefault`, `lowSecurityBiometric`, `required`, `atLeastNumeric`, `numericComplex`, `atLeastAlphabetic`, `atLeastAlphanumeric`, `alphanumericWithSymbols`.</span></span>|
|<span data-ttu-id="aa251-269">workProfileRequirePassword</span><span class="sxs-lookup"><span data-stu-id="aa251-269">workProfileRequirePassword</span></span>|<span data-ttu-id="aa251-270">Booleano</span><span class="sxs-lookup"><span data-stu-id="aa251-270">Boolean</span></span>|<span data-ttu-id="aa251-271">Se requiere contraseña o no para el perfil de trabajo</span><span class="sxs-lookup"><span data-stu-id="aa251-271">Password is required or not for work profile</span></span>|
|<span data-ttu-id="aa251-272">securityRequireVerifyApps</span><span class="sxs-lookup"><span data-stu-id="aa251-272">securityRequireVerifyApps</span></span>|<span data-ttu-id="aa251-273">Booleano</span><span class="sxs-lookup"><span data-stu-id="aa251-273">Boolean</span></span>|<span data-ttu-id="aa251-274">Requerir que la característica Verificar aplicaciones de Android esté activada.</span><span class="sxs-lookup"><span data-stu-id="aa251-274">Require the Android Verify apps feature is turned on.</span></span>|



## <a name="response"></a><span data-ttu-id="aa251-275">Respuesta</span><span class="sxs-lookup"><span data-stu-id="aa251-275">Response</span></span>
<span data-ttu-id="aa251-276">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto actualizado [androidWorkProfileGeneralDeviceConfiguration](../resources/intune-deviceconfig-androidworkprofilegeneraldeviceconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="aa251-276">If successful, this method returns a `200 OK` response code and an updated [androidWorkProfileGeneralDeviceConfiguration](../resources/intune-deviceconfig-androidworkprofilegeneraldeviceconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="aa251-277">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="aa251-277">Example</span></span>
### <a name="request"></a><span data-ttu-id="aa251-278">Solicitud</span><span class="sxs-lookup"><span data-stu-id="aa251-278">Request</span></span>
<span data-ttu-id="aa251-279">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="aa251-279">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/deviceConfigurations/{deviceConfigurationId}
Content-type: application/json
Content-length: 1831

{
  "@odata.type": "#microsoft.graph.androidWorkProfileGeneralDeviceConfiguration",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "passwordBlockFingerprintUnlock": true,
  "passwordBlockTrustAgents": true,
  "passwordExpirationDays": 6,
  "passwordMinimumLength": 5,
  "passwordMinutesOfInactivityBeforeScreenTimeout": 14,
  "passwordPreviousPasswordBlockCount": 2,
  "passwordSignInFailureCountBeforeFactoryReset": 12,
  "passwordRequiredType": "lowSecurityBiometric",
  "workProfileDataSharingType": "preventAny",
  "workProfileBlockNotificationsWhileDeviceLocked": true,
  "workProfileBlockAddingAccounts": true,
  "workProfileBluetoothEnableContactSharing": true,
  "workProfileBlockScreenCapture": true,
  "workProfileBlockCrossProfileCallerId": true,
  "workProfileBlockCamera": true,
  "workProfileBlockCrossProfileContactsSearch": true,
  "workProfileBlockCrossProfileCopyPaste": true,
  "workProfileDefaultAppPermissionPolicy": "prompt",
  "workProfilePasswordBlockFingerprintUnlock": true,
  "workProfilePasswordBlockTrustAgents": true,
  "workProfilePasswordExpirationDays": 1,
  "workProfilePasswordMinimumLength": 0,
  "workProfilePasswordMinNumericCharacters": 7,
  "workProfilePasswordMinNonLetterCharacters": 9,
  "workProfilePasswordMinLetterCharacters": 6,
  "workProfilePasswordMinLowerCaseCharacters": 9,
  "workProfilePasswordMinUpperCaseCharacters": 9,
  "workProfilePasswordMinSymbolCharacters": 6,
  "workProfilePasswordMinutesOfInactivityBeforeScreenTimeout": 9,
  "workProfilePasswordPreviousPasswordBlockCount": 13,
  "workProfilePasswordSignInFailureCountBeforeFactoryReset": 7,
  "workProfilePasswordRequiredType": "lowSecurityBiometric",
  "workProfileRequirePassword": true,
  "securityRequireVerifyApps": true
}
```

### <a name="response"></a><span data-ttu-id="aa251-280">Respuesta</span><span class="sxs-lookup"><span data-stu-id="aa251-280">Response</span></span>
<span data-ttu-id="aa251-p126">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="aa251-p126">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 2003

{
  "@odata.type": "#microsoft.graph.androidWorkProfileGeneralDeviceConfiguration",
  "id": "6decda7e-da7e-6dec-7eda-ec6d7edaec6d",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "passwordBlockFingerprintUnlock": true,
  "passwordBlockTrustAgents": true,
  "passwordExpirationDays": 6,
  "passwordMinimumLength": 5,
  "passwordMinutesOfInactivityBeforeScreenTimeout": 14,
  "passwordPreviousPasswordBlockCount": 2,
  "passwordSignInFailureCountBeforeFactoryReset": 12,
  "passwordRequiredType": "lowSecurityBiometric",
  "workProfileDataSharingType": "preventAny",
  "workProfileBlockNotificationsWhileDeviceLocked": true,
  "workProfileBlockAddingAccounts": true,
  "workProfileBluetoothEnableContactSharing": true,
  "workProfileBlockScreenCapture": true,
  "workProfileBlockCrossProfileCallerId": true,
  "workProfileBlockCamera": true,
  "workProfileBlockCrossProfileContactsSearch": true,
  "workProfileBlockCrossProfileCopyPaste": true,
  "workProfileDefaultAppPermissionPolicy": "prompt",
  "workProfilePasswordBlockFingerprintUnlock": true,
  "workProfilePasswordBlockTrustAgents": true,
  "workProfilePasswordExpirationDays": 1,
  "workProfilePasswordMinimumLength": 0,
  "workProfilePasswordMinNumericCharacters": 7,
  "workProfilePasswordMinNonLetterCharacters": 9,
  "workProfilePasswordMinLetterCharacters": 6,
  "workProfilePasswordMinLowerCaseCharacters": 9,
  "workProfilePasswordMinUpperCaseCharacters": 9,
  "workProfilePasswordMinSymbolCharacters": 6,
  "workProfilePasswordMinutesOfInactivityBeforeScreenTimeout": 9,
  "workProfilePasswordPreviousPasswordBlockCount": 13,
  "workProfilePasswordSignInFailureCountBeforeFactoryReset": 7,
  "workProfilePasswordRequiredType": "lowSecurityBiometric",
  "workProfileRequirePassword": true,
  "securityRequireVerifyApps": true
}
```



