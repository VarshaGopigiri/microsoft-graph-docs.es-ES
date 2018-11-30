---
title: Crear iosEasEmailProfileConfiguration
description: Crear un nuevo objeto iosEasEmailProfileConfiguration.
ms.openlocfilehash: 78cf37fc63f6cc62d40ffc1ef3deda587b65aaf3
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086852"
---
# <a name="create-ioseasemailprofileconfiguration"></a><span data-ttu-id="a4b4d-103">Crear iosEasEmailProfileConfiguration</span><span class="sxs-lookup"><span data-stu-id="a4b4d-103">Create iosEasEmailProfileConfiguration</span></span>

> <span data-ttu-id="a4b4d-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="a4b4d-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="a4b4d-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="a4b4d-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="a4b4d-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="a4b4d-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="a4b4d-107">Crear un nuevo objeto [iosEasEmailProfileConfiguration](../resources/intune-deviceconfig-ioseasemailprofileconfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="a4b4d-107">Create a new [iosEasEmailProfileConfiguration](../resources/intune-deviceconfig-ioseasemailprofileconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="a4b4d-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="a4b4d-108">Prerequisites</span></span>
<span data-ttu-id="a4b4d-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="a4b4d-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="a4b4d-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a4b4d-111">Permission type</span></span>|<span data-ttu-id="a4b4d-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a4b4d-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="a4b4d-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a4b4d-113">Delegated (work or school account)</span></span>|<span data-ttu-id="a4b4d-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="a4b4d-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="a4b4d-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a4b4d-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="a4b4d-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a4b4d-116">Not supported.</span></span>|
|<span data-ttu-id="a4b4d-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a4b4d-117">Application</span></span>|<span data-ttu-id="a4b4d-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a4b4d-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="a4b4d-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a4b4d-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceConfigurations
POST /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsDomainJoinConfiguration/networkAccessConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="a4b4d-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a4b4d-120">Request headers</span></span>
|<span data-ttu-id="a4b4d-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a4b4d-121">Header</span></span>|<span data-ttu-id="a4b4d-122">Valor</span><span class="sxs-lookup"><span data-stu-id="a4b4d-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="a4b4d-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="a4b4d-123">Authorization</span></span>|<span data-ttu-id="a4b4d-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="a4b4d-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="a4b4d-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="a4b4d-125">Accept</span></span>|<span data-ttu-id="a4b4d-126">application/json</span><span class="sxs-lookup"><span data-stu-id="a4b4d-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="a4b4d-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a4b4d-127">Request body</span></span>
<span data-ttu-id="a4b4d-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto iosEasEmailProfileConfiguration.</span><span class="sxs-lookup"><span data-stu-id="a4b4d-128">In the request body, supply a JSON representation for the iosEasEmailProfileConfiguration object.</span></span>

<span data-ttu-id="a4b4d-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el iosEasEmailProfileConfiguration.</span><span class="sxs-lookup"><span data-stu-id="a4b4d-129">The following table shows the properties that are required when you create the iosEasEmailProfileConfiguration.</span></span>

|<span data-ttu-id="a4b4d-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a4b4d-130">Property</span></span>|<span data-ttu-id="a4b4d-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="a4b4d-131">Type</span></span>|<span data-ttu-id="a4b4d-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="a4b4d-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="a4b4d-133">id</span><span class="sxs-lookup"><span data-stu-id="a4b4d-133">id</span></span>|<span data-ttu-id="a4b4d-134">String</span><span class="sxs-lookup"><span data-stu-id="a4b4d-134">String</span></span>|<span data-ttu-id="a4b4d-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="a4b4d-135">Key of the entity.</span></span> <span data-ttu-id="a4b4d-136">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="a4b4d-136">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="a4b4d-137">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="a4b4d-137">lastModifiedDateTime</span></span>|<span data-ttu-id="a4b4d-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="a4b4d-138">DateTimeOffset</span></span>|<span data-ttu-id="a4b4d-139">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="a4b4d-139">DateTime the object was last modified.</span></span> <span data-ttu-id="a4b4d-140">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="a4b4d-140">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="a4b4d-141">roleScopeTagIds</span><span class="sxs-lookup"><span data-stu-id="a4b4d-141">roleScopeTagIds</span></span>|<span data-ttu-id="a4b4d-142">Colección String</span><span class="sxs-lookup"><span data-stu-id="a4b4d-142">String collection</span></span>|<span data-ttu-id="a4b4d-143">Lista de etiquetas de ámbito para esta instancia de entidad.</span><span class="sxs-lookup"><span data-stu-id="a4b4d-143">List of Scope Tags for this Entity instance.</span></span> <span data-ttu-id="a4b4d-144">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="a4b4d-144">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="a4b4d-145">supportsScopeTags</span><span class="sxs-lookup"><span data-stu-id="a4b4d-145">supportsScopeTags</span></span>|<span data-ttu-id="a4b4d-146">Booleano</span><span class="sxs-lookup"><span data-stu-id="a4b4d-146">Boolean</span></span>|<span data-ttu-id="a4b4d-147">Indica si la configuración del dispositivo subyacente admite la asignación de etiquetas de ámbito.</span><span class="sxs-lookup"><span data-stu-id="a4b4d-147">Indicates whether or not the underlying Device Configuration supports the assignment of scope tags.</span></span> <span data-ttu-id="a4b4d-148">No se permite la asignación a la propiedad ScopeTags cuando este valor es false y entidades no estará visibles para los usuarios con ámbito.</span><span class="sxs-lookup"><span data-stu-id="a4b4d-148">Assigning to the ScopeTags property is not allowed when this value is false and entities will not be visible to scoped users.</span></span> <span data-ttu-id="a4b4d-149">Esto se produce para las directivas de heredado creadas en Silverlight y se puede resolver por eliminar y volver a crear la directiva en el Portal de Azure.</span><span class="sxs-lookup"><span data-stu-id="a4b4d-149">This occurs for Legacy policies created in Silverlight and can be resolved by deleting and recreating the policy in the Azure Portal.</span></span> <span data-ttu-id="a4b4d-150">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="a4b4d-150">This property is read-only.</span></span> <span data-ttu-id="a4b4d-151">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="a4b4d-151">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="a4b4d-152">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="a4b4d-152">createdDateTime</span></span>|<span data-ttu-id="a4b4d-153">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="a4b4d-153">DateTimeOffset</span></span>|<span data-ttu-id="a4b4d-154">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="a4b4d-154">DateTime the object was created.</span></span> <span data-ttu-id="a4b4d-155">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="a4b4d-155">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="a4b4d-156">descripción</span><span class="sxs-lookup"><span data-stu-id="a4b4d-156">description</span></span>|<span data-ttu-id="a4b4d-157">String</span><span class="sxs-lookup"><span data-stu-id="a4b4d-157">String</span></span>|<span data-ttu-id="a4b4d-158">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a4b4d-158">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="a4b4d-159">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="a4b4d-159">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="a4b4d-160">displayName</span><span class="sxs-lookup"><span data-stu-id="a4b4d-160">displayName</span></span>|<span data-ttu-id="a4b4d-161">String</span><span class="sxs-lookup"><span data-stu-id="a4b4d-161">String</span></span>|<span data-ttu-id="a4b4d-162">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a4b4d-162">Admin provided name of the device configuration.</span></span> <span data-ttu-id="a4b4d-163">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="a4b4d-163">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="a4b4d-164">version</span><span class="sxs-lookup"><span data-stu-id="a4b4d-164">version</span></span>|<span data-ttu-id="a4b4d-165">Int32</span><span class="sxs-lookup"><span data-stu-id="a4b4d-165">Int32</span></span>|<span data-ttu-id="a4b4d-166">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a4b4d-166">Version of the device configuration.</span></span> <span data-ttu-id="a4b4d-167">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="a4b4d-167">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="a4b4d-168">usernameSource</span><span class="sxs-lookup"><span data-stu-id="a4b4d-168">usernameSource</span></span>|[<span data-ttu-id="a4b4d-169">userEmailSource</span><span class="sxs-lookup"><span data-stu-id="a4b4d-169">userEmailSource</span></span>](../resources/intune-deviceconfig-useremailsource.md)|<span data-ttu-id="a4b4d-170">Atributo de nombre de usuario que se seleccionan de AAD y se insertan en este perfil antes de instalar en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a4b4d-170">Username attribute that is picked from AAD and injected into this profile before installing on the device.</span></span> <span data-ttu-id="a4b4d-171">Se hereda de [easEmailProfileConfigurationBase](../resources/intune-deviceconfig-easemailprofileconfigurationbase.md).</span><span class="sxs-lookup"><span data-stu-id="a4b4d-171">Inherited from [easEmailProfileConfigurationBase](../resources/intune-deviceconfig-easemailprofileconfigurationbase.md).</span></span> <span data-ttu-id="a4b4d-172">Los valores posibles son: `userPrincipalName` y `primarySmtpAddress`.</span><span class="sxs-lookup"><span data-stu-id="a4b4d-172">Possible values are: `userPrincipalName`, `primarySmtpAddress`.</span></span>|
|<span data-ttu-id="a4b4d-173">usernameAADSource</span><span class="sxs-lookup"><span data-stu-id="a4b4d-173">usernameAADSource</span></span>|[<span data-ttu-id="a4b4d-174">usernameSource</span><span class="sxs-lookup"><span data-stu-id="a4b4d-174">usernameSource</span></span>](../resources/intune-deviceconfig-usernamesource.md)|<span data-ttu-id="a4b4d-175">Nombre del campo AAD, que se usará para recuperar el nombre de usuario para el perfil de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="a4b4d-175">Name of the AAD field, that will be used to retrieve UserName for email profile.</span></span> <span data-ttu-id="a4b4d-176">Se hereda de [easEmailProfileConfigurationBase](../resources/intune-deviceconfig-easemailprofileconfigurationbase.md).</span><span class="sxs-lookup"><span data-stu-id="a4b4d-176">Inherited from [easEmailProfileConfigurationBase](../resources/intune-deviceconfig-easemailprofileconfigurationbase.md).</span></span> <span data-ttu-id="a4b4d-177">Los valores posibles son: `userPrincipalName`, `primarySmtpAddress` y `samAccountName`.</span><span class="sxs-lookup"><span data-stu-id="a4b4d-177">Possible values are: `userPrincipalName`, `primarySmtpAddress`, `samAccountName`.</span></span>|
|<span data-ttu-id="a4b4d-178">userDomainNameSource</span><span class="sxs-lookup"><span data-stu-id="a4b4d-178">userDomainNameSource</span></span>|[<span data-ttu-id="a4b4d-179">domainNameSource</span><span class="sxs-lookup"><span data-stu-id="a4b4d-179">domainNameSource</span></span>](../resources/intune-deviceconfig-domainnamesource.md)|<span data-ttu-id="a4b4d-180">Atributo UserDomainname que se seleccionan de AAD y se insertan en este perfil antes de instalar en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a4b4d-180">UserDomainname attribute that is picked from AAD and injected into this profile before installing on the device.</span></span> <span data-ttu-id="a4b4d-181">Se hereda de [easEmailProfileConfigurationBase](../resources/intune-deviceconfig-easemailprofileconfigurationbase.md).</span><span class="sxs-lookup"><span data-stu-id="a4b4d-181">Inherited from [easEmailProfileConfigurationBase](../resources/intune-deviceconfig-easemailprofileconfigurationbase.md).</span></span> <span data-ttu-id="a4b4d-182">Los valores posibles son: `fullDomainName` y `netBiosDomainName`.</span><span class="sxs-lookup"><span data-stu-id="a4b4d-182">Possible values are: `fullDomainName`, `netBiosDomainName`.</span></span>|
|<span data-ttu-id="a4b4d-183">customDomainName</span><span class="sxs-lookup"><span data-stu-id="a4b4d-183">customDomainName</span></span>|<span data-ttu-id="a4b4d-184">String</span><span class="sxs-lookup"><span data-stu-id="a4b4d-184">String</span></span>|<span data-ttu-id="a4b4d-185">Valor de nombre de dominio personalizado utilizado durante la generación de un perfil de correo electrónico antes de instalar en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a4b4d-185">Custom domain name value used while generating an email profile before installing on the device.</span></span> <span data-ttu-id="a4b4d-186">Se hereda de [easEmailProfileConfigurationBase](../resources/intune-deviceconfig-easemailprofileconfigurationbase.md)</span><span class="sxs-lookup"><span data-stu-id="a4b4d-186">Inherited from [easEmailProfileConfigurationBase](../resources/intune-deviceconfig-easemailprofileconfigurationbase.md)</span></span>|
|<span data-ttu-id="a4b4d-187">accountName</span><span class="sxs-lookup"><span data-stu-id="a4b4d-187">accountName</span></span>|<span data-ttu-id="a4b4d-188">String</span><span class="sxs-lookup"><span data-stu-id="a4b4d-188">String</span></span>|<span data-ttu-id="a4b4d-189">Nombre de la cuenta.</span><span class="sxs-lookup"><span data-stu-id="a4b4d-189">Account name.</span></span>|
|<span data-ttu-id="a4b4d-190">authenticationMethod</span><span class="sxs-lookup"><span data-stu-id="a4b4d-190">authenticationMethod</span></span>|[<span data-ttu-id="a4b4d-191">easAuthenticationMethod</span><span class="sxs-lookup"><span data-stu-id="a4b4d-191">easAuthenticationMethod</span></span>](../resources/intune-deviceconfig-easauthenticationmethod.md)|<span data-ttu-id="a4b4d-192">Método de autenticación para este perfil de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="a4b4d-192">Authentication method for this Email profile.</span></span> <span data-ttu-id="a4b4d-193">Los valores posibles son: `usernameAndPassword` y `certificate`.</span><span class="sxs-lookup"><span data-stu-id="a4b4d-193">Possible values are: `usernameAndPassword`, `certificate`.</span></span>|
|<span data-ttu-id="a4b4d-194">blockMovingMessagesToOtherEmailAccounts</span><span class="sxs-lookup"><span data-stu-id="a4b4d-194">blockMovingMessagesToOtherEmailAccounts</span></span>|<span data-ttu-id="a4b4d-195">Booleano</span><span class="sxs-lookup"><span data-stu-id="a4b4d-195">Boolean</span></span>|<span data-ttu-id="a4b4d-196">Indica si se deben bloquear mover mensajes a otras cuentas de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="a4b4d-196">Indicates whether or not to block moving messages to other email accounts.</span></span>|
|<span data-ttu-id="a4b4d-197">blockSendingEmailFromThirdPartyApps</span><span class="sxs-lookup"><span data-stu-id="a4b4d-197">blockSendingEmailFromThirdPartyApps</span></span>|<span data-ttu-id="a4b4d-198">Booleano</span><span class="sxs-lookup"><span data-stu-id="a4b4d-198">Boolean</span></span>|<span data-ttu-id="a4b4d-199">Indica si se deben bloquear el envío de correo electrónico desde aplicaciones de otros fabricantes.</span><span class="sxs-lookup"><span data-stu-id="a4b4d-199">Indicates whether or not to block sending email from third party apps.</span></span>|
|<span data-ttu-id="a4b4d-200">blockSyncingRecentlyUsedEmailAddresses</span><span class="sxs-lookup"><span data-stu-id="a4b4d-200">blockSyncingRecentlyUsedEmailAddresses</span></span>|<span data-ttu-id="a4b4d-201">Booleano</span><span class="sxs-lookup"><span data-stu-id="a4b4d-201">Boolean</span></span>|<span data-ttu-id="a4b4d-202">Indica si se deben bloquear sincronización usados recientemente direcciones de correo electrónico, por ejemplo, - al redactar correo electrónico nuevo.</span><span class="sxs-lookup"><span data-stu-id="a4b4d-202">Indicates whether or not to block syncing recently used email addresses, for instance - when composing new email.</span></span>|
|<span data-ttu-id="a4b4d-203">durationOfEmailToSync</span><span class="sxs-lookup"><span data-stu-id="a4b4d-203">durationOfEmailToSync</span></span>|[<span data-ttu-id="a4b4d-204">emailSyncDuration</span><span class="sxs-lookup"><span data-stu-id="a4b4d-204">emailSyncDuration</span></span>](../resources/intune-deviceconfig-emailsyncduration.md)|<span data-ttu-id="a4b4d-205">Duración de correo electrónico de tiempo se debe sincronizar volver a.</span><span class="sxs-lookup"><span data-stu-id="a4b4d-205">Duration of time email should be synced back to.</span></span> <span data-ttu-id="a4b4d-206">.</span><span class="sxs-lookup"><span data-stu-id="a4b4d-206"></span></span> <span data-ttu-id="a4b4d-207">Los valores posibles son: `userDefined`, `oneDay`, `threeDays`, `oneWeek`, `twoWeeks`, `oneMonth` y `unlimited`.</span><span class="sxs-lookup"><span data-stu-id="a4b4d-207">Possible values are: `userDefined`, `oneDay`, `threeDays`, `oneWeek`, `twoWeeks`, `oneMonth`, `unlimited`.</span></span>|
|<span data-ttu-id="a4b4d-208">emailAddressSource</span><span class="sxs-lookup"><span data-stu-id="a4b4d-208">emailAddressSource</span></span>|[<span data-ttu-id="a4b4d-209">userEmailSource</span><span class="sxs-lookup"><span data-stu-id="a4b4d-209">userEmailSource</span></span>](../resources/intune-deviceconfig-useremailsource.md)|<span data-ttu-id="a4b4d-210">Atributo de correo electrónico que se seleccionan de AAD y se insertan en este perfil antes de instalar en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a4b4d-210">Email attribute that is picked from AAD and injected into this profile before installing on the device.</span></span> <span data-ttu-id="a4b4d-211">Los valores posibles son: `userPrincipalName` y `primarySmtpAddress`.</span><span class="sxs-lookup"><span data-stu-id="a4b4d-211">Possible values are: `userPrincipalName`, `primarySmtpAddress`.</span></span>|
|<span data-ttu-id="a4b4d-212">hostName</span><span class="sxs-lookup"><span data-stu-id="a4b4d-212">hostName</span></span>|<span data-ttu-id="a4b4d-213">String</span><span class="sxs-lookup"><span data-stu-id="a4b4d-213">String</span></span>|<span data-ttu-id="a4b4d-214">Ubicación de Exchange esa dirección (URL) que la aplicación de correo nativo se conecta a.</span><span class="sxs-lookup"><span data-stu-id="a4b4d-214">Exchange location that (URL) that the native mail app connects to.</span></span>|
|<span data-ttu-id="a4b4d-215">requireSmime</span><span class="sxs-lookup"><span data-stu-id="a4b4d-215">requireSmime</span></span>|<span data-ttu-id="a4b4d-216">Booleano</span><span class="sxs-lookup"><span data-stu-id="a4b4d-216">Boolean</span></span>|<span data-ttu-id="a4b4d-217">Indica si se va a usar certificados S/MIME o no.</span><span class="sxs-lookup"><span data-stu-id="a4b4d-217">Indicates whether or not to use S/MIME certificate.</span></span>|
|<span data-ttu-id="a4b4d-218">smimeEnablePerMessageSwitch</span><span class="sxs-lookup"><span data-stu-id="a4b4d-218">smimeEnablePerMessageSwitch</span></span>|<span data-ttu-id="a4b4d-219">Booleano</span><span class="sxs-lookup"><span data-stu-id="a4b4d-219">Boolean</span></span>|<span data-ttu-id="a4b4d-220">Indica si se debe o no permitir que los mensajes de correo electrónico sin cifrar.</span><span class="sxs-lookup"><span data-stu-id="a4b4d-220">Indicates whether or not to allow unencrypted emails.</span></span>|
|<span data-ttu-id="a4b4d-221">requireSsl</span><span class="sxs-lookup"><span data-stu-id="a4b4d-221">requireSsl</span></span>|<span data-ttu-id="a4b4d-222">Booleano</span><span class="sxs-lookup"><span data-stu-id="a4b4d-222">Boolean</span></span>|<span data-ttu-id="a4b4d-223">Indica si se va a usar SSL o no.</span><span class="sxs-lookup"><span data-stu-id="a4b4d-223">Indicates whether or not to use SSL.</span></span>|
|<span data-ttu-id="a4b4d-224">useOAuth</span><span class="sxs-lookup"><span data-stu-id="a4b4d-224">useOAuth</span></span>|<span data-ttu-id="a4b4d-225">Booleano</span><span class="sxs-lookup"><span data-stu-id="a4b4d-225">Boolean</span></span>|<span data-ttu-id="a4b4d-226">Especifica si la conexión debe usar OAuth para la autenticación.</span><span class="sxs-lookup"><span data-stu-id="a4b4d-226">Specifies whether the connection should use OAuth for authentication.</span></span>|



## <a name="response"></a><span data-ttu-id="a4b4d-227">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a4b4d-227">Response</span></span>
<span data-ttu-id="a4b4d-228">Si tiene éxito, este método devuelve una `201 Created` código de respuesta y un objeto [iosEasEmailProfileConfiguration](../resources/intune-deviceconfig-ioseasemailprofileconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a4b4d-228">If successful, this method returns a `201 Created` response code and a [iosEasEmailProfileConfiguration](../resources/intune-deviceconfig-ioseasemailprofileconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="a4b4d-229">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a4b4d-229">Example</span></span>
### <a name="request"></a><span data-ttu-id="a4b4d-230">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a4b4d-230">Request</span></span>
<span data-ttu-id="a4b4d-231">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a4b4d-231">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations
Content-type: application/json
Content-length: 974

{
  "@odata.type": "#microsoft.graph.iosEasEmailProfileConfiguration",
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

### <a name="response"></a><span data-ttu-id="a4b4d-232">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a4b4d-232">Response</span></span>
<span data-ttu-id="a4b4d-p118">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="a4b4d-p118">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
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




