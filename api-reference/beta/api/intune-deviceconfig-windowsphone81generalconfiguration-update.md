---
title: Actualizar windowsPhone81GeneralConfiguration
description: Actualice las propiedades de un objeto windowsPhone81GeneralConfiguration.
ms.openlocfilehash: b6789ea8dcf7ebeb1a36b705256af27857c93970
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27091017"
---
# <a name="update-windowsphone81generalconfiguration"></a><span data-ttu-id="896fb-103">Actualizar windowsPhone81GeneralConfiguration</span><span class="sxs-lookup"><span data-stu-id="896fb-103">Update windowsPhone81GeneralConfiguration</span></span>

> <span data-ttu-id="896fb-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="896fb-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="896fb-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="896fb-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="896fb-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="896fb-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="896fb-107">Actualice las propiedades de un objeto [windowsPhone81GeneralConfiguration](../resources/intune-deviceconfig-windowsphone81generalconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="896fb-107">Update the properties of a [windowsPhone81GeneralConfiguration](../resources/intune-deviceconfig-windowsphone81generalconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="896fb-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="896fb-108">Prerequisites</span></span>
<span data-ttu-id="896fb-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="896fb-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="896fb-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="896fb-111">Permission type</span></span>|<span data-ttu-id="896fb-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="896fb-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="896fb-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="896fb-113">Delegated (work or school account)</span></span>|<span data-ttu-id="896fb-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="896fb-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="896fb-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="896fb-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="896fb-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="896fb-116">Not supported.</span></span>|
|<span data-ttu-id="896fb-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="896fb-117">Application</span></span>|<span data-ttu-id="896fb-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="896fb-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="896fb-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="896fb-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/groupAssignments/{deviceConfigurationGroupAssignmentId}/deviceConfiguration
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsDomainJoinConfiguration/networkAccessConfigurations/{deviceConfigurationId}
```

## <a name="request-headers"></a><span data-ttu-id="896fb-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="896fb-120">Request headers</span></span>
|<span data-ttu-id="896fb-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="896fb-121">Header</span></span>|<span data-ttu-id="896fb-122">Valor</span><span class="sxs-lookup"><span data-stu-id="896fb-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="896fb-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="896fb-123">Authorization</span></span>|<span data-ttu-id="896fb-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="896fb-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="896fb-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="896fb-125">Accept</span></span>|<span data-ttu-id="896fb-126">application/json</span><span class="sxs-lookup"><span data-stu-id="896fb-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="896fb-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="896fb-127">Request body</span></span>
<span data-ttu-id="896fb-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto [windowsPhone81GeneralConfiguration](../resources/intune-deviceconfig-windowsphone81generalconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="896fb-128">In the request body, supply a JSON representation for the [windowsPhone81GeneralConfiguration](../resources/intune-deviceconfig-windowsphone81generalconfiguration.md) object.</span></span>

<span data-ttu-id="896fb-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [windowsPhone81GeneralConfiguration](../resources/intune-deviceconfig-windowsphone81generalconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="896fb-129">The following table shows the properties that are required when you create the [windowsPhone81GeneralConfiguration](../resources/intune-deviceconfig-windowsphone81generalconfiguration.md).</span></span>

|<span data-ttu-id="896fb-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="896fb-130">Property</span></span>|<span data-ttu-id="896fb-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="896fb-131">Type</span></span>|<span data-ttu-id="896fb-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="896fb-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="896fb-133">id</span><span class="sxs-lookup"><span data-stu-id="896fb-133">id</span></span>|<span data-ttu-id="896fb-134">String</span><span class="sxs-lookup"><span data-stu-id="896fb-134">String</span></span>|<span data-ttu-id="896fb-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="896fb-135">Key of the entity.</span></span> <span data-ttu-id="896fb-136">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="896fb-136">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="896fb-137">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="896fb-137">lastModifiedDateTime</span></span>|<span data-ttu-id="896fb-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="896fb-138">DateTimeOffset</span></span>|<span data-ttu-id="896fb-139">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="896fb-139">DateTime the object was last modified.</span></span> <span data-ttu-id="896fb-140">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="896fb-140">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="896fb-141">roleScopeTagIds</span><span class="sxs-lookup"><span data-stu-id="896fb-141">roleScopeTagIds</span></span>|<span data-ttu-id="896fb-142">Colección String</span><span class="sxs-lookup"><span data-stu-id="896fb-142">String collection</span></span>|<span data-ttu-id="896fb-143">Lista de etiquetas de ámbito para esta instancia de entidad.</span><span class="sxs-lookup"><span data-stu-id="896fb-143">List of Scope Tags for this Entity instance.</span></span> <span data-ttu-id="896fb-144">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="896fb-144">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="896fb-145">supportsScopeTags</span><span class="sxs-lookup"><span data-stu-id="896fb-145">supportsScopeTags</span></span>|<span data-ttu-id="896fb-146">Booleano</span><span class="sxs-lookup"><span data-stu-id="896fb-146">Boolean</span></span>|<span data-ttu-id="896fb-147">Indica si la configuración del dispositivo subyacente admite la asignación de etiquetas de ámbito.</span><span class="sxs-lookup"><span data-stu-id="896fb-147">Indicates whether or not the underlying Device Configuration supports the assignment of scope tags.</span></span> <span data-ttu-id="896fb-148">No se permite la asignación a la propiedad ScopeTags cuando este valor es false y entidades no estará visibles para los usuarios con ámbito.</span><span class="sxs-lookup"><span data-stu-id="896fb-148">Assigning to the ScopeTags property is not allowed when this value is false and entities will not be visible to scoped users.</span></span> <span data-ttu-id="896fb-149">Esto se produce para las directivas de heredado creadas en Silverlight y se puede resolver por eliminar y volver a crear la directiva en el Portal de Azure.</span><span class="sxs-lookup"><span data-stu-id="896fb-149">This occurs for Legacy policies created in Silverlight and can be resolved by deleting and recreating the policy in the Azure Portal.</span></span> <span data-ttu-id="896fb-150">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="896fb-150">This property is read-only.</span></span> <span data-ttu-id="896fb-151">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="896fb-151">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="896fb-152">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="896fb-152">createdDateTime</span></span>|<span data-ttu-id="896fb-153">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="896fb-153">DateTimeOffset</span></span>|<span data-ttu-id="896fb-154">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="896fb-154">DateTime the object was created.</span></span> <span data-ttu-id="896fb-155">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="896fb-155">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="896fb-156">descripción</span><span class="sxs-lookup"><span data-stu-id="896fb-156">description</span></span>|<span data-ttu-id="896fb-157">String</span><span class="sxs-lookup"><span data-stu-id="896fb-157">String</span></span>|<span data-ttu-id="896fb-158">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="896fb-158">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="896fb-159">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="896fb-159">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="896fb-160">displayName</span><span class="sxs-lookup"><span data-stu-id="896fb-160">displayName</span></span>|<span data-ttu-id="896fb-161">String</span><span class="sxs-lookup"><span data-stu-id="896fb-161">String</span></span>|<span data-ttu-id="896fb-162">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="896fb-162">Admin provided name of the device configuration.</span></span> <span data-ttu-id="896fb-163">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="896fb-163">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="896fb-164">version</span><span class="sxs-lookup"><span data-stu-id="896fb-164">version</span></span>|<span data-ttu-id="896fb-165">Int32</span><span class="sxs-lookup"><span data-stu-id="896fb-165">Int32</span></span>|<span data-ttu-id="896fb-166">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="896fb-166">Version of the device configuration.</span></span> <span data-ttu-id="896fb-167">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="896fb-167">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="896fb-168">applyOnlyToWindowsPhone81</span><span class="sxs-lookup"><span data-stu-id="896fb-168">applyOnlyToWindowsPhone81</span></span>|<span data-ttu-id="896fb-169">Booleano</span><span class="sxs-lookup"><span data-stu-id="896fb-169">Boolean</span></span>|<span data-ttu-id="896fb-170">Valor que indica si esta directiva se aplica solo a Windows Phone 8.1.</span><span class="sxs-lookup"><span data-stu-id="896fb-170">Value indicating whether this policy only applies to Windows Phone 8.1.</span></span> <span data-ttu-id="896fb-171">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="896fb-171">This property is read-only.</span></span>|
|<span data-ttu-id="896fb-172">appsBlockCopyPaste</span><span class="sxs-lookup"><span data-stu-id="896fb-172">appsBlockCopyPaste</span></span>|<span data-ttu-id="896fb-173">Booleano</span><span class="sxs-lookup"><span data-stu-id="896fb-173">Boolean</span></span>|<span data-ttu-id="896fb-174">Indica si se va a impedir cortar y pegar.</span><span class="sxs-lookup"><span data-stu-id="896fb-174">Indicates whether or not to block copy paste.</span></span>|
|<span data-ttu-id="896fb-175">bluetoothBlocked</span><span class="sxs-lookup"><span data-stu-id="896fb-175">bluetoothBlocked</span></span>|<span data-ttu-id="896fb-176">Booleano</span><span class="sxs-lookup"><span data-stu-id="896fb-176">Boolean</span></span>|<span data-ttu-id="896fb-177">Indica si se va a bloquear Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="896fb-177">Indicates whether or not to block bluetooth.</span></span>|
|<span data-ttu-id="896fb-178">cameraBlocked</span><span class="sxs-lookup"><span data-stu-id="896fb-178">cameraBlocked</span></span>|<span data-ttu-id="896fb-179">Booleano</span><span class="sxs-lookup"><span data-stu-id="896fb-179">Boolean</span></span>|<span data-ttu-id="896fb-180">Indica si se va a bloquear la cámara.</span><span class="sxs-lookup"><span data-stu-id="896fb-180">Indicates whether or not to block camera.</span></span>|
|<span data-ttu-id="896fb-181">cellularBlockWifiTethering</span><span class="sxs-lookup"><span data-stu-id="896fb-181">cellularBlockWifiTethering</span></span>|<span data-ttu-id="896fb-182">Booleano</span><span class="sxs-lookup"><span data-stu-id="896fb-182">Boolean</span></span>|<span data-ttu-id="896fb-183">Indica si se va a bloquear el tethering Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="896fb-183">Indicates whether or not to block Wi-Fi tethering.</span></span> <span data-ttu-id="896fb-184">No tiene impacto si se bloquea el Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="896fb-184">Has no impact if Wi-Fi is blocked.</span></span>|
|<span data-ttu-id="896fb-185">compliantAppsList</span><span class="sxs-lookup"><span data-stu-id="896fb-185">compliantAppsList</span></span>|<span data-ttu-id="896fb-186">Colección [appListItem](../resources/intune-deviceconfig-applistitem.md)</span><span class="sxs-lookup"><span data-stu-id="896fb-186">[appListItem](../resources/intune-deviceconfig-applistitem.md) collection</span></span>|<span data-ttu-id="896fb-187">Lista de aplicaciones en el cumplimiento (sea lista de permitidos o de bloqueados, controlado por CompliantAppListType).</span><span class="sxs-lookup"><span data-stu-id="896fb-187">List of apps in the compliance (either allow list or block list, controlled by CompliantAppListType).</span></span> <span data-ttu-id="896fb-188">Esta colección puede contener un máximo de 10 000 elementos.</span><span class="sxs-lookup"><span data-stu-id="896fb-188">This collection can contain a maximum of 10000 elements.</span></span>|
|<span data-ttu-id="896fb-189">compliantAppListType</span><span class="sxs-lookup"><span data-stu-id="896fb-189">compliantAppListType</span></span>|[<span data-ttu-id="896fb-190">appListType</span><span class="sxs-lookup"><span data-stu-id="896fb-190">appListType</span></span>](../resources/intune-deviceconfig-applisttype.md)|<span data-ttu-id="896fb-191">Lista que se encuentra en la AppComplianceList.</span><span class="sxs-lookup"><span data-stu-id="896fb-191">List that is in the AppComplianceList.</span></span> <span data-ttu-id="896fb-192">Los valores posibles son: `none`, `appsInListCompliant` y `appsNotInListCompliant`.</span><span class="sxs-lookup"><span data-stu-id="896fb-192">Possible values are: `none`, `appsInListCompliant`, `appsNotInListCompliant`.</span></span>|
|<span data-ttu-id="896fb-193">diagnosticDataBlockSubmission</span><span class="sxs-lookup"><span data-stu-id="896fb-193">diagnosticDataBlockSubmission</span></span>|<span data-ttu-id="896fb-194">Booleano</span><span class="sxs-lookup"><span data-stu-id="896fb-194">Boolean</span></span>|<span data-ttu-id="896fb-195">Indica si se va a bloquear el envío de datos de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="896fb-195">Indicates whether or not to block diagnostic data submission.</span></span>|
|<span data-ttu-id="896fb-196">emailBlockAddingAccounts</span><span class="sxs-lookup"><span data-stu-id="896fb-196">emailBlockAddingAccounts</span></span>|<span data-ttu-id="896fb-197">Booleano</span><span class="sxs-lookup"><span data-stu-id="896fb-197">Boolean</span></span>|<span data-ttu-id="896fb-198">Indica si se van a bloquear las cuentas de correo electrónico personalizadas.</span><span class="sxs-lookup"><span data-stu-id="896fb-198">Indicates whether or not to block custom email accounts.</span></span>|
|<span data-ttu-id="896fb-199">locationServicesBlocked</span><span class="sxs-lookup"><span data-stu-id="896fb-199">locationServicesBlocked</span></span>|<span data-ttu-id="896fb-200">Booleano</span><span class="sxs-lookup"><span data-stu-id="896fb-200">Boolean</span></span>|<span data-ttu-id="896fb-201">Indica si se van a bloquear los servicios de ubicación.</span><span class="sxs-lookup"><span data-stu-id="896fb-201">Indicates whether or not to block location services.</span></span>|
|<span data-ttu-id="896fb-202">microsoftAccountBlocked</span><span class="sxs-lookup"><span data-stu-id="896fb-202">microsoftAccountBlocked</span></span>|<span data-ttu-id="896fb-203">Booleano</span><span class="sxs-lookup"><span data-stu-id="896fb-203">Boolean</span></span>|<span data-ttu-id="896fb-204">Indica si se va a bloquear el uso de una cuenta de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="896fb-204">Indicates whether or not to block using a Microsoft Account.</span></span>|
|<span data-ttu-id="896fb-205">nfcBlocked</span><span class="sxs-lookup"><span data-stu-id="896fb-205">nfcBlocked</span></span>|<span data-ttu-id="896fb-206">Booleano</span><span class="sxs-lookup"><span data-stu-id="896fb-206">Boolean</span></span>|<span data-ttu-id="896fb-207">Indica si se va a bloquear la transmisión de datos en proximidad.</span><span class="sxs-lookup"><span data-stu-id="896fb-207">Indicates whether or not to block Near-Field Communication.</span></span>|
|<span data-ttu-id="896fb-208">passwordBlockSimple</span><span class="sxs-lookup"><span data-stu-id="896fb-208">passwordBlockSimple</span></span>|<span data-ttu-id="896fb-209">Booleano</span><span class="sxs-lookup"><span data-stu-id="896fb-209">Boolean</span></span>|<span data-ttu-id="896fb-210">Indica si se va a bloquear la sincronización del calendario.</span><span class="sxs-lookup"><span data-stu-id="896fb-210">Indicates whether or not to block syncing the calendar.</span></span>|
|<span data-ttu-id="896fb-211">passwordExpirationDays</span><span class="sxs-lookup"><span data-stu-id="896fb-211">passwordExpirationDays</span></span>|<span data-ttu-id="896fb-212">Int32</span><span class="sxs-lookup"><span data-stu-id="896fb-212">Int32</span></span>|<span data-ttu-id="896fb-213">Número de días antes de que expire la contraseña.</span><span class="sxs-lookup"><span data-stu-id="896fb-213">Number of days before the password expires.</span></span>|
|<span data-ttu-id="896fb-214">passwordMinimumLength</span><span class="sxs-lookup"><span data-stu-id="896fb-214">passwordMinimumLength</span></span>|<span data-ttu-id="896fb-215">Int32</span><span class="sxs-lookup"><span data-stu-id="896fb-215">Int32</span></span>|<span data-ttu-id="896fb-216">Longitud mínima de las contraseñas.</span><span class="sxs-lookup"><span data-stu-id="896fb-216">Minimum length of passwords.</span></span>|
|<span data-ttu-id="896fb-217">passwordMinutesOfInactivityBeforeScreenTimeout</span><span class="sxs-lookup"><span data-stu-id="896fb-217">passwordMinutesOfInactivityBeforeScreenTimeout</span></span>|<span data-ttu-id="896fb-218">Int32</span><span class="sxs-lookup"><span data-stu-id="896fb-218">Int32</span></span>|<span data-ttu-id="896fb-219">Minutos de inactividad antes de que se agote el tiempo de espera de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="896fb-219">Minutes of inactivity before screen timeout.</span></span>|
|<span data-ttu-id="896fb-220">passwordMinimumCharacterSetCount</span><span class="sxs-lookup"><span data-stu-id="896fb-220">passwordMinimumCharacterSetCount</span></span>|<span data-ttu-id="896fb-221">Int32</span><span class="sxs-lookup"><span data-stu-id="896fb-221">Int32</span></span>|<span data-ttu-id="896fb-222">Número de juegos de caracteres que debe contener una contraseña.</span><span class="sxs-lookup"><span data-stu-id="896fb-222">Number of character sets a password must contain.</span></span>|
|<span data-ttu-id="896fb-223">passwordPreviousPasswordBlockCount</span><span class="sxs-lookup"><span data-stu-id="896fb-223">passwordPreviousPasswordBlockCount</span></span>|<span data-ttu-id="896fb-224">Int32</span><span class="sxs-lookup"><span data-stu-id="896fb-224">Int32</span></span>|<span data-ttu-id="896fb-225">Número de contraseñas anteriores que bloquear.</span><span class="sxs-lookup"><span data-stu-id="896fb-225">Number of previous passwords to block.</span></span> <span data-ttu-id="896fb-226">Valores válidos de 0 a 24</span><span class="sxs-lookup"><span data-stu-id="896fb-226">Valid values 0 to 24</span></span>|
|<span data-ttu-id="896fb-227">passwordSignInFailureCountBeforeFactoryReset</span><span class="sxs-lookup"><span data-stu-id="896fb-227">passwordSignInFailureCountBeforeFactoryReset</span></span>|<span data-ttu-id="896fb-228">Int32</span><span class="sxs-lookup"><span data-stu-id="896fb-228">Int32</span></span>|<span data-ttu-id="896fb-229">Número de errores de inicio de sesión permitidos antes del restablecimiento de fábrica.</span><span class="sxs-lookup"><span data-stu-id="896fb-229">Number of sign in failures allowed before factory reset.</span></span>|
|<span data-ttu-id="896fb-230">passwordRequiredType</span><span class="sxs-lookup"><span data-stu-id="896fb-230">passwordRequiredType</span></span>|[<span data-ttu-id="896fb-231">requiredPasswordType</span><span class="sxs-lookup"><span data-stu-id="896fb-231">requiredPasswordType</span></span>](../resources/intune-deviceconfig-requiredpasswordtype.md)|<span data-ttu-id="896fb-232">Tipo de contraseña que es necesario.</span><span class="sxs-lookup"><span data-stu-id="896fb-232">Password type that is required.</span></span> <span data-ttu-id="896fb-233">Los valores posibles son: `deviceDefault`, `alphanumeric` y `numeric`.</span><span class="sxs-lookup"><span data-stu-id="896fb-233">Possible values are: `deviceDefault`, `alphanumeric`, `numeric`.</span></span>|
|<span data-ttu-id="896fb-234">passwordRequired</span><span class="sxs-lookup"><span data-stu-id="896fb-234">passwordRequired</span></span>|<span data-ttu-id="896fb-235">Booleano</span><span class="sxs-lookup"><span data-stu-id="896fb-235">Boolean</span></span>|<span data-ttu-id="896fb-236">Indica si se va a requerir una contraseña.</span><span class="sxs-lookup"><span data-stu-id="896fb-236">Indicates whether or not to require a password.</span></span>|
|<span data-ttu-id="896fb-237">screenCaptureBlocked</span><span class="sxs-lookup"><span data-stu-id="896fb-237">screenCaptureBlocked</span></span>|<span data-ttu-id="896fb-238">Booleano</span><span class="sxs-lookup"><span data-stu-id="896fb-238">Boolean</span></span>|<span data-ttu-id="896fb-239">Indica si se van a impedir las capturas de pantalla.</span><span class="sxs-lookup"><span data-stu-id="896fb-239">Indicates whether or not to block screenshots.</span></span>|
|<span data-ttu-id="896fb-240">storageBlockRemovableStorage</span><span class="sxs-lookup"><span data-stu-id="896fb-240">storageBlockRemovableStorage</span></span>|<span data-ttu-id="896fb-241">Booleano</span><span class="sxs-lookup"><span data-stu-id="896fb-241">Boolean</span></span>|<span data-ttu-id="896fb-242">Indica si se va a impedir el almacenamiento extraíble.</span><span class="sxs-lookup"><span data-stu-id="896fb-242">Indicates whether or not to block removable storage.</span></span>|
|<span data-ttu-id="896fb-243">storageRequireEncryption</span><span class="sxs-lookup"><span data-stu-id="896fb-243">storageRequireEncryption</span></span>|<span data-ttu-id="896fb-244">Booleano</span><span class="sxs-lookup"><span data-stu-id="896fb-244">Boolean</span></span>|<span data-ttu-id="896fb-245">Indica si se va a requerir cifrado.</span><span class="sxs-lookup"><span data-stu-id="896fb-245">Indicates whether or not to require encryption.</span></span>|
|<span data-ttu-id="896fb-246">webBrowserBlocked</span><span class="sxs-lookup"><span data-stu-id="896fb-246">webBrowserBlocked</span></span>|<span data-ttu-id="896fb-247">Booleano</span><span class="sxs-lookup"><span data-stu-id="896fb-247">Boolean</span></span>|<span data-ttu-id="896fb-248">Indica si se va a bloquear el explorador web.</span><span class="sxs-lookup"><span data-stu-id="896fb-248">Indicates whether or not to block the web browser.</span></span>|
|<span data-ttu-id="896fb-249">wifiBlocked</span><span class="sxs-lookup"><span data-stu-id="896fb-249">wifiBlocked</span></span>|<span data-ttu-id="896fb-250">Booleano</span><span class="sxs-lookup"><span data-stu-id="896fb-250">Boolean</span></span>|<span data-ttu-id="896fb-251">Indica si se va a bloquear el uso de Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="896fb-251">Indicates whether or not to block Wi-Fi.</span></span>|
|<span data-ttu-id="896fb-252">wifiBlockAutomaticConnectHotspots</span><span class="sxs-lookup"><span data-stu-id="896fb-252">wifiBlockAutomaticConnectHotspots</span></span>|<span data-ttu-id="896fb-253">Booleano</span><span class="sxs-lookup"><span data-stu-id="896fb-253">Boolean</span></span>|<span data-ttu-id="896fb-254">Indica si se va a bloquear automáticamente la conexión a zonas Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="896fb-254">Indicates whether or not to block automatically connecting to Wi-Fi hotspots.</span></span> <span data-ttu-id="896fb-255">No tiene impacto si se bloquea el Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="896fb-255">Has no impact if Wi-Fi is blocked.</span></span>|
|<span data-ttu-id="896fb-256">wifiBlockHotspotReporting</span><span class="sxs-lookup"><span data-stu-id="896fb-256">wifiBlockHotspotReporting</span></span>|<span data-ttu-id="896fb-257">Booleano</span><span class="sxs-lookup"><span data-stu-id="896fb-257">Boolean</span></span>|<span data-ttu-id="896fb-258">Indica si se van a bloquear los informes de zona Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="896fb-258">Indicates whether or not to block Wi-Fi hotspot reporting.</span></span> <span data-ttu-id="896fb-259">No tiene impacto si se bloquea el Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="896fb-259">Has no impact if Wi-Fi is blocked.</span></span>|
|<span data-ttu-id="896fb-260">windowsStoreBlocked</span><span class="sxs-lookup"><span data-stu-id="896fb-260">windowsStoreBlocked</span></span>|<span data-ttu-id="896fb-261">Booleano</span><span class="sxs-lookup"><span data-stu-id="896fb-261">Boolean</span></span>|<span data-ttu-id="896fb-262">Indica si se va a bloquear la Tienda Windows.</span><span class="sxs-lookup"><span data-stu-id="896fb-262">Indicates whether or not to block the Windows Store.</span></span>|



## <a name="response"></a><span data-ttu-id="896fb-263">Respuesta</span><span class="sxs-lookup"><span data-stu-id="896fb-263">Response</span></span>
<span data-ttu-id="896fb-264">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [windowsPhone81GeneralConfiguration](../resources/intune-deviceconfig-windowsphone81generalconfiguration.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="896fb-264">If successful, this method returns a `200 OK` response code and an updated [windowsPhone81GeneralConfiguration](../resources/intune-deviceconfig-windowsphone81generalconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="896fb-265">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="896fb-265">Example</span></span>
### <a name="request"></a><span data-ttu-id="896fb-266">Solicitud</span><span class="sxs-lookup"><span data-stu-id="896fb-266">Request</span></span>
<span data-ttu-id="896fb-267">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="896fb-267">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations/{deviceConfigurationId}
Content-type: application/json
Content-length: 1544

{
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "roleScopeTagIds": [
    "Role Scope Tag Ids value"
  ],
  "supportsScopeTags": true,
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

### <a name="response"></a><span data-ttu-id="896fb-268">Respuesta</span><span class="sxs-lookup"><span data-stu-id="896fb-268">Response</span></span>
<span data-ttu-id="896fb-p119">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="896fb-p119">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1725

{
  "@odata.type": "#microsoft.graph.windowsPhone81GeneralConfiguration",
  "id": "f5e0e34d-e34d-f5e0-4de3-e0f54de3e0f5",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "roleScopeTagIds": [
    "Role Scope Tag Ids value"
  ],
  "supportsScopeTags": true,
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




