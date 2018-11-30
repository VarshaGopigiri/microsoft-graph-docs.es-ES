---
title: Actualizar iosEasEmailProfileConfiguration
description: Actualizar las propiedades de un objeto iosEasEmailProfileConfiguration.
ms.openlocfilehash: e73b5e441d99831e8b89b897a09a5809dab6d1ea
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088435"
---
# <a name="update-ioseasemailprofileconfiguration"></a><span data-ttu-id="08970-103">Actualizar iosEasEmailProfileConfiguration</span><span class="sxs-lookup"><span data-stu-id="08970-103">Update iosEasEmailProfileConfiguration</span></span>

> <span data-ttu-id="08970-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="08970-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="08970-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="08970-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="08970-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="08970-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="08970-107">Actualizar las propiedades de un objeto [iosEasEmailProfileConfiguration](../resources/intune-deviceconfig-ioseasemailprofileconfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="08970-107">Update the properties of a [iosEasEmailProfileConfiguration](../resources/intune-deviceconfig-ioseasemailprofileconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="08970-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="08970-108">Prerequisites</span></span>
<span data-ttu-id="08970-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="08970-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="08970-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="08970-111">Permission type</span></span>|<span data-ttu-id="08970-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="08970-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="08970-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="08970-113">Delegated (work or school account)</span></span>|<span data-ttu-id="08970-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="08970-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="08970-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="08970-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="08970-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="08970-116">Not supported.</span></span>|
|<span data-ttu-id="08970-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="08970-117">Application</span></span>|<span data-ttu-id="08970-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="08970-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="08970-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="08970-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/groupAssignments/{deviceConfigurationGroupAssignmentId}/deviceConfiguration
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsDomainJoinConfiguration/networkAccessConfigurations/{deviceConfigurationId}
```

## <a name="request-headers"></a><span data-ttu-id="08970-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="08970-120">Request headers</span></span>
|<span data-ttu-id="08970-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="08970-121">Header</span></span>|<span data-ttu-id="08970-122">Valor</span><span class="sxs-lookup"><span data-stu-id="08970-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="08970-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="08970-123">Authorization</span></span>|<span data-ttu-id="08970-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="08970-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="08970-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="08970-125">Accept</span></span>|<span data-ttu-id="08970-126">application/json</span><span class="sxs-lookup"><span data-stu-id="08970-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="08970-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="08970-127">Request body</span></span>
<span data-ttu-id="08970-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto [iosEasEmailProfileConfiguration](../resources/intune-deviceconfig-ioseasemailprofileconfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="08970-128">In the request body, supply a JSON representation for the [iosEasEmailProfileConfiguration](../resources/intune-deviceconfig-ioseasemailprofileconfiguration.md) object.</span></span>

<span data-ttu-id="08970-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el [iosEasEmailProfileConfiguration](../resources/intune-deviceconfig-ioseasemailprofileconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="08970-129">The following table shows the properties that are required when you create the [iosEasEmailProfileConfiguration](../resources/intune-deviceconfig-ioseasemailprofileconfiguration.md).</span></span>

|<span data-ttu-id="08970-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="08970-130">Property</span></span>|<span data-ttu-id="08970-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="08970-131">Type</span></span>|<span data-ttu-id="08970-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="08970-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="08970-133">id</span><span class="sxs-lookup"><span data-stu-id="08970-133">id</span></span>|<span data-ttu-id="08970-134">String</span><span class="sxs-lookup"><span data-stu-id="08970-134">String</span></span>|<span data-ttu-id="08970-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="08970-135">Key of the entity.</span></span> <span data-ttu-id="08970-136">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="08970-136">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="08970-137">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="08970-137">lastModifiedDateTime</span></span>|<span data-ttu-id="08970-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="08970-138">DateTimeOffset</span></span>|<span data-ttu-id="08970-139">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="08970-139">DateTime the object was last modified.</span></span> <span data-ttu-id="08970-140">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="08970-140">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="08970-141">roleScopeTagIds</span><span class="sxs-lookup"><span data-stu-id="08970-141">roleScopeTagIds</span></span>|<span data-ttu-id="08970-142">Colección String</span><span class="sxs-lookup"><span data-stu-id="08970-142">String collection</span></span>|<span data-ttu-id="08970-143">Lista de etiquetas de ámbito para esta instancia de entidad.</span><span class="sxs-lookup"><span data-stu-id="08970-143">List of Scope Tags for this Entity instance.</span></span> <span data-ttu-id="08970-144">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="08970-144">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="08970-145">supportsScopeTags</span><span class="sxs-lookup"><span data-stu-id="08970-145">supportsScopeTags</span></span>|<span data-ttu-id="08970-146">Booleano</span><span class="sxs-lookup"><span data-stu-id="08970-146">Boolean</span></span>|<span data-ttu-id="08970-147">Indica si la configuración del dispositivo subyacente admite la asignación de etiquetas de ámbito.</span><span class="sxs-lookup"><span data-stu-id="08970-147">Indicates whether or not the underlying Device Configuration supports the assignment of scope tags.</span></span> <span data-ttu-id="08970-148">No se permite la asignación a la propiedad ScopeTags cuando este valor es false y entidades no estará visibles para los usuarios con ámbito.</span><span class="sxs-lookup"><span data-stu-id="08970-148">Assigning to the ScopeTags property is not allowed when this value is false and entities will not be visible to scoped users.</span></span> <span data-ttu-id="08970-149">Esto se produce para las directivas de heredado creadas en Silverlight y se puede resolver por eliminar y volver a crear la directiva en el Portal de Azure.</span><span class="sxs-lookup"><span data-stu-id="08970-149">This occurs for Legacy policies created in Silverlight and can be resolved by deleting and recreating the policy in the Azure Portal.</span></span> <span data-ttu-id="08970-150">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="08970-150">This property is read-only.</span></span> <span data-ttu-id="08970-151">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="08970-151">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="08970-152">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="08970-152">createdDateTime</span></span>|<span data-ttu-id="08970-153">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="08970-153">DateTimeOffset</span></span>|<span data-ttu-id="08970-154">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="08970-154">DateTime the object was created.</span></span> <span data-ttu-id="08970-155">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="08970-155">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="08970-156">descripción</span><span class="sxs-lookup"><span data-stu-id="08970-156">description</span></span>|<span data-ttu-id="08970-157">String</span><span class="sxs-lookup"><span data-stu-id="08970-157">String</span></span>|<span data-ttu-id="08970-158">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="08970-158">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="08970-159">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="08970-159">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="08970-160">displayName</span><span class="sxs-lookup"><span data-stu-id="08970-160">displayName</span></span>|<span data-ttu-id="08970-161">String</span><span class="sxs-lookup"><span data-stu-id="08970-161">String</span></span>|<span data-ttu-id="08970-162">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="08970-162">Admin provided name of the device configuration.</span></span> <span data-ttu-id="08970-163">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="08970-163">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="08970-164">version</span><span class="sxs-lookup"><span data-stu-id="08970-164">version</span></span>|<span data-ttu-id="08970-165">Int32</span><span class="sxs-lookup"><span data-stu-id="08970-165">Int32</span></span>|<span data-ttu-id="08970-166">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="08970-166">Version of the device configuration.</span></span> <span data-ttu-id="08970-167">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="08970-167">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="08970-168">usernameSource</span><span class="sxs-lookup"><span data-stu-id="08970-168">usernameSource</span></span>|[<span data-ttu-id="08970-169">userEmailSource</span><span class="sxs-lookup"><span data-stu-id="08970-169">userEmailSource</span></span>](../resources/intune-deviceconfig-useremailsource.md)|<span data-ttu-id="08970-170">Atributo de nombre de usuario que se seleccionan de AAD y se insertan en este perfil antes de instalar en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="08970-170">Username attribute that is picked from AAD and injected into this profile before installing on the device.</span></span> <span data-ttu-id="08970-171">Se hereda de [easEmailProfileConfigurationBase](../resources/intune-deviceconfig-easemailprofileconfigurationbase.md).</span><span class="sxs-lookup"><span data-stu-id="08970-171">Inherited from [easEmailProfileConfigurationBase](../resources/intune-deviceconfig-easemailprofileconfigurationbase.md).</span></span> <span data-ttu-id="08970-172">Los valores posibles son: `userPrincipalName` y `primarySmtpAddress`.</span><span class="sxs-lookup"><span data-stu-id="08970-172">Possible values are: `userPrincipalName`, `primarySmtpAddress`.</span></span>|
|<span data-ttu-id="08970-173">usernameAADSource</span><span class="sxs-lookup"><span data-stu-id="08970-173">usernameAADSource</span></span>|[<span data-ttu-id="08970-174">usernameSource</span><span class="sxs-lookup"><span data-stu-id="08970-174">usernameSource</span></span>](../resources/intune-deviceconfig-usernamesource.md)|<span data-ttu-id="08970-175">Nombre del campo AAD, que se usará para recuperar el nombre de usuario para el perfil de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="08970-175">Name of the AAD field, that will be used to retrieve UserName for email profile.</span></span> <span data-ttu-id="08970-176">Se hereda de [easEmailProfileConfigurationBase](../resources/intune-deviceconfig-easemailprofileconfigurationbase.md).</span><span class="sxs-lookup"><span data-stu-id="08970-176">Inherited from [easEmailProfileConfigurationBase](../resources/intune-deviceconfig-easemailprofileconfigurationbase.md).</span></span> <span data-ttu-id="08970-177">Los valores posibles son: `userPrincipalName`, `primarySmtpAddress` y `samAccountName`.</span><span class="sxs-lookup"><span data-stu-id="08970-177">Possible values are: `userPrincipalName`, `primarySmtpAddress`, `samAccountName`.</span></span>|
|<span data-ttu-id="08970-178">userDomainNameSource</span><span class="sxs-lookup"><span data-stu-id="08970-178">userDomainNameSource</span></span>|[<span data-ttu-id="08970-179">domainNameSource</span><span class="sxs-lookup"><span data-stu-id="08970-179">domainNameSource</span></span>](../resources/intune-deviceconfig-domainnamesource.md)|<span data-ttu-id="08970-180">Atributo UserDomainname que se seleccionan de AAD y se insertan en este perfil antes de instalar en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="08970-180">UserDomainname attribute that is picked from AAD and injected into this profile before installing on the device.</span></span> <span data-ttu-id="08970-181">Se hereda de [easEmailProfileConfigurationBase](../resources/intune-deviceconfig-easemailprofileconfigurationbase.md).</span><span class="sxs-lookup"><span data-stu-id="08970-181">Inherited from [easEmailProfileConfigurationBase](../resources/intune-deviceconfig-easemailprofileconfigurationbase.md).</span></span> <span data-ttu-id="08970-182">Los valores posibles son: `fullDomainName` y `netBiosDomainName`.</span><span class="sxs-lookup"><span data-stu-id="08970-182">Possible values are: `fullDomainName`, `netBiosDomainName`.</span></span>|
|<span data-ttu-id="08970-183">customDomainName</span><span class="sxs-lookup"><span data-stu-id="08970-183">customDomainName</span></span>|<span data-ttu-id="08970-184">String</span><span class="sxs-lookup"><span data-stu-id="08970-184">String</span></span>|<span data-ttu-id="08970-185">Valor de nombre de dominio personalizado utilizado durante la generación de un perfil de correo electrónico antes de instalar en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="08970-185">Custom domain name value used while generating an email profile before installing on the device.</span></span> <span data-ttu-id="08970-186">Se hereda de [easEmailProfileConfigurationBase](../resources/intune-deviceconfig-easemailprofileconfigurationbase.md)</span><span class="sxs-lookup"><span data-stu-id="08970-186">Inherited from [easEmailProfileConfigurationBase](../resources/intune-deviceconfig-easemailprofileconfigurationbase.md)</span></span>|
|<span data-ttu-id="08970-187">accountName</span><span class="sxs-lookup"><span data-stu-id="08970-187">accountName</span></span>|<span data-ttu-id="08970-188">String</span><span class="sxs-lookup"><span data-stu-id="08970-188">String</span></span>|<span data-ttu-id="08970-189">Nombre de la cuenta.</span><span class="sxs-lookup"><span data-stu-id="08970-189">Account name.</span></span>|
|<span data-ttu-id="08970-190">authenticationMethod</span><span class="sxs-lookup"><span data-stu-id="08970-190">authenticationMethod</span></span>|[<span data-ttu-id="08970-191">easAuthenticationMethod</span><span class="sxs-lookup"><span data-stu-id="08970-191">easAuthenticationMethod</span></span>](../resources/intune-deviceconfig-easauthenticationmethod.md)|<span data-ttu-id="08970-192">Método de autenticación para este perfil de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="08970-192">Authentication method for this Email profile.</span></span> <span data-ttu-id="08970-193">Los valores posibles son: `usernameAndPassword` y `certificate`.</span><span class="sxs-lookup"><span data-stu-id="08970-193">Possible values are: `usernameAndPassword`, `certificate`.</span></span>|
|<span data-ttu-id="08970-194">blockMovingMessagesToOtherEmailAccounts</span><span class="sxs-lookup"><span data-stu-id="08970-194">blockMovingMessagesToOtherEmailAccounts</span></span>|<span data-ttu-id="08970-195">Booleano</span><span class="sxs-lookup"><span data-stu-id="08970-195">Boolean</span></span>|<span data-ttu-id="08970-196">Indica si se deben bloquear mover mensajes a otras cuentas de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="08970-196">Indicates whether or not to block moving messages to other email accounts.</span></span>|
|<span data-ttu-id="08970-197">blockSendingEmailFromThirdPartyApps</span><span class="sxs-lookup"><span data-stu-id="08970-197">blockSendingEmailFromThirdPartyApps</span></span>|<span data-ttu-id="08970-198">Booleano</span><span class="sxs-lookup"><span data-stu-id="08970-198">Boolean</span></span>|<span data-ttu-id="08970-199">Indica si se deben bloquear el envío de correo electrónico desde aplicaciones de otros fabricantes.</span><span class="sxs-lookup"><span data-stu-id="08970-199">Indicates whether or not to block sending email from third party apps.</span></span>|
|<span data-ttu-id="08970-200">blockSyncingRecentlyUsedEmailAddresses</span><span class="sxs-lookup"><span data-stu-id="08970-200">blockSyncingRecentlyUsedEmailAddresses</span></span>|<span data-ttu-id="08970-201">Booleano</span><span class="sxs-lookup"><span data-stu-id="08970-201">Boolean</span></span>|<span data-ttu-id="08970-202">Indica si se deben bloquear sincronización usados recientemente direcciones de correo electrónico, por ejemplo, - al redactar correo electrónico nuevo.</span><span class="sxs-lookup"><span data-stu-id="08970-202">Indicates whether or not to block syncing recently used email addresses, for instance - when composing new email.</span></span>|
|<span data-ttu-id="08970-203">durationOfEmailToSync</span><span class="sxs-lookup"><span data-stu-id="08970-203">durationOfEmailToSync</span></span>|[<span data-ttu-id="08970-204">emailSyncDuration</span><span class="sxs-lookup"><span data-stu-id="08970-204">emailSyncDuration</span></span>](../resources/intune-deviceconfig-emailsyncduration.md)|<span data-ttu-id="08970-205">Duración de correo electrónico de tiempo se debe sincronizar volver a.</span><span class="sxs-lookup"><span data-stu-id="08970-205">Duration of time email should be synced back to.</span></span> <span data-ttu-id="08970-206">.</span><span class="sxs-lookup"><span data-stu-id="08970-206"></span></span> <span data-ttu-id="08970-207">Los valores posibles son: `userDefined`, `oneDay`, `threeDays`, `oneWeek`, `twoWeeks`, `oneMonth` y `unlimited`.</span><span class="sxs-lookup"><span data-stu-id="08970-207">Possible values are: `userDefined`, `oneDay`, `threeDays`, `oneWeek`, `twoWeeks`, `oneMonth`, `unlimited`.</span></span>|
|<span data-ttu-id="08970-208">emailAddressSource</span><span class="sxs-lookup"><span data-stu-id="08970-208">emailAddressSource</span></span>|[<span data-ttu-id="08970-209">userEmailSource</span><span class="sxs-lookup"><span data-stu-id="08970-209">userEmailSource</span></span>](../resources/intune-deviceconfig-useremailsource.md)|<span data-ttu-id="08970-210">Atributo de correo electrónico que se seleccionan de AAD y se insertan en este perfil antes de instalar en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="08970-210">Email attribute that is picked from AAD and injected into this profile before installing on the device.</span></span> <span data-ttu-id="08970-211">Los valores posibles son: `userPrincipalName` y `primarySmtpAddress`.</span><span class="sxs-lookup"><span data-stu-id="08970-211">Possible values are: `userPrincipalName`, `primarySmtpAddress`.</span></span>|
|<span data-ttu-id="08970-212">hostName</span><span class="sxs-lookup"><span data-stu-id="08970-212">hostName</span></span>|<span data-ttu-id="08970-213">String</span><span class="sxs-lookup"><span data-stu-id="08970-213">String</span></span>|<span data-ttu-id="08970-214">Ubicación de Exchange esa dirección (URL) que la aplicación de correo nativo se conecta a.</span><span class="sxs-lookup"><span data-stu-id="08970-214">Exchange location that (URL) that the native mail app connects to.</span></span>|
|<span data-ttu-id="08970-215">requireSmime</span><span class="sxs-lookup"><span data-stu-id="08970-215">requireSmime</span></span>|<span data-ttu-id="08970-216">Booleano</span><span class="sxs-lookup"><span data-stu-id="08970-216">Boolean</span></span>|<span data-ttu-id="08970-217">Indica si se va a usar certificados S/MIME o no.</span><span class="sxs-lookup"><span data-stu-id="08970-217">Indicates whether or not to use S/MIME certificate.</span></span>|
|<span data-ttu-id="08970-218">smimeEnablePerMessageSwitch</span><span class="sxs-lookup"><span data-stu-id="08970-218">smimeEnablePerMessageSwitch</span></span>|<span data-ttu-id="08970-219">Booleano</span><span class="sxs-lookup"><span data-stu-id="08970-219">Boolean</span></span>|<span data-ttu-id="08970-220">Indica si se debe o no permitir que los mensajes de correo electrónico sin cifrar.</span><span class="sxs-lookup"><span data-stu-id="08970-220">Indicates whether or not to allow unencrypted emails.</span></span>|
|<span data-ttu-id="08970-221">requireSsl</span><span class="sxs-lookup"><span data-stu-id="08970-221">requireSsl</span></span>|<span data-ttu-id="08970-222">Booleano</span><span class="sxs-lookup"><span data-stu-id="08970-222">Boolean</span></span>|<span data-ttu-id="08970-223">Indica si se va a usar SSL o no.</span><span class="sxs-lookup"><span data-stu-id="08970-223">Indicates whether or not to use SSL.</span></span>|
|<span data-ttu-id="08970-224">useOAuth</span><span class="sxs-lookup"><span data-stu-id="08970-224">useOAuth</span></span>|<span data-ttu-id="08970-225">Booleano</span><span class="sxs-lookup"><span data-stu-id="08970-225">Boolean</span></span>|<span data-ttu-id="08970-226">Especifica si la conexión debe usar OAuth para la autenticación.</span><span class="sxs-lookup"><span data-stu-id="08970-226">Specifies whether the connection should use OAuth for authentication.</span></span>|



## <a name="response"></a><span data-ttu-id="08970-227">Respuesta</span><span class="sxs-lookup"><span data-stu-id="08970-227">Response</span></span>
<span data-ttu-id="08970-228">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto actualizado [iosEasEmailProfileConfiguration](../resources/intune-deviceconfig-ioseasemailprofileconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="08970-228">If successful, this method returns a `200 OK` response code and an updated [iosEasEmailProfileConfiguration](../resources/intune-deviceconfig-ioseasemailprofileconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="08970-229">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="08970-229">Example</span></span>
### <a name="request"></a><span data-ttu-id="08970-230">Solicitud</span><span class="sxs-lookup"><span data-stu-id="08970-230">Request</span></span>
<span data-ttu-id="08970-231">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="08970-231">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations/{deviceConfigurationId}
Content-type: application/json
Content-length: 904

{
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "roleScopeTagIds": [
    "Role Scope Tag Ids value"
  ],
  "supportsScopeTags": true,
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "usernameSource": "primarySmtpAddress",
  "usernameAADSource": "primarySmtpAddress",
  "userDomainNameSource": "netBiosDomainName",
  "customDomainName": "Custom Domain Name value",
  "accountName": "Account Name value",
  "authenticationMethod": "certificate",
  "blockMovingMessagesToOtherEmailAccounts": true,
  "blockSendingEmailFromThirdPartyApps": true,
  "blockSyncingRecentlyUsedEmailAddresses": true,
  "durationOfEmailToSync": "oneDay",
  "emailAddressSource": "primarySmtpAddress",
  "hostName": "Host Name value",
  "requireSmime": true,
  "smimeEnablePerMessageSwitch": true,
  "requireSsl": true,
  "useOAuth": true
}
```

### <a name="response"></a><span data-ttu-id="08970-232">Respuesta</span><span class="sxs-lookup"><span data-stu-id="08970-232">Response</span></span>
<span data-ttu-id="08970-p118">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="08970-p118">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1082

{
  "@odata.type": "#microsoft.graph.iosEasEmailProfileConfiguration",
  "id": "e03086da-86da-e030-da86-30e0da8630e0",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "roleScopeTagIds": [
    "Role Scope Tag Ids value"
  ],
  "supportsScopeTags": true,
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "usernameSource": "primarySmtpAddress",
  "usernameAADSource": "primarySmtpAddress",
  "userDomainNameSource": "netBiosDomainName",
  "customDomainName": "Custom Domain Name value",
  "accountName": "Account Name value",
  "authenticationMethod": "certificate",
  "blockMovingMessagesToOtherEmailAccounts": true,
  "blockSendingEmailFromThirdPartyApps": true,
  "blockSyncingRecentlyUsedEmailAddresses": true,
  "durationOfEmailToSync": "oneDay",
  "emailAddressSource": "primarySmtpAddress",
  "hostName": "Host Name value",
  "requireSmime": true,
  "smimeEnablePerMessageSwitch": true,
  "requireSsl": true,
  "useOAuth": true
}
```





