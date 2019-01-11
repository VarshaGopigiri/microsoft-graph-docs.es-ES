---
title: Actualizar windows81GeneralConfiguration
description: Actualice las propiedades de un objeto windows81GeneralConfiguration.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 13aeeab7afe6c7554815dcdb1a6b0d662bc5c0bf
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27828409"
---
# <a name="update-windows81generalconfiguration"></a><span data-ttu-id="5385b-103">Actualizar windows81GeneralConfiguration</span><span class="sxs-lookup"><span data-stu-id="5385b-103">Update windows81GeneralConfiguration</span></span>

> <span data-ttu-id="5385b-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="5385b-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="5385b-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="5385b-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="5385b-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="5385b-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="5385b-107">Actualice las propiedades de un objeto [windows81GeneralConfiguration](../resources/intune-deviceconfig-windows81generalconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="5385b-107">Update the properties of a [windows81GeneralConfiguration](../resources/intune-deviceconfig-windows81generalconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="5385b-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="5385b-108">Prerequisites</span></span>
<span data-ttu-id="5385b-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="5385b-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="5385b-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="5385b-111">Permission type</span></span>|<span data-ttu-id="5385b-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="5385b-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="5385b-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="5385b-113">Delegated (work or school account)</span></span>|<span data-ttu-id="5385b-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="5385b-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="5385b-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="5385b-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="5385b-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5385b-116">Not supported.</span></span>|
|<span data-ttu-id="5385b-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="5385b-117">Application</span></span>|<span data-ttu-id="5385b-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5385b-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="5385b-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="5385b-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/groupAssignments/{deviceConfigurationGroupAssignmentId}/deviceConfiguration
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsDomainJoinConfiguration/networkAccessConfigurations/{deviceConfigurationId}
```

## <a name="request-headers"></a><span data-ttu-id="5385b-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="5385b-120">Request headers</span></span>
|<span data-ttu-id="5385b-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5385b-121">Header</span></span>|<span data-ttu-id="5385b-122">Valor</span><span class="sxs-lookup"><span data-stu-id="5385b-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="5385b-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="5385b-123">Authorization</span></span>|<span data-ttu-id="5385b-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="5385b-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="5385b-125">Accept</span><span class="sxs-lookup"><span data-stu-id="5385b-125">Accept</span></span>|<span data-ttu-id="5385b-126">application/json</span><span class="sxs-lookup"><span data-stu-id="5385b-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="5385b-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="5385b-127">Request body</span></span>
<span data-ttu-id="5385b-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto [windows81GeneralConfiguration](../resources/intune-deviceconfig-windows81generalconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="5385b-128">In the request body, supply a JSON representation for the [windows81GeneralConfiguration](../resources/intune-deviceconfig-windows81generalconfiguration.md) object.</span></span>

<span data-ttu-id="5385b-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [windows81GeneralConfiguration](../resources/intune-deviceconfig-windows81generalconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="5385b-129">The following table shows the properties that are required when you create the [windows81GeneralConfiguration](../resources/intune-deviceconfig-windows81generalconfiguration.md).</span></span>

|<span data-ttu-id="5385b-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="5385b-130">Property</span></span>|<span data-ttu-id="5385b-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="5385b-131">Type</span></span>|<span data-ttu-id="5385b-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="5385b-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="5385b-133">id</span><span class="sxs-lookup"><span data-stu-id="5385b-133">id</span></span>|<span data-ttu-id="5385b-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="5385b-134">String</span></span>|<span data-ttu-id="5385b-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="5385b-135">Key of the entity.</span></span> <span data-ttu-id="5385b-136">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="5385b-136">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="5385b-137">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="5385b-137">lastModifiedDateTime</span></span>|<span data-ttu-id="5385b-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="5385b-138">DateTimeOffset</span></span>|<span data-ttu-id="5385b-139">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="5385b-139">DateTime the object was last modified.</span></span> <span data-ttu-id="5385b-140">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="5385b-140">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="5385b-141">roleScopeTagIds</span><span class="sxs-lookup"><span data-stu-id="5385b-141">roleScopeTagIds</span></span>|<span data-ttu-id="5385b-142">Colección String</span><span class="sxs-lookup"><span data-stu-id="5385b-142">String collection</span></span>|<span data-ttu-id="5385b-143">Lista de etiquetas de ámbito para esta instancia de entidad.</span><span class="sxs-lookup"><span data-stu-id="5385b-143">List of Scope Tags for this Entity instance.</span></span> <span data-ttu-id="5385b-144">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="5385b-144">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="5385b-145">supportsScopeTags</span><span class="sxs-lookup"><span data-stu-id="5385b-145">supportsScopeTags</span></span>|<span data-ttu-id="5385b-146">Booleano</span><span class="sxs-lookup"><span data-stu-id="5385b-146">Boolean</span></span>|<span data-ttu-id="5385b-147">Indica si la configuración del dispositivo subyacente admite la asignación de etiquetas de ámbito.</span><span class="sxs-lookup"><span data-stu-id="5385b-147">Indicates whether or not the underlying Device Configuration supports the assignment of scope tags.</span></span> <span data-ttu-id="5385b-148">No se permite la asignación a la propiedad ScopeTags cuando este valor es false y entidades no estará visibles para los usuarios con ámbito.</span><span class="sxs-lookup"><span data-stu-id="5385b-148">Assigning to the ScopeTags property is not allowed when this value is false and entities will not be visible to scoped users.</span></span> <span data-ttu-id="5385b-149">Esto se produce para las directivas de heredado creadas en Silverlight y se puede resolver por eliminar y volver a crear la directiva en el Portal de Azure.</span><span class="sxs-lookup"><span data-stu-id="5385b-149">This occurs for Legacy policies created in Silverlight and can be resolved by deleting and recreating the policy in the Azure Portal.</span></span> <span data-ttu-id="5385b-150">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="5385b-150">This property is read-only.</span></span> <span data-ttu-id="5385b-151">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="5385b-151">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="5385b-152">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="5385b-152">createdDateTime</span></span>|<span data-ttu-id="5385b-153">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="5385b-153">DateTimeOffset</span></span>|<span data-ttu-id="5385b-154">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="5385b-154">DateTime the object was created.</span></span> <span data-ttu-id="5385b-155">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="5385b-155">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="5385b-156">descripción</span><span class="sxs-lookup"><span data-stu-id="5385b-156">description</span></span>|<span data-ttu-id="5385b-157">Cadena</span><span class="sxs-lookup"><span data-stu-id="5385b-157">String</span></span>|<span data-ttu-id="5385b-158">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5385b-158">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="5385b-159">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="5385b-159">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="5385b-160">displayName</span><span class="sxs-lookup"><span data-stu-id="5385b-160">displayName</span></span>|<span data-ttu-id="5385b-161">Cadena</span><span class="sxs-lookup"><span data-stu-id="5385b-161">String</span></span>|<span data-ttu-id="5385b-162">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5385b-162">Admin provided name of the device configuration.</span></span> <span data-ttu-id="5385b-163">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="5385b-163">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="5385b-164">version</span><span class="sxs-lookup"><span data-stu-id="5385b-164">version</span></span>|<span data-ttu-id="5385b-165">Int32</span><span class="sxs-lookup"><span data-stu-id="5385b-165">Int32</span></span>|<span data-ttu-id="5385b-166">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5385b-166">Version of the device configuration.</span></span> <span data-ttu-id="5385b-167">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="5385b-167">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="5385b-168">accountsBlockAddingNonMicrosoftAccountEmail</span><span class="sxs-lookup"><span data-stu-id="5385b-168">accountsBlockAddingNonMicrosoftAccountEmail</span></span>|<span data-ttu-id="5385b-169">Booleano</span><span class="sxs-lookup"><span data-stu-id="5385b-169">Boolean</span></span>|<span data-ttu-id="5385b-170">Indica si se va a impedir que el usuario agregue cuentas de correo electrónico en el dispositivo que no están asociadas a una cuenta de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="5385b-170">Indicates whether or not to Block the user from adding email accounts to the device that are not associated with a Microsoft account.</span></span>|
|<span data-ttu-id="5385b-171">applyOnlyToWindows81</span><span class="sxs-lookup"><span data-stu-id="5385b-171">applyOnlyToWindows81</span></span>|<span data-ttu-id="5385b-172">Booleano</span><span class="sxs-lookup"><span data-stu-id="5385b-172">Boolean</span></span>|<span data-ttu-id="5385b-173">Valor que indica si esta directiva se aplica solo a Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="5385b-173">Value indicating whether this policy only applies to Windows 8.1.</span></span> <span data-ttu-id="5385b-174">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="5385b-174">This property is read-only.</span></span>|
|<span data-ttu-id="5385b-175">browserBlockAutofill</span><span class="sxs-lookup"><span data-stu-id="5385b-175">browserBlockAutofill</span></span>|<span data-ttu-id="5385b-176">Booleano</span><span class="sxs-lookup"><span data-stu-id="5385b-176">Boolean</span></span>|<span data-ttu-id="5385b-177">Indica si se va a bloquear el autorrelleno.</span><span class="sxs-lookup"><span data-stu-id="5385b-177">Indicates whether or not to block auto fill.</span></span>|
|<span data-ttu-id="5385b-178">browserBlockAutomaticDetectionOfIntranetSites</span><span class="sxs-lookup"><span data-stu-id="5385b-178">browserBlockAutomaticDetectionOfIntranetSites</span></span>|<span data-ttu-id="5385b-179">Booleano</span><span class="sxs-lookup"><span data-stu-id="5385b-179">Boolean</span></span>|<span data-ttu-id="5385b-180">Indica si se va a bloquear la detección automática de sitios de intranet.</span><span class="sxs-lookup"><span data-stu-id="5385b-180">Indicates whether or not to block automatic detection of Intranet sites.</span></span>|
|<span data-ttu-id="5385b-181">browserBlockEnterpriseModeAccess</span><span class="sxs-lookup"><span data-stu-id="5385b-181">browserBlockEnterpriseModeAccess</span></span>|<span data-ttu-id="5385b-182">Booleano</span><span class="sxs-lookup"><span data-stu-id="5385b-182">Boolean</span></span>|<span data-ttu-id="5385b-183">Indica si se va a bloquear el acceso al modo de empresa.</span><span class="sxs-lookup"><span data-stu-id="5385b-183">Indicates whether or not to block enterprise mode access.</span></span>|
|<span data-ttu-id="5385b-184">browserBlockJavaScript</span><span class="sxs-lookup"><span data-stu-id="5385b-184">browserBlockJavaScript</span></span>|<span data-ttu-id="5385b-185">Booleano</span><span class="sxs-lookup"><span data-stu-id="5385b-185">Boolean</span></span>|<span data-ttu-id="5385b-186">Indica si se va a impedir que el usuario utilice JavaScript.</span><span class="sxs-lookup"><span data-stu-id="5385b-186">Indicates whether or not to Block the user from using JavaScript.</span></span>|
|<span data-ttu-id="5385b-187">browserBlockPlugins</span><span class="sxs-lookup"><span data-stu-id="5385b-187">browserBlockPlugins</span></span>|<span data-ttu-id="5385b-188">Booleano</span><span class="sxs-lookup"><span data-stu-id="5385b-188">Boolean</span></span>|<span data-ttu-id="5385b-189">Indica si se van a bloquear los complementos.</span><span class="sxs-lookup"><span data-stu-id="5385b-189">Indicates whether or not to block plug-ins.</span></span>|
|<span data-ttu-id="5385b-190">browserBlockPopups</span><span class="sxs-lookup"><span data-stu-id="5385b-190">browserBlockPopups</span></span>|<span data-ttu-id="5385b-191">Booleano</span><span class="sxs-lookup"><span data-stu-id="5385b-191">Boolean</span></span>|<span data-ttu-id="5385b-192">Indica si se van a bloquear los elementos emergentes.</span><span class="sxs-lookup"><span data-stu-id="5385b-192">Indicates whether or not to block popups.</span></span>|
|<span data-ttu-id="5385b-193">browserBlockSendingDoNotTrackHeader</span><span class="sxs-lookup"><span data-stu-id="5385b-193">browserBlockSendingDoNotTrackHeader</span></span>|<span data-ttu-id="5385b-194">Booleano</span><span class="sxs-lookup"><span data-stu-id="5385b-194">Boolean</span></span>|<span data-ttu-id="5385b-195">Indica si se va a impedir que el usuario envíe el encabezado Do Not Track.</span><span class="sxs-lookup"><span data-stu-id="5385b-195">Indicates whether or not to Block the user from sending the do not track header.</span></span>|
|<span data-ttu-id="5385b-196">browserBlockSingleWordEntryOnIntranetSites</span><span class="sxs-lookup"><span data-stu-id="5385b-196">browserBlockSingleWordEntryOnIntranetSites</span></span>|<span data-ttu-id="5385b-197">Booleano</span><span class="sxs-lookup"><span data-stu-id="5385b-197">Boolean</span></span>|<span data-ttu-id="5385b-198">Indica si se va a bloquear la entrada de palabra única en sitios de intranet.</span><span class="sxs-lookup"><span data-stu-id="5385b-198">Indicates whether or not to block a single word entry on Intranet sites.</span></span>|
|<span data-ttu-id="5385b-199">browserRequireSmartScreen</span><span class="sxs-lookup"><span data-stu-id="5385b-199">browserRequireSmartScreen</span></span>|<span data-ttu-id="5385b-200">Booleano</span><span class="sxs-lookup"><span data-stu-id="5385b-200">Boolean</span></span>|<span data-ttu-id="5385b-201">Indica si se va a requerir que el usuario use el filtro de pantalla inteligente.</span><span class="sxs-lookup"><span data-stu-id="5385b-201">Indicates whether or not to require the user to use the smart screen filter.</span></span>|
|<span data-ttu-id="5385b-202">browserEnterpriseModeSiteListLocation</span><span class="sxs-lookup"><span data-stu-id="5385b-202">browserEnterpriseModeSiteListLocation</span></span>|<span data-ttu-id="5385b-203">Cadena</span><span class="sxs-lookup"><span data-stu-id="5385b-203">String</span></span>|<span data-ttu-id="5385b-204">Ubicación de la lista de sitios del modo de empresa.</span><span class="sxs-lookup"><span data-stu-id="5385b-204">The enterprise mode site list location.</span></span> <span data-ttu-id="5385b-205">Puede ser un archivo local, la red local o la ubicación http.</span><span class="sxs-lookup"><span data-stu-id="5385b-205">Could be a local file, local network or http location.</span></span>|
|<span data-ttu-id="5385b-206">browserInternetSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="5385b-206">browserInternetSecurityLevel</span></span>|[<span data-ttu-id="5385b-207">internetSiteSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="5385b-207">internetSiteSecurityLevel</span></span>](../resources/intune-deviceconfig-internetsitesecuritylevel.md)|<span data-ttu-id="5385b-208">Nivel de seguridad de Internet.</span><span class="sxs-lookup"><span data-stu-id="5385b-208">The internet security level.</span></span> <span data-ttu-id="5385b-209">Los valores posibles son: `userDefined`, `medium`, `mediumHigh` y `high`.</span><span class="sxs-lookup"><span data-stu-id="5385b-209">Possible values are: `userDefined`, `medium`, `mediumHigh`, `high`.</span></span>|
|<span data-ttu-id="5385b-210">browserIntranetSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="5385b-210">browserIntranetSecurityLevel</span></span>|[<span data-ttu-id="5385b-211">siteSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="5385b-211">siteSecurityLevel</span></span>](../resources/intune-deviceconfig-sitesecuritylevel.md)|<span data-ttu-id="5385b-212">Nivel de seguridad de la intranet.</span><span class="sxs-lookup"><span data-stu-id="5385b-212">The Intranet security level.</span></span> <span data-ttu-id="5385b-213">Los valores posibles son: `userDefined`, `low`, `mediumLow`, `medium`, `mediumHigh` y `high`.</span><span class="sxs-lookup"><span data-stu-id="5385b-213">Possible values are: `userDefined`, `low`, `mediumLow`, `medium`, `mediumHigh`, `high`.</span></span>|
|<span data-ttu-id="5385b-214">browserLoggingReportLocation</span><span class="sxs-lookup"><span data-stu-id="5385b-214">browserLoggingReportLocation</span></span>|<span data-ttu-id="5385b-215">Cadena</span><span class="sxs-lookup"><span data-stu-id="5385b-215">String</span></span>|<span data-ttu-id="5385b-216">Ubicación del informe de registro.</span><span class="sxs-lookup"><span data-stu-id="5385b-216">The logging report location.</span></span>|
|<span data-ttu-id="5385b-217">browserRequireHighSecurityForRestrictedSites</span><span class="sxs-lookup"><span data-stu-id="5385b-217">browserRequireHighSecurityForRestrictedSites</span></span>|<span data-ttu-id="5385b-218">Booleano</span><span class="sxs-lookup"><span data-stu-id="5385b-218">Boolean</span></span>|<span data-ttu-id="5385b-219">Indica si se va a requerir alta seguridad para los sitios restringidos.</span><span class="sxs-lookup"><span data-stu-id="5385b-219">Indicates whether or not to require high security for restricted sites.</span></span>|
|<span data-ttu-id="5385b-220">browserRequireFirewall</span><span class="sxs-lookup"><span data-stu-id="5385b-220">browserRequireFirewall</span></span>|<span data-ttu-id="5385b-221">Booleano</span><span class="sxs-lookup"><span data-stu-id="5385b-221">Boolean</span></span>|<span data-ttu-id="5385b-222">Indica si se va a requerir un firewall.</span><span class="sxs-lookup"><span data-stu-id="5385b-222">Indicates whether or not to require a firewall.</span></span>|
|<span data-ttu-id="5385b-223">browserRequireFraudWarning</span><span class="sxs-lookup"><span data-stu-id="5385b-223">browserRequireFraudWarning</span></span>|<span data-ttu-id="5385b-224">Booleano</span><span class="sxs-lookup"><span data-stu-id="5385b-224">Boolean</span></span>|<span data-ttu-id="5385b-225">Indica si se va a requerir una advertencia de fraude.</span><span class="sxs-lookup"><span data-stu-id="5385b-225">Indicates whether or not to require fraud warning.</span></span>|
|<span data-ttu-id="5385b-226">browserTrustedSitesSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="5385b-226">browserTrustedSitesSecurityLevel</span></span>|[<span data-ttu-id="5385b-227">siteSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="5385b-227">siteSecurityLevel</span></span>](../resources/intune-deviceconfig-sitesecuritylevel.md)|<span data-ttu-id="5385b-228">Nivel de seguridad de los sitios de confianza.</span><span class="sxs-lookup"><span data-stu-id="5385b-228">The trusted sites security level.</span></span> <span data-ttu-id="5385b-229">Los valores posibles son: `userDefined`, `low`, `mediumLow`, `medium`, `mediumHigh` y `high`.</span><span class="sxs-lookup"><span data-stu-id="5385b-229">Possible values are: `userDefined`, `low`, `mediumLow`, `medium`, `mediumHigh`, `high`.</span></span>|
|<span data-ttu-id="5385b-230">cellularBlockDataRoaming</span><span class="sxs-lookup"><span data-stu-id="5385b-230">cellularBlockDataRoaming</span></span>|<span data-ttu-id="5385b-231">Booleano</span><span class="sxs-lookup"><span data-stu-id="5385b-231">Boolean</span></span>|<span data-ttu-id="5385b-232">Indica si se va a bloquear la itinerancia de datos.</span><span class="sxs-lookup"><span data-stu-id="5385b-232">Indicates whether or not to block data roaming.</span></span>|
|<span data-ttu-id="5385b-233">diagnosticsBlockDataSubmission</span><span class="sxs-lookup"><span data-stu-id="5385b-233">diagnosticsBlockDataSubmission</span></span>|<span data-ttu-id="5385b-234">Booleano</span><span class="sxs-lookup"><span data-stu-id="5385b-234">Boolean</span></span>|<span data-ttu-id="5385b-235">Indica si se va a bloquear el envío de datos de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="5385b-235">Indicates whether or not to block diagnostic data submission.</span></span>|
|<span data-ttu-id="5385b-236">passwordBlockPicturePasswordAndPin</span><span class="sxs-lookup"><span data-stu-id="5385b-236">passwordBlockPicturePasswordAndPin</span></span>|<span data-ttu-id="5385b-237">Booleano</span><span class="sxs-lookup"><span data-stu-id="5385b-237">Boolean</span></span>|<span data-ttu-id="5385b-238">Indica si se va a impedir que el usuario utilice una contraseña de imágenes y un PIN.</span><span class="sxs-lookup"><span data-stu-id="5385b-238">Indicates whether or not to Block the user from using a pictures password and pin.</span></span>|
|<span data-ttu-id="5385b-239">passwordExpirationDays</span><span class="sxs-lookup"><span data-stu-id="5385b-239">passwordExpirationDays</span></span>|<span data-ttu-id="5385b-240">Int32</span><span class="sxs-lookup"><span data-stu-id="5385b-240">Int32</span></span>|<span data-ttu-id="5385b-241">Expiración de la contraseña en días.</span><span class="sxs-lookup"><span data-stu-id="5385b-241">Password expiration in days.</span></span>|
|<span data-ttu-id="5385b-242">passwordMinimumLength</span><span class="sxs-lookup"><span data-stu-id="5385b-242">passwordMinimumLength</span></span>|<span data-ttu-id="5385b-243">Int32</span><span class="sxs-lookup"><span data-stu-id="5385b-243">Int32</span></span>|<span data-ttu-id="5385b-244">La longitud mínima de contraseña.</span><span class="sxs-lookup"><span data-stu-id="5385b-244">The minimum password length.</span></span>|
|<span data-ttu-id="5385b-245">passwordMinutesOfInactivityBeforeScreenTimeout</span><span class="sxs-lookup"><span data-stu-id="5385b-245">passwordMinutesOfInactivityBeforeScreenTimeout</span></span>|<span data-ttu-id="5385b-246">Int32</span><span class="sxs-lookup"><span data-stu-id="5385b-246">Int32</span></span>|<span data-ttu-id="5385b-247">Minutos de inactividad antes de que se agote el tiempo de espera de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="5385b-247">The minutes of inactivity before the screen times out.</span></span>|
|<span data-ttu-id="5385b-248">passwordMinimumCharacterSetCount</span><span class="sxs-lookup"><span data-stu-id="5385b-248">passwordMinimumCharacterSetCount</span></span>|<span data-ttu-id="5385b-249">Int32</span><span class="sxs-lookup"><span data-stu-id="5385b-249">Int32</span></span>|<span data-ttu-id="5385b-250">Número de juegos de caracteres necesarios en la contraseña.</span><span class="sxs-lookup"><span data-stu-id="5385b-250">The number of character sets required in the password.</span></span>|
|<span data-ttu-id="5385b-251">passwordPreviousPasswordBlockCount</span><span class="sxs-lookup"><span data-stu-id="5385b-251">passwordPreviousPasswordBlockCount</span></span>|<span data-ttu-id="5385b-252">Int32</span><span class="sxs-lookup"><span data-stu-id="5385b-252">Int32</span></span>|<span data-ttu-id="5385b-253">Número de contraseñas anteriores que impide su reutilización.</span><span class="sxs-lookup"><span data-stu-id="5385b-253">The number of previous passwords to prevent re-use of.</span></span> <span data-ttu-id="5385b-254">Valores válidos de 0 a 24</span><span class="sxs-lookup"><span data-stu-id="5385b-254">Valid values 0 to 24</span></span>|
|<span data-ttu-id="5385b-255">passwordRequiredType</span><span class="sxs-lookup"><span data-stu-id="5385b-255">passwordRequiredType</span></span>|[<span data-ttu-id="5385b-256">requiredPasswordType</span><span class="sxs-lookup"><span data-stu-id="5385b-256">requiredPasswordType</span></span>](../resources/intune-deviceconfig-requiredpasswordtype.md)|<span data-ttu-id="5385b-257">Tipo de contraseña necesaria.</span><span class="sxs-lookup"><span data-stu-id="5385b-257">The required password type.</span></span> <span data-ttu-id="5385b-258">Los valores posibles son: `deviceDefault`, `alphanumeric` y `numeric`.</span><span class="sxs-lookup"><span data-stu-id="5385b-258">Possible values are: `deviceDefault`, `alphanumeric`, `numeric`.</span></span>|
|<span data-ttu-id="5385b-259">passwordSignInFailureCountBeforeFactoryReset</span><span class="sxs-lookup"><span data-stu-id="5385b-259">passwordSignInFailureCountBeforeFactoryReset</span></span>|<span data-ttu-id="5385b-260">Int32</span><span class="sxs-lookup"><span data-stu-id="5385b-260">Int32</span></span>|<span data-ttu-id="5385b-261">Número de errores de inicio de sesión permitidos antes del restablecimiento de fábrica.</span><span class="sxs-lookup"><span data-stu-id="5385b-261">The number of sign in failures before factory reset.</span></span>|
|<span data-ttu-id="5385b-262">storageRequireDeviceEncryption</span><span class="sxs-lookup"><span data-stu-id="5385b-262">storageRequireDeviceEncryption</span></span>|<span data-ttu-id="5385b-263">Booleano</span><span class="sxs-lookup"><span data-stu-id="5385b-263">Boolean</span></span>|<span data-ttu-id="5385b-264">Indica si se va a requerir el cifrado en un dispositivo móvil.</span><span class="sxs-lookup"><span data-stu-id="5385b-264">Indicates whether or not to require encryption on a mobile device.</span></span>|
|<span data-ttu-id="5385b-265">minimumAutoInstallClassification</span><span class="sxs-lookup"><span data-stu-id="5385b-265">minimumAutoInstallClassification</span></span>|[<span data-ttu-id="5385b-266">updateClassification</span><span class="sxs-lookup"><span data-stu-id="5385b-266">updateClassification</span></span>](../resources/intune-deviceconfig-updateclassification.md)|<span data-ttu-id="5385b-267">El requisito mínimo Actualizar clasificación para instalar automáticamente.</span><span class="sxs-lookup"><span data-stu-id="5385b-267">The minimum update classification to install automatically.</span></span> <span data-ttu-id="5385b-268">Los valores posibles son: `userDefined`, `recommendedAndImportant`, `important` y `none`.</span><span class="sxs-lookup"><span data-stu-id="5385b-268">Possible values are: `userDefined`, `recommendedAndImportant`, `important`, `none`.</span></span>|
|<span data-ttu-id="5385b-269">updatesMinimumAutoInstallClassification</span><span class="sxs-lookup"><span data-stu-id="5385b-269">updatesMinimumAutoInstallClassification</span></span>|[<span data-ttu-id="5385b-270">updateClassification</span><span class="sxs-lookup"><span data-stu-id="5385b-270">updateClassification</span></span>](../resources/intune-deviceconfig-updateclassification.md)|<span data-ttu-id="5385b-271">El requisito mínimo Actualizar clasificación para instalar automáticamente.</span><span class="sxs-lookup"><span data-stu-id="5385b-271">The minimum update classification to install automatically.</span></span> <span data-ttu-id="5385b-272">Los valores posibles son: `userDefined`, `recommendedAndImportant`, `important` y `none`.</span><span class="sxs-lookup"><span data-stu-id="5385b-272">Possible values are: `userDefined`, `recommendedAndImportant`, `important`, `none`.</span></span>|
|<span data-ttu-id="5385b-273">updatesRequireAutomaticUpdates</span><span class="sxs-lookup"><span data-stu-id="5385b-273">updatesRequireAutomaticUpdates</span></span>|<span data-ttu-id="5385b-274">Booleano</span><span class="sxs-lookup"><span data-stu-id="5385b-274">Boolean</span></span>|<span data-ttu-id="5385b-275">Indica si se van a requerir las actualizaciones automáticas.</span><span class="sxs-lookup"><span data-stu-id="5385b-275">Indicates whether or not to require automatic updates.</span></span>|
|<span data-ttu-id="5385b-276">userAccountControlSettings</span><span class="sxs-lookup"><span data-stu-id="5385b-276">userAccountControlSettings</span></span>|[<span data-ttu-id="5385b-277">windowsUserAccountControlSettings</span><span class="sxs-lookup"><span data-stu-id="5385b-277">windowsUserAccountControlSettings</span></span>](../resources/intune-deviceconfig-windowsuseraccountcontrolsettings.md)|<span data-ttu-id="5385b-278">Configuración de control de la cuenta de usuario.</span><span class="sxs-lookup"><span data-stu-id="5385b-278">The user account control settings.</span></span> <span data-ttu-id="5385b-279">Los valores posibles son: `userDefined`, `alwaysNotify`, `notifyOnAppChanges`, `notifyOnAppChangesWithoutDimming` y `neverNotify`.</span><span class="sxs-lookup"><span data-stu-id="5385b-279">Possible values are: `userDefined`, `alwaysNotify`, `notifyOnAppChanges`, `notifyOnAppChangesWithoutDimming`, `neverNotify`.</span></span>|
|<span data-ttu-id="5385b-280">workFoldersUrl</span><span class="sxs-lookup"><span data-stu-id="5385b-280">workFoldersUrl</span></span>|<span data-ttu-id="5385b-281">Cadena</span><span class="sxs-lookup"><span data-stu-id="5385b-281">String</span></span>|<span data-ttu-id="5385b-282">Dirección URL de las carpetas de trabajo.</span><span class="sxs-lookup"><span data-stu-id="5385b-282">The work folders url.</span></span>|



## <a name="response"></a><span data-ttu-id="5385b-283">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5385b-283">Response</span></span>
<span data-ttu-id="5385b-284">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [windows81GeneralConfiguration](../resources/intune-deviceconfig-windows81generalconfiguration.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5385b-284">If successful, this method returns a `200 OK` response code and an updated [windows81GeneralConfiguration](../resources/intune-deviceconfig-windows81generalconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="5385b-285">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="5385b-285">Example</span></span>
### <a name="request"></a><span data-ttu-id="5385b-286">Solicitud</span><span class="sxs-lookup"><span data-stu-id="5385b-286">Request</span></span>
<span data-ttu-id="5385b-287">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="5385b-287">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations/{deviceConfigurationId}
Content-type: application/json
Content-length: 1920

{
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "roleScopeTagIds": [
    "Role Scope Tag Ids value"
  ],
  "supportsScopeTags": true,
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "accountsBlockAddingNonMicrosoftAccountEmail": true,
  "applyOnlyToWindows81": true,
  "browserBlockAutofill": true,
  "browserBlockAutomaticDetectionOfIntranetSites": true,
  "browserBlockEnterpriseModeAccess": true,
  "browserBlockJavaScript": true,
  "browserBlockPlugins": true,
  "browserBlockPopups": true,
  "browserBlockSendingDoNotTrackHeader": true,
  "browserBlockSingleWordEntryOnIntranetSites": true,
  "browserRequireSmartScreen": true,
  "browserEnterpriseModeSiteListLocation": "Browser Enterprise Mode Site List Location value",
  "browserInternetSecurityLevel": "medium",
  "browserIntranetSecurityLevel": "low",
  "browserLoggingReportLocation": "Browser Logging Report Location value",
  "browserRequireHighSecurityForRestrictedSites": true,
  "browserRequireFirewall": true,
  "browserRequireFraudWarning": true,
  "browserTrustedSitesSecurityLevel": "low",
  "cellularBlockDataRoaming": true,
  "diagnosticsBlockDataSubmission": true,
  "passwordBlockPicturePasswordAndPin": true,
  "passwordExpirationDays": 6,
  "passwordMinimumLength": 5,
  "passwordMinutesOfInactivityBeforeScreenTimeout": 14,
  "passwordMinimumCharacterSetCount": 0,
  "passwordPreviousPasswordBlockCount": 2,
  "passwordRequiredType": "alphanumeric",
  "passwordSignInFailureCountBeforeFactoryReset": 12,
  "storageRequireDeviceEncryption": true,
  "minimumAutoInstallClassification": "recommendedAndImportant",
  "updatesMinimumAutoInstallClassification": "recommendedAndImportant",
  "updatesRequireAutomaticUpdates": true,
  "userAccountControlSettings": "alwaysNotify",
  "workFoldersUrl": "https://example.com/workFoldersUrl/"
}
```

### <a name="response"></a><span data-ttu-id="5385b-288">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5385b-288">Response</span></span>
<span data-ttu-id="5385b-p121">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="5385b-p121">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 2096

{
  "@odata.type": "#microsoft.graph.windows81GeneralConfiguration",
  "id": "0e9285b5-85b5-0e92-b585-920eb585920e",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "roleScopeTagIds": [
    "Role Scope Tag Ids value"
  ],
  "supportsScopeTags": true,
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "accountsBlockAddingNonMicrosoftAccountEmail": true,
  "applyOnlyToWindows81": true,
  "browserBlockAutofill": true,
  "browserBlockAutomaticDetectionOfIntranetSites": true,
  "browserBlockEnterpriseModeAccess": true,
  "browserBlockJavaScript": true,
  "browserBlockPlugins": true,
  "browserBlockPopups": true,
  "browserBlockSendingDoNotTrackHeader": true,
  "browserBlockSingleWordEntryOnIntranetSites": true,
  "browserRequireSmartScreen": true,
  "browserEnterpriseModeSiteListLocation": "Browser Enterprise Mode Site List Location value",
  "browserInternetSecurityLevel": "medium",
  "browserIntranetSecurityLevel": "low",
  "browserLoggingReportLocation": "Browser Logging Report Location value",
  "browserRequireHighSecurityForRestrictedSites": true,
  "browserRequireFirewall": true,
  "browserRequireFraudWarning": true,
  "browserTrustedSitesSecurityLevel": "low",
  "cellularBlockDataRoaming": true,
  "diagnosticsBlockDataSubmission": true,
  "passwordBlockPicturePasswordAndPin": true,
  "passwordExpirationDays": 6,
  "passwordMinimumLength": 5,
  "passwordMinutesOfInactivityBeforeScreenTimeout": 14,
  "passwordMinimumCharacterSetCount": 0,
  "passwordPreviousPasswordBlockCount": 2,
  "passwordRequiredType": "alphanumeric",
  "passwordSignInFailureCountBeforeFactoryReset": 12,
  "storageRequireDeviceEncryption": true,
  "minimumAutoInstallClassification": "recommendedAndImportant",
  "updatesMinimumAutoInstallClassification": "recommendedAndImportant",
  "updatesRequireAutomaticUpdates": true,
  "userAccountControlSettings": "alwaysNotify",
  "workFoldersUrl": "https://example.com/workFoldersUrl/"
}
```





