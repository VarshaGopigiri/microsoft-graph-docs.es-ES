---
title: Actualizar androidWorkProfileNineWorkEasConfiguration
description: Actualizar las propiedades de un objeto androidWorkProfileNineWorkEasConfiguration.
author: tfitzmac
ms.openlocfilehash: e0ecb99966c9966afce379d4c4546bc303f24e42
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27345293"
---
# <a name="update-androidworkprofilenineworkeasconfiguration"></a><span data-ttu-id="7a9e1-103">Actualizar androidWorkProfileNineWorkEasConfiguration</span><span class="sxs-lookup"><span data-stu-id="7a9e1-103">Update androidWorkProfileNineWorkEasConfiguration</span></span>

> <span data-ttu-id="7a9e1-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="7a9e1-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="7a9e1-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="7a9e1-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="7a9e1-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="7a9e1-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="7a9e1-107">Actualizar las propiedades de un objeto [androidWorkProfileNineWorkEasConfiguration](../resources/intune-deviceconfig-androidworkprofilenineworkeasconfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="7a9e1-107">Update the properties of a [androidWorkProfileNineWorkEasConfiguration](../resources/intune-deviceconfig-androidworkprofilenineworkeasconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="7a9e1-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="7a9e1-108">Prerequisites</span></span>
<span data-ttu-id="7a9e1-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="7a9e1-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="7a9e1-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="7a9e1-111">Permission type</span></span>|<span data-ttu-id="7a9e1-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="7a9e1-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="7a9e1-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="7a9e1-113">Delegated (work or school account)</span></span>|<span data-ttu-id="7a9e1-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="7a9e1-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="7a9e1-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="7a9e1-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="7a9e1-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="7a9e1-116">Not supported.</span></span>|
|<span data-ttu-id="7a9e1-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="7a9e1-117">Application</span></span>|<span data-ttu-id="7a9e1-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="7a9e1-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="7a9e1-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="7a9e1-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/groupAssignments/{deviceConfigurationGroupAssignmentId}/deviceConfiguration
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsDomainJoinConfiguration/networkAccessConfigurations/{deviceConfigurationId}
```

## <a name="request-headers"></a><span data-ttu-id="7a9e1-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="7a9e1-120">Request headers</span></span>
|<span data-ttu-id="7a9e1-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7a9e1-121">Header</span></span>|<span data-ttu-id="7a9e1-122">Valor</span><span class="sxs-lookup"><span data-stu-id="7a9e1-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="7a9e1-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="7a9e1-123">Authorization</span></span>|<span data-ttu-id="7a9e1-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="7a9e1-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="7a9e1-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="7a9e1-125">Accept</span></span>|<span data-ttu-id="7a9e1-126">application/json</span><span class="sxs-lookup"><span data-stu-id="7a9e1-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="7a9e1-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="7a9e1-127">Request body</span></span>
<span data-ttu-id="7a9e1-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto [androidWorkProfileNineWorkEasConfiguration](../resources/intune-deviceconfig-androidworkprofilenineworkeasconfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="7a9e1-128">In the request body, supply a JSON representation for the [androidWorkProfileNineWorkEasConfiguration](../resources/intune-deviceconfig-androidworkprofilenineworkeasconfiguration.md) object.</span></span>

<span data-ttu-id="7a9e1-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el [androidWorkProfileNineWorkEasConfiguration](../resources/intune-deviceconfig-androidworkprofilenineworkeasconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="7a9e1-129">The following table shows the properties that are required when you create the [androidWorkProfileNineWorkEasConfiguration](../resources/intune-deviceconfig-androidworkprofilenineworkeasconfiguration.md).</span></span>

|<span data-ttu-id="7a9e1-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="7a9e1-130">Property</span></span>|<span data-ttu-id="7a9e1-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="7a9e1-131">Type</span></span>|<span data-ttu-id="7a9e1-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="7a9e1-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="7a9e1-133">id</span><span class="sxs-lookup"><span data-stu-id="7a9e1-133">id</span></span>|<span data-ttu-id="7a9e1-134">String</span><span class="sxs-lookup"><span data-stu-id="7a9e1-134">String</span></span>|<span data-ttu-id="7a9e1-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="7a9e1-135">Key of the entity.</span></span> <span data-ttu-id="7a9e1-136">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="7a9e1-136">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="7a9e1-137">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="7a9e1-137">lastModifiedDateTime</span></span>|<span data-ttu-id="7a9e1-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="7a9e1-138">DateTimeOffset</span></span>|<span data-ttu-id="7a9e1-139">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="7a9e1-139">DateTime the object was last modified.</span></span> <span data-ttu-id="7a9e1-140">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="7a9e1-140">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="7a9e1-141">roleScopeTagIds</span><span class="sxs-lookup"><span data-stu-id="7a9e1-141">roleScopeTagIds</span></span>|<span data-ttu-id="7a9e1-142">Colección String</span><span class="sxs-lookup"><span data-stu-id="7a9e1-142">String collection</span></span>|<span data-ttu-id="7a9e1-143">Lista de etiquetas de ámbito para esta instancia de entidad.</span><span class="sxs-lookup"><span data-stu-id="7a9e1-143">List of Scope Tags for this Entity instance.</span></span> <span data-ttu-id="7a9e1-144">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="7a9e1-144">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="7a9e1-145">supportsScopeTags</span><span class="sxs-lookup"><span data-stu-id="7a9e1-145">supportsScopeTags</span></span>|<span data-ttu-id="7a9e1-146">Boolean</span><span class="sxs-lookup"><span data-stu-id="7a9e1-146">Boolean</span></span>|<span data-ttu-id="7a9e1-147">Indica si la configuración del dispositivo subyacente admite la asignación de etiquetas de ámbito.</span><span class="sxs-lookup"><span data-stu-id="7a9e1-147">Indicates whether or not the underlying Device Configuration supports the assignment of scope tags.</span></span> <span data-ttu-id="7a9e1-148">No se permite la asignación a la propiedad ScopeTags cuando este valor es false y entidades no estará visibles para los usuarios con ámbito.</span><span class="sxs-lookup"><span data-stu-id="7a9e1-148">Assigning to the ScopeTags property is not allowed when this value is false and entities will not be visible to scoped users.</span></span> <span data-ttu-id="7a9e1-149">Esto se produce para las directivas de heredado creadas en Silverlight y se puede resolver por eliminar y volver a crear la directiva en el Portal de Azure.</span><span class="sxs-lookup"><span data-stu-id="7a9e1-149">This occurs for Legacy policies created in Silverlight and can be resolved by deleting and recreating the policy in the Azure Portal.</span></span> <span data-ttu-id="7a9e1-150">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="7a9e1-150">This property is read-only.</span></span> <span data-ttu-id="7a9e1-151">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="7a9e1-151">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="7a9e1-152">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="7a9e1-152">createdDateTime</span></span>|<span data-ttu-id="7a9e1-153">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="7a9e1-153">DateTimeOffset</span></span>|<span data-ttu-id="7a9e1-154">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="7a9e1-154">DateTime the object was created.</span></span> <span data-ttu-id="7a9e1-155">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="7a9e1-155">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="7a9e1-156">descripción</span><span class="sxs-lookup"><span data-stu-id="7a9e1-156">description</span></span>|<span data-ttu-id="7a9e1-157">String</span><span class="sxs-lookup"><span data-stu-id="7a9e1-157">String</span></span>|<span data-ttu-id="7a9e1-158">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7a9e1-158">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="7a9e1-159">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="7a9e1-159">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="7a9e1-160">displayName</span><span class="sxs-lookup"><span data-stu-id="7a9e1-160">displayName</span></span>|<span data-ttu-id="7a9e1-161">String</span><span class="sxs-lookup"><span data-stu-id="7a9e1-161">String</span></span>|<span data-ttu-id="7a9e1-162">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7a9e1-162">Admin provided name of the device configuration.</span></span> <span data-ttu-id="7a9e1-163">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="7a9e1-163">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="7a9e1-164">version</span><span class="sxs-lookup"><span data-stu-id="7a9e1-164">version</span></span>|<span data-ttu-id="7a9e1-165">Int32</span><span class="sxs-lookup"><span data-stu-id="7a9e1-165">Int32</span></span>|<span data-ttu-id="7a9e1-166">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7a9e1-166">Version of the device configuration.</span></span> <span data-ttu-id="7a9e1-167">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="7a9e1-167">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="7a9e1-168">authenticationMethod</span><span class="sxs-lookup"><span data-stu-id="7a9e1-168">authenticationMethod</span></span>|[<span data-ttu-id="7a9e1-169">easAuthenticationMethod</span><span class="sxs-lookup"><span data-stu-id="7a9e1-169">easAuthenticationMethod</span></span>](../resources/intune-deviceconfig-easauthenticationmethod.md)|<span data-ttu-id="7a9e1-170">Método de autenticación para Exchange ActiveSync.</span><span class="sxs-lookup"><span data-stu-id="7a9e1-170">Authentication method for Exchange ActiveSync.</span></span> <span data-ttu-id="7a9e1-171">Se hereda de [androidWorkProfileEasEmailProfileBase](../resources/intune-deviceconfig-androidworkprofileeasemailprofilebase.md).</span><span class="sxs-lookup"><span data-stu-id="7a9e1-171">Inherited from [androidWorkProfileEasEmailProfileBase](../resources/intune-deviceconfig-androidworkprofileeasemailprofilebase.md).</span></span> <span data-ttu-id="7a9e1-172">Los valores posibles son: `usernameAndPassword` y `certificate`.</span><span class="sxs-lookup"><span data-stu-id="7a9e1-172">Possible values are: `usernameAndPassword`, `certificate`.</span></span>|
|<span data-ttu-id="7a9e1-173">durationOfEmailToSync</span><span class="sxs-lookup"><span data-stu-id="7a9e1-173">durationOfEmailToSync</span></span>|[<span data-ttu-id="7a9e1-174">emailSyncDuration</span><span class="sxs-lookup"><span data-stu-id="7a9e1-174">emailSyncDuration</span></span>](../resources/intune-deviceconfig-emailsyncduration.md)|<span data-ttu-id="7a9e1-175">Duración de correo electrónico de tiempo se debe sincronizar en.</span><span class="sxs-lookup"><span data-stu-id="7a9e1-175">Duration of time email should be synced to.</span></span> <span data-ttu-id="7a9e1-176">Se hereda de [androidWorkProfileEasEmailProfileBase](../resources/intune-deviceconfig-androidworkprofileeasemailprofilebase.md).</span><span class="sxs-lookup"><span data-stu-id="7a9e1-176">Inherited from [androidWorkProfileEasEmailProfileBase](../resources/intune-deviceconfig-androidworkprofileeasemailprofilebase.md).</span></span> <span data-ttu-id="7a9e1-177">Los valores posibles son: `userDefined`, `oneDay`, `threeDays`, `oneWeek`, `twoWeeks`, `oneMonth` y `unlimited`.</span><span class="sxs-lookup"><span data-stu-id="7a9e1-177">Possible values are: `userDefined`, `oneDay`, `threeDays`, `oneWeek`, `twoWeeks`, `oneMonth`, `unlimited`.</span></span>|
|<span data-ttu-id="7a9e1-178">emailAddressSource</span><span class="sxs-lookup"><span data-stu-id="7a9e1-178">emailAddressSource</span></span>|[<span data-ttu-id="7a9e1-179">userEmailSource</span><span class="sxs-lookup"><span data-stu-id="7a9e1-179">userEmailSource</span></span>](../resources/intune-deviceconfig-useremailsource.md)|<span data-ttu-id="7a9e1-180">Atributo de correo electrónico que se seleccionan de AAD y se insertan en este perfil antes de instalar en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7a9e1-180">Email attribute that is picked from AAD and injected into this profile before installing on the device.</span></span> <span data-ttu-id="7a9e1-181">Se hereda de [androidWorkProfileEasEmailProfileBase](../resources/intune-deviceconfig-androidworkprofileeasemailprofilebase.md).</span><span class="sxs-lookup"><span data-stu-id="7a9e1-181">Inherited from [androidWorkProfileEasEmailProfileBase](../resources/intune-deviceconfig-androidworkprofileeasemailprofilebase.md).</span></span> <span data-ttu-id="7a9e1-182">Los valores posibles son: `userPrincipalName` y `primarySmtpAddress`.</span><span class="sxs-lookup"><span data-stu-id="7a9e1-182">Possible values are: `userPrincipalName`, `primarySmtpAddress`.</span></span>|
|<span data-ttu-id="7a9e1-183">hostName</span><span class="sxs-lookup"><span data-stu-id="7a9e1-183">hostName</span></span>|<span data-ttu-id="7a9e1-184">String</span><span class="sxs-lookup"><span data-stu-id="7a9e1-184">String</span></span>|<span data-ttu-id="7a9e1-185">Ubicación de Exchange (URL) que la aplicación de correo se conecta a.</span><span class="sxs-lookup"><span data-stu-id="7a9e1-185">Exchange location (URL) that the mail app connects to.</span></span> <span data-ttu-id="7a9e1-186">Se hereda de [androidWorkProfileEasEmailProfileBase](../resources/intune-deviceconfig-androidworkprofileeasemailprofilebase.md)</span><span class="sxs-lookup"><span data-stu-id="7a9e1-186">Inherited from [androidWorkProfileEasEmailProfileBase](../resources/intune-deviceconfig-androidworkprofileeasemailprofilebase.md)</span></span>|
|<span data-ttu-id="7a9e1-187">requireSsl</span><span class="sxs-lookup"><span data-stu-id="7a9e1-187">requireSsl</span></span>|<span data-ttu-id="7a9e1-188">Boolean</span><span class="sxs-lookup"><span data-stu-id="7a9e1-188">Boolean</span></span>|<span data-ttu-id="7a9e1-189">Indica si se va a usar SSL o no.</span><span class="sxs-lookup"><span data-stu-id="7a9e1-189">Indicates whether or not to use SSL.</span></span> <span data-ttu-id="7a9e1-190">Se hereda de [androidWorkProfileEasEmailProfileBase](../resources/intune-deviceconfig-androidworkprofileeasemailprofilebase.md)</span><span class="sxs-lookup"><span data-stu-id="7a9e1-190">Inherited from [androidWorkProfileEasEmailProfileBase](../resources/intune-deviceconfig-androidworkprofileeasemailprofilebase.md)</span></span>|
|<span data-ttu-id="7a9e1-191">usernameSource</span><span class="sxs-lookup"><span data-stu-id="7a9e1-191">usernameSource</span></span>|[<span data-ttu-id="7a9e1-192">androidUsernameSource</span><span class="sxs-lookup"><span data-stu-id="7a9e1-192">androidUsernameSource</span></span>](../resources/intune-deviceconfig-androidusernamesource.md)|<span data-ttu-id="7a9e1-193">Atributo de nombre de usuario que se seleccionan de AAD y se insertan en este perfil antes de instalar en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7a9e1-193">Username attribute that is picked from AAD and injected into this profile before installing on the device.</span></span> <span data-ttu-id="7a9e1-194">Se hereda de [androidWorkProfileEasEmailProfileBase](../resources/intune-deviceconfig-androidworkprofileeasemailprofilebase.md).</span><span class="sxs-lookup"><span data-stu-id="7a9e1-194">Inherited from [androidWorkProfileEasEmailProfileBase](../resources/intune-deviceconfig-androidworkprofileeasemailprofilebase.md).</span></span> <span data-ttu-id="7a9e1-195">Los valores posibles son: `username`, `userPrincipalName`, `samAccountName` y `primarySmtpAddress`.</span><span class="sxs-lookup"><span data-stu-id="7a9e1-195">Possible values are: `username`, `userPrincipalName`, `samAccountName`, `primarySmtpAddress`.</span></span>|
|<span data-ttu-id="7a9e1-196">syncCalendar</span><span class="sxs-lookup"><span data-stu-id="7a9e1-196">syncCalendar</span></span>|<span data-ttu-id="7a9e1-197">Boolean</span><span class="sxs-lookup"><span data-stu-id="7a9e1-197">Boolean</span></span>|<span data-ttu-id="7a9e1-198">Activa o desactiva la sincronización del calendario.</span><span class="sxs-lookup"><span data-stu-id="7a9e1-198">Toggles syncing the calendar.</span></span> <span data-ttu-id="7a9e1-199">Si se establece en false el calendario está desactivado en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7a9e1-199">If set to false the calendar is turned off on the device.</span></span>|
|<span data-ttu-id="7a9e1-200">syncContacts</span><span class="sxs-lookup"><span data-stu-id="7a9e1-200">syncContacts</span></span>|<span data-ttu-id="7a9e1-201">Boolean</span><span class="sxs-lookup"><span data-stu-id="7a9e1-201">Boolean</span></span>|<span data-ttu-id="7a9e1-202">Activa o desactiva la sincronización de contactos.</span><span class="sxs-lookup"><span data-stu-id="7a9e1-202">Toggles syncing contacts.</span></span> <span data-ttu-id="7a9e1-203">Si establece en false contactos está desactivado en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7a9e1-203">If set to false contacts are turned off on the device.</span></span>|
|<span data-ttu-id="7a9e1-204">syncTasks</span><span class="sxs-lookup"><span data-stu-id="7a9e1-204">syncTasks</span></span>|<span data-ttu-id="7a9e1-205">Boolean</span><span class="sxs-lookup"><span data-stu-id="7a9e1-205">Boolean</span></span>|<span data-ttu-id="7a9e1-206">Activa o desactiva la sincronización de tareas.</span><span class="sxs-lookup"><span data-stu-id="7a9e1-206">Toggles syncing tasks.</span></span> <span data-ttu-id="7a9e1-207">Si establece en false tareas está desactivado en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7a9e1-207">If set to false tasks are turned off on the device.</span></span>|



## <a name="response"></a><span data-ttu-id="7a9e1-208">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7a9e1-208">Response</span></span>
<span data-ttu-id="7a9e1-209">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto actualizado [androidWorkProfileNineWorkEasConfiguration](../resources/intune-deviceconfig-androidworkprofilenineworkeasconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7a9e1-209">If successful, this method returns a `200 OK` response code and an updated [androidWorkProfileNineWorkEasConfiguration](../resources/intune-deviceconfig-androidworkprofilenineworkeasconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="7a9e1-210">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7a9e1-210">Example</span></span>
### <a name="request"></a><span data-ttu-id="7a9e1-211">Solicitud</span><span class="sxs-lookup"><span data-stu-id="7a9e1-211">Request</span></span>
<span data-ttu-id="7a9e1-212">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="7a9e1-212">Here is an example of the request.</span></span>
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

### <a name="response"></a><span data-ttu-id="7a9e1-213">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7a9e1-213">Response</span></span>
<span data-ttu-id="7a9e1-p120">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="7a9e1-p120">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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





