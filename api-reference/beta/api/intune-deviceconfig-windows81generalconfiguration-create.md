---
title: Crear windows81GeneralConfiguration
description: Crear un objeto windows81GeneralConfiguration.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 486b21ac0e420188dac738f9c8c2e53c78dbe30d
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27863865"
---
# <a name="create-windows81generalconfiguration"></a><span data-ttu-id="a5890-103">Crear windows81GeneralConfiguration</span><span class="sxs-lookup"><span data-stu-id="a5890-103">Create windows81GeneralConfiguration</span></span>

> <span data-ttu-id="a5890-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="a5890-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="a5890-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="a5890-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="a5890-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="a5890-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="a5890-107">Crear un objeto [windows81GeneralConfiguration](../resources/intune-deviceconfig-windows81generalconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="a5890-107">Create a new [windows81GeneralConfiguration](../resources/intune-deviceconfig-windows81generalconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="a5890-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="a5890-108">Prerequisites</span></span>
<span data-ttu-id="a5890-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="a5890-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="a5890-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a5890-111">Permission type</span></span>|<span data-ttu-id="a5890-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a5890-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="a5890-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a5890-113">Delegated (work or school account)</span></span>|<span data-ttu-id="a5890-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="a5890-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="a5890-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a5890-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="a5890-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a5890-116">Not supported.</span></span>|
|<span data-ttu-id="a5890-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a5890-117">Application</span></span>|<span data-ttu-id="a5890-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a5890-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="a5890-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a5890-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceConfigurations
POST /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsDomainJoinConfiguration/networkAccessConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="a5890-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a5890-120">Request headers</span></span>
|<span data-ttu-id="a5890-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a5890-121">Header</span></span>|<span data-ttu-id="a5890-122">Valor</span><span class="sxs-lookup"><span data-stu-id="a5890-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="a5890-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="a5890-123">Authorization</span></span>|<span data-ttu-id="a5890-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="a5890-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="a5890-125">Accept</span><span class="sxs-lookup"><span data-stu-id="a5890-125">Accept</span></span>|<span data-ttu-id="a5890-126">application/json</span><span class="sxs-lookup"><span data-stu-id="a5890-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="a5890-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a5890-127">Request body</span></span>
<span data-ttu-id="a5890-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto windows81GeneralConfiguration.</span><span class="sxs-lookup"><span data-stu-id="a5890-128">In the request body, supply a JSON representation for the windows81GeneralConfiguration object.</span></span>

<span data-ttu-id="a5890-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto windows81GeneralConfiguration.</span><span class="sxs-lookup"><span data-stu-id="a5890-129">The following table shows the properties that are required when you create the windows81GeneralConfiguration.</span></span>

|<span data-ttu-id="a5890-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a5890-130">Property</span></span>|<span data-ttu-id="a5890-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="a5890-131">Type</span></span>|<span data-ttu-id="a5890-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="a5890-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="a5890-133">id</span><span class="sxs-lookup"><span data-stu-id="a5890-133">id</span></span>|<span data-ttu-id="a5890-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="a5890-134">String</span></span>|<span data-ttu-id="a5890-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="a5890-135">Key of the entity.</span></span> <span data-ttu-id="a5890-136">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="a5890-136">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="a5890-137">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="a5890-137">lastModifiedDateTime</span></span>|<span data-ttu-id="a5890-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="a5890-138">DateTimeOffset</span></span>|<span data-ttu-id="a5890-139">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="a5890-139">DateTime the object was last modified.</span></span> <span data-ttu-id="a5890-140">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="a5890-140">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="a5890-141">roleScopeTagIds</span><span class="sxs-lookup"><span data-stu-id="a5890-141">roleScopeTagIds</span></span>|<span data-ttu-id="a5890-142">Colección String</span><span class="sxs-lookup"><span data-stu-id="a5890-142">String collection</span></span>|<span data-ttu-id="a5890-143">Lista de etiquetas de ámbito para esta instancia de entidad.</span><span class="sxs-lookup"><span data-stu-id="a5890-143">List of Scope Tags for this Entity instance.</span></span> <span data-ttu-id="a5890-144">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="a5890-144">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="a5890-145">supportsScopeTags</span><span class="sxs-lookup"><span data-stu-id="a5890-145">supportsScopeTags</span></span>|<span data-ttu-id="a5890-146">Booleano</span><span class="sxs-lookup"><span data-stu-id="a5890-146">Boolean</span></span>|<span data-ttu-id="a5890-147">Indica si la configuración del dispositivo subyacente admite la asignación de etiquetas de ámbito.</span><span class="sxs-lookup"><span data-stu-id="a5890-147">Indicates whether or not the underlying Device Configuration supports the assignment of scope tags.</span></span> <span data-ttu-id="a5890-148">No se permite la asignación a la propiedad ScopeTags cuando este valor es false y entidades no estará visibles para los usuarios con ámbito.</span><span class="sxs-lookup"><span data-stu-id="a5890-148">Assigning to the ScopeTags property is not allowed when this value is false and entities will not be visible to scoped users.</span></span> <span data-ttu-id="a5890-149">Esto se produce para las directivas de heredado creadas en Silverlight y se puede resolver por eliminar y volver a crear la directiva en el Portal de Azure.</span><span class="sxs-lookup"><span data-stu-id="a5890-149">This occurs for Legacy policies created in Silverlight and can be resolved by deleting and recreating the policy in the Azure Portal.</span></span> <span data-ttu-id="a5890-150">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="a5890-150">This property is read-only.</span></span> <span data-ttu-id="a5890-151">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="a5890-151">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="a5890-152">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="a5890-152">createdDateTime</span></span>|<span data-ttu-id="a5890-153">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="a5890-153">DateTimeOffset</span></span>|<span data-ttu-id="a5890-154">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="a5890-154">DateTime the object was created.</span></span> <span data-ttu-id="a5890-155">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="a5890-155">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="a5890-156">descripción</span><span class="sxs-lookup"><span data-stu-id="a5890-156">description</span></span>|<span data-ttu-id="a5890-157">Cadena</span><span class="sxs-lookup"><span data-stu-id="a5890-157">String</span></span>|<span data-ttu-id="a5890-158">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a5890-158">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="a5890-159">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="a5890-159">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="a5890-160">displayName</span><span class="sxs-lookup"><span data-stu-id="a5890-160">displayName</span></span>|<span data-ttu-id="a5890-161">Cadena</span><span class="sxs-lookup"><span data-stu-id="a5890-161">String</span></span>|<span data-ttu-id="a5890-162">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a5890-162">Admin provided name of the device configuration.</span></span> <span data-ttu-id="a5890-163">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="a5890-163">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="a5890-164">version</span><span class="sxs-lookup"><span data-stu-id="a5890-164">version</span></span>|<span data-ttu-id="a5890-165">Int32</span><span class="sxs-lookup"><span data-stu-id="a5890-165">Int32</span></span>|<span data-ttu-id="a5890-166">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a5890-166">Version of the device configuration.</span></span> <span data-ttu-id="a5890-167">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="a5890-167">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="a5890-168">accountsBlockAddingNonMicrosoftAccountEmail</span><span class="sxs-lookup"><span data-stu-id="a5890-168">accountsBlockAddingNonMicrosoftAccountEmail</span></span>|<span data-ttu-id="a5890-169">Booleano</span><span class="sxs-lookup"><span data-stu-id="a5890-169">Boolean</span></span>|<span data-ttu-id="a5890-170">Indica si se va a impedir que el usuario agregue cuentas de correo electrónico en el dispositivo que no están asociadas a una cuenta de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="a5890-170">Indicates whether or not to Block the user from adding email accounts to the device that are not associated with a Microsoft account.</span></span>|
|<span data-ttu-id="a5890-171">applyOnlyToWindows81</span><span class="sxs-lookup"><span data-stu-id="a5890-171">applyOnlyToWindows81</span></span>|<span data-ttu-id="a5890-172">Booleano</span><span class="sxs-lookup"><span data-stu-id="a5890-172">Boolean</span></span>|<span data-ttu-id="a5890-173">Valor que indica si esta directiva se aplica solo a Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="a5890-173">Value indicating whether this policy only applies to Windows 8.1.</span></span> <span data-ttu-id="a5890-174">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="a5890-174">This property is read-only.</span></span>|
|<span data-ttu-id="a5890-175">browserBlockAutofill</span><span class="sxs-lookup"><span data-stu-id="a5890-175">browserBlockAutofill</span></span>|<span data-ttu-id="a5890-176">Booleano</span><span class="sxs-lookup"><span data-stu-id="a5890-176">Boolean</span></span>|<span data-ttu-id="a5890-177">Indica si se va a bloquear el autorrelleno.</span><span class="sxs-lookup"><span data-stu-id="a5890-177">Indicates whether or not to block auto fill.</span></span>|
|<span data-ttu-id="a5890-178">browserBlockAutomaticDetectionOfIntranetSites</span><span class="sxs-lookup"><span data-stu-id="a5890-178">browserBlockAutomaticDetectionOfIntranetSites</span></span>|<span data-ttu-id="a5890-179">Booleano</span><span class="sxs-lookup"><span data-stu-id="a5890-179">Boolean</span></span>|<span data-ttu-id="a5890-180">Indica si se va a bloquear la detección automática de sitios de intranet.</span><span class="sxs-lookup"><span data-stu-id="a5890-180">Indicates whether or not to block automatic detection of Intranet sites.</span></span>|
|<span data-ttu-id="a5890-181">browserBlockEnterpriseModeAccess</span><span class="sxs-lookup"><span data-stu-id="a5890-181">browserBlockEnterpriseModeAccess</span></span>|<span data-ttu-id="a5890-182">Booleano</span><span class="sxs-lookup"><span data-stu-id="a5890-182">Boolean</span></span>|<span data-ttu-id="a5890-183">Indica si se va a bloquear el acceso al modo de empresa.</span><span class="sxs-lookup"><span data-stu-id="a5890-183">Indicates whether or not to block enterprise mode access.</span></span>|
|<span data-ttu-id="a5890-184">browserBlockJavaScript</span><span class="sxs-lookup"><span data-stu-id="a5890-184">browserBlockJavaScript</span></span>|<span data-ttu-id="a5890-185">Booleano</span><span class="sxs-lookup"><span data-stu-id="a5890-185">Boolean</span></span>|<span data-ttu-id="a5890-186">Indica si se va a impedir que el usuario utilice JavaScript.</span><span class="sxs-lookup"><span data-stu-id="a5890-186">Indicates whether or not to Block the user from using JavaScript.</span></span>|
|<span data-ttu-id="a5890-187">browserBlockPlugins</span><span class="sxs-lookup"><span data-stu-id="a5890-187">browserBlockPlugins</span></span>|<span data-ttu-id="a5890-188">Booleano</span><span class="sxs-lookup"><span data-stu-id="a5890-188">Boolean</span></span>|<span data-ttu-id="a5890-189">Indica si se van a bloquear los complementos.</span><span class="sxs-lookup"><span data-stu-id="a5890-189">Indicates whether or not to block plug-ins.</span></span>|
|<span data-ttu-id="a5890-190">browserBlockPopups</span><span class="sxs-lookup"><span data-stu-id="a5890-190">browserBlockPopups</span></span>|<span data-ttu-id="a5890-191">Booleano</span><span class="sxs-lookup"><span data-stu-id="a5890-191">Boolean</span></span>|<span data-ttu-id="a5890-192">Indica si se van a bloquear los elementos emergentes.</span><span class="sxs-lookup"><span data-stu-id="a5890-192">Indicates whether or not to block popups.</span></span>|
|<span data-ttu-id="a5890-193">browserBlockSendingDoNotTrackHeader</span><span class="sxs-lookup"><span data-stu-id="a5890-193">browserBlockSendingDoNotTrackHeader</span></span>|<span data-ttu-id="a5890-194">Booleano</span><span class="sxs-lookup"><span data-stu-id="a5890-194">Boolean</span></span>|<span data-ttu-id="a5890-195">Indica si se va a impedir que el usuario envíe el encabezado Do Not Track.</span><span class="sxs-lookup"><span data-stu-id="a5890-195">Indicates whether or not to Block the user from sending the do not track header.</span></span>|
|<span data-ttu-id="a5890-196">browserBlockSingleWordEntryOnIntranetSites</span><span class="sxs-lookup"><span data-stu-id="a5890-196">browserBlockSingleWordEntryOnIntranetSites</span></span>|<span data-ttu-id="a5890-197">Booleano</span><span class="sxs-lookup"><span data-stu-id="a5890-197">Boolean</span></span>|<span data-ttu-id="a5890-198">Indica si se va a bloquear la entrada de palabra única en sitios de intranet.</span><span class="sxs-lookup"><span data-stu-id="a5890-198">Indicates whether or not to block a single word entry on Intranet sites.</span></span>|
|<span data-ttu-id="a5890-199">browserRequireSmartScreen</span><span class="sxs-lookup"><span data-stu-id="a5890-199">browserRequireSmartScreen</span></span>|<span data-ttu-id="a5890-200">Booleano</span><span class="sxs-lookup"><span data-stu-id="a5890-200">Boolean</span></span>|<span data-ttu-id="a5890-201">Indica si se va a requerir que el usuario use el filtro de pantalla inteligente.</span><span class="sxs-lookup"><span data-stu-id="a5890-201">Indicates whether or not to require the user to use the smart screen filter.</span></span>|
|<span data-ttu-id="a5890-202">browserEnterpriseModeSiteListLocation</span><span class="sxs-lookup"><span data-stu-id="a5890-202">browserEnterpriseModeSiteListLocation</span></span>|<span data-ttu-id="a5890-203">Cadena</span><span class="sxs-lookup"><span data-stu-id="a5890-203">String</span></span>|<span data-ttu-id="a5890-204">Ubicación de la lista de sitios del modo de empresa.</span><span class="sxs-lookup"><span data-stu-id="a5890-204">The enterprise mode site list location.</span></span> <span data-ttu-id="a5890-205">Puede ser un archivo local, la red local o la ubicación http.</span><span class="sxs-lookup"><span data-stu-id="a5890-205">Could be a local file, local network or http location.</span></span>|
|<span data-ttu-id="a5890-206">browserInternetSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="a5890-206">browserInternetSecurityLevel</span></span>|[<span data-ttu-id="a5890-207">internetSiteSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="a5890-207">internetSiteSecurityLevel</span></span>](../resources/intune-deviceconfig-internetsitesecuritylevel.md)|<span data-ttu-id="a5890-208">Nivel de seguridad de Internet.</span><span class="sxs-lookup"><span data-stu-id="a5890-208">The internet security level.</span></span> <span data-ttu-id="a5890-209">Los valores posibles son: `userDefined`, `medium`, `mediumHigh` y `high`.</span><span class="sxs-lookup"><span data-stu-id="a5890-209">Possible values are: `userDefined`, `medium`, `mediumHigh`, `high`.</span></span>|
|<span data-ttu-id="a5890-210">browserIntranetSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="a5890-210">browserIntranetSecurityLevel</span></span>|[<span data-ttu-id="a5890-211">siteSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="a5890-211">siteSecurityLevel</span></span>](../resources/intune-deviceconfig-sitesecuritylevel.md)|<span data-ttu-id="a5890-212">Nivel de seguridad de la intranet.</span><span class="sxs-lookup"><span data-stu-id="a5890-212">The Intranet security level.</span></span> <span data-ttu-id="a5890-213">Los valores posibles son: `userDefined`, `low`, `mediumLow`, `medium`, `mediumHigh` y `high`.</span><span class="sxs-lookup"><span data-stu-id="a5890-213">Possible values are: `userDefined`, `low`, `mediumLow`, `medium`, `mediumHigh`, `high`.</span></span>|
|<span data-ttu-id="a5890-214">browserLoggingReportLocation</span><span class="sxs-lookup"><span data-stu-id="a5890-214">browserLoggingReportLocation</span></span>|<span data-ttu-id="a5890-215">Cadena</span><span class="sxs-lookup"><span data-stu-id="a5890-215">String</span></span>|<span data-ttu-id="a5890-216">Ubicación del informe de registro.</span><span class="sxs-lookup"><span data-stu-id="a5890-216">The logging report location.</span></span>|
|<span data-ttu-id="a5890-217">browserRequireHighSecurityForRestrictedSites</span><span class="sxs-lookup"><span data-stu-id="a5890-217">browserRequireHighSecurityForRestrictedSites</span></span>|<span data-ttu-id="a5890-218">Booleano</span><span class="sxs-lookup"><span data-stu-id="a5890-218">Boolean</span></span>|<span data-ttu-id="a5890-219">Indica si se va a requerir alta seguridad para los sitios restringidos.</span><span class="sxs-lookup"><span data-stu-id="a5890-219">Indicates whether or not to require high security for restricted sites.</span></span>|
|<span data-ttu-id="a5890-220">browserRequireFirewall</span><span class="sxs-lookup"><span data-stu-id="a5890-220">browserRequireFirewall</span></span>|<span data-ttu-id="a5890-221">Booleano</span><span class="sxs-lookup"><span data-stu-id="a5890-221">Boolean</span></span>|<span data-ttu-id="a5890-222">Indica si se va a requerir un firewall.</span><span class="sxs-lookup"><span data-stu-id="a5890-222">Indicates whether or not to require a firewall.</span></span>|
|<span data-ttu-id="a5890-223">browserRequireFraudWarning</span><span class="sxs-lookup"><span data-stu-id="a5890-223">browserRequireFraudWarning</span></span>|<span data-ttu-id="a5890-224">Booleano</span><span class="sxs-lookup"><span data-stu-id="a5890-224">Boolean</span></span>|<span data-ttu-id="a5890-225">Indica si se va a requerir una advertencia de fraude.</span><span class="sxs-lookup"><span data-stu-id="a5890-225">Indicates whether or not to require fraud warning.</span></span>|
|<span data-ttu-id="a5890-226">browserTrustedSitesSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="a5890-226">browserTrustedSitesSecurityLevel</span></span>|[<span data-ttu-id="a5890-227">siteSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="a5890-227">siteSecurityLevel</span></span>](../resources/intune-deviceconfig-sitesecuritylevel.md)|<span data-ttu-id="a5890-228">Nivel de seguridad de los sitios de confianza.</span><span class="sxs-lookup"><span data-stu-id="a5890-228">The trusted sites security level.</span></span> <span data-ttu-id="a5890-229">Los valores posibles son: `userDefined`, `low`, `mediumLow`, `medium`, `mediumHigh` y `high`.</span><span class="sxs-lookup"><span data-stu-id="a5890-229">Possible values are: `userDefined`, `low`, `mediumLow`, `medium`, `mediumHigh`, `high`.</span></span>|
|<span data-ttu-id="a5890-230">cellularBlockDataRoaming</span><span class="sxs-lookup"><span data-stu-id="a5890-230">cellularBlockDataRoaming</span></span>|<span data-ttu-id="a5890-231">Booleano</span><span class="sxs-lookup"><span data-stu-id="a5890-231">Boolean</span></span>|<span data-ttu-id="a5890-232">Indica si se va a bloquear la itinerancia de datos.</span><span class="sxs-lookup"><span data-stu-id="a5890-232">Indicates whether or not to block data roaming.</span></span>|
|<span data-ttu-id="a5890-233">diagnosticsBlockDataSubmission</span><span class="sxs-lookup"><span data-stu-id="a5890-233">diagnosticsBlockDataSubmission</span></span>|<span data-ttu-id="a5890-234">Booleano</span><span class="sxs-lookup"><span data-stu-id="a5890-234">Boolean</span></span>|<span data-ttu-id="a5890-235">Indica si se va a bloquear el envío de datos de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="a5890-235">Indicates whether or not to block diagnostic data submission.</span></span>|
|<span data-ttu-id="a5890-236">passwordBlockPicturePasswordAndPin</span><span class="sxs-lookup"><span data-stu-id="a5890-236">passwordBlockPicturePasswordAndPin</span></span>|<span data-ttu-id="a5890-237">Booleano</span><span class="sxs-lookup"><span data-stu-id="a5890-237">Boolean</span></span>|<span data-ttu-id="a5890-238">Indica si se va a impedir que el usuario utilice una contraseña de imágenes y un PIN.</span><span class="sxs-lookup"><span data-stu-id="a5890-238">Indicates whether or not to Block the user from using a pictures password and pin.</span></span>|
|<span data-ttu-id="a5890-239">passwordExpirationDays</span><span class="sxs-lookup"><span data-stu-id="a5890-239">passwordExpirationDays</span></span>|<span data-ttu-id="a5890-240">Int32</span><span class="sxs-lookup"><span data-stu-id="a5890-240">Int32</span></span>|<span data-ttu-id="a5890-241">Expiración de la contraseña en días.</span><span class="sxs-lookup"><span data-stu-id="a5890-241">Password expiration in days.</span></span>|
|<span data-ttu-id="a5890-242">passwordMinimumLength</span><span class="sxs-lookup"><span data-stu-id="a5890-242">passwordMinimumLength</span></span>|<span data-ttu-id="a5890-243">Int32</span><span class="sxs-lookup"><span data-stu-id="a5890-243">Int32</span></span>|<span data-ttu-id="a5890-244">La longitud mínima de contraseña.</span><span class="sxs-lookup"><span data-stu-id="a5890-244">The minimum password length.</span></span>|
|<span data-ttu-id="a5890-245">passwordMinutesOfInactivityBeforeScreenTimeout</span><span class="sxs-lookup"><span data-stu-id="a5890-245">passwordMinutesOfInactivityBeforeScreenTimeout</span></span>|<span data-ttu-id="a5890-246">Int32</span><span class="sxs-lookup"><span data-stu-id="a5890-246">Int32</span></span>|<span data-ttu-id="a5890-247">Minutos de inactividad antes de que se agote el tiempo de espera de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="a5890-247">The minutes of inactivity before the screen times out.</span></span>|
|<span data-ttu-id="a5890-248">passwordMinimumCharacterSetCount</span><span class="sxs-lookup"><span data-stu-id="a5890-248">passwordMinimumCharacterSetCount</span></span>|<span data-ttu-id="a5890-249">Int32</span><span class="sxs-lookup"><span data-stu-id="a5890-249">Int32</span></span>|<span data-ttu-id="a5890-250">Número de juegos de caracteres necesarios en la contraseña.</span><span class="sxs-lookup"><span data-stu-id="a5890-250">The number of character sets required in the password.</span></span>|
|<span data-ttu-id="a5890-251">passwordPreviousPasswordBlockCount</span><span class="sxs-lookup"><span data-stu-id="a5890-251">passwordPreviousPasswordBlockCount</span></span>|<span data-ttu-id="a5890-252">Int32</span><span class="sxs-lookup"><span data-stu-id="a5890-252">Int32</span></span>|<span data-ttu-id="a5890-253">Número de contraseñas anteriores que impide su reutilización.</span><span class="sxs-lookup"><span data-stu-id="a5890-253">The number of previous passwords to prevent re-use of.</span></span> <span data-ttu-id="a5890-254">Valores válidos de 0 a 24</span><span class="sxs-lookup"><span data-stu-id="a5890-254">Valid values 0 to 24</span></span>|
|<span data-ttu-id="a5890-255">passwordRequiredType</span><span class="sxs-lookup"><span data-stu-id="a5890-255">passwordRequiredType</span></span>|[<span data-ttu-id="a5890-256">requiredPasswordType</span><span class="sxs-lookup"><span data-stu-id="a5890-256">requiredPasswordType</span></span>](../resources/intune-deviceconfig-requiredpasswordtype.md)|<span data-ttu-id="a5890-257">Tipo de contraseña necesaria.</span><span class="sxs-lookup"><span data-stu-id="a5890-257">The required password type.</span></span> <span data-ttu-id="a5890-258">Los valores posibles son: `deviceDefault`, `alphanumeric` y `numeric`.</span><span class="sxs-lookup"><span data-stu-id="a5890-258">Possible values are: `deviceDefault`, `alphanumeric`, `numeric`.</span></span>|
|<span data-ttu-id="a5890-259">passwordSignInFailureCountBeforeFactoryReset</span><span class="sxs-lookup"><span data-stu-id="a5890-259">passwordSignInFailureCountBeforeFactoryReset</span></span>|<span data-ttu-id="a5890-260">Int32</span><span class="sxs-lookup"><span data-stu-id="a5890-260">Int32</span></span>|<span data-ttu-id="a5890-261">Número de errores de inicio de sesión permitidos antes del restablecimiento de fábrica.</span><span class="sxs-lookup"><span data-stu-id="a5890-261">The number of sign in failures before factory reset.</span></span>|
|<span data-ttu-id="a5890-262">storageRequireDeviceEncryption</span><span class="sxs-lookup"><span data-stu-id="a5890-262">storageRequireDeviceEncryption</span></span>|<span data-ttu-id="a5890-263">Booleano</span><span class="sxs-lookup"><span data-stu-id="a5890-263">Boolean</span></span>|<span data-ttu-id="a5890-264">Indica si se va a requerir el cifrado en un dispositivo móvil.</span><span class="sxs-lookup"><span data-stu-id="a5890-264">Indicates whether or not to require encryption on a mobile device.</span></span>|
|<span data-ttu-id="a5890-265">minimumAutoInstallClassification</span><span class="sxs-lookup"><span data-stu-id="a5890-265">minimumAutoInstallClassification</span></span>|[<span data-ttu-id="a5890-266">updateClassification</span><span class="sxs-lookup"><span data-stu-id="a5890-266">updateClassification</span></span>](../resources/intune-deviceconfig-updateclassification.md)|<span data-ttu-id="a5890-267">El requisito mínimo Actualizar clasificación para instalar automáticamente.</span><span class="sxs-lookup"><span data-stu-id="a5890-267">The minimum update classification to install automatically.</span></span> <span data-ttu-id="a5890-268">Los valores posibles son: `userDefined`, `recommendedAndImportant`, `important` y `none`.</span><span class="sxs-lookup"><span data-stu-id="a5890-268">Possible values are: `userDefined`, `recommendedAndImportant`, `important`, `none`.</span></span>|
|<span data-ttu-id="a5890-269">updatesMinimumAutoInstallClassification</span><span class="sxs-lookup"><span data-stu-id="a5890-269">updatesMinimumAutoInstallClassification</span></span>|[<span data-ttu-id="a5890-270">updateClassification</span><span class="sxs-lookup"><span data-stu-id="a5890-270">updateClassification</span></span>](../resources/intune-deviceconfig-updateclassification.md)|<span data-ttu-id="a5890-271">El requisito mínimo Actualizar clasificación para instalar automáticamente.</span><span class="sxs-lookup"><span data-stu-id="a5890-271">The minimum update classification to install automatically.</span></span> <span data-ttu-id="a5890-272">Los valores posibles son: `userDefined`, `recommendedAndImportant`, `important` y `none`.</span><span class="sxs-lookup"><span data-stu-id="a5890-272">Possible values are: `userDefined`, `recommendedAndImportant`, `important`, `none`.</span></span>|
|<span data-ttu-id="a5890-273">updatesRequireAutomaticUpdates</span><span class="sxs-lookup"><span data-stu-id="a5890-273">updatesRequireAutomaticUpdates</span></span>|<span data-ttu-id="a5890-274">Booleano</span><span class="sxs-lookup"><span data-stu-id="a5890-274">Boolean</span></span>|<span data-ttu-id="a5890-275">Indica si se van a requerir las actualizaciones automáticas.</span><span class="sxs-lookup"><span data-stu-id="a5890-275">Indicates whether or not to require automatic updates.</span></span>|
|<span data-ttu-id="a5890-276">userAccountControlSettings</span><span class="sxs-lookup"><span data-stu-id="a5890-276">userAccountControlSettings</span></span>|[<span data-ttu-id="a5890-277">windowsUserAccountControlSettings</span><span class="sxs-lookup"><span data-stu-id="a5890-277">windowsUserAccountControlSettings</span></span>](../resources/intune-deviceconfig-windowsuseraccountcontrolsettings.md)|<span data-ttu-id="a5890-278">Configuración de control de la cuenta de usuario.</span><span class="sxs-lookup"><span data-stu-id="a5890-278">The user account control settings.</span></span> <span data-ttu-id="a5890-279">Los valores posibles son: `userDefined`, `alwaysNotify`, `notifyOnAppChanges`, `notifyOnAppChangesWithoutDimming` y `neverNotify`.</span><span class="sxs-lookup"><span data-stu-id="a5890-279">Possible values are: `userDefined`, `alwaysNotify`, `notifyOnAppChanges`, `notifyOnAppChangesWithoutDimming`, `neverNotify`.</span></span>|
|<span data-ttu-id="a5890-280">workFoldersUrl</span><span class="sxs-lookup"><span data-stu-id="a5890-280">workFoldersUrl</span></span>|<span data-ttu-id="a5890-281">Cadena</span><span class="sxs-lookup"><span data-stu-id="a5890-281">String</span></span>|<span data-ttu-id="a5890-282">Dirección URL de las carpetas de trabajo.</span><span class="sxs-lookup"><span data-stu-id="a5890-282">The work folders url.</span></span>|



## <a name="response"></a><span data-ttu-id="a5890-283">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a5890-283">Response</span></span>
<span data-ttu-id="a5890-284">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [windows81GeneralConfiguration](../resources/intune-deviceconfig-windows81generalconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a5890-284">If successful, this method returns a `201 Created` response code and a [windows81GeneralConfiguration](../resources/intune-deviceconfig-windows81generalconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="a5890-285">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a5890-285">Example</span></span>
### <a name="request"></a><span data-ttu-id="a5890-286">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a5890-286">Request</span></span>
<span data-ttu-id="a5890-287">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a5890-287">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations
Content-type: application/json
Content-length: 1988

{
  "@odata.type": "#microsoft.graph.windows81GeneralConfiguration",
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

### <a name="response"></a><span data-ttu-id="a5890-288">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a5890-288">Response</span></span>
<span data-ttu-id="a5890-p121">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="a5890-p121">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
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





