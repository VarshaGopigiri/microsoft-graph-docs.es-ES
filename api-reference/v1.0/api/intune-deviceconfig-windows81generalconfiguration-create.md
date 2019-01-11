---
title: Crear windows81GeneralConfiguration
description: Crear un objeto windows81GeneralConfiguration.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 30da5227531696056730ec184f9d0ce7881541aa
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27830971"
---
# <a name="create-windows81generalconfiguration"></a><span data-ttu-id="9cb21-103">Crear windows81GeneralConfiguration</span><span class="sxs-lookup"><span data-stu-id="9cb21-103">Create windows81GeneralConfiguration</span></span>

> <span data-ttu-id="9cb21-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="9cb21-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="9cb21-105">Crear un objeto [windows81GeneralConfiguration](../resources/intune-deviceconfig-windows81generalconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="9cb21-105">Create a new [windows81GeneralConfiguration](../resources/intune-deviceconfig-windows81generalconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="9cb21-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="9cb21-106">Prerequisites</span></span>
<span data-ttu-id="9cb21-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="9cb21-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="9cb21-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="9cb21-109">Permission type</span></span>|<span data-ttu-id="9cb21-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="9cb21-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="9cb21-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="9cb21-111">Delegated (work or school account)</span></span>|<span data-ttu-id="9cb21-112">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="9cb21-112">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="9cb21-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="9cb21-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="9cb21-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9cb21-114">Not supported.</span></span>|
|<span data-ttu-id="9cb21-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="9cb21-115">Application</span></span>|<span data-ttu-id="9cb21-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9cb21-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="9cb21-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="9cb21-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="9cb21-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="9cb21-118">Request headers</span></span>
|<span data-ttu-id="9cb21-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9cb21-119">Header</span></span>|<span data-ttu-id="9cb21-120">Valor</span><span class="sxs-lookup"><span data-stu-id="9cb21-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="9cb21-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="9cb21-121">Authorization</span></span>|<span data-ttu-id="9cb21-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="9cb21-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="9cb21-123">Accept</span><span class="sxs-lookup"><span data-stu-id="9cb21-123">Accept</span></span>|<span data-ttu-id="9cb21-124">application/json</span><span class="sxs-lookup"><span data-stu-id="9cb21-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="9cb21-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="9cb21-125">Request body</span></span>
<span data-ttu-id="9cb21-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto windows81GeneralConfiguration.</span><span class="sxs-lookup"><span data-stu-id="9cb21-126">In the request body, supply a JSON representation for the windows81GeneralConfiguration object.</span></span>

<span data-ttu-id="9cb21-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto windows81GeneralConfiguration.</span><span class="sxs-lookup"><span data-stu-id="9cb21-127">The following table shows the properties that are required when you create the windows81GeneralConfiguration.</span></span>

|<span data-ttu-id="9cb21-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="9cb21-128">Property</span></span>|<span data-ttu-id="9cb21-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="9cb21-129">Type</span></span>|<span data-ttu-id="9cb21-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="9cb21-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="9cb21-131">id</span><span class="sxs-lookup"><span data-stu-id="9cb21-131">id</span></span>|<span data-ttu-id="9cb21-132">Cadena</span><span class="sxs-lookup"><span data-stu-id="9cb21-132">String</span></span>|<span data-ttu-id="9cb21-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="9cb21-133">Key of the entity.</span></span> <span data-ttu-id="9cb21-134">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="9cb21-134">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="9cb21-135">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="9cb21-135">lastModifiedDateTime</span></span>|<span data-ttu-id="9cb21-136">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="9cb21-136">DateTimeOffset</span></span>|<span data-ttu-id="9cb21-137">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="9cb21-137">DateTime the object was last modified.</span></span> <span data-ttu-id="9cb21-138">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="9cb21-138">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="9cb21-139">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="9cb21-139">createdDateTime</span></span>|<span data-ttu-id="9cb21-140">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="9cb21-140">DateTimeOffset</span></span>|<span data-ttu-id="9cb21-141">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="9cb21-141">DateTime the object was created.</span></span> <span data-ttu-id="9cb21-142">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="9cb21-142">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="9cb21-143">descripción</span><span class="sxs-lookup"><span data-stu-id="9cb21-143">description</span></span>|<span data-ttu-id="9cb21-144">Cadena</span><span class="sxs-lookup"><span data-stu-id="9cb21-144">String</span></span>|<span data-ttu-id="9cb21-145">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9cb21-145">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="9cb21-146">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="9cb21-146">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="9cb21-147">displayName</span><span class="sxs-lookup"><span data-stu-id="9cb21-147">displayName</span></span>|<span data-ttu-id="9cb21-148">Cadena</span><span class="sxs-lookup"><span data-stu-id="9cb21-148">String</span></span>|<span data-ttu-id="9cb21-149">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9cb21-149">Admin provided name of the device configuration.</span></span> <span data-ttu-id="9cb21-150">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="9cb21-150">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="9cb21-151">version</span><span class="sxs-lookup"><span data-stu-id="9cb21-151">version</span></span>|<span data-ttu-id="9cb21-152">Int32</span><span class="sxs-lookup"><span data-stu-id="9cb21-152">Int32</span></span>|<span data-ttu-id="9cb21-153">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9cb21-153">Version of the device configuration.</span></span> <span data-ttu-id="9cb21-154">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="9cb21-154">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="9cb21-155">accountsBlockAddingNonMicrosoftAccountEmail</span><span class="sxs-lookup"><span data-stu-id="9cb21-155">accountsBlockAddingNonMicrosoftAccountEmail</span></span>|<span data-ttu-id="9cb21-156">Booleano</span><span class="sxs-lookup"><span data-stu-id="9cb21-156">Boolean</span></span>|<span data-ttu-id="9cb21-157">Indica si se va a impedir que el usuario agregue cuentas de correo electrónico en el dispositivo que no están asociadas a una cuenta de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="9cb21-157">Indicates whether or not to Block the user from adding email accounts to the device that are not associated with a Microsoft account.</span></span>|
|<span data-ttu-id="9cb21-158">applyOnlyToWindows81</span><span class="sxs-lookup"><span data-stu-id="9cb21-158">applyOnlyToWindows81</span></span>|<span data-ttu-id="9cb21-159">Booleano</span><span class="sxs-lookup"><span data-stu-id="9cb21-159">Boolean</span></span>|<span data-ttu-id="9cb21-160">Valor que indica si esta directiva se aplica solo a Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="9cb21-160">Value indicating whether this policy only applies to Windows 8.1.</span></span> <span data-ttu-id="9cb21-161">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="9cb21-161">This property is read-only.</span></span>|
|<span data-ttu-id="9cb21-162">browserBlockAutofill</span><span class="sxs-lookup"><span data-stu-id="9cb21-162">browserBlockAutofill</span></span>|<span data-ttu-id="9cb21-163">Booleano</span><span class="sxs-lookup"><span data-stu-id="9cb21-163">Boolean</span></span>|<span data-ttu-id="9cb21-164">Indica si se va a bloquear el autorrelleno.</span><span class="sxs-lookup"><span data-stu-id="9cb21-164">Indicates whether or not to block auto fill.</span></span>|
|<span data-ttu-id="9cb21-165">browserBlockAutomaticDetectionOfIntranetSites</span><span class="sxs-lookup"><span data-stu-id="9cb21-165">browserBlockAutomaticDetectionOfIntranetSites</span></span>|<span data-ttu-id="9cb21-166">Booleano</span><span class="sxs-lookup"><span data-stu-id="9cb21-166">Boolean</span></span>|<span data-ttu-id="9cb21-167">Indica si se va a bloquear la detección automática de sitios de intranet.</span><span class="sxs-lookup"><span data-stu-id="9cb21-167">Indicates whether or not to block automatic detection of Intranet sites.</span></span>|
|<span data-ttu-id="9cb21-168">browserBlockEnterpriseModeAccess</span><span class="sxs-lookup"><span data-stu-id="9cb21-168">browserBlockEnterpriseModeAccess</span></span>|<span data-ttu-id="9cb21-169">Booleano</span><span class="sxs-lookup"><span data-stu-id="9cb21-169">Boolean</span></span>|<span data-ttu-id="9cb21-170">Indica si se va a bloquear el acceso al modo de empresa.</span><span class="sxs-lookup"><span data-stu-id="9cb21-170">Indicates whether or not to block enterprise mode access.</span></span>|
|<span data-ttu-id="9cb21-171">browserBlockJavaScript</span><span class="sxs-lookup"><span data-stu-id="9cb21-171">browserBlockJavaScript</span></span>|<span data-ttu-id="9cb21-172">Booleano</span><span class="sxs-lookup"><span data-stu-id="9cb21-172">Boolean</span></span>|<span data-ttu-id="9cb21-173">Indica si se va a impedir que el usuario utilice JavaScript.</span><span class="sxs-lookup"><span data-stu-id="9cb21-173">Indicates whether or not to Block the user from using JavaScript.</span></span>|
|<span data-ttu-id="9cb21-174">browserBlockPlugins</span><span class="sxs-lookup"><span data-stu-id="9cb21-174">browserBlockPlugins</span></span>|<span data-ttu-id="9cb21-175">Booleano</span><span class="sxs-lookup"><span data-stu-id="9cb21-175">Boolean</span></span>|<span data-ttu-id="9cb21-176">Indica si se van a bloquear los complementos.</span><span class="sxs-lookup"><span data-stu-id="9cb21-176">Indicates whether or not to block plug-ins.</span></span>|
|<span data-ttu-id="9cb21-177">browserBlockPopups</span><span class="sxs-lookup"><span data-stu-id="9cb21-177">browserBlockPopups</span></span>|<span data-ttu-id="9cb21-178">Booleano</span><span class="sxs-lookup"><span data-stu-id="9cb21-178">Boolean</span></span>|<span data-ttu-id="9cb21-179">Indica si se van a bloquear los elementos emergentes.</span><span class="sxs-lookup"><span data-stu-id="9cb21-179">Indicates whether or not to block popups.</span></span>|
|<span data-ttu-id="9cb21-180">browserBlockSendingDoNotTrackHeader</span><span class="sxs-lookup"><span data-stu-id="9cb21-180">browserBlockSendingDoNotTrackHeader</span></span>|<span data-ttu-id="9cb21-181">Booleano</span><span class="sxs-lookup"><span data-stu-id="9cb21-181">Boolean</span></span>|<span data-ttu-id="9cb21-182">Indica si se va a impedir que el usuario envíe el encabezado Do Not Track.</span><span class="sxs-lookup"><span data-stu-id="9cb21-182">Indicates whether or not to Block the user from sending the do not track header.</span></span>|
|<span data-ttu-id="9cb21-183">browserBlockSingleWordEntryOnIntranetSites</span><span class="sxs-lookup"><span data-stu-id="9cb21-183">browserBlockSingleWordEntryOnIntranetSites</span></span>|<span data-ttu-id="9cb21-184">Booleano</span><span class="sxs-lookup"><span data-stu-id="9cb21-184">Boolean</span></span>|<span data-ttu-id="9cb21-185">Indica si se va a bloquear la entrada de palabra única en sitios de intranet.</span><span class="sxs-lookup"><span data-stu-id="9cb21-185">Indicates whether or not to block a single word entry on Intranet sites.</span></span>|
|<span data-ttu-id="9cb21-186">browserRequireSmartScreen</span><span class="sxs-lookup"><span data-stu-id="9cb21-186">browserRequireSmartScreen</span></span>|<span data-ttu-id="9cb21-187">Booleano</span><span class="sxs-lookup"><span data-stu-id="9cb21-187">Boolean</span></span>|<span data-ttu-id="9cb21-188">Indica si se va a requerir que el usuario use el filtro de pantalla inteligente.</span><span class="sxs-lookup"><span data-stu-id="9cb21-188">Indicates whether or not to require the user to use the smart screen filter.</span></span>|
|<span data-ttu-id="9cb21-189">browserEnterpriseModeSiteListLocation</span><span class="sxs-lookup"><span data-stu-id="9cb21-189">browserEnterpriseModeSiteListLocation</span></span>|<span data-ttu-id="9cb21-190">Cadena</span><span class="sxs-lookup"><span data-stu-id="9cb21-190">String</span></span>|<span data-ttu-id="9cb21-191">Ubicación de la lista de sitios del modo de empresa.</span><span class="sxs-lookup"><span data-stu-id="9cb21-191">The enterprise mode site list location.</span></span> <span data-ttu-id="9cb21-192">Puede ser un archivo local, la red local o la ubicación http.</span><span class="sxs-lookup"><span data-stu-id="9cb21-192">Could be a local file, local network or http location.</span></span>|
|<span data-ttu-id="9cb21-193">browserInternetSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="9cb21-193">browserInternetSecurityLevel</span></span>|[<span data-ttu-id="9cb21-194">internetSiteSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="9cb21-194">internetSiteSecurityLevel</span></span>](../resources/intune-deviceconfig-internetsitesecuritylevel.md)|<span data-ttu-id="9cb21-195">Nivel de seguridad de Internet.</span><span class="sxs-lookup"><span data-stu-id="9cb21-195">The internet security level.</span></span> <span data-ttu-id="9cb21-196">Los valores posibles son: `userDefined`, `medium`, `mediumHigh` y `high`.</span><span class="sxs-lookup"><span data-stu-id="9cb21-196">Possible values are: `userDefined`, `medium`, `mediumHigh`, `high`.</span></span>|
|<span data-ttu-id="9cb21-197">browserIntranetSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="9cb21-197">browserIntranetSecurityLevel</span></span>|[<span data-ttu-id="9cb21-198">siteSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="9cb21-198">siteSecurityLevel</span></span>](../resources/intune-deviceconfig-sitesecuritylevel.md)|<span data-ttu-id="9cb21-199">Nivel de seguridad de la intranet.</span><span class="sxs-lookup"><span data-stu-id="9cb21-199">The Intranet security level.</span></span> <span data-ttu-id="9cb21-200">Los valores posibles son: `userDefined`, `low`, `mediumLow`, `medium`, `mediumHigh` y `high`.</span><span class="sxs-lookup"><span data-stu-id="9cb21-200">Possible values are: `userDefined`, `low`, `mediumLow`, `medium`, `mediumHigh`, `high`.</span></span>|
|<span data-ttu-id="9cb21-201">browserLoggingReportLocation</span><span class="sxs-lookup"><span data-stu-id="9cb21-201">browserLoggingReportLocation</span></span>|<span data-ttu-id="9cb21-202">Cadena</span><span class="sxs-lookup"><span data-stu-id="9cb21-202">String</span></span>|<span data-ttu-id="9cb21-203">Ubicación del informe de registro.</span><span class="sxs-lookup"><span data-stu-id="9cb21-203">The logging report location.</span></span>|
|<span data-ttu-id="9cb21-204">browserRequireHighSecurityForRestrictedSites</span><span class="sxs-lookup"><span data-stu-id="9cb21-204">browserRequireHighSecurityForRestrictedSites</span></span>|<span data-ttu-id="9cb21-205">Booleano</span><span class="sxs-lookup"><span data-stu-id="9cb21-205">Boolean</span></span>|<span data-ttu-id="9cb21-206">Indica si se va a requerir alta seguridad para los sitios restringidos.</span><span class="sxs-lookup"><span data-stu-id="9cb21-206">Indicates whether or not to require high security for restricted sites.</span></span>|
|<span data-ttu-id="9cb21-207">browserRequireFirewall</span><span class="sxs-lookup"><span data-stu-id="9cb21-207">browserRequireFirewall</span></span>|<span data-ttu-id="9cb21-208">Booleano</span><span class="sxs-lookup"><span data-stu-id="9cb21-208">Boolean</span></span>|<span data-ttu-id="9cb21-209">Indica si se va a requerir un firewall.</span><span class="sxs-lookup"><span data-stu-id="9cb21-209">Indicates whether or not to require a firewall.</span></span>|
|<span data-ttu-id="9cb21-210">browserRequireFraudWarning</span><span class="sxs-lookup"><span data-stu-id="9cb21-210">browserRequireFraudWarning</span></span>|<span data-ttu-id="9cb21-211">Booleano</span><span class="sxs-lookup"><span data-stu-id="9cb21-211">Boolean</span></span>|<span data-ttu-id="9cb21-212">Indica si se va a requerir una advertencia de fraude.</span><span class="sxs-lookup"><span data-stu-id="9cb21-212">Indicates whether or not to require fraud warning.</span></span>|
|<span data-ttu-id="9cb21-213">browserTrustedSitesSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="9cb21-213">browserTrustedSitesSecurityLevel</span></span>|[<span data-ttu-id="9cb21-214">siteSecurityLevel</span><span class="sxs-lookup"><span data-stu-id="9cb21-214">siteSecurityLevel</span></span>](../resources/intune-deviceconfig-sitesecuritylevel.md)|<span data-ttu-id="9cb21-215">Nivel de seguridad de los sitios de confianza.</span><span class="sxs-lookup"><span data-stu-id="9cb21-215">The trusted sites security level.</span></span> <span data-ttu-id="9cb21-216">Los valores posibles son: `userDefined`, `low`, `mediumLow`, `medium`, `mediumHigh` y `high`.</span><span class="sxs-lookup"><span data-stu-id="9cb21-216">Possible values are: `userDefined`, `low`, `mediumLow`, `medium`, `mediumHigh`, `high`.</span></span>|
|<span data-ttu-id="9cb21-217">cellularBlockDataRoaming</span><span class="sxs-lookup"><span data-stu-id="9cb21-217">cellularBlockDataRoaming</span></span>|<span data-ttu-id="9cb21-218">Booleano</span><span class="sxs-lookup"><span data-stu-id="9cb21-218">Boolean</span></span>|<span data-ttu-id="9cb21-219">Indica si se va a bloquear la itinerancia de datos.</span><span class="sxs-lookup"><span data-stu-id="9cb21-219">Indicates whether or not to block data roaming.</span></span>|
|<span data-ttu-id="9cb21-220">diagnosticsBlockDataSubmission</span><span class="sxs-lookup"><span data-stu-id="9cb21-220">diagnosticsBlockDataSubmission</span></span>|<span data-ttu-id="9cb21-221">Booleano</span><span class="sxs-lookup"><span data-stu-id="9cb21-221">Boolean</span></span>|<span data-ttu-id="9cb21-222">Indica si se va a bloquear el envío de datos de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="9cb21-222">Indicates whether or not to block diagnostic data submission.</span></span>|
|<span data-ttu-id="9cb21-223">passwordBlockPicturePasswordAndPin</span><span class="sxs-lookup"><span data-stu-id="9cb21-223">passwordBlockPicturePasswordAndPin</span></span>|<span data-ttu-id="9cb21-224">Booleano</span><span class="sxs-lookup"><span data-stu-id="9cb21-224">Boolean</span></span>|<span data-ttu-id="9cb21-225">Indica si se va a impedir que el usuario utilice una contraseña de imágenes y un PIN.</span><span class="sxs-lookup"><span data-stu-id="9cb21-225">Indicates whether or not to Block the user from using a pictures password and pin.</span></span>|
|<span data-ttu-id="9cb21-226">passwordExpirationDays</span><span class="sxs-lookup"><span data-stu-id="9cb21-226">passwordExpirationDays</span></span>|<span data-ttu-id="9cb21-227">Int32</span><span class="sxs-lookup"><span data-stu-id="9cb21-227">Int32</span></span>|<span data-ttu-id="9cb21-228">Expiración de la contraseña en días.</span><span class="sxs-lookup"><span data-stu-id="9cb21-228">Password expiration in days.</span></span>|
|<span data-ttu-id="9cb21-229">passwordMinimumLength</span><span class="sxs-lookup"><span data-stu-id="9cb21-229">passwordMinimumLength</span></span>|<span data-ttu-id="9cb21-230">Int32</span><span class="sxs-lookup"><span data-stu-id="9cb21-230">Int32</span></span>|<span data-ttu-id="9cb21-231">La longitud mínima de contraseña.</span><span class="sxs-lookup"><span data-stu-id="9cb21-231">The minimum password length.</span></span>|
|<span data-ttu-id="9cb21-232">passwordMinutesOfInactivityBeforeScreenTimeout</span><span class="sxs-lookup"><span data-stu-id="9cb21-232">passwordMinutesOfInactivityBeforeScreenTimeout</span></span>|<span data-ttu-id="9cb21-233">Int32</span><span class="sxs-lookup"><span data-stu-id="9cb21-233">Int32</span></span>|<span data-ttu-id="9cb21-234">Minutos de inactividad antes de que se agote el tiempo de espera de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="9cb21-234">The minutes of inactivity before the screen times out.</span></span>|
|<span data-ttu-id="9cb21-235">passwordMinimumCharacterSetCount</span><span class="sxs-lookup"><span data-stu-id="9cb21-235">passwordMinimumCharacterSetCount</span></span>|<span data-ttu-id="9cb21-236">Int32</span><span class="sxs-lookup"><span data-stu-id="9cb21-236">Int32</span></span>|<span data-ttu-id="9cb21-237">Número de juegos de caracteres necesarios en la contraseña.</span><span class="sxs-lookup"><span data-stu-id="9cb21-237">The number of character sets required in the password.</span></span>|
|<span data-ttu-id="9cb21-238">passwordPreviousPasswordBlockCount</span><span class="sxs-lookup"><span data-stu-id="9cb21-238">passwordPreviousPasswordBlockCount</span></span>|<span data-ttu-id="9cb21-239">Int32</span><span class="sxs-lookup"><span data-stu-id="9cb21-239">Int32</span></span>|<span data-ttu-id="9cb21-240">Número de contraseñas anteriores que impide su reutilización.</span><span class="sxs-lookup"><span data-stu-id="9cb21-240">The number of previous passwords to prevent re-use of.</span></span> <span data-ttu-id="9cb21-241">Valores válidos de 0 a 24</span><span class="sxs-lookup"><span data-stu-id="9cb21-241">Valid values 0 to 24</span></span>|
|<span data-ttu-id="9cb21-242">passwordRequiredType</span><span class="sxs-lookup"><span data-stu-id="9cb21-242">passwordRequiredType</span></span>|[<span data-ttu-id="9cb21-243">requiredPasswordType</span><span class="sxs-lookup"><span data-stu-id="9cb21-243">requiredPasswordType</span></span>](../resources/intune-deviceconfig-requiredpasswordtype.md)|<span data-ttu-id="9cb21-244">Tipo de contraseña necesaria.</span><span class="sxs-lookup"><span data-stu-id="9cb21-244">The required password type.</span></span> <span data-ttu-id="9cb21-245">Los valores posibles son: `deviceDefault`, `alphanumeric` y `numeric`.</span><span class="sxs-lookup"><span data-stu-id="9cb21-245">Possible values are: `deviceDefault`, `alphanumeric`, `numeric`.</span></span>|
|<span data-ttu-id="9cb21-246">passwordSignInFailureCountBeforeFactoryReset</span><span class="sxs-lookup"><span data-stu-id="9cb21-246">passwordSignInFailureCountBeforeFactoryReset</span></span>|<span data-ttu-id="9cb21-247">Int32</span><span class="sxs-lookup"><span data-stu-id="9cb21-247">Int32</span></span>|<span data-ttu-id="9cb21-248">Número de errores de inicio de sesión permitidos antes del restablecimiento de fábrica.</span><span class="sxs-lookup"><span data-stu-id="9cb21-248">The number of sign in failures before factory reset.</span></span>|
|<span data-ttu-id="9cb21-249">storageRequireDeviceEncryption</span><span class="sxs-lookup"><span data-stu-id="9cb21-249">storageRequireDeviceEncryption</span></span>|<span data-ttu-id="9cb21-250">Booleano</span><span class="sxs-lookup"><span data-stu-id="9cb21-250">Boolean</span></span>|<span data-ttu-id="9cb21-251">Indica si se va a requerir el cifrado en un dispositivo móvil.</span><span class="sxs-lookup"><span data-stu-id="9cb21-251">Indicates whether or not to require encryption on a mobile device.</span></span>|
|<span data-ttu-id="9cb21-252">updatesRequireAutomaticUpdates</span><span class="sxs-lookup"><span data-stu-id="9cb21-252">updatesRequireAutomaticUpdates</span></span>|<span data-ttu-id="9cb21-253">Booleano</span><span class="sxs-lookup"><span data-stu-id="9cb21-253">Boolean</span></span>|<span data-ttu-id="9cb21-254">Indica si se van a requerir las actualizaciones automáticas.</span><span class="sxs-lookup"><span data-stu-id="9cb21-254">Indicates whether or not to require automatic updates.</span></span>|
|<span data-ttu-id="9cb21-255">userAccountControlSettings</span><span class="sxs-lookup"><span data-stu-id="9cb21-255">userAccountControlSettings</span></span>|[<span data-ttu-id="9cb21-256">windowsUserAccountControlSettings</span><span class="sxs-lookup"><span data-stu-id="9cb21-256">windowsUserAccountControlSettings</span></span>](../resources/intune-deviceconfig-windowsuseraccountcontrolsettings.md)|<span data-ttu-id="9cb21-257">Configuración de control de la cuenta de usuario.</span><span class="sxs-lookup"><span data-stu-id="9cb21-257">The user account control settings.</span></span> <span data-ttu-id="9cb21-258">Los valores posibles son: `userDefined`, `alwaysNotify`, `notifyOnAppChanges`, `notifyOnAppChangesWithoutDimming` y `neverNotify`.</span><span class="sxs-lookup"><span data-stu-id="9cb21-258">Possible values are: `userDefined`, `alwaysNotify`, `notifyOnAppChanges`, `notifyOnAppChangesWithoutDimming`, `neverNotify`.</span></span>|
|<span data-ttu-id="9cb21-259">workFoldersUrl</span><span class="sxs-lookup"><span data-stu-id="9cb21-259">workFoldersUrl</span></span>|<span data-ttu-id="9cb21-260">Cadena</span><span class="sxs-lookup"><span data-stu-id="9cb21-260">String</span></span>|<span data-ttu-id="9cb21-261">Dirección URL de las carpetas de trabajo.</span><span class="sxs-lookup"><span data-stu-id="9cb21-261">The work folders url.</span></span>|



## <a name="response"></a><span data-ttu-id="9cb21-262">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9cb21-262">Response</span></span>
<span data-ttu-id="9cb21-263">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [windows81GeneralConfiguration](../resources/intune-deviceconfig-windows81generalconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9cb21-263">If successful, this method returns a `201 Created` response code and a [windows81GeneralConfiguration](../resources/intune-deviceconfig-windows81generalconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="9cb21-264">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9cb21-264">Example</span></span>
### <a name="request"></a><span data-ttu-id="9cb21-265">Solicitud</span><span class="sxs-lookup"><span data-stu-id="9cb21-265">Request</span></span>
<span data-ttu-id="9cb21-266">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="9cb21-266">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceManagement/deviceConfigurations
Content-type: application/json
Content-length: 1693

{
  "@odata.type": "#microsoft.graph.windows81GeneralConfiguration",
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
  "updatesRequireAutomaticUpdates": true,
  "userAccountControlSettings": "alwaysNotify",
  "workFoldersUrl": "https://example.com/workFoldersUrl/"
}
```

### <a name="response"></a><span data-ttu-id="9cb21-267">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9cb21-267">Response</span></span>
<span data-ttu-id="9cb21-p116">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="9cb21-p116">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 1865

{
  "@odata.type": "#microsoft.graph.windows81GeneralConfiguration",
  "id": "0e9285b5-85b5-0e92-b585-920eb585920e",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
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
  "updatesRequireAutomaticUpdates": true,
  "userAccountControlSettings": "alwaysNotify",
  "workFoldersUrl": "https://example.com/workFoldersUrl/"
}
```



