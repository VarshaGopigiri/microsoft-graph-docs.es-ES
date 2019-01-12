---
title: Actualizar windowsPhoneEASEmailProfileConfiguration
description: Actualizar las propiedades de un objeto windowsPhoneEASEmailProfileConfiguration.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 97d59700908221d9c2e953fa234e3a68360840e2
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27936294"
---
# <a name="update-windowsphoneeasemailprofileconfiguration"></a><span data-ttu-id="63c12-103">Actualizar windowsPhoneEASEmailProfileConfiguration</span><span class="sxs-lookup"><span data-stu-id="63c12-103">Update windowsPhoneEASEmailProfileConfiguration</span></span>

> <span data-ttu-id="63c12-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="63c12-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="63c12-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="63c12-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="63c12-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="63c12-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="63c12-107">Actualizar las propiedades de un objeto [windowsPhoneEASEmailProfileConfiguration](../resources/intune-deviceconfig-windowsphoneeasemailprofileconfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="63c12-107">Update the properties of a [windowsPhoneEASEmailProfileConfiguration](../resources/intune-deviceconfig-windowsphoneeasemailprofileconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="63c12-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="63c12-108">Prerequisites</span></span>
<span data-ttu-id="63c12-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="63c12-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="63c12-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="63c12-111">Permission type</span></span>|<span data-ttu-id="63c12-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="63c12-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="63c12-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="63c12-113">Delegated (work or school account)</span></span>|<span data-ttu-id="63c12-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="63c12-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="63c12-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="63c12-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="63c12-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="63c12-116">Not supported.</span></span>|
|<span data-ttu-id="63c12-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="63c12-117">Application</span></span>|<span data-ttu-id="63c12-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="63c12-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="63c12-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="63c12-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/groupAssignments/{deviceConfigurationGroupAssignmentId}/deviceConfiguration
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsDomainJoinConfiguration/networkAccessConfigurations/{deviceConfigurationId}
```

## <a name="request-headers"></a><span data-ttu-id="63c12-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="63c12-120">Request headers</span></span>
|<span data-ttu-id="63c12-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="63c12-121">Header</span></span>|<span data-ttu-id="63c12-122">Valor</span><span class="sxs-lookup"><span data-stu-id="63c12-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="63c12-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="63c12-123">Authorization</span></span>|<span data-ttu-id="63c12-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="63c12-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="63c12-125">Accept</span><span class="sxs-lookup"><span data-stu-id="63c12-125">Accept</span></span>|<span data-ttu-id="63c12-126">application/json</span><span class="sxs-lookup"><span data-stu-id="63c12-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="63c12-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="63c12-127">Request body</span></span>
<span data-ttu-id="63c12-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto [windowsPhoneEASEmailProfileConfiguration](../resources/intune-deviceconfig-windowsphoneeasemailprofileconfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="63c12-128">In the request body, supply a JSON representation for the [windowsPhoneEASEmailProfileConfiguration](../resources/intune-deviceconfig-windowsphoneeasemailprofileconfiguration.md) object.</span></span>

<span data-ttu-id="63c12-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el [windowsPhoneEASEmailProfileConfiguration](../resources/intune-deviceconfig-windowsphoneeasemailprofileconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="63c12-129">The following table shows the properties that are required when you create the [windowsPhoneEASEmailProfileConfiguration](../resources/intune-deviceconfig-windowsphoneeasemailprofileconfiguration.md).</span></span>

|<span data-ttu-id="63c12-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="63c12-130">Property</span></span>|<span data-ttu-id="63c12-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="63c12-131">Type</span></span>|<span data-ttu-id="63c12-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="63c12-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="63c12-133">id</span><span class="sxs-lookup"><span data-stu-id="63c12-133">id</span></span>|<span data-ttu-id="63c12-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="63c12-134">String</span></span>|<span data-ttu-id="63c12-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="63c12-135">Key of the entity.</span></span> <span data-ttu-id="63c12-136">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="63c12-136">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="63c12-137">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="63c12-137">lastModifiedDateTime</span></span>|<span data-ttu-id="63c12-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="63c12-138">DateTimeOffset</span></span>|<span data-ttu-id="63c12-139">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="63c12-139">DateTime the object was last modified.</span></span> <span data-ttu-id="63c12-140">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="63c12-140">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="63c12-141">roleScopeTagIds</span><span class="sxs-lookup"><span data-stu-id="63c12-141">roleScopeTagIds</span></span>|<span data-ttu-id="63c12-142">Colección String</span><span class="sxs-lookup"><span data-stu-id="63c12-142">String collection</span></span>|<span data-ttu-id="63c12-143">Lista de etiquetas de ámbito para esta instancia de entidad.</span><span class="sxs-lookup"><span data-stu-id="63c12-143">List of Scope Tags for this Entity instance.</span></span> <span data-ttu-id="63c12-144">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="63c12-144">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="63c12-145">supportsScopeTags</span><span class="sxs-lookup"><span data-stu-id="63c12-145">supportsScopeTags</span></span>|<span data-ttu-id="63c12-146">Booleano</span><span class="sxs-lookup"><span data-stu-id="63c12-146">Boolean</span></span>|<span data-ttu-id="63c12-147">Indica si la configuración del dispositivo subyacente admite la asignación de etiquetas de ámbito.</span><span class="sxs-lookup"><span data-stu-id="63c12-147">Indicates whether or not the underlying Device Configuration supports the assignment of scope tags.</span></span> <span data-ttu-id="63c12-148">No se permite la asignación a la propiedad ScopeTags cuando este valor es false y entidades no estará visibles para los usuarios con ámbito.</span><span class="sxs-lookup"><span data-stu-id="63c12-148">Assigning to the ScopeTags property is not allowed when this value is false and entities will not be visible to scoped users.</span></span> <span data-ttu-id="63c12-149">Esto se produce para las directivas de heredado creadas en Silverlight y se puede resolver por eliminar y volver a crear la directiva en el Portal de Azure.</span><span class="sxs-lookup"><span data-stu-id="63c12-149">This occurs for Legacy policies created in Silverlight and can be resolved by deleting and recreating the policy in the Azure Portal.</span></span> <span data-ttu-id="63c12-150">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="63c12-150">This property is read-only.</span></span> <span data-ttu-id="63c12-151">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="63c12-151">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="63c12-152">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="63c12-152">createdDateTime</span></span>|<span data-ttu-id="63c12-153">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="63c12-153">DateTimeOffset</span></span>|<span data-ttu-id="63c12-154">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="63c12-154">DateTime the object was created.</span></span> <span data-ttu-id="63c12-155">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="63c12-155">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="63c12-156">descripción</span><span class="sxs-lookup"><span data-stu-id="63c12-156">description</span></span>|<span data-ttu-id="63c12-157">Cadena</span><span class="sxs-lookup"><span data-stu-id="63c12-157">String</span></span>|<span data-ttu-id="63c12-158">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="63c12-158">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="63c12-159">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="63c12-159">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="63c12-160">displayName</span><span class="sxs-lookup"><span data-stu-id="63c12-160">displayName</span></span>|<span data-ttu-id="63c12-161">Cadena</span><span class="sxs-lookup"><span data-stu-id="63c12-161">String</span></span>|<span data-ttu-id="63c12-162">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="63c12-162">Admin provided name of the device configuration.</span></span> <span data-ttu-id="63c12-163">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="63c12-163">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="63c12-164">version</span><span class="sxs-lookup"><span data-stu-id="63c12-164">version</span></span>|<span data-ttu-id="63c12-165">Int32</span><span class="sxs-lookup"><span data-stu-id="63c12-165">Int32</span></span>|<span data-ttu-id="63c12-166">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="63c12-166">Version of the device configuration.</span></span> <span data-ttu-id="63c12-167">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="63c12-167">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="63c12-168">usernameSource</span><span class="sxs-lookup"><span data-stu-id="63c12-168">usernameSource</span></span>|[<span data-ttu-id="63c12-169">userEmailSource</span><span class="sxs-lookup"><span data-stu-id="63c12-169">userEmailSource</span></span>](../resources/intune-deviceconfig-useremailsource.md)|<span data-ttu-id="63c12-170">Atributo de nombre de usuario que se seleccionan de AAD y se insertan en este perfil antes de instalar en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="63c12-170">Username attribute that is picked from AAD and injected into this profile before installing on the device.</span></span> <span data-ttu-id="63c12-171">Se hereda de [easEmailProfileConfigurationBase](../resources/intune-deviceconfig-easemailprofileconfigurationbase.md).</span><span class="sxs-lookup"><span data-stu-id="63c12-171">Inherited from [easEmailProfileConfigurationBase](../resources/intune-deviceconfig-easemailprofileconfigurationbase.md).</span></span> <span data-ttu-id="63c12-172">Los valores posibles son: `userPrincipalName` y `primarySmtpAddress`.</span><span class="sxs-lookup"><span data-stu-id="63c12-172">Possible values are: `userPrincipalName`, `primarySmtpAddress`.</span></span>|
|<span data-ttu-id="63c12-173">usernameAADSource</span><span class="sxs-lookup"><span data-stu-id="63c12-173">usernameAADSource</span></span>|[<span data-ttu-id="63c12-174">usernameSource</span><span class="sxs-lookup"><span data-stu-id="63c12-174">usernameSource</span></span>](../resources/intune-deviceconfig-usernamesource.md)|<span data-ttu-id="63c12-175">Nombre del campo AAD, que se usará para recuperar el nombre de usuario para el perfil de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="63c12-175">Name of the AAD field, that will be used to retrieve UserName for email profile.</span></span> <span data-ttu-id="63c12-176">Se hereda de [easEmailProfileConfigurationBase](../resources/intune-deviceconfig-easemailprofileconfigurationbase.md).</span><span class="sxs-lookup"><span data-stu-id="63c12-176">Inherited from [easEmailProfileConfigurationBase](../resources/intune-deviceconfig-easemailprofileconfigurationbase.md).</span></span> <span data-ttu-id="63c12-177">Los valores posibles son: `userPrincipalName`, `primarySmtpAddress` y `samAccountName`.</span><span class="sxs-lookup"><span data-stu-id="63c12-177">Possible values are: `userPrincipalName`, `primarySmtpAddress`, `samAccountName`.</span></span>|
|<span data-ttu-id="63c12-178">userDomainNameSource</span><span class="sxs-lookup"><span data-stu-id="63c12-178">userDomainNameSource</span></span>|[<span data-ttu-id="63c12-179">domainNameSource</span><span class="sxs-lookup"><span data-stu-id="63c12-179">domainNameSource</span></span>](../resources/intune-deviceconfig-domainnamesource.md)|<span data-ttu-id="63c12-180">Atributo UserDomainname que se seleccionan de AAD y se insertan en este perfil antes de instalar en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="63c12-180">UserDomainname attribute that is picked from AAD and injected into this profile before installing on the device.</span></span> <span data-ttu-id="63c12-181">Se hereda de [easEmailProfileConfigurationBase](../resources/intune-deviceconfig-easemailprofileconfigurationbase.md).</span><span class="sxs-lookup"><span data-stu-id="63c12-181">Inherited from [easEmailProfileConfigurationBase](../resources/intune-deviceconfig-easemailprofileconfigurationbase.md).</span></span> <span data-ttu-id="63c12-182">Los valores posibles son: `fullDomainName` y `netBiosDomainName`.</span><span class="sxs-lookup"><span data-stu-id="63c12-182">Possible values are: `fullDomainName`, `netBiosDomainName`.</span></span>|
|<span data-ttu-id="63c12-183">customDomainName</span><span class="sxs-lookup"><span data-stu-id="63c12-183">customDomainName</span></span>|<span data-ttu-id="63c12-184">Cadena</span><span class="sxs-lookup"><span data-stu-id="63c12-184">String</span></span>|<span data-ttu-id="63c12-185">Valor de nombre de dominio personalizado utilizado durante la generación de un perfil de correo electrónico antes de instalar en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="63c12-185">Custom domain name value used while generating an email profile before installing on the device.</span></span> <span data-ttu-id="63c12-186">Se hereda de [easEmailProfileConfigurationBase](../resources/intune-deviceconfig-easemailprofileconfigurationbase.md)</span><span class="sxs-lookup"><span data-stu-id="63c12-186">Inherited from [easEmailProfileConfigurationBase](../resources/intune-deviceconfig-easemailprofileconfigurationbase.md)</span></span>|
|<span data-ttu-id="63c12-187">accountName</span><span class="sxs-lookup"><span data-stu-id="63c12-187">accountName</span></span>|<span data-ttu-id="63c12-188">Cadena</span><span class="sxs-lookup"><span data-stu-id="63c12-188">String</span></span>|<span data-ttu-id="63c12-189">Nombre de la cuenta.</span><span class="sxs-lookup"><span data-stu-id="63c12-189">Account name.</span></span>|
|<span data-ttu-id="63c12-190">applyOnlyToWindowsPhone81</span><span class="sxs-lookup"><span data-stu-id="63c12-190">applyOnlyToWindowsPhone81</span></span>|<span data-ttu-id="63c12-191">Booleano</span><span class="sxs-lookup"><span data-stu-id="63c12-191">Boolean</span></span>|<span data-ttu-id="63c12-192">Valor que indica si esta directiva se aplica solo a Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="63c12-192">Value indicating whether this policy only applies to Windows 8.1.</span></span> <span data-ttu-id="63c12-193">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="63c12-193">This property is read-only.</span></span>|
|<span data-ttu-id="63c12-194">syncCalendar</span><span class="sxs-lookup"><span data-stu-id="63c12-194">syncCalendar</span></span>|<span data-ttu-id="63c12-195">Booleano</span><span class="sxs-lookup"><span data-stu-id="63c12-195">Boolean</span></span>|<span data-ttu-id="63c12-196">Si desea o no sincronizar el calendario.</span><span class="sxs-lookup"><span data-stu-id="63c12-196">Whether or not to sync the calendar.</span></span>|
|<span data-ttu-id="63c12-197">syncContacts</span><span class="sxs-lookup"><span data-stu-id="63c12-197">syncContacts</span></span>|<span data-ttu-id="63c12-198">Booleano</span><span class="sxs-lookup"><span data-stu-id="63c12-198">Boolean</span></span>|<span data-ttu-id="63c12-199">Si desea o no sincronizar contactos.</span><span class="sxs-lookup"><span data-stu-id="63c12-199">Whether or not to sync contacts.</span></span>|
|<span data-ttu-id="63c12-200">syncTasks</span><span class="sxs-lookup"><span data-stu-id="63c12-200">syncTasks</span></span>|<span data-ttu-id="63c12-201">Booleano</span><span class="sxs-lookup"><span data-stu-id="63c12-201">Boolean</span></span>|<span data-ttu-id="63c12-202">Si desea sincronizar las tareas.</span><span class="sxs-lookup"><span data-stu-id="63c12-202">Whether or not to sync tasks.</span></span>|
|<span data-ttu-id="63c12-203">durationOfEmailToSync</span><span class="sxs-lookup"><span data-stu-id="63c12-203">durationOfEmailToSync</span></span>|[<span data-ttu-id="63c12-204">emailSyncDuration</span><span class="sxs-lookup"><span data-stu-id="63c12-204">emailSyncDuration</span></span>](../resources/intune-deviceconfig-emailsyncduration.md)|<span data-ttu-id="63c12-205">Duración de correo electrónico para la sincronización. Los valores posibles son: `userDefined`, `oneDay`, `threeDays`, `oneWeek`, `twoWeeks`, `oneMonth`, `unlimited`.</span><span class="sxs-lookup"><span data-stu-id="63c12-205">Duration of email to sync. Possible values are: `userDefined`, `oneDay`, `threeDays`, `oneWeek`, `twoWeeks`, `oneMonth`, `unlimited`.</span></span>|
|<span data-ttu-id="63c12-206">emailAddressSource</span><span class="sxs-lookup"><span data-stu-id="63c12-206">emailAddressSource</span></span>|[<span data-ttu-id="63c12-207">userEmailSource</span><span class="sxs-lookup"><span data-stu-id="63c12-207">userEmailSource</span></span>](../resources/intune-deviceconfig-useremailsource.md)|<span data-ttu-id="63c12-208">Atributo de correo electrónico que se seleccionan de AAD y se insertan en este perfil antes de instalar en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="63c12-208">Email attribute that is picked from AAD and injected into this profile before installing on the device.</span></span> <span data-ttu-id="63c12-209">Los valores posibles son: `userPrincipalName` y `primarySmtpAddress`.</span><span class="sxs-lookup"><span data-stu-id="63c12-209">Possible values are: `userPrincipalName`, `primarySmtpAddress`.</span></span>|
|<span data-ttu-id="63c12-210">emailSyncSchedule</span><span class="sxs-lookup"><span data-stu-id="63c12-210">emailSyncSchedule</span></span>|[<span data-ttu-id="63c12-211">emailSyncSchedule</span><span class="sxs-lookup"><span data-stu-id="63c12-211">emailSyncSchedule</span></span>](../resources/intune-deviceconfig-emailsyncschedule.md)|<span data-ttu-id="63c12-212">Programación de sincronización de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="63c12-212">Email sync schedule.</span></span> <span data-ttu-id="63c12-213">Los valores posibles son: `userDefined`, `asMessagesArrive`, `manual`, `fifteenMinutes`, `thirtyMinutes`, `sixtyMinutes` y `basedOnMyUsage`.</span><span class="sxs-lookup"><span data-stu-id="63c12-213">Possible values are: `userDefined`, `asMessagesArrive`, `manual`, `fifteenMinutes`, `thirtyMinutes`, `sixtyMinutes`, `basedOnMyUsage`.</span></span>|
|<span data-ttu-id="63c12-214">hostName</span><span class="sxs-lookup"><span data-stu-id="63c12-214">hostName</span></span>|<span data-ttu-id="63c12-215">String</span><span class="sxs-lookup"><span data-stu-id="63c12-215">String</span></span>|<span data-ttu-id="63c12-216">Ubicación de Exchange esa dirección (URL) que la aplicación de correo nativo se conecta a.</span><span class="sxs-lookup"><span data-stu-id="63c12-216">Exchange location that (URL) that the native mail app connects to.</span></span>|
|<span data-ttu-id="63c12-217">requireSsl</span><span class="sxs-lookup"><span data-stu-id="63c12-217">requireSsl</span></span>|<span data-ttu-id="63c12-218">Booleano</span><span class="sxs-lookup"><span data-stu-id="63c12-218">Boolean</span></span>|<span data-ttu-id="63c12-219">Indica si se va a usar SSL o no.</span><span class="sxs-lookup"><span data-stu-id="63c12-219">Indicates whether or not to use SSL.</span></span>|



## <a name="response"></a><span data-ttu-id="63c12-220">Respuesta</span><span class="sxs-lookup"><span data-stu-id="63c12-220">Response</span></span>
<span data-ttu-id="63c12-221">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto actualizado [windowsPhoneEASEmailProfileConfiguration](../resources/intune-deviceconfig-windowsphoneeasemailprofileconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="63c12-221">If successful, this method returns a `200 OK` response code and an updated [windowsPhoneEASEmailProfileConfiguration](../resources/intune-deviceconfig-windowsphoneeasemailprofileconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="63c12-222">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="63c12-222">Example</span></span>
### <a name="request"></a><span data-ttu-id="63c12-223">Solicitud</span><span class="sxs-lookup"><span data-stu-id="63c12-223">Request</span></span>
<span data-ttu-id="63c12-224">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="63c12-224">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations/{deviceConfigurationId}
Content-type: application/json
Content-length: 779

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
  "applyOnlyToWindowsPhone81": true,
  "syncCalendar": true,
  "syncContacts": true,
  "syncTasks": true,
  "durationOfEmailToSync": "oneDay",
  "emailAddressSource": "primarySmtpAddress",
  "emailSyncSchedule": "asMessagesArrive",
  "hostName": "Host Name value",
  "requireSsl": true
}
```

### <a name="response"></a><span data-ttu-id="63c12-225">Respuesta</span><span class="sxs-lookup"><span data-stu-id="63c12-225">Response</span></span>
<span data-ttu-id="63c12-p118">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="63c12-p118">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 966

{
  "@odata.type": "#microsoft.graph.windowsPhoneEASEmailProfileConfiguration",
  "id": "554f402a-402a-554f-2a40-4f552a404f55",
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
  "applyOnlyToWindowsPhone81": true,
  "syncCalendar": true,
  "syncContacts": true,
  "syncTasks": true,
  "durationOfEmailToSync": "oneDay",
  "emailAddressSource": "primarySmtpAddress",
  "emailSyncSchedule": "asMessagesArrive",
  "hostName": "Host Name value",
  "requireSsl": true
}
```





