---
title: Crear androidWorkProfileGeneralDeviceConfiguration
description: Crear un nuevo objeto androidWorkProfileGeneralDeviceConfiguration.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 92cdd51d4bf68aa4607b71ca31c10b35277a06ab
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27912802"
---
# <a name="create-androidworkprofilegeneraldeviceconfiguration"></a><span data-ttu-id="9fdb5-103">Crear androidWorkProfileGeneralDeviceConfiguration</span><span class="sxs-lookup"><span data-stu-id="9fdb5-103">Create androidWorkProfileGeneralDeviceConfiguration</span></span>

> <span data-ttu-id="9fdb5-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="9fdb5-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="9fdb5-105">Crear un nuevo objeto [androidWorkProfileGeneralDeviceConfiguration](../resources/intune-deviceconfig-androidworkprofilegeneraldeviceconfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="9fdb5-105">Create a new [androidWorkProfileGeneralDeviceConfiguration](../resources/intune-deviceconfig-androidworkprofilegeneraldeviceconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="9fdb5-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="9fdb5-106">Prerequisites</span></span>
<span data-ttu-id="9fdb5-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="9fdb5-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="9fdb5-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="9fdb5-109">Permission type</span></span>|<span data-ttu-id="9fdb5-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="9fdb5-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="9fdb5-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="9fdb5-111">Delegated (work or school account)</span></span>|<span data-ttu-id="9fdb5-112">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="9fdb5-112">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="9fdb5-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="9fdb5-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="9fdb5-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9fdb5-114">Not supported.</span></span>|
|<span data-ttu-id="9fdb5-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="9fdb5-115">Application</span></span>|<span data-ttu-id="9fdb5-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9fdb5-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="9fdb5-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="9fdb5-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="9fdb5-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="9fdb5-118">Request headers</span></span>
|<span data-ttu-id="9fdb5-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9fdb5-119">Header</span></span>|<span data-ttu-id="9fdb5-120">Valor</span><span class="sxs-lookup"><span data-stu-id="9fdb5-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="9fdb5-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="9fdb5-121">Authorization</span></span>|<span data-ttu-id="9fdb5-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="9fdb5-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="9fdb5-123">Accept</span><span class="sxs-lookup"><span data-stu-id="9fdb5-123">Accept</span></span>|<span data-ttu-id="9fdb5-124">application/json</span><span class="sxs-lookup"><span data-stu-id="9fdb5-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="9fdb5-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="9fdb5-125">Request body</span></span>
<span data-ttu-id="9fdb5-126">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto androidWorkProfileGeneralDeviceConfiguration.</span><span class="sxs-lookup"><span data-stu-id="9fdb5-126">In the request body, supply a JSON representation for the androidWorkProfileGeneralDeviceConfiguration object.</span></span>

<span data-ttu-id="9fdb5-127">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el androidWorkProfileGeneralDeviceConfiguration.</span><span class="sxs-lookup"><span data-stu-id="9fdb5-127">The following table shows the properties that are required when you create the androidWorkProfileGeneralDeviceConfiguration.</span></span>

|<span data-ttu-id="9fdb5-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="9fdb5-128">Property</span></span>|<span data-ttu-id="9fdb5-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="9fdb5-129">Type</span></span>|<span data-ttu-id="9fdb5-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="9fdb5-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="9fdb5-131">id</span><span class="sxs-lookup"><span data-stu-id="9fdb5-131">id</span></span>|<span data-ttu-id="9fdb5-132">Cadena</span><span class="sxs-lookup"><span data-stu-id="9fdb5-132">String</span></span>|<span data-ttu-id="9fdb5-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="9fdb5-133">Key of the entity.</span></span> <span data-ttu-id="9fdb5-134">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="9fdb5-134">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="9fdb5-135">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="9fdb5-135">lastModifiedDateTime</span></span>|<span data-ttu-id="9fdb5-136">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="9fdb5-136">DateTimeOffset</span></span>|<span data-ttu-id="9fdb5-137">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="9fdb5-137">DateTime the object was last modified.</span></span> <span data-ttu-id="9fdb5-138">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="9fdb5-138">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="9fdb5-139">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="9fdb5-139">createdDateTime</span></span>|<span data-ttu-id="9fdb5-140">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="9fdb5-140">DateTimeOffset</span></span>|<span data-ttu-id="9fdb5-141">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="9fdb5-141">DateTime the object was created.</span></span> <span data-ttu-id="9fdb5-142">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="9fdb5-142">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="9fdb5-143">descripción</span><span class="sxs-lookup"><span data-stu-id="9fdb5-143">description</span></span>|<span data-ttu-id="9fdb5-144">Cadena</span><span class="sxs-lookup"><span data-stu-id="9fdb5-144">String</span></span>|<span data-ttu-id="9fdb5-145">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9fdb5-145">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="9fdb5-146">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="9fdb5-146">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="9fdb5-147">displayName</span><span class="sxs-lookup"><span data-stu-id="9fdb5-147">displayName</span></span>|<span data-ttu-id="9fdb5-148">Cadena</span><span class="sxs-lookup"><span data-stu-id="9fdb5-148">String</span></span>|<span data-ttu-id="9fdb5-149">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9fdb5-149">Admin provided name of the device configuration.</span></span> <span data-ttu-id="9fdb5-150">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="9fdb5-150">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="9fdb5-151">version</span><span class="sxs-lookup"><span data-stu-id="9fdb5-151">version</span></span>|<span data-ttu-id="9fdb5-152">Int32</span><span class="sxs-lookup"><span data-stu-id="9fdb5-152">Int32</span></span>|<span data-ttu-id="9fdb5-153">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9fdb5-153">Version of the device configuration.</span></span> <span data-ttu-id="9fdb5-154">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="9fdb5-154">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="9fdb5-155">passwordBlockFingerprintUnlock</span><span class="sxs-lookup"><span data-stu-id="9fdb5-155">passwordBlockFingerprintUnlock</span></span>|<span data-ttu-id="9fdb5-156">Booleano</span><span class="sxs-lookup"><span data-stu-id="9fdb5-156">Boolean</span></span>|<span data-ttu-id="9fdb5-157">Indica si se va a impedir el desbloqueo por huella dactilar.</span><span class="sxs-lookup"><span data-stu-id="9fdb5-157">Indicates whether or not to block fingerprint unlock.</span></span>|
|<span data-ttu-id="9fdb5-158">passwordBlockTrustAgents</span><span class="sxs-lookup"><span data-stu-id="9fdb5-158">passwordBlockTrustAgents</span></span>|<span data-ttu-id="9fdb5-159">Booleano</span><span class="sxs-lookup"><span data-stu-id="9fdb5-159">Boolean</span></span>|<span data-ttu-id="9fdb5-160">Indica si se van a bloquear Smart Lock y otros agentes de confianza.</span><span class="sxs-lookup"><span data-stu-id="9fdb5-160">Indicates whether or not to block Smart Lock and other trust agents.</span></span>|
|<span data-ttu-id="9fdb5-161">passwordExpirationDays</span><span class="sxs-lookup"><span data-stu-id="9fdb5-161">passwordExpirationDays</span></span>|<span data-ttu-id="9fdb5-162">Int32</span><span class="sxs-lookup"><span data-stu-id="9fdb5-162">Int32</span></span>|<span data-ttu-id="9fdb5-163">Número de días antes de que expire la contraseña.</span><span class="sxs-lookup"><span data-stu-id="9fdb5-163">Number of days before the password expires.</span></span> <span data-ttu-id="9fdb5-164">Valores válidos de 1 a 365</span><span class="sxs-lookup"><span data-stu-id="9fdb5-164">Valid values 1 to 365</span></span>|
|<span data-ttu-id="9fdb5-165">passwordMinimumLength</span><span class="sxs-lookup"><span data-stu-id="9fdb5-165">passwordMinimumLength</span></span>|<span data-ttu-id="9fdb5-166">Int32</span><span class="sxs-lookup"><span data-stu-id="9fdb5-166">Int32</span></span>|<span data-ttu-id="9fdb5-167">Longitud mínima de las contraseñas.</span><span class="sxs-lookup"><span data-stu-id="9fdb5-167">Minimum length of passwords.</span></span> <span data-ttu-id="9fdb5-168">Valores válidos de 4 a 16</span><span class="sxs-lookup"><span data-stu-id="9fdb5-168">Valid values 4 to 16</span></span>|
|<span data-ttu-id="9fdb5-169">passwordMinutesOfInactivityBeforeScreenTimeout</span><span class="sxs-lookup"><span data-stu-id="9fdb5-169">passwordMinutesOfInactivityBeforeScreenTimeout</span></span>|<span data-ttu-id="9fdb5-170">Int32</span><span class="sxs-lookup"><span data-stu-id="9fdb5-170">Int32</span></span>|<span data-ttu-id="9fdb5-171">Minutos de inactividad antes de que se agote el tiempo de espera de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="9fdb5-171">Minutes of inactivity before the screen times out.</span></span>|
|<span data-ttu-id="9fdb5-172">passwordPreviousPasswordBlockCount</span><span class="sxs-lookup"><span data-stu-id="9fdb5-172">passwordPreviousPasswordBlockCount</span></span>|<span data-ttu-id="9fdb5-173">Int32</span><span class="sxs-lookup"><span data-stu-id="9fdb5-173">Int32</span></span>|<span data-ttu-id="9fdb5-174">Número de contraseñas anteriores que bloquear.</span><span class="sxs-lookup"><span data-stu-id="9fdb5-174">Number of previous passwords to block.</span></span> <span data-ttu-id="9fdb5-175">Valores válidos de 0 a 24</span><span class="sxs-lookup"><span data-stu-id="9fdb5-175">Valid values 0 to 24</span></span>|
|<span data-ttu-id="9fdb5-176">passwordSignInFailureCountBeforeFactoryReset</span><span class="sxs-lookup"><span data-stu-id="9fdb5-176">passwordSignInFailureCountBeforeFactoryReset</span></span>|<span data-ttu-id="9fdb5-177">Int32</span><span class="sxs-lookup"><span data-stu-id="9fdb5-177">Int32</span></span>|<span data-ttu-id="9fdb5-178">Número de errores de inicio de sesión permitidos antes del restablecimiento de fábrica.</span><span class="sxs-lookup"><span data-stu-id="9fdb5-178">Number of sign in failures allowed before factory reset.</span></span> <span data-ttu-id="9fdb5-179">Valores válidos de 4 a 11</span><span class="sxs-lookup"><span data-stu-id="9fdb5-179">Valid values 4 to 11</span></span>|
|<span data-ttu-id="9fdb5-180">passwordRequiredType</span><span class="sxs-lookup"><span data-stu-id="9fdb5-180">passwordRequiredType</span></span>|[<span data-ttu-id="9fdb5-181">androidWorkProfileRequiredPasswordType</span><span class="sxs-lookup"><span data-stu-id="9fdb5-181">androidWorkProfileRequiredPasswordType</span></span>](../resources/intune-deviceconfig-androidworkprofilerequiredpasswordtype.md)|<span data-ttu-id="9fdb5-182">Tipo de contraseña que es necesario.</span><span class="sxs-lookup"><span data-stu-id="9fdb5-182">Type of password that is required.</span></span> <span data-ttu-id="9fdb5-183">Los valores posibles son: `deviceDefault`, `lowSecurityBiometric`, `required`, `atLeastNumeric`, `numericComplex`, `atLeastAlphabetic`, `atLeastAlphanumeric` y `alphanumericWithSymbols`.</span><span class="sxs-lookup"><span data-stu-id="9fdb5-183">Possible values are: `deviceDefault`, `lowSecurityBiometric`, `required`, `atLeastNumeric`, `numericComplex`, `atLeastAlphabetic`, `atLeastAlphanumeric`, `alphanumericWithSymbols`.</span></span>|
|<span data-ttu-id="9fdb5-184">workProfileDataSharingType</span><span class="sxs-lookup"><span data-stu-id="9fdb5-184">workProfileDataSharingType</span></span>|[<span data-ttu-id="9fdb5-185">androidWorkProfileCrossProfileDataSharingType</span><span class="sxs-lookup"><span data-stu-id="9fdb5-185">androidWorkProfileCrossProfileDataSharingType</span></span>](../resources/intune-deviceconfig-androidworkprofilecrossprofiledatasharingtype.md)|<span data-ttu-id="9fdb5-186">Tipo de datos de uso compartido está permitido.</span><span class="sxs-lookup"><span data-stu-id="9fdb5-186">Type of data sharing that is allowed.</span></span> <span data-ttu-id="9fdb5-187">Los valores posibles son: `deviceDefault`, `preventAny`, `allowPersonalToWork` y `noRestrictions`.</span><span class="sxs-lookup"><span data-stu-id="9fdb5-187">Possible values are: `deviceDefault`, `preventAny`, `allowPersonalToWork`, `noRestrictions`.</span></span>|
|<span data-ttu-id="9fdb5-188">workProfileBlockNotificationsWhileDeviceLocked</span><span class="sxs-lookup"><span data-stu-id="9fdb5-188">workProfileBlockNotificationsWhileDeviceLocked</span></span>|<span data-ttu-id="9fdb5-189">Booleano</span><span class="sxs-lookup"><span data-stu-id="9fdb5-189">Boolean</span></span>|<span data-ttu-id="9fdb5-190">Indica si se deben bloquear las notificaciones al dispositivo bloqueado.</span><span class="sxs-lookup"><span data-stu-id="9fdb5-190">Indicates whether or not to block notifications while device locked.</span></span>|
|<span data-ttu-id="9fdb5-191">workProfileBlockAddingAccounts</span><span class="sxs-lookup"><span data-stu-id="9fdb5-191">workProfileBlockAddingAccounts</span></span>|<span data-ttu-id="9fdb5-192">Booleano</span><span class="sxs-lookup"><span data-stu-id="9fdb5-192">Boolean</span></span>|<span data-ttu-id="9fdb5-193">Impedir que los usuarios agregar o quitar cuentas en el perfil de trabajo.</span><span class="sxs-lookup"><span data-stu-id="9fdb5-193">Block users from adding/removing accounts in work profile.</span></span>|
|<span data-ttu-id="9fdb5-194">workProfileBluetoothEnableContactSharing</span><span class="sxs-lookup"><span data-stu-id="9fdb5-194">workProfileBluetoothEnableContactSharing</span></span>|<span data-ttu-id="9fdb5-195">Booleano</span><span class="sxs-lookup"><span data-stu-id="9fdb5-195">Boolean</span></span>|<span data-ttu-id="9fdb5-196">Permitir que los dispositivos bluetooth tener acceso a los contactos de la empresa.</span><span class="sxs-lookup"><span data-stu-id="9fdb5-196">Allow bluetooth devices to access enterprise contacts.</span></span>|
|<span data-ttu-id="9fdb5-197">workProfileBlockScreenCapture</span><span class="sxs-lookup"><span data-stu-id="9fdb5-197">workProfileBlockScreenCapture</span></span>|<span data-ttu-id="9fdb5-198">Booleano</span><span class="sxs-lookup"><span data-stu-id="9fdb5-198">Boolean</span></span>|<span data-ttu-id="9fdb5-199">Captura de pantalla de bloque en el perfil de trabajo.</span><span class="sxs-lookup"><span data-stu-id="9fdb5-199">Block screen capture in work profile.</span></span>|
|<span data-ttu-id="9fdb5-200">workProfileBlockCrossProfileCallerId</span><span class="sxs-lookup"><span data-stu-id="9fdb5-200">workProfileBlockCrossProfileCallerId</span></span>|<span data-ttu-id="9fdb5-201">Booleano</span><span class="sxs-lookup"><span data-stu-id="9fdb5-201">Boolean</span></span>|<span data-ttu-id="9fdb5-202">Identificador de autor de la llamada de perfil bloque para mostrar trabajo en perfil personal.</span><span class="sxs-lookup"><span data-stu-id="9fdb5-202">Block display work profile caller ID in personal profile.</span></span>|
|<span data-ttu-id="9fdb5-203">workProfileBlockCamera</span><span class="sxs-lookup"><span data-stu-id="9fdb5-203">workProfileBlockCamera</span></span>|<span data-ttu-id="9fdb5-204">Booleano</span><span class="sxs-lookup"><span data-stu-id="9fdb5-204">Boolean</span></span>|<span data-ttu-id="9fdb5-205">Cámara de perfil de trabajo de bloque.</span><span class="sxs-lookup"><span data-stu-id="9fdb5-205">Block work profile camera.</span></span>|
|<span data-ttu-id="9fdb5-206">workProfileBlockCrossProfileContactsSearch</span><span class="sxs-lookup"><span data-stu-id="9fdb5-206">workProfileBlockCrossProfileContactsSearch</span></span>|<span data-ttu-id="9fdb5-207">Booleano</span><span class="sxs-lookup"><span data-stu-id="9fdb5-207">Boolean</span></span>|<span data-ttu-id="9fdb5-208">Disponibilidad de los contactos del perfil de trabajo bloque en perfil personal.</span><span class="sxs-lookup"><span data-stu-id="9fdb5-208">Block work profile contacts availability in personal profile.</span></span>|
|<span data-ttu-id="9fdb5-209">workProfileBlockCrossProfileCopyPaste</span><span class="sxs-lookup"><span data-stu-id="9fdb5-209">workProfileBlockCrossProfileCopyPaste</span></span>|<span data-ttu-id="9fdb5-210">Booleano</span><span class="sxs-lookup"><span data-stu-id="9fdb5-210">Boolean</span></span>|<span data-ttu-id="9fdb5-211">Valor booleano que indica si la opción no permitir la entre perfil copiado y pegado está habilitado.</span><span class="sxs-lookup"><span data-stu-id="9fdb5-211">Boolean that indicates if the setting disallow cross profile copy/paste is enabled.</span></span>|
|<span data-ttu-id="9fdb5-212">workProfileDefaultAppPermissionPolicy</span><span class="sxs-lookup"><span data-stu-id="9fdb5-212">workProfileDefaultAppPermissionPolicy</span></span>|[<span data-ttu-id="9fdb5-213">androidWorkProfileDefaultAppPermissionPolicyType</span><span class="sxs-lookup"><span data-stu-id="9fdb5-213">androidWorkProfileDefaultAppPermissionPolicyType</span></span>](../resources/intune-deviceconfig-androidworkprofiledefaultapppermissionpolicytype.md)|<span data-ttu-id="9fdb5-214">Tipo de contraseña que es necesario.</span><span class="sxs-lookup"><span data-stu-id="9fdb5-214">Type of password that is required.</span></span> <span data-ttu-id="9fdb5-215">Los valores posibles son: `deviceDefault`, `prompt`, `autoGrant` y `autoDeny`.</span><span class="sxs-lookup"><span data-stu-id="9fdb5-215">Possible values are: `deviceDefault`, `prompt`, `autoGrant`, `autoDeny`.</span></span>|
|<span data-ttu-id="9fdb5-216">workProfilePasswordBlockFingerprintUnlock</span><span class="sxs-lookup"><span data-stu-id="9fdb5-216">workProfilePasswordBlockFingerprintUnlock</span></span>|<span data-ttu-id="9fdb5-217">Booleano</span><span class="sxs-lookup"><span data-stu-id="9fdb5-217">Boolean</span></span>|<span data-ttu-id="9fdb5-218">Indica si se deben bloquear la huella digital de desbloqueo para el perfil de trabajo.</span><span class="sxs-lookup"><span data-stu-id="9fdb5-218">Indicates whether or not to block fingerprint unlock for work profile.</span></span>|
|<span data-ttu-id="9fdb5-219">workProfilePasswordBlockTrustAgents</span><span class="sxs-lookup"><span data-stu-id="9fdb5-219">workProfilePasswordBlockTrustAgents</span></span>|<span data-ttu-id="9fdb5-220">Booleano</span><span class="sxs-lookup"><span data-stu-id="9fdb5-220">Boolean</span></span>|<span data-ttu-id="9fdb5-221">Indica si se deben bloquear bloqueo inteligentes y otros agentes de confianza para el perfil de trabajo.</span><span class="sxs-lookup"><span data-stu-id="9fdb5-221">Indicates whether or not to block Smart Lock and other trust agents for work profile.</span></span>|
|<span data-ttu-id="9fdb5-222">workProfilePasswordExpirationDays</span><span class="sxs-lookup"><span data-stu-id="9fdb5-222">workProfilePasswordExpirationDays</span></span>|<span data-ttu-id="9fdb5-223">Int32</span><span class="sxs-lookup"><span data-stu-id="9fdb5-223">Int32</span></span>|<span data-ttu-id="9fdb5-224">Expira el número de días antes de la contraseña de perfil de trabajo.</span><span class="sxs-lookup"><span data-stu-id="9fdb5-224">Number of days before the work profile password expires.</span></span> <span data-ttu-id="9fdb5-225">Valores válidos de 1 a 365</span><span class="sxs-lookup"><span data-stu-id="9fdb5-225">Valid values 1 to 365</span></span>|
|<span data-ttu-id="9fdb5-226">workProfilePasswordMinimumLength</span><span class="sxs-lookup"><span data-stu-id="9fdb5-226">workProfilePasswordMinimumLength</span></span>|<span data-ttu-id="9fdb5-227">Int32</span><span class="sxs-lookup"><span data-stu-id="9fdb5-227">Int32</span></span>|<span data-ttu-id="9fdb5-228">Longitud mínima de contraseña de perfil de trabajo.</span><span class="sxs-lookup"><span data-stu-id="9fdb5-228">Minimum length of work profile password.</span></span> <span data-ttu-id="9fdb5-229">Valores válidos de 4 a 16</span><span class="sxs-lookup"><span data-stu-id="9fdb5-229">Valid values 4 to 16</span></span>|
|<span data-ttu-id="9fdb5-230">workProfilePasswordMinNumericCharacters</span><span class="sxs-lookup"><span data-stu-id="9fdb5-230">workProfilePasswordMinNumericCharacters</span></span>|<span data-ttu-id="9fdb5-231">Int32</span><span class="sxs-lookup"><span data-stu-id="9fdb5-231">Int32</span></span>|<span data-ttu-id="9fdb5-232">Nº mínimo de caracteres numéricos que requiere en contraseña de perfil de trabajo.</span><span class="sxs-lookup"><span data-stu-id="9fdb5-232">Minimum # of numeric characters required in work profile password.</span></span> <span data-ttu-id="9fdb5-233">Valores válidos de 1 a 10</span><span class="sxs-lookup"><span data-stu-id="9fdb5-233">Valid values 1 to 10</span></span>|
|<span data-ttu-id="9fdb5-234">workProfilePasswordMinNonLetterCharacters</span><span class="sxs-lookup"><span data-stu-id="9fdb5-234">workProfilePasswordMinNonLetterCharacters</span></span>|<span data-ttu-id="9fdb5-235">Int32</span><span class="sxs-lookup"><span data-stu-id="9fdb5-235">Int32</span></span>|<span data-ttu-id="9fdb5-236">Nº mínimo de caracteres que no sea una letra requeridas contraseña de perfil de trabajo.</span><span class="sxs-lookup"><span data-stu-id="9fdb5-236">Minimum # of non-letter characters required in work profile password.</span></span> <span data-ttu-id="9fdb5-237">Valores válidos de 1 a 10</span><span class="sxs-lookup"><span data-stu-id="9fdb5-237">Valid values 1 to 10</span></span>|
|<span data-ttu-id="9fdb5-238">workProfilePasswordMinLetterCharacters</span><span class="sxs-lookup"><span data-stu-id="9fdb5-238">workProfilePasswordMinLetterCharacters</span></span>|<span data-ttu-id="9fdb5-239">Int32</span><span class="sxs-lookup"><span data-stu-id="9fdb5-239">Int32</span></span>|<span data-ttu-id="9fdb5-240">Nº mínimo de caracteres de letra requeridas contraseña de perfil de trabajo.</span><span class="sxs-lookup"><span data-stu-id="9fdb5-240">Minimum # of letter characters required in work profile password.</span></span> <span data-ttu-id="9fdb5-241">Valores válidos de 1 a 10</span><span class="sxs-lookup"><span data-stu-id="9fdb5-241">Valid values 1 to 10</span></span>|
|<span data-ttu-id="9fdb5-242">workProfilePasswordMinLowerCaseCharacters</span><span class="sxs-lookup"><span data-stu-id="9fdb5-242">workProfilePasswordMinLowerCaseCharacters</span></span>|<span data-ttu-id="9fdb5-243">Int32</span><span class="sxs-lookup"><span data-stu-id="9fdb5-243">Int32</span></span>|<span data-ttu-id="9fdb5-244">Nº mínimo de caracteres minúsculas requeridas contraseña de perfil de trabajo.</span><span class="sxs-lookup"><span data-stu-id="9fdb5-244">Minimum # of lower-case characters required in work profile password.</span></span> <span data-ttu-id="9fdb5-245">Valores válidos de 1 a 10</span><span class="sxs-lookup"><span data-stu-id="9fdb5-245">Valid values 1 to 10</span></span>|
|<span data-ttu-id="9fdb5-246">workProfilePasswordMinUpperCaseCharacters</span><span class="sxs-lookup"><span data-stu-id="9fdb5-246">workProfilePasswordMinUpperCaseCharacters</span></span>|<span data-ttu-id="9fdb5-247">Int32</span><span class="sxs-lookup"><span data-stu-id="9fdb5-247">Int32</span></span>|<span data-ttu-id="9fdb5-248">Nº mínimo de caracteres en mayúsculas requeridas contraseña de perfil de trabajo.</span><span class="sxs-lookup"><span data-stu-id="9fdb5-248">Minimum # of upper-case characters required in work profile password.</span></span> <span data-ttu-id="9fdb5-249">Valores válidos de 1 a 10</span><span class="sxs-lookup"><span data-stu-id="9fdb5-249">Valid values 1 to 10</span></span>|
|<span data-ttu-id="9fdb5-250">workProfilePasswordMinSymbolCharacters</span><span class="sxs-lookup"><span data-stu-id="9fdb5-250">workProfilePasswordMinSymbolCharacters</span></span>|<span data-ttu-id="9fdb5-251">Int32</span><span class="sxs-lookup"><span data-stu-id="9fdb5-251">Int32</span></span>|<span data-ttu-id="9fdb5-252">Nº mínimo de símbolos requeridas contraseña de perfil de trabajo.</span><span class="sxs-lookup"><span data-stu-id="9fdb5-252">Minimum # of symbols required in work profile password.</span></span> <span data-ttu-id="9fdb5-253">Valores válidos de 1 a 10</span><span class="sxs-lookup"><span data-stu-id="9fdb5-253">Valid values 1 to 10</span></span>|
|<span data-ttu-id="9fdb5-254">workProfilePasswordMinutesOfInactivityBeforeScreenTimeout</span><span class="sxs-lookup"><span data-stu-id="9fdb5-254">workProfilePasswordMinutesOfInactivityBeforeScreenTimeout</span></span>|<span data-ttu-id="9fdb5-255">Int32</span><span class="sxs-lookup"><span data-stu-id="9fdb5-255">Int32</span></span>|<span data-ttu-id="9fdb5-256">Minutos de inactividad antes de que se agote el tiempo de espera de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="9fdb5-256">Minutes of inactivity before the screen times out.</span></span>|
|<span data-ttu-id="9fdb5-257">workProfilePasswordPreviousPasswordBlockCount</span><span class="sxs-lookup"><span data-stu-id="9fdb5-257">workProfilePasswordPreviousPasswordBlockCount</span></span>|<span data-ttu-id="9fdb5-258">Int32</span><span class="sxs-lookup"><span data-stu-id="9fdb5-258">Int32</span></span>|<span data-ttu-id="9fdb5-259">Número de contraseñas de perfil de trabajo anterior a bloquear.</span><span class="sxs-lookup"><span data-stu-id="9fdb5-259">Number of previous work profile passwords to block.</span></span> <span data-ttu-id="9fdb5-260">Valores válidos de 0 a 24</span><span class="sxs-lookup"><span data-stu-id="9fdb5-260">Valid values 0 to 24</span></span>|
|<span data-ttu-id="9fdb5-261">workProfilePasswordSignInFailureCountBeforeFactoryReset</span><span class="sxs-lookup"><span data-stu-id="9fdb5-261">workProfilePasswordSignInFailureCountBeforeFactoryReset</span></span>|<span data-ttu-id="9fdb5-262">Int32</span><span class="sxs-lookup"><span data-stu-id="9fdb5-262">Int32</span></span>|<span data-ttu-id="9fdb5-263">Número de errores permitidos antes de que se ha quitado el perfil de trabajo y todos los datos corporativos eliminados de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="9fdb5-263">Number of sign in failures allowed before work profile is removed and all corporate data deleted.</span></span> <span data-ttu-id="9fdb5-264">Valores válidos de 4 a 11</span><span class="sxs-lookup"><span data-stu-id="9fdb5-264">Valid values 4 to 11</span></span>|
|<span data-ttu-id="9fdb5-265">workProfilePasswordRequiredType</span><span class="sxs-lookup"><span data-stu-id="9fdb5-265">workProfilePasswordRequiredType</span></span>|[<span data-ttu-id="9fdb5-266">androidWorkProfileRequiredPasswordType</span><span class="sxs-lookup"><span data-stu-id="9fdb5-266">androidWorkProfileRequiredPasswordType</span></span>](../resources/intune-deviceconfig-androidworkprofilerequiredpasswordtype.md)|<span data-ttu-id="9fdb5-267">Tipo de contraseña de perfil de trabajo que se requiere.</span><span class="sxs-lookup"><span data-stu-id="9fdb5-267">Type of work profile password that is required.</span></span> <span data-ttu-id="9fdb5-268">Los valores posibles son: `deviceDefault`, `lowSecurityBiometric`, `required`, `atLeastNumeric`, `numericComplex`, `atLeastAlphabetic`, `atLeastAlphanumeric` y `alphanumericWithSymbols`.</span><span class="sxs-lookup"><span data-stu-id="9fdb5-268">Possible values are: `deviceDefault`, `lowSecurityBiometric`, `required`, `atLeastNumeric`, `numericComplex`, `atLeastAlphabetic`, `atLeastAlphanumeric`, `alphanumericWithSymbols`.</span></span>|
|<span data-ttu-id="9fdb5-269">workProfileRequirePassword</span><span class="sxs-lookup"><span data-stu-id="9fdb5-269">workProfileRequirePassword</span></span>|<span data-ttu-id="9fdb5-270">Booleano</span><span class="sxs-lookup"><span data-stu-id="9fdb5-270">Boolean</span></span>|<span data-ttu-id="9fdb5-271">Se requiere contraseña o no para el perfil de trabajo</span><span class="sxs-lookup"><span data-stu-id="9fdb5-271">Password is required or not for work profile</span></span>|
|<span data-ttu-id="9fdb5-272">securityRequireVerifyApps</span><span class="sxs-lookup"><span data-stu-id="9fdb5-272">securityRequireVerifyApps</span></span>|<span data-ttu-id="9fdb5-273">Booleano</span><span class="sxs-lookup"><span data-stu-id="9fdb5-273">Boolean</span></span>|<span data-ttu-id="9fdb5-274">Requerir que la característica Verificar aplicaciones de Android esté activada.</span><span class="sxs-lookup"><span data-stu-id="9fdb5-274">Require the Android Verify apps feature is turned on.</span></span>|



## <a name="response"></a><span data-ttu-id="9fdb5-275">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9fdb5-275">Response</span></span>
<span data-ttu-id="9fdb5-276">Si tiene éxito, este método devuelve una `201 Created` código de respuesta y un objeto [androidWorkProfileGeneralDeviceConfiguration](../resources/intune-deviceconfig-androidworkprofilegeneraldeviceconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9fdb5-276">If successful, this method returns a `201 Created` response code and a [androidWorkProfileGeneralDeviceConfiguration](../resources/intune-deviceconfig-androidworkprofilegeneraldeviceconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="9fdb5-277">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9fdb5-277">Example</span></span>
### <a name="request"></a><span data-ttu-id="9fdb5-278">Solicitud</span><span class="sxs-lookup"><span data-stu-id="9fdb5-278">Request</span></span>
<span data-ttu-id="9fdb5-279">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="9fdb5-279">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceManagement/deviceConfigurations
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

### <a name="response"></a><span data-ttu-id="9fdb5-280">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9fdb5-280">Response</span></span>
<span data-ttu-id="9fdb5-p126">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="9fdb5-p126">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
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



