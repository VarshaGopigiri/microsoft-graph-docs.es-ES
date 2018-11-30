---
title: Actualizar macOSGeneralDeviceConfiguration
description: Actualice las propiedades de un objeto macOSGeneralDeviceConfiguration.
ms.openlocfilehash: aad4f0ed0c0b4d30842e2e643526c0d42ff4f1a3
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088293"
---
# <a name="update-macosgeneraldeviceconfiguration"></a><span data-ttu-id="1d463-103">Actualizar macOSGeneralDeviceConfiguration</span><span class="sxs-lookup"><span data-stu-id="1d463-103">Update macOSGeneralDeviceConfiguration</span></span>

> <span data-ttu-id="1d463-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="1d463-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="1d463-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="1d463-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="1d463-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="1d463-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="1d463-107">Actualice las propiedades de un objeto [macOSGeneralDeviceConfiguration](../resources/intune-deviceconfig-macosgeneraldeviceconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="1d463-107">Update the properties of a [macOSGeneralDeviceConfiguration](../resources/intune-deviceconfig-macosgeneraldeviceconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="1d463-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="1d463-108">Prerequisites</span></span>
<span data-ttu-id="1d463-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="1d463-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="1d463-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="1d463-111">Permission type</span></span>|<span data-ttu-id="1d463-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="1d463-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="1d463-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="1d463-113">Delegated (work or school account)</span></span>|<span data-ttu-id="1d463-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="1d463-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="1d463-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="1d463-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="1d463-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1d463-116">Not supported.</span></span>|
|<span data-ttu-id="1d463-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="1d463-117">Application</span></span>|<span data-ttu-id="1d463-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1d463-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="1d463-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="1d463-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/groupAssignments/{deviceConfigurationGroupAssignmentId}/deviceConfiguration
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsDomainJoinConfiguration/networkAccessConfigurations/{deviceConfigurationId}
```

## <a name="request-headers"></a><span data-ttu-id="1d463-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="1d463-120">Request headers</span></span>
|<span data-ttu-id="1d463-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1d463-121">Header</span></span>|<span data-ttu-id="1d463-122">Valor</span><span class="sxs-lookup"><span data-stu-id="1d463-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="1d463-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="1d463-123">Authorization</span></span>|<span data-ttu-id="1d463-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="1d463-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="1d463-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="1d463-125">Accept</span></span>|<span data-ttu-id="1d463-126">application/json</span><span class="sxs-lookup"><span data-stu-id="1d463-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="1d463-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="1d463-127">Request body</span></span>
<span data-ttu-id="1d463-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto [macOSGeneralDeviceConfiguration](../resources/intune-deviceconfig-macosgeneraldeviceconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="1d463-128">In the request body, supply a JSON representation for the [macOSGeneralDeviceConfiguration](../resources/intune-deviceconfig-macosgeneraldeviceconfiguration.md) object.</span></span>

<span data-ttu-id="1d463-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [macOSGeneralDeviceConfiguration](../resources/intune-deviceconfig-macosgeneraldeviceconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="1d463-129">The following table shows the properties that are required when you create the [macOSGeneralDeviceConfiguration](../resources/intune-deviceconfig-macosgeneraldeviceconfiguration.md).</span></span>

|<span data-ttu-id="1d463-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="1d463-130">Property</span></span>|<span data-ttu-id="1d463-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="1d463-131">Type</span></span>|<span data-ttu-id="1d463-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="1d463-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="1d463-133">id</span><span class="sxs-lookup"><span data-stu-id="1d463-133">id</span></span>|<span data-ttu-id="1d463-134">String</span><span class="sxs-lookup"><span data-stu-id="1d463-134">String</span></span>|<span data-ttu-id="1d463-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="1d463-135">Key of the entity.</span></span> <span data-ttu-id="1d463-136">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="1d463-136">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="1d463-137">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="1d463-137">lastModifiedDateTime</span></span>|<span data-ttu-id="1d463-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="1d463-138">DateTimeOffset</span></span>|<span data-ttu-id="1d463-139">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="1d463-139">DateTime the object was last modified.</span></span> <span data-ttu-id="1d463-140">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="1d463-140">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="1d463-141">roleScopeTagIds</span><span class="sxs-lookup"><span data-stu-id="1d463-141">roleScopeTagIds</span></span>|<span data-ttu-id="1d463-142">Colección String</span><span class="sxs-lookup"><span data-stu-id="1d463-142">String collection</span></span>|<span data-ttu-id="1d463-143">Lista de etiquetas de ámbito para esta instancia de entidad.</span><span class="sxs-lookup"><span data-stu-id="1d463-143">List of Scope Tags for this Entity instance.</span></span> <span data-ttu-id="1d463-144">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="1d463-144">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="1d463-145">supportsScopeTags</span><span class="sxs-lookup"><span data-stu-id="1d463-145">supportsScopeTags</span></span>|<span data-ttu-id="1d463-146">Booleano</span><span class="sxs-lookup"><span data-stu-id="1d463-146">Boolean</span></span>|<span data-ttu-id="1d463-147">Indica si la configuración del dispositivo subyacente admite la asignación de etiquetas de ámbito.</span><span class="sxs-lookup"><span data-stu-id="1d463-147">Indicates whether or not the underlying Device Configuration supports the assignment of scope tags.</span></span> <span data-ttu-id="1d463-148">No se permite la asignación a la propiedad ScopeTags cuando este valor es false y entidades no estará visibles para los usuarios con ámbito.</span><span class="sxs-lookup"><span data-stu-id="1d463-148">Assigning to the ScopeTags property is not allowed when this value is false and entities will not be visible to scoped users.</span></span> <span data-ttu-id="1d463-149">Esto se produce para las directivas de heredado creadas en Silverlight y se puede resolver por eliminar y volver a crear la directiva en el Portal de Azure.</span><span class="sxs-lookup"><span data-stu-id="1d463-149">This occurs for Legacy policies created in Silverlight and can be resolved by deleting and recreating the policy in the Azure Portal.</span></span> <span data-ttu-id="1d463-150">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="1d463-150">This property is read-only.</span></span> <span data-ttu-id="1d463-151">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="1d463-151">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="1d463-152">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="1d463-152">createdDateTime</span></span>|<span data-ttu-id="1d463-153">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="1d463-153">DateTimeOffset</span></span>|<span data-ttu-id="1d463-154">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="1d463-154">DateTime the object was created.</span></span> <span data-ttu-id="1d463-155">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="1d463-155">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="1d463-156">descripción</span><span class="sxs-lookup"><span data-stu-id="1d463-156">description</span></span>|<span data-ttu-id="1d463-157">String</span><span class="sxs-lookup"><span data-stu-id="1d463-157">String</span></span>|<span data-ttu-id="1d463-158">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1d463-158">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="1d463-159">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="1d463-159">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="1d463-160">displayName</span><span class="sxs-lookup"><span data-stu-id="1d463-160">displayName</span></span>|<span data-ttu-id="1d463-161">String</span><span class="sxs-lookup"><span data-stu-id="1d463-161">String</span></span>|<span data-ttu-id="1d463-162">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1d463-162">Admin provided name of the device configuration.</span></span> <span data-ttu-id="1d463-163">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="1d463-163">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="1d463-164">version</span><span class="sxs-lookup"><span data-stu-id="1d463-164">version</span></span>|<span data-ttu-id="1d463-165">Int32</span><span class="sxs-lookup"><span data-stu-id="1d463-165">Int32</span></span>|<span data-ttu-id="1d463-166">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1d463-166">Version of the device configuration.</span></span> <span data-ttu-id="1d463-167">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="1d463-167">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="1d463-168">compliantAppsList</span><span class="sxs-lookup"><span data-stu-id="1d463-168">compliantAppsList</span></span>|<span data-ttu-id="1d463-169">Colección [appListItem](../resources/intune-deviceconfig-applistitem.md)</span><span class="sxs-lookup"><span data-stu-id="1d463-169">[appListItem](../resources/intune-deviceconfig-applistitem.md) collection</span></span>|<span data-ttu-id="1d463-170">Lista de aplicaciones en el cumplimiento (sea lista de permitidos o de bloqueados, controlado por CompliantAppListType).</span><span class="sxs-lookup"><span data-stu-id="1d463-170">List of apps in the compliance (either allow list or block list, controlled by CompliantAppListType).</span></span> <span data-ttu-id="1d463-171">Esta colección puede contener un máximo de 10 000 elementos.</span><span class="sxs-lookup"><span data-stu-id="1d463-171">This collection can contain a maximum of 10000 elements.</span></span>|
|<span data-ttu-id="1d463-172">compliantAppListType</span><span class="sxs-lookup"><span data-stu-id="1d463-172">compliantAppListType</span></span>|[<span data-ttu-id="1d463-173">appListType</span><span class="sxs-lookup"><span data-stu-id="1d463-173">appListType</span></span>](../resources/intune-deviceconfig-applisttype.md)|<span data-ttu-id="1d463-174">Lista que se encuentra en la CompliantAppsList.</span><span class="sxs-lookup"><span data-stu-id="1d463-174">List that is in the CompliantAppsList.</span></span> <span data-ttu-id="1d463-175">Los valores posibles son: `none`, `appsInListCompliant` y `appsNotInListCompliant`.</span><span class="sxs-lookup"><span data-stu-id="1d463-175">Possible values are: `none`, `appsInListCompliant`, `appsNotInListCompliant`.</span></span>|
|<span data-ttu-id="1d463-176">emailInDomainSuffixes</span><span class="sxs-lookup"><span data-stu-id="1d463-176">emailInDomainSuffixes</span></span>|<span data-ttu-id="1d463-177">Colección String</span><span class="sxs-lookup"><span data-stu-id="1d463-177">String collection</span></span>|<span data-ttu-id="1d463-178">Una dirección de correo electrónico que carezca de un sufijo que coincida con cualquiera de estas cadenas se considerará fuera de dominio.</span><span class="sxs-lookup"><span data-stu-id="1d463-178">An email address lacking a suffix that matches any of these strings will be considered out-of-domain.</span></span>|
|<span data-ttu-id="1d463-179">passwordBlockSimple</span><span class="sxs-lookup"><span data-stu-id="1d463-179">passwordBlockSimple</span></span>|<span data-ttu-id="1d463-180">Booleano</span><span class="sxs-lookup"><span data-stu-id="1d463-180">Boolean</span></span>|<span data-ttu-id="1d463-181">Bloquear contraseñas sencillas.</span><span class="sxs-lookup"><span data-stu-id="1d463-181">Block simple passwords.</span></span>|
|<span data-ttu-id="1d463-182">passwordExpirationDays</span><span class="sxs-lookup"><span data-stu-id="1d463-182">passwordExpirationDays</span></span>|<span data-ttu-id="1d463-183">Int32</span><span class="sxs-lookup"><span data-stu-id="1d463-183">Int32</span></span>|<span data-ttu-id="1d463-184">Número de días antes de que expire la contraseña.</span><span class="sxs-lookup"><span data-stu-id="1d463-184">Number of days before the password expires.</span></span>|
|<span data-ttu-id="1d463-185">passwordMinimumCharacterSetCount</span><span class="sxs-lookup"><span data-stu-id="1d463-185">passwordMinimumCharacterSetCount</span></span>|<span data-ttu-id="1d463-186">Int32</span><span class="sxs-lookup"><span data-stu-id="1d463-186">Int32</span></span>|<span data-ttu-id="1d463-187">Número de juegos de caracteres que debe contener una contraseña.</span><span class="sxs-lookup"><span data-stu-id="1d463-187">Number of character sets a password must contain.</span></span> <span data-ttu-id="1d463-188">Valores válidos de 0 a 4.</span><span class="sxs-lookup"><span data-stu-id="1d463-188">Valid values 0 to 4</span></span>|
|<span data-ttu-id="1d463-189">passwordMinimumLength</span><span class="sxs-lookup"><span data-stu-id="1d463-189">passwordMinimumLength</span></span>|<span data-ttu-id="1d463-190">Int32</span><span class="sxs-lookup"><span data-stu-id="1d463-190">Int32</span></span>|<span data-ttu-id="1d463-191">Longitud mínima de las contraseñas.</span><span class="sxs-lookup"><span data-stu-id="1d463-191">Minimum length of passwords.</span></span>|
|<span data-ttu-id="1d463-192">passwordMinutesOfInactivityBeforeLock</span><span class="sxs-lookup"><span data-stu-id="1d463-192">passwordMinutesOfInactivityBeforeLock</span></span>|<span data-ttu-id="1d463-193">Int32</span><span class="sxs-lookup"><span data-stu-id="1d463-193">Int32</span></span>|<span data-ttu-id="1d463-194">Minutos de inactividad antes de que sea necesaria una contraseña.</span><span class="sxs-lookup"><span data-stu-id="1d463-194">Minutes of inactivity required before a password is required.</span></span>|
|<span data-ttu-id="1d463-195">passwordMinutesOfInactivityBeforeScreenTimeout</span><span class="sxs-lookup"><span data-stu-id="1d463-195">passwordMinutesOfInactivityBeforeScreenTimeout</span></span>|<span data-ttu-id="1d463-196">Int32</span><span class="sxs-lookup"><span data-stu-id="1d463-196">Int32</span></span>|<span data-ttu-id="1d463-197">Minutos de inactividad que se requieren antes de que se agote el tiempo de espera de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="1d463-197">Minutes of inactivity required before the screen times out.</span></span>|
|<span data-ttu-id="1d463-198">passwordPreviousPasswordBlockCount</span><span class="sxs-lookup"><span data-stu-id="1d463-198">passwordPreviousPasswordBlockCount</span></span>|<span data-ttu-id="1d463-199">Int32</span><span class="sxs-lookup"><span data-stu-id="1d463-199">Int32</span></span>|<span data-ttu-id="1d463-200">Número de contraseñas anteriores que bloquear.</span><span class="sxs-lookup"><span data-stu-id="1d463-200">Number of previous passwords to block.</span></span>|
|<span data-ttu-id="1d463-201">passwordRequiredType</span><span class="sxs-lookup"><span data-stu-id="1d463-201">passwordRequiredType</span></span>|[<span data-ttu-id="1d463-202">requiredPasswordType</span><span class="sxs-lookup"><span data-stu-id="1d463-202">requiredPasswordType</span></span>](../resources/intune-deviceconfig-requiredpasswordtype.md)|<span data-ttu-id="1d463-203">Tipo de contraseña que es necesario.</span><span class="sxs-lookup"><span data-stu-id="1d463-203">Type of password that is required.</span></span> <span data-ttu-id="1d463-204">Los valores posibles son: `deviceDefault`, `alphanumeric` y `numeric`.</span><span class="sxs-lookup"><span data-stu-id="1d463-204">Possible values are: `deviceDefault`, `alphanumeric`, `numeric`.</span></span>|
|<span data-ttu-id="1d463-205">passwordRequired</span><span class="sxs-lookup"><span data-stu-id="1d463-205">passwordRequired</span></span>|<span data-ttu-id="1d463-206">Booleano</span><span class="sxs-lookup"><span data-stu-id="1d463-206">Boolean</span></span>|<span data-ttu-id="1d463-207">Si quiere requerir o no una contraseña.</span><span class="sxs-lookup"><span data-stu-id="1d463-207">Whether or not to require a password.</span></span>|
|<span data-ttu-id="1d463-208">keychainBlockCloudSync</span><span class="sxs-lookup"><span data-stu-id="1d463-208">keychainBlockCloudSync</span></span>|<span data-ttu-id="1d463-209">Booleano</span><span class="sxs-lookup"><span data-stu-id="1d463-209">Boolean</span></span>|<span data-ttu-id="1d463-210">Indica si está o no iCloud llaves sincronización bloqueados (Mac OS 10.12 y versiones posteriores).</span><span class="sxs-lookup"><span data-stu-id="1d463-210">Indicates whether or not iCloud keychain synchronization is blocked (macOS 10.12 and later).</span></span>|
|<span data-ttu-id="1d463-211">airPrintBlocked</span><span class="sxs-lookup"><span data-stu-id="1d463-211">airPrintBlocked</span></span>|<span data-ttu-id="1d463-212">Booleano</span><span class="sxs-lookup"><span data-stu-id="1d463-212">Boolean</span></span>|<span data-ttu-id="1d463-213">Indica si está o no AirPrint bloqueados (Mac OS 10.12 y versiones posteriores).</span><span class="sxs-lookup"><span data-stu-id="1d463-213">Indicates whether or not AirPrint is blocked (macOS 10.12 and later).</span></span>|
|<span data-ttu-id="1d463-214">airPrintForceTrustedTLS</span><span class="sxs-lookup"><span data-stu-id="1d463-214">airPrintForceTrustedTLS</span></span>|<span data-ttu-id="1d463-215">Booleano</span><span class="sxs-lookup"><span data-stu-id="1d463-215">Boolean</span></span>|<span data-ttu-id="1d463-216">Indica si los certificados de confianza son necesarios para la comunicación de impresión de TLS (Mac OS 10.13 y versiones posteriores).</span><span class="sxs-lookup"><span data-stu-id="1d463-216">Indicates if trusted certificates are required for TLS printing communication (macOS 10.13 and later).</span></span>|
|<span data-ttu-id="1d463-217">airPrintBlockiBeaconDiscovery</span><span class="sxs-lookup"><span data-stu-id="1d463-217">airPrintBlockiBeaconDiscovery</span></span>|<span data-ttu-id="1d463-218">Booleano</span><span class="sxs-lookup"><span data-stu-id="1d463-218">Boolean</span></span>|<span data-ttu-id="1d463-219">Indica si se bloquea en iBeacon detección de impresoras AirPrint.</span><span class="sxs-lookup"><span data-stu-id="1d463-219">Indicates whether or not iBeacon discovery of AirPrint printers is blocked.</span></span> <span data-ttu-id="1d463-220">Esto evita falsas balizas de AirPrint Bluetooth de suplantación de identidad para el tráfico de red (Mac OS 10.3 y versiones posteriores).</span><span class="sxs-lookup"><span data-stu-id="1d463-220">This prevents spurious AirPrint Bluetooth beacons from phishing for network traffic (macOS 10.3 and later).</span></span>|
|<span data-ttu-id="1d463-221">safariBlockAutofill</span><span class="sxs-lookup"><span data-stu-id="1d463-221">safariBlockAutofill</span></span>|<span data-ttu-id="1d463-222">Booleano</span><span class="sxs-lookup"><span data-stu-id="1d463-222">Boolean</span></span>|<span data-ttu-id="1d463-223">Indica si se va a impedir que el usuario use la opción de autorrellenado en Safari.</span><span class="sxs-lookup"><span data-stu-id="1d463-223">Indicates whether or not to block the user from using Auto fill in Safari.</span></span>|
|<span data-ttu-id="1d463-224">cameraBlocked</span><span class="sxs-lookup"><span data-stu-id="1d463-224">cameraBlocked</span></span>|<span data-ttu-id="1d463-225">Booleano</span><span class="sxs-lookup"><span data-stu-id="1d463-225">Boolean</span></span>|<span data-ttu-id="1d463-226">Indica si se va a impedir que el usuario obtenga acceso a la cámara del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1d463-226">Indicates whether or not to block the user from accessing the camera of the device.</span></span>|
|<span data-ttu-id="1d463-227">iTunesBlockMusicService</span><span class="sxs-lookup"><span data-stu-id="1d463-227">iTunesBlockMusicService</span></span>|<span data-ttu-id="1d463-228">Booleano</span><span class="sxs-lookup"><span data-stu-id="1d463-228">Boolean</span></span>|<span data-ttu-id="1d463-229">Indica si se deben bloquear el servicio de música y revertir la aplicación de música en modo clásico.</span><span class="sxs-lookup"><span data-stu-id="1d463-229">Indicates whether or not to block Music service and revert Music app to classic mode.</span></span>|
|<span data-ttu-id="1d463-230">spotlightBlockInternetResults</span><span class="sxs-lookup"><span data-stu-id="1d463-230">spotlightBlockInternetResults</span></span>|<span data-ttu-id="1d463-231">Booleano</span><span class="sxs-lookup"><span data-stu-id="1d463-231">Boolean</span></span>|<span data-ttu-id="1d463-232">Indica si se deben bloquear aspectos destacados de devolver los resultados de una búsqueda de Internet.</span><span class="sxs-lookup"><span data-stu-id="1d463-232">Indicates whether or not to block Spotlight from returning any results from an Internet search.</span></span>|
|<span data-ttu-id="1d463-233">keyboardBlockDictation</span><span class="sxs-lookup"><span data-stu-id="1d463-233">keyboardBlockDictation</span></span>|<span data-ttu-id="1d463-234">Booleano</span><span class="sxs-lookup"><span data-stu-id="1d463-234">Boolean</span></span>|<span data-ttu-id="1d463-235">Indica si desea impedir que el usuario usa la entrada dictation o no.</span><span class="sxs-lookup"><span data-stu-id="1d463-235">Indicates whether or not to block the user from using dictation input.</span></span>|
|<span data-ttu-id="1d463-236">definitionLookupBlocked</span><span class="sxs-lookup"><span data-stu-id="1d463-236">definitionLookupBlocked</span></span>|<span data-ttu-id="1d463-237">Booleano</span><span class="sxs-lookup"><span data-stu-id="1d463-237">Boolean</span></span>|<span data-ttu-id="1d463-238">Indica si se deben bloquear la búsqueda de definición.</span><span class="sxs-lookup"><span data-stu-id="1d463-238">Indicates whether or not to block definition lookup.</span></span>|
|<span data-ttu-id="1d463-239">appleWatchBlockAutoUnlock</span><span class="sxs-lookup"><span data-stu-id="1d463-239">appleWatchBlockAutoUnlock</span></span>|<span data-ttu-id="1d463-240">Booleano</span><span class="sxs-lookup"><span data-stu-id="1d463-240">Boolean</span></span>|<span data-ttu-id="1d463-241">Indica si o a los usuarios de bloque de desbloqueo de su Mac con Apple Watch.</span><span class="sxs-lookup"><span data-stu-id="1d463-241">Indicates whether or to block users from unlocking their Mac with Apple Watch.</span></span>|
|<span data-ttu-id="1d463-242">iTunesBlockFileSharing</span><span class="sxs-lookup"><span data-stu-id="1d463-242">iTunesBlockFileSharing</span></span>|<span data-ttu-id="1d463-243">Booleano</span><span class="sxs-lookup"><span data-stu-id="1d463-243">Boolean</span></span>|<span data-ttu-id="1d463-244">Indica si está o no esta opción Bloquear los archivos de bienestar transfiere mediante iTunes.</span><span class="sxs-lookup"><span data-stu-id="1d463-244">Indicates whether or not to block files from being transferred using iTunes.</span></span>|
|<span data-ttu-id="1d463-245">iCloudBlockDocumentSync</span><span class="sxs-lookup"><span data-stu-id="1d463-245">iCloudBlockDocumentSync</span></span>|<span data-ttu-id="1d463-246">Booleano</span><span class="sxs-lookup"><span data-stu-id="1d463-246">Boolean</span></span>|<span data-ttu-id="1d463-247">Indica si se va a impedir la sincronización de documentos de iCloud.</span><span class="sxs-lookup"><span data-stu-id="1d463-247">Indicates whether or not to block iCloud document sync.</span></span>|
|<span data-ttu-id="1d463-248">iCloudBlockMail</span><span class="sxs-lookup"><span data-stu-id="1d463-248">iCloudBlockMail</span></span>|<span data-ttu-id="1d463-249">Booleano</span><span class="sxs-lookup"><span data-stu-id="1d463-249">Boolean</span></span>|<span data-ttu-id="1d463-250">Indica si se deben bloquear iCloud de sincronización de correo.</span><span class="sxs-lookup"><span data-stu-id="1d463-250">Indicates whether or not to block iCloud from syncing mail.</span></span>|
|<span data-ttu-id="1d463-251">iCloudBlockAddressBook</span><span class="sxs-lookup"><span data-stu-id="1d463-251">iCloudBlockAddressBook</span></span>|<span data-ttu-id="1d463-252">Booleano</span><span class="sxs-lookup"><span data-stu-id="1d463-252">Boolean</span></span>|<span data-ttu-id="1d463-253">Indica si se deben bloquear iCloud de sincronización de contactos.</span><span class="sxs-lookup"><span data-stu-id="1d463-253">Indicates whether or not to block iCloud from syncing contacts.</span></span>|
|<span data-ttu-id="1d463-254">iCloudBlockCalendar</span><span class="sxs-lookup"><span data-stu-id="1d463-254">iCloudBlockCalendar</span></span>|<span data-ttu-id="1d463-255">Booleano</span><span class="sxs-lookup"><span data-stu-id="1d463-255">Boolean</span></span>|<span data-ttu-id="1d463-256">Indica si se deben bloquear iCloud sincronización calendarios de.</span><span class="sxs-lookup"><span data-stu-id="1d463-256">Indicates whether or not to block iCloud from syncing calendars.</span></span>|
|<span data-ttu-id="1d463-257">iCloudBlockReminders</span><span class="sxs-lookup"><span data-stu-id="1d463-257">iCloudBlockReminders</span></span>|<span data-ttu-id="1d463-258">Booleano</span><span class="sxs-lookup"><span data-stu-id="1d463-258">Boolean</span></span>|<span data-ttu-id="1d463-259">Indica si se deben bloquear iCloud sincronización avisos de.</span><span class="sxs-lookup"><span data-stu-id="1d463-259">Indicates whether or not to block iCloud from syncing reminders.</span></span>|
|<span data-ttu-id="1d463-260">iCloudBlockBookmarks</span><span class="sxs-lookup"><span data-stu-id="1d463-260">iCloudBlockBookmarks</span></span>|<span data-ttu-id="1d463-261">Booleano</span><span class="sxs-lookup"><span data-stu-id="1d463-261">Boolean</span></span>|<span data-ttu-id="1d463-262">Indica si se deben bloquear iCloud sincronización marcadores de.</span><span class="sxs-lookup"><span data-stu-id="1d463-262">Indicates whether or not to block iCloud from syncing bookmarks.</span></span>|
|<span data-ttu-id="1d463-263">iCloudBlockNotes</span><span class="sxs-lookup"><span data-stu-id="1d463-263">iCloudBlockNotes</span></span>|<span data-ttu-id="1d463-264">Booleano</span><span class="sxs-lookup"><span data-stu-id="1d463-264">Boolean</span></span>|<span data-ttu-id="1d463-265">Indica si se deben bloquear iCloud de sincronización de notas.</span><span class="sxs-lookup"><span data-stu-id="1d463-265">Indicates whether or not to block iCloud from syncing notes.</span></span>|
|<span data-ttu-id="1d463-266">airDropBlocked</span><span class="sxs-lookup"><span data-stu-id="1d463-266">airDropBlocked</span></span>|<span data-ttu-id="1d463-267">Booleano</span><span class="sxs-lookup"><span data-stu-id="1d463-267">Boolean</span></span>|<span data-ttu-id="1d463-268">Indica si se va a permitir AirDrop o no.</span><span class="sxs-lookup"><span data-stu-id="1d463-268">Indicates whether or not to allow AirDrop.</span></span>|
|<span data-ttu-id="1d463-269">passwordBlockModification</span><span class="sxs-lookup"><span data-stu-id="1d463-269">passwordBlockModification</span></span>|<span data-ttu-id="1d463-270">Booleano</span><span class="sxs-lookup"><span data-stu-id="1d463-270">Boolean</span></span>|<span data-ttu-id="1d463-271">Indica si se va a permitir la modificación del código de acceso o no.</span><span class="sxs-lookup"><span data-stu-id="1d463-271">Indicates whether or not to allow passcode modification.</span></span>|
|<span data-ttu-id="1d463-272">passwordBlockFingerprintUnlock</span><span class="sxs-lookup"><span data-stu-id="1d463-272">passwordBlockFingerprintUnlock</span></span>|<span data-ttu-id="1d463-273">Booleano</span><span class="sxs-lookup"><span data-stu-id="1d463-273">Boolean</span></span>|<span data-ttu-id="1d463-274">Indica si se va a impedir el desbloqueo por huella dactilar.</span><span class="sxs-lookup"><span data-stu-id="1d463-274">Indicates whether or not to block fingerprint unlock.</span></span>|



## <a name="response"></a><span data-ttu-id="1d463-275">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1d463-275">Response</span></span>
<span data-ttu-id="1d463-276">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [macOSGeneralDeviceConfiguration](../resources/intune-deviceconfig-macosgeneraldeviceconfiguration.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1d463-276">If successful, this method returns a `200 OK` response code and an updated [macOSGeneralDeviceConfiguration](../resources/intune-deviceconfig-macosgeneraldeviceconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="1d463-277">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1d463-277">Example</span></span>
### <a name="request"></a><span data-ttu-id="1d463-278">Solicitud</span><span class="sxs-lookup"><span data-stu-id="1d463-278">Request</span></span>
<span data-ttu-id="1d463-279">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="1d463-279">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations/{deviceConfigurationId}
Content-type: application/json
Content-length: 1747

{
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "roleScopeTagIds": [
    "Role Scope Tag Ids value"
  ],
  "supportsScopeTags": true,
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
  "passwordRequired": true,
  "keychainBlockCloudSync": true,
  "airPrintBlocked": true,
  "airPrintForceTrustedTLS": true,
  "airPrintBlockiBeaconDiscovery": true,
  "safariBlockAutofill": true,
  "cameraBlocked": true,
  "iTunesBlockMusicService": true,
  "spotlightBlockInternetResults": true,
  "keyboardBlockDictation": true,
  "definitionLookupBlocked": true,
  "appleWatchBlockAutoUnlock": true,
  "iTunesBlockFileSharing": true,
  "iCloudBlockDocumentSync": true,
  "iCloudBlockMail": true,
  "iCloudBlockAddressBook": true,
  "iCloudBlockCalendar": true,
  "iCloudBlockReminders": true,
  "iCloudBlockBookmarks": true,
  "iCloudBlockNotes": true,
  "airDropBlocked": true,
  "passwordBlockModification": true,
  "passwordBlockFingerprintUnlock": true
}
```

### <a name="response"></a><span data-ttu-id="1d463-280">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1d463-280">Response</span></span>
<span data-ttu-id="1d463-p116">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="1d463-p116">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1925

{
  "@odata.type": "#microsoft.graph.macOSGeneralDeviceConfiguration",
  "id": "dc356aee-6aee-dc35-ee6a-35dcee6a35dc",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "roleScopeTagIds": [
    "Role Scope Tag Ids value"
  ],
  "supportsScopeTags": true,
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
  "passwordRequired": true,
  "keychainBlockCloudSync": true,
  "airPrintBlocked": true,
  "airPrintForceTrustedTLS": true,
  "airPrintBlockiBeaconDiscovery": true,
  "safariBlockAutofill": true,
  "cameraBlocked": true,
  "iTunesBlockMusicService": true,
  "spotlightBlockInternetResults": true,
  "keyboardBlockDictation": true,
  "definitionLookupBlocked": true,
  "appleWatchBlockAutoUnlock": true,
  "iTunesBlockFileSharing": true,
  "iCloudBlockDocumentSync": true,
  "iCloudBlockMail": true,
  "iCloudBlockAddressBook": true,
  "iCloudBlockCalendar": true,
  "iCloudBlockReminders": true,
  "iCloudBlockBookmarks": true,
  "iCloudBlockNotes": true,
  "airDropBlocked": true,
  "passwordBlockModification": true,
  "passwordBlockFingerprintUnlock": true
}
```




