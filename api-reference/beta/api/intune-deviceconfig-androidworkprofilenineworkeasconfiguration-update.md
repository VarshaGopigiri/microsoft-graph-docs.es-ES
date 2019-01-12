---
title: Actualizar androidWorkProfileNineWorkEasConfiguration
description: Actualizar las propiedades de un objeto androidWorkProfileNineWorkEasConfiguration.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 6eb42fd868b5e262c83a740847a107f4de4da518
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27944281"
---
# <a name="update-androidworkprofilenineworkeasconfiguration"></a><span data-ttu-id="7ba76-103">Actualizar androidWorkProfileNineWorkEasConfiguration</span><span class="sxs-lookup"><span data-stu-id="7ba76-103">Update androidWorkProfileNineWorkEasConfiguration</span></span>

> <span data-ttu-id="7ba76-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="7ba76-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="7ba76-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="7ba76-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="7ba76-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="7ba76-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="7ba76-107">Actualizar las propiedades de un objeto [androidWorkProfileNineWorkEasConfiguration](../resources/intune-deviceconfig-androidworkprofilenineworkeasconfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="7ba76-107">Update the properties of a [androidWorkProfileNineWorkEasConfiguration](../resources/intune-deviceconfig-androidworkprofilenineworkeasconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="7ba76-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="7ba76-108">Prerequisites</span></span>
<span data-ttu-id="7ba76-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="7ba76-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="7ba76-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="7ba76-111">Permission type</span></span>|<span data-ttu-id="7ba76-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="7ba76-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="7ba76-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="7ba76-113">Delegated (work or school account)</span></span>|<span data-ttu-id="7ba76-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="7ba76-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="7ba76-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="7ba76-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="7ba76-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="7ba76-116">Not supported.</span></span>|
|<span data-ttu-id="7ba76-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="7ba76-117">Application</span></span>|<span data-ttu-id="7ba76-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="7ba76-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="7ba76-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="7ba76-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/groupAssignments/{deviceConfigurationGroupAssignmentId}/deviceConfiguration
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsDomainJoinConfiguration/networkAccessConfigurations/{deviceConfigurationId}
```

## <a name="request-headers"></a><span data-ttu-id="7ba76-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="7ba76-120">Request headers</span></span>
|<span data-ttu-id="7ba76-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7ba76-121">Header</span></span>|<span data-ttu-id="7ba76-122">Valor</span><span class="sxs-lookup"><span data-stu-id="7ba76-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="7ba76-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="7ba76-123">Authorization</span></span>|<span data-ttu-id="7ba76-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="7ba76-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="7ba76-125">Accept</span><span class="sxs-lookup"><span data-stu-id="7ba76-125">Accept</span></span>|<span data-ttu-id="7ba76-126">application/json</span><span class="sxs-lookup"><span data-stu-id="7ba76-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="7ba76-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="7ba76-127">Request body</span></span>
<span data-ttu-id="7ba76-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto [androidWorkProfileNineWorkEasConfiguration](../resources/intune-deviceconfig-androidworkprofilenineworkeasconfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="7ba76-128">In the request body, supply a JSON representation for the [androidWorkProfileNineWorkEasConfiguration](../resources/intune-deviceconfig-androidworkprofilenineworkeasconfiguration.md) object.</span></span>

<span data-ttu-id="7ba76-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el [androidWorkProfileNineWorkEasConfiguration](../resources/intune-deviceconfig-androidworkprofilenineworkeasconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="7ba76-129">The following table shows the properties that are required when you create the [androidWorkProfileNineWorkEasConfiguration](../resources/intune-deviceconfig-androidworkprofilenineworkeasconfiguration.md).</span></span>

|<span data-ttu-id="7ba76-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="7ba76-130">Property</span></span>|<span data-ttu-id="7ba76-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="7ba76-131">Type</span></span>|<span data-ttu-id="7ba76-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="7ba76-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="7ba76-133">id</span><span class="sxs-lookup"><span data-stu-id="7ba76-133">id</span></span>|<span data-ttu-id="7ba76-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="7ba76-134">String</span></span>|<span data-ttu-id="7ba76-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="7ba76-135">Key of the entity.</span></span> <span data-ttu-id="7ba76-136">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="7ba76-136">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="7ba76-137">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="7ba76-137">lastModifiedDateTime</span></span>|<span data-ttu-id="7ba76-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="7ba76-138">DateTimeOffset</span></span>|<span data-ttu-id="7ba76-139">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="7ba76-139">DateTime the object was last modified.</span></span> <span data-ttu-id="7ba76-140">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="7ba76-140">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="7ba76-141">roleScopeTagIds</span><span class="sxs-lookup"><span data-stu-id="7ba76-141">roleScopeTagIds</span></span>|<span data-ttu-id="7ba76-142">Colección String</span><span class="sxs-lookup"><span data-stu-id="7ba76-142">String collection</span></span>|<span data-ttu-id="7ba76-143">Lista de etiquetas de ámbito para esta instancia de entidad.</span><span class="sxs-lookup"><span data-stu-id="7ba76-143">List of Scope Tags for this Entity instance.</span></span> <span data-ttu-id="7ba76-144">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="7ba76-144">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="7ba76-145">supportsScopeTags</span><span class="sxs-lookup"><span data-stu-id="7ba76-145">supportsScopeTags</span></span>|<span data-ttu-id="7ba76-146">Booleano</span><span class="sxs-lookup"><span data-stu-id="7ba76-146">Boolean</span></span>|<span data-ttu-id="7ba76-147">Indica si la configuración del dispositivo subyacente admite la asignación de etiquetas de ámbito.</span><span class="sxs-lookup"><span data-stu-id="7ba76-147">Indicates whether or not the underlying Device Configuration supports the assignment of scope tags.</span></span> <span data-ttu-id="7ba76-148">No se permite la asignación a la propiedad ScopeTags cuando este valor es false y entidades no estará visibles para los usuarios con ámbito.</span><span class="sxs-lookup"><span data-stu-id="7ba76-148">Assigning to the ScopeTags property is not allowed when this value is false and entities will not be visible to scoped users.</span></span> <span data-ttu-id="7ba76-149">Esto se produce para las directivas de heredado creadas en Silverlight y se puede resolver por eliminar y volver a crear la directiva en el Portal de Azure.</span><span class="sxs-lookup"><span data-stu-id="7ba76-149">This occurs for Legacy policies created in Silverlight and can be resolved by deleting and recreating the policy in the Azure Portal.</span></span> <span data-ttu-id="7ba76-150">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="7ba76-150">This property is read-only.</span></span> <span data-ttu-id="7ba76-151">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="7ba76-151">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="7ba76-152">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="7ba76-152">createdDateTime</span></span>|<span data-ttu-id="7ba76-153">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="7ba76-153">DateTimeOffset</span></span>|<span data-ttu-id="7ba76-154">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="7ba76-154">DateTime the object was created.</span></span> <span data-ttu-id="7ba76-155">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="7ba76-155">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="7ba76-156">descripción</span><span class="sxs-lookup"><span data-stu-id="7ba76-156">description</span></span>|<span data-ttu-id="7ba76-157">Cadena</span><span class="sxs-lookup"><span data-stu-id="7ba76-157">String</span></span>|<span data-ttu-id="7ba76-158">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7ba76-158">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="7ba76-159">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="7ba76-159">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="7ba76-160">displayName</span><span class="sxs-lookup"><span data-stu-id="7ba76-160">displayName</span></span>|<span data-ttu-id="7ba76-161">Cadena</span><span class="sxs-lookup"><span data-stu-id="7ba76-161">String</span></span>|<span data-ttu-id="7ba76-162">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7ba76-162">Admin provided name of the device configuration.</span></span> <span data-ttu-id="7ba76-163">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="7ba76-163">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="7ba76-164">version</span><span class="sxs-lookup"><span data-stu-id="7ba76-164">version</span></span>|<span data-ttu-id="7ba76-165">Int32</span><span class="sxs-lookup"><span data-stu-id="7ba76-165">Int32</span></span>|<span data-ttu-id="7ba76-166">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7ba76-166">Version of the device configuration.</span></span> <span data-ttu-id="7ba76-167">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="7ba76-167">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="7ba76-168">authenticationMethod</span><span class="sxs-lookup"><span data-stu-id="7ba76-168">authenticationMethod</span></span>|[<span data-ttu-id="7ba76-169">easAuthenticationMethod</span><span class="sxs-lookup"><span data-stu-id="7ba76-169">easAuthenticationMethod</span></span>](../resources/intune-deviceconfig-easauthenticationmethod.md)|<span data-ttu-id="7ba76-170">Método de autenticación para Exchange ActiveSync.</span><span class="sxs-lookup"><span data-stu-id="7ba76-170">Authentication method for Exchange ActiveSync.</span></span> <span data-ttu-id="7ba76-171">Se hereda de [androidWorkProfileEasEmailProfileBase](../resources/intune-deviceconfig-androidworkprofileeasemailprofilebase.md).</span><span class="sxs-lookup"><span data-stu-id="7ba76-171">Inherited from [androidWorkProfileEasEmailProfileBase](../resources/intune-deviceconfig-androidworkprofileeasemailprofilebase.md).</span></span> <span data-ttu-id="7ba76-172">Los valores posibles son: `usernameAndPassword` y `certificate`.</span><span class="sxs-lookup"><span data-stu-id="7ba76-172">Possible values are: `usernameAndPassword`, `certificate`.</span></span>|
|<span data-ttu-id="7ba76-173">durationOfEmailToSync</span><span class="sxs-lookup"><span data-stu-id="7ba76-173">durationOfEmailToSync</span></span>|[<span data-ttu-id="7ba76-174">emailSyncDuration</span><span class="sxs-lookup"><span data-stu-id="7ba76-174">emailSyncDuration</span></span>](../resources/intune-deviceconfig-emailsyncduration.md)|<span data-ttu-id="7ba76-175">Duración de correo electrónico de tiempo se debe sincronizar en.</span><span class="sxs-lookup"><span data-stu-id="7ba76-175">Duration of time email should be synced to.</span></span> <span data-ttu-id="7ba76-176">Se hereda de [androidWorkProfileEasEmailProfileBase](../resources/intune-deviceconfig-androidworkprofileeasemailprofilebase.md).</span><span class="sxs-lookup"><span data-stu-id="7ba76-176">Inherited from [androidWorkProfileEasEmailProfileBase](../resources/intune-deviceconfig-androidworkprofileeasemailprofilebase.md).</span></span> <span data-ttu-id="7ba76-177">Los valores posibles son: `userDefined`, `oneDay`, `threeDays`, `oneWeek`, `twoWeeks`, `oneMonth` y `unlimited`.</span><span class="sxs-lookup"><span data-stu-id="7ba76-177">Possible values are: `userDefined`, `oneDay`, `threeDays`, `oneWeek`, `twoWeeks`, `oneMonth`, `unlimited`.</span></span>|
|<span data-ttu-id="7ba76-178">emailAddressSource</span><span class="sxs-lookup"><span data-stu-id="7ba76-178">emailAddressSource</span></span>|[<span data-ttu-id="7ba76-179">userEmailSource</span><span class="sxs-lookup"><span data-stu-id="7ba76-179">userEmailSource</span></span>](../resources/intune-deviceconfig-useremailsource.md)|<span data-ttu-id="7ba76-180">Atributo de correo electrónico que se seleccionan de AAD y se insertan en este perfil antes de instalar en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7ba76-180">Email attribute that is picked from AAD and injected into this profile before installing on the device.</span></span> <span data-ttu-id="7ba76-181">Se hereda de [androidWorkProfileEasEmailProfileBase](../resources/intune-deviceconfig-androidworkprofileeasemailprofilebase.md).</span><span class="sxs-lookup"><span data-stu-id="7ba76-181">Inherited from [androidWorkProfileEasEmailProfileBase](../resources/intune-deviceconfig-androidworkprofileeasemailprofilebase.md).</span></span> <span data-ttu-id="7ba76-182">Los valores posibles son: `userPrincipalName` y `primarySmtpAddress`.</span><span class="sxs-lookup"><span data-stu-id="7ba76-182">Possible values are: `userPrincipalName`, `primarySmtpAddress`.</span></span>|
|<span data-ttu-id="7ba76-183">hostName</span><span class="sxs-lookup"><span data-stu-id="7ba76-183">hostName</span></span>|<span data-ttu-id="7ba76-184">String</span><span class="sxs-lookup"><span data-stu-id="7ba76-184">String</span></span>|<span data-ttu-id="7ba76-185">Ubicación de Exchange (URL) que la aplicación de correo se conecta a.</span><span class="sxs-lookup"><span data-stu-id="7ba76-185">Exchange location (URL) that the mail app connects to.</span></span> <span data-ttu-id="7ba76-186">Se hereda de [androidWorkProfileEasEmailProfileBase](../resources/intune-deviceconfig-androidworkprofileeasemailprofilebase.md)</span><span class="sxs-lookup"><span data-stu-id="7ba76-186">Inherited from [androidWorkProfileEasEmailProfileBase](../resources/intune-deviceconfig-androidworkprofileeasemailprofilebase.md)</span></span>|
|<span data-ttu-id="7ba76-187">requireSsl</span><span class="sxs-lookup"><span data-stu-id="7ba76-187">requireSsl</span></span>|<span data-ttu-id="7ba76-188">Booleano</span><span class="sxs-lookup"><span data-stu-id="7ba76-188">Boolean</span></span>|<span data-ttu-id="7ba76-189">Indica si se va a usar SSL o no.</span><span class="sxs-lookup"><span data-stu-id="7ba76-189">Indicates whether or not to use SSL.</span></span> <span data-ttu-id="7ba76-190">Se hereda de [androidWorkProfileEasEmailProfileBase](../resources/intune-deviceconfig-androidworkprofileeasemailprofilebase.md)</span><span class="sxs-lookup"><span data-stu-id="7ba76-190">Inherited from [androidWorkProfileEasEmailProfileBase](../resources/intune-deviceconfig-androidworkprofileeasemailprofilebase.md)</span></span>|
|<span data-ttu-id="7ba76-191">usernameSource</span><span class="sxs-lookup"><span data-stu-id="7ba76-191">usernameSource</span></span>|[<span data-ttu-id="7ba76-192">androidUsernameSource</span><span class="sxs-lookup"><span data-stu-id="7ba76-192">androidUsernameSource</span></span>](../resources/intune-deviceconfig-androidusernamesource.md)|<span data-ttu-id="7ba76-193">Atributo de nombre de usuario que se seleccionan de AAD y se insertan en este perfil antes de instalar en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7ba76-193">Username attribute that is picked from AAD and injected into this profile before installing on the device.</span></span> <span data-ttu-id="7ba76-194">Se hereda de [androidWorkProfileEasEmailProfileBase](../resources/intune-deviceconfig-androidworkprofileeasemailprofilebase.md).</span><span class="sxs-lookup"><span data-stu-id="7ba76-194">Inherited from [androidWorkProfileEasEmailProfileBase](../resources/intune-deviceconfig-androidworkprofileeasemailprofilebase.md).</span></span> <span data-ttu-id="7ba76-195">Los valores posibles son: `username`, `userPrincipalName`, `samAccountName` y `primarySmtpAddress`.</span><span class="sxs-lookup"><span data-stu-id="7ba76-195">Possible values are: `username`, `userPrincipalName`, `samAccountName`, `primarySmtpAddress`.</span></span>|
|<span data-ttu-id="7ba76-196">syncCalendar</span><span class="sxs-lookup"><span data-stu-id="7ba76-196">syncCalendar</span></span>|<span data-ttu-id="7ba76-197">Booleano</span><span class="sxs-lookup"><span data-stu-id="7ba76-197">Boolean</span></span>|<span data-ttu-id="7ba76-198">Activa o desactiva la sincronización del calendario.</span><span class="sxs-lookup"><span data-stu-id="7ba76-198">Toggles syncing the calendar.</span></span> <span data-ttu-id="7ba76-199">Si se establece en false el calendario está desactivado en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7ba76-199">If set to false the calendar is turned off on the device.</span></span>|
|<span data-ttu-id="7ba76-200">syncContacts</span><span class="sxs-lookup"><span data-stu-id="7ba76-200">syncContacts</span></span>|<span data-ttu-id="7ba76-201">Booleano</span><span class="sxs-lookup"><span data-stu-id="7ba76-201">Boolean</span></span>|<span data-ttu-id="7ba76-202">Activa o desactiva la sincronización de contactos.</span><span class="sxs-lookup"><span data-stu-id="7ba76-202">Toggles syncing contacts.</span></span> <span data-ttu-id="7ba76-203">Si establece en false contactos está desactivado en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7ba76-203">If set to false contacts are turned off on the device.</span></span>|
|<span data-ttu-id="7ba76-204">syncTasks</span><span class="sxs-lookup"><span data-stu-id="7ba76-204">syncTasks</span></span>|<span data-ttu-id="7ba76-205">Booleano</span><span class="sxs-lookup"><span data-stu-id="7ba76-205">Boolean</span></span>|<span data-ttu-id="7ba76-206">Activa o desactiva la sincronización de tareas.</span><span class="sxs-lookup"><span data-stu-id="7ba76-206">Toggles syncing tasks.</span></span> <span data-ttu-id="7ba76-207">Si establece en false tareas está desactivado en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7ba76-207">If set to false tasks are turned off on the device.</span></span>|



## <a name="response"></a><span data-ttu-id="7ba76-208">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7ba76-208">Response</span></span>
<span data-ttu-id="7ba76-209">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto actualizado [androidWorkProfileNineWorkEasConfiguration](../resources/intune-deviceconfig-androidworkprofilenineworkeasconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7ba76-209">If successful, this method returns a `200 OK` response code and an updated [androidWorkProfileNineWorkEasConfiguration](../resources/intune-deviceconfig-androidworkprofilenineworkeasconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="7ba76-210">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7ba76-210">Example</span></span>
### <a name="request"></a><span data-ttu-id="7ba76-211">Solicitud</span><span class="sxs-lookup"><span data-stu-id="7ba76-211">Request</span></span>
<span data-ttu-id="7ba76-212">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="7ba76-212">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations/{deviceConfigurationId}
Content-type: application/json
Content-length: 553

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
  "usernameSource": "userPrincipalName",
  "syncCalendar": true,
  "syncContacts": true,
  "syncTasks": true
}
```

### <a name="response"></a><span data-ttu-id="7ba76-213">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7ba76-213">Response</span></span>
<span data-ttu-id="7ba76-p120">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="7ba76-p120">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 742

{
  "@odata.type": "#microsoft.graph.androidWorkProfileNineWorkEasConfiguration",
  "id": "3d9e3a30-3a30-3d9e-303a-9e3d303a9e3d",
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
  "usernameSource": "userPrincipalName",
  "syncCalendar": true,
  "syncContacts": true,
  "syncTasks": true
}
```





