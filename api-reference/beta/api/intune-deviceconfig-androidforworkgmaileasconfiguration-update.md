---
title: Actualizar androidForWorkGmailEasConfiguration
description: Actualizar las propiedades de un objeto androidForWorkGmailEasConfiguration.
author: tfitzmac
ms.openlocfilehash: 9da99cb4ecb0d466a8367e2d7b5ad3902956e1c7
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27317797"
---
# <a name="update-androidforworkgmaileasconfiguration"></a><span data-ttu-id="0dd92-103">Actualizar androidForWorkGmailEasConfiguration</span><span class="sxs-lookup"><span data-stu-id="0dd92-103">Update androidForWorkGmailEasConfiguration</span></span>

> <span data-ttu-id="0dd92-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="0dd92-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="0dd92-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="0dd92-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="0dd92-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="0dd92-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="0dd92-107">Actualizar las propiedades de un objeto [androidForWorkGmailEasConfiguration](../resources/intune-deviceconfig-androidforworkgmaileasconfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="0dd92-107">Update the properties of a [androidForWorkGmailEasConfiguration](../resources/intune-deviceconfig-androidforworkgmaileasconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="0dd92-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="0dd92-108">Prerequisites</span></span>
<span data-ttu-id="0dd92-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="0dd92-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="0dd92-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="0dd92-111">Permission type</span></span>|<span data-ttu-id="0dd92-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="0dd92-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="0dd92-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="0dd92-113">Delegated (work or school account)</span></span>|<span data-ttu-id="0dd92-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="0dd92-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="0dd92-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="0dd92-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="0dd92-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="0dd92-116">Not supported.</span></span>|
|<span data-ttu-id="0dd92-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="0dd92-117">Application</span></span>|<span data-ttu-id="0dd92-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="0dd92-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="0dd92-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="0dd92-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/groupAssignments/{deviceConfigurationGroupAssignmentId}/deviceConfiguration
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsDomainJoinConfiguration/networkAccessConfigurations/{deviceConfigurationId}
```

## <a name="request-headers"></a><span data-ttu-id="0dd92-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="0dd92-120">Request headers</span></span>
|<span data-ttu-id="0dd92-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0dd92-121">Header</span></span>|<span data-ttu-id="0dd92-122">Valor</span><span class="sxs-lookup"><span data-stu-id="0dd92-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="0dd92-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="0dd92-123">Authorization</span></span>|<span data-ttu-id="0dd92-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="0dd92-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="0dd92-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="0dd92-125">Accept</span></span>|<span data-ttu-id="0dd92-126">application/json</span><span class="sxs-lookup"><span data-stu-id="0dd92-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="0dd92-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="0dd92-127">Request body</span></span>
<span data-ttu-id="0dd92-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto [androidForWorkGmailEasConfiguration](../resources/intune-deviceconfig-androidforworkgmaileasconfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="0dd92-128">In the request body, supply a JSON representation for the [androidForWorkGmailEasConfiguration](../resources/intune-deviceconfig-androidforworkgmaileasconfiguration.md) object.</span></span>

<span data-ttu-id="0dd92-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el [androidForWorkGmailEasConfiguration](../resources/intune-deviceconfig-androidforworkgmaileasconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="0dd92-129">The following table shows the properties that are required when you create the [androidForWorkGmailEasConfiguration](../resources/intune-deviceconfig-androidforworkgmaileasconfiguration.md).</span></span>

|<span data-ttu-id="0dd92-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="0dd92-130">Property</span></span>|<span data-ttu-id="0dd92-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="0dd92-131">Type</span></span>|<span data-ttu-id="0dd92-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="0dd92-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="0dd92-133">id</span><span class="sxs-lookup"><span data-stu-id="0dd92-133">id</span></span>|<span data-ttu-id="0dd92-134">String</span><span class="sxs-lookup"><span data-stu-id="0dd92-134">String</span></span>|<span data-ttu-id="0dd92-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="0dd92-135">Key of the entity.</span></span> <span data-ttu-id="0dd92-136">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="0dd92-136">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="0dd92-137">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="0dd92-137">lastModifiedDateTime</span></span>|<span data-ttu-id="0dd92-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="0dd92-138">DateTimeOffset</span></span>|<span data-ttu-id="0dd92-139">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="0dd92-139">DateTime the object was last modified.</span></span> <span data-ttu-id="0dd92-140">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="0dd92-140">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="0dd92-141">roleScopeTagIds</span><span class="sxs-lookup"><span data-stu-id="0dd92-141">roleScopeTagIds</span></span>|<span data-ttu-id="0dd92-142">Colección String</span><span class="sxs-lookup"><span data-stu-id="0dd92-142">String collection</span></span>|<span data-ttu-id="0dd92-143">Lista de etiquetas de ámbito para esta instancia de entidad.</span><span class="sxs-lookup"><span data-stu-id="0dd92-143">List of Scope Tags for this Entity instance.</span></span> <span data-ttu-id="0dd92-144">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="0dd92-144">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="0dd92-145">supportsScopeTags</span><span class="sxs-lookup"><span data-stu-id="0dd92-145">supportsScopeTags</span></span>|<span data-ttu-id="0dd92-146">Boolean</span><span class="sxs-lookup"><span data-stu-id="0dd92-146">Boolean</span></span>|<span data-ttu-id="0dd92-147">Indica si la configuración del dispositivo subyacente admite la asignación de etiquetas de ámbito.</span><span class="sxs-lookup"><span data-stu-id="0dd92-147">Indicates whether or not the underlying Device Configuration supports the assignment of scope tags.</span></span> <span data-ttu-id="0dd92-148">No se permite la asignación a la propiedad ScopeTags cuando este valor es false y entidades no estará visibles para los usuarios con ámbito.</span><span class="sxs-lookup"><span data-stu-id="0dd92-148">Assigning to the ScopeTags property is not allowed when this value is false and entities will not be visible to scoped users.</span></span> <span data-ttu-id="0dd92-149">Esto se produce para las directivas de heredado creadas en Silverlight y se puede resolver por eliminar y volver a crear la directiva en el Portal de Azure.</span><span class="sxs-lookup"><span data-stu-id="0dd92-149">This occurs for Legacy policies created in Silverlight and can be resolved by deleting and recreating the policy in the Azure Portal.</span></span> <span data-ttu-id="0dd92-150">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="0dd92-150">This property is read-only.</span></span> <span data-ttu-id="0dd92-151">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="0dd92-151">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="0dd92-152">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="0dd92-152">createdDateTime</span></span>|<span data-ttu-id="0dd92-153">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="0dd92-153">DateTimeOffset</span></span>|<span data-ttu-id="0dd92-154">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="0dd92-154">DateTime the object was created.</span></span> <span data-ttu-id="0dd92-155">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="0dd92-155">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="0dd92-156">descripción</span><span class="sxs-lookup"><span data-stu-id="0dd92-156">description</span></span>|<span data-ttu-id="0dd92-157">String</span><span class="sxs-lookup"><span data-stu-id="0dd92-157">String</span></span>|<span data-ttu-id="0dd92-158">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0dd92-158">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="0dd92-159">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="0dd92-159">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="0dd92-160">displayName</span><span class="sxs-lookup"><span data-stu-id="0dd92-160">displayName</span></span>|<span data-ttu-id="0dd92-161">String</span><span class="sxs-lookup"><span data-stu-id="0dd92-161">String</span></span>|<span data-ttu-id="0dd92-162">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0dd92-162">Admin provided name of the device configuration.</span></span> <span data-ttu-id="0dd92-163">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="0dd92-163">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="0dd92-164">version</span><span class="sxs-lookup"><span data-stu-id="0dd92-164">version</span></span>|<span data-ttu-id="0dd92-165">Int32</span><span class="sxs-lookup"><span data-stu-id="0dd92-165">Int32</span></span>|<span data-ttu-id="0dd92-166">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0dd92-166">Version of the device configuration.</span></span> <span data-ttu-id="0dd92-167">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="0dd92-167">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="0dd92-168">authenticationMethod</span><span class="sxs-lookup"><span data-stu-id="0dd92-168">authenticationMethod</span></span>|[<span data-ttu-id="0dd92-169">easAuthenticationMethod</span><span class="sxs-lookup"><span data-stu-id="0dd92-169">easAuthenticationMethod</span></span>](../resources/intune-deviceconfig-easauthenticationmethod.md)|<span data-ttu-id="0dd92-170">Método de autenticación para Exchange ActiveSync.</span><span class="sxs-lookup"><span data-stu-id="0dd92-170">Authentication method for Exchange ActiveSync.</span></span> <span data-ttu-id="0dd92-171">Se hereda de [androidForWorkEasEmailProfileBase](../resources/intune-deviceconfig-androidforworkeasemailprofilebase.md).</span><span class="sxs-lookup"><span data-stu-id="0dd92-171">Inherited from [androidForWorkEasEmailProfileBase](../resources/intune-deviceconfig-androidforworkeasemailprofilebase.md).</span></span> <span data-ttu-id="0dd92-172">Los valores posibles son: `usernameAndPassword` y `certificate`.</span><span class="sxs-lookup"><span data-stu-id="0dd92-172">Possible values are: `usernameAndPassword`, `certificate`.</span></span>|
|<span data-ttu-id="0dd92-173">durationOfEmailToSync</span><span class="sxs-lookup"><span data-stu-id="0dd92-173">durationOfEmailToSync</span></span>|[<span data-ttu-id="0dd92-174">emailSyncDuration</span><span class="sxs-lookup"><span data-stu-id="0dd92-174">emailSyncDuration</span></span>](../resources/intune-deviceconfig-emailsyncduration.md)|<span data-ttu-id="0dd92-175">Duración de correo electrónico de tiempo se debe sincronizar en.</span><span class="sxs-lookup"><span data-stu-id="0dd92-175">Duration of time email should be synced to.</span></span> <span data-ttu-id="0dd92-176">Se hereda de [androidForWorkEasEmailProfileBase](../resources/intune-deviceconfig-androidforworkeasemailprofilebase.md).</span><span class="sxs-lookup"><span data-stu-id="0dd92-176">Inherited from [androidForWorkEasEmailProfileBase](../resources/intune-deviceconfig-androidforworkeasemailprofilebase.md).</span></span> <span data-ttu-id="0dd92-177">Los valores posibles son: `userDefined`, `oneDay`, `threeDays`, `oneWeek`, `twoWeeks`, `oneMonth` y `unlimited`.</span><span class="sxs-lookup"><span data-stu-id="0dd92-177">Possible values are: `userDefined`, `oneDay`, `threeDays`, `oneWeek`, `twoWeeks`, `oneMonth`, `unlimited`.</span></span>|
|<span data-ttu-id="0dd92-178">emailAddressSource</span><span class="sxs-lookup"><span data-stu-id="0dd92-178">emailAddressSource</span></span>|[<span data-ttu-id="0dd92-179">userEmailSource</span><span class="sxs-lookup"><span data-stu-id="0dd92-179">userEmailSource</span></span>](../resources/intune-deviceconfig-useremailsource.md)|<span data-ttu-id="0dd92-180">Atributo de correo electrónico que se seleccionan de AAD y se insertan en este perfil antes de instalar en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0dd92-180">Email attribute that is picked from AAD and injected into this profile before installing on the device.</span></span> <span data-ttu-id="0dd92-181">Se hereda de [androidForWorkEasEmailProfileBase](../resources/intune-deviceconfig-androidforworkeasemailprofilebase.md).</span><span class="sxs-lookup"><span data-stu-id="0dd92-181">Inherited from [androidForWorkEasEmailProfileBase](../resources/intune-deviceconfig-androidforworkeasemailprofilebase.md).</span></span> <span data-ttu-id="0dd92-182">Los valores posibles son: `userPrincipalName` y `primarySmtpAddress`.</span><span class="sxs-lookup"><span data-stu-id="0dd92-182">Possible values are: `userPrincipalName`, `primarySmtpAddress`.</span></span>|
|<span data-ttu-id="0dd92-183">hostName</span><span class="sxs-lookup"><span data-stu-id="0dd92-183">hostName</span></span>|<span data-ttu-id="0dd92-184">String</span><span class="sxs-lookup"><span data-stu-id="0dd92-184">String</span></span>|<span data-ttu-id="0dd92-185">Ubicación de Exchange (URL) que la aplicación de correo se conecta a.</span><span class="sxs-lookup"><span data-stu-id="0dd92-185">Exchange location (URL) that the mail app connects to.</span></span> <span data-ttu-id="0dd92-186">Se hereda de [androidForWorkEasEmailProfileBase](../resources/intune-deviceconfig-androidforworkeasemailprofilebase.md)</span><span class="sxs-lookup"><span data-stu-id="0dd92-186">Inherited from [androidForWorkEasEmailProfileBase](../resources/intune-deviceconfig-androidforworkeasemailprofilebase.md)</span></span>|
|<span data-ttu-id="0dd92-187">requireSsl</span><span class="sxs-lookup"><span data-stu-id="0dd92-187">requireSsl</span></span>|<span data-ttu-id="0dd92-188">Boolean</span><span class="sxs-lookup"><span data-stu-id="0dd92-188">Boolean</span></span>|<span data-ttu-id="0dd92-189">Indica si se va a usar SSL o no.</span><span class="sxs-lookup"><span data-stu-id="0dd92-189">Indicates whether or not to use SSL.</span></span> <span data-ttu-id="0dd92-190">Se hereda de [androidForWorkEasEmailProfileBase](../resources/intune-deviceconfig-androidforworkeasemailprofilebase.md)</span><span class="sxs-lookup"><span data-stu-id="0dd92-190">Inherited from [androidForWorkEasEmailProfileBase](../resources/intune-deviceconfig-androidforworkeasemailprofilebase.md)</span></span>|
|<span data-ttu-id="0dd92-191">usernameSource</span><span class="sxs-lookup"><span data-stu-id="0dd92-191">usernameSource</span></span>|[<span data-ttu-id="0dd92-192">androidUsernameSource</span><span class="sxs-lookup"><span data-stu-id="0dd92-192">androidUsernameSource</span></span>](../resources/intune-deviceconfig-androidusernamesource.md)|<span data-ttu-id="0dd92-193">Atributo de nombre de usuario que se seleccionan de AAD y se insertan en este perfil antes de instalar en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0dd92-193">Username attribute that is picked from AAD and injected into this profile before installing on the device.</span></span> <span data-ttu-id="0dd92-194">Se hereda de [androidForWorkEasEmailProfileBase](../resources/intune-deviceconfig-androidforworkeasemailprofilebase.md).</span><span class="sxs-lookup"><span data-stu-id="0dd92-194">Inherited from [androidForWorkEasEmailProfileBase](../resources/intune-deviceconfig-androidforworkeasemailprofilebase.md).</span></span> <span data-ttu-id="0dd92-195">Los valores posibles son: `username`, `userPrincipalName`, `samAccountName` y `primarySmtpAddress`.</span><span class="sxs-lookup"><span data-stu-id="0dd92-195">Possible values are: `username`, `userPrincipalName`, `samAccountName`, `primarySmtpAddress`.</span></span>|



## <a name="response"></a><span data-ttu-id="0dd92-196">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0dd92-196">Response</span></span>
<span data-ttu-id="0dd92-197">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto actualizado [androidForWorkGmailEasConfiguration](../resources/intune-deviceconfig-androidforworkgmaileasconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0dd92-197">If successful, this method returns a `200 OK` response code and an updated [androidForWorkGmailEasConfiguration](../resources/intune-deviceconfig-androidforworkgmaileasconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="0dd92-198">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="0dd92-198">Example</span></span>
### <a name="request"></a><span data-ttu-id="0dd92-199">Solicitud</span><span class="sxs-lookup"><span data-stu-id="0dd92-199">Request</span></span>
<span data-ttu-id="0dd92-200">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="0dd92-200">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations/{deviceConfigurationId}
Content-type: application/json
Content-length: 481

{
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

### <a name="response"></a><span data-ttu-id="0dd92-201">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0dd92-201">Response</span></span>
<span data-ttu-id="0dd92-p117">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="0dd92-p117">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 663

{
  "@odata.type": "#microsoft.graph.androidForWorkGmailEasConfiguration",
  "id": "2bafc891-c891-2baf-91c8-af2b91c8af2b",
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





