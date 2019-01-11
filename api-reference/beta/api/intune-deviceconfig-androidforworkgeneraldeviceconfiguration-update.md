---
title: Actualizar androidForWorkGeneralDeviceConfiguration
description: Actualizar las propiedades de un objeto androidForWorkGeneralDeviceConfiguration.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 9f678a722071c233c2f58016cfa548837d551e37
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27853203"
---
# <a name="update-androidforworkgeneraldeviceconfiguration"></a><span data-ttu-id="e9bce-103">Actualizar androidForWorkGeneralDeviceConfiguration</span><span class="sxs-lookup"><span data-stu-id="e9bce-103">Update androidForWorkGeneralDeviceConfiguration</span></span>

> <span data-ttu-id="e9bce-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="e9bce-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="e9bce-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="e9bce-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="e9bce-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="e9bce-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="e9bce-107">Actualizar las propiedades de un objeto [androidForWorkGeneralDeviceConfiguration](../resources/intune-deviceconfig-androidforworkgeneraldeviceconfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="e9bce-107">Update the properties of a [androidForWorkGeneralDeviceConfiguration](../resources/intune-deviceconfig-androidforworkgeneraldeviceconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="e9bce-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="e9bce-108">Prerequisites</span></span>
<span data-ttu-id="e9bce-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="e9bce-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="e9bce-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e9bce-111">Permission type</span></span>|<span data-ttu-id="e9bce-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e9bce-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="e9bce-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e9bce-113">Delegated (work or school account)</span></span>|<span data-ttu-id="e9bce-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="e9bce-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="e9bce-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e9bce-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="e9bce-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e9bce-116">Not supported.</span></span>|
|<span data-ttu-id="e9bce-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e9bce-117">Application</span></span>|<span data-ttu-id="e9bce-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e9bce-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="e9bce-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e9bce-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/groupAssignments/{deviceConfigurationGroupAssignmentId}/deviceConfiguration
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsDomainJoinConfiguration/networkAccessConfigurations/{deviceConfigurationId}
```

## <a name="request-headers"></a><span data-ttu-id="e9bce-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e9bce-120">Request headers</span></span>
|<span data-ttu-id="e9bce-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e9bce-121">Header</span></span>|<span data-ttu-id="e9bce-122">Valor</span><span class="sxs-lookup"><span data-stu-id="e9bce-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="e9bce-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="e9bce-123">Authorization</span></span>|<span data-ttu-id="e9bce-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="e9bce-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="e9bce-125">Accept</span><span class="sxs-lookup"><span data-stu-id="e9bce-125">Accept</span></span>|<span data-ttu-id="e9bce-126">application/json</span><span class="sxs-lookup"><span data-stu-id="e9bce-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="e9bce-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="e9bce-127">Request body</span></span>
<span data-ttu-id="e9bce-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto [androidForWorkGeneralDeviceConfiguration](../resources/intune-deviceconfig-androidforworkgeneraldeviceconfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="e9bce-128">In the request body, supply a JSON representation for the [androidForWorkGeneralDeviceConfiguration](../resources/intune-deviceconfig-androidforworkgeneraldeviceconfiguration.md) object.</span></span>

<span data-ttu-id="e9bce-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el [androidForWorkGeneralDeviceConfiguration](../resources/intune-deviceconfig-androidforworkgeneraldeviceconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="e9bce-129">The following table shows the properties that are required when you create the [androidForWorkGeneralDeviceConfiguration](../resources/intune-deviceconfig-androidforworkgeneraldeviceconfiguration.md).</span></span>

|<span data-ttu-id="e9bce-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e9bce-130">Property</span></span>|<span data-ttu-id="e9bce-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="e9bce-131">Type</span></span>|<span data-ttu-id="e9bce-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="e9bce-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="e9bce-133">id</span><span class="sxs-lookup"><span data-stu-id="e9bce-133">id</span></span>|<span data-ttu-id="e9bce-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="e9bce-134">String</span></span>|<span data-ttu-id="e9bce-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="e9bce-135">Key of the entity.</span></span> <span data-ttu-id="e9bce-136">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="e9bce-136">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="e9bce-137">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="e9bce-137">lastModifiedDateTime</span></span>|<span data-ttu-id="e9bce-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="e9bce-138">DateTimeOffset</span></span>|<span data-ttu-id="e9bce-139">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="e9bce-139">DateTime the object was last modified.</span></span> <span data-ttu-id="e9bce-140">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="e9bce-140">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="e9bce-141">roleScopeTagIds</span><span class="sxs-lookup"><span data-stu-id="e9bce-141">roleScopeTagIds</span></span>|<span data-ttu-id="e9bce-142">Colección String</span><span class="sxs-lookup"><span data-stu-id="e9bce-142">String collection</span></span>|<span data-ttu-id="e9bce-143">Lista de etiquetas de ámbito para esta instancia de entidad.</span><span class="sxs-lookup"><span data-stu-id="e9bce-143">List of Scope Tags for this Entity instance.</span></span> <span data-ttu-id="e9bce-144">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="e9bce-144">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="e9bce-145">supportsScopeTags</span><span class="sxs-lookup"><span data-stu-id="e9bce-145">supportsScopeTags</span></span>|<span data-ttu-id="e9bce-146">Booleano</span><span class="sxs-lookup"><span data-stu-id="e9bce-146">Boolean</span></span>|<span data-ttu-id="e9bce-147">Indica si la configuración del dispositivo subyacente admite la asignación de etiquetas de ámbito.</span><span class="sxs-lookup"><span data-stu-id="e9bce-147">Indicates whether or not the underlying Device Configuration supports the assignment of scope tags.</span></span> <span data-ttu-id="e9bce-148">No se permite la asignación a la propiedad ScopeTags cuando este valor es false y entidades no estará visibles para los usuarios con ámbito.</span><span class="sxs-lookup"><span data-stu-id="e9bce-148">Assigning to the ScopeTags property is not allowed when this value is false and entities will not be visible to scoped users.</span></span> <span data-ttu-id="e9bce-149">Esto se produce para las directivas de heredado creadas en Silverlight y se puede resolver por eliminar y volver a crear la directiva en el Portal de Azure.</span><span class="sxs-lookup"><span data-stu-id="e9bce-149">This occurs for Legacy policies created in Silverlight and can be resolved by deleting and recreating the policy in the Azure Portal.</span></span> <span data-ttu-id="e9bce-150">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="e9bce-150">This property is read-only.</span></span> <span data-ttu-id="e9bce-151">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="e9bce-151">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="e9bce-152">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="e9bce-152">createdDateTime</span></span>|<span data-ttu-id="e9bce-153">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="e9bce-153">DateTimeOffset</span></span>|<span data-ttu-id="e9bce-154">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="e9bce-154">DateTime the object was created.</span></span> <span data-ttu-id="e9bce-155">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="e9bce-155">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="e9bce-156">descripción</span><span class="sxs-lookup"><span data-stu-id="e9bce-156">description</span></span>|<span data-ttu-id="e9bce-157">Cadena</span><span class="sxs-lookup"><span data-stu-id="e9bce-157">String</span></span>|<span data-ttu-id="e9bce-158">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e9bce-158">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="e9bce-159">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="e9bce-159">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="e9bce-160">displayName</span><span class="sxs-lookup"><span data-stu-id="e9bce-160">displayName</span></span>|<span data-ttu-id="e9bce-161">Cadena</span><span class="sxs-lookup"><span data-stu-id="e9bce-161">String</span></span>|<span data-ttu-id="e9bce-162">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e9bce-162">Admin provided name of the device configuration.</span></span> <span data-ttu-id="e9bce-163">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="e9bce-163">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="e9bce-164">version</span><span class="sxs-lookup"><span data-stu-id="e9bce-164">version</span></span>|<span data-ttu-id="e9bce-165">Int32</span><span class="sxs-lookup"><span data-stu-id="e9bce-165">Int32</span></span>|<span data-ttu-id="e9bce-166">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e9bce-166">Version of the device configuration.</span></span> <span data-ttu-id="e9bce-167">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="e9bce-167">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="e9bce-168">passwordBlockFingerprintUnlock</span><span class="sxs-lookup"><span data-stu-id="e9bce-168">passwordBlockFingerprintUnlock</span></span>|<span data-ttu-id="e9bce-169">Booleano</span><span class="sxs-lookup"><span data-stu-id="e9bce-169">Boolean</span></span>|<span data-ttu-id="e9bce-170">Indica si se va a impedir el desbloqueo por huella dactilar.</span><span class="sxs-lookup"><span data-stu-id="e9bce-170">Indicates whether or not to block fingerprint unlock.</span></span>|
|<span data-ttu-id="e9bce-171">passwordBlockTrustAgents</span><span class="sxs-lookup"><span data-stu-id="e9bce-171">passwordBlockTrustAgents</span></span>|<span data-ttu-id="e9bce-172">Booleano</span><span class="sxs-lookup"><span data-stu-id="e9bce-172">Boolean</span></span>|<span data-ttu-id="e9bce-173">Indica si se van a bloquear Smart Lock y otros agentes de confianza.</span><span class="sxs-lookup"><span data-stu-id="e9bce-173">Indicates whether or not to block Smart Lock and other trust agents.</span></span>|
|<span data-ttu-id="e9bce-174">passwordExpirationDays</span><span class="sxs-lookup"><span data-stu-id="e9bce-174">passwordExpirationDays</span></span>|<span data-ttu-id="e9bce-175">Int32</span><span class="sxs-lookup"><span data-stu-id="e9bce-175">Int32</span></span>|<span data-ttu-id="e9bce-176">Número de días antes de que expire la contraseña.</span><span class="sxs-lookup"><span data-stu-id="e9bce-176">Number of days before the password expires.</span></span> <span data-ttu-id="e9bce-177">Valores válidos de 1 a 365</span><span class="sxs-lookup"><span data-stu-id="e9bce-177">Valid values 1 to 365</span></span>|
|<span data-ttu-id="e9bce-178">passwordMinimumLength</span><span class="sxs-lookup"><span data-stu-id="e9bce-178">passwordMinimumLength</span></span>|<span data-ttu-id="e9bce-179">Int32</span><span class="sxs-lookup"><span data-stu-id="e9bce-179">Int32</span></span>|<span data-ttu-id="e9bce-180">Longitud mínima de las contraseñas.</span><span class="sxs-lookup"><span data-stu-id="e9bce-180">Minimum length of passwords.</span></span> <span data-ttu-id="e9bce-181">Valores válidos de 4 a 16</span><span class="sxs-lookup"><span data-stu-id="e9bce-181">Valid values 4 to 16</span></span>|
|<span data-ttu-id="e9bce-182">passwordMinutesOfInactivityBeforeScreenTimeout</span><span class="sxs-lookup"><span data-stu-id="e9bce-182">passwordMinutesOfInactivityBeforeScreenTimeout</span></span>|<span data-ttu-id="e9bce-183">Int32</span><span class="sxs-lookup"><span data-stu-id="e9bce-183">Int32</span></span>|<span data-ttu-id="e9bce-184">Minutos de inactividad antes de que se agote el tiempo de espera de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="e9bce-184">Minutes of inactivity before the screen times out.</span></span>|
|<span data-ttu-id="e9bce-185">passwordPreviousPasswordBlockCount</span><span class="sxs-lookup"><span data-stu-id="e9bce-185">passwordPreviousPasswordBlockCount</span></span>|<span data-ttu-id="e9bce-186">Int32</span><span class="sxs-lookup"><span data-stu-id="e9bce-186">Int32</span></span>|<span data-ttu-id="e9bce-187">Número de contraseñas anteriores que bloquear.</span><span class="sxs-lookup"><span data-stu-id="e9bce-187">Number of previous passwords to block.</span></span> <span data-ttu-id="e9bce-188">Valores válidos de 0 a 24</span><span class="sxs-lookup"><span data-stu-id="e9bce-188">Valid values 0 to 24</span></span>|
|<span data-ttu-id="e9bce-189">passwordSignInFailureCountBeforeFactoryReset</span><span class="sxs-lookup"><span data-stu-id="e9bce-189">passwordSignInFailureCountBeforeFactoryReset</span></span>|<span data-ttu-id="e9bce-190">Int32</span><span class="sxs-lookup"><span data-stu-id="e9bce-190">Int32</span></span>|<span data-ttu-id="e9bce-191">Número de errores de inicio de sesión permitidos antes del restablecimiento de fábrica.</span><span class="sxs-lookup"><span data-stu-id="e9bce-191">Number of sign in failures allowed before factory reset.</span></span> <span data-ttu-id="e9bce-192">Valores válidos de 4 a 11</span><span class="sxs-lookup"><span data-stu-id="e9bce-192">Valid values 4 to 11</span></span>|
|<span data-ttu-id="e9bce-193">passwordRequiredType</span><span class="sxs-lookup"><span data-stu-id="e9bce-193">passwordRequiredType</span></span>|[<span data-ttu-id="e9bce-194">androidForWorkRequiredPasswordType</span><span class="sxs-lookup"><span data-stu-id="e9bce-194">androidForWorkRequiredPasswordType</span></span>](../resources/intune-deviceconfig-androidforworkrequiredpasswordtype.md)|<span data-ttu-id="e9bce-195">Tipo de contraseña que es necesario.</span><span class="sxs-lookup"><span data-stu-id="e9bce-195">Type of password that is required.</span></span> <span data-ttu-id="e9bce-196">Los valores posibles son: `deviceDefault`, `lowSecurityBiometric`, `required`, `atLeastNumeric`, `numericComplex`, `atLeastAlphabetic`, `atLeastAlphanumeric` y `alphanumericWithSymbols`.</span><span class="sxs-lookup"><span data-stu-id="e9bce-196">Possible values are: `deviceDefault`, `lowSecurityBiometric`, `required`, `atLeastNumeric`, `numericComplex`, `atLeastAlphabetic`, `atLeastAlphanumeric`, `alphanumericWithSymbols`.</span></span>|
|<span data-ttu-id="e9bce-197">workProfileDataSharingType</span><span class="sxs-lookup"><span data-stu-id="e9bce-197">workProfileDataSharingType</span></span>|[<span data-ttu-id="e9bce-198">androidForWorkCrossProfileDataSharingType</span><span class="sxs-lookup"><span data-stu-id="e9bce-198">androidForWorkCrossProfileDataSharingType</span></span>](../resources/intune-deviceconfig-androidforworkcrossprofiledatasharingtype.md)|<span data-ttu-id="e9bce-199">Tipo de datos de uso compartido está permitido.</span><span class="sxs-lookup"><span data-stu-id="e9bce-199">Type of data sharing that is allowed.</span></span> <span data-ttu-id="e9bce-200">Los valores posibles son: `deviceDefault`, `preventAny`, `allowPersonalToWork` y `noRestrictions`.</span><span class="sxs-lookup"><span data-stu-id="e9bce-200">Possible values are: `deviceDefault`, `preventAny`, `allowPersonalToWork`, `noRestrictions`.</span></span>|
|<span data-ttu-id="e9bce-201">workProfileBlockNotificationsWhileDeviceLocked</span><span class="sxs-lookup"><span data-stu-id="e9bce-201">workProfileBlockNotificationsWhileDeviceLocked</span></span>|<span data-ttu-id="e9bce-202">Booleano</span><span class="sxs-lookup"><span data-stu-id="e9bce-202">Boolean</span></span>|<span data-ttu-id="e9bce-203">Indica si se deben bloquear las notificaciones al dispositivo bloqueado.</span><span class="sxs-lookup"><span data-stu-id="e9bce-203">Indicates whether or not to block notifications while device locked.</span></span>|
|<span data-ttu-id="e9bce-204">workProfileBlockAddingAccounts</span><span class="sxs-lookup"><span data-stu-id="e9bce-204">workProfileBlockAddingAccounts</span></span>|<span data-ttu-id="e9bce-205">Booleano</span><span class="sxs-lookup"><span data-stu-id="e9bce-205">Boolean</span></span>|<span data-ttu-id="e9bce-206">Impedir que los usuarios agregar o quitar cuentas en el perfil de trabajo.</span><span class="sxs-lookup"><span data-stu-id="e9bce-206">Block users from adding/removing accounts in work profile.</span></span>|
|<span data-ttu-id="e9bce-207">workProfileBluetoothEnableContactSharing</span><span class="sxs-lookup"><span data-stu-id="e9bce-207">workProfileBluetoothEnableContactSharing</span></span>|<span data-ttu-id="e9bce-208">Booleano</span><span class="sxs-lookup"><span data-stu-id="e9bce-208">Boolean</span></span>|<span data-ttu-id="e9bce-209">Permitir que los dispositivos bluetooth tener acceso a los contactos de la empresa.</span><span class="sxs-lookup"><span data-stu-id="e9bce-209">Allow bluetooth devices to access enterprise contacts.</span></span>|
|<span data-ttu-id="e9bce-210">workProfileBlockScreenCapture</span><span class="sxs-lookup"><span data-stu-id="e9bce-210">workProfileBlockScreenCapture</span></span>|<span data-ttu-id="e9bce-211">Booleano</span><span class="sxs-lookup"><span data-stu-id="e9bce-211">Boolean</span></span>|<span data-ttu-id="e9bce-212">Captura de pantalla de bloque en el perfil de trabajo.</span><span class="sxs-lookup"><span data-stu-id="e9bce-212">Block screen capture in work profile.</span></span>|
|<span data-ttu-id="e9bce-213">workProfileBlockCrossProfileCallerId</span><span class="sxs-lookup"><span data-stu-id="e9bce-213">workProfileBlockCrossProfileCallerId</span></span>|<span data-ttu-id="e9bce-214">Booleano</span><span class="sxs-lookup"><span data-stu-id="e9bce-214">Boolean</span></span>|<span data-ttu-id="e9bce-215">Identificador de autor de la llamada de perfil bloque para mostrar trabajo en perfil personal.</span><span class="sxs-lookup"><span data-stu-id="e9bce-215">Block display work profile caller ID in personal profile.</span></span>|
|<span data-ttu-id="e9bce-216">workProfileBlockCamera</span><span class="sxs-lookup"><span data-stu-id="e9bce-216">workProfileBlockCamera</span></span>|<span data-ttu-id="e9bce-217">Booleano</span><span class="sxs-lookup"><span data-stu-id="e9bce-217">Boolean</span></span>|<span data-ttu-id="e9bce-218">Cámara de perfil de trabajo de bloque.</span><span class="sxs-lookup"><span data-stu-id="e9bce-218">Block work profile camera.</span></span>|
|<span data-ttu-id="e9bce-219">workProfileBlockCrossProfileContactsSearch</span><span class="sxs-lookup"><span data-stu-id="e9bce-219">workProfileBlockCrossProfileContactsSearch</span></span>|<span data-ttu-id="e9bce-220">Booleano</span><span class="sxs-lookup"><span data-stu-id="e9bce-220">Boolean</span></span>|<span data-ttu-id="e9bce-221">Disponibilidad de los contactos del perfil de trabajo bloque en perfil personal.</span><span class="sxs-lookup"><span data-stu-id="e9bce-221">Block work profile contacts availability in personal profile.</span></span>|
|<span data-ttu-id="e9bce-222">workProfileBlockCrossProfileCopyPaste</span><span class="sxs-lookup"><span data-stu-id="e9bce-222">workProfileBlockCrossProfileCopyPaste</span></span>|<span data-ttu-id="e9bce-223">Booleano</span><span class="sxs-lookup"><span data-stu-id="e9bce-223">Boolean</span></span>|<span data-ttu-id="e9bce-224">Valor booleano que indica si la opción no permitir la entre perfil copiado y pegado está habilitado.</span><span class="sxs-lookup"><span data-stu-id="e9bce-224">Boolean that indicates if the setting disallow cross profile copy/paste is enabled.</span></span>|
|<span data-ttu-id="e9bce-225">workProfileDefaultAppPermissionPolicy</span><span class="sxs-lookup"><span data-stu-id="e9bce-225">workProfileDefaultAppPermissionPolicy</span></span>|[<span data-ttu-id="e9bce-226">androidForWorkDefaultAppPermissionPolicyType</span><span class="sxs-lookup"><span data-stu-id="e9bce-226">androidForWorkDefaultAppPermissionPolicyType</span></span>](../resources/intune-deviceconfig-androidforworkdefaultapppermissionpolicytype.md)|<span data-ttu-id="e9bce-227">Tipo de contraseña que es necesario.</span><span class="sxs-lookup"><span data-stu-id="e9bce-227">Type of password that is required.</span></span> <span data-ttu-id="e9bce-228">Los valores posibles son: `deviceDefault`, `prompt`, `autoGrant` y `autoDeny`.</span><span class="sxs-lookup"><span data-stu-id="e9bce-228">Possible values are: `deviceDefault`, `prompt`, `autoGrant`, `autoDeny`.</span></span>|
|<span data-ttu-id="e9bce-229">workProfilePasswordBlockFingerprintUnlock</span><span class="sxs-lookup"><span data-stu-id="e9bce-229">workProfilePasswordBlockFingerprintUnlock</span></span>|<span data-ttu-id="e9bce-230">Booleano</span><span class="sxs-lookup"><span data-stu-id="e9bce-230">Boolean</span></span>|<span data-ttu-id="e9bce-231">Indica si se deben bloquear la huella digital de desbloqueo para el perfil de trabajo.</span><span class="sxs-lookup"><span data-stu-id="e9bce-231">Indicates whether or not to block fingerprint unlock for work profile.</span></span>|
|<span data-ttu-id="e9bce-232">workProfilePasswordBlockTrustAgents</span><span class="sxs-lookup"><span data-stu-id="e9bce-232">workProfilePasswordBlockTrustAgents</span></span>|<span data-ttu-id="e9bce-233">Booleano</span><span class="sxs-lookup"><span data-stu-id="e9bce-233">Boolean</span></span>|<span data-ttu-id="e9bce-234">Indica si se deben bloquear bloqueo inteligentes y otros agentes de confianza para el perfil de trabajo.</span><span class="sxs-lookup"><span data-stu-id="e9bce-234">Indicates whether or not to block Smart Lock and other trust agents for work profile.</span></span>|
|<span data-ttu-id="e9bce-235">workProfilePasswordExpirationDays</span><span class="sxs-lookup"><span data-stu-id="e9bce-235">workProfilePasswordExpirationDays</span></span>|<span data-ttu-id="e9bce-236">Int32</span><span class="sxs-lookup"><span data-stu-id="e9bce-236">Int32</span></span>|<span data-ttu-id="e9bce-237">Expira el número de días antes de la contraseña de perfil de trabajo.</span><span class="sxs-lookup"><span data-stu-id="e9bce-237">Number of days before the work profile password expires.</span></span> <span data-ttu-id="e9bce-238">Valores válidos de 1 a 365</span><span class="sxs-lookup"><span data-stu-id="e9bce-238">Valid values 1 to 365</span></span>|
|<span data-ttu-id="e9bce-239">workProfilePasswordMinimumLength</span><span class="sxs-lookup"><span data-stu-id="e9bce-239">workProfilePasswordMinimumLength</span></span>|<span data-ttu-id="e9bce-240">Int32</span><span class="sxs-lookup"><span data-stu-id="e9bce-240">Int32</span></span>|<span data-ttu-id="e9bce-241">Longitud mínima de contraseña de perfil de trabajo.</span><span class="sxs-lookup"><span data-stu-id="e9bce-241">Minimum length of work profile password.</span></span> <span data-ttu-id="e9bce-242">Valores válidos de 4 a 16</span><span class="sxs-lookup"><span data-stu-id="e9bce-242">Valid values 4 to 16</span></span>|
|<span data-ttu-id="e9bce-243">workProfilePasswordMinNumericCharacters</span><span class="sxs-lookup"><span data-stu-id="e9bce-243">workProfilePasswordMinNumericCharacters</span></span>|<span data-ttu-id="e9bce-244">Int32</span><span class="sxs-lookup"><span data-stu-id="e9bce-244">Int32</span></span>|<span data-ttu-id="e9bce-245">Nº mínimo de caracteres numéricos que requiere en contraseña de perfil de trabajo.</span><span class="sxs-lookup"><span data-stu-id="e9bce-245">Minimum # of numeric characters required in work profile password.</span></span> <span data-ttu-id="e9bce-246">Valores válidos de 1 a 10</span><span class="sxs-lookup"><span data-stu-id="e9bce-246">Valid values 1 to 10</span></span>|
|<span data-ttu-id="e9bce-247">workProfilePasswordMinNonLetterCharacters</span><span class="sxs-lookup"><span data-stu-id="e9bce-247">workProfilePasswordMinNonLetterCharacters</span></span>|<span data-ttu-id="e9bce-248">Int32</span><span class="sxs-lookup"><span data-stu-id="e9bce-248">Int32</span></span>|<span data-ttu-id="e9bce-249">Nº mínimo de caracteres que no sea una letra requeridas contraseña de perfil de trabajo.</span><span class="sxs-lookup"><span data-stu-id="e9bce-249">Minimum # of non-letter characters required in work profile password.</span></span> <span data-ttu-id="e9bce-250">Valores válidos de 1 a 10</span><span class="sxs-lookup"><span data-stu-id="e9bce-250">Valid values 1 to 10</span></span>|
|<span data-ttu-id="e9bce-251">workProfilePasswordMinLetterCharacters</span><span class="sxs-lookup"><span data-stu-id="e9bce-251">workProfilePasswordMinLetterCharacters</span></span>|<span data-ttu-id="e9bce-252">Int32</span><span class="sxs-lookup"><span data-stu-id="e9bce-252">Int32</span></span>|<span data-ttu-id="e9bce-253">Nº mínimo de caracteres de letra requeridas contraseña de perfil de trabajo.</span><span class="sxs-lookup"><span data-stu-id="e9bce-253">Minimum # of letter characters required in work profile password.</span></span> <span data-ttu-id="e9bce-254">Valores válidos de 1 a 10</span><span class="sxs-lookup"><span data-stu-id="e9bce-254">Valid values 1 to 10</span></span>|
|<span data-ttu-id="e9bce-255">workProfilePasswordMinLowerCaseCharacters</span><span class="sxs-lookup"><span data-stu-id="e9bce-255">workProfilePasswordMinLowerCaseCharacters</span></span>|<span data-ttu-id="e9bce-256">Int32</span><span class="sxs-lookup"><span data-stu-id="e9bce-256">Int32</span></span>|<span data-ttu-id="e9bce-257">Nº mínimo de caracteres minúsculas requeridas contraseña de perfil de trabajo.</span><span class="sxs-lookup"><span data-stu-id="e9bce-257">Minimum # of lower-case characters required in work profile password.</span></span> <span data-ttu-id="e9bce-258">Valores válidos de 1 a 10</span><span class="sxs-lookup"><span data-stu-id="e9bce-258">Valid values 1 to 10</span></span>|
|<span data-ttu-id="e9bce-259">workProfilePasswordMinUpperCaseCharacters</span><span class="sxs-lookup"><span data-stu-id="e9bce-259">workProfilePasswordMinUpperCaseCharacters</span></span>|<span data-ttu-id="e9bce-260">Int32</span><span class="sxs-lookup"><span data-stu-id="e9bce-260">Int32</span></span>|<span data-ttu-id="e9bce-261">Nº mínimo de caracteres en mayúsculas requeridas contraseña de perfil de trabajo.</span><span class="sxs-lookup"><span data-stu-id="e9bce-261">Minimum # of upper-case characters required in work profile password.</span></span> <span data-ttu-id="e9bce-262">Valores válidos de 1 a 10</span><span class="sxs-lookup"><span data-stu-id="e9bce-262">Valid values 1 to 10</span></span>|
|<span data-ttu-id="e9bce-263">workProfilePasswordMinSymbolCharacters</span><span class="sxs-lookup"><span data-stu-id="e9bce-263">workProfilePasswordMinSymbolCharacters</span></span>|<span data-ttu-id="e9bce-264">Int32</span><span class="sxs-lookup"><span data-stu-id="e9bce-264">Int32</span></span>|<span data-ttu-id="e9bce-265">Nº mínimo de símbolos requeridas contraseña de perfil de trabajo.</span><span class="sxs-lookup"><span data-stu-id="e9bce-265">Minimum # of symbols required in work profile password.</span></span> <span data-ttu-id="e9bce-266">Valores válidos de 1 a 10</span><span class="sxs-lookup"><span data-stu-id="e9bce-266">Valid values 1 to 10</span></span>|
|<span data-ttu-id="e9bce-267">workProfilePasswordMinutesOfInactivityBeforeScreenTimeout</span><span class="sxs-lookup"><span data-stu-id="e9bce-267">workProfilePasswordMinutesOfInactivityBeforeScreenTimeout</span></span>|<span data-ttu-id="e9bce-268">Int32</span><span class="sxs-lookup"><span data-stu-id="e9bce-268">Int32</span></span>|<span data-ttu-id="e9bce-269">Minutos de inactividad antes de que se agote el tiempo de espera de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="e9bce-269">Minutes of inactivity before the screen times out.</span></span>|
|<span data-ttu-id="e9bce-270">workProfilePasswordPreviousPasswordBlockCount</span><span class="sxs-lookup"><span data-stu-id="e9bce-270">workProfilePasswordPreviousPasswordBlockCount</span></span>|<span data-ttu-id="e9bce-271">Int32</span><span class="sxs-lookup"><span data-stu-id="e9bce-271">Int32</span></span>|<span data-ttu-id="e9bce-272">Número de contraseñas de perfil de trabajo anterior a bloquear.</span><span class="sxs-lookup"><span data-stu-id="e9bce-272">Number of previous work profile passwords to block.</span></span> <span data-ttu-id="e9bce-273">Valores válidos de 0 a 24</span><span class="sxs-lookup"><span data-stu-id="e9bce-273">Valid values 0 to 24</span></span>|
|<span data-ttu-id="e9bce-274">workProfilePasswordSignInFailureCountBeforeFactoryReset</span><span class="sxs-lookup"><span data-stu-id="e9bce-274">workProfilePasswordSignInFailureCountBeforeFactoryReset</span></span>|<span data-ttu-id="e9bce-275">Int32</span><span class="sxs-lookup"><span data-stu-id="e9bce-275">Int32</span></span>|<span data-ttu-id="e9bce-276">Número de errores permitidos antes de que se ha quitado el perfil de trabajo y todos los datos corporativos eliminados de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="e9bce-276">Number of sign in failures allowed before work profile is removed and all corporate data deleted.</span></span> <span data-ttu-id="e9bce-277">Valores válidos de 4 a 11</span><span class="sxs-lookup"><span data-stu-id="e9bce-277">Valid values 4 to 11</span></span>|
|<span data-ttu-id="e9bce-278">workProfilePasswordRequiredType</span><span class="sxs-lookup"><span data-stu-id="e9bce-278">workProfilePasswordRequiredType</span></span>|[<span data-ttu-id="e9bce-279">androidForWorkRequiredPasswordType</span><span class="sxs-lookup"><span data-stu-id="e9bce-279">androidForWorkRequiredPasswordType</span></span>](../resources/intune-deviceconfig-androidforworkrequiredpasswordtype.md)|<span data-ttu-id="e9bce-280">Tipo de contraseña de perfil de trabajo que se requiere.</span><span class="sxs-lookup"><span data-stu-id="e9bce-280">Type of work profile password that is required.</span></span> <span data-ttu-id="e9bce-281">Los valores posibles son: `deviceDefault`, `lowSecurityBiometric`, `required`, `atLeastNumeric`, `numericComplex`, `atLeastAlphabetic`, `atLeastAlphanumeric` y `alphanumericWithSymbols`.</span><span class="sxs-lookup"><span data-stu-id="e9bce-281">Possible values are: `deviceDefault`, `lowSecurityBiometric`, `required`, `atLeastNumeric`, `numericComplex`, `atLeastAlphabetic`, `atLeastAlphanumeric`, `alphanumericWithSymbols`.</span></span>|
|<span data-ttu-id="e9bce-282">workProfileRequirePassword</span><span class="sxs-lookup"><span data-stu-id="e9bce-282">workProfileRequirePassword</span></span>|<span data-ttu-id="e9bce-283">Booleano</span><span class="sxs-lookup"><span data-stu-id="e9bce-283">Boolean</span></span>|<span data-ttu-id="e9bce-284">Se requiere contraseña o no para el perfil de trabajo</span><span class="sxs-lookup"><span data-stu-id="e9bce-284">Password is required or not for work profile</span></span>|
|<span data-ttu-id="e9bce-285">securityRequireVerifyApps</span><span class="sxs-lookup"><span data-stu-id="e9bce-285">securityRequireVerifyApps</span></span>|<span data-ttu-id="e9bce-286">Booleano</span><span class="sxs-lookup"><span data-stu-id="e9bce-286">Boolean</span></span>|<span data-ttu-id="e9bce-287">Exigir que la característica Verificar aplicaciones de Android esté activada.</span><span class="sxs-lookup"><span data-stu-id="e9bce-287">Require the Android Verify apps feature is turned on.</span></span>|
|<span data-ttu-id="e9bce-288">vpnAlwaysOnPackageIdentifier</span><span class="sxs-lookup"><span data-stu-id="e9bce-288">vpnAlwaysOnPackageIdentifier</span></span>|<span data-ttu-id="e9bce-289">Cadena</span><span class="sxs-lookup"><span data-stu-id="e9bce-289">String</span></span>|<span data-ttu-id="e9bce-290">Habilitar el modo de bloqueo para siempre en VPN.</span><span class="sxs-lookup"><span data-stu-id="e9bce-290">Enable lockdown mode for always-on VPN.</span></span>|
|<span data-ttu-id="e9bce-291">vpnEnableAlwaysOnLockdownMode</span><span class="sxs-lookup"><span data-stu-id="e9bce-291">vpnEnableAlwaysOnLockdownMode</span></span>|<span data-ttu-id="e9bce-292">Booleano</span><span class="sxs-lookup"><span data-stu-id="e9bce-292">Boolean</span></span>|<span data-ttu-id="e9bce-293">Habilitar el modo de bloqueo para siempre en VPN.</span><span class="sxs-lookup"><span data-stu-id="e9bce-293">Enable lockdown mode for always-on VPN.</span></span>|



## <a name="response"></a><span data-ttu-id="e9bce-294">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e9bce-294">Response</span></span>
<span data-ttu-id="e9bce-295">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto actualizado [androidForWorkGeneralDeviceConfiguration](../resources/intune-deviceconfig-androidforworkgeneraldeviceconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e9bce-295">If successful, this method returns a `200 OK` response code and an updated [androidForWorkGeneralDeviceConfiguration](../resources/intune-deviceconfig-androidforworkgeneraldeviceconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="e9bce-296">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e9bce-296">Example</span></span>
### <a name="request"></a><span data-ttu-id="e9bce-297">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e9bce-297">Request</span></span>
<span data-ttu-id="e9bce-298">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e9bce-298">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations/{deviceConfigurationId}
Content-type: application/json
Content-length: 2023

{
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

### <a name="response"></a><span data-ttu-id="e9bce-299">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e9bce-299">Response</span></span>
<span data-ttu-id="e9bce-p129">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="e9bce-p129">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 2210

{
  "@odata.type": "#microsoft.graph.androidForWorkGeneralDeviceConfiguration",
  "id": "a931a366-a366-a931-66a3-31a966a331a9",
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





