---
title: Crear androidEasEmailProfileConfiguration
description: Crear un nuevo objeto androidEasEmailProfileConfiguration.
author: tfitzmac
ms.openlocfilehash: 38e4e36917ac1679420261746713205f77693b73
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27361974"
---
# <a name="create-androideasemailprofileconfiguration"></a><span data-ttu-id="5c861-103">Crear androidEasEmailProfileConfiguration</span><span class="sxs-lookup"><span data-stu-id="5c861-103">Create androidEasEmailProfileConfiguration</span></span>

> <span data-ttu-id="5c861-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="5c861-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="5c861-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="5c861-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="5c861-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="5c861-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="5c861-107">Crear un nuevo objeto [androidEasEmailProfileConfiguration](../resources/intune-deviceconfig-androideasemailprofileconfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="5c861-107">Create a new [androidEasEmailProfileConfiguration](../resources/intune-deviceconfig-androideasemailprofileconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="5c861-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="5c861-108">Prerequisites</span></span>
<span data-ttu-id="5c861-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="5c861-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="5c861-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="5c861-111">Permission type</span></span>|<span data-ttu-id="5c861-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="5c861-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="5c861-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="5c861-113">Delegated (work or school account)</span></span>|<span data-ttu-id="5c861-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="5c861-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="5c861-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="5c861-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="5c861-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5c861-116">Not supported.</span></span>|
|<span data-ttu-id="5c861-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="5c861-117">Application</span></span>|<span data-ttu-id="5c861-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5c861-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="5c861-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="5c861-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceConfigurations
POST /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsDomainJoinConfiguration/networkAccessConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="5c861-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="5c861-120">Request headers</span></span>
|<span data-ttu-id="5c861-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5c861-121">Header</span></span>|<span data-ttu-id="5c861-122">Valor</span><span class="sxs-lookup"><span data-stu-id="5c861-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="5c861-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="5c861-123">Authorization</span></span>|<span data-ttu-id="5c861-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="5c861-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="5c861-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="5c861-125">Accept</span></span>|<span data-ttu-id="5c861-126">application/json</span><span class="sxs-lookup"><span data-stu-id="5c861-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="5c861-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="5c861-127">Request body</span></span>
<span data-ttu-id="5c861-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto androidEasEmailProfileConfiguration.</span><span class="sxs-lookup"><span data-stu-id="5c861-128">In the request body, supply a JSON representation for the androidEasEmailProfileConfiguration object.</span></span>

<span data-ttu-id="5c861-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el androidEasEmailProfileConfiguration.</span><span class="sxs-lookup"><span data-stu-id="5c861-129">The following table shows the properties that are required when you create the androidEasEmailProfileConfiguration.</span></span>

|<span data-ttu-id="5c861-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="5c861-130">Property</span></span>|<span data-ttu-id="5c861-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="5c861-131">Type</span></span>|<span data-ttu-id="5c861-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="5c861-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="5c861-133">id</span><span class="sxs-lookup"><span data-stu-id="5c861-133">id</span></span>|<span data-ttu-id="5c861-134">String</span><span class="sxs-lookup"><span data-stu-id="5c861-134">String</span></span>|<span data-ttu-id="5c861-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="5c861-135">Key of the entity.</span></span> <span data-ttu-id="5c861-136">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="5c861-136">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="5c861-137">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="5c861-137">lastModifiedDateTime</span></span>|<span data-ttu-id="5c861-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="5c861-138">DateTimeOffset</span></span>|<span data-ttu-id="5c861-139">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="5c861-139">DateTime the object was last modified.</span></span> <span data-ttu-id="5c861-140">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="5c861-140">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="5c861-141">roleScopeTagIds</span><span class="sxs-lookup"><span data-stu-id="5c861-141">roleScopeTagIds</span></span>|<span data-ttu-id="5c861-142">Colección String</span><span class="sxs-lookup"><span data-stu-id="5c861-142">String collection</span></span>|<span data-ttu-id="5c861-143">Lista de etiquetas de ámbito para esta instancia de entidad.</span><span class="sxs-lookup"><span data-stu-id="5c861-143">List of Scope Tags for this Entity instance.</span></span> <span data-ttu-id="5c861-144">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="5c861-144">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="5c861-145">supportsScopeTags</span><span class="sxs-lookup"><span data-stu-id="5c861-145">supportsScopeTags</span></span>|<span data-ttu-id="5c861-146">Boolean</span><span class="sxs-lookup"><span data-stu-id="5c861-146">Boolean</span></span>|<span data-ttu-id="5c861-147">Indica si la configuración del dispositivo subyacente admite la asignación de etiquetas de ámbito.</span><span class="sxs-lookup"><span data-stu-id="5c861-147">Indicates whether or not the underlying Device Configuration supports the assignment of scope tags.</span></span> <span data-ttu-id="5c861-148">No se permite la asignación a la propiedad ScopeTags cuando este valor es false y entidades no estará visibles para los usuarios con ámbito.</span><span class="sxs-lookup"><span data-stu-id="5c861-148">Assigning to the ScopeTags property is not allowed when this value is false and entities will not be visible to scoped users.</span></span> <span data-ttu-id="5c861-149">Esto se produce para las directivas de heredado creadas en Silverlight y se puede resolver por eliminar y volver a crear la directiva en el Portal de Azure.</span><span class="sxs-lookup"><span data-stu-id="5c861-149">This occurs for Legacy policies created in Silverlight and can be resolved by deleting and recreating the policy in the Azure Portal.</span></span> <span data-ttu-id="5c861-150">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="5c861-150">This property is read-only.</span></span> <span data-ttu-id="5c861-151">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="5c861-151">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="5c861-152">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="5c861-152">createdDateTime</span></span>|<span data-ttu-id="5c861-153">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="5c861-153">DateTimeOffset</span></span>|<span data-ttu-id="5c861-154">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="5c861-154">DateTime the object was created.</span></span> <span data-ttu-id="5c861-155">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="5c861-155">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="5c861-156">descripción</span><span class="sxs-lookup"><span data-stu-id="5c861-156">description</span></span>|<span data-ttu-id="5c861-157">String</span><span class="sxs-lookup"><span data-stu-id="5c861-157">String</span></span>|<span data-ttu-id="5c861-158">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5c861-158">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="5c861-159">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="5c861-159">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="5c861-160">displayName</span><span class="sxs-lookup"><span data-stu-id="5c861-160">displayName</span></span>|<span data-ttu-id="5c861-161">String</span><span class="sxs-lookup"><span data-stu-id="5c861-161">String</span></span>|<span data-ttu-id="5c861-162">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5c861-162">Admin provided name of the device configuration.</span></span> <span data-ttu-id="5c861-163">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="5c861-163">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="5c861-164">version</span><span class="sxs-lookup"><span data-stu-id="5c861-164">version</span></span>|<span data-ttu-id="5c861-165">Int32</span><span class="sxs-lookup"><span data-stu-id="5c861-165">Int32</span></span>|<span data-ttu-id="5c861-166">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5c861-166">Version of the device configuration.</span></span> <span data-ttu-id="5c861-167">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="5c861-167">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="5c861-168">accountName</span><span class="sxs-lookup"><span data-stu-id="5c861-168">accountName</span></span>|<span data-ttu-id="5c861-169">String</span><span class="sxs-lookup"><span data-stu-id="5c861-169">String</span></span>|<span data-ttu-id="5c861-170">Nombre de cuenta de Exchange ActiveSync, que se muestra a los usuarios como nombre del perfil EAS (this).</span><span class="sxs-lookup"><span data-stu-id="5c861-170">Exchange ActiveSync account name, displayed to users as name of EAS (this) profile.</span></span>|
|<span data-ttu-id="5c861-171">authenticationMethod</span><span class="sxs-lookup"><span data-stu-id="5c861-171">authenticationMethod</span></span>|[<span data-ttu-id="5c861-172">easAuthenticationMethod</span><span class="sxs-lookup"><span data-stu-id="5c861-172">easAuthenticationMethod</span></span>](../resources/intune-deviceconfig-easauthenticationmethod.md)|<span data-ttu-id="5c861-173">Método de autenticación para Exchange ActiveSync.</span><span class="sxs-lookup"><span data-stu-id="5c861-173">Authentication method for Exchange ActiveSync.</span></span> <span data-ttu-id="5c861-174">Los valores posibles son: `usernameAndPassword` y `certificate`.</span><span class="sxs-lookup"><span data-stu-id="5c861-174">Possible values are: `usernameAndPassword`, `certificate`.</span></span>|
|<span data-ttu-id="5c861-175">syncCalendar</span><span class="sxs-lookup"><span data-stu-id="5c861-175">syncCalendar</span></span>|<span data-ttu-id="5c861-176">Boolean</span><span class="sxs-lookup"><span data-stu-id="5c861-176">Boolean</span></span>|<span data-ttu-id="5c861-177">Activa o desactiva la sincronización del calendario.</span><span class="sxs-lookup"><span data-stu-id="5c861-177">Toggles syncing the calendar.</span></span> <span data-ttu-id="5c861-178">Si se establece en false calendario está desactivado en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5c861-178">If set to false calendar is turned off on the device.</span></span>|
|<span data-ttu-id="5c861-179">syncContacts</span><span class="sxs-lookup"><span data-stu-id="5c861-179">syncContacts</span></span>|<span data-ttu-id="5c861-180">Boolean</span><span class="sxs-lookup"><span data-stu-id="5c861-180">Boolean</span></span>|<span data-ttu-id="5c861-181">Activa o desactiva la sincronización de contactos.</span><span class="sxs-lookup"><span data-stu-id="5c861-181">Toggles syncing contacts.</span></span> <span data-ttu-id="5c861-182">Si establece en false contactos está desactivado en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5c861-182">If set to false contacts are turned off on the device.</span></span>|
|<span data-ttu-id="5c861-183">syncTasks</span><span class="sxs-lookup"><span data-stu-id="5c861-183">syncTasks</span></span>|<span data-ttu-id="5c861-184">Boolean</span><span class="sxs-lookup"><span data-stu-id="5c861-184">Boolean</span></span>|<span data-ttu-id="5c861-185">Activa o desactiva la sincronización de tareas.</span><span class="sxs-lookup"><span data-stu-id="5c861-185">Toggles syncing tasks.</span></span> <span data-ttu-id="5c861-186">Si establece en false tareas está desactivado en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5c861-186">If set to false tasks are turned off on the device.</span></span>|
|<span data-ttu-id="5c861-187">syncNotes</span><span class="sxs-lookup"><span data-stu-id="5c861-187">syncNotes</span></span>|<span data-ttu-id="5c861-188">Boolean</span><span class="sxs-lookup"><span data-stu-id="5c861-188">Boolean</span></span>|<span data-ttu-id="5c861-189">Activa o desactiva la sincronización de notas.</span><span class="sxs-lookup"><span data-stu-id="5c861-189">Toggles syncing notes.</span></span> <span data-ttu-id="5c861-190">Si establece en false notas está desactivado en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5c861-190">If set to false notes are turned off on the device.</span></span>|
|<span data-ttu-id="5c861-191">durationOfEmailToSync</span><span class="sxs-lookup"><span data-stu-id="5c861-191">durationOfEmailToSync</span></span>|[<span data-ttu-id="5c861-192">emailSyncDuration</span><span class="sxs-lookup"><span data-stu-id="5c861-192">emailSyncDuration</span></span>](../resources/intune-deviceconfig-emailsyncduration.md)|<span data-ttu-id="5c861-193">Duración de correo electrónico de tiempo se debe sincronizar en.</span><span class="sxs-lookup"><span data-stu-id="5c861-193">Duration of time email should be synced to.</span></span> <span data-ttu-id="5c861-194">Los valores posibles son: `userDefined`, `oneDay`, `threeDays`, `oneWeek`, `twoWeeks`, `oneMonth` y `unlimited`.</span><span class="sxs-lookup"><span data-stu-id="5c861-194">Possible values are: `userDefined`, `oneDay`, `threeDays`, `oneWeek`, `twoWeeks`, `oneMonth`, `unlimited`.</span></span>|
|<span data-ttu-id="5c861-195">emailAddressSource</span><span class="sxs-lookup"><span data-stu-id="5c861-195">emailAddressSource</span></span>|[<span data-ttu-id="5c861-196">userEmailSource</span><span class="sxs-lookup"><span data-stu-id="5c861-196">userEmailSource</span></span>](../resources/intune-deviceconfig-useremailsource.md)|<span data-ttu-id="5c861-197">Atributo de correo electrónico que se seleccionan de AAD y se insertan en este perfil antes de instalar en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5c861-197">Email attribute that is picked from AAD and injected into this profile before installing on the device.</span></span> <span data-ttu-id="5c861-198">Los valores posibles son: `userPrincipalName` y `primarySmtpAddress`.</span><span class="sxs-lookup"><span data-stu-id="5c861-198">Possible values are: `userPrincipalName`, `primarySmtpAddress`.</span></span>|
|<span data-ttu-id="5c861-199">emailSyncSchedule</span><span class="sxs-lookup"><span data-stu-id="5c861-199">emailSyncSchedule</span></span>|[<span data-ttu-id="5c861-200">emailSyncSchedule</span><span class="sxs-lookup"><span data-stu-id="5c861-200">emailSyncSchedule</span></span>](../resources/intune-deviceconfig-emailsyncschedule.md)|<span data-ttu-id="5c861-201">Programación de sincronización de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="5c861-201">Email sync schedule.</span></span> <span data-ttu-id="5c861-202">Los valores posibles son: `userDefined`, `asMessagesArrive`, `manual`, `fifteenMinutes`, `thirtyMinutes`, `sixtyMinutes` y `basedOnMyUsage`.</span><span class="sxs-lookup"><span data-stu-id="5c861-202">Possible values are: `userDefined`, `asMessagesArrive`, `manual`, `fifteenMinutes`, `thirtyMinutes`, `sixtyMinutes`, `basedOnMyUsage`.</span></span>|
|<span data-ttu-id="5c861-203">hostName</span><span class="sxs-lookup"><span data-stu-id="5c861-203">hostName</span></span>|<span data-ttu-id="5c861-204">String</span><span class="sxs-lookup"><span data-stu-id="5c861-204">String</span></span>|<span data-ttu-id="5c861-205">Ubicación de Exchange (URL) que la aplicación de correo nativo se conecta a.</span><span class="sxs-lookup"><span data-stu-id="5c861-205">Exchange location (URL) that the native mail app connects to.</span></span>|
|<span data-ttu-id="5c861-206">requireSmime</span><span class="sxs-lookup"><span data-stu-id="5c861-206">requireSmime</span></span>|<span data-ttu-id="5c861-207">Boolean</span><span class="sxs-lookup"><span data-stu-id="5c861-207">Boolean</span></span>|<span data-ttu-id="5c861-208">Indica si se va a usar certificados S/MIME o no.</span><span class="sxs-lookup"><span data-stu-id="5c861-208">Indicates whether or not to use S/MIME certificate.</span></span>|
|<span data-ttu-id="5c861-209">requireSsl</span><span class="sxs-lookup"><span data-stu-id="5c861-209">requireSsl</span></span>|<span data-ttu-id="5c861-210">Boolean</span><span class="sxs-lookup"><span data-stu-id="5c861-210">Boolean</span></span>|<span data-ttu-id="5c861-211">Indica si se va a usar SSL o no.</span><span class="sxs-lookup"><span data-stu-id="5c861-211">Indicates whether or not to use SSL.</span></span>|
|<span data-ttu-id="5c861-212">usernameSource</span><span class="sxs-lookup"><span data-stu-id="5c861-212">usernameSource</span></span>|[<span data-ttu-id="5c861-213">androidUsernameSource</span><span class="sxs-lookup"><span data-stu-id="5c861-213">androidUsernameSource</span></span>](../resources/intune-deviceconfig-androidusernamesource.md)|<span data-ttu-id="5c861-214">Atributo de nombre de usuario que se seleccionan de AAD y se insertan en este perfil antes de instalar en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5c861-214">Username attribute that is picked from AAD and injected into this profile before installing on the device.</span></span> <span data-ttu-id="5c861-215">Los valores posibles son: `username`, `userPrincipalName`, `samAccountName` y `primarySmtpAddress`.</span><span class="sxs-lookup"><span data-stu-id="5c861-215">Possible values are: `username`, `userPrincipalName`, `samAccountName`, `primarySmtpAddress`.</span></span>|
|<span data-ttu-id="5c861-216">userDomainNameSource</span><span class="sxs-lookup"><span data-stu-id="5c861-216">userDomainNameSource</span></span>|[<span data-ttu-id="5c861-217">domainNameSource</span><span class="sxs-lookup"><span data-stu-id="5c861-217">domainNameSource</span></span>](../resources/intune-deviceconfig-domainnamesource.md)|<span data-ttu-id="5c861-218">Atributo UserDomainname que se seleccionan de AAD y se insertan en este perfil antes de instalar en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5c861-218">UserDomainname attribute that is picked from AAD and injected into this profile before installing on the device.</span></span> <span data-ttu-id="5c861-219">Los valores posibles son: `fullDomainName` y `netBiosDomainName`.</span><span class="sxs-lookup"><span data-stu-id="5c861-219">Possible values are: `fullDomainName`, `netBiosDomainName`.</span></span>|
|<span data-ttu-id="5c861-220">customDomainName</span><span class="sxs-lookup"><span data-stu-id="5c861-220">customDomainName</span></span>|<span data-ttu-id="5c861-221">String</span><span class="sxs-lookup"><span data-stu-id="5c861-221">String</span></span>|<span data-ttu-id="5c861-222">Valor de nombre de dominio personalizado utilizado durante la generación de un perfil de correo electrónico antes de instalar en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5c861-222">Custom domain name value used while generating an email profile before installing on the device.</span></span>|



## <a name="response"></a><span data-ttu-id="5c861-223">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5c861-223">Response</span></span>
<span data-ttu-id="5c861-224">Si tiene éxito, este método devuelve una `201 Created` código de respuesta y un objeto [androidEasEmailProfileConfiguration](../resources/intune-deviceconfig-androideasemailprofileconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5c861-224">If successful, this method returns a `201 Created` response code and a [androidEasEmailProfileConfiguration](../resources/intune-deviceconfig-androideasemailprofileconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="5c861-225">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="5c861-225">Example</span></span>
### <a name="request"></a><span data-ttu-id="5c861-226">Solicitud</span><span class="sxs-lookup"><span data-stu-id="5c861-226">Request</span></span>
<span data-ttu-id="5c861-227">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="5c861-227">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations
Content-type: application/json
Content-length: 857

{
  "@odata.type": "#microsoft.graph.androidEasEmailProfileConfiguration",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "roleScopeTagIds": [
    "Role Scope Tag Ids value"
  ],
  "supportsScopeTags": true,
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "accountName": "Account Name value",
  "authenticationMethod": "certificate",
  "syncCalendar": true,
  "syncContacts": true,
  "syncTasks": true,
  "syncNotes": true,
  "durationOfEmailToSync": "oneDay",
  "emailAddressSource": "primarySmtpAddress",
  "emailSyncSchedule": "asMessagesArrive",
  "hostName": "Host Name value",
  "requireSmime": true,
  "requireSsl": true,
  "usernameSource": "userPrincipalName",
  "userDomainNameSource": "netBiosDomainName",
  "customDomainName": "Custom Domain Name value"
}
```

### <a name="response"></a><span data-ttu-id="5c861-228">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5c861-228">Response</span></span>
<span data-ttu-id="5c861-p121">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="5c861-p121">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 965

{
  "@odata.type": "#microsoft.graph.androidEasEmailProfileConfiguration",
  "id": "ee5e5610-5610-ee5e-1056-5eee10565eee",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "roleScopeTagIds": [
    "Role Scope Tag Ids value"
  ],
  "supportsScopeTags": true,
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "accountName": "Account Name value",
  "authenticationMethod": "certificate",
  "syncCalendar": true,
  "syncContacts": true,
  "syncTasks": true,
  "syncNotes": true,
  "durationOfEmailToSync": "oneDay",
  "emailAddressSource": "primarySmtpAddress",
  "emailSyncSchedule": "asMessagesArrive",
  "hostName": "Host Name value",
  "requireSmime": true,
  "requireSsl": true,
  "usernameSource": "userPrincipalName",
  "userDomainNameSource": "netBiosDomainName",
  "customDomainName": "Custom Domain Name value"
}
```





