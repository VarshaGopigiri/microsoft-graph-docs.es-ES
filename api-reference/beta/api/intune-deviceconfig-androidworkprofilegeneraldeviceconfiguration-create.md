---
title: Crear androidWorkProfileGeneralDeviceConfiguration
description: Crear un nuevo objeto androidWorkProfileGeneralDeviceConfiguration.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 7e44d3cbac87346034cb9c6c83054f4a048182a4
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27881252"
---
# <a name="create-androidworkprofilegeneraldeviceconfiguration"></a><span data-ttu-id="474f7-103">Crear androidWorkProfileGeneralDeviceConfiguration</span><span class="sxs-lookup"><span data-stu-id="474f7-103">Create androidWorkProfileGeneralDeviceConfiguration</span></span>

> <span data-ttu-id="474f7-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="474f7-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="474f7-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="474f7-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="474f7-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="474f7-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="474f7-107">Crear un nuevo objeto [androidWorkProfileGeneralDeviceConfiguration](../resources/intune-deviceconfig-androidworkprofilegeneraldeviceconfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="474f7-107">Create a new [androidWorkProfileGeneralDeviceConfiguration](../resources/intune-deviceconfig-androidworkprofilegeneraldeviceconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="474f7-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="474f7-108">Prerequisites</span></span>
<span data-ttu-id="474f7-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="474f7-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="474f7-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="474f7-111">Permission type</span></span>|<span data-ttu-id="474f7-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="474f7-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="474f7-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="474f7-113">Delegated (work or school account)</span></span>|<span data-ttu-id="474f7-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="474f7-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="474f7-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="474f7-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="474f7-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="474f7-116">Not supported.</span></span>|
|<span data-ttu-id="474f7-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="474f7-117">Application</span></span>|<span data-ttu-id="474f7-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="474f7-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="474f7-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="474f7-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceConfigurations
POST /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsDomainJoinConfiguration/networkAccessConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="474f7-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="474f7-120">Request headers</span></span>
|<span data-ttu-id="474f7-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="474f7-121">Header</span></span>|<span data-ttu-id="474f7-122">Valor</span><span class="sxs-lookup"><span data-stu-id="474f7-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="474f7-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="474f7-123">Authorization</span></span>|<span data-ttu-id="474f7-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="474f7-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="474f7-125">Accept</span><span class="sxs-lookup"><span data-stu-id="474f7-125">Accept</span></span>|<span data-ttu-id="474f7-126">application/json</span><span class="sxs-lookup"><span data-stu-id="474f7-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="474f7-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="474f7-127">Request body</span></span>
<span data-ttu-id="474f7-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto androidWorkProfileGeneralDeviceConfiguration.</span><span class="sxs-lookup"><span data-stu-id="474f7-128">In the request body, supply a JSON representation for the androidWorkProfileGeneralDeviceConfiguration object.</span></span>

<span data-ttu-id="474f7-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el androidWorkProfileGeneralDeviceConfiguration.</span><span class="sxs-lookup"><span data-stu-id="474f7-129">The following table shows the properties that are required when you create the androidWorkProfileGeneralDeviceConfiguration.</span></span>

|<span data-ttu-id="474f7-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="474f7-130">Property</span></span>|<span data-ttu-id="474f7-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="474f7-131">Type</span></span>|<span data-ttu-id="474f7-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="474f7-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="474f7-133">id</span><span class="sxs-lookup"><span data-stu-id="474f7-133">id</span></span>|<span data-ttu-id="474f7-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="474f7-134">String</span></span>|<span data-ttu-id="474f7-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="474f7-135">Key of the entity.</span></span> <span data-ttu-id="474f7-136">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="474f7-136">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="474f7-137">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="474f7-137">lastModifiedDateTime</span></span>|<span data-ttu-id="474f7-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="474f7-138">DateTimeOffset</span></span>|<span data-ttu-id="474f7-139">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="474f7-139">DateTime the object was last modified.</span></span> <span data-ttu-id="474f7-140">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="474f7-140">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="474f7-141">roleScopeTagIds</span><span class="sxs-lookup"><span data-stu-id="474f7-141">roleScopeTagIds</span></span>|<span data-ttu-id="474f7-142">Colección String</span><span class="sxs-lookup"><span data-stu-id="474f7-142">String collection</span></span>|<span data-ttu-id="474f7-143">Lista de etiquetas de ámbito para esta instancia de entidad.</span><span class="sxs-lookup"><span data-stu-id="474f7-143">List of Scope Tags for this Entity instance.</span></span> <span data-ttu-id="474f7-144">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="474f7-144">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="474f7-145">supportsScopeTags</span><span class="sxs-lookup"><span data-stu-id="474f7-145">supportsScopeTags</span></span>|<span data-ttu-id="474f7-146">Booleano</span><span class="sxs-lookup"><span data-stu-id="474f7-146">Boolean</span></span>|<span data-ttu-id="474f7-147">Indica si la configuración del dispositivo subyacente admite la asignación de etiquetas de ámbito.</span><span class="sxs-lookup"><span data-stu-id="474f7-147">Indicates whether or not the underlying Device Configuration supports the assignment of scope tags.</span></span> <span data-ttu-id="474f7-148">No se permite la asignación a la propiedad ScopeTags cuando este valor es false y entidades no estará visibles para los usuarios con ámbito.</span><span class="sxs-lookup"><span data-stu-id="474f7-148">Assigning to the ScopeTags property is not allowed when this value is false and entities will not be visible to scoped users.</span></span> <span data-ttu-id="474f7-149">Esto se produce para las directivas de heredado creadas en Silverlight y se puede resolver por eliminar y volver a crear la directiva en el Portal de Azure.</span><span class="sxs-lookup"><span data-stu-id="474f7-149">This occurs for Legacy policies created in Silverlight and can be resolved by deleting and recreating the policy in the Azure Portal.</span></span> <span data-ttu-id="474f7-150">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="474f7-150">This property is read-only.</span></span> <span data-ttu-id="474f7-151">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="474f7-151">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="474f7-152">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="474f7-152">createdDateTime</span></span>|<span data-ttu-id="474f7-153">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="474f7-153">DateTimeOffset</span></span>|<span data-ttu-id="474f7-154">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="474f7-154">DateTime the object was created.</span></span> <span data-ttu-id="474f7-155">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="474f7-155">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="474f7-156">descripción</span><span class="sxs-lookup"><span data-stu-id="474f7-156">description</span></span>|<span data-ttu-id="474f7-157">Cadena</span><span class="sxs-lookup"><span data-stu-id="474f7-157">String</span></span>|<span data-ttu-id="474f7-158">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="474f7-158">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="474f7-159">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="474f7-159">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="474f7-160">displayName</span><span class="sxs-lookup"><span data-stu-id="474f7-160">displayName</span></span>|<span data-ttu-id="474f7-161">Cadena</span><span class="sxs-lookup"><span data-stu-id="474f7-161">String</span></span>|<span data-ttu-id="474f7-162">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="474f7-162">Admin provided name of the device configuration.</span></span> <span data-ttu-id="474f7-163">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="474f7-163">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="474f7-164">version</span><span class="sxs-lookup"><span data-stu-id="474f7-164">version</span></span>|<span data-ttu-id="474f7-165">Int32</span><span class="sxs-lookup"><span data-stu-id="474f7-165">Int32</span></span>|<span data-ttu-id="474f7-166">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="474f7-166">Version of the device configuration.</span></span> <span data-ttu-id="474f7-167">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="474f7-167">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="474f7-168">passwordBlockFingerprintUnlock</span><span class="sxs-lookup"><span data-stu-id="474f7-168">passwordBlockFingerprintUnlock</span></span>|<span data-ttu-id="474f7-169">Booleano</span><span class="sxs-lookup"><span data-stu-id="474f7-169">Boolean</span></span>|<span data-ttu-id="474f7-170">Indica si se va a impedir el desbloqueo por huella dactilar.</span><span class="sxs-lookup"><span data-stu-id="474f7-170">Indicates whether or not to block fingerprint unlock.</span></span>|
|<span data-ttu-id="474f7-171">passwordBlockTrustAgents</span><span class="sxs-lookup"><span data-stu-id="474f7-171">passwordBlockTrustAgents</span></span>|<span data-ttu-id="474f7-172">Booleano</span><span class="sxs-lookup"><span data-stu-id="474f7-172">Boolean</span></span>|<span data-ttu-id="474f7-173">Indica si se van a bloquear Smart Lock y otros agentes de confianza.</span><span class="sxs-lookup"><span data-stu-id="474f7-173">Indicates whether or not to block Smart Lock and other trust agents.</span></span>|
|<span data-ttu-id="474f7-174">passwordExpirationDays</span><span class="sxs-lookup"><span data-stu-id="474f7-174">passwordExpirationDays</span></span>|<span data-ttu-id="474f7-175">Int32</span><span class="sxs-lookup"><span data-stu-id="474f7-175">Int32</span></span>|<span data-ttu-id="474f7-176">Número de días antes de que expire la contraseña.</span><span class="sxs-lookup"><span data-stu-id="474f7-176">Number of days before the password expires.</span></span> <span data-ttu-id="474f7-177">Valores válidos de 1 a 365</span><span class="sxs-lookup"><span data-stu-id="474f7-177">Valid values 1 to 365</span></span>|
|<span data-ttu-id="474f7-178">passwordMinimumLength</span><span class="sxs-lookup"><span data-stu-id="474f7-178">passwordMinimumLength</span></span>|<span data-ttu-id="474f7-179">Int32</span><span class="sxs-lookup"><span data-stu-id="474f7-179">Int32</span></span>|<span data-ttu-id="474f7-180">Longitud mínima de las contraseñas.</span><span class="sxs-lookup"><span data-stu-id="474f7-180">Minimum length of passwords.</span></span> <span data-ttu-id="474f7-181">Valores válidos de 4 a 16</span><span class="sxs-lookup"><span data-stu-id="474f7-181">Valid values 4 to 16</span></span>|
|<span data-ttu-id="474f7-182">passwordMinutesOfInactivityBeforeScreenTimeout</span><span class="sxs-lookup"><span data-stu-id="474f7-182">passwordMinutesOfInactivityBeforeScreenTimeout</span></span>|<span data-ttu-id="474f7-183">Int32</span><span class="sxs-lookup"><span data-stu-id="474f7-183">Int32</span></span>|<span data-ttu-id="474f7-184">Minutos de inactividad antes de que se agote el tiempo de espera de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="474f7-184">Minutes of inactivity before the screen times out.</span></span>|
|<span data-ttu-id="474f7-185">passwordPreviousPasswordBlockCount</span><span class="sxs-lookup"><span data-stu-id="474f7-185">passwordPreviousPasswordBlockCount</span></span>|<span data-ttu-id="474f7-186">Int32</span><span class="sxs-lookup"><span data-stu-id="474f7-186">Int32</span></span>|<span data-ttu-id="474f7-187">Número de contraseñas anteriores que bloquear.</span><span class="sxs-lookup"><span data-stu-id="474f7-187">Number of previous passwords to block.</span></span> <span data-ttu-id="474f7-188">Valores válidos de 0 a 24</span><span class="sxs-lookup"><span data-stu-id="474f7-188">Valid values 0 to 24</span></span>|
|<span data-ttu-id="474f7-189">passwordSignInFailureCountBeforeFactoryReset</span><span class="sxs-lookup"><span data-stu-id="474f7-189">passwordSignInFailureCountBeforeFactoryReset</span></span>|<span data-ttu-id="474f7-190">Int32</span><span class="sxs-lookup"><span data-stu-id="474f7-190">Int32</span></span>|<span data-ttu-id="474f7-191">Número de errores de inicio de sesión permitidos antes del restablecimiento de fábrica.</span><span class="sxs-lookup"><span data-stu-id="474f7-191">Number of sign in failures allowed before factory reset.</span></span> <span data-ttu-id="474f7-192">Valores válidos de 4 a 11</span><span class="sxs-lookup"><span data-stu-id="474f7-192">Valid values 4 to 11</span></span>|
|<span data-ttu-id="474f7-193">passwordRequiredType</span><span class="sxs-lookup"><span data-stu-id="474f7-193">passwordRequiredType</span></span>|[<span data-ttu-id="474f7-194">androidWorkProfileRequiredPasswordType</span><span class="sxs-lookup"><span data-stu-id="474f7-194">androidWorkProfileRequiredPasswordType</span></span>](../resources/intune-deviceconfig-androidworkprofilerequiredpasswordtype.md)|<span data-ttu-id="474f7-195">Tipo de contraseña que es necesario.</span><span class="sxs-lookup"><span data-stu-id="474f7-195">Type of password that is required.</span></span> <span data-ttu-id="474f7-196">Los valores posibles son: `deviceDefault`, `lowSecurityBiometric`, `required`, `atLeastNumeric`, `numericComplex`, `atLeastAlphabetic`, `atLeastAlphanumeric` y `alphanumericWithSymbols`.</span><span class="sxs-lookup"><span data-stu-id="474f7-196">Possible values are: `deviceDefault`, `lowSecurityBiometric`, `required`, `atLeastNumeric`, `numericComplex`, `atLeastAlphabetic`, `atLeastAlphanumeric`, `alphanumericWithSymbols`.</span></span>|
|<span data-ttu-id="474f7-197">workProfileDataSharingType</span><span class="sxs-lookup"><span data-stu-id="474f7-197">workProfileDataSharingType</span></span>|[<span data-ttu-id="474f7-198">androidWorkProfileCrossProfileDataSharingType</span><span class="sxs-lookup"><span data-stu-id="474f7-198">androidWorkProfileCrossProfileDataSharingType</span></span>](../resources/intune-deviceconfig-androidworkprofilecrossprofiledatasharingtype.md)|<span data-ttu-id="474f7-199">Tipo de datos de uso compartido está permitido.</span><span class="sxs-lookup"><span data-stu-id="474f7-199">Type of data sharing that is allowed.</span></span> <span data-ttu-id="474f7-200">Los valores posibles son: `deviceDefault`, `preventAny`, `allowPersonalToWork` y `noRestrictions`.</span><span class="sxs-lookup"><span data-stu-id="474f7-200">Possible values are: `deviceDefault`, `preventAny`, `allowPersonalToWork`, `noRestrictions`.</span></span>|
|<span data-ttu-id="474f7-201">workProfileBlockNotificationsWhileDeviceLocked</span><span class="sxs-lookup"><span data-stu-id="474f7-201">workProfileBlockNotificationsWhileDeviceLocked</span></span>|<span data-ttu-id="474f7-202">Booleano</span><span class="sxs-lookup"><span data-stu-id="474f7-202">Boolean</span></span>|<span data-ttu-id="474f7-203">Indica si se deben bloquear las notificaciones al dispositivo bloqueado.</span><span class="sxs-lookup"><span data-stu-id="474f7-203">Indicates whether or not to block notifications while device locked.</span></span>|
|<span data-ttu-id="474f7-204">workProfileBlockAddingAccounts</span><span class="sxs-lookup"><span data-stu-id="474f7-204">workProfileBlockAddingAccounts</span></span>|<span data-ttu-id="474f7-205">Booleano</span><span class="sxs-lookup"><span data-stu-id="474f7-205">Boolean</span></span>|<span data-ttu-id="474f7-206">Impedir que los usuarios agregar o quitar cuentas en el perfil de trabajo.</span><span class="sxs-lookup"><span data-stu-id="474f7-206">Block users from adding/removing accounts in work profile.</span></span>|
|<span data-ttu-id="474f7-207">workProfileBluetoothEnableContactSharing</span><span class="sxs-lookup"><span data-stu-id="474f7-207">workProfileBluetoothEnableContactSharing</span></span>|<span data-ttu-id="474f7-208">Booleano</span><span class="sxs-lookup"><span data-stu-id="474f7-208">Boolean</span></span>|<span data-ttu-id="474f7-209">Permitir que los dispositivos bluetooth tener acceso a los contactos de la empresa.</span><span class="sxs-lookup"><span data-stu-id="474f7-209">Allow bluetooth devices to access enterprise contacts.</span></span>|
|<span data-ttu-id="474f7-210">workProfileBlockScreenCapture</span><span class="sxs-lookup"><span data-stu-id="474f7-210">workProfileBlockScreenCapture</span></span>|<span data-ttu-id="474f7-211">Booleano</span><span class="sxs-lookup"><span data-stu-id="474f7-211">Boolean</span></span>|<span data-ttu-id="474f7-212">Captura de pantalla de bloque en el perfil de trabajo.</span><span class="sxs-lookup"><span data-stu-id="474f7-212">Block screen capture in work profile.</span></span>|
|<span data-ttu-id="474f7-213">workProfileBlockCrossProfileCallerId</span><span class="sxs-lookup"><span data-stu-id="474f7-213">workProfileBlockCrossProfileCallerId</span></span>|<span data-ttu-id="474f7-214">Booleano</span><span class="sxs-lookup"><span data-stu-id="474f7-214">Boolean</span></span>|<span data-ttu-id="474f7-215">Identificador de autor de la llamada de perfil bloque para mostrar trabajo en perfil personal.</span><span class="sxs-lookup"><span data-stu-id="474f7-215">Block display work profile caller ID in personal profile.</span></span>|
|<span data-ttu-id="474f7-216">workProfileBlockCamera</span><span class="sxs-lookup"><span data-stu-id="474f7-216">workProfileBlockCamera</span></span>|<span data-ttu-id="474f7-217">Booleano</span><span class="sxs-lookup"><span data-stu-id="474f7-217">Boolean</span></span>|<span data-ttu-id="474f7-218">Cámara de perfil de trabajo de bloque.</span><span class="sxs-lookup"><span data-stu-id="474f7-218">Block work profile camera.</span></span>|
|<span data-ttu-id="474f7-219">workProfileBlockCrossProfileContactsSearch</span><span class="sxs-lookup"><span data-stu-id="474f7-219">workProfileBlockCrossProfileContactsSearch</span></span>|<span data-ttu-id="474f7-220">Booleano</span><span class="sxs-lookup"><span data-stu-id="474f7-220">Boolean</span></span>|<span data-ttu-id="474f7-221">Disponibilidad de los contactos del perfil de trabajo bloque en perfil personal.</span><span class="sxs-lookup"><span data-stu-id="474f7-221">Block work profile contacts availability in personal profile.</span></span>|
|<span data-ttu-id="474f7-222">workProfileBlockCrossProfileCopyPaste</span><span class="sxs-lookup"><span data-stu-id="474f7-222">workProfileBlockCrossProfileCopyPaste</span></span>|<span data-ttu-id="474f7-223">Booleano</span><span class="sxs-lookup"><span data-stu-id="474f7-223">Boolean</span></span>|<span data-ttu-id="474f7-224">Valor booleano que indica si la opción no permitir la entre perfil copiado y pegado está habilitado.</span><span class="sxs-lookup"><span data-stu-id="474f7-224">Boolean that indicates if the setting disallow cross profile copy/paste is enabled.</span></span>|
|<span data-ttu-id="474f7-225">workProfileDefaultAppPermissionPolicy</span><span class="sxs-lookup"><span data-stu-id="474f7-225">workProfileDefaultAppPermissionPolicy</span></span>|[<span data-ttu-id="474f7-226">androidWorkProfileDefaultAppPermissionPolicyType</span><span class="sxs-lookup"><span data-stu-id="474f7-226">androidWorkProfileDefaultAppPermissionPolicyType</span></span>](../resources/intune-deviceconfig-androidworkprofiledefaultapppermissionpolicytype.md)|<span data-ttu-id="474f7-227">Tipo de contraseña que es necesario.</span><span class="sxs-lookup"><span data-stu-id="474f7-227">Type of password that is required.</span></span> <span data-ttu-id="474f7-228">Los valores posibles son: `deviceDefault`, `prompt`, `autoGrant` y `autoDeny`.</span><span class="sxs-lookup"><span data-stu-id="474f7-228">Possible values are: `deviceDefault`, `prompt`, `autoGrant`, `autoDeny`.</span></span>|
|<span data-ttu-id="474f7-229">workProfilePasswordBlockFingerprintUnlock</span><span class="sxs-lookup"><span data-stu-id="474f7-229">workProfilePasswordBlockFingerprintUnlock</span></span>|<span data-ttu-id="474f7-230">Booleano</span><span class="sxs-lookup"><span data-stu-id="474f7-230">Boolean</span></span>|<span data-ttu-id="474f7-231">Indica si se deben bloquear la huella digital de desbloqueo para el perfil de trabajo.</span><span class="sxs-lookup"><span data-stu-id="474f7-231">Indicates whether or not to block fingerprint unlock for work profile.</span></span>|
|<span data-ttu-id="474f7-232">workProfilePasswordBlockTrustAgents</span><span class="sxs-lookup"><span data-stu-id="474f7-232">workProfilePasswordBlockTrustAgents</span></span>|<span data-ttu-id="474f7-233">Booleano</span><span class="sxs-lookup"><span data-stu-id="474f7-233">Boolean</span></span>|<span data-ttu-id="474f7-234">Indica si se deben bloquear bloqueo inteligentes y otros agentes de confianza para el perfil de trabajo.</span><span class="sxs-lookup"><span data-stu-id="474f7-234">Indicates whether or not to block Smart Lock and other trust agents for work profile.</span></span>|
|<span data-ttu-id="474f7-235">workProfilePasswordExpirationDays</span><span class="sxs-lookup"><span data-stu-id="474f7-235">workProfilePasswordExpirationDays</span></span>|<span data-ttu-id="474f7-236">Int32</span><span class="sxs-lookup"><span data-stu-id="474f7-236">Int32</span></span>|<span data-ttu-id="474f7-237">Expira el número de días antes de la contraseña de perfil de trabajo.</span><span class="sxs-lookup"><span data-stu-id="474f7-237">Number of days before the work profile password expires.</span></span> <span data-ttu-id="474f7-238">Valores válidos de 1 a 365</span><span class="sxs-lookup"><span data-stu-id="474f7-238">Valid values 1 to 365</span></span>|
|<span data-ttu-id="474f7-239">workProfilePasswordMinimumLength</span><span class="sxs-lookup"><span data-stu-id="474f7-239">workProfilePasswordMinimumLength</span></span>|<span data-ttu-id="474f7-240">Int32</span><span class="sxs-lookup"><span data-stu-id="474f7-240">Int32</span></span>|<span data-ttu-id="474f7-241">Longitud mínima de contraseña de perfil de trabajo.</span><span class="sxs-lookup"><span data-stu-id="474f7-241">Minimum length of work profile password.</span></span> <span data-ttu-id="474f7-242">Valores válidos de 4 a 16</span><span class="sxs-lookup"><span data-stu-id="474f7-242">Valid values 4 to 16</span></span>|
|<span data-ttu-id="474f7-243">workProfilePasswordMinNumericCharacters</span><span class="sxs-lookup"><span data-stu-id="474f7-243">workProfilePasswordMinNumericCharacters</span></span>|<span data-ttu-id="474f7-244">Int32</span><span class="sxs-lookup"><span data-stu-id="474f7-244">Int32</span></span>|<span data-ttu-id="474f7-245">Nº mínimo de caracteres numéricos que requiere en contraseña de perfil de trabajo.</span><span class="sxs-lookup"><span data-stu-id="474f7-245">Minimum # of numeric characters required in work profile password.</span></span> <span data-ttu-id="474f7-246">Valores válidos de 1 a 10</span><span class="sxs-lookup"><span data-stu-id="474f7-246">Valid values 1 to 10</span></span>|
|<span data-ttu-id="474f7-247">workProfilePasswordMinNonLetterCharacters</span><span class="sxs-lookup"><span data-stu-id="474f7-247">workProfilePasswordMinNonLetterCharacters</span></span>|<span data-ttu-id="474f7-248">Int32</span><span class="sxs-lookup"><span data-stu-id="474f7-248">Int32</span></span>|<span data-ttu-id="474f7-249">Nº mínimo de caracteres que no sea una letra requeridas contraseña de perfil de trabajo.</span><span class="sxs-lookup"><span data-stu-id="474f7-249">Minimum # of non-letter characters required in work profile password.</span></span> <span data-ttu-id="474f7-250">Valores válidos de 1 a 10</span><span class="sxs-lookup"><span data-stu-id="474f7-250">Valid values 1 to 10</span></span>|
|<span data-ttu-id="474f7-251">workProfilePasswordMinLetterCharacters</span><span class="sxs-lookup"><span data-stu-id="474f7-251">workProfilePasswordMinLetterCharacters</span></span>|<span data-ttu-id="474f7-252">Int32</span><span class="sxs-lookup"><span data-stu-id="474f7-252">Int32</span></span>|<span data-ttu-id="474f7-253">Nº mínimo de caracteres de letra requeridas contraseña de perfil de trabajo.</span><span class="sxs-lookup"><span data-stu-id="474f7-253">Minimum # of letter characters required in work profile password.</span></span> <span data-ttu-id="474f7-254">Valores válidos de 1 a 10</span><span class="sxs-lookup"><span data-stu-id="474f7-254">Valid values 1 to 10</span></span>|
|<span data-ttu-id="474f7-255">workProfilePasswordMinLowerCaseCharacters</span><span class="sxs-lookup"><span data-stu-id="474f7-255">workProfilePasswordMinLowerCaseCharacters</span></span>|<span data-ttu-id="474f7-256">Int32</span><span class="sxs-lookup"><span data-stu-id="474f7-256">Int32</span></span>|<span data-ttu-id="474f7-257">Nº mínimo de caracteres minúsculas requeridas contraseña de perfil de trabajo.</span><span class="sxs-lookup"><span data-stu-id="474f7-257">Minimum # of lower-case characters required in work profile password.</span></span> <span data-ttu-id="474f7-258">Valores válidos de 1 a 10</span><span class="sxs-lookup"><span data-stu-id="474f7-258">Valid values 1 to 10</span></span>|
|<span data-ttu-id="474f7-259">workProfilePasswordMinUpperCaseCharacters</span><span class="sxs-lookup"><span data-stu-id="474f7-259">workProfilePasswordMinUpperCaseCharacters</span></span>|<span data-ttu-id="474f7-260">Int32</span><span class="sxs-lookup"><span data-stu-id="474f7-260">Int32</span></span>|<span data-ttu-id="474f7-261">Nº mínimo de caracteres en mayúsculas requeridas contraseña de perfil de trabajo.</span><span class="sxs-lookup"><span data-stu-id="474f7-261">Minimum # of upper-case characters required in work profile password.</span></span> <span data-ttu-id="474f7-262">Valores válidos de 1 a 10</span><span class="sxs-lookup"><span data-stu-id="474f7-262">Valid values 1 to 10</span></span>|
|<span data-ttu-id="474f7-263">workProfilePasswordMinSymbolCharacters</span><span class="sxs-lookup"><span data-stu-id="474f7-263">workProfilePasswordMinSymbolCharacters</span></span>|<span data-ttu-id="474f7-264">Int32</span><span class="sxs-lookup"><span data-stu-id="474f7-264">Int32</span></span>|<span data-ttu-id="474f7-265">Nº mínimo de símbolos requeridas contraseña de perfil de trabajo.</span><span class="sxs-lookup"><span data-stu-id="474f7-265">Minimum # of symbols required in work profile password.</span></span> <span data-ttu-id="474f7-266">Valores válidos de 1 a 10</span><span class="sxs-lookup"><span data-stu-id="474f7-266">Valid values 1 to 10</span></span>|
|<span data-ttu-id="474f7-267">workProfilePasswordMinutesOfInactivityBeforeScreenTimeout</span><span class="sxs-lookup"><span data-stu-id="474f7-267">workProfilePasswordMinutesOfInactivityBeforeScreenTimeout</span></span>|<span data-ttu-id="474f7-268">Int32</span><span class="sxs-lookup"><span data-stu-id="474f7-268">Int32</span></span>|<span data-ttu-id="474f7-269">Minutos de inactividad antes de que se agote el tiempo de espera de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="474f7-269">Minutes of inactivity before the screen times out.</span></span>|
|<span data-ttu-id="474f7-270">workProfilePasswordPreviousPasswordBlockCount</span><span class="sxs-lookup"><span data-stu-id="474f7-270">workProfilePasswordPreviousPasswordBlockCount</span></span>|<span data-ttu-id="474f7-271">Int32</span><span class="sxs-lookup"><span data-stu-id="474f7-271">Int32</span></span>|<span data-ttu-id="474f7-272">Número de contraseñas de perfil de trabajo anterior a bloquear.</span><span class="sxs-lookup"><span data-stu-id="474f7-272">Number of previous work profile passwords to block.</span></span> <span data-ttu-id="474f7-273">Valores válidos de 0 a 24</span><span class="sxs-lookup"><span data-stu-id="474f7-273">Valid values 0 to 24</span></span>|
|<span data-ttu-id="474f7-274">workProfilePasswordSignInFailureCountBeforeFactoryReset</span><span class="sxs-lookup"><span data-stu-id="474f7-274">workProfilePasswordSignInFailureCountBeforeFactoryReset</span></span>|<span data-ttu-id="474f7-275">Int32</span><span class="sxs-lookup"><span data-stu-id="474f7-275">Int32</span></span>|<span data-ttu-id="474f7-276">Número de errores permitidos antes de que se ha quitado el perfil de trabajo y todos los datos corporativos eliminados de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="474f7-276">Number of sign in failures allowed before work profile is removed and all corporate data deleted.</span></span> <span data-ttu-id="474f7-277">Valores válidos de 4 a 11</span><span class="sxs-lookup"><span data-stu-id="474f7-277">Valid values 4 to 11</span></span>|
|<span data-ttu-id="474f7-278">workProfilePasswordRequiredType</span><span class="sxs-lookup"><span data-stu-id="474f7-278">workProfilePasswordRequiredType</span></span>|[<span data-ttu-id="474f7-279">androidWorkProfileRequiredPasswordType</span><span class="sxs-lookup"><span data-stu-id="474f7-279">androidWorkProfileRequiredPasswordType</span></span>](../resources/intune-deviceconfig-androidworkprofilerequiredpasswordtype.md)|<span data-ttu-id="474f7-280">Tipo de contraseña de perfil de trabajo que se requiere.</span><span class="sxs-lookup"><span data-stu-id="474f7-280">Type of work profile password that is required.</span></span> <span data-ttu-id="474f7-281">Los valores posibles son: `deviceDefault`, `lowSecurityBiometric`, `required`, `atLeastNumeric`, `numericComplex`, `atLeastAlphabetic`, `atLeastAlphanumeric` y `alphanumericWithSymbols`.</span><span class="sxs-lookup"><span data-stu-id="474f7-281">Possible values are: `deviceDefault`, `lowSecurityBiometric`, `required`, `atLeastNumeric`, `numericComplex`, `atLeastAlphabetic`, `atLeastAlphanumeric`, `alphanumericWithSymbols`.</span></span>|
|<span data-ttu-id="474f7-282">workProfileRequirePassword</span><span class="sxs-lookup"><span data-stu-id="474f7-282">workProfileRequirePassword</span></span>|<span data-ttu-id="474f7-283">Booleano</span><span class="sxs-lookup"><span data-stu-id="474f7-283">Boolean</span></span>|<span data-ttu-id="474f7-284">Se requiere contraseña o no para el perfil de trabajo</span><span class="sxs-lookup"><span data-stu-id="474f7-284">Password is required or not for work profile</span></span>|
|<span data-ttu-id="474f7-285">securityRequireVerifyApps</span><span class="sxs-lookup"><span data-stu-id="474f7-285">securityRequireVerifyApps</span></span>|<span data-ttu-id="474f7-286">Booleano</span><span class="sxs-lookup"><span data-stu-id="474f7-286">Boolean</span></span>|<span data-ttu-id="474f7-287">Exigir que la característica Verificar aplicaciones de Android esté activada.</span><span class="sxs-lookup"><span data-stu-id="474f7-287">Require the Android Verify apps feature is turned on.</span></span>|
|<span data-ttu-id="474f7-288">vpnAlwaysOnPackageIdentifier</span><span class="sxs-lookup"><span data-stu-id="474f7-288">vpnAlwaysOnPackageIdentifier</span></span>|<span data-ttu-id="474f7-289">Cadena</span><span class="sxs-lookup"><span data-stu-id="474f7-289">String</span></span>|<span data-ttu-id="474f7-290">Habilitar el modo de bloqueo para siempre en VPN.</span><span class="sxs-lookup"><span data-stu-id="474f7-290">Enable lockdown mode for always-on VPN.</span></span>|
|<span data-ttu-id="474f7-291">vpnEnableAlwaysOnLockdownMode</span><span class="sxs-lookup"><span data-stu-id="474f7-291">vpnEnableAlwaysOnLockdownMode</span></span>|<span data-ttu-id="474f7-292">Booleano</span><span class="sxs-lookup"><span data-stu-id="474f7-292">Boolean</span></span>|<span data-ttu-id="474f7-293">Habilitar el modo de bloqueo para siempre en VPN.</span><span class="sxs-lookup"><span data-stu-id="474f7-293">Enable lockdown mode for always-on VPN.</span></span>|



## <a name="response"></a><span data-ttu-id="474f7-294">Respuesta</span><span class="sxs-lookup"><span data-stu-id="474f7-294">Response</span></span>
<span data-ttu-id="474f7-295">Si tiene éxito, este método devuelve una `201 Created` código de respuesta y un objeto [androidWorkProfileGeneralDeviceConfiguration](../resources/intune-deviceconfig-androidworkprofilegeneraldeviceconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="474f7-295">If successful, this method returns a `201 Created` response code and a [androidWorkProfileGeneralDeviceConfiguration](../resources/intune-deviceconfig-androidworkprofilegeneraldeviceconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="474f7-296">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="474f7-296">Example</span></span>
### <a name="request"></a><span data-ttu-id="474f7-297">Solicitud</span><span class="sxs-lookup"><span data-stu-id="474f7-297">Request</span></span>
<span data-ttu-id="474f7-298">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="474f7-298">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations
Content-type: application/json
Content-length: 2106

{
  "@odata.type": "#microsoft.graph.androidWorkProfileGeneralDeviceConfiguration",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "roleScopeTagIds": [
    "Role Scope Tag Ids value"
  ],
  "supportsScopeTags": true,
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
  "securityRequireVerifyApps": true,
  "vpnAlwaysOnPackageIdentifier": "Vpn Always On Package Identifier value",
  "vpnEnableAlwaysOnLockdownMode": true
}
```

### <a name="response"></a><span data-ttu-id="474f7-299">Respuesta</span><span class="sxs-lookup"><span data-stu-id="474f7-299">Response</span></span>
<span data-ttu-id="474f7-p129">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="474f7-p129">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 2214

{
  "@odata.type": "#microsoft.graph.androidWorkProfileGeneralDeviceConfiguration",
  "id": "6decda7e-da7e-6dec-7eda-ec6d7edaec6d",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "roleScopeTagIds": [
    "Role Scope Tag Ids value"
  ],
  "supportsScopeTags": true,
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
  "securityRequireVerifyApps": true,
  "vpnAlwaysOnPackageIdentifier": "Vpn Always On Package Identifier value",
  "vpnEnableAlwaysOnLockdownMode": true
}
```





