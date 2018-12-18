---
title: Crear androidWorkProfileGmailEasConfiguration
description: Crear un nuevo objeto androidWorkProfileGmailEasConfiguration.
author: tfitzmac
ms.openlocfilehash: 867cd1bf2679746ca3b8e6da01062b9338ec78fa
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27360777"
---
# <a name="create-androidworkprofilegmaileasconfiguration"></a><span data-ttu-id="a878a-103">Crear androidWorkProfileGmailEasConfiguration</span><span class="sxs-lookup"><span data-stu-id="a878a-103">Create androidWorkProfileGmailEasConfiguration</span></span>

> <span data-ttu-id="a878a-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="a878a-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="a878a-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="a878a-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="a878a-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="a878a-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="a878a-107">Crear un nuevo objeto [androidWorkProfileGmailEasConfiguration](../resources/intune-deviceconfig-androidworkprofilegmaileasconfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="a878a-107">Create a new [androidWorkProfileGmailEasConfiguration](../resources/intune-deviceconfig-androidworkprofilegmaileasconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="a878a-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="a878a-108">Prerequisites</span></span>
<span data-ttu-id="a878a-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="a878a-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="a878a-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a878a-111">Permission type</span></span>|<span data-ttu-id="a878a-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a878a-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="a878a-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a878a-113">Delegated (work or school account)</span></span>|<span data-ttu-id="a878a-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="a878a-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="a878a-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a878a-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="a878a-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a878a-116">Not supported.</span></span>|
|<span data-ttu-id="a878a-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a878a-117">Application</span></span>|<span data-ttu-id="a878a-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a878a-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="a878a-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a878a-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceConfigurations
POST /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsDomainJoinConfiguration/networkAccessConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="a878a-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a878a-120">Request headers</span></span>
|<span data-ttu-id="a878a-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a878a-121">Header</span></span>|<span data-ttu-id="a878a-122">Valor</span><span class="sxs-lookup"><span data-stu-id="a878a-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="a878a-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="a878a-123">Authorization</span></span>|<span data-ttu-id="a878a-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="a878a-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="a878a-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="a878a-125">Accept</span></span>|<span data-ttu-id="a878a-126">application/json</span><span class="sxs-lookup"><span data-stu-id="a878a-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="a878a-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a878a-127">Request body</span></span>
<span data-ttu-id="a878a-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto androidWorkProfileGmailEasConfiguration.</span><span class="sxs-lookup"><span data-stu-id="a878a-128">In the request body, supply a JSON representation for the androidWorkProfileGmailEasConfiguration object.</span></span>

<span data-ttu-id="a878a-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el androidWorkProfileGmailEasConfiguration.</span><span class="sxs-lookup"><span data-stu-id="a878a-129">The following table shows the properties that are required when you create the androidWorkProfileGmailEasConfiguration.</span></span>

|<span data-ttu-id="a878a-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a878a-130">Property</span></span>|<span data-ttu-id="a878a-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="a878a-131">Type</span></span>|<span data-ttu-id="a878a-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="a878a-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="a878a-133">id</span><span class="sxs-lookup"><span data-stu-id="a878a-133">id</span></span>|<span data-ttu-id="a878a-134">String</span><span class="sxs-lookup"><span data-stu-id="a878a-134">String</span></span>|<span data-ttu-id="a878a-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="a878a-135">Key of the entity.</span></span> <span data-ttu-id="a878a-136">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="a878a-136">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="a878a-137">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="a878a-137">lastModifiedDateTime</span></span>|<span data-ttu-id="a878a-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="a878a-138">DateTimeOffset</span></span>|<span data-ttu-id="a878a-139">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="a878a-139">DateTime the object was last modified.</span></span> <span data-ttu-id="a878a-140">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="a878a-140">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="a878a-141">roleScopeTagIds</span><span class="sxs-lookup"><span data-stu-id="a878a-141">roleScopeTagIds</span></span>|<span data-ttu-id="a878a-142">Colección String</span><span class="sxs-lookup"><span data-stu-id="a878a-142">String collection</span></span>|<span data-ttu-id="a878a-143">Lista de etiquetas de ámbito para esta instancia de entidad.</span><span class="sxs-lookup"><span data-stu-id="a878a-143">List of Scope Tags for this Entity instance.</span></span> <span data-ttu-id="a878a-144">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="a878a-144">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="a878a-145">supportsScopeTags</span><span class="sxs-lookup"><span data-stu-id="a878a-145">supportsScopeTags</span></span>|<span data-ttu-id="a878a-146">Boolean</span><span class="sxs-lookup"><span data-stu-id="a878a-146">Boolean</span></span>|<span data-ttu-id="a878a-147">Indica si la configuración del dispositivo subyacente admite la asignación de etiquetas de ámbito.</span><span class="sxs-lookup"><span data-stu-id="a878a-147">Indicates whether or not the underlying Device Configuration supports the assignment of scope tags.</span></span> <span data-ttu-id="a878a-148">No se permite la asignación a la propiedad ScopeTags cuando este valor es false y entidades no estará visibles para los usuarios con ámbito.</span><span class="sxs-lookup"><span data-stu-id="a878a-148">Assigning to the ScopeTags property is not allowed when this value is false and entities will not be visible to scoped users.</span></span> <span data-ttu-id="a878a-149">Esto se produce para las directivas de heredado creadas en Silverlight y se puede resolver por eliminar y volver a crear la directiva en el Portal de Azure.</span><span class="sxs-lookup"><span data-stu-id="a878a-149">This occurs for Legacy policies created in Silverlight and can be resolved by deleting and recreating the policy in the Azure Portal.</span></span> <span data-ttu-id="a878a-150">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="a878a-150">This property is read-only.</span></span> <span data-ttu-id="a878a-151">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="a878a-151">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="a878a-152">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="a878a-152">createdDateTime</span></span>|<span data-ttu-id="a878a-153">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="a878a-153">DateTimeOffset</span></span>|<span data-ttu-id="a878a-154">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="a878a-154">DateTime the object was created.</span></span> <span data-ttu-id="a878a-155">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="a878a-155">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="a878a-156">descripción</span><span class="sxs-lookup"><span data-stu-id="a878a-156">description</span></span>|<span data-ttu-id="a878a-157">String</span><span class="sxs-lookup"><span data-stu-id="a878a-157">String</span></span>|<span data-ttu-id="a878a-158">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a878a-158">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="a878a-159">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="a878a-159">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="a878a-160">displayName</span><span class="sxs-lookup"><span data-stu-id="a878a-160">displayName</span></span>|<span data-ttu-id="a878a-161">String</span><span class="sxs-lookup"><span data-stu-id="a878a-161">String</span></span>|<span data-ttu-id="a878a-162">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a878a-162">Admin provided name of the device configuration.</span></span> <span data-ttu-id="a878a-163">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="a878a-163">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="a878a-164">version</span><span class="sxs-lookup"><span data-stu-id="a878a-164">version</span></span>|<span data-ttu-id="a878a-165">Int32</span><span class="sxs-lookup"><span data-stu-id="a878a-165">Int32</span></span>|<span data-ttu-id="a878a-166">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a878a-166">Version of the device configuration.</span></span> <span data-ttu-id="a878a-167">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="a878a-167">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="a878a-168">authenticationMethod</span><span class="sxs-lookup"><span data-stu-id="a878a-168">authenticationMethod</span></span>|[<span data-ttu-id="a878a-169">easAuthenticationMethod</span><span class="sxs-lookup"><span data-stu-id="a878a-169">easAuthenticationMethod</span></span>](../resources/intune-deviceconfig-easauthenticationmethod.md)|<span data-ttu-id="a878a-170">Método de autenticación para Exchange ActiveSync.</span><span class="sxs-lookup"><span data-stu-id="a878a-170">Authentication method for Exchange ActiveSync.</span></span> <span data-ttu-id="a878a-171">Se hereda de [androidWorkProfileEasEmailProfileBase](../resources/intune-deviceconfig-androidworkprofileeasemailprofilebase.md).</span><span class="sxs-lookup"><span data-stu-id="a878a-171">Inherited from [androidWorkProfileEasEmailProfileBase](../resources/intune-deviceconfig-androidworkprofileeasemailprofilebase.md).</span></span> <span data-ttu-id="a878a-172">Los valores posibles son: `usernameAndPassword` y `certificate`.</span><span class="sxs-lookup"><span data-stu-id="a878a-172">Possible values are: `usernameAndPassword`, `certificate`.</span></span>|
|<span data-ttu-id="a878a-173">durationOfEmailToSync</span><span class="sxs-lookup"><span data-stu-id="a878a-173">durationOfEmailToSync</span></span>|[<span data-ttu-id="a878a-174">emailSyncDuration</span><span class="sxs-lookup"><span data-stu-id="a878a-174">emailSyncDuration</span></span>](../resources/intune-deviceconfig-emailsyncduration.md)|<span data-ttu-id="a878a-175">Duración de correo electrónico de tiempo se debe sincronizar en.</span><span class="sxs-lookup"><span data-stu-id="a878a-175">Duration of time email should be synced to.</span></span> <span data-ttu-id="a878a-176">Se hereda de [androidWorkProfileEasEmailProfileBase](../resources/intune-deviceconfig-androidworkprofileeasemailprofilebase.md).</span><span class="sxs-lookup"><span data-stu-id="a878a-176">Inherited from [androidWorkProfileEasEmailProfileBase](../resources/intune-deviceconfig-androidworkprofileeasemailprofilebase.md).</span></span> <span data-ttu-id="a878a-177">Los valores posibles son: `userDefined`, `oneDay`, `threeDays`, `oneWeek`, `twoWeeks`, `oneMonth` y `unlimited`.</span><span class="sxs-lookup"><span data-stu-id="a878a-177">Possible values are: `userDefined`, `oneDay`, `threeDays`, `oneWeek`, `twoWeeks`, `oneMonth`, `unlimited`.</span></span>|
|<span data-ttu-id="a878a-178">emailAddressSource</span><span class="sxs-lookup"><span data-stu-id="a878a-178">emailAddressSource</span></span>|[<span data-ttu-id="a878a-179">userEmailSource</span><span class="sxs-lookup"><span data-stu-id="a878a-179">userEmailSource</span></span>](../resources/intune-deviceconfig-useremailsource.md)|<span data-ttu-id="a878a-180">Atributo de correo electrónico que se seleccionan de AAD y se insertan en este perfil antes de instalar en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a878a-180">Email attribute that is picked from AAD and injected into this profile before installing on the device.</span></span> <span data-ttu-id="a878a-181">Se hereda de [androidWorkProfileEasEmailProfileBase](../resources/intune-deviceconfig-androidworkprofileeasemailprofilebase.md).</span><span class="sxs-lookup"><span data-stu-id="a878a-181">Inherited from [androidWorkProfileEasEmailProfileBase](../resources/intune-deviceconfig-androidworkprofileeasemailprofilebase.md).</span></span> <span data-ttu-id="a878a-182">Los valores posibles son: `userPrincipalName` y `primarySmtpAddress`.</span><span class="sxs-lookup"><span data-stu-id="a878a-182">Possible values are: `userPrincipalName`, `primarySmtpAddress`.</span></span>|
|<span data-ttu-id="a878a-183">hostName</span><span class="sxs-lookup"><span data-stu-id="a878a-183">hostName</span></span>|<span data-ttu-id="a878a-184">String</span><span class="sxs-lookup"><span data-stu-id="a878a-184">String</span></span>|<span data-ttu-id="a878a-185">Ubicación de Exchange (URL) que la aplicación de correo se conecta a.</span><span class="sxs-lookup"><span data-stu-id="a878a-185">Exchange location (URL) that the mail app connects to.</span></span> <span data-ttu-id="a878a-186">Se hereda de [androidWorkProfileEasEmailProfileBase](../resources/intune-deviceconfig-androidworkprofileeasemailprofilebase.md)</span><span class="sxs-lookup"><span data-stu-id="a878a-186">Inherited from [androidWorkProfileEasEmailProfileBase](../resources/intune-deviceconfig-androidworkprofileeasemailprofilebase.md)</span></span>|
|<span data-ttu-id="a878a-187">requireSsl</span><span class="sxs-lookup"><span data-stu-id="a878a-187">requireSsl</span></span>|<span data-ttu-id="a878a-188">Boolean</span><span class="sxs-lookup"><span data-stu-id="a878a-188">Boolean</span></span>|<span data-ttu-id="a878a-189">Indica si se va a usar SSL o no.</span><span class="sxs-lookup"><span data-stu-id="a878a-189">Indicates whether or not to use SSL.</span></span> <span data-ttu-id="a878a-190">Se hereda de [androidWorkProfileEasEmailProfileBase](../resources/intune-deviceconfig-androidworkprofileeasemailprofilebase.md)</span><span class="sxs-lookup"><span data-stu-id="a878a-190">Inherited from [androidWorkProfileEasEmailProfileBase](../resources/intune-deviceconfig-androidworkprofileeasemailprofilebase.md)</span></span>|
|<span data-ttu-id="a878a-191">usernameSource</span><span class="sxs-lookup"><span data-stu-id="a878a-191">usernameSource</span></span>|[<span data-ttu-id="a878a-192">androidUsernameSource</span><span class="sxs-lookup"><span data-stu-id="a878a-192">androidUsernameSource</span></span>](../resources/intune-deviceconfig-androidusernamesource.md)|<span data-ttu-id="a878a-193">Atributo de nombre de usuario que se seleccionan de AAD y se insertan en este perfil antes de instalar en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a878a-193">Username attribute that is picked from AAD and injected into this profile before installing on the device.</span></span> <span data-ttu-id="a878a-194">Se hereda de [androidWorkProfileEasEmailProfileBase](../resources/intune-deviceconfig-androidworkprofileeasemailprofilebase.md).</span><span class="sxs-lookup"><span data-stu-id="a878a-194">Inherited from [androidWorkProfileEasEmailProfileBase](../resources/intune-deviceconfig-androidworkprofileeasemailprofilebase.md).</span></span> <span data-ttu-id="a878a-195">Los valores posibles son: `username`, `userPrincipalName`, `samAccountName` y `primarySmtpAddress`.</span><span class="sxs-lookup"><span data-stu-id="a878a-195">Possible values are: `username`, `userPrincipalName`, `samAccountName`, `primarySmtpAddress`.</span></span>|



## <a name="response"></a><span data-ttu-id="a878a-196">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a878a-196">Response</span></span>
<span data-ttu-id="a878a-197">Si tiene éxito, este método devuelve una `201 Created` código de respuesta y un objeto [androidWorkProfileGmailEasConfiguration](../resources/intune-deviceconfig-androidworkprofilegmaileasconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a878a-197">If successful, this method returns a `201 Created` response code and a [androidWorkProfileGmailEasConfiguration](../resources/intune-deviceconfig-androidworkprofilegmaileasconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="a878a-198">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a878a-198">Example</span></span>
### <a name="request"></a><span data-ttu-id="a878a-199">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a878a-199">Request</span></span>
<span data-ttu-id="a878a-200">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a878a-200">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations
Content-type: application/json
Content-length: 559

{
  "@odata.type": "#microsoft.graph.androidWorkProfileGmailEasConfiguration",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "roleScopeTagIds": [
    "Role Scope Tag Ids value"
  ],
  "supportsScopeTags": true,
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "authenticationMethod": "certificate",
  "durationOfEmailToSync": "oneDay",
  "emailAddressSource": "primarySmtpAddress",
  "hostName": "Host Name value",
  "requireSsl": true,
  "usernameSource": "userPrincipalName"
}
```

### <a name="response"></a><span data-ttu-id="a878a-201">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a878a-201">Response</span></span>
<span data-ttu-id="a878a-p117">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="a878a-p117">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 667

{
  "@odata.type": "#microsoft.graph.androidWorkProfileGmailEasConfiguration",
  "id": "a4a44bb5-4bb5-a4a4-b54b-a4a4b54ba4a4",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "roleScopeTagIds": [
    "Role Scope Tag Ids value"
  ],
  "supportsScopeTags": true,
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "authenticationMethod": "certificate",
  "durationOfEmailToSync": "oneDay",
  "emailAddressSource": "primarySmtpAddress",
  "hostName": "Host Name value",
  "requireSsl": true,
  "usernameSource": "userPrincipalName"
}
```





